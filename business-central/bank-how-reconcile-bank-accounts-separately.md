---
title: Afstemma bankareikninga
description: Kynntu þér hvernig hægt er að afstemma færslur í Business Central við færslur í bankayfirlitum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.search.form: 379, 388, 389, 1290, 1692, 10124
ms.date: 08/16/2022
ms.author: bholtorf
ms.openlocfilehash: 80c8ca9f1fa9d32ae7738f95d99fc01cd0e7e548
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605354"
---
# <a name="reconcile-bank-accounts"></a>Afstemma bankareikninga

Afstemming banka hjálpar til við að tryggja að það sem er í bókhaldinu þínu passi við yfirlitin sem þú færð frá bankanum. Afstemming bankareiknings ber saman og samsvarar færslur á bankareikningunum sem þú hefur sett upp í [!INCLUDE[prod_short](includes/prod_short.md)] við bankafærslur í bankanum þínum. Afstemming getur síðan lagt innistæðurnar inn á bankareikningana þína í [!INCLUDE[prod_short](includes/prod_short.md)] svo að fjármálastjórar geti nálgast þær. Bankaafstemming er einnig hagkvæm leið til að uppgötva og leysa úr greiðslum sem vantar upp á og bókhaldsvillum.

Í þessu efnisatriði er lýst hvernig eigi að afstemma bankareikninga á síðunni **Afstemma bankareikninga**.

> [!TIP]
> Einnig er hægt að stemma af bankareikninga á síðunni **greiðsluafstemmingarbók** þegar greiðsla er meðhöndluð. Allar opnar fjárhagsfærslur bankareiknings sem tengjast jöfnuðum fjárhagsfærslum viðskiptavinar eða lánardrottins verða lokaðar þegar þú velur **Bóka Greiðslur og stemma Af Bankareikninga** aðgerð. Þetta stemmir af bankareikninginn sjálfkrafa fyrir greiðslunum sem bókaðar eru með færslubókinni. Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> Í norður-amerískum útgáfum getur þú einnig gert þetta á síðunni **Vinnublað bankaafstemmingar** sem hentar betur fyrir ávísanir og innborganir en leyfir þér ekki að flytja inn bankayfirlitsskrár. Til að nota þennan glugga í staðinn fyrir gluggann **Afstemming bankareikninga** skaltu hreinsa reitinn **Bankareikn.afstemming með sjálfvirkri jöfnun** á síðunni **Fjárhagsgrunnur**. Frekari upplýsingar er hægt að finna í [Afstemma bankareikninga](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) sem heyrir undir staðbundnar aðgerðir Bandaríkjanna.

Línur síðunnar **Afstemming bankareiknings** skiptast í tvö svæði. **BankaYfirlitslínur** svæðinu sýnir annað hvort innfluttra bankafærslur eða fjárhagsfærslur með útistandandi greiðslur. **Bankareikningsfærslur** svæðið sýnir fjárhagsfærslur á innri bankareikning.

Að afstemma færslur í yfirlitum úr bankanum þínum við bankafærslur í [!INCLUDE[prod_short](includes/prod_short.md)] er vísað í sem *jöfnun*. Hægt er að velja að jafna sjálfkrafa með því að nota aðgerðina **Jafna sjálfkrafa**. Einnig er hægt að velja línur handvirkt á báðum svæðum til að tengja hverja bankareikningslínu við eina eða fleiri tengdar fjárhagsfærslur bankareiknings og nota síðan aðgerðina **Handvirk jöfnun**. **Jafnað** gátreitur er valinn í línum þar sem færslurnar eru samsvarandi. Frekari upplýsingar eru í [Setja upp reglur fyrir sjálfvirka jöfnun á greiðslum](receivables-how-set-up-payment-application-rules.md).

> [!NOTE]  
> Ef bankayfirlitslínur tengjast tékkafærslum er ekki hægt að nota samsvörunaraðgerðirnar. Í staðinn þarf að velja aðgerðina **Jafna færslur** og velja síðan viðkomandi tékkafrærslu til að jafna bankayfirlitslínuna með.

Þegar gildið í reitnum **Heildarstaða** á svæðinu **Bankauppgjörslínur** er jafnt og gildið í reitnum **Staða til afstemmingar** ásamt reitnum **Staða síðasta yfirlits** á svæðinu **Fjárhagsfærslur bankareiknings** geturðu valið aðgerðina **Bóka**. Ójafnaðar fjárhagsfærslur bankareiknings verða áfram á síðunni, sem gefur til kynna misræmi sem ætti að leysa úr til að stemma bankareikninginn af.

Til að fara yfir afstemmingu bankareikningsins áður en þú bókar skaltu nota aðgerðina **Prófunarskýrsla** til að undirbúa forskoðun á afstemmingunni. Skýrslan er aðgengileg í eftirfarandi samhengi:

* Þegar bankaafstemming er undirbúin á síðunni **Afstemming bankareiknings**.
* Þegar greiðslur eru stemmdar af á síðunni **Greiðsluafstemmingarbækur**.

Allar línur sem ekki er hægt að jafna, gefið til kynna með gildi í reitnum **Mismunur**, verða áfram á síðunni **Afstemming bankareiknings** eftir bókun. Þær tákna einhverskonar misræmi sem nauðsynlegt er að leysa úr áður en hægt er að ljúka afstemmingu bankareiknings. Dæmigerðar aðstæður fyrirtækis sem gætu valdið mismun:

| Mismunur | Ástæða | Upplausn |
|------------|--------|------------|
| Færsla á bankareikningnum í [!INCLUDE[prod_short](includes/prod_short.md)] er ekki á bankayfirlitinu. | Bankafærslan var ekki stofnuð þótt bókun hafi farið fram í [!INCLUDE[prod_short](includes/prod_short.md)]. | Stofnaðu færsluna sem vantar upp á (eða biddu skuldunaut um að gera það). Flyttu síðan bankayfirlitsskrána aftur inn eða færður færsluna inn handvirkt. |
| Færsla á bankayfirlitinu er ekki til sem skjal eða færslubókarlína í [!INCLUDE[prod_short](includes/prod_short.md)]. | Bankafærsla var gerð án samsvarandi bókunar í [!INCLUDE[prod_short](includes/prod_short.md)], til dæmis bókun færslubókarlínu fyrir kostnað. | Búið til og bókið færsluna sem vantar. Fljótleg leið til að koma þessu í verk er að finna í [Að stofna fjárhagsfærslur sem vantar til að jafna bankafærslur við](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| Færsla á innri bankareikningi samsvarar bankafærslu en einhverjar upplýsingar eru of ólíkar til að gefa samsvörun. | Upplýsingar, t.d. upphæð eða nafn viðskiptavinar, voru færðar inn á annan hátt í bankafærslunni eða innri bókun. | Yfirfara skal upplýsingarnar og síðan jafna færslurnar tvær. Valfjrálst, leiðréttu ósamræmið. |

Leysa þarf úr muninum, til dæmis með því að stofna færslur sem vantar og leiðrétta upplýsingar sem samsvarast ekki, eða með því að klára peningafærslur sem vantar, þar til hægt er að klára og bóka afstemmingu bankareiknings.

Hægt er að fylla á **Bankayfirlitslínur** svæðið á síðunni **afstemming bankareiknings** á eftirfarandi hátt:

* Sjálfvirkt, með því að nota **Flytja inn bankayfirlit** aðgerðina til að fylla í svæðið **Bankayfirlitslínur** með bankafærslum samkvæmt innfluttri skrá eða streymi sem bankinn býður upp á.
* Handvirkt, með því að nota **Leggja til línur** aðgerðina til að fylla í svæðið **Bankayfirlitslínur** samkvæmt reikningum í [!INCLUDE[prod_short](includes/prod_short.md)] sem eru með útistandandi greiðslur.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Fylla inn í línur bankaafstemmingar með því að flytja inn bankayfirlit.

Svæðið **Bankayfirlitslínur** verður fylllt út með bankafærslum í samræmi við innflutta skrá eða streymi sem bankinn lætur í té.

Til að flytja inn bankayfirlit sem bankastreymi þarf að setja upp bankastreymisþjónustuna Envestnet Yodlee. Uppsetningin felur í sér að tengja bankareikningana þína í [!INCLUDE[prod_short](includes/prod_short.md)] við tengda netbankareikninga. Frekari upplýsingar eru í [Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> Einnig er hægt að flytja inn bankayfirlitsskrár á sniði kommu eða semíkommu (.CSV). Notið **Setja upp snið bankayfirlitsskráar** uppsetninguna með hjálp til að skilgreina innflutningssnið bankayfirlits og festa sniðið við bankareikning. Síðan er hægt að nota þessi snið þegar bankayfirlit er flutt inn á síðuna **Afstemming bankareiknings**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Afstemming bankareiknings** og velja síðan viðkomandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Í reitnum **Reikningur nr.** er viðkomandi bankareikningskóti valinn. bankareikningsfærslur sem eru til staðar á bankareikningi birtast í svæðinu **Bankareikningsfærslur**.
4. Í reitinn **Dagsetning yfirlits** er færð dagsetning bankayfirlitsins.
5. Í **Lokastaða yfirlits** reitnum, færðu inn stöðu yfirlits frá bankanum.
6. Ef þú ert með bankayfirlitsskrá, veldu **flytja inn bankayfirlit** aðgerðina.
7. Staðsetja skal skrána og velja svo hnappinn **Opna** til að flytja inn bankafærslurnar á línurnar á svæðinu **Bankayfirlitslínur** á síðunni **Afstemming bankareiknings**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>að fylla út línur í bankaafstemmingu með aðgerðin Tillögulínur

Svæðið **Bankayfirlitslínur** verður fyllt út samkvæmt reikningum í [!INCLUDE[prod_short](includes/prod_short.md)] sem eru með útistandandi greiðslur.  

1. Á síðunni **Afstemming bankareiknings** er valið á **Tillögulínur** aðgerð.
2. Í reitinn **Upphafsdagsetning** er færð inn fyrsta bókunardagsetning fyrir fjárhagsfærslurnar sem á að stemma af.
3. Í reitinn **lokadagsetning** er færð inn bókunardagsetning fyrir fjárhagsfærslurnar sem á að stemma af.

> [!NOTE]
> Venjulega mun lokadagsetningin samsvara dagsetningunni sem tilgreind er í reitnum **Dagsetning yfirlits**. Ef þú vilt hins vegar afstemma færslur fyrir hluta úr tímabili getur þú fært inn aðra lokadagsetningu.

4. Ef þú vilt ekki að fjárhagsfærslur bankareikningsins innihaldi ójafnaðar opnar bakfærslur skaltu velja víxlhnappinn **Útiloka bakfærslur**. Listinn yfir fjárhagsfærslur bankareiknings munu sjálfgefið innihalda bakfærslur fram að dagsetningu yfirlitsins.
5. Velja hnappinn **Í lagi**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>að jafna sjálfkrafa bankayfirlitslínur og bankareikningsfærslur

Síðan **Afstemming bankareiknings** býður upp á sjálfvirkar samsvörunaraðgerðir sem byggja á samsvörun texta í bankayfirlitslínu (vinstri rúðunni) við texta í einni eða fleiri fjárhagsfærslum bankareiknings (hægri rúðunni). Þú getur skrifað yfir ráðlagðar sjálfvirkar jafnanir og þú getur valið að nota ekki sjálfvirkar jafnanir yfirhöfuð. Frekari upplýsingar er að finna í [Að jafna handvirkt bankayfirlitslínur við bankareikningsfærslur](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

Hægt er að skoða nánar grundvöll jöfnunar með því að nota aðgerðina **Upplýsingar um samsvörun**. Upplýsingarnar munu til að mynda innihalda heiti reitanna sem innihéldu samsvarandi gildi.  

1. Á síðunni **Afstemming bankareiknings** er valið **jafna sjálfkrafa**. Síðan **Jafna bankafærslur** opnast.
2. Í reitnum **Vikmörk færsludagsetningar (dagar)** skal tilgreina þann fjölda daga fyrir og eftir bókunardagsetningu fjárhagsfærslu bankareiknings sem hafður er með í leitinni að samsvarandi færsludagsetningum á bankayfirlitinu.

    Ef 0 er slegið inn eða reiturinn hafður auður leitar aðgerðin **Sjálfvirk jöfnun** aðeins eftir samstæðum færsludagsetningum í bókunardagsetningu á bankareikningsfærslum.
3. Velja hnappinn **Í lagi**.

    Allar bankayfirlitslínur og fjárhagsfærslur bankareiknings sem hægt er að jafna verða grænar og gátreiturinn **Jafnað** er valinn.
4. Til að fjarlægja jöfnun skal velja bankareikningslínu og velja svo aðgerðina **fjarlægja jöfnun**.

> [!TIP]
> Hægt er að nota blöndu af handvirkri og sjálfvirkri jöfnun. Ef þú hefur jafnað færslur handvirkt mun sjálfvirk jöfnun ekki skrifa yfir valið þitt.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Að jafna handvirkt bankayfirlitslínur og bankareikningsfærslur

> [!TIP]
> Þegar línur og færslur eru jafnaðar handvirkt geta aðgerðirnar **Sýna allt**, **Sýna bakfærðar færslur**, **Fela bakfærðar færslur** og **Sýna ójafnað** gert auðveldara að fá yfirsýn. Sjálfgefið innihalda fjárhagsfærslur bankareikningsins ekki ójafnaðar bakfærðar færslur. Til að hafa þessar færslur á listanum og jafna þær handvirkt skaltu velja aðgerðina **Sýna bakfærðar færslur**. Ef þú velur að fela bakfærðar færslur eftir að þú hefur gert eina eða fleiri jafnanir, eru jöfnuðu færslurnar ennþá sýndar.

1. Á síðunni **Afstemming bankareiknings** skal velja tvær ójafnaðar línur í **Bankayfirlitslínur** svæðinu.
2. Á svæðinu **bankareikningsfærslur** skal velja eina eða fleiri bankareikningsfærslur sem hægt er að jafna við valda bankayfirlitslínu. Til að velja margar línur skal halda inni CTRL-lyklinum og síðan velja línurnar.

   > [!TIP]
   > Einnig er hægt að jafna handvirkt margar línur bankayfirlits við eina fjárhagsfærslu bankareiknings. Þetta gæti til dæmis reynst gagnlegt ef bankainnborgunin þín inniheldur ýmsa greiðslumáta, t.d. kreditkort frá ólíkum útgefendum, og bankinn þinn sýnir þá í aðskildum línum.
3. Velja **Handvirk jöfnun** aðgerð.

    Letur valinnar bankayfirlitslínu og valinna bankareikningsfærslna verður grænt og gátreiturinn **Jafnað** á hægra svæðinu er valinn.
4. Endurtakið skref 1 til 3 fyrir allar bankayfirlitslínur sem eru ekki jafnaðar.

> [!TIP]
> Til að fjarlægja jöfnun skal velja bankareikningslínu og velja svo aðgerðina **fjarlægja jöfnun**. Ef margar bankayfirlitslínur hafa verið jafnaðar við fjárhagsfærslu og þú þarft að fjarlægja eina eða fleiri jafnaðar línur, eru allar handvirkar jafnanir fjarlægðar fyrir fjárhagsfærsluna þegar þú velur **Fjarlægja jöfnun**.

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines"></a>Að stofna fjárhagsfærslur sem vantar til að jafna bankayfirlitslínur

Stundum inniheldur bankayfirlit upphæðir fyrir vexti eða gjöld. Ekki er hægt að jafna slíkar bankayfirlitslínur vegna þess að engar tengdar fjárhagsfærslur eru í [!INCLUDE[prod_short](includes/prod_short.md)]. Þú verður þá að bóka færslubókarlínu fyrir hverja færslu til að stofna tilsvarandi fjárhagsfærslu sem það má jafna við.

1. Á síðunni **Afstemming bankareiknings** er valið aðgerðin **Flytja í almenna færslubók**.  
2. Á síðunni **Flytja bankaafstemmingu í almenna færslubók** skal tilgreina hvaða almenn færslubók skal nota, og veldu svo **OK** hnappinn.

    Síðan **almenn færslubók** opnast og inniheldur nýjar færslubókarlínur fyrir allar bankayfirlitslínur með fjárhagsfærslur sem vantar.
3. Kláraðu færslubókarlína með viðeigandi upplýsingar, eins og mótreikningur. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).  
4. Til að yfirfara niðurstöður bókunar áður en þú bókar skaltu velja aðgerina **Prófunarskýrsla**. Skýrslan **Bankareikningsyfirlit** opnast og sýnir sömu reitina og í hausnum á síðunni **Afstemming bankareiknings**.
5. Valið er **Bóka** aðgerðin.

    Þegar færslan er bókuð skal jafna bankayfirlitslínuna við hana.
6. Uppfærðu eða opnaðu aftur **afstemming bankareiknings** síðuna. Nýji fjárhagsfærslan birtist í **bankareikningsfærslur** svæðinu.
7. Jafnaðu bankayfirlitslínu með bankareikningsfærslu, annað hvort handvirkt eða sjálfkrafa.

## <a name="find-outstanding-transactions-previous-periods"></a>Finna útistandandi færslur fyrri tímabila
Hægt er að nota skýrslu bankayfirlitsins til að finna útistandandi færslur á fyrri tímabilum. Útistandandi færslur voru opnaðar á undan dagsetningu yfirlitsins og þeim hefur ekki verið lokað eða var lokað eftir að bankaafstemmingin var bókuð.

Þegar bankayfirlitsskýrslan er keyrð af listasíðu bankayfirlitsins er hægt að kveikja á útistandandi færslum og skýrslan mun innihalda hluta sem sýnir útistandandi færslur.

**Dæmi** Við erum með fjárhagsfærslur A, B og C á bankareikningnum okkar fyrir ágústmánuð. Þegar við afstemmum bankareikninginn okkar fyrir ágúst finnum við bankayfirlitslínuna sem passar við færslu A, en enga fyrir B og C. Svo við bókum afstemminguna með færslu A afstemmda og B og C sem útistandandi færslur.

Í september fáum við greiðslu fyrir færslu B og ákveðum að stemma af bankareikning okkar. Ef við keyrum bankayfirlitsskýrsluna áður en við bókum afstemminguna fáum við eina afstemmda færslu og eina útistandandi.

Ef við prentum skýrsluna fyrir ágúst fáum við útistandandi færslur fyrir færslur B og C, jafnvel þótt við höfum lokað færslu B í september.

## <a name="undo-a-bank-account-reconciliation"></a>Hætta við afstemmingu bankareiknings
Ef mistök finnast í bókaðri bankaafstemmingu er hægt að nota aðgerðina **Afturkalla** á síðunni **Bankareikningsyfirlit** til að leiðrétta þau. Þegar bókuð bankaafstemming er afturkölluð verða færslur færðar á síðuna **Bankaafstemming** og merktar sem **Opnar**, sem þýðir að þær eru ekki afstemmdar. Þá er hægt að leiðrétta bankaafstemminguna og bóka hana aftur.

> [!NOTE]
> Í norður-amerísku útgáfunni, til að nota afturköllunaraðgerðina fyrir bókaðar bankaafstemmingar og bankayfirlit, þarf að kveikja á **Bankaafstemming með sjálfvirkri samsvörun** á síðunni **Uppsetning fjárhagsgrunns**. Afturköllunaraðgerðin er ekki í boði fyrir bankayfirlit sem bókuð eru í vinnublöðum bankaafstemmingar.

### <a name="reusing-the-bank-statement-number"></a>Bankayfirlitsnúmer notað aftur
Bankayfirlitsnúmerið sem er notað fyrir nýja bankaafstemmingu er fengið frá bankareikningnum sem er staða síðasta yfirlits. Hægt er að breyta þessum gildum áður en ný bankaafstemming er gerð. Hinsvegar, þegar ný bankaafstemming er stofnuð, athugar [!INCLUDE[d365fin](includes/d365fin_md.md)] hvort númer yfirlitsins sé þegar úthlutað á bókað bankayfirlit. Ef númerið er í notkun, en ætlunin er að nýja bankayfirlitið noti það í staðinn, er hægt að nota **Breyta yfirlitsnr.** aðgerðina á síðunni **Afstemming bankareiknings**.

### <a name="examples"></a>Dæmi
Eftirfarandi dæmi sýna hvernig á að lagfæra mistök í bókaðri bankaafstemmingu með eða án þess að nota sama yfirlitsnúmerið.

#### <a name="example-1"></a>Dæmi 1
Bankaafstemmingar voru fyrir janúar, febrúar og mars. Númer bankayfirlits var 100 fyrir mars. Seinna uppgötvast að mars innihélt aðeins færslur til 30. mars, sem þýðir að það vantar færslur frá 31. Þar af leiðandi þarf að endurgera bankaafstemminguna fyrir mars. Í slíku tilfelli opnum við síðuna **Bankareikningsyfirlit**, veljum yfirlitið fyrir mars og veljum síðan **Afturkalla**. 

Nýju bankaafstemmingunni er gefið yfirlitsnúmerið 101. Til að endurúthluta númerinu 100 skal velja **Breyta yfirlitsnr.** og færið inn **100**. 

> [!TIP]
> Munið að stilla viðeigandi lokadagsetningu yfirlits (í þessu dæmi er það 31. mars) og breytið reitnum **Staða síðasta yfirlits**. 

#### <a name="example-2"></a>Dæmi 2
Bankaafstemmingar voru fyrir janúar, febrúar, júní og júlí. Þú sérð að febrúar var rangur. Gerum ráð fyrir að þar hafi verið yfirlitsnúmerið 100. Eins og í dæmi 1 eru aðgerðirnar Afturkalla og Breyta yfirlitsnr. til að breyta yfirlitsnúmerinu eins og í dæmi #1 hér fyrir ofan og nú er hægt að endurgera bankaafstemmingu í febrúar.  

Þegar búið er að bóka leiðrétta bankaafstemmingu fyrir febrúar, mun á samsvarandi bankareikningsspjaldi reiturinn **Síðasta yfirlitsnr.** sýna **100** og reiturinn **Staða síðasta yfirlits** mun sýna lokastöðuna fyrir yfirlitið í febrúar. 

Ef næst er gerð bankaafstemming fyrir mars mun [!INCLUDE[d365fin](includes/d365fin_md.md)] úthluta 101 sem yfirlitsnúmeri og gefa því rétta **Stöðu síðasta yfirlits**.

Ef næst er gerð bankaafstemming fyrir ágúst skal íhuga að breyta gildunum í reitunum **Síðasta yfirlitsnr.** og **Staða síðasta yfirlits** á spjaldinu **Bankareikningur** áður en næsta bankaafstemming er stofnuð, eða nota aðgerðina **Breyta yfirlitsnr.** og einnig breyta gildinu í reitnum **Staða síðasta yfirlits** á síðu bankaafstemmingar.

> [!NOTE]
> Yfirlitsnúmerið er mikilvægt þegar bankaafstemmingar eru gerðar með innfluttum CAMT-skrám sem innihalda yfirlitsnúmer, eða þegar afstemming er gerð samkvæmt prentuðum bankayfirlitum. Ef safn af bankafærslum er einfaldlega sótt af netbankanum er yfirlitsnúmerið yfirleitt ekki mikilvægt.  
>
> Staða síðasta yfirlits er geymt á bankareikningnum til að draga úr mistökum þegar bankaafstemmingar eru gerðar, en einnig er hægt að breyta því, sem gerir kleift að gera bankaafstemmingarnar í hvaða röð sem er. Þetta þýðir einnig að ef bankayfirlit er afturkallað gæti verið að nýja lokastaðan verði ekki staða síðasta yfirlits á bankayfirlitinu. Enginn eiginleiki er til staðar sem gerir kleift að áframsenda öll síðari bankayfirlit, því skal hafa það í huga þegar Afturköllun er gerð.  

## <a name="avoid-direct-posting"></a>Forðist beina bókun

Ekki nota fjárhagsreikning sem leyfir beina bókun í bókunarflokki bankareikningsins. Bein bókun mun rjúfa tengslin milli fjárhagsfærslu bankareikningsins og fjárhagsfærslu fjárhagsreikningsins. Þegar kosið er að afstemma bankareikninginn verða færslurnar sem bókaðar eru beint á fjárhagsreikninginn ekki hafðar með og verður því erfitt að ljúka afstemmingunni.

Þessi mistök eiga sér oft stað þegar farið er í opnunarstöðu fyrir bankareikning. Mikilvægt er að bóka ekki opnunarstöðuna beint í fjárhaginn. Færslur á fjárhagsreikningnum sem eru bókaðar beint á fjárhagsreikninginn munu valda vandræðum. Þessar færslur gætu til dæmis komið í veg fyrir að þú getir stemmt af bankareikninginn þinn. Fyrir bankareikninga í erlendum gjaldmiðli geta færslurnar valdið því að mismunur safnist upp eftir að þú bókar fleiri bankaafstemmingar vegna gengisleiðréttinga gjaldmiðils. Oft er opnunarstaða í banka bókuð beint á bankareikninginn og upphæðin endar þá á fjárhagsreikningnum. Að öðrum kosti bakfærir þú hana á móti fjárhagsreikningnum sem þú notar til að jafna opnunarstöðu fjárhagsins. Í báðum tilvikum þarf að jafna allar beinar bókanir á fjárhagsreikninginn áður en þú byrjar fyrstu bankaafstemminguna og sérstaklega ef bankareikningurinn er í erlendum gjaldmiðli.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig
[Afstemming bankareikninga](bank-manage-bank-accounts.md)  
[Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Reglur settar upp fyrir sjálfvirka jöfnun á greiðslum](receivables-how-set-up-payment-application-rules.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
