---
title: Bóka milli-fyrirtækjaskjöl og færslubækur
description: Þetta efnisatriði útskýrir hvernig á að nota millifyrirtækjaskjöl eða færslubækur til að bóka færslur með millifyrirtækjafélögum þínum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary, bank-to-bank'
ms.search.form: '600, 610'
ms.service: dynamics-365-business-central
---
# <a name="work-with-intercompany-documents-and-journals"></a>Unnið með samstæðuskjöl og færslubækur

Milli-fyrirtækjaskjöl eða færslubækur eru notuð til að bóka viðskipti við milli-fyrirtækjafélaga. Hægt er að bóka færslur á fjárhagsreikninga og ef bankareikningar milli fyrirtækja hafa verið settir upp er einnig hægt að bóka bankafærslur í banka. Nánari upplýsingar um uppsetningu bankareikninga milli fyrirtækja eru settir upp með því að [fara í Tilgreina bankareikninga sem nota á fyrir MF-félaga](intercompany-how-setup.md#specify-the-bank-accounts-to-use-for-intercompany-partners).  

Þegar MF-fylgiskjal eða færslubókarlína er bókuð í fyrirtækinu er samsvarandi fylgiskjal eða færslubókarlína stofnuð í MF-úthólfinu. Línan er flutt úr úthólfinu til félagans. Félaginn getur síðan bókað samsvarandi færslu í sínu fyrirtæki án þess að færa gögnin inn aftur.

Fyrir sölu- og innkaupaskjöl tryggir MF-félagakóti viðskiptamannsins eða lánardrottinsins að allar pantanir og reikningar fyrir viðskipti milli félaganna framleiði samsvarandi fylgiskjöl í samstarfsfyrirtækjunum. Reikningsskilin stemma rétt.

Hið sama á við um færslubókarlínur milli fyrirtækja. Þú þarft ekki að tilgreina reikninga, þú velur bara félagafyrirtækið. Samsvarandi færslubókarlínur milli fyrirtækja eru síðan stofnaðar í fyrirtæki félagans.

## <a name="fill-in-and-send-an-intercompany-sales-order"></a>Sölupöntun milli fyrirtækja er fyllt út og send

Hægt er að senda sölu- og innkaupapantanir og vöruskilapantanir áður en bókað er. Ekki er hægt að senda reikninga og kreditreikninga fyrr en þeir hafa verið bókaðir.

Eftirfarandi aðferð lýsir því hvernig eigi að fylla út og senda sölupöntun milli fyrirtækja. Sömu skref eiga við um sölu- og vöruskilapantanir millifyrirtækis, og bókaða millifyrirtækjareikninga og kreditreikninga.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Veljið **Nýtt** til að stofna nýja sölupöntun. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).  
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Gangið úr skugga um að viðskiptamaðurinn sé milli-fyrirtækjafélagi.
5. Til að senda sölupöntunina áður en hún er bókuð er valin aðgerðin **Senda MF-sölupöntun**.

> [!NOTE]
> Ef 5. þrep er gert fer sölupöntunin í MF-úthólfið þar sem hægt er að senda hana síðar. Nánari upplýsingar um MF-innhólfið og úthólfið fást með því að [fara í Stjórna MF-innhólfinu og úthólfinu](intercompany-how-manage-intercompany-inbox.md).

## <a name="fill-in-and-post-an-intercompany-journal"></a>Færa inn og bóka MF-færslubók

Þegar bókuð er almenn færslubókarlína í fyrirtækinu, er samsvarandi færslubókarlína stofunuð í MF-úthólfinu sem hægt er að flytja til félagans. Með útgáfubylgju 1 2022 er einnig hægt að setja fyrirtækið upp þannig að það stofni sjálfkrafa mótteknar færslur milli fyrirtækja sem félagar bókuðu í færslubækur milli fyrirtækja. Félaginn getur síðan bókað samsvarandi færslu í sínu fyrirtæki án þess að færa gögnin inn aftur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **MF-færslubækur** og velja síðan viðkomandi tengil.  
2. Færslubókarkeyrslan er opnuð. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).
3. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](../archive/invoicing/includes/tooltip-inline-tip_md.md)]
4. Í reitinn **MF félagi fjárhagsreikningur nr.** færið inn MF fjárhagsreikninginn sem upphæðin verður bókuð á í fyrirtæki félagans.

    > [!NOTE]
    > Þennan reit verður að fylla út í línu með bankareikningi eða fjárhagsreikningi annað hvort í reitnum **Reikningsnúmer** eða reitnum **Mótreikningsnúmer**.  
5. Valið er **Bóka** aðgerðin.

Færslurnar eru bókaðar í fyrirtækinu og færslubók með tilsvarandi færslum er stofnuð í MF-úthólfinu svo hægt sé að senda þær til fyrirtækis félagans.

## <a name="see-also"></a>Sjá einnig

[Vinna með millifyrirtækjafærslur](intercompany-manage.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
