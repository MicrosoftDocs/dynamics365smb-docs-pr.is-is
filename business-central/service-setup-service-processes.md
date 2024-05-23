---
title: Uppsetning þjónustukerfisferlis
description: Lærðu að setja upp ferli sem hjálpa til við að tryggja að viðskiptamenn séu ánægðir með þjónustu þína.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'service, number sequences, setup, warnings, fee, contracts, warranties'
ms.date: 02/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Grunnstilling þjónustukerfisferlis

Eftirfarandi eru nokkur dæmi um stillingarnar sem hægt er að nota í þjónustukerfisferlum:  
  
* Nokkrar heildarstillingar fyrir ýmis ferli, svo sem viðvaranir, næstu þjónustuútreikningar fyrir þjónustuvörur, upphafsgjald til að meta, stig bilanatilkynninga sem á að nota o.s.frv.  
* Tegundir upplýsinga sem tæknimenn færa inn í þjónustuskjöl. Til dæmis gætirðu þarfnast þeirra til að tilgreina pöntunargerð, upphafs- og endadagsetningar fyrir vinnuna, og tegund vinnu sem var unnin.  
* Sumar sjálfgefnar stillingar fyrir viðbragðstíma og ábyrgðir. Þetta inniheldur sjálfgefinn svartíma fyrir upphafsþjónustu, afsláttarprósentu ábyrgðar fyrir varahluti og laun, og hversu lengi ábyrgðin gildir.  
* Stillingar á samningum, svo sem hámarksfjöldi daga sem hægt er að nota fyrir samningsbundnar þjónustupantanir, hvort nota eigi ástæðukóta þegar hætt er við samning, staðaltexta fyrir lýsingar og samningsgildi.  
* Talnaraðirnar sem á að nota fyrir þjónustutengd skjöl og vörur.  

## Að færa inn almennar og áskildar stillingar

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning þjónustustjórnunar** og svo velja viðeigandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Setja upp bókunarreglur þjónustureikninga fyrir notendur

Fyrirtæki hafa oft einstaka vinnslu fyrir reikninga og afhendingar. Vinnslur geta til dæmis verið breytilegar frá einum einstaklingi sem bókar allt í þjónustupöntun á marga starfsmenn, hver vinnur með sínar eigin síður.

Hægt er að nota bókunarreglur til að hindra notendur við bókun þjónustureikninga eða krefjast þess að þeir bóki reikninga ásamt tengdri þjónustuafhendingu. Til að setja upp bókunarreglu skal á síðunni **Notandauppsetning** í reitnum **Bókunarregla** þjónustureikninga velja einn af eftirfarandi valkostum:

* **Leyfð** (sjálfgefið): Halda skal gildandi hegðun þar sem hægt er að velja bókunarvalkosti, svo sem **Afhenda**, **Reikningsfæra** og **Afhenda og reikningsfæra**.
* **Bannað**: Komið í veg fyrir að fólk bóki þjónustureikninga. [!INCLUDE [prod_short](includes/prod_short.md)] birtir staðfestingarsvarglugga sem gefur aðeins kostinn **Afhenda** .
* **Áskilið**: Gera fólki kleift að bóka reikninga ásamt þjónustuafhendingum. [!INCLUDE [prod_short](includes/prod_short.md)] birtir staðfestingarsvarglugga sem gefur aðeins kostinn **Afhenda og reikningsfæra** .

Þessi stilling hefur áhrif á eftirfarandi skjöl:

* Þjónustupantanir
* Vöruhúsaafhendingar
* Þjónustureikningar
* Þjónustukreditreikningar

Eftirfarandi tafla lýsir áhrifum ólíkra skjala.

|Skjal  |Leyfa<br>Birtir raðir valkosta   |Bannað<br>Samræmingarsvargluggi  |Áskilið<br>Staðfestingarsvargluggi  |
|---------|---------|---------|---------|
|Þjónustupöntun     | *Skip<br>*Reikning<br>* Afhenda og reikningsfæra<br>* Afhenda og nota         |*Skip<br>* Afhenda og nota  |Á að bóka afhendinguna og reikninginn?         |
|Vöruhúsaafhending     |*Skip<br>* Afhenda og reikningsfæra         |Á að bóka afhendinguna?         | Á að bóka afhendinguna og reikninginn?        |
|Þjónustureikningur     | Á að bóka reikninginn?         | Villa: ekki er hægt að bóka.       |Á að bóka reikninginn?         |
|Þjónustukreditreikningur     | Á að bóka kreditreikninginn?         | Villa: ekki er hægt að bóka.        |Á að bóka kreditreikninginn?         |

> [!NOTE]
> Þegar þjónustureikningar og kreditreikningar eru bókaðir eru engar bókunarvalkostir. Fylgiskjölin bóka alltaf efnisleg og fjárhagsleg viðskipti saman. Ekki er hægt að bóka þjónustureikninga og kreditreikninga að hluta.

## Sjá einnig .  

[Setja upp bilanatilkynningar](service-how-setup-fault-reporting.md)  
[Setja upp forðaúthlutun](service-how-setup-resource-allocation.md)  
[Setja upp Kóta fyrir Staðlaða þjónustu](service-how-setup-service-coding.md)  
[Setja upp aukakostnað fyrir þjónustu](service-how-setup-service-costs-pricing.md)  
[Setja upp úrræðaleit](service-how-setup-troubleshooting.md)  
[Þjónustukerfi](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
