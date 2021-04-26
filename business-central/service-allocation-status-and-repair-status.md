---
title: Úthlutunarstaða og viðgerðarstaða | Microsoft Docs
description: Lærðu um sambandið á milli viðgerðarstaða þjónustuvöru og úthlutunarstaða úthlutunarfærslna fyrir þær.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resources, allocation, status, repairs
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 9cf3349d654a4e007079075c64e9e56654619810
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772405"
---
# <a name="allocation-status-and-repair-status-of-service-items"></a>Úthlutunarstaða og viðgerðarstaða
Viðgerðarstaða þjónustuvöru og úthlutarstaða úthlutunarfærslna vegna þjónustuvöru tengjast á vissan hátt í Þjónustukerfi. Úthlutunarstaðan breytist þegar viðgerðarstöðu þjónustuvöru er breytt úr  **Lokið** eða  **Hluta þjónustu lokið** og þegar þjónustutilboði er breytt í þjónustupöntun. Viðgerðarstaða þjónustuvöru breytist þegar hætt er við úthlutun þjónustuvöru eða henni er endurúthlutað til annars forða. Hægt er að skoða viðgerðastöðu þjónustuvöru á síðunni **Þjónustuverk** og hægt er að uppfæra viðgerðarstöðu í **Kóti viðgerðastöðu** á síðunni **Þjónustuvörublað**. Hægt er að skoða úthlutunarstöðuna í reitnum **Staða** á síðunni **Úthlutun forða**.  
  
## <a name="changing-repair-status"></a>Viðgerðarstöðu breytt  
Þegar viðgerðarstöðu þjónustu vöru er breytt í þjónustuvörulínu leitar forritið að samsvarandi úthlutunarfærslu fyrir þessa þjónustuvöru sem hefur stöðuna **Virk**. Ef úthlutunarfærslan finnst er staðan uppfærð á einn af eftirfarandi háttum:  
  
* Ef viðgerðarstaðan breytist í **Lokið** breytir forritið úthlutunarstöðunni úr **Virk** í **Lokið**.  
* Ef viðgerðarstaðan breytist í **Hluta þjónustu lokið** (hluti vinnunnar er búinn) eða **Verki vísað** (engin vinna hafin) breytir forritið úthlutunarstöðunni úr **Virk** í **Þarf að endurúthluta**.  
* Ef úthlutunarfærsla þjónustupöntunar er búin til og gefið er til kynna að engum forða hafi verið úthlutað stillir kerfið **Stöðu** reits á síðunni **Úthlutun forða** á **Óvirkt**.  
* Staða úthlutunarfærslu er stillt á **Hætt við** ef þjónustuvöru sem vísað er til í úthlutunarfærslu er endurúthlutað, sem gefur til kynna að úthlutaður forði eða forðaflokkur hafi ekki reynt þjónustuverkhlutann.  
  
úthlutunarstaðan ber með sér hvort þjónustuverki sé lokið eða hvort annan forða þurfi til þess að ljúka viðkomandi þjónustu.  
  
## <a name="converting-service-quotes-to-service-orders"></a>Þjónustutilboði breytt í þjónustupöntun  
Þegar þjónustutilboði er breytt í þjónustupöntun uppfærir kerfið þjónustupöntunina, þjónustuvöruna í pöntuninni og úthlutunarfærslur með einhverri eftirfarandi aðferða:  
  
* Viðgerðarstöðu þjónustuvörunnar er breytt í **Byrjun**.  
* Staða þjónustupöntunar breytist í **Í undirbúningi**.  
* Leitað er að úthlutunarfærslum vegna allrar þjónustuvörunnar í þjónustupöntuninni sem er með stöðuna **Virk**. Ef slíkar úthlutunarfærsla finnast er stöðu úthlutunar breytt úr **Virk** í **Þarf að endurúthluta**.  
  
## <a name="canceling-allocations"></a>Hætt við úthlutanir  
Þegar úthlutun vegna þjónustuvöru er afturkölluð uppfærir [!INCLUDE[prod_short](includes/prod_short.md)] úthlutunarstöðu samsvarandi úthlutunarfærslu frá **Virk** yfir í **Þörf á endurúthlutun**.

Viðgerðarstaða þjónustuvörunnar í úthlutunarfærslunni er uppfærð sem hér segir:  
  
* Ef viðgerðarstaðan er **Byrjun** er viðgerðarstöðunni breytt í **Verki vísað** (engin þjónusta hefur verið veitt).  
* Ef viðgerðarstaðan er **Í vinnslu** er viðgerðarstöðunni breytt í **Hluta þjónustu lokið** (hluti vinnunnar búinn).  
  
## <a name="reallocating-an-active-allocation-entry"></a>Endurúthluta virkri úthlutnarfærslu  
Þegar þjónustuvöru er endurúthlutað í úthlutunarfærslu sem er **Virk** er úthlutunarfærslan uppfærð sem hér segir:  
  
* Hafi þjónustan hafist þegar úthlutun var **Virk** (hafi viðgerðarstaða þjónustuvörunnar í færslunni breyst í **Í vinnslu**) er úthlutunarstöðunni breytt úr **Virk** í **Lokið**.  
* Hafi þjónusta ekki hafist þegar úthlutun var **Virk** er úthlutunarstöðu breytt úr **Virk** í **Hætt við**.  
  
Viðgerðarstaða þjónustuvörunnar í úthlutunarfærslunni er uppfærð eins og ef úthlutunin hefði verið afturkölluð.  
  
* Ef viðgerðarstaðan er **Byrjun** er viðgerðarstöðunni breytt í **Verki vísað** (engin þjónusta hefur verið veitt).  
* Ef viðgerðarstaðan er **Í vinnslu** er viðgerðarstöðunni breytt í **Hluta þjónustu lokið** (hluti vinnunnar búinn).  
  
Ný úthlutunarfærsla sem inniheldur nýja forðann er stofnuð og fær stöðuna **Virk**.  
  
## <a name="reallocating-a-service-item"></a>Endurúthlutun þjónustuvöru  
Þegar þjónustuvöru er endurúthlutað í úthlutunarfærslu sem er með stöðuna **Þarf að endurúthluta** er úthlutunarfærslan uppfærð sem hér segir:  
  
* Hafi þjónustan hafist þegar úthlutun var **Virk** (hafi viðgerðarstaða þjónustuvörunnar í færslunni breyst í **Í vinnslu**) er úthlutunarstöðunni breytt úr **Þarf að endurúthluta** í **Lokið**.  
* Hafi þjónusta ekki hafist þegar úthlutun var **Virk** er úthlutunarstöðu breytt úr **Þarf að endurúthluta** í **Hætt við**.  
  
Ný úthlutunarfærsla sem inniheldur nýja forðann er stofnuð og fær stöðuna **Virk**.  
  
## <a name="see-also"></a>Sjá einnig  
[Setja upp forðaúthlutanir](service-how-setup-resource-allocation.md)  
[Úthluta forða](service-how-to-allocate-resources.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]