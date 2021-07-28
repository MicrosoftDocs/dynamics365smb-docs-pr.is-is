---
title: Afskriftaaðferðir fyrir eignir
description: Kynntu þér mismunandi innbyggðar aðferðir til að afskrifa og niðurfæra eignir í sjálfgefinni útgáfu af Business Central sem felur í sér átta aðferðir.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 07/05/2021
ms.author: edupont
ms.openlocfilehash: 649a60f815da072a1a2794492c4e957ca74d8e08
ms.sourcegitcommit: a8a01561f46c0a60f8bfd7985be0dcd3e28441fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6343375"
---
# <a name="depreciation-methods-for-fixed-assets"></a>Afskriftaaðferðir fyrir eignir

Tiltækar eru átta afskriftaaðferðir í sjálfgefinni útgáfu [!INCLUDE [prod_short](includes/prod_short.md)]:  

* Línulegar  
* Hlutfallsleg afskrift 1  
* Hlutfallsleg afskrift 2  
* HA1/LL  
* HA2/LL  
* Notendaskilgreind  

  > [!NOTE]  
  > Tilgreinið eigin afskriftaraðferð með því að skilgreina afskriftatöflur. Upplýsingar um notkun afskriftaaðferðar sem notandi skilgreinir er að finna í [Setja upp afskriftaaðferð sem notandi skilgreinir](fa-how-setup-user-defined-depreciation-method.md).
* Handvirk  

  > [!NOTE]  
  > Hægt er að nota þessa aðferð á eignir sem ekki eru afskrifanlegar, til dæmis land. Færa þarf afskriftir eigna í eignafjárhagsfærslubók. Runuvinnslan **Reikna afskriftir** sleppir eignum sem þessi afskriftaaðferð er notuð á.  
* Tvisvar ári  

  > [!NOTE]  
  > Þegar þessi aðferð er notuð er eignin afskrifuð um sömu upphæð á hverju ári.  

## <a name="straight-line-depreciation"></a>Beinlínuafskrift

Þegar beinlínuaðferðin er notuð verður að tilgreina einn af eftirfarandi valkostum í eignaafskriftabókinni:  

* Afskriftatímabilið (ár eða mánuðir) eða lokadagsetningu afskrifta  
* Fasta árlega prósentu  
* Fasta árlega upphæð  
* Afskriftatímabil  

### <a name="depreciation-period"></a>Afskriftatímabil

Ef afskriftatímabilið (fjöldi afskriftaára, fjöldi afskriftamánaða eða lokadagsetning afskrifta) er fært inn reiknar eftirfarandi reikniregla upphæð afskrifta:  

*Afskriftaupphæð = ((Bókvirði - Hrakvirði) x Fjöldi afskriftadaga) / Afskriftadagar sem eftir*  

Afskriftadagar sem eftir eru reiknaðir sem fjöldi afskriftadaga mínus fjöldi daga milli upphafsdags afskrifta og dagsetningu síðustu eignafærslu.  

Lækka má bókvirði með upphæðum í bókaðri uppfærslu, niðurfærslu, sérsniðin upphæð 1 eða 2, eftir því hvort reiturinn **Taka með í afskriftaútreikn.** er óvirkur og hvort reiturinn **Hluti bókfærðs virðis** á síðunni: **uppsetning Eignabókunartegundar**. Þessi útreikningur tryggir að eignin sé að fullu afskrifuð á lokadegi afskrifta.  

### <a name="fixed-yearly-percentage"></a>Föst árleg prósenta

Ef færð er föst árleg prósenta notar forritið eftirfarandi reiknireglu til að reikna upphæð afskrifta:  

*Afskriftaupphæð = (Beinlínu % x Afskriftagrunnur x Fjöldi afskr. daga) / (100 x 360)*  

### <a name="fixed-yearly-amount"></a>Föst árleg upphæð

Ef færð er föst árleg upphæð notar forritið þessa reiknireglu til að reikna upphæð afskrifta:  

*Afskriftaupphæð = (Föst afskriftaupphæð x Fjöldi afskriftadaga) /360*  

### <a name="example---straight-line-depreciation"></a>Dæmi - línuleg afskrift

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

## <a name="declining-balance-1-depreciation"></a>Hlutfallsleg afskrift 1 Afskrift

Þetta er hröðunaraðferð þar sem stærstum hluta kostnaðar vegna eignar er úthlutað á fyrstu ár líftíma hennar. Nauðsynlegt er að tilgreina fasta árlega prósentu ef nota á þessa aðferð.  

Eftirfarandi formúla reiknar afskriftarupphæð:  

*Afskriftaupphæð = (Beinlínu % x Fjöldi afskr.daga x Afskriftagrunnur) / (100 x 360)*  

Afskriftagrunnurinn er reiknaður sem bókvirðið að frádregnum bókuðum afskriftum frá upphafsdagsetningu líðandi reikningsárs.  

Í upphæð bókaðra afskrifta geta verið færslur með ýmsum bókunartegundum (niðurfærslu, venju1 og venju2), bókaðar frá upphafsdagsetningu líðandi reikningsárs. Þessar bókunartegundir eru teknar með í bókaðri afskriftaupphæð ef gátmerki eru í reitunum **Afskriftategund** og **Hluti bókvirðis** á síðunni **uppsetning eignabókunartegundar**.  

### <a name="example---declining-balance-1-depreciation"></a>Dæmi - Hlutfallsleg afskrift 1 Afskrift

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

## <a name="declining-balance-2-depreciation"></a>Hlutfallsleg afskrift 2 Afskrift

Með aðferðunum Hlutfallsleg afskrift 1 og Hlutfallsleg afskrift 2 er reiknuð sama afskriftaupphæð fyrir hvert ár. Ef keyrslan **Reikna afskriftir** er keyrð oftar en einu sinni á ári leiðir aðferðin Hlutfallsleg afskrift 1 til þess að jafnar afskriftaupphæðir verða í hverju afskriftatímabili. Aðferðin Hlutfallsleg afskrift 2 leiðir á hinn bóginn til afskriftaupphæða sem lækka hlutfallslega fyrir hvert tímabil.  

### <a name="example---declining-balance-2-depreciation"></a>Dæmi - Hlutfallsleg afskrift 2 Afskrift

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

## <a name="db1sl-depreciation"></a>DB1/SL Afskrift

HLF1/LL – Þessi aðferð er blanda af hlutfallslegri afskrift 1 og línulegri. Útreikningurinn heldur áfram þar til bókfært virði er jafnt og frádráttarmagn eða hrakvirði sem þú slóst inn.  

Keyrslan **Reikna afskriftir** reiknar beinlínuupphæð og hlutfallslega upphæð, en aðeins stærri upphæðin er flutt í færslubókina.  

Þú getur notað ýmsar prósentur til að reikna minnkandi stöðu.  

Ef þessi aðferð er notuð verður að færa inn áætlaðan gagnlegan líftíma og prósentutölu hlutfallslegra afskrifta á síðunni **Eignaafskriftabækur**.  

### <a name="example---db1-sl-depreciation"></a>Dæmi - DB1-SL afskrift

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

## <a name="half-year-convention-depreciation"></a>Hálfsársafskrift

Afskriftir tvisvar á ári eru aðeins notaðar ef sett var gátmerki í reitinn **Nota hálfsársaðferð** í föstu síðunni **Eignaafskriftabók**.  

Þessa afskriftaaðferð má nota ásamt eftirfarandi afskriftaaðferðum í forritinu:  

* Línulegar  
* Hlutfallsleg afskrift 1  
* HA1/LL  

Þegar afskrifað er tvisvar á ári fær eign sex mánaða afskrift á fyrsta reikningsári án tillits til þess sem tilgreint er í reitnum **Upphafsdags. afskriftar**.  

> [!NOTE]  
> Áætlaðar eftirstöðvar af líftíma eignar eftir fyrsta reikningsárið verður alltaf hálft ár ef hálfsársaðferðin er notuð. Ef hálfsársaðferðinni er rétt beitt verður því ávallt í reitnum **Lokadags. afskriftar** á síðunni **Eignaafskriftabók** dagsetning sem er nákvæmlega sex mánuðum á undan lokadagsetningu reikningsársins þegar eignin er að fullu afskrifuð.  

### <a name="example---half-year-convention-depreciation"></a>Dæmi - Hálfsársafskriftir

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

## <a name="example---db1sl-depreciation-using-half-year-convention"></a>Dæmi - HLF1/LL tvisvar á ári

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

## <a name="duplicating-entries-to-more-depreciation-books"></a>Afritun færslna í fleiri afskriftabækur

Ef um er að ræða þrjár afskriftabækur B1, B2 og B3 og afrita á færslur úr B1 í B2 og B3 er hægt að setja gátmerki í reitinn **Hluti afritalista** á afskriftabókaspjöldunum fyrir B2 og B3. Þetta getur komið að gagni ef afskriftabókin B1 er samþætt fjárhag og notar eignafjárhagsbókina og afskriftabækurnar B2 og B3 eru ekki samþættar fjárhag og nota eignabókina.  

Þegar fært er í B1 í eignafjárhagsbókinni og gátmerki sett í reitinn **Nota afritalista** afritar forritið færsluna í bókina B2 og B3 í eignabókina þegar færslan er bókuð.  

> [!NOTE]  
> Ekki er hægt að afrita í sömu færslubók og færslubókarkeyrslu og verið er að afrita úr. Ef bókaðar eru færslur í fjárhagseignabók er hægt að afrita þær í eignabókina eða í fjárhagseignabókina með því að nota aðra keyrslu.  

> [!NOTE]  
> Ekki er hægt að nota sömu númeraröð í eignafjárhagsbók og í eignabók. Þegar færslur eru bókaðar í eignafjárhagsbók verður reiturinn **Númer fylgiskjals** að vera auður. Ef númer er fært í reitinn afritar kerfið númerið í eignabókina. Þú verður að breyta skjalnúmerinu handvirkt áður en þú getur sent inn dagbókina.  

## <a name="see-also"></a>Sjá einnig

[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
