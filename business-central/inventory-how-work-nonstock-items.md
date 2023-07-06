---
title: Búa til og hafa umsjón með vörulistaatriðum
description: Lærðu að selja vörur sem þú heldur ekki á listanum yfir vörur.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
ms.search.keywords: non-inventoriable
ms.search.forms: '5725, 5726, 5732'
---

# <a name="work-with-catalog-items"></a><a name="work-with-catalog-items"></a><a name="work-with-catalog-items"></a>Vinna með vörulistaatriði

Vörulistaatriði eru vörur sem þú hefur ekki umsjón með í [!INCLUDE[prod_short](includes/prod_short.md)] fyrr en þú selur þær. Þegar aðgerðin velja Vörulistavöru  **er notuð**  til að bæta vörulistavöru við línu í sölupöntun, tilboði eða standandi sölupöntuninni, er vörulistaatrivörunni breytt í reglubundna vöru.

> [!NOTE]  
> Ekki er hægt að velja Vörulistaatriði af  **síðunni sölureikningur** .

Vörulistaatriði hefur yfirleitt vörunúmer þess lánardrottins sem sér um að veita hana. Áður en hægt er að breyta vörulistaatriði í venjulega vöru þarftu að tilgreina hvernig á að breyta vörunúmerum lánardrottins í vörunúmerin þín. Til að fræðast nánar um vörunúmera er farið í að  [Tilgreina hvernig vörunúmer vörulista eru umbreytt í eigin tölusetningu](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Vörulistaatriði má ekki rugla saman við vörur sem eru ekki vörur í birgðum sem eru reglulegar vörur sem eru gefnar tegundina **Ekki í birgðum**, til að halda þeim ekki tiltækum og fyrir utan kostnaðarútreikningur, til dæmis vegna þess að þeir eru aðeins notaðir innbyrðis og eru lágir kostnaður. Til að læra að flytja um vörur sem ekki eru í birgðum er farið í  [um vörugerðir](inventory-about-item-types.md).

## <a name="create-a-catalog-item"></a><a name="create-a-catalog-item"></a><a name="create-a-catalog-item"></a>Búa til vörulistaatriði

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörulistaatriði** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a><a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a><a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Tilgreindu hvernig númerum vörulistaatriða er breytt í eigin númer

Áður en hægt er að umbreyta vörulistavöru í venjuleg atriði þarf að tilgreina hvernig eigi að umbreyta vörunúmerum lánardrottins í skipulagið sem notað er í vörunúmerum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning vörulistaatriðis** og velja síðan viðkomandi tengil.
2.  **Í reitnum Nr. snið**  er valinn sá valkostur sem óskað er eftir.

## <a name="convert-a-catalog-item-to-a-normal-item"></a><a name="convert-a-catalog-item-to-a-normal-item"></a><a name="convert-a-catalog-item-to-a-normal-item"></a>Breyta vörulistaatriði í venjulegt atriði

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörulistaatriði** og velja síðan viðkomandi tengil.
2. Opnaðu spjaldið fyrir vörulistaatriði sem þú vilt breyta í venjulegt atriði.
3. Á síðunni **Birgðaspjald vörulista** er valin aðgerðin **Stofna atriði**.

Nýtt birgðaspjald áfyllt með upplýsingum úr vörulistavöru og vörusniðmáti er stofnað. Hægt er að breyta upplýsingum um nýju vöruna ef þörf krefur. Til að fræðast meira um stofnun vara er farið í að  [skrá nýjar vörur](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a><a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a><a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Að selja vörulistavöru og umbreyta henni í venjuleg atriði

Eftirfarandi ferli notar sölupöntun en skrefin eru þau sömu fyrir standandi sölupantanir og tilboð.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.
2. Valið er **Nýtt** aðgerð. Fylltu út reitina á flýtiflipanum **Almennt** eins og fyrir hvaða sölustað sem er. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).
3. Á nýjum sölulínum, í reitnum **Gerð**, veldu **vöru** en skildu eftir **Nr.** að vera auður.
4. Veldu aðgerðina **Lína** og veldu síðan **Velja vörulistaatriði** aðgerð.
5. Á síðunni **Vörulistaatriði**, veljið vörulistaatriðið sem á að selja og svo hnappinn **Í lagi**.
6. Þegar sölupöntunarlínunum er lokið, skal velja **bóka** aðgerðina.

> [!NOTE]  
> Vörutilvísun er sjálfkrafa vara milli vörunúmers lánardrottins og nýja vörunúmersins þíns. Til að fræðast meira um vöruvísanir er farið í að  [nota vörutilvísanir](inventory-how-use-item-cross-refs.md).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Sérstakar pantanir stofnaðar](sales-how-to-create-special-orders.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
