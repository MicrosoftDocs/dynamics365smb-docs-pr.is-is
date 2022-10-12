---
title: Afstemma greiðslur með sjálfvirkri jöfnun
description: Lýsir því hvernig á að stemma af greiðslur með sjálfvirkri jöfnun til að jafna greiðslur eða sjóðsinnhreyfingar tengdar opnum færslum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.search.form: 389, 1290, 1294, 1287
ms.date: 06/22/2022
ms.author: bholtorf
ms.openlocfilehash: 9ea8db70d5d9392977db2a3b418cccb7d8fa3f77
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605739"
---
# <a name="reconcile-payments-using-automatic-application"></a>Afstemma greiðslur með sjálfvirkri jöfnun

**Síðan Greiðsluafstemmingarbók** síða Tilgreinir greiðslur, annað hvort á innleið eða útleið, sem hefur verið skráð sem færslur á bankareikninginn þinn eða í greiðsluþjónustu. Hægt er að jafna greiðslurnar við tengda opna viðskiptamanna-, lánardrottna-og bankareikningsfærslur. Fært er inn í færslubókina með því að flytja bankayfirlit inn sem bankastraum eða skrá eða með því að færa inn færslur sem eru gerðar í gegnum greiðsluþjónustu.

> [!NOTE]
> Síðan býður upp á sjálfvirkar samsvörunaraðgerðir sem jafna greiðslur við tengdar opnar færslur þeirra sem byggja á samsvörun texta í bankayfirlitslínu (færslubókarlínu) við gögní einni eða fleiri opnum færslum. Athugaðu að þú getur skrifað yfir ráðlagðar sjálfvirkar jafnanir og þú getur valið að nota ekki sjálfvirkar jafnanir yfirhöfuð. Frekari upplýsingar er að finna í 7 skrefi.

Greiðsluafstemmingarbók er tengd einum bankareikningi í [!INCLUDE[prod_short](includes/prod_short.md)]. Bankareikningur stendur fyrir bankareikning á netinu þar sem greiðslufærslurnar eru skráðar. Allar opnar fjárhagsfærslur bankareiknings sem tengjast jöfnuðum fjárhagsfærslum viðskiptavinar eða lánardrottins verða lokaðar þegar þú velur **Bóka Greiðslur og stemma Af Bankareikninga** aðgerð. Bankareikninginn verður sjálfkrafa stemmdur af fyrir greiðslur sem bókaðar eru með færslubókinni.

Ef notuð **er síða Greiðsluafstemmingarbókar** til að skrá og jafna greiðslur viðskiptavina er hægt að setja upp færslubók til að nota tiltekna númeraröð. Í kjölfarið er hægt að tilgreina númeraröðina í **Greiðsluafstemmingunni nr. Raðreitinn** á bankareikningi. Ef notuð er sérhæfð númeraröð er auðveldara að auðkenna færslur sem bókaðar hafa verið í gegnum færslubókina.

Líkt og í öðrum færslubókum þegar bókaðar eru réttar færslur er hægt að bakfæra færslur sem voru bókaðar í gegnum greiðsluafstemmingarbókina á **síðunni Fjárhagsskráning**. Til dæmis gæti verið hægt að bakfæra færslur fyrir greiðslur sem voru notaðar á röngum viðskiptamanni. Fyrst þarf að jafna bókuðu viðskiptamannafærslur. Síðan er hægt að nota **aðgerðina bakfæra dagbók** á **síðunni fjárhagsdagbók** til að bakfæra færslubókina sem bókaði greiðslurnar. Á **síðunni bókaðar færslubækur er einnig hægt að nota** Afrita valdar línur í færslubókaraðgerð **til að bakfæra tilteknar línur úr bókaða Greiðsluafstemmdatímaritinu**. 

Þegar Sjálfvirk jöfnun [!INCLUDE[prod_short](includes/prod_short.md)] er notuð viðurkenna bankareikningsfærslur sem þegar hafa verið bókaðar sem auðveldar að koma í veg fyrir tvíbókun.

Hægt er að flytja inn bankafærslur sem .csv-bankaskrár eða annað snið sem bankinn veitir. Ef flytja á bankayfirlit inn sem bankastrauma verður fyrst að gera sérhjálpandi bankasamþættingarþjónustu og tengja síðan bankareikninginn við tengda veflykil. greiðsluafstemmingarbók greinir síðan sjálfkrafa bankastreymi þegar þú velur aðgerðina **flytja inn bankafærslur**. Þar að auki er hægt að setja upp bankareikning til að flytja sjálfkrafa inn ný bankayfirlitsstreymi á hverri klukkustund. Færslur fyrir greiðslur sem þegar hafa verið bókaðar sem jafnaðar og/eða afstemmdar verða ekki fluttar inn. Hægt er að nota Envestnet Yodlee Bank Feeds þjónustuna til að fá þau viðskipti sem er foruppsett í sumum landútgáfum af [!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar eru í [Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md). Einnig getur Microsoft samstarfsaðila aðstoðað við að uppfylla kröfur fyrirtækja eða lands.

Aðgerðinni **varpa texta á reikning** gerir notendum kleift að hægt að setja upp vörpun á milli texta í greiðslum og tiltekinni debet-, kredit- og mótreikninga til að greiðslurnar séu bókaðar í tiltekna reikninga þegar greiðsluafstemmingarbók er bókuð. Vörpun er gagnleg t.d. fyrir endurteknar peningamóttökur eða útgjöld, svo sem tíðari innkaup á bílaeldsneyti eða bankagjöld og vexti, sem koma reglulega fram á bankayfirlitinu og þurfa ekki tengt viðskiptaskjal. (Sjá skref 10) Frekari upplýsingar er að finna [í Kortatexta á endurteknum greiðslum á lykla fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Færslubókarlínur geta ekki lagt inn umsókn, sem getur komið til af ýmsum ástæðum. Til dæmis vegna þess að skjal vantar, eða ofgreitt fyrir viðskiptavin og það er umframupphæð eftir að greiðslan hefur verið jöfnuð í annarri færslubókarlínu. Fyrir slík tilvik er hægt að nota aðgerðina **Flytja mismun á reikning** til að stofna og bóka fjárhagsfærsluna sem vantar, t.d. vegna endurgreiðslu, sem þarf til að jafna greiðsluna. (Sjá skref 11) Frekari upplýsingar er að finna [í Afstemmingargreiðslum sem ekki er hægt að nota.](receivables-how-reconcile-payments-cannot-apply-auto.md).

Þú notar aðgerðina **Sjálfvirk jöfnun**, annaðhvort sjálfvirkt þegar þú flytur inn bankaskrá eða streymi með greiðslufærslum eða þegar þú virkjar hana, til að jafna greiðslur við tengdar opnar færslur sem byggja á samsvörun texta á bankayfirlitslínu (færslubókarlínu) við texta í einni eða fleiri opnum færslum. Þessi sjálfvirkni er byggð á reglum sem eru skilgreindar á síðunni **Greiðslujöfnunarreglur** þar sem einnig er skilgreint hvort tillaga að jöfnun þarfnast yfirferðar. Frekari upplýsingar eru í [Setja upp reglur fyrir sjálfvirka jöfnun á greiðslum](receivables-how-set-up-payment-application-rules.md).

Á færslubókarlínum þar sem greiðsla hefur verið jöfnuð sjálfvirkt við eina eða fleiri opnar færslur hefur reiturinn **Áreiðanleiki samsvörunar** gildið **Lágt**, **Miðlungs** eða **Hátt** til að tilgreina gæði gagnasamsvörunar sem ráðlögð greiðslujöfnun er byggð á.

Sumar greiðslujafnanir þarfnast yfirferðar þinnar eins og það er skilgreint af notaðri samsvörunarreglu, t.d. línur með **Lágan** áreiðanleika samsvörunar. Aðrar línur krefjast skoðunar og handvirkrar breytingar því það er gildi í **reitnum Mismunur**. Til að yfirfara eina eða fleiri greiðslujafnanir skal velja reitinn **Línur til yfirferðar** eða **Línur með mismun** neðst. Síðan **Yfirferð greiðslujöfnunar** opnast og sýnir allar viðeigandi upplýsingar um viðskiptamann eða lánardrottin sem greiðslan er jöfnuð við, samsvörunarupplýsingarnar og aðgerðr til að afgreiða línuna, t.d. aðgerðina **Jöfnun**. (Sjá skref 7 og 8)

Fyrir hverja færslubókarlínu í **greiðsluafstemmingarbók** síðunni geturðu opnað **greiðslujafnanir** síðuna til að sjá alla möguleika opinna færslna fyrir greiðsluna og skoðað ítarlegar upplýsingar fyrir hverja færslu um gagnasamsvaranir sem greiðslujöfnun byggir á. Hér er hægt að jafna handvirkt greiðslur eða endurjafna greiðslur sem voru jafnaðar sjálfkrafa á ranga færslu. (Sjá skref 10) Frekari upplýsingar er að finna [í Review eða jafna greiðslum eftir sjálfvirka jöfnun](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Hægt er að hefja bankafærsluinnflutninginn á sama tíma og síðan **Greiðsluafstemmingarbók** er opnuð fyrir fyrirliggjandi bók. Eftirfarandi ferli lýsir því hvernig á að flytja inn bankafærslur á síðuna **greiðsluafstemmingarbók** eftir að ný færslubók hefur verið búin til.

## <a name="to-reconcile-payments-using-automatic-application"></a>Til að afstemma greiðslur með sjálfvirk jöfnun
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluafstemmingarbækur** og velja síðan viðkomandi tengil.
2. Til að vinna í nýrri greiðsluafstemmingarbók, veldu aðgerðina **Ný færslubók**.
3. Á síðunni **Listi yfir bankareikninga fyrir greiðslu** er valið bankareikningur sem á að jafna greiðslur fyrir, og smellt síðan á **Í lagi** hnappinn.
   Síðan **Greiðsluafstemmingarbók** opnast undirbúin fyrir valdan bankareikning.
4. Veldu aðgerðina **Flytja inn bankafærslur**
   Ef bankareikninginn fyrir völdu færslubókina er ekki settur upp fyrir innflutning á bankafærslum [!INCLUDE[d365fin](includes/d365fin_md.md)] mun það hjálpa til við að gera það.
5. Á síðunni **Velja skrá til að flytja inn** skal velja skrána sem inniheldur bankafærslurnar fyrir greiðslurnar sem á að stemma af og velja svo hnappinn **Opna**.  
6. Ef Envestnet Yodlee Bank Feeds þjónustan er virk, á síðunni **Bankayfirlitssía** sem opnast sjálfkrafa, skal tilgreina dagsetningarbil fyrir bankayfirlit sem á að flytja inn.

    Síðan **Greiðsluafstemmingarbók** er fyllt út með línum fyrir greiðslur sem tákna bankafærslur í innflutta bankayfirliti.

     Í línum fyrir greiðslur sem hafa verið sjálfkrafa jafnaðar tengdum opnum færslum **sýnir reiturinn samsvörun traust** gæði gagnajöfnunarinnar sem tillaga um greiðslu er byggð á. **Einnig reikningsheiti**, **reikningagerð** og **Reikningur nr.** reitirnir Sýna upplýsingar um viðskiptavininn eða lánardrottininn sem greiðslan er jöfnuð við.

    Sjálfvirkar umsóknir, jöfnunareiginleikar og hvort línur krefjast endurskoðunar er stjórnað eftir reglum. Hægt er að breyta reglunum til að leiðrétta niðurstöðurnar. Frekari upplýsingar eru í [Setja upp reglur fyrir sjálfvirka jöfnun á greiðslum](receivables-how-set-up-payment-application-rules.md).

7. Til að yfirfara, samþykkja/fjarlægja eða breyta mörgum greiðslujöfnunum handvirkt sem eru með gildi í reitnum **Mismunur** skal velja aðgerðina **Línur með mismun** neðst.

    Á **endurskoðunarsíðu** greiðsluumsóknar opnast og sýnir fyrsta umsókn til yfirferðar. Næsta jöfnun sem á að yfirfara verður sýnd á síðunni þegar sú fyrri er afgreidd. Endurskoðunin inniheldur upplýsingar um viðskiptavin eða lánardrottinn sem greiðslan er jöfnuð við, jöfnunarupplýsingar og aðgerðir til að vinna línuna, eins og **Samþykkja forritið** og **beita handvirkum** aðgerðum.

8. Til að yfirfara, samþykkja eða fjarlægja eða breyta mörgum greiðsluforritum sem reglan hefur stillt á að yfirfara skal velja **línurnar til að yfirfara** Aðgerðir. 

9. Til að breyta handvirkri jöfnun skaltu velja færslubókarlínuna og svo skaltu velja **Jafna handvirkt** til að endurskoða, endurjafna eða jafna greiðsluna handvirkt á síðunni **greiðslujafnanir**. Frekari upplýsingar eru í [Endurskoða eða sækja um greiðslur eftir sjálfvirkan umsókn](receivables-how-review-apply-payments-auto-application.md).

10. Veljið ójafnaða greiðslubókarlínu fyrir ítrekaða inngreiðslu eða kostnað, eins og kaup bensín á bíl, og veljið síðan **Varpa texta á reikning** aðgerðina. Frekari upplýsingar er að finna í [Varpa texta um endurteknar greiðslur í reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

    Þegar lokið er við vörpun greiðslutexta í lykla skal velja **aðgerðina nota handvirkt**.

    Þegar kortvörpun er sett upp er í meðfylgjandi sjálfvirkri greiðslujöfnun **að setja Hátexta-og lyklavörpun** í **reitinn Match-traust**.

11. Fyrir færslubókarlínu er ekki með neina tillögu að forriti þar sem ekki er hægt að jafna **fjárhagsfærslu við til að stofna og bóka þann Fjárhagsfærslumismun** sem þarf til að jafna greiðsluna við. Frekari upplýsingar er að finna [í Afstemmingargreiðslum sem ekki er hægt að nota.](receivables-how-reconcile-payments-cannot-apply-auto.md)

12. Þegar ekki þarf að yfirfara fleiri línur og reiturinn **Mismunur** er auður í öllum línum skal velja aðgerðina **Bóka** og síðan velja einn af eftirfarandi valkostum:

    - **Bóka greiðslur og afstemma bankareikninga** - Til að bóka greiðslur sem jafnaðar og einnig loka tengdum færslum í höfuðbók bankareiknings sem afstemmdum.
    - **Bóka aðeins greiðslur** - Til að bóka greiðslurnar sem jafnaðar, en skilja tengdar færslur í höfuðbók bankareiknings eftir opnar. Krafist er að þú afstemmir bankareikninginn sérstaklega, til dæmis: Frekari upplýsingar eru að finna í [Afstemma bankareikninga](bank-how-reconcile-bank-accounts-separately.md).
    - **Prófunarskýrsla** - Til að yfirfara niðurstöður bókunar áður en þú bókar. Skýrslan fyrir **Bankareikningsyfirlit** birtist og sýnir sömu reitina og neðst á síðunni **Greiðsluafstemmingarbók**.

Þegar greiðsluafstemmingarbók er bókuð eru opnu færslunum lokað. Viðskiptamaður, lánardrottinn eða fjárhagsreikningar eru uppfærðir. Fyrir greiðslur á færslubókarlínum á grunni vörpunar texta á reikning eru tilteknir viðskiptamanna-, lánardrottna- og fjárhagsreikningar uppfærðir. Bankareikningsfærslur eru búnar til fyrir allar færslubókarlínur. Allar opnar fjárhagsfærslur bankareiknings sem tengjast jöfnuðum fjárhagsfærslum viðskiptavinar eða lánardrottins verða lokaðar þegar þú velur **Bóka Greiðslur og stemma Af Bankareikninga** aðgerð. Þetta þýðir að bankareikningurinn er sjálvirkt stemmdur af fyrir greiðslur sem bókaðar eru með færslubókinni.

Hægt er að bera gildið í **Staða á bankareikningi eftir bókun** reitnum saman við gildið í reitnum **Lokastaða yfirlits** til að sjá hvenær bankareikningurinn er afstemmdur út frá bókuðum greiðslum.

> [!NOTE]  
>   Ef ekki á að afstemma bankareikninginn af síðunni **greiðsluafstemmingarbók** þá verðurðu að nota **afstemming bankareiknings** gluggann. Frekari upplýsingar er að finna í [Afstemma bankareikninga](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
