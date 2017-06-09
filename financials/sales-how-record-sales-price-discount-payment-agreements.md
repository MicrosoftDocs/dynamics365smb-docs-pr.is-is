---
title: "Hvernig á að: Skrá sérstök söluverð og afslætti | Microsoft Docs"
description: "Hvernig á að: Skrá sérstök söluverð og afslætti"
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
ms.openlocfilehash: 5ceddded2f95e15a6a7449bf2776b7776ce8a55c
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-record-special-sales-prices-and-discounts"></a>Hvernig á að: Skrá sérstök söluverð og afslætti
Skilgreina þarf ólíka verð- og greiðsluskilmála sem gilda þegar ólíkum viðskiptamönnum er selt þannig að umsamin gildi og reglur séu notuð í söluskjölum sem stofnuð eru fyrir viðskiptamennina.

Þegar notandi hefur skráð sérstakt verð og línuafslætti vegna sölu eða innkaupa tryggir [!INCLUDE[d365fin](includes/d365fin_md.md)] að hagnaður notanda af viðskiptum með vöru sé alltaf hámarkaður með því að reikna sjálfkrafa besta verð á sölu- og innkaupaskjölum og á færslubókarlínum fyrir verk og vörur. Nánari upplýsingar er að finna í [Ítarlegt: Útreikningur besta verðs](advanced-best-price-calculation.md).

Hvað varðar verð er hægt að hafa sérstakt söluverð sett í sölulínur ef tiltekin samsetning á viðskiptamanni, vöru, lágmarksmagni, mælieiningu, eða tupphafs-/ lokadagsetningu er til staðar.

Hvað varðar afslætti er hægt að setja upp og nota tvær tegundir söluafsláttar:

| Afsláttargerð | Lýsing |
| --- | --- |
| **Sölulínuafsláttur** |Afsláttarupphæð sem er sett inn í sölulínu ef tiltekin samsetning á viðskiptamanni, vöru, lágmarksmagni, mælieiningu, eða upphafs-/ lokadagsetningu er til staðar. Þetta virkar á sama hátt og fyrir söluverð. |
| **Reikningsafsláttur** |Hlutfallsafsláttur sem er dreginn frá heildarupphæð skjalsins ef upphæðin í öllum línum í söluskjali fer fram yfir ákveðið lágmark. |

Af því að söluverð og afsláttur á sölulínur byggist á samsetningu vöru og viðskiptamanns þá má einnig framkvæma þessa grunnstillingu í birgðaspjaldi vörunnar þar sem reglurnar og gildin eiga við.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Að setja upp söluverð fyrir viðskiptamann
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa inn **Viðskiptamenn**, og velja síðan viðeigandi tengil.
2. Opna skal viðeigandi viðskiptamannaspjald og veljið síðan aðgerðina **Verð**.

    Í reitnum **Tegund sölu** er búið að fylla út **Viðskiptamaður** og í reitnum **Sölukóði** er búið að fylla út númer viðskiptamannsins.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyllt er út lína fyrir hverja samsetningu sem veitir sérstakt söluverð fyrir viðskiptamanninn.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Sölulínuafsláttur stofnaður fyrir viðskiptamann
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa inn **Viðskiptamenn**, og velja síðan viðeigandi tengil.
2. Opna skal viðeigandi viðskiptamannaspjald og veljið svo aðgerðina **Línuafslættir**.

    Í reitnum **Tegund sölu** er búið að fylla út **Viðskiptamaður** og í reitnum **Sölukóði** er búið að fylla út númer viðskiptamannsins.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyllt er út lína fyrir hverja samsetningu sem veitir sérstakan sölulínuafslátt fyrir viðskiptamanninn.

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Að setja upp reikningsafslátt fyrir viðskiptamann
Eftir að ákveðið hefur verið hvaða viðskiptamenn geti fengið reikningsafslátt eru færðir inn reikningsafsláttarkóðar á viðskiptamannaspjöldin og sett upp skilyrði fyrir hvern kóða.

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa inn **Viðskiptamenn**, og velja síðan viðeigandi tengil.
2. Opna skal spjald viðskiptamanns sem getur fengið reikningsafslátt.
3. Í reitinn **Reikningsafsláttarkóði** er færður inn kóði fyrir viðeigandi reikningsafsláttarskilmála sem forritið notar til að reikna reikningsafslátt fyrir viðskiptamanninn.

    **Athugasemd**: Fyrirliggjandi viðskiptamannaspjöld standa fyrir reikningsafsláttarkóða. Þetta gerir kleift að úthluta reikningsafsláttarskilmálum hratt og örugglega til viðskiptamanna með því að velja nafn annars viðskiptamanns sem hefur sömu skilmála.

    Næsta skref er að setja upp nýja skilmála fyrir sölureikningsafslætti.
4. Í glugganum **Viðskiptamannaspjald** er aðgerðin **Reikningsafsláttur** valin. Glugginn **Reikningsafsláttur viðskm.** opnast.
5. Í reitnum **Gjaldmiðilskóði** er færður inn kóðinn fyrir gjaldmiðilinn sem reikningsafsláttarskilyrði í línunni eiga við um. Reiturinn er skilinn eftir auður ef setja á upp reikningsafsláttarskilyrði í USD.
6. Í reitinn **Lágmarksupphæð** er færð inn lágmarksupphæð sem reikningur þarf að hafa til að hægt sé að fá afslátt.
7. Í reitnum **Afsláttar %** skal slá inn reikningsafslátt sem prósentu af reikningsupphæð.
8. Endurtakið skref 5 til 7 fyrir alla gjaldmiðla sem viðskiptamaðurinn mun fá mismunandi reikningsafslátt í.

Reikningsafsláttur er nú settur upp og úthlutað á umræddan viðskiptamann. Þegar valinn er kóði viðskiptamannsins í reitnum **Reikningsafsl.kóði** á öðrum viðskiptamannaspjöldum er sama reikningsafslætti úthlutað þeim viðskiptamönnum.

## <a name="see-also"></a>Sjá einnig
[Ítarlegt: Útreikningur besta verðs](advanced-best-price-calculation.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

