---
title: Úthlutun kostnaðarauka á sölu og innkaup (inniheldur myndskeið)
description: 'Úthluta vörugjöldum þegar þú þarft birgðavörur til að bera aukinn kostnað, svo sem vöruflutninga og líkamlega meðhöndlun.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'transportation, added cost, landed cost'
ms.search.form: '5709, 5800, 5805, 5814'
ms.date: 11/08/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Notaðu vörugjöld til að gera grein fyrir auka viðskiptakostnaði

Til að tryggja rétt verðmat, verða birgðavörurnar þínar að bera allan auka kostnað, eind og t.d. farmur, efnisleg meðhöndlun, tryggingar og flutningar sem viðskipti þín með vörurnar hafa í för með sér. Fyrir innkaup samanstendur landaði kostnaður keyptrar vöru af innkaupaverði lánardrottins og öllum öðrum beinum vörugjöldum sem hægt er að úthluta á einstakar móttökur eða skilasendingar. Það getur verið fyrirtækjum jafnmikilvægt að kunna skil á kostnaði við afhendingu seldrar vöru eins og að vita raunkostnað aðkeyptrar vöru.

Auk þess að skrá kostnaðarauka í birgðaverðmæti geturðu notað vörugjöld fyrir eftirfarandi verkefni:

* Til að ákvarða raunkostnað vöru og taka réttari ákvarðanir sem miða að því að bæta dreifikerfið.
* Til að sundurliða einingarkostnað og einingarverð vöru þegar framkvæmdar eru greiningar.
* Hafðu innkaupauppbætur með í einingarkostnaði og söluuppbætur í einingarverði.

Áður en hægt er að úthluta vörugjöldum verður að setja upp vörugjaldanúmer fyrir mismunandi tegundir vörugjalda. Tölurnar innihalda á hvaða bókhaldsreikninga á að bóka kostnað sem tengist sölu, innkaupum og birgðaleiðréttingum. Kostnaðaraukanúmer inniheldur samsetningu almennra vörubókunarflokka, skattflokkskóða, VSK-vörubókunarflokka og kostnaðarauka. Þegar þú slærð inn gjaldfærslunúmer vöru á innkaupa- eða söluskjali er bókhaldsreikningurinn sóttur. Reikningurinn sem sóttur er er valinn út frá uppsetningu vörugjaldsnúmers og upplýsingum á skjalinu.

Hægt er að úthluta kostnaðarauka á bæði innkaupa- og söluskjöl á tvennan máta:

* Á skjalinu sem sýnir atriðin sem vörugjaldið tengist. Venjulega gerirðu þetta fyrir skjöl sem hafa ekki enn verið birt að fullu.
* Á sérstakan reikning með því að tengja vörugjaldið við bókaða móttöku eða sendingu þar sem vörurnar sem vörugjaldið tengist eru skráðar.

> [!NOTE]  
> Hægt er að úthluta kostnaðarauka á pantanir, reikninga og kreditreikninga fyrir bæði sölu og innkaup. Eftirfarandi ferli lýsir því hvernig á að vinna með kostnaðarauka fyrir innkaupareikning. Skrefin eru svipuð fyrir öll önnur innkaupa- og söluskjöl.

## Dæmi

Þetta myndband sýnir hvernig á að meðhöndla auka sendingarkostnað sem hluta af birgðakostnaði.
<br><br>  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4b0SB?rel=0]

## Uppsetning kostnaðaraukanúmera

Þú notar vörugjaldanúmer til að greina á milli mismunandi tegunda vörugjalda.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Kostnaðaraukar** og velja síðan viðkomandi tengil.
2. Á síðunni **Kostnaðarauki** skal velja aðgerðina **Nýtt** til að stofna nýja línu.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Að úthluta kostnaðarauka beint til innkaupareiknings fyrir vöruna

Ef þú veist vörugjaldið þegar þú bókar innkaupareikning fyrir vöruna skaltu fylgja þessari aðferð.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningar** og velja síðan viðkomandi tengil.
2. Stofna nýjan innkaupareikning. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).
3. Vertu viss um að innkaupareikningurinn hafi fleiri en eina línu af vörutegund.
4. Á nýja línu í reitnum **Tegund** er valinn **Kostnaðarauki Vöru**.
5. Í reitnum **Magn**  skaltu slá inn einingar vörugjaldsins sem þú ert reikningsfærður fyrir.
6. Í reitinn **Beinn einingakostnaður** er upphæð kostnaðaraukans færð inn.
7. Fyllið inn í eftirstandandi reiti eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Gerðu eftirfarandi skref til að framkvæma raunverulegt verkefni. Þar til kostnaðarauka hefur verið úthlutað að fullu, er gildið í **Magn til úthlutunar** reitnum skrifað með rauðu letri.
8. Á flýtiflipanum **Línur** skal velja aðgerðina **Úthlutun kostnaðarauka**.

    Síðan **Úthlutun kostnaðarauka** opnast og birtir eina línu fyrir hverja vörutegundarlínu á innkaupareikningnum. Til að úthluta kostnaðaraukanum á eina eða fleiri reikningslínur, er hægt að nota aðgerð sem úthlutar og dreifir honum fyrir þig, eða þú getur fyllt handvirkt út í reitinn **Magn til úthlutunar**. Eftirfarandi skref útskýra hvernig á að nota aðgerðina Leggja til úthlutun kostnaðarauka.

9. Á síðunni **Úthlutun kostnaðarauka** skal velja aðgerðina **Leggja til úthlutun kostnaðarauka**.
10. Ef það eru fleiri en ein vörutegundarlína í boði á reikningnum skal velja einn af fjórum dreifingarkostum.  

Ef vörugjaldið er að fullu úthlutað er gildið í **Magn. að Úthluta** reitnum á innkaupareikningnum er núll.

Nú er kostnaðarauka úthlutað til innkaupareiknings. Þegar þú bókar innhreyfingu á innkaupareikning, er birgðavirði vörunnar uppfært með kostnaði kostnaðaraukans.  

## Að úthluta kostnaðarauka frá öðrum reikningi til innkaupareiknings fyrir vöruna

Ef þú færð sendan reikning fyrir kostnaðaraukann eftir að þú bókaðir upphaflegu innkaupamóttökuna, skaltu fylgja þessu ferli.

1. Endurtakið skref 1 til 8 í [Að úthluta kostnaðarauka beint til innkaupareiknings fyrir vöruna](payables-how-assign-item-charges.md#to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item).
2. Á síðunni **Úthlutun kostnaðarauka** skal velja aðgerðina **Sækja móttökulínur**.
3. Á síðunni **Innkaupamóttökulínur** skal velja bókaða innkaupamóttöku fyrir vöruna sem þú vilt úthluta kostnaðaraukanum á, og veljið því næst hnappinn **Í lagi**.
4. Veljið aðgerðina **Leggja til úthlutun kostnaðarauka**.

Kostnaðaraukinn á þessum aðgreinda innkaupareikningi er nú úthlutað til vörunnar á bókuðu innkaupamóttökunni, og þar með uppfærist birgðagildi vörunnar með kostnaði kostnaðaraukans.

## Meðhöndla vörugjöld fyrir hlutakvittanir

Við skulum kanna dæmi um hvernig á að meðhöndla vörugjöld fyrir móttöku að hluta.

Þú ert með innkaupapöntun með þremur línum:

* Tvær línur eru fyrir hluti.
* Ein lína tekur við vörugjöldum sem skipt er yfir vörurnar eftir upphæð.

Þegar vörurnar eru afhentar finnurðu að einn af hlutunum vantar, svo þú getur ekki merkt línuna sem móttekna. Þú getur aðeins tekið við og bókað innkaupareikninginn fyrir seinni hlutinn og meðhöndlað þá vöru sem vantar síðar.

Til að meðhöndla vörukostnaðinn fyrir hlutakvittunina skaltu slá inn **0** í  **úthlutun vörugjalds**  **Magn til að meðhöndla** reitinn á línunni fyrir hlutinn sem vantar. Afritaðu síðan gildið úr **Hlutagjaldsmagninu. til að meðhöndla** reitinn í reitinn **Magn til reiknings**  á innkaupapöntunarlínunum.

Þegar þú ert tilbúinn til að meðhöndla hlutinn sem vantaði skaltu uppfæra  **Magn til að meðhöndla** reitinn og bóka pöntunina.

## Sjá einnig .

[Stjórna skuldum](payables-manage-payables.md)  
[Skrá innkaup](purchasing-how-record-purchases.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
