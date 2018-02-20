---
title: "Hvernig á að færa vörur eftir þörfum í einfaldri grunngerð vöruhúsa | Microsoft Docs"
description: "Stundum getur verið þörf á því að færa vörur á milli innri hólfa, ekki móttöku- eða sendingarhólfa, á sérstakra krafna frá upprunaskjali. Þessar tilfallandi hreyfingar gætu verið gerðar, til dæmis til að endurskipuleggja vöruhúsið, til að færa vörur í skoðunarsvæði eða til að flytja aukavörur í og úr framleiðslusvæði án kerfistengsla við upprunaskjal framleiðslupöntunar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 5c64734d9bb5cced1dbe9cb9c98385004885fa67
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="move-items-ad-hoc-in-basic-warehouse-configurations"></a>Færa vörur eftir þörfum í einfaldri grunngerð vöruhúsa
Stundum getur verið þörf á því að færa vörur á milli innri hólfa, ekki móttöku- eða sendingarhólfa, á sérstakra krafna frá upprunaskjali. Þessar tilfallandi hreyfingar gætu verið gerðar, til dæmis til að endurskipuleggja vöruhúsið, til að færa vörur í skoðunarsvæði eða til að flytja aukavörur í og úr framleiðslusvæði án kerfistengsla við upprunaskjal framleiðslupöntunar.  

Í einfaldri vöruhúsagrunnstillingu, þ.e. birgðageymslum sem nota uppsetningarreitinn **Hólf áskilið** og hugsanlega uppsetningarreitina **Krefjast tínslu** og **Þarf að ganga frá**, er hægt að skrá tilfallandi hreyfingar án upprunaskjala á eftirfarandi hátt:  

    - Með glugganum **Innri hreyfing**.  
    - Með glugganum **Vöruh.endurflokkunarbók**.  

> [!NOTE]  
>  Í ítarlegri vöruhúsagrunnstillingu, þ.e. birgðageymslum sem nota uppsetningarreitinn **Beinn frágangur og tínsla** er glugginn **Vinnublað hreyfingar**, **Innri vöruhúsatínsla** eða **Innri vöruhúsafrágangur** notaður til að færa vörur á milli hólfa eftir þörfum.  

## <a name="to-move-items-as-an-internal-movement"></a>Til að færa vörur sem innri hreyfingu  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innri hreyfing** og velja svo viðeigandi tengil.  
2.  Á flýtiflipanum **Almennt** er reiturinn **Nr.** fylltur út reitinn, annaðhvort með því að fara úr reitnum eða með því að velja hnappinn **AðstoðBreyta** til að velja úr númeraröð.  
3.  Í reitnum **Kóti birgðageymslu** er færð inn birgðageymslan þar sem hreyfingin á sér stað.  

    Ef birgðageymslan er sett upp sem sjálfgefin birgðageymsla sem starfsmaður vöruhúss er kóti birgðageymslu settur inn sjálfkrafa.  
4.  Í reitnum **Kóti til-hólfs** skal færa inn kóta fyrir hólfið sem færa á vöruna í. Við framleiðslu getur þetta t.d. verið hólfkóti opins vinnslusalar eins og skilgreint er á birgðageymsluspjaldinu eða í vinnustöð.  
5.  Í reitunum **Gjalddagi** er færð inn sú dagsetning sem hreyfingu verður að vera lokið.  
6.  Á flýtiflipanum **Línur** skal velja reitinn **Vörunr.** til að opna gluggann **Innihaldslisti hólfs** og velja síðan vöru til að færa, á grundvelli ráðstöfunar hennar í hólfum. Einnig er hægt að velja **Sækja innihald hólfs** til að fylla innri hreyfingalínur út frá afmörkunum notanda. Frekari upplýsingar, sjá ábendinguna fyrir aðgerðina **Sækja hólfainnihald**   

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

    Eftirstöðvar af tilfallandi hreyfingu eru framkvæmdar í glugganum **Birgðahreyfing** á sama hátt og gert er fyrir hreyfingar á grundvelli upprunaskjala. Frekari upplýsingar, sjá til dæmis [Færa íhluti á aðgerðasvæði með einföldum vöruhúsaaðgerðum](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  

## <a name="to-move-items-with-the-item-reclassification-journal"></a>Til að færa vörur með vöruendurflokkunarbók
Í staðinn fyrir að nota vöruhúsahreyfing skjöl, geturðu skráð vöruhreyfingu með því að endurflokka hólfakóða varanna. Nánari upplýsingar er að finna í [Telja, leiðrétta og endurflokka birgðir](inventory-how-count-adjust-reclassify.md).   
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðaendurflokkunarbók** og velja svo viðeigandi tengil.  
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
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

