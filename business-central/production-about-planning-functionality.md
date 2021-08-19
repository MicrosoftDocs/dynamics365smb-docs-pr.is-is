---
title: Um áætlunaraðgerðir
description: Áætlunarkerfið í Dynamics 365 Business Central tekur öll gögn um eftirspurn og framboð með í reikninginn, reiknar út niðurstöðurnar og kemur með tillögur að því að jafna framboðið og eftirspurnina.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/16/2021
ms.author: edupont
ms.openlocfilehash: e06bf94575c55d6e26fbe62c0b6cff06dd4fac70
ms.sourcegitcommit: acc1871afa889cb699e65b1b318028c05f8e6444
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/16/2021
ms.locfileid: "6636017"
---
# <a name="about-planning-functionality"></a>Um áætlunaraðgerðir

Áætlunarkerfið tekur öll gögn um eftirspurn og framboð með í reikninginn, reiknar út niðurstöðurnar og kemur með tillögur að því að jafna framboðið og eftirspurnina.  

Frekari og nákvæmari upplýsingar, sjá [Hönnunarupplýsingar: Framboðsáætlun](design-details-supply-planning.md)  

> [!NOTE]  
> Fyrir öll þau svið sem minnst er á í þessu efnisatriði, lesa ábendingarnar til að skilja virkni þeirra. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a>Eftirspurn og Framboð

Áætlanagerð hefur tvo hluta: eftirspurn og framboð. Halda þarf þeim í jafnvægi til að tryggja það að eftirspurninni sé annað á tímanlegan og hagkvæman hátt.  

- Eftirspurn er notað sem almennt heiti yfir hvers konar brúttóþörf eins og sölupöntun, þjónustupöntun, íhlutaþörf frá samsetningu eða framleiðslupantanir, millifærslur á útleið, standandi pöntun eða spá. Þar að auki býður forritið upp á nokkrar aðrar tæknilegar tegundir eftirspurnar - eins og neikvæða framleiðslu- eða innkaupapöntun, neikvætt birgðamat og innkaupaskil.  
- Framboð er það orð sem er mest notað fyrir hvaða tegund af áfyllingu sem er, eins og birgðir, innkaupapöntun, samsetningarpöntun, framleiðslupöntun eða millifærslu á innleið. Á sama hátt getur verið til neikvæð sölu- eða þjónustupöntun, neikvæð íhlutaþörf eða innkaupaskil – sem er allt á einhvern hátt dæmi um framboð.  

Annað markmið áætlunarkerfisins er að tryggja það að birgðamagnið hækki ekki að óþörfu. Í tilfelli minnkandi eftirspurnar mun áætlunarkerfið leggja til að annað hvort verði þeim áfyllingarpöntunum sem eru fyrir hendi frestað, þær minnkaðar eða afpantaðar.  

## <a name="planning-calculation"></a>Áætlunarútreikningur

Áætlunarkerfið er knúið áfram af viðbúinni og raunverulegri eftirspurn viðskiptavina auk endurpöntunarfæribreytum birgða. Ef áætlunarútreikningurinn er keyrður mun það leiða til þess að forritið leggi til sérstakar aðgerðir ([Aðgerðarboð](production-how-to-run-mps-and-mrp.md#action-messages)) til að framkvæma varðandi mögulega áfyllingu frá lánardrottnum, millifærslur á milli vöruhúsa eða framleiðslu. Ef áfyllingarpantanir eru þegar til gætu tillögurnar verið þess efnis að auka við pantanirnar eða flýta þeim til að koma til móts við eftirspurnarbreytingarnar.  

Grundvöllur áætlunarrútínunnar er í útreikningunum frá hagnaði til taps. Nettóþarfir knýja áætlaða útgáfu pantana sem eru tímasettar eftir leiðarupplýsingum (framleiddar vörur) eða afhendingartíma birgðaspjaldsins (keyptar vörur). Magn áætlaðrar útgáfu pöntunar er byggt á áætlunarútreikningunum og verður fyrir áhrifum af þeim færibreytum sem eru stilltar fyrir hvert stakt birgðaspjald.  

> [!TIP]
> Áætlunarkerfið fer eftir því hvernig fyrirtæki þitt notar staðsetningar. Frekari upplýsingar er að finna í [Áætlanagerð með eða án staðsetninga](production-planning-with-without-locations.md).

## <a name="planning-with-manual-transfer-orders"></a>Áætlað með handvirkum millifærslupöntunum

Eins og sjá má í reitnum **Áfyllingarkerfið** á birgðahaldseiningarspjaldi er hægt að setja áætlunarkerfið upp til að stofna millifærslupantanir til að jafna framboð og eftirspurn á milli birgðageymslna.  

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
- Sjálfgefið hömlu magn  

Nánari upplýsingar eru í [Upplýsingar um hönnun: Áætlunarfæribreytur](design-details-planning-parameters.md)  

## <a name="other-important-planning-fields"></a>Önnur mikilvæg áætlunarsvið

### <a name="planning-flexibility"></a>Sveigjanleiki áætlunar

Á flestum birgðapöntunum, eins og t.d. framleiðslupöntunum, getur valið **Ótakmarkaður** eða **Enginn** í **Sveigjanleiki áætlunar** reitnum.

Tilgreinir hvort birgðir sem framleiðslupöntunarlína sýnir eru teknar með í áætlunarkerfinu þegar aðgerðarboð eru reiknuð.
Ef reiturinn inniheldur **Ótakmarkað** tekur áætlunarkerfið línuna með í reikninginn þegar aðgerðarboð eru reiknuð. Ef reiturinn inniheldur **Enginn** er línan föst og óbreytanleg og áætlunarkerfið tekur hana ekki með í reikninginn þegar aðgerðarboð eru reiknuð.

### <a name="warning"></a>Viðvörun

Upplýsingareiturinn **Viðvörun** í **Áætlunarvinnublað** síðunni lætur þig vita um allar áætlunarlínur sem gerðar eru vegna óvenjulegra með texta, sem notandinn getur smellt á til að lesa viðbótarupplýsingar. Eftirfarandi tegundir viðvarana eru til:

- Neyð
- Frávik
- Athugið
- Neyð

Neyðarviðvörun birtist í tveimur aðstæðum:

- Birgðir eru neikvæðar á upphafsdagsetningu áætlunar.
- Framboðs- eða eftirspurnaratvik eru til aftur í tíma.

Ef birgðir vöru eru neikvæðar á upphafsdegi áætlunarinnar stingur kerfið upp á neyðarpöntun á birgðum með neikvæða magninu sem á að koma á upphafsdagsetningu áætlunarinnar. Upphafsdagsetningin og magn neyðarpöntunarinnar eru tiltekin í viðvörunartextanum.

Allar skjalalínur með skiladagsetningar á undan upphafsdagsetningu áætlunarinnar eru settar í eina neyðarpöntun til að varan berist á áætlaðri upphafsdagsetningu.

### <a name="exception"></a>Frávik

Viðvörun um frávik birtist ef áætlaðar birgðir eru undir öryggismarki birgða.

Áætlunarkerfið stingur upp á framboðspöntun til að uppfylla eftirspurnina á lokadagsetningunni. Viðvörunartextinn segir til um magn í öryggisbirgðum fyrir vöruna og dagsetninguna sem það magn varð of lítið.

Þegar farið er undir öryggismagn í birgðum er það talið frávik þar sem það ætti ekki að gerast ef endurpöntunarmark hefur verið stillt rétt.

> [!NOTE]
> Framboði fyrir áætlunarlínur með viðvörunum um frávik er yfirleitt ekki breytt samkvæmt áætlunarfæribreytum. Þess í stað stingur áætlunarkerfið einungis upp á framboði til að anna nákvæmu eftirspurnarmagni. Hins vegar er hægt að stilla áætlunarkeyrsluna þannig að hún virði tilteknar áætlunarfæribreytur fyrir áætlunarlínur með viðvörunum. Frekari upplýsingar er að finna í lýsingunni fyrir reitinn **Virða áætlunarfæribreytur fyrir viðvaranir um frávik** í greininni [Keyra fulla áætlunargerð, MPS eða MRP](production-how-to-run-mps-and-mrp.md).

### <a name="attention"></a>Athugið

Viðvörunin Til athugunar birtist í tveimur aðstæðum:

- Upphafsdagsetning áætlunarinnar er á undan kerfisdagsetningunni.
- Áætlunarlínan stingur upp á því að útgefinni innkaupa- eða framleiðslupöntun verði breytt.

> [!NOTE]
> Í áætlunarlínum með viðvaranir er reiturinn **Samþykkja aðgerðarboð** ekki valinn þar sem sá sem gerir áætlunina á að kanna þessar línur nánar áður en lokið er við áætlunina.

## <a name="planning-worksheets-and-requisition-worksheets"></a>Áætlunarvinnublöð og vinnublöð innkaupatillagna

Eins og lýst er í [Áætlanagerð](production-planning.md) er hægt að velja milli tveggja vinnublaða fyrir flesta verkþætti áætlanagerðar, áætlunarvinnublaðið og vinnublað innkaupatillögu. Flest ferlum er lýst samkvæmt áætlunarvinnublaði, en til eru nokkrar atburðarásir þar sem vinnublað innkaupatillögu er betra.

### <a name="requisition-worksheet"></a>Innkaupatillögublað

Síðan **Innkaupatillögublað** sýnir vörur sem þú vilt panta. Hægt er að setja vörur inn í vinnublaðið á eftirfarandi hátt:

- Færa vörurnar handvirkt inn í vinnublaðið og fylla út viðkomandi reiti.

- Nota runuvinnsluna **Reikna áætlun**. Þá er reiknuð áfyllingaráætlun fyrir vörur og birgðahaldseiningar sem hafa verið settar upp með innkaupatillögukerfi fyrir **innkaup** eða **millifærslu**. Þegar keyrslan er keyrð færir forritið sjálfkrafa í reitinn **Aðgerðaboð** tillögu um aðgerð sem nota má til að fylla á birgðirnar. Þetta gæti verið að auka magn vörunnar í fyrirliggjandi pöntun eða að stofna nýja pöntun, t.d.

- Ef notuð var keyrslan **Reikna áætlun** á síðunni **Áætlunarvinnublað** til að reikna út áfyllingaráætlun er hægt að nota runuvinnsluna **Framkvæma aðgerðaboð** til að afrita innkaupa- og millifærslupöntunartillögur úr áætlunarvinnublaðinu í innkaupatillögublaðið. Þetta kemur sér vel ef notendur sem sjá um framleiðslupantanir og innkaupa-/millifærslupantanir eru ekki þeir sömu.

- Hægt er að nota aðgerðina **Bein sending** til að færa inn í línur innkaupatillögublaðsins. Þessi aðgerð notar runuvinnsluna **Sækja sölupantanir** til að ákveða hvaða sölupöntunarlínur eigi að úthluta fyrir beina sendingu.

- Hægt er að nota aðgerðina **Sérpöntun** til að færa inn í línur innkaupatillögublaðsins. Þessi aðgerð notar runuvinnsluna **Sækja sölupantanir** til að ákveða hvaða sölupöntunarlínur eigi að úthluta fyrir sérpöntun.

Innkaupatillögulínur eru með nákvæmum upplýsingum um vörurnar sem þarf að endurpanta. Hægt er að breyta og eyða línunum til að leiðrétta áfyllingaráætlunina og vinna frekar úr línunum með því að nota keyrsluna **Framkvæma aðgerðarboð**.

Upplýsingar um áætlanagerð með birgðageymslum og flutningum er að finna í [Áætlanagerð með eða án birgðageymslna](production-planning-with-without-locations.md).

## <a name="see-also"></a>Sjá einnig

[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)  
[Áætlun](production-planning.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Uppsetning bestu venjur: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]