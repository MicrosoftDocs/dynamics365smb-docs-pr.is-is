---
title: Hvernig á að færa vörur eftir þörfum í einfaldri grunngerð vöruhúsa | Microsoft Docs
description: Stundum getur verið þörf á því að færa vörur á milli innri hólfa, ekki móttöku- eða sendingarhólfa, á sérstakra krafna frá upprunaskjali. Þessar tilfallandi hreyfingar gætu verið gerðar, til dæmis til að endurskipuleggja vöruhúsið, til að færa vörur í skoðunarsvæði eða til að flytja aukavörur í og úr framleiðslusvæði án kerfistengsla við upprunaskjal framleiðslupöntunar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2ada7dbf658517332af029571a63726eef038546
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391550"
---
# <a name="move-items-ad-hoc-in-basic-warehouse-configurations"></a>Færa vörur eftir þörfum í einfaldri grunngerð vöruhúsa
Stundum getur verið þörf á því að færa vörur á milli innri hólfa, ekki móttöku- eða sendingarhólfa, á sérstakra krafna frá upprunaskjali. Þessar tilfallandi hreyfingar gætu verið gerðar, til dæmis til að endurskipuleggja vöruhúsið, til að færa vörur í skoðunarsvæði eða til að flytja aukavörur í og úr framleiðslusvæði án kerfistengsla við upprunaskjal framleiðslupöntunar.  

Í einfaldri vöruhúsagrunnstillingu, þ.e. birgðageymslum sem nota uppsetningarreitinn **Hólf áskilið** og hugsanlega uppsetningarreitina **Krefjast tínslu** og **Þarf að ganga frá**, er hægt að skrá tilfallandi hreyfingar án upprunaskjala á eftirfarandi hátt:  

- Með síðunni **Innri hreyfing**.  
- Með síðunni **Vöruh.endurflokkunarbók**.  

> [!NOTE]  
>  Í ítarlegri vöruhúsagrunnstillingu, þ.e. birgðageymslum sem nota uppsetningarreitinn **Beinn frágangur og tínsla** er síðan **Vinnublað hreyfingar**, **Innri vöruhúsatínsla** eða **Innri vöruhúsafrágangur** notuð til að færa vörur á milli hólfa eftir þörfum.  

## <a name="to-move-items-as-an-internal-movement"></a>Til að færa vörur sem innri hreyfingu  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innri hreyfing** og veldu síðan tengda tengilinn.  
2.  Á flýtiflipanum **Almennt** er reiturinn **Nr.** fylltur út reitinn, annaðhvort með því að fara úr reitnum eða með því að velja hnappinn **AðstoðBreyta** til að velja úr númeraröð.  
3.  Í reitnum **Kóti birgðageymslu** er færð inn birgðageymslan þar sem hreyfingin á sér stað.  

    Ef birgðageymslan er sett upp sem sjálfgefin birgðageymsla sem starfsmaður vöruhúss er kóti birgðageymslu settur inn sjálfkrafa.  
4.  Í reitnum **Kóti til-hólfs** skal færa inn kóta fyrir hólfið sem færa á vöruna í. Við framleiðslu getur þetta t.d. verið hólfkóti opins vinnslusalar eins og skilgreint er á birgðageymsluspjaldinu eða í vinnustöð.  
5.  Í reitunum **Gjalddagi** er færð inn sú dagsetning sem hreyfingu verður að vera lokið.  
6.  Á flýtiflipanum **Línur** skal velja reitinn **Vörunr.** til að opna síðuna **Innihaldslisti hólfs** og velja síðan vöru til að færa, á grundvelli ráðstöfunar hennar í hólfum. Einnig er hægt að velja **Sækja innihald hólfs** til að fylla innri hreyfingalínur út frá afmörkunum notanda. Frekari upplýsingar, sjá ábendinguna fyrir aðgerðina **Sækja hólfainnihald**   

    Þegar varan hefur verið valin er reiturinn **Kóði frá-hólfs** sjálfkrafa fylltur út samkvæmt innihaldi valins hólfs, en hægt er að breyta honum í öll önnur hólf þar sem varan er tiltæk.  

    > [!NOTE]  
    >  Þar sem reiturinn **Vörunr.** og reiturinn **Kóti frá-hólfs** eru tengdir geta gildi þeirra breyst innbyrðis háð hinum þegar öðrum hvorum reitnum er breytt.  

    Reiturinn **Kóði til-hólfs** er fylltur með gildinu sem fært var inn í hausinn en hægt er að breyta því á línunni í hvaða annan hólfakóða sem er ekki lokaður eða frátekinn í ákveðnum tilgangi. Nánari upplýsingar um hvernig sérnýtt hólf eru útbúin eru í Sérnýtt.  
7.  Þegar búið er að skilgreina hvaða hólf á að færa vörur í og úr skal færa flutningsmagnið inn í reitinn **Magn**.  

    > [!NOTE]  
    >  Magn verður að vera tiltækt í kóta Frá hólfs.  

8.  Þegar þú ert reiðubúinn til þess að vinna innri hreyfinguna skal velja **Stofna birgðahreyfingu** aðgerðina.  

    > [!NOTE]  
    >  Þegar búið er að stofna birgðahreyfinguna er innri hreyfingarlínunum eytt.  

    Eftirstöðvar af tilfallandi hreyfingu eru framkvæmdar á síðunni **Birgðahreyfing** á sama hátt og gert er fyrir hreyfingar á grundvelli upprunaskjala. Frekari upplýsingar, sjá til dæmis [Færa íhluti á aðgerðasvæði með einföldum vöruhúsaaðgerðum](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  

## <a name="to-move-items-with-the-item-reclassification-journal"></a>Til að færa vörur með vöruendurflokkunarbók
Í staðinn fyrir að nota vöruhúsahreyfing skjöl, geturðu skráð vöruhreyfingu með því að endurflokka hólfakóða varanna. Nánari upplýsingar er að finna í [Telja, leiðrétta og endurflokka birgðir með færslubókum](inventory-how-count-adjust-reclassify.md).   
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðaendurflokkunarbók** og veldu síðan tengda tengilinn.  
2.  Fyrir hverja bókunarlínu skal skilgreina úr og í hvaða hólf flytja skal vörur með því að fylla út reitna **Hólfakóti** og **Nýr hólfakóti**.  

    1.  Ef flytja á allt innihald hólfs yfir í annað hólf, skal velja aðgerðina **Sækja innihald hólfs**.  
    2.  Færðar eru inn afmarkanir til þess að finna hólfið sem á að flytja innihald úr og síðan er hnappurinn **Í lagi** valinn. Færslubókarlínur eru fylltar út með efni hólfsins.  
3.  Aðrir reitir eru fylltir út fyrir hverja færslubókarlínu.   
4.  Bóka skal endurflokkunarbók.  

    > [!NOTE]  
    >  Ólíkt því sem gildir um hreyfingaskjöl, stofna hreyfingar sem bókaðar eru með endurflokkunarbókinni ekki vöruhúsabeiðni um að framkvæma efnislega verkið.  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]