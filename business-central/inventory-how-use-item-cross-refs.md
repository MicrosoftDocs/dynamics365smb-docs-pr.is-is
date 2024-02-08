---
title: Nota vörutilvísanir
description: 'Settu upp tilvísanir milli lýsinga, mælieininga og afbrigða sem þú og lánardrottinn eða viðskiptamaður nota fyrir vöru.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'item reference, cross reference, inventory'
ms.search.forms: '5737, 5735, 5736'
ms.date: 10/02/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="use-item-references"></a>Nota vörutilvísanir

Ef þú kaupir eða selur vörur sem þú og lánardrottinn eða viðskiptamaður nota mismunandi skilmála fyrir getur þú sett upp tilvísun milli skilmálanna þinna fyrir vörurnar og skilmálanna sem viðskiptamaður eða lánardrottinn vörunnar nota. Þannig er vörulýsingar-, mælieiningar- eða afbrigðiskóða lánardrottins sjálfkrafa settur inn á viðeigandi skjöl þegar þú fyllir út reitinn **Vörutilvísunarnúmer** .  

## <a name="to-set-up-an-item-reference"></a>Að setja upp vörutilvísun

1. Veldu :::image type="icon" source="media/ui-search/search_small.png" border="false"::: táknið, farðu í **Vörur** og veldu síðan viðkomandi tengil.
2. Opnaðu spjaldið fyrir vöruna sem þú vilt búa til tilvísun fyrir.
3. Veldu aðgerðina **Vörutilvísanir**.

     Ef ekki er hægt að finna aðgerðina **Vörutilvísanir** skal velja til að skoða fleiri valkosti og finna hana síðan undir **Tengd** > **Vara**.
  
4. Í nýrri línu á síðunni **Færslur fyrir tilvísun vöru** skal fylla í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Eftirfarandi ferli lýsir því hvernig á að tilgreina vörutilvísun í innkaupapöntun. Svipuð skref gilda um söluskjöl og önnur innkaupaskjöl.  

## <a name="to-enter-a-vendors-item-description-on-a-document"></a>Að færa inn vörulýsingu lánardrottins í skjali

1. Veljið táknið :::image type="icon" source="media/ui-search/search_small.png" border="false":::, opnið **Innkaupapantanir** og velja síðan viðkomandi tengil.
2. Stofnaðu innkaupapöntun fyrir lánardrottin sem þú setur upp tilvísun vöru fyrir í ferlinu hér á undan.
3. Stofnaðu innkaupalínu fyrir vöruna sem þú setur upp tilvísun vöru fyrir í ferlinu hér á undan.
4. Í **Vörutilvísunarnúmer** reitnum skal velja viðeigandi vörutilvísun og síðan velja hnappinn **Í lagi**.

Skrifað er yfir reitinn **Lýsing** í línunni með vörulýsingu lánardrottins eins og er uppsett í færslu fyrir tilvísun vörunnar. Ef vörutilvísunin inniheldur afbrigðiskóða eða mælieiningu eru gildin einnig afrituð í skjalið.  

## <a name="scan-barcodes-with-the-business-central-mobile-app"></a>Skanna strikamerki með Business Central farsímaforritinu

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Í eftirfarandi töflu er listi yfir síður sem styðja skönnun á vörutilvísunum úr farsímaforritinu [!INCLUDE [prod_short](includes/prod_short.md)] .

|Síða  |Gildi reits er hægt að skanna  |
|---------|---------|
|Vörutilvísun     | Tilvísunarnr.        |
|Birgðabókarlína     | Vörutilvísunarnr.        |
|Pöntunarlína efnislegra birgða     |Vörutilvísunarnr.         |
|Innkaupalína     |   Vörutilvísunarnr.      |
|Sölulína     | Vörutilvísunarnr.        |

## <a name="see-also"></a>Sjá einnig

[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
