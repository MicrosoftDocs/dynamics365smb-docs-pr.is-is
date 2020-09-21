---
title: Power BI Samþættingaríhlutur og yfirlit yfir arkitektúr fyrir Business Central| Microsoft docs
description: Það er auðvelt að fá innsýn, viðskiptaupplýsingar og afkastavísi (KPI) í Business Central gögnum með Business Central forritunum fyrir Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 9514f0355932c1b1cbd30acfdb9f6dab46db8a0a
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697767"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prodshort"></a>Power BI Samþættingaríhlutur og hönnunaryfirlit fyrir [!INCLUDE[prodshort](includes/prodshort.md)]

Í þessari grein muntu fá upplýsingar um mismunandi þætti Power BI samþættingar við [!INCLUDE[prodshort](includes/prodshort.md)] til að hjálpa þér að skilja innleiðingu og notkun.

## <a name="components"></a>Íhlutir

Eftirfarandi tafla lýsir helstu íhlutunum sem tengjast Power BI samþættingu.

|Íhlutur|Description|
|---------|-----------|
|Power BI|Skýjahýsing og stjórnunarþjónusta í skýi.|
|Power BI Desktop|Höfundarverkfæri til að búa til skýrslur og mælaborð, og gerir þér kleift að keyra skýrslur. Það er í boði sem ókeypis niðurhal á Microsoft Store og er uppsett staðbundið.|
|[!INCLUDE[prodshort](includes/prodshort.md)]|Lausn á netinu eða staðbundið með tenglum á Power BI og möguleikanum á að innfella Power BI hluta.|

## <a name="whats-available-from-the-start"></a>Það sem er í boði frá upphafi

Eftirfarandi tafla lýsir tiltækum eiginleikum.

|Sérkenni|[!INCLUDE[prodshort](includes/prodshort.md)] á netinu eða aðstoð á staðnum|
|-------|---------------------|
|Power BI Ttengi|Bæði. Mismunandi tengi fyrir netið og á staðnum. Sama tengi notað fyrir Power BI Desktop og Power BI þjónustuna |
|Innfelld reynsla fyrir skoðun á tiltekinni skýrslu innan upplýsingareits í [!INCLUDE[prodshort](includes/prodshort.md)]|Bæði. Krefst þess að grunnstilling birti skýrslur á staðnum.|
|Power BI-skýrslustjórnun frá [!INCLUDE[prodshort](includes/prodshort.md)]|Beinlínutengt|
|Sjálfgefnar Power BI skýrslur um hlutverkamiðstöðvar virkjaðar á Power BI|Beinlínutengt|
|Power BI-forrit á Microsoft AppSource|Tengt.|

## <a name="architecture"></a>Högun

[!INCLUDE[prodshort](includes/prodshort.md)] samþættist við Power BI í gegnum tengil með OData. Gagnauppruni fyrir Power BI-skýrslur er óvarinn sem OData vefþjónustur.

![Power BI högun fyrir samþættingu við Business Central](./media/power-bi-architecture.png)

## <a name="general-flow"></a>Almennt flæði

Eftirfarandi skýringarmynd sýnir grunnverkflæði fyrir notendur þegar verið er að tengja [!INCLUDE[prodshort](includes/prodshort.md)] við Power BI.

![Power BI verkflæði fyrir samþættingu við Business Central](./media/power-bi-flow.png)

1. Notandi skráir sig fyrir Power BI -reikningi.
2. Notandi tengist Power BI frá [!INCLUDE[prodshort](includes/prodshort.md)].
3. [!INCLUDE[prodshort](includes/prodshort.md)] staðfestir leyfið.
4. [!INCLUDE[prodshort](includes/prodshort.md)] virkjar sjálfgefnar skýrslur í Power BI-þjónustunni. Þetta skref gildir aðeins [!INCLUDE[prodshort](includes/prodshort.md)] á netinu.
5. [!INCLUDE[prodshort](includes/prodshort.md)] gerir skýrslur í Power BI í boði fyrir val í [!INCLUDE[prodshort](includes/prodshort.md)]. Sjálfgefnar skýrslur birtast sjálfkrafa í Power BI-hlutum.
6. Notandi stofnar skýrslu í Power BI Desktop.
7. Notandi gefur út skýrslu á Power BI -þjónustuna. Svo er hægt að velja skýrslurnar í [!INCLUDE[prodshort](includes/prodshort.md)].

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Business Central og Power BI](admin-powerbi.md)  
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
