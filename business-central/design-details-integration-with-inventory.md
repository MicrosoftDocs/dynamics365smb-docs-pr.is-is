---
title: Hönnunarupplýsingar - Sameining með birgðum
description: Vöruhúsakerfi og birgðakerfishluti vinna saman í efnislegum birgðum og í leiðréttingum á birgðum eða vöruhúsi.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-integration-with-inventory"></a>Hönnunarupplýsingar: Sameining með birgðum

Vöruhúsakerfi og birgðaaðgerðir hafa samskipti við aðra í raunbirgðum og birgða- eða vöruhúsaleiðréttingum.  

## <a name="physical-inventory"></a>Raunbirgðir

Síðan **Vöruh. - raunbirgðabók** er notaður með glugganum **Raunbirgðabók** fyrir allar ítarlegar staðsetningar vöruhúss. Birgðir á hólfastigi eru reiknaðar úr og útprentaður listi afhendur starfsmanni vöruhúss. Listinn sýnir hvaða vörur í hvaða hólfum þarf að telja.  
  
Starfsmaður vöruhússins slær inn reiknað magn síðuna **Vöruh. - raunbirgðabók** og bókar svo færslubókina.  
  
Ef talið magn er meira en magn á færslubókarlínu er hreyfing bókuð fyrir þennan mun á milli sjálfgefna leiðréttingarhólfsins og talda hólfsins. Þetta eykur magnið í talda hólfinu og minnkar magnið í sjálfgefna leiðréttingarhólfinu.  
  
Ef talið magn er minna en magnið á færslubókarlínunni er hreyfing fyrir þennan mun bókuð frá talda hólfinu í sjálfgefna leiðréttingarhólfið. Þetta lækkar magnið í talda hólfinu og eykur magnið í sjálfgefna leiðréttingarhólfinu.  
  
Í háþróaður vörugeymsla, gildi í **Magn reiknað** sviði er sótt frá birgðahöfuðbókarfærslur og gildi í **Magn raunverulegt magn á lager** reitur er sótt frá vöruhúsi færslum, að undanskildum jöfnunarhólfainnihaldi. Reiturinn **Magn** tilgreininn mismuninn á milli fyrstu reitanna tveggja, sem ætti að vera jafn innihaldinu í leiðréttingarhólfinu.  
  
Þegar þú bókar efnisbirgðabók eru birgðir og sjálfgefið leiðréttingahólf uppfærð.  

[!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]
  
## <a name="warehouse-adjustments-to-the-item-ledger"></a>Vöruhúsaleiðréttingar í birgðahöfuðbók

Síðan **birgðabók** og aðgerðin **Reikna vöruhúsaleiðréttingu** er notuð til að jafna birgðir í birgðabók samkvæmt leiðréttingu sem hefur verið gerð á birgðamagni í vöruhúsahólfi. Til að búa til tengil á milli birgða og vöruhúss, verður þú að skilgreina aðlögun sjálfgefið hólf á staðsetningu.  
  
Sjálfgefið leiðréttingarhólf skráir vörur í vöruhús þegar birgðaaukning er bókuð. Hins vegar, ef þú bókar lækkun minnkar einnig magn í sjálfgefnu hólfi. Í báðum tilvikum, eru birgðahöfuðbókarfærslur og vöruhúsafærslur stofnaðar.  
  
> [!NOTE]  
> Birgðaútreikningar innihalda ekki leiðréttingarhólfið.  
  
Til að leiðrétta innihald hólfs er birgðabók vöruhúss notuð þar sem hægt er að færa inn vörunúmer, svæðiskóta, hólfakóta og magn til leiðréttingar.  
  
Ef jákvætt magn er slegið inn og línan bókuð aukast birgðir sem geymdar eru í hólfinu og magnið í sjálfgefna leiðréttingarhólfinu minnkar að sama skapi.  
  
## <a name="see-also"></a>Sjá einnig

[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)  
[Hönnunarupplýsingar: Framboð í vöruhúsi](design-details-availability-in-the-warehouse.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
