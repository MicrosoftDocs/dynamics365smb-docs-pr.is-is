---
title: Algengar spurningar um Power BI
description: Fáðu svör við dæmigerðum spurningum um Power BI og Business Central.
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'Power BI, reports, faq, errors'
ms.date: 04/22/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="power-bi--faq"></a>ALGENGAR SPURNINGAR UM Power BI

Þessi grein svarar einhverjum þeirra spurninga sem þú gætir haft um notkun á Power BI og [!INCLUDE [prod_short](includes/prod_short.md)].

## [Almennt](#tab/general)
<!-- 26 -->
### <a name="ive-selected-a-report-for-my-role-center-in-business-central-if-i-later-make-changes-to-the-reports-visuals-online-will-the-role-center-automatically-update-to-my-changes"></a>Ég valdi skýrslu fyrir hlutverkamiðstöðina mína í Business Central. Ef ég breyti myndefni skýrslunnar síðar á netinu, uppfærist hlutverkamiðstöðin sjálfvirkt í samræmi við breytingarnar mínar?

Já, því skýrslurnar eru innfelldar úr Power BI.

<!-- 3 -->
### <a name="are-the-business-central-apps-for-power-bi-available-in-languages-other-than-english"></a>Eru Business Central forritin fyrir Power BI í boði á öðrum tungumálum en ensku?

Fj. Þessi forrit eru aðeins í boði á ensku eins og er.

<!-- 24 -->
### <a name="once-a-report-is-published-on-mypowerbicomworkspace-can-i-download-its-pbix"></a>Þegar skýrsla er birt á vinnusvæði powerbi.com, get ég sótt pbix hennar?

Já. Frekari upplýsingar eru í [Hlaða niður skýrslu frá Power BI þjónustunni til Power BI Desktop](/power-bi/create-reports/service-export-to-pbix).  

<!-- 27 -->
### <a name="can-i-download-the-apps-as-pbix-files"></a>Get ég sótt forritin sem pbix-skrár?

Fj. Sem stendur bjóðum við ekki upp á að sækja pbix-skrár fyrir opinber Power BI forrit vegna þess að þær eru birtar á AppSource.

## [Leyfi](#tab/license)

<!-- 14 -->
### <a name="do-i-need-a-power-bi-pro-license-to-publish-reports"></a>Þarf ég Power BI Pro leyfi til að birta skýrslur?

<!-- todo What does " or for every user that consults the published report" mean? fixed -->
Fj. Ekki er þörf á Pro leyfi til að birta skýrslur. Staðlað (ókeypis) Power BI leyfi nægir. Frekari upplýsingar er að finna á [Power BI Leyfisveiting](admin-powerbi-setup.md#license).

<!-- 15 -->
### <a name="is-there-anything-i-cant-do-with-the-free-license"></a>Er eitthvað sem ég get ekki gert með ókeypis leyfinu?

Ekki er hægt að deila skýrslum eða setja upp Business Central forrit fyrir Power BI. Að öðru leyti gerir ókeypis leyfið þér kleift að stofna nánast öll afbrigði af línuriti og skýrslum.

<!-- 16 -->
### <a name="if-someone-shares-a-report-with-another-person-then-that-person-needs-a-pro-license-to-see-the-report-are-there-plans-to-make-this-capability-possible-with-the-free-license"></a>Ef einhver deilir skýrslu með öðrum þarf sá aðili Pro leyfi til að skoða skýrsluna. Eru áætlanir um að bjóða upp á þessa möguleika ókeypis leyfinu?

Við stjórnum ekki þessari kröfu. Þessi krafa er sett af Power BI. Frekari upplýsingar eru í [Deila Power BI stjórnborðum og skýrslum með samstarfsfólki og öðrum](/power-bi/collaborate-share/service-share-dashboards).  

## [Hönnuður](#tab/designer)

<!-- 7 -->
### <a name="does-the-connector-work-with-api-pages"></a>Virkar tengið með API-síðum?

Já. Frá og með júní 2021 mun nýja Power BI tengingin styðja bæði vefþjónustu Business Central og API-síður. Frekari upplýsingar eru í [Virkja Power BI tengi til að vinna með API fyrir Business Central í stað þess að nota eingöngu vefþjónustu](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

### <a name="can-i-build-a-power-bi-report-using-the-sales-invoice-lines-or-journal-lines-apis"></a>Get ég smíðað Power BI skýrslu með API sölureikningslína eða færslubókarlína?

Mest notuðu færslulínurnar eru tiltækar í [Business Central API v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/)). Þú getur notað þær til að búa til skýrslur í Power BI með því að velja þær í **Dynamics 365 Business Central** tenginu. Hins vegar eru **Línur** API hannaðar til að vera aðeins notaður með mjög sértækum síum og virka kannski ekki við þínar aðstæður. Villa gæti komið upp svipað og „Tilgreina verður kenni eða kenni fylgiskjals til að sækja línurnar“. Gerðu eftirfarandi til að leysa úr þessu vandamáli þegar þú færð gögn frá Business Central fyrir skýrsluna í Power BI Desktop:

1. Í stað þess að innihalda gagnagjafann fyrir línurnar skaltu bæta við yfirgagnagjafanum. Til dæmis bæta við **Sölureikningi** í staðinn fyrir **Sölureikningslínum**.
2. Veldu **Umbreyta gögnum** í Power BI Desktop aðgerðarstikunni.
3. Veldu fyrirspurnina sem þú varst að bæta við, t.d. **Sölureikningar**.
4. Settu á allar nauðsynlegar síur á færslurnar til að draga úr færslumagninu sem þú hleður inn í skýrsluna.
5. Flettu til hægri þar til þú finnur dálk sem heitir það sama og línurnar, t.d. **SalesInvoiceLines**.
6. Veldu útvíkkunarhnappinn í hausn dálksins við hliðina á dálkheitinu.

   :::image type="content" source="media/saleinvoicelines.png" alt-text="Sýnir dálkinn SalesInvoiceLines í Power BI Desktop.":::
<!-- 11 --> 
### <a name="is-it-possible-to-choose-which-business-central-environment-to-get-data-from-for-power-bi-for-example-like-a-sandbox-or-production-environment"></a>Er hægt að velja hvaða Business Central umhveri á að sækja gögn frá, Power BI eins og sandkassa eða framleiðsluumhverfi?

Já. Það er auðvelt að velja það. Þegar tengt er við Business Central með tengingunni þarf að velja umhverfi og heiti fyrirtækis.

<!-- 6 --> 
### <a name="can-i-merge-data-from-several-production-environments-of-the-same-tenant"></a>Get ég sameinað gögn úr nokkrum framleiðsluumhverfum í sama leigjanda?

Já. Í Power BI skaltu keyra gagnaaðgerðina aftur og velja það umhverfi sem þú vilt.

<!-- 25 -->
### <a name="which-pages-in-business-central-have-the-power-bi-report-part"></a>Hvaða síður í Business Central eru með Power BI Report hlutann?

Sem stendur eru nokkrar valdar síður með upplýsingareit með hlutanum **Power BI Skýrslur** til að birta skýrslu. 

Á listasíðum er hlutinn **Power BI Skýrslur** síaður til að sýna skýrslur sem varða gögn á listanum. Hér er listi yfir tegundarsíður sem innihalda hlutann **Power BI Skýrslur**:

|Síðukenni|Name|
|-------|----|
|22|Viðskiptamannalisti|
|27|Listi yfir söluaðila|
|31|Birgðalisti|
|9305|Sölupantanalisti|
|9308|Innkaupareikningar|

Hér eru aðrar síður sem innihalda stærri, ósíaða **Power BI skýrsluhlutann**:

|Síðukenni|Name|
|-------|----|
|1156|Fyrirtækisupplýsingar|
|4013|Innsýn í Intelligent Cloud |
|9006|Hlutverkamiðstöð pöntunargjörva|
|9008|Vöruh. Grunnhlutverkamiðstöð|
|9010|Hlutverkamiðstöð framleiðslustjórnanda|
|9015|Verkefnastjóri verks RC|
|9016|Afgreiðslustjórnun þjónustu hlutverkamiðstöðvar|
|9022|Mitt hlutverk – viðskiptastjórnandi|
|9024|Mitt hlutverka – öryggisstjórnandi|
|9026|Sölu- og tengslastjórnun RC|
|9027|Endurskoðandi Mitt hlutverk|

> [!TIP]
> Við erum ekki með áætlanir um að bæta því við allar listasíður eins og er. Hins vegar er hægt að stofna einfalda síðuviðbót sem bætir **Power BI Skýrslur** hltanum við í upplýsingareitinum. Frekari upplýsingar eru í [Bæta Power BI skýrsluhlutum við síður](/dynamics365/business-central/dev-itpro/developer/devenv-power-bi-report-parts) í hjálp Developer and IT Pro.

<!-- 5 -->
### <a name="is-there-any-way-to-filter-a-dataset-from-business-central-before-i-pull-it-into-power-bi-instead-of-applying-filters-afterwards"></a>Er einhver leið til að sía gagnasafn frá Business Central *áður* en ég dreg það inn í Power BI, í stað þess að nota síur á eftir?

Til að sía stærri gagnasöfn er auðveldast að setja síu á Power BI skýrsluna með því að breyta Power Query formúlunni. Flestar þær síur sem eru stilltar á þennan hátt verða færðar yfir á Business Central í gegnum födlun fyrirspurna. Sjá [Regluleg uppfærsla fyrir gagnamengi](/power-bi/admin/service-premium-incremental-refresh).

Ekki hægt að setja upp síu fyrir vefþjónustugögnin innan Business Central eins og er. Ef forritið þarf að setja upp síu innan Business Central þarf að stofna sérsniðið Business Central forrit í þeim tilgangi.

<!-- 10 -->
### <a name="from-power-bi-besides-using-a-query-is-there-another-way-to-get-data-from-business-central-tables-that-dont-have-an-associated-page-for-example-like-the-item-attributes-value-mapping-table"></a>Úr Power BI, er til önnur leið til að sækja gögn úr Business Central töflum sem tengjast ekki síðu, fyrir utan að nota fyrirspurn? Sem dæmi má nefna töfluna *Gildisvörpun vörueigindar*.

Fj. Ekki núna.

<!-- 12 --> 
### <a name="are-published-queries-faster-to-use-than-published-pages"></a>Eru fljótlegra að nota birtar fyrirspurnir en birtar síður?

Þegar kemur að vefþjónustu eru birtar fyrirspurnir yfirleitt hraðari en samsvarandi birtar síður. Ástæðan er sú að fyrirspurnir eru sérstilltar til að lesa gögn og innihalda ekki kveikjur á borð við OnAfterGetRecord.

Vefþjónustur eru byggðar á síðum eða fyrirspurnum sem búnar eru til fyrir aðgang á vefnum og yfirleitt ekki fínstilltar fyrir aðgang í gegnum ytri þjónustur. Jafnvel þótt Business Central-tengill styðji enn að fá gögn frá vefþjónustum hvetjum við þig til að nota API-síður í stað vefþjónustu þegar það er hægt.

<!-- 13 --> 
### <a name="is-there-a-way-for-an-end-user-to-create-a-web-service-with-a-column-thats-in-a-business-central-table-but-not-a-page-or-will-the-developer-have-to-create-a-custom-query"></a>Getur endanotandi búið til vefþjónustu með dálki sem er í töflu Business Central en ekki síðu? Eða þarf þróunaraðilinn að stofna sérsniðna fyrirspurn?

Sem stendur er ekki til nein leið til að bæta nýjum reit við vefþjónustuna. API-síður bjóða upp á fullan sveigjanleika á skipulagi síðunnar þannig að þróunaraðili getur búið til nýja API-síðu til að uppfylla þessa kröfu. 

<!-- 28 --> 
### <a name="can-i-connect-power-bi-to-a-read-only-database-server-of-business-central-online"></a>Get ég tengt Power BI við skrifvarinn gagnagrunnsþjón Business Central Online?

Boðið verður upp á þessa virkni bráðlega. Frá og með febrúar 2022 munu nýjar skýrslur sem þú býrð til og byggja á gögnum Business Central Online reyna að tengjast eftirmynd af skrifvörðum gagnagrunni. Þetta verður til þess að skýrslurnar uppfærast hraðar og munu hafa minni áhrif á afköst ef Business Central er notað á meðan skýrsla er að uppfærast. Við mælum samt með því að tímasetja skýrslurnar á að uppfærast utan venjulegs vinnutíma þegar það er hægt.

Ef þú ert með gamlar skýrslur sem byggja á gögnum Business Central tengjast þær ekki eftirmynd af skrifvörðum gagnagrunni.

### <a name="ive-tried-the-preview-of-the-new-connector-for-the-february-2022-update-when-i-connect-to-my-custom-business-central-api-page-i-get-the-error-cannot-insert-a-record-current-connection-intent-is-read-only-how-can-i-fix-it"></a><a name="databasemods"></a>Ég hef prófað prufuútgáfuna af nýja tenglinum fyrir uppfærsluna í febrúar 2022. Þegar ég tengist sérstilltri API-síðu Business Central fæ ég villuna „Get ekki sett inn færsluna. Núverandi fyrirætlan tengingar er ritvarin.“. Hvernig get ég lagað þetta?

Með nýja tenglinum munu nýjar skýrslur sem nota Business Central-gögn sjálfgefið tengjast ritvarinni eftirmynd af gagnagrunni Business Central. Þessi breyting hefur í för með sér bætt afköst. Í sjaldgæfum tilfellum getur hún hins vegar leitt til villu. Þessi villa kemur yfirleitt upp vegna þess að sérstillt API er að gera breytingar á færslum Business Central á meðan Power BI reynir að sækja gögnin. Það gerist helst sem hluti af AL-kveikjum: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord og OnAfterGetCurrRecord.

Til að leysa úr þessu vandamáli með því að þvinga Business Central-tengilinn til að leyfa þessa hegðun skal skoða [Að búa til Power BI skýrslur til að sýna gögn Business Central - Lagfæring vandamála](across-how-use-financials-data-source-powerbi.md#fixing-problems).

<!--
In general, we recommend avoiding any database modifications in API pages when they're opening or loading records, because they cause performance issues and might cause your report refresh to fail. In some cases, you might still need to make a database modification when your custom API page opens or loads records. You can force the Business Central connector to allow this behavior. Do the following steps when getting data from Business Central for the report in Power BI Desktop:

1. Start Power BI Desktop.
2. In the ribbon, select **Get Data** > **Online Services**.
3. In the **Online Services** pane, select **Dynamics 365 Business Central**, then **Connect**.
4. In the **Navigator** window, select the API endpoint that you want to load data from.
5. In the preview pane on the right, you'll see the following error:

   *Dynamics365BusinessCentral: Request failed: The remote server returned an error: (400) Bad Request. (Cannot insert a record. Current connection intent is Read-Only. CorrelationId: [...])".*

6.  Select **Transform Data** instead of **Load** as you might normally do.
7. In **Power Query Editor**, select **Advanced Editor** from the ribbon.
8.  Replace the following line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null),
   ```

   with the line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false]),
   ```

9.  Select **Done**.
10. Select **Close & Apply** from the ribbon to save the changes and close Power Query Editor.

-->
### <a name="how-do-i-change-or-clear-the-user-account-im-currently-using-to-connect-to-business-central-from-power-bi-desktop"></a><a name="perms"></a>Hvernig breyti ég eða hreinsa notandareikninginn sem ég nota núna til að tengjast Business Central frá Power BI Desktop?

Í Power BI Desktop skal fara í gegnum eftirfarandi skref:

1. Í valmyndinni skal velja **Valkostir og stillingar** > **Stillingar gagnagjafa**.
2. Veldu **Dynamics Business Central** úr listanum, veldu síðan **Hreinsa heimildir** > **Eyða**.

Næst þegar þú tengist Business Central til að ná í gögn verður beðið um innskráningu.

## [Afköst](#tab/performance)

<!-- 17 -->

### <a name="is-it-faster-to-get-data-using-api-pages-than-using-web-services"></a>Er fljótara að sækja gögn með API-síðum en með vefþjónustu?

Já. Prófanir okkar gefa til kynna að API-síður séu allt að 25% afkastameiri en vefþjónusta.

<!-- 18 -->
### <a name="are-there-plans-to-have-a-mirror-on-the-azure-sql-database-instance-which-i-can-connect-to-directly"></a>Eru áform um speglun á Azure SQL gagnagrunnstilviki sem ég get tengst beint við?

Fj. Ekki núna. Aðeins er hægt að eiga samskipti við Business Central í gegnum API.

<!-- 19 -->
### <a name="loading-data-from-business-central-web-services-seems-slow-is-there-any-way-to-get-data-directly-from-the-sql-database-table"></a>Hleðsla gagna í Business Central vefþjónustu virðist hæg. Er hægt að sækja gögn beint úr töflu SQL-gagnagrunnsins?

Fj. Beinn aðgangur að gagnagrunninum er ekki mögulegur en það hjálpar mikið að skipta yfir á API-síður (þegar nýja tengið er tiltækt).

## [Ítarlegt](#tab/advanced)
<!-- 1 -->

### <a name="are-there-plans-for-the-power-bi-connector-to-support-the-incremental-refresh-features-in-the-power-bi-service"></a>Eru áætlanir um að Power BI tengilinn geti stutt stigvaxandi uppfærslueiginleika í Power BI þjónustunni?

Já. Það er á dagskrá.

<!-- 2 -->
### <a name="if-a-business-central-on-premises-solution-doesnt-have-internet-access-can-i-still-use-power-bi"></a>Ef Business Central lausn á staðnum er ekki með netaðgang, get ég þá enn notað Power BI?
<!-- todo: please explain this one-->

Já. Í því tilviki er Power BI Desktop notað staðbundið og tengt við Business Central á staðnum. Þegar þú hefur tengst geturðu stofnað og skoðað skýrslur en þú getur ekki birt þær í Power BI þjónustunni. 
<!-- 20 -->
### <a name="are-there-any-plans-to-make-it-possible-to-replicate-business-central-online-databases-so-theyre-accessible-for-read-only-sql-queries-this-capability-would-support-incremental-refresh-and-be-a-lot-faster-than-apis-or-web-services"></a>Eru einhverjar áætlanir um að gera eftirlíkingar að gagnagrunnum Business Central Online svo að þeir séu aðgengilegir fyrir skrifvarðar SQL fyrirspurnir? Þessi möguleiki myndi styðja stigvaxandi uppfærslu og vera mun hraðari en API eða vefþjónusta.

<!-- todo: what does "BC-Saas-DB-replicated DB accessible" mean? fixe-->
Já. Við erum með þennan eiginleika á langtímaáætlun okkar. 

<!-- 21 -->
### <a name="if-i-use-azure-data-factory-to-get-data-from-business-central-and-consume-it-on-power-bi-will-that-help-in-increase-in-performance"></a>Eykur það afköst ef ég nota Azure Data Factory til að sækja gögn úr Business Central og nota þau á Power BI?

Já. Þessar ítarlegu aðstæður hjálpa við að viðhalda góðum árangri Business Central vegna þess að gagnaaðgangur yrði um Azure Data Factpru.

<!-- 22 -->
### <a name="are-there-any-plans-to-support-power-bi-deployment-pipelines-or-a-way-to-build-deployment-pipelines-for-pbi-reports-similar-to-extensions-or-maybe-even-a-simple-api-in-the-business-admin-center"></a>Eru einhver áform um að styðja Power BI innleiðingarsölukeðju eða sem leið til að byggja innleiðingarsölukeðju fyrir PBI skýrslur, svipað og viðbætur? Eða kannski einfalt API í Business stjórnendamiðstöð?

Við erum að skoða þennan eiginleika. Power BI býður upp á ítarleg API til að stjórna skýrsluútfærslum. Frekari upplýsingar eru í [Kynning á innleiðingasölukeðjum](/power-bi/create-reports/deployment-pipelines-overview).

### <a name="when-i-get-data-from-business-central-to-use-in-my-power-bi-reports-i-see-some-values-like-_x0020_-what-are-these-values"></a>Þegar ég fæ gögn frá Business Central til að nota í Power BI skýrslunum mínum sé ég nokkur gildi eins og „_x0020_“. Hvað eru þessi gildi?

Sumar API-síður, þar á meðal flestar API v2.0 síður, eru með reiti sem byggja á [AL-fasttextahlutum](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums). Reitir byggðir á AL fasttextahlutum verða að hafa nöfn sem eru samræmd og alltaf eins svo að síur á skýrslunni virka alltaf&mdash;óháð tungumálinu eða stýrikerfinu sem er notað. Þess vegna eru reitirnir sem byggjast á AL fasttexta ekki þýddir og eru kóðaðir til að koma í veg fyrir sérstafi, þ.m.t. bilið. Þegar tómur valkostur er í AL fasttextahlutnum er hann kóðaður í „_x0020_“. Alltaf er hægt að umbreyta gögnum á Power BI ef sýna á mismunandi gildi fyrir þessa reiti, til dæmis „Tómt“.

## <a name="see-also"></a>Sjá einnig .

[Power BI Leyfisveiting](admin-powerbi-setup.md#license)  
[Business Central og Power BI kynning](admin-powerbi.md)  
[Power BI Yfirlit yfir samþættingu](admin-powerbi-overview.md)  
[Virkja Power BI í Business Central](admin-powerbi-setup.md)  
[Vinna með Power BI skýrslur í Business Central](across-working-with-powerbi.md)  
[Vinna með Business Central Data í Power BI](across-working-with-business-central-in-powerbi.md)  
[Búa til Power BI skýrslur til að sýna gögn frá Business Central](across-how-use-financials-data-source-powerbi.md)  
[Power BI fylgiskjöl](/power-bi/)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
