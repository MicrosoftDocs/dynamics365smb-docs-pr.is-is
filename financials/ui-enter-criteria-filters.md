---
title: "Skilyrði í afmörkunum | Microsoft Docs"
description: "Lærðu hvernig síur vinna í fjármálum."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1a94e2ead59a40081920a0b11ed545a895d89910
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="entering-criteria-in-filters"></a>Afmörkun skjalanna
Til að leita að gögnum, svo sem heiti viðskiptamanna, aðsetrum eða vöruhópum er hægt að setja inn skilyrði. Í leitarskilyrðum er hægt að nota alla sömu tölustafi og bókstafi sem venjulega eru notaðir í reitnum. Ennfremur er hægt að nota sértákn til að afmarka niðurstöðurnar frekar.

## <a name="searching-using-the-quick-filter"></a>Leita með því að nota flýtiafmörkun
Hægt er að bæta afmörkunum við allar síður með því að nota flýtiafmörkun. Flýtiafmörkun er virkjuð með því að velja stækkunarglerstáknið í efra hægra horni síðu. Þessi síugerð er notuð fyrir flýtiinnfærslu viðmiða.

**Mikilvægt**: Flýtiafmörkun veitir auðveldan aðgang að afmörkunargögnum með því að færa inn texta án sniðtákna en veitir einnig margs konar valkosti fyrir leitarskilyrði. Það fer eftir því hvort þú slærð texta eða texta með táknum, flýtiafmörkun hagar sér öðruvísi.  

* Ef ósniðinn texti er sleginn inn í leitarskilyrðum eru leitarskilyrðin túlkuð sem leit óháð há- og lágstöfum sem inniheldur ákveðinn texta.  
* Ef texti með táknum er sleginn inn í leitarskilyrðum eru leitarskilyrðin túlkuð nákvæmlega eins og þau voru slegin inn og leitin er háð há- og lágstöfum.

### <a name="quick-filter-criteria"></a>Skilyrði flýtiafmörkunar
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH>Leitarskilyrði</TH>
    <TH>Túlkað sem...</TH>
    <TH>Vöruskil...</TH>
  </TR>
  <TR>
    <TD>man</TD>
    <TD>@&#42;man&#42;</TD>
    <TD>Allar færslur þurfa að innihalda textann <b>man</b> og rétta há- og lágstafi.</TD>
  </TR>
  <TR>
    <TD>se</TD>
    <TD>@&#42;se&#42;</TD>
    <TD>Allar færslur þurfa að innihalda textann <b>se</b> og rétta há- og lágstafi.</TD>
  </TR>
  <TR>
    <TD>Man&#42;</TD>
    <TD>Hefst á <b>Man</b> og greinarmunur á litlum og stórum stöfum.</TD>
    <TD>Allar færslur sem byrja á textanum <b>Man</b></TD>
  </TR>
  <TR>
    <TD>‚man‘</TD>
    <TD>Nákvæmur texti og greinarmunur á litlum og stórum stöfum.</TD>
    <TD>Allar færslur sem samsvara <b>man</b> nákvæmlega.</TD>
  </TR>
  <TR>
    <TD>@man* </TD>
    <TD>Hefst á og enginn greinarmunur á litlum og stórum stöfum.</TD>
    <TD>Allar færslur sem byrja á <b>man</b>.</TD>
  </TR>
    <TR>
    <TD>@&#42;man</TD>
    <TD>Lýkur á og enginn greinarmunur á litlum og stórum stöfum.</TD>
    <TD>Allar færslur sem enda á <b>man</b>.</TD>
  </TR>
</TABLE>

**Athugasemd**: Ekki er hægt að nota algildisstafi þegar afmarkanir eru á tölusettum reitum, til dæmis reiturinn **Staða** á sölupöntunum. Til að færa inn afmörkun fyrir þessa gerð reits, er hægt að færa inn númeragildið sem afmörkunarbreytu. Til dæmis í reitnum **Sala** á sölupöntun sem hafa gildin **Opin**, **Útgefið**, **Samþykkt í bið** og **Fyrirframgreiðsla í bið** skal nota gildin **0**, **1**, **2** og **3** til þess að afmarka þessa valmöguleika.  

## <a name="see-also"></a>Sjá einnig
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

