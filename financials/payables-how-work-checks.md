---
title: "Hvernig á að: vinna með tékka | Microsoft Docs"
description: "Hvernig á að: vinna með tékka"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6debfe7d1f5e9726ba1f70d023076d73f123ef24
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-work-with-checks"></a>Hvernig á að: vinna með tékka
Þú getur gefið út rafrænar og handvirkar ávísanir [!INCLUDE[d365fin](includes/d365fin_md.md)]. Í báðum aðferðum er útgreiðslubók notuð til að gefa út tékka til lánardrottna. Einnig er hægt að ógilda tékka og skoða fjárhagsfærslur.

Vinnslan sem gefur út tékka stingur upp á greiðslum, býr til fjárhagsfærslur og prentar vélfærðu  tékkana.

**Til athugunar**: Til að ganga úr skugga um að bankinn þinn eingöngu taki fyrir fullgiltum athugunum og magni geturðu sent þeim skrá sem inniheldur seljanda, athugun og greiðsluupplýsingar. Nánari upplýsingar er að finna í [Hvernig á að: flytja út jákvæða greiðsluskrá](finance-how-positive-pay.md).

Prentarinn verður að vera rétt stilltur með tékkaeyðublöðum, og þú verður að skilgreina hvaða útlit tékka á að nota. Nánari upplýsingar sjá [Hvernig á að: Skilgreina útlit tékka:](finance-how-define-check-layouts.md)

## <a name="to-issue-checks"></a>gefa út tékka
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Greiðslubækur**, og velja síðan viðeigandi tengil.
2. Fyllið út færslubók, t.d. með viðeigandi greiðslum, til dæmis með því að nota virknina Greiðslutillögur til lánardrottna. Nánari upplýsingar má sjá í [Hvernig á að: Leggja til greiðslutillögur til lánardrottna](payables-how-suggest-vendor-payments.md).
3. Í reitnum **Tegund Bankagreiðslu** í færslubókarlínunum fyrir greiðslur sem þú vilt gera með tékkum, veldu einn af eftirfarandi valkostum.

   * **Vélfærður tékki**: veldu þennan valkost ef  á að prenta tékka með upphæðinni í færslubókarlínunni. Þú þarft að prenta tékkana áður en þú bókar færslubókarlínurnar. Þú getur eingöngu valið **Vélfærður tékki ** ef **Tegund mótreiknings ** eða **Tegund reiknings ** er **Bankareikningur**.
   * **Handfærður tékki**  Þessi kostur er valinn ef handfærður tékki hefur verið búinn til og  á að búa til tékkafærslu sem samsvarar upphæðinni. Með þessum valkosti er ekki hægt að prenta tékka úr [!INCLUDE[d365fin](includes/d365fin_md.md)] Þú getur eingöngu valið **handfærður tékki ** ef **Tegund mótreiknings ** eða **Tegund reiknings ** er **Bankareikningur**.

     **Athugasemd** : Þarf að prenta vélfærðu tékkana áður en hægt er að bóka tengdu færslubókarlínurnar.
4. Ef um er að ræða vélfærða tékka, veldu **Prenta Tékka**.
5. Í glugganum **ávísun** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Velja hnappinn **Prenta**.

**Athugasemd**: Ef prenta þarf tékka í fleiri en einum gjaldmiðli frá mismunandi bankareikningum verður að keyra keyrsluna **Prenta tékka** sérstaklega fyrir hvern gjaldmiðil og tilgreina réttan bankareikning.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Til að ógilda prentaðan tékka sem ekki eru bókaðar
Hægt er að ógilda tékka sem eftir á að bóka þegar þær hafa verið prentuð með því að nota **Ógilda Tékka** aðgerð í á **greiðslubók** glugga.

1. Í á **greiðslubókarglugga** er valið á **Ógilda Tékka**, og síðan valið hvaða tékka á að ógilda.

## <a name="to-void-checks"></a>Tékkar ógiltir:
Þegar tékkagreiðslur hafa verið bókaðar, geturðu aðeins afturkallað (ógilt) tékka úr bankafærslum sem fengust út úr þessu.

1. Í hægra horni efst skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Bankareikningar**, og velja síðan viðeigandi tengil.
2. Veldu viðeigandi bankareikning, veldu **breyta ** aðgerðina og veldu síðan **tékkafærslur **aðgerðina.
3. Í **tékkafærslur ** glugganum, veldu **ógilda tékka ** aðgerðina.
4. Veldu gátreitinn **eingöngu ógilda tékka**.
5. Velja hnappinn **Í lagi**.

## <a name="see-also"></a>Sjá einnig
[Stjórna skuldum](payables-manage-payables.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Hvernig á að: flytja út jákvæða greiðsluskrá](finance-how-positive-pay.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

