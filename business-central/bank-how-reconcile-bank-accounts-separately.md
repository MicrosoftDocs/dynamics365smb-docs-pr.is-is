---
title: Afstemma bankareikninga
description: Lærðu að stemma af færslur í Aðalviðskiptum með færslur í uppgjörum frá bankanum þínum.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605354"
---
# <a name="reconcile-bank-accounts"></a>Afstemma bankareikninga

Bankaafstemmingar aðstoða þig við að tryggja að það sem er í bókunum þínum samsvari þeim fullyrðingum sem þú færð frá bankanum þínum. Afstemmingu bankareikninga ber saman og stemmir færslur á bankareikninginn sem sett var upp í [!INCLUDE[prod_short](includes/prod_short.md)] bankaviðskiptum við bankann þinn. Afstemmingu er síðan hægt að bóka á Bankareikningar í [!INCLUDE[prod_short](includes/prod_short.md)] til að gera þær aðgengilegar fyrir fjármálastjórar. Bankaafstemming er einnig hagkvæm leið til að uppgötva og leysa úr greiðslum sem vantar upp á og bókhaldsvillum.

Í þessu efnisatriði er **lýst hvernig á að stemma af bankareikninga af Afstemmingarsíðunni** Bankareikningar.

> [!TIP]
> Einnig er hægt að stemma af bankareikninga á síðunni **greiðsluafstemmingarbók** þegar greiðsla er meðhöndluð. Opnum bankareikningsfærslur sem tengjast jafnaðar viðskiptamanna-eða lánardrottnafærslum verða lokaðar þegar valið er að **Bóka greiðslur og afstemma bankareikningsaðgerðir**. Þetta stemmir af bankareikninginn sjálfkrafa fyrir greiðslunum sem bókaðar eru með færslubókinni. Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> Í Norður-Ameríkuútgáfum er einnig hægt að gera þetta á **Innkaupatillögusíðu** bankans, sem er betur hentug fyrir ávísanir og innlán en ekki láta flytja inn bankayfirlitsskrár. Til að nota þennan glugga í staðinn fyrir gluggann **Afstemming bankareikninga** skaltu hreinsa reitinn **Bankareikn.afstemming með sjálfvirkri jöfnun** á síðunni **Fjárhagsgrunnur**. Frekari upplýsingar er hægt að finna í [Afstemma bankareikninga](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) sem heyrir undir staðbundnar aðgerðir Bandaríkjanna.

Línur síðunnar **Afstemming bankareiknings** skiptast í tvö svæði. **BankaYfirlitslínur** svæðinu sýnir annað hvort innfluttra bankafærslur eða fjárhagsfærslur með útistandandi greiðslur. **Bankareikningsfærslur** svæðið sýnir fjárhagsfærslur á innri bankareikning.

Það að stemma af færslur í uppgjörum frá bankanum þínum með bankafærslum í [!INCLUDE[prod_short](includes/prod_short.md)] er vísað til *samsvarandi*. Hægt er að velja að stemma sjálfkrafa við með **aðgerðinni samsvara sjálfkrafa**. Einnig er hægt að velja línur handvirkt í báðum rúðum til að tengja hverja bankayfirlitslínu við eina eða fleiri tengdar bankareikningsfærslur og nota **síðan samsvörin aðgerð handvirkt**. **Jafnað** gátreitur er valinn í línum þar sem færslurnar eru samsvarandi. Frekari upplýsingar eru í [Setja upp reglur fyrir sjálfvirka jöfnun á greiðslum](receivables-how-set-up-payment-application-rules.md).

> [!NOTE]  
> Ef bankayfirlitslínur tengjast tékkafærslum er ekki hægt að nota samsvörunaraðgerðirnar. Í staðinn þarf að velja aðgerðina **Jafna færslur** og velja síðan viðkomandi tékkafrærslu til að jafna bankayfirlitslínuna með.

Þegar gildið í **reitnum Heildarstaða** í **rúðunni línur** bankayfirlits jafnast út heildarvirði **stöðu til að stemma** svæði við reitinn **Staða í Síðasta uppgjöri** í **glugganum bankareikningsfærslur** er hægt að **Velja aðgerðina Bóka**. Ójafnar bankareikningsfærslur eru eftir á síðunni, sem gefur til kynna misræmi sem ætti að leysa til að stemma bankareikninginn af.

Ef tvöfalda á afstemmingu bankareiknings áður en hann er bókaður skal nota **aðgerðina Prófunarskýrsla** til að undirbúa forskoðun á afstemmingu. Skýrslan er aðgengileg í eftirfarandi samhengi:

* Þegar verið er að undirbúa afstemmingu banka á **afstemmingarsíðu** bankans.
* Þegar verið er að stemma af greiðslur á **síðunni Greiðsluafstemmingarbækur**.

Allar línur sem ekki er hægt að jafna, gefið til kynna með gildi í reitnum **Mismunur**, verða áfram á síðunni **Afstemming bankareiknings** eftir bókun. Þær tákna einhverskonar misræmi sem nauðsynlegt er að leysa úr áður en hægt er að ljúka afstemmingu bankareiknings. Dæmigerðar aðstæður fyrirtækis sem gætu valdið mismun:

| Mismunur | Ástæða | Upplausn |
|------------|--------|------------|
| Færsla á bankareikninginn þinn í [!INCLUDE[prod_short](includes/prod_short.md)] er ekki á bankayfirlitinu. | Bankafærsla var ekki stofnuð þótt bókun væri gerð í [!INCLUDE[prod_short](includes/prod_short.md)]. | Stofnið færsluna sem vantar (eða Hvetjið debitor til að gera hana). Síðan skal flytja bankayfirlitskrána inn eða færa færsluna inn handvirkt. |
| Færsla á bankayfirliti er ekki til sem fylgiskjal eða færslubókarlína í [!INCLUDE[prod_short](includes/prod_short.md)]. | Bankafærsla var gerð án samsvarandi bókunar í [!INCLUDE[prod_short](includes/prod_short.md)], til dæmis bókun færslubókarlínu fyrir kostnað. | Búið til og bókið færsluna sem vantar. Til að læra flýtileið til að gera það, sjá [til að stofna færslur sem eiga að samsvara bankafærslum með](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines). |
| Færsla á innri bankareikningi samsvarar bankafærslu en einhverjar upplýsingar eru of ólíkar til að gefa samsvörun. | Upplýsingar, svo sem upphæð eða nafn viðskiptavinar, var fært inn á annan hátt í bankafærslu eða innri bókun. | Yfirfara skal upplýsingarnar og síðan jafna færslurnar tvær. Að öðrum kosti skal leiðrétta Vanskil. |

Þú verður að leysa mismuninn, til dæmis með því að stofna færslur sem vantar og leiðrétta þær eða með því að týna peningafærslum þar til hægt er að ljúka og bóka afstemmingu bankareiknings.

Hægt er að fylla á **Bankayfirlitslínur** svæðið á síðunni **afstemming bankareiknings** á eftirfarandi hátt:

* Sjálfvirkt, með því að nota **Flytja inn bankayfirlit** aðgerðina til að fylla í svæðið **Bankayfirlitslínur** með bankafærslum samkvæmt innfluttri skrá eða streymi sem bankinn býður upp á.
* Handvirkt, með því að nota **Leggja til línur** aðgerðina til að fylla í svæðið **Bankayfirlitslínur** samkvæmt reikningum í [!INCLUDE[prod_short](includes/prod_short.md)] sem eru með útistandandi greiðslur.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Fylla inn í línur bankaafstemmingar með því að flytja inn bankayfirlit.

Svæðið **Bankayfirlitslínur** verður fylllt út með bankafærslum í samræmi við innflutta skrá eða streymi sem bankinn lætur í té.

Ef flytja á bankayfirlit inn sem bankastraum verður að setja upp Envestnet Yodlee Bank Feed Service. Uppsetningin felur í [!INCLUDE[prod_short](includes/prod_short.md)] sér að tengja bankareikninga þína við tengda netbankareikninga. Frekari upplýsingar eru í [Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md).  

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

4. Ef ekki er óskað eftir að bankareikningsfærslurnar taki til ófyrirframopinnar bakfærðar færslur skal velja víxla fyrir **Ósamfærðar færslur**. Sjálfgefið er að bankareikningsfærslur með bakfærða færslu eru færðar inn á uppgjörsdagsetninguna.
5. Velja hnappinn **Í lagi**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>að jafna sjálfkrafa bankayfirlitslínur og bankareikningsfærslur

Síðan **Afstemming bankareiknings** býður upp á sjálfvirkar samsvörunaraðgerðir sem byggja á samsvörun texta í bankayfirlitslínu (vinstri rúðunni) við texta í einni eða fleiri fjárhagsfærslum bankareiknings (hægri rúðunni). Hægt er að skrifa yfir leiðbeinanda Sjálfvirk samsvörun og þá má velja að nota ekki sjálfvirka jöfnun yfirleitt. Frekari upplýsingar er að finna í [Að jafna handvirkt bankayfirlitslínur við bankareikningsfærslur](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

Hægt er að skoða nánar grundvöll jöfnunar með því að nota aðgerðina **Upplýsingar um samsvörun**. Upplýsingarnar munu til að mynda innihalda heiti reitanna sem innihéldu samsvarandi gildi.  

1. Á síðunni **Afstemming bankareiknings** er valið **jafna sjálfkrafa**. Síðan **Jafna bankafærslur** opnast.
2. Í reitnum **Vikmörk færsludagsetningar (dagar)** skal tilgreina þann fjölda daga fyrir og eftir bókunardagsetningu fjárhagsfærslu bankareiknings sem hafður er með í leitinni að samsvarandi færsludagsetningum á bankayfirlitinu.

    Ef 0 er slegið inn eða reiturinn hafður auður leitar aðgerðin **Sjálfvirk jöfnun** aðeins eftir samstæðum færsludagsetningum í bókunardagsetningu á bankareikningsfærslum.
3. Velja hnappinn **Í lagi**.

    Allar línur bankayfirlits og bankareikningsfærslur sem hægt er að breyta í grænt letur eru valdar og **notaður** gátreiturinn er valinn.
4. Til að fjarlægja jöfnun skal velja bankareikningslínu og velja svo aðgerðina **fjarlægja jöfnun**.

> [!TIP]
> Hægt er að nota blöndu af handvirkri og sjálfvirkri jöfnun. Ef þú hefur jafnað færslur handvirkt mun sjálfvirk jöfnun ekki skrifa yfir valið þitt.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Að jafna handvirkt bankayfirlitslínur og bankareikningsfærslur

> [!TIP]
> Þegar samsvarandi línur og færslur eru handvirkt eru þær **sem** **Sýna bakfærðar** **færslur, hylja bakfærðar færslur** og **Sýna ósamjöfnuð** . auðveldara er að fá yfirlit. Bankareikningsfærslurnar innihalda ekki ójafnar bakfærðar færslur. Ef taka á þessar færslur með í listanum og jafna þær handvirkt skal velja **aðgerðina Sýna bakfærðar færslur**. Ef þú velur að fela bakfærðar færslur eftir að ein eða fleiri samstæður hafa verið gerðar, þá eru samsvarandi færslur enn sýndar.

1. Á síðunni **Afstemming bankareiknings** skal velja tvær ójafnaðar línur í **Bankayfirlitslínur** svæðinu.
2. Á svæðinu **bankareikningsfærslur** skal velja eina eða fleiri bankareikningsfærslur sem hægt er að jafna við valda bankayfirlitslínu. Til að velja margar línur er ýtt á CTRL-lyklinum og síðan valið línurnar.

   > [!TIP]
   > Einnig er hægt að jafna handvirkt margar línur bankayfirlits við eina fjárhagsfærslu bankareiknings. Þetta gæti til dæmis reynst gagnlegt ef bankainnborgunin þín inniheldur ýmsa greiðslumáta, t.d. kreditkort frá ólíkum útgefendum, og bankinn þinn sýnir þá í aðskildum línum.
3. Velja **Handvirk jöfnun** aðgerð.

    Letur valinnar bankayfirlitslínu og valinna bankareikningsfærslna verður grænt og gátreiturinn **Jafnað** á hægra svæðinu er valinn.
4. Endurtakið skref 1 til 3 fyrir allar línur bankayfirlits sem eru ekki jafnar.

> [!TIP]
> Til að fjarlægja jöfnun skal velja bankareikningslínu og velja svo aðgerðina **fjarlægja jöfnun**. Ef margar bankayfirlitslínur hafa verið jafnaðar við fjárhagsfærslu og þú þarft að fjarlægja eina eða fleiri jafnaðar línur, eru allar handvirkar jafnanir fjarlægðar fyrir fjárhagsfærsluna þegar þú velur **Fjarlægja jöfnun**.

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines"></a>Til að stofna færslur sem vantar til að stemma af línur bankayfirlits

Stundum inniheldur bankayfirlit upphæðir fyrir vexti eða þóknanir. Slíkar bankayfirlitslínur geta ekki verið misjafnar því það eru ekki tengdar færslur í [!INCLUDE[prod_short](includes/prod_short.md)]. Þú verður þá að bóka færslubókarlínu fyrir hverja færslu til að stofna tilsvarandi fjárhagsfærslu sem það má jafna við.

1. Á síðunni **Afstemming bankareiknings** er valið aðgerðin **Flytja í almenna færslubók**.  
2. Á síðunni **Flytja bankaafstemmingu í almenna færslubók** skal tilgreina hvaða almenn færslubók skal nota, og veldu svo **OK** hnappinn.

    Síðan **almenn færslubók** opnast og inniheldur nýjar færslubókarlínur fyrir allar bankayfirlitslínur með fjárhagsfærslur sem vantar.
3. Kláraðu færslubókarlína með viðeigandi upplýsingar, eins og mótreikningur. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).  
4. Til að yfirfara niðurstöður bókunar áður en þú bókar skaltu velja aðgerina **Prófunarskýrsla**. Skýrslan **Bankareikningsyfirlit** opnast og sýnir sömu reitina og í hausnum á síðunni **Afstemming bankareiknings**.
5. Valið er **Bóka** aðgerðin.

    Eftir að færslan hefur verið bókuð skal stemma af yfirlitslínu bankayfirlits við hana.
6. Uppfærðu eða opnaðu aftur **afstemming bankareiknings** síðuna. Nýji fjárhagsfærslan birtist í **bankareikningsfærslur** svæðinu.
7. Jafnaðu bankayfirlitslínu með bankareikningsfærslu, annað hvort handvirkt eða sjálfkrafa.

## <a name="find-outstanding-transactions-previous-periods"></a>Finna útistandandi færslur fyrri tímabila
Hægt er að nota Bankayfirlitskýrsluna til að finna útistandandi færslur á fyrri tímabilum. Útistandandi færslur opnuðu fyrir uppgjörsdegi og hafa ekki verið lokaðar eða verið lokaðar eftir að Afstemming bankaafstemmingar var bókuð.

Þegar Bankayfirlitsyfirlit er keyrð af listasíðu bankayfirlits er hægt að kveikja á útistandandi færslum og í skýrslunni er kafli sem skráir útistandandi færslur.

**Dæmis** við bankareikningsfærslur A, B og C í bankareikningi okkar um mánaðamótin ágúst. Þegar við temjum bankareikning okkar fyrir ágúst finnum við bankayfirlitslínu sem samsvarar færslu A, en engin fyrir B og C. Þannig að við bókum afstemminguna við færslu með afstemmingu og B og C sem útistandandi færslur.

Í September er tekið við greiðslu fyrir færslu B og ákveðið að stemma af bankareikning okkar. Ef við keyrum skýrsluna bankayfirlit áður en afstemmingin er bókuð, munum við hafa eina Afstemmda færslu og eina útistandandi.

Ef við prentum skýrsluna fyrir ágúst munum við hafa útistandandi færslur fyrir B-og C-færslurnar okkar, jafnvel þó að við lokuðum færslu B í September.

## <a name="undo-a-bank-account-reconciliation"></a>Hætta við afstemmingu bankareiknings
Ef mistök finnast í bókaðri bankaafstemmingu er hægt að nota **aðgerðina ógilda** aðgerð á **Bankareikn. yfirlitssíðu** til að leiðrétta hana. Þegar bókuð bankaafstemming er afturkölluð, eru færslurnar færðar á Bankaafstemmingarsíðuna **og merktar sem opnar**, sem **þýðir að** þær eru ekki stemmdar af. Þá er hægt að leiðrétta bankaafstemminguna og bóka hana aftur.

> [!NOTE]
> Í norður-amerísku útgáfunni, til að nota afturköllunaraðgerðina fyrir bókaðar bankaafstemmingar og bankayfirlit, þarf að kveikja á **Bankaafstemming með sjálfvirkri samsvörun** á síðunni **Uppsetning fjárhagsgrunns**. Afturköllunaraðgerðin er ekki í boði fyrir bankayfirlit sem bókuð eru í vinnublöðum bankaafstemmingar.

### <a name="reusing-the-bank-statement-number"></a>Bankayfirlitsnúmer notað aftur
Bankayfirlitsnúmerið sem er notað fyrir nýja bankaafstemmingu er fengið frá bankareikningnum sem er staða síðasta yfirlits. Hægt er að breyta þessum gildum áður en ný bankaafstemming er gerð. Hinsvegar, þegar ný bankaafstemming er stofnuð, athugar [!INCLUDE[d365fin](includes/d365fin_md.md)] hvort númer yfirlitsins sé þegar úthlutað á bókað bankayfirlit. Ef númerið er í notkun, en ætlunin er að nýja bankayfirlitið noti það í staðinn, er hægt að nota **Breyta yfirlitsnr.** aðgerðina á síðunni **Afstemming bankareiknings**.

### <a name="examples"></a>Dæmi
Eftirfarandi dæmi sýna hvernig á að lagfæra mistök á bókaðri bankaafstemmingu, með eða án þess að nota sama yfirlitsnúmer.

#### <a name="example-1"></a>Dæmi 1
Bankaafstemmingar voru fyrir janúar, febrúar og mars. Númer bankayfirlits var 100 fyrir mars. Seinna uppgötvast að mars innihélt aðeins færslur til 30. mars, sem þýðir að það vantar færslur frá 31. Þar af leiðandi þarf að endurgera bankaafstemminguna fyrir mars. Í slíku tilfelli opnum við síðuna **Bankareikningsyfirlit**, veljum yfirlitið fyrir mars og veljum síðan **Afturkalla**. 

Nýju bankaafstemmingunni er gefið yfirlitsnúmerið 101. Til að endurúthluta númerinu 100 skal velja **Breyta yfirlitsnr.** og færið inn **100**. 

> [!TIP]
> Munið að stilla viðeigandi lokadagsetningu yfirlits (í þessu dæmi er það 31. mars) og breytið reitnum **Staða síðasta yfirlits**. 

#### <a name="example-2"></a>Dæmi 2
Bankaafstemmingar voru fyrir janúar, febrúar, júní og júlí. Þú sérð að febrúar var rangur. Gerum ráð fyrir að þar hafi verið yfirlitsnúmerið 100. Eins og dæmi 1 er notað afturkalla-og Breytingaryfirlýsingu nr. til að breyta yfirlitsnúmerinu eins og í dæmi #1 hér fyrir ofan og nú er hægt að endurgera bankaafstemmingu í febrúar.  

Eftir að leiðrétt bankaafstemming var bókuð fyrir febrúar á samsvarandi Bankareikningur spjald **síðasta yfirlits nr.** sýna **100** og reiturinn **Staða síðasta yfirlits** mun sýna lokastöðuna fyrir yfirlitið í febrúar. 

Ef næst er gerð bankaafstemming fyrir mars mun [!INCLUDE[d365fin](includes/d365fin_md.md)] úthluta 101 sem yfirlitsnúmeri og gefa því rétta **Stöðu síðasta yfirlits**.

Ef næst er gerð bankaafstemming fyrir ágúst skal íhuga að breyta gildunum í reitunum **Síðasta yfirlitsnr.** Og **Staða í síðustu uppgjörssvæði** á **spjaldi bankareiknings** áður en næsta bankaafstemmingar er stofnað, eða Notið **breytingaryfirlitið nr.** Aðgerð og breyta einnig gildinu í **reitnum Staða í Síðasta uppgjöri** á afstemmingarsíðu banka.

> [!NOTE]
> Yfirlitsnúmerið er mikilvægt þegar bankaafstemmingar eru gerðar með innfluttum CAMT-skrám sem innihalda yfirlitsnúmer, eða þegar afstemming er gerð samkvæmt prentuðum bankayfirlitum. Ef safn af bankafærslum er einfaldlega sótt af netbankanum er yfirlitsnúmerið yfirleitt ekki mikilvægt.  
>
> Staða síðasta yfirlits er geymt á bankareikningnum til að draga úr mistökum þegar bankaafstemmingar eru gerðar, en einnig er hægt að breyta því, sem gerir kleift að gera bankaafstemmingarnar í hvaða röð sem er. Þetta þýðir einnig að ef bankayfirlit er afturkallað gæti verið að nýja lokastaðan verði ekki staða síðasta yfirlits á bankayfirlitinu. Enginn eiginleiki er til staðar sem gerir kleift að áframsenda öll síðari bankayfirlit, því skal hafa það í huga þegar Afturköllun er gerð.  

## <a name="avoid-direct-posting"></a>Forðast beina bókun

Ekki skal nota fjárhagsreikning sem leyfir beina bókun í bókunarflokk bankareiknings. Með beinni bókun hvílir tengingin á milli bankareiknings færslu og fjárhagsfærslu fjárhagsreikningsins. Þegar bankareikninginn er stemmd af eru færslurnar sem bókaðar eru beint á fjárhagsreikninginn ekki teknar með og það verður erfitt að ljúka afstemmingunni.

Þessi mistök gerast oft þegar fært er inn Opnunarstaða bankareiknings. Mikilvægt er að ekki sé bókað opnunarstöðuna beint í fjárhag. Færslur í fjárhagsreikningnum sem bókaðar eru beint í fjárhagsreikninginn valda vandræðum. Þessar færslur gætu til dæmis komið í veg fyrir að þú stemir við bankareikninginn þinn. Fyrir bankareikninga í erlendum gjaldmiðli geta færslurnar valdið mismun sem á að safnast eftir að búið er að bóka frekari bankaafstemmingar vegna gengisleiðréttingar gjaldmiðla. Oft er opnunarbankainnistaða bókuð beint á bankareikning og upphæðin endar síðan í fjárhagsreikningnum. Einnig er hægt að bakfæra hana síðar á móti fjárhagsreikningnum sem er notaður til að jafna opnunarfjárhagsstöðu. Í báðum tilvikum verður að jafna beina bókun við fjárhagsreikninginn áður en fyrsta bankaafstemming hefst, og sérstaklega svo ef bankareikninginn er í erlendum gjaldmiðli.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig
[Afstemming bankareikninga](bank-manage-bank-accounts.md)  
[Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Reglur settar upp fyrir sjálfvirka jöfnun á greiðslum](receivables-how-set-up-payment-application-rules.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
