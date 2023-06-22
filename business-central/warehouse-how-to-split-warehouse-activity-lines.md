---
title: Hvernig á að skipta vöruhúsaaðgerðalínum
description: Frekari upplýsingar um hvernig á að skipta vöruhúsaaðgerðalínum ef tiltæk afkastageta í leiðbeinandi hólfi er ekki nægileg.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 9314, 9313, 9315, 9330'
---
# <a name="split-warehouse-activity-lines" />Skipta aðgerðalínum vöruhúss

Í frágangi vöruhúsa, hreyfinga eða tínslu og í frágangi í birgðum og birgðum er hólf lagt fyrir tiltekt eða frágang vara. Magnið sem er í raun í hólfinu sem lagt er til er ekki nægilegt eða ekki er pláss í hólfinu til að ganga frá tilskilinn magni. Í þessum tilfellum er hægt að skipta línunni þannig að vörur einnar línu séu teknar úr eða settar í fleiri en eitt hólf.  

Eftirfarandi ferli á við eftirfarandi vöruhúsaskjöl:

* Frágangur vöruhúsafrágangs
* Vöruhúsahreyfingar
* Vöruhús-tínsla
* Frágangi birgða
* Birgðahreyfingar
* Birgðatínslur  

## <a name="to-split-warehouse-activity-lines" />Til að skipta vöruhúsaaðgerðalínum

1. Opna vöruhúsaaðgerðalínu þar sem þú ert að reyna að meðhöndla ófullnægjandi magn.  
2.  **Í reitinn Magn til afgreiðslu**  er fært niður lækkað magn sem hægt er að meðhöndla.  
3. Á flýtiflipanum **Línur** skal velja aðgerðina **Aðgerðir**, velja aðgerðina **Aðgerðir** og loks velja aðgerðina **Skipta línu**. Ný lína birtist. Línan er afrit af upphaflegu línunni nema að  **reiturinn Magn til afgreiðslu**  inniheldur magnið sem fjarlægt var úr upprunalegu línunni.  
4. Úthlutið hólfi og, ef notaður er beinn frágangur og tínsla, svæði eða haldið áfram að skipta línunni eftir þörfum þar til fundin eru viðeigandi hólf fyrir allt magnið.  

> [!NOTE]  
> Ef ef notaður er beinn frágangur og tínsla og línunum er skipt þarf notandinn að hafa þekkingu á vöruhúsinu og geta valið hólf sem hentar geymsluþörfum vörunnar og sem uppfyllir almennar kröfur í vöruhúsaskjalinu. Til dæmis, ekki er hægt að skipta línu í tínsluskjali og setja nokkur atriði í magngeymslu.  

## <a name="see-also" />Sjá einnig

[Yfirlit](design-details-warehouse-management.md)
[vöruhúsakerstjórnunar birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
