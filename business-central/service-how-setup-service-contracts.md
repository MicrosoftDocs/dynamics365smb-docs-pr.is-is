---
title: Uppsetning þjónustusamninga | Microsoft Docs
description: Lærðu hvernig á að setja upp þjónustusamninga
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 216bbd775c66fca619d792ff578d198405fc7612
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781532"
---
# <a name="set-up-service-contracts"></a>Setja upp þjónustusamninga
Áður en þú vinnur með samninga verður þú að setja upp eftirfarandi: 

* **Þjónustusamningsflokka** sem sem safna saman þjónustusamningum sem tengjast með einhverjum hætti.
* **Reikningsflokkar þjónustusamninga** eru notaðir til að flokka þjónustusamningsreikningana saman fyrir þjónustureikninga búna til fyrir þjónustusamninga. Þú úthlutar þessa flokka til þjónustusamningum.  
* **Samningssniðmát** sem skilgreinir samningsútlit samninga sem innihalda algengustu atriði í þjónustusamningum. Þegar þjónustusamningstilboð er stofnað er hægt að gera það með sniðmáti. Þegar þú býrð til samningstilboð, innihalda reitirnir sjálfkrafa innihald reitasniðmáts.
* **Sniðmát viðskiptamanna** sem leyfir þér að búa til tilboð fyrir tengiliði eða hugsanlega viðskiptamenn sem er ekki skráðir sem viðskiptamenn í [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="to-set-up-a-service-contract-group"></a>Uppsetning þjónustusamningsflokka  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Þjónustusamningsflokkar** og veldu síðan tengda tengilinn.  
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velja gátreitinn **Afsl. aðeins af samn. pöntunum** svo samnings- eða þjónustuafsláttur gildi aðeins um samningsþjónustupantanir, svo sem viðhald.  

## <a name="to-set-up-a-service-contract-account-group"></a>Uppsetning reikningsflokkaþjónustusamninga  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókunarflokkur þjónustusamninga** og veldu síðan tengda tengilinn.  
2. Nýr reikningsflokkur þjónustusamninga er stofnaður.   
3. Fyllt er í reitina **Kóti** og **Lýsing**. Í þessum reitum er lýsing á þjónustureikningsflokknum.  
4. Reiturinn **Reikn. Eftirágreiddra samninga** er fylltur út, velja skal númer fjárhagsreikningsins fyrir reikninginn sem er ekki fyrirframgreiddur.  
5. Í reiturinn **Reikn. Fyrirframgreiddra samninga** skal velja númer fjárhagsreikningsins fyrir reikninginn sem er fyrirframgreiddur.  

## <a name="to-set-up-a-contract-template"></a>Uppsetning samningssniðmáts  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Þjónustusamningasniðmát** og veldu síðan tengda tengilinn.  
2. Nýtt þjónustusamningssniðmát er stofnað.  
3. Í reitnum **númer** er fært inn númer fyrir samningur sniðmát.  
  
     Hafi númeraröð fyrir þjónustupantanir verið sett upp á síðunni **Þjónustukerfisgrunnur** er einnig hægt að styðja á færslulykilinn þannig að kerfið færi inn næsta lausa samningssniðmátsnúmer. Hinir reitirnir eru fylltir út, ef það á við.  
  
4. Á flýtiflipanum **Reikningur** er fyllt út reitinn **Kóði fyrir reikningaflokk þjónustusamninga**, **Reikningstímabil** o. s. frv. Hinir reitirnir eru fylltir út, ef það á við.  
5. Velja aðgerðina **Þjónustuafsláttur** til að bæta við samningsafslætti.  

## <a name="to-set-up-a-customer-template"></a>Uppsetning sniðmáts viðskiptamanns  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamannasniðmát** og veldu síðan tengda tengilinn.  
2. Nýtt  sniðmátsspjald viðskiptamannser stofnað.  
3. Á flýtiflipanum **Almennt** er ritaður kóti og lýsing fyrir sniðmát viðskiptamanns í reitina **Kóti** og **Lýsing**. 
4. Aðrir reitir, til dæmis **Landssvæðis kóði**, **Umsjónarsvæðiskóði** og **Kóði tungumáls**, eru notaðir sem leitarskilyrði og þá má fylla út.  
5. Fylla þarf út reitina **Alm. viðsk.bókunarflokkur** og **Bókunarflokkur viðskm.**.  

## <a name="see-also"></a>Sjá einnig
[Þjónustustýring sett upp](service-setup-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]