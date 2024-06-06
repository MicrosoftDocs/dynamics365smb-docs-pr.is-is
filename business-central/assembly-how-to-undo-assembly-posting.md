---
title: Afturkalla samsetningarbókun
description: Fræðast um hvernig rétt mistök í bókaðri samsetningarpöntun eru.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.service: dynamics-365-business-central
---
# Afturkalla samsetningarbókun

Afturkalla bókun samsetningarpöntunar til að leiðrétta mistök eða fjarlægja óumbeðna bókun.

Þegar bókuð samsetningarpöntun er afturköld eru birgðafærslur til leiðréttingar stofnaðar til að bakfæra upphaflegu færslurnar. Hver neikvæð frálagsfærsla fyrir samsetningaríhlutinn er bakfærð með jákvæðri frálagsfærslu. Hver neikvæð notkunarfærsla fyrir samsetningaríhlut er bakfærð með jákvæðri notkunarfærslu. Fastur kostnaður er stofnaður sjálfkrafa á milli leiðréttingarfærslna og upphaflegu færslna til að tryggja nákvæma bakfærslu kostnaðar.  

Þegar afturkallaða fullbókaða samsetningarpöntun er hægt að endurstýra upphaflegu pöntuninni. Til dæmis ef gera á leiðréttingar áður en hún er bókuð aftur.  

Þegar afturköllun samsetningarpöntunar að hluta er afturkölluð eru allir reitir fyrir magn, svo sem Samansett magn **,** Notað magn **og** Eftirstöðvar **(magn) endurheimtir það gildi sem** þeir höfðu fyrir bókunina.  

Til að endurvinna eða endurheimta samsetningarpantanir verður varan í upphaflegu bókuninni að uppfylla eftirfarandi skilyrði:  

* Það er enn í birgðum. Það er að enda hefur hún ekki verið seld eða á annan hátt notuð af færslum á útleið.  
* Hann er ekki frátekinn.  
* Það er í hólfinu sem það var frálag í.  

Aðeins er hægt að endurheimta samsetningarpantanir ef fjölda og röð lína í upphaflegu samsetningarpöntuninni er ekki breytt.  

> [!TIP]  
> Til að leysa úr árekstrum vegna breytinga í línunum skal bakfæra handvirkt breytingarnar á línunum sem um ræðir áður en bókaða samsetningarpöntunin er afturkölluð. Hægt er að bóka samsetningarpöntunina og endurnýja hana síðan þegar bókunin er afturköld.  

Eftirfarandi ferli lýsir því hvernig á að afturkalla bókaðar samsetningarpantanir með vörum sem voru settar saman á lager. Til að afturkalla bókaðar samsetningarpantanir með vörum sem voru settar saman í pöntun skal nota aðgerðina **Afturkalla afhendingu** á tengdri bókuðu afhendingu. Nánari upplýsingar um afturkalaðar afhendingar eru í [Bakfæra bókanabókabók og Afturkalla móttökur/afhendingar](finance-how-reverse-journal-posting.md). Afturkalla bókaða samsetningarpöntun gerist á sama hátt og lýst er í þeirri grein.  

## Til að afturkalla bókun samsetningarpöntunar

Hægt er að afturkalla fullbókaðar samsetningarpantanir eða að hluta.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókaðar samsetningarpantanir** og velja síðan viðkomandi tengil.  

   Hverja hlutabókun stofnar aðskilda bókaða samsetningarpöntun.  
2. Opna bókaða samsetningarpöntun sem á að afturkalla, og velja síðan aðgerðina **Afturkalla samsetningu**.  

    Ef bókuð samsetningarpöntun er tengd fullbókaðri samsetningarpöntun sem hefur verið eytt er hægt að endurstýra eyddu pöntuninni. Til dæmis er hægt að endurstofna pöntunina vegna þess að á að endurskapa hana.  
3. Samsetningarpöntunin er endurnýjuð með því að velja **Já**. Ef afturkalla á bókunina án þess að endurgerð samsetningarpöntunarinnar er Valið **Nr**.  

Reiturinn **Bakfærði** í samsetningarpöntuninni breytist í **Já**. Bókun samsetningarpöntunar er nú bakfærð. Hægt er að vinna alla samsetningarpöntunina ef valið er að endurgera hana eða þá opnu samsetningarpöntun sem endurheimt hefur verið í upphaflegu ástandi.  

> [!NOTE]  
> Til að endurheimta magn úr mörgum hlutabókunum í samsetningarpöntun þarf að afturkalla allar bókaðar samsetningarpantanir með því að fylgja skrefum 1 til 3.  

## Sjá einnig .

[Samsetningardeild](assembly-assemble-items.md)  
[Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md)  
[Vinna söluskil eða afturkallanir](sales-how-process-sales-returns-cancellations.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Birgðir](inventory-manage-inventory.md)  
[Yfirlitsvinna vöruhúsastjórnunar](design-details-warehouse-management.md)
[með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]