---
title: Aðstoðareiginleikar
description: Flýtivísanir og aðrir aðstoðareiginleikar.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, charts, tooltips, screen reader
ms.date: 04/29/2021
ms.author: jswymer
ms.openlocfilehash: 5a9b99b367ca732f5b6347462a07b0d0c3f5c522
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115891"
---
# <a name="accessibility-and-keyboard-shortcuts"></a>Aðgengi og Flýtivísanir

Þetta grein veitir upplýsingar um eiginleikana sem auðvelda aðgengi fatlaðra að [!INCLUDE[prod_short](includes/prod_short.md)]. [!INCLUDE[prod_short](includes/prod_short.md)] styður eftirfarandi aðgengiseiginleika:  

- Flýtilyklar. Sýna [flýtilykla](keyboard-shortcuts.md).
- Snerti- og pennahreyfingar á spjaldtölvum og símum. Sjá [Snerti- og pennabendingar](touch-gestures.md).
- Yfirlit  
- Yfirskrift  
- Annar texti fyrir myndir og tengla  
- Stuðningur við algeng aðstoðartækni 
- Breyta aðdrætti á hvaða síðu sem er
- Ábendingar um einingar í notandaviðmóti

## <a name="navigation"></a><a name="Navigation"></a> Leiðsögn
  
Hægt er að nota mismunandi samsetningar af dálklykli, Shift og örvalyklum á lyklaborðinu á til að fara á milli eininga á síðu. Einingarnar innihalda aðgerðir, reiti og dálka, hluta og aðrir stýringar. Yfirleitt er ýtt á dálkalykil eða Shift+dálkalykil til að fara í næstu eða fyrri einingu.

Þegar þú einbeitir þér að svæði sem inniheldur aðgerðir, eins og yfirlitsstikunni efst í hlutverkamiðstöðinni eða aðgerðarlínu á öðrum síðum, skaltu nota örvalyklana til að fara í gegnum mismunandi aðgerðir og hópa. Ýttu á Enter á hópi til að opna undirliggjandi aðgerðir hans og haltu svo áfram með örvalyklunum. Ýtt er á dálkalykil eða SHIFT+dálkalykill til að færa sig úr aðgerðarsvæðinu.

Með því að nota fliparöðun er einnig hægt að skipta á milli aðal vafrasíðu og svarglugga sem óska eftir staðfestingu, til dæmis, eða innskráningarsíðu.  

## <a name="headings-in-content"></a><a name="Headings"></a> Hausar í efni

HTML-uppruni fyrir efni [!INCLUDE[prod_short](includes/prod_short.md)] notar merki til að hjálpa notendum aðstoðartækni að skilja uppbyggingu og innihald síðunnar. Til dæmis, á listasíðum, eru dálkarnir skilgreindir í TH-merkjum og dálkur fyrirsagnir eru settar með TITLE eigind inni í merkinu. Skýringarmyndir fyrir þætti, svo sem FastTabs, FactBoxes og reitir eru í fyrirsagnamerkjum (H1, H2, H3 og H4).  

## <a name="image-and-links"></a><a name="Images"></a> Mynd og tenglar

Lýsandi texti fyrir myndir er stillt með ALT-eigind inni í IMG-merkinu. Lýsandi texti fyrir tengla er stillt með ALT-eigind inni í A-merkinu.  

## <a name="assistive-technologies"></a><a name="AssistiveTech"></a> Aðstoðartækni

[!INCLUDE[prod_short](includes/prod_short.md)] styður ýmis konar aðstoðartækni, svo sem mikla skerpu, skjálesara og raddgreiningarhugbúnaður. Sum aðstoðartækni kann ekki að virka vel með ákveðnum þáttum á síðum [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="zoom"></a><a name="zoom"></a> Súma

Flestir vafrar nota staðlaðar flýtilykla til að auka og minnka aðdrátt á opinni síðu. Þessir flýtilyklar eru EKKI aðeins fyrir [!INCLUDE [prod_short](includes/prod_short.md)] en þeir virka þegar [!INCLUDE [prod_short](includes/prod_short.md)] er notað í vafra. Listi yfir studda flýtilykla má finna á [Flýtilyklar fyrir aukinn eða minnkaðan aðdrátt](keyboard-shortcuts.md#zoomshortcuts).

## <a name="tooltips"></a>Ábending

Ábendingar eru tiltækar á flestum þáttum notandaviðmótsins, eins og síðureitum og dálkum, aðgerðum, vísbendingAREITUM og myndritum. Ábending er aukatexti sem útskýrir einingu til að hjálpa þér að skilja tilgang hennar betur. 

Ábendingar eru aðgengilegar á mismunandi hátt eftir því hvaða biðlara (vef eða farsíma) og tæki er unnið með. Notið töfluna hér á eftir til viðmiðunar. Sumir skjálesarar geta lesið tilteknar ábendingar. Í því tilviki er hægt að opna ábendingarnar eins og lýst er í töflunni og nota síðan skjálesarann til að fletta í ábendinguna eins og í öllum öðrum einingum.

#### <a name="accessing-tooltips"></a>Aðgangur ábendinga

|Eining|Músaaðgerð fyrir vefbiðlara|Flýtilykill fyrir vefbiðlara|Sneritskipan í spjaldtölvu/síma fyrir farsímaforrit|Stuðningur við skjálesara|
|-------|-----------------|------------|--------------------------|---------------------|
|Síðureitir og dálkahausar|Haltu bendli yfir reit eða smelltu á dálkahaus|Færa áherslu í reit eða dálkahaus og ýta á ALT+örvalykil upp|Smelltu á fyrirsögn reitsins |já|
|Grafþættir eins og stika, lína, sneið|Haltu bendlinum yfir einingunni|Færa áherslu á einingu, t.d. með örvalyklum|Haltu fingri á einingu|já|
|Aðgerðir|Haltu bendlinum yfir aðgerðinni|ekkert|ekkert |nei|
|Vísbendingareitir|Haltu bendlinum yfir reitnum |ekkert|ekkert|nei|


<!--
- With a mouse, hover over the element.
- With keyboard, press the Alt+Up Arrow keys.
- On a tablet or phone, tap and hold on the element. To learn about more gestures, see [Touch and Pen Gestures](touch-gestures.md)

-->

## <a name="for-more-accessibility-information"></a>Fyrir frekari upplýsingar um aðgengi

Þú getur fundið viðbótarupplýsingar um aðgengi að Microsoft vörum og aðstoðartækni á vefsíðu [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160).

## <a name="see-also"></a>Sjá einnig

[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Algengar spurningar](across-faq.yml)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
