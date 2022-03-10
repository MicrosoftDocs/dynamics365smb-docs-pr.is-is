---
title: Uppsetning sléttunargerðar reikninga
description: Ef þörf er á að slétta upphæðir reikninga þegar reikningar eru stofnaðir, má nota sjálfvirku sléttunaraðferðina sem er útskýrð hér.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5, 16, 118, 459, 460, 495
ms.date: 06/16/2021
ms.author: bholtorf
ms.openlocfilehash: 781027b74912e8971d27d6b6c7613243c135cc1f
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8143479"
---
# <a name="set-up-invoice-rounding"></a>Uppsetning sléttunargerðar reikninga
Ef þörf er á að slétta upphæðir reikninga þegar reikningar eru stofnaðir, má nota sjálfvirku sléttunaraðferðina. Þegar reikningur er sléttaður er bætt við aukalínu með sléttunarupphæðinni og þessi lína er bókuð með hinum reikningslínunum.

> [!NOTE]  
>  Staðbundnar reglugerðir eða venjur gætu krafist ákveðinnar aðferðar við sléttun reikningsins, til dæmis að upphæð sem deila má í með 0,05.  

Til að nota sjálvirka sléttun reiknings þarf að:  

* Tilgreina fjárhagsreikningana sem bóka á sléttunarmun í.  
* Setja upp reglur fyrir sléttun reikninga í staðbundnum gjaldmiðli og erlendum gjaldmiðli.  
* Virkja eiginleikann.  

> [!NOTE]  
>  Auk jöfnunareiginleika reiknings má slétta upphæðir reikninga með eiginleikunum sléttun einingaupphæða og sléttun upphæða.  

## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Uppsetning fjárhagsreikninga fyrir sléttunarmismun reikninga
Ef nota á sjálfvirka reikningssléttunaraðgerð forritsins þarf að setja upp fjárhagsreikning eða reikninga þar sem sléttunarmismunur verður bókaður. Áður en þetta er hægt þarf að setja upp VSK-vörubókunarflokka. Nánari upplýsingar um það eru í [Setja upp VSK](finance-setup-vat.md).  

### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Uppsetning fjárhagsreikninga fyrir sléttunarmismun reikninga  
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Reikningurinn er settur upp á síðunni **Bókhaldslykill** og honum er gefið heitið **Reikningssléttun** eða eitthvað álíka. [!INCLUDE[prod_short](includes/prod_short.md)] notar reikningsheitið sem texta fyrir reikninga sem eru sléttaðir.  
3. Velja skal bókunarflokka fyrir sléttaðar upphæðir í reitunum **Söluskattur vörubókunarflokkur** eða **VSK vörubókunarflokkur**, út frá því hvort notaður er VSK eða söluskattur. Ráðlegt að setja upp kóta nýja hópsins sem hægt er að nota fyrir reikningssléttun.
4. Reiturinn **Alm. bókunarflokkur**, og annað hvort **Viðsk.bókunarflokkur söluskatts** eða **Viðsk.bókunarflokkur VSK** reiturinn eru hafðir auðir. <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  

Nú getur þú úthlutað sléttunarreikningnum til bókunarflokkanna á síðunni **Bókunarflokkar Lánardrottinn**.  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a>Uppsetning sléttunar fyrir erlendan og staðbundinn gjaldmiðil
Áður en hægt er að nota sjálfvirku reikningssléttunaraðferðina þarf að setja upp sléttunarreglur fyrir erlenda og staðbundna gjaldmiðla.

### <a name="to-set-up-rounding-for-foreign-currencies"></a>Uppsetning sléttunar fyrir erlendan gjaldmiðil  
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Gjaldmiðlar** og velja síðan viðkomandi tengil.  
2. Á síðunni **Gjaldmiðlar** skal velja þann erlenda gjaldmiðil sem opna á í **Gjaldmiðilskort** og síðan fylla í reitina **Upphæð sléttunarnákvæmni**, **Eining-Upphæð sléttunarnákvæmni**, **Reikningssléttunarnákvæmni** og **Reikningssléttunartegund**.

### <a name="to-set-up-rounding-for-your-local-currency"></a>Uppsetning sléttunar fyrir þinn staðbundna gjaldmiðil
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning fjárhags** og velja síðan viðkomandi tengil.  
2. Á **Uppsetning fjárhags** síðunni á flýtiflipanum **Almennt** velurðu **Reikningssléttunarnákvæmni** og svo **Reikningssléttunargerð** reitina.  

## <a name="activate-the-invoice-rounding-function"></a>Virkja aðgerðina fyrir reikningssléttun  
Ef forritið á örugglega að slétta sölu- og innkaupareikninga sjálfkrafa þarf að gera reikningssléttunaraðgerðina virka. Hægt er að gera reikningssléttun virka fyrir sölu- og innkaupareikninga sérstaklega.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, slá inn **Uppsetning sölu og útistandandi** eða **Uppsetning Innkaupa og viðskiptaskulda** og velja svo viðeigandi tengil.  
2. Á flýtiflipanum **Almennt** skal velja gátreitinn **Sléttun reiknings**.  

## <a name="see-also"></a>Sjá einnig  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Skrá innkaup](purchasing-how-record-purchases.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]