---
title: "Yfirlit yfir víddasamstæðufærslur | Microsoft Docs"
description: "Í þessu efnisatriði er lýst hvernig víddasamstæðufærslur eru geymdar og bókaðar í Dynamics 365."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 78e98bcbc88ffb38d5da3f5089d124d915585d91
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="dimension-set-entries-overview"></a>Yfirlit yfir víddasamstæðufærslur
Í þessu efnisatriði er lýst hvernig víddasamstæðufærslur eru geymdar og bókaðar í [!INCLUDE[d365fin](includes/d365fin_md.md)].  
  
## <a name="dimension-sets"></a>Víddasamstæður  
Víddasamstæða er sérstök samsetning víddargilda. Er vistað sem víddasamstæðufærslur í gagnagrunninum. Hver víddasamstæðufærsla stendur fyrir eitt víddargildi. Víddasamstæðan er auðkennd með algengum víddasamstæðukennum sem eru úthlutuð hverri víddasamstæðufærslu sem tilheyrir víddasamstæðunni.  
  
Eftirfarandi dæmi sýnir víddasamstæðu sem hefur þrjár víddasamstæðufærslur. Víddasamstæðan er auðkennd með víddasamstæðukenni, sem er 108.  
  
|Auðkenni víddasamstæðu|Víddarkóti|Gildiskóti víddar|Nafn víddagildis|  
|----------------------|--------------------|--------------------------|--------------------------|  
|108|SVÆÐI|70|Norður Ameríka|  
|108|ATVGRHÓPUR|HOME|Heimili|  
|108|DEILD|SALA|Sala|  
  
## <a name="dimension-set-entries"></a>Víddasamstæðufærslur  
Víddasamstæður eru geymdar í töflunni **Víddasamstæðufærsla** sem víddasamstæðufærslur með sama víddasamstæðukenni.  
  
![Víddafærsluryfirlit](media/dimensionentrynav7.png "DimensionEntryNAV7")  
  
Þegar ný færslubókarlína, skjalahaus eða skjalalína er stofnuð er hægt að tilgreina samsetningu víddargilda. Í stað þess að geyma hvert víddargildi í gagnagrunninum er kenni víddasamstæðu tengt færslubókarlínu, haus skjals eða línu skjals til að tilgreina víddasamstæðuna.  
  
Þegar glugganum **Breyta Víddasamstæðufærslum** er breytt og lokað er gerð athugun til að sjá hvort samsetning víddargildanna sé til sem víddasafn í töflunni. Ef samsetningin kemur fyrir í töflunni er samsvarandi víddasamstæðukenni tengt við færslubókarlínuna, fylgiskjalshausinn eða fylgiskjalslínuna. Annars er nýrri víddasamstæðu bætt við töfluna og henni hennar bætt við línu færslubókar, haus fylgiskjals eða línu fylgiskjals.  
  
## <a name="performance-improvement"></a>Bætt afköst  
Með því að vista víddasamstæður einu sinni í gagnagrunni, er gagnagrunnsbilinu haldið við og heildarafköst eru bætt.  
  
## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar Leitað að víddarsamsetningum](design-details-searching-for-dimension-combinations.md)   
[Hönnunarupplýsingar töfluuppbygging](design-details-table-structure.md)   
[Hönnunarupplýsingar: Codeunit 408 víddarstjórnun](design-details-codeunit-408-dimension-management.md)   
[Hönnunarupplýsingar: Kóðadæmi um breytt mynstur í Breytingar](design-details-code-examples-of-changed-patterns-in-modifications.md)   
[Hönnunarupplýsingarn: Færslur víddarsamstæða](design-details-dimension-set-entries.md)   

