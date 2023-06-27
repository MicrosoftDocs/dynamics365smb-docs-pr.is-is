---
title: Nota Power Automate flæði fyrir viðvaranir vegna breytinga á einingum
description: Kynntu þér hvernig á að búa til flæði í Power Automate sem lætur þig vita þegar einingu er breytt í Dataverse umhverfi.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Power Automate, Flow, Dataverse'
ms.search.form: null
ms.date: 09/05/2022
ms.author: bholtorf
---
# <a name="use-a-power-automate-flow-for-alerts-to-dataverse-entity-changes"></a>Notaðu Power Automate flæði fyrir viðvaranir vegna Dataverse breytinga á einingum

Stjórnendur geta búið til sjálfvirkt flæði í Power Automate sem lætur [!INCLUDE[prod_short](includes/prod_short.md)] vita um breytingar á færslum í [!INCLUDE [cds_long_md](includes/cds_long_md.md)] fyrirtækinu þínu.

> [!NOTE]
> Í þessari grein er gert ráð fyrir að þú hafir tengt netútgáfu af [!INCLUDE[prod_short](includes/prod_short.md)] við [!INCLUDE [cds_long_md](includes/cds_long_md.md)] og tímasett samstillingu á milli forritanna tveggja.

## <a name="import-the-flow-template"></a>Flytja inn sniðmát flæðis

> [!TIP]
> Til að auðvelda uppsetningu á flæðinu höfum við búið til sniðmát sem skilgreinir kveikju og skilyrði flæðisins fyrir þig. Fylgdu skrefunum í þessum hluta til að nota sniðmátið. Til að búa til flæðið á eigin spýtur skaltu sleppa þessum hluta og byrja á skrefunum í [Skilgreina kveikju fllæðis](#define-the-flow-trigger).

1. Skráðu þig inn á [Power Automate](https://powerautomate.microsoft.com).
2. Veldu **Sniðmát** og leitaðu síðan að **Tilkynna Business Central**.

:::image type="content" source="media/power-automate-import-template.png" alt-text="Leitarorð til að finna sniðmát flæðis":::
3. Veldu sniðmátið **Tilkynna Business Central þegar reikningur breytist**.
4. Haltu áfram með skrefin í hlutanum [Tilkynna Business Central um breytingar](#notify-business-central-about-a-change).

## <a name="define-the-flow-trigger"></a>Skilgreina kveikju flæðis

1. Skráðu þig inn á [Power Automate](https://flow.microsoft.com).
2. Búðu til sjálfvirkt skýjaflæði sem byrjar þegar lína fyrir [!INCLUDE [cds_long_md](includes/cds_long_md.md)] einingu er bætt við, breytt eða eytt. Frekari upplýsingar er að finna í [Kveikja á flæði þegar línu er bætt við, breytt eða eytt](/power-automate/dataverse/create-update-delete-trigger). Þetta dæmi notar eininguna **Reikningar**. Eftirfarandi mynd sýnir stillingarnar fyrir fyrsta skrefið í skilgreiningu á kveikju flæðis.

:::image type="content" source="media/power-automate-flow-dataverse-trigger.png" alt-text="Stillingar fyrir kveikju flæðis":::
3. Notaðu **Valhnappinn (...)** efst í hægra horninu til að bæta tengingu við [!INCLUDE [cds_long_md](includes/cds_long_md.md)] umhverfið þitt.
4. Veldu **Sýna ítarlega valkosti** og í reitinn **Sía línur** skaltu færa inn **customertypecode eq 3** eða **customertypecode eq 11** og **statecode eq 0**. Þessi gildi þýða að kveikjan mun aðeins bregðast við þegar gerðar eru breytingar á virkum reikningum af tegundinni **viðskiptamaður** eða **lánardrottinn**.

## <a name="define-the-flow-condition"></a>Skilgreina skilyrði flæðis

Gögn eru samstillt á milli [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE [cds_long_md](includes/cds_long_md.md)] í gegnum reikning samþættingarnotanda. Til að hunsa breytingar sem samstillingin gerir skal búa til skilyrðisskref í flæðinu sem útilokar breytingar sem reikningur samþættingarnotanda gerir.  

1. Bættu við skrefinu **Sækja línu eftir auðkenni úr Dataverse** eftir kveikju flæðis með eftirfarandi stillingum. Frekari upplýsingar er að finna í [Sækja línu eftir auðkenni úr Dataverse](/power-automate/dataverse/get-row-id).

    1. Í reitnum **Töfluheiti** skal velja **Notendur**
    2. Í reitnum **Auðkenni línu** skal velja **Breytt af (gildi)** úr kveikju flæðisins.  

2. Bættu við skilyrðisskrefi með eftirfarandi **eða** stillingum til að bera kennsl á reikning samþættingarnotanda.
    1. **Aðalnetfang notandans** inniheldur **contoso.com**
    2. **Fullt nafn** notandans inniheldur **[!INCLUDE[prod_short](includes/prod_short.md)]**.

3. Bættu við stýringu til að stöðva flæðið ef einingunni var breytt af reikningi samþættingarnotanda.

Eftirfarandi mynd sýnir hvernig á að skilgreina kveikju og skilyrði flæðis.

:::image type="content" source="media/power-automate-flow-dataverse.png" alt-text="Yfirlit yfir stillingar á kveikju og skilyrði flæðis":::

## <a name="notify-business-central-about-a-change"></a>Tilkynna Business Central um breytingu

Ef flæðið stöðvast ekki vegna skilyrðisins þarf að láta [!INCLUDE[prod_short](includes/prod_short.md)] vita að breyting hafi átt sér stað. Notaðu [!INCLUDE[prod_short](includes/prod_short.md)] tengil til að gera það.

1. Í **Engin** grein af skilyrðisskrefinu skal bæta við aðgerð og leita að **Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]**. Veldu tengiltáknið á listanum.
2. Veldu aðgerðina **Stofna færslu (V3)**.

:::image type="content" source="media/power-automate-flow-dataverse-connector.png" alt-text="Stillingar fyrir [!INCLUDE[prod_short](includes/prod_short.md)] Connector":::

3. Notaðu **Valhnappinn (...)** efst í hægra horninu til að bæta tengingu við [!INCLUDE[prod_short](includes/prod_short.md)] þitt.
4. Þegar það er tengt skaltu fylla út í reitina **Heiti umhverfis** og **Heiti fyrirtækis**.
5. Í reitnum **API-flokkur** skal færa inn **microsoft/dataverse/v1.0**.
6. Í reitinn **Töfluheiti** skal færa inn **dataverseEntityChanges**.
7. Í reitinn **einingarheiti** skal færa inn **reikning**.
8. Vistið flæðið.

Eftirfarandi mynd sýnir hvernig flæðið þitt á að líta út.

:::image type="content" source="media/power-automate-flow-dataverse-summary.png" alt-text="Yfirlit yfir allar stillingar fyrir flæðið":::

Þegar þú bætir við, eyðir eða breytir aðgangi í [!INCLUDE [cds_long_md](includes/cds_long_md.md)] umhverfinu þínu mun þetta flæði gera eftirfarandi aðgerðir:

1. Kallaðu á [!INCLUDE[prod_short](includes/prod_short.md)] umhverfið sem þú tilgreindir í [!INCLUDE[prod_short](includes/prod_short.md)] tenglinum.
2. Notaðu [!INCLUDE[prod_short](includes/prod_short.md)] API til að setja inn færslu með **einingarheiti** stillt á **reikning** í töflunni **Dataverse færslubreyting**. Þessi færibreyta er nákvæmt heiti Dataverse einingarinnar sem þú ert að búa flæðið til fyrir.
3. [!INCLUDE[prod_short](includes/prod_short.md)] byrjar verkraðarfærsluna sem samstillir viðskiptamenn við reikninga.

## <a name="see-also"></a>Sjá einnig

[Nota Business Central í Power Automate flæði](across-how-use-financials-data-source-flow.md)  
[Setja upp sjálfvirk verkflæði](/business-central/dev-itpro/powerplatform/automate-workflows)  
[Samþætting við Microsoft Dataverse](admin-common-data-service.md)  
[Samstilling gagna í Business Central með Microsoft Dataverse](admin-synchronizing-business-central-and-sales.md)  
