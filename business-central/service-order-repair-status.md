---
title: Setja upp stöður fyrir þjónustupantanir og viðgerðir | Microsoft Docs
description: Þú verður að setja upp níu viðgerðarstöðuvalkosti sem sýna framvindu viðgerða og viðhalds á þjónustuvöru í þjónustupöntunum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# Setja upp stöður fyrir þjónustupantanir og viðgerðir

Þú verður að setja upp viðgerðarstöðuvalkosti sem sýna framvindu viðgerða og viðhalds á þjónustuvöru í þjónustupöntunum. Gert er ráð fyrir níu mismunandi valkostum viðgerðarstöðu miðað við aðstæður eða aðgerðir sem gripið er til þegar þjónustuvörur eru teknar til þjónustu.  

Þú getur stillt forgang stöðuvalkosti þjónustupöntunar. Fernt kemur til greina: **Mikill**, **Í meðallagi mikill**, **Í meðallagi lítill** og **Lítill**.  

Þegar viðgerðarstöðu þjónustuvöru í þjónustupöntun er breytt uppfærir kerfi þjónustupöntunarstöðuna. Viðgerðarstaða hverrar þjónustuvöru tengist stöðu þjónustupöntunarinnar. Ef þjónustuvaran tengist tveimur eða fleiri þjónustupöntunarstöðuvalkostum er þjónustupöntunarstöðuvalkosturinn valinn sem gefur mesta forgangsröð.  

Áður en hægt er að setja upp viðgerðarstöðu verður að setja upp forgang þjónustustöðu.

## Uppsetning viðgerðarstöðuforgangs

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staða þjónustupöntunar** og svo velja viðeigandi tengil.  
2. Velja skal þjónustupöntunarstöðuna sem á að forgangsraða.  
3. Í reitnum **Forgangur** er valin forgangsröð sem veita á þjónustupöntunarstöðunni.  

Þrep 2 og 3 eru endurtekin þar til búið er að forgangsraða stöðuvalkostunum fjórum. **Í undirbúningi** , **Í vinnslu** , **Lokið** og **Í bið**.  

## Uppsetning viðgerðarstöðu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðgerðarstaða** og svo velja viðeigandi tengil.
2. Stofnið nýja viðgerðarstöðu.  
3. Fyllt er í reitina **Kóti** og **Lýsing**.  
4. Í reitnum **Staða þjónustupöntunar** er valin staða pöntunar sem á að tengja viðgerðarstöðuna við. Reiturinn **Forgangur** sýnir forgangi stöðunnar á þjónustupöntun sem valin var.  
5. Veldu viðgerðarstaða Hægt er að velja aðeins eina Viðgerðarstöðu er ekki hægt að tengja við fleiri en einn valkost fyrir viðgerðarstöðu.  
6. Til að hægt sé að bóka þjónustupantanir, þar með taldar þjónustuvörur, með þessa viðgerðarstöðu, skal velja **Bókun leyfð** reitinn.  
7. Til að unnt sé að breyta handvirkt stöðukosti þjónustupöntunar í **Í undirbúningi** í þjónustupöntunum með þjónustuvöru sem hefur þessa viðgerðarstöðu, skal velja **Í undirbúningi staða leyfð** gátreitinn.  
8. Veljið gátreitina **Staðan Í vinnslu leyfð**, **Staðan Lokið leyfð** og **Staðan Í bið leyfð** á sama hátt.

Skrefin eru endurtekin fyrir hvern valkost viðgerðarstöðu sem á að stofna.

## Sjá einnig

[Þjónustupöntunarstaða og viðgerðarstaða](service-service-order-status-and-repair-status.md)  
[Þjónustustýring sett upp](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]