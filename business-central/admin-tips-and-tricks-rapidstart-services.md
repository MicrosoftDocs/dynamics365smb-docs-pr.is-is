---
title: 'Ábendingar: RapidStart Services | Microsoft Docs'
description: Þegar fyrirtæki eru skilgreind með RapidStart Services, eru nokkur ráð sem hægt er að nýta sér til að hjálpa til við að láta innleiðinguna ganga snurðulaust fyrir sig.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 875ab6f5875a842fb4c2ab906f39ae95607f6ba8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800751"
---
# <a name="tips-and-tricks-rapidstart-services"></a>Ábendingar: RapidStart Services
Þegar fyrirtæki eru skilgreind með RapidStart Services, eru nokkur ráð sem hægt er að nýta sér til að hjálpa til við að láta innleiðinguna ganga snurðulaust fyrir sig.  

## <a name="take-advantage-of-configuration-templates"></a>Nota stillingasniðmát  
Grunnstillingarsniðmát geta auðveldað innleiðingarferlið. Með því að nota þau, er hægt að taka með svipaða viðskiptamenn í hlutum og þróa síðan innleiðingarreglu sem meðhöndlar alla viðskiptamenn í hluta á svipaðan hátt. Með því móti er hægt að nota forskilgreiningu að einhverju leyti fyrir hvern hluta og halda áfram með skjóta innleiðingu.  

## <a name="configuration-questionnaires"></a>Spurningalisti grunnstillingar  
Til að hjálpa til við útfyllingu skilgreiningarspurningalista skal íhuga að skilgreina sjálfgefin svör til að gefa bestu venjur til kynna.  

## <a name="batch-creation-of-journal-lines"></a>Keyrslugerð af færslulínum  
Mælt er með að nota gagnaflutningsverkfærin sem boðið er upp á til að færa bókarfærslur. Ef keyrsla er notuð til að stofna færslubókarlínur hefur hún takmarkað gildissvið og myndar sjálfgefna reiti í færslubók. Afganginum af færslubókinni þarf svo að ljúka handvirkt.  

## <a name="migrating-transactions"></a>Flutningur á færslum  
Mælt er með því að opnunarstöður séu fluttar í skrefum í eftirfarandi röð.  

1.  Flytja opnunarstöður fjárhags án þess að nota undirhöfuðbók fjárhagslykilsins. Nota tiltekna mótfærslureikninga fyrir upphafsjöfnuð, einn uppsettan fyrir hverja undirhöfuðbók. Setja upp mótfærslureikningana til að virkja beinar bókanir.  
2.  Flytja opnar færslur í viðskiptamannabók.  
3.  Flytja opnar birgðafærslur.  
4.  Flytja opnar eignafærslur.  

## <a name="see-also"></a>Sjá einnig  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)
