---
title: Þróun skipulag og gagnasöfn í skýrslu
description: Veitir yfirsýn yfir aðalgögn viðskipta.
author: kennieNP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: feature overview
ms.date: 02/03/2022
ms.author: kepontop
ms.openlocfilehash: f1ae794b1345e50d7a649c117514c8cf94dcc025
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8139392"
---
# <a name="developing-business-central-report-layouts-and-datasets"></a>Þróun Viðskiptamiðaðrar miðlægu skýrsluuppsetningar og Gagnasett

Skýrsla í [!INCLUDE[prod_short](includes/prod_short.md)]samanstendur af skýrsluhlut sem skilgreinir _DataSet_ skýrslunnar (hvaða gögn eru tiltæk) og fjölda _skýrsluuppsetningar_ (hvernig gögn eru kynnt).  

## <a name="developing-report-layouts"></a>Þróun skýrsluuppsetningar

Kannski á að breyta núverandi skýrsluskipan sem er veitt í [!INCLUDE[prod_short](includes/prod_short.md)]? Það fer eftir því hvaða tækni er notuð við útlitinu, þetta er eitthvað sem þú gætir mögulega gert sjálfur (Excel og kannski líka Word skipulag), eða kannski þarftu forritara til þess að gera það (dísel-fullkomin RDLC-skipan).

| Til að | Sjá |
|--|--|
| Frekari upplýsingar um mismunandi útlitstegundir (Word, Excel og RDLC) | [Útlitsgerðir (Word, Excel og RDLC)](ui-manage-report-layouts.md) |
| Fræðast um hvernig hægt er að stofna nýtt útlit skýrslu. | [Búa til nýtt útlit](ui-how-create-custom-report-layout.md) |
| Upplýsingar um hvaða leturgerðir eru settar upp í [!INCLUDE[prod_short](includes/prod_short.md)]á netinu svo hægt sé að nota þær í skýrsluskipan. | [Leturgerðir notaðar í skipan](ui-fonts.md) |
| Að læra hvernig unnið er með Ritskipulag. | [Vinna með Orðskipulag](ui-how-add-fields-word-report-layout.md) |
| Til að læra hvernig á að flytja/flytja út útlitsskrár. | [Flytja út/flytja út útlit](ui-how-import-and-export-report-layout.md) |
| Til að læra hvernig á að uppfæra skilgreiningu útlits í [!INCLUDE[prod_short](includes/prod_short.md)]með nýrri útlitsskrá. | [Flytja út/flytja út útlit](ui-how-import-and-export-report-layout.md) |
| Til að læra hvernig eigi að breyta sjálfgefnu útliti fyrir skýrslu. | [Breyttu sjálfgefnu útliti](ui-how-change-layout-currently-used-report.md) |
< | Að læra hvernig unnið er með Excel-skipulag | [Vinna við Excel-skipulag](ui-how-add-fields-word-report-layout.md) | -->

## <a name="developing-report-datasets"></a>Þróa gagnasöfn með skýrslugerð

 Ef breyta á skilgreiningum DataSet sem skilgreina hvaða gögn eru tiltæk í skýrslunni þarf forritari að vita um AL-Forritunarmálið og verkfærin til að þróa skýrsluhluta og nafnauka í skýrsluviðbótum.

| Til að | Sjá |
|--|--|
| Lærðu að forrita skýrslur í AL- | [Leiðbeiningar um skýrsluþróun](/dynamics365/business-central/dev-itpro/developer/devenv-reports) |
| Lærðu að gera skýrslur framkvæmdar | [Skýrsla um árangur Tuning Guide](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-reports) |

## <a name="see-also"></a>Sjá einnig

[Viðskiptagreind og skýrslugerð Yfirlit](reports-use-reports.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]