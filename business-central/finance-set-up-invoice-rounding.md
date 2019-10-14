---
title: Setja upp reikningur sléttun | Microsoft Docs
description: Hægt er að slétta upphæðir reikninga þegar reikningar eru stofnaðir. Staðbundnar reglugerðir eða venjur gætu krafist ákveðinnar aðferðar við sléttun reikningsins, til dæmis að upphæð sem deila má í með 0,05.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 399216085913c576007bd5996cef4f3192362c4b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305645"
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
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **bókhaldslykill** og veldu síðan tengda tengilinn.  
2. Reikningurinn er settur upp á síðunni **Bókhaldslykill** og honum er gefið heitið **Reikningssléttun** eða eitthvað álíka. [!INCLUDE[d365fin](includes/d365fin_md.md)] notar reikningsheitið sem texta fyrir reikninga sem eru sléttaðir.  
3. Velja skal bókunarflokka fyrir sléttaðar upphæðir í reitunum **Söluskattur vörubókunarflokkur** eða **VSK vörubókunarflokkur**, út frá því hvort notaður er VSK eða söluskattur. Ráðlegt að setja upp kóta nýja hópsins sem hægt er að nota fyrir reikningssléttun.
4. Reiturinn **Alm. bókunarflokkur**, og annað hvort **Viðsk.bókunarflokkur söluskatts** eða **Viðsk.bókunarflokkur VSK** reiturinn eru hafðir auðir. <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  

Nú getur þú úthlutað sléttunarreikningnum til bókunarflokkanna á síðunni **Bókunarflokkar Lánardrottinn**.  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a>Uppsetning sléttunar fyrir erlendan og staðbundinn gjaldmiðil
Áður en hægt er að nota sjálfvirku reikningssléttunaraðferðina þarf að setja upp sléttunarreglur fyrir erlenda og staðbundna gjaldmiðla.

### <a name="to-set-up-rounding-for-foreign-currencies"></a>Uppsetning sléttunar fyrir erlendan gjaldmiðil  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Gjaldmiðlar** og veldu síðan tengda tengilinn.  
2. Á síðunni **Gjaldmiðlar** skal velja þann erlenda gjaldmiðil sem opna á í **Gjaldmiðilskort** og síðan fylla í reitina **Upphæð sléttunarnákvæmni**, **Eining-Upphæð sléttunarnákvæmni**, **Reikningssléttunarnákvæmni** og **Reikningssléttunartegund**.

### <a name="to-set-up-rounding-for-your-local-currency"></a>Uppsetning sléttunar fyrir þinn staðbundna gjaldmiðil
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning fjárhags** og veldu síðan tengda tengilinn.  
2. Á **Uppsetning fjárhags** síðunni á flýtiflipanum **Almennt** velurðu **Reikningssléttunarnákvæmni** og svo **Reikningssléttunargerð** reitina.  

## <a name="activate-the-invoice-rounding-function"></a>Virkja aðgerðina fyrir reikningssléttun  
Ef forritið á örugglega að slétta sölu- og innkaupareikninga sjálfkrafa þarf að gera reikningssléttunaraðgerðina virka. Hægt er að gera reikningssléttun virka fyrir sölu- og innkaupareikninga sérstaklega.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning sölu & útistandandi** eða **Uppsetning innkaupa & viðskiptaskuldir** og veldu síðan tengda tengilinn.  
2. Á flýtiflipanum **Almennt** skal velja gátreitinn **Sléttun reiknings**.  

## <a name="see-also"></a>Sjá einnig  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Skrá innkaup](purchasing-how-record-purchases.md)
