---
title: Bókunardagsetning fyrir virðisfærslu leiðréttingar í samanburði við upprunafærsluna
description: Kynntu þér „Bókunardagsetning á leiðréttingarvirðisfærslu á móti bókunardagsetningu við innfærslu sem veldur leiðréttingu, eins og endurmati eða kostnaðarauka“ þegar runuvinnslan Leiðrétta kostnað - Birgðafærslur er keyrð.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/17/2021
ms.author: edupont
ms.openlocfilehash: 9d77c13cbe60d9e9b5c4d12e55d75f8815a4a5ba
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8138675"
---
# <a name="posting-date-on-adjustment-value-entry-compared-to-the-source-entry"></a>Bókunardagsetning fyrir virðisfærslu leiðréttingar í samanburði við upprunafærsluna

Í þessari grein er bókunardagsetning fyrir virðisfærslu leiðréttingar borin saman við bókunardagsetningu færslunnar veldur því að runuvinnslan Leiðrétta kostnað - Birgðafærslur er keyrð, sérstakleag í aðstæðum endurmats og kostnaðarauka.

Runuvinnslan **Leiðrétta kostnað - Birgðafærslur** vinnur úr gögnunum þínum eftir því hverjar aðstæðurnar eru og stillingunni á [!INCLUDE[prod_short](includes/prod_short.md)]. Í þessum hluta lýsum við tveimur aðskildum ferlum og fyrir hvorn þeirra sýnum við áhrifin sem runuvinnslan Leiðrétta kostnað - Birgðafærslur hefur á gögnin.

## <a name="revaluation-scenario"></a>Aðstæður endurmats

### <a name="prerequisites"></a>Frumskilyrði  

Sláið inn eftirfarandi gildi:

**Uppsetning birgða**:  

- Sjálfvirk kostnaðarbókun = Já  

- Sjálfvirk kostnaðarleiðrétting = Alltaf  

- Tegund meðalinnk.verðs = vara  

- Meðalkostnaðartímabil = Dagur  

**Uppsetning fjárhagsgrunns**:  

- Leyfa bókanir frá = 1. janúar 2021  

- Bókun leyfð til = tómt  

**Notandauppsetning**:  

- Leyfa bókanir frá = 1. desember 2020  

- Bókun leyfð til = tómt  

### <a name="to-test-the-scenario"></a>Að prófa aðstæðurnar

Prófaðu þessar aðstæður með því að fara í gegnum eftirfarandi skref.

1. Búðu til **Vöru** sem heitir TEST með eftirfarandi gildum:  

     - Grunnmælieining = STK  

     - Kostnaðarútreikningur = Meðaltal  

     - Velja valkvæða bókunarflokka.  

2. Opnaðu **Vörubók**, stofnaðu svo nýja færslu og bókaðu línu eins og hér segir:  

     - Bókunardagur = 15. desember 2020  

     - Vara = TEST  

     - Tegund færslu = Innkaup  

     - Magn = 100  

     - Ein.upphæð = 10  

3. Opnaðu **Vörubók**, stofnaðu svo nýja færslu og bókaðu línu eins og hér segir:  

     - Dagsetning = 20. desember 2020  

     - Vara = TEST  

     - Færslugerð = Neikvæð leiðrétting  

     - Magn = 2  

4. Opnaðu **Vörubók**, stofnaðu svo nýja færslu og bókaðu línu eins og hér segir:  

     - Dagsetning = 15. janúar 2021  

     - Vara = TEST  

     - Færslugerð = Neikvæð leiðrétting  

     - Magn = 3  

5. Opnaðu **Endurmatsbók vöru**, stofnaðu svo nýja færslu og bókaðu línu eins og hér segir:  

     - Vara = TEST  

     - Gildir-fyrir færslu = veldu innkaupafærsla bókuð í skrefi 2. Bókunardagsetning endurmats verður sú sama og fyrir færsluna sem hún leiðréttir.  

     - Kostnaðarverð (endurmetið) = 40  

Eftirfarandi **Birgðahöfuðbók** og **Virðisfærslur** hafa verið bókaðar:  

**Birgðabókafærsla - innkaup**:  

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

Runuvinnslan **Leiðréttur kostnaður - Birgðafærslur** hefur borið kennsl á breytingar á kostnaði og leiðrétti neikvæðu leiðréttingarnar.  

**Endurskoðun bókunardagsetninga á stofnuðum leiðréttingarvirðisfærslum:** Fyrstu leyfilegu bókunardagsetningar sem runuvinnslan Leiðréttur kostnaður - Birgðafærslur verður að tengjast er 1. janúar 2021 eins kemur fram í fjárhagsgrunni.  

**Neikvæð leiðrétting í skrefi 3:** úthlutuð bókunardagsetning er 1. janúar, veitt af fjárhagsgrunni. Bókunardagsetning virðisfærslunnar sem heyrir undir leiðréttingu er 20. desember 2020. Samkvæmt fjárhagsgrunni er dagsetningin ekki innan leyfilegs dagsetningabils bókunar. Þess vegna er bókunardagsetningunni, sem er nefnd í Bókun leyfð frá reit fjárhagsgrunns, úthlutað á leiðrétttingarvirðisfærsluna.  

**Neikvæð leiðrétting í skrefi 4:** úthlutuð bókunardagsetning er 15. janúar. Virðisfærslan sem heyrir undir leiðréttingu er með bókunardagsetninguna 15. janúar, sem er innan leyfilegs dagsetningabils bókunar samkvæmt fjárhagsgrunni.  

Leiðréttingin sem gerð var fyrir neikvæðu leiðréttinguna í skrefi 3 veldur umræðu. Hagstæða bókunardagsetningin fyrir leiðréttingarvirðisfærsluna hefði verið 20. desember eða að minnsta kosti í desember þar sem endurmatið sem olli breytingunni á kostnaði seldrar vöru var bókað í desember.  

Til að ná leiðréttingu í desember á neikvæðu leiðréttingunni í 3. skrefi þarf fjárhagsgrunnurinn, Bókun leyfð frá reit, að tilgreina dagsetningu í desember.  

### <a name="conclusion"></a>Niðurstaða

Í ljósi reynslunnar sem fengist hefur í þessum aðstæðum, þegar reynt er að finna út hentugustu uppsetninguna fyrir leyfilegt dagsetningabil bókunar fyrir fyrirtæki, er sniðugt að hafa eftirfarandi í huga. Svo lengi sem þú heimilar bókun breytinga á birgðaverðmæti á tímabili, desember í þessu tilviki, ætti uppsetningin sem fyrirtækið notar fyrir dagsetningabil sem er leyfilegt að bóka að vera í takt við þessa ákvörðun. Bókun leyfð frá í fjárhagsgrunni, þar sem fram kemur 1. desember, myndi leyfa að áframsenda endurmatið sem gert var í desember á færslur á útleið, sem verða fyrir áhrifum, á sama tímabilinu.  

Notendahópar sem ekki mega bóka í desember en í janúar, sem fjárhagsgrunnur átti líklega að takmarka í þessum aðstæðum, ætti frekar að staðsetja í notandauppsetningu.  

## <a name="item-charge-scenario"></a>Aðstæður kostnaðarauka  

### <a name="prerequisites"></a>Frumskilyrði  

Sláið inn eftirfarandi gildi:

**Uppsetning birgða**:  

- Sjálfvirk kostnaðarbókun = Já  

- Sjálfvirk kostnaðarleiðrétting = Alltaf  

- Tegund meðalinnk.verðs = vara  

- Meðalkostnaðartímabil = Dagur  

**Uppsetning fjárhagsgrunns**:  

- Leyfa bókanir frá = 1. desember 2020.  

- Bókun leyfð til = tómt  

**Notandauppsetning**:  

- Leyfa bókanir frá = 1. desember 2020.  

- Bókun leyfð til = tómt  

### <a name="to-test-the-scenario"></a>Að prófa aðstæðurnar  

Prófaðu þessar aðstæður með því að fara í gegnum eftirfarandi skref:

1.  Búðu til **Kostnaðarauka** með eftirfarandi gildum:  

     - Grunnmælieining = STK  

     - Kostnaðarútreikningur = Meðaltal  

     - Velja valkvæða bókunarflokka.  

2.  Stofnaðu nýja **Innkaupapöntun** með eftirfarandi gildum:  

     - Kaupa af lánardrottni nr.: 10000  

     - Bókunardagur = 15. desember 2020

     - Reikningsnr. lánardrottins: 1234  

     Í innkaupapöntunarlínunni skal velja eftirfarandi gildi:  

     - Vara = GJALD  

     - Magn = 1  

     - Innkaupsverð = 100  

     Til að ljúka skrefinu skal bóka skjalið sem móttekið eða reikningsfært.  

3.  Stofnaðu nýja **Sölupöntun** með eftirfarandi gildum:  

     - Selt til Viðskiptamaður Nr.: 10000  

     - Bókunardagsetning = 16. desember 2020  

     Í sölupöntunarlínu:  

     - Vara = GJALD  

     - Magn = 1  

     - Einingarverð = 135  

     Til að ljúka skrefinu skal bóka skjalið sem móttekið eða reikningsfært.  

4.  Færðu inn gildi fyrir síðuna **Uppsetning fjárhags**:  

     - Leyfa bókanir frá = 1. janúar 2021  

    -  Bókun leyfð til = autt  

5.  Stofnaðu nýja **Innkaupapöntun** með eftirfarandi gildum:  

     - Kaupa af lánardrottni nr.: 10000  

     - Bókunardagur = 2. janúar, 2021  

     - Reikningsnr. lánardrottins: 2345  

     Á innkaupapöntunarlínunni:  

     - Kostnaðarauki = JB-FLUTN  

     - Magn = 1  

     - Innkaupsverð = 3  

     - Úthlutaðu kostnaðarauka á innkaupakvittun úr skrefi 2.  

     Til að ljúka skrefinu skal bóka skjalið sem móttekið eða reikningsfært.  


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

     Stofnaðu nýja **Innkaupapöntun** með eftirfarandi gildum:  

     - Kaupa af lánardrottni nr.: 10000  

     - Bókunardagur = 30. desember 2020  

     - Reikningsnr. lánardrottins: 3456  

     Í innkaupapöntunarlínunni skal velja eftirfarandi gildi:  

     - Kostnaðarauki = JB-FLUTN  

     - Magn = 1  

     - Innkaupsverð = 2  

     Úthluta kostnaðarauka á innkaupamóttöku úr skrefi 2  

     Til að ljúka skrefinu skal bóka skjalið sem móttekið eða reikningsfært.  


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

Útlistaðar aðstæður enda með verðmætamati á birgðum sem sýnir magn = 0 á meðan gildið = 2. Bókaður kostnaðarauki í skrefi 6 er hluti af birgðaaukningunni í desember á meðan birgðaminnkun sama tímabils verður ekki fyrir áhrifum.  

Að fjárhagsgrunnurinn skyldi gefa upp Leyfa bókun frá og með 1. janúar var gott fyrir fyrsta kostnaðaraukann. Kostnaður við birgðaaukningu og -minnkun var skráð á sama tímabilið. Fyrir seinni kostnaðaraukann er það hins vegar fjárhagsgrunnurinn sem veldur því að breytingin á kostnaði seldrar vöru verði samþykktur fyrir næsta tímabil.  

**Niðurstaða:**  

Það er áskorun að fá skýrslu birgðavirðis til að sýna magn = 0 á meðan gildið <> 0. Í þessu tilfelli er það líka erfiðara að tjá ákjósanlegustu stillingar með því að hafa innkaupareikninga sem koma á sama degi en taka til mismunandi tímabila eða jafnvel reikningsára. Að færast yfir á nýtt reikningsár krefst yfirleitt einhverrar skipulagningar og sem hluti af því þarf að íhuga nánar ferli leiðréttingarkostnaðar - birgðafærslna, gera sér grein fyrir kostnaði seldra vara.  

Í þessari atburðarás getur einn möguleiki verið að hafa fjárhagsgrunninn, reitinn Bókun leyfð frá, gefa upp dagsetningu í desember fyrir nokkra daga í viðbót og fresta bókun á fyrsta kostnaðaraukanum svo allir kostnaðir fyrir fyrra tímabil/fjárhagsár verði viðurkenndir fyrir tímabilið sem þeir tilheyra í fyrstu, keyra síðan runuvinnslu Leiðrétts kostnaðar - Birgðafærslna og í kjölfarið færa leyfða bókunardagsetningu yfir á nýtt tímabil\/fjárhagsársins. Fyrsti kostnaðaraukinn með bókunardagsetninguna 2. janúar getur þá verið bókaður.  

## <a name="see-also"></a>Sjá einnig  

[Hönnunarupplýsingar: Bókunardagsetning á leiðréttingarvirðisfærslum](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Hönnunarupplýsingar: Umsókn vöru](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
