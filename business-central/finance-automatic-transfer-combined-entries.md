---
title: "Sjálfvirkur flutningur og sameinaðar færslur | Microsoft Docs"
description: "Í kostnaðarbókhaldi er hægt að flytja fjárhagsfærslur í tegund kostnaðar með því að nota blandaða bókun. Þú getur tilgreint það ef kostnaðargerð fær sameinaðar færslur í reitinn **Sameinaðar færslur** í skilgreiningunni á kostnaðargerð. Eftirfarandi tafla lýsir hinum mismunandi valkostum."
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
ms.openlocfilehash: 4f1bcf009b397438bb302a16a23be2f4638cefc4
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="automatic-transfer-and-combined-entries"></a>Sjálfvirkur flutningur og færslur sameinaðar
Í kostnaðarbókhaldi er hægt að flytja fjárhagsfærslur í tegund kostnaðar með því að nota blandaða bókun. Þú getur tilgreint það ef kostnaðargerð fær sameinaðar færslur í reitinn **Sameinaðar færslur** í skilgreiningunni á kostnaðargerð. Eftirfarandi tafla lýsir hinum mismunandi valkostum.  

|Sameina færslur|Lýsing|  
|---------------------|-----------------|  
|Ekkert|Hver fjárhagsfærsla er flutt sérstaklega í samsvarandi kostnaðartegund.|  
|Dagur|Fjárhagsfærslur með sömu bókunardagsetningu eru fluttar sem ein færsla í samsvarandi tegund kostnaðar.|  
|Mánuður|Allar fjárhagsfærslur í sama almanaksmánuði eru fluttar sem ein færsla í samsvarandi tegund kostnaðar.|  

> [!IMPORTANT]  
>  Ef gátreiturinn **Sjálfvirk færsla úr fjárhag** er valinn í glugganum **Uppsetning kostnaðarbókhalds**, uppfærir [!INCLUDE[d365fin](includes/d365fin_md.md)] kostnaðarbókhaldið eftir hverja bókun í fjárhag. Sameinaðar færslur eru ekki mögulegar.  

## <a name="see-also"></a>Sjá einnig  
 [Flytja fjárhagsfærslur í kostnaðarfærslur](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Skilyrði til að millifærslu fjárhagsfærslna í kostnaðarfærslur](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
 [Niðurstöður millifærslu](finance-results-of-the-transfer.md)   
 [Flytja og bóka kostnaðarfærslur](finance-transfer-and-post-cost-entries.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

