---
title: Greining á skýrslugögnum með Excel
description: Lærðu að nota Excel til að greina gagnasett í skýrslunni.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.date: 02/09/2022
ms.author: jswymer
ms.openlocfilehash: f3996c051eed69974de9511aa570f232e44764fa
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8145473"
---
# <a name="analyzing-report-data-with-excel"></a>Greining á skýrslugögnum með Excel

[!INCLUDE[2021_releasewave2](includes/2021_releasewave2.md)]

Ef um er að ræða forritara eða ítarnotanda hjálpar það við að skoða gögnin sem mynduð eru fyrir tiltekið skýrslugagnamengi á meðan nýjar skýrslur eru stofnaðar eða þeim breytt. Til að styðja þennan möguleika er hægt að flytja út skýrslugagnasafn sem hrágögn yfir í Excel vinnublað &mdash; beint af síðu skýrslubeiðninnar í biðlaranum. Í Excel er síðan hægt að gera tilfallandi greiningar á gögnum og greina mál.

## <a name="get-started"></a>Hefjast handa

Til að flytja DataSet skýrslu út í Excel Opnið þið skýrsluna í biðlaranum og á beiðasíðunni Veljið **Senda í** > **Microsoft Excel skjal (aðeins gögn)**. 

**Microsoft Excel Skjal (gagnaeinin)** valmöguleiki flytur út niðurstöður skýrslunnar og viðmiðin sem notuð voru til að mynda þau &mdash; en það felur ekki í sér útlit skýrslunnar. Excel-skráin mun innihalda allt gagnasafnið sem hrágögn, raðað í línur og dálka. Allir gagnadálkar í gagnasafni skýrslunnar eru innifaldir, óháð því hvort þeir eru notaðir í skýrsluútlitinu.

Þegar þú hefur Excel-skrána geturðu byrjað að greina gögnin. Til dæmis er hægt að sía gögnin og nota Power Pivot til að birta það.

Í hvert skipti sem þú flytur út niðurstöður er nýtt vinnublað búið til. Með því að nota valkostinn **Microsoft Excel Skjal (aðeins gögn)** er hægt að keyra sömu skýrsluna og endurnota sniðsbreytingar. Til dæmis fyrir Power Pivot geturðu keyrt skýrsluna aftur fyrir annað tímabil, afritað niðurstöðurnar í vinnublaðið og síðan uppfært vinnublaðið. Einnig er hægt að finna skýrslugerðarforrit í [AppSource](https://appsource.microsoft.com/).

> [!NOTE]
> Ekki er hægt að flytja út skýrslu sem er með fleiri en 1.048.576 línur eða 16.384 dálka. Með Business Central á staðnum gæti hámarksfjöldi útfluttra lína verið jafnvel minni. Business Central Server inniheldur grunnstillingasafn sem kallast **Hámarksfjöldi gagnaraða sem má senda til Excel** til að minnka mörk hámarksgildisins. Frekari upplýsingar er að finna í [Skilgreining Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) eða hafa samband við stjórnanda.

## <a name="for-administrators"></a>Fyrir stjórnendur

- **Microsoft Excel Skjal (aðeins gögn)** var kynnt sem valfrjáls eiginleiki í útgáfutímabili 1, uppfærslu 18.3 fyrir árið 2021. Ef veita á notendum aðgang að þessari aðgerð þegar 2021 losun bylgju 1 er keyrð skal virkja **DataSet Microsoft Excel fyrir skjalauppfærslu** í **aðgangsstjórnun**. Frekari upplýsingar er að finna [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management). Í 2021 útgáfu Wave 2 varð þessi eiginleiki varanlegur, svo ekki verður hægt að virkja hann.

- Til að nota **Microsoft Excel skjal (aðeins gögn)** þarf notendareikninga að **Leyfa útflutningsskýrslu útflutnings-DataSet yfir Excel** -heimild. Hægt er að veita notendum þessa heimild með því að **úthluta verkfærum** eða **Flytja út skýrslu með Excel** heimildinni. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).  

## <a name="for-developers-and-advanced-users"></a>Fyrir þróunaraðila og reynslumikla notendur

Valkosturinn **Microsoft Excel Skjal (aðeins gögn)** flytur út alla dálka, þ.m.t. dálka sem geyma leiðbeiningar um síur og snið fyrir önnur gildi. Hér eru nokkur áhugaverð atriði:

- Tvíundargögn í reit, eins og mynd, eru ekki flutt út.

  Í dálkum sem geyma tvíundargögn munu reitir innihalda textann **Tvíundargögn ({0} bæti)** þar sem **{0}** gefur til kynna fjölda bæta.
- Frá og með útgáfutímabil 2 í Business Central 2021 mun Excel-skráin einnig innihalda vinnublaðið **Lýsigögn skýrslu**.

  Þetta vinnublað sýnir síurnar sem notaðar eru í skýrslunni og almenna skýrslueiginleika eins og heiti, auðkenni og upplýsingar um viðbót. Síurnar eru sýndar í dálknum **Sía (DataItem::Table::FilterGroupNo::FieldName)**. Síurnar í þessum dálki innihalda síur sem eru stilltar á beiðnisíðu skýrslunnar. Þar eru einnig síur sem skilgreindar eru til að mynda í AL-kóða af [DataItemLink-eiginleikanum](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) og [DataItemTableView-eiginleikanum](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Frekari upplýsingar um skýrsluhönnun er að finna í [Yfirlit skýrslu](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

## <a name="see-also"></a>Sjá einnig

[Unnið með skýrslur](ui-work-report.md)  
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]