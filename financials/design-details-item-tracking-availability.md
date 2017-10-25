---
title: "Hönnunarupplýsingar - Vörurakning Framboð | Microsoft Docs"
description: "**Vörurakningarlínurnar** Og **Samantekt vörurakningar** gluggar afla kvikar framboðsupplýsingar fyrir raðnúmer eða lotunúmeri. Tilgangurinn með þessu er að auka gagnsæi fyrir notendur á fylgiskjölum á útleið, svo sem sölupöntunum, með því að sýna þeim hvaða raðnúmerum eða hve mörgum einingum lotunúmers er sem stendur úthlutað á önnur opin fylgiskjöl. Þetta minnkar óvissu sem stafar af tvöfaldri úthlutun og framkallar traust í pantanavinnslum að vörurakningarnúmerin og dagsetningar sem þeir eru að lofa á óbókuðum sölupöntunum sé hægt að uppfylla."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: cacedb1252133c5370e13fda36e984a784217e51
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-item-tracking-availability"></a>Hönnunarupplýsingar: vörurakning framboð
**Vörurakningarlínur** Og **Samantekt vörurakningar** gluggar afla kvikar framboðsupplýsingar fyrir raðnúmer eða lotunúmeri. Tilgangurinn með þessu er að auka gagnsæi fyrir notendur á fylgiskjölum á útleið, svo sem sölupöntunum, með því að sýna þeim hvaða raðnúmerum eða hve mörgum einingum lotunúmers er sem stendur úthlutað á önnur opin fylgiskjöl. Þetta minnkar óvissu sem stafar af tvöfaldri úthlutun og framkallar traust í pantanavinnslum að vörurakningarnúmerin og dagsetningar sem þeir eru að lofa á óbókuðum sölupöntunum sé hægt að uppfylla. Nánari upplýsingar eru í [Upplýsingar um hönnun: Vörurakningarlínur gluggi](design-details-item-tracking-lines-window.md).  

 Þegar þú opnar gluggann **Vörurakningarlínu** eru aðgengisgögn sótt úr töflunni **birgðafærsla** og töflunni **Frátekningarfærsla** án nokkurrar gagnaafmörkunar. Þegar þú velur reitinn **Raðnr.** eða **Lotunr.** opnast glugginn **Samantekt vörurakningar** og birtir samantekt á vörurakningarupplýsingum í töflunni **Frátekningarfærsla**. Þessi samantekt inniheldur eftirfarandi upplýsingar um hvert rað- eða lotunúmer í vörurakningarlínunni:  

|Svæði|Description|  
|---------------------------------|---------------------------------------|  
|**Heildarmagn**|Heildarmagn rað- eða lotunúmers sem er í birgðum.|  
|**Umbeðið magn samtals**|Heildarmagn lotu- eða raðnúmers sem þegar er í beiðni í öllum skjölum.|  
|**Magn í undirbúningi**|Magnið sem er fært inn í núverandi tilvik í glugganum **Vörurakningarlínur** en hefur enn ekki verið skuldbundið í gagnagrunninum.|  
|**Heildarmagn tiltækt**|Tilgreinir tiltækt magn sem notandinn getur tekið frá í þeim gerðum af færslum sem eru í línunni.<br /><br /> Þetta magn er reiknað út frá öðrum reitum í gluggann sem hér segir:<br /><br /> heildarmagn – (umbeðið heildarmagn + núgildandi magn í bið).|  

> [!NOTE]  
>  Einnig er hægt að sjá upplýsingar í töflunni á undan með því að nota aðgerðina **Velja færslur** í glugganum**Vörurakningarlínur**.  

 Til að varðveita gagnasafn frammistöðu, gögn um magn til ráðstöfunar er aðeins sótt einu sinni úr gagnagrunninum þegar þú opnar **Vörurakningarlínur** glugga og nota **Endurnýja Til ráðstöfunar** eiginleikann í glugganum.  

## <a name="calculation-formula"></a>Tegund útreiknings  
 Eins og lýst er í undanfarandi töflu er framboð á tilteknu raðnúmeri eða lotunúmeri reiknað á eftirfarandi hátt.  

 Allt Laust Magn = magn birgða - (öll eftirspurn + magn ekki enn úthlutað á gagnagrunninum  

> [!IMPORTANT]  
>  Þessi formúla gefur til kynna að rað- eða lotunúmer framboðsútreiknings taki aðeins til birgða og hundsi áætlaðar innhreyfingar. Í samræmi hefur framboð sem ekki hefur verið bókað í birgðir ekki áhrif á framboð vörurakningar öfugt við eðlilegt vöruframboð þar sem áætlaðar móttökur eru teknar með.  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: vörurakning](design-details-item-tracking.md)

