---
title: Stjórna afurðarafbrigðum
description: Lærðu hvernig hægt er að taka upp vörur sem eru nánast eins en eru breytilegar í lit, stærð eða efni sem vöruafbrigði.
author: edupont04
ms.topic: conceptual
ms.workload: na
ms.search.keywords: item, variant, finished good, component, raw material, assembly item, item substitution
ms.search.form: 30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719
ms.date: 09/26/2022
ms.author: edupont
ms.openlocfilehash: 1782d876a1b6e861a78a12fb745e1bee93bced18
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608488"
---
# <a name="manage-product-variants"></a>Stjórna afurðarafbrigðum

Vöruafbrigði eru frábær leið til að halda þínum lista af vörum undir eftirliti. Til dæmis er mikið af vörum sem eru nánast eins og eru aðeins breytilegar í lit. Hægt er að skilgreina hvert afbrigði sem aðskilda vöru. En valið er að setja upp eitt atriði og tilgreina ýmsa liti sem afbrigði vörunnar.  

> [!TIP]
> Til að fá hagnýta kynningu á notkun afbrigða í framleiðslu, sjá [Walkthrough: vöruvíddasamsetningar](contoso-coffee/variants.md) fyrir kaffiuppbrot contoso.  

## <a name="add-variants-to-an-item"></a>Bæta við vöruvíddasamsetningar á vöru

Ef fyrirtækið hefur ákveðið að nota vöruvíddasamsetningar er það nógu auðvelt til að skilgreina afbrigði fyrir vöru.  

### <a name="to-add-variants"></a>Til að bæta við vöruvíddasamsetningar

1. [Opnið **listasíðuna**](https://businesscentral.dynamics.com/?page=31) vörur, Opnið viðeigandi vöru.  
2. **Á birgðaspjaldinu** er vöruaðgerðin **valin** og síðan er **valin aðgerðin afbrigði**.  
3. **Á síðunni vöruvíddasamsetningar** er listi yfir afbrigðin.  

Þegar söluskjal er stofnað og bætt við vöruna er hægt að tilgreina afbrigði vörunnar í **reitnum Afbrigðiskóti**. Sama á við um innkaupaskjöl.  

## <a name="item-availability-by-variant"></a>Vöruframboð eftir afbrigði

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## <a name="require-use-of-variants"></a>Krefjast notkunar vöruvíddasamsetningar

Byrjað er á 2022 2, viðurkenningar getur krafist þess að notendur tilgreini afbrigði í skjölum og færslubókum fyrir vörur sem eru með vöruvíddasamsetningar. Til að virkja getuinn er farið á **síðuna Birgðagrunnur** og síðan er valið afbrigði sem **er áskilið ef svæðið er til**. Hægt er að hnekkja altækum stillingum fyrir tilteknar vörur.  

Á birgðaspjöldum er **afbrigðið áskilið að eftirfarandi valkostir séu til staðar**:

|Gildi svæðis |Lýsing|
|---------|----|
|Sjálfgefið| Stillingin frá **birgðauppsetningu** gildir um þessa vöru.|
|Nr.| Notendur þurfa ekki að tilgreina afbrigði fyrir þessa vöru.|
|Já| Ef varan er með eitt eða fleiri afbrigði verða notendur að tilgreina viðkomandi afbrigði. Ef þeir eru það ekki verða þeir lokaðir frá bókun færslunnar.|

> [!NOTE]
> Þessar stillingar hafa ekki áhrif á vörur sem engin afbrigði eru með.

Ef kveikt er á getunum geta notendur ekki bókað færslu ef afbrigðið er ekki tilgreint.

## <a name="categories-attributes-and-variants"></a>Flokkar, eigindir og afbrigði

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Sjá einnig .

[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Setja upp almennar birgðaupplýsingar](inventory-how-setup-general.md)  
[Walkthrough: afbrigði](contoso-coffee/variants.md)  
