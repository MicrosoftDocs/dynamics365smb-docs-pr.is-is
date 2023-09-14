---
title: Afskráning eða innköllun eignar
description: Þegar eign er seld eða afskráð með öðrum hætti verður að bóka afskráningarverðmæti hennar til að reikna út og skrá hagnað eða tap.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.search.form: '5628, 5610, 5611, 5629, 5633'
ms.date: 06/15/2021
ms.author: bholtorf
---
# Afskrá eða innkalla eignir

Þegar eign er seld eða afskráð með öðrum hætti verður að bóka afskráningarverðmæti hennar til að reikna út og skrá hagnað eða tap. Afskráningarfærsla verður að vera síðasta færslan sem bókuð er vegna eignar. Vegna eigna sem eru að hluta afskráðar er hægt að bóka eina eða fleiri afskráningarfærslur. Samtala allra bókaðra afskráningarupphæða verður að vera kreditupphæð.  

> [!NOTE]  
> Ef ný eign kemur í stað annarrar verður að skrá bæði söluna á gömlu eigninni (afskráning) og innkaupin á þeirri nýju (kaup). Nánari upplýsingar eru í [Komast yfir eignir](fa-how-acquire.md).  

Eftirfarandi skref gera ráð fyrir að þú hafir þegar sett upp viðkomandi bókunarflokka á síðu **Eignabókunarflokkana**. Frekari upplýsingar er að finna í [Að setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  

## Bóka afskráningu úr fjárhagsbók eigna

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagsbækur eignar** og velja síðan viðkomandi tengil.  
2. Stofnaður er upprunaleg Færslubókarlína og reitirnir fylltir út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Í reitnum **Eignabókunartegund** er valinn **afskráning**.  
4. Valið er **Setja inn mótreikn. eigna** aðgerð. Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun afskráningar.  

    > [!NOTE]  
    >  Skref 4 virkar eingöngu ef búið er að setja upp eftirfarandi: Í **Eignabókunarflokksspjald** síðunni fyrir bókunarflokkur eigna, inniheldur reiturinn **afskráningarreikningur** debetreikning fjárhags og reiturinn **Mótreikningur afskráningar** inniheldur fjárhagsreikninginn sem á að bóka mótfærslur í fyrir styrkingu. Frekari upplýsingar er að finna í [Að setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Valið er **Bóka** aðgerðin.  

Ef hluti eignar er seldur eða afskráður verður að skipta eigninni upp í hluta áður en hægt er að afskrá. Nánari upplýsingar eru í [Skipta upp, eða sameina eignir](fa-how-trans-split-combine.md).  

## Skoðun afskráningarfærslna:

Þegar eign er seld eða afskráð með öðrum hætti er afskráningarverðmæti hennar bókað í fjárhags þar sem má sjá niðurstöðurnar.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignir** og velja síðan viðkomandi tengil.  
2. Valin er eignin sem á að skoða færslur fyrir og veldu síðan aðgerðina **afskriftabækur**.  
3. Valin er afskriftabók sem á að skoða færslur fyrir og veldu síðan aðgerðina **fjárhagsfærslur**.  
4. Veljið línu með **Afskráningu** í reitnum **Eignabókunarflokkur** og veljið síðan aðgerðina **Finna færslur**.  
5. Á síðunni **Finna færslur** skal velja línu fjárhagsfærslu og síðan velja aðgerðina **Sýna tengdar færslur**.  

Síðan **Fjárhagsfærslur** opnast og sýnir færslurnar sem afskráningarfærslan hefur myndað.  

## Sjá tengda [Microsoft þjálfun](/training/modules/dispose-fixed-assets/)

## Sjá einnig .

[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
[Fjármál](finance.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Finna færslur](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
