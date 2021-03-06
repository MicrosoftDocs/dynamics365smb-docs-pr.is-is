---
title: Yfirlit yfir víddasamstæðufærslur | Microsoft Docs
description: Í þessu efnisatriði er lýst hvernig víddasamstæðufærslur eru geymdar og bókaðar í Dynamics 365.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: c6e3df748269e2f40e3acf0a28ce0f6bc48ca944
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215304"
---
# <a name="dimension-set-entries-overview"></a>Yfirlit yfir víddasamstæðufærslur
Í þessu efnisatriði er lýst hvernig víddasamstæðufærslur eru geymdar og bókaðar í [!INCLUDE[prod_short](includes/prod_short.md)].  

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

![Flæði víddasamstæðufærslna](media/dimensionentrynav7.png "Flæði víddasamstæðufærslna")  

Þegar ný færslubókarlína, skjalahaus eða skjalalína er stofnuð er hægt að tilgreina samsetningu víddargilda. Í stað þess að geyma hvert víddargildi í gagnagrunninum er kenni víddasamstæðu tengt færslubókarlínu, haus skjals eða línu skjals til að tilgreina víddasamstæðuna.  

Þegar síðunni **Breyta Víddasamstæðufærslum** er breytt og lokað er gerð athugun til að sjá hvort samsetning víddargildanna sé til sem víddasafn í töflunni. Ef samsetningin kemur fyrir í töflunni er samsvarandi víddasamstæðukenni tengt við færslubókarlínuna, fylgiskjalshausinn eða fylgiskjalslínuna. Annars er nýrri víddasamstæðu bætt við töfluna og henni hennar bætt við línu færslubókar, haus fylgiskjals eða línu fylgiskjals.

## <a name="codeunit-408-dimension-management"></a>Codeunit 408 víddarstjórnun
Codeunit 408, Víddastjórnun, er aðgerðasafn sem sér um algeng verkefni sem tengjast víddum, m.a. afritun úr einni töflu í aðra eða úr einu skjali í annað.

## <a name="performance-improvement"></a>Bætt afköst  
Með því að vista víddasamstæður einu sinni í gagnagrunni, er gagnagrunnsbilinu haldið við og heildarafköst eru bætt.  

## <a name="see-also"></a>Sjá einnig
[Hönnunarupplýsingar Leitað að víddarsamsetningum](design-details-searching-for-dimension-combinations.md)   
[Hönnunarupplýsingar töfluuppbygging](design-details-table-structure.md)   
[Hönnunarupplýsingar: Færslur víddarsamstæða](design-details-dimension-set-entries.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
