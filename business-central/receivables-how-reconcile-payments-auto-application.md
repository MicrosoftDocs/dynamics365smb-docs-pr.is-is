---
title: Afstemma greiðslur með sjálfvirkri jöfnun
description: Lýsir því hvernig nota skal aðgerðina Sjálfvirk jöfnun til að jafna greiðslur eða inngreiðslur við opnar færslur þeim tengdum, og afstemma greiðslur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3b90cb523449367672be71abe0a7cf02effcde5a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748544"
---
# <a name="reconcile-payments-using-automatic-application"></a>Afstemma greiðslur með sjálfvirkri jöfnun

Síðan **Greiðsluafstemmingarbók** tilgreinir greiðslur, annaðhvort greiðslur inn eða út, sem hafa verið skráðar sem færslur á netbankareikning og sem hægt er að jafna við tengdar opnar fjárhagsfærslur viðskiptavinar, lánardrottins, og bankareiknings. Línurnar í færslubókinni eru fylltar inn með því að flytja inn bankayfirlitið sem bankastreymi eða skrá.

> [!NOTE]
> Síðan býður upp á sjálfvirkar samsvörunaraðgerðir sem jafna greiðslur við tengdar opnar færslur þeirra sem byggja á samsvörun texta í bankayfirlitslínu (færslubókarlínu) við texta í einni eða fleiri opnum færslum í höfuðbók bankareiknings (hægri rúðunni). Athugaðu að þú getur skrifað yfir ráðlagðar sjálfvirkar jafnanir og þú getur valið að nota ekki sjálfvirkar jafnanir yfirhöfuð. Frekari upplýsingar er að finna í 7 skrefi.

Greiðsluafstemmingarbók tengist einum bankareikningi í [!INCLUDE[prod_short](includes/prod_short.md)] sem endurspeglar netbankareikninginn þar sem greiðslufærslurnar eru skráðar. Allar opnar fjárhagsfærslur bankareiknings sem tengjast jöfnuðum fjárhagsfærslum viðskiptavinar eða lánardrottins verða lokaðar þegar þú velur **Bóka Greiðslur og stemma Af Bankareikninga** aðgerð. Þetta þýðir að bankareikningurinn er sjálvirkt stemmdur af fyrir greiðslur sem bókaðar eru með færslubókinni.

Ef þú vilt flytja inn bankayfirlit sem bankastreymi, verður þú að virkja Envestnet Yodlee Bank Feeds þjónustu , og tengja síðan bankareikningana við viðkomandi netbankareikninga. greiðsluafstemmingarbók greinir síðan sjálfkrafa bankastreymi þegar þú velur aðgerðina **flytja inn bankafærslur**. Þar að auki er hægt að setja upp bankareikning til að flytja sjálfkrafa inn ný bankayfirlitsstreymi á hverri klukkustund. Færslur fyrir greiðslur sem þegar hafa verið bókaðar sem jöfnuð og/eða stemmt af verða ekki fluttar inn. Frekari upplýsingar eru í [Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md).

Með aðgerðinni **varpa texta á reikning** er hægt að setja upp vörpun á milli texta í greiðslum og tiltekinni debet-, kredit- og mótreikninga til að greiðslurnar séu bókaðar í tiltekna reikninga þegar greiðsluafstemmingarbók er bókuð. Sjá skref 8. Frekari upplýsingar er að finna í [Varpa texta um endurteknar greiðslur í reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Svipað aðgerð er til til að stemma af umframupphæðir á greiðsluafstemmingarbókarlínum á sérstækum grundvelli. Frekari upplýsingar eru í [Afstemma greiðslur sem ekki er hægt að afstemma.](receivables-how-reconcile-payments-cannot-apply-auto.md)

Þú notar aðgerðina **Sjálfvirk jöfnun**, annaðhvort sjálfvirkt þegar þú flytur inn bankaskrá eða streymi með greiðslufærslum eða þegar þú virkjar hana, til að jafna greiðslur við tengdar opnar færslur sem byggja á samsvörun texta á bankayfirlitslínu (færslubókarlínu) við texta í einni eða fleiri opnum færslum. Frekari upplýsingar eru í [Setja upp reglur fyrir sjálfvirka jöfnun á greiðslum](receivables-how-set-up-payment-application-rules.md).

Á færslubókarlínum þar sem greiðsla hefur verið jöfnuð sjálfvirkt við eina eða fleiri opnar færslur hefur reiturinn **áreiðanleiki samsvörunar** gildi á milli Lágt og Hátt til að tilgreina gæði gagnasamsvörunar sem ráðlögð greiðslujöfnun er byggð á. Að auki eru **Reikningsgerð** og **Reikningsnúmer** reitirnir fylltir með viðskiptamanninum eða lánardrottninum sem greiðslan er jöfnuð við. Ef þú hefur sett upp vörpun texta á reikning getur sjálfvirk jöfnunin leitt til áreiðanleiki samsvörunar upp á **Hátt - Vörpun texta á reikning**.

Fyrir hverja færslubókarlínu í **greiðsluafstemmingarbók** síðunni geturðu opnað **greiðslujafnanir** síðuna til að sjá alla möguleika opinna færslna fyrir greiðsluna og skoðað ítarlegar upplýsingar fyrir hverja færslu um gagnasamsvaranir sem greiðslujöfnun byggir á. Hér er hægt að jafna handvirkt greiðslur eða endurjafna greiðslur sem voru jafnaðar sjálfkrafa á ranga færslu. Frekari upplýsingar eru í [Endurskoða eða sækja um greiðslur eftir sjálfvirkan umsókn](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Hægt er að hefja bankafærsluinnflutninginn á sama tíma og glugginn **greiðsluafstemmingarbók** er opnaður fyrir fyrirliggjandi greiðsluafstemmingarbók á síðunni **Greiðsluafstemmingarbækur**. Eftirfarandi ferli lýsir því hvernig á að flytja inn bankafærslur á síðuna **greiðsluafstemmingarbók** eftir að ný færslubók hefur verið búin til.

## <a name="to-reconcile-payments-using-automatic-application"></a>Til að afstemma greiðslur með sjálfvirk jöfnun
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiðsluafstemmingarbækur** og veldu síðan tengda tengilinn.
2. Til að vinna í nýrri greiðsluafstemmingarbók, veldu aðgerðina **Ný færslubók**.
3. Á síðunni **Listi yfir bankareikninga fyrir greiðslu** er valið bankareikningur sem á að jafna greiðslur fyrir, og smellt síðan á **Í lagi** hnappinn.
   Síðan **Greiðsluafstemmingarbók** opnast undirbúin fyrir valdan bankareikning.
4. Veldu aðgerðina **Flytja inn bankafærslur**
   Ef bankareikningurinn fyrir valda færslubók er ekki settur upp til að flytja inn bankafærslur opnast svargluggi sem aðstoðar við að fylla út í viðeigandi reiti.
5. Á síðunni **Velja skrá til að flytja inn** skal velja skrána sem inniheldur bankafærslurnar fyrir greiðslurnar sem á að stemma af og velja svo hnappinn **Opna**.  
6. Ef Bankayfirlitsþjónusta er virk, á síðunni **Bankayfirlitssía** sem opnast sjálfkrafa, skal tilgreina dagsetningarbil fyrir bankayfirlit sem á að flytja inn.

    Síðan **Greiðsluafstemmingarbók** er fyllt út með línum fyrir greiðslur sem tákna bankafærslur í innflutta bankayfirliti.

    Á línum fyrir greiðslur sem hafa verið jafnaðar sjálfvirkt við tengdar opnar færslur hefur reiturinn **áreiðanleiki samsvörunar** gildi á milli **Lítið** og **Hátt** til að tilgreina gæði gagnasamsvörunar sem ráðlögð greiðslujöfnun er byggð á. Að auki eru **Reikningsgerð** og **Reikningsnúmer** reitirnir fylltir með viðskiptamanninum eða lánardrottninum sem greiðslan er jöfnuð við.
7. Veldu færslubókarlínuna og svo skaltu velja **Jafna handvirkt** til að endurskoða, endurjafna eða jafna greiðsluna handvirkt á síðunni **Greiðslujafnanir**. Frekari upplýsingar eru í [Endurskoða eða sækja um greiðslur eftir sjálfvirkan umsókn](receivables-how-review-apply-payments-auto-application.md).

    Þegar þú hefur lokið við handvirka jöfnun inniheldur **áreiðanleiki samsvörunar** reiturinn á færslubókarlínunni sem þú hefur meðhöndlað handvirkt **Samþykkt**.
8. Veljið ójafnaða greiðslubókarlínu fyrir ítrekaða inngreiðslu eða kostnað, eins og kaup bensín á bíl, og veljið síðan **Varpa texta á reikning** aðgerðina. Frekari upplýsingar er að finna í [Varpa texta um endurteknar greiðslur í reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)
9. Þegar vörpun greiðslutexta á reikninga er lokið velurðu **Handvirk jöfnun**.
10. Þegar þú telur að allar greiðslur á færslubókarlínunum séu rétt jafnaðar eða stilltar á beina bókun velurðu aðgerðina **Bóka** og síðan velurðu einn af þessum valkostum:

    - **Bóka greiðslur og afstemma bankareikninga** - Til að bóka greiðslur sem jafnaðar og einnig loka tengdum færslum í höfuðbók bankareiknings sem afstemmdum.
    - **Bóka aðeins greiðslur** - Til að bóka greiðslurnar sem jafnaðar, en skilja tengdar færslur í höfuðbók bankareiknings eftir opnar. Krafist er að þú afstemmir bankareikninginn sérstaklega, til dæmis: Frekari upplýsingar eru að finna í [Afstemma bankareikninga](bank-how-reconcile-bank-accounts-separately.md).
    - **Prófunarskýrsla** - Til að yfirfara niðurstöður bókunar áður en þú bókar. Skýrslan fyrir **Bankareikningsyfirlit** birtist og sýnir sömu reitina og neðst á síðunni **Greiðsluafstemmingarbók**.

Þegar greiðsluafstemmingarbók er bókuð er jöfnuðu opnu færslureikningunum lokað og tengdir reikningar viðskiptamannsins, lánardrottinsins eða almennir reikningar eru uppfærðir. Fyrir greiðslur á færslubókarlínum á grunni vörpunar texta á reikning eru tilteknir viðskiptamanna-, lánardrottna- og fjárhagsreikningar uppfærðir. Bankareikningsfærslur eru búnar til fyrir allar færslubókarlínur. Allar opnar fjárhagsfærslur bankareiknings sem tengjast jöfnuðum fjárhagsfærslum viðskiptavinar eða lánardrottins verða lokaðar þegar þú velur **Bóka Greiðslur og stemma Af Bankareikninga** aðgerð. Þetta þýðir að bankareikningurinn er sjálvirkt stemmdur af fyrir greiðslur sem bókaðar eru með færslubókinni.

Hægt er að bera gildið í **Staða á bankareikningi eftir bókun** reitnum saman við gildið í reitnum **Lokastaða yfirlits** til að sjá hvenær bankareikningurinn er afstemmdur út frá bókuðum greiðslum.

> [!NOTE]  
>   Ef ekki á að afstemma bankareikninginn af síðunni **greiðsluafstemmingarbók** þá verðurðu að nota **afstemming bankareiknings** gluggann. Frekari upplýsingar er að finna í [Afstemma bankareikninga](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-also"></a>Sjá einnig
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
