---
title: Greining skýrslugagna með Excel og XML
description: Kynntu þér hvernig þú notar Excel og XML til að greina gagnasafn skýrslu.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, Word, dataset'
ms.date: 03/16/2022
ms.author: jswymer
---
# <a name="analyzing-report-data-with-excel-and-xml"></a>Greining skýrslugagna með Excel og XML

[!INCLUDE[2021_releasewave2](includes/2021_releasewave2.md)]

Sem þróunaraðili eða vanur notandi er hjálplegt að skoða gögnin sem eru búin til fyrir tiltekið gagnasafn skýrslu á meðan þú býrð til nýjar skýrslur eða breytir þeim sem fyrir eru. Til að styðja við þennan möguleika er hægt að flytja út gagnasafn skýrslu sem hrá gögní Excel-vinnubók eða XML-skrá&mdash;beint. Í Excel er til dæmis hægt að gera tilfallandi greiningu á gögnum og greina vandamál.

## <a name="get-started"></a>Hafist handa

Til að flytja gagnasafn skýrslu út í Excel-vinnubók eða XML-skrá skal opna skýrsluna í biðlaranum, síðan á beiðnisíðunni velja **Senda til** > **Microsoft Excel skjal (aðeins gögn)** eða **XML-skjal**. Skránni verður hlaðið niður í tækið þitt.

## <a name="more-about-excel-data-only"></a>Meira um Excel (aðeins gögn)

Valkosturinn **Microsoft Excel Skjal (aðeins gögn)** flytur út niðurstöður skýrslunnar og skilyrðið sem var notað til að mynda þær&mdash;en hún inniheldur ekki skýrsluútlitið. Excel-skráin mun innihalda allt gagnasafnið sem hrágögn, raðað í línur og dálka. Allir gagnadálkar í gagnasafni skýrslunnar eru innifaldir, óháð því hvort þeir eru notaðir í skýrsluútlitinu.

Þegar Excel-skráin er komin er hægt að greina gögnin. Til dæmis er hægt að sía gögnin og nota Power Pivot til að birta þau.

Í hvert skipti sem þú flytur út niðurstöður er nýtt vinnublað búið til. Með því að nota valkostinn **Microsoft Excel Skjal (aðeins gögn)** er hægt að keyra sömu skýrsluna og endurnota sniðsbreytingar. Til dæmis fyrir Power Pivot geturðu keyrt skýrsluna aftur fyrir annað tímabil, afritað niðurstöðurnar í vinnublaðið og síðan uppfært vinnublaðið. Einnig er hægt að finna skýrslugerðarforrit í [AppSource](https://appsource.microsoft.com/).

> [!NOTE]
> Ekki er hægt að flytja út skýrslu sem er með fleiri en 1.048.576 línur eða 16.384 dálka. Með Business Central á staðnum gæti hámarksfjöldi útfluttra lína verið jafnvel minni. Business Central Server inniheldur grunnstillingasafn sem kallast **Hámarksfjöldi gagnaraða sem má senda til Excel** til að minnka mörk hámarksgildisins. Frekari upplýsingar er að finna í [Skilgreining Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) eða hafa samband við stjórnanda.

## <a name="for-administrators"></a>Fyrir stjórnendur

- **Microsoft Excel Skjal (aðeins gögn)** var kynnt sem valfrjáls eiginleiki í útgáfutímabili 1, uppfærslu 18.3 fyrir árið 2021. Til að veita notendum aðgang að þessum eiginleika skal virkja 2021 útgáfutímabil 1, virkja eiginleikauppfærsluna **Vista gagnasafn skýrslu í Microsoft Excel skjal** í **Eiginleikastjórnun**. Frekari upplýsingar er að finna [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management). Á útgáfutímabili 2 fyrir árið 2021 er þessi eiginleiki varanlegur og þarf þá ekki að virkja hann.

- Til að nota **Microsoft Excel skjal (aðeins gögn)** þurfa notandareikningar á leyfinu **Leyfa aðgerð til að flytja út skýrslugagnasafn í Excel** að halda. Hægt er að gefa notendum þessa heimild með því að úthluta annaðhvort heimildasamstæðunni **Verkfæri úrræðaleitar** eða **Flytja út skýrslu í Excel**. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).  

## <a name="for-developers-and-advanced-users"></a>Fyrir þróunaraðila og reynslumikla notendur

Valkosturinn **Microsoft Excel Skjal (aðeins gögn)** flytur út alla dálka, þ.m.t. dálka sem geyma leiðbeiningar um síur og snið fyrir önnur gildi. Hér eru nokkur áhugaverð atriði:

- Tvíundargögn í reit, eins og mynd, eru ekki flutt út.

  Í dálkum sem geyma tvíundargögn munu reitir innihalda textann **Tvíundargögn ({0} bæti)** þar sem **{0}** gefur til kynna fjölda bæta.
- Frá og með útgáfutímabil 2 í Business Central 2021 mun Excel-skráin einnig innihalda vinnublaðið **Lýsigögn skýrslu**.

  Þetta vinnublað sýnir síurnar sem notaðar eru í skýrslunni og almenna skýrslueiginleika eins og heiti, auðkenni og upplýsingar um viðbót. Síurnar eru sýndar í dálknum **Sía (DataItem::Table::FilterGroupNo::FieldName)**. Síurnar í þessum dálki innihalda síur sem eru stilltar á beiðnisíðu skýrslunnar. Þar eru einnig síur sem skilgreindar eru til að mynda í AL-kóða af [DataItemLink-eiginleikanum](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) og [DataItemTableView-eiginleikanum](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Frekari upplýsingar um skýrsluhönnun er að finna í [Yfirlit skýrslu](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

## <a name="see-also"></a>Sjá einnig

[Unnið með Skýrslur](ui-work-report.md)  
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
