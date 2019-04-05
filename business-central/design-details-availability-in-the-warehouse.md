---
title: Hönnunarupplýsingar - Framboð í vöruhúsi | Microsoft Docs
description: Kerfið þarf að halda sífelldri stjórn á vörum til ráðstöfunar í vöruhúsinu þannig að vörur á útleið gangi vel og sé skilað á sem besta hátt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 5fd4bedcef6fcec79b1b2c8744c7c08d8170d97e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799406"
---
# <a name="design-details-availability-in-the-warehouse"></a>Hönnunarupplýsingar: Framboð á lager
Kerfið þarf að halda sífelldri stjórn á vörum til ráðstöfunar í vöruhúsinu þannig að vörur á útleið gangi vel og sé skilað á sem besta hátt.  

 Framboð er mismunandi eftir úthlutun á þeim hólfastigum þegar vöruhúsaaðgerðir, t.d. tiltektir og hreyfingar eiga sér stað og þegar frátekningarkerfið setur takmarkanir. Frekar flókið reiknirit staðfestir að öllu skilyrði eru uppfyllt áður en magni er úthlutað í tínslu fyrir útleiðarflæði.  

## <a name="bin-content-and-reservations"></a>Innihald hólfs og frátekningar  
 Í hvaða uppsetningu af vöruhúsakerfi sem er, er magn vara bæði til sem vöruhúsafærslur, í vöruhúsanotkunarsvæði, og sem birgðabókarfærslur í birgðanotkunarsvæði. Þessar tvær færslugerðir innihalda mismunandi upplýsingar um það hvar vara er til og hvort hún er tiltæk. Vöruhúsafærslur skilgreina framboð vöru eftir hólfi og hólfagerð, sem kallast innihald hólfs. Birgðahöfuðbókarfærslur skilgreina hvort vara er laus með frátekningu hennar samkvæmt fylgiskjölum á útleið.  

 Sérstök virkni í tiltektaralgrím til að reikna það magn sem er í boði til tínslu þegar innihald innihald hólfs er tengt við frátekningu.  

## <a name="quantity-available-to-pick"></a>Magn tiltækt í tínslu  
 Ef, til dæmis, tínslureiknirit tekur ekki tillit til vörumagns sem eru frátekin fyrir yfirvofandi sölupöntunarsendingu, þá þessir vörur gætu verið tíndar fyrir aðra sölupöntun sem er send fyrr, sem kemur í veg fyrir fyrstu sölu frá því að vera uppfyllt. Til að forðast þetta ástand, dregur tínslureikniritið frá magn sem eru frátekin fyrir aðra útleið skjöl, magni á núverandi tínsluskjalum og magn sem er valinn en ekki enn flutt eða neytt.  

 Niðurstöðurnar eru birtar í reitnum **Tiltækt magn** að tína á síðunni **Vinnublað** fyrir tínslu þar sem reiturinn er stöðugt reiknaður. Gildið er einnig reiknað út þegar notendur stofna tiltektir í vöruhúsi beint fyrir skjöl á útleið. Slík útleiðarskjöl gætu verið sölupantanir, framleiðslunotkun eða útleiðarflutningur, þar sem niðurstaðan endurspeglast í tengdum magnreitum, svo sem **Magn til afgreiðslu**.  

> [!NOTE]  
>  Varðandi forgang frátekninga er magn frátekningar dregið frá magni sem er laust til tiltektar. Til dæmis ef magnið sem tiltækt er í tínsluhólfum er 5 einingar en 100 einingar eru í frágangshólfum þá birtast villuboð ef reynt er að taka frá fleiri en 5 einingar fyrir aðra pöntun, vegna þess að viðbótarmagnið verður að vera tiltækt í tínsluhólfum.  

### <a name="calculating-the-quantity-available-to-pick"></a>Reiknar magn tilbúið í tiltekt  
 Magnið sem tiltækt er til tiltektar er reiknað svona:  

 magn tiltækt í tínslu = magn í tínsluhólfum - magn í tínslu og hreyfingar – (frátekið magn í tínsluhólfum + frátekið magn í tínslu og hreyfingu)  

 Eftirfarandi skýringarmynd sýnir mismunandi þætti í útreikningi.  

 ![Tiltækt í tínslu, með pöntunarskörun](media/design_details_warehouse_management_availability_2.png "Tiltækt í tínslu, með pöntunarskörun")  

## <a name="quantity-available-to-reserve"></a>Magn tiltækt til frátekn.  
 Þar sem hugmyndir um innihald hólfs og frátekningu og fyrirvara eru til saman, verður magn af vörum fyrir frátekningu með úthlutunum í vöruhúsaskjöl á útleið.  

 Það ætti að vera hægt að taka frá allar vörur í birgðum, nema þær sem eru þegar komnar í útleiðarferli. Í samræmi er magnið sem er tiltækt fyrir frátekningu skilgreint sem magn í öllum skjölum og öllum hólfagerðum, nema eftirfarandi magn á útleið:  

-   Magn í óskráðum tínsluskjölum  
-   Magn í afhendingarhólfum  
-   Magn í hólfkótum til framleiðslu  
-   Magn í hólfkóta opins vinnslusalar  
-   Magn í hólfum til samsetningar  
-   Magn í leiðréttingarhólfum  

 Niðurstöðurnar eru birtar í reitnum **Tiltækt heildarmagn** á síðunni **Frátekning**.  

 Á frátekningarlínu er magnið sem ekki er hægt að taka frá, vegna þess að því hefur verið úthlutað í vöruhús, birta í reitnum **Magni úthlutað í vöruhúsi** á síðunni **Frátekning**.  

### <a name="calculating-the-quantity-available-to-reserve"></a>Reikna magnið laust til frátekningar  
 Magnið sem tiltækt er til frátektar er reiknað svona:  

 magn tiltækt í frátekningu = heildarmagn í birgðum - magn í tínslu og hreyfingu fyrir upprunaskjöl - frátekið magn - magn í hólfum á útleið  

 Eftirfarandi skýringarmynd sýnir mismunandi þætti í útreikningi.  

 ![Tiltækt í frátekningu, fyrir úthlutanir í vöruhúsi](media/design_details_warehouse_management_availability_3.png "Tiltækt í frátekningu, fyrir úthlutanir í vöruhúsi")  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)
