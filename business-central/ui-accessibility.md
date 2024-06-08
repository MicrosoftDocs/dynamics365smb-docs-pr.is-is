---
title: Aðstoðareiginleikar
description: Þessi grein veitir upplýsingar um flýtilykla og önnur hjálpartæki í Business Central fyrir fólk með fötlun.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'accessibility, shortcuts, charts, tooltips, screen reader'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 06/23/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
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

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="navigation"></a><a name="Navigation"></a>Leiðsögn
  
Hægt er að nota mismunandi samsetningar af dálklykli, Shift og örvalyklum á lyklaborðinu á til að fara á milli eininga á síðu. Einingarnar innihalda aðgerðir, reiti og dálka, hluta og aðrir stýringar. Almennt skal velja <kbd>Dálklykill</kbd> eða <kbd>Vaktarflipi</kbd>+<kbd></kbd> til að færa í næsta eða fyrri einingu.

Þegar þú einbeitir þér að svæði sem inniheldur aðgerðir, eins og yfirlitsstikunni efst í hlutverkamiðstöðinni eða aðgerðarlínu á öðrum síðum, skaltu nota örvalyklana til að fara í gegnum mismunandi aðgerðir og hópa. Færið <kbd>inn</kbd> í hóp til að opna það eru undirliggjandi aðgerðir og haldið svo áfram að nota örvalyklana. Veljið <kbd>Dálklykill</kbd> eða <kbd>Vaktarflipi</kbd>+<kbd></kbd> til að flytja út úr aðgerðasvæðinu.

Með því að nota fliparöðun er einnig hægt að skipta á milli aðal vafrasíðu og svarglugga sem óska eftir staðfestingu, til dæmis, eða innskráningarsíðu.  

## <a name="headings-in-content"></a><a name="Headings"></a>Hausar í efni

HTML-uppruni fyrir efni [!INCLUDE[prod_short](includes/prod_short.md)] notar merki til að hjálpa notendum aðstoðartækni að skilja uppbyggingu og innihald síðunnar. Til dæmis, á listasíðum, eru dálkarnir skilgreindir í TH-merkjum og dálkur fyrirsagnir eru settar með TITLE eigind inni í merkinu. Skýringarmyndir fyrir þætti, svo sem FastTabs, FactBoxes og reitir eru í fyrirsagnamerkjum (H1, H2, H3 og H4).  

## <a name="image-and-links"></a><a name="Images"></a>Mynd og tenglar

Lýsandi texti fyrir myndir er stillt með ALT-eigind inni í IMG-merkinu. Lýsandi texti fyrir tengla er stillt með ALT-eigind inni í A-merkinu.  

## <a name="assistive-technologies"></a><a name="AssistiveTech"></a>Aðstoðartækni

[!INCLUDE[prod_short](includes/prod_short.md)] styður ýmis konar aðstoðartækni, svo sem mikla skerpu, skjálesara og raddgreiningarhugbúnaður. Sum aðstoðartækni kann ekki að virka vel með ákveðnum þáttum á síðum [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="zoom"></a><a name="zoom"></a>Súma

Flestir vafrar nota staðlaðar flýtilykla til að auka og minnka aðdrátt á opinni síðu. Þessir flýtilyklar eru EKKI aðeins fyrir [!INCLUDE [prod_short](includes/prod_short.md)] en þeir virka þegar [!INCLUDE [prod_short](includes/prod_short.md)] er notað í vafra. Listi yfir studda flýtilykla má finna á [Flýtilyklar fyrir aukinn eða minnkaðan aðdrátt](keyboard-shortcuts.md#zoomshortcuts).

## <a name="tooltips"></a>Ábending

Ábendingar eru tiltækar á flestum þáttum notandaviðmótsins, eins og síðureitum og dálkum, aðgerðum, vísbendingAREITUM og myndritum. Ábending er aukatexti sem útskýrir einingu til að hjálpa þér að skilja tilgang hennar betur. 

Ábendingar eru aðgengilegar á mismunandi hátt eftir því hvaða biðlara (vef eða farsíma) og tæki er unnið með. Notið töfluna hér á eftir til viðmiðunar. Sumir skjálesarar geta lesið tilteknar ábendingar. Í því tilviki er hægt að opna ábendingarnar eins og lýst er í töflunni og nota síðan skjálesarann til að fletta í ábendinguna eins og í öllum öðrum einingum.

#### <a name="accessing-tooltips"></a>Aðgangur ábendinga

|Eining|Músaaðgerð fyrir vefbiðlara|Flýtilykill fyrir vefbiðlara|Sneritskipan í spjaldtölvu/síma fyrir farsímaforrit|Stuðningur við skjálesara|
|-------|-----------------|------------|--------------------------|---------------------|
|Síðureitir og dálkahausar|Haltu bendli yfir reit eða smelltu á dálkahaus|Færa fókus í reit eða dálkfyrirsögn og velja <kbd>Alt</kbd>+<kbd>up örvalykla</kbd> |Smelltu á fyrirsögn reitsins |já|
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
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Algengar spurningar](across-faq.yml)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
