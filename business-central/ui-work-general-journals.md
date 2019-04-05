---
title: Nota færslubækur til að bóka beint í fjárhag| Microsoft Docs
description: Kynntu þér hvernig skal nota færslubækur til að bóka fjárhagsfærslur í fjárhagsreikninga og aðra reikninga, eins og banka- og lánardrottnareikninga.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: ddcda93c59df3f8390dc3852595d4f07f03648f5
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800243"
---
# <a name="working-with-general-journals"></a>Vinna í færslubókum

Flestar fjárhagsfærslur eru bókaðar í fjárhag gegnum sérstök viðskiptaskjöl, eins og innkaupareikninga og sölupantanir. Einnig er hægt að vinna úr viðskiptaaðgerðum, svo sem kaupum, greiðslum eða endurgreiðslum vegna útgjalda starfsmanna með því að bóka færslubókarlínur í ýmsum færslubókum í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Flestar færslubækur eru byggðar á *Almennri færslubók* og þú getur unnið úr öllum færslum á síðunni **Almenn færslubók**. Frekari upplýsingar, sjá [Bóka færslu beint yfir í Fjárhag](finance-how-post-transactions-directly.md).  

Þú getur til dæmis notað bókun greiðslna útgjalda starfsmanna í viðskiptaerindum fyrir endurgreiðslu síðar meir. Nánari upplýsingar eru í [Skrá og endurgreiða starfsmannaútgjöld](finance-how-record-reimburse-employee-expenses.md).

Í ýmsum tilvikum munt þú vilja nota færslubækurnar sem eru sérsniðar fyrir sérstakar tegundir af færslum, svo sem **Greiðslubók** til að skrá greiðslur. Frekari upplýsingar er að finna í [Skrá greiðslur og endurgreiðslur í greiðslubókina](payables-how-post-payments-refunds.md).  

Nota færslubækur til bóka fjárhagsfærslur beint í fjárhagsreikninga og aðra reikninga, svo sem banka-, viðskiptamanna-, lánardrottna- og starfsmannareikninga. Bókun með almennri færslubók stofnar alltaf færslur á fjárhagsreikningum. Slíkt á við jafnvel í tilvikum þegar færslubókarlína er bókuð á reikning viðskiptamanns, vegna þess að færsla er bókuð í safnreikning færslubókar með bókunarflokki.

Upplýsingarnar sem eru færðar inn í færslubók eru til bráðabirgða og það er hægt að breyta þeim í færslubókinni. Þegar færslubókin er bókuð, eru upplýsingarnar færðar í færslur á einstökum reikningum, þar sem ekki er hægt að breyta þeim. Það er samt sem áður hægt að ógilda bókaðar færslur og snúa við bókunum eða leiðrétta bókanir. Frekari upplýsingar eru í [Bakfæra bókanir](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="using-journal-templates-and-batches"></a>Nota sniðmát færslubóka og keyrslur

Til eru nokkur færslubókarsniðmát. Hvert sniðmát færslubókar er með sérstaka síðu með ákveðnum aðgerðum og reitum sem verða að styðja aðgerðirnar, eins og síðan **greiðsluafstemmingarbók** til að vinna bankagreiðslur og síðan **greiðslubók** til að borga lánardrottnum þínum eða endurgreiða starfsmönnum. Frekari upplýsingar er að finna í [Framkvæma greiðslur](payables-make-payments.md) og [Afstemma greiðslur viðskiptamanns við inngreiðslubók eða úr færslum í viðskiptamannabók](receivables-how-apply-sales-transactions-manually.md).

Fyrir hvert sniðmát færslubókar, geturðu sett upp þína eigin færslbók sem bókarkeyrsla. Til dæmis er hægt að skilgreina eigin færslubókarkeyrslu fyrir greiðslubók sem er með þitt persónulega útlit og stillingar. Eftirfarandi ábending er dæmi um hvernig skal sérsníða færslubók.

> [!TIP]  
> Ef valinn er gátreiturinn **Leggja til afstemmingarupphæð** á línunni fyrir keyrsla á síðunni **Færslubókakeyrslur**, þá er **Upphæð** reiturinn í, t.d. færslubókarlínum fyrir sama skjalanúmer sjálfkrafa forfyllt með sama gildi sem þarf til að stemma fylgiskjalið. Nánari upplýsingar er að finna í [Leyfa [!INCLUDE[d365fin](includes/d365fin_md.md)] að stinga upp á gildum](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Að skilja aðalreikninga og mótreikninga
Ef stofnaðir voru sjálfgefnir mótreikningar fyrir bókakeyrslur á síðunni **Færslubækur**, eru mótreikningarnir fylltir út sjálfkrafa þegar fyllt er í reitinn **Reikningur nr** Að öðrum kosti er fyllt í reitinn **Reikningur nr.** og reitinn **Mótreikningur nr.** handvirkt. Jákvæð upphæð í reitnum **Upphæð** er tekin út af aðalreikningnum og lögð inn á mótreikninginn. Neikvæð upphæð er lögð inn á aðalreikninginn og tekin út af mótreikningnum.

> [!NOTE]  
>   VSK er reiknaður út á aðskilin hátt fyrir aðalreikninginn og mótreikninginn, þannig að þar er hægt að nota mismunandi VSK prósentuhlutfall.

## <a name="working-with-recurring-journals"></a>Vinna með Ítrekunarbækur
Ítrekunarbók er færslubók með sérstökum reitum til að stjórna færslum sem eru bókaðar reglulega með litlum eða engum breytingum, t.d. leigu, áskriftum, rafmagni og hita. Með því að nota þessa reiti fyrir endurteknar færslur er hægt að bóka bæði fastar og breytilegar upphæðir. Einnig er hægt að tilgreina sjálfvirkar bakfærslur daginn eftir bókunardagsetningu. Einnig er hægt að nota úthlutunarlykla til að skipta ítrekunarfærslum niður á ýmsa reikninga. Nánari upplýsingar eru í [Úthluta upphæðum ítrekunarbókar á nokkra reikninga](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).

Með ítrekunarbók þarf aðeins einu sinni að setja inn færslur sem bókaðar verða reglulega. Það þýðir að reikningar, víddir og víddargildi o.s.frv sem fært er inn verður áfram í færslubókinni að lokinni bókun. Óhjákvæmilegar leiðréttingar má gera við hverja bókun.

### <a name="recurring-method-field"></a>Reitur ítrekunarmáta
Reiturinn ákvarðar hvernig upphæðin í færslubókarlínunni er meðhöndluð eftir bókun. Ef til dæmis á að nota sömu upphæðina í hvert sinn sem bókað er í línuna er hægt að láta upphæðina standa. Ef óskað er eftir að nota sömu reikninga og texta í línunni en breyta upphæðinni í hvert sinn sem er bókað er hægt að velja að eyða upphæðinni eftir bókun.

| Til | Sjá |
| --- | --- |
|Fast|Magnið í bókarlínunni er látið standa eftir bókun.|
|Breytilegt|Magninu í bókarlínunni er eytt eftir bókun.|
|Staða|Bókaða upphæðin á reikningnum í línunni deilist á reikningana sem eru tilgreindir fyrir línuna í töflunni Færslubók úthlutunar . Reikningsstaðan verður stillt á núll. Nauðsynlegt er að fylla út reitinn **Úthlutunar %** á síðunni **Úthlutanir**. Nánari upplýsingar eru í [Úthluta upphæðum ítrekunarbókar á nokkra reikninga](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).|
|Föst bakfærsla|Upphæðin í færslubókarlínunni helst eftir bókun og mótfærsla bókast næsta dag.|
|Breytileg bakfærsla|Upphæðinni í færslubókarlínunni er eytt eftir bókun og mótfærsla bókast næsta dag.|
|Bakfærð staða|Bókaða upphæðin á reikningnum í línunni verður úthlutað á reikningana sem eru tilgreindir fyrir línuna á síðunni **Úthlutanir**. Staðan á reikningnum verður sett á núll og mótfærsla bókast næsta dag.|

> [!NOTE]  
>  Hægt er að fylla út VSK-reitina annaðhvort í ítrekunarbókarlínu eða úthlutunarbókarlínu en ekki í báðum. Það ma sem sagt einungis fylla þá út á síðunni **Úthlutanir** ef samsvarandi línur í ítrekunarbókinni hafa ekki verið fylltar út.

### <a name="recurring-frequency-field"></a>Reitur ítrekunartíðni
Reiturinn ákvarðar hversu oft skuli bóka færsluna í bókarlínunni. Þetta er reitur með dagsetningarreiknireglu og það verður að fylla hann út fyrir ítrekunarbókarlínur. Frekari upplýsingar er að finna í [Að nota dagsetningarreiknireglur](ui-enter-date-ranges.md#using-date-formulas).

#### <a name="examples"></a>Dæmi
Ef þarf að bóka færslubókarlínuna í hverjum mánuði skal færa inn „1M“. Eftir hverja bókun er dagsetningin í reitnum **Bókunardags.** uppfærð í sama mánaðardag næsta mánaðar.

Ef bóka á færslu á síðasta degi hvers mánaðar má gera eitt af þessu:

- Bóka fyrstu færslu á síðasta degi mánaðar með því að færa inn 1D+1M+1D (1 dagur + 1 mánuður + 1 dagur). Með þessari reiknireglu er bókunardagsetningin reiknuð rétt án tillits til þess hve margir dagar eru í mánuðinum.

- Bóka fyrstu færslu á hvaða mánaðardegi sem vera skal með því að færa inn 1M+CM. Með þessari reiknireglu verður bókunardagsetningin eftir einn heilan mánuð + dagana sem eftir eru í líðandi mánuði.

### <a name="expiration-date-field"></a>Reitur lokadagsetningar
Reiturinn ákvarðar dagsetninguna þegar línan verður bókuð í síðasta sinn. Ekki er hægt að bóka línuna eftir þessa dagsetningu.

Kosturinn við notkun þessa reits er sá að línunni verður ekki eytt úr bókinni tafarlaust og alltaf má setja nýja dagsetningu í stað þeirrar sem er að renna út, þannig að línan verði nothæf til frambúðar.

Ef reiturinn er auður er línan bókuð í hvert sinn sem bókað er þar til henni er eytt úr færslubókinni.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Úthlutun upphæða á ítrekunarfærslum á nokkra reikninga
Á síðunni **Ítrekunarfærslubók** er hægt að velja aðgerðina **Úthlutanir** til að sjá eða stjórna hvernig upphæðum á ítrekunarbókarlínu er úthlutað á nokkra reikninga og víddir. Athugið að úthlutunin virkar sem móttreikningslína gagnvart ítrekunarbókarlínu.

Eins og í ítrekunarbók þarf aðeins að færa úthlutun inn einu sinni. Úthlutun verður eftir í úthlutunarbók að lokinni bókun þannig að ekki þarf að færa inn upphæðir og úthlutanir í hvert skipti sem ítrekunarbókarlína er bókuð.

Ef reiturinn ítrekunarmáti í ítrekunarbók er stilltur á **Staða** eða **Bakfærð staða** er ekki hirt um víddargildiskóða í ítrekunarbók þar sem reikningur stendur á núlli. Þannig verður aðeins ein bakfærsla stofnuð ef mismunandi víddargildum er úthlutað ítrekunarlínu á síðunni **Úthlutanir**. Því má ekki færa inn sama kóða á síðunni **Úthlutanir** ef ítrekunarbókarlínu með víddargildiskóða er úthlutað. Ef það er gert verða víddargildin röng.

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Dæmi: Úthlutun á leigugreiðslum til mismunandi deilda
Leiga er greidd í hverjum mánuði þannig að leiguupphæð hefur verið færð inn á sjóðsreikning í ítrekunarbókarlínu. Á síðunni **Úthlutanir** er hægt að skipta kostnaðinum á milli deilda (deildarvídd) í samræmi við fermetrafjölda sem hver og ein hefur til umráða. Útreikningurinn byggist á úthlutunarprósentu fyrir hverja línu. Færa má nokkra reikninga í mismunandi úthlutunarlínum (ef leigunni er jafnframt skipt niður á nokkra reikninga), eða færa á sama reikning, með mismunandi víddargildiskóðum fyrir víddina Deild í hverri línu.

## <a name="working-with-standard-journals"></a>Vinna með Staðlaðar færslubækur
Þegar bókarlínur sem líklegt er að verði stofnaðar aftur hafa verið stofnaðar er hægt að vista þær sem staðlaða færslubók áður en bókin er bókuð. Þessi virkni gildir um birgðabækur og almennar færslubækur.

> [!NOTE]  
>   Eftirfarandi ferli vísar í birgðabókina en upplýsingarnar á einnig við um almennu færslubókina.

### <a name="to-save-a-standard-journal"></a>Að vista sem staðlaða færslubók
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðabækur** og veldu síðan tengda tengilinn.
2. Kóti er færður inn í eina eða fleiri færslubókarlínur.
3. Velja skal bókarlínurnar sem á að nota aftur.
4. Velja skal **Vista sem staðlaða færslubók** aðgerðina.
5. Á beiðnisíðunni **Vista sem staðlaða birgðabók** þarf að skilgreina nýja eða eldri staðlaða birgðabók til að vista línurnar í.

    Ef ein eða fleiri staðlaðar birgðabækur hafa verið stofnaðar og skipta á einni þeirra út með nýjum vörubókalínum skal velja kótann sem óskað er eftir í reitnum Kóti.
6. Veldu hnappinn **Í lagi** til að staðfesta að skrifa eigi yfir stöðluðu birgðabókina sem til er og skipta út öllu efni hennar.
7. Velja skal reitinn **Vista ein.upphæð** ef vista á gildin í reitnum **Ein.upphæð** í staðlaðri birgðabók.
8. Velja skal reitinn **Vista magn** ef kerfið á að vista gildin í reitnum **Magn**.
9. Velja hnappinn **Í lagi** til að vista stöðluðu birgðabókina.

Þegar lokið hefur verið við að vista staðlaða birgðabókina opnast síðan Birgðabók þannig að hægt er að halda áfram og bóka hana, vitandi það að auðvelt er að stofna hana aftur næst þegar bóka þarf sömu eða svipaðar línur.

### <a name="to-reuse-a-standard-journal"></a>Að endurnýta staðlaða færslubók
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðabækur** og veldu síðan tengda tengilinn.
2. Valin er **Ná í staðlaðar færslubækur** aðgerðin.

    Síðan Staðlaðar birgðabækur opnast með kótum og lýsingum á öllum stöðluðum birgðabókum sem til eru.
3. Ef skoða á staðlaða birgðabók áður en hún er valin til endurnotkunar, skal velja aðgerðina **Sýna færslubók**.

    Allar breytingar sem gerðar eru á staðlaðri birgðabók verða virkar um leið. Þær verða til staðar næst þegar staðlaða birgðabókin sem um ræðir er opnuð eða endurnýtt. Þess vegna skal ganga úr skugga um hvort breytingin sé nógu mikilvæg til að beita henni almennt. Annars skal gera sértækar breytingar í birgðabókinni eftir að stöðluðu birgðabókarlínurnar hafa verið settar inn. Sjá þrep 4 hér að neðan.
4. Á síðunni **Staðlaðar birgðabækur** er staðlaða birgðabókarinnar sem nota á aftur valin og smellt á hnappinn **Í lagi**.

    Nú hafa línurnar sem vistaðar voru sem stöðluð birgðabók verið færðar inn í birgðabókina. Ef færslubókarlínur eru þegar til í birgðabókinni koma línurnar sem settar voru inn á eftir þeim sem fyrir eru.

    Ef ekki var merkt við reitinn **Vista ein.upphæð** í keyrslunni **Vista sem staðlaða birgðabók** er reiturinn **Ein.upphæð** í línum sem settar eru inn úr stöðluðu birgðabókinni sjálfkrafa fylltur út með gildandi virði vörunnar, afrituðu úr reitnum **Ein.kostnaður** á birgðaspjaldinu.

    > [!NOTE]  
    >   Ef merkt var við reitina **Vista ein.upphæð** eða **Vista magn** skal nú ganga úr skugga um að gildin sem færð voru inn séu rétt fyrir þessa tilteknu birgðaleiðréttingu áður en birgðabókin er bókuð.

    Ef birgðabókarlínurnar sem settar eru inn innihalda vistaðar einingaupphæðir sem ekki á að bóka er fljótlegt að breyta þeim í gildandi virði vörunnar eins og hér er lýst.

6. Velja skal birgðabókarlínur sem á að leiðrétta, og svo velja **Endurreikna einingaupphæð** aðgerðina. Það uppfærir reitinn Ein.upphæð með gildandi kostnaðarverði vörunnar.
7. Valið er **Bóka** aðgerðin.

## <a name="to-renumber-document-numbers-in-journals"></a>Endurraða númerum fylgiskjals í færslubókum
Til að ganga úr skugga um að þú fáir ekki bókunarvillur vegna fylgiskjalsnúmers pöntunar, geturðu notað aðgerðina **Endurraða númerum fylgiskjals** áður en þú bókar færslubókina.

Í öllum færslubókum sem byggja á almennri færslubók er hægt að breyta reitnum **Skjal nr** þannig að hægt sé að tilgreina mismunandi númer fylgiskjala fyrir mismunandi færslubókarlínur eða sama númer fylgiskjals fyrir tengdar færslubókarlínur.

Ef **Númeraraðir** reiturinn á bókarkeyrslunni er fylltur út krefst bókunargerðin í færslubókunum þess að númer fylgiskjala á stakri eða nokkrum færslubókarlínum séu í réttri röð. Til að ganga úr skugga um að þú fáir ekki bókunarvillur vegna fylgiskjalsnúmers pöntunar, geturðu notað aðgerðina **Endurraða númerum fylgiskjals** áður en þú bókar færslubókina. Ef tengdar færslubókarlínur voru teknar saman eftir númerum fylgiskjala áður en aðgerðin var notuð eru þær áfram teknar saman en gæti verið úthlutað á annað skjalanúmer.

Þessi aðgerð virkar einnig á afmörkuðum yfirlitum.

Sér hver endurnúmerun skjalanúmera mun taka tillit til tengdra jafnana, s.s. greiðslujafnana sem hafa verið framkvæmdar úr skjalinu á færslubókarlínunni á lánardrottnalykli. Að sama skapi geta reitirnir **Kenni jöfnunar** og **Nr. jöfnunarskjals** í færslubókunum sem um ræðir verið uppfærðir.

Eftirfarandi ferli byggist á glugganum **Færslubók**, en á við um allar aðrar bækur sem eru byggðar á færslubókum, eins og síðunni **Greiðslubók**.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Færslubækur** og veldu síðan tengda tengilinn.
2. Þegar þú ert tilbúinn að bóka færslubókina, skal velja **Endurraða númerum skjals** aðgerðina.

Gildi í **Skjal nr.** reitnum breytast þar sem þörf er á, þannig að númer fylgiskjala á stakri eða nokkrum færslubókarlínum eru í réttri röð. Hægt er að birta færslubókin eftir endurnúmerun skjala.

## <a name="see-also"></a>Sjá einnig
[Bóka færslu beint í Fjárhag](finance-how-post-transactions-directly.md)  
[Bakfæra bókanir](finance-how-reverse-journal-posting.md)  
[Úthluta kostnaði og tekjum](year-allocate-costs-income.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
