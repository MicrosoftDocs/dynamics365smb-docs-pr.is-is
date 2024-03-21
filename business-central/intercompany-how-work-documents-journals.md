---
title: Bóka milli-fyrirtækjaskjöl og færslubækur
description: Þetta efnisatriði útskýrir hvernig á að nota millifyrirtækjaskjöl eða færslubækur til að bóka færslur með millifyrirtækjafélögum þínum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary, bank-to-bank'
ms.search.form: '600, 610'
ms.service: dynamics-365-business-central
---
# Unnið með samstæðuskjöl og færslubækur

Milli-fyrirtækjaskjöl eða færslubækur eru notuð til að bóka viðskipti við milli-fyrirtækjafélaga. Hægt er að bóka færslur á fjárhagsreikninga og ef settir hafa verið upp samstæðubankareikningar er einnig hægt að bóka færslur í banka. Til að fræðast meira um uppsetningu bankareikninga fyrirtækja er farið að  [Tilgreina bankareikninga til að nota fyrir samstæðufélaga](intercompany-how-setup.md#specify-the-bank-accounts-to-use-for-intercompany-partners).  

Þegar MF-fylgiskjal eða færslubókarlína er bókuð í fyrirtækinu er samsvarandi skjal eða færslubókarlína stofnað í MF-Úthólfinu. Línan er flutt úr Úthólfinu til félaganna. Félaginn getur síðan bókað samsvarandi færslu í sínu fyrirtæki án þess að færa gögnin inn aftur.

Fyrir sölu-og innkaupaskjöl tryggir MF-félagakótinn á viðskiptamanninum eða lánardrottninum að allar pantanir og reikningar vegna færslna á milli samstarfsaðila mynda samsvarandi skjöl í félagasamfyrirtækjunum. Reikningsskilastaðan rétt.

Það sama gildir um færslubókarlínur MF-samstæðu. Þú þarft ekki að tilgreina reikninga, þú bara velur samstarfsfyrirtækið. Samsvarandi færslubókarlínur innan samstæðu eru síðan stofnaðar í félagasamfélaginu.

## Fylla út og senda samstæðusölupöntun

Hægt er að senda sölu- og innkaupapantanir og vöruskilapantanir áður en bókað er. Ekki er hægt að senda reikninga og kreditreikninga fyrr en þeir eru bókaðir.

Eftirfarandi aðferð lýsir því hvernig eigi að fylla út og senda sölupöntun milli fyrirtækja. Sömu skref eiga við um sölu- og vöruskilapantanir millifyrirtækis, og bókaða millifyrirtækjareikninga og kreditreikninga.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Veljið **Nýtt** til að stofna nýja sölupöntun. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).  
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Gangið úr skugga um að viðskiptamaðurinn sé milli-fyrirtækjafélagi.
5. Til að senda sölupöntunina áður en hún er bókuð er valin aðgerðin **Senda MF-sölupöntun**.

> [!NOTE]
> Ef það er gert í skrefi 5 fer sölupöntunin í MF-Úthólf þar sem hægt er að senda hana síðar. Til að fræðast meira um MF-Innhólf og Úthólf er farið að  [stjórna MF-innhólfinu og Úthólfinu](intercompany-how-manage-intercompany-inbox.md).

## Færa inn og bóka samstæðufærslubók

Þegar bókuð er almenn færslubókarlína í fyrirtækinu, er samsvarandi færslubókarlína stofunuð í MF-úthólfinu sem hægt er að flytja til félagans. Með 2022 sleppingu bylgju 1 er einnig hægt að setja fyrirtækið upp til að stofna færslur sjálfkrafa mótteknar MF-félaga sem eru bókaðar í MF-færslubók. Félaginn getur síðan bókað samsvarandi færslu í sínu fyrirtæki án þess að færa gögnin inn aftur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-færslubækur** og velja síðan viðkomandi tengil.  
2. Opnið bókarkeyrsluna. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).
3. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](../archive/invoicing/includes/tooltip-inline-tip_md.md)]
4. Í reitinn **MF félagi fjárhagsreikningur nr.** færið inn MF fjárhagsreikninginn sem upphæðin verður bókuð á í fyrirtæki félagans.

    > [!NOTE]
    > Þennan reit verður að fylla út í línu með bankareikningi eða fjárhagsreikningi annað hvort í reitnum **Reikningsnúmer** eða reitnum **Mótreikningsnúmer**.  
5. Valið er **Bóka** aðgerðin.

Færslurnar eru bókaðar í fyrirtæki notanda og færslubók með samsvarandi færslur eru stofnaðar í MF-úthólfinu svo hægt sé að senda þær til félagasamfélagsins.

## Sjá einnig

[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]