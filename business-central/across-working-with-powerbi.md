---
title: Unnið með Power BI skýrslur í Business Central| Microsoft-skjöl
description: 'Fáðu innsýn, viðskiptaupplýsingar og afkastavísi (KPI) úr Business Central gögnum með Power BI.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 04/24/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# <a name="work-with-power-bi-reports-in-"></a>Vinna með Power BI skýrslur í [!INCLUDE [prod_short](includes/prod_short.md)]

Í þessari grein lærir þú nokkrar af grunnatriðum um að vinna með skýrslur. Þar með talið eru skoðaðar Power BI skýrslur inni [!INCLUDE [prod_short](includes/prod_short.md)]  (þ.m.t. árangursmat og mælaborð) og breytingar Power BI á skýrslum sem nota [!INCLUDE [prod_short](includes/prod_short.md)] sem gagnagjafa. Greinin fjallar um suma þætti sem munu hjálpa til við að hefjast handa sem [!INCLUDE[prod_short](includes/prod_short.md)] notandi. Almennar leiðbeiningar og leiðbeiningar um notkun á Power BI er að finna í [Power BI fylgigögnum fyrir neytendur](/power-bi/consumer).

## <a name="overview"></a>Yfirlit

Power BI skýrslur veita innsýn inn í [!INCLUDE[prod_short](includes/prod_short.md)]. Ýmsar síður í [!INCLUDE [prod_short](includes/prod_short.md)] innihalda Power BI-skýrsluhluta sem getur birt Power BI skýrslur. Hlutverkamiðstöð er dæmigerð síða þar sem þú sérð Power BI skýrsluhluta. Sumar listasíður, eins og **Vörur**, innihalda einnig Power BI hluta.

[!INCLUDE [prod_short](includes/prod_short.md)] vinnur með Power BI þjónustunni. Skýrslur fyrir birtingu í [!INCLUDE [prod_short](includes/prod_short.md)] eru geymdar í Power BI-þjónustu. Í [!INCLUDE [prod_short](includes/prod_short.md)] er hægt að skipta skýrslunni sem birtist í Power BI hlutanum til allra Power BI-skýrslna sem eru í boði í Power BI þjónustunni. Í fyrsta skipti sem þú skráir þig inn á [!INCLUDE [prod_short](includes/prod_short.md)], og þar til þú tengist Power BI-þjónustu, eru hlutar auðir, eins og sýnt er hér:

![Power BI hluti í Business Central.](./media/power-bi-part.png)

## <a name="get-started"></a>Hefjast handa

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] á netinu er þegar uppsett til að samþætta sig við Power BI.

### <a name="sign-up-power-bi"></a>Skráning Power BI

Áður en hægt er að nota Power BI með [!INCLUDE[prod_short](includes/prod_short.md)] þarf að skrá sig fyrir Power BI-þjónustunni. Ef þú hefur ekki þegar skráð þig skaltu fara á [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Þegar þú skráir þig skaltu nota vinnunetfang og aðgangsorð.

Þegar þú ert með Power BI-reikning geturðu skráð þig inn á [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

Power BI þjónustan hýsir allar skýrslur sem eru í boði. Til að sjá skýrslu á vinnusvæðið er Vinnubilsskýrslur **mínar valdar.** > **·** Veljið svo skýrsluna sem á að skoða. Ef notandi hefur aðgang að einu eða fleiri samnýttum Power BI vinnusvæðum er einnig hægt að sjá skýrslur á þessum vinnusvæðum.

Með [!INCLUDE[prod_short](includes/prod_short.md)] á netinu er sjálfkrafa hægt að hafa sjálfgefnar skýrslur á vinnusvæðinu. Ef stofna á eigin skýrslur er hægt að nota Power BI Desktop til að stofna skýrslur og birta þær síðan á eigin vinnusvæði. Frekari upplýsingar er að finna í [Hafist handa með skýrslur í Power BI Desktop til að birta [!INCLUDE [prod_long](includes/prod_long.md)] gögn](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

## <a name="connect-to-power-bi---one-time-only"></a><a name="connect"></a>Tengjast við Power BI - aðeins einu sinni

Þegar þú skráir þig inn í [!INCLUDE [prod_short](includes/prod_short.md)] í fyrsta skipti sérðu líklega auðan Power BI hluta (eins og sýnt er á fyrri mynd) á ýmsum síðum. Það fyrsta sem þú skalt gera er að tengjast Power BI -reikningnum þínum. Eftir tengingu er hægt að skoða skýrslur. Þú þarft aðeins að gera þetta einu sinni.

1. Veljið tengilinn **Hefjast handa með Power BI** í hlutanum **Power BI Skýrslur**.
2. Uppsetningarleiðbeiningin **Setja upp Power BI skýrslur í Business Central** hefst. Veldu **Næst** til að halda áfram.
3. Á síðunni **Athugaðu Power BI-leyfið þitt**. Framkvæmdu eitt af eftirfarandi skrefum:

    - Ef þú hefur ekki enn skráð þig fyrir Power BI skaltu velja [Fara á Power BI heimasíðu](https://powerbi.microsoft.com). Skráðu þig fyrir reikningi, farðu síðan aftur á [!INCLUDE[prod_short](includes/prod_short.md)] og kláraðu uppsetninguna.

    - Ef þú ert þegar með leyfi skaltu velja **Næst**.
4. Á næstu síðu mun [!INCLUDE[prod_short](includes/prod_short.md)] nú hlaða upp sýniútgáfu af skýrslu í Power BI. Þetta tekur nokkrar mínútur, svo það er gert í bakgrunni. Til að ljúka uppsetningunni skal velja **Næst** og síðan **Ljúka**.

Tengingarferlið hefst. Við ferlið hefur [!INCLUDE [prod_short](includes/prod_short.md)] samskipti við Power BI-þjónustuna til að komast að því hvort þú sért með gildan Power BI-reikning og leyfi. Þegar leyfið þitt hefur verið staðfest birtast sjálfgefna Power BI-skýrslan á heimasíðunni þinni. Ef engin skýrsla birtist er hægt að velja skýrslu úr hlutanum.

> [!TIP]
> Á [!INCLUDE [prod_short](includes/prod_short.md)] netinu hlaða þetta skref sjálfkrafa upp sjálfgefnum Power BI skýrslum sem notaðar eru á [!INCLUDE [prod_short](includes/prod_short.md)]  Power BI vinnusvæðið.

<!--#### From [!INCLUDE [prod_short](includes/prod_short.md)] on-premises

Connecting to Power BI from [!INCLUDE [prod_short](includes/prod_short.md)] is similar to online. However, you might be prompted on the **MICROSOFT ENTRA SERVICE PERMISSIONS** page to grant access to Power BI Services. To grant access, select **Authorize Azure Services**, and then **Accept**.

Once connected, you can select a report from the Power BI part on pages.-->

## <a name="work-with-power-bi-reports"></a>Vinna með Power BI skýrslur

### <a name="get-the-latest-data"></a>Fá nýjustu gögnin

Hver Power BI skýrsla byggir á gagnasafni sem fær gögn frá [!INCLUDE[prod_short](includes/prod_short.md)] uppruna. Þú vilt ganga úr skugga um að gögnin í Power BI-skýrslunum séu uppfærð með gögnunum í [!INCLUDE[prod_short](includes/prod_short.md)]. Þetta hugtak er nefnt *uppfærsla*.  Ekki er víst að endurnýjun gerist sjálfkrafa, allt eftir því hvernig fyrirtækið hefur sett upp Power BI. Það eru tvær leiðir til að uppfæra gögn: handvirkt eða með því að tímasetja uppfærslu. Handvirk endurnýjun fer fram eftir þörfum. Áætluð endurnýjun gerir þér kleift að uppfæra sjálfkrafa á skilgreindum tímabilum.

#### <a name="refresh-manually"></a>Uppfæra handvirkt

Frá Power BI netinu, á yfirlitssvæðinu, undir **Datasets**, veljið **Fleiri valkosti (...)** Við hlið gagnasafnsins skal velja **Endurnýja núna**.

#### <a name="schedule-a-refresh"></a>Áætla uppfærslu

Frá Power BI netinu, á yfirlitssvæðinu, undir Datasets, skal velja Fleiri valkosti (...) við hlið gagnamengisins og velja **svo Tímasetja endurnýjun**. Fylltu út upplýsingarnar í **Tímasetja uppfærslu** og veldu **Not**.

Frekari upplýsingar eru í [Grunnstilla uppfærsluáætlun](/power-bi/connect-data/refresh-scheduled-refresh)

### <a name="show-reports-on-list-pages"></a>Sýna skýrslur á listasíðum

[!INCLUDE[prod_long](includes/prod_long.md)] inniheldur Power BI upplýsingareit á nokkrum lyklalistasíðum. Þessi upplýsingareitur veitir frekari innsýn í gögnin á listanum. Þegar farið er milli lína í listanum er skýrslan uppfærð og síuð fyrir valda færslu.

Frekari upplýsingar um hvernig á að búa til skýrslur fyrir listasíður er að finna í [Stofna Power BI skýrslur til að birta listagögn í [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

> [!TIP]
> Ef þú sérð ekki Power BI upplýsingareitinn gæti hann verið falinn á vinnusvæðinu þínu vegna sérstillingar. Veldu ![Stillingar.](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") táknið og veldu síðan aðgerðina **Sérsníða**. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).
>
> Eða ef þú ert með eldri útgáfu af Business Central skaltu fara á aðgerðastikuna, velja **Aðgerðir** > **Birta** > **Sýna/fela Power BI skýrslur**.

### <a name="switch-reports"></a>Skipta í aðra skýrslu

Power BI hluti á síðu getur birt allar Power BI skýrslur sem þú hefur aðgang að. Til að skipta yfir í aðra skýrslu skal velja **Velja skýrslu** aðgerðina úr fellilista sem er efst í hlutanum.  

**Power BI Síða skýrsluvals** sýnir lista yfir allar Power BI-skýrslur sem þú hefur aðgang að. Þessi listi er sóttur úr vinnusvæðum þínum eða vinnusvæðum sem deilt hefur verið með þér í Power BI þjónustunni. Veldu **Virkja** fyrir allar þær skýrslur sem þú vilt birta á heimasíðunni og veldu síðan **Í lagi**. Þú munt fara aftur á síðuna og síðasta skýrsla sem þú virkjaðir birtist. Í fellilistanum með skipunum skaltu nota skipanirnar **Fyrri** og **Næsta** til að fletta á milli skýrsla.  

### <a name="get-more-reports"></a>Fá fleiri skýrslur

Ef þú sérð engar skýrslur á síðunni **Power BI Skýrsluval** eða sérð ekki skýrsluna sem þú vilt skaltu velja **Fá skýrslur**. Þessi aðgerð gerir þér kleift að leita að skýrslum frá tveimur staðsetningum: *Fyrirtækið mitt* eða *Þjónusta*.

- Veldu **Fyrirtækið mitt** til að fara í Power BI þjónustuna. Hér að neðan er hægt að skoða skýrslurnar innan fyrirtækisins sem þú hefur fengið heimild til að skoða. Síðan er hægt að bæta þeim við vinnusvæðið.
- Veldu **Þjónustur** til að fara í Microsoft AppSource þar sem þú getur sett upp Power BI-forrit.  

> [!TIP]
> Ef þú ert með Power BI Desktop geturðu einnig búið til nýjar Power BI skýrslur. Þegar þessar skýrslur eru gefna út á Power BI-vinnusvæðið þitt, birtast þær á síðunni **Power BI Skýrsluval**.  

### <a name="manage-and-modify-reports"></a>Stjórna og breyta skýrslum

Hægt er að gera breytingar á skýrslu í Power BI hlutanum. Breytingarnar sem þú gerir verða síðan birtar í Power BI-þjónustunni. Ef verið er að deila skýrslum með öðrum notendum sjá þeir einnig breytingarnar, nema breytingar séu vistaðar í nýja skýrslu.

Til að breyta skýrslu skal velja aðgerðina **Stjórna skýrslu** úr fellilista í Power BI hlutanum. Byrjaðu svo að gera breytingar. Þegar þú hefur lokið við að gera breytingar skaltu velja **Skrá** > **Vista**. Ef þetta er samnýtt skýrsla og þú vilt koma í veg fyrir að gera þessa breytingu fyrir alla notendur skaltu velja **Vista sem**.

Þegar þú ferð aftur í Mitt hlutverk mun uppfærða skýrslan birtast þar. Ef **Vista sem** r notað þarf að velja **Velja skýrslu** og virkja svo nýja skýrslu til að sjá hana.

> [!NOTE]
> Þessi eiginleiki er ekki í boði með [!INCLUDE [prod_short](includes/prod_short.md)] á staðnum.

### <a name="upload-reports"></a><a name="upload"></a>Hlaða upp skýrslum

Hægt er að dreifa Power BI skýrslum á meðal notenda sem. pbix-skrám. Ef þú ert með .pbix-skrár er hægt að hlaða þeim upp og deila þeim með öllum notendum [!INCLUDE [prod_short](includes/prod_short.md)]. Skýrslunum er deilt innan hvers fyrirtækis í [!INCLUDE [prod_short](includes/prod_short.md)].  

Til að hlaða upp skýrslu skaltu velja aðgerðina **Hlaða upp skýrslu** úr fellilistanum yfir skipanir á hlutanum **Power BI Skýrslur**. Síðan skaltu finna .pbix-skrá sem skilgreinir skýrsluna sem þú vilt deila. Þá er hægt að breyta sjálfgefnu skráarinnar.  

Þegar skýrslunni hefur verið hlaðið upp á Power BI-vinnusvæðið þitt hleðst hún sjálfkrafa upp á Power BI-vinnusvæði annarra.

> [!NOTE]
> Ef skýrslu er hlaðið upp með [!INCLUDE[prod_short](includes/prod_short.md)] þarf ofurnotandaheimild. [!INCLUDE[prod_short](includes/prod_short.md)] Ekki þarf neinar sérstakar heimildir til að hlaða skýrslum inn á vinnusvæðið með þjónustunni Power BI .

## <a name="upload-reports-from-files"></a><a name="upload"></a>Hlaða upp skýrslum úr skrám

Hægt er að dreifa Power BI skýrslum á meðal notenda sem. pbix-skrám. Ef þú ert með .pbix-skrá er hægt að hlaða skránni upp á vinnusvæði. Til að hlaða upp skýrslu skal gera eftirfarandi:

1. Á nýja vinnusvæðinu skal velja **Sækja gögn**.

2. Í reitnum Skrár skal velja **Sækja**.

3. Veldu **Staðbundin skrá**, farðu þangað sem hún er vistuð og veldu **Opna**.

Frekari upplýsingar er að finna á [Hlaða upp skýrslu á þjónustu](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

<!--
> [!NOTE]
> Uploading a report requires that you have a [Premium capacity](/power-bi/service-premium-what-is) work space. For more information, see [Managing Premium capacities](/power-bi/admin/service-premium-capacity-manage). -->

> [!TIP]
> Ef þú notar [!INCLUDE[prod_short](includes/prod_short.md)] á netinu geturðu einnig hlaðið upp skýrslu úr [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar er að finna í [Vinna með Power BI skýrslur í [!INCLUDE [prod_short](includes/prod_short.md)] - Hlaða upp skýrslum](across-working-with-powerbi.md#upload).

## <a name="share-reports-with-others"></a><a name="share"></a>Deila skýrslum með öðrum

Þegar skýrsla er á vinnusvæðinu er hægt að deila henni með öðrum í fyrirtækinu.

Til að deila skýrslu, í listaskýrslum, eða í opinni skýrslu skal velja **Deila**. Á hlutanum **Deila skýrslu** skal slá inn fullt netfang fyrir einstaklinga eða hóp viðtakenda sem á að deila með. Fylgdu leiðbeiningunum á skjánum til að ljúka deilingunni. Frekari upplýsingar er að finna á [Deila stjórnborði eða skýrslu](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> Þess er krafist að bæði þú og fólkið sem þú deilir skýrslunni með [Power BI Pro leyfi](/power-bi/service-features-license-type). Að öðrum kosti verður efnið að vera í [iðgjaldagetu](/power-bi/service-premium-what-is). Nánari upplýsingar eru í [Aðferðir við að deila vinnu þinn í Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).

## <a name="fixing-problems"></a>Vandamál lagfærð

Hins vegar, ef eitthvað fer úrskeiðis, þessi kafli gefur lausn fyrir dæmigerður vandamál.  

### <a name="you-dont-have-a-power-bi-account"></a>Þú ert ekki með Power BI reikning

Power BI-Reikningur hefur ekki verið settur upp. Til að fá gildan Power BI reikning verður þú að vera með leyfi og þú þarf að hafa skráð þig inn í Power BI til að stofna Power BI vinnusvæði.

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Skilaboð: Engar skýrslur eru virkar. Veljið Velja skýrslu til að sjá hvaða skýrslur er hægt að birta.

Þessi skilaboð birtast ef ekki tókst að virkja sjálfgefna skýrslu á Power BI vinnusvæði. Eða það var virkjað en uppfærðist ekki. Farðu í skýrsluna á Power BI vinnusvæðinu, velja **Gagnasafn**, **Stillingar** og uppfæra svo skilríkin handvirkt. Þegar gagnasafnið hefur verið endurnýjað er farið aftur í [!INCLUDE[prod_short](includes/prod_short.md)] og valið skýrslu handvirkt af **Velja skýrslur** síðunni.

#### <a name="you-cant-see-a-report-on-the-select-report-page-on-a-list-page"></a>Ekki er hægt að sjá skýrslur á síðu skýrsluvals á listasíðunni

Það er líklega vegna þess að heiti skýrslunnar inniheldur ekki heiti listasíðunnar. Hreinsaðu síuna til að birta heildarlista yfir skýrslur sem eru tiltækar í Power BI.

## <a name="see-also"></a>Sjá einnig .

[Business Central og Power BI](admin-powerbi.md)    
[Byggingarskýrslur Power BI til að birta [!INCLUDE [prod_long](includes/prod_long.md)] gögn](across-how-use-financials-data-source-powerbi.md)    
[Power BI Samþættingaríhlutur og arkitektúryfirlit fyrir [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)    
[Tengjast við Power BI innanhúss [!INCLUDE [prod_short](includes/prod_short.md)]](across-working-with-business-central-in-powerbi.md)    
[Power BI fyrir neytendur](/power-bi/consumer/end-user-consumer)     
['nýtt útlit' þjónustunnar Power BI](/power-bi/service-new-look)    
[QuickStart: Tengjast gögnum í Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)    
[Power BI Skjöl](/power-bi/)    
[Viðskiptagreind](bi.md)    
[Að verða tilbúinn fyrir að gera viðskipti](ui-get-ready-business.md)    
[Innflutningur viðskiptagagna frá öðrum fjármálakerfum](across-import-data-configuration-packages.md)    
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)    
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem gagnagjafa Power BI](across-how-use-financials-data-source-powerapps.md)    
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] sem gagnagjafa Power Apps](across-how-use-financials-data-source-powerapps.md)    
[Nota [!INCLUDE[prod_short](includes/prod_short.md)] í Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
