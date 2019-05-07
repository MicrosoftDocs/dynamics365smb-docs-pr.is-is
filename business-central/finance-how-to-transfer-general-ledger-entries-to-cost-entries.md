---
title: Hvernig á að flytja fjárhagsfærslur í kostnaðarfærslur | Microsoft Docs
description: Hægt er að flytja fjárhagsfærslur í kostnaðarfærslur
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: a33fb434cc239de951d18783911c879587a3ace0
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2019
ms.locfileid: "939035"
---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Flytja fjárhagsfærslur í kostnaðarfærslur
Hægt er að flytja fjárhagsfærslur í kostnaðarfærslur  

Áður en ferlið til að flytja fjárhagsfærslur til kostnaðarfærslna er keyrt, þarf að undirbúa flutninginn til að forðast handvirka leiðréttingarbókun.  

## <a name="to-prepare-the-transfer"></a>Til að undirbúa færsluna  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning kostnaðarbókahalds** og veldu síðan tengda tengilinn.  
2.  Á síðunni **Uppsetning kostnaðarbókhalds** skal ganga úr skugga um að reiturinn **Upphafsdagur fyrir fjárhagsfærslur** sé stilltur á rétt gildi.  
3.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Myndrit yfir kostnaðargerðir** og veldu síðan tengda tengilinn.  
4.  Á síðunni **Kostnaðargerðarspjald** skal ganga úr skugga um að reiturinn **Fjárhagsreikningssvið** sé tengdur rétt þannig að hver kostnaðargerð taki færslur úr fjárhag.  
5.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **bókhaldslykill** og veldu síðan tengda tengilinn.  
6.  Fyrir hvern viðeigandi fjárhagsreikning, á síðunni **Fjárhagsreikningsspjald**, skal sannreyna að reiturinn **Kostnaðargerð nr.** sé rétt tengdur í kostnaðartegund. Nánari upplýsingar er að finna í [Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md).  
7.  Staðfesta að allar viðeigandi fjárhagsfærslur hafa víddargildi sem samsvara kostnaðarstað og kostnaðarhlut.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Til að færa fjárhagsfærslur yfir í kostnaðarfærslur  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Flytja fjárhagsfærslur til vottorðaútgefanda** og veldu síðan tengda tengilinn.  
2.  Velja hnappinn **Já** til að hefja millifærsluna. Ferlið færir allar fjárhagsfærslur sem hafa ekki þegar verið færðar.  

    Meðan á millifærslu stendur býr ferlið til tengingar í færslurnar í töflunni **Kostnaðarfærsla** og töflunni **Kostnaðarskráning**. Þannig er hægt að rekja uppruna kostnaðarfærsla.  

## <a name="see-also"></a>Sjá einnig  
[Flytja og bóka kostnaðarfærslur](finance-transfer-and-post-cost-entries.md)   
[Uppsetning kostnaðarbókhalds](finance-set-up-cost-accounting.md)   
