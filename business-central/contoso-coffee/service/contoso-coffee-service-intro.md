---
title: Kynning á Contoso Coffee þjónustustjórnun
description: Þessi grein kynnir þig á Consoso Coffee sýnikennslugögn fyrir þjónustukerfi.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 11/27/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Kynning á Contoso Coffee þjónustustjórnun

Contoso Coffee er skáldað fyrirtæki sem framleiðir kaffivélar fyrir neytendur og fyrirtæki. Contoso-kaffiforritin **fyrir** Business Central bæta við kynningargögnum sem hægt er að nota til að læra hvernig á að nota þjónustukerfismöguleikana í Business Central.

Í forritinu eru nokkrir þættir sem notaðir eru í aðalkynningunum:

- Forði með úthlutaða þekkingu
- Vörur sem eru grunnstilltar til að stofna þjónustuvörur
- Lánsbúnaður

> [!IMPORTANT]
> Áður en þú keyrir einhverjar aðstæður fyrir Contoso Coffee skaltu bóka allar birgðabókarlínur með opnunarstöðum. Nánari kröfur má finna í hlutanum [Setja upp Contoso-kaffigögn](#set-up-contoso-coffee-service-management-data) .
>
> 
## Uppsetning Contoso-kaffiþjónustustjórnunargagna

[!INCLUDE [contoso-coffee-app-install](../../includes/contoso-coffee-app-install.md)]

Þegar viðkomandi forrit hafa verið sett upp er farið á [síðuna Contoso Demo Tool](https://businesscentral.dynamics.com/?page=5194) í [!INCLUDE [prod_short](../../includes/prod_short.md)], línan Þjónustueining *valin* og aðgerðin **Grunnstilla** til að undirbúa einingarnar. Eftirfarandi tafla lýsir stillingunum:  

|Svæði  |Heimildasamstæða  |
|---------|---------|
|**Númer viðskiptamanns**  |Viðskiptavinurinn sem á að nota í dæmum í söluaðgerðum.|
|**Nr. lánardrottins**  |Lánardrottinn sem á að nota fyrir öll dæmi í innkaupaaðgerðum.|
|**Vara 1 nr.**  |Varan sem nota á í viðgerðar- og viðhaldsaðstæðum.|
|**Nr. þjónustuvöru 1**  |Vara af gerðinni þjónusta til að nota endurtekið dæmi.|
|**Nr. þjónustuvöru 2**  |Vara af gerðinni þjónusta til að nota endurtekið dæmi.|
|**Forði 1 nr.**  |Forðinn sem á að nota í tilfellum samninga.|
|**Forði 2 nr.**  |Forðinn sem á að nota fyrir brot/lagfæringar.|
|**Þjónustustaður** |Tilgreinir vöruhúsið sem nota á fyrir þjónustuaðgerðir. Sjálfgildið er AÐALatriði *en hægt er* að breyta því eftir þörfum.|

Þegar allt er til reiðu skaltu velja aðgerðina **Búa til sýnigögn**. Það tekur nokkrar mínútur að bæta gögnunum við undirliggjandi gagnagrunn en eftir það er allt til reiðu til að keyra ýmsar aðstæður.  

## Dæmi

Gögn contoso-kaffisins styðja nú eftirfarandi þjónustuaðstæður til prófunar og þjálfunar:

1. Stofna þjónustupöntun fyrir tilfalningarviðgerðarbeiðni, setja og taka á móti lánsbúnaði, skrá tíma og reikningsfæra viðskiptamenn með [Kynningu á þjónustupöntunum fyrir þjónustuvörur](service-basic-flow-order.md)
2. Stofna þjónustusamninga, búa til þjónustupantanir, reikningsfæra samningsgjöld og úthluta forða með [kynningu á þjónustusamningum fyrir þjónustuvörur](service-contract-flow.md)

Lestu skrefin fyrir hverjar aðstæður í viðkomandi grein.  

> [!IMPORTANT]
> Kynningin á þjónustunni krefst þess að notandaupplifun sé stillt á **Iðgjald** á síðunni **Stofngögn** .


## Sjá einnig .

[Þjónusta](../../service-service.md)
