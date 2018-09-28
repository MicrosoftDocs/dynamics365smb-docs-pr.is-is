---
title: "Hönnunarupplýsingar - töfluuppbygging | Microsoft Docs"
description: "Til að skilja hvernig víddafærsla vistun og bókun er endurhannað, það er mikilvægt að skilja töflu uppbyggingu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 900605cd276698e3e6146d18e36ed18363b6c99c
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-table-structure"></a>Hönnunarupplýsingar töfluuppbygging
Til að skilja hvernig víddafærsla vistun og bókun er endurhannað, það er mikilvægt að skilja töflu uppbyggingu.  

## <a name="new-tables"></a>Nýjar töflur  
 Þrír nýjjar töflur hafa verið hannað til að stjórna víddasamstæðufærslum.  

### <a name="table-480-dimension-set-entry"></a>Víddasamstæðufærsla í töflu 480  
 Tafla 480 **Víddasamstæðufærsla** er ný tafla. Ekki er hægt að breyta þessari töflu. Eftir að gögn hafa verið skrifuð í töfluna er ekki hægt að eyða þeim eða breyta. Eyðing ganga útheimtir samanburð við öll tilvik víddasamstæðukennisins í öllum gagnagrunninum, þar á meðal yfirlausnum.  

|Nr. reits|Heiti reits|Gagnagerð|Athugasemd|  
|---------------|----------------|---------------|-------------|  
|1|**Auðkenni**|Heiltala|>0.0 er f´ratekið fyrir tóma víddarsamstæðuna. Tilvísunarreitur 3 í töflu 481.|  
|2|**Víddarkóti**|Kóði 20|Töflutengsl við töflu 348|  
|3|**Gildiskóti víddar**|Kóði 20|Töflutengsl við töflu 349.|  
|4|**Víddargildi**|Heiltala|Tilvísanareitur 12 í töflu 349. Hann er aukalykill sem notaður er þegar farið er yfir töflu 481.|  
|5|**Heiti víddar**|Texti 30|CalcField. Uppfletting í töflu 348|  
|6|**Nafn víddagildis**|Texti 30|CalcField. Uppfletting í töflu 349|  

#### <a name="table-481-dimension-set-tree-node"></a>Víddasamstæðutrjáhnútur í töflu 481  
 Tafla 481 **Víddasamstæðutrjáhnútur** er ný tafla. Ekki er hægt að breyta þessari töflu. Taflan er notuð til að leita að víddasamstæðu. Ef víddasamstæðan finnst ekki er ný samstæða búin til.  

|Nr. reits|Heiti reits|Gagnagerð|Athugasemd|  
|---------------|----------------|---------------|-------------|  
|1|**Auðkenni víddasamstæðu**|Heiltala|0 fyrir efsta tengipunkt.|  
|2|**Víddargildi**|Heiltala|Töflutengsl við reit 12 í töflu 349.|  
|3|**Auðkenni víddasamstæðu**|Heiltala|AutoIncrement. Notað í reitinn 1 í töflu 480.|  
|4|**Í notkun**|Boole|Ósatt ef ekki í notkun|  

##### <a name="table-482-reclas-dimension-set-buffer"></a>Endurflokkunarbiðsvæði víddasamstæðu í töflu 482  
 Tafla 482 **Endurflokkunarbiðsvæði víddasamstæðu** er ný tafla. Taflan er notuð til að breyta auðkenni víddasamstæðunnar. Þetta er nauðsynlegt við breytingar á víddargildiskóða og nýjum víddargildiskóða, til dæmis, í töflunni **Endurflokkunarbók vöru**.  

|Nr. reits|Heiti reits|Gagnagerð|Athugasemd|  
|---------------|----------------|---------------|-------------|  
|1|**Víddarkóti**|Kóði 20|Töflutengsl við töflu 348|  
|2|**Gildiskóti víddar**|Kóði 20|Töflutengsl við töflu 349.|  
|3|**Víddargildi**|Heiltala|Tilvísanareitur 12 í töflu 349.|  
|4|**Nýr víddargildiskóti**|Kóði 20|Töflutengsl við töflu 349.|  
|5|**Nýtt auðkenni víddargildis**|Heiltala|Tilvísanareitur 12 í töflu 349.|  
|6|**Heiti víddar**|Texti 30|CalcField. Uppfletting í töflu 348|  
|7|**Nafn víddagildis**|Texti 30|CalcField. Uppfletting í töflu 349|  
|8|**Nýtt nafn víddagildis**|Texti 30|CalcField. Uppfletting í töflu 349|  

## <a name="modified-tables"></a>Töflur sem breytt hefur verið  
 Öllum færslu- og fjárhagstöflum hefur verið breytt til að stjórna víddasamstæðufærslum.  

### <a name="changes-to-transaction-and-budget-tables"></a>Breytingar á færslu og fjárhagsáætlunartöflum  
 Nýjum reit hefur verið bætt við allar færslur og fjárhagstöflur.  

|Nr. reits|Heiti reits|Gagnagerð|Athugasemd|  
|---------------|----------------|---------------|-------------|  
|480|**Auðkenni víddasamstæðu**|Heiltala|Tilvísanareitur 1 í töflu 480.|  

#### <a name="changes-to-table-83-item-journal-line"></a>Breytingar á töflu 83 birgðabókarlínu  
 Tvö nýir reitir hafa verið bætt við töflu 83 **Birgðabókarlína**  

|Nr. reits|Heiti reits|Gagnagerð|Athugasemd|  
|---------------|----------------|---------------|-------------|  
|480|**Auðkenni víddasamstæðu**|Heiltala|Tilvísanareitur 1 í töflu 480.|  
|481|**Nýtt auðkenni víddasamstæðu**|Heiltala|Tilvísanareitur 1 í töflu 480.|  

##### <a name="changes-to-table-349-dimension-value"></a>Breytingar á töflu 349 víddargildum  
 Nýjum reit hefur verið bætt við töflu 349 **Víddargildi**.  

|Nr. reits|Heiti reits|Gagnagerð|Athugasemd|  
|---------------|----------------|---------------|-------------|  
|12|**Víddargildi**|Heiltala|AutoIncrement. Notað fyrir tilvísanir í töflu 480 og töflu 481.|  

###### <a name="tables-that-get-new-field-480-dimension-set-id"></a>Töflur sem fá nýtt víddasamstæðukenni reitur 480  
 Nýjum reit, 480 **Auðkenni víddasamstæðu**, hefur verið bætt við eftirfarandi töflur. Fyrir töflurnar  sem vista bókuð gögn gefur reiturinn aðeins upp óbreytanlegt yfirlit yfir víddir, sem merkt er sem Kafa niður. Fyrir töflur sem vista vinnuskjöl er hægt að breyta reitnum. Biðminnistöflur í innri notkun þurfa ekki breytanlega eða óbreytanlega eiginleika.  

 Ekki er hægt að breyta reitnum 480 í eftirfarandi töflum.  

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

 Hægt er að breyta reitnum 480 í eftirfarandi töflum.  

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

 Reitnum 480 hefur verið bætt við eftirfarandi biðminnistöflur.  

|Nr. töflu.|Töfluheiti|  
|---------------|----------------|  
|49|**Bókunarbiðminni reikninga**|  
|212|**Biðminni verkbókunar**|  
|372|**Biðminni greiðslu**|  
|382|**Biðminni VL-færslu**|  
|461|**Biðminni reikn.línu fyrirframgr.**|  
|5637|**Fjárhagsbókunarbiðminni eigna**|  
|7136|**Biðminni birgðaáætlunar**|  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingarn: Færslur víddarsamstæða](design-details-dimension-set-entries.md)   
 [Yfirlit yfir víddasamstæðufærslur](design-details-dimension-set-entries-overview.md)   
 [Hönnunarupplýsingar Leitað að víddarsamsetningum](design-details-searching-for-dimension-combinations.md)   
 [Hönnunarupplýsingar: Codeunit 408 víddarstjórnun](design-details-codeunit-408-dimension-management.md)   
 [Hönnunarupplýsingar: Kóðadæmi um breytt mynstur í Breytingar](design-details-code-examples-of-changed-patterns-in-modifications.md)

