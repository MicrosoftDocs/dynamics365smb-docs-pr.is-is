---
title: Afstemma bankareikninga | Microsoft Docs
description: Lýsir því hvernig birgðavirði er stemmt af við fjárhaginn.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 08b7f6c092267b965af491cd80144950db138c3d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388700"
---
# <a name="reconcile-bank-accounts"></a>Afstemma bankareikninga

Bankaafstemming er framkvæmd til að ganga úr skugga um að ýmsar viðskiptafærslur og útgjöld endurspeglist rétt í bókum fyrirtækisins. Þetta er gert með því að bera saman og jafna færslur á innri bankareikningum við bankafærslur í bankanum þínum og síðan bóka stöðurnar á innri bankareikningana svo að samtölur verði í boði fyrir fjármálastjóra. Bankaafstemming er einnig hagkvæm leið til að uppgötva og leysa úr greiðslum sem vantar upp á og bókhaldsvillum.

Eftirfarandi lýsir því hvernig á að framkvæma bankaafstemmingu með síðunni **Afstemming bankareiknings**.

> [!TIP]
> Einnig er hægt að stemma af bankareikninga á síðunni **greiðsluafstemmingarbók** þegar greiðsla er meðhöndluð. Allar opnar fjárhagsfærslur bankareiknings sem tengjast jöfnuðum fjárhagsfærslum viðskiptavinar eða lánardrottins verða lokaðar þegar þú velur **Bóka Greiðslur og stemma Af Bankareikninga** aðgerð. Þetta stemmir af bankareikninginn sjálfkrafa fyrir greiðslunum sem bókaðar eru með færslubókinni. Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> Í norður-amerískum útgáfum getur þú einnig unnið þetta á síðunni **Vinnublað bankaafstemmingar** sem hentar betur fyrir ávísanir og innborganir en býður ekki upp á innflutning á bankayfirlitsskrám. Til að nota þennan glugga í staðinn fyrir gluggann **Afstemming bankareikninga** skaltu afvelja reitinn **Bankareikn.afstemming með sjálfvirkri jöfnun** á síðunni **Fjárhagsgrunnur**. Frekari upplýsingar er hægt að finna í [Afstemma bankareikninga](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) sem heyrir undir staðbundnar aðgerðir Bandaríkjanna.

Línur síðunnar **Afstemming bankareiknings** skiptast í tvö svæði. **BankaYfirlitslínur** svæðinu sýnir annað hvort innfluttra bankafærslur eða fjárhagsfærslur með útistandandi greiðslur. **Bankareikningsfærslur** svæðið sýnir fjárhagsfærslur á innri bankareikning.

Afstemming bankafærsla við innri bankafærslur er kölluð *samsvörun*. Hægt er að velja að framkvæma samsvörun sjálfkrafa með því að nota aðgerðina **Sjálfvirk jöfnun**. Einnig er hægt að velja línur handvirkt í báðum gluggum til að tengja hverja bankareikningslínu við eina eða fleiri tengdar bankareikningsfærslur og nota síðan aðgerðina **Handvirk jöfnun**. **Jafnað** gátreitur er valinn í línum þar sem færslurnar eru samsvarandi. Frekari upplýsingar eru í [Setja upp reglur fyrir sjálfvirka jöfnun á greiðslum](receivables-how-set-up-payment-application-rules.md).

> [!NOTE]  
> Ef bankayfirlitslínur tengjast tékkafærslum er ekki hægt að nota samsvörunaraðgerðirnar. Í staðinn þarf að velja aðgerðina **Jafna færslur** og velja síðan viðkomandi tékkafrærslu til að jafna bankayfirlitslínuna með.

Þegar gildið í **heildarstaða** reitnum á **Bankauppgjörslínur** svæðinu jafngildir gildið í **Staða til afstemmingar** í á **Bankareikningsfærslur** svæðinu, er hægt að velja **Bóka** aðgerðina. Allar færslur ójafnaðar bankareiknings verða áfram á síðunni, sem gefur til kynna einhver misræmi sem þú ættir að leysa til að stemma bankareikninginn af.

Allar línur sem ekki er hægt að jafna, gefið til kynna með gildi í reitnum **Mismunur**, verða áfram á síðunni **Afstemming bankareiknings** eftir bókun. Þær tákna einhverskonar misræmi sem nauðsynlegt er að leysa úr áður en hægt er að ljúka afstemmingu bankareiknings. Dæmigerðar aðstæður fyrirtækis sem gætu valdið mismun:

|Mismunur|Ástæða|Upplausn|
|-|-|
|Færsla á innri bankareikningi er ekki á bankayfirlitinu.|Bankafærslan kom ekki upp þrátt fyrir að bókun væri gerð í [!INCLUDE[prod_short](includes/prod_short.md)].|Klárið peningafærsluna sem vantar (eða biðjið skuldunaut um að klára færsluna) og flytjið síðan aftur inn bankayfirlitsskrána eða færið færsluna inn handvirkt.|
|Færsla á bankayfirliti er ekki til sem fylgiskjal eða færslubókarlína í [!INCLUDE[prod_short](includes/prod_short.md)].|Bankafærsla var gerð án samsvarandi bókunar í [!INCLUDE[prod_short](includes/prod_short.md)], til dæmis bókun færslubókarlínu fyrir kostnað.|Búið til og bókið færsluna sem vantar. Upplýsingar um fljótlega leið til að koma þessu í verk er að finna í [Að stofna fjárhagsfærslur sem vantar til að jafna bankafærslur við](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines-with).|
|Færsla á innri bankareikningi samsvarar bankafærslu en einhverjar upplýsingar eru of ólíkar til að gefa samsvörun.|Upplýsingar, t.d. upphæð eða nafn viðskiptavinar, voru færðar inn á annan hátt í tengslum við bankafærsluna eða innri bókun.|Yfirfara skal upplýsingarnar og síðan jafna færslurnar tvær. Einnig er rétt að leiðrétta misræmi í upplýsingum.||

Nauðsynlegt er að leysa úr muninum, til dæmis með því að stofna færslur sem vantar og leiðrétta upplýsingar sem samsvarast ekki, eða með því að klára peningafærslur sem vantar, þar til afstemmingu bankareiknings er lokið og hún bókuð.

Hægt er að fylla á **Bankayfirlitslínur** svæðið á síðunni **afstemming bankareiknings** á eftirfarandi hátt:

* Sjálfvirkt, með því að nota **Flytja inn bankayfirlit** aðgerðina til að fylla í svæðið **Bankayfirlitslínur** með bankafærslum samkvæmt innfluttri skrá eða streymi sem bankinn býður upp á.
* Handvirkt, með því að nota **Leggja til línur** aðgerðina til að fylla í svæðið **Bankayfirlitslínur** samkvæmt reikningum í [!INCLUDE[prod_short](includes/prod_short.md)] sem eru með útistandandi greiðslur.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Fylla inn í línur bankaafstemmingar með því að flytja inn bankayfirlit.

Svæðið **Bankayfirlitslínur** verður fylllt út með bankafærslum í samræmi við innflutta skrá eða streymi sem bankinn lætur í té.

Til að virkja innflutning bankayfirlits, verður þú að setja upp og virkja Envestnet Yodlee Bank Feed þjónustu og tengja síðan bankareikningana við viðkomandi netbankareikninga. Frekari upplýsingar eru í [Setja upp Envestnet Yodlee Bank Feeds þjónustuna](bank-how-setup-bank-statement-service.md).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Afstemming bankareiknings** og veldu síðan tengda tengilinn.
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
4. Veldu **hafa með tékka** gátreitinn til að leggja til tékkafærslur í stað samsvarandi bankareikningsfærslna.
5. Velja hnappinn **Í lagi**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>að jafna sjálfkrafa bankayfirlitslínur og bankareikningsfærslur

Síðan **Afstemming bankareiknings** býður upp á sjálfvirkar samsvörunaraðgerðir sem byggja á samsvörun texta í bankayfirlitslínu (vinstri rúðunni) við texta í einni eða fleiri fjárhagsfærslum bankareiknings (hægri rúðunni). Athugaðu að þú getur skrifað yfir ráðlagðar sjálfvirkar jafnanir og þú getur valið að nota ekki sjálfvirkar jafnanir yfirhöfuð. Frekari upplýsingar er að finna í [Að jafna handvirkt bankayfirlitslínur við bankareikningsfærslur](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

1. Á síðunni **Afstemming bankareiknings** er valið **jafna sjálfkrafa**. Síðan **Jafna bankafærslur** opnast.
2. Í reitnum **Vikmörk færsludagsetningar (dagar)** skal tilgreina þann fjölda daga fyrir og eftir bókunardagsetningu fjárhagsfærslu bankareiknings sem hafður er með í leitinni að samsvarandi færsludagsetningum á bankayfirlitinu.

    Ef 0 er slegið inn eða reiturinn hafður auður leitar aðgerðin **Sjálfvirk jöfnun** aðeins eftir samstæðum færsludagsetningum í bókunardagsetningu á bankareikningsfærslum.
3. Velja hnappinn **Í lagi**.

    Allar bankayfirlitslínur og bankareikningsfærslur sem hægt er að jafna verða grænar og gátreiturinn **Jafnað** er valinn.
4. Til að fjarlægja jöfnun skal velja bankareikningslínu og velja svo aðgerðina **fjarlægja jöfnun**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Að jafna handvirkt bankayfirlitslínur og bankareikningsfærslur

1. Á síðunni **Afstemming bankareiknings** skal velja tvær ójafnaðar línur í **Bankayfirlitslínur** svæðinu.
2. Á svæðinu **bankareikningsfærslur** skal velja eina eða fleiri bankareikningsfærslur sem hægt er að jafna við valda bankayfirlitslínu. Til að velja margar línur skal halda inni Ctrl-lyklinum.
3. Velja **Handvirk jöfnun** aðgerð.

    Letur valinnar bankayfirlitslínu og valinna bankareikningsfærslna verður grænt og gátreiturinn **Jafnað** á hægra svæðinu er valinn.
4. Endurtakið liði 1 til 3 fyrir allar bankayfirlitslínur sem ganga af.
5. Til að fjarlægja jöfnun skal velja bankareikningslínu og velja svo aðgerðina **fjarlægja jöfnun**.

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines-with"></a>Að stofna fjárhagsfærslur sem vantar til að jafna bankayfirlitslínur við

Stundum geta verið vextir eða kostnaður á bankayfirlitinu. Slíkar bankayfirlitslínur geta ekki verið jafnaðar vegna þess að engar tilsvarandi fjárhagsfærslur eru til í [!INCLUDE[prod_short](includes/prod_short.md)]. Þú verður þá að bóka færslubókarlínu fyrir hverja færslu til að stofna tilsvarandi fjárhagsfærslu sem það má jafna við.

1. Á síðunni **Afstemming bankareiknings** er valið aðgerðin **Flytja í almenna færslubók**.  
2. Á síðunni **Flytja bankaafstemmingu í almenna færslubók** skal tilgreina hvaða almenn færslubók skal nota, og veldu svo **OK** hnappinn.

    Síðan **almenn færslubók** opnast og inniheldur nýjar færslubókarlínur fyrir allar bankayfirlitslínur með fjárhagsfærslur sem vantar.
3. Kláraðu færslubókarlína með viðeigandi upplýsingar, eins og mótreikningur. Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).  
4. Til að yfirfara niðurstöður bókunar áður en þú bókar skaltu velja aðgerina **Prófunarskýrsla**. Skýrslan **Bankareikningsyfirlit** opnast og sýnir sömu reitina og í hausnum á síðunni **Afstemming bankareiknings**.
5. Valið er **Bóka** aðgerðin.

    Þegar færslan er bókuð skal halda áfram og jafna bankayfirlitslínu við hana.
6. Uppfærðu eða opnaðu aftur **afstemming bankareiknings** síðuna. Nýji fjárhagsfærslan birtist í **bankareikningsfærslur** svæðinu.
7. Jafnaðu bankayfirlitslínu með bankareikningsfærslu, annað hvort handvirkt eða sjálfkrafa.

## <a name="undo-a-bank-account-reconciliation"></a>Hætta við afstemmingu bankareiknings
Ef mistök voru gerð í bókaðri bankaafstemmingu er hægt að nota aðgerðina **Afturkalla** á síðunni **Bankareikningsyfirlit** til að leiðrétta mistökin. Þegar bókuð bankaafstemming er afturkölluð verða færslur færðar á síðuna **Bankaafstemming** og merktar sem **Opnar**, sem þýðir að þær eru ekki afstemmdar. Þá er hægt að leiðrétta bankaafstemminguna og bóka hana aftur.

> [!NOTE]
> Í norður-amerísku útgáfunni, til að nota afturköllunaraðgerðina fyrir bókaðar bankaafstemmingar og bankayfirlit, þarf að kveikja á **Bankaafstemming með sjálfvirkri samsvörun** á síðunni **Uppsetning fjárhagsgrunns**. Afturköllunaraðgerðin er ekki í boði fyrir bankayfirlit sem bókuð eru í vinnublöðum bankaafstemmingar.

### <a name="reusing-the-bank-statement-number"></a>Bankayfirlitsnúmer notað aftur
Bankayfirlitsnúmerið sem er notað fyrir nýja bankaafstemmingu er fengið frá bankareikningnum sem er staða síðasta yfirlits. Hægt er að breyta þessum gildum áður en ný bankaafstemming er gerð. Hinsvegar, þegar ný bankaafstemming er stofnuð, athugar [!INCLUDE[d365fin](includes/d365fin_md.md)] hvort númer yfirlitsins sé þegar úthlutað á bókað bankayfirlit. Ef númerið er í notkun, en ætlunin er að nýja bankayfirlitið noti það í staðinn, er hægt að nota **Breyta yfirlitsnr.** aðgerðina á síðunni **Afstemming bankareiknings**.

### <a name="examples"></a>Dæmi
Eftirfarandi eru nokkur dæmi um hvernig á að lagfæra mistök í bókaðri bankaafstemmingu með eða án þess að nota sama yfirlitsnúmer.

#### <a name="example-1"></a>Dæmi 1
Bankaafstemmingar voru fyrir janúar, febrúar og mars. Númer bankayfirlits var 100 fyrir mars. Seinna uppgötvast að mars innihélt aðeins færslur til 30. mars, sem þýðir að það vantar færslur frá 31. Þar af leiðandi þarf að endurgera bankaafstemminguna fyrir mars. Í slíku tilfelli opnum við síðuna **Bankareikningsyfirlit**, veljum yfirlitið fyrir mars og veljum síðan **Afturkalla**. 

Nýju bankaafstemmingunni er gefið yfirlitsnúmerið 101. Til að endurúthluta númerinu 100 skal velja **Breyta yfirlitsnr.** og færið inn **100**. 

> [!TIP]
> Munið að stilla viðeigandi lokadagsetningu yfirlits (í þessu dæmi er það 31. mars) og breytið reitnum **Staða síðasta yfirlits**. 

#### <a name="example-2"></a>Dæmi 2
Bankaafstemmingar voru fyrir janúar, febrúar, júní og júlí. Þú sérð að febrúar var rangur. Gerum ráð fyrir að þar hafi verið yfirlitsnúmerið 100. Eins og í dæmi 1 eru aðgerðirnar Afturkalla og Breyta yfirlitsnr. til að breyta yfirlitsnúmerinu eins og í dæmi #1 hér fyrir ofan og nú er hægt að endurgera bankaafstemmingu í febrúar.  

Þegar búið er að bóka leiðrétta bankaafstemmingu fyrir febrúar, mun á samsvarandi bankareikningsspjaldi reiturinn **Síðasta yfirlitsnr.** sýna **100** og reiturinn **Staða síðasta yfirlits** mun sýna lokastöðuna fyrir yfirlitið í febrúar. 

Ef næst er gerð bankaafstemming fyrir mars mun [!INCLUDE[d365fin](includes/d365fin_md.md)] úthluta 101 sem yfirlitsnúmeri og gefa því rétta **Stöðu síðasta yfirlits**.

Ef næst er gerð bankaafstemming fyrir ágúst skal íhuga að breyta gildunum í reitunum **Síðasta yfirlitsnr.** og **Staða síðasta yfirlits** á spjaldinu **Bankareikningur** áður en næsta bankaafstemming er stofnuð, eða nota aðgerðina Breyta yfirlitsnr. og einnig breyta gildinu í reitnum „Staða síðasta yfirlits“ á síðu bankaafstemmingar.

> [!NOTE]
> Yfirlitsnúmerið er mikilvægt þegar bankaafstemmingar eru gerðar með innfluttum CAMT-skrám sem innihalda yfirlitsnúmer, eða þegar afstemming er gerð samkvæmt prentuðum bankayfirlitum. Ef safn af bankafærslum er einfaldlega sótt af netbankanum er yfirlitsnúmerið yfirleitt ekki mikilvægt. 
>
>Staða síðasta yfirlits er geymt á bankareikningnum til að draga úr mistökum þegar bankaafstemmingar eru gerðar, en einnig er hægt að breyta því, sem gerir kleift að gera bankaafstemmingarnar í hvaða röð sem er. Þetta þýðir einnig að ef bankayfirlit er afturkallað gæti verið að nýja lokastaðan verði ekki staða síðasta yfirlits á bankayfirlitinu. Enginn eiginleiki er til staðar sem gerir kleift að áframsenda öll síðari bankayfirlit, því skal hafa það í huga þegar Afturköllun er gerð. 

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Afstemming bankareikninga](bank-manage-bank-accounts.md)  
[Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Reglur settar upp fyrir sjálfvirka jöfnun á greiðslum](receivables-how-set-up-payment-application-rules.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]