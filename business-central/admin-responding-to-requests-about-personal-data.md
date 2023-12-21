---
title: Að bregðast við beiðnum um persónuupplýsingar notenda
description: Þessi grein útskýrir hvernig á að bregðast við beiðnum um persónuupplýsingar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 04/25/2023
ms.custom: bap-template
---

# <a name="responding-to-requests-about-users-personal-data"></a>Að bregðast við beiðnum um persónuupplýsingar notenda

Skráðir aðilar geta óskað eftir nokkrum tegundum aðgerða varðandi persónuupplýsingar þeirra. Til dæmis, samkvæmt sumum persónuverndarlögum og reglum, hafa þeir rétt til að biðja um útflutning, eyðingu og breytingu á persónuupplýsingum sínum. Þessar beiðnir eru kallaðar *Beiðnir um gagnaðila*. Ef þú hefur flokkað næmni gagna þinna og ert viss um að þau séu réttar, getur stjórnandi svarað beiðnum með því að nota valkostina á  **Gagnavernd** flipanum í **Upplýsingatæknistjóri** Hlutverkamiðstöð. 
<!--
For more information about classifying data and data sensitivity in [!INCLUDE[prod_long](includes/prod_long.md)], go to the following articles:

* [Classifying Data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) 
* [Classifying Data Sensitivity](admin-classifying-data-sensitivity.md)  -->

## <a name="types-of-requests"></a>Tegundir beiðna

Eftirfarandi tafla gefur dæmi um þær tegundir beiðna sem stjórnendur geta svarað.

> [!Note]
> Þó að við bjóðum upp á möguleika til að bregðast við slíkum beiðnum og þar með aðgang að persónuupplýsingum, er það á þína ábyrgð að tryggja að persónuleg og viðkvæm gögn séu staðsett og flokkuð á viðeigandi hátt.

|Tegund beiðni|Lýsing og leiðbeinandi svar|
|-----|-----|
|Flutningsbeiðni|Skráður einstaklingur getur lagt fram beiðni um gagnaflutning. Þú verður að flytja út persónuupplýsingar hins skráða úr kerfum þínum og láta þær í té á skipulögðu, almennu sniði. Til að bregðast við þessum beiðnum geturðu notað **Data Privacy Utility** til að flytja út persónuleg gögn í Excel skrá eða RapidStart stillingarpakka. Með því að nota Excel er hægt að breyta persónulegum gögnum og vista þau á algengu, vélalesanlegu sniði, eins og .csv eða .xml. Fyrir RapidStart-grunnstillingapakka er hægt að grunnstilla aðalgagnatöflur og tengdar töflur sem innihalda persónuleg gögn. <br><br> **Athugið:** Þegar þú flytur út gögn tilgreinirðu lágmarksnæmni. Útflutningur mun innihalda lágmarksstigið og öll stigin þar fyrir ofan. Til dæmis, ef þú flytur út gögn sem eru flokkuð sem persónuleg, inniheldur útflutningurinn einnig gögn sem flokkuð eru sem viðkvæm. <br><br>Við útflutning gagna sem tengjast skráðum einstaklingi leitar **Hjálparforrit gagnaverndar** að beinum venslum milli skráðs einstaklings og gagna sem tengjast honum. Óbein vensl milli gagna sem tengjast skráðum einstaklingi og annarra gagna eru ekki flutt sjálfkrafa út af **Hjálparforriti gagnaverndar**. Til dæmis hefur tengiliðataflan beintengd gögn tengiliðasvara forstillingar og tafla tengiliðasvara forstillingar tengist enn fremur gögnum forstillingarspurninga. Ef þú vilt einnig flytja út forstillingarspurningar verður þú að bæta þessari töflu við handvirkt sem röð með viðeigandi síum úr grunnstillingarpakkanum sem **Hjálparforrit gagnaverndar** býr til.|
|Beiðni um eyðingu|Skráður aðili getur óskað eftir því að þú eyðir persónulegum gögnum. Það eru nokkrar leiðir til að eyða persónulegum gögnum með því að nota sérstillingarmöguleikana, en ákvörðun og framkvæmd er á þína ábyrgð. Í sumum tilfellum gætirðu valið að breyta gögnunum þínum beint. Til dæmis, eyða tengilið og keyra síðan runuvinnsluna Eyða aflýstum samskiptum til að eyða samskiptum fyrir tengiliðinn. <br><br> **Athugið:** Ef þú hefur tilgreint dagsetningu í **Leyfa eyðingu skjala áður** á reitnum **Sala & Uppsetning krafna** eða **Kaup & Uppsetning skulda** síður gætirðu þurft að breyta dagsetningunni þannig að þú getir eytt bókuðum sölu- og innkaupaskjölum sem hafa bókunardagsetningar á eða fyrir þá dagsetningu.|
|Beiðnir um leiðréttingu|Skráður aðili getur óskað eftir því að ónákvæm persónuleg gögn verði leiðrétt. Hægt er gera það á nokkra vegu: Í sumum tilfellum er hægt að flytja út lista í Excel til að magnbreyta margar skrár á fljótlegan hátt og síðan flytja inn uppfærðu gögnin. Frekari upplýsingar eru í [Flytja út viðskiptagögn í Excel](about-export-data.md). Einnig er hægt að breyta reitum handvirkt sem innihalda persónuleg gögn, t.d. með því að breyta upplýsingum um viðskiptavin í viðskiptamannaspjaldinu. Hins vegar eru færslur eins og almennar, viðskiptamanna- og skattafærslur mikilvægar. Ef þú geymir persónuleg gögn í viðskiptafærsluskrám skaltu íhuga að nota sérstillingarmöguleikana til að breyta slíkum persónulegum gögnum.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Takmarka gagnavinnslu fyrir skráðan einstakling

Skráður aðili getur óskað eftir því að þú hættir tímabundið með vinnslu á persónulegum gögnum hans. Til að heiðra slíkar beiðnir er hægt að merkja færslur þeirra sem lokaðar vegna persónuverndar til að hætta að vinna úr gögnum þeirra. Þegar skrá er merkt sem lokuð er ekki hægt að búa til nýjar færslur sem nota þessa færslu. Til dæmis getur þú ekki búið til nýjan reikning fyrir viðskiptavini þegar annað hvort viðskiptavinurinn eða seljandi er lokaður. Til að merkja skráðan aðila sem læstan skal opna spjaldið fyrir skráða aðilann, t.d. spjald viðskiptavinar, lánardrottins eða tengiliðs og velja gátreitinn **Lokað fyrir vegna persónuverndar**. Þú gætir þurft að velja **Sýna fleiri** til að birta reitinn.  

## <a name="handling-data-subject-requests-when-using-a-trial-version"></a>Meðhöndlun beiðna skráðra einstaklinga þegar prufuútgáfa er notuð

Ákveðnar tegundir persónuupplýsinga eru hluti af Microsoft 365 reikningi og aðeins stjórnendur geta flutt gögnin út. Ferlið sem nær utan um beiðnir skráðs einstaklings fer eftir gerð [!INCLUDE[prod_short](includes/prod_short.md)] leigjandans.

Ef þú ert með greidda áskrift að [!INCLUDE[prod_short](includes/prod_short.md)] verða notendur að hafa samband við leigjanda stjórnanda fyrirtækisins til að leggja fram beiðni um skráða einstaklinga. Stjórnendur hafa stjórnunarréttindi og tæki til að uppfylla beiðnir skráðra einstaklinga.

Ef þú skráðir þig í [!INCLUDE[prod_short](includes/prod_short.md)] af  [Prufunarsíðunni](https://trials.dynamics.com/) og þú ert enn að nota prufuútgáfuna geta notendur hlaðið niður og flutt út sín eigin gögn í  [Persónuverndarsíðu vinnu og skóla í Azure gáttinni](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade).

Á persónuverndarsíðu vinnu og skóla geturðu einnig lokað reikningnum þínum. Hins vegar mælum við með því að þú flytur út og eyðir öllum gögnum fyrst. Að eyða reikningnum þínum þýðir að þú missir aðgang að [!INCLUDE[prod_short](includes/prod_short.md)].

Þú getur samt merkt fólk sem útilokað vegna persónuverndar og útflutnings, breytt eða eytt færslum eins og lýst er annars staðar í þessari grein.  

## <a name="exporting-data-from-tables-not-classified-by-data-subject"></a>Flytja út gögn úr töflum sem ekki eru flokkaðar eftir skráðum einstaklingi

Ef þú verður að flytja út gögn sem eru ekki flokkuð á þann hátt að þau séu flutt sjálfkrafa út, eins og gögn úr töflunni prófílsvör, verður þú að grípa til eftirfarandi aðgerða:

* Íhugaðu hvort þú verður virkilega að flytja út viðbótargögn sem eru ekki beintengd tengiliðnum.
* Bættu töflunni og sambandinu handvirkt við Rapid Start pakkann og fluttu hana beint úr Rapid Start pakkanum. Við búum til hraðbyrjunarpakka fyrir þig, svo þú getir lagað hann við slíkar aðstæður.

## <a name="handling-data-about-minors"></a>Meðhöndlun gagna um ólögráða börn

Ef tengiliðar er undir lögaldri samkvæmt lögum á þínu svæði getur þú bent á það með því að velja gátreitinn **Barn** á spjaldinu **Tengiliður**. Þegar þú gerir það verður gátreiturinn **Lokað fyrir vegna persónuverndar** valinn sjálfkrafa. Þegar þú færð samþykki foreldris eða forráðamanns getur þú valið gátreitinn **Samþykki foreldra fengið** til að opna aftur á tengiliðinn. Þó að þú getir unnið úr persónulegum gögnum fyrir ólögráða einstakling, getur þú ekki notað lýsingaraðgerðina í Microsoft Dynamics 365 Sales.

> [!Note]
> Breytingaskráin getur skráð upplýsingar eins og hvenær og af hverjum gátreiturinn **Samþykki foreldra fengið** var valinn. Stjórnandi getur sett það upp með því að nota leiðarvísinn **Uppsetning breytingaskrár** og einnig velja gátreitinn **Skrá breytingar á fengnu samþykki foreldris** á spjaldinu **Tengiliður**. Frekari upplýsingar eru í [Skráning breytinga](across-log-changes.md).  

### <a name="see-also"></a>Sjá einnig .

<!-- [Classifying Data](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Classifying Data Sensitivity](admin-classifying-data-sensitivity.md)  -->
[Flutningur viðskiptagagna í Excel](about-export-data.md)  
[Skráning breytinga](across-log-changes.md)  
[Gagnabeiðnir](/microsoft-365/compliance/gdpr-data-subject-requests)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
