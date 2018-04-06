---
title: "Svara beiðnum um persónuleg gögn"
description: "Þú verður að bregðast við beiðnum skráðra aðila."
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.date: 03/13/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 89f53f24f74401ce384b54d04fbeb473aedad96d
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---

# <a name="responding-to-requests-about-personal-data"></a>Svara beiðnum um persónuleg gögn  
Skráðir aðilar geta óskað eftir nokkrum tegundum aðgerða varðandi persónuupplýsingar þeirra. Ef þú hefur flokkað viðkvæmni gagna og ert viss um að þau séu rétt, getur kerfisstjóri brugðist við beiðnum með því að nota vinnublað gagnaflokkunnar í Mitt hlutverk **Stjórna notendum, notendaflokkar og heimildir** eða, ef þú notar Windows-biðlarann, í Mitt hlutverk **Tæknistjóri**. Nánari upplýsingar um gagnaflokkun og flokkun á gagnatrúnaði er að finna í [Gagnaflokkun](/dynamics-nav/classifying-data) og [Flokkun á gagnatrúnaði](admin-classifying-data-sensitivity.md).

Eftirfarandi tafla veitir dæmi um tegundir beiðna sem þú getur svarað.

> [!Note]
> Þó að við bjóðum upp á möguleika til að bregðast við slíkum beiðnum og þar með aðgang að persónulegum gögnum er það á þína ábyrgð að tryggja að persónuleg og viðkvæm gögn séu staðsett og flokkuð á viðeigandi hátt.

|Tegund beiðni|Lýsing og leiðbeinandi svar|
|-----|-----|
|Flutningsbeiðni|Skráður aðili getur gert gagnaflutningsbeiðni, sem þýðir að hluta til að þú verður að flytja persónuleg gögn skráðs aðila úr þínu kerfi og senda það á skipulögðu, algengu sniði. Til að bregðast við þessum beiðnum skal nota hjálparforrit gagnaverndar til að flytja út persónuleg gögn í Excel-skrá. Með því að nota Excel er hægt að breyta persónulegum gögnum og vista þau á algengu, vélalesanlegu sniði, eins og .csv eða .xml. Stjórnendur geta einnig flutt gögn út með því að nota Rapid Start grunnstillingapakka og þá grunnstilla aðalgagnatöflur og tengdar töflur sem innihalda persónuleg gögn. |
|Beiðni um eyðingu|Skráður aðili getur óskað eftir því að þú eyðir persónulegum gögnum. Það eru nokkrar leiðir til að eyða persónulegum gögnum með því að nota sérstillingarmöguleikana, en ákvörðun og framkvæmd er á þína ábyrgð. Í sumum tilfellum er hægt að velja að breyta gögnunum beint, til dæmis með því að eyða tengilið og þá keyra runuvinnsluna Eyða samskiptum sem hætt er við til að eyða samskiptum við tengiliðinn. <br><br> **Athugið:** Ef búið er að tilgreina dagsetningu í reitinn **Leyfa eyðingu skjals** fyrir á síðunni **Uppsetning sölu og útistandandi** eða **Uppsetning innkaupa & viðskiptaskulda** getur verið að það þurfi að breyta dagsetningunni þannig að hægt sé að eyða bókuðum sölu- og innkaupaskjölum sem hafa verið prentuð og sem hafa bókunardagsetningar á eða fyrir þessa dagsetningu.|
|Beiðnir um leiðréttingu|Skráður aðili getur óskað eftir því að ónákvæm persónuleg gögn verði leiðrétt. Hægt er gera það á nokkra vegu: Í sumum tilfellum er hægt að flytja út lista í Excel til að magnbreyta margar skrár á fljótlegan hátt og síðan flytja inn uppfærðu gögnin. Frekari upplýsingar eru í [Flytja út viðskiptagögn í Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data). Einnig er hægt að breyta reitum handvirkt sem innihalda persónuleg gögn, t.d. með því að breyta upplýsingum um viðskiptavin í viðskiptamannaspjaldinu. Hins vegar eru færsluskrár eins og almennar, viðskiptavinir og skattafjárhagsfærslur nauðsynlegar fyrir áreiðanleika skipulagsáætlunar fyrirtækisins. Ef þú geymir persónuleg gögn í viðskiptafærsluskrám skaltu íhuga að nota sérstillingarmöguleikana til að breyta slíkum persónulegum gögnum.|

## <a name="restrict-data-processing-for-a-data-subject"></a>Takmarka gagnavinnslu fyrir skráðan aðila
Skráður aðili getur óskað eftir því að þú hættir tímabundið með vinnslu á persónulegum gögnum hans. Til að heiðra slíkar beiðnir er hægt að merkja færslur þeirra sem lokaðar vegna persónuverndar til að hætta að vinna úr gögnum þeirra. Þegar skrá er merkt sem lokuð er ekki hægt að búa til nýjar færslur sem nota þessa færslu. Til dæmis getur þú ekki búið til nýjan reikning fyrir viðskiptavini þegar annað hvort viðskiptavinurinn eða seljandi er lokaður. Til að merkja skráðan aðila sem læstan skal opna spjaldið fyrir skráða aðilann, t.d. spjald viðskiptavinar, lánardrottins eða tengiliðs og velja gátreitinn **Lokað fyrir vegna persónuverndar**. Þú gætir þurft að velja **Sýna fleiri** til að birta reitinn.

## <a name="handling-data-about-minors"></a>Meðhöndlun gagna um börn
Ef tengiliðar er undir lögaldri samkvæmt lögum á þínu svæði getur þú bent á það með því að velja gátreitinn **Barn** á spjaldinu **Tengiliður**. Þegar þú gerir það verður gátreiturinn **Lokað fyrir vegna persónuverndar** valinn sjálfkrafa. Þegar þú færð samþykki foreldris eða forráðamanns getur þú valið gátreitinn **Samþykki foreldra fengið** til að opna aftur á tengiliðinn. Þó að þú getir unnið úr persónulegum gögnum fyrir ólögráða einstakling, getur þú ekki notað lýsingaraðgerðina í Microsoft Dynamics 365 for Sales.

> [!Note]
> Breytingaskráin getur skráð upplýsingar eins og hvenær og af hverjum gátreiturinn **Samþykki foreldra fengið** var valinn. Stjórnandi getur sett það upp með því að nota leiðarvísinn **Uppsetning breytingaskrár** og einnig velja gátreitinn **Skrá breytingar á fengnu samþykki foreldris** á spjaldinu **Tengiliður**. Frekari upplýsingar eru í [Skráning breytinga](/dynamics-nav-app/across-log-changes).  

## <a name="see-also"></a>Sjá einnig
[Gagnaflokkun](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data)  
[Flokkun gagnatrúnaðar](admin-classifying-data-sensitivity.md)  
[Flutningur viðskiptagagna í Excel](https://docs.microsoft.com/en-us/dynamics-nav-app/about-export-data)  

