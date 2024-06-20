---
title: Tengjast við Power BI frá Business Central á staðnum| Microsoft-skjöl
description: 'Það er auðvelt að fá innsýn, viðskiptaupplýsingar og afkastavísi (KPI) í Business Central með Power BI.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 01/22/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# <a name="connect-to-power-bi-from-business-central-on-premises"></a>Tengjast við Power BI frá Business Central á staðnum

<!--In this article, you learn some of the basics about working with reports and dashboards in Power BI that use [!INCLUDE [prod_short](includes/prod_short.md)] as a data source. The article discusses some aspects that will help you get started as a [!INCLUDE[prod_short](includes/prod_short.md)] user. For general guidelines and instructions about using Power BI, see [Power BI documentation for consumers](/power-bi/consumer).

## <a name="get-ready"></a>Get ready

Sign up for the Power BI service. If you haven't already signed up, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). When you sign up, use a work email address and password.-->

## <a name="get-started"></a>Hefjast handa

Til að nota [!INCLUDE [prod_short](includes/prod_short.md)] á staðnum verður að virkja hana til Power BI samþættingar. Þetta verk er vanalega framkvæmt af stjórnanda. Nánari upplýsingar um Power BI virkjun samþættingar við Business Central á netinu eru [í Setja upp Business Central innanhúss fyrir Power BI samþættingu](admin-powerbi-setup.md).

Sumir eiginleikar eru aðeins í boði með Business Central á netinu, ekki á staðnum. Nánari upplýsingar eru [í Introduction to Business Central og Power BI](admin-powerbi.md#what-you-can-do-with-power-bi-and-business-central)

## <a name="set-up--on-premises-for-power-bi-integration"></a><a name="setup"></a>Setja upp [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss fyrir Power BI samþættingu

Þessi hluti útskýrir kröfur fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum til að samþætta við Power BI.

1. Grunnstilla annaðhvort [NavUserPassword](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-navuserpassword) eða [Microsoft Entra Kenni](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-ad-overview) sem sannvottunaraðferð fyrir virkjunina.  
    
    > [!NOTE]
    > Power BI samþætting styður ekki Windows sannvottun og er ekki studd í Windows-biðlara.

2. Virkja OData-vefþjónustu og ODataV4 endastöð .

    OData-vefþjónusta verður að vera virk á [!INCLUDE[server](includes/server.md)], og OData-tengið opnað í eldvegg. Frekari upplýsingar er að finna í [Skilgreining Business Central Server - OData vefþjónustur](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    Staðbundni þjónninn verður að vera aðgengilegur á internetinu.

3. Gefa [!INCLUDE[prod_short](includes/prod_short.md)] notendareikninga aðgangslykil vefþjónustu.

    Aðgangslykill vefþjónustu er aðeins nauðsynlegur til að skoða [!INCLUDE[prod_short](includes/prod_short.md)] gögn í Power BI. Hægt er að úthluta aðgangslykli vefþjónustunnar á hvern notendareikning. Eða þess í stað skaltu stofna tiltekinn reikning með aðgangslykli vefþjónustu til notkunar fyrir alla notendur. Frekari upplýsingar eru í [Sannvottun vefþjónustu](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

4. Búið til forritsskráningu fyrir [!INCLUDE[prod_short](includes/prod_short.md)] í Microsoft Azure.

    Til að skoða Power BI skýrslur sem eru innfelldar á [!INCLUDE[prod_short](includes/prod_short.md)] síður verður forrit að vera skráð fyrir [!INCLUDE[prod_short](includes/prod_short.md)] í Microsoft Azure. Skráð forrit þarf að hafa leyfi fyrir Power BI þjónustunni. Forritið þarf að lágmarki heimildina **User.ReadWrite.All**. Til að notendur geti skoðað skýrslur frá samnýttum Power BI vinnusvæðum þarf forritið heimildina **Workspace.Read.All**. Nánari upplýsingar [eru í Skráning [!INCLUDE[prod_short](includes/prod_short.md)] innanhúss í Microsoft Entra Kenni til samþættingar við aðra þjónustu](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Ef virkjun notar NavUserPassword-sannvottun, tengist [!INCLUDE[prod_short](includes/prod_short.md)] sömu Power BI þjónustunni fyrir alla notendur. Þessi þjónustureikningur er tilgreindur sem hluti af skráningu á forritinu. Með Microsoft Entra sannvottun [!INCLUDE[prod_short](includes/prod_short.md)]  er tengst þjónustunni Power BI sem tengist einstökum notendareikningum.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Gerið upphaflega tengingu frá Business Central til Power BI.

    Áður en notendur geta notað Power BI í [!INCLUDE[prod_short](includes/prod_short.md)] verður stjórnandi Azure-forrits að veita samþykki fyrir Power BI-þjónustunni.

    Til að koma á fyrstu tengingunni skal opna [!INCLUDE[prod_short](includes/prod_short.md)] og keyra **Hefjast handa með Power BI** af heimasíðunni. Þessi aðgerð mun leiða þig í gegnum samþykktarferlið og fara yfir Power BI-leyfið þitt. Þegar beðið er um innskráningu með stjórnunarreikningi Microsoft Entra . Frekari upplýsingar er að finna í [Tengjast við Power BI - aðeins einu sinni](across-working-with-powerbi.md#connect).

## <a name="build-power-bi-reports-to-display--data"></a>Byggja Power BI skýrslur til að birta [!INCLUDE [prod_long](includes/prod_long.md)] gögn

Þú getur gert gögnin þín Dynamics 365 Business Central tiltæk sem gagnagjafa í Power BI Desktop og byggt upp öflugar skýrslur um stöðu fyrirtækisins.

Nota Power BI Desktop til að stofna skýrslur sem sýna Dynamics 365 Business Central gögn. Þegar búið er að stofna skýrslur er hægt að birta þær í Power BI þjónustunni eða deila þeim með öllum notendum í fyrirtækinu. Þegar þessar skýrslur eru í þjónustunni Power BI geta notendur sem hafa verið settir upp fyrir hana skoðað skýrslurnar í Dynamics 365 Business Central.

- Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum skal fá eftirfarandi upplýsingar:

  - OData-vefslóð fyrir [!INCLUDE[prod_short](includes/prod_short.md)].
  
    Yfirleitt er þessi vefslóð með sniðinu `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, til dæmis, `https://localhost:7048/BC190/ODataV4`. Ef um er að ræða virkjun með margleigjanda skal hafa leigjanda á vefslóðinni, til dæmis, `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - Notandanafn og aðgangslykill vefþjónustu af [!INCLUDE[prod_short](includes/prod_short.md)] -reikningi.

    Til að sækja gögn úr [!INCLUDE[prod_short](includes/prod_short.md)] notar Power BI grunnsannvottun. Svo þarftu að fá notandanafn og aðgangslykil vefþjónustu til að tengjast. Reikningurinn gæti verið þinn eigin notandareikningur eða fyrirtækið kann að hafa sérstakan reikning í þeim tilgangi.

## <a name="add--as-a-data-source-in-power-bi-desktop"></a><a name="getdata"></a>Bæta [!INCLUDE[prod_short](includes/prod_short.md)] við sem gagnaveitu í Power BI Desktop

Fyrsta verk í stofnun skýrslna er að bæta [!INCLUDE[prod_short](includes/prod_short.md)] við sem gagnagjafa á Power BI Desktop. Þegar það er tengt er hægt að byrja að búa til skýrslu.

1. Ræsið Power BI Desktop.
2. Velja **Fá-gögn**.

    Ef þú sérð ekki **Sækja gögn** skaltu velja **Skrá** valmyndina og síðan **Sækja gögn**.
3. Á síðunni **Sækja gögn** skaltu velja **Netþjónusta**.
4.  **Á glugganum Netþjónusta** er tengst  [!INCLUDE [prod_short](includes/prod_short.md)] við staðbundið svæði, valið **Dynamics 365 Business Central  (innanhúss)** og síðan **tengst**.
5. Skráðu þig inn í [!INCLUDE [prod_short](includes/prod_short.md)] (aðeins í eitt skipti).

    Ef þú hefur ekki skráð þig inn í [!INCLUDE [prod_short](includes/prod_short.md)] úr Power BI skjáborðinu verður þú beðin(n) um að skrá þig inn.

   - Fyrir [!INCLUDE [prod_short](includes/prod_short.md)] á staðnum skal fyrst færa inn OData-vefslóðina fyrir [!INCLUDE[prod_short](includes/prod_short.md)] og síðan velja **Í lagi**. Síðan skal færa inn notandanafn og aðgangsorð reikningsins sem á að nota til að tengjast við [!INCLUDE[prod_short](includes/prod_short.md)] þegar beðið er um það. Færa skal inn aðgangslykil vefþjónustunnar í reitinn **Aðgangsorð**. Þegar því er lokið velur þú **Tengjast**.
   
    > [!NOTE]  
    > Þegar þú hefur tengst við [!INCLUDE[prod_short](includes/prod_short.md)] verð þú ekki beðinn aftur um að skrá þig inn. [Hvernig breyti ég eða hreinsa reikninginn sem ég nota núna til að tengjast Business Central frá Power BI Desktop?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Þegar þú hefur tengst, Power BI tengiliðir við Business Central-þjónustuna. Glugginn **Skoðun** birtist og sýnir tiltæka gagnagjafa til að búa til skýrslur. Veldu möppu til að stækka hana og sjá tiltæka gagnagjafa. 

   Þessi gagnagjafar standa fyrir allar vefþjónusturnar og API-síðurnar sem eru gefnar út fyrir [!INCLUDE [prod_short](includes/prod_short.md)]. Gagnagjöfunum er flokkað eftir umhverfum og fyrirtækjum Business Central.

   > [!NOTE]
    > Skipulagið fyrir Business Central á staðnum er öðruvísi vegna þess að það styður ekki API-síður.

7. Veldu gagnagjafana eða upprunastaðina sem þú vilt bæta við gagnalíkanið þitt og veldu svo hnappinn **Hlaða**.
8. Ef þú vilt síðar bæta við frekari gögnum Business Central er hægt að endurtaka fyrri skref.

Þegar gögnum hefur verið hlaðið er hægt að sjá þau á hægra yfirlitssvæði síðunnar. Þér tókst að tengjast gögnum þínum í [!INCLUDE[prod_short](includes/prod_short.md)] og getur byrjað að byggja upp Power BI-skýrsluna þína.  

> [!TIP]
> Frekari upplýsingar um notkun Power BI Desktop eru í [Hafist handa með Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="manage-and-modify-reports"></a>Stjórna og breyta skýrslum

> [!NOTE]
> Ekki er hægt að stjórna og breyta skýrslum. 

## <a name="upload-reports"></a>Hlaða inn skýrslum

Fyrir [!INCLUDE [prod_short](includes/prod_short.md)] á staðnum eru engar kynningarskýrslur tiltækar, þannig að þú verður að byrja frá grunni með því að nota Power BI Desktop.  Power BI Einnig er hægt að dreifa skýrslum sem skrám sem hægt er að hlaða beint upp frá Power BI netþjónustu. Frekari upplýsingar er að finna á [Hlaða upp skýrslu á þjónustu](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

<!--
> [!NOTE]
> Uploading a report requires that you have SUPER user permissions in [!INCLUDE[prod_short](includes/prod_short.md)]. Also, you can't upload reports with [!INCLUDE [prod_short](includes/prod_short.md)] on-premises. With on-premises, you upload reports directly to your Power BI workspace. For more information, see [Connect to Power BI from [!INCLUDE [prod_short](includes/prod_short.md)] on-premises](across-working-with-business-central-in-powerbi.md).

<!--Once you have a Power BI account, you can sign in at [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

The Power BI service hosts all the reports available to you. To see the report, select **My Workspace** > **Reports**. Then just select the report that you want to view.

With [!INCLUDE[prod_short](includes/prod_short.md)] online, you'll automatically have a set of default reports on your workspace. If you want to create your own reports, you can use Power BI Desktop to create reports, and then publish them to your workspace. For more information, see [Getting Started Building Reports in Power BI Desktop to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, you'll have to start from scratch by using Power BI Desktop. Optionally, Power BI reports can be distributed as files, that you can upload.

<!--## Get the latest data

Each Power BI report is based on a dataset that gets data from the [!INCLUDE[prod_short](includes/prod_short.md)] sources. You want to make sure that the data in your Power BI reports is up to date with the data in [!INCLUDE[prod_short](includes/prod_short.md)]. This concept is referred to as *refreshing*.  Depending on how your organization has set up Power BI, refreshing might not happen automatically. There are two ways to refresh data: manually or by scheduling a refresh. Manual refreshing is done on-demand, as needed. Scheduled refreshing lets you refresh automatically at defined time intervals.

### <a name="refresh-manually"></a>Refresh manually

In the navigation pane, under **Datasets**, select **More options (...)** next to the dataset, then select **Refresh now**.

### <a name="schedule-a-refresh"></a>Schedule a refresh

In the navigation pane, under Datasets, select More options (...) next to the dataset, then select **Schedule refresh**. Fill in the information under the **Schedule refresh** section, and select **Apply**.

For more information, see [Configure scheduled refresh](/power-bi/connect-data/refresh-scheduled-refresh)-->

<!--## <a name="upload"></a>Upload reports from files

Power BI Reports can be distributed among users as .pbix files. If you have a .pbix file, you can upload the file to a workspace. To upload a report, do the following steps:

1. In your new workspace, select **Get Data**.

2. In the Files box, select **Get**.

3. Select **Local File**, navigate to where you saved the file, and select **Open**.

For more information, see [Upload the report to the service](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

> [!NOTE]
> Uploading a report requires that you have a [Premium capacity](/power-bi/service-premium-what-is) work space. For more information, see [Managing Premium capacities](/power-bi/admin/service-premium-capacity-manage). 

> [!TIP]
> If you're using [!INCLUDE[prod_short](includes/prod_short.md)] online, you can also upload a report from within [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Work with Power BI Reports in [!INCLUDE [prod_short](includes/prod_short.md)] - Upload Reports](across-working-with-powerbi.md#upload).

## <a name="share-reports-with-others"></a><a name="share"></a>Share reports with others

Once a report is in your workspace, you can share it with others in your organization.

To share a report, in a list reports, or in an open report, select **Share**. In the **Share report** pane, enter the full email addresses for individuals or distribution groups you want to share with. Follow the instructions on screen to complete the sharing. For more information, see [Share a dashboard or report](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> You must have  [Power BI Pro license](/power-bi/service-features-license-type), and the people you share with do too. The content must be in a workspace in a [Premium capacity](/power-bi/service-premium-what-is). For more information, see [Ways to share your work in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).-->

## <a name="see-also"></a>Sjá einnig .

[Business Central og Power BI](admin-powerbi.md)  
[Hlaða inn skýrslum](across-working-with-business-central-in-powerbi.md#upload-reports)
 
[!INCLUDE[footer-include](includes/footer-banner.md)]
