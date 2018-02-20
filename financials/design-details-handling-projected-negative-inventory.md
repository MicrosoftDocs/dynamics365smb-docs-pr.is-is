---
title: "Hönnunarupplýsingar - Meðhöndlun Áætlaðrar Neikvæðra birgða | Microsoft Docs "
description: "Endurpöntunarmarkið endurspeglar ætlaða eftirspurn á afhendingartíma vörunnar. Þegar farið er yfir endurpöntunarmark er kominn tími til að panta meira magn. En áætlaðar birgðir verður að vera nógu stórt til að hylja eftirspurn þar til ný pöntun er móttekin. Á meðan ættu öryggisbirgðir að uppfylla sveiflur í eftirspurn að áætluðu þjónustustigi."
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
ms.openlocfilehash: 3436e2a00858a1dbfcbb0a44cb9db32bd7665593
ms.contentlocale: is-is
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-handling-projected-negative-inventory"></a>Hönnunarupplýsingar: Meðhöndlun Áætlaðrar Neikvæðra birgða
Endurpöntunarmarkið endurspeglar ætlaða eftirspurn á afhendingartíma vörunnar. Þegar farið er yfir endurpöntunarmark er kominn tími til að panta meira magn. En áætlaðar birgðir verður að vera nógu stórt til að hylja eftirspurn þar til ný pöntun er móttekin. Á meðan ættu öryggisbirgðir að uppfylla sveiflur í eftirspurn að áætluðu þjónustustigi.  

 Þar af leiðandi lítur áætlanakerfi á það sem neyðarástand ef framtíðareftirspurn er ekki hægt að mæta úr áætlaðar birgðir eða m.ö.o. ef áætlaðar birgðir verða neikvæðar. Kerfið meðhöndlar þannig frávik með því að leggja til nýja birgðapöntun til að uppfylla þann hluta eftirspurnarinnar sem birgðir eða önnur eftirspurn getur ekki uppfyllt. Stærð pöntunar í nýju birgðapöntuninni mun ekki taka tillit til hámarksbirgða eða pöntunarmagns, né heldur til pantanabreytinganna Hámarksmagn pöntunar, Lágmarksmagn pöntunar eða Margföld pöntun. Í Staðinn, mun það endurspegla nákvæmlega skort.  

 Áætlunarlína fyrir þessa gerð birgðapöntunar birtir viðvörunartákn og viðbótarupplýsingar birtast við uppflettingu, til að upplýsa notandann um stöðu mála.  

 Í eftirfarandi dæmi, framboð D táknar neyðarpöntun til að leiðrétta fyrir neikvæðum birgðum.  

 ![](media/nav_app_supply_planning_2_negative_inventory.png "NAV_APP_supply_planning_2_negative_inventory")  

1.  Framboð **A**, fyrstu áætlaðar birgðir, er undir pöntunarmark.  

2.  Nýtt framsendingaráætlað framboð er stofnað (**C**).  

     (Magn = Hámarksbirgðir – Áætlað birgðastig)  

3.  Framboð **A** er lokað með eftirspurn **B**, sem er ekki að öllu leyti annað.  

     (Eftirspurn **B** gæti reynt að áætla framboð C en það gerist ekki samkvæmt tímaramma.)  

4.  Nýtt framboð (**D**) er stofnað til að uppfylla eftirstandandi magn eftirspurnar **B**  

5.  Eftirspurn **B** er lokað (búa til áminningu fyrir áætluðum birgðum).  

6.  Nýjar birgðir **D** eru lokaðar.  

7.  Áætlaðar birgðir er athugaðar. Endurpöntunarmarki hefur ekki verið náð.  

8.  Framboð **C** er lokað (ekki meiri eftirspurn til staðar).  

9. Lokaathugun: Engin útistandandi birgðastigsinnheimtubréf eru eftir.  

> [!NOTE]  
>  Skref 4 endurspeglar hvernig kerfið bregst við í útgáfum fyrr en Microsoft Dynamics NAV 2009 SP1.  

 Þetta lýkur lýsingu miðlægra reglna sem tengjast birgðaáætlunargerð sem byggir á reglum um endurpöntun. Í eftirfarandi kafla er fjallað um einkenni fjögurra studdra endurpöntunarstefna.  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: Endurpöntunarstefnur](design-details-reordering-policies.md)   
 [Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)   
 [Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
 [Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)

