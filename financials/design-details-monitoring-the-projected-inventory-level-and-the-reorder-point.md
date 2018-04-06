---
title: "Hönnunarupplýsingar Vöktun áætlaðar birgðastigs og endurpöntunarmark | Microsoft Docs"
description: "Lærðu hvernig birgðaáætlun greinir á milli áætlaðar birgða og áætlaðra tiltækra birgðar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, inventory, planning
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a0e64d96389739c67a9e9f548958fac12e3aca2a
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Hönnunarupplýsingar Vöktun áætlaðar birgðastigs og endurpöntunarmark
Birgðir eru tegund af framboði, en fyrir birgðaáætlanagerð, greinir áætlanakerfið milli tveggja birgðastiga:  

* Áætlaðar birgðir  
* Áætlaðar tiltækar birgðir  

## <a name="projected-inventory"></a>Áætlaðar birgðir  
Upphaflega áætlað birgðir er magn af vergri birgðum, þ.mt framboð og eftirspurn í fortíðinni, jafnvel þótt ekki bókað, þegar áætlanagerð er ræst. Í framtíðinni, verður þetta færanlegar áætlaðar birgðastig sem er viðhaldið af vergu magni frá síðara framboð og eftirspurn vegna þess að þeir eru kynnt eftir tímalínu (hvort sem er fráteknar eða öðrum hætti úthlutað).  

Áætlaðar birgðir skal nota af áætlanakerfinu þegar eftirlit er haft með endurpöntunarmarki og til að ákvarða endurpöntunarmang þegar endurpöntunarstefnan Hámarksmagn er notuð.  

## <a name="projected-available-inventory"></a>Áætlaðar tiltækar birgðir  
Áætlaðar tiltækar birgðir eru hluti af áætluðum birgðum sem eru tiltækar á einhverjum tilteknum tíma til að mæta eftirspurn. Áætlaðar tiltækar birgðir skal nota af áætlanakerfinu þegar eftirlit er haft með öryggisbirgðum.  

Áætlaðar tiltækar birgðir skal nota af áætlanakerfinu þegar eftirlit er haft með öryggisbirgðum, þar sem öryggisbirgðir þurfa alltaf að vera tiltækar til að mæta óvæntri eftirspurn.  

## <a name="time-buckets"></a>Tímarammar  
Góð stjórna á áætluðum birgðum er lykilatriði þegar greina á hvenær endurpöntunarmarki er náð og farið er yfir það og til að ákvarða rétt endurpöntunarmagn þegar endurpöntunarstefnan Hámarksmagn er notuð.  

Eins og fyrr segir er áætlað birgðastig reiknað í upphafi áætlunartímabilsins. Það er brúttó stig sem tekur ekki tillit til frátekninga og svipa‘ðra úthlutun. Til að fylgjast með þessu birgðastig á áætlunarröð, kerfið fylgist uppsöfnuðum breytingar yfir a tímabil , tímarammi. Kerfið tryggir að tímaramminn sé a.m.k. einn dagur þar sem það er nákvæmasta tímaeiningin fyrir birgðir eða eftirspurn.  

## <a name="determining-the-projected-inventory-level"></a>Ákvarða áætlaðar birgðir  
Eftirfarandi röð lýsir því hvernig áætlað birgðastig er ákvarðað:  

* Þegar framboðstilvik, svo sem innkaupapöntun, hefur verið algerlega skipulögð, mun það auka áætlaðar birgðir á skiladegi.  
* Þegar eftirspurnartilvik hefur verið að fullu uppfyllt, mun það ekki minnka áætlaðar birgðir strax. Í staðinn, bókar það minnkunaráminningu, sem er innri skrá sem geymir dagsetningu og magn af framlagi þess til áætlaðra birgða.  
* Þegar síðara framboðstilvik er skipulögð og sett á tímalínu, eru bókaðar minnkunaráminningar rannsakaðar eitt af öðru fram til fyrirhuguðum degi framboðs meðan áætlaðar birgðir eru uppfærðar. Á meðan á þessu ferli getur endurpöntunarmarki innri aukningaráminningar verið náð eða farið yfir það.  
* Ef ný birgðapöntun er innleidd athugar kerfið hvort hún sé færð inn á undan núverandi birgðum. Ef svo er verður nýja framboðið núverandi framboð og mótreikningsaðferðin hefst upp á nýtt.  

Eftirfarandi sýnir mynd af þessari meginreglu:  

![](media/nav_app_supply_planning_2_projected_inventory.png "NAV_APP_supply_planning_2_projected_inventory")  

1. Framboð **Sa** af 4 (fast) lokar Eftirspurn **Da** af -3.  
2. CloseDemand: Búa til lækkunaráminningu -3 (ekki sýnt).  
3. Framboð **Sa** er lokað með afgangi upp á 1 (engin frekari eftirspurn er til).  

     Þetta eykur áætlað birgðastig í +4, á sama tíma og áætlaðar tiltækar birgðir **í boði** verða -1.  

4. Næsta eftirspurn **Sb** af 2 (önnur pöntun) hefur þegar verið sett á tímalínuna.  
5. Kerfið athugar hvort það sé einhver minnkunaráminning á undan **Sb** (það er ekki, þannig að ekki er gripið til aðgerða).  
6. Kerfið lokar framboði **Sb** (ekki fleiri eftirspurn) -annað hvort A: með því að minnka það til 0 hætta við eða B: með því að skilja eftir eins og er.  

     Þetta eykur áætlað birgðastig (A: +0 => +4 eða B: +2 = +6).  

7. Kerfið gerir endanlega athugum: Er einhver minnkunaráminning? Já, það er eitt á dagsetningunni **Da**.  
8. Kerfi bætir við minnkunaráminningu -3 við áætlað birgðastig, annað hvort A: +4 -3 = 1 eða B: +6 -3 = +3.  
9. Í tilviki A býr kerfið til framvirkt áætlaða pöntun sem hefst á degi **Da**  

     Í tilviki B er pöntunarmarki náð og ný pöntun er stofnuð.  

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Endurpöntunarstefnur](design-details-reordering-policies.md)   
[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)   
[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)

