---
title: "Hvernig á að: Búa til númeraröð | Microsoft Docs"
description: "Lærðu hvernig á að setja upp númeraröð sem úthlutar einstökum auðkenniskóðum til reikninga og skjala í Dynamics 365 for Financials."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 06/02/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7cc119c5879400adf63e468259a2c3a275b71cca
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-number-series"></a>Hvernig á að: Stofnun númeraraða
Fyrir hvert fyrirtæki sem þú setur upp þarftu að úthluta einstökum kennitölum við hluti eins og aðalbókarreikninga, viðskiptavinar- og seljanda, reikninga og önnur skjöl. Númeraröð er ekki aðeins mikilvæg fyrir auðkenningu. Vel unnið númerakerfi gerir einnig auðveldara að stýra og greina fyrirtækið og getur fækkað villum sem upp koma í gagnafærslu.

> [!NOTE]  
>   Við mælum með að þú notir sömu númeraraðakóða eins og þú sérð skráða í glugga **nr. Raðarlisti** í CRONUS sýningarfyrirtækinu. Codes eins og *P-INV +* gætu ekki skilað þér strax, en [!INCLUDE[d365fin](includes/d365fin_md.md)] hefur marga sjálfgefna stillingar sem eru háð þessum númeraröðakóðum.

Númerakerfi er stofnað með því að setja upp einn eða fleiri kóta fyrir hverja tegund aðalgagna eða skjala. Til dæmis má setja upp einn kóta fyrir númerun viðskiptamanna, annan kóta fyrir númerun sölureikninga og annan fyrir númerun skjala í almennri færslubók. Þegar kóti hefur verið settur upp verður að setja upp minnst eina númeraraðarlínu. Í númeraraðarlínunni eru upplýsingar líkt og fyrsta og síðasta talan í röðinni og upphafsdagsetningin. Hægt er að setja upp fleiri en eina númeraraðarlínu á hvern númeraraðarkóta með mismunandi upphafsdagsetningu fyrir hverja línu. Raðirnar verða notaðar hver á eftir annarri og hver röð hefst á tilgreindum upphafsdegi.

Þú setur venjulega upp númeraröðina þína til að setja inn næsta röð í röð á nýjum kortum eða skjölum sem þú býrð til. Þú getur hins vegar einnig stillt númeraröð til að leyfa þér að slá inn nýja númerið handvirkt. Þú tilgreinir þetta með **Handfærð númeraröð** gátreitnum.

Hægt er að nota fleiri en einn númeraraðarkóta fyrir hverja tegund frumgagna með því að nota númeraraðatengsl, til dæmis til að nota mismunandi númeraraðir fyrir mismunandi vöruflokka.

## <a name="to-create-a-new-number-series"></a>Til að búa til nýja númeraröð
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Númeraraðir** og velja svo viðeigandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Fyllt er í reitina í nýju línunni. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**Ábending**: Til að leyfa handvirkt færslu af númeri í nýjum kortum eða skjölum skaltu afvelja **Sjálfgefin númeraröð** gátreitinn og velja **Handvirk númeraröð** gátreitinn.

Nú þegar þú býrð til nýtt kort eða skjal sem er sett upp til að nota viðkomandi númeraröð, geturðu handvirkt fylgt **Nr.** reitur með hvaða gildi sem er.  

## <a name="to-set-up-where-a-number-series-is-used"></a>Til að setja upp hvar númeraröð er notuð
Eftirfarandi málsmeðferð sýnir hvernig á að setja númeraröð fyrir sölustaðinn. Skrefin eru svipuð fyrir önnur svæði.
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Sala & útistandandi** og velja svo viðeigandi tengil.
2. Í **Sala** glugganum, í **Númeraröð**, veldu viðkomandi númeraröð fyrir hvert sölukort eða skjal.

Völdu númerið verður nú notað til að fylla út **Nr.** Sviði á viðkomandi korti eða skjali, í samræmi við þær stillingar sem þú gerðir á númeraröðinni.

## <a name="to-create-relationships-between-number-series"></a>Stofnun tengsla milli númeraraða
Ef settir hafa verið upp fleiri númeraraðakótar en einn fyrir sömu tegund grunnupplýsinga eða færslna er hægt að stofna tengsl milli kótanna. Með þessari aðgerð er auðvelt að velja á milli kóta þegar númer er notað.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Númeraraðir** og velja svo viðeigandi tengil.
2. Velja skal línuna með númeraröðinni sem á að stofna tengsl við. og veljið síðan **Tengsl**.
3. Færður er inn í reitinn **Raðarkóti** kóti fyrir númeraröðina sem á að tengja við röðina sem valin var í 2. þrepi.
4. Bætt er við línu fyrir hvern kóta sem á að tengja völdum númeraröðum.
5. Glugganum er lokað.

Þegar eitthvað er sett upp eftir þetta sem þarfnast númers er hægt að nota tengslin sem voru stofnuð til að velja úr skyldum númeraröðum.

## <a name="see-also"></a>Sjá einnig
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

