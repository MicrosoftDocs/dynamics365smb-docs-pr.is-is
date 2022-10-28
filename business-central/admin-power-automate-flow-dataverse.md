---
title: Power Automate Nota flæði fyrir viðvaranir við Einingarbreytingar
description: Lærðu að búa til streymi í Power Automate sem mun gera viðvart þegar einingu er breytt í Dataverse umhverfi.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power Automate, Flow, Dataverse
ms.search.form: ''
ms.date: 09/05/2022
ms.author: bholtorf
ms.openlocfilehash: d58a8ba6b1b2c451caa391ef5dd89e0d73d38b5a
ms.sourcegitcommit: 902834e76460d751a345485c66fd2831066b396b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716503"
---
# <a name="use-a-power-automate-flow-for-alerts-to-dataverse-entity-changes"></a>Power Automate Nota flæði fyrir viðvaranir við Dataverse einingarbreytingar

Kerfisstjórar geta búið til sjálfvirkt flæði í Power Automate því tilkynnir notanda [!INCLUDE[prod_short](includes/prod_short.md)] um breytingar á færslum í [!INCLUDE [cds_long_md](includes/cds_long_md.md)] fyrirtækinu.

> [!NOTE]
> Þessi grein gerir ráð fyrir þú hefur tengda netútgáfu af [!INCLUDE[prod_short](includes/prod_short.md)] með [!INCLUDE [cds_long_md](includes/cds_long_md.md)] og áætlaða samstillingu á milli tveggja forrita.

## <a name="import-the-flow-template"></a>Flytja inn Flæðisniðmát

> [!TIP]
> Til að auðvelda uppsetningu áklæðis þá höfum við útbúið sniðmát sem skilgreinir flæðikveikja og flæðiskilyrði fyrir þig. Fylgdu skrefunum í þessum kafla til að nota sniðmátið. Til að búa til flæðið sjálfur skaltu sleppa þessum hluta og byrja á skrefunum í [að skilgreina Flæðislekkinn](#define-the-flow-trigger).

1. Innskráning í [Power Automate](https://powerautomate.microsoft.com).
2. Velja **Sniðmát** og leita síðan eftir aðalnotanda **til að** Tilkynna.

:::image type="content" source="media/power-automate-import-template.png" alt-text="Leitarorð til að finna flæðisniðmátið.":::
3. **Veljið Viðskiptaseðla tilkynningarinnar þegar reikningur breytist** í sniðmát.
4. Halda áfram með skrefin í [aðaltilkynningu frá Viðskiptamiðinu um breytingarhluta](#notify-business-central-about-a-change).

## <a name="define-the-flow-trigger"></a>Skilgreina Flæðikveikjuna

1. Innskráning í [Power Automate](https://flow.microsoft.com).
2. Stofna sjálfvirkt skýflæði sem er ræst þegar línu fyrir [!INCLUDE [cds_long_md](includes/cds_long_md.md)] einingu er bætt við, breytt eða eytt. Sjá [Trigger streymi þegar röð er bætt við, henni breytt eða eytt](/power-automate/dataverse/create-update-delete-trigger), til að fá frekari upplýsingar. Þetta dæmi notar **viðskiptaeininguna**. Eftirfarandi mynd sýnir stillingar fyrir fyrsta skrefið í að skilgreina flæðikveikju.

:::image type="content" source="media/power-automate-flow-dataverse-trigger.png" alt-text="Stillingar fyrir kveikju í flæði":::
3. **Notaðu AssistEdit (...)** hnappinn efst í hægra horninu til að bæta tengingunni við umhverfi þitt [!INCLUDE [cds_long_md](includes/cds_long_md.md)].
4. Velja **skal sýna ítarlega valkosti** og færa inn í **reitinn Afmörkun afmörkunar**, slá inn **customertypecode EQ 3** eða **customertypecode EQ 11** og **statecode EQ 0**. Þessi gildi þýða að kveikjan bregst aðeins við þegar breytingar eru gerðar á virkum reikningum af gerðinni **Viðskiptavinur** eða **Lánardrottinn**.

## <a name="define-the-flow-condition"></a>Skilgreina Flæðiskilyrðin

Gögn eru samstillt á milli [!INCLUDE[prod_short](includes/prod_short.md)] og [!INCLUDE [cds_long_md](includes/cds_long_md.md)] í gegnum samþættingarnotandareikning. Til að hunsa breytingarnar sem Samstillingin býr til þarf að stofna skilyrði skref í flæði sem útilokar breytingar á notandareikning samþættingarins.  

1. **Bæta við færðu línu eftir auðkenni frá Dataverse** skrefi á eftir flæðikveikjunni með eftirfarandi stillingum. Frekari upplýsingar er að finna [í fá röð eftir kenni Dataverse](/power-automate/dataverse/get-row-id).

    1. **Í reitnum töfluheiti** er hægt að velja **notendur**
    2. **Í reitnum LÍNUKENNI** er breytt (gildi) **valið** úr flæðigimröðinni.  

2. Bæta við skilyrði skrefi á eftir **eða** stillingum til að auðkenna notandareikninginn samþættingarlykil.
    1. Aðalnetfang notandans er **að finna** contoso.com **·**
    2. Fullt nafn **notanda** inniheldur **[!INCLUDE[prod_short](includes/prod_short.md)]**.

3. Bæta við segja stýringu til að stöðva flæðið ef einingunni var breytt af notandareikninginn sameining.

Eftirfarandi mynd sýnir hvernig á að skilgreina flæðikveikjuna og flæðiskilyrðin.

:::image type="content" source="media/power-automate-flow-dataverse.png" alt-text="Yfirlit yfir flæðikveikja og ástandstillingar":::

## <a name="notify-business-central-about-a-change"></a>Tilkynning frá Viðskiptaaðalfundi um breytingu

Ef rennslið er ekki stöðvað af skilyrðinu verður að tilkynna [!INCLUDE[prod_short](includes/prod_short.md)] að breyting hafi átt sér stað. [!INCLUDE[prod_short](includes/prod_short.md)] Notaðu tengivirkið til að gera það.

1. **Í engri** gaffal ástandi stíga, bæta við aðgerð og leita að **Dynamics 365[!INCLUDE[prod_short](includes/prod_short.md)]**. Velja skal tengitáknið á listanum.
2. Aðgerðin stofna færslu (v3) **er** valin.

:::image type="content" source="media/power-automate-flow-dataverse-connector.png" alt-text="Stillingar fyrir [!INCLUDE[prod_short](includes/prod_short.md)] tengibúnað":::

3. **Notaðu Assist breytingarhnappinn (...)** í efra hægra horninu til að bæta tengingunni við [!INCLUDE[prod_short](includes/prod_short.md)].
4. Við tengingu skal fylla út **reitina heiti** umhverfis og **fyrirtækis**.
5. **Í API-tegundarsvæðinu** er fært inn **Microsoft/dataverse/v 1.0**.
6. **Í reitinn töfluheiti** er fært inn **dataverseentitybreytingar**.
7. **Færið inn** lykil **í entityname** -svæðinu.
8. Spara flæðið.

Eftirfarandi mynd sýnir hvernig áklæði á að líta út.

:::image type="content" source="media/power-automate-flow-dataverse-summary.png" alt-text="Yfirlit yfir allar stillingar fyrir áklæðið":::

Þegar lykli er bætt við, eytt eða breytt er í [!INCLUDE [cds_long_md](includes/cds_long_md.md)] umhverfi mun þetta flæði gera eftirfarandi aðgerðir:

1. Kalla á [!INCLUDE[prod_short](includes/prod_short.md)] umhverfið sem tilgreint var í [!INCLUDE[prod_short](includes/prod_short.md)] tengivirkinu.
2. [!INCLUDE[prod_short](includes/prod_short.md)] Nota API til að setja inn færslu með **entityname** **-lykli** í **Dataverse töfluna færslubreyting**. Þessi færibreyta er nákvæmt heiti Dataverse einingarinnar sem verið er að búa til flæðið fyrir.
3. [!INCLUDE[prod_short](includes/prod_short.md)] ræsum vinnslu færslunnar sem samstillir viðskiptamenn með lykla.

## <a name="see-also"></a>Sjá einnig

[Nota Viðskiptamiðað í Power Automate streymi](across-how-use-financials-data-source-flow.md)  
[Setja upp sjálfvirk verkflæði](/business-central/dev-itpro/powerplatform/automate-workflows)  
[Samþætting við Microsoft Dataverse](admin-common-data-service.md)  
[Samstilla gögn í Viðskiptamiðinu við Microsoft Dataverse](admin-synchronizing-business-central-and-sales.md)  
