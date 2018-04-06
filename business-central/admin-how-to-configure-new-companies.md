---
title: "Hvernig á að grunnstilla ný fyrirtæki | Microsoft Docs"
description: "Hægt er að skilgreina og sérstilla nýtt fyrirtæki sem búið var til. Til að fínstilla innleiðinguna framkvæmirðu grunnstillinguna þína í þremur skrefum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b9e701f102f1a2fc7ccbd4882dfec37f65cfe3b7
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies"></a>Grunnstilla ný fyrirtæki
Til að grunnstilla nýtt fyrirtæki innleiðingarlausn þinni er vanalega fylgt eftir þremur áföngum. Í fyrsta áfanganum er grunnstillingarpakkinn fluttur inn, sem er .rapidstart-skrá með grunnstillingarupplýsingum. Í öðrum áfanganum er grunnstillingarupplýsingum breytt og þær notaðar á nýja fyrirtækið. Í lokaáfanganum er farið yfir og villur lagaðar.  

Eftirfarandi ferli gera ráð fyrir að grunnstillingarpakkar hafi verið stofnaðir og vistaðir. Nánari upplýsingar eru í [Undirbúa grunnstillingarpakka](admin-how-to-prepare-a-configuration-package.md).  

Eftirfarandi ferli gerir ráð fyrir að þú hafir frumstillt og opnað nýja fyrirtækið og að þú sért að nota Mitt hlutverk RapidStart Services innleiðara.

## <a name="to-import-a-configuration-package"></a>Til að flytja inn grunnstillingarpakka.  
1. Nýja fyrirtækið er opnað í [!INCLUDE[d365fin](includes/d365fin_md.md)] gagnagrunninum.  
2. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarpakkar** og velja svo viðeigandi tengil.  
3. Velja skal aðgerðina **Flytja inn pakka**.  
4. Farið er í staðsetninguna þar sem .rapidstart grunnstillingarpakkaskráin var vistuð og velja svo hnappinn **Opna**.  
5. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fyrirtækjaupplýsingar** og velja svo viðeigandi tengil. Færa inn upplýsingar um fyrirtækið í upplýsingakorti fyrirtækisins. Hafa upplýsingar með eins og bankaupplýsingar. Einnig er hægt setja inn lógó fyrirtækisins.  

Allar töflurnar sem búið er að tákna að verði teknar með í nýja fyrirtækinu eru fluttar inn. Á þessum tímapunkti er hægt að jafna pakkagögn í gagnagrunninn eða leiðrétta og breyta töflugögnum til að uppfylla lýsingar viðskiptamanns.  

## <a name="to-apply-package-data"></a>Til að nota pakkagögn  
1. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarvinnublað** og velja svo viðeigandi tengil.  
2. Valin er tafla þar sem á að breyta gögnum og svo er valin aðgerðin **Nota gögn**. Velja hnappinn **Já** til að staðfesta jöfnun.
3. Til að staðfesta að gögnin séu nú í gagnagrunninum og að jöfnunin hafi tekist skal fara aftur í gluggann **Grunnstillingarvinnublað** og velja aðgerðina **Gagnagrunnsgögn**.  

> [!NOTE]  
>  Eftir að gögn hafa verið notuð, er aðeins hægt að skoða þau í gagnagrunninum. Hún er ekki lengur í pakkanum.  

## <a name="to-modify-and-apply-package-data"></a>Til að breyta og nota gögn pakka  
1. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarvinnublað** og velja svo viðeigandi tengil.  
2. Valin er tafla þar sem á að breyta gögnum og svo velja aðgerðina **Pakkagögn**.  
3. Gera skal breytingarnar í glugganum **Grunnstilling pakkafærslna**. Til dæmis er hægt að eyða valkostum sem eiga ekki við.  
4. Veldu aðgerðina **Nota gögn** og veldu síðan hnappinn **Í lagi**.  
5. Til að staðfesta að gögnin séu nú í gagnagrunninum og að jöfnunin hafi tekist skal fara aftur í gluggann **Grunnstillingarvinnublað** og velja aðgerðina **Gagnagrunnsgögn**.  

## <a name="to-locate-and-identify-a-configuration-error"></a>Til þess að finna og auðkenna skilgreiningarvillu  
Ákveðnar villugerðir geta komið upp þegar gögn eru notuð á gagnagrunn. Algengasta villan er að nauðsynlegar tengdar töflur voru ekki innifaldar. Þannig vilur eru lagaðar í grunnstillingarvinnublaðinu.

1. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarpakkar** og velja svo viðeigandi tengil.  
2. Pakkinn er valinn sem þú vilt yfirfara og síðan skal velja aðgerðina **Breyta**.  

    Allar töflur sem er með villur eru auðkenndar. Fjölda pakkavillna birtist í reitnum **Fjöldi pakkavillna**.  

3. Velja reitinn **Fj. pakkavilla** til að opna gluggann **Grunnstillingar pakkafærslna** sem sýnir færslur með villum.  

### <a name="to-fix-an-error"></a>Til að laga villu  
1. Opna fyrirtækið sem grunnstillingapakkinn er byggður á.  
2. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarvinnublað** og velja svo viðeigandi tengil.  
3. Laga villur eins og tengdar töflur sem vantar á vinnublaðið.  
4. Bæta töflum við fyrirliggjandi grunnstillingarpakka eða stofna nýjan pakka sem aðeins inniheldur nýju töfluna. Nánari upplýsingar eru í [Undirbúa grunnstillingarpakka](admin-how-to-prepare-a-configuration-package.md).  
5. Enduropna skal nýja fyrirtækið þar sem verið er að innleiða grunnstillingar.  
6. Flytja inn grunnstillingarpakka.  

    > [!NOTE]  
    >  Ef sami pakki er fluttur inn aftur kann að skrifast yfir breytingar sem þegar hafa verið gerðar á gögnum. Af þeirri ástæðu gæti verið ráðlegt að setja nýjar töflur í nýja pakka og flytja þá inn í staðinn.  

7. Nota gögnin í gagnagrunninum eins og lýst er í kaflanum „Til að breyta og nota gögn pakka.“

## <a name="see-also"></a>Sjá einnig  
[Nota skilgreiningu á ný fyrirtæki](admin-apply-configuration-to-new-companies.md)  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)

