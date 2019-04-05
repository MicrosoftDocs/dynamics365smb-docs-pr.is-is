---
title: Búa til númeraröð | Microsoft Docs
description: Lærðu hvernig á að setja upp númeraröð sem úthlutar einstökum auðkenniskóðum til reikninga og skjala í Business Central.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 46131d6ad5f77a02ffe33d24f1210a226c3041c1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799735"
---
# <a name="create-number-series"></a>Stofnun númeraraða
Fyrir hvert fyrirtæki sem þú setur upp þarftu að úthluta einstökum kennitölum við hluti eins og aðalbókarreikninga, viðskiptavinar- og seljanda, reikninga og önnur skjöl. Númeraröð er ekki aðeins mikilvæg fyrir auðkenningu. Vel unnið númerakerfi gerir einnig auðveldara að stýra og greina fyrirtækið og getur fækkað villum sem upp koma í gagnafærslu.

> [!NOTE]  
>   Við mælum með að þú notir sömu númeraraða kóða eins og þú sérð skráða á síðunni **nr. Raðarlisti** í CRONUS sýnifyrirtækinu. Codes eins og *P-INV +* gætu ekki skilað þér strax, en [!INCLUDE[d365fin](includes/d365fin_md.md)] hefur marga sjálfgefna stillingar sem eru háð þessum númeraröðakóðum.

Númerakerfi er stofnað með því að setja upp einn eða fleiri kóta fyrir hverja tegund aðalgagna eða skjala. Til dæmis má setja upp einn kóta fyrir númerun viðskiptamanna, annan kóta fyrir númerun sölureikninga og annan fyrir númerun skjala í almennri færslubók. Þegar kóti hefur verið settur upp verður að setja upp minnst eina númeraraðarlínu. Í númeraraðarlínunni eru upplýsingar líkt og fyrsta og síðasta talan í röðinni og upphafsdagsetningin. Hægt er að setja upp fleiri en eina númeraraðarlínu á hvern númeraraðarkóta með mismunandi upphafsdagsetningu fyrir hverja línu. Raðirnar verða notaðar hver á eftir annarri og hver röð hefst á tilgreindum upphafsdegi.

Þú setur venjulega upp númeraröðina þína til að setja inn næsta röð í röð á nýjum kortum eða skjölum sem þú býrð til. Þú getur hins vegar einnig stillt númeraröð til að leyfa þér að slá inn nýja númerið handvirkt. Þú tilgreinir þetta með **Handfærð númeraröð** gátreitnum.

Hægt er að nota fleiri en einn númeraraðarkóta fyrir hverja tegund frumgagna með því að nota númeraraðatengsl, til dæmis til að nota mismunandi númeraraðir fyrir mismunandi vöruflokka.

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Hegðun nr. reitur á skjölum og kortum
Á sölu-, innkaupa og flutningsskjölum og á öllum kortum, **Nr.** hægt að fylla út sjálfkrafa með númeraröð eða handvirkt og hægt er að setja það upp svo það verði ósýnilegt.

**númer** reitinn má fylla út á þrjá vegu:

1. Ef aðeins ein númeraröð fyrir gerð skjals eða korts er til staðar þar sem gátreiturinn **Sjálfgefin nr.** er valinn og gátreiturinn **Handfærð nr.röð** er ekki valinn, þá er fyllt út í reitinn sjálfkrafa fyllt með næsta númeri í röðinni, og **Nr.** reiturinn verður ekki sýnilegur.

    > [!NOTE]  
    > Ef númeraröðin virkar ekki, til dæmis vegna þess að hún hefur númerin hafa klárast, þá **Nr.** reitur verður sýnilegur og þú getur handvirkt slegið inn númer eða leyst vandann á síðunni **Listi númeraraða**.

2. Ef fleiri en ein númeraröð fyrir gerð skjals eða korts eru fyrir hendi og gátreiturinn **Sjálfgefin nr.** er ekki valinn fyrir númeraröðina sem er verið að úthluta, þá **Nr.** reiturinn er sýnilegur og þú getur skoðað síðuna **Listi númeraraða** og valið númeraröðina sem þú vilt nota. Næsta númer í röðinni er síðan sett í **Nr.** .

3. Ef númeraröð hefur ekki verið sett upp fyrir gerð skjals eða korts, eða ef reiturinn **Handfærð nr.röð** er valinn fyrir númeraröðina, þá **Nr.** sýnilegur og slá verður inn númer handvirkt. Mest má rita 20 stafi, bæði tölustafi og bókstafi.

Þegar þú opnar nýtt skjal eða kort sem þar sem númeraröð er til staðar, þá opnast viðkomandi síða **Uppsetning númeraraðir** þannig að þú getir sett upp númeraröð fyrir þessa gerð skjals eða korts áður en þú heldur áfram með aðra gagnafærslu.

> [!NOTE]  
> Ef þú þarft að virkja handvirka númerun á til dæmis nýjum birgðaspjöldum sem hafa verið stofnuð með gagnaflutningsferli sem hefur falið **Nr.** sjálfgefið, þá er farið á síðuna **Uppsetning birgða** og valinn reiturinn **Vörunr.** til að opna og stilla tengda númeraröð á **Handfærð nr.röð**.

## <a name="to-create-a-new-number-series"></a>Til að búa til nýja númeraröð
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Númeraraðir** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð.
3. Fyllt er í reitina í nýju línunni. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-where-a-number-series-is-used"></a>Til að setja upp hvar númeraröð er notuð
Eftirfarandi málsmeðferð sýnir hvernig á að setja númeraröð fyrir sölustaðinn. Skrefin eru svipuð fyrir önnur svæði.
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sala og útistandandi** og veldu síðan tengda tengilinn.
2. Á síðunni **Sala**, í **Númeraröð**, veldu viðkomandi númeraröð fyrir hvert sölukort eða skjal.

Völdu númerið verður nú notað til að fylla út **Nr.** Sviði á viðkomandi korti eða skjali, í samræmi við þær stillingar sem þú gerðir á númeraröðinni.

## <a name="to-create-relationships-between-number-series"></a>Stofnun tengsla milli númeraraða
Ef settir hafa verið upp fleiri númeraraðakótar en einn fyrir sömu tegund grunnupplýsinga eða færslna er hægt að stofna tengsl milli kótanna. Með þessari aðgerð er auðvelt að velja á milli kóta þegar númer er notað.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Númeraraðir** og veldu síðan tengda tengilinn.
2. Velja skal línuna með númeraröðinni sem á að stofna tengsl við. og veljið síðan **Tengsl**.
3. Færður er inn í reitinn **Raðarkóti** kóti fyrir númeraröðina sem á að tengja við röðina sem valin var í 2. þrepi.
4. Bætt er við línu fyrir hvern kóta sem á að tengja völdum númeraröðum.
5. Lokaðu síðunni.

Þegar eitthvað er sett upp eftir þetta sem þarfnast númers er hægt að nota tengslin sem voru stofnuð til að velja úr skyldum númeraröðum.

## <a name="see-also"></a>Sjá einnig
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
