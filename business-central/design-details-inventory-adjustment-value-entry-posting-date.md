---
title: Bókunardagsetning á virðisfærslum
description: Lærðu hvernig runuvinnslan Leiðréttur kostnaður - birgðafærslur ber kennsl á og úthlutar bókunardagsetningu fyrir virðisfærslurnar sem runuvinnslan er að búa til.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/19/2021
ms.author: edupont
ms.openlocfilehash: 3dcda7f44797f52e50babe4dbec90e3b2be6f19d
ms.sourcegitcommit: e891484daad25f41c37b269f7ff0b97df9e6dbb0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/27/2021
ms.locfileid: "7440739"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Hönnunarupplýsingar: Bókunardagsetning á leiðréttingarvirðisfærslu  

Þessi grein veitir leiðbeiningar fyrir notendur birgðakostnaðarvirkni í [!INCLUDE[prod_short](includes/prod_short.md)]. Tilgreind grein veitir leiðbeiningar um hvernig runuvinnslan **Leiðréttur kostnaður - Birgðafærslur** ber kennsl á og úthlutar bókunardagsetningu fyrir virðisfærslurnar sem runuvinnslan er að búa til.  

Fyrst er hugmynd ferlisins yfirfarin, hvernig runuvinnslan ber kennsl á og úthlutar bókunardagsetningu fyrir virðisfærsluna sem verður búin til. Eftir það eru nokkrar aðstæður sem við í stuðningshópnum rekumst á af og til og að lokum er samantekt yfir hugtökin sem eru notuð.  

## <a name="the-concept"></a>Hugtakið  

Runuvinnslan **Leiðrétta kostnað - Birgðafærslur** úthlutar bókunardagsetningu fyrir virðisfærsluna sem hún kemur til með að búa til í eftirfarandi skrefum:  

1.  Upphaflega er bókunardagsetning færslunnar sem á að búa til sú sama og dagsetning færslunnar sem hún leiðréttir.  

2.  Bókunardagsetningin er sannprófuð gagnvart birgðatímabili og/eða fjárhagsgrunni.  

3.  Úthlutun bókunardagsetningu; Ef upphafleg bókunardagsetning er ekki innan leyfilegs dagsetningabils bókunar, þá mun runuvinnslan úthluta leyfilegri bókunardagsetningu frá annað hvort fjárhagsgrunni eða birgðatímabili. Ef bæði birgðatímabil og leyfileg bókunardagsetning í fjárhagsgrunni eru skilgreind, verður síðari dagsetning þessara tveggja úthlutað til leiðréttingarvirðisfærslu.  

 Við skulum yfirfara þetta ferli betur með dæmi. Gerum ráð fyrir að við séum með birgðafærslu fyrir sölu. Þessi hlutur var sendur 5. september 2020 og reikningsfærður daginn eftir.  


**Birgðafærsla**  
Dagsetningarsnið ÁÁÁÁ-MM-DD

|Færslunr.  |Vörunr.  |Bókunardagsetning  |Tegund færslu  | Nr. fylgiskjals |Kóti birgðageymslu   |Magn  |Kostnaðarupphæð (raunverul.)  |Reikningsfært magn  |Eftirstöðvar (magn)  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Sala       |102033     |  Blátt       | -1    |    -11     |-1     |    0     |

Hér að neðan táknar fyrsta virðisfærslan (379) sendinguna og bera þær sömu bókunardagsetningu og yfirbirgðafærslan.  
  
Önnur virðisfærslan (381) táknar reikninginn.  

Þriðja virðisfærslan (391) er leiðrétting á virði reikningsfærslu (381).  
  

|Færslunr.  |Vörunr.  |Bókunardagsetning  |Birgðafærslutegund  |Tegund færslu  |Nr. fylgiskjals  |Birgðafærsla nr.  |Kóti birgðageymslu   |Magn birgðafærslu  |Reikningsfært magn  |Kostnaðarupphæð (raunverul.)  |Kostnaðarupphæð (væntanl.)  |LEIÐRÉTT  |Jafna færslu  |Upprunakóði  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Sala     | Beinn kostnaður   | 102033        |319     | Blátt        | -1       |0         |  0       |     -10   |Nr   |0    |Sölur          |
|381     |  A       |    2020-09-06     |    Sala     | Beinn kostnaður   | 103022        |319     | Blátt        |  0       |-1        |-10       |    10     | Nr  |0      |       Sölur   |
|391     |  A       |    2020-09-10     |    Sala     | Beinn kostnaður   | 103022        |319     | Blátt        |  0       |0         |-1        |    0     |Já   |    181   | BIRGLEIÐR   |

Bókunardagsetning leiðréttingarfærslu er upphaflega stillt á sömu bókunardagsetningu og færsluna sem hún leiðréttir.

 Skref 1: Leiðréttingarvirðisfærsla sem á að búa til er úthlutað sömu bókunardagsetningu og færslan sem hún leiðréttir, sýnt hér að framan með virðisfærslu 391.  
  
 Skref 2: Villuleit á upphaflega úthlutaðri bókunardagsetningu.  

Runuvinnslan **Leiðrétta kostnað - Birgðafærslur** ákvarðar hvort upphafleg bókunardagsetning fyrir leiðréttingarvirðisfærslu er innan leyfilegs dagsetningabils bókunar byggt á birgðatímabili og/eða fjárhagsgrunni.  

Við skulum endurskoða ofangreinda sölu með því að bæta við uppsetningu á leyfilegu dagsetningabili bókunar.  
  
**Birgðatímabil**

|Lokadagsetning  |Name  |Lokað  |
|---------|---------|---------|
|2020-01-31     |2020. janúar      |  Já    |
|2020-02-28     |2020. febrúar     |  Já    |
|2020-03-31     |Mars 2020        |  Já    |
|2020-04-30     |Apríl 2020        |  Já    |
|2020-05-31     |Maí 2020        |  Já    |
|2020-06-30     |Júní 2020       |  Já    |
|2020-07-31     |Júlí 2020        |   Já   |
|2020-08-31     |Ágúst 2020     |   Já   |
|2020-09-30     |September 2020  |         |
|2020-10-31     |Október 2020    |         |
|2020-11-30     |Nóvember 2020   |         |
|2020-12-31     |Desember 2020   |         |

Fyrsta leyfilega bókunardagsetning er fyrsta daginn í fyrsta opna tímabilinu. 1. september 2020.  

**Fjárhagsgrunnur**

|Svæði|Gildi:  |
|---------|---------|
|Bókun leyfð frá:  |  2020-09-10      |
|Bókun leyfð til:    |  2020-09-30      |
|Skrá tíma:       |         |
|Snið staðbundins aðseturs:|   Póstnúmer      |  

 Fyrsta leyfilega bókunardagsetning er dagsetningin sem tilgreind er í reitnum Leyfa bókanir frá: 10. september 2020.  
 Ef bæði birgðatímabil og leyfilegar bókunardagsetningar í fjárhagsgrunni eru skilgreind mun síðari dagsetning þessara tveggja skilgreina leyfilegt dagsetningabil bókunar.  

 Skref 3: Úthlutun á leyfilegri bókunardagsetningu;  

 Upphaflega úthlutaða bókunardagsetningin var 6. september eins og sýnt er í skrefi 1. Í öðru skrefi ber runuvinnslan Leiðrétta kostnað - Birgðafærslur kennsl 10. september sem fyrstu leyfilegu bókunardagsetninguna og úthlutar þess vegna 10. september á leiðréttingarvirðisfærsluna fyrir neðan.  

   
|Færslunr.  |Vörunr.  |Bókunardagsetning  |Birgðafærslutegund  |Tegund færslu  |Nr. fylgiskjals  |Birgðafærsla nr.  |Kóti birgðageymslu   |Magn birgðafærslu  |Reikningsfært magn  |Kostnaðarupphæð (raunverul.)  |Kostnaðarupphæð (væntanl.)  |LEIÐRÉTT  |Jafna færslu  |Upprunakóði  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Sala     | Beinn kostnaður   | 102033        |319     | Blátt        | -1       |0         |  0       |     -10   |Nr   |0    |Sölur          |
|381     |  A       |    2020-09-06     |    Sala     | Beinn kostnaður   | 103022        |319     | Blátt        |  0       |-1        |-10       |    10     | Nr  |0      |       Sölur   |
|391     |  A       |    **10-09-2020**     |    Sala     | Beinn kostnaður   | 103022        |319     | Blátt        |  0       |0         |-1        |    0     |Já   |    181   | BIRGLEIÐR   |

 Við höfum nú yfirfarið hugtakið fyrir úthlutun bókunardagsetninga á virðisfærslur sem eru búnar til af runuvinnslu Leiðrétts kostnaðar - Birgðafærslna.  

 Við skulum halda áfram að yfirfara sumar aðstæður sem við í stuðningshópnum rekumst á af og til í tengslum við úthlutaðar bókunardagsetningar í runuvinnslu Leiðrétts kostnaðar - Birgðafærslna og tengdum uppsetningum.  

## <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Aðstæður I: „Bókunardagsetning er ekki innan marka leyfilegra bókunardagsetninga...“  

 Þetta eru aðstæður þar sem notandi fær upp umrædd villuboð þegar runuvinnsla Leiðrétts kostnaðar - Birgðafærsla er keyrð.  

 Í fyrri kafla, sem lýsir hugmyndinni um að gefa út bókunardagsetningar, er ætlunin með runuvinnslu Leiðrétts kostnaðar - Birgðafærslna að búa til virðisfærslu með bókunardagsetninguna 10. september.  

![Villuboð um bókunardagsetningu.](media/helene/TechArticleAdjustcost6.png "Villuboð um bókunardagsetningu")

 Við fylgjum eftir notandauppsetningu:  

**Notandaupplýsingar**  

Röðun: Notandakenni  

|Notandakenni  |Bókun leyfð frá  | Bókun leyfð til  |
|---------|---------|--------|
|Í EVRÓPU  |  2020-09-11      |2020-09-30      |

 Notandinn í þessu tilfelli hefur leyfilegt dagsetningabil bókunar frá 11. september til 30. september og er því ekki heimilt að bóka leiðréttingarvirðisfærsluna með bókunardagsetninguna 10. september.  

### <a name="overview-of-involved-posting-date-setup"></a>Yfirlit yfir virka uppsetningu bókunardagsetningar:

**Birgðatímabil**  

|Lokadagsetning  |Name  |Lokað  |
|---------|---------|---------|
|2020-01-31     |2020. janúar      |  Já    |
|2020-02-28     |2020. febrúar     |  Já    |
|2020-03-31     |Mars 2020        |  Já    |
|2020-04-30     |Apríl 2020        |  Já    |
|2020-05-31     |Maí 2020        |  Já    |
|2020-06-30     |Júní 2020       |  Já    |
|2020-07-31     |Júlí 2020        |   Já   |
|2020-08-31     |Ágúst 2020     |   Já   |
|2020-09-30     |September 2020  |         |
|2020-10-31     |Október 2020    |         |
|2020-11-30     |Nóvember 2020   |         |
|2020-12-31     |Desember 2020   |         |  

**Fjárhagsgrunnur**  

|Svæði|Gildi:|
|---------|---------|
|Bókun leyfð frá:  |  2020-09-10      |
|Bókun leyfð til:    |  2020-09-30      |
|Skrá tíma:       |         |
|Snið staðbundins aðseturs:|   Póstnúmer      |  

**Notandaupplýsingar**    

|Notandakenni  |Bókun leyfð frá  | Bókun leyfð til  |
|---------|---------|--------|
|NOTANDANAFN |  2020-09-10      |2020-09-30      |

 Með því að úthluta notandanum víðtækara (eða sama) leyfilegu dagsetningabili bókunar eins og í birgðatímabili eða almennri uppsetningu fjárhags verður komið í veg fyrir áðurnefndan árekstur. Færsla leiðréttingargildis með bókunardagsetningu 10. september verður bókuð með þessari uppsetningu.

Eldri grein þekkingargrunns [952996](https://support.microsoft.com/topic/information-about-inventory-adjustment-posting-dates-in-microsoft-dynamics-nav-99e22b2b-5b79-a9b2-3b43-7f3484fa31d9) fjallar um fleiri aðstæður sem tengjast nefndu villuboði.  

## <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Aðstæður II: Bókunardagsetning á leiðréttingarvirðisfærslum á móti bókunardagsetningu við innfærslu sem veldur leiðréttingu, eins og endurmati eða kostnaðarauka.  

### <a name="revaluation-scenario"></a>Aðstæður endurmats:  

 Skilyrði:  

 Birgðagrunnur:  
ég
-   Sjálfvirk kostnaðarbókun = Já  

-   Sjálfvirk kostnaðarleiðrétting = Alltaf  

-   Tegund meðalinnk.verðs = vara  

-   Meðalkostnaðartímabil = Dagur  

 Uppsetning fjárhags:  

-   Leyfa bókanir frá = 1. janúar 2021  

-   Bókun leyfð til = tómt  

 Notandauppsetning:  

-   Leyfa bókanir frá = 1. desember 2020  

-   Bókun leyfð til = tómt  

### <a name="to-test-the-scenario"></a>Að prófa aðstæðurnar  

1.  Stofna TEST vöru:  

     Grunnmælieining = STK  

     Kostnaðarútreikningur = Meðaltal  

     Velja valkvæða bókunarflokka.  

2.  Opna birgðabók, stofna og bóka línu á eftirfarandi hátt:  

     Bókunardagur = 15. desember 2020  

     Vara = TEST  

     Tegund færslu = Innkaup  

     Magn = 100  

     Ein.upphæð = 10  

3.  Opna birgðabók, stofna og bóka línu á eftirfarandi hátt:  

     Dagsetning = 20. desember 2020  

     Vara = TEST  

     Færslugerð = Neikvæð leiðrétting  

     Magn = 2  

4.  Opna birgðabók, stofna og bóka línu á eftirfarandi hátt:  

     Dagsetning = 15. janúar 2021  

     Vara = TEST  

     Færslugerð = Neikvæð leiðrétting  

     Magn = 3  

5.  Opna endurmatsbók, stofna og bóka línu á eftirfarandi hátt:  

     Vara = TEST  

     Gildir-fyrir færslu = veldu innkaupafærsla bókuð í skrefi 2. Bókunardagsetning endurmats verður sú sama og fyrir færsluna sem hún leiðréttir.  

     Kostnaðarverð endurmetið = 40  

Eftirfarandi **Birgðahöfuðbók** og **Virðisfærslur** hafa verið bókaðar:  

**Birgðabókafærsla - innkaup**:  
Dagsetningarsnið ÁÁÁÁ-MM-DD  

|Færslunúmer  |Vörunr.  |Bókunardagsetning  |Tegund færslu  |Nr. fylgiskjals  |Magn  |Kostnaðarupphæð (raunverul.)  |Eftirstöðvar (magn)  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|317     |PRÓFUN         |2020-12-15         |Innkaup         |T00001         |100%         |4000         |95        |

**Virðisfærslur**  

|Færslunúmer  |Vörunr.  |Bókunardagsetning  |Birgðafærsla nr.  |Birgðafærslutegund  |Tegund færslu  |Nr. fylgiskjals  |Magn vörunúmersfærslu  |Kostnaðarupphæð (raunverul.)  |Kostnaður bókaður í fjárhag  |LEIÐRÉTT  |Á við um færslu  |Upprunakóði  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|376     |PRÓFUN|   2020-12-15    |317         |Innkaup         |Beinn kostnaður         |T00001         |100%         |1000,00          |1000,00    |Nr         |0         |ITEMNL         |
|379     |PRÓFUN   |**15-12-2020**    |317         |Innkaup         |Endurmat         |T04002         |0         |3000,00         |3000,00         |Nr         |0         |REVALINL         |

**Birgðabókafærsla - neikvæð leiðrétting, skref 3**  

|Færslunr.  |Vörunr.  |Bókunardagsetning  |Tegund færslu  |Nr. fylgiskjals  |Magn  |Kostnaðarupphæð (raunverul.)  |Eftirstöðvar (magn)  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|318     |PRÓFUN      |2020-12-20   |Minnkun  |T00002         |-2         |-80         | 0        |

**Virðisfærslur**  

|Færslunúmer  |Vörunr.  |Bókunardagsetning  |Birgðafærsla nr.  |Birgðafærslutegund  |Tegund færslu  |Nr. fylgiskjals  |Magn vörunúmersfærslu  |Kostnaðarupphæð (raunverul.)  |Kostnaður bókaður í fjárhag  |LEIÐRÉTT  |Á við um færslu  |Upprunakóði  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|377     |PRÓFUN|   2020-12-20    |318         |Minnkun         |Beinn kostnaður         |T00002         |-2         |-20          |-20    |Nr         |0         |ITEMNL         |
|380     |PRÓFUN   |**01-01-2021**    |318         |Minnkun         |Beinn kostnaður         |T04002         |0         |-60         |-60         |Já         |377         |INVTADAMT         |

**Birgðabókafærsla - neikvæð leiðrétting, skref 4**  

|Færslunr.  |Vörunr.  |Bókunardagsetning  |Tegund færslu  |Nr. fylgiskjals  |Magn  |Kostnaðarupphæð (raunverul.)  |Eftirstöðvar (magn)  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |PRÓFUN      |2021-01-15   |Minnkun  |T00003         |-3         |-120         | 0        |

**Virðisfærslur**  

|Færslunúmer  |Vörunr.  |Bókunardagsetning  |Birgðafærsla nr.  |Birgðafærslutegund  |Tegund færslu  |Nr. fylgiskjals  |Magn vörunúmersfærslu  |Kostnaðarupphæð (raunverul.)  |Kostnaður bókaður í fjárhag  |LEIÐRÉTT  |Á við um færslu  |Upprunakóði  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|378     |PRÓFUN|   2021-01-15    |319         |Minnkun         |Beinn kostnaður         |T00003         |-3         |-30          |-30    |Nr         |0         |ITEMNL         |
|381     |PRÓFUN   |**01-15-2021**    |319         |Minnkun         |Beinn kostnaður         |T04003         |0         |-90         |-90         |Já         |378         |INVTADAMT         |

Runuvinnslan Leiðréttur kostnaður - Birgðafærslur hefur borið kennsl á breytingar á kostnaði og leiðrétti neikvæðu leiðréttingarnar.  

**Endurskoðun bókunardagsetninga á stofnuðum leiðréttingarvirðisfærslum:** Fyrstu leyfilegu bókunardagsetningar sem runuvinnslan Leiðréttur kostnaður - Birgðafærslur verður að tengjast er 1. janúar 2021 eins kemur fram í fjárhagsgrunni.  

**Neikvæð leiðrétting í skrefi 3:** úthlutuð bókunardagsetning er 1. janúar, veitt af fjárhagsgrunni. Bókunardagsetning virðisfærslunnar sem heyrir undir leiðréttingu er 20. desember 2020. Samkvæmt fjárhagsgrunni er dagsetningin ekki innan leyfilegs dagsetningabils bókunar. Þess vegna er bókunardagsetningunni, sem er nefnd í Bókun leyfð frá reit fjárhagsgrunns, úthlutað á leiðrétttingarvirðisfærsluna.  

**Neikvæð leiðrétting í skrefi 4:** úthlutuð bókunardagsetning er 15. janúar. Virðisfærslan sem heyrir undir leiðréttingu er með bókunardagsetninguna 15. janúar, sem er innan leyfilegs dagsetningabils bókunar samkvæmt fjárhagsgrunni.  

Leiðréttingin sem gerð var fyrir neikvæðu leiðréttinguna í skrefi 3 veldur umræðu. Hagstæða bókunardagsetningin fyrir leiðréttingarvirðisfærsluna hefði verið 20. desember eða að minnsta kosti í desember þar sem endurmatið sem olli breytingunni á kostnaði seldrar vöru var bókað í desember.  

Til að ná leiðréttingu í desember á neikvæðu leiðréttingunni í 3. skrefi þarf fjárhagsgrunnurinn, Bókun leyfð frá reit, að tilgreina dagsetningu í desember.  

**Niðurstaða:**  

Með reynslu af þessari atburðarás, miðað við hentugastu uppsetningu leyfilegs dagsetningabils bókunar fyrir fyrirtæki, gætirðu viljað íhuga eftirfarandi upplýsingar: Svo lengi sem þú heimilar bókun breytinga á birgðaverðmæti á tímabili, desember í þessu tilviki, ætti uppsetningin sem fyrirtækið notar fyrir dagsetningabil sem er leyfilegt að bóka að vera í takt við þessa ákvörðun. Bókun leyfð frá í fjárhagsgrunni, þar sem fram kemur 1. desember, myndi leyfa að áframsenda endurmatið sem gert var í desember á færslur á útleið, sem verða fyrir áhrifum, á sama tímabilinu.  

Notendahópar sem ekki mega bóka í desember en í janúar, sem fjárhagsgrunnur átti líklega að takmarka í þessum aðstæðum, ætti frekar að staðsetja í notandauppsetningu.  

### <a name="item-charge-scenario"></a>Aðstæður kostnaðarauka:  

 Skilyrði:  

 Birgðagrunnur:  

-   Sjálfvirk kostnaðarbókun = Já  

-   Sjálfvirk kostnaðarleiðrétting = Alltaf  

-   Tegund meðalinnk.verðs = vara  

-   Meðalkostnaðartímabil = Dagur  

 Uppsetning fjárhags:  

-   Leyfa bókanir frá = 1. desember 2020.  

-   Bókun leyfð til = tómt  

 Notandauppsetning:  

-   Leyfa bókanir frá = 1. desember 2020.  

-   Bókun leyfð til = tómt  


### <a name="to-test-the-scenario"></a>Að prófa aðstæðurnar  

1.  Stofna kostnaðarauka:  

     Grunnmælieining = STK  

     Kostnaðarútreikningur = Meðaltal  

     Velja valkvæða bókunarflokka.  

2.  Stofna nýja innkaupapöntun  

     Kaupa af lánardrottni nr.: 10000  

     Bókunardagur = 15. desember 2020

     Reikningsnr. lánardrottins: 1234  

     Á innkaupapöntunarlínunni:  

     Vara = GJALD  

     Magn = 1  

     Innkaupsverð = 100  

     Bóka móttaka og reikningsfæra.  

3.  Stofna nýja sölupöntun:  

     Selt til Viðskiptamaður Nr.: 10000  

     Bókunardagsetning = 16. desember 2020  

     Í sölupöntunarlínu:  

     Vara = GJALD  

     Magn = 1  

     Einingarverð = 135  

     Bóka afhenda og reikningsfæra.  

4.  Uppsetning fjárhags:  

     Leyfa bókanir frá = 1. janúar 2021  

     Bókun leyfð til = autt  

5.  Stofna nýja innkaupapöntun:  

     Kaupa af lánardrottni nr.: 10000  

     Bókunardagur = 2. janúar, 2021  

     Reikningsnr. lánardrottins: 2345  

     Á innkaupapöntunarlínunni:  

     Kostnaðarauki = JB-FLUTN  

     Magn = 1  

     Innkaupsverð = 3  

     Úthluta kostnaðarauka á innkaupamóttöku úr skrefi 2.  

     Bóka kvittun og reikningsfæra.  


**Staða fjárhagsfærslu vöru í innkaupaskrefi 2**:  
  
|Færslunúmer  |Vörunr.  |Bókunardagsetning  |Tegund færslu  |Nr. fylgiskjals  |Magn  |Kostnaðarupphæð (raunverul.)  |Eftirstöðvar (magn)  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |GJALD         |2020-12-15         |Innkaup         |107030         |1         |105         |0        |

**Virðisfærslur**  

|Færslunúmer |Vörunr.  |Bókunardagsetning  |Birgðafærsla nr.  |Birgðafærslutegund  |Tegund færslu  |Nr. fylgiskjals  | Nr. kostnaðarauka vöru    |  Magn birgðafærslu   |Kostnaðarupphæð (raunverul.)     |Kostnaður bókaður í fjárhag |LEIÐRÉTT |Jafna færslu |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |GJALD|   2020-12-15    |324         |Innkaup         |Beinn kostnaður         |108029         |         |1          |100%    |100%         |NEI         |0         |
|399      |GJALD   |2021-01-02    |324         |Innkaup         |Beinn kostnaður         |108009         |JBFREIGHT         |0         |3         |3         |NEI         |0         |


**Staða á sölu birgðafærslu vöru**:  
  
|Færslunr.  |Vörunr.  |Bókunardagsetning  |Tegund færslu  |Nr. fylgiskjals  |Magn  |Kostnaðarupphæð (raunverul.)  |Eftirstöðvar (magn)  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |GJALD         |2020-12-16         |Sala         |102035         |-1         |-105         |0        |

**Virðisfærslur**  

|Færslunúmer |Vörunr.  |Bókunardagsetning  |Birgðafærsla nr.  |Birgðafærslutegund  |Tegund færslu  |Nr. fylgiskjals  | Nr. kostnaðarauka vöru    |  Magn birgðafærslu   |Kostnaðarupphæð (raunverul.)     |Kostnaður bókaður í fjárhag |LEIÐRÉTT |Jafna færslu |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |GJALD|   2020-12-16    |325         |Sala         |Beinn kostnaður         |109024         |         |-1          |-100    |-100         |NEI         |0         |
|400      |GJALD   |2021-01-01    |325         |Sala         |Beinn kostnaður         |109024         |         |0         |-3         |-3         |Já         |398         |


6.  Á vinnudaginn 3. janúar kemur innkaupareikningur sem inniheldur viðbótargjald við kaupin sem voru gerð í skrefi 2. Þessi reikningur hefur dagsetningu skjals 30. desember og er því bókaður með bókunardagsetningunni 30. desember 2020.  

     Stofna nýja innkaupapöntun:  

     Kaupa af lánardrottni nr.: 10000  

     Bókunardagur = 30. desember 2020  

     Reikningsnr. lánardrottins: 3456  

     Á innkaupapöntunarlínunni:  

     Kostnaðarauki = JB-FLUTN  

     Magn = 1  

     Innkaupsverð = 2  

     Úthluta kostnaðarauka á innkaupamóttöku úr skrefi 2  

     Bóka kvittun og reikningsfæra.  


**Staða fjárhagsfærslu vöru í innkaupum**:  

|Færslunúmer  |Vörunr.  |Bókunardagsetning  |Tegund færslu  |Nr. fylgiskjals  |Magn  |Kostnaðarupphæð (raunverul.)  |Eftirstöðvar (magn)  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |GJALD         |2020-12-15         |Innkaup         |107030         |1         |105         |0        |

**Virðisfærslur**  

|Færslunr. |Vörunr.  |Bókunardagsetning  |Birgðafærsla nr.  |Birgðafærslutegund  |Tegund færslu  |Nr. fylgiskjals  | Nr. kostnaðarauka vöru    |  Magn birgðafærslu   |Kostnaðarupphæð (raunverul.)     |Kostnaður bókaður í fjárhag |LEIÐRÉTT |Jafna færslu |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |GJALD   |2020-12-15    |324         |Innkaup         |Beinn kostnaður         |108029         |            |1         |100%    |100%         |Nr         |0         |
|399      |GJALD   |2021-01-02    |324         |Innkaup         |Beinn kostnaður         |108030         |JBFREIGHT   |0         |3         |3         |Nr         |0         |
|401      |GJALD   |**30-12-2020**    |324         |Innkaup         |Beinn kostnaður         |108031         |JBFREIGHT   |0         |2         |2         |Nr         |0         |

**Staða á sölu birgðafærslu vöru**:  
  
|Færslunúmer  |Vörunr.  |Bókunardagsetning  |Tegund færslu  |Nr. fylgiskjals  |Magn  |Kostnaðarupphæð (raunverul.)  |Eftirstöðvar (magn)  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |GJALD         |2020-12-16         |Sala         |102035         |-1         |-105         |0        |

**Virðisfærslur**  

|Færslunr. |Vörunr.  |Bókunardagsetning  |Birgðafærsla nr.  |Birgðafærslutegund  |Tegund færslu  |Nr. fylgiskjals  | Nr. kostnaðarauka vöru    |  Magn birgðafærslu   |Kostnaðarupphæð (raunverul.)     |Kostnaður bókaður í fjárhag |LEIÐRÉTT |Jafna færslu |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |GJALD   |2020-12-16        |325         |Sala         |Beinn kostnaður         |103024         |            |-1         |-100       |-100         |Nr         |0         |
|400      |GJALD   |2021-01-01        |325         |Sala         |Beinn kostnaður         |103024         |            |0          |-3         |-3         |Já         |398         |
|402      |GJALD   |**01-01-2021**    |325         |Sala         |Beinn kostnaður         |103024         |            |0          |-2         |-2         |Já         |398         |

Skýrsla birgðavirðis er prentuð frá og með dagsetningunni 31. desember 2020

![Innihald birgðavirðisskýrslu.](media/helene/TechArticleAdjustcost13.png "Innihald birgðavirðisskýrslu")

 **Samantekt á aðstæðum:**  

 Útlistaðar aðstæður enda með verðmætamati á birgðum sem sýnir magn = 0 á meðan gildið = 2. Bókaður kostnaðarauki í skrefi 11 er hluti af birgðaaukningunni í desember á meðan birgðaminnkun sama tímabils verður ekki fyrir áhrifum.  

 Að fjárhagsgrunnurinn skyldi gefa upp Leyfa bókun frá og með 1. janúar var gott fyrir fyrsta kostnaðaraukann. Kostnaður við birgðaaukningu og -minnkun var skráð á sama tímabilið. Fyrir seinni kostnaðaraukann er það hins vegar fjárhagsgrunnurinn sem veldur því að breytingin á kostnaði seldrar vöru verði samþykktur fyrir næsta tímabil.  

 **Niðurstaða:**  

 Það er áskorun að hafa skýrslu birgðavirðis til að sýna magn = 0 á meðan gildið <> 0. Í þessu tilfelli er það líka erfiðara að tjá ákjósanlegustu stillingar með því að hafa innkaupareikninga sem koma á sama degi en taka til mismunandi tímabila eða jafnvel reikningsára. Að færast yfir á nýtt reikningsár krefst yfirleitt einhverrar skipulagningar og sem hluti af því þarf að íhuga nánar ferli leiðréttingarkostnaðar - birgðafærslna, gera sér grein fyrir kostnaði seldra vara.  

 Í þessari atburðarás getur einn möguleiki verið að hafa fjárhagsgrunninn, reitinn Bókun leyfð frá, gefa upp dagsetningu í desember fyrir nokkra daga í viðbót og fresta bókun á fyrsta kostnaðaraukanum svo allir kostnaðir fyrir fyrra tímabil/fjárhagsár verði viðurkenndir fyrir tímabilið sem þeir tilheyra í fyrstu, keyra síðan runuvinnslu Leiðrétts kostnaðar - Birgðafærslna og í kjölfarið færa leyfða bókunardagsetningu yfir á nýtt tímabil\/fjárhagsársins. Fyrsti kostnaðaraukinn með bókunardagsetninguna 2. janúar getur þá verið bókaður.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Ferill runuvinnslu Leiðrétts kostnaðar – birgðafærslna  

 Hér fyrir neðan er samantekt á hugmyndinni um að úthluta bókunardagsetningum á leiðrétttingarvirðisfærslum með Leiðr. kostnað – Birgðafærslur runuvinnslunni.  

### <a name="about-the-request-form-posting-date"></a>Um bókunardagsetningu beiðnineyðublaðsins:  

 Ekki þarf lengur að gefa upp bókunardagsetningu í beiðniglugga fyrir runuvinnslu leiðrétts kostnaðar - birgðafærslna. Runuvinnslan fer í gegnum allar nauðsynlegar breytingar og stofnar virðisfærslur með bókunardagsetningu virðisfærslunnar sem hún leiðréttir. Ef bókunardagsetningin er ekki innan leyfilegs dagsetningabils bókunar verður bókunardagsetningin í reitnum Bókun leyfð frá í fjárhagsgrunni notuð, EÐA ef birgðatímabil eru notuð, verður eldri dagsetningin af þessum tveimur notuð. Sjá útskýrt hugtak hér að ofan.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Ferill runuvinnslunnar Bóka birgðabreytingar  

 Runuvinnslan Bóka birgðabreytingar er nátengd runuvinnslunni Leiðrétta kostnað - Birgðafærslur og því er ferill runuvinnslunnar að auki tekin saman og deilt hér.  
 
![Raunverulegur kostnaður á móti áætluðum kostnaði.](media/helene/TechArticleAdjustcost14.png "Raunverulegur kostnaður á móti áætluðum kostnaði")

### <a name="about-the-posting-date"></a>Um bókunardagsetninguna  

 Ekki þarf lengur að tilgreina bókunardagsetningu í beiðniglugganum fyrir runuvinnslu birgðabreytinga. Fjárhagsfærslan er búin til með sömu bókunardagsetningu og tengd virðisfærsla. Til þess að ljúka runuvinnslunni verður leyfilegt dagsetningabil bókunar að leyfa bókunardagsetningu stofnuðu fjárhagsfærslunnar. Ef ekki, verður að opna tímabundið leyfilegt dagsetningabil bókunar með því að breyta eða fjarlægja dagsetningarnar í reitunum Bókun leyfð frá og til í fjárhagsgrunni. Til að koma í veg fyrir afstemmingarvandamál er nauðsynlegt að bókunardagsetning fjárhagsfærslu samsvari bókunardagsetningu virðisfærslu.  

 Runuvinnslan skannar tafla 5811 - Bóka virðisfærslu í fjárhag, til að bera kennsl á virðisfærslur sem heyra undir bókun í fjárhag. Taflan var tæmd eftir heppnaða keyrslu.

## <a name="see-also"></a>Sjá einnig  

[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Hönnunarupplýsingar: Umsókn vöru](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
