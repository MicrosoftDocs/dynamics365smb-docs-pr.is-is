---
title: "Skilyrði til að millifærslu fjárhagsfærslna í kostnaðarfærslur | Microsoft Docs"
description: "Mikilvægt er að átta sig á skilyrðum fyrir því að flytja fjárhagsfærslur til kostnaðarfærslna. Meðan á millifærslu stendur notar runuvinnslan **Millifæra fjárhagsfærslu til kostnaðarbókhalds** eftirfarandi skilyrði til að tilgreina hvort og hvernig fjárhagsfærslur eru fluttar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b1ac9d3d0ab7022d5a11ad1642cf496d07bc81ce
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a>Skilyrði til að millifærslu fjárhagsfærslna í kostnaðarfærslur
Mikilvægt er að átta sig á skilyrðum fyrir því að flytja fjárhagsfærslur til kostnaðarfærslna. Meðan á millifærslu stendur notar runuvinnslan **Millifæra fjárhagsfærslu til kostnaðarbókhalds** eftirfarandi skilyrði til að tilgreina hvort og hvernig fjárhagsfærslur eru fluttar.  

Fjárhagsfærslur eru fluttar ef:  

-   Færslurnar hafa víddargildi sem samsvara annaðhvort kostnaðarstað eða kostnaðarhlut.  
-   Færslurnar hafa víddargildi sem samsvara kostnaðarstað og kostnaðarhlut. Kostnaðarstaðurinn hefur forgang í þessum færslum. Þetta hjálpar til við að forðast aðstæður þar sem kostnaðargerð birtist í bæði kostnaðarhlut og kostnaðarstað og er því talin tvisvar í tölfræðigögnum.  
-   Fylgiskjalsnúmerið í færslunum er autt, þannig að það birtist með fylgiskjalsnúmerinu 0000 í kostnaðarfærslunum.  
-   Færslurnar eru færðar í kostnaðartegund sem leyfir við blandaðar færslur og þessar færslur eru fluttar sem blönduð færsla, annaðhvort mánaðarlega eða daglega.  

Fjárhagsfærslur eru ekki fluttar ef:  

-   Færslurnar hafa víddargildi sem samsvara ekki kostnaðarstað né kostnaðarhlut.  
-   Færslurnar hafa upphæð núll.  
-   Færslurnar hafa fjárhagsreikning sem hefur verið eytt.  
-   Færslurnar hafa fjárhagsreikning sem er ekki af tegundinni **Rekstrarreikningur**.  
-   Færslurnar hafa fjárhagsreikning sem er ekki tengdur kostnaðartegund.  
-   Færslurnar hafa bókunardagsetningu fyrir **Upphafsdagsetning fjárhagsmillifærslu**.  
-   Færslurnar hafa verið bókaðar með lokadagsetningu. Þetta eru yfirleitt færslur sem stilla aftur stöðu rekstrarreiknings við lok hvers árs.  

## <a name="see-also"></a>Sjá einnig  
[Kostnaðarreikningur](finance-manage-cost-accounting.md)  
 [Flytja fjárhagsfærslur í kostnaðarfærslur](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Flytja og bóka kostnaðarfærslur](finance-transfer-and-post-cost-entries.md)   
 [Um kostnaðarbókhald](finance-about-cost-accounting.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

