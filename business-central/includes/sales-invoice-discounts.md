---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035787"
---
Þegar allar vörur hafa verið færðar í sölupöntunarlínurnar er hægt að reikna reikningsafslátt af öllu söluskjalinu með því að velja aðgerðina **Reikna reikningsafsl**.

Ef reiturinn **Reikna reikn.afsl.** er valinn í glugganum **Sölugrunnur** þá er reikningsafslátturinn reiknaður sjálfkrafa þegar þú gerir annað af eftirfarandi á söluskjali:

* Skoða tölfræði
* Skoða prufuskýrslu
* Prenta
* Færsla

Afslættinum er jafnað niður á allar línur í söluskjalinu fyrir vörur þar sem **Já** er í reitnum **Reikna reikningsafsl.** Þetta er sjálfgefin stilling fyrir vörur.

Reikningsafsláttarskilmálar eru skilgreindir á síðunni **Reikningsafsl. viðskm.** til að reikna út reikningsafsláttinn. Kerfið notar gjaldmiðilskóðann í sölureikningnum til að finna skilmála reikningsafsláttar í samsvarandi gjaldmiðli.

Ef reikningsafsláttur hefur ekki verið skilgreindur í erlendum gjaldeyri þá eru notaðir skilmálar reikningsafsláttarsem skilgreindir eru í töflunni **Reikningsafsl. viðskm** síðunni með upphæðir í staðbundnum gjaldmiðli og gengi á bókunardegi söluskjalsins er notað til að reikna reikningsafsláttinn í erlendum gjaldeyri.
