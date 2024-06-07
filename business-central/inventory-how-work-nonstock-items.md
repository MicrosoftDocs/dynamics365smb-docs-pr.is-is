---
title: Búa til og hafa umsjón með vörulistaatriðum
description: Læra að selja vörur sem ekki eru á listanum yfir vörur.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
ms.search.keywords: non-inventoriable
ms.search.forms: '5725, 5726, 5732'
ms.service: dynamics-365-business-central
---

# <a name="work-with-catalog-items"></a>Vinna með vörulistaatriði

Vörulistaatriði eru vörur sem þú hefur ekki umsjón með í [!INCLUDE[prod_short](includes/prod_short.md)] fyrr en þú selur þær. Þegar aðgerðin **Velja vörulistavöru** er notuð til að bæta vörulistavöru við línu á sölupöntun, tilboði eða standandi sölupöntun er vörulistavörunni breytt í venjulega vöru.

> [!NOTE]  
> Ekki er hægt að velja vörulistavöru af síðunni **Sölureikningur** .

Vörulistaatriði hefur yfirleitt vörunúmer þess lánardrottins sem sér um að veita hana. Áður en hægt er að breyta vörulistaatriði í venjulega vöru þarftu að tilgreina hvernig á að breyta vörunúmerum lánardrottins í vörunúmerin þín. Til að fræðast meira um vörunúmer er farið í [Tilgreina hvernig vörunúmerum er umbreytt í eigin númeraröð](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Vörulistaatriði má ekki rugla saman við vörur sem eru ekki vörur í birgðum sem eru reglulegar vörur sem eru gefnar tegundina **Ekki í birgðum**, til að halda þeim ekki tiltækum og fyrir utan kostnaðarútreikningur, til dæmis vegna þess að þeir eru aðeins notaðir innbyrðis og eru lágir kostnaður. Til að fræðast um vörur sem eru ekki í birgðum er farið í [Um vörutegundir](inventory-about-item-types.md).

## <a name="create-a-catalog-item"></a>Búa til vörulistaatriði

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörulistaatriði** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Tilgreindu hvernig númerum vörulistaatriða er breytt í eigin númer

Áður en hægt er að umbreyta vörulista í venjulega vöru þarf að tilgreina hvernig á að umbreyta vörunúmerum lánardrottna í samsetningu sem notuð er fyrir vörunúmer.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning vörulistaatriðis** og velja síðan viðkomandi tengil.
2. Í reitnum **Nr. Reiturinn Snið** er valinn sá kostur sem hentar.

## <a name="convert-a-catalog-item-to-a-normal-item"></a>Breyta vörulistaatriði í venjulegt atriði

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörulistaatriði** og velja síðan viðkomandi tengil.
2. Opnaðu spjaldið fyrir vörulistaatriði sem þú vilt breyta í venjulegt atriði.
3. Á síðunni **Birgðaspjald vörulista** er valin aðgerðin **Stofna atriði**.

Nýtt birgðaspjald er áfyllt með upplýsingum úr vörulistavörunni og vörusniðmáti. Hægt er að breyta upplýsingum um nýju vöruna ef þörf krefur. Nánari upplýsingar um stofnun vöru eru skráðar [í Nýjar vörur](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Til að selja vörulista og breyta henni í venjulega vöru

Eftirfarandi ferli notar sölupöntun en skrefin eru hin sömu fyrir standandi sölupantanir og tilboð.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.
2. Valið er **Nýtt** aðgerð. Fylltu út reitina á flýtiflipanum **Almennt** eins og fyrir hvaða sölustað sem er. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).
3. Á nýjum sölulínum, í reitnum **Gerð**, veldu **vöru** en skildu eftir **Nr.** að vera auður.
4. Veldu aðgerðina **Lína** og veldu síðan **Velja vörulistaatriði** aðgerð.
5. Á síðunni **Vörulistaatriði**, veljið vörulistaatriðið sem á að selja og svo hnappinn **Í lagi**.
6. Þegar sölupöntunarlínunum er lokið, skal velja **bóka** aðgerðina.

> [!NOTE]  
> Vörutilvísun er sjálfkrafa vara milli vörunúmers lánardrottins og nýja vörunúmersins þíns. Til að fræðast meira um vörutilvísanir er farið í [Nota vörutilvísanir](inventory-how-use-item-cross-refs.md).

## <a name="see-also"></a>Sjá einnig .

[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Sérstakar pantanir stofnaðar](sales-how-to-create-special-orders.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
