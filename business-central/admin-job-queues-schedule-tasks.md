---
title: "Tímasetja verk til að keyrast sjálfvirkt | Microsoft Docs"
description: "Tímasettum verkum er stjórnað af verkröðinni. Þessi verk keyra skýrslur og kóðaeiningar. Stilla má verk svo þau keyri einu sinni eða endurtekið."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: fae1b2937a3c06fc947dd3dbec529826322d035c
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="use-job-queues-to-schedule-tasks"></a>Nota verkraðir til að tímaraða verkhlutum
Verkraðir í [!INCLUDE[d365fin](includes/d365fin_md.md)] gera notendum kleift að tímasetja og keyra tilteknar skýrslur og kótasöfn. Stilla má verk svo þau keyri einu sinni eða endurtekið. Til dæmis kann notandi að vilja keyra skýrslu yfir **Sölutölur sölumanns** vikulega, að rekja sölu sölumanns í hverri viku eða keyra kóðaeininguna **Úrvinnsla þjónustupóstraðar** daglega, til að tryggja að tölvupóstur sem bíður á leið til viðskiptamanna, varðandi þjónustupantanir þeirra, sé sendur út tímanlega.  

## <a name="add-jobs-to-the-job-queue"></a>Bæta við verkum í verkröð.
Glugginn **Verkraðarfærslur** birtir öll núverandi verk. Ef bætt er inn nýrri verkraðarfærslu sem á að tímasetja, er nauðsynlegt að tiltaka upplýsingar um tegund hlutarins sem þú vilt keyra, eins og t.d. skýrsla eða kóðasafn, og heiti og hlutkenni hlutarins sem keyra á. Einnig er hægt að bæta færibreytum við til að tilgreina virkni verkraðarfærslu. Til dæmis er hægt að bæta við færibreytu til að sent einungis bókaðar sölupantanir. Notandi verður að hafa heimild til að keyra skýrsluna eða kótasafnið; annars kemur upp villa þegar verkröðin er keyrð.  

Einnig er hægt að velja afmörkun sem gildir í reitnum **Afmörkun flokks verkraðar**. Flokka verkraðar má nota til að flokka verk sem eru á listanum.

[!INCLUDE[d365fin](includes/d365fin_md.md)] keyrir verkin sjálfvirkt samkvæmt tilteknum tímasetningum fyrir hverja verkraðarfærslu. Þú getur einnig byrjað, stoppað og slegið verkraðarfærslu á frest handvirkt.

### <a name="log-files"></a>Kladdaskrár
Villur eru taldar upp í glugganum **Skráarfærslur verkraðar** sem þú getur farið inn í gegnum borðann. Einnig er hægt að leita úrræða vegna verkraðarvillna. Gögn sem verða til þegar verkröð er keyrð eru geymd í gagnagrunninum.  

### <a name="background-posting-with-job-queues"></a>Bókun í bakgrunni með verkraðir
Verkraðir eru áhrifaríkt verkfæri til að raða notkun viðskiptaferla í bakgrunni. Til dæmis gæti komið upp tilvik þar sem margir notendur reyna að bóka sölupantanir samtímis, en einungis er hægt að afgreiða eina pöntun í einu. Með því að setja upp bakgrunnsbókunarferli er hægt að setja bókanirnar í biðröð fyrir vinnslu í bakgrunni.  

 Einnig er hægt að á að áætla bókanir fyrir tíma hentugum fyrir fyrirtækið. Til dæmis getur það verið við hæfi í fyrirtæki notanda að keyra tilteknar vinnslur þegar flestum gagnafærslum fyrir daginn er lokið. Þú getur náð þessu fram með því að láta verkröðina keyra mismunandi bókunarskrár í runu, eins og t.d. skrárnar **Bókunarsölupantanir í runu**, **Bókunarsölureikningar í runu**, og **Bókunarsölukreditreikningar í runu**.  

 [!INCLUDE[d365fin](includes/d365fin_md.md)] styður bakgrunnsbókun fyrir eftirfarandi tegundir skjala:  

-   Sala: sölupöntun, vöruskilapöntun, kreditreikningur, reikningur  

-   Innkaup: innkaupapöntun, vöruskilapöntun, kreditreikningur, reikningur  

 Ef ekki er hægt að bóka sölupöntunina breytist staðan í **Villa** og þá er sölupöntuninni bætt við lista yfir sölupantanir sem notandinn mun meðhöndla.  

> [!NOTE]  
>  Þegar fylgiskjal hefur verið tímasett til bókunar og bókunarferlið hefst, mun það renna út sjálfkrafa eftir tvo klukkutíma ef bókunarferlið svarar ekki einhverra hluta vegna.  

Þú setur upp þessa notkun á verkröðinni í glugganum **Uppsetning Sala & Útistandandi** glugganum eða **Innkaup & Viðskiptaskuldir**, eftir því sem við á. Á flýtiflipanum **Bókun í bakgrunni** skal velja **Bóka skjöl gegnum verkröðgátreitinn** og síðan setja inn viðeigandi upplýsingar. Hér geturðu einnig notað **Flokkskóði verkraðar** reitinn til að keyra allar verkraðarfærslur með þeim kóða. Þú getur til dæmis notað **SöluBókun** flokk sem afmarkast á allar sölupantanir sem passa við hverja þá verkröð sem hefur sama flokkakóða.  

> [!IMPORTANT]  
>  Ef þú setur upp verk sem mun bóka og prenta skjöl, og prentarinn sýnir svarglugga, svo sem beiðni um auðkennisupplýsingar eða viðvörun um að blek sé að klárast, bókast fylgiskjalið en prentast ekki út. Samsvarandi verkraðarfærsla rennur á endanum út á tíma og reiturinn **Staða** stillist á **Villa**. Ekki er mælt með notkun prentarauppsetningar sem krefst samskipta við svarglugga prentara samhliða bakgrunnsbókunar.  

## <a name="use-the-my-job-queue-part"></a>Nota Mín Verkröð hlutann
Hlutinn **Mín verkröð** sýnir verkraðarfærslurnar sem notandi hefur hafið, en er ekki lokið enn. Að sjálfgefnu er hlutinn ekki sjáanlegur, þannig að þú veður að bæta honum inn í Hlutverkamiðstöðina þína. Frekari upplýsingar, sjá [Breyta grunnstillingum](ui-change-basic-settings.md).  

Í þessum hluta er hægt að sjá fylgiskjölin sem verið er að vinna úr eða þau sem eru í bið fyrir það sem auðkennið tilgreinir í reitnum **Úthlutað notandakenni**. Hlutinn hjálpar til við að halda utan um allar verkraðarfærslur, þar á meðal þær sem tengjast bakgrunnsbókun. Hlutinn gefur til kynna á svipstundu hvort um villu hafi verið að ræða við bókun skjals eða hvort það hafi verið villur í verkraðarfærslu. Hlutinn býður einnig upp á að hætta við bókun skjals ef hún er ekki í gangi.  

## <a name="security"></a>Öryggi  
Verkraðarfærslur keyra á grundvelli heimilda. Þessar heimildir verða að leyfa framkvæmd skýrslunnar eða kóðaeiningarinnar.  

Þegar verkröð er virkjuð handvirkt er hún keyrð með notendaheimildum notandans. Þegar verkröð er virkjuð sem tímasett verkefni er hún keyrð með notendaheimildum notandans. Þegar verk er keyrt er það keyrt með notendaheimildum verkraðarinnar sem virkjar það. Hins vegar verður notandinn sem stofnaði verkraðarfærsluna einnig að hafa heimildir. Þegar verk er „Keyra í notandalotu“ (til dæmis í Bakgrunnsbókun) er það keyrt með notendaheimildum notandans sem stofnaði verkið.  

> [!IMPORTANT]  
>  Ef notað er SUPER-heimildasafnið sem fylgir með [!INCLUDE[d365fin](includes/d365fin_md.md)] hafa bæði þú og þínir notendur heimild til að keyra alla hluti. Í þessu tilfelli er aðgangur hvers notanda aðeins takmarkaður af heimildum fyrir gögn.  

## <a name="using-job-queues-effectively"></a>Að nota verkraðir á skilvirkan hátt  
Verkraðarfærsluskrá er með marga reiti sem hafa þann tilgang að setja færibreytur í codeunit sem tilgreind hefur verið til keyrslu með verkröð. Þetta þýðir einnig að kóðaeiningar sem á að keyra með verkröðinni verður að tilgreina með skránni Verkraðarfærsla sem færibreytur í **OnRun** rofanum. Þetta stuðlar að auknu öryggi, þar sem þetta kemur í veg fyrir að notendur keyri tilviljanakenndar kóðaeiningar gegnum verkröðina. Þurfi notandi að senda færibreytur í skýrslu er eina leiðin til að gera það að vefja skýrslukeyrslunni í kótaeiningu sem þáttar inntaksbreyturnar og skráir þær í skýrsluna fyrir keyrslu hennar.  

## <a name="see-also"></a>Sjá einnig  
[Stjórnun](admin-setup-and-administration.md)  
[Uppsetning Business Central](setup.md)  

