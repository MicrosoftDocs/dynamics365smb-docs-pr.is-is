---
title: Jafna greiðslur við ógreidd söluskjöl
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606587"
---
# <a name="reconcile-customer-payments-from-a-list-of-unpaid-sales-documents"></a>Afstemma greiðslur viðskiptamanna úr lista yfir ógreidd söluskjöl

Eftir að viðskiptamenn framkvæma rafræna greiðslu á bankareikninginn þinn þarftu að grípa til eftirfarandi aðgerða:

* Jafna hverja greidda upphæð við tengt söluskjal
* Bókaðu greiðsluna til að uppfæra viðskiptamanna-, fjárhags og bankafærslur. 

Það fer eftir þörfum fyrirtækis þíns, þú getur fengið greitt og skráð þessi greiðslu á mismunandi vegu: handvirkt, sjálfkrafa og með greiðsluþjónustu.  

> [!NOTE]  
> Þú getur framkvæmt sömu verk, þar á meðal greiðslur lánardrottins á síðunni **greiðsluafstemmingarbók** með því að nota aðgerð fyrir innflutning bankayfirlits, sjálfvirk jöfnun, og afstemming bankareiknings. Frekari upplýsingar eru í [afstemma greiðslur með því að nota sjálfvirk jöfnun](receivables-how-reconcile-payments-auto-application.md)

Notaðu stöðu innri reikninga á síðunni **Skrá greiðslur viðskiptamanna** með því að nota raunverulegt reiðufé til að tryggja að greiðslur séu innheimtar. Hægt er að staðfesta og bóka einstakar eða fastar greiðslur, vinna úr greiðslum með afslætti og finna ógreidd skjöl.

Greiðslur fyrir mismunandi viðskiptamenn, sem hafa mismunandi borgunardagsetningu, verður að bóka sem einstaka greiðslur. Greiðslur fyrir sama viðskiptamann, sem hafa sömu greiðsludagsetningu, er hægt að bóka sem fastagreiðslu. Fastar greiðslur eru gagnlegar til dæmis ef viðskiptamaður hefur gert staka greiðslu sem nær yfir marga sölureikninga.

## <a name="to-set-up-the-payment-registration-journal"></a>Uppsetning greiðsluskráningarbókar
Þar sem hægt er að bóka nokkrar greiðslutegundir á nokkra mótreikninga verður að velja mótreikning á síðunni **Uppsetning skráningar greiðslna** áður en greiðslur viðskiptamanns eru unnar. Ef alltaf er bókað á sama mótreikninginn, er hægt að stilla þann reikning sem sjálfgefinn og forðast þetta skref í hvert sinn sem síðan **Skrá greiðslur viðskiptamanna** er opnuð.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning greiðsluskráningar** og velja síðan viðkomandi tengil. Einnig er hægt að velja aðgerðina **Setja upp** á síðunni **Skrá greiðslur viðskiptamanna**.
2. Reitirnir á síðunni **Uppsetning skráningar greiðslna** eru fylltir út. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)] Velja reit til að lesa inn stutta lýsingu á reitunum eða tengja við tengdar upplýsingar.  

> [!TIP]
> Til að auðvelda að bera kennsl á færslur sem voru bókaðar í gegnum færslubókina er hægt að úthluta færslubókinni tiltekinni númeraröð. Þetta er gagnlegt ef þú notar greiðsluafstemmingarbækur til að skrá og jafna greiðslur.

## <a name="to-register-customer-payments-individually"></a>Til að skrá greiðslur viðskiptamanna hverja fyrir sig

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skrá greiðslur viðskiptavina** og velja síðan viðkomandi tengil.  

    Síðan **Skrá greiðslur viðskiptamanns** sýnir öll bókuð skjöl sem hægt er að skrá greiðslu fyrir. Einnig er hægt að opna síðuna á síðunni **Viðskiptamenn** og **Viðskiptamannaspjald** þar sem hún er sjálfkrafa síuð fyrir tiltekinn viðskiptamann.  
2. Veljið gátreitinn **greiðsla framkvæmd** á línunni sem stendur fyrir bókaða fylgiskjalið sem borgun hefur verið gerð fyrir.

    Ef gátreiturinn **sjálfvirk útfylling dagsetningar móttöku** er valinn á síðunni **uppsetning skráning greiðslna**, fyllist vinnudagsetningin út í reitnum **dagsetning móttöku**.  
3. Í reitnum **dagsetning móttöku**, færið inn dagsetninguna sem greiðslan var gerð á. Þessi dagsetning má vera önnur en vinnudagsetningin.  
4. Í reitnum **móttekin upphæð**, færið inn upphæðina sem hefur verið greidd.

    Fyrir fullnaðargreiðslu er þetta sama og upphæðin í reitnum **Eftirstandandi upphæð** í línunni. Fyrir hlutagreiðslur er þetta lægri en upphæðin í reitnum **Eftirstandandi upphæð** á línunni.
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

Ef greiðsla í bankanum er ekki tilgreind með línu á síðunni **Greiðsluskráning** er það hugsanlega vegna þess að tengda skjalið hefur ekki verið bókað. Í því tilviki, er hægt að nota leitareiginleika til að finna skjalið hratt og bóka það til að meðhöndla greiðsluna. Frekari upplýsingar er að finna í [Til að finna tiltekið söluskjal sem er ekki reikningsfært að fullu](#to-find-a-specific-sales-document-that-isnt-fully-invoiced).  

Ef greiðsla í bankanum er ekki tilgreind með neinu fylgiskjali í [!INCLUDE[prod_short](includes/prod_short.md)], er hægt að opna fyrirfram útfyllta færslubók úr glugganum **Skráning greiðslna** til að bóka greiðsluna beint á mótreikninginn án þess að bóka greiðsluna í fylgiskjal. Að öðrum kosti er hægt að skrá greiðsluna í færslubókina þar til uppruni greiðslunnar hefur verið leystur. Frekari upplýsingar eru í [Að skráð eða bóka greiðslu án tengdra fylgiskjala](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-record-or-post-a-payment-without-a-related-document).  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Meðhöndla greiðslur með afslætti handvirkt
Ef samið hefur verið um greiðsluafslátt við viðskiptamanninn, getur greiðsluupphæðin verið lægri en reikningsupphæðin ef greiðslan á sér stað fyrir umsamda afsláttardagsetningu.  

Eftirfarandi ferli útskýrir fjórar mismunandi leiðir til að bóka greiðslur með afslætti á síðunni **Greiðsluskráning**.  

* Greiðsluupphæðin er jöfn hinni eftirstandandi afsláttarupphæð og dagsetning greiðslunnar er fyrir afsláttardagsetninguna. Greiðslan er bókuð eins og hún er.  
* Greiðsluupphæðin er jöfn hinni eftirstandandi afsláttarupphæð, en dagsetning greiðslunnar er eftir afsláttardagsetninguna. Greiðslan er bókuð sem hlutagreiðsla. Fylgiskjalið er áfram opið til að innheimta/borga eftirstandandi upphæð. Einnig er hægt að setja afsláttardagsetninguna síðar til leyfa greiðslu að fullu.  
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

    Villuboðin og rauða leturgerðin hverfa og nú er hægt að meðhöndla afsláttargreiðsluna.    
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

## <a name="to-find-a-specific-sales-document-that-isnt-fully-invoiced"></a>Að finna tiltekið söluskjal sem er ekki reikningsfært að fullu
Síðunni **Skráning greiðslna** er ætlað að veita aðstoð í verkum sem þarf til að stemma af innanhúsreikninga með raunverulegum sjóðstölum til að tryggja skilvirka söfnun frá viðskiptamönnum. Það sýnir útistandandi væntanlega innkomu á línum sem tákna söluskjöl þar sem upphæð er fallinn á gjalddaga.  

Venjulega, ef greiðsla hefur verið gerð, skráð í bankanum eða á annan hátt, eru tengd sölu eða innkaupaskjöl sýnd sem lína á síðunni **Skráning greiðslna** þar sem fylgiskjalið sem um ræðir bíður eftir að greiðslan sé bókuð gegn hinni útstandandi upphæð. Það getur hins vegar komið fyrir að greiðslur eru ekki sýndar sem línur á síðunni **Greiðsluskráning** yfirleitt því að umrætt skjal hefur ekki verið bókað að fullu.

Á síðunni **Skjalaleit** er hægt að leita meðal skjala sem ekki eru reikningsfærð að fullu. Hægt er framkvæma leit út frá einu eða fleiri eftirfarandi gildum:  

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

    Ef fært er inn 10 mun aðgerðin leita að upphæðum sem eru á milli tíu prósent lægri eða hærri en gildið í reitnum **Upphæð**.    
6. Valið er **leita** aðgerð.  

Leitareiginleikinn leitar í skjölum sem ekki eru enn reikningsfærð að fullu samkvæmt tilgreindum leitarskilyrðum.  

Ef fleiri en eitt fylgiskjal svarar leitarskilyrðunum, opnast síðan **Niðurstöður skjalaleitar** sem sýnir línur sem tilgreina viðkomandi fylgiskjöl. Í hverri línu er númer fylgiskjals, lýsing og upphæð. Þessar upplýsingar auðvelda leit að tilteknu skjali.

Ef greiðsla í bankanum er ekki tilgreind með fylgiskjali í [!INCLUDE[prod_short](includes/prod_short.md)], er hægt að opna fyrirfram útfyllta færslubók af síðunni **Skráning greiðslna** til að bóka greiðsluna beint á mótreikninginn án þess að bóka greiðsluna í fylgiskjal. Að öðrum kosti er hægt að skrá greiðsluna í færslubókina þar til uppruni greiðslunnar hefur verið leystur.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Greiðslur skráðar eða bókaðar án tengdra fylgiskjala
Ef greiðsla í bankanum er ekki til í formi neins skjals í [!INCLUDE[prod_short](includes/prod_short.md)] getur þú opnað færslubókarlínu sem þegar er útfyllt úr **Skráning greiðslna** síðunni til að bóka greiðsluna beint á mótreikninginn án þess að jafna greiðsluna á skjali. Að öðrum kosti er hægt að skrá greiðsluna í færslubókina þar til uppruni greiðslunnar hefur verið skýrður.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluskráning** og velja síðan viðkomandi tengil.
2. Valið er **Færslubók** aðgerð.  

    Síðan **Færslubók** opnast með einni línu sem inniheldur mótreikning bókarkeyrslunnar sem er sett upp á síðunni **Uppsetning greiðsluskráningar**.  
3. Fylltu út eftirstandandi reiti í færslubókarlínunni. Gefðu til dæmis upp upphæðina, viðskiptamannanúmerið eða upplýsingar úr bankayfirlitinu. Frekari upplýsingar, sjá [Bóka færslu beint yfir í Fjárhag](finance-how-post-transactions-directly.md).  

Hægt er að bóka færslubókarlínuna til að uppfæra heildarupphæðina á mótreikningnum. Einnig er hægt að skilja færslubókarlínuna eftir óbókaða og ef til vill bæta við athugasemd um að greiðslan þarfnist frekari skoðunar.  

Ef færslubókarlínan er óbókuð, bætir hún við gildinu úr reitnum **óbókuð staða** neðst á síðunni **skráning greiðslna**.  

## <a name="see-also"></a>Sjá einnig
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]