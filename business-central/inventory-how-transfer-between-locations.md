---
title: Flytja vörur á milli birgðageymslna| Microsoft Docs
description: Lýsir hvernig á að flytja birgðir frá einum stað eða vörugeymslu til annars, annaðhvort með endurflokkunarfærslubók eða með flutningsfyrirmæli.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f406a44a3d786c06ea1ac1e61d5b51bb97b67f12
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746142"
---
# <a name="transfer-inventory-between-locations"></a>Flytja birgðir milli birgðageymslna
Það er hægt að flytja birgðavörur milli tveggja staða með því að búa til flutningspantanir. Einnig er hægt að nota vöruendurflokkunarbók.

Með flutningspöntun eru flutningar á útleið fluttir frá einum stað og tekið á móti flutningum á innleið á hinum staðnum. Þannig er hægt að stjórna vöruhúsaaðgerðunum og meira öryggi er fyrir því að birgðamagn sé rétt uppfært.

Með vöruendurflokkunarbók þarf einfaldlega að fylla inn í reitina **Staðsetningarkóði** og **Nýr staðsetningarkóði**. Þegar bókin er bókuð eru færslur birgðahöfuðbókar aðlagaðar þeirri staðsetningu sem um ræðir. Vöruhúsaaðgerðum er ekki stjórnað með þessari aðferð.

> [!NOTE]  
>   Ef þú hefur hluti skráð í birgðum þínum án staðsetningar kóða, t.d. frá því að þú átt aðeins eitt vörugeymsla, þá getur þú ekki flutt þau vörur með því að nota flutningsfyrirmæli. Þess í stað verður þú að nota endurflokkunarskýrsluna til að endurflokka atriði úr autt staðarnúmeri í raunverulegan staðarnúmer.  Nánari upplýsingar er að finna í skrefi 3 í [Að flytja vörur með vöruendurflokkunarbók](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).

Staðsetning og flutningsleiðir þurfa að vera uppsett til að flytja vörur. Nánari upplýsingar er að finna í [Setja upp birgðageymslur](inventory-how-setup-locations.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>Vörur fluttar með flutningspöntun
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Flutningspantanir** og veldu síðan tengda tengilinn.
2. Fyllt er út í reiti eftir því sem á við í haus síðunnar **Millifærslupöntun**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Ef búið er að fylla út reitina **Millifærslukóði**, **Flutningsaðilakóði** og **Flutningsþjónusta** á síðunni **Lýsing millifærsluleiðar** þegar flutningsleið var sett upp, fyllir kerfið sjálfkrafa út samsvarandi reiti á millifærslupöntuninni.

    Þegar fyllt er út í reitinn **Flutningsþjónusta** reiknar kerfið út móttökudagsetningu fyrir flutt-til birgðageymslu með því að bæta flutningstíma flutningsþjónustunnar við afhendingardagsetninguna.

3. Til að fylla út í línurnar skal annaðhvort færa þær inn handvirkt eða velja einn eftirfarandi valkosta á undir aðgerðinni **Aðgerðir**:
    - Veldu **Sækja innihald hólfs** aðgerðina til að velja fyrirliggjandi vörur úr tilteknu hólfi á staðsetningunni.
    - Veldu **Sækja móttökulínur** til að velja vörur sem eru nýkomnar á sendist-frá staðsetningu.   

    Sem starfsmaður vörugeymslu við flutninginn frá staðsetninginni skaltu halda áfram að senda vörurnar.
4. Veldu aðgerðina **Bóka** veldu **Senda** valkostinn og veldu síðan **Í lagi** hnappinn.

    Atriðin eru nú í flutningi milli tilgreindra staða, í samræmi við tilgreint flutningsleið.

    Sem starfsmaður vörugeymslu við flutninginn frá staðsetninginni skaltu halda áfram að fá vörurnar. Flutningspöntunarlínurnar eru þær sömu og við sendingu og er ekki hægt að breyta þeim.
5. Veldu aðgerðina **Bóka**, veldu **Móttaka** valkostinn og veldu síðan **Í lagi** hnappinn.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Til að flytja vörur með vöruendurflokkunarbók
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vöruendurflokkunarbók** og veldu síðan tengda tengilinn.
2. Á síðunni **Birgðaendurflokkunarbók** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Í reitnum **Kóði birgðageymslu** er færð inn birgðageymslan þar sem vörurnar eru nú geymdar.

    > [!NOTE]  
    >   Til að flytja hluti sem ekki hafa staðsetningarkóða skal skilja reitinn **Staðsetningarkóða** eftir auðan.
4. Í reitnum **Nýr staðsetningarkóði**, sláðu inn staðinn sem þú vilt flytja hlutina í.
5. Valið er **Bóka** aðgerðin.

## <a name="see-also"></a>Sjá einnig
[Stjórna birgðum](inventory-manage-inventory.md)  
[Uppsetning birgðageymsla](inventory-how-setup-locations.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]