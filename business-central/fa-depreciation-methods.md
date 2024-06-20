---
title: Afskriftaaðferðir fyrir eignir
description: Fræðast um mismunandi innbyggðar aðferðir til að afskrifa eða niðurfæra eignir.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'write down, depreciate, depreciation'
ms.search.form: '5629, 5633'
ms.date: 03/25/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Afskriftaaðferðir fyrir eignir

[!INCLUDE [prod_short](includes/prod_short.md)] styður átta mismunandi afskriftaaðferðir fyrir eignir:

* Línuleg (LL)
* Hlutfallsleg 1 (HLF1)
* Hlutfallsleg afsl.2 (HLF2)
* HLF1/LL
* HLF2/LL
* Tvisvar ári
* Handvirkt
* Notandaskilgreindar afskriftir

## Línuleg afskrift

Með línulegri afskrift er eignavirðið afskrifað annaðhvort með fastri árlegri prósentu eða fastri árlegri upphæð yfir afskriftatímabilið. Þegar beinlínuaðferðin er notuð verður að tilgreina einn af eftirfarandi valkostum í eignaafskriftabókinni:  

* Afskriftatímabilið (ár eða mánuðir) eða lokadagsetningu afskrifta  
* Fasta árlega prósentu  
* Fasta árlega upphæð  
* Afskriftatímabil  

### Afskriftatímabil

Ef afskriftatímabilið (fjöldi afskriftaára, fjöldi afskriftamánaða eða lokadagsetning afskrifta) er fært inn reiknar eftirfarandi reikniregla upphæð afskrifta:  

* Afskriftaupphæð = ((Bókfært virði - Hrakvirði) x Fjöldi afskriftadaga) / Afskriftadagar sem eftir eru*  

Afskriftadagarnir sem eftir eru reiknaðir sem fjöldi afskriftadaga mínus fjöldi daga milli upphafsdagsetningar afskrifta og síðustu dagsetningu eignafærslu.  

Lækka má bókfært virði með bókuðum uppfærslum, niðurfærslu, venju 1 eða venju 2 eftir því hvort Reiturinn **Taka með í afskr. Reiturinn Útreikningur** er gerður óvirkur og hvort reiturinn **Hluti bókfærðs virðis** er virkjaður á síðunni **Eignabókunartegund, grunnur** . Þessi útreikningur tryggir að eignin sé að fullu afskrifuð á lokadegi afskrifta.  

### Föst árleg prósenta

Ef færð er föst árleg prósenta [!INCLUDE [prod_short](includes/prod_short.md)]  er eftirfarandi reikniregla notuð til að reikna upphæð afskrifta:  

* Afskriftaupphæð = (Línuleg % x Afskriftagrunnur x Fjöldi afskr. Dagar) / (100 x 360)*  

### Föst árleg upphæð

Ef færð er föst árleg upphæð [!INCLUDE [prod_short](includes/prod_short.md)]  er eftirfarandi reikniregla notuð til að reikna upphæð afskrifta:  

* Afskriftaupphæð = (Föst afskriftaupphæð x Fjöldi afskriftadaga) / 360*  

### Dæmi - Línuleg afskrift

Eign hefur stofnkostnaðinn SGM 100.000. Áætluð ending er átta ár. Keyrslan **Reikna afskrift** er keyrð annað hvert ár.  

Í þessu dæmi lítur færslan í eignabókinni svona út:  

| Dagsetning | Eignabókunartegund | Dagar | Upphæð | Bókfært virði |
| ---- | --------------- | ---- | ------ | ---------- |
| 01/01/20 |Stofnkostnaður |(Upphafsdagsetning afskrifta) |100,000.00 |100,000.00 |
| 06/30/20 |Afskrift |180 |-6.250,00 |93,750.00 |
| 12/31/20 |Afskrift |180 |-6.250,00 |87,500.00 |
| 06/30/21 |Afskrift |180 |-6.250,00 |81,250.00 |
| 12/31/21 |Afskrift |180 |-6.250,00 |75,000.00 |
| ...      |             |    |          |          |
| 06/30/27 |Afskrift |180 |-6.250,00 |6,250.00  |
| 12/31/27 |Afskrift |180 |-6.250,00 |0         |

## Hlutfallsleg afskrift 1

Þessi afskriftaaðferð úthlutar stærstum hluta kostnaðar eignar á fyrstu árin sem nýtist líftíma hennar. Nauðsynlegt er að tilgreina fasta árlega prósentu ef nota á þessa aðferð.  

Eftirfarandi formúla reiknar afskriftarupphæð:  

* Afskriftaupphæð = (Hlutfallsleg mótreikn. % x Fjöldi afskriftadaga x Afskr. Grunnur) / (100 x 360)*  

Afskriftagrunnurinn er reiknaður sem bókfært virði í upphafi ársins. Fjöldi afskriftadaga er fjöldi daga milli bókunardagsetningar og síðustu afskriftadagsetningar. [!INCLUDE [prod_short](includes/prod_short.md)] reiknar afskriftir sem miða að því að allar afskriftir sem gerðar eru á reikningsárinu séu gerðar með þessari reiknireglu.  

Í upphæð bókaðra afskrifta geta verið færslur með ýmsum bókunartegundum (niðurfærslu, venju1 og venju2), bókaðar frá upphafsdagsetningu líðandi reikningsárs. Þessar bókunartegundir eru teknar með í bókaðri afskriftaupphæð ef gátmerki eru í reitunum **Afskriftategund** og **Hluti bókvirðis** á síðunni **uppsetning eignabókunartegundar**.  

### Dæmi 1 - Hlutfallsleg afskrift 1

Eign hefur stofnkostnaðinn SGM 100.000. Reiturinn **Hlutfallsleg afskrift %** er 25. Keyrslan **Reikna afskrift** er keyrð annað hvert ár.  

Eftirfarandi tafla sýnir hvernig færslurnar í eignabókinni líta út.  

| Dagsetning | Eignabókunartegund | Dagar | Upphæð | Bókfært virði |
| ---- | --------------- | ---- | ------ | ---------- |
| 01/01/20 |Stofnkostnaður |(Upphafsdagsetning afskrifta) |100,000.00 |100,000.00 |
| 06/30/20 |Afskrift |180 |-12.500,00 |87,500.00 |
| 12/31/20 |Afskrift |180 |-12.500,00 |75,000.00 |
| 06/30/21 |Afskrift |180 |-9.375,00 |65,625.00 |
| 12/31/21 |Afskrift |180 |-9.375,00 |56,250.00 |
| 06/30/22 |Afskrift |180 |-7.031,25 |49,218.75 |
| 12/31/22 |Afskrift |180 |-7.031,25 |42,187.50 |
| 06/30/23 |Afskrift |180 |-5.273,44 |36,914.06 |
| 12/31/23 |Afskrift |180 |-5.273,44 |31,640.62 |
| 06/30/24 |Afskrift |180 |-3.955,08 |27,685.54 |
| 12/31/24 |Afskrift |180 |-3.955,08 |23,730.46 |
| ...      |             |    |          |          |

Reikningsaðferð:  

* Ár 1: *25% af 100.000 = 25.000 = 12.500 + 12.500*
* Ár 2: *25% af 75.000 = 18.750 = 9.375 + 9.375*
* Ár 3: *25% af 56.250 = 14.062,50 = 7.031,25 + 7.031,25*
* ...

Útreikningurinn heldur áfram þar til bókað virði er jafnt sléttaðri lokaupphæð eða hrakvirðinu sem var fært inn.  

### Dæmi 2 - Hlutfallsleg afskrift 1

Bókfært virði eignar er 100.000 þann 31.31.2022. Afskriftir eru bókaðar 1.778 þann 2/2/23, sem er væntanleg (hlutfallsleg) afskrift á 32 dögum. Ef afskriftir eru keyrðar 6/30/2023 [!INCLUDE [prod_short](includes/prod_short.md)] leggja til 8.222 því 148 dagar eru frá 2/2/2023 til 6/30/2023. Væntanlegar afskriftir fyrir 6/30/2023 eru reiknaðar með eftirfarandi reiknireglu:

* *148/360 x 0,20 x 100.000 = 8.222*

### Dæmi 3 - Hlutfallsleg afskrift 1

Ef bókuð er upphæð sem er ekki jöfn afskriftaaðferðinni Hlutfallsleg afskrift, til dæmis 5.000, [!INCLUDE [prod_short](includes/prod_short.md)]  leggur til afgangurinn af væntanlegri upphæð.

Bókfært virði eignar er 100.000 þann 31.31.2022. Afskriftir eru bókaðar 5.000 þann 2/2/2023 sem er hærri en áætluð (hlutfallsleg) 2/2/2023 á 32 dögum. Ef afskriftir eru keyrðar 6/30/2023 [!INCLUDE [prod_short](includes/prod_short.md)]  mun leggja til 8.222 því 148 dagar eru frá 2/2/2023 til 6/30/2023. Væntanlegar afskriftir fyrir 6/30/2023 eru reiknaðar með eftirfarandi reiknireglu:

* *148/360 x 0,20 x 100.000 = 8.222*

### Dæmi 4 - Hlutfallsleg afskrift 1

Bókfært virði eignar er 100.000 þann 31.31.2023. Afskriftir eru bókaðar 95.000 þann 2/2/2023 sem er hærri en leyfð afskriftaupphæð ársins. Ef afskriftir eru keyrðar 6/30/2023 [!INCLUDE [prod_short](includes/prod_short.md)]  eru tillögur um 5000 því 148 dagar eru frá 2/2/2023 til 6/30/2023. Væntanlegar afskriftir fyrir 6/30/2023 eru reiknaðar með eftirfarandi reiknireglu: 

* *148/360 x 0,20 x 100.000 = 8.222*

Bókfært virði sem eftir er er þó aðeins 5.000 svo [!INCLUDE [prod_short](includes/prod_short.md)] að það leggur til 5.000 vegna þess að bókfært virði getur ekki verið neikvætt.

## Hlutfallsleg afskrift 2

Með aðferðunum Hlutfallsleg afskrift 1 og Hlutfallsleg afskrift 2 er reiknuð sama afskriftaupphæð fyrir hvert ár. Ef keyrslan Reikna afskriftir **er keyrð** oftar en einu sinni á ári leiðir aðferðin Hlutfallsleg afskrift 1 af sér jafnar afskriftaupphæðir fyrir hvert afskriftatímabil. Aðferðin Hlutfallsleg 2 leiðir hins vegar til afskriftaupphæða sem lækka fyrir hvert tímabil.  

### Dæmi - Hlutfallsleg afskrift 2

Eign hefur stofnkostnaðinn SGM 100.000. Reiturinn **Hlutfallsleg afskrift %** er 25. Keyrslan **Reikna afskrift** er keyrð annað hvert ár. Færslurnar í eignabókinni líta þannig:  

| Dagsetning     | Eignabókunartegund  | Dagar                       | Upphæð    | Bókfært virði |
| -------- | ---------------- | -------------------------  | --------- | ---------- |
| 01/01/20 |Stofnkostnaður |(Upphafsdagsetning afskrifta)|100,000.00 |100,000.00 |
| 06/30/20 |Afskrift      |180                         |-13.397,46 | 86,602.54 |
| 12/31/20 |Afskrift      |180                         |-11.602,54 | 75,000.00 |
| 06/30/21 |Afskrift      |180                         |-10.048,09 | 64,951.91 |
| 12/31/21 |Afskrift      |180                         |-8,701.91  | 56,250.00 |
| ...      |                  |                            |           |           |

Reikningsaðferð:  

* *BV* = Bókfært virði  
* *Fd* = fjöldi afskriftadaga  
* *HLFP* = Hlutfallsleg afskriftaprósenta  
* *P* = *DBP*/100  
* *D* = *ND*/360  

Reiknireglan sem reiknar afskriftaupphæðirnar er:  

* *DA* = *BV* x (1 – (1 –P)<sup>D</sup>)

Afskriftargildi eru:  

| Dagsetning     | Útreikningur                                                |
| -------- | -----------                                                |
| 06/30/20 |AU = 100.000,00 x (1-(1 - 0,25)<sup>0,5</sup>) = 13.397,46 |
| 12/31/20 |AU = 86.602,54 x (1 - (1 - 0,25)<sup>0,5</sup>) = 11.602,54 |
| 06/30/21 |AU = 75.000,00 x (1 - (1 - 0,25)<sup>0,5</sup>) = 10.048,09 |
| 12/31/21 |AU = 64.951,91 x (1 - (1 - 0,25)<sup>0,5</sup>) = 8.701,91  |
| ...      |                                                            |

## HA1/LL afskrift

HLF1/LL – Þessi aðferð er blanda af hlutfallslegri afskrift 1 og línulegri. Útreikningurinn heldur áfram þar til bókfært virði er jafnt og frádráttarmagn eða hrakvirði sem þú slóst inn.  

 **Keyrslan Reikna afskriftir** reiknar línulega upphæð og hlutfallslega upphæð, en aðeins hærri upphæðirnar tvær eru fluttar í færslubókina.  

Þú getur notað ýmsar prósentur til að reikna minnkandi stöðu.  

Ef þessi aðferð er notuð verður að færa inn áætlaðan gagnlegan líftíma og prósentutölu hlutfallslegra afskrifta á síðunni **Eignaafskriftabækur**.  

> [!NOTE]
> Ef einhver af afskriftaaðferðum hlutfallslegrar afskriftar er notuð og keyra á afskriftir til margra ára þarf að keyra afskriftir hvers árs sérstaklega. Ef afskriftir eru keyrðar fyrir allt tímabilið frá kaupdagsetningu til loka síðasta reikningsárs eða síðasta reikningstímabils er líklegt að niðurstaðan verði röng. Til dæmis gæti þurft að keyra hana í mörg ár ef eldri gögn hafa verið flutt inn og raunverulegir kaupdagar fyrir eignirnar eru notaðir og ætlunin er að ná uppsöfnuðum afskriftum. Þegar um hlutfallslegar [!INCLUDE [prod_short](includes/prod_short.md)]  aðferðir er að ræða reiknast leyfðar afskriftir á ári og byrja á skráðu bókfærðu virði hvers árs. Það getur ekki gert margra ára afskriftir í einu þrepi.
>
> Skýrslan **Eignir - Áætlað virði** getur varpað afskriftum á mörgum árum sem gæti verið ruglingslegt samanborið við niðurstöðurnar sem notandi fær ef keyrðar eru afskriftir í mörg ár með einni af hlutfallslegu stöðuaðferðunum. 

### Dæmi - DB1-LL afskrift

Eign hefur stofnkostnaðinn SGM 100.000. Á síðunni **Eignaafskriftabækur** inniheldur reiturinn **Hlutfallsleg afskrift %** 25 og í reitnum **Fjöldi afskriftaára** er **8**. Keyrslan **Reikna afskrift** er keyrð annað hvert ár.  

Færslurnar í eignabókinni líta þannig:  

| Dagsetning | Eignabókunartegund | Dagar | Upphæð | Bókfært virði |
| --- | --- | --- | --- | --- |
| 01/01/20 |Stofnkostnaður |(Upphafsdagsetning afskrifta) |100,000.00 |100,000.00 |
| 06/30/20 |Afskrift |180 |-12.500,00 |87,500.00 |
| 12/31/20 |Afskrift |180 |-12.500,00 |75,000.00 |
| 06/30/21 |Afskrift |180 |-9.375,00 |65,625.00 |
| 12/31/21 |Afskrift |180 |-9.375,00 |56,250.00 |
| 06/30/22 |Afskrift |180 |-7.031,25 |49,218.75 |
| 12/31/22 |Afskrift |180 |-7.031,25 |42,187.50 |
| 06/30/23 |Afskrift |180 |-5.273,44 |36,914.06 |
| 12/31/23 |Afskrift |180 |-5.273,44 |31,640.62 |
| 06/30/24 |Afskrift |180 |-3.955,08 |27,685.54 |
| 12/31/24 |Afskrift |180 |-3.955,08 |23,730.46 |
| 06/30/25 |Afskrift |180 |-3.955,08 |19.775,38 LL |
| 12/31/25 |Afskrift |180 |-3.955,08 |15.820,30 LL |
| 06/30/26 |Afskrift |180 |-3.955,08 |11.865,22 LL |
| 12/31/26 |Afskrift |180 |-3.955,07 |7.910,15 LL |
| 06/30/27 |Afskrift |180 |-3.955,08 |3.955,07 LL |
| 12/31/27 |Afskrift |180 |-3.955,07 |0,00 LL |

`SL` eftir að bókfærða gildið merkir að beinlínuaðferðin var notuð.  

Reikningsaðferð:  

* Ár 1 (2020):  

    *Hlutfallsleg upphæð: 25% af 100.000 =  25.000 = 12.500 + 12.500*  

    *Línuleg upphæð = 100.000/8=12.500=6.250+6.250*  

    Hlutfallsleg upphæð er notuð vegna þess að hún er hærri.  
* ...
* Ár 5 (2025):  

    *Hlutfallsleg upphæð: 25% af 23.730,46 = 4.943,85= 2.471,92 + 2.471,92*  

    *Línuleg upphæð = 23.730,46/3 = 7.910,15=3.995,07+3.995,08*  

    Línulega upphæðin er notuð vegna þess að hún er hærri.  

## Afskriftir hálfs árs

Hálfsársaðferðin er aðeins notuð ef kveikt er á **víxluninni Nota hálfsársaðferð** fyrir eignina **á síðunni Eignaspjald** .  

Hægt er að nota þessa afskriftaaðferð með eftirfarandi afskriftaaðferðum:  

* Línuleg  
* Hlutfallsleg 1  
* HLF1/LL  

Þegar hálfsársaðferðinni er beitt hefur eign sex mánaða afskrift á fyrsta reikningsári, óháð efni reitsins **Upphafsdags** . afskriftar.  

> [!NOTE]  
> Áætlaðar eftirstöðvar af líftíma eignar eftir fyrsta reikningsárið verður alltaf hálft ár ef hálfsársaðferðin er notuð. Ef hálfsársaðferðinni er rétt beitt verður því ávallt í reitnum **Lokadags. afskriftar** á síðunni **Eignaafskriftabók** dagsetning sem er nákvæmlega sex mánuðum á undan lokadagsetningu reikningsársins þegar eignin er að fullu afskrifuð.  

### Dæmi - Hálfsársafskriftir

Eign hefur stofnkostnaðinn SGM 100.000. **Upphafsdags. afskriftar** er 01/03/20. Áætlaður líftími er fimm ár, þannig að **Lokadags. afskriftar** verður að vera 30/06/25. Keyrslan **Reikna afskriftir** er keyrð einu sinni á ári. Í þessu dæmi miðast fjárhagsárið við almanaksárið.  

Færslurnar í eignabókinni líta þannig:  

| Dagsetning | Eignabókunartegund | Dagar | Upphæð | Bókfært virði |
| --- | --- | --- | --- | --- |
| 03/01/20 |Stofnkostnaður |(Upphafsdagsetning afskrifta) |100,000.00 |100,000.00 |
| 12/31/20 |Afskrift |270 |-10.000,00 |90,000.00 |
| 12/31/21 |Afskrift |360 |-20.000,00 |70,000.00 |
| 12/31/22 |Afskrift |360 |-20.000,00 |50,000.00 |
| 12/31/23 |Afskrift |360 |-20.000,00 |30,000.00 |
| 12/31/24 |Afskrift |360 |-20.000,00 |10,000.00 |
| 12/31/25 |Afskrift |180 |-10.000,00 |0.00 |

## Dæmi - HLF1/LL afskriftir af hálfsársaðferð

Eign hefur stofnkostnaðinn SGM 100.000. **Upphafsdags. afskriftar** er 01/11/20. Áætlaður líftími er fimm ár, þannig að **Lokadagsetning afskriftar** verður að vera 30/06/25. Á síðunni **Eignaafskriftabækur** inniheldur reiturinn **Hlutfallsleg afskrifta %** 40. Keyrslan **Reikna afskriftir** er keyrð einu sinni á ári. Í þessu dæmi miðast fjárhagsárið við almanaksárið.  

Færslurnar í eignabókinni líta þannig:  

| Dagsetning | Eignabókunartegund | Dagar | Upphæð | Bókfært virði |
| --- | --- | --- | --- | --- |
| 11/01/20 |Stofnkostnaður |(Upphafsdagsetning afskrifta) |100,000.00 |100,000.00 |
| 12/31/20 |Afskrift |60 |-20.000,00 |80,000.00 |
| 12/31/21 |Afskrift |360 |-32.000,00 |48,000.00 |
| 12/31/22 |Afskrift |360 |-19.200,00 |28,800.00 |
| 12/31/23 |Afskrift |360 |-11.520,00 |17,280.00 |
| 12/31/24 |Afskrift |360 |-11.520,00 |5.760,00 LL |
| 12/31/25 |Afskrift |180 |  -5,760.00 |0,00 LL |

`SL` eftir að bókfærða gildið merkir að beinlínuaðferðin var notuð.  

Reikningsaðferð:  

* 1. ár:  

    *Hlutfallsleg upphæð = Upphæðin fyrir allt árið = 40% af 100.000 = 40.000.* Fyrir hálft ár þá 40.000 / 2 = 20.000  

    *Beinlínuupphæð = upphæðin fyrir Allt árið = 100.000 / 5 = 20.000.* Fyrir hálft ár þá = 20.000 / 2 = 10.000  

    Hlutfallsleg upphæð er notuð vegna þess að hún er hærri.  
* ...
* Ár 5 (2024):  

    *Hlutfallsleg upphæð: 40% af 17.280,00 = 6.912,00*  

    *Línuleg upphæð = 28.800 / 1,5 = 11.520,00*  

    Línulega upphæðin er notuð vegna þess að hún er hærri.  

## Afrita færslur í aðrar afskriftabækur

Ef um er að ræða þrjár afskriftabækur, B1, B2 og B3 og afrita á færslur úr B1 í B2 og B3 er hægt að kveikja á vífærslum í Hluta afritalista **á** afskriftabókarspjöldunum fyrir B2 og B3. Þessi stilling getur til dæmis verið gagnleg við eftirfarandi aðstæður:

* Afskriftabók B1 er samþætt fjárhag og notar eignafjárhagsbókina.
* Afskriftabækur B2 og B3 eru ekki samþættar fjárhag og nota eignabókina.  

Þegar færsla er gerð í B1 í eignafjárhagsbókinni og kveikt á **víxluninni Hluti afritalista** afritast [!INCLUDE [prod_short](includes/prod_short.md)]  færslan í bókina B2 og B3 í eignabókina þegar færslan er bókuð.  

> [!NOTE]  
> Ekki er hægt að afrita í sömu færslubók og bókarkeyrslu og verið er að afrita úr. Ef bókaðar eru færslur í fjárhagseignabók er hægt að afrita þær í eignabókina eða í fjárhagseignabókina með því að nota aðra keyrslu.  

> [!NOTE]  
> Ekki er hægt að nota sömu númeraröð í eignafjárhagsbók og eignabók. Þegar færslur eru bókaðar í eignafjárhagsbók verður reiturinn **Númer fylgiskjals** að vera auður. Ef númer er fært í reitinn er númerið afritað í eignabókina. Þú verður að breyta skjalnúmerinu handvirkt áður en þú getur sent inn dagbókina.  

## Handvirk afskrift

Handvirk aðferð er notuð fyrir eignir sem ekki falla undir afskriftir, til dæmis land. Færa þarf afskriftir eigna í eignafjárhagsfærslubók. Keyrslan **Reikna afskriftir** sleppir eignum sem handvirk afskriftaaðferð er notuð á.

## Notandaskilgreindar afskriftir

Ef innbyggðar afskriftaaðferðir uppfylla ekki þarfir notanda er hægt að skilgreina eigin afskriftaaðferð með því að nota afskriftatöflur. Nánari upplýsingar um notkun notendaskilgreindra afskriftaaðferða eru notaðar með því að fara í [Setja upp afskriftaaðferð sem notandi skilgreinir](fa-how-setup-user-defined-depreciation-method.md).

## Sjá einnig .

[Yfirlit yfir eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
