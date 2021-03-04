---
title: Bókunardagsetning á virðisfærslum
description: Lærðu hvernig runuvinnslan Leiðréttur kostnaður - birgðafærslur ber kennsl á og úthlutar bókunardagsetningu fyrir virðisfærslurnar sem runuvinnslan er að búa til.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fe03f25c4f9024cb82b83af915e69073d2fdcf1e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751506"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Hönnunarupplýsingar: Bókunardagsetning á leiðréttingarvirðisfærslu
Þessi grein veitir leiðbeiningar fyrir notendur birgðakostnaðarvirkni í [!INCLUDE[prod_short](includes/prod_short.md)]. Tilgreind grein veitir leiðbeiningar um hvernig runuvinnslan **Leiðréttur kostnaður - Birgðafærslur** ber kennsl á og úthlutar bókunardagsetningu fyrir virðisfærslurnar sem runuvinnslan er að búa til.  

Fyrst er hugmynd ferlisins yfirfarin, hvernig runuvinnslan ber kennsl á og úthlutar bókunardagsetningu fyrir virðisfærsluna sem verður búin til. Eftir það eru nokkrar aðstæður sem við í stuðningshópnum rekumst á af og til og að lokum er samantekt yfir hugtökin sem eru notuð í útgáfu 3.0.  

## <a name="the-concept"></a>Hugtakið  
Frá útgáfu 5.0, runuvinnslan **Leiðrétta kostnað - Birgðafærslur** úthlutar bókunardagsetningu fyrir virðisfærsluna sem hún kemur til með að búa til í eftirfarandi skrefum:  

1.  Upphaflega er bókunardagsetning færslunnar sem á að búa til sú sama og dagsetning færslunnar sem hún leiðréttir.  

2.  Bókunardagsetningin er sannprófuð gagnvart birgðatímabili og/eða fjárhagsgrunni.  

3.  Úthlutun bókunardagsetningu; Ef upphafleg bókunardagsetning er ekki innan leyfilegs dagsetningabils bókunar, þá mun runuvinnslan úthluta leyfilegri bókunardagsetningu frá annað hvort fjárhagsgrunni eða birgðatímabili. Ef bæði birgðatímabil og leyfileg bókunardagsetning í fjárhagsgrunni eru skilgreind, verður síðari dagsetning þessara tveggja úthlutað til leiðréttingarvirðisfærslu.  

 Við skulum yfirfara þetta ferli betur með dæmi. Gerum ráð fyrir að við séum með birgðafærslu fyrir sölu. Þessi hlutur var sendur 5. september 2013 og reikningsfærður daginn eftir.  

![Staða birgðahöfuðbókarfærslna í atburðarásinni](media/helene/TechArticleAdjustcost1.png "Staða birgðahöfuðbókarfærslna í atburðarásinni")  

Hér að neðan táknar fyrsta virðisfærslan (379) sendinguna og bera þær sömu bókunardagsetningu og yfirbirgðafærslan.  

Önnur virðisfærslan (381) táknar reikninginn.  

 Þriðja virðisfærslan (391) er leiðrétting á reikningsfærðri virðisfærslu (381)  

 ![Staða virðisfærslna í atburðarásinni](media/helene/TechArticleAdjustcost2.png "Staða virðisfærslna í atburðarásinni")  

 Skref 1: Leiðréttingarvirðisfærsla sem á að búa til er úthlutað sömu bókunardagsetningu og færslan sem hún leiðréttir, sýnt hér að framan með virðisfærslu 391.  

 Skref 2: Villuleit á upphaflega úthlutaðri bókunardagsetningu.  

Runuvinnslan **Leiðrétta kostnað - Birgðafærslur** ákvarðar hvort upphafleg bókunardagsetning fyrir leiðréttingarvirðisfærslu er innan leyfilegs dagsetningabils bókunar byggt á birgðatímabili og/eða fjárhagsgrunni.  

 Við skulum endurskoða ofangreinda sölu með því að bæta við uppsetningu á leyfilegu dagsetningabili bókunar.  

 Birgðatímabil:  

![Birgðahaldstími í atburðarásinni](media/helene/TechArticleAdjustcost3.png "Birgðahaldstími í atburðarásinni")

 Fyrsta leyfilega bókunardagsetning er fyrsta daginn í fyrsta opna tímabilinu. 1. september 2013.  

 Uppsetning fjárhags:  

![Uppsetning fjárhags í atburðarásinni](media/helene/TechArticleAdjustcost4.png "Uppsetning fjárhags í atburðarásinni")

 Fyrsta leyfilega bókunardagsetning er dagsetningin sem tilgreind er í reitnum Leyfa bókanir frá: 10. september 2013.  

 Ef bæði birgðatímabil og leyfilegar bókunardagsetningar í fjárhagsgrunni eru skilgreind mun síðari dagsetning þessara tveggja skilgreina leyfilegt dagsetningabil bókunar.  

 Skref 3: Úthlutun á leyfilegri bókunardagsetningu;  

 Upphaflega úthlutaða bókunardagsetningin var 6. september eins og sýnt er í skrefi 1. Í 2. skrefi ber runuvinnslan Leiðrétta kostnað - Birgðafærslur kennsl 10. september sem fyrstu leyfilegu bókunardagsetninguna og úthlutar þess vegna 10. september á leiðréttingarvirðisfærsluna fyrir neðan.  

 ![Staða virðisfærslna í atburðarásinni 2](media/helene/TechArticleAdjustcost5.png "Staða virðisfærslna í atburðarásinni 2")

 Við höfum nú yfirfarið hugtakið fyrir úthlutun bókunardagsetninga á virðisfærslur sem eru búnar til af runuvinnslu Leiðrétts kostnaðar - Birgðafærslna.  

 Við skulum halda áfram að yfirfara sumar aðstæður sem við í stuðningshópnum rekumst á af og til í tengslum við úthlutaðar bókunardagsetningar í runuvinnslu Leiðrétts kostnaðar - Birgðafærslna og tengdum uppsetningum.  

## <a name="scenarios"></a>Dæmi  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Aðstæður I: „Bókunardagsetning er ekki innan marka leyfilegra bókunardagsetninga...“  
 Þetta eru aðstæður þar sem notandi fær upp umrædd villuboð þegar runuvinnsla Leiðrétts kostnaðar - Birgðafærsla er keyrð.  

 Í fyrri kafla, sem lýsir hugmyndinni um að gefa út bókunardagsetningar, er ætlunin með runuvinnslu Leiðrétts kostnaðar - Birgðafærslna að búa til virðisfærslu með bókunardagsetninguna 10. september.  

![Villuboð um bókunardagsetningu](media/helene/TechArticleAdjustcost6.png "Villuboð um bókunardagsetningu")

 Við fylgjum eftir notandauppsetningu:  

![Uppsetning heimilaðra bókunardagsetninga fyrir notanda](media/helene/TechArticleAdjustcost7.png "Uppsetning heimilaðra bókunardagsetninga fyrir notanda")

 Notandinn í þessu tilfelli hefur leyfilegt dagsetningabil bókunar frá 11. september til 30. september og er því ekki heimilt að bóka leiðréttingarvirðisfærsluna með bókunardagsetninguna 10. september.  

![Yfirlit yfir virka uppsetningu bókunardagsetningar](media/helene/TechArticleAdjustcost8.png "Yfirlit yfir virka uppsetningu bókunardagsetningar")

 Grein þekkingargrunns [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) fjallar um fleiri aðstæður sem tengjast nefndu villuboði.  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Aðstæður II: Bókunardagsetning á leiðréttingarvirðisfærslum á móti bókunardagsetningu við innfærslu sem veldur leiðréttingu, eins og endurmati eða kostnaðarauka.  

### <a name="revaluation-scenario"></a>Aðstæður endurmats:  
 Skilyrði:  

 Birgðagrunnur:  

-   Sjálfvirk kostnaðarbókun = Já  

-   Sjálfvirk kostnaðarleiðrétting=Alltaf  

-   Meðalkostnaður Teg. útreikn=vara  

-   Meðalkostnaðartímabil=Dagur  

 Uppsetning fjárhags:  

-   Bókun leyfð frá = 1. janúar 2014  

-   Bókun leyfð til = tómt  

 Notandauppsetning:  

-   Bókun leyfð frá = 1. desember 2013.  

-   Bókun leyfð til = tómt  

##### <a name="to-test-the-scenario"></a>Að prófa aðstæðurnar  

1.  Stofna TEST vöru:  

     Grunnmælieining = STK  

     Kostnaðarútreikningur = Meðaltal  

     Velja valkvæða bókunarflokka.  

2.  Opna birgðabók, stofna og bóka línu á eftirfarandi hátt:  

     Bókunardagsetning = 15. desember, 2013  

     Vara = TEST  

     Tegund færslu = Innkaup  

     Magn = 100  

     Ein.upphæð = 10  

3.  Opna birgðabók, stofna og bóka línu á eftirfarandi hátt:  

     Dagsetning = 20. desember 2013  

     Vara = TEST  

     Tegund færslu = Neikvæð leiðrétting  

     Magn = 2  

4.  Opna birgðabók, stofna og bóka línu á eftirfarandi hátt:  

     Dagsetning = 15. janúar 2014  

     Vara = TEST  

     Tegund færslu = Neikvæð leiðrétting  

     Magn = 3  

5.  Opna endurmatsbók, stofna og bóka línu á eftirfarandi hátt:  

     Vara = TEST  

     Gildir-fyrir færslu = veldu innkaupafærsla bókuð í skrefi 2. Bókunardagsetning endurmats verður sú sama og fyrir færsluna sem hún leiðréttir.  

     Kostnaðarverð endurmetið = 40  

 Eftirfarandi birgðahöfuðbók og virðisfærslur hafa verið bókaðar:  

![Yfirlit yfir birgðahöfuðbók og virðisfærslur sem urðu til 1](media/helene/TechArticleAdjustcost9.png "Yfirlit yfir birgðahöfuðbók og virðisfærslur sem urðu til 1")

 ![Yfirlit yfir birgðahöfuðbók og virðisfærslur sem urðu til 2](media/helene/TechArticleAdjustcost10.png "Yfirlit yfir birgðahöfuðbók og virðisfærslur sem urðu til 2")

 Runuvinnslan Leiðréttur kostnaður - Birgðafærslur hefur borið kennsl á breytingar á kostnaði og leiðrétti neikvæðu leiðréttingarnar.  

 **Endurskoðun bókunardagsetninga á stofnuðum leiðréttingarvirðisfærslum:** Fyrstu leyfilegu bókunardagsetningar sem runuvinnslan Leiðréttur kostnaður - Birgðafærslur verður að tengjast er 1. janúar 2014 eins kemur fram í fjárhagsgrunni.  

 **Neikvæð leiðrétting í skrefi 3:** úthlutuð bókunardagsetning er 1. janúar, veitt af fjárhagsgrunni. Bókunardagsetning virðisfærslunnar sem heyrir undir leiðréttingu er 20. desember 2013. Samkvæmt fjárhagsgrunni er dagsetningin ekki innan leyfilegs dagsetningabils bókunar. Þess vegna er bókunardagsetningunni, sem er nefnd í Bókun leyfð frá reit fjárhagsgrunns, úthlutað á leiðrétttingarvirðisfærsluna.  

 **Neikvæð leiðrétting í skrefi 4:** úthlutuð bókunardagsetning er 15. janúar. Virðisfærslan sem heyrir undir leiðréttingu er með bókunardagsetninguna 15. janúar, sem er innan leyfilegs dagsetningabils bókunar samkvæmt fjárhagsgrunni.  

 Leiðréttingin sem gerð var fyrir neikvæðu leiðréttinguna í skrefi 3 veldur umræðu. Hagstæða bókunardagsetningin fyrir leiðréttingarvirðisfærsluna hefði verið 20. desember eða að minnsta kosti í desember þar sem endurmatið sem olli breytingunni á kostnaði seldrar vöru var bókað í desember.  

 Til að ná leiðréttingu í desember á neikvæðu leiðréttingunni í 3. skrefi þarf fjárhagsgrunnurinn, Bókun leyfð frá reit, að tilgreina dagsetningu í desember.  

 **Niðurstaða:**  

 Með reynslu af þessari atburðarás, miðað við hentugastu uppsetningu leyfilegs dagsetningabils bókunar fyrir fyrirtæki, gæti eftirfarandi verið gagnlegt: Svo lengi sem er heimilt að bóka breytingar á birgðaverðmæti á tímabili, desember í þessu tilviki, ætti uppsetningin sem fyrirtækið notar fyrir dagsetningabil sem er leyfilegt að bóka að vera í takt við þessa ákvörðun. Bókun leyfð frá í fjárhagsgrunni, þar sem fram kemur 1. desember, myndi leyfa að áframsenda endurmatið sem gert var í desember á færslur á útleið, sem verða fyrir áhrifum, á sama tímabilinu.  

 Notendahópar sem ekki mega bóka í desember en í janúar, sem fjárhagsgrunnur átti líklega að takmarka í þessum aðstæðum, ætti frekar að staðsetja í notandauppsetningu.  

### <a name="item-charge-scenario"></a>Aðstæður kostnaðarauka:  
 Skilyrði:  

 Birgðagrunnur:  

-   Sjálfvirk kostnaðarbókun = Já  

-   Sjálfvirk kostnaðarleiðrétting=Alltaf  

-   Meðalkostnaður Teg. útreikn=vara  

-   Meðalkostnaðartímabil=Dagur  

 Uppsetning fjárhags:  

-   Bókun leyfð frá = 1. desember 2013.  

-   Bókun leyfð til = tómt  

 Notandauppsetning:  

-   Bókun leyfð frá = 1. desember 2013.  

-   Bókun leyfð til = tómt  

##### <a name="to-test-the-scenario"></a>Að prófa aðstæðurnar  

1.  Stofna kostnaðarauka:  

     Grunnmælieining = STK  

     Kostnaðarútreikningur = Meðaltal  

     Velja valkvæða bókunarflokka.  

2.  Stofna nýja innkaupapöntun  

     Kaupa af lánardrottni nr.: 10000  

     Bókunardagsetning = 15. desember, 2013  

     Reikningsnr. lánardrottins: 1234  

     Á innkaupapöntunarlínunni:  

     Vara = GJALD  

     Magn = 1  

     Innkaupsverð = 100  

     Bóka móttaka og reikningsfæra.  

3.  Stofna nýja sölupöntun:  

     Selt til Viðskiptamaður Nr.: 10000  

     Bókunardagsetning = 16. desember 2013  

     Í sölupöntunarlínu:  

     Vara = GJALD  

     Magn = 1  

     Einingarverð = 135  

     Bóka afhenda og reikningsfæra.  

4.  Uppsetning fjárhags:  

     Bókun leyfð frá = 1. janúar 2014  

     Bókun leyfð til = autt  

5.  Stofna nýja innkaupapöntun:  

     Kaupa af lánardrottni nr.: 10000  

     Bókunardagsetning = 2. janúar 2014  

     Reikningsnr. lánardrottins: 2345  

     Á innkaupapöntunarlínunni:  

     Kostnaðarauki = JB-FLUTN  

     Magn = 1  

     Innkaupsverð = 3  

     Úthluta kostnaðarauka á innkaupamóttöku úr skrefi 2.  

     Bóka kvittun og reikningsfæra.  

     ![Yfirlit yfir birgðahöfuðbók og virðisfærslur sem urðu til 3](media/helene/TechArticleAdjustcost11.png "Yfirlit yfir birgðahöfuðbók og virðisfærslur sem urðu til 3")

6.  Á vinnudaginn 3. janúar kemur innkaupareikningur sem inniheldur viðbótargjald við kaupin sem voru gerð í skrefi 2. Þessi reikningur hefur dagsetningu skjals 30. desember og er því bókaður með bókunardagsetningunni 30. desember 2013.  

     Stofna nýja innkaupapöntun:  

     Kaupa af lánardrottni nr.: 10000  

     Bókunardagsetning = 30. desember 2013  

     Reikningsnr. lánardrottins: 3456  

     Á innkaupapöntunarlínunni:  

     Kostnaðarauki = JB-FLUTN  

     Magn = 1  

     Innkaupsverð = 2  

     Úthluta kostnaðarauka á innkaupamóttöku úr skrefi 2  

     Bóka kvittun og reikningsfæra.  

   ![Yfirlit yfir birgðahöfuðbók og virðisfærslur sem urðu til 4](media/helene/TechArticleAdjustcost12.png "Yfirlit yfir birgðahöfuðbók og virðisfærslur sem urðu til 4")

 Skýrsla birgðavirðis er prentuð frá og með dagsetningunni 31. desember 2013  

![Innihald birgðavirðisskýrslu](media/helene/TechArticleAdjustcost13.png "Innihald birgðavirðisskýrslu")

 **Samantekt á aðstæðum:**  

 Útlistaðar aðstæður enda með verðmætamati á birgðum sem sýnir magn = 0 á meðan gildið = 2. Bókaður kostnaðarauki í skrefi 11 er hluti af birgðaaukningunni í desember á meðan birgðaminnkun sama tímabils verður ekki fyrir áhrifum.  

 Að fjárhagsgrunnurinn skyldi gefa upp Leyfa bókun frá og með 1. janúar var gott fyrir fyrsta kostnaðaraukann. Kostnaður við birgðaaukningu og -minnkun var skráð á sama tímabilið. Fyrir seinni kostnaðaraukann er það hins vegar fjárhagsgrunnurinn sem veldur því að breytingin á kostnaði seldrar vöru verði samþykktur fyrir næsta tímabil.  

 **Niðurstaða:**  

 Það er áskorun að hafa skýrslu birgðavirðis til að sýna magn = 0 á meðan gildið <> 0. Í þessu tilfelli er það líka erfiðara að tjá ákjósanlegustu stillingar með því að hafa innkaupareikninga sem koma á sama degi en taka til mismunandi tímabila eða jafnvel reikningsára. Að færast yfir á nýtt reikningsár krefst yfirleitt einhverrar skipulagningar og sem hluti af því þarf að íhuga nánar ferli leiðréttingarkostnaðar - birgðafærslna, gera sér grein fyrir kostnaði seldra vara.  

 Í þessari atburðarás getur einn möguleiki verið að hafa fjárhagsgrunninn, reitinn Bókun leyfð frá, gefa upp dagsetningu í desember fyrir nokkra daga í viðbót og fresta bókun á fyrsta kostnaðaraukanum svo allir kostnaðir fyrir fyrra tímabil/fjárhagsár verði viðurkenndir fyrir tímabilið sem þeir tilheyra í fyrstu, keyra síðan runuvinnslu Leiðrétts kostnaðar - Birgðafærslna og í kjölfarið færa leyfða bókunardagsetningu yfir á nýtt tímabil\/fjárhagsársins. Fyrsti kostnaðaraukinn með bókunardagsetninguna 2. janúar getur þá verið bókaður.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Ferill runuvinnslu Leiðrétts kostnaðar – birgðafærslna  
 Hér fyrir neðan er samantekt á hugmyndinni um að úthluta bókunardagsetningum á leiðrétttingarvirðisfærslum með runuvinnslu leiðrétts kostnaðar - birgðafærslna síðan í útgáfu 3.0.  

### <a name="from-version-30370a"></a>Frá útgáfu 3.0..3.70.A  
 Í beiðniglugga fyrir runuvinnslu leiðrétts kostnaðar - birgðafærslna þarf notandi að færa inn bókunardagsetningu. Runuvinnslan fer í gegnum allar nauðsynlegar breytingar og stofnar virðisfærslur með bókunardagsetningunni sem hefur verið færð inn í beiðnigluggann. Ráðlögð bókunardagsetning er dagurinn í dag.  

### <a name="version-370b40"></a>Útgáfa 3.70.B..4.0  
 Í beiðniglugga fyrir runuvinnslu leiðrétts kostnaðar - birgðafærslna þarf notandi að færa inn bókunardagsetningu lokaðrar tímabilsfærslu. Runuvinnslan fer í gegnum nauðsynlegar breytingar og stofnar virðisfærslur með bókunardagsetningu á yfirbirgðafærslunni (afhendingardagur sölunnar sem leiðréttingin gefur upp). Ef bókunardagsetning yfirbirgðafærslunnar er ekki innan leyfilegs dagsetningabils bókunar verður bókunardagsetningu lokaðrar tímabilsfærslu úthlutað leiðréttingarvirðisfærslu. Dagsetning telst vera á lokuðu tímabili þegar hún er eldri en dagsetningin í reitnum Bókun leyfð frá í fjárhagsgrunni.  

### <a name="from-version-50"></a>Frá útgáfu 5,0:  
 Ekki þarf lengur að gefa upp bókunardagsetningu í beiðniglugga fyrir runuvinnslu leiðrétts kostnaðar - birgðafærslna. Runuvinnslan fer í gegnum allar nauðsynlegar breytingar og stofnar virðisfærslur með bókunardagsetningu virðisfærslunnar sem hún leiðréttir. Ef bókunardagsetningin er ekki innan leyfilegs dagsetningabils bókunar verður bókunardagsetningin í reitnum Bókun leyfð frá í fjárhagsgrunni notuð, EÐA ef birgðatímabil eru notuð, verður eldri dagsetningin af þessum tveimur notuð. Sjá útskýrt hugtak hér að ofan.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Ferill runuvinnslunnar Bóka birgðabreytingar  
 Runuvinnslan Bóka birgðabreytingar er nátengd runuvinnslunni Leiðrétta kostnað - Birgðafærslur og því er ferill runuvinnslunnar að auki tekin saman og deilt hér.  

### <a name="from-version-30370a"></a>Frá útgáfu 3.0..3.70.A  
 Í beiðniglugga fyrir birgðabreytingar þarf notandi að færa inn bókunardagsetningu. Runuvinnslan keyrir í gegnum allar virðisfærslur innan síunnar, ef það er einhver, og stofnar fjárhagsfærslur þar sem bókunardagsetning er færð inn í beiðnigluggann.  

### <a name="version-370b40"></a>Útgáfa 3.70.B..4.0  
 Í beiðniglugga birgðabreytinga er reiturinn bókunardagsetning lokaðrar tímabilsfærslu tiltækur. Forritið notar dagsetninguna sem þú slærð inn í þennan reit sem bókunardagsetningu fyrir fjárhagsfærslurnar sem það stofnar fyrir virðisfærslur, en bókunardagsetningar þeirra eru á lokuðu reikningstímabili. Að öðrum kosti munu fjárhagsfærslurnar hafa sömu bókunardagsetningu og upprunalegu virðisfærslurnar. Dagsetning telst vera á lokuðu tímabili þegar hún er eldri en dagsetningin í reitnum Bókun leyfð frá í fjárhagsgrunni. Ef fjár\/hagur er bókaður fyrir hvern bókunarflokk munu fjárhagsfærslurnar fá bókunardagsetninguna sem er tilgreind í reit bókunardagsetningar í beiðniglugganum.  

 Í útgáfum 3 og 4 skannar runuvinnslan allar virðisfærslur til að greina hvort einhverjar virðisfærslur séu til þar sem kostnaðarupphæð (raunveruleg) er frábrugðin kostnaði bókuðum í fjárhag. Ef finnst mismunur verður frábrugðna upphæðin bókuð í fjárhagsfærslu. Ef bókun áætlaðs kostnaðar er notaður er unnið úr samsvarandi reitum á sama hátt.  

![Raunverulegur kostnaður á móti áætluðum kostnaði](media/helene/TechArticleAdjustcost14.png "Raunverulegur kostnaður á móti áætluðum kostnaði")

### <a name="from-version-50"></a>Frá útgáfu 5,0:  
 Ekki þarf lengur að tilgreina bókunardagsetningu í beiðniglugganum fyrir runuvinnslu birgðabreytinga. Fjárhagsfærslan er búin til með sömu bókunardagsetningu og tengd virðisfærsla. Til þess að ljúka runuvinnslunni verður leyfilegt dagsetningabil bókunar að leyfa bókunardagsetningu stofnuðu fjárhagsfærslunnar. Ef ekki, verður að enduropna tímabundið leyfilegt dagsetningabil bókunar með því að breyta eða fjarlægja dagsetningarnar í reitunum Bókun leyfð frá og til í fjárhagsgrunni. Til að koma í veg fyrir afstemmingarvandamál er nauðsynlegt að bókunardagsetning fjárhagsfærslu samsvari bókunardagsetningu virðisfærslu.  

 Runuvinnslan skannar tafla 5811 - Bóka virðisfærslu í fjárhag, til að bera kennsl á virðisfærslur sem heyra undir bókun í fjárhag. Taflan var tæmd eftir heppnaða keyrslu.

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Hönnunarupplýsingar: Umsókn vöru](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]