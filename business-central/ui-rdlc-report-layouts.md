---
title: Vinna með RDLC-útlit
description: Fáðu kynningu á RDLC-skýrsluútlitum.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/14/2022
ms.author: jswymer
---
# <a name="working-with-rdlc-layouts"></a>Vinna með RDLC-útlit

RDLC-útlit eru byggð á útlitsskrám skýrsluskilgreiningar biðlara (.rdl eða .rdlc-skráargerðir). Hönnunarhugmyndirnar fyrir RDLC-útlit eru svipaðar og fyrir aðrar útlitsgerðir. Útlitið ræður hvaða reiti á að sýna og hvernig þeim er raðað. Hönnun RDLC-útlits er hins vegar ítarlegra en Word- og Excel-útlits.

[![Sýnir mismunandi einingar RDLC-útlits.](media/rdlc-layout.png)](media/rdlc-layout.png#lightbox)

## <a name="required-tools"></a>Nauðsynleg verkfæri

Til að breyta RDL-útliti er hægt að nota annaðhvort Microsoft SQL Server Report Builder eða Microsoft RDLC Report Designer.

- Report Builder er sjálfstætt forrit sem þú eða stjórnandi þinn hefur sett upp í tölvunni þinni. Með Business Central á staðnum er Report Builder sjálfkrafa settur upp með uppsetningu Business Central Server. Frekari upplýsingar um uppsetningu Report Builder er að finna í [Setja upp Report Builder](/sql/reporting-services/install-windows/install-report-builder) í fylgiskjölum SQL Server.

- RDLC Report Designer er viðbót fyrir Visual Studio 2017 og nýrra. Þú getur sótt og sett upp RDLC Report Designer á [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftRdlcReportDesignerforVisualStudio-18001).

## <a name="create-and-modify-rdlc-layouts"></a>Stofna og breyta RDLC-útlitum

Að búa til og breyta RDLC-útlitum er ítarlegt verk sem yfirleitt yfirnotendur eða þróunaraðilar gera. Grunnhugmyndirnar eru ekki sértækar fyrir skýrsluútlit Business Central. Af þessum sökum vísum við þér á eftirfarandi fylgiskjöl:

- [Búa til RDL-útlitsskýrslu](/dynamics365/business-central/dev-itpro/developer/devenv-howto-rdl-report-layout)

    Þessi grein útskýrir hvernig á að búa til RDLC-skýrsluútlit með AL-kóða.

- [Skýrslur, skýrsluhlutar og skýrsluskilgreiningar](/sql/reporting-services/report-design/reports-report-parts-and-report-definitions-report-builder-and-ssrs?)

 Þetta tengir þig inn á fylgiskjöl SQL Server Reporting Services fyrir RDL/RDLC. Þessi fylgiskjöl útskýra hugmyndina  
á bak við RDL/RDLC og hvernig á að nota Report Builder.

> [!NOTE]
> Report Builder þekkir aðeins .rdl-skráargerð;, ekki .rdlc. Útlitsskrár fluttar út úr Business Central eru: .rdlc-skráargerðir. Þannig að til breyta þessu útliti í Report Builder skal endurnefna skráargerðina sem .rdl.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Stilla útlit sem skýrsla notar](ui-set-report-layout.md)  
[Hefjast handa við að búa til skýrsluútlit](ui-get-started-layouts.md)  
[Unnið með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
[Viðskiptaupplýsingar](bi.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Greina skýrslugögn með Excel](report-analyze-excel.md).

[!INCLUDE[footer-include](includes/footer-banner.md)]
