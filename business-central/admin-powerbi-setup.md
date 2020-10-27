---
title: Virkjun Power BI samþættingar við Business Central
description: Fáið upplýsingar um hvernig á að setja upp tenginguna við Power BI til að fá innsýn, viðskiptagreind og KPI (afkastavísa) úr gögnum Business Central með forriti Business Central fyrir Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: ce4b45dbe80ab1972c92cde144b457eeeaff3402
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927073"
---
# <a name="enabling-power-bi-integration-with-prodshort"></a>Virkjun Power BI samþættingar við [!INCLUDE[prodshort](includes/prodshort.md)]

Þessi grein lýsir því hvernig hægt er að undirbúa [!INCLUDE[prodshort](includes/prodshort.md)] til samþættingar við Power BI. [!INCLUDE[prodshort](includes/prodshort.md)] á netinu er þegar virkt fyrir samþættingu, þó þú kunnir að vilja lesa einhverjar upplýsingar um leyfi. Fyrir [!INCLUDE[prodshort](includes/prodshort.md)] á staðnum er búið að setja upp umhverfi til að tengjast við Power BI áður en notendur geta unnið með það.

## <a name="power-bi-licensing"></a><a name="license"></a>Power BI Leyfisveiting

Með [!INCLUDE[prodshort](includes/prodshort.md)] fá notendur ókeypis Power BI leyfi sem veitir aðgang að algengustu aðgerðunum í [!INCLUDE[prodshort](includes/prodshort.md)] og Power BI. Einnig er hægt að kaupa Power BI Pro-leyfi sem veitir aðgang að viðbótareiginleikum. Eftirfarandi tafla sýnir yfirlit yfir tiltæka eiginleika með hverju leyfi.

|Power-leyfi|Skoða skýrslur|Stofna skýrslur|Deila skýrslum|Uppfæra skýrslur| [!INCLUDE[prodshort](includes/prodshort.md)] Forrit|
|-------------|--------||
|Power BI laus|![hak](media/check.png)|![annað hak](media/check.png)|(takmarkað)|(takmarkað)||
|Power BI Pro|![enn eitt hakið](media/check.png)|![þetta er hak](media/check.png)|![aftur hak](media/check.png)|(ítarlegt)|![síðasta hakið](media/check.png)|

Frekari upplýsingar er að finna í [Leyfi fyrir Power BI þjónustunni fyrir notendur í fyrirtækinu](/power-bi/admin/service-admin-licensing-organization) eða [Skráning á þjónustunni Power BI sem einstaklingur](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="set-up-prodshort-on-premises-for-power-bi-integration"></a><a name="setup"></a>Setja upp [!INCLUDE[prodshort](includes/prodshort.md)] innanhúss fyrir Power BI samþættingu

Þessi hluti útskýrir kröfur fyrir [!INCLUDE[prodshort](includes/prodshort.md)] á staðnum til að samþætta við Power BI.

1. OData-vefþjónusta og endastöð ODataV4 eru virk.

    OData-vefþjónusta verður að vera virk á [!INCLUDE[server](includes/server.md)], og OData-tengið opnað í eldvegg. Frekari upplýsingar er að finna í [Skilgreining Business Central Server - OData vefþjónustur](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).
    
    Staðbundni þjónninn verður að vera aðgengilegur á internetinu.

2. [!INCLUDE[prodshort](includes/prodshort.md)] notandareikningur er með aðgangslykil vefþjónustu.

    Aðgangslykill vefþjónustu er nauðsynlegur til að skoða [!INCLUDE[prodshort](includes/prodshort.md)] gata í Power BI. Hægt er að úthluta aðgangslykli vefþjónustunnar á hvern notendareikning. Eða þess í stað skaltu stofna tiltekinn reikning með aðgangslykli vefþjónustu til notkunar fyrir alla notendur. Frekari upplýsingar eru í [Sannvottun vefþjónustu](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

3. NavUserPassword eða Azure Active Directory sannvottun er grunnstillt.

4. Til að skoða Power BI skýrslur sem eru innfelldar á [!INCLUDE[prodshort](includes/prodshort.md)] síður verður forrit að vera skráð fyrir [!INCLUDE[prodshort](includes/prodshort.md)] í Microsoft Azure.

    Skráð forrit þarf að hafa leyfi fyrir Power BI þjónustunni. Frekari upplýsingar er að finna á [Skráning [!INCLUDE[prodshort](includes/prodshort.md)] innanhúss í Azure AD fyrir samþættingu við aðrar þjónustur](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Ef virkjun notar NavUserPassword-sannvottun, tengist [!INCLUDE[prodshort](includes/prodshort.md)] sömu Power BI þjónustunni fyrir alla notendur. Þessi þjónustureikningur er tilgreindur sem hluti af skráningu á forritinu. Með Azure AD sannvottun er [!INCLUDE[prodshort](includes/prodshort.md)] tengt við Power BI-þjónustuna sem tengist einstökum notendareikningum.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->

## <a name="publish-data-as-web-services"></a>Birta gögn sem vefþjónustu

Kóðaeiningar, síður og fyrirspurnir sem ætlunin er að nota sem gagnagjafa í Power BI-skýrslum verða að vera birtar sem vefþjónustur. Margar vefþjónustur birtast sjálfkrafa. Auðveld leið til að finna vefþjónustu er að leita að *vefþjónustu* í [!INCLUDE[prodshort](includes/prodshort.md)]. Á síðunni **Vefþjónusta** skal ganga úr skugga um að reiturinn **Birta** sé valinn fyrir vefþjónustuna sem finna má að ofan. Þetta verk er oftast stjórnunarverk.

Frekari upplýsingar um birtingu vefþjónustu er að finna á [Birta vefþjónustu](across-how-publish-web-service.md).

> [!TIP]
> Til að fræðast um hvað hægt er að gera til að tryggja bestu frammistöðu vefþjónustunnar, eins og hún birtist úr Business Central Server (endastöð) og frá neytanda (viðskiptavini), skal lesa [Skrifa gagnalega vefþjónustu](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).




## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Business Central og Power BI](admin-powerbi.md)  
[Power BI Samþættingaríhlutur og hönnunaryfirlit fyrir [!INCLUDE[prodshort](includes/prodshort.md)]](admin-powerbi-overview.md)  
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
