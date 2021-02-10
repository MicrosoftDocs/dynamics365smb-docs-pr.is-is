---
title: Hvernig á að afturkalla samsetningarbókun | Microsoft Docs
description: Stundum gæti þurft að afturkalla bókaða samsetningarpöntun, til dæmis ef pöntunin var bókuð með mistökum sem þarf að leiðrétta, eða vegna þess að hana hefði ekki átt að bóka til að byrja með og verður því að afturkalla.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d672b28dda7c586bd68412fbbb89fb8e33cba1b8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747316"
---
# <a name="undo-assembly-posting"></a>Afturkalla samsetningarbókun
Stundum gæti þurft að afturkalla bókaða samsetningarpöntun, til dæmis ef pöntunin var bókuð með mistökum sem þarf að leiðrétta, eða vegna þess að hana hefði ekki átt að bóka til að byrja með og verður því að afturkalla.

Þegar bókuð samsetningarpöntun er bókuð er færslubunki stofnaður í birgðahöfuðbók til að snúa við upphaflegum færslum. Hver neikvæð frálagsfærsla fyrir samsetningaríhlutinn er bakfærð með jákvæðri frálagsfærslu. Hver neikvæð notkunarfærsla fyrir samsetningaríhlut er bakfærð með jákvæðri notkunarfærslu. Fastur kostnaður er stofnaður sjálfkrafa á milli leiðréttingarfærslna og upphaflegu færslna til að tryggja nákvæma bakfærslu kostnaðar.  

Þegar fullbókuð samsetningarpöntun er afturkölluð er hægt að velja að útbúa pöntunina aftur á upphaflegu sniði, t.d. til að gera leiðréttingar áður en hún er bókuð á ný. Að öðrum kosti er hægt að velja að endurstofna ekki samsetningarpöntunina.  

Þegar afturkalla á hlutabókaða samsetningarpöntun verða allir tilheyrandi magnreitir, s.s. **Samsett magn** **Notað magn** og **Eftirstandandi magn** að vera færðir aftur í þau gildi sem voru áður en á bókað var.  

Til að endurheimta eða endurstofna samsetningarpantanir verða eftirfarandi skilyrði að eiga við samsetningarvöruna sem var frálag í upprunalegu bókuninni:  

-   Hún verður að vera enn í birgðum, þannig að hún sé ekki seld eða á annan hátt notuð af færslum á útleið.  
-   Hún má ekki vera frátekin.  
-   Það verður að vera til í hólfinu sem það var sett í sem frálag.  

Auk þess er aðeins hægt að endurheimta samsetningarpantanir ef línunúmer og línuröð í upphaflegu samsetningarpöntuninni hafa ekki breyst.  

> [!TIP]  
>  Til að leysa úr árekstrum vegna línubreytinga er hægt að afturkalla breytingarnar á umræddum línum handvirkt áður en tengda bókaða samsetningarpöntunin er afturkölluð. Einnig er hægt að bóka samsetningarpöntunina að fullu og velja síðan að endurstofna hana þegar bókunin er afturkölluð.  

Eftirfarandi ferli lýsir því hvernig eigi afturkalla bókaðar samsetningarpantanir þar sem vörurnar voru settar saman í birgðir. Eigi að afturkalla bókaðar samsetningarpantanir þar sem vörur voru settar saman í sölupöntun þarf að nota aðgerðina **Afturkalla afhendingu** í bókuðu afhendingunni sem tengist bókuðu samsetningarpöntuninni. Frekari upplýsingar er að finna í [Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md). Afturköllun bókaðrar samsetningarpöntunar gerist síðan sjálfkrafa eins og lýst er í þessu efnisatriði.  

## <a name="to-undo-posting-of-an-assembly-order"></a>Til að afturkalla bókun samsetningarpöntunar  
1.  Til að afturkalla bókaða samsetningarpöntun eða pöntun sem hefur verið bókuð að hluta, veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókaðar samsetningarpantanir** og veldu síðan tengda tengilinn.  

    Síðan **Bókaðar samsetningarpantanir** opnast og birtir eina eða fleiri bókaðar samsetningarpantanir sem eru bókaðar úr viðkomandi samsetningarpöntun. Hverja hlutabókun stofnar aðskilda bókaða samsetningarpöntun.  
2.  Opna bókaða samsetningarpöntun sem á að afturkalla, og velja síðan aðgerðina **Afturkalla samsetningu**.  

    Ef bókuð samsetningarpöntun sem á að afturkalla tengist fullbókaðri samsetningarpöntun sem nú hefur verið eytt er hægt að endurstofna hana, yfirleitt til þess að endurvinna hana.  
3.  Ef endurgera á samsetningarpöntunina skal velja hnappinn **Já**. Til að afturkalla bókunina án þess að endurstofna tengdu samsetningarpöntunina skal velja hnappinn **Nei**.  

**Frátekið** Svæðið í haus samsetningarpöntunar breytist í **Já**. Bókun samsetningarpöntunarinnar er nú bakfærð, og hægt er að halda áfram að vinna alla samsetningarpöntunina ef valið var að endurstofna hana eða opnu samsetningarpöntunina sem hefur verið færð til baka í upphaflegt horf.  

> [!NOTE]  
>  Til að endurheimta magn úr mörgum hlutabókunum í samsetningarpöntun þarf að afturkalla allar bókaðar samsetningarpantanir sem um ræðir með því að fylgja skrefum 1 til 3 hér að ofan fyrir hverja bókaða samsetningarpöntun.  

## <a name="see-also"></a>Sjá einnig  
[Samsetningardeild](assembly-assemble-items.md)  
[Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md)  
[Vinna söluskil eða afturkallanir](sales-how-process-sales-returns-cancellations.md)    
[Vinna með uppskriftir](inventory-how-work-BOMs.md)  
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
