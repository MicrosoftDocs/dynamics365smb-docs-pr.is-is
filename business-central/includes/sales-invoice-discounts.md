---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 95121642b62f33ea1fc160c103ee845816706530
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778648"
---
Þegar allar vörur hafa verið færðar sem línur er hægt að reikna reikningsafslátt af öllu söluskjalinu með því að velja aðgerðina **Reikna reikningsafsl**.

Afslátturinn er reiknaður byggt á öllum línum í söluskjalinu fyrir vörur þar sem **Já** er í reitnum **Reikna reikningsafslátt**. Þetta er sjálfgefin stilling fyrir vörur. Línur með kostnaðarauka eru til dæmis ekki teknar með í útreikningi reikningsafsláttar. Ef nota á afslátt á slíkar línur verður að stilla reitinn **Línuafsláttur %** í línunni sem á við.  

> [!TIP]
> Ef reiturinn **Reikna reikn.afsl.** er valinn á síðunni **Sölugrunnur** þá er reikningsafslátturinn reiknaður sjálfkrafa þegar þú gerir annað af eftirfarandi á söluskjali:
>
> * Skoða tölfræði
> * Skoða prufuskýrslu
> * Prenta
> * Færsla

Reikningsafsláttarskilmálar fyrir viðskiptamann eru skilgreindir á síðunni **Reikningsafsl. viðskm.** fyrir viðskiptamanninn. Kerfið notar gjaldmiðilskóðann í sölureikningnum til að finna skilmála reikningsafsláttar í samsvarandi gjaldmiðli.

Ef reikningsafsláttur hefur ekki verið skilgreindur í erlendum gjaldeyri þá eru notaðir skilmálar reikningsafsláttarsem skilgreindir eru í töflunni **Reikningsafsl. viðskm** síðunni með upphæðir í staðbundnum gjaldmiðli og gengi á bókunardegi söluskjalsins er notað til að reikna reikningsafsláttinn í erlendum gjaldeyri.
