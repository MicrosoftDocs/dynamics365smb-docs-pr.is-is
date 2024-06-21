---
title: Endurflokka eignir
description: 'Eign er endurflokkuð til að flytja hana yfir í aðra deild, skipta henni upp eða sameina hana öðrum eignum.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '5638, 5636, 5640, 5637'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Flytja, skipta upp eða sameina eignir

Þú notar eignaendurflokkunarbókina til að flytja til eignir, skipta þeim upp og sameina þær. Skoða eða prenta útkomu eignaendurflokkunar með skýrslunni **Bókfært Virði eignar 02** skýrslu.

## Að færa eign í aðra deild

Þú gætir þurft að flytja eignir í aðra deild þegar t.d. þú setja eign í framleiðsludeildina meðan verið er að búa hana til og flytja hana svo í stjórnunardeildina þegar lokið er við hana.  

1. Uppsetning nýrrar eignar. Færið inn nýja deild sem vídd.  
2. Úthluta eigna-/afskriftabók á nýju eignina. Nánari upplýsingar eru í [Komast yfir eignir](fa-how-acquire.md).
3. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Endurflokkunarbækur eignar** og velja síðan viðkomandi tengil.
4. Stofna færslubókarlínu þar sem **Eignanr.** reiturinn inniheldur upphaflega eign og **Nýtt Eignanr.** reiturinn inniheldur nýju eignina sem á að færa. Hinir reitirnir eru fylltir út eins og á við.  
5. Valið er **endurflokka** aðgerð.

    Línurnar tvær eru nú stofnaðar í eignafjárhagsbókinni með því að nota sniðmátið og keyrsluna sem tilgreind voru á síðunni **uppsetning eignabókar** fyrir tilgreinda afskriftabók. Frekari upplýsingar eru í [Uppsetning afskriftir eigna](fa-how-setup-depreciation.md).
6. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.    
7. Á síðunni **fjárhagsbók eigna** er valið **Bóka** aðgerð til að bóka endurflokkun sem framkvæmd var í skrefi 4 til 5.

Ef bókaður hefur verið stofnkostnaður fyrir eina eign er hægt að nota eignaendurflokkunarbókina til að skipta stofnkostnaðinum á nokkrar eignir.  

## Til að skipta eign í þremur eignir
Hægt er að skipta einni eign í margar eignir, til dæmis þegar þörf er á að skipta eign á þrjú mismunandi deildum. Í því tilfelli geturðu til dæmis að flytja 25 prósent af kaupverði og afskriftum upprunalegrar eignar yfir á aðra eign og 45 prósent yfir á þriðju eignina. Prósenturnar 30 sem eftir eru verða áfram á upphaflegu eigninni.

1. Uppsetning tveggja nýrra eigna. Færa skal inn viðeigandi deildir sem vídd.  
2. Úthluta eigna-/afskriftabók á nýju eignirnar. Nánari upplýsingar eru í [Komast yfir eignir](fa-how-acquire.md).
3. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Endurflokkunarbækur eignar** og velja síðan viðkomandi tengil.
4. Búa til tvö endurflokkunarbókarlínur, ein fyrir hverja nýja eign.
5. Í fyrstu línunni er færð inn önnur eignin í reitinn **Nýtt Eignanr.** og 25 í **Endurflokka kaupverð %** reitinn.
6. Í annarri línunni er færð inn þriðja eignin í reitinn **Nýtt Eignanr.** og 40 í **Endurflokka kaupverð %** reitinn.
7. Í báðum línum velja **Endurflokka kaupverð** og **Endurflokka Afskriftir** gátreiti.  
8. Valið er **endurflokka** aðgerð.  

    Línurnar tvær eru nú stofnaðar í eignafjárhagsbókinni með því að nota sniðmátið og keyrsluna sem tilgreind voru á síðunni **uppsetning eignabókar** fyrir tilgreinda afskriftabók. Frekari upplýsingar eru í [Uppsetning afskriftir eigna](fa-how-setup-depreciation.md).    
9. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.
10. Á síðunni **fjárhagsbók eigna** er valið **Bóka** aðgerð til að bóka endurflokkun sem framkvæmd var í skrefi 4 til og með 8.

## Sameina tvær eignir í eina

Hægt er að sameina margar eignir í eina eign, til dæmis þegar þú færir skiptum eignum í eina deild. Ef búið er að bóka kaupverð og afskriftir fyrir eignina sem á að færa, verða þessi gildi sameinuð í eina staka eign.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Endurflokkunarbækur eignar** og velja síðan viðkomandi tengil.
2. Stofna endurflokkunarbók þar sem **Eignanr.** reiturinn inniheldur eignina sem á að færa/sameina og **Nýtt Eignanr.** reiturinn inniheldur eignina sem hún verður sameinuð við.
3. Láttu Reiturinn **Endurflokka kaupverðs %** auðan til að flytja/sameina allt kaupverð.  
4. Veldu **Endurflokka kaupverð** og **Endurflokka Afskriftir** gátreiti.
5. Valið er **endurflokka** aðgerð.

    Línurnar tvær eru nú stofnaðar í eignafjárhagsbókinni með því að nota sniðmátið og keyrsluna sem tilgreind voru á síðunni **Uppsetning eignabókar** fyrir tilgreinda afskriftabók. Frekari upplýsingar eru í [Uppsetning afskriftir eigna](fa-how-setup-depreciation.md).   
6. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagsbækur eignar** og velja síðan viðkomandi tengil.
7. Á síðunni **fjárhagsbók eigna** er valið **Bóka** aðgerð til að bóka endurflokkun sem framkvæmd var í skrefi 2 til og með 5.

## Skoða breytt bókfært afskriftarvirði vegna endurflokkunar eigna.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignir - Bókfært virði 02** og velja síðan viðkomandi tengil.
2. Fyllið inn reitina eftir þörfum.
3. Veljið hnappinn **Prenta** eða **Forskoðun**.  

## Sjá einnig .

[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
