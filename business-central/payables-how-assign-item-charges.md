---
title: Úthlutun kostnaðarauka á sölu og innkaup
description: 'Úthluta kostnaðarauka þegar þörf er á vörum í birgðum til að bera viðbót við kostnað, t.d. flutningskostnað og efnislega meðhöndlun.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'transportation, added cost, landed cost'
ms.search.form: '5709, 5800, 5805, 5814'
ms.date: 11/08/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Nota kostnaðarauka til að gera grein fyrir viðbótarviðskiptakostnaði

Til að tryggja rétt verðmat, verða birgðavörurnar þínar að bera allan auka kostnað, eind og t.d. farmur, efnisleg meðhöndlun, tryggingar og flutningar sem viðskipti þín með vörurnar hafa í för með sér. Í innkaupum samanstendur landaður kostnaður keyptrar vöru af innkaupaverði lánardrottins og öllum öðrum beinum kostnaðarauka sem hægt er að úthluta á einstakar móttökur eða endursendar afhendingar. Það getur verið fyrirtækjum jafnmikilvægt að kunna skil á kostnaði við afhendingu seldrar vöru eins og að vita raunkostnað aðkeyptrar vöru.

Auk þess að skrá aukinn kostnað í birgðavirði er hægt að nota kostnaðarauka fyrir eftirfarandi verkhluta:

* Til að ákvarða raunkostnað vöru og taka réttari ákvarðanir sem miða að því að bæta dreifikerfið.
* Til að sundurliða einingarkostnað og einingarverð vöru þegar framkvæmdar eru greiningar.
* Hafðu innkaupauppbætur með í einingarkostnaði og söluuppbætur í einingarverði.

Áður en hægt er að úthluta kostnaðarauka verður að setja upp númer kostnaðarauka fyrir mismunandi tegundir kostnaðarauka. Tölurnar innihalda hvaða fjárhagsreikninga á að bóka kostnað sem tengist sölu, innkaupum og birgðaleiðréttingum. Kostnaðaraukanúmer inniheldur samsetningu almennra vörubókunarflokka, skattflokkskóða, VSK-vörubókunarflokka og kostnaðarauka. Þegar kostnaðaraukanúmerið er fært inn á innkaupa- eða söluskjal er fjárhagsreikningurinn sóttur. Reikningurinn sem sóttur er er valinn á grundvelli uppsetningar kostnaðaraukanúmersins og upplýsinganna í skjalinu.

Hægt er að úthluta kostnaðarauka á bæði innkaupa- og söluskjöl á tvennan máta:

* Á fylgiskjalinu er listi yfir vörurnar sem kostnaðaraukinn tengist. Yfirleitt er þetta gert fyrir fylgiskjöl sem enn hafa ekki verið bókuð að fullu.
* Á sérstökum reikningi með því að tengja kostnaðaraukann við bókaða móttöku eða afhendingu þar sem vörurnar sem kostnaðaraukinn tengist eru birtar.

> [!NOTE]  
> Hægt er að úthluta kostnaðarauka á pantanir, reikninga og kreditreikninga fyrir bæði sölu og innkaup. Eftirfarandi ferli lýsir því hvernig á að vinna með kostnaðarauka fyrir innkaupareikning. Skrefin eru svipuð fyrir öll önnur innkaupa- og söluskjöl.

## Dæmi

Þetta myndband sýnir hvernig á að meðhöndla auka flutningskostnað sem hluta af birgðakostnaði.
<br><br>  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4b0SB?rel=0]

## Uppsetning kostnaðaraukanúmera

Númer kostnaðarauka eru notuð til að greina á milli mismunandi tegunda kostnaðarauka.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Kostnaðaraukar** og velja síðan viðkomandi tengil.
2. Á síðunni **Kostnaðarauki** skal velja aðgerðina **Nýtt** til að stofna nýja línu.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Að úthluta kostnaðarauka beint til innkaupareiknings fyrir vöruna

Ef kostnaðaraukinn er þekktur þegar innkaupareikningur er bókaður fyrir vöruna er þessari aðferð fylgt.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningar** og velja síðan viðkomandi tengil.
2. Stofna nýjan innkaupareikning. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).
3. Vertu viss um að innkaupareikningurinn hafi fleiri en eina línu af vörutegund.
4. Á nýja línu í reitnum **Tegund** er valinn **Kostnaðarauki Vöru**.
5. Í reitinn **Magn** eru færðar inn einingar kostnaðaraukans sem verið er að reikningsfæra fyrir.
6. Í reitinn **Beinn einingakostnaður** er upphæð kostnaðaraukans færð inn.
7. Fyllið inn í eftirstandandi reiti eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Gera skal eftirfarandi skref til að framkvæma sjálfa úthlutunina. Þar til kostnaðarauka hefur verið úthlutað að fullu, er gildið í **Magn til úthlutunar** reitnum skrifað með rauðu letri.
8. Á flýtiflipanum **Línur** skal velja aðgerðina **Úthlutun kostnaðarauka**.

    Síðan **Úthlutun kostnaðarauka** opnast og birtir eina línu fyrir hverja vörutegundarlínu á innkaupareikningnum. Til að úthluta kostnaðaraukanum á eina eða fleiri reikningslínur, er hægt að nota aðgerð sem úthlutar og dreifir honum fyrir þig, eða þú getur fyllt handvirkt út í reitinn **Magn til úthlutunar**. Eftirfarandi skref útskýra hvernig á að nota aðgerðina Leggja til úthlutun kostnaðarauka.

9. Á síðunni **Úthlutun kostnaðarauka** skal velja aðgerðina **Leggja til úthlutun kostnaðarauka**.
10. Ef það eru fleiri en ein vörutegundarlína í boði á reikningnum skal velja einn af fjórum dreifingarkostum.  

Ef kostnaðaraukanum er að fullu úthlutað er gildið í reitnum **Magn til úthlutunar** á innkaupareikningnum núll.

Nú er kostnaðarauka úthlutað til innkaupareiknings. Þegar þú bókar innhreyfingu á innkaupareikning, er birgðavirði vörunnar uppfært með kostnaði kostnaðaraukans.  

## Að úthluta kostnaðarauka frá öðrum reikningi til innkaupareiknings fyrir vöruna

Ef þú færð sendan reikning fyrir kostnaðaraukann eftir að þú bókaðir upphaflegu innkaupamóttökuna, skaltu fylgja þessu ferli.

1. Endurtakið skref 1 til 8 í [Að úthluta kostnaðarauka beint til innkaupareiknings fyrir vöruna](payables-how-assign-item-charges.md#to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item).
2. Á síðunni **Úthlutun kostnaðarauka** skal velja aðgerðina **Sækja móttökulínur**.
3. Á síðunni **Innkaupamóttökulínur** skal velja bókaða innkaupamóttöku fyrir vöruna sem þú vilt úthluta kostnaðaraukanum á, og veljið því næst hnappinn **Í lagi**.
4. Veljið aðgerðina **Leggja til úthlutun kostnaðarauka**.

Kostnaðaraukinn á þessum aðgreinda innkaupareikningi er nú úthlutað til vörunnar á bókuðu innkaupamóttökunni, og þar með uppfærist birgðagildi vörunnar með kostnaði kostnaðaraukans.

## Afgreiða kostnaðarauka fyrir hlutamóttökur

Könnum dæmi um hvernig á að meðhöndla kostnaðarauka fyrir hlutamóttöku.

Innkaupapöntun er með þremur línum:

* Tvær línur eru fyrir vörur.
* Ein lína safnar kostnaðarauka sem úthlutað er á vörur eftir upphæð.

Þegar vörurnar eru afhentar finnur notandi að eina af vörunum vantar og því er ekki hægt að merkja þá línu sem móttekna. Aðeins er hægt að taka á móti og bóka innkaupareikning fyrir seinni vöruna og eiga viðskipti við þá vöru sem vantar síðar.

Á síðunni Skipting **kostnaðarauka er fært inn** 0 **í** reitinn Magn til afgreiðslu **á línunni fyrir** vöruna sem vantar. Síðan er gildið afritað úr reitnum **Kostnaðaraukamagn til afgreiðslu** yfir í reitinn **Magn til reikningsf** . í innkaupapöntunarlínunum.

Þegar notandi er tilbúinn að afgreiða vöruna sem vantaði skal uppfæra reitinn **Magn til afgreiðslu** og bóka pöntunina.

## Sjá einnig .

[Stjórna skuldum](payables-manage-payables.md)  
[Skrá innkaup](purchasing-how-record-purchases.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
