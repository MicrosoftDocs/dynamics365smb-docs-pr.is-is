---
title: Úthluta rað- eða lotunúmera til vara fyrir rakningu | Microsoft Docs
description: Hægt er að úthluta rað- og lotunúmer við hvaða útleiðarskjal eða innleiðarskjal sem er og bókaðar vörurakningarfærslur þess er síðan hægt að skoða í viðkomandi birgðabókarfærslum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f0136c253e38f4950837bc0fdafae5f5c35cab28
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746092"
---
# <a name="work-with-serial-and-lot-numbers"></a>Vinna með rað- og lotunúmer
Hægt er að úthluta rað- og lotunúmer við hvaða útleiðarskjal eða innleiðarskjal sem er og bókaðar færslur þess er síðan hægt að skoða í viðkomandi birgðafærslum. Þú framkvæmir vinnuna á síðunni **Vörurakningarlínur** sem hægt er að opna úr skjali á innleið eða útleið.

Fylki magnreita efst á síðunni **Vörurakningarlínur** birtir magn og summu vörurakningarnúmera sem verið er að skilgreina á línunum. Magnið verður að samsvara því sem er í fylgiskjalslínunni, sem er sýnt með 0 undir **Óskilgreint** reitunum.

Til að mæla afköst safnar forritið ráðstöfunarupplýsingum af síðunni **Vörurakningarlínur** eingöngu einu sinni, þegar hann er opnaður. Þetta þýðir að forritið uppfærir ekki ráðstöfunarupplýsingarnar á meðan síðan er höfð opin, jafnvel þó að breytingar eigi sér stað í birgðum eða í öðrum skjölum á þeim tíma.

Vörur með rað- eða lotunúmer er hægt að rekja bæði afturábak og áfram í aðfangakeðjunni. Þetta er nytsamlegt fyrir almennt gæðaeftirlit og vöruinnköllun. Frekari upplýsingar er að finna í [Rekja vörurakta vöru](inventory-how-to-trace-item-tracked-items.md).

## <a name="about-picking-serial-or-lot-numbers-in-the-warehouse"></a>Um tiltekt rað- eða lotunúmera í vöruhúsinu
Útleiðarvinnsla rað- eða lotunúmera er verkhluti sem gerist við mörg mismunandi vöruhúsaferli.  

Í sumum vinnslum hafa birgðavörur ekki rað- eða lotunúmer og þá þarf starfsmaður í vöruhúsi að úthluta nýju númeri við útleiðarafgreiðslu, oftast úr forskilgreindri númeraröð.

Í einföldum vinnslum hafa birgðavörur þegar rað- eða lotunúmer, sem þeim hefur t.d. verið úthlutað á meðan á frágangi stóð, og þessi númer flytjast sjálfkrafa með þeim í gegnum allar útleiðaraðgerðir í vöruhúsi án aðgerða starfsmanna í vöruhúsi.

Í sérstökum tilvikum varðandi rað- og lotunúmeraðar birgðir, eru sérstök rað- og lotunúmer skilgreind í upprunaskjalinu, t.d. sem sölupöntun, sem starfsmaður í vöruhúsi verður að taka tillit til við afgreiðslu úr vöruhúsi. Þetta getur verið vegna þess að viðskiptavinurinn bað um ákveðna lotu í framleiðsluferlinu. Þegar birgðatínslu- eða vöruhúsatínsluskjal er stofnað úr upprunaskjali á útleið þar sem rað- eða lotunúmer eru þegar skilgreind þá eru allir reitir á síðunni **Vörurakningarlínur** undir birgðatínslunni skrifvarðir nema reiturinn **Magn til afgreiðslu**. Í því tilvikum eru vörurakningarnúmer tilgreind í aðskildum frágangs-/tínslulínum í birgðatínslulínunum. Magninu hefur þegar verið skipt í sérstakar samstæður rað- eða lotunúmera því í sölupöntuninni eru vörurakningarnúmerin sem á að afhenda tilgreind.  

## <a name="item-tracking-availability"></a>Vörurakning til ráðstöfunar
Þegar unnið er með lotu- og raðnúmer reiknar [!INCLUDE[prod_short](includes/prod_short.md)] út upplýsingar um það hvað til er af lotu- og raðnúmerum og sýnir þær í hinum ýmsu vörurakningarsíðum. Þetta gerir það mögulegt að sjá hversu mikið af lotu- og raðnúmerum er nú þegar verið að nota fyrir önnur fylgiskjöl. Þetta minnkar villur og óvissu vegna tvöfaldra úthlutana.

Á síðunni **Vörurakningarlínur** er viðvörunartákn sýnt í reitunum **Lotunr. til ráðstöfunar** eða **Raðnr. til ráðstöfunar** ef eitthvað af magninu sem valið var, eða það allt, er notað í öðrum skjölum eða hvort lotu- eða raðnúmerið er ekki fyrir hendi.

Á síðunum **Lotunr./Raðnr.-listi**, **Lotunr./Raðnr.-ráðstöfunarmagn** og **Vörurakning - Valdar færslur** eru birtar upplýsingar um það hversu mikið magn af vöru er verið að nota. Þetta felur í sér eftirfarandi upplýsingar.

|Svæði|Description|
|-----|-----------|  
|**Heildarmagn**|Heildarmagn þeirra vara sem eru í birgðum.|
|**Umbeðið magn samtals**|Heildarfjöldi þeirra vara sem beðið er um og verða notuð í þessu og öðrum skjölum.|
|**Magn í undirbúningi**|Fjöldi þeirra vara sem búið er að biðja um að nota í núverandi skjali en hefur ekki enn verið bundið við gagnagrunninn.|
|**Umbeðið magn**|Fjöldi þeirra vara sem búið er að biðja um að nota í núverandi skjali.|
|**Heildarmagn tiltækt**|Heildarfjöldi atriða í birgðum, að frádregnu magni varanna sem beðið er um í þessu skjali og öðrum skjölum (umbeðið magn samtals) að frádregnu magninu sem beðið er um en hefur ekki verið fært í skjalið (magn í undirbúningi).|

Ef unnið er á síðunni **Vörurakningarlínur** í langan tíma eða ef mikið er um aðgerðir með þeirri vöru sem verið er að vinna með er hægt að velja **Endurnýjun ráðstöfunar**. Að auki er ráðstöfun vörunnar endurskoðuð sjálfkrafa þegar síðunni er lokað til að fá staðfestingu á því að engin ráðstöfunarvandamál eru fyrir hendi.

## <a name="to-set-up-item-tracking-codes"></a>Til að setja upp vörurakningarkóða
Vörurakningarkóti endurspeglar ýmis íhugunarefni fyrirtækis varðandi notkun rað- og lotunúmera á vörur sem eru á leið í gegnum birgðirnar.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörurakningarkóðar** og veldu síðan tengda tengilinn.  
2. Valið er **Nýtt** aðgerð.
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Smellt er á flýtiflipana **Raðnr.** og **Lotunr.** til að skilgreina aðferðir í vörurakningu eftir rað- og lotunúmerum.  

> [!NOTE]  
>  Ef þú vilt fylgjast með ákveðnum vörum eða ákveðnum lotum í gegnum líftíma þeirra, verður þú að velja reitina **Sértæk SN rakning** og **Sértæk loturakning** í þessari röð. Þar af leiðandi þegar fengist er við einingu á útleið af vöru með þessum vörurakningarkóða verður þú alltaf að tilgreina hvaða fyrirliggjandi raðnúmer skuli notað. Þetta merkir að þegar seld er eining af vörunni verður að tengja hana ákveðnum hópi raðnúmera eða ákveðnu lotunúmeri í birgðum. Með öðrum orðum, raðnúmer eða lotunúmer sem tengt er vöru þegar hún fer í birgðir verður að fylgja þeirri vörutegund út úr birgðunum.

Þar sem þessi ákveðni uppsetningarreitur nær til allra mögulegra færslna varðandi vöruna verða einstakir inn-/útleiðarreitir einnig valdir. Þó hefur sérhver inn- og útleiðarreitur ekkert með jöfnun þvert á birgðir að gera - þeir eru aðeins til skilgreiningar á verkflæði í fyrirtækinu og hafa með það að gera hvenær á að úthluta vörurakningarnúmerum.  

### <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Uppsetning gildistíma fyrir rað- og lotunúmer  
Fyrir sumar vörur þarf ef til vill að setja upp tiltekna gildistíma og reglur með vörurakningaruppsetningunni. Með þessari aðgerð má fylgjast með því hvenær tiltekin rað- og lotunúmer falla úr gildi.

1. Veljið fyrirliggjandi vörurakningarkóða og svo aðgerðina **Breyta**.  
2.  Á flýtiflipanum **Ýmislegt** skal velja eftirfarandi gátreiti.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Ströng lokasöludagsetning**|Tilgreinir að fyrningardagsetning sem tengd er vörunni þegar hún kemur í birgðir verður að gilda þegar hún fer þaðan.|  
    |**Handv. lokasöludags. áskilin**|Tilgreinir að færa þarf dagsetninguna þegar varan rennur út handvirkt í vörurakningarlínuna.|  
    |**Hunsa lokadagsetningar**|Tilgreinir að þú viljir ekki reikna út lokadagsetningar. |  

### <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Uppsetning ábyrgðar fyrir rað- og lotunúmer  
Fyrir sumar vörur þarf ef til vill að setja upp tilteknar ábyrgðir í vörurakningarkótanum. Þessi aðgerðareiginleiki gerir kleift að halda utan um það hvenær ábyrgðin á tilteknum rað- eða lotunúmerum í birgðahaldi rennur út.        
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörurakningarkóðar** og veldu síðan tengda tengilinn.  

1. Veljið fyrirliggjandi vörurakningarkóða og svo aðgerðina **Breyta**.  
2.  Á flýtiflipanum **Ýmisl.** skal fylla inn í reitinn **Ábyrgðardagsetning** og velja svo gátreitinn sem hér segir.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Ábyrgðardagsetningarregla**|Tilgreinir síðasta dag ábyrgðar á vörunni.|  
    |**Handv. áb.dags.færsla áskilin**|Tilgreinir að færa þurfi inn ábyrgðardagsetninguna handvirkt í vörurakningarlínuna.|  

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Úthlutun rað- eða lotunúmera á færslur á leið inn.  
Það getur komið fyrirtækjum vel að hægt sé að rekja vöru frá því hún berst fyrirtækinu. Þegar svo háttar til er innkaupapöntun oft helsta vísbendingin, en vörurakningu má gera út frá hvaða skjali sem er og færslur í því birtar í samsvarandi birgðafærslum.  

Nákvæmar reglur um vörurakningu í fyrirtækinu ráðast af uppsetningu á síðunni **Kóðakort vörurakningar**.  

> [!NOTE]  
>  Til að nota vörurakningarnúmer í vöruhúsaaðgerðum verða uppsetningarreitirnir **Lotuvöruhúsarakning** og **SN vöruhúsarakning** að vera valdir, þar sem þeir skilgreina sérstakar reglur við meðhöndlun rað- og lotunúmera í vöruhúsaaðgerðum.  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupapantanir** og veldu síðan tengda tengilinn.  
2.  Valin er viðkomandi fylgiskjalslína og á flýtiflipanum **Línur** skal velja aðgerðina **Lína** og loks aðgerðina **Vörurakningarlínur**.  

    Nú er hægt að úthluta rað- eða lotunúmerum á eftirfarandi hátt:  

    -   Sjálfvirkt, með því að smella á **Úthluta raðnr.** eða **Úthluta lotunr.** og úthlutar kerfið þá rað- eða lotunúmerum úr forskilgreindum númeraröðum.  
    -   Sjálfvirkt, með því að smella á **Stofna sérsniðin RN**, og úthlutar þá kerfið rað- eða lotunúmerum samkvæmt númeraröðum um sem notandi skilgreinir sérstaklega fyrir mótteknar vörur.  
    -   Handvirkt með því að færa inn rað- eða lotunúmer beint, t.d. númer birgis.  
    -   Handvirkt með því að úthluta hverri vörueiningu sérstöku númeri.  

3. Til að úthluta sjálfvirkt skal velja **Stofna sérstillt raðnúmer** aðgerðina.  
4. Í reitinn **Sérsniðin raðnr.** er fært inn upphafsnúmer lýsandi númeraraðar, t.d. **r.nr.-Birg0001**.  
5. Í reitinn **Hækka** er færð talan 1 til að tiltaka að hvert raðnúmer hækkar um einn.  

    Reiturinn **Magn sem stofna á** inniheldur sjálfgefið línumagn en því má breyta.  

6. Gátmerki er sett í gátreitinn **Stofna nýtt lotunr.** svo að nýju raðnúmerin flokkist í sérstaka lotu.  
7. Velja hnappinn **Í lagi**.  

Lotunúmer með einstökum raðnúmerum er stofnað eftir vörumagni í skjalslínu og er byrjað á **r.nr.-Birg0001**.  

Magnreitirnir í hausnum sýna magn og samtölur vörurakningarnúmeranna sem eru skilgreind á síðunni. Magnið verður að samsvara því sem er í fylgiskjalslínunni, og er sýnt með í reitunum **Óskilgreint**.  

Þegar fylgiskjalið er bókað eru vörurakningarfærslurnar fluttar í tengdar birgðafærslur.

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Úthlutun rað- eða lotunúmera vegna færslna á leið út.  
Tvær leiðir eru færar til að bæta við rað- og lotunúmerum fyrir færslur á útleið:  

-   Valið úr tiltækum rað- og lotunúmerum Þetta á við þegar vörurakningarnúmerum hefur þegar verið úthlutað við færslu á innleið. Frekari upplýsingar er að finna í [Að velja úr tiltækum rað- og lotunúmerum](inventory-how-work-item-tracking.md#to-select-from-existing-serial-or-lot-numbers).
-   Nýjum rað- eða lotunúmerum úthlutað við færslur á útleið. Þetta á við þegar vörurakningarkóðum er ekki úthlutað á vörur fyrr en þær eru seldar og tilbúnar til afhendingar.  

Mismunandi reglur um vörurakningarnúmer eru settar upp á síðunni **Kóðaspjald vörurakningar**.  

> [!NOTE]  
>  Til að úthluta vörurakningarnúmerum í vöruhúsaaðgerðum þarf að velja gátreitina **RN vöruhúsarakning** og **Lotuvöruhúsarakning** á vörurakningarkóðaspjaldi vörunnar.    

1. Valin er viðkomandi fylgiskjal og á flýtiflipanum **Línur** skal velja aðgerðina **Pöntun** og loks aðgerðina **Vörurakningarlínur**.  

    Hægt er að úthluta vörurakningarnúmerum með eftirtöldum aðferðum:  
    -   Sjálfvirkt, úr forskilgreindum númeraröðum: Velja aðgerðina **Úthluta raðnúmeri** eða **Úthluta lotunúmeri**.  
    -   Sjálfvirkt, á grundvelli færibreyta sem notandi skilgreinir sérstaklega fyrir útleiðarvöruna: Velja aðgerðina **Stofna sérsniðið RN**.  
    -   Handvirkt með því að færa inn rað- og lotunúmer án þess að nota númeraraðir.  

2.  Í þessu ferli skal úthluta raðnúmeri sjálfkrafa með því að velja **Úthluta raðnúmeri**.  

    Reiturinn **Magn sem stofna á** inniheldur sjálfgefið línumagn en því má breyta.  
3.  Gátmerki er sett í reitinn **Stofna nýtt lotunr.** svo að nýju raðnúmerin flokkist í sérstaka lotu.  
4.  Veldu hnappinn **Í lagi** og stofnar kerfið þá lotunúmer og ný einstök raðnúmer samkvæmt magninu til afgreiðslu í viðkomandi fylgiskjalslínum.  

Fylki magnreitanna efst sýna á gagnvirkan hátt magn og samtölur vörurakningarnúmeranna sem eru skilgreind á síðunni. Magnið verður að samsvara því sem er í fylgiskjalslínunni, og er sýnt með **0** undir **Óskilgreint**.  

Þegar fylgiskjalið er bókað eru vörurakningarfærslurnar fluttar í tengdar birgðafærslur.  

## <a name="to-select-from-existing-serial-or-lot-numbers"></a>Valið úr tiltækum rað- og lotunúmerum  
Þegar unnið er með vörur sem krefjast vörurakningar og verið er að stofna færslur á útleið (þar sem vörur fara úr birgðum) þarf yfirleitt að velja lotu- eða raðnúmerið frá þeim sem eru til fyrir í birgðum.  

 Nákvæmar reglur um vörurakningu í fyrirtækinu ráðast af uppsetningu á töflunni **Vörurakningarkóti**.  

> [!NOTE]  
>  Ef hægt á að vera að halda utan um vörurakningarnúmer í vöruhúsaaðgerðum verður að setja vöruna upp með  vöruhúsrakningu lotu-/raðnúmera, því hún segir fyrir um sérstakar reglur varðandi rað- og lotunúmer í vöruhúsi. .

1.  Af skjali á útleið er valin lína sem á að velja rað- eða lotunúmer í.  
2.  Á flýtiflipanum **Línur** skal velja aðgerðina **Aðgerðir**, velja aðgerðina **Lína** eða **Vara** og loks aðgerðina **Vörurakningarlínur**.  
3.  Á síðunni **Vörurakningarlínur** er um þrennt að velja þegar kemur að því að tilgreina lotu- eða raðnúmer:  

    -   Velja **Lotunr.** eða **Raðnr.** reitinn og svo valið númer á síðunni **Yfirlit vörurakningar**.  
    -   Valið er **Velja Færslur** aðgerð. Síðan **Velja færslur** sýnir öll lotu- eða raðnúmer ásamt upplýsingum um það hvað er til.

4. Í reitnum **Valið magn** er slegið inn magn hvers lotu- eða raðnúmers sem á að nota.   
5. Veldu hnappinn **Í lagi** og valdar vörurakningarupplýsingar eru færðar á síðuna **Vörurakningarlínur**.  
6. Vörurakningarnúmerið er slegið inn eða skannað.

Magnreitirnir í hausnum sýna magn og samtölur vörurakningarnúmeranna sem skilgreind eru á síðunni. Magnið verður að samsvara því sem er í fylgiskjalslínunni, og er sýnt með **0** undir **Óskilgreint**.  

 Þegar fylgiskjalið er bókað eru vörurakningarfærslurnar fluttar í tengdar birgðafærslur.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Hvernig á að meðhöndla rað- og lotunúmer í millifærslupöntunum  
Ferlum við meðferð rað- og lotunúmera sem verið er að flytja milli birgðastöðva svipar til þeirra sem beitt er þegar vara er keypt og seld.  

Millifærslupöntunin er þó sérstök að því leyti að sending og móttaka er framkvæmd úr sömu millifærslulínu og því er notað sama eintak af Uppsetningarspjald fyrir uppfærslu gengis **Vörurakningarlínur**. Þetta merkir að vörurakningarnúmer sem send eru úr einni birgðageymslu verður að móttaka óbreytt í annarri birgðageymslu.  

 Nákvæmar reglur um vörurakningu í fyrirtækinu ráðast af uppsetningu á töflunni  **Vörurakningarkóti** .    
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Flutningspantanir** og veldu síðan tengda tengilinn.  
2.  Opna skal flutningspöntunina sem á að vinna. Á flýtiflipanum **Línur** skal velja aðgerðina **Lína**, velja aðgerðina **Vörurakningarlínur** og loks aðgerðina **Afhending**.  
3.  Á síðunni **Vörurakningarlínur** er rað- eða lotunúmerum úthlutað eða þau valin eins og fyrir hverja aðra útleiðar-birgðafærslu.  

    Þegar unnið er við rað- og lotunúmer vegna millifærsluvöru er yfirleitt búið að úthluta vörunni númerum. Þess vegna felst ferlið yfirleitt í því að velja úr þeim rað- eða lotunúmerum sem fyrir eru.  

4.  Millifærslupöntunin, fyrst afhending og síðan móttaka, er bókuð til þess að skráð sé að varan sé flutt með vörurakningarfærslum.  

Meðan á millifærslu stendur er síðan **Vörurakningarlínur** skrifvarin.  

## <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>Meðhöndla rað- og lotunúmer þegar móttökulínur eru sóttar úr innkaupareikningi  
Þegar notuð er aðgerð til að sækja bókaðar kvittanir eða afhendingarlínur frá tengdum reikningum eða kreditreikningum þá eru vörurakningarlínur í vöruhúsaskjölum færðar sjálfkrafa. Hins vegar eru þær unnar á sérstakan hátt.

Aðgerðin styður við eftirfarandi ferli á innleið:  
-   **Sækja móttökulínur** - úr innkaupareikningi.  
-   **Sækja skilaafhend.línur** - úr innkaupakreditreikningi.  

Aðgerðin styður við eftirfarandi ferli á útleið:  
-   **Sækja afhendingarlínur** - úr sölureikningi eða tengdum afhendingum.  
-   **Sækja vöruskilamóttökulínur** - úr sölukreditreikningi.  

Í þessum tilvikum eru fyrirliggjandi vörurakningarlínur afritaðar sjálfkrafa í reikninginn eða kreditreikninginn en síðan **Vörurakningarlínur** leyfir ekki breytingar á rað- eða lotunúmerum - aðeins er hægt að breyta magni. Aðeins er hægt að breyta magni.  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupareikningar** og veldu síðan tengda tengilinn.  
2.  Opna innkaupareikning fyrir vörur sem eru innkaup með rað- eða lotunúmerum.  
3.  Frá línu innkaupareiknings á flýtiflipanum **Línur** skal velja **Sækja móttökulínur** aðgerðina.  
4.  Á síðunni **Sækja móttökulínur** veljið móttökulínur sem eru með vörurakningarlínur og veljið svo hnappinn **Í lagi**.  

    Upprunaskjalið er afritað í innkaupareikninginn sem ný lína og vörurakningarlínurnar afritaðar af síðunni **Vörurakningarlínur** sem liggur að baki.  

5.  Í glugganum innk. kr. veljið fluttu móttökulínuna.  
6.  Á flýtiflipanum **Línur** skal velja aðgerðina **Lína**, og svo velja aðgerðina **Vörurakningarlínur**  til að sjá vörurakningarlínurnar sem hafa verið færðar.  

Ekki er hægt að breyta efni reitanna  **Raðnr.** og  **Lotunr.** Þó er hægt að eyða heilum línum eða breyta magni til samræmis við breytingarnar í upprunalínunni.  

## <a name="to-record-serial-or-lot-number-information"></a>Skráning upplýsinga um rað- og lotunúmer  
Ef tengja þarf einhverjar upplýsingar við tiltekið vörurakningarnúmer, t.d. vegna gæðaeftirlits, er hægt að gera það á upplýsingaspjaldinu fyrir rað- eða lotunúmer.

1. Opna skjal sem hefur verið úthlutað rað- eða lotunúmerum.
2. Opnaðu síðuna **Vörurakningarlínur** fyrir skjalið.
3. Velja, til dæmis, aðgerðina **Raðnr. upplýsingaspjalds**  

    Reitirnir **Raðnúmer** og **Lotunr.** eru fyllt út fyrirfram úr vörurakningarlínunni.  
4. Færa inn stuttan texta í reitinn **Lýsing**, til dæmis um ástand vörunnar.  
5. Velja aðgerðina **Athugasemd** til að stofna aðra athugasemdaskrá.  
6. Veljið gátreitinn **Lokaður** til að sleppa rað- eða lotunúmerinu úr færslum.  

Ef búið er að stofna raðnúmer í magni með því að nota **Stofna sérsniðið RN** eða **Úthluta raðnúmeri** er hægt að virkja **Stofna raðnúmersupplýsingar** og upplýsingakort verður stofnað fyrir hverja rakningarlínu.

Einnig er hægt að búa til upplýsingakort þegar færslubækur eða skjöl eru bókuð á síðunni **Vörurakningarkóði** með því að kveikja á víxlun **Stofna raðnúmersuppl. við bókun** eða **Stofna raðnúmersuppl. við bókun**. 

Hægt er að breyta stofnuðum rað- eða lotuupplýsingaspjöldum síðar.

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Breyta fyrirliggjandi upplýsingum um rað- og lotunúmer  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vara** og veldu síðan tengda tengilinn.  
2. Velja vöru sem hefur vörurakningarkóða og upplýsingar um rað- eða lotunúmer.
3. Á síðunni **Birgðaspjald** skal velja aðgerðina **Færslur** og velja síðan **Fjárhagsfærslur**.
4. Velja reitinn **Lotunr.** eða **Raðnúmer**. Ef upplýsingar eru til fyrir þetta vörurakningarnúmer þá mun síðan **Lotunr. upplýsingalista** eða **Raðnr. upplýsingalista** opnast.  
5. Velja skal spjald og síðan **Lotunr./raðnúmeraupplýsingaspjald** aðgerðina.  
6. Breyta stuttri lýsingu, athugasemdafærslu eða reitnum **Lokaður**.  

Ekki er hægt að breyta rað- eða lotunúmerum eða magni. Til að gera það verður að endurflokka birgðabókarfærsluna í spurningu. Nánari upplýsingar er að finna í [Endurflokkun lotu- eða raðnúmera](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## <a name="to-reclassify-serial-or-lot-numbers"></a>Endurflokka rað- eða lotunúmer  
Endurflokkun vörurakningar fyrir vöru þýðir að breyta lotu- eða raðnúmeri í nýtt lotu- eða raðnúmer eða breyta lokadagsetningunni í nýja lokadagsetningu. Ef verið er að vinna með lotur er líka hægt að sameina margar lotur í eina lotu. Þessi verkefni eru framkvæmd með notkun vöruendurflokkunarbókarinnar.

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðaendurflokkunarbók** og veldu síðan tengda tengilinn.  
2.  Línan er fyllt út með viðeigandi upplýsingum. Nánari upplýsingar er að finna í [Telja birgðir með skjölum](inventory-how-count-inventory-with-documents.md) eða [Telja, leiðrétta og endurflokka birgðir með Færslubókum](inventory-how-count-adjust-reclassify.md).
3.  Velja aðgerðina **Vörurakningarlínur**  
4.  Í reitnum **Raðnr.** eða **Lotunr** skal velja gildandi rað- eða lotunúmer.  
5.  Hægt er að slá inn nýtt vörurakningarnúmer með því að slá það inn í reitinn **Nýtt raðnr.** eða **Nýtt lotunr.**. Hægt er að sameina eina eða fleiri lotur við eina nýja lotu eða lotu sem er til fyrir.  

    > [!NOTE]  
    >  Athuga skal að þegar notandi endurflokkar fyrningardagsetningar, eru þær vörur sem hafa elstu lokadagsetningarnar fyrir færslur á útleið lagðar til fyrst. Frekari upplýsingar eru í [Tínsla skv. FEFO](warehouse-picking-by-fefo.md).  

5.  Hægt er að slá inn nýja lokadagsetningu fyrir rað- eða lotunúmerið með því að slá það inn í reitinn **Ný lokadagsetning**.  

    > [!IMPORTANT]  
    >  Ef verið er að endurflokka lotu á sama lotunúmer en með aðra lokadagsetningu þá þarf að endurflokka alla lotuna með því að nota línu einnar vöru í endurflokkunarbókinni. Ef verið er að endurflokka meira en eina lotu á fleira en eitt lotunúmer, sem þýðir að verið er að sameina fleiri en eina lotu inn í eina nýja lotu, þá þarf að slá sömu lokadagsetningu inn fyrir allar loturnar. Ef verið er að endurflokka eina lotu sem er í annarri lotu en hefur aðra lokadagsetningu þá þarf að nota lokadagsetningu seinni lotunnar. Ef reiturinn **Ný lokadagsetning** er látinn standa auður þá verður lotu- eða raðnúmerið endurflokkað með auðri lokadagsetningu.  

6.  Ef til eru upplýsingar um gamla rað- eða lotunúmerið er hægt að afrita það yfir á nýja rað- eða lotunúmerið.  

    1.  Á síðunni **Vörurakningarlínur** skal velja **Nýtt raðnr. upplýsingar** aðgerðina eða **Nýtt lotunr. upplýsingar** aðgerðina.  
    2.  Til að afrita upplýsingar frá gamla lotu- eða raðnúmerinu er aðgerðin **Afrita upplýsingar** valin.  
    3.  Á upplýsingalistasíðunni er valið það lotu- eða raðnúmer sem ætlunin er að afrita og hnappurinn **Í lagi** valinn.  

7.  Hægt er að breyta upplýsingunum sem eru fyrir hendi varðandi lotu- eða raðnúmerið með því að skrá lotu- eða raðupplýsingarnar.  
8.  Færslubókin er bókuð til að tengja nýju vörurakningarnúmerin eða lokadagsetningarnar við viðkomandi birgðafærslu.

## <a name="see-also"></a>Sjá einnig
[Rekja vöruraktar vörur](inventory-how-to-trace-item-tracked-items.md)   
[Birgðir](inventory-manage-inventory.md)  
[Hönnunarupplýsingar: vörurakning](design-details-item-tracking.md)
[Hönnunarupplýsingar - vörurakning og frátekning](design-details-item-tracking-and-reservations.md)  
[Taka frá vörur](inventory-how-to-reserve-items.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]