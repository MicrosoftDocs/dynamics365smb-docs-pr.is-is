---
title: "Svara beiðnum um persónuleg gögn"
description: "Þú verður að bregðast við beiðnum skráðra aðila."
author: bholtorf
ms.service: dynamics365-business-central
ms.author: bholtorf
ms.custom: na
ms.date: 11/06/2018
ms.reviewer: na
ms.topic: article
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 313ebe68ae1963e22bc17d53a7c41ae8f090de60
ms.contentlocale: is-is
ms.lasthandoff: 11/22/2018

---

# <a name="responding-to-requests-about-personal-data"></a>Svara beiðnum um persónuleg gögn  
Skráðir aðilar geta óskað eftir nokkrum tegundum aðgerða varðandi persónuupplýsingar þeirra. Til dæmis, samkvæmt almennu persónuverndarreglugerðinni (GDPR), hafa íbúar ESB rétt til að óska eftir útflutningi, eyðingu og breytingu á persónuupplýsingum sínum. Þetta er þekkt sem *Beiðni skráðs einstaklings*. Ef þú hefur flokkað viðkvæmni gagna og ert viss um að þau séu rétt, getur kerfisstjóri brugðist við beiðnum með því að nota valkostina sem heyra undir **Gagnavernd** í **Stjórna notendum, notendaflokkum og heimildum** í Mínu hlutverki eða, ef þú notar Windows-biðlarann, í **Tæknistjóri** í Mínu hlutverki. Nánari upplýsingar um gagnaflokkun og flokkun á gagnatrúnaði í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] er að finna í [Gagnaflokkun](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json) og [Flokkun á gagnatrúnaði](admin-classifying-data-sensitivity.md).  

## <a name="types-of-requests"></a>Tegundir beiðna

Eftirfarandi tafla veitir dæmi um tegundir beiðna sem þú getur svarað.

> [!Note]
> Þó að við bjóðum upp á möguleika til að bregðast við slíkum beiðnum og þar með aðgang að persónulegum gögnum er það á þína ábyrgð að tryggja að persónuleg og viðkvæm gögn séu staðsett og flokkuð á viðeigandi hátt.

|Tegund beiðni|Lýsing og leiðbeinandi svar|
|-----|-----|
|Flutningsbeiðni|Skráður aðili getur gert gagnaflutningsbeiðni, sem þýðir að hluta til að þú verður að flytja persónuleg gögn skráðs aðila úr þínu kerfi og senda það á skipulögðu, algengu sniði. Til að bregðast við þessum beiðnum skal nota **Hjálparforrit gagnaverndar** til að flytja út persónuleg gögn í Excel-skrá eða RapidStart-grunnstillingapakka. Með því að nota Excel er hægt að breyta persónulegum gögnum og vista þau á algengu, vélalesanlegu sniði, eins og .csv eða .xml. Fyrir RapidStart-grunnstillingapakka er hægt að grunnstilla aðalgagnatöflur og tengdar töflur sem innihalda persónuleg gögn. <br><br> **Athugið:** Þegar gögn eru flutt út þarf að tilgreina lágmarksstig trúnaðar. Útflutningur mun innihalda lágmarksstigið og öll stigin þar fyrir ofan. Til dæmis, ef þú velur að flytja gögn sem eru flokkuð sem persónuleg, mun útflutningurinn einnig innihalda gögn sem eru flokkuð sem viðkvæm. <br><br>Við útflutning gagna sem tengjast skráðum einstaklingi leitar **Hjálparforrit gagnaverndar** að beinum venslum milli skráðs einstaklings og gagna sem tengjast honum. Óbein vensl milli gagna sem tengjast skráðum einstaklingi og annarra gagna eru ekki flutt sjálfkrafa út af **Hjálparforriti gagnaverndar**. Til dæmis hefur tengiliðataflan beintengd gögn tengiliðasvara forstillingar og tafla tengiliðasvara forstillingar tengist enn fremur gögnum forstillingarspurninga. Ef þú vilt einnig flytja út forstillingarspurningar verður þú að bæta þessari töflu við handvirkt sem röð með viðeigandi síum úr grunnstillingarpakkanum sem **Hjálparforrit gagnaverndar** býr til.|
|Beiðni um eyðingu|Skráður aðili getur óskað eftir því að þú eyðir persónulegum gögnum. Það eru nokkrar leiðir til að eyða persónulegum gögnum með því að nota sérstillingarmöguleikana, en ákvörðun og framkvæmd er á þína ábyrgð. Í sumum tilfellum er hægt að velja að breyta gögnunum beint, til dæmis með því að eyða tengilið og þá keyra runuvinnsluna Eyða samskiptum sem hætt er við til að eyða samskiptum við tengiliðinn. <br><br> **Athugið:** Ef búið er að tilgreina dagsetningu í reitinn **Leyfa eyðingu skjals** fyrir á síðunni **Uppsetning sölu og útistandandi** eða **Uppsetning innkaupa & viðskiptaskulda** getur verið að það þurfi að breyta dagsetningunni þannig að hægt sé að eyða bókuðum sölu- og innkaupaskjölum sem hafa verið prentuð og sem hafa bókunardagsetningar á eða fyrir þessa dagsetningu.|
|Beiðnir um leiðréttingu|Skráður aðili getur óskað eftir því að ónákvæm persónuleg gögn verði leiðrétt. Hægt er gera það á nokkra vegu: Í sumum tilfellum er hægt að flytja út lista í Excel til að magnbreyta margar skrár á fljótlegan hátt og síðan flytja inn uppfærðu gögnin. Frekari upplýsingar eru í [Flytja út viðskiptagögn í Excel](about-export-data.md). Einnig er hægt að breyta reitum handvirkt sem innihalda persónuleg gögn, t.d. með því að breyta upplýsingum um viðskiptavin í viðskiptamannaspjaldinu. Hins vegar eru færsluskrár eins og almennar, viðskiptavinir og skattafjárhagsfærslur nauðsynlegar fyrir áreiðanleika skipulagsáætlunar fyrirtækisins. Ef þú geymir persónuleg gögn í viðskiptafærsluskrám skaltu íhuga að nota sérstillingarmöguleikana til að breyta slíkum persónulegum gögnum.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Takmarka gagnavinnslu fyrir skráðan aðila
Skráður aðili getur óskað eftir því að þú hættir tímabundið með vinnslu á persónulegum gögnum hans. Til að heiðra slíkar beiðnir er hægt að merkja færslur þeirra sem lokaðar vegna persónuverndar til að hætta að vinna úr gögnum þeirra. Þegar skrá er merkt sem lokuð er ekki hægt að búa til nýjar færslur sem nota þessa færslu. Til dæmis getur þú ekki búið til nýjan reikning fyrir viðskiptavini þegar annað hvort viðskiptavinurinn eða seljandi er lokaður. Til að merkja skráðan aðila sem læstan skal opna spjaldið fyrir skráða aðilann, t.d. spjald viðskiptavinar, lánardrottins eða tengiliðs og velja gátreitinn **Lokað fyrir vegna persónuverndar**. Þú gætir þurft að velja **Sýna fleiri** til að birta reitinn.  

## <a name="handling-data-subject-requests-while-in-trial"></a>Að meðhöndla beiðnir skráðra einstaklinga í prufuútgáfu
Ákveðnar gerðir persónuupplýsinga eru hluti af Office 365 reikningnum þínum og krefst stjórnunaraðgangs til að flytja út ef þú færð beiðni skráðs einstaklings frá notanda varðandi þessa tegund persónuupplýsinga samkvæmt almennu persónuverndarreglugerðinni (GDPR). Ferlið sem nær utan um beiðnir skráðs einstaklings fer eftir gerð [!INCLUDE[d365fin](includes/d365fin_md.md)] leigjandans.  

Ef þú hefur greitt áskrift fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] verður þú að hafa samband við handhafastjóra fyrirtækisins til að búa til beiðni skráðs einstaklings. Stjórnandi hefur stjórnunarréttindi og verkfæri til að uppfylla beiðni þína.  

Ef þú skráðir þig fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] frá síðunni [Prufuáskriftir](https://trials.dynamics.com/) og þú hefur ekki fært þig úr þessari áskriftarupplifun yfir í greidda áskrift fyrir tilstuðlan handhafastjóra fyrirtækisins, þá getur þú útfyllt þína eigin beiðni skráðs einstaklings á [Persónuverndarsíðu vinnu og skóla í Azure-gáttinni](https://portal.azure.com#blade/Microsoft_AAD_IAM/GDPRViralBlade). Hér getur þú flutt út og sótt persónuupplýsingar þínar.

Á persónuverndarsíðu vinnu og skóla geturðu einnig lokað reikningnum þínum. Hins vegar mælum við með því að þú tryggir að þú hafir flutt út og eytt öllum gögnum fyrst, þar sem að eyða reikningnum þínum þýðir að þú missir aðgang að [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Þú getur samt merkt fólk sem útilokað vegna persónuverndar og útflutnings, breytt eða eytt færslum eins og lýst er annars staðar í þessari grein.  

## <a name="exporting-data-from-tables-not-classified-by-data-subject"></a>Flytur út gögn frá töflum sem eru ekki flokkaðar eftir skráðum aðila
Ef kringumstæður eru þannig að þú þarft að flytja út gögn sem eru ekki flokkuð á þann hátt að þau séu sjálfkrafa flutt út, svo sem gögn úr svörunartöflu forstillingar, verður þú að gera eftirfarandi: 
-   Íhugaðu hvort þú í raun viljir eða þurfir að flytja þessi viðbótargögn sem tengjast ekki tengiliðnum, sem þýðir að það hefur engin bein tengsl við hann 
-   Bættu þessari töflu og venslum handvirkt við Rapid Start pakkann og flyttu hann beint út frá Rapid Start pakkanum - þetta er ástæðan fyrir því að við búum til Rapid Start pakka handa þér, svo þú getir fínpússað hann í aðstæðum líkt og þessum.

## <a name="handling-data-about-minors"></a>Meðhöndlun gagna um börn
Ef tengiliðar er undir lögaldri samkvæmt lögum á þínu svæði getur þú bent á það með því að velja gátreitinn **Barn** á spjaldinu **Tengiliður**. Þegar þú gerir það verður gátreiturinn **Lokað fyrir vegna persónuverndar** valinn sjálfkrafa. Þegar þú færð samþykki foreldris eða forráðamanns getur þú valið gátreitinn **Samþykki foreldra fengið** til að opna aftur á tengiliðinn. Þó að þú getir unnið úr persónulegum gögnum fyrir ólögráða einstakling, getur þú ekki notað lýsingaraðgerðina í Microsoft Dynamics 365 for Sales.

> [!Note]
> Breytingaskráin getur skráð upplýsingar eins og hvenær og af hverjum gátreiturinn **Samþykki foreldra fengið** var valinn. Stjórnandi getur sett það upp með því að nota leiðarvísinn **Uppsetning breytingaskrár** og einnig velja gátreitinn **Skrá breytingar á fengnu samþykki foreldris** á spjaldinu **Tengiliður**. Frekari upplýsingar eru í [Skráning breytinga](across-log-changes.md).  

## <a name="see-also"></a>Sjá einnig
[Gagnaflokkun](/dynamics-nav/classifying-data?toc=/dynamics365/business-central/toc.json)  
[Flokkun gagnatrúnaðar](admin-classifying-data-sensitivity.md)  
[Flutningur viðskiptagagna í Excel](about-export-data.md)  
[Skráning breytinga](across-log-changes.md)  
[Beiðni skráðs einstaklings fyrir almennu persónuverndarreglugerðinni](/microsoft-365/compliance/gdpr-data-subject-requests)  

