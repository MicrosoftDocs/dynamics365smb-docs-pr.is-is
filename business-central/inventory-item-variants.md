---
title: Vinna með afurðarafbrigði
description: 'Kynntu þér hvernig þú getur skráð vörur sem eru nánast eins en hvað varðar lit, stærð eða efni sem vöruafbrigði.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, variant, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---

# <a name="manage-product-variants"></a>Vinna með afurðarafbrigði

Vöruafbrigði eru frábær leið til að halda stjórn á lista yfir vörur. Til dæmis gætirðu verið með mikinn vörufjölda sem er nánst eins nema með ólíkan lit. Hægt er að skilgreina hvert afbrigði sem aðskilda vöru. Einnig er hægt að velja að setja upp eina vöru og tilgreina mismunandi liti sem afbrigði af vörunni.  

> [!TIP]
> Hagnýt kynning á afbrigðum í framleiðslu má fá [í Kynning: Afbrigði](contoso-coffee/manufacturing/variants.md) fyrir contoso-kaffi kynningargögnin.  

## <a name="add-variants-to-an-item"></a>Bæta afbrigðum við vöru

Það er auðvelt að skilgreina afbrigði fyrir vöru.  

### <a name="to-add-variants"></a>Til að bæta við afbrigðum

1. Opnaðu [ **Vörulisti** síðuna](https://businesscentral.dynamics.com/?page=31), opnaðu viðkomandi vöru.  
2.  **Á Birgðaspjaldinu** skal velja aðgerðina **Tengdar**, velja **svo Vara** og velja svo aðgerðina **Afbrigði** .  
3. Á síðunni **Vöruafbrigði er** listi yfir afbrigðin.  

Þegar söluskjal er síðan stofnað og vörunni bætt við er hægt að tilgreina afbrigði vörunnar í reitnum **Afbrigðiskóti** . Það sama á við um innkaupaskjöl.  

## <a name="item-availability-by-variant"></a>Til ráðstöfunar e. afbrigði

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## <a name="require-use-of-variants"></a>Krefjast notkunar afbrigða

Frá og með 2022 útgáfutímabil 2 krefjast stjórnendur þess að notendur tilgreini afbrigðið í skjölum og færslubókum fyrir vörur sem eru með afbrigði. Til að virkja getu skal á síðunni **Birgðagrunnur** og velja reitinn **Afbrigði áskilið ef til er** . Hægt er að hnekkja þessari altæku stillingu fyrir tilteknar vörur.  

Á birgðaspjaldinu er reiturinn **Afbrigði áskilið ef það er til** með eftirfarandi valkosti:

|Svæðisgildi |Heimildasamstæða|
|---------|----|
|Sjálfgefið (Nei)| Stillingin frá **Uppsetning birgða** gildir um þessa vöru.|
|Nr.| Notendur þurfa ekki að tilgreina afbrigði fyrir þessa vöru.|
|Já| Ef varan er með eitt eða fleiri afbrigði verða notendur að tilgreina viðeigandi afbrigði. Ef svo er ekki, er þeim lokað fyrir að bóka færsluna.|

> [!NOTE]
> Þessar stillingar hafa ekki áhrif á vörur sem ekki eru með afbrigði.

Ef kveikt er á getu er ekki hægt að bóka færslu ef afbrigðið er ekki tilgreint.

## <a name="categories-attributes-and-variants"></a>Flokkar, eigindir og afbrigði

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Sjá einnig .

[Skrá nýjar vörur](inventory-how-register-new-items.md)    
[Uppsetning almennra birgðaupplýsinga](inventory-how-setup-general.md)    
[Kynning: Afbrigði](contoso-coffee/manufacturing/variants.md)    
