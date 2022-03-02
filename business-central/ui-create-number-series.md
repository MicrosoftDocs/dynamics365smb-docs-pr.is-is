---
title: Stofnun númeraraða
description: Lærðu að setja upp númeraraðir sem úthluta einkvæmum kennikóðum á lykla og skjöl í Business Central.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.search.form: 456, 457, 458, 459, 460, 461, 21, 22, 26, 27, 31
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e95b60af569511a8a95154a53f80bcc235f883f5
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8140476"
---
# <a name="create-number-series"></a>Stofnun númeraraða

Fyrir hvert fyrirtæki sem þú setur upp þarftu að úthluta einstökum kennitölum við hluti eins og aðalbókarreikninga, viðskiptavinar- og seljanda, reikninga og önnur skjöl. Númeraröð er ekki aðeins mikilvæg fyrir auðkenningu. Vel unnið númerakerfi gerir einnig auðveldara að stýra og greina fyrirtækið og getur fækkað villum sem upp koma í gagnafærslu.

> [!Important]
> Sjálfgefið er að eyður er ekki leyfð í númeraröðum vegna þess að nákvæmlega Ferill fjárhagsfærslna verður að vera tiltækur fyrir endurskoðun, samkvæmt lögum, og því verður að fylgja óbrotinn röð með engum Eydd númer.<br /><br />
> Ef þú vilt leyfa eyður í tilteknum númeraröðum skaltu fyrst ráðfæra þig við endurskoðanda eða aðalbókara til að tryggja að þú farir eftir lagalegum skilyrðum í þínu landi/svæði. Nánari upplýsingar er að [finna í eyðurnar í númeraröðinni](#gaps-in-number-series).

> [!NOTE]  
> Við mælum með að þú notir sömu númeraraða kóða eins og þú sérð skráða á síðunni **nr. Raðarlisti** í CRONUS sýnifyrirtækinu. Codes eins og *P-INV +* gætu ekki skilað þér strax, en [!INCLUDE[prod_short](includes/prod_short.md)] hefur marga sjálfgefna stillingar sem eru háð þessum númeraröðakóðum.

Númerakerfi er stofnað með því að setja upp einn eða fleiri kóta fyrir hverja tegund aðalgagna eða skjala. Til dæmis má setja upp einn kóta fyrir númerun viðskiptamanna, annan kóta fyrir númerun sölureikninga og annan fyrir númerun skjala í almennri færslubók. Þegar kóti hefur verið settur upp verður að setja upp minnst eina númeraraðarlínu. Í númeraraðarlínunni eru upplýsingar líkt og fyrsta og síðasta talan í röðinni og upphafsdagsetningin. Hægt er að setja upp fleiri en eina númeraraðarlínu á hvern númeraraðarkóta með mismunandi upphafsdagsetningu fyrir hverja línu. Raðirnar verða notaðar hver á eftir annarri og hver röð hefst á tilgreindum upphafsdegi.

> [!NOTE]
> Hámarkslengd númers í númeraröð er 20 stafir. Við sumar aðstæður mun [!INCLUDE[prod_short](includes/prod_short.md)] bæta við númeri með kerfismynduðu auðkenni. Til dæmis þegar skjöl á borð við reikninga eru notuð til að nota færslur, svo sem greiðslur, myndar [!INCLUDE[prod_short](includes/prod_short.md)] auðkenni fyrir notaðar færslur. Auðkennið er samsett úr númeri númeraraðar og sex stafa auðkenni sem kerfið myndar, t.d. -12345. Ef búist er við því að unnið verði úr meira en 9999 skjölum í bankafærslubók eða gíróbók, eða inngreiðslubókum, skal setja upp númeraröð fyrir skjöl af þessu tagi sem á að hafa færri en 14 stafi.

Þú setur venjulega upp númeraröðina þína til að setja inn næsta röð í röð á nýjum kortum eða skjölum sem þú býrð til. Þú getur hins vegar einnig stillt númeraröð til að leyfa þér að slá inn nýja númerið handvirkt. Þú tilgreinir þetta með **Handfærð númeraröð** gátreitnum.

Hægt er að nota fleiri en einn númeraraðarkóta fyrir hverja tegund frumgagna með því að nota númeraraðatengsl, til dæmis til að nota mismunandi númeraraðir fyrir mismunandi vöruflokka.

## <a name="gaps-in-number-series"></a>Eyður í númeraröðum
Ekki allar færslur sem stofnaðar eru í [!INCLUDE[prod_short](includes/prod_short.md)] eru fjárhagsfærslur sem þarf að nota í röð númeraraðar. Viðskiptamannaspjald, sölutilboð og vöruhúsaaðgerðir eru dæmi um færslur sem eru úthlutaðar númeri úr númeraröðum en eru ekki háðar fjárhagsendurskoðun og/eða er hægt að eyða þeim. Til slíkrar númeraraðar er hægt að velja **Leyfa eyður í númeraröðum** í gátreitnum á síðunni **Númeraröð nr.**. Einnig er hægt að breyta þessari stillingu eftir að búið er að stofna númeraröðina. Frekari upplýsingar eru í [Búa til nýja númeraröð](ui-create-number-series.md#to-create-a-new-number-series).

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Hegðun nr. Reitur á skjölum og kortum
Á sölu-, innkaupa og flutningsskjölum og á öllum kortum, **Nr.** hægt að fylla út sjálfkrafa með númeraröð eða handvirkt og hægt er að setja það upp svo það verði ósýnilegt.

**númer** reitinn má fylla út á þrjá vegu:

1. Ef aðeins ein númeraröð fyrir gerð skjals eða korts er til staðar þar sem gátreiturinn **Sjálfgefin nr.** er valinn og gátreiturinn **Handfærð nr.röð** er ekki valinn, þá er fyllt út í reitinn sjálfkrafa fyllt með næsta númeri í röðinni, og **Nr.** reiturinn verður ekki sýnilegur.

    > [!NOTE]  
    > Ef númeraröðin virkar ekki, til dæmis vegna þess að hún hefur númerin hafa klárast, þá **Nr.** reitur verður sýnilegur og þú getur handvirkt slegið inn númer eða leyst vandann á síðunni **Númeraraðir**.

2. Ef fleiri en ein númeraröð fyrir gerð skjals eða korts eru fyrir hendi og gátreiturinn **Sjálfgefin nr.** er ekki valinn fyrir númeraröðina sem er verið að úthluta, þá **Nr.** reiturinn er sýnilegur og þú getur skoðað síðuna **Listi númeraraða** og valið númeraröðina sem þú vilt nota. Næsta númer í röðinni er síðan sett í **Nr.** .

3. Ef númeraröð hefur ekki verið sett upp fyrir gerð skjals eða korts, eða ef reiturinn **Handfærð nr.röð** er valinn fyrir númeraröðina, þá **Nr.** sýnilegur og slá verður inn númer handvirkt. Mest má rita 20 stafi, bæði tölustafi og bókstafi.

Þegar þú opnar nýtt skjal eða kort sem þar sem númeraröð er til staðar, þá opnast viðkomandi síða **Uppsetning númeraraðir** þannig að þú getir sett upp númeraröð fyrir þessa gerð skjals eða korts áður en þú heldur áfram með aðra gagnafærslu.

> [!NOTE]  
> Ef þú þarft að virkja handvirka númerun á til dæmis nýjum birgðaspjöldum sem hafa verið stofnuð með gagnaflutningsferli sem hefur falið **Nr.** sjálfgefið, þá er farið á síðuna **Uppsetning birgða** og valinn reiturinn **Vörunr.** til að opna og stilla tengda númeraröð á **Handfærð nr.röð**.

## <a name="to-create-a-new-number-series"></a>Til að búa til nýja númeraröð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Númeraraðir** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.  
3. Fyllt er í reitina í nýju línunni. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Veljið aðgerðina **Línur**.  
5. Á síðunni **Númeraraðarlínur nr.** fyllið inn reitina til að skilgreina raunnotkun og innihald númeraraðarinnar sem var stofnuð í skrefi 2.  
6. Endurtakið skref 5 fyrir sem margar mismunandi notkun á númeraröðinni sem þörf er á. Reiturinn **Upphafsdagsetning** skilgreinir svæðið sem númeraröðin er virk.  

> [!TIP]
> Til að leyfa notendum að tilgreina númer handvirkt þegar þeir skrá nýjan viðskiptavin eða lánardrottinn, til dæmis, **er reiturinn handvirkt nr.** í númeraröðinni. Til að afnema handvirka númerið hreinsast svæðið.

Hægt er að úthluta númeraröðinni á sniðmátin sem eru sett upp fyrir mismunandi gerðir viðskiptavina og lánardrottna sem sölumennirnir og innkaupaaðilar bætast oftast við [!INCLUDE [prod_short](includes/prod_short.md)]. Í þeim tilvikum skal setja upp viðeigandi númeraröð, tengja þau í gegnum sambönd og bæta síðan við fyrstu númeraröðinni í viðkomandi sambandi á uppsetningarsíðu viðkomandi.  

## <a name="to-create-relationships-between-number-series"></a>Stofnun tengsla milli númeraraða

Ef settir hafa verið upp fleiri númeraraðakótar en einn fyrir sömu tegund grunnupplýsinga eða færslna er hægt að stofna tengsl milli kótanna. Með þessari aðgerð er auðvelt að velja á milli kóta þegar númer er notað. Þegar samband er sett upp milli flokkarnúmeraraðar er öll tengd röð tengd við einn númerararkóta. Síðan er hægt að færa kótann í reit á **flipanum Tölusetning** fastflipa á einni af viðeigandi uppsetningarsíðu, svo sem **söluuppsetningu &**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Númeraraðir** og velja síðan viðkomandi tengil.
2. Velja skal línuna með númeraröðinni sem á að stofna tengsl við. og veljið síðan **Tengsl**.
3. Færður er inn í reitinn **Raðarkóti** kóti fyrir númeraröðina sem á að tengja við röðina sem valin var í 2. þrepi.
4. Bætt er við línu fyrir hvern kóta sem á að tengja völdum númeraröðum.
5. Lokaðu síðunni.

Þegar eitthvað er sett upp eftir þetta sem þarfnast númers er hægt að nota tengslin sem voru stofnuð til að velja úr skyldum númeraröðum.

## <a name="to-set-up-where-a-number-series-is-used"></a>Til að setja upp hvar númeraröð er notuð

Eftirfarandi málsmeðferð sýnir hvernig á að setja númeraröð fyrir sölustaðinn. Skrefin eru svipuð fyrir önnur svæði.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptakröfur og viðskiptaskuldir** og velja svo viðeigandi tengil.
2. Á síðunni **Sala**, í **Númeraröð**, veldu viðkomandi númeraröð fyrir hvert sölukort eða skjal.

Völdu númerið verður nú notað til að fylla út **Nr.** Sviði á viðkomandi korti eða skjali, í samræmi við þær stillingar sem þú gerðir á númeraröðinni.  



## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/number-series-trail-codes-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]