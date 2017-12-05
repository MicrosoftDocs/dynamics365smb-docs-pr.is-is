---
title: "Búa til samskipti á tengiliði og hluta| Microsoft Docs"
description: "Lýsir hvernig á að stofna samskipti á milli þín og tengiliða og hluta í Dynamics 365, eins og til dæmis beint tölvupóstsamband."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/15/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 57cbc08ab2e05777fae54018fe714d44b64d14e0
ms.contentlocale: is-is
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-create-interactions-on-contacts-and-segments"></a>Hvernig á að stofna Samskipti á tengiliðum og hlutum
Hægt er að stofna samskipti til að skrá öll samskipti við viðskiptavinina og hlutana, til dæmis markpóstur.

Áður en hægt er að stofna samskipti þarf að setja upp samskiptasniðmát. Til að fá nánari upplýsingar sjá  [Setja upp samskiptasniðmát](marketing-interactions.md).

## <a name="to-create-an-interaction"></a>Til að stofna samskipti
1. Opna færslu um tengilið, sölumann eða samskiptaskráningarfærslu.
2. Valið er **Stofna samskipti** aðgerð.
3. Fyllið út reitina og smellið á hnappinn **Í lagi**.

> [!NOTE]  
>   Ef framkvæma þarf annað verk áður en samskiptunum lýkur er hægt velja **hætta við** og ljúka samskiptunum síðar. Þetta frestar samskiptunum.

## <a name="to-finish-and-delete-postponed-interactions"></a>ljúka og eyða frestuðum samskiptum
1. Opna færslu um tengilið, sölumann eða samskiptaskráningarfærslu.
2. Velja **Frestuð samskipti**
3. Veljið samskiptin sem á að ljúka og veldu svo aðgerðina **halda áfram**.

## <a name="to-create-an-interaction-on-a-segment"></a>Til að stofna samskipti á hluta.
1. Á heimasíðunni skal velja **Virkir hlutar** eða veljið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Hlutar** og velja svo viðeigandi tengil.
2. Á **hlutaglugganum** í hlutanum **samskipti** er fyllt í reitina til að tilgreina hvers konar samskiptum eigi að úthluta á hlutann.

    Þegar samskiptum hefur verið úthlutað á hluta er hægt að sérsníða samskiptin fyrir hvern einstakan tengilið innan hlutans, til dæmis með því að velja annað samskiptasniðmát í línunum í glugganum **Hluti**.  
3. Til að skrá hlutann og samskiptin veldu aðgerðina **kladdi**. Glugginn **Skrá hluta** opnast.
4. Ef stofna á nýjan hluta með sömu tengiliðum skal velja gátreitinn **Stofna eftirfylgnihluta**. Ef forritið á að geta stofnað eftirfylgnihluta verður að tilgreina númeraraðir fyrir hluta í glugganum **Tengslastjórnunargrunnur**.

Samskipti eru skráð fyrir hvern tengilið í hlutanum í töflunni **samskiptaskráningarfærsla** og hlutinn er skráður. Skráðir hlutar eru í glugganum **Skráðir hlutar**.

Ef gátreiturinn **Stofna eftirfylgnihluta** er valinn verður nýr hluti búinn með sömu tengiliðum og hlutinn sem var verið að skrá.

## <a name="see-also"></a>Sjá einnig
[Samskipti skráð](marketing-interactions.md)  
[Vinna með tengiliði](marketing-contacts.md)  
[Umsjón sölutækifæra](marketing-manage-sales-opportunities.md)  
[Uppsetning tengslastjórnunar](marketing-setup-marketing.md)  
[Unnið með Dynamics 365](ui-work-product.md)

