---
title: Afstemma greiðslur með sjálfvirkri jöfnun
description: Lýsir því hvernig nota skal aðgerðina Sjálfvirk jöfnun til að jafna greiðslur eða inngreiðslur við opnar færslur þeim tengdum, og afstemma greiðslur.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.search.form: 389, 1290, 1294, 1287
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8c4d11dd4e031388ea5ec28bb8a181122b50b470
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9074589"
---
# <a name="reconcile-payments-using-automatic-application"></a>Afstemma greiðslur með sjálfvirkri jöfnun

Síðan **Greiðsluafstemmingarbók** tilgreinir greiðslur, annaðhvort greiðslur inn eða út, sem hafa verið skráðar sem færslur á netbankareikning eða greiðsluþjónusta og sem hægt er að jafna við tengdar opnar fjárhagsfærslur viðskiptavinar, lánardrottins, og bankareiknings. Línurnar í færslubókinni er hægt að fylla inn í með því að flytja inn bankayfirlitið sem bankastreymi eða -skrá eða með því að færa færslur inn handvirkt sem gerðar eru í greiðsluþjónustunni.

> [!NOTE]
> Síðan býður upp á sjálfvirkar samsvörunaraðgerðir sem jafna greiðslur við tengdar opnar færslur þeirra sem byggja á samsvörun texta í bankayfirlitslínu (færslubókarlínu) við gögní einni eða fleiri opnum færslum. Athugaðu að þú getur skrifað yfir ráðlagðar sjálfvirkar jafnanir og þú getur valið að nota ekki sjálfvirkar jafnanir yfirhöfuð. Frekari upplýsingar er að finna í 7 skrefi.

Greiðsluafstemmingarbók tengist einum bankareikningi í [!INCLUDE[prod_short](includes/prod_short.md)] sem endurspeglar netbankareikninginn þar sem greiðslufærslurnar eru skráðar. Allar opnar fjárhagsfærslur bankareiknings sem tengjast jöfnuðum fjárhagsfærslum viðskiptavinar eða lánardrottins verða lokaðar þegar þú velur **Bóka Greiðslur og stemma Af Bankareikninga** aðgerð. Þetta þýðir að bankareikningurinn er sjálvirkt stemmdur af fyrir greiðslur sem bókaðar eru með færslubókinni.

Hægt er að flytja inn bankafærslur sem .csv-bankaskrár eða annað snið sem bankinn veitir. Ef þú vilt flytja inn bankayfirlit sem bankastreymi, verður þú að virkja tiltekna samþættingarþjónustu banka, og tengja síðan bankareikningana við viðkomandi netbankareikninga. greiðsluafstemmingarbók greinir síðan sjálfkrafa bankastreymi þegar þú velur aðgerðina **flytja inn bankafærslur**. Þar að auki er hægt að setja upp bankareikning til að flytja sjálfkrafa inn ný bankayfirlitsstreymi á hverri klukkustund. Færslur fyrir greiðslur sem þegar hafa verið bókaðar sem jöfnuð og/eða stemmt af verða ekki fluttar inn. Hægt er að nota Envestnet Yodlee Bank Feeds-þjónustuna fyrir þetta, sem er foruppsett í sumum landsútgáfum [!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar eru í [Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md). Að öðrum kosti skal hafa samband við samstarfsaðila Microsoft til að fá aðstoð við að uppfylla kröfur fyrirtækisins eða landsins.

Aðgerðinni **varpa texta á reikning** gerir notendum kleift að hægt að setja upp vörpun á milli texta í greiðslum og tiltekinni debet-, kredit- og mótreikninga til að greiðslurnar séu bókaðar í tiltekna reikninga þegar greiðsluafstemmingarbók er bókuð. Þetta er t.d. gagnlegt passar fyrir ítrekaðar inngreiðslur eða gjöld, t.d. ítrekuð kaup eldsneytis eða bankagjöld og vextir, sem gerist reglulega á bankayfirliti og sem ekki þarf tengt viðskiptaskjal. (Sjá skref 10 hér á eftir.) Frekari upplýsingar er að finna í [Varpa texta um endurteknar greiðslur í reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Færslubókarlínur kunna að hafa enga ráðlagða jöfnun. Þetta kann að vera af ýmsum ástæðum, svo sem týndu skjali eða vegna þess að viðskiptamaður ofgreiddi þannig að umframupphæð er til þegar greiðslan er notuð í annarri færslubókarlínu. Fyrir slík tilvik er hægt að nota aðgerðina **Flytja mismun á reikning** til að stofna og bóka fjárhagsfærsluna sem vantar, t.d. vegna endurgreiðslu, sem þarf til að jafna greiðsluna. (Sjá skref 11 hér á eftir) Frekari upplýsingar eru í [Afstemma greiðslur sem ekki er hægt að afstemma.](receivables-how-reconcile-payments-cannot-apply-auto.md).

Þú notar aðgerðina **Sjálfvirk jöfnun**, annaðhvort sjálfvirkt þegar þú flytur inn bankaskrá eða streymi með greiðslufærslum eða þegar þú virkjar hana, til að jafna greiðslur við tengdar opnar færslur sem byggja á samsvörun texta á bankayfirlitslínu (færslubókarlínu) við texta í einni eða fleiri opnum færslum. Þessi sjálfvirkni er byggð á reglum sem eru skilgreindar á síðunni **Greiðslujöfnunarreglur** þar sem einnig er skilgreint hvort tillaga að jöfnun þarfnast yfirferðar. Frekari upplýsingar eru í [Setja upp reglur fyrir sjálfvirka jöfnun á greiðslum](receivables-how-set-up-payment-application-rules.md).

Á færslubókarlínum þar sem greiðsla hefur verið jöfnuð sjálfvirkt við eina eða fleiri opnar færslur hefur reiturinn **Áreiðanleiki samsvörunar** gildið **Lágt**, **Miðlungs** eða **Hátt** til að tilgreina gæði gagnasamsvörunar sem ráðlögð greiðslujöfnun er byggð á.

Sumar greiðslujafnanir þarfnast yfirferðar þinnar eins og það er skilgreint af notaðri samsvörunarreglu, t.d. línur með **Lágan** áreiðanleika samsvörunar. Aðrar línu krefjast yfirferðar og handvirkrar breytingar vegna þess að það er gildi í reitnum **Mismunur**. Til að yfirfara eina eða fleiri greiðslujafnanir skal velja reitinn **Línur til yfirferðar** eða **Línur með mismun** neðst. Síðan **Yfirferð greiðslujöfnunar** opnast og sýnir allar viðeigandi upplýsingar um viðskiptamann eða lánardrottin sem greiðslan er jöfnuð við, samsvörunarupplýsingarnar og aðgerðr til að afgreiða línuna, t.d. aðgerðina **Jöfnun**. (Sjá skref 7 og 8 hér á eftir.)

Fyrir hverja færslubókarlínu í **greiðsluafstemmingarbók** síðunni geturðu opnað **greiðslujafnanir** síðuna til að sjá alla möguleika opinna færslna fyrir greiðsluna og skoðað ítarlegar upplýsingar fyrir hverja færslu um gagnasamsvaranir sem greiðslujöfnun byggir á. Hér er hægt að jafna handvirkt greiðslur eða endurjafna greiðslur sem voru jafnaðar sjálfkrafa á ranga færslu. (Sjá skref 10 hér á eftir.) Frekari upplýsingar eru í [Endurskoða eða sækja um greiðslur eftir sjálfvirkan umsókn](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Hægt er að hefja bankafærsluinnflutninginn á sama tíma og síðan **Greiðsluafstemmingarbók** er opnuð fyrir fyrirliggjandi bók. Eftirfarandi ferli lýsir því hvernig á að flytja inn bankafærslur á síðuna **greiðsluafstemmingarbók** eftir að ný færslubók hefur verið búin til.

## <a name="to-reconcile-payments-using-automatic-application"></a>Til að afstemma greiðslur með sjálfvirk jöfnun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðsluafstemmingarbækur** og velja síðan viðkomandi tengil.
2. Til að vinna í nýrri greiðsluafstemmingarbók, veldu aðgerðina **Ný færslubók**.
3. Á síðunni **Listi yfir bankareikninga fyrir greiðslu** er valið bankareikningur sem á að jafna greiðslur fyrir, og smellt síðan á **Í lagi** hnappinn.
   Síðan **Greiðsluafstemmingarbók** opnast undirbúin fyrir valdan bankareikning.
4. Veldu aðgerðina **Flytja inn bankafærslur**
   Ef bankareikningurinn fyrir valda færslubók er ekki settur upp til að flytja inn bankafærslur opnast svargluggi sem aðstoðar við að fylla út í viðeigandi reiti.
5. Á síðunni **Velja skrá til að flytja inn** skal velja skrána sem inniheldur bankafærslurnar fyrir greiðslurnar sem á að stemma af og velja svo hnappinn **Opna**.  
6. Ef Envestnet Yodlee Bank Feeds þjónustan er virk, á síðunni **Bankayfirlitssía** sem opnast sjálfkrafa, skal tilgreina dagsetningarbil fyrir bankayfirlit sem á að flytja inn.

    Síðan **Greiðsluafstemmingarbók** er fyllt út með línum fyrir greiðslur sem tákna bankafærslur í innflutta bankayfirliti.

     Á línum fyrir greiðslur sem hafa verið jafnaðar sjálfvirkt við tengdar opnar færslur hefur reiturinn **áreiðanleiki samsvörunar** gildi á milli **Lítið** og **Hátt** til að tilgreina gæði gagnasamsvörunar sem ráðlögð greiðslujöfnun er byggð á. Að auki eru **Reikningsheiti**, **Reikningsgerð** og **Reikningsnúmer** reitirnir fylltir með viðskiptamanninum eða lánardrottninum sem greiðslan er jöfnuð við.

    Sjálfvirkar jafnanir, gæði samsvörunar og hvort línur þurfi yfirferð er skilgreint af reglum sem hægt er að breyta til að laga niðurstöðurnar. Frekari upplýsingar eru í [Setja upp reglur fyrir sjálfvirka jöfnun á greiðslum](receivables-how-set-up-payment-application-rules.md).

7. Til að yfirfara, samþykkja/fjarlægja eða breyta mörgum greiðslujöfnunum handvirkt sem eru með gildi í reitnum **Mismunur** skal velja aðgerðina **Línur með mismun** neðst.

    Síðan **Yfirferð greiðslujöfnunar** opnast og sýnir fyrstu jöfnun til að yfirfara. Næsta jöfnun sem á að yfirfara verður sýnd á síðunni þegar sú fyrri er afgreidd. Allar viðeigandi upplýsingar um viðskiptamann eða lánardrottin sem greiðslan er jöfnuð við, samsvörunarupplýsingarnar og aðgerðr til að afgreiða línuna, t.d. aðgerðirnar **Samþykkja jöfnun** og **Handvirk jöfnun**.

8. Til að yfirfara, samþykkja/fjarlægja eða breyta mörgum greiðslujöfnunum sem eru stilltar á yfirferð, samkvæmt reglu greiðslujöfnunar, skal velja aðgerðina **Línur til yfirferðar** neðst. Sama upplifun og lýst er í skrefi 8 kemur fram

9. Til að breyta handvirkri jöfnun skaltu velja færslubókarlínuna og svo skaltu velja **Jafna handvirkt** til að endurskoða, endurjafna eða jafna greiðsluna handvirkt á síðunni **greiðslujafnanir**. Frekari upplýsingar eru í [Endurskoða eða sækja um greiðslur eftir sjálfvirkan umsókn](receivables-how-review-apply-payments-auto-application.md).

10. Veljið ójafnaða greiðslubókarlínu fyrir ítrekaða inngreiðslu eða kostnað, eins og kaup bensín á bíl, og veljið síðan **Varpa texta á reikning** aðgerðina. Frekari upplýsingar er að finna í [Varpa texta um endurteknar greiðslur í reikninga fyrir sjálfvirka afstemmingu](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

    Þegar vörpun greiðslutexta á reikninga er lokið velurðu **Handvirk jöfnun**.

    Þegar vörpun texta á reikning er sett upp mun sjálfvirk greiðslujöfnun í kjölfarið innihalda **Hátt - Vörpun texta á reikning** í reitnum **Áreiðanleiki samsvörunar**.

11. Fyrir færslubókarlínu sem ekki er með neina ráðlagða jöfnun vegna þess að engin færslubókarlína er til staðar sem hægt er að jafna hana við skal velja aðgerðina **Flytja mismun á reikning** til að stofna og bóka fjárhagsfærsluna sem vantar til að jafna greiðsluna við. Frekari upplýsingar eru í [Afstemma greiðslur sem ekki er hægt að afstemma.](receivables-how-reconcile-payments-cannot-apply-auto.md)

10. Þegar ekki þarf að yfirfara fleiri línur og reiturinn **Mismunur** er auður í öllum línum skal velja aðgerðina **Bóka** og síðan velja einn af eftirfarandi valkostum:

    - **Bóka greiðslur og afstemma bankareikninga** - Til að bóka greiðslur sem jafnaðar og einnig loka tengdum færslum í höfuðbók bankareiknings sem afstemmdum.
    - **Bóka aðeins greiðslur** - Til að bóka greiðslurnar sem jafnaðar, en skilja tengdar færslur í höfuðbók bankareiknings eftir opnar. Krafist er að þú afstemmir bankareikninginn sérstaklega, til dæmis: Frekari upplýsingar eru að finna í [Afstemma bankareikninga](bank-how-reconcile-bank-accounts-separately.md).
    - **Prófunarskýrsla** - Til að yfirfara niðurstöður bókunar áður en þú bókar. Skýrslan fyrir **Bankareikningsyfirlit** birtist og sýnir sömu reitina og neðst á síðunni **Greiðsluafstemmingarbók**.

Þegar greiðsluafstemmingarbók er bókuð er jöfnuðu opnu færslureikningunum lokað og tengdir reikningar viðskiptamannsins, lánardrottinsins eða almennir reikningar eru uppfærðir. Fyrir greiðslur á færslubókarlínum á grunni vörpunar texta á reikning eru tilteknir viðskiptamanna-, lánardrottna- og fjárhagsreikningar uppfærðir. Bankareikningsfærslur eru búnar til fyrir allar færslubókarlínur. Allar opnar fjárhagsfærslur bankareiknings sem tengjast jöfnuðum fjárhagsfærslum viðskiptavinar eða lánardrottins verða lokaðar þegar þú velur **Bóka Greiðslur og stemma Af Bankareikninga** aðgerð. Þetta þýðir að bankareikningurinn er sjálvirkt stemmdur af fyrir greiðslur sem bókaðar eru með færslubókinni.

Hægt er að bera gildið í **Staða á bankareikningi eftir bókun** reitnum saman við gildið í reitnum **Lokastaða yfirlits** til að sjá hvenær bankareikningurinn er afstemmdur út frá bókuðum greiðslum.

> [!NOTE]  
>   Ef ekki á að afstemma bankareikninginn af síðunni **greiðsluafstemmingarbók** þá verðurðu að nota **afstemming bankareiknings** gluggann. Frekari upplýsingar er að finna í [Afstemma bankareikninga](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/modules/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Stjórnun skulda](receivables-manage-receivables.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]