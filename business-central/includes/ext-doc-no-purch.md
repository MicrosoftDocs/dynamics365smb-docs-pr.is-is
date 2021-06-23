---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 59376b96dcd6f755040b07784ceca53e157bcf14
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115966"
---
Á innkaupaskjölum og færslubókum er hægt að tilgreina fylgiskjalsnúmer sem vísar til númerakerfis lánardrottins. Notaðu þennan reit til að skrá númerið sem lánardrottinn úthlutaði pöntuninni, reikningnum eða kreditreikningnum. Síðar má nota númerið ef af einhverjum ástæðum þarf að leita að bókaðri færslu með þessu númeri.

Reiturinn **Nr. utanaðk. skjals áskilið** í **Uppsetning innkaupagrunns** síðunni tilgreinir hvort áskilið er að færa inn númer utanaðkomandi skjals við eftirfarandi aðstæður:

* Í **Pöntunarnr. lánardr.** reitinn, **Pöntunarnr. lánardr.** reitinn, eða **Kr.reikn.nr. lánardr.** reitnum á innkaupahaus

* Í reitnum **External Númer ytra fylgiskjals** á færslubókarlínu, þar sem reiturinn **Tegund fylgiskjals** er stilltur á *Reikningur*, *Kreditreikningur* eða *Vaxtareikningur* og reiturinn **Tegund reiknings** er stillt á *Lánardrottinn*.

Ef þú velur þennan reit verður ekki hægt að bóka reikning, kreditreikning eða færslubókarlínur eins og þá sem lýst er hér fyrir ofan án númers utanaðkomandi skjals.

Númer ytra skjals fylgir með í bókuðum skjölum þar sem hægt er að leita eftir viðkomandi númeri. Einnig er hægt að leita eftir númeri ytra skjals þegar leitað er í lánardrottnafærslum.

Önnur leið til að meðhöndla utanaðkomandi skjalanúmer er að nota reitinn **Tilvísunarnúmer notanda**. Ef reiturinn **Tilvísun þín** er notaður verður númerið tekið með í bókuðum skjölum og þú getur leitað eftir því á sama hátt og eftir gildum úr reitum **Nr. ytra skjals**. En reiturinn er ekki tiltækur í færslubókarlínum.
