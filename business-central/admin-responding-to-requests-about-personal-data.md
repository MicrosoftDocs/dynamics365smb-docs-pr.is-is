---
title: Svara beiðnum um persónugögn notenda
description: Þessi grein útskýrir hvernig á að bregðast við beiðnum um persónugögn.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/25/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Svara beiðnum um persónugögn notenda

Skráðir aðilar geta óskað eftir nokkrum tegundum aðgerða varðandi persónuupplýsingar þeirra. Til dæmis, samkvæmt sumum lögum og reglum um persónuvernd, hafa þeir til dæmis rétt til að óska eftir útflutningi, eyðingu og breytingu á persónugögnum sínum. Þessar beiðnir kallast *beiðnir um efni gagna*. Ef næmi gagna hefur verið flokkað og hann er viss um að þau séu rétt getur stjórnandi svarað beiðnum með því að nota valkostina í flipanum Persónuvernd gagna **í**  **hlutverkamiðstöð tæknistjóra** .

## Tegundir beiðna

Í eftirfarandi töflu eru dæmi um tegundir beiðnastjóra sem stjórnendur geta svarað.

> [!Note]
> Þó að við bjóðum upp á möguleika til að svara þessum gerðum beiðna og með því að fá aðgang að persónugögnum ber það ábyrgð á því að tryggja að persónuleg og viðkvæm gögn séu staðsett og flokkuð á viðeigandi hátt.

|Tegund beiðni|Lýsing og leiðbeinandi svar|
|-----|-----|
|Flutningsbeiðni|Gagnaefni getur gert gagnaflutningsbeiðni. Flytja verður út persónugögn gagnaaðila úr kerfunum og gefa þau upp á skipulagðu, algengu sniði. Til að svara þessum beiðnum **er hægt að nota gagnaverndarforritið** til að flytja persónugögn út í Excel-skrá eða RapidStart grunnstillingarpakka. Með því að nota Excel er hægt að breyta persónulegum gögnum og vista þau á algengu, vélalesanlegu sniði, eins og .csv eða .xml. Fyrir RapidStart-grunnstillingapakka er hægt að grunnstilla aðalgagnatöflur og tengdar töflur sem innihalda persónuleg gögn. <br><br> **Til athugunar:** Þegar gögn eru flutt út er lágmarksnæmisstig tilgreint. Útflutningur mun innihalda lágmarksstigið og öll stigin þar fyrir ofan. Ef til dæmis gögn sem flokkast sem persónuleg eru flutt út inniheldur útflutningurinn einnig gögn sem flokkuð eru sem Viðkvæm. <br><br>Við útflutning gagna sem tengjast skráðum einstaklingi leitar **Hjálparforrit gagnaverndar** að beinum venslum milli skráðs einstaklings og gagna sem tengjast honum. Óbein vensl milli gagna sem tengjast skráðum einstaklingi og annarra gagna eru ekki flutt sjálfkrafa út af **Hjálparforriti gagnaverndar**. Til dæmis hefur tengiliðataflan beintengd gögn tengiliðasvara forstillingar og tafla tengiliðasvara forstillingar tengist enn fremur gögnum forstillingarspurninga. Ef þú vilt einnig flytja út forstillingarspurningar verður þú að bæta þessari töflu við handvirkt sem röð með viðeigandi síum úr grunnstillingarpakkanum sem **Hjálparforrit gagnaverndar** býr til.|
|Beiðni um eyðingu|Skráður aðili getur óskað eftir því að þú eyðir persónulegum gögnum. Það eru nokkrar leiðir til að eyða persónulegum gögnum með því að nota sérstillingarmöguleikana, en ákvörðun og framkvæmd er á þína ábyrgð. Í sumum tilfellum gæti notandi valið að breyta gögnunum beint. Til dæmis má eyða tengilið og keyra síðan keyrsluna Eyða ógiltum samskiptum til að eyða samskiptum fyrir tengiliðinn. <br><br> **Til athugunar:** Ef tilgreind hefur verið dagsetning í reitnum **Leyfa eyðingu skjals fyrir** á síðunum **Sölugrunnur** eða **Innkaupagrunnur** gæti þurft að breyta dagsetningunni svo að hægt sé að eyða bókuðum sölu- og innkaupaskjölum með bókunardagsetningum á eða fyrir þá dagsetningu.|
|Beiðnir um leiðréttingu|Skráður aðili getur óskað eftir því að ónákvæm persónuleg gögn verði leiðrétt. Hægt er gera það á nokkra vegu: Í sumum tilfellum er hægt að flytja út lista í Excel til að magnbreyta margar skrár á fljótlegan hátt og síðan flytja inn uppfærðu gögnin. Frekari upplýsingar eru í [Flytja út viðskiptagögn í Excel](about-export-data.md). Einnig er hægt að breyta reitum handvirkt sem innihalda persónuleg gögn, t.d. með því að breyta upplýsingum um viðskiptavin í viðskiptamannaspjaldinu. Hins vegar eru færslur á borð við almennar, viðskiptamanna- og skattbókarfærslur mikilvægar. Ef þú geymir persónuleg gögn í viðskiptafærsluskrám skaltu íhuga að nota sérstillingarmöguleikana til að breyta slíkum persónulegum gögnum.|

## Takmarka vinnslu gagna fyrir gagnaaðila

Skráður aðili getur óskað eftir því að þú hættir tímabundið með vinnslu á persónulegum gögnum hans. Til að heiðra slíkar beiðnir er hægt að merkja færslur þeirra sem lokaðar vegna persónuverndar til að hætta að vinna úr gögnum þeirra. Þegar skrá er merkt sem lokuð er ekki hægt að búa til nýjar færslur sem nota þessa færslu. Til dæmis getur þú ekki búið til nýjan reikning fyrir viðskiptavini þegar annað hvort viðskiptavinurinn eða seljandi er lokaður. Til að merkja skráðan aðila sem læstan skal opna spjaldið fyrir skráða aðilann, t.d. spjald viðskiptavinar, lánardrottins eða tengiliðs og velja gátreitinn **Lokað fyrir vegna persónuverndar**. Þú gætir þurft að velja **Sýna fleiri** til að birta reitinn.  

## Meðhöndlun efnisbeiðna gagna þegar prufuútgáfa er notuð

Ákveðnar gerðir persónugagna eru hluti af reikningi Microsoft 365 og aðeins stjórnendur geta flutt gögnin út. Ferlið sem nær utan um beiðnir skráðs einstaklings fer eftir gerð [!INCLUDE[prod_short](includes/prod_short.md)] leigjandans.

Ef áskrift er greidd verða notendur að hafa samband við leigjanda fyrirtækisins til að gera beiðni um efnisþörf [!INCLUDE[prod_short](includes/prod_short.md)] gagna. Stjórnendur hafa stjórnunarréttindi og verkfæri til að uppfylla beiðnir um efnisþörf gagna.

Ef þú skráðir þig inn á [!INCLUDE[prod_short](includes/prod_short.md)]  [prufusíðuna og notandinn notar](https://trials.dynamics.com/) prufuútgáfuna enn þá geta notendur sótt og flutt út eigin gögn á síðunni [Vinnu- og skólavernd í Azure-gáttinni](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade).

Á persónuverndarsíðu vinnu og skóla geturðu einnig lokað reikningnum þínum. Hins vegar er mælt með því að öll gögn séu flutt út og þeim eytt fyrst. Ef reikningnum er eytt verður aðgangi [!INCLUDE[prod_short](includes/prod_short.md)] að því glatað.

Þú getur samt merkt fólk sem útilokað vegna persónuverndar og útflutnings, breytt eða eytt færslum eins og lýst er annars staðar í þessari grein.  

## Útflutningur gagna úr töflum sem ekki eru flokkaðar eftir gögnum

Ef flytja þarf út gögn sem ekki eru flokkuð á þann hátt að þau séu sjálfkrafa flutt út, t.d. gögn úr töflunni Svör forstillingar, þarf að framkvæma eftirfarandi aðgerðir:

* Íhuga þarf hvort flytja þurfi viðbótargögn út sem ekki tengjast tengiliðnum beint.
* Bætið töflunni og sambandinu handvirkt við hraðbyrjunarpakkann og flytjið hana út beint úr hraðræsingarpakkanum. Við myndum skjóta byrjunarpakka fyrir þig, svo að þú getir klipið hann í slíkum aðstæðum.

## Meðferð gagna um minnihlutahópa

Ef tengiliðar er undir lögaldri samkvæmt lögum á þínu svæði getur þú bent á það með því að velja gátreitinn **Barn** á spjaldinu **Tengiliður**. Þegar þú gerir það verður gátreiturinn **Lokað fyrir vegna persónuverndar** valinn sjálfkrafa. Þegar þú færð samþykki foreldris eða forráðamanns getur þú valið gátreitinn **Samþykki foreldra fengið** til að opna aftur á tengiliðinn. Þó að þú getir unnið úr persónulegum gögnum fyrir ólögráða einstakling, getur þú ekki notað lýsingaraðgerðina í Microsoft Dynamics 365 Sales.

> [!Note]
> Breytingaskráin getur skráð upplýsingar eins og hvenær og af hverjum gátreiturinn **Samþykki foreldra fengið** var valinn. Stjórnandi getur sett það upp með því að nota leiðarvísinn **Uppsetning breytingaskrár** og einnig velja gátreitinn **Skrá breytingar á fengnu samþykki foreldris** á spjaldinu **Tengiliður**. Frekari upplýsingar eru í [Skráning breytinga](across-log-changes.md).  

### Sjá einnig .

<!-- [Classifying Data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Classifying Data Sensitivity](admin-classifying-data-sensitivity.md)  -->
[Flutningur viðskiptagagna í Excel](about-export-data.md)  
[Skráning breytinga](across-log-changes.md)  
[Beiðnir um efni gagna](/microsoft-365/compliance/gdpr-data-subject-requests)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
