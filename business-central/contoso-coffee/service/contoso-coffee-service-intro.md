---
title: Kynning á þjónustustjórnun Contoso Kaffi
description: Þessi grein kynnir þér Consoso Coffee sýnikennslugögnin fyrir þjónustustjórnun.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/27/2023
ms.custom: bap-template
---

# <a name="introduction-to-contoso-coffee-service-management"></a>Kynning á þjónustustjórnun Contoso Kaffi

Contoso Coffee er skáldað fyrirtæki sem framleiðir kaffivélar fyrir neytendur og fyrirtæki.  **Contoso Coffee** öppin fyrir Business Central bæta við kynningargögnum sem þú getur notað til að læra hvernig á að nota þjónustustjórnunargetu í Business Central.

Þetta app býður upp á nokkra þætti sem eru notaðir fyrir helstu gönguleiðir:

- Tilföng með úthlutaðri færni
- Hlutir stilltir til að búa til þjónustuvörur
- Lánshlutir

> [!IMPORTANT]
> Áður en þú keyrir einhverjar aðstæður fyrir Contoso Coffee skaltu bóka allar birgðabókarlínur með opnunarstöðum. Fyrir frekari kröfur, sjá [Setja upp Contoso kaffigögn](#set-up-contoso-coffee-service-management-data) hlutann.
>
> 
## <a name="set-up-contoso-coffee-service-management-data"></a>Settu upp Contoso Coffee þjónustustjórnunargögn

[!INCLUDE [contoso-coffee-app-install](../contoso-coffee-app-install.md)].

Þegar viðeigandi öpp hafa verið sett upp skaltu fara á [Contoso Demo Tool](https://businesscentral.dynamics.com/?page=5194) síðuna í [!INCLUDE [prod_short](../../includes/prod_short.md)], velja *Service Module* línan og notaðu **Stilla** aðgerðina til að undirbúa einingarnar. Eftirfarandi tafla lýsir stillingunum:  

|Svæði  |Heimildasamstæða  |
|---------|---------|
|**Viðskiptavinur nr.**  |Viðskiptavinurinn til að nota fyrir atburðarás í sölustarfsemi.|
|**Seljandi nr.**  |Seljandinn sem á að nota fyrir allar aðstæður í innkaupaaðgerðum.|
|**Liður 1 nr.**  |Hluturinn sem á að nota fyrir viðgerðir og viðhald.|
|**Þjónustuliður 1 nr.**  |Atriði af tegund þjónustu til að nota endurgerð atburðarás.|
|**Þjónustuliður 2 nr.**  |Atriði af tegund þjónustu til að nota endurgerð atburðarás.|
|**Heimild 1 nr.**  |Tilfangið sem á að nota fyrir samningssviðsmyndirnar.|
|**Heimild 2 nr.**  |Tilfangið sem á að nota fyrir brot/lagfæringu atburðarás.|
|**Staðsetning þjónustu** |Tilgreinir vöruhúsið sem á að nota fyrir þjónustuaðgerðir. Sjálfgefið er *MAIN*, en þú getur breytt því til að henta þínum þörfum.|

Þegar allt er til reiðu skaltu velja aðgerðina **Búa til sýnigögn**. Það tekur nokkrar mínútur að bæta gögnunum við undirliggjandi gagnagrunn en eftir það er allt til reiðu til að keyra ýmsar aðstæður.  

## <a name="scenarios"></a>Dæmi

Contoso Coffee kynningargögnin styðja eins og er eftirfarandi þjónustusviðsmyndir fyrir próf og þjálfun:

1. Búðu til þjónustupöntun fyrir sérstakar viðgerðarbeiðnir, settu inn og taktu á móti lánveitendum, skráðu tíma og reikningsfærðu viðskiptavini með [Gynningu þjónustupantana fyrir þjónustuvörur](service-basic-flow-order.md)
2. Búðu til þjónustusamninga, búðu til þjónustupantanir, reikningsfærðu samningsgjöld og úthlutaðu tilföngum með [Gynningar um þjónustusamninga fyrir þjónustuvörur](service-contract-flow.md)

Lestu skrefin fyrir hverjar aðstæður í viðkomandi grein.  

> [!IMPORTANT]
> Þjónustuleiðirnar krefjast þess að notendaupplifun sé stillt á **Premium** á  **Fyrirtækisupplýsingum** síðunni.


## <a name="see-also"></a>Sjá einnig .

[Þjónusta](../../service-service.md)
