---
title: Upplýsingar um hönnun - Til ráðstöfunar í vöruhúsinu
description: Fræðast um þá þætti sem hafa áhrif á tiltækni vöru í vöruhúsinu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Hönnunarupplýsingar: Framboð á lager

Halda skal ofan á vörur til ráðstöfunar til að tryggja að pantanir á útleið flæði á skilvirkan hátt og að afhendingartímar séu ákjósanlegir.  

Ráðstöfunarmagn getur verið mismunandi eftir mörgum þáttum. Fr.dæmi:

* Úthlutanir á hólfastigi þegar vöruhúsaaðgerðir eins og tínslur og hreyfingar gerast.
* Þegar birgðafrátekningarkerfið bætir takmarkanir á að samræmast.

Áður en magni er úthlutað til tínslu fyrir flæði [!INCLUDE [prod_short](includes/prod_short.md)]  á útleið er staðfest að öllum skilyrðum sé uppfyllt.

Þegar skilyrðum er ekki uppfyllt birtast villuboð. Dæmigerð skilaboð eru almenn "Ekkert til að meðhöndla." skilaboð. Skilaboðin er hægt að birta af mörgum mismunandi ástæðum í flæði á útleið og innleið þar sem í fylgiskjalslínu er **reiturinn Magn til afgreiðslu** .

## Innihald hólfs og frátekningar  

Vörumagn er bæði til sem vöruhúsafærslur og birgðafærslur í birgðum. Þessar tvær tegundir færslna innihalda ólíkar upplýsingar um hvar vörurnar eru og hvort þær eru tiltækar. Vöruhúsafærslur skilgreina framboð vöru eftir hólfi og hólfagerð, sem kallast innihald hólfs. Birgðafærslur skilgreina ráðstöfunarmagn vöru með því að taka frá fyrir fylgiskjöl á útleið.  

[!INCLUDE [prod_short](includes/prod_short.md)] reiknar magnið sem er tiltækt til tínslu þegar innihald hólfs er parað með frátekningum.  

## Tiltækt magn til tínslu  

[!INCLUDE [prod_short](includes/prod_short.md)] Tekur vörur frá fyrir afhendingu sölupöntunar í undirbúningi svo að þær séu ekki tíndar fyrir aðrar sölupantanir sem afhendast fyrr. [!INCLUDE [prod_short](includes/prod_short.md)] dregur frá magn vara sem þegar er verið að vinna, á eftirfarandi hátt:

* Magn frátekið fyrir önnur skjöl á útleið.
* Magn í tínsluskjölum sem fyrir eru.
* Magn sem hefur verið tínt en ekki enn afhent eða notað.  

Útkoman er reiknuð kviklega og birt í reitnum **Tiltækt magn til tínslu** á síðunni **Vinnublað** tínslu. Gildið er einnig reiknað út þegar notendur stofna tiltektir í vöruhúsi beint fyrir skjöl á útleið. Eftirfarandi eru dæmi um skjöl á útleið:

* Sölupantanir
* Framleiðslunotkun
* Millifærslur á útleið

Niðurstaðan er tiltæk í þessum skjölum í magnreitunum, t.d. reitnum **Magn til afgreiðslu** .  

> [!NOTE]  
> Fyrir forgang frátekninga er magnið sem á að taka frá dregið frá tiltæku magni sem hægt er að tína. Til dæmis ef tiltækt magn í tínsluhólfum er 5 einingar en 100 einingar eru í frágangshólfum þegar fleiri en 5 einingar eru teknar frá fyrir aðra pöntun birtast villuboð þar sem viðbótarmagn verður að vera tiltækt í tínsluhólfum.  

### Reiknar tiltækt magn til tínslu  

[!INCLUDE [prod_short](includes/prod_short.md)] reiknar tiltækt magn til tínslu á eftirfarandi hátt:  

magn tiltækt í tínslu = magn í tínsluhólfum - magn í tínslu og hreyfingar – (frátekið magn í tínsluhólfum + frátekið magn í tínslu og hreyfingu)  

Eftirfarandi skýringarmynd sýnir mismunandi þætti í útreikningi.  

![Tiltækt í tínslu, með skörun í frátekningu.](media/design_details_warehouse_management_availability_2.png "Tiltækt í tínslu, með pöntunarskörun")  

## Tiltækt magn til frátekninga

Þar sem hugtökin um innihald hólfa og frátekningu á hólfum verða magn vara sem tiltækar eru til frátekningar að samræmast úthlutunum á vöruhúsaskjöl á útleið.  

Hægt er að taka frá allar birgðavörur, nema vörur sem vinnsla á útleið hefur hafist fyrir. Magnið sem er tiltækt til að taka frá er skilgreint sem magn í öllum skjölum og hólfategundum. Eftirfarandi magn á útleið eru undantekningar:  

* Magn í óskráðum tínsluskjölum  
* Magn í afhendingarhólfum  
* Magn í hólfkótum til framleiðslu  
* Magn í hólfkóta opins vinnslusalar  
* Magn í hólfum til samsetningar  
* Magn í leiðréttingarhólfum  

Niðurstöðurnar eru birtar í reitnum **Tiltækt heildarmagn** á síðunni **Frátekning**.  

Í frátekningarlínu er magnið sem ekki er hægt að taka frá vegna þess að því er úthlutað í vöruhúsinu birt í reitnum **Úthlutað magn í vöruhúsi** á **frátekningarsíðunni** .  

## Kanna hvort vörur séu tiltækar til tínslu

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

### Útreikningur á tiltæku magni til að taka frá

[!INCLUDE [prod_short](includes/prod_short.md)] reiknar tiltækt magn til að taka frá á eftirfarandi hátt:  

magn tiltækt í frátekningu = heildarmagn í birgðum - magn í tínslu og hreyfingu fyrir upprunaskjöl - frátekið magn - magn í hólfum á útleið  

Eftirfarandi skýringarmynd sýnir mismunandi þætti í útreikningi.  

![Tiltækt í frátekningu, fyrir úthlutanir í vöruhúsi.](media/design_details_warehouse_management_availability_3.png "Tiltækt í frátekningu, fyrir úthlutanir í vöruhúsi")  

## Sjá einnig  

[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)
[Skoða tiltækileika vöru](inventory-how-availability-overview.md)
[Tínsla fyrir framleiðslu, samsetningu eða verk í ítarlegri vöruhúsagrunnstillingu](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]