---
title: Jafna greiðslur á Ógreidd söluskjöl
description: Þú jafna upphæðir greiddar af viðskiptamönnum við tengt söluskjal og bóka svo greiðsluna til að uppfæra viðskiptamann, fjárhag og bankafærslur.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts, customer payment
ms.search.form: 1290, 1294, 1287
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f11eeacd21d39a9b816fa763ae333fc4cb4efd54
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606587"
---
# <a name="reconcile-customer-payments-from-a-list-of-unpaid-sales-documents"></a>Afstemma greiðslur viðskiptamanna úr lista yfir ógreidd söluskjöl

Eftir að Viðskiptavinir taka rafrænar greiðslur inn á bankareikninginn sinn þarf að grípa til eftirfarandi aðgerða:

* Nota hverja greidda upphæð á tengda söluskjali
* Bókið greiðsluna til að uppfæra viðskiptamanninn, fjárhag og bankareikningsfærslur. 

Það fer eftir þörfum fyrirtækis þíns, þú getur fengið greitt og skráð þessi greiðslu á mismunandi vegu: handvirkt, sjálfkrafa og með greiðsluþjónustu.  

> [!NOTE]  
> Þú getur framkvæmt sömu verk, þar á meðal greiðslur lánardrottins á síðunni **greiðsluafstemmingarbók** með því að nota aðgerð fyrir innflutning bankayfirlits, sjálfvirk jöfnun, og afstemming bankareiknings. Frekari upplýsingar eru í [afstemma greiðslur með því að nota sjálfvirk jöfnun](receivables-how-reconcile-payments-auto-application.md)

**Notið stöðu innri reikninga viðskiptavinagreiðslna** fyrir skrá viðskiptavinar með því að nota raunverulegar sjóðstölur til að tryggja að greiðslum sé safnað. Fljótlegt er að sannreyna og bóka stakar eða Samtala greiðslna, vinna úr launagreiðslum og finna ógreidda skjölin.

Greiðslur fyrir mismunandi viðskiptamenn, sem hafa mismunandi borgunardagsetningu, verður að bóka sem einstaka greiðslur. Greiðslur fyrir sama viðskiptamann, sem hafa sömu greiðsludagsetningu, er hægt að bóka sem fastagreiðslu. Moll-samtölugreiðslur eru gagnlegar, t.d. þegar viðskiptamaður hefur gert staka greiðslu sem nær til margra sölureikninga.

## <a name="to-set-up-the-payment-registration-journal"></a>Uppsetning greiðsluskráningarbókar
Þar sem hægt er að bóka nokkrar greiðslutegundir á nokkra mótreikninga verður að velja mótreikning á síðunni **Uppsetning skráningar greiðslna** áður en greiðslur viðskiptamanns eru unnar. Ef alltaf er bókað á sama mótreikninginn, er hægt að stilla þann reikning sem sjálfgefinn og forðast þetta skref í hvert sinn sem síðan **Skrá greiðslur viðskiptamanna** er opnuð.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning greiðsluskráningar** og velja síðan viðkomandi tengil. Einnig er hægt að **Velja uppsetningaraðgerðina** á **síðunni skrá viðskiptavinagreiðslur**.
2. Reitirnir á síðunni **Uppsetning skráningar greiðslna** eru fylltir út. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)] Veljið reit til að lesa stutta lýsingu á svæðinu eða tengja við tengdar upplýsingar.  

> [!TIP]
> Til að auðvelda síðar að auðkenna færslur sem voru bókaðar í gegnum færslubókina er hægt að úthluta tilteknum númeraröð til færslubókarinnar. Þetta er gagnlegt ef greiðsluafstemmingabækur eru notaðar til að skrá og jafna greiðslur.

## <a name="to-register-customer-payments-individually"></a>Til að skrá greiðslur viðskiptamanna hverja fyrir sig

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skrá greiðslur viðskiptavina** og velja síðan viðkomandi tengil.  

    Síðan **Skrá greiðslur viðskiptamanns** sýnir öll bókuð skjöl sem hægt er að skrá greiðslu fyrir. Einnig er hægt að opna síðuna á **kortasíðum** viðskiptavina **og** viðskiptavina þar sem hún er sjálfkrafa síuð fyrir tilgreindan viðskiptavin.  
2. Veljið gátreitinn **greiðsla framkvæmd** á línunni sem stendur fyrir bókaða fylgiskjalið sem borgun hefur verið gerð fyrir.

    Ef gátreiturinn **sjálfvirk útfylling dagsetningar móttöku** er valinn á síðunni **uppsetning skráning greiðslna**, fyllist vinnudagsetningin út í reitnum **dagsetning móttöku**.  
3. Í reitnum **dagsetning móttöku**, færið inn dagsetninguna sem greiðslan var gerð á. Þessi dagsetning má vera önnur en vinnudagsetningin.  
4. Í reitnum **móttekin upphæð**, færið inn upphæðina sem hefur verið greidd.

    Fyrir fullar greiðslur er upphæðin sú sama og í reitnum Eftirstöðvar **í þessari upphæð í** línunni. Fyrir hlutagreiðslur er þessi upphæð lægri en upphæðin í reitnum Eftirstöðvar **í** línunni.
5. Endurtakið skref 2-4 fyrir aðrar línur sem standa fyrir bókuð skjöl þar sem greiðslur er gerðar á.  
6. Valið er **bóka Greiðslur** aðgerð.  

Greiðsluupplýsingarnar eru bókaðar í fylgiskjölum og sýndar sem línur þar sem gátreiturinn **Greiðsla framkvæmd** er valinn.  

Greiðslufærslur eru bókaðar í fjárhags-, banka- og viðskipta- eða viðskiptamannareikningum. Hver greiðsla er jöfnuð við tengt bókað söluskjal.  

## <a name="to-reconcile-lump-sum-payments"></a>Að stemma af fastagreiðslur
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluskráning** og velja síðan viðkomandi tengil.
2. Veljið gátreitinn **Greiðsla framkvæmd** í línunum sem standa fyrir bókuðu fylgiskjölin fyrir sama viðskiptamanninn sem fastagreiðsla hefur verið gerð fyrir.  

    > [!NOTE]  
    >   Viðskiptamaðurinn í reitnum **Nafn** verður að vera eins í öllum línum sem verða bókaðar sem fastagreiðsla.  

    Ef gátreiturinn **sjálfvirk útfylling dagsetningar móttöku** er valinn á síðunni **uppsetning skráning greiðslna** fyllist vinnudagsetningin út í reitnum **dagsetning móttöku**.  
3. Í reitnum **dagsetning móttöku**, færið inn dagsetninguna sem greiðslan var gerð á. Þessi dagsetning má vera önnur en vinnudagsetningin.  

    > [!NOTE]  
    >   Þessi dagsetning verður að vera sú sama í öllum línum sem verða bókaðar sem fastagreiðslur.  
4. Í reitnum **móttekin greiðsla**, færið inn upphæðir á margar línur sem ná samanlagt upp í fastagreiðsluupphæðina.  

    > [!TIP]  
    > Reynið að bóka eins margar fullnaðargreiðslur og mögulegt er í fastagreiðslunni. Færa inn upphæðir sem eru þær sömu og upphæðin í reitnum **Eftirstandandi upphæð** á eins margar línur og mögulegt er.  
5. Endurtakið skref 2-4 fyrir aðrar línur sem standa fyrir bókuð skjöl fyrir sama viðskiptamann eða lánardrottin sem fastagreiðsla hefur verið gerð fyrir.  
6. Valið er **bóka sem fastgreiðslu** aðgerð. Innfærðar Greiðsluupplýsingarnar eru bókaðar í fylgiskjölum og sýndar sem línur þar sem gátreiturinn **Greiðsla framkvæmd** er valinn.  

Greiðslufærslur eru bókaðar í fjárhags-, banka- og viðskiptavinalykil. Hver greiðsla er jöfnuð við tengt bókað söluskjal.  

Ef greiðsla í banka er ekki táknuð með línu á **Greiðsluskráningarsíðu** getur það verið vegna þess að tengt skjal hefur ekki enn verið bókað. Í því tilviki, er hægt að nota leitareiginleika til að finna skjalið hratt og bóka það til að meðhöndla greiðsluna. Sjá [til að finna sérstakt söluskjal sem ekki er fyllilega reikningsfært](#to-find-a-specific-sales-document-that-isnt-fully-invoiced) fyrir frekari upplýsingar.  

Ef greiðsla í banka er ekki táknuð með skjali í [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að opna forfylltar færslubók af **greiðsluskráningarsíðu** til að bóka greiðsluna beint á mótlykilinn án þess að jafna greiðsluna við skjal. Að öðrum kosti er hægt að skrá greiðsluna í færslubókina þar til uppruni greiðslunnar hefur verið leystur. Frekari upplýsingar eru í [Að skráð eða bóka greiðslu án tengdra fylgiskjala](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-record-or-post-a-payment-without-a-related-document).  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Meðhöndla greiðslur með afslætti handvirkt
Ef þú hefur samið um staðgreiðsluafslátt hjá viðskiptavini þá geta greiðsluupphæðirnar verið lægri en upphæðir reikningsins ef greiðsla á sér stað fyrir umsaminn afsláttardag.  

Eftirfarandi verklagsreglur útskýra fjórar mismunandi leiðir til að bóka afgreiðu greiðslur á **Greiðsluskráningarsíðunni**.  

* Greiðsluupphæðin er jöfn hinni eftirstandandi afsláttarupphæð og dagsetning greiðslunnar er fyrir afsláttardagsetninguna. Greiðslan er bókuð eins og hún er.  
* Greiðsluupphæðin er jöfn hinni eftirstandandi afsláttarupphæð, en dagsetning greiðslunnar er eftir afsláttardagsetninguna. Greiðslan er bókuð sem hlutagreiðsla. Fylgiskjalið er áfram opið til að innheimta/borga eftirstandandi upphæð. Einnig er hægt að stilla afsláttardagsetninguna síðar til að hægt sé að heimila greiðsluna að fullu.  
* Greiðsluupphæðin er lægri en hin eftirstandandi afsláttarupphæð. Greiðslan er bókuð sem hlutagreiðsla. Fylgiskjalið er áfram opið til að innheimta/borga eftirstandandi upphæð.  
* Greiðsluupphæðin er hærri en hin eftirstandandi afsláttarupphæð. Greiðslan er bókuð eins og hún er. Aðeins eftirstandandi upphæð er bókuð. Viðbótarupphæðin er kreditfærð á viðskiptamanninn.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Meðhöndlun greiðsluupphæðar sem er jöfn afsláttarupphæðinni og dagsetning greiðslunnar er fyrir afsláttardagsetninguna.
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluskráning** og velja síðan viðkomandi tengil.  
2. Færa inn reikningsupphæðina í reitinn **Móttekin upphæð**. Upphæðin er jöfn upphæðinni í reitnum **Eftirstöðvar eftir afslátt**.

    Gátreiturinn **Greiðsla framkvæmd** er valinn sjálfvirkt og reiturinn **Dagsetning móttöku** fyllist út með vinnudagsetningunni.    
3. Færa inn reikningsupphæðina í reitinn **Móttökudagsetning**. Dagsetninguna ber upp á undan dagsetningunni í reitnum **Dagsetning greiðsluafsláttar**.
4. Staðfestið að reiturinn **Eftirstandandi upphæð** inniheldur núll (0).  
5. Veldu **bóka greiðslur** aðgerðina til að bóka alla greiðsluna í fjárhag, banka og viðskiptavinalykla.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Meðhöndlun greiðsluupphæðar sem er jöfn afsláttarupphæðinni og dagsetning greiðslunnar er fyrir afsláttardagsetninguna
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluskráning** og velja síðan viðkomandi tengil.  
2. Færa inn reikningsupphæðina í reitinn **Móttekin upphæð**. Upphæðin er jöfn upphæðinni í reitnum **Eftirstöðvar eftir afslátt**.

    Gátreiturinn **Greiðsla framkvæmd** er valinn sjálfvirkt og reiturinn **Dagsetning móttöku** fyllist út með vinnudagsetningunni.
3. Í reitnum **dagsetning móttöku**, færið inn dagsetningu greiðslu sem ber upp eftir dagsetningunni í reitnum **dagsetning greiðsluafsláttar**. Dagsetningareitum breytt í rauða leturgerð og villuboð birtast neðst á síðunni.

    > [!TIP]  
    >   Ef veita á undanþágu og gefa afslátt jafnvel þótt greiðslan berist seint, fylgið þessum skrefum:
4. Valið er **Sundurliðun** aðgerð.  
5. Á síðunni **upplýsingar um skráning greiðslna** í reitnum **dagsetning greiðsluafsláttar** á Flýtiflipanum **Greiðsluafsláttur**, setjið inn dagsetningu sem ber upp á eftir dagsetninguna í reitnum **dagsetning móttöku** á síðunni **skráning greiðslna**.  

    Villuboðin og Rauða Leturgerðin hverfa og hægt er að halda áfram að vinna úr ógreiðugreiðslunni.    
6. Staðfestið að reiturinn **Eftirstandandi upphæð** inniheldur upphæðina sem eftir á að greiða af allri reikningsupphæðinni.  
7. Veldu **bóka greiðslur** aðgerðina til að bóka hlutagreiðslu í fjárhag, banka og viðskiptavinalykla.  

Viðkomandi fylgiskjal er enn opið.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Meðhöndlun greiðsluupphæðar sem er lægri en hin eftirstandandi afsláttarupphæð
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluskráning** og velja síðan viðkomandi tengil.  
2. Færa inn reikningsupphæðina í reitinn **Móttekin upphæð**. Upphæðin er lægri en upphæðin í reitnum **Eftirstöðvar eftir afslátt**.

    Gátreiturinn **Greiðsla framkvæmd** er valinn sjálfvirkt og reiturinn **Dagsetning móttöku** fyllist út með vinnudagsetningunni.  
3. Færa inn reikningsupphæðina í reitinn **Móttökudagsetning**. Dagsetninguna ber upp á undan dagsetningunni í reitnum **Dagsetning greiðsluafsláttar**.
4. Staðfestið að reiturinn **Eftirstandandi upphæð** inniheldur upphæðina sem eftir á að greiða af allri reikningsupphæðinni.  
5. Veldu **bóka greiðslur** aðgerðina til að bóka hlutagreiðslu í fjárhag, banka og viðskiptavinalykla.  

Viðkomandi fylgiskjal er enn opið.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Meðhöndlun greiðsluupphæðar sem er hærri en hin eftirstandandi afsláttarupphæð
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluskráning** og velja síðan viðkomandi tengil.  
2. Færa inn reikningsupphæðina í reitinn **Móttekin upphæð**. Upphæðin er hærri en upphæðin í reitnum **Eftirstöðvar eftir afslátt**.  

    Gátreiturinn **Greiðsla framkvæmd** er valinn sjálfvirkt og reiturinn **Dagsetning móttöku** fyllist út með vinnudagsetningunni.    
3. Færa inn reikningsupphæðina í reitinn **Móttökudagsetning**. Dagsetninguna ber upp á undan dagsetningunni í reitnum **Dagsetning greiðsluafsláttar**.
4. Staðfestið að reiturinn **Eftirstandandi upphæð** inniheldur núll (0).  
5. Veldu **bóka greiðslur** aðgerðina til að bóka alla greiðsluna í fjárhag, banka og viðskiptavinalykla.  

Viðkomandi fylgiskjal er lokað og umframgreiðsluupphæðin er færð á viðskiptamanninn.  

## <a name="to-find-a-specific-sales-document-that-isnt-fully-invoiced"></a>Til að finna ákveðið söluskjal sem ekki er fyllilega reikningsfært
Síðunni **Skráning greiðslna** er ætlað að veita aðstoð í verkum sem þarf til að stemma af innanhúsreikninga með raunverulegum sjóðstölum til að tryggja skilvirka söfnun frá viðskiptamönnum. Það sýnir útistandandi væntanlega innkomu á línum sem tákna söluskjöl þar sem upphæð er fallinn á gjalddaga.  

Venjulega, ef greiðsla hefur verið gerð, skráð í bankanum eða á annan hátt, eru tengd sölu eða innkaupaskjöl sýnd sem lína á síðunni **Skráning greiðslna** þar sem fylgiskjalið sem um ræðir bíður eftir að greiðslan sé bókuð gegn hinni útstandandi upphæð. Stundum er hins vegar greiðsla sem hefur verið gerð ekki táknuð með línu á **Greiðsluskráningarsíðu**, yfirleitt vegna þess að skjalið sem um ræðir hefur ekki verið bókað að fullu.

**Á leitarsíðu** skjalsins er hægt að leita að skjölum sem ekki eru fyllilega reikningsfærð. Hægt er framkvæma leit út frá einu eða fleiri eftirfarandi gildum:  

* Númer skjals  
* Upphæð eða svið upphæðar  

Eftirfarandi aðgerð útskýrir hvernig skal finna tiltekið fylgiskjal með því að nota bæði leitarskilyrðin.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluskráning** og velja síðan viðkomandi tengil.
2. Með bendilinn á hvaða línu sem er, veldu aðgerðina **Leita í fylgiskjölum**.
3. Á síðunni **Leit í Skjölum**, færið inn leitargildi í reitinn **Númer fylgiskjals**.  

    > [!NOTE]  
    >   Faldir algildisstafir eru meðfylgjandi í gildinu sem fært er í þennan reit. Þetta þýðir að aðgerðin leitar eftir öllum fylgiskjalsnúmerum sem innihalda gildið sem fært var inn.    
4. Í reitnum **Upphæð**, tilgreinið ákveðna upphæð sem er til á fylgiskjalinu sem finna skal.  
5. Í reitnum **Upphæð vikmarka %**, færið inn prósentugildi til að skilgreina svið upphæða sem leita á eftir til að finna opna fylgiskjalið.  

    Ef fært er inn 10, þá leitar aðgerðin að upphæðum í bilinu 10 prósentum lægri og 10 prósentum hærra en gildið í **reitnum Upphæð**.    
6. Valið er **leita** aðgerð.  

Leitaraðgerðin leitar á milli skjala sem ekki eru fyllilega reikningsfærð miðað við tilgreindar forsendur.  

Ef fleiri en eitt fylgiskjal svarar leitarskilyrðunum, opnast síðan **Niðurstöður skjalaleitar** sem sýnir línur sem tilgreina viðkomandi fylgiskjöl. Í hverri línu er númer fylgiskjals, Lýsing og upphæð. Þessar upplýsingar auðvelda leit að tilteknu skjali.

Ef greiðsla í bankanum er ekki táknuð með neinu skjali í [!INCLUDE[prod_short](includes/prod_short.md)], þá er hægt að opna forfylltar færslubók af **greiðsluskráningarsíðu** til að bóka greiðsluna beint á mótlykilinn án þess að jafna greiðsluna við skjal. Að öðrum kosti er hægt að skrá greiðsluna í færslubókina þar til uppruni greiðslunnar hefur verið leystur.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Greiðslur skráðar eða bókaðar án tengdra fylgiskjala
Ef greiðsla í banka er ekki táknuð með neinu skjali í [!INCLUDE[prod_short](includes/prod_short.md)], þá er hægt að opna forfyllta færslubókarlínu af **greiðsluskráningarsíðu** til að bóka greiðsluna beint á mótlykilinn án þess að jafna greiðsluna við skjal. Að öðrum kosti er hægt að skrá greiðsluna í færslubókina þar til uppruni greiðslunnar hefur verið skýrður.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluskráning** og velja síðan viðkomandi tengil.
2. Valið er **Færslubók** aðgerð.  

    **Síðan almenna færslubók** opnast með eina línu sem inniheldur mótlykil bókarkeyrslunnar sem er sett upp á **síðu greiðsluskráningaruppsetningar**.  
3. Reitirnir sem eftir eru eru fylltir út í færslubókarlínunni. Til dæmis er kveðið á um upphæð, viðskiptamannanúmer eða upplýsingar úr bankayfirliti. Frekari upplýsingar, sjá [Bóka færslu beint yfir í Fjárhag](finance-how-post-transactions-directly.md).  

Hægt er að bóka færslubókarlínuna til að uppfæra samtölu mótreikningsins. Einnig er hægt að skilja færslubókarlínuna un bókaðan og bæta henni við með athugasemd um að greiða þurfi meiri greiningu.  

Ef færslubókarlínan er óbókuð, bætir hún við gildinu úr reitnum **óbókuð staða** neðst á síðunni **skráning greiðslna**.  

## <a name="see-also"></a>Sjá einnig
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]