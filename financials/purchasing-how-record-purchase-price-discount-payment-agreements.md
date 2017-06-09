---
title: "Hvernig á að: Skráðu sérstakt kaupverð og afslætti| Microsoft Docs"
description: "Hvernig á að: Skrá söluverð og afslætti"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 67625231d62a72bb0a62ab362bce92aa16b8956e
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-record-special-purchase-prices-and-discounts"></a>Hvernig á að: Skrá sérstakt söluverð og sérstaka afslætti
Skilgreina verður mismunandi verð- og afsláttarsamninga sem gilda þegar vörur eru keyptar frá mismunandi lánardrottnum svo að þeim reglum og gildum sem samkomulag hefur náðst um sé beitt á innkaupaskjöl sem gerð eru fyrir lánardrottininn.

Þegar notandi hefur skráð sérstakt verð og línuafslætti vegna sölu eða innkaupa tryggir [!INCLUDE[d365fin](includes/d365fin_md.md)] að hagnaður notanda af viðskiptum með vöru sé alltaf hámarkaður með því að reikna sjálfkrafa besta verð á sölu- og innkaupaskjölum og á færslubókarlínum fyrir verk og vörur. Nánari upplýsingar er að finna í [Ítarlegt: Útreikningur besta verðs](advanced-best-price-calculation.md).

Hvað varðar verð, er hægt að hafa sérstakt söluverð í sölulínunum ef tiltekin samsetning á viðskiptamanni, vöru, lágmarksmagni, mælieiningu, eða upphafs-/ lokadagsetningu er til staðar.

Hvað varðar afslátt, er hægt að setja upp og nota tvær tegundir innkaupaafsláttar:

| Afsláttargerð | Lýsing |
| --- | --- |
| **Innkaupalínuafsláttur** |Afsláttarupphæð sem er sett inn í sölulínur ef tiltekin samsetning á lánardrottni, vöru, lágmarksmagni, mælieiningu, eða upphafs-/ lokadagsetningu er til staðar. Þetta virkar á sama háttog fyrir innkaupsverð. |
| **Reikningsafsláttur** |Hlutfallsafsláttur sem er dreginn frá heildarupphæð skjalsins ef upphæðin í öllum línum í söluskjali fer fram yfir ákveðið lágmark. |

Vegna þess að innkaupalínuafslættir og innkaupaverð byggjast á samsetningu vöru og lánardrottins er einnig hægt að færa þessa grunnstillingu inn af birgðaspjaldinu, þar sem reglurnar og gildin eru skilgreind. Nánari upplýsingar eru í [Hvernig á að: Skrá nýjar vörur](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Að setja upp sérstakt innkaupsverð fyrir lánardrottin
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Lánardrottnar** og velja síðan viðeigandi tengil.
2. Opna skal viðeigandi lánardrottnaspjald og velja síðan aðgerðina **Verð**.

    Reiturinn **Tegund innkaupa** er fylltur út fyrirfram með **Lánardrottinn**og í reitnum **Innkaupakóði**er númer lánardrottins.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Fyllt er út lína fyrir hverja samsetningu sem lánardrottinn veitir innkaupalínuafsláttur fyrir.

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Að setja upp línuafslátt fyrir lánardrottin
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Lánardrottnar** og velja síðan viðeigandi tengil.
2. Opna skal viðeigandi lánardrottinsspjald og veljið síðan aðgerðina **Línuafslættir**.

    Reiturinn **Tegund innkaupa** er fylltur út fyrirfram með **Lánardrottinn**og í reitnum **Innkaupakóði**er númer lánardrottins.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Fyllt er út lína fyrir hverja samsetningu sem lánardrottinn veitir innkaupalínuafsláttur fyrir.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Að setja upp reikningsafslátt fyrir lánardrottin
Þegar lánardrottnar þínir hafa veitt þér upplýsingar um hvaða reikningsafslætti þeir veita eru færðir inn reikningsafsláttarkóðar á lánardrottnaspjöldin og sett upp skilyrði fyrir hvern kóða.

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Lánardrottnar** og velja síðan viðeigandi tengil.
2. Opna skal spjald lánardrottins sem getur veitt reikningsafslátt.
3. Í reitnum **Reikningsafsláttarkóði** er valinn kóði fyrir viðeigandi reikningsafsláttarskilmála sem forritið notar til að reikna reikningsafslátt fyrir lánardrottin.

    **Athugasemd**: Fyrirliggjandi lánardrottnaspjöld standa fyrir reikningsafsláttarkóða. Þetta gerir kleift að úthluta reikningsafsláttarskilmálum hratt og örugglega til lánardrottna með því að velja nafn annars lánardrottins sem hefur sömu skilmála.

    Næsta skref er að setja upp nýja skilmála fyrir reikningsafslátt.
4. Í glugganum **Lánardrottnaspjald** er aðgerðin **Reikningsafslættir** valin. Glugginn **Reikningsafsláttur lánardr.** opnast.
5. Í reitnum **Gjaldmiðilskóði** er færður inn kóðinn fyrir gjaldmiðilinn sem reikningsafsláttarskilyrði í línunni eiga við um. Reiturinn er skilinn eftir auður ef setja á upp reikningsafsláttarskilyrði í USD.
6. Í reitinn **Lágmarksupphæð** er færð inn lágmarksupphæð sem reikningur þarf að hafa til að hægt sé að fá afslátt.
7. Í reitnum **Afsláttar %** skal slá inn reikningsafslátt sem prósentu af reikningsupphæð.
8. Endurtakið skref 5 til 7 fyrir alla gjaldmiðla sem lánardrottinn mun fá mismunandi reikningsafslátt í.

Reikningsafsláttur er nú settur upp og úthlutað á umræddan lánardrottin. Þegar valinn er lánardrottinskóði í reitnum **Kóði reikningsafsláttar** á öðrum lánardrottnaspjöldum er sama reikningsafslætti úthlutað þeim lánardrottini.

## <a name="see-also"></a>Sjá einnig
[Ítarlegt: Útreikningur besta verðs](advanced-best-price-calculation.md)  
[Uppsetning innkaupa](purchasing-setup-purchasing.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

