---
title: Meðhöndlun Lostærðir
description: Þetta efnisatriði lýsir mismunandi leiðum til að meðhöndla lotustærðir.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 6d6316fbe214512f5d42622c47502a4361ce604e
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8135751"
---
# <a name="handling-lot-sizes-in-production"></a>Stjórna lotustærð í framleiðslu
Hvað varðar magn er ekki víst að fjöldi vara sem framleiddar eru í framleiðsluaðgerð tengist því hvernig þær eru seldar. Til dæmis væri hægt að búa til hundruð vörur í einni lotu, en selja hverja vöru sérstaklega. Þegar skilgreindar eru framleiðsluleiðir og uppskriftir (uppskriftir) eru nokkur tilbrigði sem ætti að hafa í huga varðandi lotustærðir. Í þessu efnisatriði er því lýst hvernig lotustærðir hafa áhrif á kostnaðarútreikninga og tilfangaáætlun.

## <a name="units-of-measure-in-production-bill-of-materials"></a>Mælieining í framleiðsluuppskrift
Þótt grunnmælieining fyrir vöru er tilgreind, gæti uppskriftin notað aðra mælieiningu fyrir tilbúnu afurðina. Til dæmis gæti grunnmælieiningin fyrir vöru verið STK, en uppskriftin gæti viljað bretti eða tonn. Þetta kemur sér vel þegar vélarnar þínar eða hráefnishlutar stjórna magninu. Þú vilt til dæmis líklega ekki baka eina formköku því að það er erfitt að nota hluta af eggi. Þess í stað bakar þú einn skammt af formkökum til að draga úr sóun. Frekari upplýsingar eru í [Stofna framleiðsluuppskriftir](production-how-to-create-production-boms.md).

## <a name="lot-size-on-routing-lines"></a>Lotustærð í leiðarlínum
Frá sjónarhorni leiðar er hægt að tilgreina lotustærð í leiðarlínum þannig að hún passi við afkastagetu vélanna sem framleiða vörurnar. Keyrslutími á leiðarlínum er styttur í hlutfalli við lotustærðina. 

Þetta virkar vel þegar magnið í framleiðslupöntun er þáttur lotustærðar í leiðinni. Ef til dæmis bökunarpappírinn rúmar 10 formkökur, ætti að baka 10, 20, 30 og svo framvegis, en ekki 5 eða 15.  Þetta skiptir töluvert minna máli ef mikið magn er notað.

Lotustærð er einnig vinsæl í framleiðsluumhverfum þar sem framleiðnin er mæld sem magn sem hægt er að inna af hendi á ákveðið löngum tíma. Dæmi um það er ef magn á níu tíma vakt er 25.000 rúmfet, er hægt að stilla keyrslutíma á 9 tíma og lotustærð á 25.000.
Magn framleiðslupöntunar skiptir minna máli þar sem keyrslutími framleiðslupöntunar er reiknaður sem keyrslutími / lotustærð til að fá út keyrslutíma á hvert stykki.
 
> [!NOTE]
> Gildið sem tilgreint er í lotustærð hefur ekki áhrif á tíma sem tilgreindur er í reitnum **Uppsetningartími** fyrir línu leiðarinnar. Uppsetningin gerist aðeins einu sinni, jafnvel þótt nokkrar lotur eru til staðar. Til dæmis svo ekki þurfi að hita ofninn fyrir seinni lotuna af formkökum. Nánari upplýsingar eru í [Stofna leiðir](production-how-to-create-routings.md).

## <a name="lot-sizes-for-items-and-stockkeeping-units"></a>Lotustærðir fyrir vörur og birgðahaldseiningar
Lotustærðir sem skilgreindar eru fyrir leiðirnar eru ekki þær sömu og lotustærðir fyrir vörur eða birgðahaldseiningar. Þessi gildi eru notuð í öðrum tilgangi og hafa ekki áhrif á framleiðslugetu. 

## <a name="lot-size-on-item-and-stockkeeping-units"></a>Lotustærð á vörum og birgðahaldseiningum
Fyrir vörur og birgðahaldseiningar hafa lotustærðir eftirfarandi áhrif á kostnaðarútreikning og framboðsáætlanagerð:

* Fyrir útreikning staðlaðs kostnaðar, ef **Uppsetning innifalins kostnaðar** á síðunni **Framleiðsluuppsetning**, er kostnaði fyrir uppsetninguna bætt við staðalkostnaðinn. Ef lotustærð er tilgreind verður uppsettur kostnaður fyrir leiðaraðgerð lækkaður niður í eina lotustærð. Ef til dæmis lotustærðin sem skilgreind er á birgðaspjaldi er 10 og það tekur 15 mínútur að hita ofninn, verður orkukostnaðinum úthlutað á 10 formkökur sem u.þ.b. 1,5 mínúta. 

> [!NOTE]
> Uppsetningarkostnaður er meðhöndlaður á annan hátt séð út frá úthlutun staðalkostnaðar og afkastagetu. Ef framleitt magn stemmir ekki við lotustærð sem er skilgreind á birgðaspjaldinu leiðir það til breytileika. Frekari upplýsingar eru í [Stjórnun birgðakostnaðar](finance-manage-inventory-costs.md). <!--not sure that I got this part right seems to repeat the first example.-->

Fyrir framboðsáætlun virkar stilling lotustærðar með **Sjálfgefnar hömlur %** á síðunni **Framleiðsluuppsetning**. [!INCLUDE[prod_short](includes/prod_short.md)] hunsar breytingar á eftirspurn sem eru fyrir neðan hömluprósentuna og stofnar ekki tillögur um áætlanagerð. Til dæmis er 15 tilgreint í reitnum „Sjálfgefnar hömlur %“ og framleiðslupöntun er upp á 20 formkökur handa 20 gestum, en einn gesturinn getur ekki mætt. [!INCLUDE[prod_short](includes/prod_short.md)] mun hunsa það að einn gest vanti vegna þess að það er aðeins 10% af lotustærðinni 10 skilgreint í vörunni. Ef tveir gestir geta hinsvegar ekki komist mun [!INCLUDE[prod_short](includes/prod_short.md)] leggja til að við minnkum pöntunarmagnið vegna þess að tveir er 20% af lotustærðinni. Frekari upplýsingar um áætlanagerð er að finna í [Áætlanagerð](production-planning.md).

## <a name="see-also"></a>Sjá einnig
[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)  
[Vinna með mælieiningu framleiðslukeyrslu](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)
[Stofna leiðir](production-how-to-create-routings.md)  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]