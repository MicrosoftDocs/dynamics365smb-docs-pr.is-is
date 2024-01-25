---
title: Kynning á Contoso kaffi
description: Yfirlit yfir aðstæður fyrir hvernig Contoso Coffee kynningargögn geta hjálpað þér að læra hvernig á að nota vörugeymslumöguleikana í Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: 4764
author: brentholtorf
ms.author: bholtorf
---

# <a name="introduction-to-contoso-coffee-warehousing"></a>Kynning á Contoso kaffigeymslu

Contoso Coffee er skáldað fyrirtæki sem framleiðir kaffivélar fyrir neytendur og fyrirtæki.  **Contoso Coffee** öppin fyrir Business Central bæta við kynningargögnum sem þú getur notað til að læra hvernig á að nota vörugeymslumöguleikana í Business Central. Þú getur stillt vöruhúseiginleika á ýmsa vegu, sjá [Yfirlit yfir mismunandi stillingarvalkosti](../../design-details-warehouse-management.md#overview-of-different-configuration-options).

Forritið býður upp á þrjár staðsetningar sem eru fínstilltar fyrir mismunandi aðstæður:

- **SILFUR**  

  Þessi staðsetning stillt til að nota hólf. Það er auðvelt að stilla það til að styðja grunn eða háþróaða. 

- **GULT**  

  Þessi staðsetning notar háþróaða vöruhúsastillingu, en notar ekki hólf. Það er hægt að endurstilla það til að styðja grunnstillingar.

- **HVÍTUR**  

  Þessi staðsetning notar háþróaða vöruhúsastillingu með beint frágangi og vali, sem gerir ítarlegri reglur um hvernig hlutir flytjast um vöruhús.

## <a name="set-up-contoso-coffee-warehousing-data"></a>Settu upp Contoso Coffee Warehousing gögn

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

Þegar viðeigandi öpp hafa verið sett upp skaltu fara á [Contoso Demo Tool](https://businesscentral.dynamics.com/?page=5194) síðuna í [!INCLUDE [prod_short](../../includes/prod_short.md)], velja *Warehouse Module* línan og notaðu **Configure** aðgerðina til að undirbúa einingarnar. Eftirfarandi töflur lýsa stillingunum.  

|Svæði  |Heimildasamstæða  |
|---------|---------|
|**Staðsetning Bin**  |Staðsetningin sem á að nota fyrir helstu staðsetningaratburðarás.|
|**Staðsetning Ítarleg**  |Staðsetningin til að nota fyrir einfaldar skipulagssviðsmyndir.|
|**Staðsetningarstýrt frágangi og vali**  |Staðsetningin til að nota fyrir háþróaða flutningasviðsmyndir.|
|**Staðsetning í flutningi**  |Staðsetningin sem á að nota fyrir flutningsstaðsetningu í flutningsatburðarás.|
|**Viðskiptavinur nr.**  |Viðskiptavinurinn til að nota fyrir grunn og einföld atburðarás í sölustarfsemi.|
|**Seljandi nr.**  |Seljandinn sem á að nota fyrir allar aðstæður í innkaupaaðgerðum.|
|**Liður 1 nr.**  |Aðalatriðið til að nota fyrir allar aðstæður.|
|**Liður 2 nr.**  |Aukahluturinn til að nota fyrir allar aðstæður.|
|**Liður 3 nr.**  |Atriðið með rakningu.|

Þegar allt er til reiðu skaltu velja aðgerðina **Búa til sýnigögn**. Það tekur nokkrar mínútur að bæta gögnunum við undirliggjandi gagnagrunn en eftir það er allt til reiðu til að keyra ýmsar aðstæður.  

> [!IMPORTANT]
> Ef þú ert að keyra sviðsmyndirnar gætirðu viljað staðfesta að notandanum þínum hafi verið bætt við eins og á völdum stöðum. Fyrir frekari upplýsingar, sjá [Setja upp starfsmenn í vöruhúsum](../../warehouse-how-to-set-up-warehouse-employees.md).

## <a name="scenarios"></a>Dæmi

Sýningargögn Contoso Coffee vörugeymsla styðja eins og er eftirfarandi aðstæður fyrir próf og þjálfun:

1.  [Farið yfir inn- og útstreymi í grunnstillingum vöruhúsa](warehouse-basic-flow-putaway-pick.md)
2.  [Yfirferð á inn- og útstreymi í blönduðum vöruhúsastillingum](warehouse-mixed-flow-receive-pick-ship.md)
3.  [Yfirferð á inn- og útstreymi í háþróaðri vöruhúsastillingu með beint frágangi og vali](warehouse-directed-flow.md)

Lestu skrefin fyrir hverjar aðstæður í viðkomandi grein.  

## <a name="see-also"></a>Sjá einnig .

[Uppsetning birgða](../../inventory-setup-inventory.md) 
[Hvernig á að setja upp staðsetningar](../../inventory-how-setup-locations.md) 
[Vörugeymsla](../../warehouse-manage-warehouse.md) 
[Hönnunarupplýsingar](../../design-details-warehouse-overview.md) 
