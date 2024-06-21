---
title: Unnið með uppskriftir
description: Þú stofnar samsetningar- eða framleiðsluuppskrift til að tilgreina íhlutina eða tilföngin sem þarf til að setja saman vöruna sem samsetningaruppskriftin segir til um.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bills of material, assembly BOM, production BOM,'
ms.search.form: null
ms.date: 06/06/2024
ms.service: dynamics-365-business-central
---
# <a name="work-with-bills-of-material"></a>Unnið með uppskriftir

Nota skal uppskriftir til að byggja upp yfirvörur sem verða að vera settar saman úr öðrum vörum eða framleiddar af tilföngum eða vélastöðvum úr íhlutum.

## <a name="assembly-boms-or-production-boms"></a>Samsetningaruppskriftir eða framleiðsluuppskriftir

[!INCLUDE[prod_short](includes/prod_short.md)] styður tvær mismunandi gerðir af uppskriftum:

| Gerð uppskriftar | Almennur flokkur | Dæmi |
| -------- | ---------------- | ------- |
| [Samsetningaruppskriftir](assembly-how-work-assembly-boms.md) | Vöruhús / samsetning | Vörur sem samanstanda af öðrum vörum, settum saman með einföldum eða engum tilföngum. |
| [Framl.uppskriftir](production-how-to-create-production-boms.md) | Framleiðsla / vinnsla | Vörur sem samanstanda af mismunandi íhlutum og undiríhlutum, framleiddar á vinnu- eða vélastöð. |

Nota samsetningarpantanir til að gera lokavörur úr íhlutum í einföldu ferli sem einn eða fleiri grunnforði sem ekki eru véla- eða vinnustöðvar geta gert, eða án nokkurs forða. Til dæmis gæti samsetningarferli falið í sér að velja tvær vínflöskur og einn kaffipoka og pakka þeim sem gjafavöru.  

Samsetningaruppskrift er aðalgögn sem skilgreina hvaða íhlutavörur fara í samsetta endanlega vöru og hvaða forðar er notaðir til að setja saman samsetningarvöruna. Þegar samsetningarvara og magn er fært í haus nýrrar samsetningarpöntunar koma samsetningarpöntunarlínurnar sjálfkrafa inn í samræmi við samsetningaruppskriftina með einni samsetningarpöntunarlínu á hvern íhlut eða forða. Frekari upplýsingar má finna á [Samsetningarstjórnun](assembly-assemble-items.md).

Framleiðslupantanir er notaðar til að búa til lokavörur úr íhlutum í flóknu ferli sem krefst framleiðsluleiða og vinnu- eða vélastöðva, sem endurspegla framleiðslugetu. Til dæmis getur verið að framleiðsluferli falið í sér að skera stálplötur í einni aðgerð, sjóða þær í þeirri næsta aðgerð og mála endanlegur vöruna í síðustu aðgerðinni. Frekari upplýsingar eru í [Framleiðsla](production-manage-manufacturing.md).

Framleiðsluuppskrift er aðalgögn sem skilgreinir framleiðsluvöru og íhlutina sem notaðir eru í hana. Fyrir samsetningarvörur verður framleiðsluuppskriftin að vera vottuð og henni úthlutað á framleiðsluvöruna áður en hægt er að nota hana í framleiðslupöntun. Þegar framleiðsluvaran er færð inn í framleiðslupöntunarlínu, annað hvort handvirkt eða með því að endurnýjun pöntunina, verður framleiðsluuppskriftin framleiðslupöntunaríhlutirnir. Frekari upplýsingar eru í [Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md).

Hugtakið forði í framleiðslu er mun flóknara en í samsetningarstjórnun. Vinnustöðvar og vélastöðvar eru forði. Aðgerðirnar sem úthlutað er á forða í framleiðsluleiðum tákna framleiðsluskref. Frekari upplýsingar er að finna í greininni [Stofna leiðir](production-how-to-create-routings.md).

Bæði samsetningarpantanir og framleiðslupantanir gætu verið tengdar beint við sölupantanir. Hins vegar er aðeins hægt að nota samsetningarpantanir til að sérsníða endanlegu vöruna beint samkvæmt beiðni viðskiptamanns með sölupöntun.

## <a name="see-also"></a>Sjá einnig .

[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)  
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Stjórna afurðarafbrigðum](inventory-item-variants.md)  
[Birgðir](inventory-manage-inventory.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
