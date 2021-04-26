---
title: Vöruhúsaaðgerðir | Microsoft Docs
description: Eftir að tekið hefur verið á móti vörum og áður en vörur eru afhentar, fer röð vöruhúsaaðgerða fram til þess að tryggja að flæði gegnum vöruhúsið sé skilvirkt og til að skipuleggja og viðhalda birgðum fyrirtækisins.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c9ca3597a681ae5494510be2dd0c4ca9ae8bdc52
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784093"
---
# <a name="warehouse-management"></a>Vöruhúsastjórnun
Eftir að tekið hefur verið á móti vörum og áður en vörur eru afhentar, fer röð vöruhúsaaðgerða fram til þess að tryggja að flæði gegnum vöruhúsið sé skilvirkt og til að skipuleggja og viðhalda birgðum fyrirtækisins.

Dæmigerðar vöruhúsaaðgerðir felast í frágangi vöru, færslu á vörum inni í eða milli vöruhúsa og tínslu á vörum fyrir samsetningu, framleiðslu eða afhendingu. Vörusamsetning fyrir sölu eða birgðir geta einnig talist til vöruhúsaðgerða, en um það er fjallað annarsstaðar. Nánari upplýsingar, sjá [Samsetningarstjórnun](assembly-assemble-items.md).  

Í stórum vöruhúsum er hægt að aðskilja mismunandi meðhöndlunarverk með deildum og samhæfingu sem stjórnað er með stýrðu verkflæði. Í einfaldari uppsetningum er flæðið ekki jafn formfast og vöruhúsaaðgerðir eru framkvæmdar með svokölluðum birgðafrágangi og -tínslu. Nánari upplýsingar um mismunandi vöruhúsaflækjustig, einfalt og ítarlegt, eru í [Hönnunarupplýsingar: Vöruhúsayfirlit](design-details-warehouse-overview.md).

Áður en þú framkvæmir vöruhúsaaðgerðir, er nauðsynlegt að setja kerfið upp fyrir viðeigandi flækjustig vöruhúsaferla. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Birgðatengd verk talningar, leiðréttingar og endurflokkunar á vörum kann að fela í sér verk vöruhúss sem verður að framkvæma í færslum vöruhúss áður en hægt er að samstilla þau við tengdar birgðabókafærslur. Nánari upplýsingar er að finna í [Telja, leiðrétta og endurflokka birgðir](inventory-how-count-adjust-reclassify.md).

 Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.   

|**Til að**|**Sjá**|  
|------------|-------------|  
|Skrá móttöku vara í vöruhúsabirgðageymslum (þar með talið umframmóttökum), annað hvort með innkaupapöntun eingöngu, í einfaldri birgðageymsluuppsetningu, eða með vöruhúsamóttöku, ef skyldi vera sjálfvirkt vöruhúsaferli, að hluta eða í heild, í birgðageymslunni.|[Móttaka vara](warehouse-how-receive-items.md)|
|Tengja framhjá frágangs- og tínsluferlinu til að flýta vöru beint frá móttöku eða framleiðslu yfir í afhendingu.|[Hjáskipa vörur](warehouse-how-to-cross-dock-items.md)|    
|Ganga frá vörum sem eru mótteknar vegna innkaupa, söluvöruskila, flutnings eða framleiðslufrálagi samkvæmt tilgreindu aðgerðaflæði vöruhúss.|[Gengið frá vörum](warehouse-put-away-items.md)|
|Færa vörur milli hólfa í vöruhúsinu.|[Færa vörur](warehouse-move-items.md)|
|Tína til vörur fyrir afhendingu, flutning eða til notkunar í framleiðslu eða samsetningu, samkvæmt tilgreindu aðgerðaflæði vöruhúss.|[Tína vörur](warehouse-pick-items.md)|
|Skrá afhendingu vara frá vöruhúsabirgðageymslum, annað hvort með sölupöntun eingöngu, í einfaldri birgðageymsluuppsetningu, eða með vöruhúsaafhendingu, ef skyldi vera sjálfvirkt vöruhúsaferli, að hluta eða í heild, í birgðageymslunni.|[Senda vörur](warehouse-how-ship-items.md)|  

## <a name="see-also"></a>Sjá einnig  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]