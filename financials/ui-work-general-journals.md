---
title: "Nota færslubækur til að bóka beint í fjárhag| Microsoft Docs"
description: "Kynntu þér hvernig skal nota færslubækur til að bóka fjárhagsfærslur í fjárhagsreikninga og aðra reikninga, eins og banka- og lánardrottnareikninga."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2aac957fc253f6c7d2f621ea2e5e039733081a19
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="working-with-general-journals"></a>Vinna í færslubókum
Flestar fjárhagsfærslur eru bókaðar í fjárhag gegnum sérstök viðskiptaskjöl, eins og innkaupareikninga og sölupantanir. Fyrir fyrirtækjaaðgerðir sem ekki eru táknaðar með fylgiskjölum í [!INCLUDE[d365fin](includes/d365fin_md.md)], eins og smærri útgjöld og inngreiðslur, er hægt að búa til færslur sem tengjast aðgerðunum með því að stofna færslubókarlínu í glugganum **Fjárhagur**. Frekari upplýsingar, sjá [Bóka færslu beint yfir í Fjárhag](finance-how-post-transactions-directly.md).

Þú getur til dæmis bókað greiðslur útgjalda starfsmanna í viðskiptaerindum fyrir endurgreiðslu síðar meir. Nánari upplýsingar eru í [Skrá og endurgreiða starfsmannaútgjöld](finance-how-record-reimburse-employee-expenses.md).

Nota færslubækur til bóka fjárhagsfærslur beint í fjárhagsreikninga og aðra reikninga, svo sem banka-, viðskiptamanna-, lánardrottna- og starfsmannareikninga. Bókun með almennri færslubók stofnar alltaf færslur á fjárhagsreikningum. Slíkt á við jafnvel í tilvikum þegar færslubókarlína er bókuð á reikning viðskiptamanns, vegna þess að færsla er bókuð í safnreikning færslubókar með bókunarflokki.

Upplýsingarnar sem eru færðar inn í færslubók eru til bráðabirgða og það er hægt að breyta þeim í færslubókinni. Þegar færslubókin er bókuð, eru upplýsingarnar færðar í færslur á einstökum reikningum, þar sem ekki er hægt að breyta þeim. Það er samt sem áður hægt að ógilda bókaðar færslur og snúa við bókunum eða leiðrétta bókanir. Frekari upplýsingar eru í [Bakfæra bókanir](finance-how-reverse-journal-posting.md).

## <a name="using-journal-templates-and-batches"></a>Nota sniðmát færslubóka og keyrslur
Til eru nokkur færslubókarsniðmát. Hvert sniðmát færslubókar er með sérstakan glugga með ákveðnum aðgerðum og reitum sem verða að styðja aðgerðirnar, eins og **greiðsluafstemmingarbók** glugginn til að vinna bankagreiðslur og **greiðslubók** glugginn til að borga lánardrottnum þínum eða endurgreiða starfsmönnum. Frekari upplýsingar, sjá [Framkvæma greiðslur](payables-make-payments.md) og [Afstemma greiðslur viðskiptamanns handvirkt](receivables-how-apply-sales-transactions-manually.md).

Fyrir hvert sniðmát færslubókar, geturðu sett upp þína eigin færslbók sem bókarkeyrsla. Til dæmis er hægt að skilgreina eigin færslubókarkeyrslu fyrir greiðslubók sem er með þitt persónulega útlit og stillingar. Eftirfarandi ábending er dæmi um hvernig skal sérsníða færslubók.

> [!TIP]  
> Ef valið er **Leggja til afstemmingarupphæð** gátreitinn á línunni fyrir keyrsla í á **færslubókakeyrslur** glugganum, þá er **Upphæð** reiturinní, t.d. færslubókarlínur fyrir sama skjalnúmer sjálfkrafa forfyllt út með sama gildi sem þarf til að stemma fylgiskjal. Nánari upplýsingar er að finna í [Leyfa [!INCLUDE[d365fin](includes/d365fin_md.md)] að stinga upp á gildum](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Að skilja aðalreikninga og mótreikninga
Ef stofnaðir voru sjálfgefnir mótreikningar fyrir bókakeyrslur á síðunni **Færslubækur**, eru mótreikningarnir fylltir út sjálfkrafa þegar fyllt er í reitinn **Reikningur nr** Að öðrum kosti er fyllt í reitinn **Reikningur nr.** og reitinn **Mótreikningur nr.** handvirkt. Jákvæð upphæð í reitnum **Upphæð** er tekin út af aðalreikningnum og lögð inn á mótreikninginn. Neikvæð upphæð er lögð inn á aðalreikninginn og tekin út af mótreikningnum.

> [!NOTE]  
>   VSK er reiknaður út á aðskilin hátt fyrir aðalreikninginn og mótreikninginn, þannig að þar er hægt að nota mismunandi VSK prósentuhlutfall.

## <a name="working-with-recurring-journals"></a>Vinna með Ítrekunarbækur
Ítrekunarbók er færslubók með sérstökum reitum til að stjórna færslum sem eru bókaðar reglulega með litlum eða engum breytingum. Með því að nota þessa reiti fyrir endurteknar færslur er hægt að bóka bæði fastar og breytilegar upphæðir. Einnig er hægt að tilgreina sjálfvirkar bakfærslur daginn eftir bókunardag og nota úthlutunarlykla fyrir ítrekunarfærslur.

## <a name="working-with-standard-journals"></a>Vinna með Staðlaðar færslubækur
Þegar bókarlínur sem líklegt er að verði stofnaðar aftur hafa verið stofnaðar er hægt að vista þær sem staðlaða færslubók áður en bókin er bókuð. Þessi virkni gildir um birgðabækur og almennar færslubækur.

> [!NOTE]  
>   Eftirfarandi ferli vísar í birgðabókina en upplýsingarnar á einnig við um almennu færslubókina.

### <a name="to-save-a-standard-journal"></a>Að vista sem staðlaða færslubók
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðafærslubækur** og velja svo viðeigandi tengil.
2. Kóti er færður inn í eina eða fleiri færslubókarlínur.
3. Velja skal bókarlínurnar sem á að nota aftur.
4. Velja skal **Vista sem staðlaða færslubók** aðgerðina.
5. Í beiðniglugganum **Vista sem staðlaða birgðabók** þarf að skilgreina nýja eða eldri staðlaða birgðabók til að vista línurnar í.

    Ef ein eða fleiri staðlaðar birgðabækur hafa verið stofnaðar og skipta á einni þeirra út með nýjum vörubókalínum skal velja kótann sem óskað er eftir í reitnum Kóti.
6. Veldu hnappinn **Í lagi** til að staðfesta að skrifa eigi yfir stöðluðu birgðabókina sem til er og skipta út öllu efni hennar.
7. Velja skal reitinn **Vista ein.upphæð** ef vista á gildin í reitnum **Ein.upphæð** í staðlaðri birgðabók.
8. Velja skal reitinn **Vista magn** ef kerfið á að vista gildin í reitnum **Magn**.
9. Velja hnappinn **Í lagi** til að vista stöðluðu birgðabókina.

Þegar lokið hefur verið við að vista staðlaða birgðabókina opnast glugginn Birgðabók þannig að hægt er að halda áfram og bóka hana, vitandi það að auðvelt er að stofna hana aftur næst þegar bóka þarf sömu eða svipaðar línur.

### <a name="to-reuse-a-standard-journal"></a>Að endurnýta staðlaða færslubók
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Birgðafærslubækur** og velja svo viðeigandi tengil.
2. Valin er **Ná í staðlaðar færslubækur** aðgerðin.

    Glugginn Staðlaðar birgðabækur opnast með kótum og lýsingum á öllum stöðluðum birgðabókum sem til eru.
3. Ef skoða á staðlaða birgðabók áður en hún er valin til endurnotkunar, skal velja aðgerðina **Sýna færslubók**.

    Allar breytingar sem gerðar eru á staðlaðri birgðabók verða virkar um leið. Þær verða til staðar næst þegar staðlaða birgðabókin sem um ræðir er opnuð eða endurnýtt. Þess vegna skal ganga úr skugga um hvort breytingin sé nógu mikilvæg til að beita henni almennt. Annars skal gera sértækar breytingar í birgðabókinni eftir að stöðluðu birgðabókarlínurnar hafa verið settar inn. Sjá þrep 4 hér að neðan.
4. Í glugganum **Staðlaðar birgðabækur** er staðlaða birgðabókin sem nota á aftur valin og smellt á hnappinn **Í lagi**.

    Nú hafa línurnar sem vistaðar voru sem stöðluð birgðabók verið færðar inn í birgðabókina. Ef færslubókarlínur eru þegar til í birgðabókinni koma línurnar sem settar voru inn á eftir þeim sem fyrir eru.

    Ef ekki var merkt við reitinn **Vista ein.upphæð** í keyrslunni **Vista sem staðlaða birgðabók** er reiturinn **Ein.upphæð** í línum sem settar eru inn úr stöðluðu birgðabókinni sjálfkrafa fylltur út með gildandi virði vörunnar, afrituðu úr reitnum **Ein.kostnaður** á birgðaspjaldinu.

    > [!NOTE]  
>   Ef merkt var við reitina **Vista ein.upphæð** eða **Vista magn** skal nú ganga úr skugga um að gildin sem færð voru inn séu rétt fyrir þessa tilteknu birgðaleiðréttingu áður en birgðabókin er bókuð.

    Ef birgðabókarlínurnar sem settar eru inn innihalda vistaðar einingaupphæðir sem ekki á að bóka er fljótlegt að breyta þeim í gildandi virði vörunnar eins og hér er lýst.

6. Velja skal birgðabókarlínur sem á að leiðrétta, og svo velja **Endurreikna einingaupphæð** aðgerðina. Það uppfærir reitinn Ein.upphæð með gildandi kostnaðarverði vörunnar.
7. Valið er **bóka** aðgerð.

## <a name="to-renumber-document-numbers-in-journals"></a>Endurraða númerum fylgiskjals í færslubókum
Til að ganga úr skugga um að þú fáir ekki bókunarvillur vegna fylgiskjalsnúmers pöntunar, geturðu notað aðgerðina **Endurraða númerum fylgiskjals** áður en þú bókar færslubókina.

Í öllum færslubókum sem byggja á almennri færslubók er hægt að breyta reitnum **Skjal nr** þannig að hægt sé að tilgreina mismunandi númer fylgiskjala fyrir mismunandi færslubókarlínur eða sama númer fylgiskjals fyrir tengdar færslubókarlínur.

Ef **Númeraraðir** reiturinn á bókarkeyrslunni er fylltur út krefst bókunargerðin í færslubókunum þess að númer fylgiskjala á stakri eða nokkrum færslubókarlínum séu í réttri röð. Til að ganga úr skugga um að þú fáir ekki bókunarvillur vegna fylgiskjalsnúmers pöntunar, geturðu notað aðgerðina **Endurraða númerum fylgiskjals** áður en þú bókar færslubókina. Ef tengdar færslubókarlínur voru teknar saman eftir númerum fylgiskjala áður en aðgerðin var notuð eru þær áfram teknar saman en gæti verið úthlutað á annað skjalanúmer.

Þessi aðgerð virkar einnig á afmörkuðum yfirlitum.

Sér hver endurnúmerun skjalanúmera mun taka tillit til tengdra jafnana, s.s. greiðslujafnana sem hafa verið framkvæmdar úr skjalinu á færslubókarlínunni á lánardrottnalykli. Að sama skapi geta reitirnir **Kenni jöfnunar** og **Nr. jöfnunarskjals** í færslubókunum sem um ræðir verið uppfærðir.

Eftirfarandi ferli byggist á glugganum **Færslubók**, en á við um allar aðrar bækur sem eru byggðar á færslubókum, eins og glugganum **Greiðslubók**.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **færslubók** og velja svo viðeigandi tengil.
2. Þegar þú ert tilbúinn að bóka færslubókina, skal velja **Endurraða númerum skjals** aðgerðina.

Gildi í **Skjal nr.** reitnum breytast þar sem þörf er á, þannig að númer fylgiskjala á stakri eða nokkrum færslubókarlínum eru í réttri röð. Hægt er að birta færslubókin eftir endurnúmerun skjala.

## <a name="see-also"></a>Sjá einnig
[Bóka færslu beint í Fjárhag](finance-how-post-transactions-directly.md)  
[Bakfæra bókanir](finance-how-reverse-journal-posting.md)  
[Úthluta kostnaði og tekjum](year-allocate-costs-income.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

