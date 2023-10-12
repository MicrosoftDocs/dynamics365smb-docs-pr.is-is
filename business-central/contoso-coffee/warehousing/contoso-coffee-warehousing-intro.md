---
title: Kynning á contoso Coffee
description: Yfirlit yfir Aðstæður fyrir hvernig contoso kaffi sýnikennsla getur auðveldað þér að læra hvernig hægt er að nýta vöruhúsaggetu í viðskiptum miðsvæðis.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4764
author: brentholtorf
ms.author: bholtorf
---

# <a name="introduction-to-contoso-coffee-warehousing"></a>Kynning á contoso Coffee Vöruhúsnæðinu

Contoso Coffee er skáldað fyrirtæki sem framleiðir kaffivélar fyrir neytendur og fyrirtæki.  **Útinnandi kaffiforrit**  fyrir fyrirtæki seðlabankar bæta við sýnigögnum sem nota má til að læra hvernig hægt er að nýta sér Vöruhúsagetu í viðskiptum miðsvæðis. Hægt er að skilgreina vöruhúsaaðgerðir á ýmsa vegu, sjá  [Yfirlit yfir mismunandi skilgreiningarvalkosti](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

Í App eru þrjár staðsetningar sem eru bestar fyrir mismunandi atburðarás:

- **SILFUR**  

  Þessi staðsetning samskipar að nota hólf. Auðvelt getur verið að skilgreina hann til að styðja undirstöðu eða Ítarlegt. 

- **GULT**  

  Þessi staðsetning notar ítarlegri skilgreiningu vöruhúss en notar ekki hólf. Hægt er að endurskilgreina hana til að styðja grunnskilgreiningar.

- **HVÍTT**  

  Þessi staðsetning notar ítarlega samstillingu vöruhússins með beinum frágangi og tínslu, sem gerir ítarlegri reglur um hvernig vörur eru færðar í öllu vöruhúsi.

## <a name="set-up-contoso-coffee-warehousing-data"></a>Setja upp contoso Coffee Vöruhúsgagnagerð

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

Þegar viðeigandi forrit eru sett upp þarf að fara á  [síðuna contoso demo](https://businesscentral.dynamics.com/?page=5194)  í  [!INCLUDE [prod_short](../../includes/prod_short.md)], velja  *línu vöruhúsaeiningar*  og nota  **samskipanaraðgerðina**  til að undirbúa einingarnar. Eftirfarandi töflur lýsa stillingunum.  

|Svæði  |Heimildasamstæða  |
|---------|---------|
|**Birgðageymsla bí**  |Staðsetning til nota fyrir helstu aðstæður á staðnum.|
|**Ítarlegar staðsetningar**  |Staðsetningin til að nota við að einfalda vörustjórnunaraðstæður.|
|**Staðsetning beinn frágangur og tínsla**  |Staðsetningin til að nota fyrir ítarlegar aðstæður vörustjórnunar.|
|**Staðsetning í flutningi**  |Staðsetning til að nota fyrir innsendingarstað í flutningsáætlunum.|
|**Viðskiptamaður nr.**  |Viðskiptavininn til að nota til grundvallar og einfaldrar atburðarásar í söluaðgerðum.|
|**Nr. lánardrottins**  |Lánardrottinn sem nota á fyrir allar áætlanir í innkaupaaðgerðum.|
|**Liður 1 nr.**  |Aðalatriðið til að nota við allar aðstæður.|
|**Liður 2 nr.**  |Aukavaran sem nota á fyrir allar aðstæður.|
|**Liður 3 nr.**  |Atriðið við mælingar.|

Þegar allt er til reiðu skaltu velja aðgerðina **Búa til sýnigögn**. Það tekur nokkrar mínútur að bæta gögnunum við undirliggjandi gagnagrunn en eftir það er allt til reiðu til að keyra ýmsar aðstæður.  

> [!IMPORTANT]
> Ef verið er að keyra atburðarásina kann að vera hægt að sannreyna að notandanum hafi verið bætt við hana á völdum stöðum. Frekari upplýsingar er að finna  [í setja upp starfsmenn](../../warehouse-how-to-set-up-warehouse-employees.md) vöruhúss.

## <a name="scenarios"></a>Dæmi

Contoso Coffee vöruhúsgögnunum sýnigögn sem nú styðja við eftirfarandi Aðstæður til prófs og þjálfunar:

1.  [Ganga frá innflæði á innleið og útleið í grunnstillingum vöruhúss](warehouse-basic-flow-putaway-pick.md)
2.  [Vasaljós á inn-og útrennsli í Blönduðum Vöruhúsaleiðingum](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Ganga frá inn-og útstreymissútflæði í ítarlegri samskipan vöruhúss með beinan frágang og tínslu](warehouse-directed-flow.md)

Lestu skrefin fyrir hverjar aðstæður í viðkomandi grein.  

## <a name="see-also"></a>Sjá einnig .

[Setting Up Inventory](../../inventory-setup-inventory.md) 
[How to Setup Locations](../../inventory-how-setup-locations.md) 
[Warehousing](../../warehouse-manage-warehouse.md) 
[Design Details](../../design-details-warehouse-overview.md) 
