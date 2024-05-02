---
title: 'Yfirlit yfir greiningar, viðskiptagreind og skýrslur'
description: 'Veitir yfirlit yfir allar greiningar, viðskiptagreind og skýrslugerðaraðgerðir sem eru studdar í Business Central.'
author: KennieNP
ms.topic: get-started
ms.devlang: al
ms.search.keywords: feature overview
ms.reviewer: bholtorf
ms.date: 09/22/2022
ms.author: kepontop
ms.service: dynamics-365-business-central
---

# Yfirlit yfir greiningar, viðskiptagreind og skýrslur

Lítil og meðalstór fyrirtæki reiða sig á tilbúna innbyggða möguleika greiningar og skýrslugjafar sem þau geta notað til að halda utan um reksturinn. [!INCLUDE[prod_short](includes/prod_short.md)] býður upp á skýrslur og greiningarverkfæri sem ná til grunn- og flókinna viðskiptaferla fyrir slík fyrirtæki. Einnig er hægt að gera ad-hoc greiningar beint af heimasíðunni þinni.  

## Greiningarþarfir hjá fyrirtækjum

Þegar hugað er að greiningarþörfum hjá fyrirtækjum getur það hjálpað til við að nota andlegt líkan sem byggist á einstaklingum sem lýst er á hástigi og mismunandi greiningarþarfir þeirra.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Útskýring ólíkra einstaklinga við greiningar" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Líkanið byggist á því að mismunandi hlutverk innan fyrirtækis séu með mismunandi þarfir þegar kemur að gögnum. Því hærra sem hlutverk er sett í stjórnunarritið, þeim mun samanlagðari gögn sem einhver í hlutverkinu þarf til að vinna vinnuna sína.

Hlutverk hafa oft fremur leiðir til að neyta og greina gögn, leiðir sem endurspegla stig uppsöfnunar gagna sem þau þurfa.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Útskýring á því hvernig mismunandi einstaklingar hafa mismunandi greiningarþarfir." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

Eftirfarandi hlutar eru notaðir til að fræðast meira um leiðir til að nota gögn úr [!INCLUDE[prod_short](includes/prod_short.md)]:

- Fjárhagsskýrslur
- KPI og mælaborð
- Tilfalengd greining
- Skýrslur

## Notkun fjárhagsskýrslna til að búa til ársreikninga og afkastalsreikninga

Eiginleikinn Fjárhagsskýrslur veitir innsýn í fjárhagsgögnin sem geymd eru í bókhaldslyklinum (COA). Hægt er að setja upp fjárhagsskýrslur til að greina tölur á fjárhagsreikningum og bera saman fjárhagsfærslur og áætlunarfærslur.

:::image type="content" source="media/acc_schedule_13_columns.jpg" alt-text="Skjámynd af fjárhagsskýrslu." lightbox="media/acc_schedule_13_columns.jpg":::

Víddir gegna mikilvægu hlutverki í viðskiptagreind. Vídd er gögn sem þú getur bætt við færslu sem færibreytu. Í víddum er hægt að flokka færslur sem hafa svipaða eiginleika, t.d. viðskiptamenn, svæði, vörur og sölumenn, og sækja þessa flokka auðveldlega til greiningar. Meðal annars er hægt að nota víddir þegar greiningaryfirlit eru skilgreind og fjárhagsskýrslur stofnaðar. Frekari upplýsingar eru í [Vinna með víddir](finance-dimensions.md).

Til að fræðast meira um ársreikninga og afkastalsreikninga er farið í [Notkun fjárhagsskýrslna til að búa til ársreikninga og afkastalsreikninga](bi.md).

## Nota lykilstærðir til að uppfylla viðskiptamarkmið

Lykilafkastavísir (afkastavísir) er mælanleg gildi sem sýnir hversu skilvirkt notandi uppfyllir markmiðin. Hugsaðu um afkastastærðir sem árangursmat fyrirtækisins, leið til að mæla hvort þú ert að afhenda markmiðin.

Með því að auðkenna og rekja afkastakstur gerir það kleift að vita hvort fyrirtækið sé á réttri slóð eða hvort þú ættir að breyta námskeiðinu. Þegar það er notað á réttan hátt eru afkastað verkfæri sem hjálpa þér að:

- Fylgjast með fjármálaheilsu fyrirtækisins.
- Mælikvarða framvindu gagnvart markmiðum.
- Blettavandamál snemma á.
- Gera tímanlegar leiðréttingar á aðferðum.
- Hvetja liđsfélaga.
- Taktu betri ákvarðanir, hraðar.

Til að [fræðast meira um afkastavísa er farið í Notkun lykilstærða til að uppfylla viðskiptamarkmið fyrirtækisins](./analytics-about-kpis.md)

## Tilfallandi gagnagreining

Stundum er bara þörf á að athuga hvort tölurnar séu rétt staðfestar eða debunk tilgátu um viðskiptin eða leita kannski að frávikum í fjárhagsgögnum. Tilfallandi greiningar er hugsanlega ekki til innbyggð skýrsla sem hjálpar til við að svara spurningum. Þessir tveir eiginleikar eru notaðir til að tilfalkka greiningar:

- Gagnagreining á fjárhagslistasíðum
- Opna í Excel

Eiginleikinn Gagnagreining gerir kleift að opna næstum hvaða listasíðu sem er, svo sem síðurnar Fjárhagur eða Viðskiptamannafærslur, færa inn greiningarstillingu og síðan flokka, afmarka og velta gögnum eftir hentugleikum. 

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Dæmi um gagnagreiningu á fjárhagsfærslusíðunni." lightbox="media/data-analysis-gl-entries.png":::

Á svipaðan hátt er hægt að nota aðgerðina **Opna í Excel** til að opna listasíðu, afmarka listann við undirmengi gagna og nota Excel svo til að vinna með gögnin. Til dæmis með því að nota aðgerðir eins og Greiningargögn, Hvað-Ef greining eða Spárblað.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Dæmi um hvernig eigi að gera greiningu á gögnum um fjárhagsfærslur með Excel." lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Ef grunnstillt OneDrive er fyrir kerfisaðgerðir opnast Excel-vinnubókin í vafranum með því að nota Excel fyrir vefinn.

Til að [fræðast meira um auglýsingar er farið í Ad-hoc gagnagreiningu](reports-adhoc-analysis.md).

## Skýrslur

Skýrsla í [!INCLUDE[prod_short](includes/prod_short.md)] ssafnar saman upplýsingum byggðum á sérstöku safni af skilyrðum. Skýrslur skipuleggja og birta upplýsingar á auðlesnu sniði sem hægt er að nota í Excel, prenta eða vista sem skrá.  

Sem dæmi um gagnvirka skýrslu í Excel gerir ***Aldursgreindir safnreikningar** kleift að greina það sem viðskiptamenn skulda og hvenær greiðslur eru gjaldfallnar.

:::image type="content" source="media/aged-accounts-receivables-excel.png" alt-text="Dæmi um gagnvirka safnreikninga aldursgreindra reikninga í Excel." lightbox="media/aged-accounts-receivables-excel.png":::

Fyrir aldursgreindar safnreikninga [!INCLUDE[prod_short](includes/prod_short.md)]  er einnig skýrsla sem er hönnuð til prentunar. Getan til að prenta er hentug ef óskað er eftir að gögn séu í .pdf skrá.

:::image type="content" source="media/aged-accounts-receivables-pdf.png" alt-text="Dæmi um aldursgreinda safnreikninga í pdf." lightbox="media/aged-accounts-receivables-pdf.png":::

[!INCLUDE[prod_short](includes/prod_short.md)] Fleiri en 300 innbyggðar skýrslur sem hægt er að nota til að styðja viðskiptaferlið með innsýn í gögn. Til að fá snöggt yfirlit yfir allar skýrslur sem eru tiltækar fyrir hlutverk notanda er hægt að opna skýrsluvafra frá mitt hlutverk, allar listasíður og frá **Tell Me**.

:::image type="content" source="media/report-explorer-finance.png" alt-text="Dæmi um hvernig skýrslukönnuðurinn sýnir allar skýrslur um hlutverk." lightbox="media/report-explorer-finance.png":::

Nánari upplýsingar um notkun skýrslukönnuðar eru í skýrslukönnuninni til að skoða allar innbyggðar skýrslur með því að [fara í Skoða skýrslur eftir hlutverkum](ui-role-explorer.md).

Í eftirfarandi töflu eru greinar um notkun innbyggðra skýrslna. [!INCLUDE[prod_short](includes/prod_short.md)]

| Til  | Sjá |
| --- | --- |
| Fræðast um notkun skýrslna (bókamerki, keyra, prenta, tímasetja og breyta útlitinu). | [Nota skýrslur í daglegu starfi](reports-use-reports.md) |
| Fræðast um í hvaða innbyggðu skýrslum er að ræða [!INCLUDE[prod_short](includes/prod_short.md)]. |[Skýrsluyfirlit](reports-available-reports.md)| 
| Skýrsluvafrinn er notaður til að skoða allar innbyggðar skýrslur. | [Skýrslur skoðaðar eftir hlutverkum](ui-role-explorer.md) |

## Ytri viðskiptauppljóstrun og skýrslugerðarverkfæri

Ef notandi kýs frekar að nota viðskiptagreindarverkfæri sem ekki er innifalið í fæst tenglar í [!INCLUDE[prod_short](includes/prod_short.md)] leiðbeiningar um verkfæri og leiðir til að nota utanaðkomandi verkfæri.

| Til  | Sjá |
| --- | --- |
| Notkun Power BI með Business Central gögnum | [Nota Power BI með Business Central](admin-powerbi.md) |
| Samþætta ytri verkfæri viðskiptagreindar með [!INCLUDE[prod_short](includes/prod_short.md)].| [Ytri verkfæri viðskiptagreindar](reports-external-analysis.md) |
| Draga gögn út í gagnavöruhús eða gagnavötn| [Hvernig á að draga gögn til vöruhúsa gagna eða gagna vötn](/dynamics365/business-central/dev-itpro/performance/performance-developer#efficient-extracts-to-data-lakes-or-data-warehouses) |
| Greina Gögn Business Central með Microsoft Fabric| [Kynning á Microsoft Fabric og Business Central](admin-fabric.md) |
| Lesa gögn frá Business Central með API | [Business Central API v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/) |

## Sjá einnig .

[Notkun fjárhagsskýrslna til að búa til ársreikninga og afkastalsreikninga](bi.md)  
[Nota lykilstærðir (afkastavísa) til að uppfylla viðskiptamarkmið](analytics-about-kpis.md)  
[Gerð greiningar á tilfalöngum gögnum](reports-adhoc-analysis.md)  
[Nota skýrslur í daglegu starfi](reports-use-reports.md)  
[Yfirlit yfir innbyggðar skýrslur](reports-available-reports.md)  
[Skýrslur skoðaðar eftir hlutverkum](ui-role-explorer.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
