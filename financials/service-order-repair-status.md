---
title: "Setja upp stöður fyrir þjónustupantanir og viðgerðir | Microsoft Docs"
description: "Þú verður að setja upp níu viðgerðarstöðuvalkosti sem sýna framvindu viðgerða og viðhalds á þjónustuvöru í þjónustupöntunum."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8ffd5d6893b2b6c8ce7b7377c586f4f5414279b5
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Setja upp stöður fyrir þjónustupantanir og viðgerðir
Þú verður að setja upp viðgerðarstöðuvalkosti sem sýna framvindu viðgerða og viðhalds á þjónustuvöru í þjónustupöntunum. Gert er ráð fyrir níu mismunandi valkostum viðgerðarstöðu miðað við aðstæður eða aðgerðir sem gripið er til þegar þjónustuvörur eru teknar til þjónustu.  

Þú getur stillt forgang stöðuvalkosti þjónustupöntunar. Fernt kemur til greina: Mikill, Í meðallagi mikill, Í meðallagi lítill og Lítill.  
  
Þegar viðgerðarstöðu þjónustuvöru í þjónustupöntun er breytt uppfærir kerfi þjónustupöntunarstöðuna. Viðgerðarstaða hverrar þjónustuvöru tengist stöðu þjónustupöntunarinnar. Ef þjónustuvaran tengist tveimur eða fleiri þjónustupöntunarstöðuvalkostum er þjónustupöntunarstöðuvalkosturinn valinn sem gefur mesta forgangsröð.  

## <a name="to-set-up-a-repair-status"></a>Uppsetning viðgerðarstöðu  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **viðgerðarstaða** og velja svo viðeigandi tengil. 2. Stofnið nýja viðgerðarstöðu.  
3. Fyllt er í reitina **Kóti** og **Lýsing**.  
4. Í reitnum **Staða þjónustupöntunar** er valin staða pöntunar sem á að tengja viðgerðarstöðuna við. Reiturinn **Forgangur** sýnir forgangi stöðunnar á þjónustupöntun sem valin var.  
5. Veldu viðgerðarstaða Hægt er að velja aðeins eina  
6. Til að hægt sé að bóka þjónustupantanir, þar með taldar þjónustuvörur, með þessa viðgerðarstöðu, skal velja **Bókun leyfð** reitinn.  
7. Til að unnt sé að breyta handvirkt stöðukosti þjónustupöntunar í **Í undirbúningi** í þjónustupöntunum með þjónustuvöru sem hefur þessa viðgerðarstöðu, skal velja **Í undirbúningi staða leyfð** gátreitinn.  
8. Veljið gátreitina **Staðan Í vinnslu leyfð**, **Staðan Lokið leyfð** og **Staðan Í bið leyfð** á sama hátt.
  
## <a name="to-set-up-service-status-priorities"></a>Uppsetning viðgerðarstöðuforgangs  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Staða þjónustupöntunar** og velja svo viðeigandi tengil.  
2. Velja skal þjónustupöntunarstöðuna sem á að forgangsraða.  
3. Í reitnum **Forgangur** er valin forgangsröð sem veita á þjónustupöntunarstöðunni. Endurtakið þetta skref fyrir hvert staða.  
  
## <a name="see-also"></a>Sjá einnig  
[Skilja þjónustupöntunarstaða og viðgerðarstaða]()  
[Þjónustustýring sett upp](service-setup-service.md)  

