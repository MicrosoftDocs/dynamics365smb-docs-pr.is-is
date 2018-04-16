---
title: "Halda skýrsluútliti nútímalegu | Microsoft Docs"
description: "Stundum þarf að uppfæra sérsniðið skýrsluútlit sem er notað í skýrslu. Þetta er nauðsynlegt þegar breyting hefur verið gerð á hönnun gagnasafns skýrslu, til dæmis ef reitur sem er notaður í útlitinu hefur verið fjarlægður úr gagnasafni skýrslunnar."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 0395cf37d56282684c2a6e4c2066fd9b249f16f0
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="updating-report-or-document-layouts"></a>Uppfæra skýrsluútlit eða skjalaútlit
Stundum þarf að uppfæra sérsniðið skýrsluútlit sem er notað í skýrslu. Þetta er nauðsynlegt þegar breyting hefur verið gerð á hönnun gagnasafns skýrslu, til dæmis ef reitur sem er notaður í útlitinu hefur verið fjarlægður úr gagnasafni skýrslunnar. Ef skýrsluútlit krefst uppfærslu birtast villuboð þegar reynt er að forskoða, prenta eða vista skýrsluna.  
  
Hægt er að uppfæra skýrsluútlit sjálfvirkt úr villuboðunum sem þú færð þegar þú keyrir skýrslu með því að velurðu **Já** hnappinn í villuboðunum. Eða áður en þú keyrir skýrslur, geturðu uppfæra tiltekið útlit skýrslu eða öll sérstillt skýrsluútlit sem gætu orðið fyrir áhrifum af breytingum á gagnamengi.  
  
Einnig býðst sá valkostur að prófa uppfærslur án þess að nota umbeðnar breytingar á sérsniðin skýrsluútliti. Þannig er hægt að sjá hvaða breytringar verða notaðar í skýrsluútliti og greina hugsanleg vandamál í ferlinu. Úr niðurstaða prófunar er hægt að opna sérsniðin skýrsluútlit beint til að breyta og lagfæra villur. Við mælum með því að prófa uppfærslu á skýrsluútliti áður en uppfærslum er beitt.  
  
Ekki geta allar breytingar á skýrsluútliti verið uppfærðar sjálfkrafa í skýrsluútliti. Sumar breytingar krefjast þess að skýrsluútliti sé breytt handvirkt. Frekari upplýsingar eru í [Takmarkanir á uppfærslum skýrsluútlits](ui-update-report-layouts.md#UpdateLimitations).  
  
## <a name="to-update-one-or-more-custom-report-layouts"></a>Uppfærir eitt eða fleiri Sérsniðin skýrsluútlit.  
  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **útliti skýrslu** og velja svo viðeigandi tengil.  
  
2.  Í glugganum **Skýrsluútlit** ef þú vilt uppfæra sérstaka skýrslu, skal velja útlitið af listanum og svo velja aðgerðina **Uppfæra útlit**. Eða, ef þú vilt uppfæra allt sérsniðið skýrsluútlit fyrir fyrirtækið, skal velja aðgerðina **Uppfæra allt útlit**.  

Ef engar villur koma upp er uppfærslan notuð í skýrsluútliti. Ef villur koma upp birtast skilaboð sem innihalda villurnar. Þá þarf handvirkt að breyta sérsniðin skýrsluútlit til að laga villurnar. Frekari upplýsingar eru í [Villur leiðréttar](ui-update-report-layouts.md#FixErrors).  

## <a name="to-test-custom-report-layout-updates"></a>Til að prófa uppfærslur á sérsniðið skýrsluútlit  
  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Val á útliti skýrslu** og velja svo viðeigandi tengil.  
  
2. Í glugganum **Val Útlit skýrslu** er valið aðgerðin **Prufa uppfærsla útlit**.  
  
   Breytingar á skýrsluútliti eru prufaðar en ekki settar upp raunverulega í skýrsluútlitinu. Glugginn **Uppfærslukladdi skýrsluútlits** birtist og sýnir stöðu á mögulegum uppfærslum fyrir hvert skýrsluútlit Ef villur koma upp fyrir skýrsluútlit er hægt að opna skýrsluútlit beint til að breyta og lagfæra villur. Frekari upplýsingar eru í [Villur leiðréttar](ui-update-report-layouts.md#FixErrors).  
  
##  <a name="UpdateLimitations"></a> Takmarkanir á uppfærslum sérsniðins skýrsluútlits  
 Nokkrar gerðir af breytingum getur sjálfvirk uppfærsla notað í sérsniðnu skýrsluútliti, til dæmis ef reitur sem er notaður í útlitinu hefur verið fjarlægður úr gagnasafni skýrslunnar. Sjálfvirk uppfærsla getur hins vegar ekki ráðið við eftirfarandi breytingar á skýrsluútliti.  
  
1. Reitir, merkimiðar eða gagnavörur sem hefur verið eytt.  
  
2. Tvítekning á heitum reita í skýrsluútliti eftir að reitur hefur verið endurnefndur í gagnasafni. Fara skal með þetta sem hönnunargalla.  
  
3. Uppfæra sviðsmyndir þar sem koma fram margar ítrekana á skýrsluútliti sem valda mörgum endurnefningaraðgerðum á sama reit, merkimiði eða gagnahlut.  
  
   Ef uppfærsluferlið greinir þessi vandamál er ekki hægt að nota uppfærsluna. Laga verður þessi vandamál handvirkt, t.d. með því að breyta skýrsluútliti í Word eða með forritun og notkun á uppfærslukóðaeiningum.  
  
##  <a name="FixErrors"></a> Villur leiðréttar  
 Ef þú færð ennþá villuboð við uppfærslu eða prófun á uppfærslu skýrsluútlits þá muntu líklega þurfa að breyta skýrsluútliti til að laga vandamálið. Lesa skal villuboðin til ráða orsök vandamálsins.  
  
 Algengasta vandamálið er þegar reitur sem er notaður í útlitinu hefur verið fjarlægður úr gagnamengi skýrslunnar. Í þessu tilviki er lína í villuboðunum sem segir til um að vara hafi verið fjarlægð. Til að laga þetta þarf að breyta útlitinu og fjarlægja viðkomandi reit.  
  
 Nánari upplýsingar er að finna í [Búa til og breyta sérsniðnu skýrsluútliti](ui-how-create-custom-report-layout.md#ModifyCustomLayout).  
  
 Eftir að útlitinu er breytt skaltu reyna að uppfæra það afur.  
  
## <a name="see-also"></a>Sjá einnig  
 [Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
 [Unnið með Skýrslur](ui-work-report.md)  
