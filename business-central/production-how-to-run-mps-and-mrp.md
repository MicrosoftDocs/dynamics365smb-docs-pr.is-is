---
title: 'Keyra fulla áætlunargerð, MPS eða MRP'
description: Áætlunarkerfið getur reiknað MPS og MRP samkvæmt beiðni eða reiknað bæði á sama tíma.
author: brentholtorf
ms.topic: conceptual
ms.search.form: '99000852, 99000860'
ms.date: 01/24/2024
ms.author: bholtorf
ms.reviewer: andreipa
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="run-full-planning-mps-or-mrp"></a>Keyra fulla áætlunargerð, MPS eða MRP

Skilmálarnir "sem keyra áætlunarvinnublaðið" eða "MRP" vísa til útreikninga á aðalframleiðsluáætlun og efnisþörfum. Útreikningurinn byggist á raunverulegri eftirspurn og spáðri eftirspurn. Áætlunarkerfið getur reiknað MPS og MRP samkvæmt beiðni eða reiknað bæði á sama tíma.  

- MPS er útreikningur á aðalframleiðsluáætlun byggt á raunverulegri eftirspurn og eftirspurnarspá. MPS-útreikningur er notaður fyrir lokavörur sem eru með spá eða sölupöntunarlínu. Þessar vörur eru kallaðar "MPS-vörur" og eru auðkenndar þegar útreikningur hefst.  
- MRP er útreikningur á efnisþörfum sem byggjast á raunverulegri eftirspurn eftir hlutum og eftirspurnarspá á hlutastigi. MRP er eingöngu reiknað fyrir vörur sem eru ekki MPS-vörur. Tilgangur MRP er að gera tímasettar áætlanir, vara, til að útvega viðeigandi vöru, á viðeigandi tíma, á viðeigandi stað og í viðeigandi magni.  

Áætlunarrök MPS og MRP eru eins. Reiknireglurnar tengjast nettóvinnslu, endurnýtingu fyrirliggjandi áfyllingarpantana og aðgerðarboðum. Áætlunarkerfisvinnslan skoðar hvað er, eða verður, þörf (eftirspurn) og hvað er til eða væntanlegt (framboð). Þegar magnið er nettó á móti hvoru öðru birtast [!INCLUDE[prod_short](includes/prod_short.md)]  aðgerðarboð. Aðgerðarboð eru tillögur um að stofna nýja pöntun, breyta pöntun (magni eða dagsetningu) eða hætta við pöntun. Hugtakið „pöntun“ inniber innkaupapantanir, samsetningarpöntun, framleiðslupantanir og millifærslupantanir.

Hægt er að rekja tenglana sem áætlunin stofnar á milli eftirspurnar og framboðs á síðunni **Rakning** pöntunar. Frekari upplýsingar eru í [Rekja tengsl á milli framboðs og eftirspurnar](production-how-track-demand-supply.md).

Viðundandi niðurstöður áætlunar byggjast á uppsetningu í birgðaspjöldum, samsetningaruppskriftum, framleiðsluuppskriftum og leiðum.  

## <a name="methods-for-generating-a-plan"></a>Aðferðir við gerð áætlunar

- **Reikna áætlun endurgerðar:** Vinnsla eða endurgera efnisáætlunina. Þessi vinnsla hefst á eyðingu allra áætlaðra birgðapantana sem eru hlaðnar. Allar vörur í gagnagrunninum eru enduráætlaðar.  
- **Reikna áætlun hreyfingar**: Vinna áætlun hreyfingar. Vörur eru teknar með í hreyfingaáætlun vegna tveggja breytinga:  
   - **Breytingar á eftirspurn/framboði:** Þessar breytingar fela í sér breytingar á magni í sölupöntunum, eftirspurnarspár, samsetningarpantanir, framleiðslupantanir eða innkaupapantanir. Óáætluð breyting á birgðastigi er einnig talin breyting á magni.  
   - **Breytingar á áætlunarfæribreytum:** Þessar breytingar fela í sér breytingar á öryggisbirgðum, endurpöntunarmarki, leið, uppskrift og breytingum á tímaramma eða útreikningi afhendingartíma.  
- **Sækja aðgerðarboð:** Þjónar sem skammtímaáætlunarverkfæri með því að gefa út aðgerðarboð til að gera viðvart um breytingar sem gerðar voru frá síðasta skipti sem endurgerðar- eða hreyfingaáætlun var reiknuð út.  

Með hverri áætlunaraðferð, myndar [!INCLUDE[prod_short](includes/prod_short.md)] vinnublaðafærslur þar sem gert er ráð fyrir óendanlegum afköstum. Afkastageta vinnustöðvar og vélastöðvar er ekki tekin með þegar áætlanir eru gerðar.  

> [!IMPORTANT]  
> Áætlunin Reikna út endurgerð er algengasta vinnsla. Hins vegar er hægt að nota Reikna áætlun og Framkvæma aðgerðarboð til að keyra ferlið Reikna áætlun hreyfingar.  
>
> Hægt er að keyra áætlun aðgerðarboða milli endurgerðar- og hreyfingaáætlunarkeyrslna til að fá skjóta yfirsýn yfir áhrif áætlanabreytinga. Hins vegar er ekki ætlunin að skipta út fullri endurgerðar- eða hreyfingaáætlunarferli.  

## <a name="to-calculate-the-planning-worksheet"></a>Til að reikna áætlunarvinnublað:
  
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Áætlunarvinnublað** og velja síðan viðkomandi tengil.  
2. Velja **Reikna áætlun endurgerðar** aðgerðina til að opna síðuna **Reikna áætlun**.  
3. Á flýtiflipanum **Valkostir** skal fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Heimildasamstæða|  
    |---------------------------------|---------------------------------------|  
    |**MPS**|Reikna út aðalframleiðsluáætlun. Atriði sem eru með opnum sölupöntunum eða eftirspurnarspám eru talin í þessari keyrslu. <br/>Ef önnur eftirspurn, til dæmis öryggisbirgðir, endurpöntunarmark eða opnar framleiðsluíhlutalínur, eru einnig til fyrir slíkar vörur er þessi eftirspurn innifalin í MPS-útreikningnum til að tryggja að áætlunarkerfið sjái um alla birgðaforstillinguna.  |  
    |**MRP**|Reikna áætlun efnisþarfa. Vörur með tengdar kröfur eru teknar með í þessari keyrslu. Yfirleitt eru MPS og MRP keyrðar samtímis. Til að keyra MPS og MRP samtímis er reiturinn **Sameinaður MPS/MRP útreikningur** valinn **á síðunni Uppsetning** framleiðslu á flýtiflipanum **Áætlun** .|  
    |**Upphafsdagsetning**|Meta birgðastöðu. Ef birgðastaða vöru er fyrir neðan endurpöntunarmark flýtir kerfið áfyllingarpöntun. Ef vara er fyrir neðan öryggisbirgðir (frá og með upphafsdagsetningunni) færir kerfið aftur áfyllingarpöntun sem átti að falla á upphafsdagsetningu áætlunarinnar.|  
    |**Lokadagsetning**|Lokadagsetning áætlunarsjóðsins. Hvorki er litið til eftirspurnar né framboðs eftir þessa dagsetningu. Ef endurpöntunarferlið fyrir vöru nær fram yfir lokadagsetninguna er skilvirkt áætlunarsjónarmið fyrir þá vöru jafnt og pöntunardagsetningin plús endurpöntunarferlið.<br/><br/> Áætlunartímabilið er sá tími sem áætlunin nær yfir. Ef sjónkortið er of stutt eru vörur með lengri afhendingartíma ekki pantaðar á tíma. Ef sjónbilið er of langt er of miklum tíma eytt í að yfirfara og vinna úr upplýsingum sem líklega breytast áður en þess er þörf. Hægt er að stilla eitt áætlunarsjónarmið fyrir framleiðslu og lengra tímabil fyrir innkaup, þó að þess sé ekki krafist. Áætlunarsjónvarp fyrir innkaup og framleiðslu ætti að ná yfir heildarforskot íhluta.|  
    |**Stöðva og sýna fyrstu villu**|Þessi kostur er valinn ef áætlunarkeyrslan á að stöðvast um leið og villa finnst. Skilaboð birtast með upplýsingum um villuna. Ef villa er til staðar birtast aðeins áætlunarlínurnar sem tókst áður en villan kom upp í áætlunarvinnublaðinu. Ef þessi reitur **er ekki valinn heldur keyrslan Reikna áætlun** áfram fyrr en henni lýkur. Villur ráfa ekki keyrsluna. Ef ein eða fleiri villur eru til staðar birtast skilaboð þegar upplýsingum um hversu mörg atriði eru með villu. Síðan **Villukladdi áætlunar** opnast og birtir upplýsingar um villuna og tengla í þau birgðaspjöld sem hún hafði áhrif á.|  
    |**Nota spá**|Valin er spá til að taka með sem eftirspurn þegar áætlunarkeyrslan er keyrð. Sjálfgefna spáin er sett upp á flipanum **Áætlun** á síðunni **Uppsetning framleiðslu**.|  
    |**Sleppa spá fyrir**|Skilgreint er hversu mikið af valinni spá eigi að taka með í áætlunarkeyrslunni með því að færa inn fyrir hvaða dagsetningu spáreftirspurn er ekki tekin með.|  
    |**Virða áætlunarfæribreytur fyrir viðvaranir um frávik**|Reiturinn er sjálfgefið valinn.<br/><br/> Framboði fyrir áætlunarlínur með viðvörunum er yfirleitt ekki breytt samkvæmt áætlunarfæribreytum. Þess í stað stingur áætlunarkerfið einungis upp á framboði til að anna nákvæmu eftirspurnarmagni. Hins vegar er hægt að skilgreina sérstakar áætlunarfæribreytur fyrir áætlunarlínur sem á að fylgja með viðvörunum.<br/><br/>|  

4. Á flýtiflipanum **Vara** eru settar afmarkanir til að keyra áætlun byggða á vöru, vörulýsingu eða birgðageymslu.  
5. Velja hnappinn **Í lagi**. Keyrslunni eru keyrðar og áætlunarlínum er bætt við áætlunarvinnublaðið.  

## <a name="to-perform-action-messages"></a>Til að framkvæma aðgerðaboð
  
1. Á síðunni **Áætlunarvinnublað** veljið aðgerðina **Framkvæma aðgerðaboð**.  
2. Á flýtiflipanum **Valkostir** skal tilgreina hvernig á að stofna aðföngin. Fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

    |Svæði|Heimildasamstæða|  
    |---------------------------------|---------------------------------------|  
    |**Framleiðslupöntun**|Tilgreina hvernig á að stofna framleiðslupantanir. Hægt er að gera þetta beint úr áætlunarlínutillögunum. Hægt er að búa til annað hvort áætlaðar eða fastáætlaðar framleiðslupantanir.|  
    |**Samsetningarpöntun**|Tilgreina hvernig samsetningarpantanir eru stofnaðar. Hægt er að gera þetta beint úr áætlunarlínutillögunum.|  
    |**Innkaupapöntun**|Tilgreina hvernig búa á til innkaupapantanir. Hægt er að gera þetta beint úr áætlunarlínutillögunum.<br/><br/> Hægt er að breyta í þessum reit ef valið hefur verið að afrita áætlunarlínutillögurnar fyrir innkaupapantanirnar á innkaupatillögublaðið.|  
    |**Millifærslupöntun**|Tilgreina hvernig stofna á millifærslupantanir. Hægt er að gera þetta beint úr áætlunarlínutillögunum.<br/><br/> Hægt er að breyta í þessum reit ef valið hefur verið að afrita áætlunarlínutillögurnar fyrir flutningspantanirnar á innkaupatillögublaðið.|  
    |**Sameina millifærslupantanir**|Velja skal hvort sameina eigi millifærslupantanir.|  
    |**Stöðva og sýna fyrstu villu**|Þessi kostur er valinn ef framkvæma á **aðgerðarskilmálana - Áætl.** er notuð til að stöðva um leið og villa finnst. Aa skilaboð sýna upplýsingar um villuna. Ef villa er til staðar stofnar aðeins áætlunarlínurnar sem unnar voru áður en villan fannst.|  

3. Á flipanum **Áætlunarlína** er hægt að velja afmarkanir til að takmarka birtingu aðgerðarboða.  
4. Velja hnappinn **Í lagi**.  

Keyrslan eyðir línum á áætlunarblaðinu eftir að hún hefur framkvæmt aðgerðaboðin. Aðrar línur eru áfram á áætlunarvinnublaðinu þar til þær eru annaðhvort samþykktar síðar eða þeim eytt. Einnig er hægt að eyða línunum handvirkt.  

## <a name="action-messages"></a>Aðgerðaboð
  
Aðgerðarboð eru gefin út eftir pöntunarrakningarkerfinu þegar staðan er ótæk innan pöntunarnetsins. Hægt er að líta á skilaboðin sem tillögur um að vinna úr breytingum sem koma á jafnvægi á milli framboðs og eftirspurnar.  

Stofnun aðgerðarboða gerist á einu stigi í einu, með tilliti til kóta lágrar stöðu á hverju stigi. Þetta tryggir að allar vörur sem fara í gegnum breytingar á framboði og eftirspurn eru teknar með.  

Til að forðast lítil, óþörf eða óþörf aðgerðarboð er hægt að stilla hömlur sem eru notaðir til að takmarka stofnun aðgerðaboða við aðeins þær breytingar sem fara fram úr tilgreindu magni eða dagafjölda.  

Þegar aðgerðarboðin hafa verið skoðuð og ákveðið hvort samþykkja eigi einhverjar eða allar breytingarnar sem lagðar hafa verið til er reiturinn **Samþykkja aðgerðarboð** valinn. Næst skal uppfæra áætlanirnar í samræmi við það.  

> [!NOTE]  
> Aðgerðarboð eru tillaga um nýja pöntun, afturköllun pöntunar eða breytingar á magn eða dagsetningu pöntunar. Pöntun er innkaupapöntun, millifærslupöntun eða framleiðslupöntun.  

Þegar ójafnvægis verður vart í framboði/eftirspurn eru eftirfarandi aðgerðarboð stofnuð.  

|Aðgerðarboð|Heimildasamstæða|  
|--------------------|---------------------------------------|  
|**Nýtt**|Ef ekki er hægt að uppfylla eftirspurn með því að leggja til **aðgerðarboð um Breyta magni**, **Enduráætla** eða **Enduráætla & Breyta magni.** á fyrirliggjandi pöntunum eru aðgerðarboðin **Nýtt** mynduð til að leggja til nýja pöntun. Skilaboðin **Nýtt** birtast einnig ef ekki eru framboðspantanir í endurpöntunarferli vörunnar. Þessi valkostur ákvarðar fjölda tímabila framvirkt og afturvirkt í ráðstöfunarforstillingunni þegar leitað er að pöntun til að endurtímasetja.|  
|**Breyta magni**|Þegar magnið breytist vegna eftirspurnar sem rakin er til framboðspöntunar breyta aðgerðarboðunum **Breyta magni.** er mynduð. Skilaboðin gefa til kynna að breyta skuli tengdu framboði miðað við breytingar á eftirspurn. Ef ný eftirspurn myndast leitar [!INCLUDE[prod_short](includes/prod_short.md)] að næstu ófráteknu framboðspöntun innan endurpöntunarferlisins og gefur út aðgerðarboð um að breyta þeirri pöntun.|  
|**Endurtímasetja**|Þegar dagsetningarbreyting fyrir framboðs- eða eftirspurnarpöntun veldur ójafnvægi á pöntunarnetinu verða aðgerðarboðin **Enduráætla** . Ef tengsl eru á milli eftirspurnar og framboðs birtast aðgerðarboð til að leggja til að framboðspöntunin sé færð. Ef framboðspöntunin annar eftirspurn úr meira en einni sölupöntun er framboðspöntunin enduráætluð til jafns við dagsetningu fyrstu eftirspurnarinnar.|  
|**Endurtímas. og br. magni.**|Ef bæði dagsetningar og magn pöntunarbreytinga þarf að breyta áætlunum með tilliti til beggja. Aðgerðaboð taka báðar aðgerðir í ein skilaboð, **Enduráætla og Breyta magni**, til að tryggja jafnvægi komist á pöntunarnetið.|  
|**Hætta við**|Ef eftirspurn sem fjallað hefur verið um á grundvelli pöntunar-eftir pöntunar er eytt verða aðgerðarboð mynduð til að hætta við tengda framboðspöntun. Ef tengslin eru ekki eftir pöntun eru aðgerðarboð mynduð til að breytast til að draga úr framboðinu. Ef aðrir þættir, t.d. birgðaleiðréttingar, er ekki krafist framboðspöntunar þegar aðgerðaboð eru búin til, [!INCLUDE[prod_short](includes/prod_short.md)]  leggur til aðgerðarboðin **Hætta við** á vinnublaðinu.|  

## <a name="see-also"></a>Sjá einnig .

[Áætlun](production-planning.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)    
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)   
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
