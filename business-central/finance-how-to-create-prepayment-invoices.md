---
title: "Hvernig skal búa til fyrirframgreiðslureikning | Microsoft Docs"
description: "Lærið að fást við aðstæður þar sem þú eða lánardrottinn þinn krefjast fyrirframgreiðslu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 50b77f4c6e333f3024f2261eb0c6df42b3e535d0
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="create-prepayment-invoices"></a>Stofna fyrirframgreiðslureikninga
Ef viðskiptamenn þurfa að leggja fram greiðslu áður en þeir fá pöntun afhenta eða ef lánardrottin fer fram á greiðslu áður en hann afhendir pöntun er hægt að nota aðgerð fyrirframgreiðslu.  

Þegar búið er að stofna sölu- eða innkaupapöntun er hægt að stofna fyrirframgreiðslureikning. Hægt er að nota sjálfgefnar prósentur fyrir sölu- og innkauplínur eða leiðrétta upphæðina eins og með þarf. Til dæmis er hægt að tilgreina heildarupphæð fyrir alla pöntunina.  

Eftirfarandi ferli sýnir hvernig skal gefa út fyrirframgreiðslureikning fyrir sölupantanir. Skrefin eru svipuð fyrir innkaupapöntun.  

## <a name="to-create-a-prepayment-invoice"></a>Stofnun fyrirframgreiðslureiknings  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.  
2. Stofna skal nýja sölupöntun. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).  

    Á flýtiflipanum **Fyrirframgreiðsla**, er reiturinn **Fyrirframgreiðsla %** fylltur út sjálfkrafa ef sjálfgefin fyrirframgreiðsluprósenta er til staðar í viðskiptamannsspjaldinu. Hægt er að breyta efni þessa reits. Fyrirframgreiðslan er eingöngu afrituð úr hausnum í línur sem ekki afrita sjálfgefna fyrirframgreiðsluprósentu úr vörunni.  

    Ef reiturinn **Þjappa fyrirframgreiðslu** er valinn verða línur sameinaðar á reikningnum ef:  
    - Þær eru með sama fjárhagsreikninginn fyrir fyrirframgreiðslur samkvæmt stillingum í almenna bókunargrunninum.  
    - Þeir hafa sömu víddir.  

    Þessi reitur er hafður auður ef tilgreina á fyrirframgreiðslureikning með einni línu fyrir hverja sölupöntunarlínu sem er með fyrirframgreiðsluprósentu.  

3. Sölulínurnar eru fylltar út.  

    Ef sjálfgefnar fyrirframgreiðsluprósentur hafa verið settar upp fyrir vörurnar eru þær afritaðar sjálfvirkt í reitinn **Fyrirframgreiðsla %** í línunni. Annars er prósentan afrituð úr hausnum. Hægt er að breyta innihaldi reitsins **Fyrirframgreiðsla %** í línunni.  
4. Ef þú vilt jafna eina fyriframgreiðsluprósentu við heildarpöntunina, breyttu þá **Fyrirframgreiðsla %** reitnum á hausnum eftir að hafa fyllt inn í þessar línur.  
5. Veldu **Upplýsingar** aðgerðina til að skoða heildarupphæð fyrirframgreiðslu.

    Ef leiðrétta á heildarupphæð fyrirframgreiðslunnar fyrir pöntunina er hægt að breyta innihaldi reitsins **Upphæð fyrirframgreiðslu** í glugganum **Tölfræði sölupöntunar**.  

    Ef reiturinn **Verð ásamt VSK** er valinn er hægt að breyta reitnum **Upphæð fyrirframgreiðslu með VSK**.  

    Ef þú breytir innihaldi reitsins **Fyrirframgreiðsluupphæð**, mun upphæðinni verða dreift hlutfallslega á milli allra lína, nema þeirra sem hafa **0** í reitnum **Fyrirframgreiðsla %**.  
6. Til að prenta prufuskýrslu áður en fyrirframgreiðslureikningurinn er bókaður skal velja aðgerðina **Fyrirframgreiðsla**, og síðan aðgerðina **Prufuskýrsla fyrirframgreiðslu**.  
7. Til að bóka fyrirframgreiðslureikningurinn skal velja aðgerðina **Fyrirframgreiðsla**, og síðan aðgerðina **Bóka fyrirframgreiðslureikning**.  

    Fyrirframgreiðslureikningur er bókaður og prentaður með því að velja aðgerðina **Bóka og prenta fyrirframgr.reikning**.  

Hægt er að gefa út viðbótar fyrirframgreiðslureikninga fyrir pöntunina. Þetta er gert með því að hækka upphæð fyrirframgreiðslunnar í einni eða fleiri línum, leiðrétta dagsetningu fylgiskjalsins, ef þess þarf, og bóka fyrirframgreiðslureikninginn. Nýr reikningur er stofnaður fyrir mismuninn á milli reikningsfærðra upphæða fyrirframgreiðslu og nýju fyrirframgreiðsluupphæðarinnar.  

> [!NOTE]  
>  Ef þú ert í Norður Ameríku, geturðu ekki breytt fyrirframgreiðsluprósentunni eftir að fyrirframgreiðslureikningurinn hefur verið bókaður. Í N-amerísku útgáfu [!INCLUDE[d365fin](includes/d365fin_md.md)] er komið í veg fyrir þetta, því útreikningur söluskatts yrði annars rangur.  

 Þegar hægt er að bóka restina af reikningnum er hann bókaður eins og hver annar reikningur og fyrirframgreiðsluupphæðin er sjálfvirkt dregin frá þeirri upphæð sem greiða á.  

## <a name="see-also"></a>Sjá einnig  
[Reikningsfærsla fyrirframgreiðslna](finance-invoice-prepayments.md)  
[Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

