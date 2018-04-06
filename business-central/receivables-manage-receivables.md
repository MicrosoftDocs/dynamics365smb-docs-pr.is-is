---
title: "Yfirlit yfir umsjónarverkhluta viðskiptakrafna | Microsoft Docs"
description: "Útskýrir verkhluta sem fela í sér umsjón með viðskiptakröfum og jöfnun greiðslna við fjárhagsfærslur viðskiptamanna og lánardrottna."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3ffd3b31dcef871ceb30eae6a041f68a4972b2cb
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="managing-receivables"></a>Stjórnun útistandandi reikninga
Reglulegt skref í fjárhag er að afstemma bankareikninga, sem merkir að þú þarft að jafna greiðslur á viðskiptamann og lánardrottnafærslur til að loka sölureikningum og innkaupakreditreikningum.  

Í [!INCLUDE[d365fin](includes/d365fin_md.md)] einn af hraðustu leiðum til að skrá greiðslur úr gluggann í **Greiðsluafstemmingarbók** með því að flytja inn bankareikningsskrá eða fæða. Greiðslur eru beittar til að opna viðskiptareikninga eða söluaðilum fyrir aðalbókanir á grundvelli gagna sem passa á milli greiðslu texta og færsluupplýsingar. Þú getur skoðað og breytt samsvörununum áður en þú sendir dagbókina og lokaðu færslureikningi bankareiknings fyrir færsluskrá þegar þú sendir dagbókina. Bankareikningurinn er sáttur þegar allar greiðslur eru sóttar.

Það eru hins vegar aðrar handhægar stöður til að sækja greiðslur og afgreiða bankareikninga:  

* **Afstemming bankareikninga** glugginn, sem leyfir þér einnig að skoða færsluskrár. Frekari upplýsingar í [Afstemma Bankareikninga Sérstaklega](bank-how-reconcile-bank-accounts-separately.md).  
* **Greiðsluskráin**, þar sem þú getur sótt um og handvirkt athugað greiðslur sem eru mótteknar sem reiðufé, athugaðu eða bankastarfsemi gegn mynda lista yfir ógreiddar söluskrár. Athugaðu að þessi virkni er aðeins í boði fyrir söluskrá.  
* **Inngreiðslubók**, þar sem þú sendir handvirkt inn kvittanir til viðkomandi aðalbókar, viðskiptavina eða annan reikning með því að slá inn greiðslu línu. Þú getur annaðhvort sótt um kvittun eða endurgreiðslu í eina eða fleiri opna færslur áður en þú sendir inn kvittunarskýrslu dagbókina eða frá aðalbókarfærslunni.  

Annar hluti í stjórnun viðskiptakrafna er að safna útistandandi staða, þar með talið vaxtagjöldum og gefa út innheimtubréf. [!INCLUDE[d365fin](includes/d365fin_md.md)] býður upp á leiðir til að gera það líka. Nánari upplýsingar er að finna í [Innheimta útistandandi skuldir](receivables-collect-outstanding-balances.md).  

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.  

| Til | Sjá |
| --- | --- |
| Jafna greiðslur við opnar viðskiptavina- eða lánardrottnafærslur með því að flytja inn bankayfirlit í formi skjals eða streymis, og afstemma bankareikning þegar allar greiðslur eru jafnaðar. |[Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Jafna greiðslur við opna viðskiptamannafærslur samkvæmt handvirka færslu í lista yfir ógreidd söluskjöl. |[Afstemma greiðslur viðskiptamanna handvirkt úr lista yfir ógreidd söluskjöl](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Bóka inngreiðslur eða endurgreiðslur fyrir viðskiptavini í ínngreiðslubók og jafna við viðskiptamannafærslur, annað hvort úr færslubók eða úr bókuðum fjárhagsfærslum. |[Afstemma greiðslum viðskiptamanns handvirkt](receivables-how-apply-sales-transactions-manually.md) |
| Minna viðskiptamenn á upphæðir á gjalddaga, reikna vexti og álag og stjórna útistandandi kröfum. |[Innheimta útistandandi skuldir](receivables-collect-outstanding-balances.md) |
|Vertu viss um kostnað afgreiddra vara, með því að úthluta viðbótar vörukostnaði, eins og farmur, efnisleg meðhöndlun, tryggingar og flutningar sem fellur til eftir sölu.|[Nota kostnaðarauka til að gera grein fyrir viðbótar viðskiptakostnaði](payables-how-assign-item-charges.md)|
|Hægt er að setja upp vikmörk þannig að kerfið loki reikningi jafnvel þótt greiðsla, að meðteknum afslætti, nái ekki upp í fulla upphæð á reikningnum.|[Unnið með greiðsluvikmörk og greiðsluafsláttarvikmörk](finance-payment-tolerance-and-payment-discount-tolerance.md)|
## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)  
[Stjórna skuldum](payables-manage-payables.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

