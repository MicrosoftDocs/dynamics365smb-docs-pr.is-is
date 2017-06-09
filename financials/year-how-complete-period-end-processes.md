---
title: "Lokunartímabil | Microsoft Docs"
description: "Útskýrir ferli sem þarf að ljúka til að loka tímabili."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 03/21/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 1d0af3dbc94c32447facfbd24747ddc140cc1691
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="closing-periods"></a>Lokunartímabil
[!INCLUDE[d365fin](includes/d365fin_md.md)] þvingar þig ekki til að loka tímabilum, en það eru margar aðgerðir í lokunartíma (lok mánaðar) sem þú getur gert. Þetta efni gefur yfirlit yfir valfrjáls ferli og starfsemi fyrir lokunartímabil.  

## <a name="general-ledger"></a>Fjárhagur
* Tilgreindu kerfisbundið og notendasértækt bókunartímabil.  

    Þetta tilgreinir dagsetningar þar sem hægt er að bóka. Þú gætir viljað leyfa bókun í byrjun tímabilsins eða í lok tímabilsins, allt eftir fyrirtækinu. Nánari upplýsingar eru í [Hvernig á að tilgreina bókunartímabil](finance-how-specify-posting-periods.md).  
* Allar nauðsynlegar fjárhagsleiðréttingar eru framkvæmdar.  
* Ítrekunarbækur eru uppfærðar og bókaðar.  
  <!--* Process Consolidations-->
* Fjárhagsskema keyrt sem hér segir:  
  * Glugginn **Fjárhagsskema** er opnaður og smellt á aðgerðina **Prenta**.  

## <a name="sales-and-receivables"></a>Sala and útistandandi
* Allar sölupantanir, reikningar, kreditreikningar og vöruskilapantanir eru bókaðar.  
* Inngreiðslubókin er bókuð.  
* Uppfæra og birta bækur tímarit sem tengjast sölu og útistandandi.  
* Afstemma viðskiptakröfur við færslubók.  
* Runuvinnslan **Eyða reikningsf. sölupöntunum** er keyrð.  

## <a name="purchases-and-payables"></a>Innkaup og viðskiptaskuldir
* Allar pantanir, reikningar, kreditreikningar og vöruskilapantanir eru bókaðar.  
* Allar greiðslubækur eru bókaðar.  
* Ítrekunarfærslubækur tengdar innkaupum og viðskiptaskuldum eru uppfærðar og bókaðar.  
* Skýrslan **Aldursgreindar skuldir** er keyrð og skuldir stemmdar af við fjárhaginn.  
* Runuvinnslan **Eyða reikningsf. innk.pöntunum** er keyrð.  

<!-- ### Fixed Assets
* Post all maintenance costs have been posted through the fixed asset journals or invoices.
* Post adjustments.
* Post appreciation.
* Post depreciation.
* Update and post the recurring fixed asset journal.-->

<!--### Intercompany
* Process Intercompany Postings.-->

## <a name="calculate-and-process-sales-tax"></a>VSK er reiknaður og unninn
* Lokið er við skattyfirlit.  

## <a name="see-also"></a>Sjá einnig
[Lokaár og Tímabil](year-close-years-periods.md)  
[Bókum lokað](year-close-books.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

