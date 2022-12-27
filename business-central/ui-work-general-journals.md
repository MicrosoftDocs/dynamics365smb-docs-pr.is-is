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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728479"
---
# <a name="work-with-general-journals"></a>Vinna í færslubókum

Flestar fjárhagsfærslur eru bókaðar í fjárhag gegnum skjöl, eins og innkaupareikninga og sölupantanir. Hins vegar er einnig hægt að vinna úr viðskiptaaðgerðum eins og:

* Innkaup
* Greiðslur
* Notkun ítrekunarbóka til að bóka uppsafnanir
* Endurgreiðslur á útgjöldum starfsmanna með því að bóka dagbókarlínur í færslubókum  

Flestar færslubækur eru byggðar á Almennri færslubók og þú getur unnið úr öllum færslum á síðunni **Almenn færslubók**. Frekari upplýsingar er að finna á [Bóka færslu beint í Fjárhag](finance-how-post-transactions-directly.md).  

Til dæmis er hægt að nota kostnað starfsmanna fyrir endurgreiðslu. Frekari upplýsingar er að finna í [Skrá og endurgreiða starfsmannaútgjöld](finance-how-record-reimburse-employee-expenses.md)

Hins vegar býður [!INCLUDE [prod_short](includes/prod_short.md)] einnig upp á færslubækur sem eru fínstilltar fyrir sérstakar tegundir af færslum, svo sem **Greiðslubók** til að skrá greiðslur. Frekari upplýsingar er að finna í [Skrá greiðslur og endurgreiðslur í greiðslubókina](payables-how-post-payments-refunds.md).  

Þú notar færslubækur til að bóka fjárhagsfærslur á fjárhagsreikninga og ýmsa aðra reikninga. Hinir reikningarnir eru m.a. banka-, viðskiptamanna-, lánardrottna- og starfsmannareikningar. Bókun með almennri færslubók stofnar færslur á fjárhagsreikningum jafnvel þótt þú til dæmis bókir færslubókarlínu á viðskiptamannareikning. Færslan er bókuð á safnreikning fjárhagsbókar í gegnum bókunarflokk.

Upplýsingarnar sem eru færðar inn í færslubók eru til bráðabirgða og það er hægt að breyta þeim í færslubókinni. Þegar færslubókin er bókuð eru upplýsingarnar færðar í færslur á einstökum reikningum, þar sem ekki er hægt að breyta þeim. Það er samt sem áður hægt að ógilda bókaðar færslur og snúa við bókunum eða leiðrétta bókanir. Frekari upplýsingar er að finna í [Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="use-journal-templates-and-batches"></a>Nota sniðmát færslubóka og keyrslur

Til eru nokkur færslubókarsniðmát. Hvert sniðmát færslubókar er með sérstaka síðu með ákveðnum aðgerðum og reitum sem verða að styðja aðgerðirnar, eins og síðan **greiðsluafstemmingarbók** til að vinna bankagreiðslur og síðan **greiðslubók** til að borga lánardrottnum þínum eða endurgreiða starfsmönnum. Frekari upplýsingar er að finna í [Framkvæma greiðslur](payables-make-payments.md) og [Afstemma greiðslur viðskiptamanns við inngreiðslubók eða úr færslum í viðskiptamannabók](receivables-how-apply-sales-transactions-manually.md).

Fyrir hvert sniðmát færslubókar, geturðu sett upp þína eigin færslbók sem bókarkeyrsla. Til dæmis er hægt að skilgreina eigin færslubókarkeyrslu fyrir greiðslubók sem er með þitt persónulega útlit og stillingar. Eftirfarandi ábending er dæmi um hvernig skal sérsníða færslubók.

> [!TIP]  
> Ef valinn er gátreiturinn **Leggja til afstemmingarupphæð** á línunni fyrir keyrsla á síðunni **Færslubókakeyrslur**, þá er **Upphæð** reiturinn í t.d. færslubókarlínum fyrir sama skjalanúmer sjálfkrafa forfylltur með sama gildi sem þarf til að stemma af fylgiskjalið. Nánari upplýsingar er að finna í [Leyfa [!INCLUDE[prod_short](includes/prod_short.md)] að stinga upp á gildum](ui-let-system-suggest-values.md).

> [!TIP]
> Til að bæta við eða fjarlægja reiti í færslubókum skal nota borðann **Sérsníða**. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

### <a name="validating-general-journal-batches"></a>Staðfesta almennar færslubókarkeyrslur

Hægt er að kveikja á bakgrunnsathugun sem hjálpar til við að koma í veg fyrir tafir við bókun. Athugunin lætur þig vita þegar mistök í fjárhagsbókinni sem þú ert að vinna í koma í veg fyrir að þú bókir færslubókina. Á síðunni **Færslubókarkeyrsla** er hægt að velja að láta **Athugun á villu í bakgrunni** [!INCLUDE[prod_short](includes/prod_short.md)] villuleita fjárhagsbækur, svo sem almennar bækur eða greiðslubækur, meðan verið er að vinna í þeim. 

Þegar staðfestingin er virkjuð mun upplýsingareiturinn **Athugun færslubókar** sýna vandamál í núverandi línu og allri keyrslunni. Staðfesting kemur upp þegar verið er að hlaða fjárhagsbókarkeyrslu, og þegar önnur færslubókarlína er valin. **Heildarfjöldi vandamála** reiturinn í upplýsingareitnum sýnir heildarfjölda vandamála sem [!INCLUDE[prod_short](includes/prod_short.md)] fann og hægt er að velja hann til að opna yfirlit yfir vandamálin. 

Hægt er að nota aðgerðirnar **Sýna línur með vandamál** og **Sýna allar línur** til að skipta á milli færslubókarlína sem eru og eru ekki með vandamál. Gátreiturinn **Upplýsingar færslubókarlínu** veitir flýtiyfirlit og aðgang að gögnum úr færslubókarlínum, svo sem fjárhagsreikningi, viðskiptamanni eða lánardrottni, sem og bókunargrunn fyrir tiltekna reikninga.

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]  

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Að skilja aðalreikninga og mótreikninga

Ef stofnaðir voru sjálfgefnir mótreikningar fyrir bókakeyrslur á síðunni **Færslubækur**, eru mótreikningarnir fylltir út sjálfkrafa þegar fyllt er í reitinn **Reikningur nr** Að öðrum kosti er fyllt í reitinn **Reikningur nr.** og reitinn **Mótreikningur nr.** handvirkt. Jákvæð upphæð í reitnum **Upphæð** er tekin út af aðalreikningnum og lögð inn á mótreikninginn. Neikvæð upphæð er lögð inn á aðalreikninginn og tekin út af mótreikningnum.

> [!NOTE]  
> VSK er reiknaður út á aðskilin hátt fyrir aðalreikninginn og mótreikninginn, þannig að þar er hægt að nota mismunandi VSK prósentuhlutfall.

## <a name="work-with-recurring-journals"></a>Vinna með ítrekunarbækur

Ítrekunarbók er færslubók með sérstökum reitum til að stjórna færslum sem eru bókaðar reglulega með litlum eða engum breytingum. Til dæmis færslur vegna kostnaðar eins og leigu, áskrifta, rafmagns og hita. Notkun ítrekunarbóka gerir þér kleift að bóka fastar og breytilegar upphæðir og tilgreina sjálfkrafa bakfærslur fyrir daginn eftir bókunardag. Úthlutunarlyklar gera þér kleift að deila endurteknum færslum á mismunandi reikninga. Nánari upplýsingar eru í [Úthluta upphæðum ítrekunarbókar á nokkra reikninga](#allocating-recurring-journal-amounts-to-several-accounts).

Með ítrekunarbók er hægt að stofna færslur sem bókaðar verða reglulega í aðeins eitt skipti. Til dæmis haldast reikningar, víddir, víddargildi og svo framvegis áfram í færslubókinni eftir bókun. Ef breytinga er þörf getur þú gert þær í hvert sinn sem þú bókar.

### <a name="recurring-method-field"></a>Reitur ítrekunarmáta

Þessi reitur ákvarðar hvernig meðhöndla skal upphæðina í færslubókarlínunni eftir bókun. Ef til dæmis á að nota sömu upphæðina í hvert sinn sem línan er bókuð er hægt að láta upphæðina standa. Ef nota skal sömu reikninga og texta í línunni en breyta upphæðinni í hvert sinn sem er bókað er hægt að velja að eyða upphæðinni eftir bókun.

| Til að | Sjá |
| --- | --- |
|F  Föst|Magnið í bókarlínunni er látið standa eftir bókun.|
|B  Breytileg|Magninu í bókarlínunni er eytt eftir bókun.|
|S  Staða|Bókaða upphæðin á reikningnum í línunni deilist á reikningana sem eru tilgreindir fyrir línuna í töflunni Færslubók úthlutunar. Reikningsstaðan verður stillt á núll. Nauðsynlegt er að fylla út reitinn **Úthlutunar %** á síðunni **Úthlutanir**. Nánari upplýsingar eru í [Úthluta upphæðum ítrekunarbókar á nokkra reikninga](#allocating-recurring-journal-amounts-to-several-accounts).|
|FB Föst bakfærsla|Upphæðin í færslubókarlínunni helst eftir bókun og mótfærsla bókast næsta dag.|
|BB Breytileg bakfærsla|Upphæðinni í færslubókarlínunni er eytt eftir bókun og mótfærsla bókast næsta dag.|
|BS Bakfærð staða|Bókaða upphæðin á reikningnum í línunni verður úthlutað á reikningana sem eru tilgreindir fyrir línuna á síðunni **Úthlutanir**. Staðan á reikningnum verður sett á núll og mótfærsla bókast næsta dag.|
|BD – staða eftir vídd|Færslubókarlínan úthlutar kostnaði samkvæmt stöðu fjárhagsreiknings eftir vídd. Beðið verður um að stilla víddarafmarkanir sem á að nota til að reikna stöðu upprunalegs fjárhagsreiknings eftir vídd þar sem á að úthluta kostnaði frá. Einnig geturðu valið aðgerðina **Stilla víddarafmarkanir** síðar.|
|RBD – bakfæra stöðu eftir vídd|Færslubókarlínan úthlutar kostnaði samkvæmt bakfærðri stöðu fjárhagsreiknings eftir vídd. Beðið verður um að stilla víddarafmarkanir sem á að nota til að reikna stöðu upprunalegs fjárhagsreiknings eftir vídd þar sem á að úthluta kostnaði frá. Einnig er hægt að velja aðgerðina **Stilla víddarafmarkanir** síðar.|

> [!NOTE]  
> Hægt er að fylla út VSK-reitina annaðhvort í ítrekunarbókarlínu eða úthlutunarbókarlínu en ekki í báðum. Það ma sem sagt einungis fylla þá út á síðunni **Úthlutanir** ef samsvarandi línur í ítrekunarbókinni hafa ekki verið fylltar út.

### <a name="recurring-frequency-field"></a>Reitur ítrekunartíðni

Þessi reitur dagsetningarformúlu ákvarðar hversu oft á að bóka færsluna í færslubókarlínuna og fylla þarf hann út. Frekari upplýsingar er að finna í [Nota dagsetningarformúlur](ui-enter-date-ranges.md#use-date-formulas).

#### <a name="examples"></a>Dæmi

Ef þarf að bóka færslubókarlínuna í hverjum mánuði skal færa inn „1M“. Eftir hverja bókun er dagsetningin í reitnum **Bókunardags.** uppfærð í sama mánaðardag næsta mánaðar.

Ef bóka á færslu á síðasta degi hvers mánaðar má gera eitt af þessu:

* Bóka fyrstu færslu á síðasta degi mánaðar með því að færa inn 1D+1M+1D (1 dagur + 1 mánuður + 1 dagur). Með þessari reiknireglu er bókunardagsetningin reiknuð rétt án tillits til þess hve margir dagar eru í mánuðinum.

* Bókaðu fyrstu færsluna á hvaða mánaðardegi sem er með því að slá inn 1M+CM. Með þessari reiknireglu verður bókunardagsetningin eftir einn heilan mánuð + dagana sem eftir eru í líðandi mánuði.

### <a name="expiration-date-field"></a>Reitur lokadagsetningar

Reiturinn ákvarðar dagsetninguna þegar línan verður bókuð í síðasta sinn. Línan verður ekki bókuð eftir þessa dagsetningu.

Kosturinn við að nota reitinn „Lokadagsetning“ er sá að línunni verður ekki eytt strax úr færslubókinni. Þú getur slegið inn síðari dagsetningu þannig að þú getir notað línuna í framtíðinni.

Ef reiturinn er auður verður línan bókuð í hvert skipti þar til henni er eytt úr færslubókinni.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Úthlutun upphæða á ítrekunarfærslum á nokkra reikninga

Á síðunni **Ítrekunarfærslubók** er hægt að velja aðgerðina **Úthlutanir** til að sjá eða stjórna hvernig upphæðum á ítrekunarbókarlínu er úthlutað á nokkra reikninga og víddir. Athugaðu að úthlutun virkar sem mótreikningslína fyrir línu ítrekunarbókar.

Eins og ítrekunarbók slærðu inn úthlutun í eitt skipti og hún heldur sér í úthlutunarbókinni eftir bókun. Ekki þarf að færa inn upphæðir og úthlutanir í hvert skipti sem ítrekunarbókarlína er bókuð.

Ef ítrekunaraðferðin í ítrekunarbókinni er stillt á **Staða** eða **Bakfærð staða** eru víddargildiskóðar í ítrekunarbókinni hunsaðir þegar reikningurinn er stilltur á núll. Ef þú úthlutar ítrekunarlínu á víddargildi á síðunni **Úthlutanir** er aðeins ein bakfærsla stofnuð. 

> [!NOTE]
> Ef þú úthlutar ítrekunarbókarlínu sem inniheldur víddargildiskóða skaltu ekki slá inn sama kóðann á síðunni **Úthlutanir**. Ef það er gert verða víddargildin röng.  

Til að úthluta upphæðum ítrekunarbókar samkvæmt víddum skal stilla reitinn **Ítrekunarmáti** á **Staða eftir vídd** eða **Bakfærð staða eftir vídd** í staðinn. Ef ítrekunarmáti í ítrekunarbók er stilltur á **Staða eftir vídd** eða **Bakfærð staða eftir vídd**, þá eru allir víddargildiskóðar í ítrekunarbókinni teknir til greina þegar lykillinn er stilltur á núll. Þannig að ef þú úthlutar ítrekunarlínu á víddargildi á síðunni **Úthlutanir** þá verða stofnaðar nokkrar bakfærslur sem passa við fjölda samsetninga af víddargildum sem staðan samanstendur af. Ef þú úthlutar reikningsstöðu í gegnum ítrekunarbókina sem inniheldur víddargildiskóða þarf að muna að nota **Staða eftir vídd** eða **Bakfærð staða eftir vídd** til að ganga úr skugga um að staða víddargildanna sé rétt eða rétt bakfærð úr upprunalegum reikningi.  

Fyrirtækið þitt er til að mynda með nokkrar viðskiptaeiningar og nokkrar deildir sem ábyrgðaraðilar þínir hafa sett upp sem víddir. Til að flýta fyrir ferli innkaupareikningsfærslunnar ákveður þú að fá starfsmann viðskiptaskulda til að færa aðeins inn víddir viðskiptaeiningar. Þar sem hver viðskiptaeining er með tiltekna úthlutunarlykla fyrir deildarvíddina, t.d. byggða á fjölda starfsmanna, geturðu notað ítrekunaraðferðirnar **BD – staða eftir vídd** eða **RBD – bakfærð staða eftir vídd** til að endurúthluta kostnaði fyrir hverja viðskiptaeiningu til réttra deilda samkvæmt úthlutunarlyklunum.  

> [!NOTE]
> Víddir sem eru stilltar á úthlutunarlínur eru ekki sjálfkrafa reiknaðar út og nauðsynlegt er að tilgreina hvaða víddargildi þarf að stilla á úthlutunarlyklunum. Ef ætlunin er að varðveita tengilinn á milli víddar upprunalykils og víddar úthlutunarlykils er mælt með því að nota möguleikann [Kostnaðarbókhald](finance-about-cost-accounting.md) í staðinn.

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Dæmi: Úthlutun á leigugreiðslum til mismunandi deilda

Leiga er greidd mánaðarlega, þannig að þú hefur fært upphæðina inn á sjóðsreikninginn í ítrekunarbókarlínu. Á síðunni **Úthlutanir** er hægt að nota vídd deildar til að skipta kostnaðinum á milli nokkurra deilda. Til dæmis eftir fermetrafjölda sem hver deild hefur til umráða. Útreikningurinn byggist á úthlutunarprósentu fyrir hverja línu. Hægt er að úthluta á mismunandi hátt:

* Sláðu inn mismunandi reikninga á mismunandi úthlutunarlínum til að deila leigukostnaði á nokkra reikninga.
* Sláðu inn sama reikninginn en notaðu mismunandi víddargildiskóða fyrir deildarvíddina í hverri línu.

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

### <a name="reversal-date-calculation"></a>Útreikningur bakfærsludags

Þegar endurteknar færslubækur eru notaðar til að bóka uppsöfnun við lok tímabils er mikilvægt að hafa fulla stjórn á bakfærslum. Á síðunni **Ítrekunarfærslubækur** gerir reiturinn **Útreikningur bakfærsludags** þér kleift að stjórna dagsetningunni þegar bakfærslur verða bókaðar þegar ítrekunaraðferðir bakfærslu eru notaðar.

#### <a name="example"></a>Dæmi

Uppsafnanir eru yfirleitt bókaðar með **Föstum**, **Breytilegum** eða **Staða** ítrekunarmátum í færslubókarlínunni. Bókunardagsetning bókuðu upphæðarinnar á lykli í færslubókarlínu er reiknuð út með ítrekunartíðni. Bókunardagsetning mótfærslunnar er reiknuð með því að nota **Útreikningur bakfærsludags**, á eftirfarandi hátt:

* Ef reiturinn er auður er mótfærslan bókuð næsta dag.
* Ef reiturinn inniheldur dagsetningarformúlu (til dæmis **5D** fyrir fimm daga) verður mótfærslan bókuð með bókunardagsetningu sem er reiknuð með því að nota útreikning bakfærsludagsetningar.

> [!NOTE]
> Sjálfgefið er að reiturinn **Útreikningur bakfærsludags** sé ekki tiltækur á síðunni **Ítrekunarfærslubækur**. Til að nota svæðið þarf að bæta því við með því að sérsníða síðuna. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

## <a name="work-with-standard-journals"></a>Vinna með staðlaðar færslubækur

Þegar færslubókarlínur sem líklegt er að verði stofnaðar aftur hafa verið stofnaðar er hægt að vista þær sem staðlaða færslubók áður en færslubókin er bókuð. Hið sama gildir um birgðabækur og almennar færslubækur.

> [!NOTE]  
> Eftirfarandi ferli vísar í birgðabókina en upplýsingarnar á einnig við um almennu færslubókina.

### <a name="to-save-a-standard-journal"></a>Að vista sem staðlaða færslubók

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðabækur** og velja síðan viðkomandi tengil.
2. Kóti er færður inn í eina eða fleiri færslubókarlínur.
3. Velja skal bókarlínurnar sem á að nota aftur.
4. Velja skal **Vista sem staðlaða færslubók** aðgerðina.
5. Á beiðnisíðunni **Vista sem staðlaða birgðabók** þarf að skilgreina nýja eða eldri staðlaða birgðabók til að vista línurnar í.

    Ef ein eða fleiri staðlaðar birgðabækur hafa verið stofnaðar og skipta á einni þeirra út með nýjum birgðabókarlínum skal velja birgðabókina í reitnum **Kóði**.
6. Veldu **Í lagi** til að staðfesta að þú viljir skipta út efni birgðabókar sem er til staðar.
7. Til að vista gildin í reitnum **Einingarupphæð** í staðlaðri birgðabók skal velja reitinn **Vista einingarupphæð**.
8. Til að vista gildin í reitnum **Magn** skal velja reitinn **Vista magn**.
9. Veldu **Í lagi** til að vista stöðluðu birgðabókina.

Þegar þú vistar stöðluðu birgðabókina birtist síða birgðabókarinnar til að þú getir bókað hana.

### <a name="to-reuse-a-standard-journal"></a>Að endurnýta staðlaða færslubók

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðabækur** og velja síðan viðkomandi tengil.
2. Valin er **Ná í staðlaðar færslubækur** aðgerðin.

    Síðan Staðlaðar birgðabækur opnast með kótum og lýsingum á öllum stöðluðum birgðabókum sem til eru.
3. Ef skoða á staðlaða birgðabók áður en hún er valin til endurnotkunar, skal velja aðgerðina **Sýna færslubók**.

    Breytingar sem gerðar eru á staðlaðri birgðabók eru strax innleiddar og þær verða þarna í næsta skipti sem þú opnar eða notar aftur stöðluðu birgðabókina. Gakktu úr skugga um að breytingin sé nógu mikilvæg til að beita henni almennt. Annars skal gera tilteknar breytingar í birgðabókinni eftir að stöðluðu birgðabókarlínunum hefur verið bætt við. Sjá skref 4.
4. Á síðunni **Staðlaðar birgðabækur** er staðlaða birgðabókin sem nota á aftur valin og síðan valið **Í lagi**.

    Birgðabókin inniheldur línurnar sem þú vistaðir. Ef birgðabókin er þegar með línur birtast nýju línurnar á eftir þeim.

    Ef þú kveikir ekki á **Vista einingarupphæð** inniheldur reiturinn **Einingarupphæð** í línum sem bætt er við úr stöðluðu birgðabókinni gildið úr reitnum **Einingarkostnaður** á birgðaspjaldinu.

    > [!NOTE]  
    > Ef þú kveiktir á **Vista einingarupphæð** eða **Vista magn** skaltu ganga úr skugga um að nýju gildin séu rétt áður en þú bókar birgðabókina. <!--need to say where and when these were turned on-->

    Ef birgðabókarlínurnar sem settar eru inn innihalda vistaðar einingarupphæðir sem ekki á að bóka er hægt að breyta þeim á fljótlegan hátt í núverandi gildi vörunnar á eftirfarandi hátt. <!--as follows where?-->

5. Velja skal birgðabókarlínur sem á að leiðrétta, og svo velja **Endurreikna einingaupphæð** aðgerðina. Þessi aðgerð uppfærir reiti einingarupphæðar með núverandi einingarkostnaði vörunnar.
6. Valið er **Bóka** aðgerðin.

## <a name="to-renumber-document-numbers-in-journals"></a>Endurraða númerum fylgiskjals í færslubókum

Til að forðast að bóka villur af völdum skjalanúmerins er hægt að nota aðgerðina **Endurraða númerum fylgiskjals** áður en færslubók er bókuð.

Í öllum færslubókum sem byggja á almennri færslubók er hægt að breyta reitnum **Skjal nr** þannig að hægt sé að tilgreina mismunandi númer fylgiskjala fyrir mismunandi færslubókarlínur eða sama númer fylgiskjals fyrir tengdar færslubókarlínur.

Ef **Númeraraðir** reiturinn á bókarkeyrslunni er fylltur út krefst bókunargerðin í færslubókunum þess að númer fylgiskjala á stakri eða nokkrum færslubókarlínum séu í réttri röð. Veldu aðgerðina **Endurraða númerum fylgiskjals** og viðeigandi **Fylgiskjal nr.** reitir eru síðan uppfærðir. Ef tengdar færslubókarlínur voru teknar saman eftir skjalanúmeri áður en aðgerðin var notuð eru þær áfram saman en gæti verið úthlutað á annað skjalanúmer.  

Þessi aðgerð virkar einnig á afmörkuðum yfirlitum.

Öll endurröðun á númerum fylgiskjals mun taka tillit til tengdra jafnana, t.d. greiðslujöfnunar sem gerð er úr skjalinu á færslubókarlínunni á lánardrottnalykli. Að sama skapi verða reitirnir **Kenni jöfnunar** og **Skjalanr. jöfnunar** uppfærðir í fjárhagsfærslunum.

### <a name="to-renumber-documents-in-journals"></a>Til að endurraða fylgiskjölum í færslubókum

Eftirfarandi ferli byggist á glugganum **Færslubók**, en á við um allar aðrar bækur sem eru byggðar á færslubókum, eins og síðunni **Greiðslubók**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Færslubækur** og velja síðan viðkomandi tengil.
2. Þegar þú ert tilbúinn að bóka færslubókina skaltu velja aðgerðina **Endurraða númerum fylgiskjals**.

Gildi í **Skjal nr.** reitnum breytast þar sem þörf er á, þannig að númer fylgiskjala á stakri eða nokkrum færslubókarlínum eru í réttri röð. Hægt er að bóka færslubókina eftir að skjöl hafa verið númeruð aftur.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/paths/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig

[Bóka færslu beint í Fjárhag](finance-how-post-transactions-directly.md)  
[Bakfæra bókanir í færslubók og afturkalla kvittanir/sendingar](finance-how-reverse-journal-posting.md)  
[Úthluta kostnaði og tekjum](year-allocate-costs-income.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Loka opnum færslum birgðahöfuðbókar vegna fastrar jöfnunar í birgðabók](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Endurmat birgða í endurmatsbókinni](inventory-how-revalue-inventory.md)  
[Talning, breytingar og endurflokkun birgða með færslubókum](inventory-how-count-adjust-reclassify.md)  
[Afstemma greiðslur viðskiptavinar með inngreiðslubók eða úr færslum í viðskiptamannabók](receivables-how-apply-sales-transactions-manually.md)  
[Afstemma greiðslur lánardrottins með greiðslubók eða úr færslum í lánardrottnabók](payables-how-apply-purchase-transactions-manually.md)  
[Unnið með samstæðuskjöl og færslubækur](intercompany-how-work-documents-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
