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
ms.date: 09/09/2020
ms.author: edupont
ms.openlocfilehash: 6816ba11203e697ff833b9ea96aa85139fbcffe9
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783602"
---
# <a name="use-job-queues-to-schedule-tasks"></a>Nota verkraðir til að tímaraða verkhlutum

Verkraðir í [!INCLUDE[d365fin](includes/d365fin_md.md)] gera notendum kleift að tímasetja og keyra tilteknar skýrslur og kótasöfn. Stilla má verk svo þau keyri einu sinni eða endurtekið. Til dæmis kann notandi að vilja keyra skýrslu yfir **Sölutölur sölumanns** vikulega, að rekja sölu sölumanns í hverri viku eða keyra kóðaeininguna **Framselja samþykktarbeiðnir** daglega, til að tryggja að skjöl safnist saman eða stífli verkflæðið á annan hátt.

Síðan **Verkraðarfærslur** birtir öll núverandi verk. Ef bætt er inn nýrri verkraðarfærslu sem á að tímasetja, er nauðsynlegt að tiltaka upplýsingar um tegund hlutarins sem þú vilt keyra, eins og t.d. skýrsla eða kóðasafn, og heiti og hlutkenni hlutarins sem keyra á. Einnig er hægt að bæta færibreytum við til að tilgreina virkni verkraðarfærslu. Til dæmis er hægt að bæta við færibreytu til að sent einungis bókaðar sölupantanir. Notandi verður að hafa heimild til að keyra skýrsluna eða kótasafnið; annars kemur upp villa þegar verkröðin er keyrð.  

Verkröðin getur haft margar færslur sem eru þau verk sem biðröð stjórnar og keyrir. Upplýsingar í færslunni tilgreina hvaða kótaeining eða skýrsla er keyrð, hvenær og hve oft færslan er keyrð, í hvaða flokki verkið er keyrt og hvernig það er keyrt.  

## <a name="to-set-up-background-posting-with-job-queues"></a>Að setja upp bókun í bakgrunni með verkraðir

Verkraðir eru áhrifaríkt verkfæri til að raða keyrslu viðskiptaferla í bakgrunni, t.d. þegar margir notendur reyna að bóka sölupantanir, en aðeins er hægt að vinna úr einni pöntun í einu.  

Eftirfarandi ferli lýsir hvernig setja á upp bakgrunnsbókun fyrir sölupantanir. Skrefin eru svipuð fyrir Kaup í innkaup.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölugrunnur** og veldu síðan tengda tengilinn.
2. Á síðunni **Uppsetning sölu og útistandandi** skal velja gátreitinn **Bóka með verkröð**.
3. Veldu **Flokkakóði verkraðar** svæðið tilgreindu síðan **SALESPOST** koðann.

    > [!NOTE]
    > Sum verk breyta sömu gögnum og ekki ætti að keyra þau samtímis þar sem það getur valdið árekstrum. Til dæmis munu bakgrunnsvinnslur fyrir söluskjöl reyna að breyta sömu gögnum á sama tíma. Verkraðarflokkar koma í veg fyrir að þessar gerðir árekstrar með því að tryggja að þegar ein vinnsla er keyrð muni önnur vinnsla sem tilheyrir sömu verkraðarflokki ekki keyra fyrr en henni lýkur. Til dæmis mun vinnsla sem tilheyrir flokki söluverkraðar bíða þar til öll önnur sölutengd verk eru búin. Verkraðarflokkur er tilgreindur á flýtiflipanum **Bókun í bakgrunni** á síðunni **Sölugrunnur**.
    >
    > [!INCLUDE[d365fin](includes/d365fin_md.md)] bíður upp á verkraðarflokka fyrir sölu, innkaup og bókun í fjárhag. Mælt er með því að eitt þessara, eða eitt þess sem er búið til, sé alltaf tilgreint. Ef bilanir koma upp vegna árekstra skal íhuga að setja upp flokk fyrir allar sölur, innkaup og bakgrunnsbókun í fjárhag.

    Ef þú vilt einnig að söluskjöl verði prentuð þegar þau eru bókuð skal velja gátreitinn **Bóka & Prenta með verkröð** á síðunni **Uppsetning sölu og útistandandi**.  

    > [!IMPORTANT]  
    > Ef þú setur upp verk sem mun bóka og prenta skjöl, og prentarinn sýnir svarglugga, svo sem beiðni um auðkennisupplýsingar eða viðvörun um að blek sé að klárast, bókast fylgiskjalið en prentast ekki út. Samsvarandi verkraðarfærsla rennur á endanum út á tíma og reiturinn **Staða** stillist á **Villa**. Ekki er mælt með notkun prentarauppsetningar sem krefst samskipta við svarglugga prentara samhliða bakgrunnsbókunar.

    Næst þegar söluskjöl eru bókuð þarf stofnar [!INCLUDE [prodshort](includes/prodshort.md)] sjálfkrafa verkraðarafærslu fyrir hvert fylgiskjal og keyrir vinnslurnar í bakgrunni, eina í einu.

4. Til að staðfesta að verkröðin vinni eins og búist er við skal bóka sölupöntun. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).

5. Yfirfara síðuna **Skrárfærslur verkraðar** ef tókst að bóka sölupöntun. Nánari upplýsingar eru í [Til að skoða stöðu eða villur í verkröð](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

## <a name="to-create-a-job-queue-entry-for-batch-posting-of-sales-orders"></a>Til að stofna færslu verkraðar fyrir bókun runu á sölupöntunum

Einnig er hægt að fresta bókunum þar til það hentar fyrirtækinu. Til dæmis getur það verið gagnlegt í fyrirtæki að keyra tilteknar vinnslur þegar flestum gagnafærslum fyrir daginn er lokið. Þú getur náð þessu fram með því að láta verkröðina keyra mismunandi bókunarskrár í runu, eins og t.d. skrárnar **Bókunarsölupantanir í runu**, **Fjöldabóka sölureikninga**, og Bókunarsölukreditreikningar í runu. [!INCLUDE[d365fin](includes/d365fin_md.md)] styður bakgrunnsbókun fyrir öll sölu-, innkaupa- og þjónustuskjöl.

Eftirfarandi ferli sýnir hvernig á að setja upp skýrsluna **Fjöldabóka sölupantanir** til að bóka sjálfkrafa sölupantanir kl. 16:00 á virkum dögum.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkraðarfærslur** og veldu síðan viðeigandi tengil.  
2. Valið er **Nýtt** aðgerð.  
3. Í reitnum **Gerð hlutar sem á að keyra** skal velja **Skýrsla**.  
4. Í reitnum **Kenni hlutar sem á að keyra**, skal velja 296, **Fjöldabóka sölupantanir**.

   Einnig er hægt að nota eftirfarandi skýrslur:
  
   * 900 **Fjölbóka samsetningarpantanir**
   * 497 **Fjöldabóka innkaupareikninga**
   * 496 **Fjöldabóka innkaupapantanir**
   * 498 **Fjöldabóka innk.kreditreikning**
   * 6665 **Fjöldabóka innkaupavöruskilapantanir**
   * 298 **Fjöldabóka sölukreditreikninga**
   * 297 **Fjöldabóka sölureikninga**
   * 296 **Fjöldabóka sölupantanir**
   * 6655 **Fjöldabóka söluvöruskilapantanir**
   * 6005 **Fjöldabóka kreditreikninga þjónustu**
   * 6004 **Fjöldabóka þjónustureikninga**
   * 6001 **Fjöldabóka þjónustupantanir**

5. Veldu gátreitinn **Beiðnisíða skýrslu**.
6. Á beiðnisíðunni **Fjöldabóka sölupantanir** skal skilgreina hvað er innifalið við sjálfvirka bókun á sölupöntunum og síðan velja hnappinn **Í lagi**.

    > [!IMPORTANT]
    > Munið að stilla strangar síur; annars bókar [!INCLUDE [prodshort](includes/prodshort.md)] öll skjöl, jafnvel þau sem ekki eru tilbúin. Íhugið að setja síu á svæðið **Staða** fyrir *Losað*, og síu á **Bókunardagsetning** fyrir gildið *.. í dag*. Nánari upplýsingar er að finna í [Flokkun, leit og síun](ui-enter-criteria-filters.md).
7. Veldu alla gátreitina frá **Keyra á mánudögum** til og með **Keyra á föstudögum**.
8. Í reitinn **Upphafstími** skal slá inn kl. 16:00.
9. Velja aðgerðina **Stilla stöðu á Tilbúin**.

Sölupantanir sem eru innan tilgreindra síu verða nú bókaðar í hverri viku kl. 16:00.

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
1. Úr skjalinu sem þú reyndir að bóka með verkröðinni skal velja bakgrunnsbókun **Staða verkraðar** sem mun innihalda **Villu**.
2. Fara skal yfir villuboðin og leysa vandann.

## <a name="the-my-job-queue-part"></a>Hlutinn fyrir Mína verkröð
Hlutinn **Mín verkröð** í hlutverkamiðstöðinni þinni sýnir færslur verkraða sem þú hefur byrjað á, en er enn ekki lokið. Að sjálfgefnu er hlutinn ekki sjáanlegur, þannig að þú veður að bæta honum inn í Hlutverkamiðstöðina þína. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).  

Sá hluti sýnir hvaða skjöl með auðkenni þitt í reitnum **Úthlutuð notandakenni** er verið að vinna úr eða eru í röð, þ.á.m. þau sem tengjast bakgrunnsbókun. Hlutinn gefur til kynna á svipstundu hvort um villu hafi verið að ræða við bókun skjals eða hvort það hafi verið villur í verkraðarfærslu. Hlutinn býður einnig upp á að hætta við bókun skjals ef hún er ekki í gangi.

### <a name="to-view-an-error-from-the-my-job-queue-part"></a>Til að skoða villu ú hlutanum Mín verkröð
1. Í færslu með stöðuna **Villa** skal velja aðgerðina **Sýna villu**.
2. Fara skal yfir villuboðin og leysa vandann.

## <a name="security"></a>Öryggi  
Verkraðarfærslur keyra á grundvelli heimilda. Þessar heimildir verða að leyfa framkvæmd skýrslunnar eða kóðaeiningarinnar.  

Þegar verkröð er virkjuð handvirkt er hún keyrð með notendaheimildum notandans. Þegar verkröð er virkjuð sem tímasett verkefni er hún keyrð með notendaheimildum notandans. Þegar verk er keyrt er það keyrt með notendaheimildum verkraðarinnar sem virkjar það. Hins vegar verður notandinn sem stofnaði verkraðarfærsluna einnig að hafa heimildir. Þegar verk er „Keyra í notandalotu“ (til dæmis í bakgrunnsbókun) er það keyrt með notendaheimildum notandans sem stofnaði verkið.  

> [!IMPORTANT]  
> Ef notað er SUPER-heimildasafnið sem fylgir með [!INCLUDE[d365fin](includes/d365fin_md.md)] hafa bæði þú og þínir notendur heimild til að keyra alla hluti. Í þessu tilfelli er aðgangur hvers notanda aðeins takmarkaður af heimildum fyrir gögn.  

## <a name="using-job-queues-effectively"></a>Að nota verkraðir á skilvirkan hátt  
Verkraðarfærsluskrá er með marga reiti sem hafa þann tilgang að setja færibreytur í codeunit sem tilgreind hefur verið til keyrslu með verkröð. Þetta þýðir einnig að kóðaeiningar sem á að keyra með verkröðinni verður að tilgreina með skránni Verkraðarfærsla sem færibreytur í **OnRun** rofanum. Þetta stuðlar að auknu öryggi, þar sem þetta kemur í veg fyrir að notendur keyri tilviljanakenndar kóðaeiningar gegnum verkröðina. Þurfi notandi að senda færibreytur í skýrslu er eina leiðin til að gera það að vefja skýrslukeyrslunni í kótaeiningu sem þáttar inntaksbreyturnar og skráir þær í skýrsluna fyrir keyrslu hennar.  

## <a name="scheduling-synchronization-between-d365fin-and-d365fin"></a>Tímastillir samstillingu á milli [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)]

Ef þú hefur samþætt [!INCLUDE[d365fin](includes/d365fin_md.md)] við [!INCLUDE[d365fin](includes/cds_long_md.md)] geturðu notað verkröðina til að tímasetja hvenær þú vilt samstilla gögn fyrir færslurnar sem þú ert með í viðskiptaforritunum tveimur. Samstillingarvinnslur geta einnig búið til nýjar færslur í áfangaforritinu til að passa við þær sem eru í upprunanum, allt eftir stefnu og reglum sem þú hefur skilgreint fyrir samþættingu. Ef Sölumaður stofnar til dæmis nýjan tengilið í [!INCLUDE[crm_md](includes/crm_md.md)] getur samstillingarvinnslan búið til þann tengilið fyrir tengdan sölumann í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar eru í [Áætla samstillingu milli Business Central og Dynamics 365 Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

## <a name="see-also"></a>Sjá einnig

[Stjórnun](admin-setup-and-administration.md)  
[Uppsetning Business Central](setup.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
