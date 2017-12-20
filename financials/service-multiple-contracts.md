---
title: Margir samningar | Microsoft Docs
description: "Það ræðst af þjónustustigssamkomulagi við viðskiptavin hvort afgreiða verður þjónustuvöru í fleiri en einum þjónustusamningi."
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
ms.openlocfilehash: c4abfbcb3bc182fa14c44c427bc41ebd9d67f6cf
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="multiple-contracts"></a>Margir samningar
Það ræðst af þjónustustigssamkomulagi við viðskiptavin hvort afgreiða verður þjónustuvöru í fleiri en einum þjónustusamningi.  
  
Með því að afgreiða þjónustuvöru undir skv. samningum er hægt að gera eftirfarandi:  
  
* Gefa út mismunandi samninga fyrir sömu þjónustuvöru.  
* Þjónusta varahluti sérstaklega.  
* Taka mið af ólíkri þekkingu sem er nauðsynleg til að þjónusta mismunandi þætti þjónustuvöru, til dæmis vélbúnað og hugbúnað.  
* Tilgreinið mismunandi svartíma og tíðni við þjónustu ólíkra hluta þjónustuvöru.  
* Segja fyrir um ólíka verkþætti sem þarf að vinna í tengslum við þjónustuvöru þegar þjónustuvaran þarfnast mismunandi þjónustu á mismunandi tímabilum.  
* Velja og úthluta réttu samningsnúmeri til þjónustuvörulínu þegar þjónustupöntun er stofnuð.  
* Afgreiða viðeigandi fjárhagslegar upplýsingar um þjónustuvörur og samkomulag um þjónustustig.  
  
Hægt er að skoða eftirfarandi dæmi um notkun margra samninga.  
  
## <a name="creating-multiple-contracts-per-service-item"></a>Margir samningar fyrir hverja þjónustuvöru stofnaðir  
Hægt er að stofna þjónustusamning eða samningstilboð handvirkt fyrir þjónustuvörur sem þegar eru skráðar í samninga sem ekki hefur verið hætt við og eru í eigu sama viðskiptamanns. Þetta er gert með því að fara eins og venjulega í gegnum  ferli til að stofna þjónustusamninga og þjónustusamningstilboð. Frekari upplýsingar, sjá [Hvernig á að: Vinna með þjónustusamninga og þjónustusamningstilboð](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
  
Þegar valið er að bæta þjónustuvöru í samningslínu sem er skráð í öðrum þjónustusamningum eða samningstilboðum birtir kerfið viðvörun þar sem segir að þjónustuvaran tilheyri þegar einum eða fleirum þjónustusamningum eða samningstilboðum. Ef þessi viðvörun er staðfest eru allar viðeigandi upplýsingar um þjónustuvöru afritaðar í nýstofnaða samningslínu.  
  
## <a name="copying-documents"></a>Afritun skjala  
Hægt er að stofna þjónustusamning eða samningstilboð sjálfkrafa fyrir þjónustuvörur sem þegar eru skráðar í öðrum þjónustusamningum eða samningstilboðum með aðgerðinni **Afrita skjal**.  
  
## <a name="creating-service-orders-for-multiple-contracts"></a>Þjónustupantanir stofnaðar út frá mörgum samningum  
Hægt er að stofna þjónustupöntun handvirkt fyrir þjónustuvöru sem skráð er í marga virka samninga. Þjónustusamningur er virkur þegar hann er undirritaður og ekki útrunninn.  
  
## <a name="see-also"></a>Sjá einnig  
[Uppfylla þjónustusamninga](service-fulfill-service-contracts.md)  
[Hvernig á að: Stofna Þjónustupantanir](service-how-to-create-service-orders.md)  
