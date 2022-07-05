---
title: Stofna og stjórna vörulistaatriðum
description: Lýsir því hvernig á að selja vörur sem ekki er hægt að geyma á listanum yfir vörur.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.search.forms: 5725, 5726, 5732
ms.date: 06/20/2022
ms.author: bholtorf
ms.openlocfilehash: c12eb256d4e7f1e211e28dacf4c403406dba3d85
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077008"
---
# <a name="work-with-catalog-items"></a>Vinna með vörulistaatriði

Vörulistavörur eru vörur sem þú hefur ekki umsjón með [!INCLUDE[prod_short](includes/prod_short.md)] fyrr en þú selur þær. Þegar gátreiturinn velja Vörulistavöru **er notaður** til að bæta vörulistavöru við línu í sölupöntun eða tilboði, er vörulistaatrivörunni breytt í reglubundna vöru.

> [!NOTE]  
> Ekki hægt er að velja vörulistaatriði á síðunni **Sölureikningur**.

Vörulistaatriði hefur yfirleitt vörunúmer þess lánardrottins sem sér um að veita hana. Áður en hægt er að umbreyta vörulistavöru í venjulega vöru verður að tilgreina hvernig eigi að umbreyta vörunúmerum lánardrottins á tölusetningu vörunnar. Sjá [Tilgreinið hvernig vörunúmer vörulista eru umbreytt í eigin tölusetningu](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Vörulistaatriði má ekki rugla saman við vörur sem eru ekki vörur í birgðum sem eru reglulegar vörur sem eru gefnar tegundina **Ekki í birgðum**, til að halda þeim ekki tiltækum og fyrir utan kostnaðarútreikningur, til dæmis vegna þess að þeir eru aðeins notaðir innbyrðis og eru lágir kostnaður. Nánari upplýsingar er að finna í [Um vörugerðir](inventory-about-item-types.md).

## <a name="create-a-catalog-item"></a>Stofna Vörulistaatriði

Vörulistaatriðaspjöld hafa miklu minni upplýsingar en venjulegir birgðaspjald vegna þess að þú notar þær aðeins til að bjóða upp á vitna og á annan hátt. Af þeirri ástæðu þær þarf að umbreyta þeim í venjulegur birgðaspjöldum áður en hægt bóka sölufærslur fyrir þá.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörulistaatriði** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Tilgreinið hvernig vörunúmer vörulista eru umreiknuð í eigin tölusetningu

Áður en hægt er að umbreyta vörulistavöru í venjulega vöru verður að tilgreina hvernig eigi að umbreyta vörunúmerum lánardrottins á tölusetningu vörunnar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning vörulistaatriðis** og velja síðan viðkomandi tengil.
2. Fyllið inn reitina eftir þörfum.

## <a name="convert-a-catalog-item-to-a-normal-item"></a>Umbreyta Vörulistaatriði í venjulega vöru

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörulistaatriði** og velja síðan viðkomandi tengil.
2. Opnaðu spjaldið fyrir vörulistaatriði sem þú vilt breyta í venjulegt atriði.
3. Á síðunni **Birgðaspjald vörulista** er valin aðgerðin **Stofna atriði**.

Stofnað er nýtt birgðaspjald sem er forútfyllt með upplýsingum úr vörulistaatriði og viðeigandi vörusniðmát. Hægt er síðan að fylla inn í eða breyta reitum á nýja birgðaspjaldinu eins og þörf krefur. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Til að selja vörulistaatriði og breyta því í venjulegt atriði

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.
2. Valið er **Nýtt** aðgerð. Fylltu út reitina á flýtiflipanum **Almennt** eins og fyrir hvaða sölustað sem er. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).
3. Á nýjum sölulínum, í reitnum **Gerð**, veldu **vöru** en skildu eftir **Nr.** að vera auður.
4. Veldu aðgerðina **Lína** og veldu síðan **Velja vörulistaatriði** aðgerð.

    Vörulistaatriði breytt í venjulegt atriði. Stofnuð eru Nýtt birgðaspjald sem er forútfyllt með upplýsingum úr vörulistaatriði og viðeigandi vörusniðmát.
5. Á síðunni **Vörulistaatriði**, veljið vörulistaatriðið sem á að selja og svo hnappinn **Í lagi**.
6. Þegar sölupöntunarlínunum er lokið, skal velja **bóka** aðgerðina.

Hægt er síðan að fylla inn í eða breyta reitum á nýja birgðaspjaldinu eins og þörf krefur. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).

> [!NOTE]  
> Vörutilvísun er sjálfkrafa vara milli vörunúmers lánardrottins og nýja vörunúmersins þíns. Frekari upplýsingar er að finna í [Nota vörutilvísanir](inventory-how-use-item-cross-refs.md).

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Sérstakar pantanir stofnaðar](sales-how-to-create-special-orders.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
