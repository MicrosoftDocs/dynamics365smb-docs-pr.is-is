---
title: "Afstemma greiðslur með sjálfvirkri jöfnun| Microsoft Docs"
description: "Lýsir því hvernig nota skal aðgerðina Sjálfvirk jöfnun til að jafna greiðslur eða inngreiðslur við opnar færslur þeim tengdum, og afstemma greiðslur."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: b4ff3d64f23a5dfb9800abeedb7374764b060f4d
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reconcile-payments-using-automatic-application"></a>Hvernig á að afstemma greiðslur með sjálfvirkri jöfnun
**greiðsluafstemmingarbók** glugginn tilgreinir greiðslur, annaðhvort greiðslur inn eða út, sem hafa verið skráðar sem færslur á netbankareikning og sem hægt er að jafna við tengdar opnar fjárhagsfærslur viðskiptavinar, lánardrottins, og bankareiknings. Línurnar í færslubókinni eru fylltar inn með því að flytja inn bankayfirlitið sem bankastreymi eða skrá.

Greiðsluafstemmingarbók tengist einum bankareikningi í [!INCLUDE[d365fin](includes/d365fin_md.md)] sem endurspeglar netbankareikninginn þar sem greiðslufærslurnar eru skráðar. Allar opnar fjárhagsfærslur bankareiknings sem tengjast jöfnuðum fjárhagsfærslum viðskiptavinar eða lánardrottins verða lokaðar þegar þú velur **Bóka Greiðslur og stemma Af Bankareikninga** aðgerð. Þetta þýðir að bankareikningurinn er sjálvirkt stemmdur af fyrir greiðslur sem bókaðar eru með færslubókinni.

Ef þú vilt flytja inn bankayfirlit sem bankastreymi, verður þú að virkja Envestnet Yodlee bankastreymisþjónustu , og tengja síðan bankareikningana við viðkomandi netbankareikninga. greiðsluafstemmingarbók greinir síðan sjálfkrafa bankastreymi þegar þú velur aðgerðina **flytja inn bankafærslur**. Þar að auki er hægt að setja upp bankareikning til að flytja sjálfkrafa inn ný bankayfirlitsstreymi á hverri klukkustund. Færslur fyrir greiðslur sem þegar hafa verið bókaðar sem jöfnuð og/eða stemmt af verða ekki fluttar inn. Frekari upplýsingar sjá [Hvernig: Setja á Upp Envestnet Yodlee bankastreymisþjónustu](bank-how-setup-bank-statement-service.md).

Með aðgerðinni **varpa texta á reikning** er hægt að setja upp vörpun á milli texta í greiðslum og tiltekinni debet-, kredit- og mótreikninga til að greiðslurnar séu bókaðar í tiltekna reikninga þegar greiðsluafstemmingarbók er bókuð. Sjá skref 8  Fyrir frekar upplýsingar, sjá [Hvernig á að varpa texta á endurteknar greiðslur á reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

Svipað aðgerð er til til að stemma af umframupphæðir á greiðsluafstemmingarbókarlínum á sérstækum grundvelli. Frekari upplýsingar eru í [hvernig á að afstemma greiðslur sem ekki er hægt að afstemma](receivables-how-reconcile-payments-cannot-apply-auto.md).

Þú notar aðgerðina **Sjálfvirk jöfnun**, annaðhvort sjálfvirkt þegar þú flytur inn bankaskrá eða streymi með greiðslufærslum eða þegar þú virkjar hana, til að jafna greiðslur við tengdar opnar færslur sem byggja á vörpun gagna á færslubókarlínu með gögnum eða einni eða fleiri opinni færslu.

Á færslubókarlínum þar sem greiðsla hefur verið jöfnuð sjálfvirkt við eina eða fleiri opnar færslur hefur reiturinn **áreiðanleiki samsvörunar** gildi á milli Lágt og Hátt til að tilgreina gæði gagnasamsvörunar sem ráðlögð greiðslujöfnun er byggð á. Að auki eru **Reikningsgerð** og **Reikningsnúmer** reitirnir fylltir með viðskiptamanninum eða lánardrottninum sem greiðslan er jöfnuð við. Ef þú hefur sett upp vörpun texta á reikning getur sjálfvirk jöfnunin leitt til áreiðanleiki samsvörunar upp á **Hátt - Vörpun texta á reikning**.

Fyrir hverja færslubókarlínu í **greiðsluafstemmingarbók** glugganum geturðu opnað **greiðslujafnanir** gluggann til að sjá alla möguleika opinna færslna fyrir greiðsluna og skoðað ítarlegar upplýsingar fyrir hverja færslu um gagnasamsvaranir sem greiðslujöfnun byggir á. Hér er hægt að jafna handvirkt greiðslur eða endurjafna greiðslur sem voru jafnaðar sjálfkrafa á ranga færslu. Fyrir frekar upplýsingar, sjá [Hvernig á að endurskoða eða jafna greiðslur eftir sjálfvirka jöfnun](receivables-how-review-apply-payments-auto-application.md)

> [!NOTE]  
>   Hægt er að hefja bankafærsluinnflutninginn á sama tíma og glugginn **greiðsluafstemmingarbók** er opnaður fyrir fyrirliggjandi greiðsluafstemmingarbók í glugganum **Greiðsluafstemmingarbækur**. Eftirfarandi ferli lýsir því hvernig á að flytja inn bankafærslur í **greiðsluafstemmingarbók** gluggann eftir að ný færslubók hefur verið búin til.

## <a name="to-reconcile-payments-using-automatic-application"></a>Til að afstemma greiðslur með sjálfvirk jöfnun
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **greiðsluafstemmingarbækur** og velja svo viðeigandi tengil.
2. Til að vinna í nýrri greiðsluafstemmingarbók, veldu aðgerðina **Ný færslubók**.
3. Í glugganum **Listi yfir bankareikninga fyrir greiðslu** er valið bankareikningur sem á að jafna greiðslur fyrir, og smellt síðan á **Í lagi** hnappinn.
   **greiðsluafstemmingarbók** Glugginn opnast undirbúinn fyrir valda bankareikninginn.
4. Veldu aðgerðina **Flytja inn bankafærslur**
   Ef bankareikningurinn fyrir valda færslubók er ekki settur upp til að flytja inn bankafærslur opnast svargluggi sem aðstoðar við að fylla út í viðeigandi reiti.
5. Í glugganum **Velja skrá til að flytja inn** skal velja skrána sem inniheldur bankafærslurnar fyrir greiðslurnar sem á að stemma af og velja svo hnappinn **Opna**.  
6. Ef Bankayfirlitsþjónusta er virk, í glugganum **bankayfirlitssía** sem opnast sjálfkrafa, skal tilgreina dagsetningarbil fyrir bankayfirlit sem á að flytja inn.

    **greiðsluafstemmingarbók** Glugginn er fylltur út með línum fyrir greiðslur sem tákna bankafærslur í innflutta bankayfirliti.

    Á línum fyrir greiðslur sem hafa verið jafnaðar sjálfvirkt við tengdar opnar færslur hefur reiturinn **áreiðanleiki samsvörunar** gildi á milli **Lítið** og **Hátt** til að tilgreina gæði gagnasamsvörunar sem ráðlögð greiðslujöfnun er byggð á. Að auki eru **Reikningsgerð** og **Reikningsnúmer** reitirnir fylltir með viðskiptamanninum eða lánardrottninum sem greiðslan er jöfnuð við.
7. Veldu færslubókarlínuna og og svo skaltu velja **Jafna handvirkt** til að endurskoða, endurjafna eða jafna greiðsluna handvirkt í  glugganum **greiðslujafnanir**. Fyrir frekar upplýsingar, sjá [Hvernig á að endurskoða eða jafna greiðslur eftir sjálfvirka jöfnun](receivables-how-review-apply-payments-auto-application.md)

    Þegar þú hefur lokið við handvirka jöfnun inniheldur **áreiðanleiki samsvörunar** reiturinn á færslubókarlínunni sem þú hefur meðhöndlað handvirkt **Samþykkt**.
8. Veljið ójafnaða greiðslubókarlínu fyrir ítrekaða inngreiðslu eða kostnað, eins og kaup bensín á bíl, og veljið síðan **Varpa texta á reikning** aðgerðina. Fyrir frekar upplýsingar, sjá [Hvernig á að varpa texta á endurteknar greiðslur á reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)
9. Þegar vörpun greiðslutexta á reikninga er lokið velurðu **Handvirk jöfnun**.
10. Þegar þú telur að allar greiðslur á færslubókarlínunum séu rétt jafnaðar eða stilltar á beina bókun velurðu **Bóka**.

Þegar greiðsluafstemmingarbók er bókuð er jöfnuðu opnu færslureikningunum lokað og tengdir reikningar viðskiptamannsins, lánardrottinsins eða almennir reikningar eru uppfærðir. Fyrir greiðslur á færslubókarlínum á grunni vörpunar texta á reikning eru tilteknir viðskiptamanna-, lánardrottna- og fjárhagsreikningar uppfærðir. Bankareikningsfærslur eru búnar til fyrir allar færslubókarlínur. Allar opnar fjárhagsfærslur bankareiknings sem tengjast jöfnuðum fjárhagsfærslum viðskiptavinar eða lánardrottins verða lokaðar þegar þú velur **Bóka Greiðslur og stemma Af Bankareikninga** aðgerð. Þetta þýðir að bankareikningurinn er sjálvirkt stemmdur af fyrir greiðslur sem bókaðar eru með færslubókinni.

Hægt er að bera gildið í **Staða á bankareikningi eftir bókun** reitnum saman við gildið í reitnum **Lokastaða yfirlits** til að sjá hvenær bankareikningurinn er afstemmdur út frá bókuðum greiðslum.

> [!NOTE]  
>   Ef ekki á að afstemma bankareikninginn úr glugganum **greiðsluafstemmingarbók** þá verðurðu að nota **afstemming bankareiknings** gluggann. Frekari upplýsingar í [Afstemma Bankareikninga Sérstaklega](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-also"></a>Sjá einnig
[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

