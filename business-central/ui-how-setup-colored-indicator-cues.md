---
title: "Sérstilla sjónræn merki um virkni bendingar | Microsoft Docs"
description: "Setja upp litaðan vísi á ramma bendingar til að útvega sérsniðið sjónrænt merki um virkni bendingar."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c93bd33d972b030ede02ad7b24a8127ff2174141
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-a-colored-indicator-on-cues"></a>Setja upp litaðan vísi á bunka
Þú getur sett upp Bunka sem birtast í **heimasíðu** þannig að þeir innihaldi vísi sem breytir um lit eftir gagnagildum í bunkum.

Vísirinn birtist sem stika efst í ramma bendingarinnar. Veitir sjónrænt merki um virknistöðu bendingarinnar sem getur táknað hagstæð eða óhagstæð skilyrði sem kalla á viðbrögð frá notanda. Ef bunki birtir til dæmis viðvarandi sölureikninga er hægt að stilla vísinn á að vera grænn (jákvætt) þegar heildarfjöldi viðvarandi sölureikninga er undir 10 og rauður (óæskilegt) þegar samtalan er yfir 20.

Í glugganum **uppsetning bunka** seturðu setja upp vísa fyrir allar bendingar sem eru tiltækar í gagnagrunni fyrirtækisins.

Til að setja upp vísi tilgreinirðu allt að tvö þröskuldsgildi sem tilgreina þrjú svið gagnagilda (lágt, miðlungs og hátt) sem hægt er að nota annan lit (eða stíl) við.

## <a name="to-set-up-colored-indicators-on-cues"></a>Til að setja upp litaða vísa í bendingum
1. Undir **Aðgerðir** í notanda **Heimasíðu** , velja **Setja Upp bunka**.  
   Glugginn **uppsetning bunka** birtist. Glugginn birtir vísana sem nú eru uppsettir í bunkum.
2. Til að breyta vísi, breyta reitunum og breyta, t.d. gildi fyrir mismunandi þröskulda.  

Eftirfarandi tafla sýnir liti sem samsvara valkostir af sem **lágsviðsstíll**, **millisviðsstíll**, og **hásviðsstíll** reiti.

| Valkostur | Litur |
| --- | --- |
| **Ekkert** |Enginn litur (sami litur og í bunkareit)|
| **Hagstæð** |Grænt |
| **Slæmt** |Rautt |
| **Tvírætt** |Gult |
| **Undirstig** |Grár |

## <a name="see-also"></a>Sjá einnig
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

