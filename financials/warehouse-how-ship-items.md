---
title: "Hvernig á að afhenda vörur | Microsoft Docs"
description: "Út frá grunngerð vöruhússins, geturðu annað hvort skráð afhendingu á tengt viðskiptaskjal á útleið, eins og t.d. sölupöntun, beint, eða þú getur notað vöruhúsaafhendingarskjöl sem virða verkflæði og samlagast ýmsum vöruhúsaaðgerðum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0ca92ce0266c6a57d211f9ddb70dc5499f4f9648
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-ship-items"></a>Hvernig á að: Afgreiða vörur
Þegar vörur eru afhentar út frá vöruhús sem er ekki sett upp fyrir vinnslu vöruhúsaafhendingu, þarf einfaldlega að skrá afhendinguna á viðeigandi viðskiptaskjal, eins og t.d. sölupöntun, þjónustupöntun, vöruskilapöntun innkaupa, eða millifærslupöntun á útleið.

Þegar þú afhendir vörur frá vöruhúsi sem er sett upp fyrir vinnslu vöruhúsaafhendingu, er hægt að afhenda vörur aðeins á grunni upprunaskjala sem aðrar fyrirtækiseiningar hafa gefið út á vöruhúsið til aðgerðar.

> [!NOTE]
> Ef vöruhúsið notar hjáskipun og hólf fyrir hverja línu er hægt að skoða magn vara sem hafa verið settar í hjáskipunarhólf. Kerfið reiknar þetta magn sjálfkrafa í hvert sinn sem reitirnir í afhendingunni eru uppfærðir. Ef þær vörur tengjast afhendingunni sem verið er að undirbúa er hægt að stofna tínslu fyrir allar línurnar og ljúka síðan afhendingunni. Frekari upplýsingar sjá [Hvernig skal: Hjáskipa vörum](warehouse-how-to-cross-dock-items.md).

## <a name="to-ship-items-with-a-sales-order"></a>Afhenda vörur með sölupöntun
Eftirfarandi lýsir því hvernig skal taka á móti vörum með innkaupapöntun. Skrefin eru svipuð fyrir Vöruskilapöntun innkaupa, þjónustupantanir og millifærslupantanir á útleið.  
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Sölupantanir** og velja svo viðeigandi tengil.
2. Opna sölupöntun sem þegar er til eða stofna nýja. Nánari upplýsingar eru í [Hvernig á að: selja vörur.](sales-how-sell-products.md)
3. Í reitnum **Magn til afhendingar** er fært inn magnið sem hefur verið móttekið.

    Gildið í reitnum **Afhent magn** er uppfært. Ef um er að ræða afhendingu að hluta, getur þetta magn verið lægra en gildið í svæðinu **Magn**.
4. Valið er **Bóka** aðgerðin.

## <a name="to-ship-items-with-a-warehouse-shipment"></a>Afhenda vörur með vöruhúsaafhendingu
Fyrst er stofnað afhendingarskjal frá viðskiptaupprunaskjali. Síðan er tilgreindar vörur teknar til fyrir afhendinguna.

### <a name="to-create-a-warehouse-shipment"></a>Stofna vöruhúsaafhendingu
Vanalega stofnar starfsmaður sem er ábyrgur fyrir afhendingu vöruhúsaafhendingu.
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vöruhúsaafhending** og velja svo viðeigandi tengil.  
2.  Valið er **Nýtt** aðgerð.  

    Fyllt er út í reitina á flýtiflipanum **Almennt**. Þegar upprunaskjalalínur eru sóttar er eitthvað af upplýsingunum afritað í hverja línu.  

    Fyrir grunngerð vöruhúss með beinan frágangur og tínsla ef birgðageymslan er með sjálfgefið svæði og hólf fyrir afhendingu eru reitirnir **Svæðiskóði** og **Hólfakóði** fylltir út sjálfkrafa en hægt er að breyta þeim eftir þörfum.  

    > [!NOTE]  
    >  Ef afhenda á vörur með öðrum vöruhúsaflokkskótum en flokkskóta hólfsins í reitnum **Hólfkóti** í fylgiskjalshausnum verður að eyða innihaldi reitsins **Hólfkóti** í hausnum áður en upprunaskjalslínurnar eru sóttar fyrir vörurnar.  
3.  Valið er **Sækja upprunaskjöl** aðgerð. Glugginn **Upprunaskjöl** opnast.

    Í nýrri eða opinni vöruhúsaafhendingu er hægt að nota gluggann **Afmörkun til að sækja upprunaskjal** til að sækja þær línur útgefna upprunaskjalsins sem segja til um hvaða vörur á að afhenda.

    1. Velja skal **Nota afmarkanir til að sækja uppr.skjöl.** aðgerðina.  
    2. Til að setja upp nýja afmörkun er lýsandi kóti færður inn í reitinn **Kóti** og smellt á **Breyta** aðgerðina.  
    3. Skilgreina hvaða gerð af upprunaskjalslínum eigi að sækja með því að fylla út viðeigandi afmörkunarreiti.  
    4. Velja skal aðgerðina **Keyra**.  

    Allar útgefnar upprunaskjalslínur sem uppfylla afmörkunarskilyrðin eru nú settar inn í gluggann **Vöruhúsaafhending** eða Vöruhúsaafhending þar sem afmörkunaraðgerðin er virkjuð.  

    Skilgreindar afmörkunarsamsetningar eru vistaðar í **Afmarkanir til að sækja upprunaskjöl** glugganum þar til þeirra er næst þörf. Hægt er að búa til ótakmarkaðan fjölda af afmörkunarsamsetningum. Hægt er að breyta skilyrði hvenær sem er með því að smella á **Breyta** aðgerðina.

4.  Valin eru þau upprunaskjöl sem afhenda á vörur fyrir og smellt á **Í lagi** hnappinn.  

Línurnar úr upprunaskjölunum birtast í glugganum **Vöruhúsaafhending**. Reiturinn **Magn til afhendingar** hefur verið fylltur út með eftirstöðvum hverrar línu en hægt er að breyta magninu eftir þörfum. Ef gildinu í reitnum  **Hólfkóti** er eytt á flýtiflipanum **Almennt** áður en línurnar eru sóttar þarf að færa inn viðkomandi hólfkóta í hverri afhendingarlínu.  

> [!NOTE]  
>  Ekki er hægt að afhenda fleiri vörur en talan í reitnum **Magn eftirstöðva** á upprunaskjalslínunni segir til um. Til að afhenda fleiri vörur skal sækja annað upprunaskjal sem inniheldur línu fyrir vöruna með því að nota afmörkun til að sækja upprunaskjöl með vörunni.  

Þegar línurnar sem á að senda eru komnar er hægt að hefja ferlið sem sendir línurnar til starfsmanna vöruhússins til tínslu.

### <a name="to-pick-and-ship"></a>Tínt og sent:
Vanalega stofnar starfsmaður vöruhússins, sem ber ábyrgð á tínslu, tínsluskjal eða opnar eitt slíkt sem þegar er til.
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Vöruhúsaafhending** og velja svo viðeigandi tengil.
2. Valin er Vöruhúsaafhending sem á að Tína fyrir og veldu síðan aðgerðina **Stofna tínslu**.
3. Fylla inn í reitina í beiðniglugganum og velja svo hnappinn **Í lagi**. Fylgiskjal Birgðatínslu vöruhúss er stofnað.

    Að öðrum kosti skal opna fyrirliggjandi vöruhúsatínslu.
4. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Tínsla** og velja svo viðeigandi tengil. Veljið vöruhúsatínsluna sem á að vinna með.

    Ef vöruhúsið er sett upp þannig að það noti hólf hefur tínslulínunum verið breytt í Taka og Setja aðgerðalínur.

    Hægt er að raða línunum, úthluta starfsmanni tínslunni, setja einingaskiptaafmörkun, ef beinn frágangur og tínsla er notuð, og prenta leiðbeiningarnar.

5. Framkvæma eiginlega vörutínslu og setja vörurnar í tilgreint afhendingarhólf, eða á afhendingarsvæðið ef engin eru hólfin.
6. Velja aðgerðina **Skrá tínslu**.

    Reiturinn **Magn til afhendingar** og reiturinn **Staða fylgiskjals** á haus afhendingarskjalsins eru uppfærðir. Vörurnar sem tíndar hafa verið eru ekki lengur tiltækar til tínslu fyrir aðrar afhendingar eða innri rekstur.
7. Prenta skal afhendingarskjölin, undirbúa afhendingarpakka og bóka síðan afhendinguna.

Nánari upplýsingar um tínslu fyrir vöruhúsaafhendingar er að finna í [Hvernig á að: tína vörur fyrir vöruhúsaafhendingu](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Einnig er hægt að nota tínsluvinnublaðið til að sameina nokkrar tínsluleiðbeiningar í einar (fyrir fleiri en eina afhendingu) og gera þar með tínslu í vöruhúsinu skilvirkari. Frekari upplýsingar, sjá [Hvernig á að áætla tínslu á vinnublöðum](warehouse-how-to-plan-picks-in-worksheets.md).

> [!NOTE]
> Ef verið er að bíða eftir tilteknum vörum í vöruhúsinu, og hjáskipunarvirkni er notuð reiknar [!INCLUDE[d365fin](includes/d365fin_md.md)] í hverri afhendingar- eða tínslublaðslínu magnið af vörunni sem er í hjáskipunarhólfinu. Það uppfærir þennan reit í hvert skipti sem farið er úr afhendingarskjali eða vinnublaði eða þau opnuð. Frekari upplýsingar sjá [Hvernig skal: Hjáskipa vörum](warehouse-how-to-cross-dock-items.md).

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

