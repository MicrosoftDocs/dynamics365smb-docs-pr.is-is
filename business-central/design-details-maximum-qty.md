---
title: Hönnunarupplýsingar - Hámarksmagn | Microsoft Docs
description: Reglan um hámarksmag er ein leið til að viðhalda birgðum með því að nota endurpöntunarmark.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 857a01bac28d85a35668f3aa01e8807a6f6dc845
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "936648"
---
# <a name="design-details-maximum-qty"></a>Hönnunarupplýsingar: Hámarksmagn
Reglan um hámarksmag er ein leið til að viðhalda birgðum með því að nota endurpöntunarmark.  

 Allt sem gildir um stefnu endurpöntunarmagns gildir einnig um þessa stefnu. Eini munurinn er magnið sem lagt er til sem framboð. Þegar reglan um hámarksmagn rer notuð verður endurpöntunarmagnið skilgrein á virkan hátt samkvæmt ætluðu birgðastigi og verður því yfirleitt mismunandi eftir pöntunum.  

## <a name="calculated-per-time-bucket"></a>Reiknuð fyrir hvern tímaramma  
 Endurpöntunarmarkið er ákvarðað á þeim tímapunkti (við lok tímaramma) þegar áætlanakerfið greinir að farið hefur verið yfir endurpöntunarmark. Á þessum tíma mælir kerfið bilið frá núverandi áætlaðar birgðum upp að tilteknum hámarksbirgðum. Þetta stendur fyrir magnið sem þarf að endurpanta. Kerfið kannar þá hvort birgðir hafi þegar verið pantaðar annars staðar þannig að þær berist innan afhendingartímans og, ef svo er, minnkar magn nýju birgðapöntunarinnar í samræmi við það magn sem þegar hefur verið pantað.  

 Kerfið tryggir að áætlaðar birgðir nái a.m.k. endurpöntunarmarkinu - ef vera skyldi að notandinn hafi gleymt að tilgreina hámarksbirgðagildi.  

## <a name="combines-with-order-modifiers"></a>Samsett við Breytingalykla  
 Það fer eftir uppsetningu, getur það verið best að sameina það hámarksmagn stefnu með breytingalyklum til að tryggja lágmarksupphæð þess magn eða sléttun innkaupaeiningar, eða kljúfa það í fleiri lotur samkvæmt skilgreiningu hámarksmagns.  

## <a name="combines-with-calendars"></a>Sameinast dagbók  
 Áður en ný birgðapöntun er lögð til að mæta endurpöntunarmarki, kannar áætlanakerfið hvort pöntunin sé áætluð á frídegi, samkvæmt öllum dagatölum sem eru skilgreind í **Grunndagatalskóði** reitnum á síðunni **Fyrirtækjaupplýsingar** og **Birgðageymslukort**.  

 Ef fyrirhuguð dagsetning er frídagur, færir áætlanakerfið pöntunina áfram á næsta virka dag. Þetta getur orsakað pöntun sem uppfyllir endurpöntunarmark en uppfyllir ekki einhverja tiltekna eftirspurn. Fyrir svona ójafna eftirspurn, býr áætlanakerfið til auka framboð.  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: Endurpöntunarstefnur](design-details-reordering-policies.md)   
 [Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)   
 [Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
 [Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)
