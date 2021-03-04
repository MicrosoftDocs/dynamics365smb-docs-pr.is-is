---
title: Hönnunarupplýsingar - Sameining með birgðum | Microsoft Docs
description: Hlutarnir Vöruhúsakerfi og Birgðir vinna saman í efnislegum birgðum og leiðréttingu birgða eða vöruhúss.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7e1b7a922109155471c212d688ce3ab468977deb
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922118"
---
# <a name="design-details-integration-with-inventory"></a>Hönnunarupplýsingar: Sameining með birgðum
Hlutarnir Vöruhúsakerfi og Birgðir vinna saman í efnislegum birgðum og leiðréttingu birgða eða vöruhúss.  
  
## <a name="physical-inventory"></a>Birgðir  
 Síðan **Vöruh. - raunbirgðabók** er notaður með glugganum **Raunbirgðabók** fyrir allar ítarlegar staðsetningar vöruhúss. Birgðir á hólfastigi eru reiknaðar úr og útprentaður listi afhendur starfsmanni vöruhúss. Listinn sýnir hvaða vörur í hvaða hólfum þarf að telja.  
  
 Starfsmaður vöruhússins slær inn reiknað magn síðuna **Vöruh. - raunbirgðabók** og bókar svo færslubókina.  
  
 Ef talið magn er meira en magn á færslubókarlínu er hreyfing bókuð fyrir þennan mun á milli sjálfgefna leiðréttingarhólfsins og talda hólfsins. Þetta eykur magnið í talda hólfinu og minnkar magnið í sjálfgefna leiðréttingarhólfinu.  
  
 Ef talið magn er minna en magnið á færslubókarlínunni er hreyfing fyrir þennan mun bókuð frá talda hólfinu í sjálfgefna leiðréttingarhólfið. Þetta lækkar magnið í talda hólfinu og eykur magnið í sjálfgefna leiðréttingarhólfinu.  
  
 Í háþróaður vörugeymsla, gildi í **Magn reiknað** sviði er sótt frá birgðahöfuðbókarfærslur og gildi í **Magn raunverulegt magn á lager** reitur er sótt frá vöruhúsi færslum, að undanskildum jöfnunarhólfainnihaldi. Reiturinn **Magn** tilgreininn mismuninn á milli fyrstu reitanna tveggja, sem ætti að vera jafn innihaldinu í leiðréttingarhólfinu.  
  
 Þegar þú bókar efnisbirgðabók eru birgðir og sjálfgefið leiðréttingahólf uppfærð.  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a>Vöruhúsaleiðréttingar í birgðahöfuðbók  
 Síðan **birgðabók** og aðgerðin **Reikna vöruhúsaleiðréttingu** er notuð til að jafna birgðir í birgðabók samkvæmt leiðréttingu sem hefur verið gerð á birgðamagni í vöruhúsahólfi. Til að búa til tengil á milli birgða og vöruhúss, verður þú að skilgreina aðlögun sjálfgefið hólf á staðsetningu.  
  
 Sjálfgefið leiðréttingarhólf skráir vörur í vöruhús þegar birgðaaukning er bókuð. Hins vegar, ef þú bókar lækkun minnkar einnig magn í sjálfgefnu hólfi. Í báðum tilvikum, eru birgðahöfuðbókarfærslur og vöruhúsafærslur stofnaðar.  
  
> [!NOTE]  
>  Leiðréttingarhólfið er ekki innifalið í framboðsútreikningi.  
  
 Ef stilla á innihald hólfs er hægt að nota vöruhúsabirgðabókina þar sem hægt er að færa inn vörunúmer, svæðiskóða, hólfkóða og magn sem á að stilla.  
  
 Ef jákvætt magn er slegið inn og línan bókuð aukast birgðir sem geymdar eru í hólfinu og magnið í sjálfgefna leiðréttingarhólfinu minnkar að sama skapi.  
  
## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)   
 [Hönnunarupplýsingar: Framboð í vöruhúsi](design-details-availability-in-the-warehouse.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]