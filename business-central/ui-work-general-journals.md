---
title: Vinna með færslubækur til að bóka beint í fjárhag
description: Kynntu þér hvernig skal nota færslubækur til að bóka fjárhagsfærslur í fjárhagsreikninga og aðra reikninga, eins og banka- og lánardrottnareikninga. Notaðu ítrekunarbækur til að bóka uppsafnanir og úthluta stöðum eftir víddargildum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: journals, recurring, accrual, renumber, bulk-post
ms.search.form: 39, 101, 102, 182, 184, 185, 201, 207, 250, 251, 253, 255, 256, 261, 262, 283, 519, 750, 751, 752, 753, 754, 755, 12409, 12410, 12411, 1290, 10101, 11400, 11402, 11403, 11405, 11300, 2000000, 2000001, 2000003, 2000020, 2000021, 2000022
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9fa231ea56c15836d2a3139fc6a35148292a449c
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728479"
---
# <a name="work-with-general-journals"></a>Vinna í færslubókum

Flestar fjárhagslegar færslur eru bókaðar í fjárhag í gegnum skjöl eins og innkaupareikninga og sölupantanir. Hins vegar er einnig hægt að vinna að starfsemi fyrirtækja eins og:

* Innkaup
* Greiðslur
* Notkun ítrekunarbóka til bókunar uppsöfnunar
* Endurfjármögnum kostnað starfsmanns með því að bóka færslubókarlínur í færslubókum  

Flestar færslubækur eru byggðar á færslubókinni og hægt er að vinna allar færslur á **síðunni færslubók**. [Frekari upplýsingar um bókun færslna beint í fjárhag](finance-how-post-transactions-directly.md).  

Til dæmis er hægt að nota Bóka kostnað starfsmanns til endurgreiðslu. Frekari upplýsingar við skráningu og endurgreiðslu á [útgjöldum starfsmanna](finance-how-record-reimburse-employee-expenses.md).

[!INCLUDE [prod_short](includes/prod_short.md)] Býður þó einnig upp á færslubækur sem eru bestar fyrir tilteknar tegundir af færslum, eins og **T.d. greiðslubók** til að skrá greiðslur. Frekari upplýsingar er að finna í [Skrá greiðslur og endurgreiðslur í greiðslubókina](payables-how-post-payments-refunds.md).  

Almennar færslubækur eru notaðar til að bóka fjárhagslegar færslur á fjárhagsreikninga og ýmsa aðra lykla. Aðrir lyklar eru m.a. Banki, Viðskiptamaður, lánardrottinn og starfsmannareikningar. Bókun með færslubók stofnar færslur á fjárhagslykli, jafnvel enn, til dæmis, færslubókarlína er bókuð á viðskiptavinalykil. Færslan er bókuð í fjárhagsreikning í gegnum bókunarflokk.

Upplýsingarnar sem eru færðar inn í færslubók eru til bráðabirgða og það er hægt að breyta þeim í færslubókinni. Þegar færslubókin er bókuð eru upplýsingarnar fluttar í færslur á einstaka lykla þar sem ekki er hægt að breyta þeim. Það er samt sem áður hægt að ógilda bókaðar færslur og snúa við bókunum eða leiðrétta bókanir. Frekari upplýsingar er að finna í [Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="use-journal-templates-and-batches"></a>Nota sniðmát og keyrslur færslubóka

Til eru nokkur færslubókarsniðmát. Hvert sniðmát færslubókar er með sérstaka síðu með ákveðnum aðgerðum og reitum sem verða að styðja aðgerðirnar, eins og síðan **greiðsluafstemmingarbók** til að vinna bankagreiðslur og síðan **greiðslubók** til að borga lánardrottnum þínum eða endurgreiða starfsmönnum. Frekari upplýsingar er að finna í [Framkvæma greiðslur](payables-make-payments.md) og [Afstemma greiðslur viðskiptamanns við inngreiðslubók eða úr færslum í viðskiptamannabók](receivables-how-apply-sales-transactions-manually.md).

Fyrir hvert sniðmát færslubókar, geturðu sett upp þína eigin færslbók sem bókarkeyrsla. Til dæmis er hægt að skilgreina eigin færslubókarkeyrslu fyrir greiðslubók sem er með þitt persónulega útlit og stillingar. Eftirfarandi ábending er dæmi um hvernig skal sérsníða færslubók.

> [!TIP]  
> Ef gátreiturinn leggja til Mótstöðuupphæð **í línunni í rununni á** almennum færslubókarkeyrslum **er** valinn **er reiturinn Upphæð** t.d. í almennum færslubókarlínum fyrir sama fylgiskjalsnúmer sjálfkrafa forfylltur með gildinu sem þarf til að jafna skjalið. Nánari upplýsingar er að finna í [Leyfa [!INCLUDE[prod_short](includes/prod_short.md)] að stinga upp á gildum](ui-let-system-suggest-values.md).

> [!TIP]
> Til að bæta við eða fjarlægja reiti í færslubókum skal nota borðann **Sérsníða**. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

### <a name="validating-general-journal-batches"></a>Staðfesta almennar færslubókarkeyrslur

Hægt er að kveikja á bakgrunnsathugun sem hjálpar til við að koma í veg fyrir tafir þegar bókað er. Ávísunin gerir þér viðvart þegar mistök í fjármálafærslubókinni sem þú ert að vinna í koma í veg fyrir að þú Bókir færslubókina. Á síðunni **Færslubókarkeyrsla** er hægt að velja að láta **Athugun á villu í bakgrunni** [!INCLUDE[prod_short](includes/prod_short.md)] villuleita fjárhagsbækur, svo sem almennar bækur eða greiðslubækur, meðan verið er að vinna í þeim. 

Þegar villuleit **er gerð virk mun FACTBOX Færslubókarávísunum Sýna úthreyfingar í gildandi línu og allt runan**. Staðfesting kemur upp þegar verið er að hlaða fjárhagsbókarkeyrslu, og þegar önnur færslubókarlína er valin. **Heildarfjöldi vandamála** reiturinn í upplýsingareitnum sýnir heildarfjölda vandamála sem [!INCLUDE[prod_short](includes/prod_short.md)] fann og hægt er að velja hann til að opna yfirlit yfir vandamálin. 

Hægt er að nota **Sýna línur með úthreyfingar** og **Sýna allar** Aðgerðir til að skipta á milli færslubókarlína sem ekki eru með úthreyfingar. **Upplýsingakassi fyrir Færslubókarlínuupplýsingar** veitir flýtiyfirlit og aðgang að gögnum úr færslubókarlínum, svo sem fjárhagsreikningi, viðskiptamanni eða lánardrottni og bókunaruppsetningu fyrir lykla.

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]  

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Að skilja aðalreikninga og mótreikninga

Ef stofnaðir voru sjálfgefnir mótreikningar fyrir bókakeyrslur á síðunni **Færslubækur**, eru mótreikningarnir fylltir út sjálfkrafa þegar fyllt er í reitinn **Reikningur nr** Að öðrum kosti er fyllt í reitinn **Reikningur nr.** og reitinn **Mótreikningur nr.** handvirkt. Jákvæð upphæð í reitnum **Upphæð** er tekin út af aðalreikningnum og lögð inn á mótreikninginn. Neikvæð upphæð er lögð inn á aðalreikninginn og tekin út af mótreikningnum.

> [!NOTE]  
> VSK er reiknaður út á aðskilin hátt fyrir aðalreikninginn og mótreikninginn, þannig að þar er hægt að nota mismunandi VSK prósentuhlutfall.

## <a name="work-with-recurring-journals"></a>Vinna með Ítrekunarbækur

Ítrekunarbók er færslubók með sérstökum svæðum til að stjórna færslum sem oft er bókað með fáum, ef einhverjar eru, breytingar. T.d. færslur vegna útgjalda eins og Leigu, áskrifta, rafmagns og hita. Með því að nota Ítrekunarbækur er hægt að bóka fastar og breytilegar upphæðir og tilgreina sjálfvirkar bakfærslufærslur daginn eftir bókunardagsetninguna. Úthlutunarlyklar láta skipta ítrekunarfærslum í ýmsa lykla. Nánari upplýsingar eru í [Úthluta upphæðum ítrekunarbókar á nokkra reikninga](#allocating-recurring-journal-amounts-to-several-accounts).

Með ítrekunarbók er hægt að stofna færslurnar sem bókaðar eru reglulega í einu lagi. Til dæmis lyklar, víddir, víddargildi o. a. frv., skal vera í færslubókinni að lokinni bókun. Ef breytinga er þörf er hægt að gera þær í hvert sinn sem bókað er.

### <a name="recurring-method-field"></a>Reitur ítrekunarmáta

Þessi reitur ákvarðar hvernig meðhöndla á upphæðina í færslubókarlínunni eftir bókun. Til dæmis, ef notuð er sama upphæð í hvert sinn sem lína er bókuð er hægt að láta upphæðina standa. Ef notaðir eru sömu reikningar og texti í línunni, en upphæðin verður breytileg í hvert skipti sem bókað er, er hægt að velja að eyða upphæðinni að lokinni bókun.

| Til að | Sjá |
| --- | --- |
|F  Föst|Magnið í bókarlínunni er látið standa eftir bókun.|
|B  Breytileg|Magninu í bókarlínunni er eytt eftir bókun.|
|S  Staða|Bókaða upphæðin á reikningnum í línunni deilist á reikningana sem eru tilgreindir fyrir línuna í töflunni Færslubók úthlutunar. Staðan á reikningnum verður stillt á núll. Nauðsynlegt er að fylla út reitinn **Úthlutunar %** á síðunni **Úthlutanir**. Nánari upplýsingar eru í [Úthluta upphæðum ítrekunarbókar á nokkra reikninga](#allocating-recurring-journal-amounts-to-several-accounts).|
|FB Föst bakfærsla|Upphæðin í færslubókarlínunni helst eftir bókun og mótfærsla bókast næsta dag.|
|BB Breytileg bakfærsla|Upphæðinni í færslubókarlínunni er eytt eftir bókun og mótfærsla bókast næsta dag.|
|BS Bakfærð staða|Bókaða upphæðin á reikningnum í línunni verður úthlutað á reikningana sem eru tilgreindir fyrir línuna á síðunni **Úthlutanir**. Staðan á reikningnum verður sett á núll og mótfærsla bókast næsta dag.|
|BD – staða eftir vídd|Færslubókarlínan úthlutar kostnaði samkvæmt stöðu fjárhagsreiknings eftir vídd. Beðið verður um að stilla víddarafmarkanir sem á að nota til að reikna stöðu upprunalegs fjárhagsreiknings eftir vídd þar sem á að úthluta kostnaði frá. Velja **skal afmarkanir sem stilla víddarsíun** aðgerðar síðar.|
|RBD – bakfæra stöðu eftir vídd|Færslubókarlínan úthlutar kostnaði samkvæmt bakfærðri stöðu fjárhagsreiknings eftir vídd. Beðið verður um að stilla víddarafmarkanir sem á að nota til að reikna stöðu upprunalegs fjárhagsreiknings eftir vídd þar sem á að úthluta kostnaði frá. Einnig er hægt að **Velja aðgerðina Setja víddarafmarkanir** síðar.|

> [!NOTE]  
> Hægt er að fylla út VSK-reitina annaðhvort í ítrekunarbókarlínu eða úthlutunarbókarlínu en ekki í báðum. Það ma sem sagt einungis fylla þá út á síðunni **Úthlutanir** ef samsvarandi línur í ítrekunarbókinni hafa ekki verið fylltar út.

### <a name="recurring-frequency-field"></a>Reitur ítrekunartíðni

Þessi dagsetningarreikniregla ákvarðar hversu oft á að bóka færsluna í færslubókarlínuna og hana verður að fylla út. Frekari upplýsingar í [Notkunardagaformum](ui-enter-date-ranges.md#use-date-formulas).

#### <a name="examples"></a>Dæmi

Ef þarf að bóka færslubókarlínuna í hverjum mánuði skal færa inn „1M“. Eftir hverja bókun er dagsetningin í reitnum **Bókunardags.** uppfærð í sama mánaðardag næsta mánaðar.

Ef bóka á færslu á síðasta degi hvers mánaðar má gera eitt af þessu:

* Bóka fyrstu færslu á síðasta degi mánaðar með því að færa inn 1D+1M+1D (1 dagur + 1 mánuður + 1 dagur). Með þessari reiknireglu er bókunardagsetningin reiknuð rétt án tillits til þess hve margir dagar eru í mánuðinum.

* Bóka fyrstu færsluna á hvaða mánaðardegi sem er með því að færa inn 1M + CM. Með þessari reiknireglu verður bókunardagsetningin eftir einn heilan mánuð + dagana sem eftir eru í líðandi mánuði.

### <a name="expiration-date-field"></a>Reitur lokadagsetningar

Reiturinn ákvarðar dagsetninguna þegar línan verður bókuð í síðasta sinn. Línan verður ekki bókuð eftir þessa dagsetningu.

Kosturinn við að nota reitinn gildistími er sá að línunni er ekki eytt strax úr færslubókinni. Hægt er að færa inn seinna dags svo hægt sé að nota línuna í framtíðinni.

Ef reiturinn er auður verður línan bókuð í hvert sinn þar til henni er eytt úr færslubókinni.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Úthlutun upphæða á ítrekunarfærslum á nokkra reikninga

Á síðunni **Ítrekunarfærslubók** er hægt að velja aðgerðina **Úthlutanir** til að sjá eða stjórna hvernig upphæðum á ítrekunarbókarlínu er úthlutað á nokkra reikninga og víddir. Athugið að úthlutunin virkar sem mótreikningslína fyrir ítrekunarbókarlínuna.

Eins og í ítrekunarbók er úthlutunin færð inn einu sinni og hún helst í úthlutunarfærslubók eftir bókun. Ekki þarf að færa inn upphæðir og úthlutanir í hvert skipti sem ítrekunarbókarlína er bókuð.

Ef aðferðin í ítrekunarbók er stillt á **Staða** eða **bakfæra stöðu**, eru víddargildiskóta í ítrekunarbók ekki hunsaðir þegar lykillinn er stilltur á núll. Ef ítrekunarlínu er úthlutað á víddargildi á úthlutunum **á** síðunni er aðeins ein bakfærsla stofnuð. 

> [!NOTE]
> Ef þessari ítrekunarbókarlínu sem inniheldur víddargildiskóta er úthlutað er ekki hægt að færa inn sama kóta á **úthlutunarsíðunni**. Ef það er gert verða víddargildin röng.  

Til að úthluta upphæðum ítrekunarbókar samkvæmt víddum skal stilla reitinn **Ítrekunarmáti** á **Staða eftir vídd** eða **Bakfærð staða eftir vídd** í staðinn. Ef staðan er endurtekin í ítrekunarbók er stillt á **Staða eftir vídd** eða **Bakfærslustöðu eftir víddum** eru víddargildiskóta í ítrekunarbók taldir með þegar lykillinn er stilltur á núll. Ef ítrekunarlínu er úthlutað á víddargildi á **úthlutunum** er stofnuð bakfærslufærslur sem samsvara fjölda víddargildissamsetninga sem staðan er samsett úr. Ef lykilstöðu er úthlutað í ítrekunarbók sem inniheldur víddargildiskóta skal muna að nota **stöðu með vídd** eða **bakfæra stöðu eftir víddum** til að tryggja að víddargildin séu rétt jöfnuð eða bakfærð frá upprunareikninginn.  

Fyrirtækið þitt er til að mynda með nokkrar viðskiptaeiningar og nokkrar deildir sem ábyrgðaraðilar þínir hafa sett upp sem víddir. Til að flýta fyrir ferli innkaupareikningsfærslunnar ákveður þú að fá starfsmann viðskiptaskulda til að færa aðeins inn víddir viðskiptaeiningar. Þar sem hver Fyrirtækiseining hefur sérstaka úthlutunarlykla fyrir víddina deild, eins og byggt er á starfsmannafjölda, er hægt að **nota stöðuna BD. vídd** eða **Rbd bakfæra stöðu eftir víddarendurteknum** aðferðum til að endurúthluta útgjöld fyrir hverja fyrirtækiseiningu á réttar deildir á grundvelli úthlutunarlykla.  

> [!NOTE]
> Víddir sem eru stilltar á úthlutunarlínur eru ekki sjálfkrafa reiknaðar út og nauðsynlegt er að tilgreina hvaða víddargildi þarf að stilla á úthlutunarlyklunum. Ef ætlunin er að varðveita tengilinn á milli víddar upprunalykils og víddar úthlutunarlykils er mælt með því að nota möguleikann [Kostnaðarbókhald](finance-about-cost-accounting.md) í staðinn.

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Dæmi: Úthlutun á leigugreiðslum til mismunandi deilda

Þú borgar Leigu mánaðarlega, þannig að þú hefur fært upphæðina inn á staðgreiðslureikningnum í ítrekunarbókarlínu. **Á síðunni úthlutun** er hægt að nota deildarvíddina til að skipta útgjaldunum á milli nokkurra deilda. Til dæmis í samræmi við þann fjölda fermetra sem hver deild starfar við. Útreikningurinn byggist á úthlutunarprósentu fyrir hverja línu. Hægt er að ráðstafa á mismunandi vegu:

* Færið inn mismunandi lykla í mismunandi úthlutunarlínum til að skipta leigukostnaði á milli lykla.
* Færa skal inn sama lykil en nota mismunandi víddargildiskóta fyrir deildarvíddina í hverri línu.

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

### <a name="reversal-date-calculation"></a>Útreikningur bakfærsludags

Þegar endurteknar færslubækur eru notaðar til að bóka uppsöfnun við lok tímabils er mikilvægt að hafa fulla stjórn á bakfærslum. Á síðunni **Ítrekunarfærslubækur** gerir reiturinn **Útreikningur bakfærsludags** þér kleift að stjórna dagsetningunni þegar bakfærslur verða bókaðar þegar ítrekunaraðferðir bakfærslu eru notaðar.

#### <a name="example"></a>Dæmi

Uppsafnanir eru vanalega bókaðar með **endurteknum föstum**, **breytilegum** eða **reikningsjöfnunar** í færslubókarlínunni. Bókunardagsetning bókuðu upphæðarinnar á lykli í færslubókarlínu er reiknuð út með ítrekunartíðni. Bókunardagsetning mótfærslunnar er reiknuð með því að nota **Útreikningur bakfærsludags**, á eftirfarandi hátt:

* Ef reiturinn er auður er mótfærslan bókuð næsta dag.
* Ef reiturinn inniheldur dagsetningarformúlu (til dæmis **5D** fyrir fimm daga) verður mótfærslan bókuð með bókunardagsetningu sem er reiknuð með því að nota útreikning bakfærsludagsetningar.

> [!NOTE]
> Sjálfgefið er að reiturinn **Útreikningur bakfærsludags** sé ekki tiltækur á síðunni **Ítrekunarfærslubækur**. Til að nota svæðið þarf að bæta því við með því að sérsníða síðuna. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

## <a name="work-with-standard-journals"></a>Vinna við staðlaðar færslubækur

Þegar færslubókarlínur sem notandi þekkir eru líklegar til að hafa verið stofnaðar aftur síðar er hægt að vista þær sem staðlaða færslubók áður en færslubókin er bókuð. Sama gildir um vörufærslubækur og Almennar færslubækur.

> [!NOTE]  
> Eftirfarandi ferli vísar í birgðabókina en upplýsingarnar á einnig við um almennu færslubókina.

### <a name="to-save-a-standard-journal"></a>Að vista sem staðlaða færslubók

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðabækur** og velja síðan viðkomandi tengil.
2. Kóti er færður inn í eina eða fleiri færslubókarlínur.
3. Velja skal bókarlínurnar sem á að nota aftur.
4. Velja skal **Vista sem staðlaða færslubók** aðgerðina.
5. Á beiðnisíðunni **Vista sem staðlaða birgðabók** þarf að skilgreina nýja eða eldri staðlaða birgðabók til að vista línurnar í.

    Ef stofnuð hefur verið ein eða fleiri staðlaðar birgðabækur og óskað er eftir að skipta einum þeirra út með nýju birgðabókarlínunum í reitnum kóti **er birgðabókin** valin.
6. Valið **er í lagi** til að sannprófa að skipta eigi innihaldi fyrirliggjandi staðlaða birgðabókar.
7. Til að vista gildin í **reitnum einingarupphæð** í stöðluðu birgðabókarbókinni er reiturinn vista einingarupphæð **valinn**.
8. Til að vista gildin í **reitnum Magn** er reiturinn Vista magn **valinn**.
9. Valið **er í lagi** til að vista stöðluðu birgðabókinn.

Þegar stöðluð birgðabók er vistuð birtir birgðabókarsíðan svo að hægt sé að bóka hana.

### <a name="to-reuse-a-standard-journal"></a>Að endurnýta staðlaða færslubók

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðabækur** og velja síðan viðkomandi tengil.
2. Valin er **Ná í staðlaðar færslubækur** aðgerðin.

    Síðan Staðlaðar birgðabækur opnast með kótum og lýsingum á öllum stöðluðum birgðabókum sem til eru.
3. Ef skoða á staðlaða birgðabók áður en hún er valin til endurnotkunar, skal velja aðgerðina **Sýna færslubók**.

    Breytingar sem gerðar eru í stöðluðu birgðabóki eru útfærðar strax og þær verða þar næst þegar stöðluð birgðabókarbók er opnuð eða endurnýtt. Gætið þess að breytingin sé nógu mikilvæg til að eiga almennt við. Að öðrum kosti skal gera tiltekna breytingu í birgðabókarlínu eftir að stöðluðu birgðabókarlínunum hefur verið bætt við. Sjá skref 4.
4. **Á síðunni staðlaðar birgðabækur** er stöðluð birgðabók valin til að endurnýta og síðan er valið **í lagi**.

    Í birgðabókarbókinni eru línurnar sem voru vistaðar. Ef birgðabókin er þegar með línur, birtast nýju línurnar á eftir þeim.

    Ef ekki er hægt að kveikja á **Vista einingarupphæð** skipta **er reiturinn eining upphæð** í línum sem bætt er við úr stöðluðu bókinni gildið úr **reitnum** Kostnaðarverð á birgðaspjaldinu.

    > [!NOTE]  
    > Ef kveikt er á **Vistunarupphæð eða** tímasetja **vistunarmagns** þarf að gæta þess að nýju gildin séu rétt áður en birgðabókin er bókuð. <!--need to say where and when these were turned on-->

    Ef innsettar birgðabókarlínur innihalda vistaðar einingarupphæðir sem ekki á að bóka er fljótlegt að leiðrétta það í gildandi gildi vörunnar á eftirfarandi hátt. <!--as follows where?-->

5. Velja skal birgðabókarlínur sem á að leiðrétta, og svo velja **Endurreikna einingaupphæð** aðgerðina. Þessi aðgerð uppfærir reitinn eining upphæð með gildandi kostnaðarverði vörunnar.
6. Valið er **Bóka** aðgerðin.

## <a name="to-renumber-document-numbers-in-journals"></a>Endurraða númerum fylgiskjals í færslubókum

Til að forðast bókunarvillur sem stafa af númeri fylgiskjals er hægt að **nota aðgerðina endurnýumber fylgiskjalsnúmer** áður en færslubók er bókuð.

Í öllum færslubókum sem byggja á almennri færslubók er hægt að breyta reitnum **Skjal nr** þannig að hægt sé að tilgreina mismunandi númer fylgiskjala fyrir mismunandi færslubókarlínur eða sama númer fylgiskjals fyrir tengdar færslubókarlínur.

Ef **Númeraraðir** reiturinn á bókarkeyrslunni er fylltur út krefst bókunargerðin í færslubókunum þess að númer fylgiskjala á stakri eða nokkrum færslubókarlínum séu í réttri röð. Veldu aðgerðina **Endurraða númerum fylgiskjals** og viðeigandi **Fylgiskjal nr.** reitir eru síðan uppfærðir. Ef tengdar færslubókarlínur voru flokkaðar eftir skjalnúmeri áður en aðgerðin var notuð, verða þær flokkaðar, en heimilt er að úthluta öðru númeri.  

Þessi aðgerð virkar einnig á afmörkuðum yfirlitum.

Allar endurgerðir skjalanúmera munu virða tengdar umsóknir, eins og greiðsluforrit úr skjalinu í færslubókarlínunni á lánardrottnalykil. **Í samræmi við REITINA kenni** jöfnunar og **Jöfnunarnúmer verður ekki** uppfært í færslunum.

### <a name="to-renumber-documents-in-journals"></a>Til að endurraða fylgiskjölum í færslubókum

Eftirfarandi ferli byggist á glugganum **Færslubók**, en á við um allar aðrar bækur sem eru byggðar á færslubókum, eins og síðunni **Greiðslubók**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Færslubækur** og velja síðan viðkomandi tengil.
2. Þegar bóka á færslubókina skal velja **aðgerðina endurnýumber fylgiskjalsnúmer**.

Gildi í **Skjal nr.** reitnum breytast þar sem þörf er á, þannig að númer fylgiskjala á stakri eða nokkrum færslubókarlínum eru í réttri röð. Eftir að skjöl eru endurklippt er hægt að bóka færslubókina.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/paths/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig

[Bóka færslu beint í Fjárhag](finance-how-post-transactions-directly.md)  
[Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md)  
[Úthluta kostnaði og tekjum](year-allocate-costs-income.md)  
[Fjármál](finance.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Loka opnum færslum birgðahöfuðbókar vegna fastrar jöfnunar í birgðabók](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Endurmat birgða í endurmatsbókinni](inventory-how-revalue-inventory.md)  
[Talning, breytingar og endurflokkun birgða með færslubókum](inventory-how-count-adjust-reclassify.md)  
[Afstemma greiðslur viðskiptavinar með inngreiðslubók eða úr færslum í viðskiptamannabók](receivables-how-apply-sales-transactions-manually.md)  
[Afstemma greiðslur lánardrottins með greiðslubók eða úr færslum í lánardrottnabók](payables-how-apply-purchase-transactions-manually.md)  
[Unnið með samstæðuskjöl og færslubækur](intercompany-how-work-documents-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
