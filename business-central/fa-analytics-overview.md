---
title: Greiningar á eignum
description: 'Fræðast um hvernig á að safna saman, greina og deila gögnum um eignir fyrir viðskiptaupplýsingar.'
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5601, 5600, 5615, 5616, 5617'
ms.date: 05/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="fixed-assets-analytics"></a>Greiningar á eignum

Fyrirtæki með eignir safna mikið af gögnum um þær við daglegar aðgerðir. Gögnin styðja verðmætar viðskiptaupplýsingar (BI) fyrir eignastjóra:

- Eignakaup
- Eignafrádráttur
- Vátrygging og viðhald
- Eignaáætlanir

[!INCLUDE[prod_short](includes/prod_short.md)] veitir eiginleika sem hjálpa til við söfnun, greiningu og samnýtingu gagna um eignir fyrirtækisins:

- Ársskýrslugerð (fyrir ársreikninga og afkastsreikninga eignareikninga)
- Ad-hoc greining á listum
- Tilfallandi greining á gögnum í Excel (með opnum í Excel)
- Innbyggð greiningarverkfæri fyrir eignir
- Innbyggðar eignaskýrslur

> [!NOTE]
> Greining eigna er lítið annað en önnur svæði. Greina þarf gögn sem þegar eru til staðar, svo sem eignakaup, afskriftir og tryggingar, en einnig gögn um framtíðargögn (áætluð) gögn eins og afskriftir og eftirlaun eigna. Fyrir seinni gerð greiningar er [!INCLUDE[prod_short](includes/prod_short.md)]  með innbyggðar skýrslur sem geta reiknað þessi tölur.

Hver eiginleiki hefur sína kosti og galla, allt eftir tegund greiningar á gögnum og hlutverki notandans. Til að [fræðast meira er yfirlit yfir Analytics, viðskiptagreind og skýrslugerðaryfirlit](reports-bi-reporting.md).

Þessi grein lýsir því hvernig nota má þessar greiningaraðgerðir til að fá innsýn í eignirnar.

## <a name="analytics-needs-in-asset-management"></a>Greiningarþarfir í eignastýringu

Þegar hugsað er um greiningarþarfir í eignastjórnun gæti það hjálpað til við að nota starfsmannahald sem lýsir greiningarþörfum þeirra á háu stigi.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Útskýring ólíkra einstaklinga við greiningar" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Þegar kemur að gögnum hefur fólk í mismunandi hlutverkum mismunandi þarfir og notar gögnin á mismunandi hátt. Til dæmis getur starfsfólk í eignastjórnun og fjármagnað samskipti við gögn á annan hátt en fólk í sölu.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Útskýring á því hvernig mismunandi einstaklingar hafa mismunandi greiningarþarfir." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Hlutverk              | Uppsöfnun gagna  | Dæmigerðar leiðir til að nota gögn                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CFO / COO / forstjóri                 | Gögn um afköst  | Afkastavísar (KPI) <br> Mælaborð <br> Fjárhagsskýrslur           |
|Eignastýring / stjóri   | Þróun, samantektir | Innbyggðar stjórnunarskýrslur <br> Tilfalengd greining      | 
|Bókari                      | Sundurliðuð gögn     | Innbyggðar rekstrarskýrslur <br> Gögn um verk á skjá |

## <a name="asset-management-kpis"></a>Afkastal eignastýringar

Lykilafkastavísir (afkastavísir) er mælanleg gildi sem sýnir hversu skilvirkt notandi uppfyllir markmiðin. Í eignastýringu notar fólk oft eftirfarandi afkastastyrk til að fylgjast með notkun fyrirtækisins á eignum:

- Velta heildareignar
- Skil á eignum

## <a name="use-financial-reporting-to-produce-financial-statements-and-kpis-related-to-fixed-assets"></a>Nota fjárhagsskýrslugerð til að búa til ársreikninga og afkastatengdar eignir

Eiginleikinn **Ársskýrslur** veitir innsýn í fjárhagsgögnin sem birtast í bókhaldslyklinum (COA). Hægt er að setja upp fjárhagsskýrslur til að greina tölur á fjárhagsreikningum og bera saman fjárhagsfærslur og áætlunarfærslur. Sérstaklega er hægt að setja upp fjárhagsskýrslur á fjárhagsreikningum sem notaðir eru til að rekja eignabókanir.

Víddir gegna mikilvægu hlutverki í viðskiptagreind. Vídd er gögn sem þú getur bætt við færslu sem færibreytu. Í víddum er hægt að flokka saman færslur sem hafa svipaða eiginleika, t.d. viðskiptamenn, vörur og sölumenn, og sækja þessa flokka auðveldlega til greiningar. Meðal annars er hægt að nota víddir þegar greiningaryfirlit eru skilgreind og fjárhagsskýrslur stofnaðar. Frekari upplýsingar eru í [Vinna með víddir](finance-dimensions.md).

Nánari upplýsingar um fjármálaskýrslur eru undirbúnar [með fjárhagsgögnum og reikningsflokkum](bi-how-work-account-schedule.md).

## <a name="finance-reporting-across-business-units-or-legal-entities-related-to-fixed-assets"></a>Fjármálaskýrsla þvert á fyrirtækiseiningar eða lögaðila (tengd eignum)

Sum fyrirtæki nota [!INCLUDE [prod_short](includes/prod_short.md)] í mörgum fyrirtækiseiningum eða lögaðilum. Aðrir nota [!INCLUDE [prod_short](includes/prod_short.md)] skýrslur um dótturfyrirtæki til móðurfyrirtækja. [!INCLUDE [prod_short](includes/prod_short.md)] gefur endurskoðendum verkfæri sem hjálpa þeim að flytja fjárhagsfærslur frá tveimur eða fleiri fyrirtækjum (dótturfyrirtækjum) í samsteypufyrirtæki. Sérstaklega er hægt að styrkja fjárhagsfærslur fyrir eignareikninga til að geta rakið afkastavísa eigna í fyrirtækiseiningum eða lögaðilum.

Nánari upplýsingar eru í [Sameiningu fyrirtækis](finance-consolidated-company-reporting.md).

## <a name="ad-hoc-analysis-of-fixed-assets-data"></a>Tilfalengin greining á gögnum um eignir

Stundum þarf bara að athuga hvort tölurnar eru rétt settar upp eða staðfesta tölu á fljótlegan hátt. Eftirfarandi eiginleikar eru frábærir fyrir tilfalengdar greiningar:

- Gagnagreining á fjárhagslistasíðum
- Opna í Excel

Með gagnagreiningaraðgerðinni er hægt að opna næstum hvaða listasíðu sem **er, t.d. Fjárhagsfærslur** eða **Eignafærslur**, færa inn greiningarham og síðan flokka, afmarka og veltigögn eftir hentugleikum.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Dæmi um hvernig á að gera gagnagreiningu á síðunni Eignafærslur til að sjá eignavirði." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

Á svipaðan hátt er hægt að nota aðgerðina **Opna í Excel** til að opna listasíðu fyrir færslur, afmarka listann við hlutmengi gagna og nota Excel svo til að vinna með gögnin. Til dæmis með því að nota aðgerðir eins og Greiningargögn, Hvað-Ef greining eða Spárblað.

<!-- :::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Example of how to do data analysis on the G/L entries data using Excel." lightbox="media/open-in-excel-gl-entries.png"::: -->

> [!TIP]
> Ef grunnstillt OneDrive er fyrir kerfisaðgerðir opnast Excel-vinnubókin í vafranum með því að nota Excel fyrir vefinn. 

Nánari upplýsingar um hvernig á að gera tilfallanda greiningu á eignahöfuðbókum [eru í Til-hoc greining á eignagögnum](ad-hoc-analysis-fa.md).


## <a name="built-in-reports-for-fixed-assets"></a>Innbyggðar skýrslur fyrir eignir

[!INCLUDE [prod_short](includes/prod_short.md)] í henni eru nokkrar innbyggðar skýrslur, rakningaraðgerðir og verkfæri til að hjálpa endurskoðendum eða ráðamönnum sem gefa skýrslu um eignir.

Til að fá yfirlit yfir tiltækar skýrslur skal velja **Allar skýrslur** efst á heimasíðunni. Þessi aðgerð opnar síðuna Hlutverk Explorer sem er afmarkað eftir aðgerðunum í valkostinum **Skýrsla & Greining** . Til að finna skýrslur sem tengjast eignum er færðar inn **eignir**  í reitnum **Finna**. Nánari upplýsingar eru í [Finna skýrslur með hlutverkavafranum](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-fixed-assets.png" alt-text="Dæmi um skýrslur í fjármálahlutverkamiðstöðinni." lightbox="media/report-explorer-fixed-assets.png":::

<!-- Built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Nánari upplýsingar um skýrslur sem varða eignir [eru í Innbyggt eignaskýrslur](fa-reports.md).

## <a name="on-screen-fixed-assets-analytics"></a>Greiningar á eignum

[!INCLUDE [prod_short](includes/prod_short.md)] á nokkrum síðum þar sem eignir eru yfirlit yfir eignir og verkhlutar. Hér eru nokkur dæmi til að koma þér í gang:

- [Reikna afskriftir, bóka afskriftir og greina afskriftir](fa-how-depreciate-amortize.md)
- [Fylgjast með viðhaldskostnaði](fa-how-maintain.md#monitor-maintenance-costs)
- [Eftirlit með vátryggingasviði](fa-how-insure.md#to-monitor-insurance-coverage)
- [Skoða breytt afskriftabókargildi](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification)
- [Skoða afskráningarbókarfærslur](fa-how-dispose-retire.md#to-view-disposal-ledger-entries)
- [Skoða áætlað virði afskráninga](fa-how-manage-budgets.md#to-view-projected-disposal-values)

### <a name="show-fixed-asset-general-ledger-entries-and-balances-from-the-chart-of-accounts-page"></a>Sýna fjárhagsfærslur og stöður eigna af síðunni Bókhaldslykill

Síðan Bókhaldslykill sýnir alla fjárhagsreikninga með samanlögðum tölum í fjárhag. Á þessari síðu er hægt að gera hluti eins og:  

- Skoða skýrslur sem sýna aðalbókaratriði og jafnvægi.  
- Skoða lista yfir bókunarflokka fyrir þann reikning.
- Skoða debet- og kreditstöður fyrir einstakan fjárhagsreikning

Sérstaklega fyrir eignir er hægt að búa til yfirlit á síðunni Bókhaldslykill sem sýnir aðeins eignareikninga eða kannski aðeins þá eignareikninga sem notaðir eru til að bóka eignafærslur.

:::image type="content" source="media/chart-of-accounts-page-fa.png" alt-text="Dæmi um hvernig síðan Bókhaldslykill sýnir fjárhagsinnsýni" lightbox="media/chart-of-accounts-page-fa.png":::

Nánari upplýsingar eru í [Skilja bókhaldslykilinn](finance-general-ledger.md#the-chart-of-accounts).

### <a name="analyze-data-by-dimensions-related-to-fixed-assets"></a>Greina gögn eftir víddum (tengdum eignum)

Víddir eru gildi sem flokka færslur svo hægt sé að rekja og greina þær í fylgiskjölum, svo sem eignabókum. Víddir geta til dæmis gefið til kynna deildina eða stöðina sem færsla kom frá.  

Í stað þess að setja upp sérstaka fjárhagsreikninga fyrir hverja deild eða staðsetningu er hægt að nota víddir sem grunn að greiningu og komast hjá því að búa til flókið bókhaldslykilsuppbyggingu.

Nánari upplýsingar eru notaðar til að greina [gögn eftir víddum](bi-how-analyze-data-dimension.md)

## <a name="see-also"></a>Sjá einnig .

[Meðhöndla fjárhagsskýrslur yfir rekstrareiningar eða lögaðila](finance-consolidated-company-reporting.md)  
[Undirbúa fjárhagsskýrslur með fjárhagsgögnum og reikningsflokkum](bi-how-work-account-schedule.md)  
[Skilja bókhaldslykilinn](finance-general-ledger.md#the-chart-of-accounts)  
[Tilfalengin greining á gögnum um eignir](ad-hoc-analysis-fa.md)   
[Innbyggðar eignaskýrslur](fa-reports.md)  
[Yfirlit yfir greiningar, viðskiptagreind og skýrslur](reports-bi-reporting.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
