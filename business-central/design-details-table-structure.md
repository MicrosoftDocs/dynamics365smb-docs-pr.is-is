---
title: Hönnunarupplýsingar - töfluuppbygging | Microsoft Docs
description: 'Til að skilja hvernig víddafærsla vistun og bókun er endurhannað, það er mikilvægt að skilja töflu uppbyggingu.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Hönnunarupplýsingar töfluuppbygging
Til að skilja hvernig víddafærslur eru vistaðar og bókaðar er mikilvægt að skilja töfluuppbyggingu.  

## Víddasamstæðufærsla í töflu 480  
Ekki er hægt að breyta þessari töflu. Eftir að gögn hafa verið skrifuð í töfluna er ekki hægt að eyða þeim eða breyta.

|Nr. reits|Heiti reits|Gerð gagna|Athugasemd|  
|---------------|----------------|---------------|-------------|  
|1|**Auðkenni**|Heiltala|>0.0 er f´ratekið fyrir tóma víddarsamstæðuna. Tilvísunarreitur 3 í töflu 481.|  
|2|**Víddarkóti**|Kóði 20|Töflutengsl við töflu 348|  
|3|**Gildiskóti víddar**|Kóði 20|Töflutengsl við töflu 349.|  
|4|**Víddargildi**|Heiltala|Tilvísanareitur 12 í töflu 349. Hann er aukalykill sem notaður er þegar farið er yfir töflu 481.|  
|5|**Heiti víddar**|Texti 30|CalcField. Uppfletting í töflu 348|  
|6|**Nafn víddagildis**|Texti 30|CalcField. Uppfletting í töflu 349|  

## Víddasamstæðutrjáhnútur í töflu 481  
Ekki er hægt að breyta þessari töflu. Taflan er notuð til að leita að víddasamstæðu. Ef víddasamstæðan finnst ekki er ný samstæða búin til.  

|Nr. reits|Heiti reits|Gagnagerð|Athugasemd|  
|---------------|----------------|---------------|-------------|  
|1|**Auðkenni víddasamstæðu**|Heiltala|0 fyrir efsta tengipunkt.|  
|2|**Víddargildi**|Heiltala|Töflutengsl við reit 12 í töflu 349.|  
|3|**Auðkenni víddasamstæðu**|Heiltala|AutoIncrement. Notað í reitinn 1 í töflu 480.|  
|4|**Í notkun**|Boole|Ósatt ef ekki í notkun|  

## Endurflokkunarbiðsvæði víddasamstæðu í töflu 482  
Þessi tafla er notuð þegar þú breytir víddargildiskóða, til dæmis á færslu fjárhagsfærslu með því að nota síðuna **Endurflokkunarbók vöru**.  

|Nr. reits|Heiti reits|Gerð gagna|Athugasemd|  
|---------------|----------------|---------------|-------------|  
|1|**Víddarkóti**|Kóði 20|Töflutengsl við töflu 348|  
|2|**Gildiskóti víddar**|Kóði 20|Töflutengsl við töflu 349.|  
|3|**Víddargildi**|Heiltala|Tilvísanareitur 12 í töflu 349.|  
|4|**Nýr víddargildiskóti**|Kóði 20|Töflutengsl við töflu 349.|  
|5|**Nýtt auðkenni víddargildis**|Heiltala|Tilvísanareitur 12 í töflu 349.|  
|6|**Heiti víddar**|Texti 30|CalcField. Uppfletting í töflu 348|  
|7|**Nafn víddagildis**|Texti 30|CalcField. Uppfletting í töflu 349|  
|8|**Nýtt nafn víddagildis**|Texti 30|CalcField. Uppfletting í töflu 349.|  

## Færslu- og fjárhagsáætlunartöflur  
Ásamt öðrum víddarreitum í töflunni, er þessi reitur mikilvægur:  

|Nr. reits|Heiti reits|Gerð gagna|Athugasemd|  
|---------------|----------------|---------------|-------------|  
|480|**Auðkenni víddasamstæðu**|Heiltala|Tilvísanareitur 1 í töflu 480.|  

### Tafla 83, birgðabókarlína  
Ásamt öðrum víddarreitum í töflunni, er þessir reitir mikilvægir.  

|Nr. reits|Heiti reits|Gerð gagna|Athugasemd|  
|---------------|----------------|---------------|-------------|  
|480|**Auðkenni víddasamstæðu**|Heiltala|Tilvísanareitur 1 í töflu 480.|  
|481|**Nýtt auðkenni víddasamstæðu**|Heiltala|Tilvísanareitur 1 í töflu 480.|  

### Tafa 349, víddargildi  
Ásamt öðrum víddarreitum í töflunni, er þessir reitir mikilvægir.  

|Nr. reits|Heiti reits|Gerð gagna|Athugasemd|  
|---------------|----------------|---------------|-------------|  
|12|**Víddargildi**|Heiltala|AutoIncrement. Notað fyrir tilvísanir í töflu 480 og töflu 481.|  

### Töflur sem innihalda reit fyrir auðkenni víddasamstæðu
 Reiturinn (480) **Auðkenni víddasamstæðu** er til í eftirfarandi töflum. Fyrir töflurnar  sem vista bókuð gögn gefur reiturinn aðeins upp óbreytanlegt yfirlit yfir víddir, sem merkt er sem Kafa niður. Fyrir töflur sem vista vinnuskjöl er hægt að breyta reitnum. Biðminnistöflur í innri notkun þurfa ekki breytanlega eða óbreytanlega eiginleika.  

 Ekki er hægt að breyta reit 480 í eftirfarandi töflum.  

|Nr. töflu.|Töfluheiti|  
|---------------|----------------|  
|17|**Fjárhagsfærsla**|  
|21|**Viðskm.færsla**|  
|25|**Lánardr.færsla**|  
|32|**Birgðafærsla**|  
|110|**Söluafhendingarhaus**|  
|111|**Söluafhendingarlína**|  
|112|**Sölureikningshaus**|  
|113|**Sölureikningslína**|  
|114|**Sölukreditreikningshaus**|  
|115|**Sölukreditreikningslína**|  
|120|**Innk.móttökuhaus**|  
|121|**Innk.móttökulína**|  
|122|**Innk.reikningshaus**|  
|123|**Innk.reikn.lína**|  
|124|**Innk.kreditreikningshaus**|  
|125|**Innk.kreditreikningslína**|  
|169|**Verkfærsla**|  
|203|**Forðafærsla**|  
|271|**Bankareikningsfærsla**|  
|281|**Raunbirgðafærsla**|  
|297|**Haus sends innheimtubréfs**|  
|304|**Sendur vaxtareikningshaus**|  
|5107|**Söluhaus - Skjalasafn**|  
|5108|**Sölulína - Skjalasafn**|  
|5109|**Skjalasafn - Innkaupahaus**|  
|5110|**Innkaupalína - Skjalasafn**|  
|5601|**Eignafærsla**|  
|5625|**Viðhaldsbókarfærsla**|  
|5629|**Vátryggingarsviðsfærsla**|  
|5744|**Millifærsluafhendingarhaus**|  
|5745|**Millifærsluafhendingarlína**|  
|5746|**Millifærslumóttökuhaus**|  
|5747|**Millifærslumóttökulína**|  
|5802|**Virðisfærsla**|  
|5832|**Afkastagetufærsla**|  
|5907|**Þjónustufærsla**|  
|5908|**Þjónustuhaus**|  
|5933|**Bókunarbiðminni þjón.pantana**|  
|5970|**Skráður haus þjónustusamnings**|  
|5990|**Haus þjónustuafhendingar**|  
|5991|**Þjónustuafhendingarlína**|  
|5992|**Haus þjónustureiknings**|  
|5993|**Þjónustureikningslína**|  
|5994|**Kreditreikn.haus þjónustu**|  
|5995|**Kreditreikn.lína þjónustu**|  
|6650|**Skilaafhendingarhaus**|  
|6651|**Skilaafhendingarlína**|  
|6660|**Vöruskilamóttökuhaus**|  
|6661|**Skilamóttökuhaus**|  

Hægt er að breyta reit 480 í eftirfarandi töflum.  

|Nr. töflu.|Töfluheiti|  
|---------------|----------------|  
|36|**Söluhaus**|  
|37|**Sölulína**|  
|38|**Innkaupahaus**|  
|39|**Innkaupalína**|  
|81|**Fh.færslubókarlína**|  
|83|**Birgðabókarlína**|  
|89|**Uppskr.bókarlína**|  
|96|**Fjárhagsáætl.færsla**|  
|207|**Forðabókarlína**|  
|210|**Verkbókarlína**|  
|221|**Færslubók úthlutunar**|  
|246|**Innkaupatillögulína**|  
|295|**Haus innheimtubréfs**|  
|302|**Vaxtareikningshaus**|  
|5405|**Framleiðslupöntun**|  
|5406|**Framl.pöntunarlína**|  
|5407|**Framl.pöntunaríhlutur**|  
|5615|**Eignaúthlutun**|  
|5621|**Eignabókarlína**|  
|5635|**Vátryggingabókarlína**|  
|5740|**Millifærsluhaus**|  
|5741|**Millifærslulína**|  
|5900|**Þjónustuhaus**|  
|5901|**Þjónustuvörulína**|  
|5902|**Þjónustulína**|  
|5965|**Haus þjónustusamnings**|  
|5997|**Stöðluð þjónustulína**|  
|7134|**Birgðaáætlunarfærsla**|  
|99000829|**Áætlunaríhlutur**|  

Reitur 480 er til í eftirfarandi biðminnistöflum.  

|Nr. töflu.|Töfluheiti|  
|---------------|----------------|  
|49|**Bókunarbiðminni reikninga**|  
|212|**Biðminni verkbókunar**|  
|372|**Biðminni greiðslu**|  
|382|**Biðminni VL-færslu**|  
|461|**Biðminni reikn.línu fyrirframgr.**|  
|5637|**Fjárhagsbókunarbiðminni eigna**|  
|7136|**Biðminni birgðaáætlunar**|  

## Sjá einnig

[Yfirlit yfir víddasamstæðufærslur](design-details-dimension-set-entries-overview.md)  
[Hönnunarupplýsingar Leitað að víddarsamsetningum](design-details-searching-for-dimension-combinations.md)   
