---
title: "Víddir | Microsoft Docs"
description: "Nota víddir til að greina gögn."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/24/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7552ee2b3398c203a7f3295f3203c83914fbb15f
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="dimensions"></a>Víddir
Til að auðvelda greiningu á skjölum, svo sem sölupöntum, geturðu notað stærðir. Víddir eru eiginleikar og gildi sem flokkar færslur svo þú getir fylgst með og greina þær. Til dæmis má vísa til verkefnisins eða deildarinnar sem innganga kom frá.  

Til dæmis, í stað þess að setja upp sérstaka aðalbókarreikninga fyrir hverja deild og verkefni, getur þú notað stærðir. Þetta gefur mikið tækifæri til greininga án þess að búa til flókið kort af reikningum.  

Annað dæmi er að setja upp vídd sem kallast *Deild* og nota þá vídd þegar þú bókar söluskjöl. Þetta mun leyfa þér að nota viðskipti upplýsingaöflun tól til að sjá hvaða deild selt hvaða atriði.
Því fleiri stærðir sem þú notar, nákvæmari skýrslurnar sem þú getur byggt á viðskiptatengslunum þínum. Til dæmis getur einn sölutilgangur innihaldið upplýsingar um marga vídd, svo sem:  

* Reikningurinn sem vörusalan var sendur til  
* Þar sem hluturinn var seldur
* Hver seldi það
* Tegund viðskiptavina sem keypti hana  

Þú getur búið til eins mörg mál með eins mörgum gildum og þú vilt.  

**Athugið**: Þessi virkni krefst að upplifun þín er stilltur á **Pakki**. Nánari upplýsingar, sjá [Sérstilli þína [!INCLUDE[d365fin](includes/d365fin_md.md)]upplifun](ui-experiences.md).

## <a name="using-dimensions"></a>Notkun vídda
Í skjalinu eins og sölupöntun, er hægt að bæta við víddaupplýsingum fyrir bæði einstaka fylgiskjalslínu og skjalið sjálft. Til dæmis, í **Sölupöntun** glugganum getur þú slegið inn víddarmörk fyrir fyrstu tvær flýtivísanirnar á einstökum sölulínum og þú getur bætt við stærri víddarupplýsingum ef þú velur hnappinn **Víddir**.  

Ef þú vinnur í dagbók í staðinn geturðu bætt við víddargögn við færslu á sama hátt ef þú hefur sett upp flýtileiðarmörk sem reitir beint á blaðalínum.  

Hægt er að setja upp sjálfgefnar víddir fyrir reikninga eða reikningstegundir, svo að víddir og víddargildi eru fyllt út sjálfkrafa.  

## <a name="dimension-sets"></a>Víddasamstæður
Víddasamstæða er sérstök samsetning víddargilda. Er vistað sem víddasamstæðufærslur í gagnagrunninum. Hver víddasamstæðufærsla stendur fyrir eitt víddargildi. Víddasamstæðan er auðkennd með algengum víddasamstæðukennum sem eru úthlutuð hverri víddasamstæðufærslu sem tilheyrir víddasamstæðunni.  

Þegar þú býrð til dagbókarlínu, skjalhaus eða skjalastiku, getur þú tilgreint samsetningu af víddarmörkum. Í stað þess að geyma hvert víddargildi í gagnagrunninum er kenni víddasamstæðu tengt færslubókarlínu, haus skjals eða línu skjals til að tilgreina víddasamstæðuna.  

## <a name="see-also"></a>Sjá einnig
[Fjármál](finance.md)  
[Uppsetning vídda](finance-setup-dimensions.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

