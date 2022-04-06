---
title: Stjórna útliti skýrslna og skjala
description: Nota útlitssnið skýrslu til að sérstilla skjöl, til dæmis að hafa persónulega leturgerð, lógó og síðustillingar PDF skjala sem þú sendir til viðskiptamanna.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9652, 9650
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 5fed722bb5929da100c1c92e63aebb1f10cf53d0
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520683"
---
# <a name="report-and-document-layouts-overview"></a>Yfirlit yfir skýrslur og Skjalaskipan

Skýrslusnið stjórnar efni og sniði skýrslunnar, þar á meðal hvaða gagnasvæði í skýrslugagnabanka kemur fram í skýrslunni og hvernig þeim er raðað, textastíl, myndum og fleiru. Í [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að breyta því hvaða útlit er notað í skýrslu, búa til nýtt útlit eða breyta fyrirliggjandi útliti.

> [!NOTE]  
> Í [!INCLUDE[prod_short](includes/prod_short.md)] táknar hugtakið "skýrsla" einnig utanaðkomandi skjöl, s.s. sölureikninga og pöntunarstaðfestingar sem þú sendir til viðskiptavina sem PDF skjöl.

## <a name="introduction"></a>Kynning

Einkum setur skýrsluskipan fram eftirfarandi atriði:

* Merkið og gagnareitir sem taka á með úr gagnamengi tiltekinnar [!INCLUDE[prod_short](includes/prod_short.md)] skýrslu.
* Textasniðið, eins og leturgerð, stærð og litur.
* Fyrirtækjamerki og staðsetning þess.
* Almennar síðustillingar, eins og spássíur og bakgrunnsmyndir.

Skýrsla getur verið uppsett með mismunandi útliti sem hægt er að skipta á milli. 

<!--You can use one of the built-in report layouts or you can create custom report layouts and assign them to your reports as needed. For more information, see [Create a Custom Report or Document Layout](ui-how-create-custom-report-layout.md).-->

Það eru tveir mikilvægir þættir í skýrsluskipan sem hafa áhrif á það hvernig unnið er með þá: *útlitsgerð* og *Uppruni útlits*. Gerð útlits Tilgreinir hvers konar skrá sem útlitið byggist á. Uppruni útlits segir til um uppruna útlitins.

## <a name="layout-types"></a>Gerðir útlits

Til eru fjórar gerðir af útliti sem hægt er að nota á skýrslur: Word, RDLC, Excel og utanumhald.

### <a name="word"></a>Orðið

Ritskipan er byggð á Word skjölum (. docx skrárgerð). Orð skipulag gera þér kleift að hanna skipulag skýrslu með notkun Microsoft Word. Word skipulag ákvarðar efnisþætti skýrslunnar hvernig þeim efnisþáttum er raðað upp og hvernig þeir líta út. Word-útlitsskjal notar gjarnan töflur til að raða efni, þar sem í frumunum geta verið gagnasvæði, texti eða myndir.

[![Dæmi um Word-skýrsluútlit skjals fyrir Seðlabankaviðskipti.](media/word-layout-overview.png)](media/word-layout-overview.png#lightbox) 

<!--![Example of a word report layout document for Business Central.](media/nav_wordreportlayout_edit_in_word_example.png) -->

Nánari upplýsingar má finna [í vinnu með Word skipulag](ui-how-add-fields-word-report-layout.md).

### <a name="excel"></a>Excel

Excel skipulag byggir á Microsoft Excel vinnubókum (. xlsx skrárgerð). Þeir gera kleift að stofna skýrslur með því að nota kunnuglegar Excel-aðgerðir til að samantekta, greina og kynna gögn með verkfærum eins og formúlum, PivotTables, Pivotgrösum og fleira.

[![Sýnir dæmi um Excel útlit.](media/excel-layout-2.png)](media/excel-layout-2.png#lightbox)

Sjá [vinnu með Excel-skipan](ui-excel-report-layouts.md) fyrir frekari upplýsingar.

### <a name="rdlc"></a>RDLC-

RDLC-skipan byggja á skrárgerð fyrir biðlaraskilgreiningar (. RDL eða. RDLC-skrár). Þessi skipan er stofnuð og henni breytt með SQL Server Report Builder eða Microsoft RDLC-Skýrsluhönnuði. Hönnunarhugmynd fyrir RDLC-uppsetningu er svipuð og Word skipulag, þar sem útlitið ræður því hvaða svæði á að sýna og hvernig þeim er raðað. Hins vegar er hanna RDLC-skipan mun ítarlegri en Word-skipulag.

[![Sýnir dæmi um uppsetningu RDLC.](media/rdlc-layout-overview.png)](media/rdlc-layout-overview.png#lightbox)

Frekari upplýsingar [fást í vinnu með RDLC-skipan](ui-rdlc-report-layouts.md).

### <a name="external"></a>Ytri

Gerð ytri útlits vísar til ítarlegrar gerðar sem er sérstaklega hönnuð fyrir tilteknar skýrslur. Skýrslurnar og skipulag sjálfir koma gjarnan frá samstarfsaðilum, ekki Microsoft. Raunveruleg skrárgerð útlits mun vera breytileg eftir veitunni.

Frekari upplýsingar er að finna [í þróun sérsniðinna](/dynamics365/business-central/dev-itpro/developer/devenv-report-custom-render) skýrslna.

## <a name="layout-sources"></a>Heimildir útlits

Auk tegundanna er skipulag frekar skipt í þrjá flokka eftir uppruna þeirra eða uppruna.

* Skipulag viðaukauppsetningar

   Framlengingarskipulag er útlit sem er hluti af framlengingu sem sett hefur verið upp í appinu. Þessi uppsetning er vanalega stöðluð skipan sem Microsoft veitir, til dæmis í grunnforritinu. Eða gætu þær verið uppsetningar sem eru innifaldar í viðaukum frá öðrum hugbúnaðarveitum. Hægt er að þekkja viðaukaskipan á **síðu skýrsluuppsetningar** þar sem nafn viðaukann og útgefanda er sýnt í **viðaukdálkinum**.

* Skipulag notandaskilgreinds

   Hin upprunaliga skipan er endaliga-notandinn. Í innu Business Central getur notandi með réttar heimildir bætt við nýju útliti á ýmsa vegu. Til dæmis væri hægt að ræsa núgildandi framlengingarútlit eða annað Notandaskilgreint. **Í útliti skýrslunnar** mun Notandaskilgreint útlit vera með tóma **viðaukadálk**.

   Frekari upplýsingar er að finna [í fá hóf að búa til Skýrsluskipulag](ui-get-started-layouts.md).

* Sérsniðnar uppsetningar

  Sérsniðnar uppsetningar eru einnig skipulag sem eru stofnaðar af notendum. Munurinn er sá að þessar skipanir eru búnar til úr eldri **síðu sérsniðinnar uppsetningar** á skýrslum og þær eru bara orð og RDLC-gerð. Þó að hægt sé að stofna sérsniðna skipan er verið að búa þær til í þágu notendaskilgreinds uppsetningar.

  Frekari upplýsingar er að finna [í (Legacy) stofna og breyta skipan](ui-how-create-custom-report-layout.md) sérsniðinnar skýrslu.

Fyrir upplýsingar sem hjálpa þér að ákveða hvaða tegund er best fyrir þig, sérðu [ákveða hvaða gerð af útliti þú vilt](ui-get-started-layouts.md#decide).

> [!IMPORTANT]
> Eitt mikilvægt atriði til muna er að ekki er hægt að breyta framlengingarútliti frá Viðskiptamiðinu. Til dæmis er ekki leyfilegt að breyta heiti útlits eða upphleðslu og skipta henni út fyrir aðra útgáfu. Ef þú reynir færðu villuskilaboð. Stofna þarf Notandaskilgreint eða sérsniðið útlit á grundvelli framlengingarútlits í staðinn.

<!--
### Built-in and custom report layouts



[!INCLUDE[prod_short](includes/prod_short.md)] includes several built-in layouts. Built-in layouts are predefined layouts that are designed for specific reports. [!INCLUDE[prod_short](includes/prod_short.md)] reports will have a built-in layout as either an RDLC report layout, Word report layout, or in some cases both. You can’t modify a built-in report layout from [!INCLUDE[prod_short](includes/prod_short.md)] but you use them as a starting point for building your own custom report layouts.

Custom layouts are report layouts that you design to change the appearance of a report. You typically create a custom layout based on a built-in layout, but you can create them from scratch or from a copy of an existing custom layout. Custom layouts enable you to have multiple layouts for the same report, which you switch among as needed. For example, you can have different layouts for each [!INCLUDE[prod_short](includes/prod_short.md)] company, or you can have different layouts for the same company for specific occasions or events, like a special campaign or holiday season.


Deciding on whether to use a Word, Excel, or RDLC layout type will depend on how you want the generated report to look and your knowledge of tools for creating the layouts, like Word, Excel, and SQL Server Report Builder.

* The general design concepts for Word and RDLC layouts are similar. However each type has certain design features that affect how the generated report appears in [!INCLUDE[prod_short](includes/prod_short.md)]. This means that the same report might look different when using the Word report layout compared to the RDLC report layout.

* The process for setting up Word, Excel, and RDLC report layouts on reports is the same. The main difference is in the way you modify the layouts. Word and especially Excel layouts are typically easier to create and modify than RDLC report layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.

* Not all reports and document have a dataset that is optimized for use with an Excel layout. For example, aggregations and complex calculations work best with RDLC or Word layouts. The same is true for documents.

For information about how to switch the layout currently used on a report, see [Set the Layout Used by a Report](ui-set-report-layout.md).

-->



## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Uppfæra sérsniðið skýrsluútlit](ui-update-report-layouts.md)  
[Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md)  
[Flytja inn og út sérsniðið skýrsluútlit eða skjalaútlit](ui-how-import-and-export-report-layout.md)  
[Skilgreina sérstakt útlit skjala fyrir viðskiptamenn og lánardrottna](ui-define-customer-vendor-document-layouts.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Vinna með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]