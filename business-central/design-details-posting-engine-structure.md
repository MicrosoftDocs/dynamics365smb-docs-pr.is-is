---
title: Hönnunarupplýsingar - Uppbygging bókunarvélar | Microsoft Docs
description: Bókunarviðmót og sumar aðrar aðgerðir í kóðaeiningu 12 nota aðgerðir bókunarvélar til að undirbúa og setja inn færslur í fjárhag og VKS. Bókunarvélin er einnig ábyrg fyrir stofnun fjárhags.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 3e49d9c521ebfb73caeae6987472c5123ab54eba
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185469"
---
# <a name="design-details-posting-engine-structure"></a>Hönnunarupplýsingar: Uppbygging bókunarvélar
Bókunarviðmót og sumar aðrar aðgerðir í kóðaeiningu 12 nota aðgerðir bókunarvélar til að undirbúa og setja inn færslur í fjárhag og VKS. Bókunarvélin er einnig ábyrg fyrir stofnun fjárhags.  
  
 Virknin í eftirfarandi töflu veitir staðlaðan ramma fyrir hönnun bókunarferla (t.d. Code, CustPostApplyCustledgEntry, VendPostApplyVendLedgEntry, UnapplyCustLedgEntry, UnapplyVendLedgEntry og Reverse) og einkaaðgang að töflu 17, fjárhagsfærslu.  
  
|Algengar aðgerðir|Description|  
|-------------|---------------------------------------|  
|StartPosting|Ræsir bókunarbiðminni TempGLEntryBuf, læsir fjárhagsfærslu og töflu VSK-færslu, og ræsir reikningstímabil, fjárhagsdagbók og gengi. Ætti að kalla aðeins á einu sinni, NextEntryNo er þá 0.|  
|ContinuePosting|Kannar og bókar óinnleystan VSK fyrir fyrri færslu eykur NextTransactionNo og undirbýr bókun næstu línu.|  
|FinishPosting|Lýkur bókun með því að setja inn fjárhagsfærslur úr tímabundnu skyndimynni í gagnagrunnstöflu. Alltaf notað ásamt StartPosting. Leita að ósamræmi.|  
|InitGLEntry|Notað til að ræsa nýja fjárhagsfærslu fyrir Almenna færslubókarlínu. Skilar GLEntry sem færibreytu.|  
|InitGLEntryVAT|Sama og InitGLEntry en úthlutar einnig Mótreikningur nr. og SummarizeVAT.|  
|InitGLEntryVATCopy|Svipað InitGLEntryVAT, en afritar einnig bókunarflokksgögn úr VSK-færslu fyrir SummarizeVAT.|  
|InsertGLEntry|Eina virknin sem setur fjárhagsfærslu inn í altæka TempGLEntryBuf töflu. Notaðu alltaf þennan virkni til að setja inn.|  
|CreateGLEntry|Framkvæmir InitGLEntry, úthlutar Viðbótarupphæð gjaldmiðils og framkvæmir svo InsertGLEntry. Skiptir út nokkrum línum af kóða fyrir eina virkni.|  
|CreateGLEntryBalAcc|Sasma og CreateGLEntry, en tengir einnig Gerð mótreiknings og Númer mótreiknings.|  
|CreateGLEntryVAT|Sama og CreateGLEntry, en með viðbótarferli fyrir bókun flokka og vistunar í tímabundið VSK-biðminni:<br /><br /> `GLEntry.CopyPostingGroupsFromDtldCVBuf(DtldCVLedgEntryBuf,GenJnlLine."Gen. Posting Type");`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryVATCollectAdj|Sama og CreateGLEntry, en með viðbótarsafni stillinga og vistunar í tímabundið VSK-biðminni:<br /><br /> `CollectAdjustment(AdjAmount,GLEntry.Amount,GLEntry."Additional-Currency Amount",OriginalDateSet);`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryFromVATEntry|Sama og CreateGLEntry, en afritar einnig bókunarflokka úr VSK-færslu.|  
  
## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: Uppbygging bókunarviðmóts](design-details-posting-interface-structure.md)