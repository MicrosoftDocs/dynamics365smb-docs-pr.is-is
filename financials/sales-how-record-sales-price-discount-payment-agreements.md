---
title: "Setja upp sérstakt söluverð og afslætti fyrir viðskiptamenn | Microsoft Docs"
description: "Lýsir því hvernig skal skilgreina varaverðlagningu og aflsáttarsamkomulag sem þú vilt að sé í söluskjölunum þegar verið er að selja til mismunandi viðskiptamanna."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 07/03/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 85d15de13739e944ff8817b402b37ae1c7e1b144
ms.openlocfilehash: 41558d6eec29a277db3cf8f156ae476faf315238
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-record-special-sales-prices-and-discounts"></a>Hvernig á að: Skrá sérstök söluverð og afslætti
Skilgreina þarf ólíka verð- og greiðsluskilmála sem gilda þegar ólíkum viðskiptamönnum er selt þannig að umsamin gildi og reglur séu notuð í söluskjölum sem stofnuð eru fyrir viðskiptamennina.

Þegar notandi hefur skráð sérstakt verð og línuafslætti vegna sölu eða innkaupa tryggir [!INCLUDE[d365fin](includes/d365fin_md.md)] að hagnaður notanda af viðskiptum með vöru sé alltaf hámarkaður með því að reikna sjálfkrafa besta verð á sölu- og innkaupaskjölum og á færslubókarlínum fyrir verk og vörur. Nánari upplýsingar, sjá: „Útreikningur besta verðs“ hlutann.

Hvað varðar verð er hægt að hafa sérstakt söluverð sett í sölulínur ef tiltekin samsetning á viðskiptamanni, vöru, lágmarksmagni, mælieiningu, eða tupphafs-/ lokadagsetningu er til staðar.

Hvað varðar afslætti er hægt að setja upp og nota tvær tegundir söluafsláttar:

| Afsláttargerð | Lýsing |
| --- | --- |
| **Sölulínuafsláttur** |Afsláttarupphæð sem er sett inn í sölulínu ef tiltekin samsetning á viðskiptamanni, vöru, lágmarksmagni, mælieiningu, eða upphafs-/ lokadagsetningu er til staðar. Þetta virkar á sama hátt og fyrir söluverð. |
| **Reikningsafsláttur** |Hlutfallsafsláttur sem er dreginn frá heildarupphæð skjalsins ef upphæðin í öllum línum í söluskjali fer fram yfir ákveðið lágmark. |

Af því að söluverð og afsláttur á sölulínur byggist á samsetningu vöru og viðskiptamanns þá má einnig framkvæma þessa grunnstillingu í birgðaspjaldi vörunnar þar sem reglurnar og gildin eiga við.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Að setja upp söluverð fyrir viðskiptamann
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **viðskiptamenn** og velja svo viðeigandi tengil.
2. Opna skal viðeigandi viðskiptamannaspjald og veljið síðan aðgerðina **Verð**.

    Í reitnum **Tegund sölu** er búið að fylla út **Viðskiptamaður** og í reitnum **Sölukóði** er búið að fylla út númer viðskiptamannsins.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyllt er út lína fyrir hverja samsetningu sem veitir sérstakt söluverð fyrir viðskiptamanninn.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Sölulínuafsláttur stofnaður fyrir viðskiptamann
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **viðskiptamenn** og velja svo viðeigandi tengil.
2. Opna skal viðeigandi viðskiptamannaspjald og veljið svo aðgerðina **Línuafslættir**.

    Í reitnum **Tegund sölu** er búið að fylla út **Viðskiptamaður** og í reitnum **Sölukóði** er búið að fylla út númer viðskiptamannsins.
3. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyllt er út lína fyrir hverja samsetningu sem veitir sérstakan sölulínuafslátt fyrir viðskiptamanninn.

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Að setja upp reikningsafslátt fyrir viðskiptamann
Eftir að ákveðið hefur verið hvaða viðskiptamenn geti fengið reikningsafslátt eru færðir inn reikningsafsláttarkóðar á viðskiptamannaspjöldin og sett upp skilyrði fyrir hvern kóða.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **viðskiptamenn** og velja svo viðeigandi tengil.
2. Opna skal spjald viðskiptamanns sem getur fengið reikningsafslátt.
3. Í reitinn **Reikningsafsláttarkóði** er færður inn kóði fyrir viðeigandi reikningsafsláttarskilmála sem forritið notar til að reikna reikningsafslátt fyrir viðskiptamanninn.

    > [!NOTE]  
>   Fyrirliggjandi viðskiptamannaspjöld standa fyrir reikningsafsláttarkóða. Þetta gerir kleift að úthluta reikningsafsláttarskilmálum hratt og örugglega til viðskiptamanna með því að velja nafn annars viðskiptamanns sem hefur sömu skilmála.

    Næsta skref er að setja upp nýja skilmála fyrir sölureikningsafslætti.
4. Í glugganum **Viðskiptamannaspjald** er aðgerðin **Reikningsafsláttur** valin. Glugginn **Reikningsafsláttur viðskm.** opnast.
5. Í reitnum **Gjaldmiðilskóði** er færður inn kóðinn fyrir gjaldmiðilinn sem reikningsafsláttarskilyrði í línunni eiga við um. Reiturinn er skilinn eftir auður ef setja á upp reikningsafsláttarskilyrði í USD.
6. Í reitinn **Lágmarksupphæð** er færð inn lágmarksupphæð sem reikningur þarf að hafa til að hægt sé að fá afslátt.
7. Í reitnum **Afsláttar %** skal slá inn reikningsafslátt sem prósentu af reikningsupphæð.
8. Endurtakið skref 5 til 7 fyrir alla gjaldmiðla sem viðskiptamaðurinn mun fá mismunandi reikningsafslátt í.

Reikningsafsláttur er nú settur upp og úthlutað á umræddan viðskiptamann. Þegar valinn er kóði viðskiptamannsins í reitnum **Reikningsafsl.kóði** á öðrum viðskiptamannaspjöldum er sama reikningsafslætti úthlutað þeim viðskiptamönnum.

## <a name="sales-invoice-discounts-and-service-charges"></a>Afslættir Sölureiknings og Þjónustugjöld
Þegar reikningsafslættir eru notaðir fer afslátturinn sem er veittur eftir því hve reikningsupphæðin er há.  

Í glugganum **Reikningsafsláttur viðskm** er einnig hægt að leggja þjónustugjald á reikninga sem eru yfir tiltekinni upphæð.  

Áður en hægt er að veita reikningsafslátt af sölu þarf að færa tilteknar upplýsingar í kerfið. Ákveða þarf:  

- hvaða viðskiptamönnum eigi að veita þessa tegund afsláttar.  
- hvaða afsláttarprósentu eigi að nota.  

Eigi að láta kerfið reikna reikningsafslátt sjálfkrafa er hægt að velja það í glugganum Sölugrunnur.  

Við hvern viðskiptamann er hægt að tilgreina hvort veita eigi reikningsafslátt ef skilyrðum er fullnægt (það er, ef reikningurinn nær ákveðinni upphæð). Skilmála um reikningsafslátt innlendra viðskiptamanna má tilgreina í SGM og í erlendum gjaldmiðli hjá erlendum viðskiptamönnum.  

Afsláttarprósentur eru tengdar við ákveðnar reikningsupphæðir í glugganum **Reikningsafsláttur viðskiptamanns**. Hægt er að færa inn hvaða prósentutölu sem er inn í hvern glugga. Hver viðskiptamaður getur haft sinn eigin glugga, eða þá að hægt er að tengja nokkra viðskiptamenn saman í glugga.  

Til viðbótar við (eða í staðinn fyrir) afsláttarprósentu er hægt að tengja ákveðið þjónustugjald við ákveðna reikningsupphæð.  

> [!TIP]  
>  Áður en hafist er handa við að setja upplýsingarnar inn í forritið er gott að útbúa uppkast af því afsláttarformi sem á að nota. Þannig er auðveldara að átta sig á því hvaða viðskiptamenn er hægt að tengja við sama reikningsafsláttarglugga. Eftir því sem setja þarf upp færri glugga, þeim mun fljótlegra er að færa inn grunnupplýsingarnar.  

## <a name="best-price-calculation"></a>Útreikningur besta verðs
Þegar notandi hefur skráð sérstakt verð og línuafslætti vegna sölu eða innkaupa tryggir [!INCLUDE[d365fin](includes/d365fin_md.md)] að hagnaður notanda af viðskiptum með vöru sé alltaf hámarkaður með því að reikna sjálfkrafa besta verð á sölu- og innkaupaskjölum og á færslubókarlínum fyrir verk og vörur.

Besta verð er lægsta leyfilega verð með hæsta leyfilega línuafslættinum þennan tiltekna dag. [!INCLUDE[d365fin](includes/d365fin_md.md)] reiknar þetta sjálfkrafa þegar það setur einingarverð og línuafsláttarprósentuna fyrir vörur í nýja skjalinu og í færslubókarlínum.

> [!NOTE]  
>   Eftirfarandi lýsir því hvernig besta verð er reiknað fyrir sölu. Útreikningurinn er sá sami fyrir innkaup.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)]kannar samsetningu reikningsfærslu á viðskiptamann og vöru og velur svo rétt viðeigandi verð og afslátt samkvæmt eftirfarandi skilyrðum:

    - Er þessi viðskiptamaður með sérstakan samning um verð eða línuafslætti, eða tilheyrir viðskiptamaðurinn hóp með slíkan samning?
    - Fellur varan eða vöruafsláttarflokkurinn á línunni undir þessa samninga?
    - Er pöntunardagsetningin (eða bókunardagsetning reikningsins og kreditreikningsins) á milli upphafs- og lokadagsetningar verðs/línuafsláttar?
    - Er mælieiningarkóti tilgreindur? Ef svo er leitar [!INCLUDE[d365fin](includes/d365fin_md.md)] að verði/línuafslætti með sama mælieiningarkóða og verði/afslætti án mælieiningarkóða.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] kannar hvort einhverjir samningar um verð/afslátt í eiga við um skjalið eða færslubókarlínuna og bætir svo við viðeigandi einingaverði og prósentu línuafsláttar samkvæmt eftirfarandi skilyrðum:

    - Er krafa um lágmarksmagn til staðar í samningi um verð/afslátt sem er uppfyllt?
    - Er krafa um gjaldmiðil til staðar í samningi um verð/afslátt sem er uppfyllt? Ef svo er, er lægsta verðið og hæsti línuafsláttur fyrir þann gjaldmiðil bætt við, jafnvel þótt SGM myndi veita betra verð. Ef ekkert verð/línuafsláttur er til í tilgreindum gjaldmiðilskóða, setur [!INCLUDE[d365fin](includes/d365fin_md.md)] inn lægsta verðið og hæsta línuafsláttinn í SGM.

Ef ekkert verð finnst fyrir vörurnar á línunni er síðasta innkaupsverð eða einingaverð sótt af birgðaspjaldinu eða birgðahaldseiningarspjaldinu.

## <a name="see-also"></a>Sjá einnig
[Uppsetning sölu](sales-setup-sales.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

