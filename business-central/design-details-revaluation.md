---
title: Hönnunarupplýsingar - Endurmat
description: Hægt er að endurmeta birgðir á grundvelli virðisgrundvallar sem endurspeglar nákvæmast birgðavirði.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 07/07/2023
ms.custom: bap-template
---

# Hönnunarupplýsingar: Endurmat

Hægt er að endurmeta birgðir á grundvelli virðisgrundvallar sem endurspeglar nákvæmast birgðavirði. Einnig er hægt að bakfærsludagsetninguna til að uppfæra rétt Kostnaðarverð seldra vara (COGS) fyrir vörur sem notandi hefur þegar selt. Vörur sem nota staðalaðferð kostnaðarútreiknings og eru ekki fyllilega reikningsfærðar er einnig hægt að endurmeta.  

Í [!INCLUDE[prod_short](includes/prod_short.md)] er eftirfarandi sveigjanleiki studdur varðandi endurmat:  

- Endurmetanlegt magn er hægt að reikna fyrir allar dagsetningar, líka aftur í tímann.  
- Fyrir vörur sem nota kostnaðarútreikninginn Staðlað eru áætlaðar kostnaðarfærslur hafðar með í endurmatinu.  
- Birgðaminnkanir sem verða fyrir áhrifum af endurmati eru greindar.  

## Reiknaðu endurverðmagnið

Magnið sem hægt er að endurmeta er þær birgðir sem eru tiltækar á tiltekinni dagsetningu. Magnið er Samtala reikningsfærðra birgðafærslna sem bókaðar eru á eða á undan endurmatsdagsetningunni.  

> [!NOTE]  
>  Vörur sem nota hefðbundna aðferð kostnaðarútreiknings eru meðhöndlaðar á annan hátt við reikningu endurmetanlegs magns fyrir vöru, birgðageymslu og afbrigði. Magn og virði birgðahöfuðbókarfærslna sem ekki hafa verið að fullu reikningsfærðar eru teknar með í endurverðmetanlega magninu.  

Eftir bókun endurmats er hægt að bóka birgðaaukningu eða -minnkun með bókunardagsetningu sem er á eftir bókunardagsetningu endurmats. Hins vegar hefur endurmat ekki áhrif á þetta magn. Til að halda jafnvægi á birgðum, aðeins upprunalega endurmetanlegt magn er talið.  

Þar sem hægt er að endurmeta á hvaða degi verður að hafa reglur um það hvenær vara er gerð sem hluti af birgðum. Til dæmis hvenær vara er í birgðum og hvenær varan er verk í vinnslu (VÍV).  

### Dæmi  

Eftirfarandi dæmi sýnir þegar VÍV-vara verður hluti birgða. Dæmið er byggt á við framleiðsluna á keðja með 150 tenglum.  

![VÍV birgðir og endurmat.](media/design_details_inventory_costing_10_revaluation_wip.png "VÍV birgðir og endurmat")  

**1Q**: Notandinn bókar innkaupatenglana sem móttekna. Eftirfarandi tafla sýnir afleidda birgðafærslu.  

|Bókunardags.|Vara|Tegund færslu|Magn|Færslunr.|  
|------------------|----------|----------------|--------------|---------------|  
|01-01-20|TENGILL|Innkaup|150|1|  

> [!NOTE]  
>  Nú er vara sem notar hefðbundna aðferð kostnaðarútreiknings í boði fyrir endurmat.  

**1V**: Notandinn bókar innkaupatengla sem reikningsfærða og tenglarnir verða hluti birgða, fjárhagslega séð. Eftirfarandi tafla sýnir afleiddar virðisfærslur.  

|Bókunardags.|Tegund færslu|Dagsetning mats|Kostnaðarupphæð (raunverul.)|Birgðafærslunr.|Færslunr.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-15-20|Beinn kostnaður|01-01-20|150,00|1|1|  

 **2Q + 2 V**: Notandinn bókar innkaupatengla sem notaða í framleiðslu járnkeðju. Fjárhagslega séð verða tenglarnir hluti af birgðum VÍV.  Eftirfarandi tafla sýnir afleidda birgðafærslu.  

|Bókunardags.|Vara|Tegund færslu|Magn|Færslunr.|  
|------------------|----------|----------------|--------------|---------------|  
|02-01-20|TENGILL|Notkun|-150|1|  

Eftirfarandi tafla sýnir afleidda virðisfærslu.  

|Bókunardags.|Tegund færslu|Dagsetning mats|Kostnaðarupphæð (raunverul.)|Birgðafærslunr.|Færslunr.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|02-01-20|Beinn kostnaður|02-01-20|-150,00|2|2|  

Virðisdagsetningin er stillt á dagsetningu bókunar fyrir notkun (02-01-20) sem regluleg birgðaminnkun.  

**3Q**: Notandinn bókar keðjuna sem frálag og lokar framleiðslupöntuninni. Eftirfarandi tafla sýnir afleidda birgðafærslu.  

|Bókunardags.|Vara|Tegund færslu|Magn|Færslunr.|  
|------------------|----------|----------------|--------------|---------------|  
|02-15-20|KEÐJA|Frálag|1|3|  

**3V**: Notandinn keyrir runuvinnsluna **Leiðrétta kostnað - Birgðafærslur**, sem bókar keðjuna sem reikningsfærða tila ð sýna að öll efnisnotkun hefur verið reikningsfærð að fullu. Fjárhagslega séð eru tenglarnir ekki lengur hluti af birgðum VÍV þegar frálagið er reikningsfært og jafnað að fullu. Eftirfarandi tafla sýnir afleiddar virðisfærslur.  

|Bókunardags.|Tegund færslu|Dagsetning mats|Kostnaðarupphæð (raunverul.)|Birgðafærslunr.|Færslunr.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-15-20|Beinn kostnaður|01-01-20|150,00|2|2|  
|02-01-20|Beinn kostnaður|02-01-20|-150,00|2|2|  
|02-15-20|Beinn kostnaður|02-15-20|150.00|3|3|  

## Áætlaður kostnaður við endurmat

Magnið sem hægt er að endurmeta er Samtala magns fyrir reikningsfærðar birgðafærslur sem voru bókaðar á eða fyrir endurmatsuppfærslu. Þegar sumar vörur eru mótteknar eða afhentar en ekki reikningsfærðar er ekki hægt að reikna birgðavirði þeirra. Vörur sem nota staðalaðferð kostnaðarútreiknings eru ekki takmarkaðar á þennan hátt.  

> [!NOTE]  
>  Önnur gerð áætlaðs kostnaðar sem hægt er að endurmeta eru VÍV-birgðir, eftir tilteknum reglum. Frekari upplýsingar eru í [VÍV endurmat á birgðum](design-details-revaluation.md#wip-inventory-revaluation).  

Þegar reiknað er endurverðmagn fyrir vörur sem nota staðlaða aðferð við útreikning kostnaðar inniheldur Útreikningur birgðafærslur sem eru ekki fyllilega reikningsfærðar. Færslurnar eru endurmetnar þegar endurmatið er bókað. Þegar endurmetna færslan er reikningsstofnuð eru eftirfarandi virðisfærslur stofnaðar:  

- Vanaleg virðisdagsetning reikningsins með færslugerðinni **Beinn kostnaður**. Kostnaðurupphæð á þessari færslu er bein kostnaður frá upptökum línu.  
- Virðisfærsla með færslugerðinni **Frávik**. Þessi færsla skráir muninn milli reikningsfærðs kostnaðar og endurmetins staðalkostnaðar.  
- Virðisfærsla með færslugerðinni **Endurmat**. Þessi færsla sýnir bakfærslu á endurmati væntanlegs kostnaðar.

### Dæmi  

Eftirfarandi dæmi miðast við framleiðslu keðjunnar í fyrra dæminu. Þetta dæmi sýnir hvernig færslurnar þrjár eru stofnaðar, Byggt á eftirfarandi atburðarás:  

1.  Þú bókar keyptu hlekkinn sem móttekur með kostnaðarverði ISK 2,00.  
2.  Endurmat á tenglunum er bókað með nýju kostnaðarverði ISK 3,00 og uppfærsla staðalkostnaðarins í ISK 3,00.  
3.  Upphafleg kaup eru bókuð á keðjutengla sem reikningsfærðar, sem stofnar eftirfarandi virðisfærslur:  

    1.  Reikningsfærð virðisfærsla með færslugerð **Beinn kostnaður**.  
    2.  Virðisfærsla með færslugerð **Endurmat** til að skrá bakfærslu endurmats áætlaðs kostnaðar.  
    3.  Virðisfærsla með færslugerðinni Frávik, skráir mismun milli reikningsfærðs kostnaðar og endurmetins staðalkostnaðar.  

Eftirfarandi tafla sýnir niðurstöðurnar.  

|Skref|Bókunardagsetning|Færslutegund|Dagsetning virðismats|Kostnaðarupphæð (væntanl.)|Kostnaðarupphæð (raunverul.)|Birgðafærslunr.|Færslunr.|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|01-15-20|Beinn kostnaður|01-15-20|300,00|0,00|1|1|  
|2.|01-20-20|Endurmat|01-20-20|150,00|0,00|1|2|  
|3.a.|01-15-20|Beinn kostnaður|01-15-20|-300,00|0,00|1|3|  
|3.b.|01-15-20|Endurmat|01-20-20|-150,00|0,00|1|4|  
|3.c.|01-15-20|Frávik|01-15-20|0.00|450.00|1|5|  

## Ákvarða hvort Endurmat hafi áhrif á minnkun birgða  

Nota dagsetningu bókunar eða endurmats til að ákvarða hvort minnkun á birgðum hafi áhrif á endurmat.  

Eftirfarandi tafla sýnir skilyrðin sem eru notuð fyrir vöru sem notar ekki Meðalkostnaðarútreikningsaðferðina.  

|Aðstæður|Færslunr.|Tímasetning|Verða fyrir áhrifum af endurmati|  
|--------------|---------------|------------|-----------------------------|  
|A|Fyrr en endurmatsfærslunúmer|Fyrr en bókunardagsetning endurmats|Nei|  
|B|Fyrr en endurmatsfærslunr.|Jafnt bókunardagsetningu endurmats|Nei|  
|C|Fyrr en endurmatsfærslunr.|Síðar en bókunardagsetning endurmats|Já|  
|D|Síðar en endurmatsfærslu nr.|Fyrr en bókunardagsetning endurmats|Já|  
|Villa|Síðar en endurmatsfærslu nr.|Jafnt bókunardagsetningu endurmats|Já|  
|F|Síðar en endurmatsfærslu nr.|Síðar en bókunardagsetning endurmats|Já|  

### Dæmi  

Eftirfarandi dæmi sýnir endurmat á vöru sem notar FIFO kostnaðarútreikningsaðferðina. Dæmið byggist á eftirfarandi atburðarás:  

1.  Þann 01-01-20, bókið kaup á 6 einingum.  
2.  Þann 02-01-20 er Sala á 1 einingu bókuð.  
3.  Þann 03-01-20 er Sala á 1 einingu bókuð.  
4.  Þann 04-01-20 er Sala á 1 einingu bókuð.  
5.  Þann 03-01-20 reiknar þú út birgðavirði vörunnar og bókar endurmat á kostnaðarverði vörunnar úr ISK 10,00 í ISK 8,00.  
6.  Þann 02-01-20 er Sala á 1 einingu bókuð.  
7.  Þann 03-01-20 er Sala á 1 einingu bókuð.  
8.  Þann 04-01-20 er Sala á 1 einingu bókuð.  
9. Keyrslan Leiðr. kostn. birgðafærslur  **er keyrð** .  

Eftirfarandi tafla sýnir afleiddar virðisfærslur.  

|Aðstæður|Bókunardags.|Tegund færslu|Dagsetning mats|Virt magn|Kostnaðarupphæð (raunverul.)|Birgðafærslunr.|Færslunr.|  
|--------------|------------------|----------------|--------------------|---------------------|----------------------------|---------------------------|---------------|  
||01-01-20|Innkaup|01-01-20|6|60,00|1|1|  
||03-01-20|Endurmat|03-01-20|4|-8,00|1|5|  
|A|02-01-20|Sala|02-01-20|-1|-10,00|2|2|  
|B|03-01-20|Sala|03-01-20|-1|-10,00|3|3|  
|C|04-01-20|Sala|04-01-20|-1|-10,00|4|4|  
||04-01-20|Sala|04-01-20|-1|2,00|4|9|  
|D|02-01-20|Sala|03-01-20|-1|-10,00|5|6|  
||02-01-20|Sala|03-01-20|-1|2,00|5|10|  
|Villa|03-01-20|Sala|03-01-20|-1|-10,00|6|7|  
||03-01-20|Sala|03-01-20|-1|2,00|6|11|  
|F|04-01-20|Sala|04-01-20|-1|-10,00|7|8|  
||04-01-20|Útsala|04-01-20|-1|2.00|7|12|  

## Endurmat VÍV birgða  

Endurúthlutun VÍV birgða felur í sér að íhlutir eru endurmetnar sem skráðar sem VÍV-birgðir.  

Mikilvægt er að hafa reglur sem stýra því hvenær vara er VÍV birgða frá fjárhagslegu sjónarmiði. Í [!INCLUDE[prod_short](includes/prod_short.md)], er til eftirfarandi hefð:  

- Innkeyptur hluti verður hluti af hráefnisbirgðum þegar innkaup eru bókuð sem reikningsfærð.  
- Íhlutur sem keyptur er og undirsettur verður hluti af VÍV birgðum þegar notkun hans er bókuð með framleiðslupöntun.  
- Íhlutur keypts/undirsamsettra helst hluti af VÍV birgðum þar til framleiðslupöntun er reikningsgerð (framleidd vara).  

Hvernig Gildisdagsetning fyrir virðisfærslu notkunar er sett upp fylgir sömu reglum og fyrir færslur sem ekki eru í VÍV. Til að fá frekari upplýsingar er farið að  [ákvarða hvort Endurmat hafi áhrif á minnkun birgða](#determine-whether-revaluation-affects-an-inventory-decrease).  

Hægt er að endurmeta VÍV-birgðir undir eftirfarandi skilyrði:

- Endurmatsdagsetning er á undan bókunardagsetningum samsvarandi birgðafærslna af gerðinni notkun.
- Framleiðslupöntunin hefur ekki verið reikningsfærð.  

> [!CAUTION]  
>  **Birgðamat-VÍV**  -skýrsla sýnir virði bókaðra framleiðslupöntunarfærslna, og gæti verið smá ruglingsleg fyrir ENDURMAT á VÍV-vörum.  

## Endurmeta vörur með Meðalútreikningsaðferð

Aðeins er hægt að endurmeta vörur sem nota aðferðina Meðalkostn. Ef  **reikna á**  *vöru*.

Aðeins er hægt að gera Endurmat í lok þess tímabils sem valið er  **í reitnum Meðalkostnaðartímabil**  á  **síðunni Birgðagrunnur** .

Endurmat hefur ekki áhrif á neikvæðar færslur í líðandi mánuði sem er ástæðan fyrir því að færslum á innleið er ekki komið við.

### Dæmi

Þetta dæmi sýnir hvað gerist þegar reiknað er út birgðavirðið á  **síðunni Endurmatsfærslubók**  vöru. Á síðunni  **Birgðagrunnur**  er vara  **valin í**  reitnum meðalkostnaðartegund  **og**  mánuður  **er valinn í**  svæðinu meðalkostnaðartímabil  **.** 

Eftirfarandi tafla sýnir birgðafærslur fyrir sýnishorn meðalkostnaðarvara, ITEM1.

|Bókunardagsetning|Tegund birgðafærslu|Magn|Kostnaðarupphæð (raunveruleg)|Færslunr.|
|----|----|----|----|----|
25-04-23|Innkaup|5|5.00|1
26-04-23|Innkaup|3|3.00|2
27-04-23|Útsala|-5|--5,00|3
28-04-23|Útsala|-1|--1,00|4
13-05-23|Innkaup|2|20.00|5
17-06-23|Útsala|-6|--22,00|6

Eftirfarandi tafla sýnir niðurstöður þess að keyra skal  **skýrsluna reikna út birgðavirði**  með mismunandi dagsetningardagsetningum.

|Bókunardagsetning|Magn|Athugasemd|
|---|---|-------------|
30-04-23|2|Inniheldur aðeins eftirstandandi magn frá færslu 2. Færsla 1 er að öllu leyti notuð áður en bókunardagsetning og færsla 5 er eftir bókunardagsetningu.
31-05-23|4|Inniheldur eftirstöðvar magns af færslum 2 og 13.
30-06-23|0|Ekkert eftirstöðvar magns á bókunardegi.

Útkoman úr eftirfarandi færslum verður 0, óháð bókunardagsetningunni.

|Bókunardagsetning|Tegund birgðafærslu|Magn|Kostnaðarupphæð (raunveruleg)|Færslunr.|
|----|----|----|----|----|
13-05-23|Innkaup|5|5.00|1
26-04-23|Útsala|-5|5.00|2

## Sjá einnig  

[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)   
[Hönnunarupplýsingar: Aðferð kostnaðarútreiknings](design-details-costing-methods.md)   
[Design Details: Inventory Valuation](design-details-inventory-valuation.md)
[Managing Inventory Costs](finance-manage-inventory-costs.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
