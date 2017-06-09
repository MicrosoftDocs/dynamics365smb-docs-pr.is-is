---
title: "Vinna í færslubókum | Microsoft Docs"
description: "Lærðu hvernig almennar færslubækur er."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/03/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 13257a5d82d742d92fb22da9da7ff7f773d7d2f8
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="working-with-general-journals"></a>Vinna í færslubókum
Þú notar Færslubækur eru til að bóka fjárhagsfærslur og aðra reikninga, svo sem banka-, viðskiptamanna-, lánardrottnareikninga. Bókun með almennri færslubók stofnar alltaf færslur á fjárhagsreikningum. Slíkt á við jafnvel í tilvikum þegar færslubókarlína er bókuð á reikning viðskiptamanns, vegna þess að færsla er bókuð í safnreikning færslubókar með bókunarflokki.

[!INCLUDE[d365fin](includes/d365fin_md.md)] hefur einnig óviðskiptatengdar færslubækur, t.d. í Birgðabók og í Raunbirgðabók, en þessar bækur eru ekki sýnilegar í notandaviðmótinu.

Upplýsingarnar sem eru færðar inn í færslubók eru til bráðabirgða og það er hægt að breyta þeim í færslubókinni. Þegar færslubókin er bókuð, eru upplýsingarnar færðar í færslur á einstökum reikningum, þar sem ekki er hægt að breyta þeim. Það er samt sem áður hægt að ógilda bókaðar færslur og snúa við bókunum eða leiðrétta bókanir.

## <a name="journal-templates-and-batches"></a>Sniðmát færslubóka og keyrslur
Til eru nokkur færslubókarsniðmát. Hvert sniðmát er með sérstakan glugga með ákveðnum aðgerðum og reitum sem verða að styðja aðgerðirnar, eins og **greiðsluafstemmingarbók** glugginn til að vinna bankagreiðslur og **greiðslubók** glugginn til að borga lánardrottnum þínum.

**Til athugunar**: Ef þú flytur út greiðsluskrár í bankann þinn úr greiðslubókinni verður þú að velja **Leyfa greiðsluútflutning** gátreitinn í bókarkeyrslunni í glugganum **Fh. færslubókarkeyrslur**. Nánari upplýsingar sjá [Hvernig: Flytja Greiðslur í bankaskrá](payables-how-export-payments-bank-file.md).

Fyrir hvert sniðmát færslubókar, geturðu sett upp þína eigin færslbók sem bókarkeyrsla. Til dæmis er hægt að skilgreina eigin færslubókarkeyrslu fyrir greiðslubók sem er með þitt persónulega útlit og stillingar.

Dæmi um persónulega stillingu sem þú getur skilgreint á almennum dagbókaratriðum þínum er að kerfið hjálpar þér að fylla upp fjölda sviða. Ef valið er **Leggja til afstemmingarupphæð** gátreitinn á línunni fyrir keyrsla í á **færslubókakeyrslur** glugganum, þá er **Upphæð** reiturinní, t.d. færslubókarlínur fyrir sama skjalnúmer sjálfkrafa forfyllt út með sama gildi sem þarf til að stemma fylgiskjal. Nánari upplýsingar er að finna í [Leyfa [!INCLUDE[d365fin](includes/d365fin_md.md)] að stinga upp á gildum] (ui-let-system-suggest-values.md).

## <a name="main-accounts-and-balancing-accounts"></a>Aðalreikningar og mótreikningar
Ef stofnaðir voru sjálfgefnir mótreikningar fyrir bókakeyrslur, eru mótreikningarnir fylltir út sjálfkrafa þegar fyllt er í reitinn **Reikningur nr** . Að öðrum kosti er fyllt bæði í reitinn **Reikningur nr.** og **Mótreikningur nr.** handvirkt. Jákvæð upphæð í reitnum **Upphæð** er tekin út af aðalreikningnum og lögð inn á mótreikninginn. Neikvæð upphæð er lögð inn á aðalreikninginn og tekin út af mótreikningnum.

**Athugasemd**: VSK er reiknaður út á aðskilin hátt fyrir aðalreikninginn og mótreikninginn, þannig að þar er hægt að nota mismunandi VSK prósentuhlutfall.

## <a name="recurring-journals"></a>Ítrekunarbækur
Ítrekunarbók er færslubók með sérstökum reitum til að stjórna færslum sem eru bókaðar reglulega með litlum eða engum breytingum. Með því að nota þessa reiti fyrir endurteknar færslur er hægt að bóka bæði fastar og breytilegar upphæðir. Einnig er hægt að tilgreina sjálfvirkar bakfærslur daginn eftir bókunardag og nota úthlutunarlykla fyrir ítrekunarfærslur.

## <a name="see-also"></a>Sjá einnig
[Hvernig á að nota úthlutunarlykla í færslubókum](ui-how-use-allocation-keys-general-journals.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

