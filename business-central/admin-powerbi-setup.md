---
title: Samþætting Power BI virkjuð við Business Central
description: 'Kynntu þér hvernig á að setja upp Power BI. Með Power BI skýrslum geturðu öðlast innsýn, viðskiptaupplýsingar og afkastavísa (KPI) úr Business Central gögnum.'
author: jswymer
ms.topic: get-started
ms.search.keywords: 'Power BI, setup, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 01/28/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.reviewer: jswymer
---
# <a name="enabling-power-bi-integration-with-"></a>Samþætting Power BI virkjuð með [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Þessi grein lýsir því hvernig hægt er að undirbúa [!INCLUDE[prod_short](includes/prod_short.md)] til samþættingar við Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] á netinu er þegar virkt fyrir samþættingu, þó þú kunnir að vilja lesa einhverjar upplýsingar um leyfi. Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum er búið að setja upp umhverfi til að tengjast við Power BI áður en notendur geta unnið með það.

## <a name="power-bi-licensing"></a><a name="license"></a>Power BI Leyfisveiting

Með [!INCLUDE[prod_short](includes/prod_short.md)] fá notendur ókeypis Power BI leyfi sem veitir aðgang að algengustu aðgerðunum í [!INCLUDE[prod_short](includes/prod_short.md)] og Power BI. Einnig er hægt að kaupa Power BI Pro-leyfi sem veitir aðgang að viðbótareiginleikum. Eftirfarandi tafla sýnir yfirlit yfir tiltæka eiginleika með hverju leyfi.

|Power-leyfi|Skoða skýrslur|Stofna skýrslur|Deila skýrslum|Uppfæra skýrslur| [!INCLUDE[prod_short](includes/prod_short.md)] Forrit|
|-------------|--------||
|Power BI laus|![hak.](media/check.png)|![annað hak](media/check.png)|(takmarkað)|(takmarkað)||
|Power BI Pro|![enn eitt hakið.](media/check.png)|![þetta er hak](media/check.png)|![aftur hak](media/check.png)|(ítarlegt)|![síðasta hakið](media/check.png)|

Frekari upplýsingar er að finna í [Leyfi fyrir Power BI þjónustunni fyrir notendur í fyrirtækinu](/power-bi/admin/service-admin-licensing-organization) eða [Skráning á þjónustunni Power BI sem einstaklingur](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="expose-data-through-api-or-odata-web-services"></a><a name="exposedata"></a>Birta gögn í gegnum API eða OData-vefþjónustur

Business Central býður upp á tvær leiðir til að birta gögn sem Power BI skýrslur geta notað: API-síður eða fyrirspurnir og OData-vefþjónustur.

### <a name="api-pages-and-queries"></a>API-síður og fyrirspurnir

> **GILDIR UM:** Eingöngu Business Central á netinu

Þróunaraðilar geta skilgreint síðuhluti og fyrirspurnarhluti sem eru af gerðinni *API*. Þannig geta þeir birt gögn úr gagnagrunnstöflum í gegnum veftengda OData, v4-virka, REST-þjónustu. Ekki er hægt að birta slík gögn í notandaviðmótinu, en er ætlað til að setja á stofn áreiðanlegar samþættingarþjónustur.

Business Central á netinu er í boði með safni af innbyggðu API sem hægt er að nota til að sækja gögn fyrir algengustu viðskiptaeiningarnar, eins og viðskiptavini, vörur, sölupantanir og margt fleira. Engin viðbótarvinna eða uppsetning er nauðsynleg til að nota þessi API sem gagnagjafa fyrir Power BI skýrslur. Frekari upplýsingar um þessi API er að finna í [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

Business Central á netinu styður einnig sérsniðin API. Þróunaraðilar forrita fyrir Business Central-lausnir geta búið til sínar eigin API-síður og fyrirspurnir og pakkað þeim inn í forrit. Þú setur svo forritin upp í leigjandanum. Þegar þær hafa verið settar upp er hægt að nota API-síðurnar fyrir Power BI skýrslurnar eins og þú myndir gera með innbyggða API (v2.0). Nánari upplýsingar um hvernig stofna á API með því að birta síður eða fyrirspurnir er að finna í [Þróun ](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

> [!IMPORTANT]
> Frá og með febrúar 2022 eru Power BI skýrslur fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á netinu fengnar úr afleiddri eftirmynd af skrifvörðum gagnagrunni af afkastaástæðum. Þar af leiðandi ættu AL-þróunaraðilar að forðast að hanna API-síður sem gera breytingar á gagnagrunni á meðan síðurnar eru að opna og hlaða færslum. Íhugaðu sérstaklega kóðann í AL-kveikjum: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord og OnAfterGetCurrRecord. Þessar breytingar á gagnagrunni geta í sumum tilvikum valdið vandræðum með afköst og komið í veg fyrir að skýrslan uppfæri gögnin. Frekari upplýsingar er að finna í [Greinar um afköst fyrir þróunaraðila](/dynamics365/business-central/dev-itpro/performance/performance-developer?branch=main#writing-efficient-web-services) í þróunarefni Business Central.
>
> Í sjaldgæfum tilvikum mun hegðunin valda villu þegar notandi reynir að ná í gögn úr API fyrir skýrslu í Power BI Desktop. Ef breytingar á gagnagrunni eru nauðsynlegar í sérsniðnu API geta Power BI Desktop notendur hins vegar þvingað fram hegðunina. Frekari upplýsingar er að finna í [Búa til Power BI skýrslur til að sýna Business Central-gögn](across-how-use-financials-data-source-powerbi.md#fixing-problems).

### <a name="odata-web-services"></a>OData-vefþjónustur

Þú getur birt hugbúnaðarhluti Business Central, eins og kóðaeiningar, síðu og fyrirspurnir, sem [OData-vefþjónustur](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). Með Business Central á netinu eru margar vefþjónustur birtar sjálfkrafa. Auðveld leið til að finna vefþjónustu er að leita að *vefþjónustu* í [!INCLUDE[prod_short](includes/prod_short.md)]. Á síðunni **Vefþjónusta** skal ganga úr skugga um að reiturinn **Birta** sé valinn fyrir vefþjónustuna sem finna má að ofan. Frekari upplýsingar um birtingu vefþjónustu er að finna á [Birta vefþjónustu](across-how-publish-web-service.md).

Til að fræðast um hvað hægt er að gera til að tryggja bestu frammistöðu vefþjónustunnar, eins og hún birtist úr Business Central Server (endastöð) og frá neytanda (viðskiptavini), skal lesa [Skrifa gagnalega vefþjónustu](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

### <a name="choosing-whether-to-use-api-pages-or-odata-web-services"></a>Velja hvort eigi að nota API-síður eða OData-vefþjónustur

Við hvert tækifæri er mælt með að nota API-síður í stað OData-vefþjónustu. API-síður eru fljótlegri þegar hlaða á gögnum í Power BI skýrslum en vefþjónustu OData. Auk þess eru þær sveigjanlegri vegna þess að þær gera þér kleift að sækja gögn úr töflureitum sem eru ekki skilgreindir í síðuhlut.

<!--## <a name="setup"></a>Set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for Power BI integration

This section explains the requirements for a [!INCLUDE[prod_short](includes/prod_short.md)] on-premises deployment to integrate with Power BI.

1. Configure either [NavUserPassword](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-navuserpassword) or [Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-ad-overview) as the authentication method for the deployment.  
    
    > [!NOTE]
    > Power BI integration doesn't support Windows authentication and is not supported on Windows Client.

2. Enable OData web services and the ODataV4 endpoint.

    OData web service must be enabled on the [!INCLUDE[server](includes/server.md)], and OData port opened in firewall. For more information, see [Configuring Business Central Server - OData Web Services](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    The local server must be accessible from the Internet.

3. Give [!INCLUDE[prod_short](includes/prod_short.md)] user accounts a web service access key.

    A web service access key is only needed to view [!INCLUDE[prod_short](includes/prod_short.md)] data in Power BI. You can assign a web service access key to each user account. Or instead, create a specific account with a web service access key for use by all users. For more information, see [Web Services Authentication](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

    <!--
    > [!IMPORTANT]
    > With [!INCLUDE[prod_short](../developer/includes/prod_short.md)] online, the use of access keys (Basic Auth) for web service authentication is [deprecated](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#accesskeys). We recommend that you use OAuth2 instead. For more information, see [Use OAuth to Authorize Business Central Web Services](/dynamics365/business-central/dev-itpro/webservices/authenticate-web-services-using-oauth).-->

<!--4. Create an application registration for [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure.

    To view Power BI reports embedded in [!INCLUDE[prod_short](includes/prod_short.md)] pages, an application must be registered for [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure. The registered application needs permission to Power BI services. At a minimum, the app requires  **User.ReadWrite.All** permission. For users to view reports from shared Power BI workspaces, the app requires **Workspace.Read.All** permission. For more information, see [Registering [!INCLUDE[prod_short](includes/prod_short.md)] On-Premises in Microsoft Entra ID for Integrating with Other Services](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > If your deployment uses NavUserPassword authentication, [!INCLUDE[prod_short](includes/prod_short.md)] connects to the same Power BI service for all users. You'll specify this service account as part of registering the application. With Microsoft Entra authentication, [!INCLUDE[prod_short](includes/prod_short.md)] connects to the Power BI service associated with the individual user accounts.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
<!--5. Make the initial connection from Business Central to Power BI.

    Before end-users can use Power BI in [!INCLUDE[prod_short](includes/prod_short.md)], an Azure application administrator will have to give consent to the Power BI service.

    To make the initial connection, open [!INCLUDE[prod_short](includes/prod_short.md)], and run **Get Started with Power BI** from the Home page. This action will lead you through the consent process, and check your Power BI license. When prompted sign in using an Microsoft Entra admin account. For more information, see [Connect to Power BI - one time only](across-working-with-powerbi.md#connect).-->

## <a name="setting-up-dataflows"></a>Uppsetning gagnaflæðis

Gagnaflæði gerir kleift að setja inn, breyta og hlaða gögnum inn á Power BI vinnusvæðið og nota gögnin sem grunn fyrir skýrslurnar. Þessi gögn geta í sumum tilfellum upplifað tímabundnar villur þegar endurnýjun er gerð á tímasettri endurnýjun. Villuboðin líta þannig út: `DataSource.Error: OData: Unable to read data from the transport connection: An existing connection was forcibly closed by the remote host.` 

Með PowerAutomate er hægt að setja upp endurtekningar vegna þessa ástands. Nánari upplýsingar eru [í Sjálfkrafa reynir á gagnaflæði um misgáning](/power-query/dataflows/automatically-retry-dataflow).

## <a name="see-also"></a>Sjá einnig .

[Business Central og Power BI](admin-powerbi.md)  
[Power BI Samþættingaríhlutur og hönnunaryfirlit fyrir [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
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
