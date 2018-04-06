---
title: "Hvernig á að flytja fjárhagsfærslur í kostnaðarfærslur | Microsoft Docs"
description: "Hægt er að flytja fjárhagsfærslur í kostnaðarfærslur"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cd52387ec1396164f6da1b87a2a97227901df592
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a>Flytja fjárhagsfærslur í kostnaðarfærslur
Hægt er að flytja fjárhagsfærslur í kostnaðarfærslur  

Áður en ferlið til að flytja fjárhagsfærslur til kostnaðarfærslna er keyrt, þarf að undirbúa flutninginn til að forðast handvirka leiðréttingarbókun.  

## <a name="to-prepare-the-transfer"></a>Til að undirbúa færsluna  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Uppsetning kostnaðarbókhalds** og velja svo viðeigandi tengil.  
2.  Í glugganum **Uppsetning kostnaðarbókhalds** skal ganga úr skugga um að reiturinn **Upphafsdagur fyrir fjárhagsfærslur** sé stilltur á rétt gildi.  
3.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Myndrit yfir kostnaðartegundir** og velja svo viðeigandi tengil.  
4.  Í glugganum **Kostnaðargerðarspjald** skal ganga úr skugga um að reiturinn **Fjárhagsreikningssvið** sé tengdur rétt þannig að hver kostnaðargerð taki færslur úr fjárhag.  
5.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bókhaldslykill** og velja svo viðeigandi tengil.  
6.  Fyrir hvern viðeigandi fjárhagsreikning, í glugganum **Fjárhagsreikningsspjald**, skal sannreyna að reiturinn **Kostnaðargerð nr.** sé rétt tengdur í kostnaðartegund. Frekari upplýsingar, sjá [Skilgreining á venslum milli kostnaðargerða og fjárhagsreikninga](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).  
7.  Staðfesta að allar viðeigandi fjárhagsfærslur hafa víddargildi sem samsvara kostnaðarstað og kostnaðarhlut.  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a>Til að færa fjárhagsfærslur yfir í kostnaðarfærslur  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Flytja fjárhagsfærslur í kostanaðarbókhald** og velja svo viðeigandi tengil.  
2.  Velja hnappinn **Já** til að hefja millifærsluna. Ferlið færir allar fjárhagsfærslur sem hafa ekki þegar verið færðar.  

    Meðan á millifærslu stendur býr ferlið til tengingar í færslurnar í töflunni **Kostnaðarfærsla** og töflunni **Kostnaðarskráning**. Þannig er hægt að rekja uppruna kostnaðarfærsla.  

## <a name="see-also"></a>Sjá einnig  
 [Skilyrði til að millifærslu fjárhagsfærslna í kostnaðarfærslur](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Sjálfvirkur flutningur og færslur sameinaðar](finance-automatic-transfer-combined-entries.md)   
 [Niðurstöður millifærslu](finance-results-of-the-transfer.md)   
 [Flytja og bóka kostnaðarfærslur](finance-transfer-and-post-cost-entries.md)   
 [Skilgreining á venslum milli kostnaðargerða og fjárhagsreikninga](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

