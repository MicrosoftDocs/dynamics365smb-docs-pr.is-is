---
title: "Hvernig á að setja upp mælieiningar | Microsoft Docs"
description: "Hægt er að setja upp margar mælieiningar fyrir vöru þannig að hægt sé að úthluta mælieiningum á vöruna."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 01/12/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f6fad390b5b8d209212f20cfca5dfdd5fafd11cc
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-item-units-of-measure"></a>Setja upp mælieiningu vara
Hægt er að setja upp margar mælieiningar fyrir vöru þannig að hægt sé að úthluta mælieiningum til vörunnar í eftirfarandi tilgangi:

- Úthluta grunnmælieiningu á birgðaspjaldi vörunnar til skilgreiningar á því hvernig hún er geymd í birgðum og þjónar sem umbreytigrundvöllur fyrir aðrar mælieiningar.
- Úthluta öðrum mælieiningum til innkaupa, framleiðslu eða söluskjala til skilgreiningar á hversu margar einingar af grunnmælieiningunum eru afgreiddar á sama tíma í ferlinu. Til dæmis er varan hugsanlega keypt á brettum en er notuð í stykkjatali við framleiðslu.

Ef vara er sett á lager eftir einni mælieiningu en framleidd eftir annarri er framleiðslupöntun stofnuð sem notar mælieiningu framleiðslukeyrslu til að reikna út rétt magn íhluta meðan á keyrslunni **Endurnýjun framleiðslupöntunar** stendur. Dæmi um útreikning með mælieiningu framleiðslukeyrslu er þegar framleiddur hlutur er merktur á lager í stykkjum en framleiddur í tonnum. Frekari upplýsingar eru í [Vinna með mælieiningu framleiðslukeyrslu](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).

## <a name="to-set-up-a-unit-of-measure"></a>Til að setja upp mælieiningu
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.
2. Opna spjald vörunnar sem á að setja upp aðra mælieiningu fyrir.
3. Veldu **Mælieining**. Þá birtist glugginn **Mælieiningar vöru**.
4. Ef reiturinn **Grunneining mælingareits** á birgðaspjaldinu er fylltur út, hefur sú mælieining þegar verið sett upp.
5. Valið er **Nýtt** aðgerð. Ný auð lína er sett inn.
6. Í reitnum **Kóði**, setjið inn heiti mælieiningarinnar. Að öðrum kosti skal velja reitinn til að velja úr mælieiningarkóðum í gagnagrunninum.
7. Í reitnum **Magn á mælieiningu**, tilgreinið hversu margar grunnmælieiningar varan inniheldur.
8. Eindurtakið skref 5 til 7 til að setja upp allar aðrar mælieiningar sem nota á í mismunandi ferlum fyrir þessa vöru.

Nú er hægt að nota aðrar mælieiningar í innkaupa-, framleiðslu- og söluskjölum. Frekari upplýsingar er að finna í Hvernig á að færa inn sjálfgefna mælieiningakóða fyrir innkaupafærslur og sölufærslur eða Nota mælieiningakeyrslu framleiðslu.

## <a name="to-set-up-unit-of-measure-translations"></a>Setja upp mælieiningatexta
Þegar selt er til erlendra viðskiptavina er hægt að tilgreina mælieininguna á viðeigandi tungumáli. Þetta er hægt að gera þegar búið er að setja upp nauðsynlega mælieiningatexta.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Mælieiningar** og velja svo viðeigandi tengil.
2. Velja þarf tungumálakóðann sem setja á upp þýðingar fyrir og svo aðgerðina **Þýðingar**.
3. Í reitnum **Tungumálskóti** er felliörin valin til að skoða lista yfir tiltæka tungumálakóta. Valinn er sá tungumálskóti sem setja á inn þýðingu fyrir og síðan er smellt á Í lagi til að afrita kótann í reitinn.
4. Í reitinn **Lýsing** er færður inn viðeigandi texti.
5. Skref 2 til 4 eru endurtekin fyrir þá mælieiningarkóða og tungumál sem setja á inn þýðingar á.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Færa inn sjálfgefna mælieiningarkóða fyrir sölu- og innkaupafærslur
Ef venjulega er keypt eða selt í einingum sem eru aðrar en grunnmælieiningin er hægt að tilgreina sérstakar mælieiningar fyrir innkaup og sölu. Ef gera á þetta verða  **mælieiningar** að vera uppsettar í glugganum  Mælieiningar vöru.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vörur** og velja svo viðeigandi tengil.
2. Opna viðeigandi birgðaspjaldi þar sem á að tilgreina sjálfgefinn mælieiningarkóða fyrir sölu- eða innkaupaeiningu.
3. Fyrir sölu, á flýtiflipanum **Reikningsfærsla**, í reitnum **Sölumælieining** er glugginn **Mælieiningar vöru** opnaður.
4. Fyrir innkaup, á flýtiflipanum **Áfylling**, í reitnum **Innkaupamælieining** er glugginn **Mælieiningar vöru** opnaður.
5. Velja skal kóðann sem setja á upp sem sjálfgefna mælieiningu fyrir sölu eða innkaup og veljið svo hnappinn **Í lagi**.

## <a name="see-also"></a>Sjá einnig
[Vinna með mælieiningu framleiðslukeyrslu](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Stjórnun birgða](inventory-manage-inventory.md)  
[Stjórnun innkaupa](purchasing-manage-purchasing.md)  
[Stjórna sölu](sales-manage-sales.md)    
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
