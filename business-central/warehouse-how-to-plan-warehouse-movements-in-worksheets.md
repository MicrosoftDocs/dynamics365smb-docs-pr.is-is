---
title: 'Hvernig á að áætla vöruhúsahreyfingar á vinnublöðum | Microsoft '
description: Hreyfingar eru áætlaðar á vinnublaðinu með hólfaáfyllingu eða með handvirkri áætlun á línum sem á að stofna sem hreyfingaleiðbeiningar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1ec80435211b139868bf62ddf0ce269a802d2abc
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534049"
---
# <a name="plan-warehouse-movements-in-worksheets"></a>Áætla vöruhúsahreyfingar á vinnublöðum

Hreyfingar eru áætlaðar á vinnublaðinu með hólfaáfyllingu eða með handvirkri áætlun á línum sem á að stofna sem hreyfingaleiðbeiningar.  

## <a name="to-calculate-a-replenishment-movement"></a>Áfyllingarhreyfingar reiknaðar:

Jafnframt því sem vörur eru sendar viðskiptamönnum úr vöruhúsi, fækkar vörunum í hólfunum með hæstu hólfaflokkunina. Til að fylla á þessi hólf með vörum úr öðrum hólfum er keyrð aðgerðin **Reikna út áfyllingu hólfs** á **Hreyfing Vinnublað** síðunni

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað hreyfingar** og velja síðan viðkomandi tengil.  
2.  Velja skal aðgerðina **Reikna áfyllingu hólfs**.  

    [!INCLUDE[prod_short](includes/prod_short.md)] stofnar línur sem gefa nákvæmlega til kynna hvernig færa á vörur úr lægra flokkuðum hólfum í hærra flokkuð.  

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

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað hreyfingar** og velja síðan viðkomandi tengil.  
2.  Valið er **Sækja innihald hólfs** aðgerð. Beiðnisíðan er notuð til að afmarka það hvaða hólf og vörur skuli birtast í hreyfingavinnublaðslínunum.  
3.  Reitirnir á keyrslusíðunni eru fylltir út. Eigi t.d. að skoða innihald allra hólfa á vissu svæði í birgðageymslunni er reiturinn **Svæðiskóti** . Eigi að sækja línur fyrir hvert hólf sem tiltekin vara er í er reiturinn **Vörunr.** fylltur út.  

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

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/move-items/)

## <a name="see-also"></a>Sjá einnig .

[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
