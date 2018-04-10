---
title: "Staða þjónustupöntunar og staða viðgerða | Microsoft Docs"
description: "Reitirnir **Staða** í glugganum **Þjónustupöntun** og þjónustuvöruviðgerðarstaðan sem vísað er til í reitnum **Viðgerðarstöðukóti** í glugganum **Þjónustupöntun** hafa ákveðið samband í Þjónustukerfi. Þjónustupöntunarstaðan sýnir viðgerðarstöðu allra þjónustuvara í þjónustupöntuninni."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cb4fcab32ffe6b5fe7ae7c30a9d3376ab18a78ca
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="service-order-status-and-repair-status"></a>Þjónustupöntunarstaða og viðgerðarstaða
Reitirnir **Staða** í glugganum **Þjónustupöntun** og þjónustuvöruviðgerðarstaðan sem vísað er til í reitnum **Viðgerðarstöðukóti** í glugganum **Þjónustupöntun** hafa ákveðið samband í Þjónustukerfi. Þjónustupöntunarstaðan sýnir viðgerðarstöðu allra þjónustuvara í þjónustupöntuninni.  
  
> [!NOTE]  
>  Þessir tveir stöðureitir tengjast ekki reitnum **Losunarstaða** á þjónustupöntunarhausnum, sem ákvarðar hvernig vöruhúsið meðhöndlar þjónustuvörur.  
  
 Í hvert sinn sem viðgerðarstöðu þjónustuvöru er breytt í þjónustupöntun er staða pöntunarinnar uppfærð. Til að forritið sýni stöðuna sem sýnir yfirlit yfir viðgerðarstöðuna hjá einstökum þjónustuvörum verður að tilgreina eftirfarandi:  
  
* Staða þjónustupöntunar sem allar viðgerðarstöður tengjast. Frekari upplýsingar eru í Þjónustupöntunarstaða.  
* Forgangsröð fyrir hvern valkost þjónustupöntunarstöðu. Frekari upplýsingar eru í Forgangur.  
  
 Þegar þjónustutilboði er breytt í þjónustupöntun breytir kerfið viðgerðarstöðu hverrar þjónustuvöru í pöntuninni í **Byrjun** og stöðu þjónustupöntunar í **Í undirbúningi**.  
  
## <a name="specifying-service-order-status-for-repair-status"></a>Þjónustupöntunarstaða tilgreind fyrir viðgerðarstöðu  
Hver viðgerðarstaða er tengt tiltekinni þjónustupöntunarstöðu. Valkostirnir fyrir þjónustupöntunarstöðuna eru **Í undirbúningi**, **Í vinnslu**, **Bið** og **Lokið**. Viðgerðarstöðuvalkostir eru eftirfarandi: **Byrjun**, **Í vinnslu**, **Verki vísað**, **Hluta þjónustu lokið**, **Tilboði lokið**, **Beðið eftir viðskiptavini**, **Varahlutur pantaður**, **Varahlutur móttekinn** og **Lokið**.  
  
### <a name="pending"></a>Í undirbúningi  
Þjónustupöntunarstaðan **Í undirbúningi** gefur til kynna að þjónustan geti hafist eða haldið áfram hvenær sem er. Því er hægt að tengja viðgerðarstöðuvalkostina **Byrjun**, **Verki vísað**, **Hluta þjónustu lokið** og **Varahlutur móttekinn** við þjónustupöntunarstöðuna.  
  
### <a name="in-process"></a>Í vinnslu  
Þjónustupöntunarstaðan **Í vinnslu** gefur til kynna að þjónustan sé í vinnslu. Því er hægt að tengja viðgerðarstöðuvalkostina **Í vinnslu** og **Varahlutur pantaður** við þjónustupöntunarstöðuna. Ef staðan **Varahlutur pantaður** er tengd við þjónustupöntunarstöðuna **Í vinnslu** verður einnig að tengja stöðuna **Varahlutur móttekinn** við þessa þjónustupöntunarstöðu.  
  
### <a name="on-hold"></a>Bið  
Þjónustupöntunarstaðan **Bið** gefur til kynna að þjónustan sé um stundarsakir í bið þar sem beðið sé eftir viðbrögðum frá viðskiptavini eða varahlutum áður en þjónustan getur hafist. Því er hægt að tengja viðgerðarstöðuvalkostina **Tilboði lokið**, **Varahlutur pantaður** og **Beðið eftir viðskiptavini** við þjónustupöntunarstöðuna.  
  
### <a name="finished"></a>Lokið  
Þjónustupöntunarstaðan **Lokið** gefur til kynna að þjónustunni sé lokið. Því er viðgerðarstaðan **Lokið** tengd við þessa stöðu.  
  
## <a name="assigning-priority-to-service-order-status"></a>Þjónustupöntunarstöðu úthlutað forgangi  
Þegar viðgerðarstöðu þjónustuvöru er breytt eru þjónustupöntunarstöðurnar tengdar við viðgerðarstöður allra þjónustuvaranna í pöntuninni. Ef þjónustuvaran tengist einni eða fleiri þjónustupöntunarstöðuvalkostum er þjónustupöntunarstöðuvalkosturinn valinn sem gefur mesta forgangsröð.  
  
Ákveða þarf hvaða þjónustupöntunarstöðuvalkostur hefur mikilvægustu upplýsingarnar í stöðunni í þjónustupöntuninni og setja þá stöðu efst í forgangsröðina o.s.frv.  
  
### <a name="example"></a>Dæmi  
Dæmigerð úthlutun forgangsraðar gæti verið sem hér segir:  
  
* Í vinnslu - Mikill  
* Í undirbúningi - Í meðallagi mikill  
* Bið - Í meðallagi lítill  
* Lokið - Lítill  
  
Ef ein þjónustuvara er til dæmis með viðgerðarstöðuna **Byrjun** tengda við þjónustupöntunarstöðuna **Í undirbúningi**, önnur er með viðgerðarstöðuna **Í vinnslu**, tengda við þjónustupöntunarstöðuna **Í vinnslu** og sú þriðja er með viðgerðarstöðuna **Varahlutur pantaður**, tengda við þjónustupöntunarstöðuna **Bið**, verður útkoman staðan **Í vinnslu** þar sem hún er með mestan forgang.  
  
## <a name="see-also"></a>Sjá einnig  
[Setja upp stöður fyrir þjónustupantanir og viðgerðir](service-order-repair-status.md)  
[Þjónustustýring sett upp](service-setup-service.md)  
