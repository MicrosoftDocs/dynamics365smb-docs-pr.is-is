---
title: Fjöldabóka notkun
description: Ef flæðiaðferðin er stillt á Handvirk þarf að bóka íhlutina handvirkt með notkunarbók.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0b3ee6ca54e21605b4e9cf340b04656694c9801e
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935187"
---
# <a name="batch-post-production-consumption"></a>Fjöldabóka framleiðslunotkun

Ef flæðiaðferðin er stillt á **Handvirk** þarf að bóka íhlutina handvirkt með notkunarbók.  

>[!NOTE]
> Ef sett hefur verið gátmerki í reitinn **Krefjast tínslu** á birgðageymsluspjaldinu til að sýna að birgðageymslan krefjist tínsluvinnslu þarf ekki að nota þessa runuvinnslu. [!INCLUDE[prod_short](includes/prod_short.md)] mun sjá um notkun þegar birgðatínslan er bókuð. Frekari upplýsingar eru í [Taka til fyrir framleiðslu í einföldum vöruhúsagrunnstillingum](warehouse-how-to-pick-for-production.md#pick-for-production-in-basic-warehouse-configurations).  

Einnig er hægt að setja [!INCLUDE[prod_short](includes/prod_short.md)] upp þannig að það bóki sjálfvirkt (*flæða*) íhluti þegar byrjar eða endar framleiðslupantanir. Nánari upplýsingar eru í [Leyfa flæði íhluta samkvæmt frálagi aðgerða](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Bóka notkun fyrir eina eða fleiri framleiðslupantanalínur

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notkunarbók** og veldu síðan tengda tengilinn.  
2. Reitirnir eru fylltir út með framleiðslupöntunargögnunum og notkunargögnunum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Notið aðgerðina **Reikna notkun** til að mynda færslubókarlínur úr framleiðslupöntunum sem byggja á raunverulegu frálagi (magni tilbúinnar vöru sem tilkynnt hefur verið um) eða væntanlegu frálagi (magni tilbúinnar vöru sem stefnt er að því að framleiða).

    > [!NOTE]
    > Ef birgðageymsluspjaldið var skilgreint til að krefjast tínsluvinnu vöruhúss, þá má aðeins slá inn magn sem þegar er búið að tína í gegnum vöruhúsaaðgerð í reitinn **Magn** á síðunni **Notkunarbók**, ekki neitt reiknað magn. Frekari upplýsingar eru í [Taka til fyrir framleiðslu eða samsetningu í Grunngerðir vöruhúss](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

3. Velja **Bóka** aðgerðina til að bóka notkunina. Tengdar birgðir eru minnkaðar.

## <a name="see-also"></a>Sjá einnig

[Framleiðsla](production-manage-manufacturing.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Áætlun](production-planning.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
