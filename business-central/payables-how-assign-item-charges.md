---
title: Úthluta kostnaðarauka á sölu og innkaup (inniheldur Video)
description: Úthlutaðu kostnaðarauka þegar þú þarft að setja aukinn kostnað á birgðavörur, t.d. flutningskostnað og kostnað vegna meðhöndlunar, sem kemur upp þegar vörur eru keyptar eða seldar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: transportation, added cost, landed cost
ms.search.form: 5709, 5800, 5805, 5814
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 6cfebffb12eb2cd7ffa84e12a07c01968c429069
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8145603"
---
# <a name="use-item-charges-to-account-for-additional-trade-costs"></a>Nota kostnaðarauka til að gera grein fyrir viðbótar viðskiptakostnaði
Til að tryggja rétt verðmat, verða birgðavörurnar þínar að bera allan auka kostnað, eind og t.d. farmur, efnisleg meðhöndlun, tryggingar og flutningar sem viðskipti þín með vörurnar hafa í för með sér. Í innkaupum, þá samanstendur raunkostnaður innkeyptrar vöru af innkaupaverði frá lánardrottni og öllu beinu viðbótarvörugjaldi sem hægt er að leggja á einstaka móttöku eða endursendar afhendingar. Það getur verið fyrirtækjum jafnmikilvægt að kunna skil á kostnaði við afhendingu seldrar vöru eins og að vita raunkostnað aðkeyptrar vöru.

Til viðbótar við skráningu aukakostnaðar á birgðavirði, geturðu notað eiginleikann Kostnaðarauki fyrir eftirfarandi:

- Til að ákvarða raunkostnað vöru og taka réttari ákvarðanir sem miða að því að bæta dreifikerfið.
- Til að sundurliða einingarkostnað og einingarverð vöru þegar framkvæmdar eru greiningar.
- Hafðu innkaupauppbætur með í einingarkostnaði og söluuppbætur í einingarverði.

Áður en þú getur úthlutað kostnaðarauka, þarf að setja upp kostnaðaraukanúmer fyrir ólíkar gerðir kostnaðarauka, og líka tiltaka á hvaða fjárhagsreikninga skal bóka kostnað sem hlýst af sölu, innkaupum og leiðréttingu birgða.  Kostnaðaraukanúmer inniheldur samsetningu almennra vörubókunarflokka, skattflokkskóða, VSK-vörubókunarflokka og kostnaðarauka. Þegar þetta kostnaðaraukanúmer er fært inn í innkaupa- eða söluskjal sækir kerfið fjárhagsreikning eftir uppsetningu kostnaðaraukanúmersins og upplýsingunum í viðkomandi skjali.

Hægt er að úthluta kostnaðarauka á bæði innkaupa- og söluskjöl á tvennan máta:
- Á skjalinu þar sem vörurnar sem kostnaðurinn tengist eru birtar. Þetta er vanalega gert við skjöl sem ekki eru enn fullbókuð.
- Á sérstakan reikning með því að tengja kostnaðaraukann við bókaða móttöku eða afhendingu, þar sem vörurnar sem kostnaðaraukinn tengist eru skráðar.

> [!NOTE]  
>   Hægt er að úthluta kostnaðarauka á pantanir, reikninga og kreditreikninga fyrir bæði sölu og innkaup. Eftirfarandi ferli lýsir því hvernig á að vinna með kostnaðarauka fyrir innkaupareikning. Skrefin eru svipuð fyrir öll önnur innkaupa- og söluskjöl.

## <a name="example"></a>Dæmi
Þetta myndband sýnir hvernig á að meðhöndla viðbótarkostnað afhendingar sem hluta af birgðakostnaði.
<br><br>  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4b0SB?rel=0]

## <a name="to-set-up-item-charge-numbers"></a>Uppsetning kostnaðaraukanúmera
Vörugjaldsnúmer eru notuð til að greina á milli mismunandi vörugjalda sem notuð eru fyrir innkaupaskjöl í fyrirtækinu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Kostnaðaraukar** og velja síðan viðkomandi tengil.
2. Á síðunni **Kostnaðarauki** skal velja aðgerðina **Nýtt** til að stofna nýja línu.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item"></a>Að úthluta kostnaðarauka beint til innkaupareiknings fyrir vöruna
Ef þú veist hver kostnaðaraukinn er þegar þú bókar innkaupareikning fyrir vöruna, skaltu fylgja þessu ferli.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningar** og velja síðan viðkomandi tengil.
2. Stofna nýjan innkaupareikning. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).
3. Vertu viss um að innkaupareikningurinn hafi fleiri en eina línu af vörutegund.
4. Á nýja línu í reitnum **Tegund** er valinn **Kostnaðarauki Vöru**.
5. Í reitinn **Magn** er færður inn fjöldi eininga þess kostnaðarauka sem hefur verið reikningsfærður.
6. Í reitinn **Beinn einingakostnaður** er upphæð kostnaðaraukans færð inn.
7. Fyllið inn í eftirstandandi reiti eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Í eftirfarandi skrefum, muntu framkvæma hina raunverulegu úthlutun. Þar til kostnaðarauka hefur verið úthlutað að fullu, er gildið í **Magn til úthlutunar** reitnum skrifað með rauðu letri.
8. Á flýtiflipanum **Línur** skal velja aðgerðina **Úthlutun kostnaðarauka**.

    Síðan **Úthlutun kostnaðarauka** opnast og birtir eina línu fyrir hverja vörutegundarlínu á innkaupareikningnum. Til að úthluta kostnaðaraukanum á eina eða fleiri reikningslínur, er hægt að nota aðgerð sem úthlutar og dreifir honum fyrir þig, eða þú getur fyllt handvirkt út í reitinn **Magn til úthlutunar**. Eftirfarandi skref útskýra hvernig á að nota aðgerðina Leggja til úthlutun kostnaðarauka.

9. Á síðunni **Úthlutun kostnaðarauka** skal velja aðgerðina **Leggja til úthlutun kostnaðarauka**.
10. Ef það eru fleiri en ein vörutegundarlína í boði á reikningnum skal velja einn af fjórum dreifingarkostum.  

Ef kostnaðarauka hefur verið úthlutað að fullu, er gildið í **Magn til úthlutunar** reitnum á innkaupareikningnum núll.

Nú er kostnaðarauka úthlutað til innkaupareiknings. Þegar þú bókar innhreyfingu á innkaupareikning, er birgðavirði vörunnar uppfært með kostnaði kostnaðaraukans.  

## <a name="to-assign-an-item-charge-from-a-separate-invoice-to-the-purchase-invoice-for-the-item"></a>Að úthluta kostnaðarauka frá öðrum reikningi til innkaupareiknings fyrir vöruna
Ef þú færð sendan reikning fyrir kostnaðaraukann eftir að þú bókaðir upphaflegu innkaupamóttökuna, skaltu fylgja þessu ferli.
1. Endurtakið skref 1 til 8 í [Að úthluta kostnaðarauka beint til innkaupareiknings fyrir vöruna](payables-how-assign-item-charges.md#to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item).
2. Á síðunni **Úthlutun kostnaðarauka** skal velja aðgerðina **Sækja móttökulínur**.
3. Á síðunni **Innkaupamóttökulínur** skal velja bókaða innkaupamóttöku fyrir vöruna sem þú vilt úthluta kostnaðaraukanum á, og veljið því næst hnappinn **Í lagi**.
4. Veljið aðgerðina **Leggja til úthlutun kostnaðarauka**.

Kostnaðaraukinn á þessum aðgreinda innkaupareikningi er nú úthlutað til vörunnar á bókuðu innkaupamóttökunni, og þar með uppfærist birgðagildi vörunnar með kostnaði kostnaðaraukans.

## <a name="see-also"></a>Sjá einnig
[Stjórna skuldum](payables-manage-payables.md)  
[Skrá innkaup](purchasing-how-record-purchases.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]