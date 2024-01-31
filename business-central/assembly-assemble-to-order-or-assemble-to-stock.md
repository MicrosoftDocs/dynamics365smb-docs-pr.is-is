---
title: Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir
description: Fræðast um þing-vörur fyrir sölupantanir eða geyma á lager fyrir síðari sölu.
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
# Skilja hvernig skal setja saman í pöntun eða setja saman í birgðir

[!INCLUDE [prod_short](includes/prod_short.md)] gerir þér kleift að veita samsetningarvörur á eftirfarandi hátt:

* Setja saman til að panta  
* Setja saman á lager  

## Setja saman til að panta

Notaðu samsetningarferlið fyrir vörur sem þú vilt ekki eiga á lager. Til dæmis af eftirfarandi ástæðum:

* Vörurnar eru sérsniðnar fyrir þarfir viðskiptavina.
* Óskað er eftir að lágmarka kostnað við lagerbirgðir.

Á eftirfarandi lista er lýst nokkrum kostum þess að sameina ferlið:  

* Sérsníða vörur samsetningar þegar sölupöntun er tekin.  
* Yfirlit yfir ráðstöfunarvöru og íhluti hennar.  
* Taka skal frá samsetningaríhluti strax til að ábyrgjast uppfyllingu pöntunar.  
* Ákvarða arðsemi sérsniðinnar pöntunar með því að rúlla upp verði og kostnaði.  
* Innbyggt vöruhús til að gera samsetningar og sendingu auðveldari.  
* Setja saman við pöntun þegar sölutilboð er stofnað eða Standandi sölupöntun.  
* Sameina birgðamagn með saman magn til-pöntunar.  

Í samsaftanlegu ferlinu eru vörur settar saman fyrir sölupöntun. Það er ein Tenging milli samsetningarpöntunar og sölupöntunarinnar.  

Þegar verið er að færa inn saman vöru til-pöntunar í sölupöntunarlínu, stofnast samsetningarpöntun sjálfkrafa. Samsetningarpöntunin er byggð á sölulínu og línur hennar eru byggðar á SAMSETNINGARUPPSKRIFT vörunnar. Magn íhluta í samsetningaruppskriftinni er margfaldað með pöntunarmagni.  **Á síðunni línur**  á milli lína birtast upplýsingar um tengdar samsetningarpöntunarlínur. Upplýsingarnar geta auðveldað að sérsníða samsetningarvöruna. Afhendingardagsetningin er byggð á framboði íhluta. Ef fræðast á um þing-vörur fyrir sölupantanir er farið í að  [selja vörur saman til pöntunar](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
> Þó að hún sé ekki hluti af sjálfgefnu ferli er hægt að selja birgðamagn og setja saman magn til magns í sömu sölupöntun. Til að fræðast meira um birgðir og setja saman vörur á lager er farið í að  [selja birgðavörur í saman-til-Pöntunarstreymi](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

Til að tilgreina að vara sé sett saman-til-pöntunar, í  **reitnum Samsetningarregla**  á  **birgðaspjaldinu**  síðu fyrir vöruna, skal velja  **setja saman pöntun**.  

## Setja saman á lager

Nota skal samsetningarferlið, til að taka saman birgðir, og geyma fyrir síðari sölu. Samsettar vörur á lager eru staðlaðar vörur, eins og pakkað pökkum, sem þú Sérsníður ekki. Einnig er hægt að nota þessar vörur sem undirsamsetningaríhluti. Vörurnar eru teknar til og unnar í stökum vörum og eru meðhöndlaðar sem tilbúnar framleiðsluvörur. Til að fræðast meira um samsetningarvörur er farið í  [setja saman atriði](assembly-how-to-assemble-items.md).  

Þegar sett er saman birgðavara á lager í sölulínu er varan meðhöndluð eins og öll önnur vara sem seld er úr birgðum. Til dæmis er  [!INCLUDE [prod_short](includes/prod_short.md)]  aðeins tiltækt framboð fyrir samsettu vöruna og ekki íhluti hennar.  

> [!NOTE]  
> Þrátt fyrir að hún sé ekki hluti af sjálfgefnu ferli er hægt að setja saman vöru til að panta jafnvel þótt varan sé sett upp til Hlutabréfakaup. Lærðu meira á  [að selja samsettar vörur og birgðavörur saman](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

Til að tilgreina að vara sé sett saman við birgðir, í  **reitnum Samsetningarregla**  á  **birgðaspjaldinu**  -síðunni fyrir vöruna, skal velja  **setja saman birgðir**.  

## Samsetning atburðarásar

Þegar saman-til-pöntunar-og birgðamagn er sameinað sölupöntun þarf að setja magn saman til að magnið sé sent fyrst.  

Ef söfnunarpöntun er tengd við sölupöntunarlínu er gildið í  **reitnum Magn til að setja saman við í pöntunarreitnum**  í sölupöntunarlínunni afritað  **í það magn sem á að setja saman**  í gegnum  **magnreitinn**  í samsetningarpöntuninni. Læra meira at  [selja vörur saman til að panta](assembly-how-to-sell-items-assembled-to-order.md).  

Gildið í  **reitnum Magn til að setja saman**  við er tengt  **reitnum Magn til sendingar**  í sölupöntunarlínunni. Þessi tengsl tengjast því hvernig magn er skipað upp að hluta og að öllu saman:

* Þegar heildarmagnið á sölupöntunarlínunni er sett saman við pöntun
* Í samsettri atburðarás þar sem hluti magns er settur saman við pöntun og hluti er sendur úr birgðum.

Samsetningaraðstæður leyfa sveigjanleika fyrir hlutaafhendingar. Hægt er að nota  **magnið til að setja saman**  reitinn til að tilgreina magnið sem á að senda að hluta úr birgðum og með því að leggja til.  

Ef magnið í fullu sölulínunni verður að vera sett saman við pöntun og afhent er gildið í  **reitnum Magn til afhendingar**  afritað  **í magnið sem á að setja saman**  við tengda samsetningarpöntunina þegar magninu í sendist er breytt. Þessi uppfærsla tryggir að magnið sem verið er að afhenda sé að fullu lagt til magns fyrir saman-pöntunarmagnið.  

Í samsettri atburðarás er þó fullt gildið í reitnum  **Magn til sendingar**  ekki afritað  **í magnið sem á að setja saman**  við samsetningarpöntunina. Í staðinn er sjálfgildi sett inn í  **magnið til að setja saman**  svæði. Gildið er reiknað út úr  **reitnum Magn til sendingar**  til að tryggja að magnið sem er sett saman sé skipað út fyrst.

Til að víkja frá sjálfgildi, t.d. vegna þess að aðeins er ætlunin að setja saman meira eða minna af magninu í reitinn Magn til sendingar  **er hægt að breyta**  magninu til að setja saman  **svæði í**  fyrirfram skilgreindum reglum eins og sýnt er hér að neðan.  

Dæmi um hvers vegna breyta á magninu sem á að setja saman er að hluta til bókuð á birgðamagn áður en samsetningarframleiðsla er skipanleg.  

Eftirfarandi tafla útskýrir reglurnar sem skilgreina lágmarks- og hámarksgildi sem hægt er að færa inn í reitinn **Magn til samsetningar** til að víkja frá sjálfgildinu í samsetningardæmi. Taflan sýnir samsetningardæmi þar sem reiturinn **Magn afhent** í tengdu sölupöntunarlínunni er breytt úr 7 í 4 og **Magn sett saman** verður þess vegna að sjálfgefnu 4.  

**Sölupöntunarlínu**

|                | **Magn** | **Magn til afhendingar** | **Magn til samsetningar til pöntunar** | **Afhent magn** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Upphafsgildi**| 10          | 7                | 7                             | 0                    |
|**Breyting**      |              | 4                |                               |                      |

**Haus samsetningar pöntunar**

|                | **Magn** | **Magn til afhendingar** | **Magn til samsetningar til pöntunar** | **Afhent magn** |
|----------------|--------------|------------------|-------------------------------|----------------------|
|**Upphafsgildi**| 7           | 7                | 0                             | 7                    |
|**Breyting**      |              | 4 (sett inn sjálfgefið)|                         |                      |

Samkvæmt þessu dæmi er hægt að breyta  **magninu sem á að setja saman**  á eftirfarandi hátt:  

* Lágmarksmagn sem hægt er að færa inn er 1. Þú verður að setja saman einingarnar að minnsta kosti eina einingu til að selja þær fjórar, miðað við að hinar þrjár séu tiltækar í birgðum.  
* Hámarksmagn sem hægt er að færa inn er 4. Þessi takmörk tryggja að þú skalt ekki setja meira af vörunni en þú þarft fyrir söluna.  

## Sjá einnig .

[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Birgðir](inventory-manage-inventory.md)  
[Warehouse Management Overview](design-details-warehouse-management.md)
[Work with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
