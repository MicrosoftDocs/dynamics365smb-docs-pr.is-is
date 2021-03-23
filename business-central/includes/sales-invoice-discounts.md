---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 539ee2eb2c9e4a71eacfb78d95320870128fb1d9
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470288"
---
Þegar allar vörur hafa verið færðar í sölulínurnar er hægt að reikna reikningsafslátt af öllu skjalinu með því að velja aðgerðina **Reikna reikningsafsl**.

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
