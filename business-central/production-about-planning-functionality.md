---
title: Um áætlunaraðgerðir
description: Lærðu hvernig áætlun notar eftirspurn og framboð gagna til að leggja til hvernig á að jafna framboð til að mæta eftirspurn.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '5430,'
ms.date: 09/19/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="about-planning-functionality"></a>Um áætlunaraðgerðir

Áætlunarkerfið tekur öll gögn um eftirspurn og framboð með í reikninginn, reiknar út niðurstöðurnar og kemur með tillögur að því að jafna framboðið og eftirspurnina.  

Nánari upplýsingar eru í [Upplýsingar um hönnun: áætlun birgða](design-details-supply-planning.md).  

> [!NOTE]  
> Fyrir öll þau svið sem minnst er á í þessu efnisatriði, lesa ábendingarnar til að skilja virkni þeirra. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="supply-and-demand"></a>Framboð og eftirspurn

Áætlanagerð hefur tvo hluta: eftirspurn og framboð. Þessir verða að jafnvægi til að tryggja að eftirspurnin sé uppfyllt.  

- Eftirspurn er hvers konar brúttóþörf, svo sem sölupöntun, þjónustupöntun, eða íhlutalagreining á samsetningu eða framleiðslupöntunum, Millifærsla á útleið, standandi pöntun eða spá. Þar að auki eru aðrar tæknilegar tegundir eftirspurnar, til dæmis neikvæð framleiðsla eða innkaupapöntun, neikvæðar birgðir og innkaupaskil.  
- Framboð á við um hvaða tegund af áfyllingu sem er, eins og birgðir, innkaupapöntun, samsetningarpöntun, framleiðslupöntun eða millifærslu á innleið. Á sama hátt getur verið til neikvæð sölu- eða þjónustupöntun, neikvæð íhlutaþörf eða innkaupaskil sem stendur einnig fyrir framboð.  

Annað markmið áætlunarkerfisins er að tryggja það að birgðamagnið hækki ekki að óþörfu. Í tilfelli minnkandi eftirspurnar mun áætlunarkerfið leggja til að annað hvort verði þeim áfyllingarpöntunum sem eru fyrir hendi frestað, þær minnkaðar eða afpantaðar.  

## <a name="planning-calculation"></a>Útreikningur áætlunar

Áætlunarkerfið er knúið áfram af viðbúinni og raunverulegri eftirspurn viðskiptavina auk endurpöntunarfæribreytum birgða. Ef áætlunarútreikningurinn er keyrður mun það leiða til þess að forritið leggi til sérstakar aðgerðir ([Aðgerðarboð](production-how-to-run-mps-and-mrp.md#action-messages)) til að framkvæma varðandi mögulega áfyllingu frá lánardrottnum, millifærslur á milli vöruhúsa eða framleiðslu. Ef áfyllingarpantanir eru þegar til gætu tillögurnar verið þess efnis að auka við pantanirnar eða flýta þeim til að koma til móts við eftirspurnarbreytingarnar.  

Grundvöllur áætlunarrútínunnar er í útreikningunum frá hagnaði til taps. Nettóþarfir knýja áætlaða útgáfu pantana sem eru tímasettar eftir leiðarupplýsingum (framleiddar vörur) eða afhendingartíma birgðaspjaldsins (keyptar vörur). Magn áætlaðrar útgáfu pöntunar er byggt á áætlunarútreikningunum og verður fyrir áhrifum af þeim færibreytum sem eru stilltar fyrir hvert stakt birgðaspjald.  

> [!TIP]
> Áætlunarkerfið fer eftir því hvernig fyrirtæki þitt notar staðsetningar. Frekari upplýsingar er að finna í [Áætlanagerð með eða án staðsetninga](production-planning-with-without-locations.md).

## <a name="planning-with-manual-transfer-orders"></a>Áætlun með handvirkum millifærslupöntunum

 **Í reitnum Áfyllingarkerfi**  á birgðaspjaldi er hægt að setja upp áætlanakerfið til að stofna flutningspantanir til að jafna framboð og eftirspurn eftir stöðum.  

Til viðbótar slíkum sjálfvirkum millifærslupöntunum getur stundum þurft að framkvæma almennan flutning á birgðum í aðra birgðageymslu, óháð eftirspurn. Til þess er millifærslupöntun stofnuð handvirkt fyrir magnið sem á að flytja. Til að tryggja að áætlunarkerfið breyti ekki þessari handvirku millifærslupöntun þarf að stilla reitinn **Sveigjanleiki áætlunar** í millifærslulínunum á Enginn.  

Hins vegar, ef áætlunarkerfið á að leiðrétta magn og dagsetningar í millifærslupöntunum samkvæmt eftirspurn þarf að stilla reitinn **Sveigjanleiki áætlunar** á sjálfgildið, Ótakmarkað.

## <a name="planning-parameters"></a>Áætlunarfæribreytur

Áætlunarfæribreyturnar stýra því hvenær, hversu mikið og hvernig er fyllt á eftir mismunandi stillingunum á birgðaspjaldinu (eða birgðaeiningu - SKU) og framleiðsluuppsetningunni.  

Eftirtaldar áætlunarfæribreytur eru til á vöru eða birgðahaldseiningarspjaldi:  

- Hömlutímabil  
- Hömlu magn  
- Endurpöntunarstefna  
- Endurpöntunarmark
- Hámarksbirgðir  
- Yfirflæðisstig  
- Tímarammi  
- Lotusöfnunartímabil  
- Enduráætlunartímabil  
- Pöntunarmagn  
- Öryggisforskot  
- Magn í öryggisbirgðum  
- Samsetningarstefna  
- Framleiðslustefna  

Eftirfarandi pöntunarbreytur eru til á vöru eða birgðahaldseiningarspjaldi:  

- Lágmarksmagn pöntunar  
- Hámarksmagn pöntunar  
- Fjöldapanta  

Á meðal uppsetningarreita altækrar áætlunar á síðunni **Framleiðsluuppsetning** eru:  

- Kvikur lágstigskóti  
- Núgildandi eftirspurnarspá  
- Nota spá með staðsetningu  
- Sjálfgefið öryggisforskot  
- Autt yfirflæðisstig  
- Sameinaður MPS/MRP útreikn.
- Íhlutir á staðnum  
- Sjálfgefið hömlunartímabil  
- Sjálfgefið hömlunarmagn  

Til að fræðast meira er farið í  [hönnunarupplýsingar: áætlunarfæribreytur](design-details-planning-parameters.md)  

## <a name="other-important-planning-fields"></a>Öðrum mikilvægum áætlunarsvæðum

### <a name="planning-flexibility"></a>Sveigjanleiki áætlunar

Á flestum birgðapöntunum, eins og t.d. framleiðslupöntunum, getur valið **Ótakmarkaður** eða **Enginn** í **Sveigjanleiki áætlunar** reitnum.

Tilgreinir hvort birgðir sem framleiðslupöntunarlína sýnir eru teknar með í áætlunarkerfinu þegar aðgerðarboð eru reiknuð.
Ef reiturinn inniheldur **Ótakmarkað** tekur áætlunarkerfið línuna með í reikninginn þegar aðgerðarboð eru reiknuð. Ef reiturinn inniheldur **Enginn** er línan föst og óbreytanleg og áætlunarkerfið tekur hana ekki með í reikninginn þegar aðgerðarboð eru reiknuð.

### <a name="warning"></a>Viðvörun

Upplýsingareiturinn **Viðvörun** í **Áætlunarvinnublað** síðunni lætur þig vita um allar áætlunarlínur sem gerðar eru vegna óvenjulegra með texta, sem notandinn getur smellt á til að lesa viðbótarupplýsingar. Eftirfarandi tegundir viðvarana eru til:

- Neyð
- Frávik
- Athugið

### <a name="emergency"></a>Neyð

Neyðarviðvörunarbjöllur Sýna við tvenns konar aðstæður:

- Birgðir eru neikvæðar á upphafsdagsetningu áætlunar.
- Framboðs- eða eftirspurnaratvik eru til aftur í tíma.

Ef birgðir vöru eru neikvæðar á upphafsdegi áætlunarinnar stingur kerfið upp á neyðarpöntun á birgðum með neikvæða magninu sem á að koma á upphafsdagsetningu áætlunarinnar. Upphafsdagsetningin og magn neyðarpöntunarinnar eru tiltekin í viðvörunartextanum.

Allar skjalalínur með skiladagsetningar á undan upphafsdagsetningu áætlunarinnar eru settar í eina neyðarpöntun til að varan berist á áætlaðri upphafsdagsetningu.

### <a name="exception"></a>Frávik

Viðvaranir í undantekningartilfellum Sýna Ef áætlaðar tiltækar birgðir falla undir öryggisbirgðamagn.

Áætlunarkerfið stingur upp á framboðspöntun til að uppfylla eftirspurnina á lokadagsetningunni. Viðvörunartextinn segir til um magn í öryggisbirgðum fyrir vöruna og dagsetninguna sem það magn varð of lítið.

Brot á öryggisbirgðastigi telst til undantekninga þar sem það ætti ekki að eiga sér stað ef endurpöntunarpunkturinn hefur verið rétt stilltur.

> [!NOTE]
> Framboði fyrir áætlunarlínur með viðvörunum um frávik er yfirleitt ekki breytt samkvæmt áætlunarfæribreytum. Þess í stað stingur áætlunarkerfið einungis upp á framboði til að anna nákvæmu eftirspurnarmagni. Hins vegar er hægt að stilla áætlunarkeyrsluna þannig að hún virði tilteknar áætlunarfæribreytur fyrir áætlunarlínur með viðvörunum. Frekari upplýsingar er að finna í lýsingunni fyrir reitinn **Virða áætlunarfæribreytur fyrir viðvaranir um frávik** í greininni [Keyra fulla áætlunargerð, MPS eða MRP](production-how-to-run-mps-and-mrp.md).

### <a name="attention"></a>Athugið

Viðvörun vegna athyglisbrests birtist við tvenns konar aðstæður:

- Upphafsdagsetning áætlunarinnar er á undan kerfisdagsetningunni.
- Áætlunarlínan stingur upp á því að útgefinni innkaupa- eða framleiðslupöntun verði breytt.

> [!NOTE]
> Í áætlunarlínum með viðvaranir er reiturinn **Samþykkja aðgerðarboð** ekki valinn þar sem sá sem gerir áætlunina á að kanna þessar línur nánar áður en lokið er við áætlunina.

## <a name="planning-worksheets-and-requisition-worksheets"></a>Áætlunarvinnublöð og vinnublöð innkaupatillagna

Eins og lýst er í [Áætlanagerð](production-planning.md) er hægt að velja milli tveggja vinnublaða fyrir flesta verkþætti áætlanagerðar, áætlunarvinnublaðið og vinnublað innkaupatillögu. Flest ferlum er lýst samkvæmt áætlunarvinnublaði, en til eru nokkrar atburðarásir þar sem vinnublað innkaupatillögu er betra.

[!INCLUDE [edit-in-excel](includes/edit-in-excel.md)]

### <a name="requisition-worksheet"></a>Innkaupatillögublað

Síðan **Innkaupatillögublað** sýnir vörur sem þú vilt panta. Hægt er að setja vörur inn í vinnublaðið á eftirfarandi hátt:

- Færa vörurnar handvirkt inn í vinnublaðið og fylla út viðkomandi reiti.

- Nota runuvinnsluna **Reikna áætlun**. Þá er reiknuð áfyllingaráætlun fyrir vörur og birgðahaldseiningar sem hafa verið settar upp með innkaupatillögukerfi fyrir **innkaup** eða **millifærslu**. Þegar keyrslan er keyrð færir forritið sjálfkrafa í reitinn **Aðgerðaboð** tillögu um aðgerð sem nota má til að fylla á birgðirnar. Þetta gæti verið að auka magn vörunnar í fyrirliggjandi pöntun eða að stofna nýja pöntun, t.d.

- Ef notuð var keyrslan **Reikna áætlun** á síðunni **Áætlunarvinnublað** til að reikna út áfyllingaráætlun er hægt að nota runuvinnsluna **Framkvæma aðgerðaboð** til að afrita innkaupa- og millifærslupöntunartillögur úr áætlunarvinnublaðinu í innkaupatillögublaðið. Þetta kemur sér vel ef notendur sem sjá um framleiðslupantanir og innkaupa-/millifærslupantanir eru ekki þeir sömu.

- Hægt er að nota aðgerðina **Bein sending** til að færa inn í línur innkaupatillögublaðsins. Þessi aðgerð notar runuvinnsluna **Sækja sölupantanir** til að ákveða hvaða sölupöntunarlínur eigi að úthluta fyrir beina sendingu.

- Hægt er að nota aðgerðina **Sérpöntun** til að færa inn í línur innkaupatillögublaðsins. Þessi aðgerð notar runuvinnsluna **Sækja sölupantanir** til að ákveða hvaða sölupöntunarlínur eigi að úthluta fyrir sérpöntun.

Innkaupatillögulínur eru með nákvæmum upplýsingum um vörurnar sem þarf að endurpanta. Hægt er að breyta og eyða línunum til að leiðrétta áfyllingaráætlunina og vinna frekar úr línunum með því að nota keyrsluna **Framkvæma aðgerðarboð**. 

Upplýsingar um áætlanagerð með birgðageymslum og flutningum er að finna í [Áætlanagerð með eða án birgðageymslna](production-planning-with-without-locations.md).

> [!TIP]
> Þegar unnið er á síðunum **Innkaupatillögublað** eða **Áætlunarvinnublað** geturðu skipulagt línurnar með því að raða eftir dálkheiti. Þetta er sérstaklega gagnlegt á síðunni Áætlunarvinnublað því að hægt er að nota hana fyrir marglaga framleiðslupantanir. Línum er sjálfgefið raðað eftir reitnum **Vörunúmer**. Til að flokka línur fyrir marglaga pöntun skal raða eftir **Tilv. pöntunarnr** . Einnig geta reitirnir **MPS-pöntun** og **Áætlunarstig** hjálpað til við að sýna stigveldi línanna.

## <a name="see-also"></a>Sjá einnig .

[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)  
[Áætlun](production-planning.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
