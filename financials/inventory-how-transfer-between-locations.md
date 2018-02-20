---
title: "Flytja vörur á milli birgðageymslna| Microsoft Docs"
description: "Lýsir hvernig á að flytja birgðir frá einum stað eða vörugeymslu til annars, annaðhvort með endurflokkunarfærslubók eða með flutningsfyrirmæli."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 01/25/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6a865d8772dc82295545edb65849d69bf5af819c
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="transfer-inventory-between-locations"></a>Flytja birgðir milli birgðageymslna
Það er hægt að flytja birgðavörur milli tveggja staða með því að búa til flutningspantanir. Einnig er hægt að nota vöruendurflokkunarbók.

Með flutningspöntun eru flutningar á útleið fluttir frá einum stað og tekið á móti flutningum á innleið á hinum staðnum. Þannig er hægt að stjórna vöruhúsaaðgerðunum og meira öryggi er fyrir því að birgðamagn sé rétt uppfært.

Með vöruendurflokkunarbók þarf einfaldlega að fylla inn í reitina **Staðsetningarkóði** og **Nýr staðsetningarkóði**. Þegar bókin er bókuð eru færslur birgðahöfuðbókar aðlagaðar þeirri staðsetningu sem um ræðir. Vöruhúsaaðgerðum er ekki stjórnað með þessari aðferð.

> [!NOTE]  
>   Ef þú hefur hluti skráð í birgðum þínum án staðsetningar kóða, t.d. frá því að þú átt aðeins eitt vörugeymsla, þá getur þú ekki flutt þau vörur með því að nota flutningsfyrirmæli. Þess í stað verður þú að nota endurflokkunarskýrsluna til að endurflokka atriði úr autt staðarnúmeri í raunverulegan staðarnúmer.  Nánari upplýsingar er að finna í skrefi 3 í "Til að flytja hluti með hlutanum um endurflokkunarskýrslu" hluta.

Staðsetning og flutningsleiðir þurfa að vera uppsett til að flytja vörur. Nánari upplýsingar er að finna í [Setja upp birgðageymslur](inventory-how-setup-locations.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>Vörur fluttar með flutningspöntun
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Flutningspantanir** og velja svo viðeigandi tengil.
2. Í glugganum **Flutningspöntun** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   Ef búið er að fylla út reitina **Millifærslukóði**, **Flutningsaðilakóði** og **Flutningsþjónusta** í glugganum **Lýsing millifærsluleiðar** þegar flutningsleið var sett upp, fyllir kerfið sjálfkrafa út samsvarandi reiti á millifærslupöntuninni.

    Þegar fyllt er út í reitinn **Flutningsþjónusta** reiknar kerfið út móttökudagsetningu fyrir flutt-til birgðageymslu með því að bæta flutningstíma flutningsþjónustunnar við afhendingardagsetninguna.

    Sem starfsmaður vörugeymslu við flutninginn frá staðsetninginni skaltu halda áfram að senda vörurnar.
3. Veldu aðgerðina **Bóka** veldu **Senda** valkostinn og veldu síðan **Í lagi** hnappinn.

    Atriðin eru nú í flutningi milli tilgreindra staða, í samræmi við tilgreint flutningsleið.

    Sem starfsmaður vörugeymslu við flutninginn frá staðsetninginni skaltu halda áfram að fá vörurnar.
4. Veldu aðgerðina **Bóka**, veldu **Móttaka** valkostinn og veldu síðan **Í lagi** hnappinn.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Til að flytja vörur með vöruendurflokkunarbók
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðaendurflokkunarbækur** og velja svo viðeigandi tengil.
2. Í glugganum **Birgðaendurflokkunarbók** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Í reitnum **Kóði birgðageymslu** er færð inn birgðageymslan þar sem vörurnar eru nú geymdar.

    > [!NOTE]  
>   Til að flytja hluti sem ekki hafa staðsetningarkóða skal skilja reitinn **Staðsetningarkóða** eftir auðan.
4. Í reitnum **Nýr staðsetningarkóði**, sláðu inn staðinn sem þú vilt flytja hlutina í.
5. Valið er **Bóka** aðgerðin.

## <a name="see-also"></a>Sjá einnig
[Stjórna birgðum](inventory-manage-inventory.md)  
[Uppsetning birgðageymsla](inventory-how-setup-locations.md)  

[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Sérstillir þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).  
[Almenn viðskiptavirkni](ui-across-business-areas.md)

