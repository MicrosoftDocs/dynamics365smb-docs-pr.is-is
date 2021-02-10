---
title: Skilgreina almenna birgðauppsetningu
description: Lýsir því hvernig á að skilgreina almenna uppsetningu birgða þannig að hægt sé að stjórna vöruhúsinu og birgðum.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e3ecf8d206e50244c19a820bdb67d2992cbefe36
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746367"
---
# <a name="set-up-general-inventory-information"></a>Setja upp almennar birgðaupplýsingar

Almennar birgðaupplýsingar eru tilgreindar á síðunni **Birgðagrunnur**.

## <a name="to-set-up-general-inventory-information"></a>Til að setja upp almennar birgðaupplýsingar

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðauppsetning** og veldu síðan tengda tengilinn.
2. Á síðunni **Birgðagrunnur** skal fylla út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Ítarlegar upplýsingar um kostnaðarreitina **Sjálfvirk kostnaðarbókun** og **Væntanleg kostnaðarbókun á fjárhag** og **Sjálfgefin aðferð kostnaðarútreiknings** er að finna í [Afstemma birgðakostnað í fjárhag](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md) og [Hönnunarupplýsingar: Væntanleg kostnaðarfærsla](design-details-expected-cost-posting.md). Frekari upplýsingar um almennan kostnaðarútreikning er að finna í [Stjórnun birgðakostnaðar](finance-manage-inventory-costs.md).  

Ef afgreiðslutími á vörum inn í vöruhús á að vera tekinn með þegar reiknað er út hvenær pöntun er lofað í innkaupalínu er hægt að setja þetta upp sem sjálfgefið fyrir birgðirnar á síðunni **Birgðagrunnur** og fyrir staðsetninguna þína. Nánari upplýsingar er að finna í [Reikna dagsetningar pöntunarloforða](sales-how-to-calculate-order-promising-dates.md).  

> [!NOTE]
> Kveikt er á **Sjálfvirk kostnaðarleiðrétting** að sjálfgefnu til að tryggja að birgðavirði sé alltaf rétt í fjárhag, sem fyrir vikið heldur sölu- og hagnaðartölum uppfærðum. Kostnaðarbreytingum úr færslum á innleið, til dæmis færslur fyrir innkaup eða framleiðslufrálag, er úthlutað á tengdar færslur á útleið, t.d. sölu og flutninga. Þetta er gagnlegt fyrir nýja [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptavini og lítil fyrirtæki með tiltölulega lágt birgðafærslustig. Þegar fyrirtæki hinsvegar stækkar og birgðastöður aukast getur þetta hægt á afköst kerfisins. Til að lágmarka minnkuð afköst við bókun skal velja tímavalkost til að skilgreina hversu langt aftur í tímann frá vinnudagsetningu færsla á innleið getur átt sér stað til að hugsanlega ræsa leiðréttingu á tengdum virðisfærslum á útleið. Að öðrum kosti er handvirkt hægt að leiðrétta kostnað með reglulegu millibili með runuvinnslunni Leiðrétta kostnað - Vörufærslur.

## <a name="see-also"></a>Sjá einnig
[Setja upp birgðir](inventory-setup-inventory.md)  
[Hönnunarupplýsingar: Aðferð kostn.útreiknings](design-details-costing-methods.md)    
[Stjórna birgðum](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)
