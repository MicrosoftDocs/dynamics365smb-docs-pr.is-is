---
title: Hönnunarupplýsingar - Vörujöfnun | Microsoft Docs
description: Þetta efnisatriði lýsir því hvar birgðamagn og virði eru skráð þegar þú bókar birgðafærslu.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, items, ledger entries, posting, inventory'
ms.date: 06/08/2021
ms.author: bholtorf
---
# <a name="design-details-item-application"></a>Hönnunarupplýsingar: umsókn vöru

Þegar þú bókar birgðafærslu er bókunarmagnið skráð í birgðabókarfærslurnar en bókun virðis í virðisfærslur. Nánari upplýsingar, sjá [Upplýsingar um hönnun: Birgðabókun](design-details-inventory-posting.md)  

Að auki vörujöfnun er gert til að tengja kostnað viðtakanda kostnaðar við kostnaðaruppruna il að gefa upp kostnaðarframsendingu samkvæmt kostnaðaraðferð. Nánari upplýsingar eru í [Upplýsingar um hönnun: Kostnaðarútreikningar](design-details-costing-methods.md).  

[!INCLUDE[prod_short](includes/prod_short.md)] gerir tvær tegundir af vörujöfnun.  

|Jöfnunargerð|Description|  
|----------------------|---------------------------------------|  
|Magnjöfnun|Stofnað fyrir allar birgðafærslur|  
|Jöfnun kostnaðar|Stofnað fyrir færslur á innleið ásamt magnjöfnun sem afleiðing af samskiptum notaenda í sérstökum ferlum.|  

Hægt er að færa vörunotkun í reitinn á eftirfarandi hátt:  

|Aðferð|Description|Jöfnunargerð|  
|------------|---------------------------------------|----------------------|  
|Sjálfvirkt|Á sér stað sem framsending almenns kostnaðar samkvæmt aðferð kostnaðarútreiknings.|Magnjöfnun|  
|Fast|Gerðar af notanda þegar:<br /><br /> -   Vinnsla skilar<br />-   Bókun leiðréttinga<br />-   Ógildir magnbókun<br />-   Búa til beina sendingar **Athugið:** Hægt er að nota fasta jöfnun annað hvort handvirkt með því að slá inn færslunúmer í reitinn **Jafna frá birgðafærslu** eða með því að nota aðgerð, svo sem **Sækja bókaðar fylgiskjalalínur til að bakfæra**.|Magnjöfnun<br /><br /> Kostnaðarjöfnun **Athugið:**  Kostnaðarjöfnun gerist aðeins í færslum á innleið þar sem reiturinn **Jafna frá birgðafærslu** er fylltur út til að stofna fasta jöfnun. Sjá næstu töflu.|  

Hvort magnjöfnun eða kostnaðarjöfnun er gerð fer eftir stefnu birgðafærslunnar og hvort vörujöfnunin er gerð sjálfvirkt eða fast, í tengslum við sértæk ferli.  

Eftirfarandi tafla sýnir, byggt á meginjöfnunarreitum í birgðafærslulínum, hvernig kostnaður flæðir samkvæmt átt færslunnar. Það sýnir einnig hvenær og hvers vegna vörujöfnun umsókn er af taginu magni eða kostnað.  

|-|Jafna í birgðafærslu|Jafna frá birgðafærslu|  
|-|--------------------------------|----------------------------------|  
|Jöfnun fyrir færslu á útleið|Færslan á útleið sækir kostnaðinn úr opnu færslunni á innleið.<br /><br /> **Magnjöfnun**|Ekki stutt|  
|Jöfnun fyrir færslu á innleið|Færslan á innleið flytur kostnaðinn inn í opnu færsluna á útleið.<br /><br /> Færslan á innleið er uppruni kostnaðar.<br /><br /> **Magnjöfnun**|Færslan á innleið sækir kostnaðinn úr færslunni á útleið. **Athugið:**  Við gerð á þessari föstu jöfnun, er færsla á innleið meðhöndluð sem vöruskil. Því mun færsla á útleið sem var notuð vera opin. <br /><br /> Færslan á innleið er EKKI uppruni kostnaðar.<br /><br /> **Jöfnun kostnaðar**|  

> [!IMPORTANT]  
> Söluskil eru EKKI talin kostnaðaruppruni við fasta jöfnun.  
>
> Sölufærslur eru áfram opnar þar til raunveruleg tilföng eru bókuð.  

Vörufærsla skrári eftirfarandi upplýsinagr.  

|Svæði|Description|  
|---------------------------------|---------------------------------------|  
|**Birgðafærslunr.**|Númer birgðafærslunnar fyrir þá hreyfingu sem þessi jöfnunarfærsla er stofnuð fyrir.|  
|**Birgðafærslunr. vöru á innleið**|Birgðafærslunúmer birgðaaukningarinnar sem færslan á að vera tengd við, ef það á við.|  
|**Birgðafærslunr. vöru á útleið**|Birgðafærslunúmer birgðaminnkunarinnar sem færslan á að vera tengd við, ef það á við.|  
|**Magn**|Það magn sem verið er að jafna.|  
|**Bókunardags.**|Bókunardagsetning færslunnar.|  

## <a name="inventory-increase"></a>Birgðaaukning
Þegar birgðaaukning er bókuð er einföld vörujöfnunarfærsla stofnuð án jöfnunar við færsla á útleið.  

### <a name="example"></a>Dæmi
Eftirfarandi tafla sýnir vörujöfnunarfærslu sem var búin til innkaupakvittun upp á 10 einingar var bókuð.  

|Bókunardagsetning|Birgðafærslunr. vöru á innleið|Birgðafærslunr. vöru á útleið|Magn|Birgðafærslunr.|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  

## <a name="inventory-decrease"></a>Birgðaminnkun
Þegar birgðaminnkun er bókuð er vörujöfnunarfærsla stofnuð til að tengja birgðaminnkunina við birgðaaukningu. Þessi tengill er búinn til með því að nota aðferð kostnaðarútreiknings á vörunni til leiðsagnar. Fyrir vörur sem nota kostnaðarútreikninginn FIFO (fyrst inn - fyrst út), Staðlað og Meðaltal er tengingin byggð á fyrst inn, fyrst út reglunni. Birgðaminnkuninni er jafnað á birgðaaukninguna miðað við síðustu bókunardagsetningu. Fyrir vörur sem nota kostnaðarútreikninginn LIFO (síðast inn - fyrst út) er tengingin byggð á síðast inn - fyrst út reglunni. Birgðaminnkuninni er jafnað á birgðaaukninguna miðað við síðustu bókunardagsetningu.  

Í töflunni **Birgðafærsla** sýnir reiturinn **Eftirstandandi magn** þá upphæð sem hefur enn ekki verið úthlutað. Ef magn eftirstöðva er meira en 0 er gátreiturinn **Opna** valinn.  

### <a name="example-1"></a>Dæmi
Eftirfarandi dæmi sýnir vörujöfnunarfærslu sem var stofnuð þegar bókuð var söluafhending fimm eininga af vörum sem mótteknar voru í síðasta dæmi. Fyrsta vörujöfnunarfærslan er kvittun. Önnur jöfnunarfærslan er söluafhending.  

Eftirfarandi tafla sýnir tvær vörujöfnunarfærslur sem koma til bæði vegna birgðaaukningar og birgðaminnkunar.  

|Bókunardagsetning|Birgðafærslunr. vöru á innleið|Birgðafærslunr. vöru á útleið|Magn|Birgðafærslunr.|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  
|01-03-20|1|2|-5|2|  

## <a name="fixed-application"></a>Fastar jafnanir
Föst jöfnun er gerð þegar tekið er fram að kostnaður birgðaaukningar ætti að eiga við um tiltekna birgðaminnkun eða öfugt. Fast jöfnunin hefur áhrif á eftirstöðvamagn færslnanna en fasta jöfnunin hefur líka þau áhrif að snúa nákvæmlega við kostnaði upprunalegu færslunnar sem verið er að jafna við (eða frá).  

Til að gera fasta jöfnun notarðu **Jöfnun til birgðafærslu** reit eða **Jöfnun frá birgðafærslu** reit í skjalalínum að tilgreina birgðafærslu sem þú vilt að færslulínu til að eiga við, eða frá. Til dæmis er hægt að gera fasta jöfnun ef búa á til kostnaðarjöfnun sem tilgreinir að söluskil skuli gilda um tiltekna sölusendingu til að bakfæra kostnað af sölusendingunni. Í þessu tilfelli, [!INCLUDE[prod_short](includes/prod_short.md)] hundsar aðferð kostnaðarútreiknings og beitir birgðaminnkun eða hækkun fyrir vöruskil á birgðahöfuðbókarfærslu sem þú tilgreinir. Kosturinn við að gera fasta jöfnun er að kostnaður af upprunalegu færslunnar er sendur í nýja færslu.  

### <a name="example--fixed-application-in-purchase-return"></a>Dæmi – Föst Jöfnun við innkaupaskil
Eftirfarandi dæmi, sem sýnir áhrif fastrar jöfnunar innkaupaskila vöru sem notar FIFO-kostnaðarmatsaðferð, er byggt á eftirfarandi atburðarás:  

1. Í færslu 1 bókar notandinn innkaup með kostnaðinn 10,00 SGM.  
2. Í færslu 2 bókar notandinn innkaup með kostnaðinn 20,00 SGM.  
3. Í færslu 3 bókar notandinn innkaupaskil. Notandinn setur fram bundna pöntun í önnur kaup með því að slá inn birgðafærslunúmerið í **Jöfnun til birgðafærslu** reitinn á vöruskilapöntun innkaupa.  

Eftirfarandi tafla sýnir birgðahöfuðbókarfærslur vegna atburðarásarinnar.  

|**Bókunardags.**|**Tegund birgðafærslu**|**Magn**|**Kostnaðarupphæð (raunverul.)**|**Birgðafærslunr.**|  
|----------------------|---------------------------------------------------|------------------|----------------------------------------------------|---------------------------------------------------|  
|01-04-20|Innkaup|10|10.00|1|  
|01-05-20|Innkaup|10|20.00|2|  
|01-06-20|Innkaup (skil)|-10|-20,00|3|  

Þar sem föst jöfnun er ntouð við innkaupaskil á aðra kaupfærslu er vörum skilað á raunkostnaði. Ef notandi hefði ekki framkvæmt fasta jöfnun hefði skilavaran verið ranglega virt á 10,00 SGM vegna þess að ávöxtuninni hefði verið beitt á fyrstu kaupfærsluna samkvæmt FIFO-meginreglunni.  

Eftirfarandi tafla sýnir vörujöfnunarfærslu vegna fastrar jöfnunar.  

|Bókunardagsetning|Birgðafærslunr. vöru á innleið|Jafnað af færslu nr.|Magn|Birgðafærsla nr.|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-06-20|2|3|10|3|  

Kostnaður annarra innkaup, SGM 20,00 er sendur rétt í innkaupaskilin.  

### <a name="example--fixed-application-with-average-cost"></a>Dæmi – Föst jöfnun með meðalkostnaði
Eftirfarandi dæmi, sem sýnir áhrif fastrar jöfnunar, er byggt á eftirfarandi atburðarás fyrir vöru sem notar meðalkostnaðarmatsaðferð:  

1. Í færslu númer 1 og 2 bókar notandinn tvo innkaupareikninga. Annar reikningurinn er með rangt innkaupsverð upp á SGM 1000,00.  
2. Í færslu númer 3, notandinn bókar innkaupakreditreikning með fasta jöfnun beitt á innkaupafærslu með rangt beint einingarkostnað. Summa reitsins **Kostnaðarupphæð Raunveruleg** fyrir tvær fastar jafnaðar gildisfærslur verður 0,00  
3. Í færslu númer 4, bókar notandinn annan innkaupareikning með réttum beinum einingarkostnaði upp á 100,00 kr  
4. Í færslu númer 5, notandinn bókar sölureikning.  
5. Birgðamagn er 0 og birgðavirði er einnig 0,00.  

Eftirfarandi tafla sýnir áhrif atburðarásarinnar í virðisfærslum vörunnar.  

Eftirfarandi tafla sýnir áhrif atburðarásarinnar í virðisfærslum vörunnar eftir bókun og þegar kostnaðarleiðrétting hefur veirð keyrð.

|Bókunardagsetning|Birgðafærslutegund|Virt magn|Kostnaðarupphæð (raunverul.)|Jafna birgðafærslu|Virt skv. meðalinnkaupsverði|Birgðafærslunr.|Færslunr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Innkaup|1|200.00||Nr|1|1|  
|01-01-20|Innkaup|1|1000.00||Nei|2|2|  
|01-01-20|Innkaup|-1|-1000|2|Nei|3|3|  
|01-01-20|Innkaup|1|100,00||Nei|4|4|  
|01-01-20|Sala|-2|-300,00||Já|5|5|  

Ef notandi hefði ekki gert fasta jöfnun á milli innkaupakreditreikningsins og innkaupanna með röngu innkaupsverði (skref 2 í fyrri atburðarás) hefði kostnaðurinn verið leiðréttur á annan hátt.  

Eftirfarandi tafla sýnir áhrifin á virðisfærslum vörunnar ef skref 2 í fyrri atburðarás er framkvæmt án fastrar jöfnunar.  

|Bókunardagsetning|Tegund birgðafærslu|Virt magn|Kostnaðarupphæð (raunverul.)|Jafna birgðafærslu|Virt skv. meðalinnkaupsverði|Birgðafærslunr.|Færslunr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Innkaup|1|200.00||Nr|1|1|  
|01-01-20|Innkaup|1|1000.00||Nei|2|2|  
|01-01-20|Innkaup|-1|433,33||Já|3|3|  
|01-01-20|Innkaup|1|100,00||Nei|4|4|  
|01-01-20|Sala|-2|866,67||Já|5|5|  

Í færslu númer 3, er gildi í **Kostnaðarupphæð Raunveruleg** reitnum metinn af meðaltali og tekur því til rangra bókana upp á 1000,00. Í samræmi verður það -433,33, sem er hækkuð kostnaðarupphæð. Útreikningurinn er 1300 / 3 = .-433,33.  

Í færslu númer 5, er gildi reitsins **Kostnaðarupphæð Raunveruleg** fyrir þessa færslu einnig ónákvæm af sömu ástæðu.  

> [!NOTE]  
>  Ef þú stofnar fasta jöfnun fyrir birgðaminnkun fyrir vöru sem notar aðferð meðalkostnaðar mun minnkunin ekki fá meðalkostnað fyrir vöruna lítk og vanalega heldur kostnað birgðaaukningar sem er tilgreind. Sú birgðaminnkun er svo ekki lengur hluti af útreikningi meðalinnkaupaverðs.  

### <a name="example--fixed-application-in-sales-return"></a>Dæmi – Föst Jöfnun við söluskil
Fastar jafnanir eru einnig mjög góð leið til að bakfæra kostnað nákvæmlega, eins og við söluvöruskil.  

Eftirfarandi dæmi, sem sýnir hvernig föst jöfnun tryggir nákvæma bakfærslu kostnaðar, er byggt á eftirfarandi atburðarás:  

1.  Notandinn bókar innkaupareikning.  
2.  Notandinn bókar sölureikning.  
3.  Notandinn bókar sölukreditreikning fyrir skilavöruna sem gildir um sölufærsluna, til að bakfæra kostnaðinn rétt.  
4.  Flutningskostnaður, tengdur innkaupapöntun sem var bókuð fyrr, er móttekinn. Notandinn bókar það sem kostnaðarauka.  

Eftirfarandi tafla sýnir niðurstöðu úr skrefi 1 til 3 í atburðarásinni fyrir virðisfærslur vörunnar.  

|Bókunardagsetning|Birgðafærslutegund|Virt magn|Kostnaðarupphæð (raunverul.)|Jafna frá birgðafærslu|Birgðafærslunr.|Færslunr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Innkaup|1|1000.00||1|1|  
|02-01-20|Sala|-1|1000.00||2|2|  
|03-01-20|Sala (kreditreikningur)|1|1000|2|3|3|  

Eftirfarandi tafla sýnir virðisfærsluna sem kemur til vegna atburðarásarskrefs 4, bókun kostnaðarauka.  

|Bókunardagsetning|Tegund birgðafærslu|Virt magn|Kostnaðarupphæð (raunverul.)|Jafna frá birgðafærslu|Birgðafærslunr.|Færslunr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|04-01-20|(Kostnaðarauki)|1|100.00||1|4|  

Eftirfarandi tafla sýnir hvaða áhrif nákvæm bakfærsla kostnaðar hefur á virðisfærslur vörunnar.  

|Bókunardagsetning|Birgðafærslutegund|Virt magn|Kostnaðarupphæð (raunverul.)|Jafna frá birgðafærslu|Birgðafærslunr.|Færslunr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Innkaup|1|1000.00||1|1|  
|02-01-20|Sala|-1|1100.00||2|2|  
|03-01-20|Sala (kreditreikningur)|1|1100.00|2|3|3|  
|04-01-20|(Kostnaðarauki)|1|100.00||1|4|  

Þegar runuvinnslan **Kostnaðarleiðrétting - Birgðafærslur** er keyrð er aukinn kostnaður við innkaupafærsluna vegna kostnaðarauka áframsendur á sölufærsluna færslu nr. 2. Sölufærslan framsendir svo þennan aukna kostnað á sölukreditfærslu (færsla númer 3). Endanleg niðurstaða er sú að kostnaður er rétt bakfærður.  

> [!NOTE]  
>  Ef verið er að vinna með skil eða kreditreikninga og settur hefur verið upp reiturinn **Nákvæm og lögbundin bakfærsla kostnaðar** annaðhvort á síðunni **Uppsetning fyrir Innkaup & Viðskiptaskuldir** eða glugganum **Sala & Útistandandi kröfur**, eins og við á í viðkomandi aðstæðum, fyllir [!INCLUDE[prod_short](includes/prod_short.md)] sjálfkrafa út í mismunandi jöfnunarfærslureiti þegar aðgerðin **Afrita úr fylgiskjali** er notuð. Til að nota aðgerðina **Sækja bókaðar fylgiskjalalínur til að bakfæra** eru allir reitir fylltir út sjálfkrafa.  

> [!NOTE]  
>  Ef Þú bókar færslu með fastri jöfnun og birgðahöfuðbók sem bókuð er er lokað, sem merkir að eftirstandandi magn er núll, verður eldri jöfnunin afgerð sjálfkrafa og notar birgðafærsluna með föstu jöfnuninni sem þú hefur valið.  

## <a name="transfer-application"></a>Jöfnun millifærslu
Þegar vara er flutt frá einum staðsetningu til annars, innan fyrirtækjabirgða, þá er jöfnun búin til milli tveggja millifærslufærslna. Að meta millifærslu  veltur á aðferð kostnaðarútreiknings. Fyrir vörur sem nota aðferðina Meðaltal til kostnaðarútreiknings er matið gert með því að nota meðalkostnaðinn á meðalkostnaðartímabilinu sem verðmatsdagsetning flutningsins á sér stað. Fyrir vörur sem nota aðrar aðferðir kostnaðarútreiknings er matið gert með því að rekja aftur í kostnað upprunalegrar birgðaaukningar.  

### <a name="example--average-costing-method"></a>Dæmi – Aðferð meðalkostn.útreiknings
Eftirfarandi dæmi, sem sýnir hvernig millifærslufærslur eru jafnaðar, byggist á eftirfarandi atburðarás fyrir vöru sem notar Meðalkostnaðarmatsaðferð og meðalkostnaðartímabil dags.  

1. Notandinn kaupir vöruna með kostnaði upp á SGM 10.00.  
2. Notandinn kaupir vöru aftur með kostnaði upp á SGM 20.00.  
3. Notandinn flytur vöruna úr staðsetningunni EAST í WEST.  

Eftirfarandi tafla sýnir hvaða áhrif flutningurinn hefur á virðisfærslur vörunnar.  

|Bókunardagsetning|Birgðafærslutegund|Kóti birgðageymslu |Virt magn|Kostnaðarupphæð (raunverul.)|Færslunr.|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Innkaup|Austurdeildin|1|10,00|1|  
|01-01-20|Innkaup|Austurdeildin|1|20,00|2|  
|02-01-20|Millifærsla|Austurdeildin|-1|15,00|3|  
|02-01-20|Millifærsla|Vesturdeildin|1|15,00|4|  

### <a name="example--standard-costing-method"></a>Dæmi staðalaðferð kostnaðarútreiknings
Eftirfarandi dæmi, sem sýnir hvernig millifærslufærslur eru jafnaðar, byggist á eftirfarandi atburðarás fyrir vöru sem notar Staðalkostnaðarmatsaðferð og meðalkostnaðartímabil dags.  

1. Notandinn kaupir vöruna með staðalkostnaði upp á SGM 10.00.  
2. Notandinn flytur vöruna úr staðsetningunni EAST í WEST með staðalkostnaði upp á SGM 12.00.  

Eftirfarandi tafla sýnir hvaða áhrif flutningurinn hefur á virðisfærslur vörunnar.  

|Bókunardagsetning|Birgðafærslutegund|Kóti birgðageymslu |Virt magn|Kostnaðarupphæð (raunverul.)|Færslunr.|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Innkaup|Austurdeildin|1|10,00|1|  
|02-01-20|Millifærsla|Austurdeildin|-1|10,00|2|  
|02-01-20|Millifærsla|Vesturdeildin|1|10,00|3|  

Þar sem gildi upprunalegu birgðaaukningar er mælt í staðbundinni mynt 10,00, er millifærsla metin á þeim kostnaði, ekki staðbundinni mynt 12.00.  

## <a name="reapplication"></a>Endurjöfnun
Vegna þess hvernig kostnaðarverð vöru er reiknað út gæti skökk vörujöfnun leitt til skekkts meðalkostnaðar og einingarkostnaðar. Eftirfarandi atburðarás getur valdið röngum vörujöfnunum sem krefst þess að vörujafnanir séu afturkallaðar og vörubókarfærslur endurjafnaðar.  

* Gleymst hefur að gera fasta jöfnun.  
* Röng föst jöfnun var gerð.  
* Æskilegt er að hnekkja jöfnuninni sem var stofnuð sjálfkrafa við bókun samkvæmt aðferð kostnaðarútreiknings fyrir vöruna.  
* Skila þarf vöru sem búið er að jafna sölu við handvirkt án þess að nota aðgerðina**Sækja bókaðar fylgiskjalalínur til að bakfæra** og því verður að afturkalla þessa jöfnun.  

[!INCLUDE[prod_short](includes/prod_short.md)] býður upp á eiginleika til að greina og leiðrétta jöfnun vöru. Þetta er framkvæmt á síðunni **Vinnublað fyrir jöfnun**.  

## <a name="see-also"></a>Sjá einnig
[Hönnunarupplýsingar: Þekkt vandamál birgðajöfnunar](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Hönnunarupplýsingar: Aðferð kostnaðarútreiknings](design-details-costing-methods.md)  
[Hönnunarupplýsingar: Meðalkostnaður](design-details-average-cost.md)   
[Hönnunarupplýsingar: kostnaðarleiðrétting](design-details-cost-adjustment.md)  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
