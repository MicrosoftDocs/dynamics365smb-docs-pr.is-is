---
title: Stjórna afurðarafbrigðum
description: 'Kynntu þér hvernig þú getur skráð vörur sem eru nánast eins en hvað varðar lit, stærð eða efni sem vöruafbrigði.'
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'item, variant, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 09/26/2022
ms.author: edupont
---
# Stjórna afurðarafbrigðum

Vöruafbrigði eru frábær leið til að halda stjórn á lista yfir vörur. Til dæmis gætirðu verið með mikinn vörufjölda sem er nánst eins nema með ólíkan lit. Hægt er að skilgreina hvert afbrigði sem aðskilda vöru. En þú velur að setja upp eina vöru og tilgreina litina sem afbrigði af vörunni.  

> [!TIP]
> Fyrir hagnýta kynningu á því hvernig á að nota afbrigði í framleiðslu skal skoða [Kynning: Afbrigði](contoso-coffee/variants.md) fyrir sýnigögn Contoso Coffee.  

## Bæta afbrigðum við vöru

Ef fyrirtækið þitt hefur ákveðið að nota afbrigði, þá er auðvelt að skilgreina afbrigði fyrir vöru.  

### Til að bæta við afbrigðum

1. Opnaðu [ **Vörulisti** síðuna](https://businesscentral.dynamics.com/?page=31), opnaðu viðkomandi vöru.  
2. Í **Birgðaspjaldinu** skal velja aðgerðina **Vara** og síðan aðgerðina **Afbrigði**.  
3. Á síðunni **Vöruafbrigði** skal gefa upp afbrigðin.  

Þegar söluskjal er búið til og bætt við vöruna er hægt að tilgreina afbrigði vörunnar í reitnum **Afbrigðiskóði**. Það sama á við um innkaupaskjöl.  

## Til ráðstöfunar e. afbrigði

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## Krefjast notkunar afbrigða

Frá og með 2022 útgáfutímabil 2 krefjast stjórnendur þess að notendur tilgreini afbrigðið í skjölum og færslubókum fyrir vörur sem eru með afbrigði. Til að virkja möguleikann skal fara á síðuna **Uppsetning birgða** og síðan velja reitinn **Afbrigði áskilið ef það er til**. Hægt er að hnekkja þessari altæku stillingu fyrir tilteknar vörur.  

Á birgðaspjaldinu er reiturinn **Afbrigði áskilið ef það er til** með eftirfarandi valkosti:

|Svæðisgildi |Lýsing|
|---------|----|
|Sjálfgefið| Stillingin frá **Uppsetning birgða** gildir um þessa vöru.|
|Nr.| Notendur þurfa ekki að tilgreina afbrigði fyrir þessa vöru.|
|Já| Ef varan er með eitt eða fleiri afbrigði verða notendur að tilgreina viðeigandi afbrigði. Ef það er ekki gert verða notendur útilokaðir frá því að bóka færsluna.|

> [!NOTE]
> Þessar stillingar hafa ekki áhrif á hluti sem hafa engin afbrigði.

Ef kveikt er á möguleikanum geta notendur ekki bókað færslu ef afbrigðið er ekki tilgreint.

## Flokkar, eigindir og afbrigði

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## Sjá einnig .

[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Setja upp almennar birgðaupplýsingar](inventory-how-setup-general.md)  
[Kynning: Afbrigði](contoso-coffee/variants.md)  
