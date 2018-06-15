---
title: "Gefa út, prenta, hætta við og ógilda ávísanir| Microsoft Docs"
description: "Lýsir því hvernig skal gefa út ávísanir með því að nota greiðslubók, prenta ávísanir og ógilda eða skoða ávísanafjárhagsfærslur í Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: db28ad9a4adb45514b1d1287d269d8daefe64865
ms.openlocfilehash: 39b48fbd34b29db56b39712fbd2cbf5dc91fefc6
ms.contentlocale: is-is
ms.lasthandoff: 04/26/2018

---
# <a name="make-check-payments"></a>Framkvæma ávísanagreiðslur
Þú getur gefið út rafrænar og handvirkar ávísanir [!INCLUDE[d365fin](includes/d365fin_md.md)]. Í báðum aðferðum er útgreiðslubók notuð til að gefa út tékka til lánardrottna. Einnig er hægt að ógilda tékka og skoða fjárhagsfærslur.

Eftirfarandi ferli sýnir hvernig á að greiða lánardrottni með tölvuávísunum með því að jafna greiðsluna við viðeigandi reikning lánardrottins, prenta út ávísunina og síðan bóka greiðsluna sem greidda. Þetta leiðir til jákvæðra lánardrottnafærslna, jafnaðar við neikvæðar bankafjárhagsfærslur og raunverulegar ávísanir fyrir úrvinnslu í bankanum.

Hægt er að greiða með tveimur gerðum af ávísunum. Fyrir báðar gerðir verður reiturinn **Mótreikningur nr.** eða **Tegund reiknings** að innihalda **Bankareikning**.

- **Vélfærður tékki**: veldu þennan valkost ef  á að prenta tékka með upphæðinni í færslubókarlínunni. Þú þarft að prenta tékkana áður en þú bókar færslubókarlínurnar. Þú getur eingöngu valið **Vélfærður tékki** ef
- **Handfærður tékki**  Þessi kostur er valinn ef handfærður tékki hefur verið búinn til og  á að búa til tékkafærslu sem samsvarar upphæðinni. Með því að nota þennan valkost er ekki hægt að prenta út ávísun.

> [!NOTE]  
> Til að ganga úr skugga um að bankinn þinn eingöngu taki við fullgildum ávísunum og upphæðum, geturðu sent þeim skrá sem inniheldur seljanda, ávísun og greiðsluupplýsingar. Nánari upplýsingar er að finna í [Flytja út jákvæða greiðsluskrá](finance-how-positive-pay.md).

Prentarinn verður að vera rétt stilltur með tékkaeyðublöðum, og þú verður að skilgreina hvaða útlit tékka á að nota. Nánari upplýsingar sjá [Skilgreina útlit ávísana](finance-how-define-check-layouts.md)

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a>Til að greiða reikning lánardrottins með vélfærðum tékka
Eftirfarandi dæmi sýnir hvernig á að greiða lánardrottni með ávísun. Skrefin eru svipuð og endurgreiðsla til viðskiptavinar með ávísun.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **greiðslubækur** og velja svo viðeigandi tengil.
2. Fyllið út greiðslubókarlínurnar. Nánari upplýsingar eru í [Skrá greiðslur og endurgreiðslur](payables-how-post-payments-refunds.md).
3. Í reitnum **Kóði greiðslumáta** skal velja **Ávísun**.
4. Í reitnum **Tegund bankagreiðslu** skal velja **Vélfærður tékki**.
5. Veldu aðgerðina **Prenta ávísun**.
6. Í glugganum **ávísun** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Veldu hnappinn **Senda til**, veldu valkostinn **PDF-skjal** og veldu síðan hnappinn **Í lagi**.

    Raunverulegu ávísanirnar er nú hægt að fara með í bankann til vinnslu. Haltu áfram að bóka greiðsluna eins og hún er jöfnuð við lánardrottin og þar af leiðandi greidd í kerfinum.
8. Valið er **Bóka** aðgerðin.

Lánardrottnafærslur og fjárhagsfærslur sem eru jafnaðar að fullu eru stofnaðar.

> [!NOTE]  
> Ef þarf að prenta og greiða tékka í fleiri en einum gjaldmiðli frá mismunandi bankareikningum verður að keyra keyrsluna **Prenta tékka** sérstaklega fyrir hvern gjaldmiðil og tilgreina réttan bankareikning.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Til að ógilda prentaðan tékka sem ekki eru bókaðar
Hægt er að ógilda tékka sem eftir á að bóka þegar þær hafa verið prentuð með því að nota **Ógilda Tékka** aðgerð í á **greiðslubók** glugga.

1. Í á **greiðslubókarglugga** er valið á **Ógilda Tékka**, og síðan valið hvaða tékka á að ógilda.

## <a name="to-void-checks"></a>Tékkar ógiltir:
Þegar tékkagreiðslur hafa verið bókaðar, geturðu aðeins afturkallað (ógilt) tékka úr bankafærslum sem fengust út úr þessu.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bankareikningar** og velja svo viðeigandi tengil.
2. Veldu viðeigandi bankareikning, veldu **breyta** aðgerðina og veldu síðan **tékkafærslur** aðgerðina.
3. Í **tékkafærslur** glugganum, veldu **ógilda tékka** aðgerðina.
4. Veldu gátreitinn **eingöngu ógilda tékka**.
5. Velja hnappinn **Í lagi**.

## <a name="to-view-a-summary-of-posted-checks"></a>Til að skoða samantekt bókaðra tékka
Ef þú vilt endurskoða bókaða tékka, til dæmis til að staðfesta marga greidda tékka til eins lánardrottins, getur þú notað skýrsluna **Bankareikningur - Upplýsingar um tékka**.
1. Velja skal táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið"), slá inn **Bankareikningur - Upplýsingar um tékka** og velja svo viðeigandi tengil.
2. Stilla afmarkanir sem viðeigandi og velja svo hnappinn **Forskoða**.

## <a name="see-also"></a>Sjá einnig
[Framkvæma greiðslur](payables-make-payments.md)  
[Stjórna skuldum](payables-manage-payables.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Flytja út jákvæða greiðsluskrá](finance-how-positive-pay.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

