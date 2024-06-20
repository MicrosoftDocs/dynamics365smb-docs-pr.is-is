---
author: brentholtorf
ms.topic: include
ms.date: 09/21/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

Starfsmenn í vöruhúsi geta sent og tekið á móti vörum sem ekki eru í birgðum ásamt efnislegum vörum á sölu- og innkaupapöntunum. Vörur sem ekki eru í birgðum eru óáþreifanlegar, t.d. vátrygging eða aukakostnaður.

Sölu- og innkaupapantanir eru oft með ýmsar tegundir hluta í línunum. Pantanir geta til dæmis falið í sér fjárhagsvörur, reikninga og eignir. Ef vöruhúsaskjöl eru notuð til að meðhöndla raunvörur er einnig hægt að bóka nokkrar tegundir vara sem ekki eru í birgðum. Eftirfarandi eru dæmi um vöruhúsaskjöl:

* Birgðafrágangur
* Vöruhúsamóttökur
* Birgðatínslur
* Vöruhúsaafhendingar

Ef gera á starfsmönnum vöruhúss kleift að senda og taka á móti vörum sem ekki eru í birgðum skal fylla út reitinn **Sjálfvirk bókun óbirgða í vöruhúsi.** á síðunum **Sölugrunnur og** Innkaupagrunnur **·** . Í reitnum eru eftirfarandi valkostir:

|Valkostur  |Heimildasamstæða  |
|---------|---------|
|Engin     |Ekki á að afhenda eða taka á móti vörum sem ekki eru í birgðum.         |
|Hengt við/úthlutað     | Bóka kostnaðarauka og aðrar vörulínur sem ekki eru í birgðum sem eru tengdar eða tengdar efnislegum vörum. Til að tengja línur sem ekki eru í birgðum við efnislegar vörur skal nota aðgerðina **Tengja við birgðalínu** .        |
|Allt     | Bóka allar línur sem ekki eru í birgðaskrá í upprunaskjalinu um leið og að minnsta kosti ein vara er bókuð af vöruhúsaskjalinu.        |

> [!NOTE]
> Valkosturinn **Ljúka** í reitnum **Fyrirmæli** um afhendingu í sölupöntuninni hefur forgang yfir valinu í reitnum **Sjálfvirk bókun óbirgða í vöruhúsi.** á síðunni **Sölugrunnur** .