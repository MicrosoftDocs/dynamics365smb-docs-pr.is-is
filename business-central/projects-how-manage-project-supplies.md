---
title: Unnið með verkbirgðir
description: Lýsir mismunandi leiðum til að stjórna framboði og innkaupum á efni og þjónustu vegna verkefna.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: 'project management, material, purchase'
ms.search.form: '98, 1020'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="manage-project-supplies"></a>Unnið með verkbirgðir

Stjórna ætti verkbirgðum af vörum, þjónustu og útgjöldum sem óaðskiljandi og mikilvægur þáttur í öllum verkefnum. Hægt er að nota birgðamagn eða búa til verktengd innkaup með innkaupapöntunum eða innkaupareikningum. Til dæmis krefst þjónustuverkefnis á tölvu nýjum diski. Búinn er til innkaupareikningur til kaupa á nýjum diski og verkefnið sem notar hann skráð.

Ef innkaupaferlið krefst þess ekki að efnislegu viðskiptin séu skráð sérstaklega er hægt að vinna innkaup á síðunni **Fjárhagsbók** verks. Nánari upplýsingar eru [í Til að bóka verktengdan kostnað](projects-how-manage-project-supplies.md#to-post-a-project-related-expense).

## <a name="to-purchase-items-or-services-for-a-project"></a>Til að kaupa vörur eða þjónustu fyrir verk

Eftirfarandi ferli sýnir hvernig á að nota innkaupareikning til að kaupa vörur fyrir verkefni. Sömu skref eiga við þegar innkaupapöntun er notuð.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningar** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).
3. Í reitnum **Verknr.** og **Verkhlutanr.**  verkseru valdar upplýsingar um verkefnið sem kaupa á vörur eða þjónustu fyrir. Nota skal sérstillingartólin ef reitur er ekki sýnilegur. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

    Gildið sem valið er í reitnum **Tegund** verklínu tilgreinir hvort áætlunarlína er stofnuð þegar notkun vörunnar er bókuð. Ef reikningshæft **er í reitnum** eru stofnaðar verkáætlunarlínur sem eru tilbúnar til reikningsfærslu á viðskiptavininn. Nánari upplýsingar eru í [Reikningsverk.](projects-how-invoice-jobs.md)
4. Valið er **Bóka** aðgerðin.

## <a name="to-view-the-value-of-purchases-for-a-project"></a>Til að skoða virði innkaupa fyrir verk

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.
2. Viðeigandi verkspjald er opnað.

    Á flýtiflipanum **Verkhlutar** sýnir reiturinn **Óafgreiddar pantanir** óafgreidda heildarupphæð, í staðarmynt, vara í birgðum og þjónustu á innkaupaskjölum fyrir verkhlutalínuna.  

    Reiturinn **Afh. upph. óreikn.færð** sýnir virði vara sem afhentra vara í innkaupaskjölum sem ekki hafa verið reikningsfærðar enn.  
3. Velja annan hvorn reitinn til að opna **síðuna Innkaupalínur** þar sem hægt er að fara yfir upplýsingar um tengdar innkaupaskjalslínur, þar á meðal hvaða vörur eða þjónusta eru móttekin.

## <a name="to-post-a-project-related-expense"></a>Til að bóka verktengdan kostnað

Ef um óeðlilegan eða einstakan verkkostnað er að ræða er hægt að nota **síðuna Fjárhagsbók** verks til að bóka þær beint á viðeigandi verkreikning.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **fjárhagsbækur verks** og velja síðan viðeigandi tengil.  
2. Ný lína er stofnuð og upplýsingar um kostnaðinn færðar inn, þ.m.t. upplýsingar í reitnum **Verknr.** og **Verkhlutanr** .  
3. Þegar færslubókin er tilbúin skal velja aðgerðina **Bóka**.

## <a name="see-also"></a>Sjá einnig .

[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
