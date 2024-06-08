---
title: Hönnunarupplýsingar - Endurmat
description: Hægt er að endurmeta birgðir á grundvelli virðisgrundvallar sem endurspeglar nákvæmast birgðavirði.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 07/07/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="design-details-revaluation"></a>Hönnunarupplýsingar: Endurmat

Hægt er að endurmeta birgðir á grundvelli virðisgrundvallar sem endurspeglar nákvæmast birgðavirði. Einnig er hægt að bakfæra endurmat til að uppfæra kostnað seldra vara (KSV) vara sem þegar hafa verið seldar. Einnig er hægt að endurmeta vörur sem nota aðferð staðlaðs kostnaðarútreiknings og eru ekki reikningsfærðar að fullu.  

Í [!INCLUDE[prod_short](includes/prod_short.md)] er eftirfarandi sveigjanleiki studdur varðandi endurmat:  

- Endurmetanlegt magn er hægt að reikna fyrir allar dagsetningar, líka aftur í tímann.  
- Fyrir vörur sem nota kostnaðarútreikninginn Staðlað eru áætlaðar kostnaðarfærslur hafðar með í endurmatinu.  
- Birgðaminnkanir sem verða fyrir áhrifum af endurmati eru greindar.  

## <a name="calculate-the-revaluable-quantity"></a>Reikna út endurmetanlegt magn

Magnið sem hægt er að endurmeta eru eftirstöðvar sem eru tiltækar á tilteknum degi. Magnið er samtala fullkomlega reikningsfærðra birgðafærslna sem bókaðar eru á eða fyrir endurmatsdagsetninguna.  

> [!NOTE]  
>  Vörur sem nota hefðbundna aðferð kostnaðarútreiknings eru meðhöndlaðar á annan hátt við reikningu endurmetanlegs magns fyrir vöru, birgðageymslu og afbrigði. Magn og virði birgðahöfuðbókarfærslna sem ekki hafa verið að fullu reikningsfærðar eru teknar með í endurverðmetanlega magninu.  

Eftir bókun endurmats er hægt að bóka birgðaaukningu eða -minnkun með bókunardagsetningu sem er á eftir bókunardagsetningu endurmats. Hins vegar hefur endurmat ekki áhrif á þetta magn. Til að halda jafnvægi á birgðum, aðeins upprunalega endurmetanlegt magn er talið.  

Þar sem hægt er að endurmeta á hvaða degi sem er verður að vera venjur þegar vara er tekin sem hluti af birgðum. Til dæmis hvenær vara er í birgðum og hvenær varan er verk í vinnslu (VÍV).  

### <a name="example"></a>Dæmi

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

## <a name="expected-cost-in-revaluation"></a>Áætlaður kostnaður í endurmati

Magnið sem hægt er að endurmeta er summa magnsins fyrir reikningsfærðar birgðafærslur sem bókaðar voru á eða fyrir endurmatsdagsetninguna. Þegar einhverjar vörur eru mótteknar eða afhentar en ekki reikningsfærðar er ekki hægt að reikna birgðavirði þeirra. Vörur sem nota aðferð staðlaðs kostnaðarútreiknings eru ekki takmarkaðar á þennan hátt.  

> [!NOTE]  
>  Önnur gerð áætlaðs kostnaðar sem hægt er að endurmeta eru VÍV-birgðir, eftir tilteknum reglum. Frekari upplýsingar eru í [VÍV endurmat á birgðum](design-details-revaluation.md#wip-inventory-revaluation).  

Þegar endurmetanlegt magn er reiknað fyrir vörur sem nota staðlaða aðferð við útreikning kostnaðar eru í útreikningnum birgðafærslur sem eru ekki reikningsfærðar að fullu. Þessar færslur eru endurmetnar þegar endurmatið er bókað. Þegar endurmetna færslan er reikningsfærð eru eftirfarandi virðisfærslur stofnaðar:  

- Vanaleg virðisdagsetning reikningsins með færslugerðinni **Beinn kostnaður**. Kostnaðurupphæð á þessari færslu er bein kostnaður frá upptökum línu.  
- Virðisfærsla með færslugerðinni **Frávik**. Þessi færsla skráir muninn milli reikningsfærðs kostnaðar og endurmetins staðalkostnaðar.  
- Virðisfærsla með færslugerðinni **Endurmat**. Þessi færsla sýnir bakfærslu á endurmati væntanlegs kostnaðar.

### <a name="example-1"></a>Dæmi

Eftirfarandi dæmi er byggt á framleiðslu keðjunnar í fyrra dæmi. Þetta dæmi sýnir hvernig færslurnar þrjár eru stofnaðar, byggt á eftirfarandi dæmi:  

1.  Keyptir tenglar eru bókaðir sem mótteknir með 2,00 SGM kostnaðarverð.  
2.  Bókuð er endurmat á tenglunum með nýtt kostnaðarverð upp á SGM 3,00 og staðlað kostnaðarverð uppfært í SGM 3,00.  
3.  Upphafleg innkaup keðjutenglanna eru bókuð sem reikningsfærð sem stofnar eftirfarandi virðisfærslur:  

    1.  Reikningsfærð virðisfærsla með færslugerð **Beinn kostnaður**.  
    2.  Virðisfærsla með færslugerð **Endurmat** til að skrá bakfærslu endurmats áætlaðs kostnaðar.  
    3.  Virðisfærsla með færslugerðinni Frávik, skráir mismun milli reikningsfærðs kostnaðar og endurmetins staðalkostnaðar.  

Eftirfarandi tafla sýnir niðurstöðurnar.  

|Skref|Bókunardagsetning|Færslugerð|Reikningsdagur innlausnarvirðis|Kostnaðarupphæð (væntanl.)|Kostnaðarupphæð (raunverul.)|Birgðafærslunr.|Færslunr.|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|01-15-20|Beinn kostnaður|01-15-20|300,00|0,00|1|1|  
|2.|01-20-20|Endurmat|01-20-20|150,00|0,00|1|2|  
|3.a.|01-15-20|Beinn kostnaður|01-15-20|-300,00|0,00|1|3|  
|3.b.|01-15-20|Endurmat|01-20-20|-150,00|0,00|1|4|  
|3.c.|01-15-20|Frávik|01-15-20|0.00|450.00|1|5|  

## <a name="determine-whether-revaluation-affects-an-inventory-decrease"></a>Ákvarða hvort endurmat hefur áhrif á birgðaminnkun

Nota dagsetningu bókunar eða endurmats til að ákvarða hvort birgðaminnkun verður fyrir áhrifum af endurmati.  

Eftirfarandi tafla sýnir viðmið sem notuð eru fyrir vöru sem ekki notar meðalkostnaðarútreikningsaðferðina.  

|Aðstæður|Færslunr.|Tímasetning|Verða fyrir áhrifum af endurmati|  
|--------------|---------------|------------|-----------------------------|  
|A|Fyrr en endurmatsfærslunúmer|Fyrr en bókunardagsetning endurmats|Nei|  
|B|Fyrr en endurmatsfærslunr.|Jafnt bókunardagsetningu endurmats|Nei|  
|C|Fyrr en endurmatsfærslunr.|Síðar en bókunardagsetning endurmats|Já|  
|D|Síðar en endurmatsfærslu nr.|Fyrr en bókunardagsetning endurmats|Já|  
|Villa|Síðar en endurmatsfærslu nr.|Jafnt bókunardagsetningu endurmats|Já|  
|F|Síðar en endurmatsfærslu nr.|Síðar en bókunardagsetning endurmats|Já|  

### <a name="example-2"></a>Dæmi

Eftirfarandi dæmi sýnir endurmat á vöru sem notar FIFO-kostnaðarútreikningsaðferðina. Dæmið byggir á eftirfarandi dæmi:  

1.  01-01-20 er keypt upp á 6 einingar.  
2.  02-01-20 er bókuð sala á 1 einingu.  
3.  03-01-20 er bókuð sala á 1 einingu.  
4.  04-01-20 er bókuð sala á 1 einingu.  
5.  03-01-20 er birgðavirði vörunnar reiknað út og endurmat á kostnaðarverði vörunnar bókað úr SGM 10,00 í SGM 8,00.  
6.  02-01-20 er bókuð sala á 1 einingu.  
7.  03-01-20 er bókuð sala á 1 einingu.  
8.  04-01-20 er bókuð sala á 1 einingu.  
9. Keyrslan **Leiðr. kostnað - Birgðafærslur er keyrð** .  

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

## <a name="wip-inventory-revaluation"></a>VÍV-endurmat birgða

Endurmat VÍV-birgða felur í sér að endurmeta íhluti sem eru skráðir sem VÍV-birgðir.  

Mikilvægt er að hafa ráðstafanir sem stýra því hvenær vara er VÍV-birgðir frá fjárhagslegu sjónarhóli. Í [!INCLUDE[prod_short](includes/prod_short.md)], er til eftirfarandi hefð:  

- Keyptur íhlutur verður hluti hráefnisbirgðanna þegar innkaup eru bókuð sem reikningsfærð.  
- Keyptur/undirsamsettur íhlutur verður hluti VÍV-birgða þegar notkun hennar er bókuð með framleiðslupöntun.  
- Keyptur/undirsamsettur íhlutur er hluti VÍV-birgða þar til framleiðslupöntun er reikningsfærð (framleidd vara).  

Hvernig matsdagsetning virðisfærslu notkunar er stillt fer eftir sömu reglum og fyrir birgðir sem eru ekki í gangi. Nánari upplýsingar eru notaðar til að ákvarða [hvort endurmat hafi áhrif á birgðaminnkun](#determine-whether-revaluation-affects-an-inventory-decrease).  

Hægt er að endurmeta VÍV-birgðir við eftirfarandi skilyrði:

- Endurmatsdagsetningin er á undan bókunardagsetningum samsvarandi birgðafærslna af gerðinni Notkun.
- Framleiðslupöntunin hefur ekki verið reikningsfærð.  

> [!CAUTION]  
> Skýrslan **Birgðir - Verðmætamat - VÍV** sýnir virði bókaðra framleiðslupantanafærslna og gæti verið smá ruglingur fyrir endurmetnar VÍV-vörur.  

## <a name="revaluate-items-with-the-average-costing-method"></a>Endurmeta vörur með aðferðinni Meðalkostnaður

Aðeins er hægt að endurmeta vörur sem nota meðalkostnaðarútreikning ef **Reikna á** er *Vara*.

Aðeins er hægt að endurmeta í lok tímabilsins sem valið er í reitnum **Meðalinnkaupaverðstímabil** á síðunni **Birgðagrunnur** .

Endurmat hefur ekki áhrif á neikvæðar færslur í líðandi mánuði, þess vegna eru færslur á innleið að fullu ekki heldur teknar með.

### <a name="example-3"></a>Dæmi

Þetta dæmi sýnir hvað gerist þegar birgðavirði er reiknað á síðunni **Endurmatsbók** vöru. Á **síðunni**  Birgðagrunnur **er Vara** valin í reitnum **Útreikn.teg** . meðalinnkaupsverðs og **Mánuður** er valinn í reitnum **Tímabil** meðalinnkaupsverðs.

Eftirfarandi tafla sýnir birgðafærslur fyrir sýnishorn meðalinnkaupaverðsvöru, VÖRU1.

|Bókunardagsetning|Tegund birgðafærslu|Magn|Kostnaðarupphæð (raunveruleg)|Færslunr.|
|----|----|----|----|----|
25-04-23|Innkaup|5|5.00|1
26-04-23|Innkaup|3|3.00|2
27-04-23|Útsala|-5|-5.00|3
28-04-23|Útsala|-1|-1.00|4
13-05-23|Innkaup|2|20.00|5
17-06-23|Útsala|-6|-22.00|6

Eftirfarandi tafla sýnir niðurstöður keyrslu skýrslunnar **Reikna út birgðavirði** með mismunandi dagsetningum.

|Bókunardagsetning|Magn|Athugasemd|
|---|---|-------------|
30-04-23|2|Tekur aðeins með það magn sem eftir er úr færslu 2. Færsla 1 er að fullu jöfnuð fyrir bókunardagsetninguna og færsla 5 er eftir bókunardagsetninguna.
31-05-23|4|Tekur með eftirstöðvar magns úr færslum 2 og 13.
30-06-23|0|Ekkert eftirstöðvar magns á bókunardagsetningu.

Niðurstaða eftirfarandi færslna verður 0, óháð bókunardagsetningunni.

|Bókunardagsetning|Tegund birgðafærslu|Magn|Kostnaðarupphæð (raunveruleg)|Færslunr.|
|----|----|----|----|----|
13-05-23|Innkaup|5|5.00|1
26-04-23|Útsala|-5|5.00|2

## <a name="see-also"></a>Sjá einnig

[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)   
[Hönnunarupplýsingar: Aðferð kostnaðarútreiknings](design-details-costing-methods.md)   
[Upplýsingar um hönnun: Birgðir - Verðmætamat](design-details-inventory-valuation.md)
[stjórnun birgðakostnaðar](finance-manage-inventory-costs.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
