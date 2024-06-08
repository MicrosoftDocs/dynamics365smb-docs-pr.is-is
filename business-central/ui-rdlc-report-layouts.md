---
title: Vinna með RDLC-útlit
description: Fáðu kynningu á RDLC-skýrsluútlitum.
author: jswymer
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 12/04/2023
ms.author: jswymer
ms.reviewer: jswymer
---
# Vinna með RDLC-útlit

RDLC útlit er byggt á skýrsluskilgreiningarskrám (.rdll eða .rdlc skráartegundum). Hönnunarhugmyndirnar fyrir RDLC-útlit eru svipaðar og fyrir aðrar útlitsgerðir. Útlitið ræður hvaða reiti á að sýna og hvernig þeim er raðað. Hönnun RDLC-útlits er hins vegar ítarlegra en Word- og Excel-útlits.

[![Sýnir mismunandi einingar RDLC-útlits.](media/rdlc-layout.png)](media/rdlc-layout.png#lightbox)

## Nauðsynleg verkfæri

Til að breyta útliti RDL er hægt að nota annaðhvort Microsoft SQL Server skýrslusmið eða Microsoft Visual Studio með viðbótinni við RDLC Report Designer.

- Report Builder er sjálfstætt forrit sem þú eða stjórnandi þinn hefur sett upp í tölvunni þinni. Með Business Central á staðnum er Report Builder sjálfkrafa settur upp með uppsetningu Business Central Server. Frekari upplýsingar um uppsetningu Report Builder er að finna í [Setja upp Report Builder](/sql/reporting-services/install-windows/install-report-builder) í fylgiskjölum SQL Server.

- RDLC Report Designer er viðbót fyrir Visual Studio 2019 og nýrra. Þú getur sótt og sett upp RDLC Report Designer á [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftRdlcReportDesignerforVisualStudio-18001).

## Stofna og breyta RDLC-útlitum

Að búa til og breyta RDLC-útlitum er ítarlegt verk sem yfirleitt yfirnotendur eða þróunaraðilar gera. Grunnhugmyndirnar eru ekki sértækar fyrir skýrsluútlit Business Central. Af þessum sökum vísum við þér á eftirfarandi fylgiskjöl:

- [Búa til RDL-útlitsskýrslu](/dynamics365/business-central/dev-itpro/developer/devenv-howto-rdl-report-layout)

   Þessi grein útskýrir hvernig á að búa til RDLC-skýrsluútlit með AL-kóða.

- [Skýrslur, skýrsluhlutar og skýrsluskilgreiningar](/sql/reporting-services/report-design/reports-report-parts-and-report-definitions-report-builder-and-ssrs?)

   Þetta tengir þig við fylgiskjöl SQL Server Reporting Services fyrir RDL/RDLC. Þessi grein útskýrir hugtökin á bak við RDL/RDLC og hvernig á að nota skýrslusmið.

> [!NOTE]
> Skýrslusmiður þekkir aðeins .rdl skráartegundina, ekki .rdlc. Útlitsskrár fluttar út úr Business Central eru: .rdlc-skráargerðir. Þannig að til breyta þessu útliti í Report Builder skal endurnefna skráargerðina sem .rdl.

## Sjá einnig

[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Stilla útlit sem skýrsla notar](ui-set-report-layout.md)  
[Hefjast handa við að búa til skýrsluútlit](ui-get-started-layouts.md)  
[Unnið með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
[Viðskiptaupplýsingar](bi.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Greina skýrslugögn með Excel](report-analyze-excel.md).

[!INCLUDE[footer-include](includes/footer-banner.md)]
