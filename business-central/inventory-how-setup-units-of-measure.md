---
title: Hvernig á að setja upp mælieiningar | Microsoft Docs
description: Hægt er að setja upp margar mælieiningar fyrir vöru þannig að hægt sé að úthluta mælieiningum á vöruna.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-units-of-measure"></a><a name="set-up-units-of-measure"></a><a name="set-up-units-of-measure"></a>Setja upp mælieiningar

Sem hluti af uppsetningu á [!INCLUDE [prod_short](includes/prod_short.md)] er hægt að setja upp almennar mælieiningar á síðunni **Mælieiningar**. Síðan þegar þú skráir nýjar vörur tilgreinir þú grunnmælieininguna á **Birgðaspjaldinu**. Einnig er hægt að bæta við mælieiningum síðar.  

Hægt er að setja upp margar mælieiningar fyrir vöru þannig að hægt sé að úthluta mælieiningum til vörunnar í eftirfarandi tilgangi:

- Úthluta grunnmælieiningu á birgðaspjaldi vörunnar til skilgreiningar á því hvernig hún er geymd í birgðum og þjónar sem umbreytigrundvöllur fyrir aðrar mælieiningar.
- Úthluta öðrum mælieiningum til innkaupa, framleiðslu eða söluskjala til skilgreiningar á hversu margar einingar af grunnmælieiningunum eru afgreiddar á sama tíma í ferlinu. Til dæmis er varan hugsanlega keypt á brettum en er notuð í stykkjatali við framleiðslu.

Ef vara er sett á lager eftir einni mælieiningu en framleidd eftir annarri er framleiðslupöntun stofnuð sem notar mælieiningu framleiðslukeyrslu til að reikna út rétt magn íhluta meðan á keyrslunni **Endurnýjun framleiðslupöntunar** stendur. Dæmi um útreikning með mælieiningu framleiðslukeyrslu er þegar framleiddur hlutur er merktur á lager í stykkjum en framleiddur í tonnum. Frekari upplýsingar eru í [Vinna með mælieiningu framleiðslukeyrslu](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).  

Annað verkfæri sem auðveldar vinnu með margar mælieiningar fyrir vörur er getan til að tilgreina sléttunarnákvæmni fyrir grunnmælieiningar. Með því að tilgreina sléttunarnákvæmni eru upplýsingar gefnar upp um hvað eigi að slá inn fyrir uppgefið viðskiptaferli og dregur úr vandamálum varðandi sléttun. Þegar notaðar eru aðrar mælieiningar hjálpar gildið í reitnum **Magn á mælieiningu** að reikna út magnið í grunnmælieiningunni sem getur leitt til vandamála varðandi sléttun. Ímyndaðu þér til dæmis að þú sért að fá einn kassa sem inniheldur sex hluti. Þegar kassinn kemur í vöruhúsið uppgötvarðu að einn af hlutunum sex er týndur. Þú ákveður að bóka ekki móttöku á einu kassa heldur breytir í staðinn mótteknu magni úr fimm af sex stykkjum. Það myndi leiða til móttöku á 4,99998 stykkjum, frekar en fimm. Á síðunni **Mælieiningar vöru** gerir reiturinn **Sléttunarnákvæmni magns** þér kleift að tilgreina gildi sem mun umbreyta magninu í tölu sem er auðveldara að skilja. Ef við höldum áfram með dæmið myndum við slá inn **1** í reitinn til að slétta upp í nákvæmlega fimm stykki.

## <a name="to-set-up-units-of-measure"></a><a name="to-set-up-units-of-measure"></a><a name="to-set-up-units-of-measure"></a>Til að setja upp mælieiningarkóða

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Mælieiningar** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**. Ný auð lína er sett inn.  
3. Reitirnir eru fylltir út. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
4. Ef þú veist að fyrirtækið þitt ætlar að selja vörur með þessari mælieiningu til viðskiptavina í öðrum löndum er hægt að bæta við þýðingum.  
    1. Velja þarf tungumálakóðann sem setja á upp þýðingar fyrir og svo aðgerðina **Þýðingar**.
    2. Í reitnum **Tungumálskóti** er felliörin valin til að skoða lista yfir tiltæka tungumálakóta. Valinn er sá tungumálskóti sem setja á inn þýðingu fyrir og síðan er smellt á Í lagi til að afrita kótann í reitinn.
    3. Í reitinn **Lýsing** er færður inn viðeigandi texti.
5. Endurtakið fyrri skref fyrir allar aðrar mælieiningar sem þú vilt bæta við.  

Þegar þú skráir nýja vöru getu þú valið grunnmælieiningu af listanum yfir mælieiningar sem þú hefur nú sett upp. Einnig er hægt að setja upp margar mælieiningar fyrir vöru.  

## <a name="to-set-up-multiple-item-units-of-measure"></a><a name="to-set-up-multiple-item-units-of-measure"></a><a name="to-set-up-multiple-item-units-of-measure"></a>Hvernig á að setja upp margar mælieiningar vara

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.
2. Opna spjald vörunnar sem á að setja upp aðra mælieiningu fyrir.
3. Veldu **Mælieining**. Síðan **Mælieiningar vöru** opnast.
4. Ef reiturinn **Grunneining mælingareits** á birgðaspjaldinu er fylltur út, hefur sú mælieining þegar verið sett upp.
5. Valið er **Nýtt** aðgerð. Ný auð lína er sett inn.
6. Í reitnum **Kóði**, setjið inn heiti mælieiningarinnar. Að öðrum kosti skal velja reitinn til að velja úr mælieiningarkóðum í gagnagrunninum.
7. Í reitnum **Magn á mælieiningu**, tilgreinið hversu margar grunnmælieiningar varan inniheldur.
8. Einnig er hægt að tilgreina nákvæmlega upplýsingar um stærð einnar mælingar á svæðunum **Hæð**, **Breidd**, **Lengd** og **Þyngd**, þannig að [!INCLUDE [prod_short](includes/prod_short.md)] geti reiknað út hversu margar einingar er hægt að setja í hvert hólf. Svæðið **Rúmmál** er reiknað sjálfkrafa út frá **Hæð**, **Breidd** og **Lengd**.

    Ef einhver þessara svæða innihalda annað gildi en 0, þá er slík mælieining notuð við öll ferli sem fela í sér að setja vörur í hólf: Frágangur, hreyfingar, kvittanir, afhendingar, tiltekt og leiðréttingar. [!INCLUDE [prod_short](includes/prod_short.md)] ber samtölu hverrar mælieiningar varanna sem gengið er frá og varanna sem þegar eru í hólfinu saman við hámarksstærðina eða aðra mælieiningu sem kemst í hólfið samkvæmt hólfagetureglunni sem valin var á birgðaspjaldinu fyrir þessa vöru. Með öðrum orðum verður að nota sömu mælieininguna í hverri vídd fyrir allar mælieiningar vara - nota kílógrömm eða pund fyrir þyngd, til dæmis, en gæta verður samræmis.
9. Eindurtakið skref 5 til 7 til að setja upp allar aðrar mælieiningar sem nota á í mismunandi ferlum fyrir þessa vöru.

    Á svæðinu **Grunnmælieining** neðst í glugganum, er hægt að skoða eða breyta grunnmælieiningu vörunnar. Einnig er hægt að breyta grunnmælieiningunni í reitnum **Grunnmælieining** á birgðaspjaldinu. Á síðunni **Mælieiningar vöru** verður grunnmælieiningin að hafa gildið **1** í svæðinu **Magn á mælieiningu**.

Nú er hægt að nota aðrar mælieiningar í innkaupa-, framleiðslu- og söluskjölum. Frekari upplýsingar eru í [Færa inn sjálfgefna mælieiningarkóða fyrir sölu- og innkaupafærslur](#to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions).  

## <a name="to-set-up-unit-of-measure-translations"></a><a name="to-set-up-unit-of-measure-translations"></a><a name="to-set-up-unit-of-measure-translations"></a>Setja upp mælieiningatexta

Þegar selt er til erlendra viðskiptavina er hægt að tilgreina mælieininguna á viðeigandi tungumáli. Það getur þú gert með því að tilgreina umreikninga fyrir mælieiningar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Mælieiningar** og velja síðan viðkomandi tengil.
2. Velja þarf tungumálakóðann sem setja á upp þýðingar fyrir og svo aðgerðina **Þýðingar**.
3. Í reitnum **Tungumálskóti** er felliörin valin til að skoða lista yfir tiltæka tungumálakóta. Valinn er sá tungumálskóti sem setja á inn þýðingu fyrir og síðan er smellt á Í lagi til að afrita kótann í reitinn.
4. Í reitinn **Lýsing** er færður inn viðeigandi texti.
5. Skref 2 til 4 eru endurtekin fyrir þá mælieiningarkóða og tungumál sem setja á inn þýðingar á.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a><a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a><a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Færa inn sjálfgefna mælieiningarkóða fyrir sölu- og innkaupafærslur

Ef venjulega er keypt eða selt í einingum sem eru aðrar en grunnmælieiningin er hægt að tilgreina sérstakar mælieiningar fyrir innkaup og sölu. Ef gera á þetta verða mælieiningar að vera uppsettar á síðunni **Mælieiningar vöru**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.
2. Opna viðeigandi birgðaspjaldi þar sem á að tilgreina sjálfgefinn mælieiningarkóða fyrir sölu- eða innkaupaeiningu.
3. Fyrir sölu, á flýtiflipanum **Reikningsfærsla**, í reitnum **Sölumælieining** er síðan **Mælieiningar vöru** opnuð.
4. Fyrir innkaup, á flýtiflipanum **Áfylling**, í reitnum **Innkaupamælieining** er síðan **Mælieiningar vöru** opnuð.
5. Velja skal kóðann sem setja á upp sem sjálfgefna mælieiningu fyrir sölu eða innkaup og veljið svo hnappinn **Í lagi**.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/trade-master-data-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Vinna með mælieiningu framleiðslukeyrslu](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Stjórnun birgða](inventory-manage-inventory.md)  
[Stjórnun innkaupa](purchasing-manage-purchasing.md)  
[Stjórna sölu](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
