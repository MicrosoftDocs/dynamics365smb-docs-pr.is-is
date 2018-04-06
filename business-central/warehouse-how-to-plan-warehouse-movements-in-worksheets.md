---
title: "Hvernig á að áætla vöruhúsahreyfingar á vinnublöðum | Microsoft "
description: "Hreyfingar eru áætlaðar á vinnublaðinu með hólfaáfyllingu eða með handvirkri áætlun á línum sem á að stofna sem hreyfingaleiðbeiningar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0f518b96cb21a9637ae9b6e64e4c9e22a5fc6512
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="plan-warehouse-movements-in-worksheets"></a>Áætla vöruhúsahreyfingar á vinnublöðum
Hreyfingar eru áætlaðar á vinnublaðinu með hólfaáfyllingu eða með handvirkri áætlun á línum sem á að stofna sem hreyfingaleiðbeiningar.  

## <a name="to-calculate-a-replenishment-movement"></a>Áfyllingarhreyfingar reiknaðar:  
Jafnframt því sem vörur eru sendar viðskiptamönnum úr vöruhúsi, fækkar vörunum í hólfunum með hæstu hólfaflokkunina. Til að fylla á þessi hólf með vörum úr öðrum hólfum er keyrð aðgerðin **Reikna út áfyllingu hólfs** í **Hreyfing Vinnublað** glugganum.

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Hreyfingarvinnublað** og velja svo viðeigandi tengil.  
2.  Velja skal aðgerðina **Reikna áfyllingu hólfs**.  

    [!INCLUDE[d365fin](includes/d365fin_md.md)] stofnar línur sem gefa nákvæmlega til kynna hvernig færa á vörur úr lægra flokkuðum hólfum í hærra flokkuð.  

    > [!NOTE]  
    >  Stungið er upp á hreyfingu í samræmi við FEFO aðgerðin **Stofna hreyfingu** er virkjuð ef eftirfarandi skilyrðum fyrir vöru er fullnægt:  
    >   
    >  -   Varan er fyrningadagsett.  
    > -   Gátreiturinn **Tína eftir FEFO** í birgðageymsluspjaldinu er valinn.  
    > -   Gátreiturinn **Hólf áskilið** á birgðageymsluspjaldinu er valið.  
    > -   Reitirnir **Frá svæði** og **Frá hólf** eru auðir.  

    Frekari upplýsingar eru í [Tínsla skv. FEFO](warehouse-picking-by-fefo.md).  

3.  Farið er yfir línurnar og þeim breitt eftir þörfum eða eytt ef ekki er tími til að framkvæma þær allar.  
4.  Velja aðgerðina **Stofna hreyfingu** til að búa til vöruhúsaleiðbeiningar fyrir aðgerðir starfsmanna vöruhúss.  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a>Með aðgerðinni sækja innihald hólfs er hægt að sækja allt sem er í einu eða fleiri hólfum:  
Einnig er hægt að nota vinnublað hreyfinga til að áætla aðrar hreyfingar á birgðum innan vöruhússins. Þegar setja á vörur í hólf fyrir gæðaeftirlit, til dæmis, er hægt að nota vinnublað hreyfinga til að áætla aðgerðina og stofna síðan hreyfingu til að útbúa fyrirmæli fyrir starfsmann.  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Hreyfingarvinnublað** og velja svo viðeigandi tengil.  
2.  Valið er **Sækja innihald hólfs** aðgerð. Beiðniglugginn er notaður til að afmarka það hvaða hólf og vörur skuli birtast í hreyfingavinnublaðslínunum.  
3.  Reitirnir í keyrsluglugganum eru fylltir út. Eigi t.d. að skoða innihald allra hólfa á vissu svæði í birgðageymslunni er reiturinn **Svæðiskóti** . Eigi að sækja línur fyrir hvert hólf sem tiltekin vara er í er reiturinn **Vörunr.** fylltur út.  

    > [!NOTE]  
    >  Ekki er hægt að færa vörur handvirkt inn og út úr hólfi af gerðinni RECEIVE því vörur sem eru í hólfi af þeirri gerð verður að skrá sem frágengnar áður en þær verða hluti af tiltækum birgðum.  

4.  Ef sækja á margar línur skal velja **Raða** til að velja röðunaraðferð til að ákveða í hvaða röð línurnar birtast á vinnublaðinu og síðan skal velja hnappinn **Í lagi**.  

    > [!NOTE]  
    >  Hreyfingalínur eru sóttar í samræmi við FEFO aðgerðin **Sækja hólfaefni** er virkjuð ef eftirfarandi skilyrðum fyrir vöru er fullnægt:  
    >   
    >  -   Varan er fyrningadagsett.  
    > -   Gátreiturinn **Tína eftir FEFO** í birgðageymsluspjaldinu er valinn.  
    > -   Gátreiturinn **Hólf áskilið** á birgðageymsluspjaldinu er valið.  
    > -   Reitirnir **Frá svæði** og **Frá hólf** eru auðir.  

5.  Reitir í einhverjum línunum sem voru sóttar eru fylltir út til að breyta eins og þarf. Fyrir hverja vöru sem á að færa þarf að fylla út reitina **Vörunr.**, **Kóti frá-hólfs**, **Kóti til-hólfs** og **Magn**.  
6.  Línum sem ekkert er fært í skal eytt.  
7.  Þegar línur hreyfingavinnublaðsins eru orðnar eins og þær eiga að vera skal velja aðgerðina **Stofna hreyfingu** til að útbúa leiðbeiningarnar fyrir starfsmanninn.  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

