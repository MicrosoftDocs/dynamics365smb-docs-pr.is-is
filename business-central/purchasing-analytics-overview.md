---
title: Greiningar í innkaupum
description: 'Business Central inniheldur margar aðgerðir til að hjálpa þér að safna saman, greina og deila verðmætum sölugögnum fyrir viðskiptaupplýsingar og ákvarðanatöku innan innkaupafyrirtækisins.'
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '9306, 9307, 518, 29'
ms.date: 04/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Greiningar í innkaupum

Fyrirtæki safna fjölda gagna við daglegar aðgerðir sem styðja viðskiptaupplýsingar (BI) fyrir innkaupastjóra:

- Innkaupabeiðnir
- Innkaupapantanir
- Innkaupareikningar

[!INCLUDE[prod_short](includes/prod_short.md)] veitir eiginleika sem hjálpa til við söfnun, greiningu og samnýtingu innkaupagagna fyrirtækisins:

- Ad-hoc greining á listum
- Tilfallandi greining á gögnum í Excel (með opnum í Excel)
- Innbyggðar söluskýrslur

Hver þessara eiginleika hefur kosti og galla, allt eftir tegund gagnagreiningar og hlutverki notandans. Til að [fræðast meira er yfirlit yfir Analytics, viðskiptagreind og skýrslugerðaryfirlit](reports-bi-reporting.md).

Þessi grein kynnir hvernig hægt er að nota þessar greiningaraðgerðir til að fá innsýn í innkaup.

## Greiningarþarfir í innkaupum

Þegar hugsað er um greiningarþarfir í innkaupum getur það hjálpað til við að nota líkan sem lýsir mismunandi greiningarþörfum á háu stigi.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Útskýring ólíkra einstaklinga við greiningar" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Starfsfólk í mismunandi hlutverkum hefur mismunandi þarfir þegar kemur að gögnum og notar gögnin á mismunandi hátt. Til dæmis getur starfsfólk í eignastjórnun og fjármagnað samskipti við gögn á annan hátt en fólk í sölu.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Útskýring á því hvernig mismunandi einstaklingar hafa mismunandi greiningarþarfir." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Hlutverk              | Uppsöfnun gagna  | Dæmigerðar leiðir til að nota gögn                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|COO / CSO / CFO / forstjóri    | Gögn um afköst  | Afkastavísar (KPI) <br> Mælaborð <br> Fjárhagsskýrslur           |
|Yfirmaður innkaupa      | Þróun, samantektir | Innbyggðar stjórnunarskýrslur <br> Tilfalengd greining      | 
|Innkaupastjóri / Innkaupaaðili | Sundurliðuð gögn     | Innbyggðar rekstrarskýrslur <br> Gögn um verk á skjá |

<!-- 
## Purchasing KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In purchasing management, people often use the following KPIs to monitor their organization's purchasing performance:

- TODO  
-->

## Nota fjárhagsskýrslugerð til að búa til ársreikninga og afkastatengsl (tengd innkaupum)

Eiginleikinn **Ársskýrslur** veitir innsýn í fjárhagsgögnin sem birtast í bókhaldslyklinum (COA). Hægt er að setja upp fjárhagsskýrslur til að greina tölur á fjárhagsreikningum og bera saman fjárhagsfærslur og áætlunarfærslur. Sérstaklega er hægt að setja upp fjárhagsskýrslur á fjárhagsreikningum sem notaðir eru til að rekja innkaupabókanir.

Víddir gegna mikilvægu hlutverki í viðskiptagreind. Vídd er gögn sem þú getur bætt við færslu sem færibreytu. Í víddum er hægt að flokka færslur sem hafa svipaða eiginleika, t.d. viðskiptamenn, svæði og vörur, og sækja þessa flokka auðveldlega til greiningar. Meðal annars má nota víddir þegar greiningaryfirlit eru skilgreind og fjárhagsskýrslur stofnaðar. Frekari upplýsingar eru í [Vinna með víddir](finance-dimensions.md).

Frekari upplýsingar um fjárhagsskýrslur er farið [í Undirbúning fjárhagsskýrslna með fjárhagsgögnum og reikningsflokkum](bi-how-work-account-schedule.md).

## Fjármálaskýrsla þvert á fyrirtækiseiningar eða lögaðila (tengd innkaupum)

Sum fyrirtæki nota [!INCLUDE [prod_short](includes/prod_short.md)] í mörgum fyrirtækiseiningum eða lögaðilum. Aðrir nota [!INCLUDE [prod_short](includes/prod_short.md)] í dótturfélögum sem gefa skýrslu til móðurfyrirtækja. [!INCLUDE [prod_short](includes/prod_short.md)] gefur endurskoðendum verkfæri sem hjálpa þeim að flytja fjárhagsfærslur frá tveimur eða fleiri fyrirtækjum (dótturfyrirtækjum) í samsteypufyrirtæki. Sérstaklega til innkaupastjórnunar gæti þurft að sameina fjárhagsfærslur fyrir innkaupareikninga til að rekja sölukrafa í fyrirtækiseiningum eða lögaðilum.

Nánari upplýsingar eru í [Sameiningu fyrirtækis](finance-consolidated-company-reporting.md).

## Tilfallandi greining á innkaupum gagna

Stundum þarf bara að athuga hvort tölurnar eru rétt settar upp eða staðfesta tölu á fljótlegan hátt. Eftirfarandi eiginleikar eru frábærir fyrir tilfalengdar greiningar:

- Gagnagreining á fjárhagslistasíðum
- Opna í Excel

Eiginleikinn **Gagnagreining** gerir kleift að opna næstum hvaða listasíðu sem er, svo sem **Innkaupapantanir**, **Bókaðir innkaupareikningar**, **Lánardr.færslur** eða **Fjárhagsfærslur**, færa inn greiningarstillingu og síðan flokka, afmarka og velta gögnum eftir hentugleika.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Dæmi um gagnagreiningu á síðunni Viðskm.færslur." lightbox="media/data-analysis-vendor-ledger-entries.png":::

Á svipaðan hátt er hægt að nota aðgerðina **Opna í Excel** til að opna listasíðu, afmarka listann við undirmengi gagna og nota Excel til að vinna með gögnin. Til dæmis með því að nota aðgerðir eins og Greiningargögn, Hvað-Ef greining eða Spárblað.

:::image type="content" source="media/open-in-excel-vendor-ledger-entries.png" alt-text="Dæmi um hvernig á að gera gagnagreiningu á gögnum viðskiptamannafærslna með Excel." lightbox="media/open-in-excel-vendor-ledger-entries.png":::

> [!TIP]
> Ef grunnstillt OneDrive er fyrir kerfisaðgerðir opnast Excel-vinnubókin í vafranum.

Nánari upplýsingar um hvernig gera á tilfallandi greiningu á innkaupagögnum er farið í [Tilfallandi greiningu á innkaupagögnum](ad-hoc-analysis-purchasing.md).

## Innbyggðar skýrslur um innkaup

[!INCLUDE [prod_short](includes/prod_short.md)] þar á meðal eru nokkrar innbyggðar skýrslur, rakningaraðgerðir og verkfæri til að hjálpa við innkaup fyrirtækja að gefa skýrslu um gögn sín.

Til að fá yfirlit yfir tiltækar skýrslur skal velja **Allar skýrslur** efst á heimasíðunni. Þessi aðgerð opnar Hlutverkavafrann sem er afmarkaður við aðgerðirnar í valkostinum **Skýrsla & Greining** . Nánari upplýsingar eru í [Finna skýrslur með hlutverkavafranum](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-purchasing.png" alt-text="Dæmi um skýrslur í hlutverkamiðstöð XXX." lightbox="media/report-explorer-purchasing.png":::

<!-- Built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Nánari upplýsingar um skýrslur sem varða innkaup er farið [í Innbyggðar innkaupaskýrslur](purchase-reports.md).

## Greiningar á skjánum

[!INCLUDE [prod_short](includes/prod_short.md)] á nokkrum síðum sem gefa innkaup yfirlit og verkhluta. Hér er dæmi um að þú hafir hafist handa:

- [Skoða tiltækileika vöru](inventory-how-availability-overview.md)  
- [Reikna út dagsetningar fyrir innkaup](purchasing-date-calculation-for-purchases.md)
- [Skoða fjárhagsfærslur innkaupa](purchasing-how-record-purchases.md#viewing-ledger-entries)


### Sýna innkaupatengdar fjárhagsfærslur og stöður af síðunni Bókhaldslykill

Síðan Bókhaldslykill sýnir alla fjárhagsreikninga með samanlögðu númeri sem bókuð eru í fjárhaginn. Á þessari síðu er hægt að gera hluti eins og:  

- Skoða skýrslur sem sýna aðalbókaratriði og jafnvægi.  
- Skoða lista yfir bókunarflokka fyrir þann reikning.
- Skoða debet- og kreditstöður fyrir einstakan fjárhagsreikning

Hægt er að búa til yfirlit sérstaklega fyrir innkaup á síðunni Bókhaldslykill sem sýnir aðeins reikningana sem notaðir eru til að bóka innkaupafærslur.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Dæmi um hvernig síðan Bókhaldslykill sýnir fjárhagsinnsýni" lightbox="media/chart-of-accounts-page.png":::

Nánari upplýsingar eru í [Skilja bókhaldslykilinn](finance-general-ledger.md#the-chart-of-accounts).

### Greina gögn eftir víddum (tengd innkaupum)

Víddir eru gildi sem flokka færslur svo hægt sé að rekja og greina þær í fylgiskjölum, t.d. innkaupapöntunum. Víddir geta til dæmis gefið í skyn verkið eða deildina sem færsla koma frá.  

Í stað þess að setja upp sérstaka fjárhagsreikninga fyrir hverja deild eða staðsetningu er hægt að nota víddir sem grunn að greiningu og komast hjá því að búa til flókið bókhaldslykilsuppbyggingu.

Nánari upplýsingar eru notaðar til að greina [gögn eftir víddum](bi-how-analyze-data-dimension.md).

## Sjá einnig .

[Sameining fyrirtækja](finance-consolidated-company-reporting.md)  
[Undirbúa fjárhagsskýrslur með fjárhagsgögnum og reikningsflokkum](bi-how-work-account-schedule.md)  
[Meðhöndla fjárhagsskýrslur yfir rekstrareiningar eða lögaðila](finance-consolidated-company-reporting.md)  
[Tilfallandi greining á innkaupum gagna](ad-hoc-analysis-purchasing.md)  
[Innbyggðar innkaupaskýrslur](purchase-reports.md)  
[Skilja bókhaldslykilinn](finance-general-ledger.md#the-chart-of-accounts)  
[Greina gögn eftir víddum](bi-how-analyze-data-dimension.md)  
[Yfirlit yfir greiningar, viðskiptagreind og skýrslur](reports-bi-reporting.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]