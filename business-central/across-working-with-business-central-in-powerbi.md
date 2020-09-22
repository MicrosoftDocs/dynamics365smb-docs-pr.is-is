---
title: Unnið með Business Central Data í Power BI| Microsoft docs
description: Það er auðvelt að fá innsýn, viðskiptaupplýsingar og afkastavísi (KPI) í Business Central með Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 07/10/2020
ms.author: jswymer
ms.openlocfilehash: bdcbcb0fa82d799e29cfcdbb034e231635510656
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697771"
---
# <a name="working-with-prodshort-data-in-power-bi"></a>Unnið með [!INCLUDE [prodshort](includes/prodshort.md)] gögn í Power BI

Í þessari grein lærir þú undirstöðuatriði varðandi vinnu við skýrslur og mælaborð í Power BI sem nota [!INCLUDE [prodshort](includes/prodshort.md)] sem gagnaveitu. Greinin fjallar um suma þætti sem munu hjálpa til við að hefjast handa sem [!INCLUDE[prodshort](includes/prodshort.md)] notandi. Almennar leiðbeiningar og leiðbeiningar um notkun á Power BI er að finna í [Power BI fylgigögnum fyrir neytendur](https://review.docs.microsoft.com/en-us/power-bi/consumer).

## <a name="get-ready"></a>Vertu með allt á tæru

Skráðu þig fyrir nýju Power BI þjónustuna. Ef þú hefur ekki þegar skráð þig skaltu fara á [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Þegar þú skráir skaltu nota vinnunetfang og aðgangsorð.

## <a name="get-started"></a>Hefjast handa

Þegar þú ert með Power BI-reikning geturðu skráð þig inn á [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

Power BI þjónustan hýsir allar skýrslur sem eru í boði. Til að sjá skýrslu skal velja **Vinnusvæðið mitt** > **Skýrslur**. Veljið svo skýrsluna sem á að skoða.

Með [!INCLUDE[prodshort](includes/prodshort.md)] á netinu er sjálfkrafa hægt að hafa sjálfgefnar skýrslur á vinnusvæðinu. Ef stofna á eigin skýrslur er hægt að nota Power BI Desktop til að stofna skýrslur og birta þær síðan á eigin vinnusvæði. Frekari upplýsingar er að finna í [Hafist handa með skýrslur í Power BI Desktop til að birta [!INCLUDE [prodlong](includes/prodlong.md)] gögn](across-how-use-financials-data-source-powerbi.md).

Ef þú ert að nota [!INCLUDE[prodshort](includes/prodshort.md)] á staðnum þarftu að byrja frá grunni með því að nota Power BI Desktop. Hægt er að dreifa Power BI skýrslum sem skrám, sem hægt er að hlaða upp.

## <a name="get-the-latest-data"></a>Fá nýjustu gögnin

Hver Power BI skýrsla byggir á gagnasafni sem fær gögn frá [!INCLUDE[prodshort](includes/prodshort.md)] uppruna. Þú vilt ganga úr skugga um að gögnin í Power BI-skýrslunum séu uppfærð með gögnunum í [!INCLUDE[prodshort](includes/prodshort.md)]. Þetta hugtak er nefnt *uppfærsla*.  Ekki er víst að endurnýjun gerist sjálfkrafa, allt eftir því hvernig fyrirtækið hefur sett upp Power BI. Það eru tvær leiðir til að uppfæra gögn: handvirkt eða með því að tímasetja uppfærslu. Handvirk endurnýjun fer fram eftir þörfum. Áætluð endurnýjun gerir þér kleift að uppfæra sjálfkrafa á skilgreindum tímabilum.

### <a name="refresh-manually"></a>Uppfæra handvirkt

Í skoðunarrúðunni, undir **Gagnasafn**, skal velja **Fleiri valkostir (...)** við hliðina á gagnasafni og velja svo **Uppfæra núna**.

### <a name="schedule-a-refresh"></a>Áætla uppfærslu

Í skoðunarrúðunni, undir Gagnasafn, skal velja Fleiri valkostir (...) við hliðina á gagnasafn og velja svo **Uppfæra núna**. Fylltu út upplýsingarnar í **Tímasetja uppfærslu** og veldu **Not**.

Frekari upplýsingar eru í [Grunnstilla uppfærsluáætlun](/power-bi/connect-data/refresh-scheduled-refresh)

## <a name="upload-reports-from-files"></a><a name="upload"></a>Hlaða upp skýrslum úr skrám

Hægt er að dreifa Power BI skýrslum á meðal notenda sem. pbix-skrám. Ef þú ert með .pbix-skrá er hægt að hlaða skránni upp á vinnusvæði. Til að hlaða upp skýrslu skal gera eftirfarandi:

1. Á nýja vinnusvæðinu skal velja **Sækja gögn**.

2. Í reitnum Skrár skal velja **Sækja**.

3. Veldu **Staðbundin skrá**, farðu þangað sem hún er vistuð og veldu **Opna**.

Frekari upplýsingar er að finna á [Hlaða upp skýrslu á þjónustu](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

> [!NOTE]
> Til að hlaða upp skýrslu þarftu að hafa [Premium afkastagetu](/power-bi/service-premium-what-is) vinnusvæði. Nánari upplýsingar er að finna í [Stjórnun Premium eiginleika](/power-bi/admin/service-premium-capacity-manage). 

> [!TIP]
> Ef þú notar [!INCLUDE[prodshort](includes/prodshort.md)] á netinu geturðu einnig hlaðið upp skýrslu úr [!INCLUDE[prodshort](includes/prodshort.md)]. Frekari upplýsingar er að finna í [Unnið með Power BI kýrslur í [!INCLUDE [prodshort](includes/prodshort.md)] Hlaða upp skýrslum](across-working-with-powerbi.md#upload).

## <a name="share-reports-with-others"></a><a name="share"></a>Deila skýrslum með öðrum

Þegar skýrsla er á vinnusvæðinu er hægt að deila henni með öðrum í fyrirtækinu.

Til að deila skýrslu, í listaskýrslum, eða í opinni skýrslu skal velja **Deila**. Á hlutanum **Deila skýrslu** skal slá inn fullt netfang fyrir einstaklinga eða hóp viðtakenda sem á að deila með. Fylgdu leiðbeiningunum á skjánum til að ljúka deilingunni. Frekari upplýsingar er að finna á [Deila stjórnborði eða skýrslu](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> Þú verður að hafa  [Power BI Pro-leyfi](/power-bi/service-features-license-type) og fólkið sem þú deilir með einnig. Efnið verður að vera á vinnusvæði með [Premium réttindi](/power-bi/service-premium-what-is). Nánari upplýsingar eru í [Aðferðir við að deila vinnu þinn í Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Business Central og Power BI](admin-powerbi.md)  
[Búa til Power BI skýrslur til að birta [!INCLUDE [prodlong](includes/prodlong.md)]-gögn](across-how-use-financials-data-source-powerbi.md)  
[Power BI Samþættingaríhlutur og hönnunaryfirlit fyrir [!INCLUDE[prodshort](includes/prodshort.md)]](admin-powerbi-overview.md)  
[Unnið með Power BI Skýrslur í [!INCLUDE [prodshort](includes/prodshort.md)]](across-working-with-powerbi.md)  
[Power BI fyrir neytendur](/power-bi/consumer/end-user-consumer)  
[„Nýtt útlit“ Power BI þjónustunnar](/power-bi/service-new-look)  
[Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI fylgiskjöl](/power-bi/)  
[Viðskiptaupplýsingar](bi.md)  
[Hafist handa](product-get-started.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md)  
[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] sem Power Apps gagnaveitu](across-how-use-financials-data-source-powerapps.md)  
[Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] í Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  