---
title: Hönnunarupplýsingar - Framboð í vöruhúsi | Microsoft Docs
description: Kerfið þarf að halda sífelldri stjórn á vörum til ráðstöfunar í vöruhúsinu þannig að vörur á útleið gangi vel og sé skilað á sem besta hátt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 7d23dc10ffb215ee2ac160c9ec9b9fd1ddb5cc2d
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6442536"
---
# <a name="design-details-availability-in-the-warehouse"></a>Hönnunarupplýsingar: Framboð á lager
Kerfið þarf að halda sífelldri stjórn á vörum til ráðstöfunar í vöruhúsinu þannig að vörur á útleið gangi vel og sé skilað á sem besta hátt.  

Framboð er mismunandi eftir úthlutun á þeim hólfastigum þegar vöruhúsaaðgerðir, t.d. tiltektir og hreyfingar eiga sér stað og þegar frátekningarkerfið setur takmarkanir. Frekar flókið reiknirit staðfestir að öllu skilyrði eru uppfyllt áður en magni er úthlutað í tínslu fyrir útleiðarflæði.

Ef eitt eða fleiri skilyrði eru ekki uppfyllt geta mismunandi villuboð verið sýndar, þar með talið almennu boðin „Ekkert að afgreiða.“ skilaboð. „Ekkert að afgreiða.“ skilaboð geta komið upp af mörgum ólíkum ástæðum, bæði í flæði á útleið og innleið, þar sem skjalalína, sem tengist með beinum eða óbeinum hætti, inniheldur reitinn **Magn til afgreiðslu**.

> [!NOTE]
> Upplýsingarnar birtast fljótlega hér um hugsanlegar ástæður og lausnir fyrir „Ekkert að afgreiða“. skilaboð.

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

 ![Tiltækt í tínslu, með skörun í frátekningu.](media/design_details_warehouse_management_availability_2.png "Tiltækt í tínslu, með pöntunarskörun")  

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

 ![Tiltækt í frátekningu, fyrir úthlutanir í vöruhúsi.](media/design_details_warehouse_management_availability_3.png "Tiltækt í frátekningu, fyrir úthlutanir í vöruhúsi")  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
 [Skoða tiltækileika vöru](inventory-how-availability-overview.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]