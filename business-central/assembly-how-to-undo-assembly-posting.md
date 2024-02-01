---
title: Afturkalla samsetningarbókun
description: Lærðu að leiðrétta mistökin í bókaðri söfnunarpöntun.
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
# <a name="undo-assembly-posting"></a>Afturkalla samsetningarbókun

Afturkalla bókun samsetningarpöntunar til að leiðrétta mistök eða fjarlægja óæskilega bókun.

Þegar bókuð samsetningarpöntun er afturkölluð eru leiðréttingar á leiðréttum birgðafærslum stofnaðar til að bakfæra upprunalegu færslurnar. Hver neikvæð frálagsfærsla fyrir samsetningaríhlutinn er bakfærð með jákvæðri frálagsfærslu. Hver neikvæð notkunarfærsla fyrir samsetningaríhlut er bakfærð með jákvæðri notkunarfærslu. Fastur kostnaður er stofnaður sjálfkrafa á milli leiðréttingarfærslna og upphaflegu færslna til að tryggja nákvæma bakfærslu kostnaðar.  

Þegar fullbókuð samsetningarpöntun er afturkölluð er hægt að endurgera upprunalegu pöntunina. Til dæmis til að gera leiðréttingar áður en það er bókað aftur.  

Þegar bókuð samsetningarpöntun er afturkölluð að öllu leyti er öllum svæðum sem eiga við magnið, svo sem  **samsett magn,** notað magn  **og** Eftirstöðvar  **, sett**  aftur í gildin sem þau höfðu fyrir bókunina.  

Til að endurgera eða endurheimta samsetningarpantanir þarf atriðið í upphaflegu bókuninni að uppfylla eftirfarandi skilyrði:  

* Þetta er enn í birgðum. Það er, það hefur ekki verið selt né á annan hátt neytt þeirra í viðskiptum á útleið.  
* Það er ekki frátekið.  
* Það er í hólfinu sem það var úttak að.  

Aðeins er hægt að endurheimta samsetningarskipanir Ef fjöldi og röð lína í upprunalegu samsetningarpöntuninni eru ekki breyttar.  

> [!TIP]  
> Ef leysa á úr árekstrum vegna breytinga í línunum snúa breytingarnar handvirkt að línunum sem um ræðir áður en bókuð samsetningarpöntun er afturfyrir. Hægt er að bóka samsetningarpöntunina og endurgera hana þegar bókun er afturkölluð.  

Eftirfarandi ferli lýsir því hvernig á að afturkalla bókaðar samsetningarpantanir sem innihalda vörur sem voru settar saman á lager. Til að afturkalla bókaðar samsetningarpantanir með vörum sem settar voru saman til pöntunar er notuð  **afturkalla Sendingaraðgerð**  á tengdri bókaðri afhendingu. Frekari upplýsingar um afturkalla afhendingu fara í  [Bakfæra Færslubókarbókanir og afturkalla innhreyfingar/afhendingar](finance-how-reverse-journal-posting.md). Afturkalla bókaða söfnunarpöntun gerist á sama hátt og lýst er í þeirri grein.  

## <a name="to-undo-posting-of-an-assembly-order"></a>Til að afturkalla bókun samsetningarpöntunar

Hægt er að afturkalla bókaðar samsetningarpantanir að fullu eða að hluta.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókaðar samsetningarpantanir** og velja síðan viðkomandi tengil.  

   Hverja hlutabókun stofnar aðskilda bókaða samsetningarpöntun.  
2. Opna bókaða samsetningarpöntun sem á að afturkalla, og velja síðan aðgerðina **Afturkalla samsetningu**.  

    Ef bókaða samsetningarpöntunin er tengd við fullkomlega bókaða samsetningarpöntun sem hefur verið eytt er hægt að endurgera þá pöntun sem er eytt. Til dæmis gæti verið hægt að afþakka pöntunina vegna þess að hún á að endurvinna hana.  
3. Til að endurgera samsetningarpöntun skaltu velja  **Já**. Til að afturkalla bókunina án þess að endurstofna samsetningarpöntun skaltu velja  **Nei**.  

 **Bakfært**  svæðið á samsetningarpöntuninni breytist í  **Já**. Nú er verið að bakfæra bókun samsetningarpöntunar. Hægt er að vinna alla samsetningarpöntunina ef valið er að endurgera hana eða opna samsetningarpöntunina sem hefur verið endurheimt í upprunalega stöðu.  

> [!NOTE]  
> Til að endurheimta magn úr mörgum bókunum í samsetningarpöntun verður að afturkalla allar bókaðar samsetningarpantanir með því að fylgja þrepum 1 til 3.  

## <a name="see-also"></a>Sjá einnig .

[Samsetningardeild](assembly-assemble-items.md)  
[Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md)  
[Vinna söluskil eða afturkallanir](sales-how-process-sales-returns-cancellations.md)  
[Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md)  
[Birgðir](inventory-manage-inventory.md)  
[Yfirlit yfir](design-details-warehouse-management.md)
[vöruhúsastjórnun vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
