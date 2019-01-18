---
title: Endurflokka eignir| Microsoft Docs
description: "Eign er endurflokkuð til að flytja hana yfir í aðra deild, skipta henni upp eða sameina hana öðrum eignum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 81b23fd28426d5241ce24b2a3bd40a5b3ec3379d
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="transfer-split-or-combine-fixed-assets"></a>Flytja, skipta upp eða sameina eignir
Þú notar eignaendurflokkunarbókina til að flytja til eignir, skipta þeim upp og sameina þær. Skoða eða prenta útkomu eignaendurflokkunar með skýrslunni **Bókfært Virði eignar 02** skýrslu.

## <a name="to-transfer-a-fixed-asset-to-a-different-department"></a>Að færa eign í aðra deild
Þú gætir þurft að flytja eignir í aðra deild þegar t.d. þú setja eign í framleiðsludeildina meðan verið er að búa hana til og flytja hana svo í stjórnunardeildina þegar lokið er við hana.  

1. Uppsetning nýrrar eignar. Nýr deild er færður inn í reitinn **Deildarkóði**.
2. Úthluta eigna-/afskriftabók á nýju eignina. Nánari upplýsingar eru í [Komast yfir eignir](fa-how-acquire.md).
3. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **eignaendurflokkunarbók** og veldu síðan tengda tengilinn.
4. Stofna endurflokkunarbók þar sem **Eignanr.** reiturinn inniheldur upphaflega eign og **Nýtt Eignanr.** reiturinn inniheldur nýju eignina sem á að færa.  
5. Valið er **endurflokka** aðgerð.

    Línurnar tvær eru nú stofnaðar í eignafjárhagsbókinni með því að nota sniðmátið og keyrsluna sem tilgreind voru á síðunni **uppsetning eignabókar** fyrir tilgreinda afskriftabók. Frekari upplýsingar eru í [Uppsetning afskriftir eigna](fa-how-setup-depreciation.md).
6. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignafjárhagsbækur** og veldu síðan tengda tengilinn.    
7. Á síðunni **fjárhagsbók eigna** er valið **Bóka** aðgerð til að bóka endurflokkun sem framkvæmd var í skrefi 4 til 5.

Ef bókaður hefur verið stofnkostnaður fyrir eina eign er hægt að nota eignaendurflokkunarbókina til að skipta stofnkostnaðinum á nokkrar eignir.  

## <a name="to-split-a-fixed-asset-into-three-fixed-assets"></a>Til að skipta eign í þremur eignir
Hægt er að skipta einni eign í margar eignir, til dæmis þegar þörf er á að skipta eign á þrjú mismunandi deildum. Í því tilfelli geturðu til dæmis að flytja 25 prósent af kaupverði og afskriftum upprunalegrar eignar yfir á aðra eign og 45 prósent yfir á þriðju eignina. Prósenturnar 30 sem eftir eru verða áfram á upphaflegu eigninni.

1. Uppsetning tveggja nýrra eigna. Nýr deild er færður inn í reitinn **Deildarkóði**.
2. Úthluta eigna-/afskriftabók á nýju eignirnar. Nánari upplýsingar eru í [Komast yfir eignir](fa-how-acquire.md).
3. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **eignaendurflokkunarbók** og veldu síðan tengda tengilinn.
4. Búa til tvö endurflokkunarbókarlínur, ein fyrir hverja nýja eign.
5. Í fyrstu línunni er færð inn önnur eignin í reitinn **Nýtt Eignanr.** og 25 í **Endurflokka kaupverð %** reitinn.
6. Í annarri línunni er færð inn þriðja eignin í reitinn **Nýtt Eignanr.** og 40 í **Endurflokka kaupverð %** reitinn.
7. Í báðum línum velja **Endurflokka kaupverð** og **Endurflokka Afskriftir** gátreiti.   
8. Valið er **endurflokka** aðgerð.

    Línurnar tvær eru nú stofnaðar í eignafjárhagsbókinni með því að nota sniðmátið og keyrsluna sem tilgreind voru á síðunni **uppsetning eignabókar** fyrir tilgreinda afskriftabók. Frekari upplýsingar eru í [Uppsetning afskriftir eigna](fa-how-setup-depreciation.md).    
9. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignafjárhagsbækur** og veldu síðan tengda tengilinn.
10. Á síðunni **fjárhagsbók eigna** er valið **Bóka** aðgerð til að bóka endurflokkun sem framkvæmd var í skrefi 4 til og með 8.

## <a name="to-combine-two-fixed-assets-into-one"></a>Sameina tvær eignir í eina
Hægt er að sameina margar eignir í eina eign, til dæmis þegar þú færir skiptum eignum í eina deild. Ef búið er að bóka kaupverð og afskriftir fyrir eignina sem á að færa, verða þessi gildi sameinuð í eina staka eign.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **eignaendurflokkunarbók** og veldu síðan tengda tengilinn.
2. Stofna endurflokkunarbók þar sem **Eignanr.** reiturinn inniheldur eignina sem á að færa/sameina og **Nýtt Eignanr.** reiturinn inniheldur eignina sem hún verður sameinuð við.
3. Láttu Reiturinn **Endurflokka kaupverðs %** auðan til að flytja/sameina allt kaupverð.    
4. Veldu **Endurflokka kaupverð** og **Endurflokka Afskriftir** gátreiti.
5. Í flipanum **Aðgerðir** veljið **Endurflokka**.

    Línurnar tvær eru nú stofnaðar í eignafjárhagsbókinni með því að nota sniðmátið og keyrsluna sem tilgreind voru á síðunni **uppsetning eignabókar** fyrir tilgreinda afskriftabók. Frekari upplýsingar eru í [Uppsetning afskriftir eigna](fa-how-setup-depreciation.md).   
6. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignafjárhagsbækur** og veldu síðan tengda tengilinn.
7. Á síðunni **fjárhagsbók eigna** er valið **Bóka** aðgerð til að bóka endurflokkun sem framkvæmd var í skrefi 2 til og með 5.

## <a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a>Skoða breytt bókfært afskriftarvirði vegna endurflokkunar eigna.
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókað virði eignar 02** og veldu síðan tengda tengilinn.
2. Fyllið inn í svæðin eftir þörfum.
3. Veljið hnappinn **Prenta** eða **Forskoðun**.  

## <a name="see-also"></a>Sjá einnig
[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Hafist handa](product-get-started.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

