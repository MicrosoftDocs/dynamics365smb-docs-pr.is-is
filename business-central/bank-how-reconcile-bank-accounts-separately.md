---
title: Afstemma bankareikninga hvern fyrir sig| Microsoft Docs
description: "Lýsir því hvernig birgðavirði er stemmt af við fjárhaginn."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 05/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 32f5b2b19dc74d3849a313e3d93fdb70146cdb23
ms.contentlocale: is-is
ms.lasthandoff: 05/17/2018

---
# <a name="reconcile-bank-accounts-separately"></a>Afstemma bankareikninga hvern fyrir sig
Til að afstemma bankareikninga í [!INCLUDE[d365fin](includes/d365fin_md.md)] með yfirlitum sem koma frá bankanum þarf fyrst að fylla inn í vinstri rúðuna í glugganum **Að afstemma bankareikninga** með upplýsingum um bankayfirlit sem þú síðan jafnar (afstemmir) við færslur í höfuðbók bankareiknings í hægri rúðunni. Sniðug leið til að fylla út í bankayfirlitslínur er með því að flytja inn bankayfirlitsskrá eða streymi.

> [!NOTE]  
> Í norður-amerískum útgáfum getur þú einnig unnið þetta í glugganum **Vinnublað bankaafstemmingar** sem hentar betur fyrir ávísanir og innborganir en býður ekki upp á innflutning á bankayfirlitsskrám. Til að nota þennan glugga í staðinn fyrir gluggann **Afstemming bankareikninga** skaltu afvelja reitinn **Bankareikn.afstemming með sjálfvirkri jöfnun** í glugganum **Fjárhagsgrunnur**. Frekari upplýsingar er hægt að finna í hlutanum „Afstemma bankareikninga“ sem heyrir undir staðbundnar aðgerðir Bandaríkjanna.

> [!TIP]  
> Einnig er hægt að stemma af bankareikninga í glugganum **greiðsluafstemmingarbók** Allar opnar fjárhagsfærslur bankareiknings sem tengjast jöfnuðum fjárhagsfærslum viðskiptavinar eða lánardrottins verða lokaðar þegar þú velur **Bóka Greiðslur og stemma Af Bankareikninga** aðgerð. Þetta þýðir að bankareikningurinn er sjálvirkt stemmdur af fyrir greiðslur sem bókaðar eru með færslubókinni. Frekari upplýsingar eru í [afstemma greiðslur með því að nota sjálfvirk jöfnun](receivables-how-reconcile-payments-auto-application.md)

Til að virkja innflutning bankayfirlits, verður þú að setja upp og virkja Envestnet Yodlee bankastreymisþjónustu, og tengja síðan bankareikningana við viðkomandi netbankareikninga. Frekari upplýsingar eru í [Setja upp Envestnet Yodlee bankastreymisþjónustu](bank-how-setup-bank-statement-service.md).

Línur gluggans **afstemming bankareiknings** skiptast í tvö svæði. **BankaYfirlitslínur** svæðinu sýnir annað hvort innfluttra bankafærslur eða fjárhagsfærslur með útistandandi greiðslur. **Bankareikningsfærslur** svæðið sýnir fjárhagsfærslur á bankareiknings.

Aðgerðin Að finna og jafna færslur til að jafna kallast að *samsvörun*. Hægt er að velja að framkvæma samsvörun sjálfkrafa með því að nota aðgerðina **Sjálfvirk jöfnun**. Einnig er hægt að velja línur handvirkt í báðum gluggum til að tengja hverja bankareikningslínu við eina eða fleiri tengdar bankareikningsfærslur og nota síðan aðgerðina **Handvirk jöfnun**. **Jafnað** gátreitur er valinn í línum þar sem færslurnar eru samsvarandi.

Hægt er að fylla á **Bankayfirlitslínur** svæðið í á **afstemming bankareiknings** glugganum á eftirfarandi hátt:

* Sjálfvirkt, með því að nota **Flytja inn bankayfirlit** aðgerð til að fylla inn í línurnar samkvæmt raunverulegu bankayfirliti byggðu á skrá frá bankanum.
* Handvirkt, með því að nota **Leggja til línur** aðgerðina til að fylla í línur með fjárhagsfærslum fyrir reikninga sem eru með útistandandi greiðslur.

Þegar gildið í **heildarstaða** reitnum á **Bankauppgjörslínur** svæðinu jafngildir gildið í **Staða til afstemmingar** í á **Bankareikningsfærslur** svæðinu, er hægt að velja **Bóka** aðgerð til að stemma af jafnaðar bankareikningsfærslur. Allar ójafnaðar bankareikningsfærslur verða áfram í glugganum sem gefur til kynna að greiðslur sem unnar voru fyrir bankareikninginn birtast ekki í síðasta bankayfirliti eða að sumar greiðslur voru sendar með ávísunum.

> [!NOTE]  
>   Ef bankayfirlitslínur tengjast tékkafærslum þá er ekki hægt að nota jöfnunaraðgerðirnar. Í staðinn þarf að velja aðgerðina **Jafna færslur** og velja síðan viðkomandi tékkafrærslu til að jafna bankayfirlitslínuna með.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Fylla inn í línur bankaafstemmingar með því að flytja inn bankayfirlit.
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **afstemming bankareiknings** og velja svo viðeigandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Í reitnum **Reikningur nr.** er viðkomandi bankareikningskóti valinn. bankareikningsfærslur sem eru til staðar á bankareikningi birtast í svæðinu **Bankareikningsfærslur**.
4. Í reitinn **Dagsetning yfirlits** er færð dagsetning bankayfirlitsins.
5. Í **Lokastaða yfirlits** reitnum, færðu inn stöðu yfirlits frá bankanum.
6. Ef þú ert með bankayfirlitsskrá, veldu **flytja inn bankayfirlit** aðgerðina.
7. Staðsetja skal skrána og velja svo **Opna** til að flytja inn bankafærslurnar á línurnar í glugganum **afstemming bankareiknings**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>að fylla út línur í bankaafstemmingu með aðgerðin Tillögulínur
1. Í glugganum **Afstemming bankareiknings** er valið á **Tillögulínur** aðgerð.
2. Í reitinn **Upphafsdagsetning** er færð inn fyrsta bókunardagsetning fyrir fjárhagsfærslurnar sem á að stemma af.
3. Í reitinn **lokadagsetning** er færð inn bókunardagsetning fyrir fjárhagsfærslurnar sem á að stemma af.
4. Veldu **hafa með tékka** gátreitinn til að leggja til tékkafærslur í stað samsvarandi bankareikningsfærslna.
5. Velja hnappinn **Í lagi**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>að jafna sjálfkrafa bankayfirlitslínur og bankareikningsfærslur
Glugginn býður upp á sjálfvirkar jöfnunaraðgerðir sem beita greiðslum á tengdar opnar færslur þeirra sem byggja á samsvörun texta í bankayfirlitslínu (vinstri rúðunni) við texta í einni eða fleiri færslum í höfuðbók bankareiknings (hægri rúðunni). Athugaðu að þú getur skrifað yfir ráðlagðar sjálfvirkar jafnanir og þú getur valið að nota ekki sjálfvirkar jafnanir yfirhöfuð. Nánari upplýsingar er að finna í næsta ferli.

1. Í glugganum **Afstemming bankareiknings** er valið **jafna sjálfkrafa** Glugginn **Jafna bankafærslur** opnast.
2. Í reitnum **Vikmörk færsludagsetningar (dagar** skal tilgreina þann fjölda daga fyrir og eftir bókunardagsetningu fjárhagsfærslu bankareiknings sem hafður er með í leitinni að samsvarandi færsludagsetningum á bankayfirlitinu.

    Ef 0 er slegið inn eða reiturinn hafður auður leitar aðgerðin **Sjálfvirk jöfnun** aðeins eftir samstæðum færsludagsetningum í bókunardagsetningu á bankareikningsfærslum.
3. Velja hnappinn **Í lagi**.

    Allar bankayfirlitslínur og bankareikningsfærslur sem hægt er að jafna verða grænar og gátreiturinn **Jafnað** er valinn.
4. Til að fjarlægja jöfnun skal velja bankareikningslínu og velja svo aðgerðina **fjarlægja jöfnun**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Að jafna handvirkt bankayfirlitslínur og bankareikningsfærslur
1. Í gluggans **afstemming bankareiknings** veldu tvo ójafnaðar línur í **bankayfirlitslínur** svæðinu.
2. Á svæðinu **bankareikningsfærslur** skal velja eina eða fleiri bankareikningsfærslur sem hægt er að jafna við valda bankayfirlitslínu. Til að velja margar línur skal halda inni Ctrl-lyklinum.
3. Velja **Handvirk jöfnun** aðgerð.

    Letur valinnar bankayfirlitslínu og valinna bankareikningsfærslna verður grænt og gátreiturinn **Jafnað** á hægra svæðinu er valinn.
4. Endurtakið liði 1 til 3 fyrir allar bankayfirlitslínur sem ganga af.
5. Til að fjarlægja jöfnun skal velja bankareikningslínu og velja svo aðgerðina **fjarlægja jöfnun**.

## <a name="to-create-missing-ledger-entries-to-match-bank-transactions-with"></a>Að stofna fjárhagsfærslur sem vantar til að jafna bankafærslur við
Stundum geta verið vextir eða kostnaður á bankayfirlitinu. Slíkar bankafærslur geta ekki verið jafnaðar vegna þess að engar tilsvarandi fjárhagsfærslur eru til í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þú verður þá að bóka færslubókarlínu fyrir hverja færslu til að stofna tilsvarandi fjárhagsfærslu sem það má jafna við.

1. Í glugganum **Afstemming bankareiknings** er valið aðgerðina **flytja í almenn færslubók**  
2. Í glugganum **Flytja bankaafstemmingu í almenna færslubók** skal tilgreina hvaða almenn færslubók skal nota, og veldu svo **OK** hnappinn.

    Glugginn **almenn færslubók** opnast og inniheldur nýjar færslubókarlínur fyrir allar bankayfirlitslínur með fjárhagsfærslur sem vantar.
3. Kláraðu færslubókarlína með viðeigandi upplýsingar, eins og mótreikningur. Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).  
4. Til að yfirfara niðurstöður bókunar áður en þú bókar skaltu velja aðgerina **Prófunarskýrsla**. Skýrslan **Bankareikningsyfirlit** opnast og sýnir sömu reitina og í hausnum á glugganum **Afstemming bankareiknings**.
4. Valið er **Bóka** aðgerðin.

    Þegar færslan er bókuð, farðu þá í að jafna bankafærsluna við hana.
5. Uppfærðu eða opnaðu aftur **afstemming bankareiknings** gluggann. Nýji fjárhagsfærslan birtist í **bankareikningsfærslur** svæðinu.
6. Jafnaðu bankayfirlitslínu með bankareikningsfærslu, annað hvort handvirkt eða sjálfkrafa.

## <a name="see-also"></a>Sjá einnig
[Stjórna bankareikningum](bank-manage-bank-accounts.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

