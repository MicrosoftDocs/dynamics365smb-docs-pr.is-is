---
title: Afskráning eða innköllun eignar| Microsoft Docs
description: Nauðsynlegt er að bóka afskráningarvirði þegar þú rýrir, selur eða innkallar eignir.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 041f228a0ea2e34fb9986ebb45e98c1300f02f8d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774031"
---
# <a name="dispose-of-or-retire-fixed-assets"></a>Afskrá eða innkalla eignir

Þegar eign er seld eða afskráð með öðrum hætti verður að bóka afskráningarverðmæti hennar til að reikna út og skrá hagnað eða tap. Afskráningarfærsla verður að vera síðasta færslan sem bókuð er vegna eignar. Vegna eigna sem eru að hluta afskráðar er hægt að bóka eina eða fleiri afskráningarfærslur. Samtala allra bókaðra afskráningarupphæða verður að vera kreditupphæð.  

> [!NOTE]  
> Ef ný eign kemur í stað annarrar verður að skrá bæði söluna á gömlu eigninni (afskráning) og innkaupin á þeirri nýju (kaup). Nánari upplýsingar eru í [Komast yfir eignir](fa-how-acquire.md).  

Eftirfarandi skref gera ráð fyrir að þú hafir þegar sett upp viðkomandi bókunarflokka á síðu **Eignabókunarflokkana**. Frekari upplýsingar er að finna í [Að setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Bóka afskráningu úr fjárhagsbók eigna

1. Veldu táknið ![ljósapera sem opnar eiginleikann „Viðmótsleit“](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"), sláið inn **Eignafjárhagsbók** og veljið síðan tengda tengilinn.  
2. Stofnaður er upprunaleg Færslubókarlína og reitirnir fylltir út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Í reitnum **Eignabókunartegund** er valinn **afskráning**.  
4. Valið er **Setja inn mótreikn. eigna** aðgerð. Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun afskráningar.  

    > [!NOTE]  
    >  Skref 4 virkar eingöngu ef búið er að setja upp eftirfarandi: Í **Eignabókunarflokksspjald** síðunni fyrir bókunarflokkur eigna, inniheldur reiturinn **afskráningarreikningur** debetreikning fjárhags og reiturinn **Mótreikningur afskráningar** inniheldur fjárhagsreikninginn sem á að bóka mótfærslur í fyrir styrkingu. Frekari upplýsingar er að finna í [Að setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Valið er **Bóka** aðgerðin.  

Ef hluti eignar er seldur eða afskráður verður að skipta eigninni upp í hluta áður en hægt er að afskrá. Nánari upplýsingar eru í [Skipta upp, eða sameina eignir](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>Skoðun afskráningarfærslna:
Þegar eign er seld eða afskráð með öðrum hætti er afskráningarverðmæti hennar bókað í fjárhags þar sem má sjá niðurstöðurnar.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignir** og veldu síðan tengda tengilinn.  
2. Valin er eignin sem á að skoða færslur fyrir og veldu síðan aðgerðina **afskriftabækur**.  
3. Valin er afskriftabók sem á að skoða færslur fyrir og veldu síðan aðgerðina **fjárhagsfærslur**.  
4. Veljið línu með **Afskráningu** í reitnum **Eignabókunarflokkur** og veljið síðan aðgerðina **Finna færslur**.  
5. Á síðunni **Finna færslur** skal velja línu fjárhagsfærslu og síðan velja aðgerðina **Sýna tengdar færslur**.  

Síðan **Fjárhagsfærslur** opnast og sýnir færslurnar sem afskráningarfærslan hefur myndað.  

## <a name="see-also"></a>Sjá einnig

[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
[Fjármál](finance.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Finna færslur](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]