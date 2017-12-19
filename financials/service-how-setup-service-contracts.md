---
title: "Uppsetning þjónustusamninga | Microsoft Docs"
description: "Lærðu hvernig á að setja upp þjónustusamninga"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 203f6ef7f156bdccaa491fdac761711fd32c317e
ms.contentlocale: is-is
ms.lasthandoff: 12/14/2017

---

# <a name="how-to-set-up-service-contracts"></a>Hvernig á að: setja upp þjónustusamninga
Áður en þú vinnur með samninga verður þú að setja upp eftirfarandi: 

* **Þjónustusamningsflokka** sem sem safna saman þjónustusamningum sem tengjast með einhverjum hætti.
* **Reikningsflokkar þjónustusamninga** eru notaðir til að flokka þjónustusamningsreikningana saman fyrir þjónustureikninga búna til fyrir þjónustusamninga. Þú úthlutar þessa flokka til þjónustusamningum.  
* **Samningssniðmát** sem skilgreinir samningsútlit samninga sem innihalda algengustu atriði í þjónustusamningum. Þegar þjónustusamningstilboð er stofnað er hægt að gera það með sniðmáti. Þegar þú býrð til samningstilboð, innihalda reitirnir sjálfkrafa innihald reitasniðmáts.
* **Sniðmát viðskiptamanna** sem leyfir þér að búa til tilboð fyrir tengiliði eða hugsanlega viðskiptamenn sem er ekki skráðir sem viðskiptamenn í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-set-up-a-service-contract-group"></a>Uppsetning þjónustusamningsflokka  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustusamningsflokkar** og velja svo viðeigandi tengil.  
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velja gátreitinn **Afsl. aðeins af samn. pöntunum** svo samnings- eða þjónustuafsláttur gildi aðeins um samningsþjónustupantanir, svo sem viðhald.  

## <a name="to-set-up-a-service-contract-account-group"></a>Uppsetning reikningsflokkaþjónustusamninga  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Reikningsflokkar þjónustusamninga** og velja svo viðeigandi tengil.  
2. Nýr reikningsflokkur þjónustusamninga er stofnaður.   
3. Fyllt er í reitina **Kóti** og **Lýsing**. Í þessum reitum er lýsing á þjónustureikningsflokknum.  
4. Reiturinn **Reikn. Eftirágreiddra samninga** er fylltur út, velja skal númer fjárhagsreikningsins fyrir reikninginn sem er ekki fyrirframgreiddur.  
5. Í reiturinn **Reikn. Fyrirframgreiddra samninga** skal velja númer fjárhagsreikningsins fyrir reikninginn sem er fyrirframgreiddur.  

## <a name="to-set-up-a-contract-template"></a>Uppsetning samningssniðmáts  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónustusamningssniðmát** og velja svo viðeigandi tengil.  
2. Nýtt þjónustusamningssniðmát er stofnað.  
3. Í reitnum **númer** er fært inn númer fyrir samningur sniðmát.  
  
     Hafi númeraröð fyrir þjónustupantanir verið sett upp í glugganum **Þjónustukerfisgrunnur** er einnig hægt að styðja á færslulykilinn þannig að kerfið færi inn næsta lausa samningssniðmátsnúmer. Hinir reitirnir eru fylltir út, ef það á við.  
  
4. Á flýtiflipanum **Reikningur** er fyllt út reitinn **Kóði fyrir reikningaflokk þjónustusamninga**, **Reikningstímabil** o. s. frv. Hinir reitirnir eru fylltir út, ef það á við.  
5. Velja aðgerðina **Þjónustuafsláttur** til að bæta við samningsafslætti.  

## <a name="to-set-up-a-customer-template"></a>Uppsetning sniðmáts viðskiptamanns  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **viðskiptamaður sniðmát** og velja svo viðeigandi tengil.  
2. Nýtt  sniðmátsspjald viðskiptamannser stofnað.  
3. Á flýtiflipanum **Almennt** er ritaður kóti og lýsing fyrir sniðmát viðskiptamanns í reitina **Kóti** og **Lýsing**. 
4. Aðrir reitir, til dæmis **Landssvæðis kóði**, **Umsjónarsvæðiskóði** og **Kóði tungumáls**, eru notaðir sem leitarskilyrði og þá má fylla út.  
5. Fylla þarf út reitina **Alm. viðsk.bókunarflokkur** og **Bókunarflokkur viðskm.**.  

## <a name="see-also"></a>Sjá einnig
[Þjónustustýring sett upp](service-setup-service.md)
