---
title: "Hönnunarupplýsingar - Fast Magn endurpöntunar | Microsoft Docs"
description: "Stefnan Fast endurpöntunarmagn tengist birgðaáætlanagerð á dæmigerðum C-vörum (lágur birgðakostnaður, lítil hætta á úreldingu og / eða mörgum vörum). Þessi stefna er yfirleitt notað í tengslum við pöntunarmark endurspeglar fyrirsjáanlegs eftirspurn meðan á afhendingartími vörunanr stendur."
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
ms.openlocfilehash: 7726a1b5749aa4da14d06d3484ee83668531f84f
ms.contentlocale: is-is
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-fixed-reorder-qty"></a>Hönnunarupplýsingar: Fast Magn endurpöntunar
Stefnan Fast endurpöntunarmagn tengist birgðaáætlanagerð á dæmigerðum C-vörum (lágur birgðakostnaður, lítil hætta á úreldingu og / eða mörgum vörum). Þessi stefna er yfirleitt notað í tengslum við pöntunarmark endurspeglar fyrirsjáanlegs eftirspurn meðan á afhendingartími vörunanr stendur.  

## <a name="calculated-per-time-bucket"></a>Reiknuð fyrir hvern tímaramma  
 Ef áætlanakerfið greinir að endurpöntunarmarkinu hafi verið náð eða farið yfir það innan tiltekins tímaramma (endurpöntunarferli) – yfir eða við endurpöntunarmarkið í upphafi tímabilsins og undir því eða við það í lokin – leggur það til stofnun nýrrar birgðapöntunar á tilgreinda endurpöntunarmagninu og áætlar það áfram frá fyrstu dagsetningunni eftir lok tímarammans.  

 Hugtakið um hólfað endurpöntunarmark dregur úr fjölda framboðstillaga. Þetta endurspeglar handvirkt ferli af því að fara oft inn á lager til að athuga raunverulegt innihald í hinum ýmsu hólfum.  

## <a name="creates-only-necessary-supply"></a>Stofanr aðeins nauðsynlegar birgðir  
 Áður en ný birgðapöntun er lögð til til að mæta endurpöntunarmarki, kannar áætlanakerfið hvort framboð hafi verið pantað eða móttekið innan afhendingartíma vörunnar. Ef núverandi birgðapöntun leysir vandamálið með því að færa áætlaðar birgðir að eða yfir endurpöntunarmarkið innan afhendingartímans leggur kerfið ekki til nýja birgðapöntun.  

 Birgðapantanri sem eru búnar til sérstaklega til að mæta pöntunarmark er útilokuð frá venjulegum framboðsjöfnun, og mun ekki á nokkurn hátt hægt að breyta eftirá. Þar af leiðandi, ef á að áfangaskipta út vöru með endurpöntunarmarki (ekki endurnýja) er ráðlegt að endurskoða útistandandi birgðapantanir handvirkt eða breyta endurpöntunarstefnu í Lotu fyrir lotu, þannig að kerfið dragi úr eða afturkalli umframbirgðir.  

## <a name="combines-with-order-modifiers"></a>Samsett við Breytingalykla  
 Pantanabreytingarnar, Lágmarksmagn pöntunar, Hámarksmagn pöntunar og Margföld pöntun, ættu ekki að gegna stóru hlutverki þegar notuð er stefnan um fast pöntunarmagn. Hins vegar reiknar áætlanakerfið enn með þessum breytingalyklum og minnkar magnið í tilgreint hámarkspöntunarmagn (og býr til tvær eða fleiri birgðir til að ná heildarpöntunarmagninu), eykur pöntunina í tilgreint lágmarkspöntunarmagn, eða námundar pöntunarmagnið upp til að ná tiltekinni margfaldri pöntun.  

## <a name="combines-with-calendars"></a>Sameinast dagbók  
 Áður en ný birgðapöntun er lögð til til að mæta endurpöntunarmarki, kannar áætlanakerfið hvort pöntunin sé áætluð á frídegi, samkvæmt öllum dagatölum sem eru skilgreind í **Grunndagatalskóði** reitnum í gluggunum **Fyrirtækjaupplýsingar** og **Birgðageymslukort**  

 Ef fyrirhuguð dagsetning er frídagur, færir áætlanakerfið pöntunina áfram á næsta virka dag. Þetta getur orsakað pöntun sem uppfyllir endurpöntunarmark en uppfyllir ekki einhverja tiltekna eftirspurn. Fyrir svona ójafna eftirspurn, býr áætlanakerfið til auka framboð.  

## <a name="should-not-be-used-with-forecast"></a>Ætti ekki að nota við spá  
 Þar sem væntalega eftirspurn er þegar lýst í endurpöntunarmarki er ekki nauðsynlegt að spá í að skipuleggja hlut með endurpöntunarmarki. Ef það er viðeigandi að byggja áætlun á spá skal nota stefnuna lotu-fyrir-lotu.  

## <a name="must-not-be-used-with-reservations"></a>Má ekki nota með frátekningu  
 Ef notandi hefur tekið frá magn, til dæmis magn í birgðum fyrir einhverja fjarlæga eftirspurn, truflar það forsendur áætlunarinnar. Jafnvel þótt áætlað birgðastig sé leyfilegt með tilliti til endurpöntunarmarks, má magnið ekki vera til staðar vegna frátekningarinnar. Kerfið kann að reyna að bæta það upp með því að stofna frávikspantanir. Þó er mælt með því að reiturinn Taka frá sé stilltur á Aldrei fyrir vörur sem eru planaðar með endurpöntunarmarki.  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: Endurpöntunarstefnur](design-details-reordering-policies.md)   
 [Hönnunarupplýsingar: Hámarksmagn](design-details-maximum-qty.md)   
 [Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)   
 [Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
 [Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)

