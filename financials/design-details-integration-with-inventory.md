---
title: "Hönnunarupplýsingar - Sameining með birgðum | Microsoft Docs"
description: "Hlutarnir Vöruhúsakerfi og Birgðir vinna saman í efnislegum birgðum og leiðréttingu birgða eða vöruhúss."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 00a12f3f2203ed3b22cfee1af6aa8f155ca5fe4b
ms.contentlocale: is-is
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-integration-with-inventory"></a>Hönnunarupplýsingar: Sameining með birgðum
Hlutarnir Vöruhúsakerfi og Birgðir vinna saman í efnislegum birgðum og leiðréttingu birgða eða vöruhúss.  
  
## <a name="physical-inventory"></a>Physical Inventory  
 Glugginn **Vöruh. - raunbirgðabók** er notaður með glugganum **Raunbirgðabók** fyrir allar ítarlegar staðsetningar vöruhúss. Birgðir á hólfastigi eru reiknaðar úr og útprentaður listi afhendur starfsmanni vöruhúss. Listinn sýnir hvaða vörur í hvaða hólfum þarf að telja.  
  
 Starfsmaður vöruhússins slær inn reiknað magn í gluggann **Vöruh. - raunbirgðabók** og bókar svo færslubókina.  
  
 Ef talið magn er meira en magn á færslubókarlínu er hreyfing bókuð fyrir þennan mun á milli sjálfgefna leiðréttingarhólfsins og talda hólfsins. Þetta eykur magnið í talda hólfinu og minnkar magnið í sjálfgefna leiðréttingarhólfinu.  
  
 Ef talið magn er minna en magnið á færslubókarlínunni er hreyfing fyrir þennan mun bókuð frá talda hólfinu í sjálfgefna leiðréttingarhólfið. Þetta lækkar magnið í talda hólfinu og eykur magnið í sjálfgefna leiðréttingarhólfinu.  
  
 Í háþróaður vörugeymsla, gildi í **Magn reiknað** sviði er sótt frá birgðahöfuðbókarfærslur og gildi í **Magn raunverulegt magn á lager** reitur er sótt frá vöruhúsi færslum, að undanskildum jöfnunarhólfainnihaldi. Reiturinn **Magn** tilgreininn mismuninn á milli fyrstu reitanna tveggja, sem ætti að vera jafn innihaldinu í leiðréttingarhólfinu.  
  
 Þegar þú bókar efnisbirgðabók eru birgðir og sjálfgefið leiðréttingahólf uppfærð.  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a>Vöruhúsaleiðréttingar í birgðahöfuðbók  
 Glugginn **birgðabók** og aðgerðin **Reikna vöruhúsaleiðréttingu** eru notuð til að jafna birgðir í birgðabók samkvæmt leiðréttingu sem hefur verið gerð á birgðamagni í vöruhúsahólfi. Til að búa til tengil á milli birgða og vöruhúss, verður þú að skilgreina aðlögun sjálfgefið hólf á staðsetningu.  
  
 Sjálfgefið leiðréttingarhólf skráir vörur í vöruhús þegar birgðaaukning er bókuð. Hins vegar, ef þú bókar lækkun minnkar einnig magn í sjálfgefnu hólfi. Í báðum tilvikum, eru birgðahöfuðbókarfærslur og vöruhúsafærslur stofnaðar.  
  
> [!NOTE]  
>  Leiðréttingarhólfið er ekki innifalið í framboðsútreikningi.  
  
 Ef stilla á innihald hólfs er hægt að nota vöruhúsabirgðabókina þar sem hægt er að færa inn vörunúmer, svæðiskóða, hólfkóða og magn sem á að stilla.  
  
 Ef jákvætt magn er slegið inn og línan bókuð aukast birgðir sem geymdar eru í hólfinu og magnið í sjálfgefna leiðréttingarhólfinu minnkar að sama skapi.  
  
## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)   
 [Hönnunarupplýsingar: Framboð í vöruhúsi](design-details-availability-in-the-warehouse.md)
