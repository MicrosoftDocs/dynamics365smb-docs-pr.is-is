---
title: 'Gefa út, prenta, hætta við og ógilda tékka'
description: 'Lýsir því hvernig skal gefa út ávísanir með því að nota greiðslubók, prenta ávísanir og ógilda eða skoða ávísanafjárhagsfærslur í Business Central.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'payment journal, print check, vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256, 404,'
ms.date: 05/07/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="make-check-payments"></a>Framkvæma tékkagreiðslur

Þú getur gefið út rafrænar og handvirkar ávísanir [!INCLUDE[prod_short](includes/prod_short.md)]. Í báðum aðferðum er útgreiðslubók notuð til að gefa út tékka til lánardrottna. Einnig er hægt að ógilda tékka og skoða fjárhagsfærslur.

Eftirfarandi ferli sýnir hvernig á að greiða lánardrottni með tölvuávísunum með því að jafna greiðsluna við viðeigandi reikning lánardrottins, prenta út ávísunina og síðan bóka greiðsluna sem greidda. Þetta leiðir til jákvæðra lánardrottnafærslna, jafnaðar við neikvæðar bankafjárhagsfærslur og raunverulegar ávísanir fyrir úrvinnslu í bankanum.

Hægt er að greiða með tveimur gerðum af ávísunum. Fyrir báðar gerðir verður reiturinn **Mótreikningur nr.** eða **Tegund reiknings** að innihalda **Bankareikning**.

- **Vélfærður tékki**: veldu þennan valkost ef  á að prenta tékka með upphæðinni í færslubókarlínunni. Þú þarft að prenta tékkana áður en þú bókar færslubókarlínurnar.
- **Handfærður tékki**  Þessi kostur er valinn ef handfærður tékki hefur verið búinn til og  á að búa til tékkafærslu sem samsvarar upphæðinni. Með því að nota þennan valkost er ekki hægt að prenta út ávísun.

> [!NOTE]  
> Til að ganga úr skugga um að bankinn þinn eingöngu taki við fullgildum ávísunum og upphæðum, geturðu sent þeim skrá sem inniheldur seljanda, ávísun og greiðsluupplýsingar. Nánari upplýsingar er að finna í [Flytja út jákvæða greiðsluskrá](finance-how-positive-pay.md).

> [!IMPORTANT]
> Prentarinn verður að vera rétt stilltur með tékkaeyðublöðum, og þú verður að skilgreina hvaða útlit tékka á að nota. Frekari upplýsingar er að finna í [Velja útlit ávísunar](finance-how-define-check-layouts.md). Að öðrum kosti er t.d. hægt að senda ávísunina sem PDF-skrá.  

Hægt er að prenta allt að 10 reikninga á síðu fyrir ávísanabút. Ef ávísun á við um meira en 10 reikninga, ógildum við stubbinn á fyrstu síðunni og prentum orðið ÓGILD á ávísunina þegar þú prentar hana. Við prentum síðan afganginn af reikningunum og heildarupphæð ávísunar á seinni blaðsíðunni.

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a>Til að greiða reikning lánardrottins með vélfærðum tékka

Eftirfarandi dæmi sýnir hvernig á að greiða lánardrottni með ávísun. Skrefin eru svipuð og endurgreiðsla til viðskiptamanns með ávísun.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðslubækur** og velja síðan viðkomandi tengil.
2. Fyllið út greiðslubókarlínurnar. Nánari upplýsingar eru í [Skrá greiðslur og endurgreiðslur](payables-how-post-payments-refunds.md).
3. Í reitnum **Kóði greiðslumáta** skal velja **Ávísun**.
4. Í reitnum **Tegund bankagreiðslu** skal velja **Vélfærður tékki**.
5. Veldu aðgerðina **Prenta ávísun**.
6. Á síðunni **Athuga** skal fyllt í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Ef prentarinn er settur upp til að prenta ávísanir skal velja hnappinn **Prenta**. Veldu hnappinn **Senda til**, veldu valkostinn **PDF-skjal** og veldu síðan hnappinn **Í lagi** og prentaðu út PDF-skjalið.

    Þá er hægt að senda efnislegar ávísanir á lánardrottna til úrvinnslu. Haltu áfram að bóka greiðsluna eins og hún er jöfnuð við lánardrottin og þar af leiðandi greidd í kerfinum.
8. Valið er **Bóka** aðgerðin.

Lánardrottnafærslur og fjárhagsfærslur sem eru jafnaðar að fullu eru stofnaðar.

> [!NOTE]  
> Ef þarf að prenta og greiða tékka í fleiri en einum gjaldmiðli frá mismunandi bankareikningum verður að keyra keyrsluna **Prenta tékka** sérstaklega fyrir hvern gjaldmiðil og tilgreina réttan bankareikning.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Til að ógilda prentaðan tékka sem ekki eru bókaðar

Hægt er að ógilda tékka sem eftir á að bóka þegar þær hafa verið prentuð með því að nota **Ógildur tékki** aðgerðina á síðunni **Greiðslubók**.

1. Á síðunni **Greiðslubók** er valið **Ógildur tékki** og síðan valið hvaða tékka á að ógilda.

## <a name="to-void-checks"></a>Tékkar ógiltir:

Þegar tékkagreiðslur hafa verið bókaðar, geturðu aðeins afturkallað (ógilt) tékka úr bankafærslum sem fengust út úr þessu.

> [!IMPORTANT]
> Ef ávísunin er jöfnuð á reikning, skal fyrst hætta við val hennar fyrst svo að hægt sé að greiða reikninginn og ógilda síðan ávísunina. Ef ávísunin var prentuð og ekki notuð til að greiða reikning skaltu velja **Eingöngu ógilda ávísun** eins og lýst er í þessum hluta.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikningar** og velja síðan viðkomandi tengil.
2. Veldu viðeigandi bankareikning, veldu **breyta** aðgerðina og veldu síðan **tékkafærslur** aðgerðina.
3. Á síðunni **Tékkafærslur** skal velja aðgerðina **Ógildur tékki**.
4. Veldu gátreitinn **eingöngu ógilda tékka**.
5. Velja hnappinn **Í lagi**.

## <a name="to-view-a-summary-of-posted-checks"></a>Til að skoða samantekt bókaðra tékka

Ef þú vilt endurskoða bókaða tékka, til dæmis til að staðfesta marga greidda tékka til eins lánardrottins, getur þú notað skýrsluna **Bankareikningur - Upplýsingar um tékka**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bankareikn. - Upplýsingar um ávísun** og velja síðan viðkomandi tengil.
2. Stilla afmarkanir sem viðeigandi og velja svo hnappinn **Forskoða**.

## <a name="see-also"></a>Sjá einnig .

[Framkvæma greiðslur](payables-make-payments.md)  
[Stjórna skuldum](payables-manage-payables.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Flytja út jákvæða greiðsluskrá](finance-how-positive-pay.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
