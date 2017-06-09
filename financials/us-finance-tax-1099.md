---
title: "Skráning 1099 færslna í Bandaríkjunum | Microsoft Docs"
description: "Á innkaupaskjölunum er hægt að tilgreina að skjalið gildi fyrir 1099 og hægt er að tilgreina 1099-kóðann fyrir lánardrottinninn."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a0a31c28b6c96dc80593ac3862b97b36c3ec81c7
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="reporting-1099-transactions-in-the-us"></a>Skráning 1099 færslna í Bandaríkjunum
Skattstofan krefst einnar eða fleiri útgáfa af 1099 skattaskýrslunni fyrir greiðslur til lánardrottna. Senda verður afrit af þessum eyðublöðum til lánardrottna árlega á eða fyrir síðasta dag janúar. Á innkaupaskjölunum er hægt að tilgreina að skjalið gildi fyrir 1099 og hægt er að tilgreina 1099-kóðann fyrir lánardrottinninn.  

## <a name="1099-codes"></a>1099-kóðar
Í [!INCLUDE[d365fin](includes/d365fin_md.md)] eru algengustu 1099 númerin nú þegar sett upp fyrir þig svo þú ert tilbúin til að búa til nauðsynlegar skýrslur. Kóðarnir eru skilgreindir í glugganum **Eyðublaðsreitur IRS 1099** þar sem einnig er hægt að bæta við nýjum 1099-kóðum. Fyrir hvern lánardrottin sem standa þarf skil á sköttum er svo hægt að tilgreina viðeigandi 1099-kóða á flýtiflipanum **Greiðslur** á spjaldi lánardrottinsins.  

Með skýrslunni **1099-upplýsingar lánardrottins** er hægt að skoða 1099-færslur sem voru greiddar á tilteknum tíma. Við lok ársins er hægt að prenta 1099-færslur á forprentuðum eyðublöðum.  

## <a name="printing-1099-tax-forms"></a>Prentun 1099-skattaskýrslna
Í glugganum **Eyðublaðsreitur IRS 1099** fæst aðgangur að eftirfarandi skattaskýrslum:  

* Lánardrottinn 1099 Div  

  Prentar landsbundna eyðublaðið 1099-DIV fyrir arðgreiðslur og útgreiðslu. Hægt er að prenta út öll eða tilgreind 1099-DIV eyðublöð. Skýrslan notar kóðana sem gilda um upphæðareitina á DIV-eyðublaðinu úr glugganum **Eyðublaðsreitur IRS 1099**.  
* Lánardrottinn 1099 Int  

  Prentar landsbundna eyðublaðið 1099-INT fyrir vaxtatekjur. Hægt er að prenta út öll eða tilgreind 1099-INT eyðublöð. Skýrslan notar kóðana sem gilda um upphæðareitina á INT-eyðublaðinu úr glugganum **Eyðublaðsreitur IRS 1099**.  
* Lánardrottinn 1099 Misc – ýmsar tekjur  

  Prentar landsbundna eyðublaðið 1099-MISC fyrir ýmsar tekjur. Hægt er að prenta út öll eða tilgreind 1099-MISC eyðublöð. Skýrslan notar kóðana sem gilda um upphæðareitina á MISC-eyðublaðinu úr glugganum **Eyðublaðsreitur IRS 1099**.  

Stjórnsýslubreytingar sem hafa áhrif á þessa skýrslu og töflugögn eru almennt meðhöndluð í árslokauppfærslum.
Það getur komið að gagni að keyra skýrsluna **1099-upplýsingar lánardrottins** til að fara yfir gögnin áður en eyðublöðin eru prentuð út.

## <a name="submitting-1099-tax-forms-electronically"></a>1099-skattaskýrslur lagðar fram rafrænt
Til að leggja fram 1099-skattaskýrslurnar rafrænt skal nota skýrsluna **1099-segulmiðlun lánardrottins**. Tilgreinir 1099-eyðublöðin sem hægt er að flytja út. Eyðublaðaupplýsingarnar sem eru fluttar út í þessari skýrslu eru þær sömu og í skýrslunum sem prenta 1099-eyðublöð sem er lýst í fyrri hluta.  

Skýrslan notar kóðana sem gilda um upphæðareitina á eyðublaðinu úr glugganum **Eyðublaðsreitur IRS 1099**. Kóðunum er varpað í eyðublaðsreitina í skráarútlitum þessarar skýrslu og því verða töflugögnin og skýrsluútgáfan fyrir tiltekið skattaár að passa saman. Ef einhverjum sérsniðnum kóðum er bætt við töfluna verður að varpa þeim í eyðublaðsreitina inni í þessum hlut.  

Stjórnsýslubreytingar sem hafa áhrif á þessa skýrslu og töflugögn eru almennt meðhöndluð í árslokauppfærslum.
Það getur komið að gagni að keyra skýrsluna **1099-upplýsingar lánardrottins** til að fara yfir gögnin áður en rafræna skráin er mynduð.  

## <a name="see-also"></a>Sjá einnig
[Hvernig á að Skrá nýja lánardrottna](purchasing-how-register-new-vendors.md)  
[Hvernig á að skrá innkaup](purchasing-how-record-purchases.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

