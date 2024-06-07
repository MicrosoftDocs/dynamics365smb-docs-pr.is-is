---
title: Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir
description: Fræðast um samsetningu vara í sölupöntunum eða að geyma á lager fyrir seinni hluta sölu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.service: dynamics-365-business-central
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock"></a>Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir

[!INCLUDE [prod_short](includes/prod_short.md)] gerir kleift að setja saman vörur á eftirfarandi hátt:

* Setja saman í pöntun  
* Setja saman á lager  

## <a name="assemble-to-order"></a>Setja saman í pöntun

Nota skal samsetningarferlið fyrir vörur sem ekki á að koma á lager. Til dæmis af eftirfarandi ástæðum:

* Sérsníða verður vörurnar að þörfum viðskiptamanns.
* Minnka á birgðir á lager.

Eftirfarandi listi lýsir nokkrum af ávinningi ferlisins saman í pöntun:  

* Sérstilla samsetningarvörur þegar sölupöntun er tekin.  
* Yfirlit til ráðstöfunar vegna samsetningarvöru og íhluta hennar.  
* Taka samsetningaríhluti strax frá til að tryggja uppfyllingu pöntunar.  
* Ákvarða arðsemi sérsniðnu pöntunarinnar með því að leggja saman verð og kostnað.  
* Samþætt vöruhúsinu til að auðvelda samsetningu og afhendingu.  
* Setja saman pöntun þegar sölutilboð eða standandi sölupöntun er stofnuð.  
* Sameina birgðamagn og magnsamsetningu eftir pöntunum.  

Í samsetningarferlinu eru vörur settar saman fyrir sölupöntun. Einn er tengill milli samsetningarpöntunarinnar og sölupöntunarinnar.  

Þegar samsetningarvara er færð inn á sölupöntunarlínu er samsetningarpöntun sjálfkrafa stofnuð. Samsetningarpöntunin er byggð á sölulínunni og línur hennar eru byggðar á samsetningaruppskrift vörunnar. Magn íhluta í samsetningaruppskriftinni er margfaldað með pöntunarmagninu. Síðan **Setja saman til pöntunarlínur** sýnir upplýsingar um tengdar samsetningarpöntunarlínur. Upplýsingarnar geta hjálpað til við sérsnið samsetningarvörunnar. Afgreiðsludagsetningin byggist á því hvað er til ráðstöfunar af íhlutum. Til að fræðast meira um samsetningu vara í sölupöntunum er farið í [Selja vörur sem settar eru saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
> Þó að hún sé ekki hluti af sjálfgefna ferlinu er hægt að selja birgðamagn og magnsamsetningu á pöntun á sömu sölupöntun. Nánari upplýsingar um samsetningu birgða og samsetningar á pöntunarvörum er farið [í Selja birgðavörur í flæði samsetningar í pöntun](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

Til að tilgreina að vara sé sett saman eftir pöntun skal velja **Setja saman í**  pöntun í **reitnum Samsetningarstefna** á **síðunni Birgðaspjald** fyrir vöruna.  

## <a name="assemble-to-stock"></a>Setja saman á lager

Nota skal samsetningarferli til birgða fyrir vörur sem settar eru saman og geyma til sölu í framtíðinni. Samsetning vara á lager eru staðlaðar vörur, svo sem pakkað pökk, sem sérsníða ekki. Einnig er hægt að nota þessar vörur sem millivöruíhluti. Vörurnar eru tíndar og unnar sem einstakar vörur og eru meðhöndlaðar sem tilbúnar framleiðsluvörur. Nánari upplýsingar um samsetningarvörur er farið í [Samsetningarvörur](assembly-how-to-assemble-items.md).  

Þegar vara sem sett er saman á lager er tilgreind í sölulínu er farið með vöruna eins og aðrar vörur sem seldar eru úr birgðum. Til dæmis [!INCLUDE [prod_short](includes/prod_short.md)]  athugar aðeins ráðstöfunarmagn fyrir samsettu vöruna en ekki íhluti hennar.  

> [!NOTE]  
> Þó að hún sé ekki hluti af sjálfgefna ferlinu er hægt að setja saman vöru til pöntunar jafnvel þótt varan sé sett saman á lager. Fræðast meira um [vörur í samsetningu eftir pöntun og vörur í birgðum.](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)  

Til að tilgreina að vara sé sett saman til birgða skal velja **Setja saman til birgðir**  í **reitinn Samsetningarstefna** á **birgðaspjaldssíðu** fyrir vöruna.  

## <a name="combination-scenarios"></a>Samsetningaraðstæður

Þegar magn saman til pöntunar og birgðamagn er sameinað í sölupöntun þarf fyrst að afhenda magn saman til pöntunar.  

Ef samsetningarpöntun er tengd sölupöntunarlínu er gildið í reitnum **Magn til samsetningar í pöntun** afritað í reitinn Magn í samsetningarlínu í sölupöntunarlínunni afritað **í reitinn Magn í samsetningu** með reitnum **Magn** á samsetningarpöntuninni. Nánari upplýsingar um sölu á [vörum sem settar eru saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).  

Gildið í reitnum **Magn til samsetningar** er tengt reitnum **Magn til afhendingar** í sölupöntunarlínunni. Þessi tengsl stjórna því hvernig magn að hluta til er sent og allt saman í pöntun:

* Þegar allt magnið í sölupöntunarlínunni er sett saman á pöntun
* Í samsetningartilvikum þar sem hluti magnsins er settur saman í pöntun og hluti er sendur úr birgðum.

Samsetningaraðstæður gera hlutaafhendingar kleift að sveigjanleika. Hægt er að nota reitinn **Magn til samsetningar** til að tilgreina magnið sem á að afhenda að hluta úr birgðum og með því að setja saman til pöntunar.  

Ef setja þarf fullt sölulínumagn saman í pöntun og afhenda, er gildið í reitnum **Magn til afhendingar** afritað **í reitinn Magn til samsetningar** á tengdri samsetningarpöntun þegar magninu sem á að afhenda er breytt. Þessi uppfærsla tryggir að magnið sem verið er að afhenda sé að fullu gefið upp með magninu sem sett er saman til pöntunar.  

Í samsetningartilvikum er fullt gildi í reitnum **Magn til afhendingar** ekki afritað í reitinn **Magn til samsetningar í samsetningarpöntuninni** . Þess í stað er sjálfgefið gildi sett inn í reitinn **Magn til samsetningar** . Gildið er reiknað út frá reitnum **Magn til afhendingar** til að tryggja að magnið sem sett er saman til pöntunar verði fyrst sent.

Til að víkja frá sjálfgefnu, til dæmis vegna þess að aðeins á að setja saman meira eða minna af magninu í reitnum **Magn til afhendingar**, er hægt að breyta reitnum **Magn til samsetningar** í forskilgreindum reglum, eins og lýst er hér á eftir.  

Dæmi um hvers vegna magninu sem á að setja saman er að hluta á að bóka afhendingu birgðamagns áður en samsetningarfrálagið er afhent.  

Eftirfarandi tafla útskýrir reglurnar sem skilgreina lágmarks- og hámarksgildi sem hægt er að færa inn í reitinn **Magn til samsetningar** til að víkja frá sjálfgildinu í samsetningardæmi. Taflan sýnir samsetningardæmi þar sem reiturinn **Magn afhent** í tengdu sölupöntunarlínunni er breytt úr 7 í 4 og **Magn sett saman** verður þess vegna að sjálfgefnu 4.  

**Sölupöntunarlína**

|                | **Magn** | **Magn til afhendingar** | **Magn til samsetningar til pöntunar** | **Afhent magn** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Upphafsgildi**| 10          | 7                | 7                             | 0                    |
|**Breyting**      |              | 4                |                               |                      |

**Samsetningarpöntunarhaus**

|                | **Magn** | **Magn til afhendingar** | **Magn til samsetningar til pöntunar** | **Afhent magn** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Upphafsgildi**| 7           | 7                | 0                             | 7                    |
|**Breyting**      |              | 4 (sett inn sjálfgefið)|                         |                      |

Á grundvelli þessa dæmis er hægt að breyta reitnum **Magn í samsetningar** á eftirfarandi hátt:  

* Lágmarksmagnið sem færa má inn er 1. Setja verður saman að minnsta kosti eina einingu til að hægt sé að selja einingarnar fjórar, þannig að þær þrjár sem eftir eru séu tiltækar í birgðum.  
* Hámarksmagn sem hægt er að færa inn er 4. Þessi takmörkun tryggir að ekki er sett saman meira af vörunni en þörf krefur vegna sölunnar.  

## <a name="see-also"></a>Sjá einnig .

[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Birgðir](inventory-manage-inventory.md)  
[Yfirlitsvinna vöruhúsastjórnunar](design-details-warehouse-management.md)
[með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
