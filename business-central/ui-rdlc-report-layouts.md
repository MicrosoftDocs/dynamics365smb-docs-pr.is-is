---
title: Vinna við RDLC-skipan
description: Fá kynningu á skipan RDLC-skýrslunnar.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/14/2022
ms.author: jswymer
ms.openlocfilehash: 0d3a1ce19b094fa77ae332a8dc90f1e8b3712cbf
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532485"
---
# <a name="working-with-rdlc-layouts"></a>Vinna við RDLC-skipan

RDLC-skipan byggja á skrárgerð fyrir biðlaraskilgreiningar (. RDL eða. RDLC-skrár). Hönnunarhugmyndir fyrir RDLC-skipulag eru svipaðar og aðrar gerðir útlits. Útlitið ræður því hvaða svæði á að sýna og hvernig þeim er raðað. Hins vegar er hönnun RDLC mun ítarlegri en Word og Excel-skipulag.

[![Sýnir mismunandi einingar RDLC-útlits.](media/rdlc-layout.png)](media/rdlc-layout.png#lightbox)

## <a name="required-tools"></a>Nauðsynleg verkfæri

Til að breyta skipan RDL er hægt að nota annað hvort Microsoft SQL Server Skýrslusmið eða Microsoft RDLC-Skýrsluhönnuði.

- Skýrslusmiður er Stand-eingi forrit uppsett á tölvunni af notanda eða stjórnanda. Með Business Central innanhúss er Skýrslusmiður settur upp sjálfvirkt með uppsetningu miðlægu þjónsins. Nánari upplýsingar um uppsetningu skýrslusmiðs er að finna [í setja upp Skýrslusmið](/sql/reporting-services/install-windows/install-report-builder) í fylgigögnum SQL Server.

- RDLC-skýrsla hönnuð í viðauka fyrir Visual Studio 2017 og nýrri. Hægt er að sækja og setja upp RDLC Skýrsluhönnuði úr [Visual Studio markaðstorginu](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftRdlcReportDesignerforVisualStudio-18001).

## <a name="create-and-modify-rdlc-layouts"></a>Stofna og breyta um RDLC-skipan

Að búa til og breyta RDLC-skipan er Ítarlegt verk sem er vanalega gert af orkunotendum eða hönnuðum. Grunnhugtökin eru ekki sértæk fyrir skipulag miðlægu skýrslunnar. Af þessum ástæðum er m.a. vísað í eftirfarandi fylgigögn:

- [Stofna RDL-útlit skýrslu](/dynamics365/business-central/dev-itpro/developer/devenv-howto-rdl-report-layout)

    Í þessari grein er útskýrt hvernig á að búa til RDLC-skýrsluuppsetningu úr AL-kóða.

- [Skýrslur, hlutar og skýrsluskilgreiningar](/sql/reporting-services/report-design/reports-report-parts-and-report-definitions-report-builder-and-ssrs?)

 Tenglar í fylgigögn með SQL Server Reporting Services fyrir RDL/RDLC. Í þessum fylgigögnum er útskýrt hugtökin  
Bak við RDL/RDLC og hvernig á að nota Skýrslusmið.

> [!NOTE]
> Skýrslusmiður þekkir aðeins. RDL-skrárgerð;, ekki. RDLC. Útlitsskrár fluttar úr skrárgerðum fyrirtækja miðlægt. RDLC. Svo til að breyta þessu útliti í Skýrslusmið þarf að endurnefna skrárgerðina. RDL.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Stilla útlit sem skýrsla er notuð fyrir](ui-set-report-layout.md)  
[Byrja að búa til Skýrsluskipulag](ui-get-started-layouts.md)  
[Unnið með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
[Viðskiptaupplýsingar](bi.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Greining á skýrslugögnum með Excel](report-analyze-excel.md).

[!INCLUDE[footer-include](includes/footer-banner.md)]
