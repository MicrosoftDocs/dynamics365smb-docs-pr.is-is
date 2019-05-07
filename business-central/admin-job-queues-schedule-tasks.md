---
title: Tímasetja verk til að keyrast sjálfvirkt | Microsoft Docs
description: Tímasettum verkum er stjórnað af verkröðinni. Þessi verk keyra skýrslur og kóðaeiningar. Stilla má verk svo þau keyri einu sinni eða endurtekið.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 1cf5b75bc63acfa07a90cda1d03f45579a0aa51d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "935376"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Nota verkraðir til að tímaraða verkhlutum
Verkraðir í [!INCLUDE[d365fin](includes/d365fin_md.md)] gera notendum kleift að tímasetja og keyra tilteknar skýrslur og kótasöfn. Stilla má verk svo þau keyri einu sinni eða endurtekið. Til dæmis kann notandi að vilja keyra skýrslu yfir **Sölutölur sölumanns** vikulega, að rekja sölu sölumanns í hverri viku eða keyra kóðaeininguna **Úrvinnsla þjónustupóstraðar** daglega, til að tryggja að tölvupóstur sem bíður á leið til viðskiptamanna, varðandi þjónustupantanir þeirra, sé sendur út tímanlega.

Síðan **Verkraðarfærslur** birtir öll núverandi verk. Ef bætt er inn nýrri verkraðarfærslu sem á að tímasetja, er nauðsynlegt að tiltaka upplýsingar um tegund hlutarins sem þú vilt keyra, eins og t.d. skýrsla eða kóðasafn, og heiti og hlutkenni hlutarins sem keyra á. Einnig er hægt að bæta færibreytum við til að tilgreina virkni verkraðarfærslu. Til dæmis er hægt að bæta við færibreytu til að sent einungis bókaðar sölupantanir. Notandi verður að hafa heimild til að keyra skýrsluna eða kótasafnið; annars kemur upp villa þegar verkröðin er keyrð.  

Verkröðin getur haft margar færslur sem eru þau verk sem biðröð stjórnar og keyrir. Upplýsingar í færslunni tilgreina hvaða kótaeining eða skýrsla er keyrð, hvenær og hve oft færslan er keyrð, í hvaða flokki verkið er keyrt og hvernig það er keyrt.  

## <a name="to-set-up-background-posting-with-job-queues"></a>Að setja upp bókun í bakgrunni með verkraðir
Verkraðir eru áhrifaríkt verkfæri til að raða keyrslu viðskiptaferla í bakgrunni, t.d. þegar margir notendur reyna að bóka sölupantanir, en aðeins er hægt að vinna úr einni pöntun í einu. Einnig er hægt að á að áætla bókanir fyrir tíma hentugum fyrir fyrirtækið. Til dæmis getur það verið við hæfi í fyrirtæki notanda að keyra tilteknar vinnslur þegar flestum gagnafærslum fyrir daginn er lokið.

Þú getur náð þessu fram með því að láta verkröðina keyra mismunandi bókunarskýrslur í runu, eins og t.d. skýrslurnar **Bókunarsölupantanir í runu**, **Bókunarsölureikningar í runu**, **Bókunarskilapöntun sölu í runu** og **Bókunarsölukreditreikningar í runu**. Frekari upplýsingar er að finna í [Að stofna færslu verkraðar fyrir bókun sölupöntunar í bakgrunni](admin-job-queues-schedule-tasks.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).  

[!INCLUDE[d365fin](includes/d365fin_md.md)] styður bakgrunnsbókun fyrir öll sölu-, innkaupa- og þjónustuskjöl.

Eftirfarandi ferli lýsir hvernig setja á upp bakgrunnsbókun fyrir sölupantanir. Skrefin eru svipuð fyrir innkaup og þjónustu.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning sölu & útistandandi** og veldu síðan tengda tengilinn.
2. Á síðunni **Uppsetning sölu og útistandandi** skal velja gátreitinn **Bóka með verkröð**.
3. Til að sía í verkraðarfærslum fyrir bókun sölupöntunar skal velja reitinn **Flokkakóði verkraðar** og velja flokkinn **Sölubókun**.

    Hlutur verkraðar, codeunit 88 **Bókun sölu í gegnum verkröð**, er stofnaður. Haltu áfram til að virkja hann á síðunni **Verkraðarfærslur**.
4. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkraðarfærslur** og veldu síðan viðeigandi tengil.
5. Á síðunni **Verkraðarfærslur** skal velja aðgerðina **Ný**.
6. Í reitnum **Gerð hlutar sem á að keyra** skal velja **Codeunit**.  
7. Í reitnum **Kenni hlutar til að keyra**, skal velja 88, **Bókun sölu í gegnum verkröð**.

    Engir aðrir reitir eiga við fyrir þessa atburðarás.
8. Velja aðgerðina **Stilla stöðu á Tilbúin**.
9. Til að staðfesta að verkröðin vinni eins og búist er við skal bóka sölupöntun. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).
10. Yfirfara síðuna **Skrárfærslur verkraðar** ef tókst að bóka sölupöntun. Nánari upplýsingar eru í [Til að skoða stöðu eða villur í verkröð](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Ef þú vilt einnig að söluskjöl verði prentuð þegar þau eru bókuð skal velja gátreitinn **Bóka & Prenta með verkröð** á síðunni **Uppsetning sölu og útistandandi**.  

> [!IMPORTANT]  
> Ef þú setur upp verk sem mun bóka og prenta skjöl, og prentarinn sýnir svarglugga, svo sem beiðni um auðkennisupplýsingar eða viðvörun um að blek sé að klárast, bókast fylgiskjalið en prentast ekki út. Samsvarandi verkraðarfærsla rennur á endanum út á tíma og reiturinn **Staða** stillist á **Villa**. Ekki er mælt með notkun prentarauppsetningar sem krefst samskipta við svarglugga prentara samhliða bakgrunnsbókunar.

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Til að stofna færslu verkraðar fyrir bókun runu á sölupöntunum
Eftirfarandi ferli sýnir hvernig á að setja upp skýrsluna **Fjöldabóka sölupantanir** til að bóka sjálfkrafa útgefnar sölupantanir kl. 16:00 á virkum dögum.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkraðarfærslur** og veldu síðan viðeigandi tengil.  
2. Valið er **Nýtt** aðgerð.  
3. Í reitnum **Gerð hlutar sem á að keyra** skal velja **Skýrsla**.  
4. Í reitnum **Kenni hlutar sem á að keyra**, skal velja 296, **Fjöldabóka sölupantanir**.
5. Veldu gátreitinn **Beiðnisíða skýrslu**.
6. Á beiðnisíðunni **Fjöldabóka sölupantanir** skal skilgreina hvað er innifalið við sjálfvirka bókun á sölupöntunum og síðan velja hnappinn **Í lagi**.
7. Veldu alla gátreitina frá **Keyra á mánudögum** til og með **Keyra á föstudögum**.
8. Í reitinn **Upphafstími** skal slá inn kl. 16:00.
9. Velja aðgerðina **Stilla stöðu á Tilbúin**.

Sölupantanir sem eru tilbúnar til bókunar verða nú bókaðar í hverri viku kl. 16:00.

> [!NOTE]
> Ef verkröðin getur ekki bókað sölupöntunina breytist staðan í **Villa** og er sölupöntuninni þá bætt við lista yfir sölupantanir sem notandinn verður að meðhöndla handvirkt. Nánari upplýsingar eru í [Til að skoða stöðu eða villur í verkröð](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Eftir að verkraðir eru settar upp og í keyrslu getur staðan breyst eins og fylgir hér á eftir innan hvers endurtekins tímabils:

* **Bið**  
* **Tilbúið**  
* **Í vinnslu**  
* **Villa**  
* **Lokið**  

Þegar verki lýkur er það fjarlægt af lista yfir færslur verkraðar nema það sé endurtekið verk. Ef um endurtekið verk er að ræða er reiturinn **Fyrsti upphafstími** stilltur til að sýna næsta áætlaða keyrslutíma verksins.  

## <a name="to-view-status-or-errors-in-the-job-queue"></a>Til að skoða stöðu eða villur í verkröð
Gögn sem verða til þegar verkröð er keyrð eru geymd í gagnagrunninum svo hægt sé að úrræðaleita villur verkraðar.

### <a name="to-view-status-for-any-job"></a>Til að skoða stöðu fyrir hvaða verk sem er
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkraðarfærslur** og veldu síðan viðeigandi tengil.
2. Á síðunni **Verkraðarfærslur** skal velja færslu verkraðar og síðan velja aðgerðina **Skráarfærslur**.  

### <a name="to-view-status-from-a-sales-or-purchase-document"></a>Til að skoða stöðu úr sölu- eða innkaupaskjali
1. Úr skjalinu sem þú reyndir að bóka með verkröðinni skal velja reitinn **Staða verkraðar** sem mun innihalda **Villu**.
2. Fara skal yfir villuboðin og leysa vandann.

## <a name="the-my-job-queue-part"></a>Hlutinn fyrir Mína verkröð
Hlutinn **Mín verkröð** í hlutverkamiðstöðinni þinni sýnir færslur verkraða sem þú hefur byrjað á, en er enn ekki lokið. Að sjálfgefnu er hlutinn ekki sjáanlegur, þannig að þú veður að bæta honum inn í Hlutverkamiðstöðina þína. Frekari upplýsingar, sjá [Breyta grunnstillingum](ui-change-basic-settings.md).  

Sá hluti sýnir hvaða skjöl með auðkenni þitt í reitnum **Úthlutuð notandakenni** er verið að vinna úr eða eru í röð, þ.á.m. þau sem tengjast bakgrunnsbókun. Hlutinn gefur til kynna á svipstundu hvort um villu hafi verið að ræða við bókun skjals eða hvort það hafi verið villur í verkraðarfærslu. Hlutinn býður einnig upp á að hætta við bókun skjals ef hún er ekki í gangi.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Til að skoða villu ú hlutanum Mín verkröð
1. Í færslu með stöðuna **Villa** skal velja aðgerðina **Sýna villu**.
2. Fara skal yfir villuboðin og leysa vandann.

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
[Breyta grundvallarstillingum](ui-change-basic-settings.md)  
