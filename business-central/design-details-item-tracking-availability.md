---
title: Hönnunarupplýsingar - Vörurakning Framboð | Microsoft Docs
description: Síður fyrir vörurakningarlínur og samantekt vörurakningar veita gagnvirkar framboðsupplýsingar fyrir raðnúmer eða lotunúmer. Tilgangurinn með þessu er að auka gagnsæi fyrir notendur á fylgiskjölum á útleið, svo sem sölupöntunum, með því að sýna þeim hvaða raðnúmerum eða hve mörgum einingum lotunúmers er sem stendur úthlutað á önnur opin fylgiskjöl.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ac580a9ffebc8d8a3587a9802855af41ca7402cc
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922043"
---
# <a name="design-details-item-tracking-availability"></a>Hönnunarupplýsingar: vörurakning framboð
Síðurnar **Vörurakningarlínur** og **Samantekt vörurakningar** veita gagnvirkar framboðsupplýsingar fyrir raðnúmer eða lotunúmer. Tilgangurinn með þessu er að auka gagnsæi fyrir notendur á fylgiskjölum á útleið, svo sem sölupöntunum, með því að sýna þeim hvaða raðnúmerum eða hve mörgum einingum lotunúmers er sem stendur úthlutað á önnur opin fylgiskjöl. Þetta minnkar óvissu sem stafar af tvöfaldri úthlutun og framkallar traust í pantanavinnslum að vörurakningarnúmerin og dagsetningar sem þeir eru að lofa á óbókuðum sölupöntunum sé hægt að uppfylla. Nánari upplýsingar eru á síðunni [Upplýsingar um hönnun: Vörurakningarlínur](design-details-item-tracking-lines-window.md).  

 Þegar þú opnar síðuna **Vörurakningarlínu** eru aðgengisgögn sótt úr töflunni **birgðafærsla** og töflunni **Frátekningarfærsla** án nokkurrar gagnaafmörkunar. Þegar þú velur reitinn **Raðnr.** eða **Lotunr.** opnast síðan **Samantekt vörurakningar** og birtir samantekt á vörurakningarupplýsingum í töflunni **Frátekningarfærsla** . Þessi samantekt inniheldur eftirfarandi upplýsingar um hvert rað- eða lotunúmer í vörurakningarlínunni:  

|Svæði|Lýsing|  
|---------------------------------|---------------------------------------|  
|**Heildarmagn**|Heildarmagn rað- eða lotunúmers sem er í birgðum.|  
|**Umbeðið magn samtals**|Heildarmagn lotu- eða raðnúmers sem þegar er í beiðni í öllum skjölum.|  
|**Magn í undirbúningi**|Magnið sem er fært inn í núverandi tilvik á síðunni **Vörurakningarlínur** en hefur enn ekki verið skuldbundið í gagnagrunninum.|  
|**Heildarmagn tiltækt**|Tilgreinir tiltækt magn sem notandinn getur tekið frá í þeim gerðum af færslum sem eru í línunni.<br /><br /> Þetta magn er reiknað út frá öðrum reitum á síðuna sem hér segir:<br /><br /> heildarmagn – (umbeðið heildarmagn + núgildandi magn í bið).|  

> [!NOTE]  
>  Einnig er hægt að sjá upplýsingar í töflunni á undan með því að nota aðgerðina **Velja færslur** á síðunni **Vörurakningarlínur** .  

 Til að varðveita gagnasafn frammistöðu, gögn um magn til ráðstöfunar er aðeins sótt einu sinni úr gagnagrunninum þegar þú opnar **Vörurakningarlínur** glugga og þegar þú notar **Endurnýja Til ráðstöfunar** eiginleikann á síðunni.  

## <a name="calculation-formula"></a>Tegund útreiknings  
 Eins og lýst er í undanfarandi töflu er framboð á tilteknu raðnúmeri eða lotunúmeri reiknað á eftirfarandi hátt.  

 Allt Laust Magn = magn birgða - (öll eftirspurn + magn ekki enn úthlutað á gagnagrunninum)  

> [!IMPORTANT]  
>  Þessi formúla gefur til kynna að rað- eða lotunúmer framboðsútreiknings taki aðeins til birgða og hundsi áætlaðar innhreyfingar. Í samræmi hefur framboð sem ekki hefur verið bókað í birgðir ekki áhrif á framboð vörurakningar öfugt við eðlilegt vöruframboð þar sem áætlaðar móttökur eru teknar með.  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: vörurakning](design-details-item-tracking.md)
