---
title: Um útreikning á kostnaðarverði
description: Frekari upplýsingar um aðferð við kostnaðarútreikning og aðra þætti hafa áhrif á reitinn kostnaðarverð á birgðaspjaldinu.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 03/06/2022
ms.author: a-reishima
ms.openlocfilehash: ac5878185f8ed65a2242c5e82b3d3b8a84936289
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950586"
---
# <a name="about-unit-cost-calculation"></a>Um útreikning á kostnaðarverði

Hver vara er með kostnaðarverði sem er reiknað út á grundvelli kostnaðaraðferðar fyrirtækisins og annarra þátta. Eftir því sem regla, með *staðlaðri* aðferð kostnaðarútreiknings, er gildið í **reitnum** Kostnaðarverð Byggt á staðalkostnaðinum fyrir vöruna. Fyrir allar aðrar aðferðir við kostnaðarútreikning (*FIFO*, *LIFO*, *specific* og *Average*) er kostnaðarverð reiknað út frá meðalkostnaðarverði yfir tímabil.  

Frekari upplýsingar eru í [Stjórnun birgðakostnaðar](finance-manage-inventory-costs.md).  

## <a name="when-is-the-unit-cost-field-updated"></a>Hvenær er reiturinn kostnaðarverð uppfærður

Valið áhrif kostnaðaraðferðar þegar **reiturinn** kostnaðarverð er uppfærður.

Þegar kostnaðarútreikningsaðferðin er stillt sem *stöðluð* **er reiturinn kostnaðarverð** uppfærður þegar staðalkostnaðinum er breytt og notendur geta ekki breytt **reitnum** Kostnaðarverð. Frekari upplýsingar [fást í að uppfæra staðalkostnað](finance-how-to-update-standard-costs.md).

Ef kostnaðaraðferðin er *FIFO*, *LIFO*, *Sérstök* eða *meðaltal* **er** kostnaðarverð uppfært í eftirfarandi tilvikum:

* Þegar varan er kostnaðarleiðrétt, sjálfkrafa eða með leiðréttandi [kostnaðarverki](inventory-how-adjust-item-costs.md#to-adjust-item-costs-manually).
* Við bókun innkaupareikninga, úttaks eða jákvæðrar leiðréttingar ef eitt af eftirfarandi skilyrðum er rétt:
  * Nettó reikningsfært magn vörunnar breytist úr neikvæðu eða núlli í jákvætt.
  * Gildandi kostnaðarverð er núll.

Ef annað þessara skilyrða er rétt **er** reiturinn kostnaðarverð uppfærður með gildinu í **reitnum Síðasti Beinn kostnaður** á birgðaspjaldinu.

> [!NOTE]
> **Reiturinn Kostn. kostnaður** er ekki uppfærður ef gildandi kostnaðarverð er hærra en núll og nýja einingarkostnaðurinn er núll. Kostn aður við núllið telst vera undantekning frá venjubundnum viðskiptum. Þess vegna er gildandi kostnaðarverð haldið til að veita síðast þekkt, viðeigandi gildi. Þessi undantekning á við jafnvel þó að fyrirliggjandi birgðir hafi verið endurmetnar á núll.

**Í** reitnum Kostnaðarverð á birgðaspjaldinu er hægt að kafa niður til að skoða sögu færslna sem meðalkostnaður á einingar á lager er reiknaður út frá í **glugganum meðalkostnaður í Calc. yfirlits**.

## <a name="unit-cost-calculation-for-purchases"></a>Útreikningur á kostnaðarverði fyrir innkaup

Þegar vörur eru innkomnar er gildið í **reitnum Síðasti Beinn kostnaður** á birgðaspjaldinu afritað í **reitinn innkaupsverð** í innkaupalínunni eða **í einingarupphæðarlínuna** í birgðabókarlínu.

Það sem valið er í reitnum **Aðferð kostnaðarútreiknings** hefur áhrif á hvernig [!INCLUDE[prod_short](includes/prod_short.md)] reiknar innihald reitarins **Einingarkostnaður** á línunum.

### <a name="costing-method-fifo-lifo-specific-or-average"></a>Kostnaðarútreikningsaðferð FIFO, LIFO, sértækt eða meðaltal

[!INCLUDE[prod_short](includes/prod_short.md)] reiknar út í reitinn **Einingarkostnaður SGM** í innkaupalínunni eða í reitinn **Einingarkostnaður** í birgðabókarlínunni eftir þessari reiknireglu:

*Kostnaðarverð (ISK) = (innkaupsverð – (afsláttarupphæð/magn)) x (1 + óbeinn kostnaður%/100) + hlutfall sameiginlegs kostnaðar*

### <a name="costing-method-standard"></a>Staðalaðferð kostnaðarútreiknings

Reiturinn **Kostn.verð (ISK)** á innkaupalínunni eða reiturinn **Kostnaðarverð** hefur verið fylltur út í birgðabókarlínunni með gildinu í reitnum **Kostnaðarverð** á birgðaspjaldinu. Með því að nota kostnaðarútreikningsaðferðarsett sem *Staðlað* er þetta gildi alltaf Byggt á staðlaðan kostnað.

Þegar innkaup [!INCLUDE[prod_short](includes/prod_short.md)] eru bókuð notar kostnaðarverð úr innkaupalínunni eða birgðabókarlínu í innkaupareikningsfærslu. Hægt er að sjá hana á færslunalistanum fyrir vöruna.

### <a name="all-costing-methods"></a>Allar aðferðir við kostnaðarútreikning

Kostnaðarverðið í upprunaskjalslínunni er notað til að reikna út efni reitsins **Kostnaðarupphæð raunveruleg** eða, ef við á reitinn **Kostnaðarupphæð (væntanleg)** sem tengist þessari birgðafærslu, sama hvaða kostnaðaraðferð er notuð á vöruna.

## <a name="unit-cost-calculation-for-sales"></a>Útreikningur á kostnaðarverði fyrir sölu

Þegar vörur eru seldar er kostnaðarverð afritað úr **reitnum** Kostnaðarverð á birgðaspjaldinu í sölulínuna eða birgðabókarlínuna.

Við bókun er kostnaðarverðið afritað yfir á birgðafærslu sölureiknings og má skoða það á færslulista vörunnar. [!INCLUDE[prod_short](includes/prod_short.md)] notar kostnaðarverðið í upprunaskjalslínunni til að reikna út efni reitsins **Kostnaðarupphæð (raunveruleg)** eða, ef við á **Kostnaðarupphæð (væntanleg)** reitinn í gildisfærslunni sem tengist þessar vörufærslu.

## <a name="see-also"></a>Sjá einnig .

[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Skráning nýrra atriða](inventory-how-register-new-items.md)  
[Um birgðakostnað](finance-learn-about-costing.md)  
[Birgðir](inventory-manage-inventory.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Uppsetning bestu venjur: Aðferð kostnaðarútreiknings](setup-best-practices-costing-method.md)  
[Hönnunarupplýsingar: Aðferð kostnaðarútreiknings](design-details-costing-methods.md)  
[Hönnunarupplýsingar: kostnaðarleiðrétting](design-details-cost-adjustment.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
