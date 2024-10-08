---
title: Stemma af bankareikninga og jafna greiðslur
description: 'Útskýrir verkhluta sem fela í sér afstemmingu bankareikninga, krafna og skulda reikninga, bókanir inngreiðslna og útgjalda og sjálfvirka greiðslujöfnun.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '1290, 1291, 1293, 1294'
ms.date: 07/25/2024
ms.service: dynamics-365-business-central
---

# <a name="apply-payments-automatically-and-reconciling-bank-accounts"></a>Jafna greiðslur sjálfvirkt og afstýra bankareikningum
Þú verður að reglulega samræma bankareikninga þína, kröfur og skuldir reikninga með því að sækja greiðslur skráð í bankanum til tengdra (ógreiddra) reikninga og lánshæfiseinkunnana eða annarra opna færslna í [!INCLUDE[prod_short](includes/prod_short.md)].  

Þú getur gert þetta verkefni á síðunni **Greiðsluafstemmingarbók**, til dæmis með því að flytja inn bankayfirlitsskrá eða straum til að skrá greiðslurnar fljótt. Greiðslur eru beittar til að opna viðskiptavinar- eða seljanda bókasafns færslur sem eru byggðar á samsvörun milli greiðslustaðs og upplýsinga um innganga. Hægt er að skoða og breyta sjálfvirk jafnanir áður en færslubókin er bókuð. Þú getur valið að loka öllum opnum bankareikningsfærslum sem tengjast jöfnuðu fjárhagsfærslunum þegar þú bókar færslubókina. Bankareikningurinn er sjálfkrafa sáttur þegar allar greiðslur eru sóttar.

Á síðunni **Greiðslujöfnunarreglur** er hægt að setja upp forgangsraðaðar reglur sem stjórna því hvernig greiðslutexti er sjálfkrafa jafnaður við færsluupplýsingar.

Einnig er hægt að afstemma bankareikninga án þess að greiðslujafna samtímis. Þetta verk er framkvæmt á síðunni **Afstemming bankareiknings**. Frekari upplýsingar er að finna í [Afstemma bankareikninga](bank-how-reconcile-bank-accounts-separately.md).

Til að flytja inn bankareikninga sem bankafæða þarftu fyrst að setja upp og virkja Envestnet Yodlee Bank Feed þjónustu og síðan tengja bankareikninga þína við tengda bankareikninga. Nánari upplýsingar eru [í Envestnet Yodlee bankastraumsþjónustan](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Einnig er hægt að flytja inn bankayfirlitsskrár á sniði kommu eða semíkommu (.CSV). Notið **Setja upp snið bankayfirlitsskráar** uppsetninguna með hjálp til að skilgreina innflutningssnið bankayfirlits og festa sniðið við bankareikning. Síðan er hægt að nota þessi snið þegar bankayfirlit er flutt inn á síðuna **Afstemming bankareiknings**.

Einnig er hægt að nota AMC Banking 365 Fundamentals viðbótina til að umbreyta bankayfirliti sem þú fékkst úr bankanum þínum í gagnastraum sem hægt er að flytja inn í [!INCLUDE[prod_short](includes/prod_short.md)]. Nánari upplýsingar eru [í AMC-bankakerfinu 365 grundvallarviðbót](ui-extensions-amc-banking.md).  

Eftirfarandi tafla lýsir röð verkefna með tenglum í greinar þar sem þeim er lýst.  

| Til | Sjá |
| --- | --- |
| Jafna greiðslur við opnar viðskiptamanna- eða lánardrottnafærslur með því að flytja inn bankayfirlit og stemma svo bankareikninginn af eftir að allar greiðslur hafa verið jafnaðar. |[Afstemma greiðslur með sjálfvirkri jöfnun](receivables-how-reconcile-payments-auto-application.md) |
| Jafnaðu greiðslur handvirkt með því að skoða ítarlegar upplýsingar um samsvöruð gögn og tillögur um mögulegar færslur til að jafna greiðslur á. |[Endurskoða eða sækja um greiðslur eftir sjálfvirkan umsókn](receivables-how-review-apply-payments-auto-application.md) |
| Leysa greiðslur sem ekki er hægt að jafna sjálfkrafa við tengdar opnar færslur. Til dæmis vegna þess að upphæðirnar eru mismunandi eða vegna þess að tengd færsla er ekki til. |[Stemma af greiðslur sem ekki er hægt að jafna sjálfvirkt](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Tengja skal texta á greiðslum við tiltekinn viðskiptamanns-, lánardrottins- eða fjárhagsreikning til að bóka alltaf endurtekna móttöku eða útgjöld reiðufés á þá reikninga þegar engin skjöl eru til til að beita þessu. |[Varpa texta um endurteknar greiðslur í reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
|Setja upp reglurnar til að stjórna því hvernig greiðslur/bankafærslur eiga að vera sjálfkrafa jafnaðar við tengdar opnar fjárhagsfærslur þegar þú notar aðgerðina **Notað sjálfkrafa** á síðunni **Greiðsluafstemmingarbók**.|[Reglur settar upp fyrir sjálfvirka jöfnun á greiðslum](receivables-how-set-up-payment-application-rules.md)|

## <a name="see-also"></a>Sjá einnig .
[Afstemma bankareikninga](bank-how-reconcile-bank-accounts-separately.md)  
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
