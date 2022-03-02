---
title: 'Ábendingar: RapidStart Services | Microsoft Docs'
description: Þegar fyrirtæki eru skilgreind með RapidStart Services, eru nokkur ráð sem hægt er að nýta sér til að hjálpa til við að láta innleiðinguna ganga snurðulaust fyrir sig.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9b08f4ed71afb580438a5fc8d67cbdfc6c0f5ac6
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8129026"
---
# <a name="tips-and-tricks-rapidstart-services"></a>Ábendingar og góð ráð: RapidStart Services

Þegar fyrirtæki eru skilgreind með RapidStart Services, eru nokkur ráð sem hægt er að nýta sér til að hjálpa til við að láta innleiðinguna ganga snurðulaust fyrir sig.  

## <a name="take-advantage-of-configuration-templates"></a>Nota stillingasniðmát

Grunnstillingarsniðmát geta auðveldað innleiðingarferlið. Með því að nota þau, er hægt að taka með svipaða viðskiptamenn í hlutum og þróa síðan innleiðingarreglu sem meðhöndlar alla viðskiptamenn í hluta á svipaðan hátt. Með því móti er hægt að nota forskilgreiningu að einhverju leyti fyrir hvern hluta og halda áfram með skjóta innleiðingu.  

## <a name="configuration-questionnaires"></a>Spurningalisti grunnstillingar

Til að hjálpa til við útfyllingu skilgreiningarspurningalista skal íhuga að skilgreina sjálfgefin svör til að gefa bestu venjur til kynna.  

## <a name="batch-creation-of-journal-lines"></a>Keyrslugerð af færslulínum

Mælt er með að nota gagnaflutningsverkfærin sem boðið er upp á til að færa bókarfærslur. Ef keyrsla er notuð til að stofna færslubókarlínur hefur hún takmarkað gildissvið og myndar sjálfgefna reiti í færslubók. Afganginum af færslubókinni þarf svo að ljúka handvirkt.  

## <a name="migrating-transactions"></a>Flutningur á færslum

Mælt er með því að opnunarstöður séu fluttar í skrefum í eftirfarandi röð. <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. Flytja opnunarstöður fjárhags án þess að nota undirhöfuðbók fjárhagslykilsins. Nota tiltekna mótfærslureikninga fyrir upphafsjöfnuð, einn uppsettan fyrir hverja undirhöfuðbók. Setja upp mótfærslureikningana til að virkja beinar bókanir.  
2. Flytja opnar færslur í viðskiptamannabók.  <!--work on these-->
3. Flytja opnar birgðafærslur.  
4. Flytja opnar eignafærslur.  

## <a name="make-each-package-manageable"></a>Gera hvern pakka viðráðanlegri

Þegar skilgreiningarpakkar eru notaðir til að flytja gögn, skal aðskilja gögnin í aðskilda pakka til að auðveldara sé að meðhöndla þá. Ef ætlunin er til dæmis að flytja fjárhagsfærslur 20 ára gæti innflutningurinn tekið margar klukkustundir og daga. Þess í stað skaltu skipta gögnunum upp þannig að hver pakki verði viðráðanlegri. Sem stendur eru engar fastreglur til um gerð pakka, en ef þú sérð vandamál við að flytja pakka inn eða út skaltu prófa að minnka hann og sjá hvort það hjálpar.  

## <a name="see-also"></a>Sjá einnig

[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]