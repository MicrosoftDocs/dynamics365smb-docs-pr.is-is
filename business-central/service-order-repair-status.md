---
title: Setja upp stöður fyrir þjónustupantanir og viðgerðir | Microsoft Docs
description: Þú verður að setja upp níu viðgerðarstöðuvalkosti sem sýna framvindu viðgerða og viðhalds á þjónustuvöru í þjónustupöntunum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0c4dd1916f60c424d93d4e225aa87830d34a1fff
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915237"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Setja upp stöður fyrir þjónustupantanir og viðgerðir
Þú verður að setja upp viðgerðarstöðuvalkosti sem sýna framvindu viðgerða og viðhalds á þjónustuvöru í þjónustupöntunum. Gert er ráð fyrir níu mismunandi valkostum viðgerðarstöðu miðað við aðstæður eða aðgerðir sem gripið er til þegar þjónustuvörur eru teknar til þjónustu.  

Þú getur stillt forgang stöðuvalkosti þjónustupöntunar. Fernt kemur til greina: Mikill, Í meðallagi mikill, Í meðallagi lítill og Lítill.  

Þegar viðgerðarstöðu þjónustuvöru í þjónustupöntun er breytt uppfærir kerfi þjónustupöntunarstöðuna. Viðgerðarstaða hverrar þjónustuvöru tengist stöðu þjónustupöntunarinnar. Ef þjónustuvaran tengist tveimur eða fleiri þjónustupöntunarstöðuvalkostum er þjónustupöntunarstöðuvalkosturinn valinn sem gefur mesta forgangsröð.  

## <a name="to-set-up-a-repair-status"></a>Uppsetning viðgerðarstöðu  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðgerðarstaða** og veldu síðan tengda tengilinn.
2. Stofnið nýja viðgerðarstöðu.  
3. Fyllt er í reitina **Kóti** og **Lýsing** .  
4. Í reitnum **Staða þjónustupöntunar** er valin staða pöntunar sem á að tengja viðgerðarstöðuna við. Reiturinn **Forgangur** sýnir forgangi stöðunnar á þjónustupöntun sem valin var.  
5. Veldu viðgerðarstaða Hægt er að velja aðeins eina  
6. Til að hægt sé að bóka þjónustupantanir, þar með taldar þjónustuvörur, með þessa viðgerðarstöðu, skal velja **Bókun leyfð** reitinn.  
7. Til að unnt sé að breyta handvirkt stöðukosti þjónustupöntunar í **Í undirbúningi** í þjónustupöntunum með þjónustuvöru sem hefur þessa viðgerðarstöðu, skal velja **Í undirbúningi staða leyfð** gátreitinn.  
8. Veljið gátreitina **Staðan Í vinnslu leyfð** , **Staðan Lokið leyfð** og **Staðan Í bið leyfð** á sama hátt.
  
## <a name="to-set-up-service-status-priorities"></a>Uppsetning viðgerðarstöðuforgangs  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staða þjónustupöntunar** og veldu síðan tengda tengilinn.  
2. Velja skal þjónustupöntunarstöðuna sem á að forgangsraða.  
3. Í reitnum **Forgangur** er valin forgangsröð sem veita á þjónustupöntunarstöðunni. Endurtakið þetta skref fyrir hvert staða.  

## <a name="see-also"></a>Sjá einnig  
[Þjónustupöntunarstaða og viðgerðarstaða](service-service-order-status-and-repair-status.md)  
[Þjónustustýring sett upp](service-setup-service.md)  
