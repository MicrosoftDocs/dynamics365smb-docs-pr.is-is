---
title: Keyra fulla áætlanagerð, MPS eða MRP
description: Áætlunarkerfið getur reiknað MPS og MRP samkvæmt beiðni eða reiknað bæði á sama tíma.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 99000852, 99000860
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: b8a9f648030e0a307ccd1a086c681ba8492cf357
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516667"
---
# <a name="run-full-planning-mps-or-mrp"></a>Keyra fulla áætlanagerð, MPS eða MRP

Skilmálarnir "sem keyra áætlunarvinnublaðið" eða "MRP" eiga við útreikning aðalframleiðsluáætlunar og efnisþarfa samkvæmt raunverulegri eftirspurn og eftirspurn samkvæmt spá. Áætlunarkerfið getur reiknað MPS og MRP samkvæmt beiðni eða reiknað bæði á sama tíma.  

-   MPS er útreikningur á aðalframleiðsluáætlun byggt á raunverulegri eftirspurn og eftirspurnarspá. MPS-útreikningur er notaður fyrir lokavörur sem eru með spá eða sölupöntunarlínu. Þessar vörur eru kallaðar "MPS-vörur" og eru auðkenndar þegar útreikningur hefst.  
-   MRP er útreikningur á efnisþörfum sem byggjast á raunverulegri eftirspurn eftir hlutum og eftirspurnarspá á hlutastigi. MRP er eingöngu reiknað fyrir vörur sem eru ekki MPS-vörur. Tilgangur MRP er bjóða upp á tímasettar áætlanir þannig að viðeigandi vara er til á viðeigandi tíma, á viðeigandi stað og í viðeigandi magni.  

Áætlunaralgóritmarnir fyrir MPS og MRP eru eins. Þeir ná yfir samantekt nettóstöðu, endurnotkun fyrirliggjandi áfyllingarpantana og aðgerðarboð. Áætlunarkerfisvinnslan tekur mið af þörfum eða væntanlegum þörfum (eftirspurn) og hvað er til staðar (framboð). Þegar þessar tegundir magns eru nettófærðar stofnar [!INCLUDE[prod_short](includes/prod_short.md)] aðgerðarboð. Aðgerðarboð eru tillögur um að stofna nýja pöntun, breyta pöntun (magni eða dagsetningu) eða hætta við pöntun í pöntun. Hugtakið „pöntun“ inniber innkaupapantanir, samsetningarpöntun, framleiðslupantanir og millifærslupantanir.

Tengla sem eru stofnaðir af áætlunarkerfinu milli eftirspurnar og tengds framboðs er hægt að rekja á síðunni **Pöntunarrakning**. Frekari upplýsingar eru í [Rekja tengsl á milli framboðs og eftirspurnar](production-how-track-demand-supply.md).   

Viðundandi niðurstöður áætlunar byggjast á uppsetningu í birgðaspjöldum, samsetningaruppskriftum, framleiðsluuppskriftum og leiðum.  

## <a name="methods-for-generating-a-plan"></a>Aðferðir við stofnun áætlunar  

-   **Reikna áætlun endurgerðar:** Þessi aðgerð vinnur eða endurgerir alla efnisáætlunina. Þessi vinnsla hefst á eyðingu allra áætlaðra birgðapantana sem eru hlaðnar. Allar vörur í gagnagrunninum eru enduráætlaðar.  
-   **Reikna áætlun hreyfingar**: Þessi aðgerð vinnur hreyfingaáætlun. Vörur eru teknar með í hreyfingaáætlun vegna tveggja breytinga:  
    - **Breytingar á eftirspurn/framboði:** Þar með talið eru breytingar á magni í sölupöntunum, eftirspurnarspám, samsetningarpöntunum, framleiðslupöntunum eða innkaupapöntunum. Óáætluð breyting á birgðastigi er einnig talin breyting á magni.  
    - **Breytingar á áætlunarfæribreytum**: Þar með talið eru breytingar á öryggisbirgðum, endurpöntunarmarki, leið, uppskrift og breytingar útreikningi tímaramma eða afhendingartíma.  
-   **Sækja aðgerðarboð:** Þessi aðgerð er skammtímaáætlunarverkfæri sem gefur út aðgerðarboð sem tilkynna notanda breytingar síðan síðasta endurgerðar- eða hreyfingaáætlun var reiknuð.  

Með hverri áætlunaraðferð, myndar [!INCLUDE[prod_short](includes/prod_short.md)] vinnublaðafærslur þar sem gert er ráð fyrir óendanlegum afköstum. Afköst vinnustöðvar og vélastöðvar eru ekki tekin með þegar skemu eru unnin.  

> [!IMPORTANT]  
>  Aðgerðin Reikna áætlun endurgerðar er algengasta vinnslan. Aðgerðirnar útreikningsvinnublaða áætlunar og aðgerðarboð eru hins vegar notaðar til keyra vinnsluna Reikna áætlun hreyfingar.  
>   
>  Eiginleikann Aðgerðarboðaáætlun er hægt að keyra á milli endurgerðaráætlana og hreyfingaráætlana til að fá fljótlegt yfirlit yfir áhrif áætlanabreytinga. Hún er hins vegar ekki hugsuð til að koma að fullu í stað hinna tveggja.  

## <a name="to-calculate-the-planning-worksheet"></a>Til að reikna áætlunarvinnublað:  
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Áætlunarvinnublað** og velja síðan viðkomandi tengil.  
2.  Velja **Reikna áætlun endurgerðar** aðgerðina til að opna síðuna **Reikna áætlun**.  
3.  Á flýtiflipanum **Valkostir** skal fylla reitina út eins og lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**MPS**|Valið til að hefja útreikning aðalframleiðsluáætlunar. Atriði sem eru með opnum sölupöntunum eða eftirspurnarspám eru talin í þessari keyrslu.|  
    |**MRP**|Valið til að hefja útreikning efnisþarfaáætlunar. Vörur með tengdar kröfur eru teknar með í þessari keyrslu. Yfirleitt eru MPS og MRP keyrðar á sama tíma. Til að keyra þær saman þarf að haka í gátreitinn **Sameinaður MPS/MRP útreikn.** á flipanum **Áætlun** á síðunni **Uppsetning framleiðslu**.|  
    |**Upphafsdagsetning**|Þessi dagsetning er notuð til að meta birgðastöðu. Ef birgðastaða vöru er fyrir neðan endurpöntunarmark flýtir kerfið áfyllingarpöntun. Ef vara er fyrir neðan öryggisbirgðir (frá og með upphafsdagsetningunni) færir kerfið aftur áfyllingarpöntun sem átti að falla á upphafsdagsetningu áætlunarinnar.|  
    |**Lokadagsetning**|Þetta er lokadagsetningin fyrir áætlunarhringinn. Hvorki eftirspurn né framboð er tekið með eftir þessa dagsetningu. Ef endurpöntunarferli vöru fer fram yfir lokadagsetningu jafngildir virkt áætlunartímabil þeirrar vöru pöntunardagsetningu + endurpöntunarferli.<br /><br /> Áætlunartímabilið er sá tími sem áætlunin nær yfir. Ef tímabilið er of stutt eru vörur með lengri afhendingartíma ekki pantaðar í tíma. Ef tímabilið er of langt er of miklum tíma eytt í endurskoðun og vinnslu upplýsingar sem líklega breytast áður en þeirra er þörf. Hægt er að velja eitt áætlunartímabil fyrir framleiðslu og lengra tímabil fyrir innkaup, þótt þess sé ekki krafist. Áætlunartímabil fyrir innkaup og framleiðslu ætti að ná yfir uppsafnaðan afhendingartíma íhluta.|  
    |**Stöðva og sýna fyrstu villu**|Veljið ef áætlunarkeyrsla á að stöðvast um leið og villa kemur upp. Um leið birtast skilaboð með upplýsingum um fyrstu villuna. Ef villa er til staðar eru aðeins áætlunarlínur sem lokið var við fyrir villuna í áætlunarvinnublaðinu. Ef þessi reitur er ekki valinn heldur keyrslan **Reikna áætlun** áfram þar til henni er lokið án þess að stöðvast ef villur koma upp. Ef ein eða fleiri villur eru til staðar birtast skilaboð þegar keyrslunni er lokið með upplýsingum um hversu mörg atriði eru með villu. Síðan **Villukladdi áætlunar** opnast og birtir upplýsingar um villuna og tengla í þau birgðaspjöld sem hún hafði áhrif á.|  
    |**Nota spá**|Valin er spá sem taka á með sem eftirspurn þegar áætlunarkeyrslan er keyrð. Sjálfgefna spáin er sett upp á flipanum **Áætlun** á síðunni **Uppsetning framleiðslu**.|  
    |**Sleppa spá fyrir**|Skilgreina hversu mikið af völdu spánni á að taka með í áætlunarkeyrsluna með því að færa inn dagsetningu sem spáreftirspurn er ekki tekin með fyrir. Þannig er hægt að sleppa gömlum upplýsingum.|  
    |**Virða áætlunarfæribreytur fyrir viðvaranir um frávik**|Reiturinn er sjálfgefið valinn.<br /><br /> Framboði fyrir áætlunarlínur með viðvörunum er yfirleitt ekki breytt samkvæmt áætlunarfæribreytum. Þess í stað stingur áætlunarkerfið einungis upp á framboði til að anna nákvæmu eftirspurnarmagni. Hins vegar er hægt að skilgreina sérstakar áætlunarfæribreytur fyrir áætlunarlínur sem á að fylgja með viðvörunum.<br /><br />|  

4.  Á flýtiflipanum **Vara** afmarkarðu og keyrir áætlunarvinnslur samkvæmt vöru, vörulýsingu eða birgðageymslu.  
5.  Velja hnappinn **Í lagi**. Keyrslan fer í gang og áætlunarlínur eru færðar inn í áætlunarvinnublaðið.  

## <a name="to-perform-action-messages"></a>Til að framkvæma aðgerðaboð  
1.  Á síðunni **Áætlunarvinnublað** veljið aðgerðina **Framkvæma aðgerðaboð**.  
2.  Á flýtiflipanum **Valkostir** skal tilgreina hvernig á að stofna aðföngin. Fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

    |Svæði|Lýsing|  
    |---------------------------------|---------------------------------------|  
    |**Framleiðslupöntun**|Tilgreinið hvernig á að stofna framleiðslupantanir. Hægt er að gera þetta beint úr áætlunarlínutillögunum. Hægt er að búa til annað hvort áætlaðar eða fastáætlaðar framleiðslupantanir.|  
    |**Samsetningarpöntun**|Tilgreinið hvernig á að stofna samsetningarpantanir. Hægt er að gera þetta beint úr áætlunarlínutillögunum.|  
    |**Innkaupapöntun**|Tilgreinið hvernig á að stofna innkaupapantanir. Hægt er að gera þetta beint úr áætlunarlínutillögunum.<br /><br /> Hægt er að breyta í þessum reit ef valið hefur verið að afrita áætlunarlínutillögurnar fyrir innkaupapantanirnar á innkaupatillögublaðið.|  
    |**Millifærslupöntun**|Tilgreinið hvernig á að stofna millifærslupantanir. Hægt er að gera þetta beint úr áætlunarlínutillögunum.<br /><br /> Hægt er að breyta í þessum reit ef valið hefur verið að afrita áætlunarlínutillögurnar fyrir flutningspantanirnar á innkaupatillögublaðið.|  
    |**Sameina millifærslupantanir**|Valið ef sameina á millifærslupantanir.|  
    |**Stöðva og sýna fyrstu villu**|Valið ef keyrslan **Framkvæma aðgerðarboð - Áætl.** á að stöðvast um leið og villa kemur upp. Um leið birtast skilaboð með upplýsingum um fyrstu villuna. Ef villa er til staðar stofna eingöngu áætlunarlínur sem unnar voru áður en villan kom upp framboðspantanir.|  

3.  Á flipanum **Áætlunarlína** er hægt að velja afmarkanir til að takmarka birtingu aðgerðarboða.  
4.  Velja hnappinn **Í lagi**.  

Keyrslan eyðir línum á áætlunarblaðinu eftir að hún hefur framkvæmt aðgerðaboðin. Aðrar línur eru áfram á áætlunarvinnublaðinu þar til þær eru annaðhvort samþykktar síðar eða þeim eytt. Einnig er hægt að eyða línunum handvirkt.  

## <a name="action-messages"></a>Aðgerðarboð  
Aðgerðarboð eru gefin út eftir pöntunarrakningarkerfinu þegar staðan er ótæk innan pöntunarnetsins. Þau er hægt að líta á sem tillögur um að hefja vinnslu sem kemur á jafnvægi á milli framboðs og eftirspurnar.  

Stofnun aðgerðarboða gerist á einu stigi í einu, með tilliti til kóta lágrar stöðu á hverju stigi. Þetta tryggir að allar vörur sem fara í gegnum breytingar á framboði og eftirspurn eru teknar með.  

Til að koma í veg fyrir óþörf aðgerðaboð getur notandi stofnað hömlur sem hindra stofnun aðgerðarboða annarra við þær breytingar sem fara fram úr tilgreindu magni eða fjölda daga.  

Þegar búið er að skoða aðgerðarboðin og búið er að ákveða hvort eigi að samþykkja sumar eða allar breytingar í þeim með því velja reitinn **Samþykkja aðgerðarboð**, þá er hægt að uppfæra áætlunina.  

> [!NOTE]  
>  Aðgerðarboð eru tillaga um nýja pöntun, afturköllun pöntunar eða breytingar á magn eða dagsetningu pöntunar. Pöntun er innkaupapöntun, millifærslupöntun eða framleiðslupöntun.  

Þegar ójafnvægis verður vart í framboði/eftirspurn eru eftirfarandi aðgerðarboð stofnuð.  

|Aðgerðarboð|Lýsing|  
|--------------------|---------------------------------------|  
|**Nýtt**|Ef ekki er hægt að uppfylla eftirspurn með aðgerðarboðum um **Breyta magni**, **Enduráætla** eða **Enduráætla og breyta** í fyrirliggjandi pöntunum birtast aðgerðarboðin **Nýtt** sem er tillaga um nýja pöntun. Auk þess eru aðgerðarboðin **Nýtt** gefin út ef engar framboðspantanir eru í endurpöntunarferli fyrir viðkomandi vöru eru til staðar. Þessi færibreyta ákvarðar fjölda tímabila fram og til baka í ráðstöfunarforstillingunni þegar leitað er að pöntun fyrir til að enduráætla.|  
|**Breyta magni**|Þegar eftirspurn sem rakin er til framboðspöntunar verður fyrir magnbreytingu birtast aðgerðaboðin **Breyta magni** , sem þýðir að tengdu framboði ætti að breyta miðað við breytinguna í eftirspurn. Ef ný eftirspurn myndast leitar [!INCLUDE[prod_short](includes/prod_short.md)] að næstu ófráteknu framboðspöntun innan endurpöntunarferlisins og gefur út aðgerðarboð um að breyta þeirri pöntun.|  
|**Endurtímasetja**|Þegar dagsetning framboðs- eða eftirspurnarpöntunar breytist og ójafnvægi skapast út frá því gefur kerfið út aðgerðarboðin **Enduráætla**. Ef bein tengsl eru á milli framboðs og eftirspurnar er gefið út aðgerðarboð þar sem stungið er upp á að framboð verði fært um það sama. Ef framboðspöntunin annar eftirspurn úr meira en einni sölupöntun er framboðspöntunin enduráætluð til jafns við dagsetningu fyrstu eftirspurnarinnar.|  
|**Endurtímas. og br. magni.**|Ef bæði dagsetning og magn í pöntun breytast verður að breyta áætlunum með tilliti til beggja þátta. Aðgerðaboð taka báðar aðgerðir í ein skilaboð, **Enduráætla og Breyta magni**, til að tryggja jafnvægi komist á pöntunarnetið.|  
|**Hætta við**|Ef eftirspurn, sem uppfyllt er samkvæmt hverri beiðni, er eytt birtast aðgerðarboð um að hætta við tengda framboðspöntun. Ef tengslin eru ekki byggð á hverri pöntun fyrir sig eru stofnuð aðgerðarboð um að breyta pöntuninni til að draga úr framboði. Ef aðrir þættir, t.d. birgðaleiðréttingar, valda því að framboðspöntun er óþörf þegar notandi gefur út aðgerðarboð birtir [!INCLUDE[prod_short](includes/prod_short.md)] aðgerðarboðin **Hætta við** á vinnublaðinu.|  

## <a name="see-also"></a>Sjá einnig  
[Áætlun](production-planning.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)    
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)   
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]