---
title: Svara beiðnum um persónuleg gögn notanda
description: Í greininni er útskýrt hvernig brugðist er við beiðnum um persónuleg gögn.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 04/25/2023
ms.custom: bap-template
---

# <a name="responding-to-requests-about-users-personal-data" />Svara beiðnum um persónuleg gögn notanda

Skráðir aðilar geta óskað eftir nokkrum tegundum aðgerða varðandi persónuupplýsingar þeirra. Undir suma persónuverndarlög og reglugerðir hafa til dæmis menn rétt til að óska eftir útflutningi, eyðingu og breytingum á persónuupplýsingum sínum. Þessar beiðnir eru kallaðar  *Gagnaefnisbeiðnir*. Ef þú hefur flokkað næmi gagnanna, og ert viss um að þau séu rétt, getur kerfisstjóri svarað beiðnum með því að nota valkostina í  **flipanum Gagnanæði**  í  **hlutverkamiðstöð stjórnunarstjóra** . Nánari upplýsingar um flokkun gagna og gagna næmi í  [!INCLUDE[prod_long](includes/prod_long.md)], farið er í eftirfarandi greinar:

* [Gagnaflokkun](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) 
* [Flokkun gagnatrúnaðar](admin-classifying-data-sensitivity.md)  

## <a name="types-of-requests" />Tegundir beiðna

Eftirfarandi tafla gefur dæmi um tegundir beiðna sem stjórnendur geta brugðist við.

> [!Note]
> Á meðan við bjóðum upp á getu til að svara þessum gerðum beiðna, og þar með aðgang, persónuleg gögn, er það á þína ábyrgð að tryggja að persónuleg og viðkvæm gögn séu geymd og flokkuð á viðeigandi hátt.

|Tegund beiðni|Lýsing og leiðbeinandi svar|
|-----|-----|
|Flutningsbeiðni|Gagnaðili getur gert beiðni um gagnabeiðni. Nauðsynlegt er að flytja persónugögn gagnanna úr kerfunum og koma því á skipulegu, almennt notuðu sniði. Til að bregðast við þessum beiðnum er hægt að nota  **forritið**  gagnapersónuvernd til að flytja persónuleg gögn í Excel skrá eða  RapidStart  skilgreiningarpakka. Með því að nota Excel er hægt að breyta persónulegum gögnum og vista þau á algengu, vélalesanlegu sniði, eins og .csv eða .xml. Fyrir RapidStart-grunnstillingapakka er hægt að grunnstilla aðalgagnatöflur og tengdar töflur sem innihalda persónuleg gögn. <br><br> **Athugið:**  þegar gögn eru flutt út er tilgreint lágmarks næmnistig. Útflutningur mun innihalda lágmarksstigið og öll stigin þar fyrir ofan. Til dæmis, ef Útflutningur gagna sem flokkast sem persónulegt, er útflutningur einnig eru gögn flokkuð sem viðkvæm. <br><br>Við útflutning gagna sem tengjast skráðum einstaklingi leitar **Hjálparforrit gagnaverndar** að beinum venslum milli skráðs einstaklings og gagna sem tengjast honum. Óbein vensl milli gagna sem tengjast skráðum einstaklingi og annarra gagna eru ekki flutt sjálfkrafa út af **Hjálparforriti gagnaverndar**. Til dæmis hefur tengiliðataflan beintengd gögn tengiliðasvara forstillingar og tafla tengiliðasvara forstillingar tengist enn fremur gögnum forstillingarspurninga. Ef þú vilt einnig flytja út forstillingarspurningar verður þú að bæta þessari töflu við handvirkt sem röð með viðeigandi síum úr grunnstillingarpakkanum sem **Hjálparforrit gagnaverndar** býr til.|
|Beiðni um eyðingu|Skráður aðili getur óskað eftir því að þú eyðir persónulegum gögnum. Það eru nokkrar leiðir til að eyða persónulegum gögnum með því að nota sérstillingarmöguleikana, en ákvörðun og framkvæmd er á þína ábyrgð. Í sumum tilfellum gæti verið hægt að velja að breyta gögnunum. Til dæmis er búið að eyða tengilið og keyra síðan keyrsluna Eyða afturkölluðum milliverkunum til að eyða samskiptum tengiliðarins. <br><br> **Til athugunar:**  ef dagsetning er tilgreind í  **reitnum leyfa eyðingu áður en**  reiturinn á  **uppsetningarsíðum**  &  **sölu eða**  innkaupa & lánardrottna er tilgreindur gæti þurft að breyta dagsetningunni svo hægt sé að eyða bókuðum sölu-og innkaupafylgiskjölum sem eru með bókunardagsetningar á eða fyrir þá dagsetningu.|
|Beiðnir um leiðréttingu|Skráður aðili getur óskað eftir því að ónákvæm persónuleg gögn verði leiðrétt. Hægt er gera það á nokkra vegu: Í sumum tilfellum er hægt að flytja út lista í Excel til að magnbreyta margar skrár á fljótlegan hátt og síðan flytja inn uppfærðu gögnin. Frekari upplýsingar eru í [Flytja út viðskiptagögn í Excel](about-export-data.md). Einnig er hægt að breyta reitum handvirkt sem innihalda persónuleg gögn, t.d. með því að breyta upplýsingum um viðskiptavin í viðskiptamannaspjaldinu. Hins vegar eru færslur eins og almennar, viðskiptamanna-og skattfærslur mikilvægar. Ef þú geymir persónuleg gögn í viðskiptafærsluskrám skaltu íhuga að nota sérstillingarmöguleikana til að breyta slíkum persónulegum gögnum.|

## <a name="restrict-data-processing-for-a-data-subject" />Takmarka gagnavinnslu við gagnaefni

Skráður aðili getur óskað eftir því að þú hættir tímabundið með vinnslu á persónulegum gögnum hans. Til að heiðra slíkar beiðnir er hægt að merkja færslur þeirra sem lokaðar vegna persónuverndar til að hætta að vinna úr gögnum þeirra. Þegar skrá er merkt sem lokuð er ekki hægt að búa til nýjar færslur sem nota þessa færslu. Til dæmis getur þú ekki búið til nýjan reikning fyrir viðskiptavini þegar annað hvort viðskiptavinurinn eða seljandi er lokaður. Til að merkja skráðan aðila sem læstan skal opna spjaldið fyrir skráða aðilann, t.d. spjald viðskiptavinar, lánardrottins eða tengiliðs og velja gátreitinn **Lokað fyrir vegna persónuverndar**. Þú gætir þurft að velja **Sýna fleiri** til að birta reitinn.  

## <a name="handling-data-subject-requests-when-using-a-trial-version" />Afgreiðsla á efnisbeiðnum gagna við notkun prufuútgáfu

Ákveðnar gerðir af persónugögnum eru hluti af  Microsoft 365  lykli og aðeins kerfisstjórar geta flutt út gögnin. Ferlið sem nær utan um beiðnir skráðs einstaklings fer eftir gerð [!INCLUDE[prod_short](includes/prod_short.md)] leigjandans.

Ef þú hefur greitt áskrift fyrir  [!INCLUDE[prod_short](includes/prod_short.md)] þurfa notendur að hafa samband við stjórnanda leigjendabeiðni þíns til að gera gagnaháð beiðni. Stjórnendur hafa stjórnunarheimildir og tæki til að uppfylla beiðnir um gagnaefni.

Ef þú áritar þig fyrir  [!INCLUDE[prod_short](includes/prod_short.md)]  af síðunni rannsóknir  [og þú ert enn að nota prufuútgáfuna geta notendur sótt og flutt niður sín eigin gögn í](https://trials.dynamics.com/)  vinnu-og Skólapersónuverndarsíðunni í Azure [gáttinni](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade).

Á persónuverndarsíðu vinnu og skóla geturðu einnig lokað reikningnum þínum. Hins vegar mælum við með því að öll gögn séu flutt út og öllum eytt. Ef þú vilt eyða reikningnum þínum merkir það að þú tapir aðgangi að [!INCLUDE[prod_short](includes/prod_short.md)].

Þú getur samt merkt fólk sem útilokað vegna persónuverndar og útflutnings, breytt eða eytt færslum eins og lýst er annars staðar í þessari grein.  

## <a name="exporting-data-from-tables-not-classified-by-data-subject" />Útflutningur gagna úr töflum ekki flokkaður eftir efni gagna

Ef flytja þarf gögn sem ekki eru flokkuð á þann hátt þannig að það sé sjálfvirkt flutt inn, s.s. gögn úr töflunni svör lýsingar, verður að grípa til eftirfarandi aðgerða:

* Íhugaðu hvort þú ættir raunverulega að flytja út viðbótargögn sem eru ekki beint tengd tengiliðinn.
* Bættu töflu og venslum handvirkt við Hraðstart-pakkann og útfærðu hann beint úr Hraðstart pakkanum. Við það myndast Hraðstart pakki fyrir þig, svo hægt sé að klikka á honum í slíkum aðstæðum.

## <a name="handling-data-about-minors" />Meðhöndlun gagna um myntsafnið

Ef tengiliðar er undir lögaldri samkvæmt lögum á þínu svæði getur þú bent á það með því að velja gátreitinn **Barn** á spjaldinu **Tengiliður**. Þegar þú gerir það verður gátreiturinn **Lokað fyrir vegna persónuverndar** valinn sjálfkrafa. Þegar þú færð samþykki foreldris eða forráðamanns getur þú valið gátreitinn **Samþykki foreldra fengið** til að opna aftur á tengiliðinn. Þó að þú getir unnið úr persónulegum gögnum fyrir ólögráða einstakling, getur þú ekki notað lýsingaraðgerðina í Microsoft Dynamics 365 Sales.

> [!Note]
> Breytingaskráin getur skráð upplýsingar eins og hvenær og af hverjum gátreiturinn **Samþykki foreldra fengið** var valinn. Stjórnandi getur sett það upp með því að nota leiðarvísinn **Uppsetning breytingaskrár** og einnig velja gátreitinn **Skrá breytingar á fengnu samþykki foreldris** á spjaldinu **Tengiliður**. Frekari upplýsingar eru í [Skráning breytinga](across-log-changes.md).  

### <a name="see-also" />Sjá einnig .

[Gagnaflokkun](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Flokkun gagnatrúnaðar](admin-classifying-data-sensitivity.md)  
[Flutningur viðskiptagagna í Excel](about-export-data.md)  
[Skráning breytinga](across-log-changes.md)  
[Efnisbeiðnir um gögn](/microsoft-365/compliance/gdpr-data-subject-requests)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
