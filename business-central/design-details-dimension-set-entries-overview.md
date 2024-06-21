---
title: Yfirlit yfir víddasamstæðufærslur
description: Í þessari grein er yfirlit yfir hvernig færslur víddasamstæðu eru geymdar sem víddasamstæðufærslur og hvernig þær eru bókaðar.
author: brentholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: dimension
ms.date: 06/14/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Yfirlit yfir víddasamstæðufærslur
Í þessu efnisatriði er lýst hvernig víddasamstæðufærslur eru geymdar og bókaðar í [!INCLUDE[prod_short](includes/prod_short.md)].  

## Víddasamstæður  
Víddasamstæða er sérstök samsetning víddargilda. Er vistað sem víddasamstæðufærslur í gagnagrunninum. Hver víddasamstæðufærsla stendur fyrir eitt víddargildi. Víddasamstæðan er auðkennd með algengum víddasamstæðukennum sem eru úthlutuð hverri víddasamstæðufærslu sem tilheyrir víddasamstæðunni.  

Eftirfarandi dæmi sýnir víddasamstæðu sem hefur þrjár víddasamstæðufærslur. Víddasamstæðan er auðkennd með víddasamstæðukenni, sem er 108.  

|Auðkenni víddasamstæðu|Víddarkóti|Gildiskóti víddar|Nafn víddagildis|  
|----------------------|--------------------|--------------------------|--------------------------|  
|108|SVÆÐI|70|Norður Ameríka|  
|108|ATVGRHÓPUR|HOME|Heimili|  
|108|DEILD|SALA|Sala|  

## Víddasamstæðufærslur  
Víddasamstæður eru geymdar í töflunni **Víddasamstæðufærsla** sem víddasamstæðufærslur með sama víddasamstæðukenni.  

![Flæði víddasamstæðufærslna.](media/dimensionentrynav7.png "Flæði víddasamstæðufærslna")  

Þegar ný færslubókarlína, skjalahaus eða skjalalína er stofnuð er hægt að tilgreina samsetningu víddargilda. Í stað þess að geyma hvert víddargildi í gagnagrunninum er kenni víddasamstæðu tengt færslubókarlínu, haus skjals eða línu skjals til að tilgreina víddasamstæðuna.  

Þegar síðunni **Breyta Víddasamstæðufærslum** er breytt og lokað er gerð athugun til að sjá hvort samsetning víddargildanna sé til sem víddasafn í töflunni. Ef samsetningin kemur fyrir í töflunni er samsvarandi víddasamstæðukenni tengt við færslubókarlínuna, fylgiskjalshausinn eða fylgiskjalslínuna. Annars er nýrri víddasamstæðu bætt við töfluna og henni hennar bætt við línu færslubókar, haus fylgiskjals eða línu fylgiskjals.

## Codeunit 408 víddarstjórnun
Codeunit 408, Víddastjórnun, er aðgerðasafn sem sér um algeng verkefni sem tengjast víddum, m.a. afritun úr einni töflu í aðra eða úr einu skjali í annað.

## Bætt afköst  
Með því að vista víddasamstæður einu sinni í gagnagrunni, er gagnagrunnsbilinu haldið við og heildarafköst eru bætt.  

## Sjá einnig
[Hönnunarupplýsingar Leitað að víddarsamsetningum](design-details-searching-for-dimension-combinations.md)   
[Hönnunarupplýsingar töfluuppbygging](design-details-table-structure.md)   
[Hönnunarupplýsingar: Færslur víddarsamstæða](/dynamics365/business-central/design-details-dimension-set-entries-overview)   


[!INCLUDE[footer-include](includes/footer-banner.md)]