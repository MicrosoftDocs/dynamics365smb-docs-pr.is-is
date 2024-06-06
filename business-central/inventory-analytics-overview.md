---
title: Birgðagreining
description: 'Business Central inniheldur margar aðgerðir til að hjálpa þér að safna saman, greina og deila verðmætum gögnum um birgðir þínar vegna viðskiptaupplýsinga og ákvarðanatöku innan fyrirtækisins.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="inventory-analytics"></a>Birgðagreining

Fyrirtæki safna fjölda gagna við daglegar aðgerðir sem styðja viðskiptaupplýsingar (BI) fyrir birgðastjóra:

- Afhending vara þegar sölupöntunum er uppfyllt.
- Móttöku vara þegar innkaupapöntunum er uppfyllt.
- Hreyfingar á vörum milli birgðageymslna.

[!INCLUDE[prod_short](includes/prod_short.md)] veitir eiginleika sem hjálpa til við söfnun, greiningu og samnýtingu birgðagagna fyrirtækisins:

- Ad-hoc greining á listum
- Tilfallandi greining á gögnum í Excel (með Opið í Excel)
- Innbyggð birgðagreiningarverkfæri
- Innbyggðar birgðaskýrslur

Hver þessara eiginleika hefur sína kosti og galla, allt eftir tegund greiningar á gögnum og hlutverki notandans. Til að [fræðast meira er yfirlit yfir Analytics, viðskiptagreind og skýrslugerðaryfirlit](reports-bi-reporting.md).

Þessi grein kynnir hvernig hægt er að nota þessar greiningaraðgerðir til að fá innsýn í birgðir.

## <a name="analytics-needs-in-inventory"></a>Greiningarþarfir í birgðum

Þegar hugsað er um greiningarþarfir í birgðastjórnun getur það hjálpað til við að nota starfsmannalíkan sem lýsir mismunandi greiningarþörfum á háu stigi.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Útskýring ólíkra einstaklinga við greiningar" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Starfsfólk í mismunandi hlutverkum hefur mismunandi þarfir þegar kemur að gögnum og notar gögnin á mismunandi hátt. Til dæmis getur starfsfólk í eignastjórnun og fjármagnað samskipti við gögn á annan hátt en fólk í sölu.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Útskýring á því hvernig mismunandi einstaklingar hafa mismunandi greiningarþarfir." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Hlutverk              | Uppsöfnun gagna  | Dæmigerðar leiðir til að nota gögn                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|COO / CFO / forstjóri    | Gögn um afköst  | Afkastaveita, mælaborð, fjárhagsskýrslur           |
|Birgðastjóri  | Þróun, samantektir | Innbyggðar stjórnunarskýrslur, tilfallandi greining      | 
|Starfsmaður í vöruhúsi   | Sundurliðuð gögn     | Innbyggðar rekstrarskýrslur, gögn um verk á skjá |

<!-- 
## <a name="inventory-kpis"></a>Inventory KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In inventory management, people often use the following KPIs to monitor their organization's sales performance:

- TODO  
-->

## <a name="use-financial-reporting-to-produce-financial-statements-and-kpis-related-to-inventory"></a>Nota fjárhagsskýrslugerð til að framleiða ársreikninga og afkastatengdar birgðir

Eiginleikinn **Ársskýrslur** veitir innsýn í fjárhagsgögnin sem birtast í bókhaldslyklinum (COA). Hægt er að setja upp fjárhagsskýrslur til að greina tölur á fjárhagsreikningum og bera saman fjárhagsfærslur og áætlunarfærslur. Sérstaklega fyrir birgðastjórnun er hægt að setja upp fjárhagsskýrslur á fjárhagsreikningum sem notaðir eru til að rekja birgðabókanir.

Víddir gegna mikilvægu hlutverki í viðskiptagreind. Vídd eru gögn sem bætt er við færslu sem færibreytu. Í víddum er hægt að flokka færslur með svipaða eiginleika, t.d. viðskiptamenn, svæði, vörur og sölumann. Meðal annars má nota víddir þegar greiningaryfirlit eru skilgreind og fjárhagsskýrslur stofnaðar. Frekari upplýsingar eru í [Vinna með víddir](finance-dimensions.md).

Frekari upplýsingar um fjárhagsskýrslur er farið [í Undirbúning fjárhagsskýrslna með fjárhagsgögnum og reikningsflokkum](bi-how-work-account-schedule.md).

## <a name="finance-reporting-across-business-units-or-legal-entities-related-to-inventory"></a>Fjárhagsskýrslur þvert á fyrirtækiseiningar eða lögaðila (tengdar birgðum)

Sum fyrirtæki nota [!INCLUDE [prod_short](includes/prod_short.md)] í mörgum fyrirtækiseiningum eða lögaðilum. Aðrir nota [!INCLUDE [prod_short](includes/prod_short.md)] í dótturfélögum sem gefa skýrslu til móðurfyrirtækja. [!INCLUDE [prod_short](includes/prod_short.md)] gefur endurskoðendum verkfæri sem hjálpa þeim að flytja fjárhagsfærslur frá tveimur eða fleiri fyrirtækjum (dótturfyrirtækjum) í samsteypufyrirtæki. Sérstaklega er hægt að sameina fjárhagsfærslur fyrir birgðareikninga til að geta rakið söluafkastagetu í fyrirtækiseiningum eða lögaðilum.

Nánari upplýsingar eru í [Sameiningu fyrirtækis](finance-consolidated-company-reporting.md).

## <a name="ad-hoc-analysis-of-inventory-data"></a>Tilfalengd greining á birgðagögnum

Stundum þarf bara að athuga hvort tölurnar eru rétt settar upp eða staðfesta tölu á fljótlegan hátt. Eftirfarandi eiginleikar eru frábærir fyrir tilfalengdar greiningar:

- Gagnagreining á fjárhagslistasíðum
- Opna í Excel

Eiginleikinn Gagnagreining gerir kleift að opna næstum hvaða listasíðu sem er, t.d. Birgðafærslur **, færa inn greiningarstillingu og síðan flokka, afmarka og veltigögn eftir því sem** við á.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Dæmi um hvernig á að gera gamla greiningu á birgðagögnum á síðunni Birgðafærslur." lightbox="media/data-analysis-inventory-dead-stock.png":::

Á svipaðan hátt er hægt að nota aðgerðina **Opna í Excel** til að opna listasíðu, afmarka listann við undirmengi gagna og nota Excel svo til að vinna með gögnin. Til dæmis með því að nota aðgerðir eins og Greiningargögn, Hvað-Ef greining eða Spárblað.

<!-- :::image type="content" source="media/open-in-excel-item-ledger-entries.png" alt-text="Example of how to do data analysis on the Item Ledger Entries data using Excel." lightbox="media/open-in-excel-item-ledger-entries.png"::: -->

> [!TIP]
> Ef grunnstillt OneDrive er fyrir kerfisaðgerðir opnast Excel-vinnubókin í vafranum.

Nánari upplýsingar um hvernig á að gera tilfallanda greiningu á birgðagögnum er farið í Tilfallandsgreiningu [á birgðagögnum](ad-hoc-analysis-inventory.md).

## <a name="built-in-reports-for-inventory"></a>Innbyggðar skýrslur fyrir birgðir

[!INCLUDE [prod_short](includes/prod_short.md)] inniheldur nokkrar innbyggðar skýrslur, rakningaraðgerðir og verkfæri til að hjálpa birgðafyrirtækjum að gefa skýrslu um gögn sín.

Til að fá yfirlit yfir tiltækar skýrslur skal velja **Allar skýrslur** á heimasíðunni. Þessi aðgerð opnar skýrsluvafrann sem er afmarkaður við aðgerðirnar í valkostinum **Skýrsla & Greining** . Undir hausnum **Sala og Markaðssetning** skal velja **Skoða**. Nánari upplýsingar eru í [Finna skýrslur með hlutverkavafranum](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-sales.png" alt-text="Dæmi um skýrslur í söluhlutverkamiðstöðinni." lightbox="media/report-explorer-sales.png":::

<!-- The built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Nánari upplýsingar um skýrslur sem eiga við birgðir er farið [í Innbyggðar birgðir og vöruhúsaskýrslur](inventory-WMS-reports.md).

## <a name="on-screen-inventory-analytics"></a>Greiningar á birgðum á skjánum

[!INCLUDE [prod_short](includes/prod_short.md)] hefur nokkrar síður sem gefa birgðayfirlitum og verkhlutum kleift að vinna. Hér eru nokkur dæmi til að koma þér í gang:

- [Skoða tiltækileika vöru](inventory-how-availability-overview.md)
- [Rekja vörur með rað-, lotu- og pakkanúmerum](inventory-how-work-item-tracking.md)
- [Rekja vöruraktar vörur](inventory-how-to-trace-item-tracked-items.md)
- [Endurskoða afstemmingu á milli birgðabókar og fjárhags](finance-how-to-post-inventory-costs-to-the-general-ledger.md#to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger)
- [Skoða hjáskipunarvörur í sendingu eða tínsluvinnublaði](warehouse-how-to-cross-dock-items.md#to-view-cross-docked-items-in-a-shipment-or-pick-worksheet)

Í sölukerfinu eru einnig greiningarsíður sem tengjast birgðum:

- [Reikna dagsetningar pöntunarloforða](sales-how-to-calculate-order-promising-dates.md)
- [Reikna út afhendingardagsetningar fyrir sölupantanir](sales-date-calculation-for-sales.md)
- [Finna sendingar](sales-how-track-packages.md)

### <a name="show-inventory-related-general-ledger-entries-and-balances-from-the-chart-of-accounts-page"></a>Sýna birgðatengdar fjárhagsfærslur og stöður á síðunni Bókhaldslykill

Síðan **Bókhaldslykill** sýnir alla fjárhagsreikninga með samanlögðu númeri sem bókuð eru í fjárhaginn. Á þessari síðu er hægt að gera hluti eins og:  

- Skoða skýrslur sem sýna aðalbókaratriði og jafnvægi.  
- Skoða lista yfir bókunarflokka fyrir þann reikning.
- Skoða debet- og kreditstöður fyrir einstakan fjárhagsreikning

Sérstaklega fyrir birgðastjórnun er hægt að búa til yfirlit á síðunni Bókhaldslykill sem sýnir aðeins reikningana sem notaðir eru til að bóka birgðafærslur.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Dæmi um hvernig síðan Bókhaldslykill sýnir fjárhagsinnsýni" lightbox="media/chart-of-accounts-page.png":::

Nánari upplýsingar eru í [Skilja bókhaldslykilinn](finance-general-ledger.md#the-chart-of-accounts).

### <a name="analyze-inventory-data-by-dimensions"></a>Greina birgðagögn eftir víddum

Víddir eru gildi sem flokka færslur svo þú getir fylgst með og greint þær í skjölum, t.d. sölupöntunum. Víddir geta til dæmis gefið í skyn verkið eða deildina sem færsla koma frá.  

Í stað þess að setja upp sérstaka fjárhagsreikninga fyrir hverja deild eða staðsetningu er hægt að nota víddir sem grunn að greiningu og komast hjá því að búa til flókið bókhaldslykilsuppbyggingu.

Nánari upplýsingar eru notaðar til að greina [gögn eftir víddum](bi-how-analyze-data-dimension.md).

## <a name="see-also"></a>Sjá einnig .

[Samsteypufyrirtæki](finance-consolidated-company-reporting.md)   
[Undirbúa fjárhagsskýrslur með fjárhagsgögnum og reikningsflokkum](bi-how-work-account-schedule.md)  
[Meðhöndla fjárhagsskýrslur yfir rekstrareiningar eða lögaðila](finance-consolidated-company-reporting.md)  
[Sérstök greining á bigðagögnum](ad-hoc-analysis-inventory.md)  
[Innbyggðar skýrslur birgða og vöruhúss](inventory-WMS-reports.md)  
[Skilja bókhaldslykilinn](finance-general-ledger.md#the-chart-of-accounts)  
[Greina gögn eftir víddum](bi-how-analyze-data-dimension.md)  
[Yfirlit yfir greiningar, viðskiptagreind og skýrslur](reports-bi-reporting.md)   
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
