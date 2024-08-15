---
title: Jafna greiðslur við ógreidd söluskjöl
description: 'Þú jafna upphæðir greiddar af viðskiptamönnum við tengt söluskjal og bóka svo greiðsluna til að uppfæra viðskiptamann, fjárhag og bankafærslur.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts, customer payment'
ms.search.form: '1290, 1294, 1287'
ms.date: 07/08/2024
ms.service: dynamics-365-business-central
---

# <a name="reconcile-customer-payments-from-a-list-of-unpaid-sales-documents"></a>Stemma af greiðslur viðskiptamanns af lista yfir ógreidd söluskjöl

Eftir að viðskiptamenn framkvæma rafræna greiðslu á bankareikninginn þinn þarftu að grípa til eftirfarandi aðgerða:

* Jafna hverja greidda upphæð á tengda söluskjalið.
* Bókaðu greiðsluna til að uppfæra viðskiptamanna-, fjárhags og bankafærslur.

Hægt er að skrá greiðslur handvirkt, sjálfvirkt og með greiðsluþjónustu, allt eftir þörfum fyrirtækisins.  

> [!NOTE]  
> Hægt er að gera sömu verkhluta, þar á meðal greiðslur lánardrottna, á síðunni **Greiðsluafstemmingarbók** . Til dæmis er hægt að flytja inn bankayfirlit, nota sjálfvirka jöfnun og stemma af bankareikninga. Frekari upplýsingar eru í [afstemma greiðslur með því að nota sjálfvirk jöfnun](receivables-how-reconcile-payments-auto-application.md)

Nota síðuna **Skrá greiðslur viðskiptamanna** til að jafna innri reikninga með því að nota raunverulegar sjóðstölur til að tryggja að greiðslur séu innheimtar. Hægt er að staðfesta og bóka einstakar eða fastar greiðslur, vinna úr greiðslum með afslætti og finna ógreidd skjöl.

Bóka þarf greiðslur fyrir mismunandi viðskiptamenn sem hafa mismunandi greiðsludagsetningar sem einstakar greiðslur. Greiðslur fyrir sama viðskiptamann, sem hafa sömu greiðsludagsetningu, er hægt að bóka sem fastagreiðslu. Greiðslur með moltugreiðslum eru gagnlegar, til dæmis þegar viðskiptamaður greiðir eina greiðslu sem nær yfir marga sölureikninga.

## <a name="to-set-up-the-payment-registration-journal"></a>Uppsetning greiðsluskráningarbókar

Þar sem hægt er að bóka nokkrar greiðslutegundir á nokkra mótreikninga verður að velja mótreikning á síðunni **Uppsetning skráningar greiðslna** áður en greiðslur viðskiptamanns eru unnar. Ef alltaf er bókað á sama mótreikninginn, er hægt að stilla þann reikning sem sjálfgefinn og forðast þetta skref í hvert sinn sem síðan **Skrá greiðslur viðskiptamanna** er opnuð.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning greiðsluskráningar** og velja síðan viðkomandi tengil. Einnig er hægt að velja aðgerðina **Setja upp** á síðunni **Skrá greiðslur viðskiptamanna**.
2. Reitirnir á síðunni **Uppsetning skráningar greiðslna** eru fylltir út. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)].  

> [!TIP]
> Ef auðvelda á að auðkenna færslur sem voru bókaðar um bókina er hægt að úthluta tiltekinni númeraröð í útgreiðslubókina. Númeraröðin kemur að notum ef greiðsluafstemmingarbækur eru notaðar til að skrá og jafna greiðslur.

## <a name="to-register-customer-payments-individually"></a>Til að skrá greiðslur viðskiptamanna hverja fyrir sig

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skrá greiðslur viðskiptavina** og velja síðan viðkomandi tengil.  

    Síðan **Skrá greiðslur viðskiptamanns** sýnir öll bókuð skjöl sem hægt er að skrá greiðslu fyrir. Einnig er hægt að opna síðuna af síðunum **Viðskiptamenn** og **Viðskiptamannaspjald**, afmarkað fyrir tilgreindan viðskiptamann.  
2. Velja skal gátreitinn **Greiðsluskil í** línunni sem stendur fyrir bókaða fylgiskjalið sem greiðsla var innt af hendi fyrir.
3. Í reitnum **dagsetning móttöku**, færið inn dagsetninguna sem greiðslan var gerð á. Þessi dagsetning gæti verið önnur en vinnudagsetningin.  

   Ef gátreiturinn **Sjálfvirk móttökudags. móttöku** er valinn á síðunni **Uppsetning greiðsluskráningar** er vinnudagsetningin í reitnum **Dags. móttöku** .  
4. Í reitinn **Móttekin** upphæð er færð inn upphæðin sem var greidd.

    Fyrir fullnaðargreiðslu er þetta sama og upphæðin í reitnum **Eftirstandandi upphæð** í línunni. Fyrir hlutagreiðslur er þetta lægri en upphæðin í reitnum **Eftirstandandi upphæð** á línunni.
5. Skref 2-4 eru endurtekin fyrir aðrar línur fyrir bókuð fylgiskjöl sem greiðslur eru innt af hendi fyrir.  
6. Valið er **bóka Greiðslur** aðgerð.  

Greiðsluupplýsingarnar eru bókaðar fyrir fylgiskjöl í línum þar sem gátreiturinn **Greiðslutilboð** er valinn. Greiðslufærslur eru bókaðar í fjárhags-, banka- og viðskipta- eða viðskiptamannareikningum.

## <a name="to-reconcile-lump-sum-payments"></a>Að stemma af fastagreiðslur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skrá greiðslur viðskiptavina** og velja síðan viðkomandi tengil.
2. Velja skal gátreitinn Greiðsla **gerð** í línunum fyrir bókuð fylgiskjöl fyrir sama viðskiptamann og sem greiðsla með moltusamtölu var gerð fyrir.  

    > [!NOTE]  
    > Viðskiptamaðurinn í reitnum **Heiti** verður að vera sá sami í öllum línum til að hafa með í samtölugreiðslunni.  

    Ef gátreiturinn **Sjálfvirk móttökudags. móttöku** er valinn á síðunni **Uppsetning greiðsluskráningar** er vinnudagsetningin í reitnum **Dags. móttöku** .  
3. Í reitnum **dagsetning móttöku**, færið inn dagsetninguna sem greiðslan var gerð á. Þessi dagsetning gæti verið önnur en vinnudagsetningin.  

    > [!NOTE]  
    > Þessi dagsetning verður að vera sú sama í öllum línum sem verða bókaðar sem fastagreiðslur.  
4. Í reitnum **móttekin greiðsla**, færið inn upphæðir á margar línur sem ná samanlagt upp í fastagreiðsluupphæðina.  

    > [!TIP]  
    > Reynið að bóka eins margar fullnaðargreiðslur og mögulegt er í fastagreiðslunni. Færa inn upphæðir sem eru þær sömu og upphæðin í reitnum **Eftirstandandi upphæð** á eins margar línur og mögulegt er.  
5. Þrep 2-4 eru endurtekin fyrir aðrar línur sem standa fyrir bókuð fylgiskjöl fyrir sama viðskiptamann og greiðsla með moltusamtölu var framkvæmd fyrir.  
6. Valið er **bóka sem fastgreiðslu** aðgerð.

   Greiðsluupplýsingarnar eru bókaðar fyrir fylgiskjöl í línum þar sem gátreiturinn **Greiðslutilboð** er valinn. Greiðslufærslur eru bókaðar í fjárhags-, banka- og viðskiptavinalykil. Hver greiðsla er jöfnuð við tengt bókað söluskjal.  

Ef greiðsla í bankanum stendur ekki fyrir með línu á síðunni **Skrá greiðslur** viðskm. getur verið vegna þess að tengda skjalið er ekki bókað. Í því tilviki, er hægt að nota leitareiginleika til að finna skjalið hratt og bóka það til að meðhöndla greiðsluna. Frekari upplýsingar er að finna í [Til að finna tiltekið söluskjal sem er ekki reikningsfært að fullu](#to-find-a-specific-sales-document-that-isnt-fully-invoiced).  

Ef greiðsla í bankanum stendur ekki fyrir í fylgiskjali er hægt að opna fyrirframfyllta færslubók af síðunni **Skrá greiðslur viðskiptamanna** til að bóka greiðsluna beint á mótreikninginn án þess að jafna greiðsluna við fylgiskjal. Einnig er hægt að skrá greiðsluna í færslubókina þar til uppruni greiðslunnar er leystur. Frekari upplýsingar eru í [Að skráð eða bóka greiðslu án tengdra fylgiskjala](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-record-or-post-a-payment-without-a-related-document).  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Meðhöndla greiðslur með afslætti handvirkt

Ef samið er um greiðsluafslátt við viðskiptamann geta greiðsluupphæðir verið lægri en reikningsupphæðirnar ef greiðsla á sér stað fyrir umsaminn afsláttardag.  

Eftirfarandi ferli útskýra leiðir til að bóka afsláttargreiðslur á **síðunni Skráning** greiðslu.  

* Greiðsluupphæðin er jöfn hinni eftirstandandi afsláttarupphæð og dagsetning greiðslunnar er fyrir afsláttardagsetninguna. Greiðslan er bókuð eins og hún er.  
* Greiðsluupphæðin er jöfn hinni eftirstandandi afsláttarupphæð, en dagsetning greiðslunnar er eftir afsláttardagsetninguna. Greiðslan er bókuð sem hlutagreiðsla. Fylgiskjalið er áfram opið til að innheimta/borga eftirstandandi upphæð. Einnig er hægt að setja afsláttardagsetninguna síðar til leyfa greiðslu að fullu.  
* Greiðsluupphæðin er lægri en hin eftirstandandi afsláttarupphæð. Greiðslan er bókuð sem hlutagreiðsla. Fylgiskjalið er áfram opið til að innheimta/borga eftirstandandi upphæð.  
* Greiðsluupphæðin er hærri en hin eftirstandandi afsláttarupphæð. Greiðslan er bókuð eins og hún er. Aðeins eftirstandandi upphæð er bókuð. Viðbótarupphæðin er kreditfærð á viðskiptamanninn.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Meðhöndlun greiðsluupphæðar sem er jöfn afsláttarupphæðinni og dagsetning greiðslunnar er fyrir afsláttardagsetninguna.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skrá greiðslur viðskiptavina** og velja síðan viðkomandi tengil.  
2. Færa inn reikningsupphæðina í reitinn **Móttekin upphæð**. Upphæðin er jöfn upphæðinni í reitnum **Eftirstöðvar með afslátt.** 

    Gátreiturinn Útgreiddur **greiðslu** er sjálfkrafa valinn og **vinnudagsetningin er fyllt út í reitinn Dags. móttöku** .
3. Færa inn reikningsupphæðina í reitinn **Móttökudagsetning**. Dagsetninguna ber upp á undan dagsetningunni í reitnum **Dagsetning greiðsluafsláttar**.
4. Staðfestið að reiturinn **Eftirstandandi upphæð** inniheldur núll (0).  
5. Veldu **bóka greiðslur** aðgerðina til að bóka alla greiðsluna í fjárhag, banka og viðskiptavinalykla.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Meðhöndlun greiðsluupphæðar sem er jöfn afsláttarupphæðinni og dagsetning greiðslunnar er fyrir afsláttardagsetninguna

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skrá greiðslur viðskiptavina** og velja síðan viðkomandi tengil.  
2. Færa inn reikningsupphæðina í reitinn **Móttekin upphæð**. Upphæðin er jöfn upphæðinni í reitnum **Eftirstöðvar með afslátt.** 

    Gátreiturinn Útgreiddur **greiðslu** er sjálfkrafa valinn og **vinnudagsetningin er fyllt út í reitinn Dags. móttöku** .
3. Í reitnum **dagsetning móttöku**, færið inn dagsetningu greiðslu sem ber upp eftir dagsetningunni í reitnum **dagsetning greiðsluafsláttar**.

   Dagsetningareitum breytt í rauða leturgerð og villuboð birtast neðst á síðunni. Næstu tvö skref laga það.
4. Valið er **Sundurliðun** aðgerð.  
5. Á síðunni **Greiðsluskráningarupplýsingar**, í reitnum **Dagsetning** greiðsluafsláttar á **flýtiflipanum Greiðsluafsláttur**, er færð inn dagsetning sem er eftir dagsetninguna í **reitnum Dagsetning móttöku** á síðunni **Greiðsluskráningargrunnur** .  

    Villuboðin og rauða leturgerðin hverfa og nú er hægt að meðhöndla afsláttargreiðsluna.
6. Staðfestið að reiturinn **Eftirstandandi upphæð** inniheldur upphæðina sem eftir á að greiða af allri reikningsupphæðinni.  
7. Veldu **bóka greiðslur** aðgerðina til að bóka hlutagreiðslu í fjárhag, banka og viðskiptavinalykla.  

Viðkomandi fylgiskjal er enn opið.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Meðhöndlun greiðsluupphæðar sem er lægri en hin eftirstandandi afsláttarupphæð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skrá greiðslur viðskiptavina** og velja síðan viðkomandi tengil.  
2. Færa inn reikningsupphæðina í reitinn **Móttekin upphæð**. Upphæðin er lægri en upphæðin í reitnum **Endurm.upphæð með afslátt** .

    Gátreiturinn Útgreiddur **greiðslu** er sjálfkrafa valinn og **vinnudagsetningin er fyllt út í reitinn Dags. móttöku** .  
3. Færa inn reikningsupphæðina í reitinn **Móttökudagsetning**. Dagsetninguna ber upp á undan dagsetningunni í reitnum **Dagsetning greiðsluafsláttar**.
4. Staðfestið að reiturinn **Eftirstandandi upphæð** inniheldur upphæðina sem eftir á að greiða af allri reikningsupphæðinni.  
5. Veldu **bóka greiðslur** aðgerðina til að bóka hlutagreiðslu í fjárhag, banka og viðskiptavinalykla.  

Viðkomandi fylgiskjal er enn opið.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Meðhöndlun greiðsluupphæðar sem er hærri en hin eftirstandandi afsláttarupphæð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skrá greiðslur viðskiptavina** og velja síðan viðkomandi tengil.  
2. Færa inn reikningsupphæðina í reitinn **Móttekin upphæð**. Upphæðin er hærri en upphæðin í reitnum **Eftirstöðvar með afslátt** .  

    Gátreiturinn Útgreiddur **greiðslu** er sjálfkrafa valinn og **vinnudagsetningin er fyllt út í reitinn Dags. móttöku** .
3. Færa inn reikningsupphæðina í reitinn **Móttökudagsetning**. Dagsetninguna ber upp á undan dagsetningunni í reitnum **Dagsetning greiðsluafsláttar**.
4. Staðfestið að reiturinn **Eftirstandandi upphæð** inniheldur núll (0).  
5. Veldu **bóka greiðslur** aðgerðina til að bóka alla greiðsluna í fjárhag, banka og viðskiptavinalykla.  

Viðkomandi fylgiskjal er lokað og umframgreiðsluupphæðin er færð á viðskiptamanninn.  

## <a name="to-find-a-specific-sales-document-that-isnt-fully-invoiced"></a>Að finna tiltekið söluskjal sem er ekki reikningsfært að fullu

Síðan **Skrá greiðslur viðskiptamanna** styður þig í verkum sem þarf til að jafna innri reikninga með raunverulegum sjóðstölum til að tryggja skilvirka söfnun frá viðskiptamönnum. Það sýnir útistandandi væntanlega innkomu á línum sem tákna söluskjöl þar sem upphæð er fallinn á gjalddaga.  

Þegar greiðsla er innt af hendi, skráð í banka eða á annan hátt er sölu- eða innkaupaskjalið táknað sem lína á síðunni **Skrá greiðslur viðskiptamanna** . Fylgiskjalið bíður þess að bóka greiðsluna á útistandandi upphæð. Stundum táknar greiðsla sem var innt af hendi ekki með línu á síðunni **Skrá greiðslur viðskiptamanns**, yfirleitt vegna þess að skjalið er ekki fullkomlega reikningsfært.

Nota aðgerðina **Leitarskjöl** til að leita að skjölum sem eru ekki fullkomlega reikningsfærð. Hægt er framkvæma leit út frá einu eða fleiri eftirfarandi gildum:  

* Númer skjals  
* Upphæð eða svið upphæðar  

Eftirfarandi aðgerð útskýrir hvernig skal finna tiltekið fylgiskjal með því að nota bæði leitarskilyrðin.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skrá greiðslur viðskiptavina** og velja síðan viðkomandi tengil.
2. Með bendilinn á hvaða línu sem er, veldu aðgerðina **Leita í fylgiskjölum**.
3. Á síðunni **Leit í Skjölum**, færið inn leitargildi í reitinn **Númer fylgiskjals**.  

    > [!NOTE]  
    > Faldir algildisstafir eru meðfylgjandi í gildinu sem fært er í þennan reit. Það þýðir að aðgerðin leitar að öllum fylgiskjalsnúmerum sem innihalda innfært gildi.
4. Í reitinn **Upphæð** er færð inn upphæðin á fylgiskjalinu sem á að finna.  
5. Í reitnum **Upphæð vikmarka %**, færið inn prósentugildi til að skilgreina svið upphæða sem leita á eftir til að finna opna fylgiskjalið.  

    Ef fært er inn 10 leitar aðgerðin að upphæðum á bilinu plús eða mínus 10 prósent af gildinu í reitnum **Upphæð** .
6. Valið er **leita** aðgerð.  

Ef eitt eða fleiri skjöl uppfylla skilyrðin **opnast síðan Niðurstaða** skjalaleitar til að birta línur sem standa fyrir þessi skjöl. Í hverri línu er númer fylgiskjals, lýsing og upphæð.

Ef greiðsla í bankanum stendur ekki fyrir með fylgiskjali má nota áfyllta færslubók af síðunni **Skrá greiðslur viðskiptamanns** til að bóka greiðsluna beint á mótreikninginn án þess að jafna greiðsluna við fylgiskjal. Einnig er hægt að skrá greiðsluna í færslubókina þar til uppruni greiðslunnar er leystur.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Greiðslur skráðar eða bókaðar án tengdra fylgiskjala

Ef greiðsla í bankanum stendur ekki fyrir með fylgiskjali má nota aðgerðina **Færslubók** til að opna fyrirframfyllta færslubókarlínu af síðunni **Skrá greiðslur viðskiptamanns** . Nota færslubókina til að bóka greiðsluna beint á mótreikninginn án þess að jafna greiðsluna við fylgiskjal. Einnig er hægt að skrá greiðsluna í færslubókina þar til uppruni greiðslunnar er leystur.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skrá greiðslur viðskiptavina** og velja síðan viðkomandi tengil.
2. Valið er **Færslubók** aðgerð.  

    Síðan **Færslubók** opnast með einni línu sem inniheldur mótreikning bókarkeyrslunnar sem er sett upp á síðunni **Uppsetning greiðsluskráningar**.  
3. Fylltu út eftirstandandi reiti í færslubókarlínunni. Gefðu til dæmis upp upphæðina, viðskiptamannanúmerið eða upplýsingar úr bankayfirlitinu. Frekari upplýsingar, sjá [Bóka færslu beint yfir í Fjárhag](finance-how-post-transactions-directly.md).  

Hægt er að bóka færslubókarlínuna til að uppfæra heildarupphæðina á mótreikningnum. Einnig er hægt að láta bókarlínuna óbókaða og bæta henni við með athugasemd að greiðslna þurfi meiri greiningu.  

Ef færslubókarlínan er ekki bókuð er virði hennar bætt við gildið í reitnum **Eftirstöðvar með afslætti**  **á síðunni Skráning** greiðslu.  

## <a name="see-also"></a>Sjá einnig .

[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
