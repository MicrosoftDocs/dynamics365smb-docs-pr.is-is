---
title: Búa til samskipti á tengiliði og hluta| Microsoft Docs
description: Lýsir hvernig á að stofna samskipti á milli þín og tengiliða og hluta í Business Central, eins og til dæmis beint tölvupóstsamband.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 79b92b3e7be6f226fb6c32a55e2ec37a4ac6a363
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181557"
---
# <a name="create-interactions-on-contacts-and-segments"></a>Búa til samskipti á tengiliði og hluta
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
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Hlutar** og veldu síðan tengda tengilinn.
2. Á **Hlutsíðunni** í hlutanum **samskipti** er fyllt í reitina til að tilgreina hvers konar samskiptum eigi að úthluta á hlutann.

    Þegar samskiptum hefur verið úthlutað á hluta er hægt að sérsníða samskiptin fyrir hvern einstakan tengilið innan hlutans, til dæmis með því að velja annað samskiptasniðmát í línunum á síðunni **Hluti**.  
3. Til að skrá hlutann og samskiptin veldu aðgerðina **kladdi**. Síðan **Skrá hluta** opnast.
4. Ef stofna á nýjan hluta með sömu tengiliðum skal velja gátreitinn **Stofna eftirfylgnihluta**. Ef forritið á að geta stofnað eftirfylgnihluta verður að tilgreina númeraraðir fyrir hluta á síðunni **Tengslastjórnunargrunnur**.

Samskipti eru skráð fyrir hvern tengilið í hlutanum í töflunni **samskiptaskráningarfærsla** og hlutinn er skráður. Skráðir hlutar eru á síðunni **Skráðir hlutar**.

Ef gátreiturinn **Stofna eftirfylgnihluta** er valinn verður nýr hluti búinn með sömu tengiliðum og hlutinn sem var verið að skrá.

## <a name="see-also"></a>Sjá einnig
[Samskipti skráð](marketing-interactions.md)  
[Vinna með tengiliði](marketing-contacts.md)  
[Umsjón sölutækifæra](marketing-manage-sales-opportunities.md)  
[Unnið með Business Central](ui-work-product.md)
