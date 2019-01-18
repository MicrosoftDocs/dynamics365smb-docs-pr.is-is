---
title: "Yfirlit yfir umsjónarverkhluta viðskiptaskulda| Microsoft Docs"
description: "Útskýrir verkhluta sem felur í sér stjórnun viðskiptaskulda, til dæmis að borga skuldareiganda eða úthluta greiðslum á útleið á fjárhagsfærslur til að loka reikningum eða kreditreikningum."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 11/15/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 9bc4eaf292c20c1525c499cde715964eb6e6631f
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="managing-payables"></a>Stjórna skuldum

Stór hluti af stjórnun viðskiptaskulda er að borga lánardrottnum þínum eða endurgreiða starfsmönnum útgjöld. Þú getur notað aðgerðir til að bæta við greiðslumörkum fyrir innkaupareikninga sem eru komnir á gjalddaga á síðunni **Greiðslubók**. Til að senda viðskipti í bankann þinn, getur þú flutt margar greiðslubókalínur í skrá og síðan hlaðið skránum inn í bankann þinn. Einnig er hægt að framkvæma greiðslur með tékka, þar með talið senda tékka sem rafræn greiðsla

Annar dæmigerður verkefni er að jafna útgjöld við tengdar fjárhagsfærslur lánardrottna og starfsmanna, til þess að loka innkaupareikningum, innkaupakreditreikningum eða starfsmannareikningnum sem greiddir. Þú getur gert þetta á síðunni **Greiðsluafstemmingarbók** með því að flytja inn bankareikningsskrá til að skrá greiðslur. Greiðslurnar eru jafnaðar við opinn lánardrottinn, viðskiptamann eða starfsmanna fjárhagsfærslur með því að láta greiðslu texta og færsluupplýsingar passa saman. Það eru ýmsar leiðir til að skoða og breyta leikjunum áður en þú sendir dagbókina. Þú getur valið að loka öllum opnum bankareikningsfærslum sem tengjast jöfnuðu fjárhagsfærslunum þegar þú bókar færslubókina. Bankareikningurinn er sjálfkrafa sáttur þegar allar greiðslur eru sóttar.

Einnig er hægt að jafna greiðslur á útleið handvirkt á síðunni **greiðslubók** eða úr tengdum lánardrottna- eða starfsmanna fjárhagsfærslur.

Í eftirfarandi töflu er lýsing á röð verka  innan viðskiptaskulda með tenglum í efnisatriðin sem lýsa þeim.

| Til | Sjá |
| --- | --- |
| Mynda lánardrottnagreiðslur komnar á gjalddaga eða endurgreiðslur til starfsmanna, undirbúa ávísanagreiðslur og flytja út greiðslur á bankaskrá við bókun. |[Framkvæma greiðslur](payables-make-payments.md) |
| Jafna greiðslur lánardrottna sjálfkrafa við ógreidda innkaupareikninga með því að flytja inn bankayfirlitsskrá. |[Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
|Setja upp vörpun á milli texta í greiðslum og tiltekinni debet-, kredit- og mótreikninga til að greiðslurnar séu bókaðar í tiltekna reikninga þegar greiðsluafstemmingarbók er bókuð.|[Varpa texta um endurteknar greiðslur í reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)|
| Jafna greiðslur lánardrottna handvirkt við ógreidda innkaupareikninga. |[Afstemma greiðslur lánardrottna handvirkt](payables-how-apply-purchase-transactions-manually.md) |
|Jafna greiðslur sjálfkrafa, annaðhvort greiðslur á innleið eða útleið, sem hafa verið skráðar sem færslur á netbankareikningi við tengdar opnar fjárhagsfærslur viðskiptavinar, lánardrottins og bankareiknings. Listinn er búinn til úr bankastraumi eða skrá.|[Afstemma greiðslur með sjálfvirkri jöfnun](receivables-how-reconcile-payments-auto-application.md)|
|Meðhöndla greiðslur handvirkt á bankareikninginn þinn sem ekki er hægt að jafna sjálfvirkt, t.d. vegna þess að ekkert skjal er til þar sem hægt er að jafna greiðsluna á, eða tengda skjalið í hefur aðra fjárhæð en færsluupphæðin, t.d. vegna gjaldeyrismunar.|[Afstemma greiðslur sem ekki er hægt að nota sjálfkrafa](receivables-how-reconcile-payments-cannot-apply-auto.md)|
|Tryggðu rétt birgðamat með því að úthluta viðbótar vörukostnaði, eins og farmur, efnisleg meðhöndlun, tryggingar og flutningar sem viðskipti þín með vörurnar hafa í för með sér.|[Nota kostnaðarauka til að gera grein fyrir viðbótar viðskiptakostnaði](payables-how-assign-item-charges.md)|
|Ef greiða þarf lánardrottni með peningum eða ávísun er hægt að bóka greiðsluna um leið og reikningurinn er bókaður.|[Greiða innkaupareikninga tímanlega](finance-how-to-settle-purchase-invoices-promptly.md)|
|Endurgreiða starfsmönnum fyrir persónuleg útgjöld í viðskiptaerindum með því að greiða inn á bankareikning þeirra.|[Skrá og endurgreiða starfsmannaútgjöld](finance-how-record-reimburse-employee-expenses.md)|

## <a name="see-also"></a>Sjá einnig
[Innkaup](purchasing-manage-purchasing.md)  
[Stjórnun skulda](receivables-manage-receivables.md)  
[Nota kostnaðarauka til að gera grein fyrir viðbótar viðskiptakostnaði](payables-how-assign-item-charges.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

