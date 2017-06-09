---
title: "Stjórnun skýrsluútlits | Microsoft Docs"
description: "Upplýsingar um skýrsluútlit"
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: e221f5264190a90e04132ed4326afe2cf8364164
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="managing-report-and-document-layouts"></a>Stjórna útliti skýrslna og skjala
Útlit skýrslu stjórnar efni og sniði skýrslunnar, þ.m.t. hvaða gagnareitir gagnasafn skýrslu birtast í henni, stöðu þeirra, textastíl, myndir og meira. Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að breyta því hvaða útlit er notað í skýrslu, búa til nýtt útlit eða breyta fyrirliggjandi útliti.

**Athugasemd**: Í [!INCLUDE[d365fin](includes/d365fin_md.md)] táknar hugtakið "skýrsla" einnig utanaðkomandi skjöl, s.s. sölureikninga og pöntunarniðurstöður sem þú sendir til viðskiptavina sem PDF skjöl.

Skýrsluútlit setur einkum eftirfarandi upp:

* Merkið og gagnareitir sem taka á með úr gagnamengi tiltekinnar [!INCLUDE[d365fin](includes/d365fin_md.md)] skýrslu.
* Textasniðið, eins og leturgerð, stærð og litur.
* Fyrirtækjamerki og staðsetning þess.
* Almennar síðustillingar, eins og spássíur og bakgrunnsmyndir.

[!INCLUDE[d365fin](includes/d365fin_md.md)] getur verið uppsett með mismunandi útliti sem hægt er að skipta á milli. Hægt er að nota eitt af innbyggðum skýrsluútlitum eða stofna sérsniðið skýrsluútlit og úthluta þeim á skýrslur eftir þörfum. Nánari upplýsingar er að finna í [Hvernig á að: Búa til sérsniðið skýrsluútlit eða skjalaútlit](ui-how-create-custom-report-layout.md).

Það eru tvær gerðir skýrsluútlita sem hægt er að nota á skýrslur, Word og RDLC.

## <a name="word-report-layout-overview"></a>Yfirlit Word skýrsluútlits
Word-skýrsluútlit byggir á Word-skjali (.docx-skráargerð). Word-skýrsluútlit gerir þér kleift að hanna skýrsluútlit með Microsoft Word 2013 eða síðar. Word skýrsluútlit ákvarðar innihald skýrslunnar og stjórnar því hvernig þeir efnisþættir raðast og hvernig þeir líta út. Word skýrsluútlitsskjal notar vanalega töflur til að raða efni, þar sem hólf geta innihaldið gögn, reiti, texta eða myndir.

## <a name="rdlc-layout-overview"></a>Yfirlit RDLC-útlits
RDLC-útlit eru byggð á skýrsluskilgreiningarútliti biðlara (.rdlc- eða .rdl-skráargerðir). Þessi útlit eru búin til og þeim breytt með SQL Server Report Builder. Hönnun RDLC-útlits er svipað og Word útlits, þar sem útlitið tilgreinir almennt snið skýrslunnar og ákvarðar reitina sem á að taka með úr gagnamenginu. Hönnun RDLC-útlits er ítarlegra en Word-útlits.

## <a name="built-in-and-custom-report-layouts"></a>Innbyggt og sérsniðið skýrsluútlit
[!INCLUDE[d365fin](includes/d365fin_md.md)] inniheldur nokkur innbyggð útlit. Innbyggt útlit er skilgreint útlit hönnuð fyrir tilteknar skýrslur. [!INCLUDE[d365fin](includes/d365fin_md.md)] skýrslur eru með innbyggt útlit sem RDLC-skýrsluútlit, Word-skýrsluútlit eða, í sumum tilfellum, bæði. Ekki er hægt að breyta innbyggðu útliti úr [!INCLUDE[d365fin](includes/d365fin_md.md)] en þau eru notuð sem upphafspunktur til að búa til eigin sérsniðin skýrsluútlit.

Sérstillt útlit er skýrsluútlit sem þú hannar til að breyta útliti skýrslu. Þú býrð vanalega til sérsniðið útlit byggt á innbyggðu útliti, en þú getur búið þau til frá grunni eða úr afriti fyrirliggjandi sérsniðins útlits. Sérstillt útlit gera þér kleift að hafa mörg útlit fyrir sömu skýrsluna, sem hægt er að skipta á milli eftir þörfum. Til dæmis er hægt að hafa mismunandi útlit fyrir hvert [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrirtæki, eða hægt er að hafa mismunandi útlit fyrir sama fyrirtækið við tiltekin tilefni eða aðstæður, eins og sérstaka herferð eða hátíðir.

## <a name="deciding-whether-to-use-a-word-or-rdlc-report-layout"></a>Ákvörðun um hvort Word eða RDLC-skýrsluútlit er notað
Skýrsluútlit getur verið byggt á Word-skjali eða RDLC-skrá. Þegar ákvörðun er tekin um hvort nota eigi Word-skýrsluútlit eða RDLC-skýrsluútlit fer það eftir því hvernig skýrslan sem mynduð er á að líta út og þekkingu notanda á Word og SQL Server Report Builder.

Almenna hönnunin fyrir Word og RDLC-útlit eru mjög svipaðar. Hins vegar er hver gerð með tiltekin hönnunareinkenni sem hafa áhrif á það hvernig skýrslan sem mynduð er birtist í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þetta þýðir að sama skýrsla gæti litið mismunandi út eftir því hvort Word-skýrsluútlitið eða RDLC-skýrsluútlitið er notað.

Ferlið til að setja upp Word-skýrsluútlit og RDLC-skýrsluútlit á skýrslum er það sama. Helsti munurinn liggur í því hvernig útlitinu er breytt. Yfirleitt er auðveldara að búa til og breyta Word-skýrsluútliti en RDLC-útliti þar sem hægt er að nota Word. RDLC-skýrsluútlitum er breytt með SQL Server Report Builder sem ætlað er reyndari notendum.

Fyrir upplýsingar um hvernig eigi að breyta útliti, sjá [Hvernig á að breyta því hvaða útlit er notað á skýrslum](ui-how-change-layout-currently-used-report.md)

## <a name="see-also"></a>Sjá einnig
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Hvernig á að: Búa til sérsniðið skýrsluútlit eða skjalaútlit](ui-how-create-custom-report-layout.md)  
[Hvernig á að: Senda skjöl í tölvupósti](ui-how-send-documents-email.md)

