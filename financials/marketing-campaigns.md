---
title: "Setja upp markaðsherferðir í fjármálum | Microsoft Docs"
description: "Lýsir hvernig hægt er að setja upp og stunda markaðssetninguherferðir í Dynamics 365 for Financials"
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 03/08/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8f616382e28e29aab1ce7d9b45b8efb4ad374b96
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="managing-marketing-campaigns"></a>Stjórnun markaðsherferða
Öflug markaðsáætlun gerir fyrirtækinu kleift að finna, vinna og halda viðskiptamönnum. Markaðsáætlun samanstendur af ýmsum söluherferðum og öðrum samskiptum í tengslum við sölur og markaðssetningaraðgerðir. Þegar söluherferð er skipulögð þarf að ákveða hvaða tengiliði skal miða á, hvaða gerð söluherferðar (t.d. vörusýningu eða beinan auglýsingapóst) skal nota og hvaða sölumen munu framkvæma hvert verk.

<!-- Each campaign consists of various activities or to-dos. Activities are large tasks that can be broken down into several smaller tasks or to-dos. To-dos are individual or team tasks that can be created within activities or individually and then be assigned to individual salespeople or groups of salespeople.-->

## <a name="defining-individual-campaigns"></a>Skilgreina stakar söluherferðir
Áður en herferð er stofnuð þarf að setja upp *stöðukóða herferðar*. Notkun þessara kóta hjálpar til við stjórnun herferða með því að úthluta herferðum stöðu. Þegar unnið er gegnum þrep herferðar er hægt að sjá á hvaða þrepi herferðin er og hvaða þrep kemur næst. Þú setur upp stöðuherferðarkóða í glugganum **Staða herferðar**.

Þú getur búið til *herferðarkort* fyrir hvern herferð sem þú vilt halda utan um. Einnig er hægt að skoða þessi herferðarspjöld til að fá almennar upplýsingar um herferðirnar.
Þú getur eytt herferðarpósta, svo sem ef færslan skráir aðgerð sem hefur verið lokað. Aðeins er hægt að eyða ógiltum söluherferðarfærslum.

### <a name="selecting-the-target-audience"></a>Val á markhópi
Þegar herferð hefur verið stofnuð er hægt að byrja að stofna hluta þar sem tilgreindir eru viðtakendur herferðar. Nánari upplýsingar er að finna í [Umsjón hluta](marketing-segments.md).

### <a name="registering-discount-percentages"></a>Skráning afsláttarprósentu
Þegar lokið er við að setja upp söluherferð, ákveða hvaða hluta á að höfða til með herferðinni og velja upphafs- og lokadagsetningu, er afsláttarprósenta sem viðskiptamaður fær af einstaka vörum skráð í línum í glugganum **Sölulínuafslættir**. Þú getur einnig skráð söluverð fyrir einstök atriði á línurnar í **Söluverð** gluggans. Þú getur opnað báða glugga frá söluherferðarkortinu.

 Þegar söluverð/línuafsláttur og hlutarnir á söluherferðarspjaldinu hafa verið settir upp þarf að virkja þá til þess að verð/afsláttur í söluherferð komi fram í línunum.

> [!NOTE]  
>  Til þess að virkja söluverð / lína afslætti verður þú að tilgreina hvort allt hlutinn eða aðeins nokkrir tengiliðir eru markmið herferðarinnar. Ef söluverðið/línuafslátturinn nær yfir alla tengiliðina í hlutanum reiturinn **Markhópur söluherferðar** valinn á flýtiflipanum **Söluherferð** á spjaldinu **Hluti**.
Ef ekki er boðið upp á söluverð / lína afslátt fyrir alla tengiliðina í hlutanum geturðu hreinsað **herferðarmarkið** fyrir viðkomandi tengiliði. Ef þú getur ekki séð þetta reit geturðu bætt því við skoðunina þína. Nánari upplýsingar er að finna í [Sérstillingar notanda](ui-user-personalization.md).

<!-- ## Conducting campaigns
As a campaign runs, all interactions with your contacts, or segment, are recorded so that you can get statistics and other information about the costs and success rates of the campaign.

Campaigns are conducted by salespeople, and you must create activities to represent each task and assign them to the relevant salespeople.  -->

## <a name="see-also"></a>Sjá einnig
[Vinna með tengiliði](marketing-contacts.md)  
[Umsjón hluta](marketing-segments.md)  
[Umsjón sölutækifæra](marketing-manage-sales-opportunities.md)  
[Unnið með Financials](ui-work-product.md)  

