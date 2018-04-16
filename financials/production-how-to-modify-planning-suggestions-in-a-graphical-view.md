---
title: "Hvernig á að: Breyta áætlunartillögum í myndrænu yfirliti | Microsoft Docs"
description: "Dæmigerð verkþáttaáætlun er til að breyta eða bæta við línum áætlunarvinnublaðs til að breyta þeim birgðapöntunum sem lagðar eru til áður þær eru færðar inn með því að keyra aðgerðina **Framkvæma aðgerðarboð**. Í stað þess að gera þetta í áætlunarvinnublaðinu er notað myndrænt yfirlit."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 9217d8707ab65d231a6759e86f6f2b2866835bb8
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="modify-planning-suggestions-in-a-graphical-view"></a>Breyta áætlunartillögum í myndrænu yfirliti
Dæmigerð verkþáttaáætlun er til að breyta eða bæta við línum áætlunarvinnublaðs til að breyta þeim birgðapöntunum sem lagðar eru til áður þær eru færðar inn með því að keyra aðgerðina **Framkvæma aðgerðarboð**. Í stað þess að gera þetta í áætlunarvinnublaðinu er notað myndrænt yfirlit.

Í glugganum **Vara til ráðstöfunar samkvæmt tímalínu** er hægt að breyta tilteknum birgðapöntunum og tillögum með því að draga atriði eftir y-ásnum til að breyta magni eða eftir x-ásnum til að breyta gjalddaga.  

 Í glugganum **Vara til ráðstöfunar samkvæmt tímalínu** og glugganum **Áætlunarvinnublað** er hægt að velja úr eftirfarandi breytingum:  

-   Breyta tillagðri framboðspöntun sem aðeins er til sem áætlunarlína.  
-   Breyta birgðapöntun sem kerfið stingur upp á að breyta.  
-   Stofna nýja framboðspöntun sem lögð er til og breyta henni.  

Nánari upplýsingar um þær tegundir áætlunarlína sem birtast eru í reitnum Lýsing á flýtiflipanum **Atviksbreytingar**.  

Þegar **Vista breytingar** er valið í glugganum **Vara til ráðstöfunar samkvæmt tímalínu** eru breytingarnar sem gerðar hafa verið afritaðar í áætlunar- eða beiðnivinnublaðið. Nú er hægt að innleiða þetta með **Framkvæma aðgerðaboðaáætlun**.  

Eftirfarandi ferli sýnir hvernig eigi að breyta framboðstillögum með því að draga og sleppa. Einnig er hægt að breyta reitunum **Skiladagur** og **Magn** á flýtiflipanum **Atviksbreytingar** og sjá strax breytingarnar á myndrænan hátt á flýtiflipanum **Tímalína** í glugganum **Áætlunarvinnublað**.  

## <a name="to-modify-suggested-supply-orders-in-the-graphical-view"></a>Til að breyta ráðlögðum birgðapöntunum í myndræna yfirlitinu  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vara til ráðstöfunar samkvæmt tímalínu** og velja svo viðeigandi tengil.  

    Glugginn **Vara til ráðstöfunar samkvæmt tímalínu** opnast með vörunúmerinu, staðsetningu og afbrigði vörunnar í völdum áætlunarlínum forvöldum í flýtiflipanum **Valkostir**. Flýtiflipinn **Tímalína** sýnir myndræna lýsingu á áætluðum birgðum vörunnar, að meðtöldum áætlunartillögum.  

2.  Ganga þarf úr skugga um að reiturinn **Taka með áætlunartillögur** sé valinn.  
3.  Finna ráðlagða framboðspöntun sem ætlunin er að breyta. Hægt er að auðkenna breytanlegar einingar með græna hringnum og disktákninu. Nánari upplýsingar um tákn eru í „Tákn og táknmyndir í flýtiflipa tímalínu“.  
4.  Setjið bendilinn yfir græna hringinn þar til hann stækkar og bendillinn breytist í færsluformið (fjórar örvar).  
5.  Haldið inni músarhnappi á meðan bendillinn er færður til upp eða niður til að breyta magni. Haldið inni músarhnappi á meðan bendillinn er færður til vinstri eða hægri til að breyta lokadeginum.  
6.  Auk þess að flytja einingar með því að draga og sleppa er hægt að breyta áætlunartillögum með því að nota ýmsar aðgerðir með fellilistanum. Opna skal flettilista fyrir grænan hring tillagðrar framboðseiningar og ein eftirfarandi aðgerða valin  

    |Virkni|Lýsing|  
    |--------------|---------------------------------------|  
    |**Búa til nýtt framboð**|Stofnar nýjan atriðispunkt þar sem fellilisti er opnaður, sem stendur fyrir nýja framboðspöntun sem stungið er upp á. Verður nýja línan í áætlunarvinnublaðinu þegar valið er **Vista breytingar**.<br /><br /> **ATHUGIÐ:** Ef reitirnir **Afmörkun staðsetningar** eða **Afmörkun afbrigðis** í **Valkostir** eru auðir eða hafa fleiri en eitt afmörkunargildi verður nýja framboðið er stofnað og síðar vistað í áætlunarblaðið eða innkaupatillöguna með eftirfarandi kóðum:<br /><br /> * Ef afmörkunarreiturinn er auður er ný eftirspurn búin til án birgðageymslu- eða afbrigðiskóta.<br /><br /> * Ef fleiri en ein afmörkun er skilgreind verður nýja framboðið stofnað fyrir fyrsta afmörkunargildið samkvæmt röðunaraðferðinni.<br /><br /> Ef nota á annað afbrigði eða annan birgðageymslukóta þarf að breyta því handvirkt í nýju áætlunarlínunni.|  
    |**Lagfæra framboð sjálfkrafa**|Fínstillir nýtt framboð sem var búið til á grafinu með því að tryggja að það myndi engar birgðir á undan næsta framboði.|  
    |**Eyða framboði**|Eyðir einingu í Flýtiflipanum **Tímaás** og eyðir áætlunarlínunni þegar valið er **Vista breytingar**. Táknið breytist í disk sem hefur rauðan kross þegar framboði hefur verið eytt.<br /><br /> **Athugið:** Aðeins er hægt að eyða framboði aðgerðaskilaboða af gerðinni **Nýtt**. Eftir að hafa valið **Vista breytingar**, verður að eyða handvirkt viðkomandi áætlunarlínu í áætlun eða innkaupatillögubók.|  

7.  Veljið **Endurstilla** ef á að endurstilla allar breytingar sem hafa verið gerðar eftir að glugginn **Vara til ráðstöfunar eftir tímalínu** er opnaður eða veldu **Endurstilla**.  
8. Þegar einingar hafa verið settar þar sem þær eiga að vera í skýringarmyndinni skal velja **Vista breytingar** til að afrita breytt magn og dagsetningarbreytingar í áætlunar- eða beiðnilínurnar sem tákna myndrænu einingarnar.  

Til að virkja breytingar á framboðsáætluninni þarf að fylgja aðgerðarboðunum sem koma úr áætlunar- eða beiðnivinnublaðinu. Frekari upplýsingar, sjá Framkvæma aðgerðarboðaáætlun.

## <a name="symbols-and-icons-on-the-timeline-fasttab"></a>Tákn og táknmyndir í flýtiflipa tímalínu

 |Tákn/ táknmynd|Lýsing|  
 |------------------|---------------------------------------|  
 |Black cross|Pantanir (bæði framboð og eftirspurn).<br /><br /> -   Má ekki breyta.<br />-   Sjáanleg þegar reiturinn **Sýna áætlaðar birgðir** er valinn (appelsínugult myndrit).|  
 |Rauður hringur|Núverandi framboðspantanir sem eru ekki í áætlunartillögum.<br /><br /> -   Má ekki breyta.<br />-   Sjáanleg þegar reiturinn **Sýna áætlaðar birgðir** er valinn (appelsínugult myndrit).|  
 |Gul stjarna|Spá um eftirspurn.<br /><br /> -   Má ekki breyta.<br />-   Sjáanleg þegar reiturinn **Heiti spár** hefur gildi.<br /><br /> Ef bæði reitirnir **Sýna áætlaðar birgðir** og **Taka með áætlunartillögur** eru valdir hefur hver gul stjarna samsvarandi stjörnu í hinu línuritinu. Þetta sýnir hvernig tillaga um framboð uppfyllir eftirspurnarspána.|  
 |Grænn hringur með tákni sem lagað er eins og diskur með rauðum krossi|Tillögð framboðspöntun með aðgerðaboðunum *Hætta við*.<br /><br /> -   Má ekki breyta.<br />-   Sjáanleg þegar reiturinn **Taka með áætlunartillögur** er valinn (grænt línurit).|  
 |Grænn hringur með tákni sem lagað er eins og diskur með stjörnu|Tillagðar framboðspöntun með aðgerðaboðunum *Nýtt*.<br /><br /> -   Má breyta.<br />-   Sjáanleg þegar reiturinn **Taka með áætlunartillögur** er valinn (grænt línurit).|  
 |Grænn hringur með tákni sem lagað er eins og diskur með einni eða tveimur örvum|Tillagðar birgðapantanir með aðgerðarboðunum *Endurtímasetja*, *Breyta magni*, eða *Endurtímasetja og Breyta magni*<br /><br /> -   Má breyta.<br />-   Sjáanleg þegar reiturinn **Taka með áætlunartillögur** er valinn (grænt línurit).<br /><br /> Örvarnar endurspegla stefnu áætlunartillögu. Til dæmis endurspeglar vinstri ör ásamt upp ör aðgerðaboð *Endurtímasetja og Breyta magni* sem samanstanda af afturvirkri endurröðun og aukningu magns.|  

Þegar þú opnar flettilista á **Tímalína** birtast eftirfarandi aðgerðir, eftir því hvar er smellt.  

 |Virkni|Lýsing|  
 |--------------|---------------------------------------|  
 |**Búa til nýtt framboð**|Stofnar nýjan atriðispunkt þar sem fellilisti er opnaður, sem stendur fyrir nýja framboðspöntun sem stungið er upp á. Verður nýja línan í áætlunarvinnublaðinu þegar valið er **Vista breytingar** á flipanum **Vinna**.<br /><br /> Hvers kyns síugildi sem eru skilgreind í reitunum **Staðsetningarsía** eða **Afbrigðisafmörkun** flýtiflipanum **Valkostir** verða jöfnuð við nýju framboðspöntunina. **Athugið:** Ef afmörkunarreitir eru auðir eða hafa fleiri en eitt afmörkunargildi verður nýja framboðspöntunin stofnuð með því að nota eftirfarandi kóða: <ul><li>Ef afmörkunarreiturinn er auður er ný eftirspurn búin til án birgðageymslu- eða afbrigðiskóta.</li><li>Ef fleiri en ein afmörkun er skilgreind verður nýja framboðið er stofnað með því að nota fyrsta afmörkunargildið samkvæmt röðunarstefnunni.</li></ul> Ef nota á annað afbrigði eða annan birgðageymslukóta í nýju birgðapöntuninni þarf að breyta því handvirkt í nýju áætlunarlínunni.|  
 |**Lagfæra framboð sjálfkrafa**|Fínstillir nýtt framboð sem var búið til á grafinu með því að tryggja að það myndi engar birgðir á undan næsta framboði.|  
 |**Eyða framboði**|Eyðir einingu í flýtiflipanum **Tímaás** og eyðir áætlunarlínunni þegar valið er **Vista breytingar** á flipanum **Vinna**. Táknið breytist í disk með rauðum krossi þegar framboði hefur verið eytt. **Athugið:** Aðeins er hægt að eyða framboði aðgerðaskilaboða af gerðinni *Nýtt*. Eftir að hafa valið **Vista breytingar** á flipanum **Vinna**, verður að eyða handvirkt viðkomandi áætlunarlínu í áætlun eða innkaupatillögubók.|  
 |**Sýna Fylgiskjal**|Opnar pöntun, áætlunarlínu eða -spá sem einingin stendur fyrir.|  
 |**Minni aðdráttur (Ctrl++)**|Gerir kvarðann af x-ásnum stærri, þannig að færri dagar eru sýndir. **Athugið:** Einnig er hægt að gera þetta með því að styðja á Ctrl + flett músinni hjólið.|  
 |**Meiri aðdráttur (Ctrl+-)**|Gerir kvarðann af x-ásnum minni, þannig að fleiri dagar eru sýndir. **Athugið:** Einnig er hægt að gera þetta með því að styðja á Ctrl + flett músinni hjólið.|  
 |**Endurstilla aðdrátt (Ctrl+0)**|Færir kvarða x-áss aftur í sama horf og fyrir aðdrátt.|  

Auk lyklaborðsaðgerðanna sem áður var minnst á er einnig hægt að nota eftirfarandi lyklaborðsaðgerðir á flipanum **Tímalína**.  

 |Aðgerð á lyklaborði|Lýsing|  
 |---------------------|---------------------------------------|  
 |Ctrl + flettihjól á mús|Breytir kvarða x-ássins.|  
 |Veljið einingu og styðjið svo á Shift+ör|Flytur eininguna í stefnu örvarinnar.|  
 |Dálklykill|Fer yfir í næstu einingu.|  
 |SHIFT+DÁLKLYKILL|Fer yfir í fyrri einingu.|  
 |Ýtið á Esc á meðan einingin er flutt.|Hættir við flutning. **Athugið:** Virkar ekki ef notandinn hefur sleppt músarhnappinum.|

## <a name="see-also"></a>Sjá einnig  
[Áætlun](production-planning.md)   
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)    
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)   
[Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

