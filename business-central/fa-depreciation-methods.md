---
title: Afskriftaaðferðir fyrir eignir
description: Læri um mismunandi byggðaðferðaðferðir við afskriftir eða niðurfærslu eigna.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'write down, depreciate, depreciation'
ms.search.form: '5629, 5633'
ms.date: 08/08/2023
ms.custom: bap-template
---
# Afskriftaaðferðir fyrir eignir

Til eru átta afskriftareglur sem tiltækar eru í [!INCLUDE [prod_short](includes/prod_short.md)]:  

* Línuleg  
* Hlutfallsleg 1  
* Hlutfallsleg 2  
* HA1/LL  
* HA2/LL  
* Notendaskilgreind  

  > [!NOTE]  
  > Tilgreinið eigin afskriftaraðferð með því að skilgreina afskriftatöflur. Til að fræðast meira um jöfnun á afskriftaraðferð sem notandi skilgreinir er farið í að  [Setja upp notandaskilgreinda afskriftaraðferð](fa-how-setup-user-defined-depreciation-method.md).
* Handvirkt  

  > [!NOTE]  
  > Notaðu handvirka aðferðina fyrir eignir sem eru ekki háðar afskriftum, t.d. land. Færa þarf afskriftir eigna í eignafjárhagsfærslubók.  **Keyrslan Reikna afskriftir**  fella niður eignir sem nota handvirka afskriftaaðferðina.  
* Tvisvar ári  

  > [!NOTE]  
  > Með þessari aðferð afskrifast eignir um sömu upphæð á hverju ári.  

## Línuleg afskrift

Þegar beinlínuaðferðin er notuð verður að tilgreina einn af eftirfarandi valkostum í eignaafskriftabókinni:  

* Afskriftatímabilið (ár eða mánuðir) eða lokadagsetningu afskrifta  
* Fasta árlega prósentu  
* Fasta árlega upphæð  
* Afskriftatímabil  

### Afskriftatímabil

Ef afskriftatímabilið (fjöldi afskriftaára, fjöldi afskriftamánaða eða lokadagsetning afskrifta) er fært inn reiknar eftirfarandi reikniregla upphæð afskrifta:  

*Afskriftaupphæð = ((Bókvirði - Hrakvirði) x Fjöldi afskriftadaga) / Afskriftadagar sem eftir*  

Afskriftadagar sem eftir eru reiknaðir sem fjöldi afskriftadaga mínus fjöldi daga milli upphafsdags afskrifta og dagsetningu síðustu eignafærslu.  

Lækka má bókvirði með upphæðum í bókaðri uppfærslu, niðurfærslu, sérsniðin upphæð 1 eða 2, eftir því hvort reiturinn **Taka með í afskriftaútreikn.** er óvirkur og hvort reiturinn **Hluti bókfærðs virðis** á síðunni: **uppsetning Eignabókunartegundar**. Þessi útreikningur tryggir að eignin sé að fullu afskrifuð á lokadegi afskrifta.  

### Föst árleg hlutfallstala

Ef föst árleg prósenta er færð inn er  [!INCLUDE [prod_short](includes/prod_short.md)]  notuð eftirfarandi formúla til að reikna út afskriftaupphæðina:  

*Afskriftaupphæð = (Beinlínu % x Afskriftagrunnur x Fjöldi afskr. daga) / (100 x 360)*  

### Föst árleg upphæð

Ef föst árleg upphæð er færð inn er  [!INCLUDE [prod_short](includes/prod_short.md)]  notuð eftirfarandi formúla til að reikna út afskriftaupphæðina:  

* *Afskriftaupphæð = (Föst afskriftaupphæð x Fjöldi afskriftadaga) /360*  

### Dæmi-línuleg afskrift

Eign hefur stofnkostnaðinn SGM 100.000. Áætluð ending er átta ár. Keyrslan **Reikna afskrift** er keyrð annað hvert ár.  

Í þessu dæmi lítur færslan í eignabókinni svona út:  

| Dagsetning | Eignabókunartegund | Dagar | Upphæð | Bókfært virði |
| --- | --- | --- | --- | --- |
| 01/01/20 |Stofnkostnaður |(Upphafsdagsetning afskrifta) |100,000.00 |100,000.00 |
| 06/30/20 |Afskrift |180 |-6.250,00 |93,750.00 |
| 12/31/20 |Afskrift |180 |-6.250,00 |87,500.00 |
| 06/30/21 |Afskrift |180 |-6.250,00 |81,250.00 |
| 12/31/21 |Afskrift |180 |-6.250,00 |75,000.00 |
| 06/30/27 |Afskrift |180 |-6.250,00 |6,250.00 |
| 12/31/27 |Afskrift |180 |-6.250,00 |0 |

## Hlutfallsleg afskrift 1.

Þessi afskriftaaðferð úthlutar stærstum hluta kostnaðar eignar á fyrstu árum líftíma hennar. Nauðsynlegt er að tilgreina fasta árlega prósentu ef nota á þessa aðferð.  

Eftirfarandi formúla reiknar afskriftarupphæð:  

* *Afskriftaupphæð = (Beinlínu % x Fjöldi afskr.daga x Afskriftagrunnur) / (100 x 360)*  

Afskrifanlegur Grunnur er reiknaður sem bókfært virði í upphafi árs. Fjöldi afskriftadaga er fjöldi daga á milli bókunardagsetningar og síðustu afskriftadagsetningar. [!INCLUDE [prod_short](includes/prod_short.md)] reiknar afskriftir miðað við að allar afskriftir sem eru gerðar á reikningsárinu sé gert með þessari formúlu.  

Í upphæð bókaðra afskrifta geta verið færslur með ýmsum bókunartegundum (niðurfærslu, venju1 og venju2), bókaðar frá upphafsdagsetningu líðandi reikningsárs. Þessar bókunartegundir eru teknar með í bókaðri afskriftaupphæð ef gátmerki eru í reitunum **Afskriftategund** og **Hluti bókvirðis** á síðunni **uppsetning eignabókunartegundar**.  

### Dæmi 1-Hlutfallsleg afskrift 1

Eign hefur stofnkostnaðinn SGM 100.000. Reiturinn **Hlutfallsleg afskrift %** er 25. Keyrslan **Reikna afskrift** er keyrð annað hvert ár.  

Eftirfarandi tafla sýnir hvernig færslurnar í eignabókinni líta út.  

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

Reikningsaðferð:  

* Ár 1: *25% af 100.000 = 25.000 = 12.500 + 12.500*

* Ár 2: *25% af 75.000 = 18.750 = 9.375 + 9.375*

* Ár 3: *25% af 56.250 = 14.062,50 = 7.031,25 + 7.031,25*

Útreikningurinn heldur áfram þar til bókað virði er jafnt sléttaðri lokaupphæð eða hrakvirðinu sem var fært inn.  

### Dæmi 2-Hlutfallsleg afskrift 1

Bókfært virði eignarinnar er 100.000 þann 12/31/2022. Þú bókar afskrift 1.778. á 2/2/23 sem er áætluð (Hlutfallsleg) upphæð afskrifta á ári í 32 daga. Ef keyrslan afskrift þann 6/30/2023  [!INCLUDE [prod_short](includes/prod_short.md)]  leggst á 8.222 þar af eru 148 dagar frá 2/2/2023 fram til 6/30/2023. Áætlaðar Eftirstöðvar afskrifta fyrir 6/30/2023 eru reiknaðar með eftirfarandi formúlu:

* *148/360 x 0,20 x 100.000 = 8.222*

### Dæmi 3-Hlutfallsleg afskrift 1

Ef upphæð sem ekki er samræmd með stiglækkandi stöðu 1 afskriftaraðferð, t.d. 5.000,  [!INCLUDE [prod_short](includes/prod_short.md)]  leggst á afgang af áætlaðri upphæð.

Bókfært virði eignarinnar er 100.000 þann 12/31/2022. Þú bókar afskrift 5.000. á 2/2/2023 sem er meira en Væntanleg (Hlutfallsleg) upphæð á 2/2/2023 á 32 daga. Ef keyrt er afskrift á 6/30/2023,  [!INCLUDE [prod_short](includes/prod_short.md)]  leggst 8.222, þar af eru 148 dagar frá 2/2/2023 fram til 6/30/2023. Áætlaðar Eftirstöðvar afskrifta fyrir 6/30/2023 eru reiknaðar með eftirfarandi formúlu:

* *148/360 x 0,20 x 100.000 = 8.222*

### Dæmi 4-Hlutfallsleg afskrift 1.

Bókfært virði eignarinnar er 100.000 þann 12/31/2023. Afskrift er bókuð á 95.000 í 2/2/2023 sem er umfram leyfða afskriftarupphæð ársins. Ef keyrt er afskrift á 6/30/2023,  [!INCLUDE [prod_short](includes/prod_short.md)]  leggst 5000, þar af eru 148 dagar frá 2/2/2023 fram til 6/30/2023. Áætlaðar Eftirstöðvar afskrifta fyrir 6/30/2023 eru reiknaðar með eftirfarandi formúlu: 

* *148/360 x 0,20 x 100.000 = 8.222*

Bókfært virði er hins vegar aðeins 5.000, þannig  [!INCLUDE [prod_short](includes/prod_short.md)]  að lagt er 5.000 vegna þess að bókfært virði getur ekki verið neikvætt.

## Hlutfallsleg afskrift 2

Með aðferðunum Hlutfallsleg afskrift 1 og Hlutfallsleg afskrift 2 er reiknuð sama afskriftaupphæð fyrir hvert ár. Ef keyrslan **Reikna afskriftir** er keyrð oftar en einu sinni á ári leiðir aðferðin Hlutfallsleg afskrift 1 til þess að jafnar afskriftaupphæðir verða í hverju afskriftatímabili. Aðferðin Hlutfallsleg afskrift 2 leiðir á hinn bóginn til afskriftaupphæða sem lækka hlutfallslega fyrir hvert tímabil.  

### Dæmi-Hlutfallsleg afskrift 2

Eign hefur stofnkostnaðinn SGM 100.000. Reiturinn **Hlutfallsleg afskrift %** er 25. Keyrslan **Reikna afskrift** er keyrð annað hvert ár. Færslurnar í eignabókinni líta þannig:  

| Dagsetning | Eignabókunartegund | Dagar | Upphæð | Bókfært virði |
| --- | --- | --- | --- | --- |
| 01/01/20 |Stofnkostnaður |(Upphafsdagsetning afskrifta)|100,000.00 |100,000.00 |
| 06/30/20 |Afskrift |180 |-13.397,46 |86,602.54 |
| 12/31/20 |Afskrift |180 |-11.602,54 |75,000.00 |
| 06/30/21 |Afskrift |180 |-10.048,09 |64,951.91 |
| 12/31/21 |Afskrift |180 |-8,701.91 |56,250.00 |

Reikningsaðferð:  

* *BV* = Bókfært virði  
* *Fd* = fjöldi afskriftadaga  
* *HLFP* = Hlutfallsleg afskriftaprósenta  
* *P* = *DBP*/100  
* *D* = *ND*/360  

Reiknireglan fyrir útreikning á afskriftaupphæðum er:  

*DA* = *BV* x (1 – (1 –P)<sup>D</sup>)

Afskriftargildi eru:  

| Dagsetning | Útreikningur |
| --- | --- |
| 06/30/20 |AU = 100.000,00 x (1-(1 - 0,25)<sup>0,5</sup>) = 13.397,46 |
| 12/31/20 |AU = 86.602,54 x (1 - (1 - 0,25)<sup>0,5</sup>) = 11.602,54 |
| 06/30/21 |AU = 75.000,00 x (1 - (1 - 0,25)<sup>0,5</sup>) = 10.048,09 |
| 12/31/21 |AU = 64.951,91 x (1 - (1 - 0,25)<sup>0,5</sup>) = 8.701,91 |

## HA1/LL.M. afskrift

HLF1/LL – Þessi aðferð er blanda af hlutfallslegri afskrift 1 og línulegri. Útreikningurinn heldur áfram þar til bókfært virði er jafnt og frádráttarmagn eða hrakvirði sem þú slóst inn.  

 **Keyrslan Reikna afskriftir**  reiknar línulega upphæð og minnkandi stöðu upphæðar en aðeins upphæðirnar sem eru tvær eru færðar í færslubókina.  

Þú getur notað ýmsar prósentur til að reikna minnkandi stöðu.  

Ef þessi aðferð er notuð verður að færa inn áætlaðan gagnlegan líftíma og prósentutölu hlutfallslegra afskrifta á síðunni **Eignaafskriftabækur**.  

### Dæmi-HA1-SL afskrift

Eign hefur stofnkostnaðinn SGM 100.000. Á síðunni **Eignaafskriftabækur** er 25 í reitnum **Hlutfallsleg afskrifta %** og í reitnum **Fjöldi afskriftaára** er talan 8. Keyrslan **Reikna afskrift** er keyrð annað hvert ár.  

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

`SL` á eftir bókfærðu virði merkir að beinlínuaðferð hafi verið notuð.  

Reikningsaðferð:  

* Ár 1 (2020):  

    *Hlutfallsleg upphæð: 25% af 100.000 =  25.000 = 12.500 + 12.500*  

    *Línuleg upphæð = 100.000/8=12.500=6.250+6.250*  

    Hlutfallsleg upphæð er notuð vegna þess að hún er hærri.  

* Ár 5 (2025):  

    *Hlutfallsleg upphæð: 25% af 23.730,46 = 4.943,85= 2.471,92 + 2.471,92*  

    *Línuleg upphæð = 23.730,46/3 = 7.910,15=3.995,07+3.995,08*  

    Línulega upphæðin er notuð vegna þess að hún er hærri.  

## Hálfs árs samningur um afskriftir

Afskriftir tvisvar á ári eru aðeins notaðar ef sett var gátmerki í reitinn **Nota hálfsársaðferð** í föstu síðunni **Eignaafskriftabók**.  

Hægt er að nota þessa afskriftaraðferð með eftirfarandi afskriftaraðferðum:  

* Línuleg  
* Hlutfallsleg 1  
* HLF1/LL  

Þegar afskrifað er tvisvar á ári fær eign sex mánaða afskrift á fyrsta reikningsári án tillits til þess sem tilgreint er í reitnum **Upphafsdags. afskriftar**.  

> [!NOTE]  
> Áætlaðar eftirstöðvar af líftíma eignar eftir fyrsta reikningsárið verður alltaf hálft ár ef hálfsársaðferðin er notuð. Ef hálfsársaðferðinni er rétt beitt verður því ávallt í reitnum **Lokadags. afskriftar** á síðunni **Eignaafskriftabók** dagsetning sem er nákvæmlega sex mánuðum á undan lokadagsetningu reikningsársins þegar eignin er að fullu afskrifuð.  

### Dæmi-hálfs árs samningur afskriftir

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

## Dæmi-HA1/SL afskrift með hálfs árs samningi

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

`SL` á eftir bókfærðu virði merkir að beinlínuaðferð hafi verið notuð.  

Reikningsaðferð:  

* 1. ár:  

    *Hlutfallsleg upphæð = Upphæðin fyrir allt árið = 40% af 100.000 = 40.000.* Fyrir hálft ár þá 40.000 / 2 = 20.000  

    *Beinlínuupphæð = upphæðin fyrir Allt árið = 100.000 / 5 = 20.000.* Fyrir hálft ár þá = 20.000 / 2 = 10.000  

    Hlutfallsleg upphæð er notuð vegna þess að hún er hærri.  

* Ár 5 (2024):  

    *Hlutfallsleg upphæð: 40% af 17.280,00 = 6.912,00*  

    *Línuleg upphæð = 28.800 / 1,5 = 11.520,00*  

    Línulega upphæðin er notuð vegna þess að hún er hærri.  

## Afritar færslur í fleiri afskriftabækur

Ef þú ert með þrjár afskriftabækur B1, B2 og B3 og þú vilt taka afrit af færslum úr B1 í B2 og B3, getur þú valið  **gátreitinn í gátreitnum Afriation list**  á afskriftabókarspjöldin fyrir B2 og B3. Þessi stilling getur til dæmis hentað vel við eftirfarandi aðstæður:

* Afskriftabók B1 samnýtir fjárhagsbók og notar eiginn fjárhagsfærslubók.
* Afskriftabækur B2 og B3 ekki samþætta við fjárhag og nota eignabók.  

Þegar færsla í B1 er gerð í eignakaup fjárhags og gátreiturinn nota afritunarlista  **·**  er valinn  [!INCLUDE [prod_short](includes/prod_short.md)]  skal tvítaka færsluna í bókinni B2 og B3 í eignabók þegar færslan er bókuð.  

> [!NOTE]  
> Ekki er hægt að afrita í sömu færslubók og færslubókarkeyrslu og verið er að afrita úr. Ef bókaðar eru færslur í fjárhagseignabók er hægt að afrita þær í eignabókina eða í fjárhagseignabókina með því að nota aðra keyrslu.  

> [!NOTE]  
> Ekki er hægt að nota sömu númeraröð í eignakaup-og eignabók. Þegar færslur eru bókaðar í eignafjárhagsbók verður reiturinn **Númer fylgiskjals** að vera auður. Ef númer er fært í reitinn er númerið tvískráð í eignabók. Þú verður að breyta skjalnúmerinu handvirkt áður en þú getur sent inn dagbókina.  

## Sjá einnig .

[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
