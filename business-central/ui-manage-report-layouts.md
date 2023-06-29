---
title: Stjórna útliti skýrslna og skjala
description: 'Nota útlitssnið skýrslu til að sérstilla skjöl, til dæmis að hafa persónulega leturgerð, lógó og síðustillingar PDF skjala sem þú sendir til viðskiptamanna.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650'
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="report-and-document-layouts-overview"></a><a name="report-and-document-layouts-overview"></a>Yfirlit yfir skýrslu- og skjalaútlit

Útlit skýrslu stjórnar efni og sniði skýrslunnar, þ.m.t. hvaða gagnareitir gagnasafn skýrslu birtast í henni, stöðu þeirra, textastíl, myndir og meira. Í [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að breyta því hvaða útlit er notað í skýrslu, búa til nýtt útlit eða breyta fyrirliggjandi útliti.

> [!NOTE]  
> Í [!INCLUDE[prod_short](includes/prod_short.md)] táknar hugtakið "skýrsla" einnig utanaðkomandi skjöl, s.s. sölureikninga og pöntunarstaðfestingar sem þú sendir til viðskiptavina sem PDF skjöl.

Einnig er hægt að nota skýrsluútlit til að bæta efni við tölvupóstskeyti. Til dæmis getur skýrsluútlit sparað tíma og tryggt samræmi með því að endurnota sama efnið þegar haft er samband við viðskiptamenn. Til að nota sérsniðið skýrsluútlit með tölvupósti verður skráargerðin fyrir útlitið að vera Word. Ekki er hægt að nota RDLC-skráargerðina. Frekari upplýsingar eru í [Setja upp endurnýtanlega texta og útlit tölvupósts](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## <a name="introduction"></a><a name="introduction"></a>Kynning

Skýrsluútlit setur einkum eftirfarandi upp:

* Merkið og gagnareitir sem taka á með úr gagnamengi tiltekinnar [!INCLUDE[prod_short](includes/prod_short.md)] skýrslu.
* Textasniðið, eins og leturgerð, stærð og litur.
* Fyrirtækjamerki og staðsetning þess.
* Almennar síðustillingar, eins og spássíur og bakgrunnsmyndir.

Skýrsla getur verið uppsett með mismunandi útliti sem hægt er að skipta á milli. 

<!--You can use one of the built-in report layouts or you can create custom report layouts and assign them to your reports as needed. For more information, see [Create a Custom Report or Document Layout](ui-how-create-custom-report-layout.md).-->

Tveir mikilvægir þættir í skýrsluútliti munu hafa áhrif á hvernig þú vinnur með þau: *útlitsgerðin* og *útlitsuppruninn*. Gerð útlits gefur til kynna hvers konar skrá útlitið byggir á. Uppruni útlits gefur til kynna uppruna útlitsins.

## <a name="layout-types"></a><a name="layout-types"></a>Útlitsgerðir

Þú getur notað fjórar gerðir útlita í skýrslum: Word, RDLC, Excel og ytra.

### <a name="word"></a><a name="word"></a>Word

Word-útlit byggja á Word-skjölum (.docx-skráargerð). Word-útlit gerir þér kleift að hanna skýrsluútlit með Microsoft Word. Word útlit ákvarðar innihald skýrslunnar og stjórnar því hvernig þeir efnisþættir raðast og hvernig þeir líta út. Word útlitsskjal notar vanalega töflur til að raða efni, þar sem hólf geta innihaldið gögn, reiti, texta eða myndir.

[![Dæmi um skjal word-skýrsluútlits fyrir Business Central.](media/word-layout-overview.png)](media/word-layout-overview.png#lightbox) 

<!--![Example of a word report layout document for Business Central.](media/nav_wordreportlayout_edit_in_word_example.png) -->

Nánari upplýsingar eru í [Vinna með Word-útlit](ui-how-add-fields-word-report-layout.md).

### <a name="excel"></a><a name="excel"></a>Excel

Excel-útlit byggir á Microsoft Excel vinnubókum (.xlsx skráargerð). Þær gera þér kleift að búa til skýrslur með því að nota Excel-eiginleika til að taka saman, greina og kynna gögn með verkfærum eins og formúlum, PivotTable, PivotChart og fleirum.

[![Sýnir dæmi um Excel-útlit.](media/excel-layout-2.png)](media/excel-layout-2.png#lightbox)

Nánari upplýsingar eru í [Vinna með Excel-útlit](ui-excel-report-layouts.md).

### <a name="rdlc"></a><a name="rdlc"></a>RDLC

RDLC-útlit eru byggð á útlitsskrám skýrsluskilgreiningar biðlara (.rdl eða .rdlc-skráargerðir). Þessi útlit eru búin til og þeim breytt með SQL Server Report Builder eða Microsoft RDLC Report Designer. Hönnunarhugmyndin fyrir RDLC-útlit er svipuð og fyrir Word-útlitið þar sem útlitið ákveður hvaða reiti á að sýna og hvernig þeim er raðað upp. Hönnun RDLC-útlits er hins vegar ítarlegra en Word-útlits.

[![Sýnir dæmi um RDLC-útlit.](media/rdlc-layout-overview.png)](media/rdlc-layout-overview.png#lightbox)

Nánari upplýsingar eru í [Vinna með RDLC-útlit](ui-rdlc-report-layouts.md).

### <a name="external"></a><a name="external"></a>Ytri

Gerð ytra útlits vísar til ítarlegrar gerðar sem er sérstaklega hönnuð fyrir tilteknar skýrslur. Skýrslurnar og útlitin sjálf eru yfirleitt fengin frá samstarfsaðilum, ekki Microsoft. Raunveruleg skráargerð útlitsins fer eftir veitunni.

Frekari upplýsingar er að finna í [Þróun myndþýðingar á sérsniðinni skýrslu](/dynamics365/business-central/dev-itpro/developer/devenv-report-custom-render).

## <a name="layout-sources"></a><a name="layout-sources"></a>Útlitsupprunar

Auk gerðar er útlitum frekar skipt niður í þrjá flokka út frá uppruna þeirra.

* Útlit viðbóta

   Útlit viðbóta eru útlit sem eru hluti af viðbót sem hefur verið sett upp í umhverfinu. Þessi útlit eru yfirleitt stöðluð útlit sem Microsoft býður upp á, t.d. í grunnforritinu. Eða þau gætu verið útlit sem eru hlut af viðbótum úr öðrum hugbúnaðarveitum. Hægt er að þekkja útlit viðbóta á síðunni **Skýrsluútlit** því að heiti viðbótar og útgefanda er sýnt í dálkinum **Viðbót**.

* Útlit skilgreind af notanda

   Hinn uppruni útlita er endanotandinn. Í Business Central getur notandi með réttar heimildir bætt við nýjum útlitum á ýmsan hátt. Til dæmis er hægt að byrja á núverandi útliti viðbótar eða öðru útlit skilgreindu af notanda. Í **Skýrsluútliti** verður útlit skilgreint af notanda með auðan dálk fyrir **Viðbót**.

   Frekari upplýsingar eru í [Hefjast handa við að búa til skýrsluútlit](ui-get-started-layouts.md).

* Sérstilla útlit

  Sérsniðin útlit eru einnig útlit sem notendur búa til. Munurinn er sá að þessi útlit eru búin til á eldri síðunni **Sérsniðin skýrsluútlit** og þau geta bara verið af Word- eða RDLC-gerðinni. Þótt þú getir enn búið til sérsniðin útlit er verið að taka þau úr umferð og nota frekar útlit skilgreind af notanda.

  Nánari upplýsingar er að finna í [(Eldra) Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md).

Fyrir upplýsingar sem hjálpa þér að ákveða hvaða gerð er best fyrir þig skaltu skoða [Taktu ákvörðun um hvers konar útlit þú vilt nota](ui-get-started-layouts.md#decide).

> [!IMPORTANT]
> Eitt mikilvægt atriði til að hafa í huga er að þú getur ekki breytt útlitum viðbóta úr biðlara Business Central. Til dæmis máttu ekki breyta heiti útlitsins eða gerðinni, eða hlaða upp og skipta því út fyrir aðra útgáfu. Ef það er reynt koma upp villuboð. Í staðinn þarftu að búa til notandaskilgreint útlit eða sérsniðið útlit sem byggir á útliti viðbótarinnar.

<!--
### <a name="built-in-and-custom-report-layouts"></a><a name="built-in-and-custom-report-layouts"></a>Built-in and custom report layouts



[!INCLUDE[prod_short](includes/prod_short.md)] includes several built-in layouts. Built-in layouts are predefined layouts that are designed for specific reports. [!INCLUDE[prod_short](includes/prod_short.md)] reports will have a built-in layout as either an RDLC report layout, Word report layout, or in some cases both. You can’t modify a built-in report layout from [!INCLUDE[prod_short](includes/prod_short.md)] but you use them as a starting point for building your own custom report layouts.

Custom layouts are report layouts that you design to change the appearance of a report. You typically create a custom layout based on a built-in layout, but you can create them from scratch or from a copy of an existing custom layout. Custom layouts enable you to have multiple layouts for the same report, which you switch among as needed. For example, you can have different layouts for each [!INCLUDE[prod_short](includes/prod_short.md)] company, or you can have different layouts for the same company for specific occasions or events, like a special campaign or holiday season.


Deciding on whether to use a Word, Excel, or RDLC layout type will depend on how you want the generated report to look and your knowledge of tools for creating the layouts, like Word, Excel, and SQL Server Report Builder.

* The general design concepts for Word and RDLC layouts are similar. However each type has certain design features that affect how the generated report appears in [!INCLUDE[prod_short](includes/prod_short.md)]. This means that the same report might look different when using the Word report layout compared to the RDLC report layout.

* The process for setting up Word, Excel, and RDLC report layouts on reports is the same. The main difference is in the way you modify the layouts. Word and especially Excel layouts are typically easier to create and modify than RDLC report layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.

* Not all reports and document have a dataset that is optimized for use with an Excel layout. For example, aggregations and complex calculations work best with RDLC or Word layouts. The same is true for documents.

For information about how to switch the layout currently used on a report, see [Set the Layout Used by a Report](ui-set-report-layout.md).

-->



## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig

[Uppfæra sérsniðið skýrsluútlit](ui-update-report-layouts.md)  
[Búa til og breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md)  
[Flytja inn og út sérsniðið skýrsluútlit eða skjalaútlit](ui-how-import-and-export-report-layout.md)  
[Skilgreina sérstakt útlit skjala fyrir viðskiptamenn og lánardrottna](ui-define-customer-vendor-document-layouts.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Vinna með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
