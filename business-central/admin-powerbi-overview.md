---
title: Power BI Samþættingaríhlutur og yfirlit yfir arkitektúr fyrir Business Central| Microsoft docs
description: Lærðu um mismunandi þætti samþættingar Power BI við Business Central.
author: jswymer
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="power-bi-integration-component-and-architecture-overview-for-includeprodshortincludesprodshortmd" />Power BI Samþættingaríhlutur og hönnunaryfirlit fyrir [!INCLUDE[prod_short](includes/prod_short.md)]

Í þessari grein muntu fá upplýsingar um mismunandi þætti Power BI samþættingar við [!INCLUDE[prod_short](includes/prod_short.md)] til að hjálpa þér að skilja innleiðingu og notkun.

## <a name="components" />Íhlutir

Eftirfarandi tafla lýsir helstu íhlutunum sem tengjast Power BI samþættingu.

|Íhlutur|Description|
|---------|-----------|
|Power BI|Skýjahýsing og stjórnunarþjónusta í skýi.|
|Power BI Desktop|Höfundarverkfæri til að búa til skýrslur og mælaborð, og gerir þér kleift að keyra skýrslur. Það er í boði sem ókeypis niðurhal á Microsoft Store og er uppsett staðbundið.|
|[!INCLUDE[prod_short](includes/prod_short.md)]|Lausn á netinu eða staðbundið með tenglum á Power BI og möguleikanum á að innfella Power BI hluta.|

## <a name="whats-available-from-the-start" />Það sem er í boði frá upphafi

Eftirfarandi tafla lýsir tiltækum eiginleikum.

|Sérkenni|[!INCLUDE[prod_short](includes/prod_short.md)] á netinu eða aðstoð á staðnum|
|-------|---------------------|
|Power BI Ttengi|Bæði. Mismunandi tengi fyrir netið og á staðnum. Sama tengi notað fyrir Power BI Desktop og Power BI þjónustuna |
|Innfelld reynsla fyrir skoðun á tiltekinni skýrslu innan upplýsingareits í [!INCLUDE[prod_short](includes/prod_short.md)]|Bæði. Krefst þess að grunnstilling birti skýrslur á staðnum.|
|Power BI-skýrslustjórnun frá [!INCLUDE[prod_short](includes/prod_short.md)]|Beinlínutengt|
|Sjálfgefnar Power BI skýrslur um hlutverkamiðstöðvar virkjaðar á Power BI|Beinlínutengt|
|Power BI-forrit á Microsoft AppSource|Beinlínutengt|

## <a name="architecture" />Högun

[!INCLUDE[prod_short](includes/prod_short.md)] samþættist við Power BI í gegnum tengil með OData. Gagnagjafi fyrir Power BI-skýrslur kemur fyrir sem API-síður og OData-vefþjónustur.

:::image type="content" source="./media/power-bi-architecture.png" alt-text="Annar myndtexti." lightbox="./media/power-bi-architecture.png":::

Frá og með febrúar 2022 eru Power BI skýrslur fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á netinu fengnar frá aukalegri eftirmynd af skrifvörðum gagnagrunni. Eftirmynd gagnagrunnsins er hluti af möguleikanum [lesa útvíkkun](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) í [!INCLUDE[prod_short](includes/prod_short.md)] á netinu. Þessi grunnstilling losar um aðalgagnagrunninn fyrir færslur, sem eykur afköst kerfisins. Að tengjast við skrifvarða eftirmynd gagnagrunnsins er mikilvægur hluti af tengli Business Central Online og þarfnast ekki frekari uppsetningar af þinni hálfu. Allar nýjar skýrslur munu sjálfgefið tengjast við skrifvarða eftirmynd gagnagrunnsins. Gamlar skýrslur munu enn nota aðalgagnagrunninn. Frekari upplýsingar er að finna í [Business Central 2021 útgáfutímabil 2 áskriftarleið](/dynamics365-release-plan/2021wave2/smb/dynamics365-business-central/use-secondary-read-only-database-power-bi-reporting).

## <a name="general-flow" />Almennt flæði

Eftirfarandi skýringarmynd sýnir grunnverkflæði fyrir notendur þegar verið er að tengja [!INCLUDE[prod_short](includes/prod_short.md)] við Power BI.

![Power BI verkflæði fyrir samþættingu við Business Central.](./media/power-bi-flow.png)

1. Notandi skráir sig fyrir Power BI -reikningi.
2. Notandi tengist Power BI frá [!INCLUDE[prod_short](includes/prod_short.md)].
3. [!INCLUDE[prod_short](includes/prod_short.md)] staðfestir leyfið.
4. [!INCLUDE[prod_short](includes/prod_short.md)] virkjar sjálfgefnar skýrslur í Power BI-þjónustunni. Þetta skref gildir aðeins [!INCLUDE[prod_short](includes/prod_short.md)] á netinu.
5. [!INCLUDE[prod_short](includes/prod_short.md)] gerir skýrslur í Power BI í boði fyrir val í [!INCLUDE[prod_short](includes/prod_short.md)]. Sjálfgefnar skýrslur birtast sjálfkrafa í Power BI-hlutum.
6. Notandi stofnar skýrslu í Power BI Desktop.
7. Notandi gefur út skýrslu á Power BI -þjónustuna. Svo er hægt að velja skýrslurnar í [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex" />Sjá tengda [Microsoft þjálfun](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also" />Sjá einnig

[Business Central og Power BI](admin-powerbi.md)  
[Power BI fyrir neytendur](/power-bi/consumer/end-user-consumer)  
[„Nýtt útlit“ Power BI þjónustunnar](/power-bi/service-new-look)  
[Stutt leiðbeining: Tengjast við gögn í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI fylgiskjöl](/power-bi/)  
[Viðskiptaupplýsingar](bi.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem Power BI gagnaveitu](across-how-use-financials-data-source-powerbi.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem Power Apps gagnaveitu](across-how-use-financials-data-source-powerapps.md)  
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] í Power Automate](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
