---
title: Hvernig á að afhenda vörur | Microsoft Docs
description: Út frá grunngerð vöruhússins, geturðu annað hvort skráð afhendingu á tengt viðskiptaskjal á útleið, eins og t.d. sölupöntun, beint, eða þú getur notað vöruhúsaafhendingarskjöl sem virða verkflæði og samlagast ýmsum vöruhúsaaðgerðum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8e5a9c93315c1bc199dbcbfe9076c01828524e96
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759943"
---
# <a name="ship-items"></a>Senda vörur

Þegar vörur eru afhentar út frá vöruhús sem er ekki sett upp fyrir vinnslu vöruhúsaafhendingu, þarf einfaldlega að skrá afhendinguna á viðeigandi viðskiptaskjal, eins og t.d. sölupöntun, þjónustupöntun, vöruskilapöntun innkaupa, eða millifærslupöntun á útleið.

Þegar þú afhendir vörur frá vöruhúsi sem er sett upp fyrir vinnslu vöruhúsaafhendingu, er hægt að afhenda vörur aðeins á grunni upprunaskjala sem aðrar fyrirtækiseiningar hafa gefið út á vöruhúsið til aðgerðar.

> [!NOTE]
> Ef vöruhúsið notar hjáskipun og hólf fyrir hverja línu er hægt að skoða magn vara sem hafa verið settar í hjáskipunarhólf. Forritið reiknar þetta magn sjálfkrafa í hvert sinn sem reitirnir í afhendingunni eru uppfærðir. Ef þær vörur tengjast afhendingunni sem verið er að undirbúa er hægt að stofna tínslu fyrir allar línurnar og ljúka síðan afhendingunni. Frekari upplýsingar eru í [Hjáskipunarvörur](warehouse-how-to-cross-dock-items.md).

## <a name="to-ship-items-with-a-sales-order"></a>Afhenda vörur með sölupöntun

Eftirfarandi lýsir því hvernig skal afgreiða vörur í sölupöntun. Skrefin eru svipuð fyrir Vöruskilapöntun innkaupa, þjónustupantanir og millifærslupantanir á útleið.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölupantanir** og veldu síðan tengda tengilinn.
2. Opna sölupöntun sem þegar er til eða stofna nýja. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).
3. Í reitnum **Magn til afhendingar** er fært inn magnið sem hefur verið afhent.

    Gildið í reitnum **Afhent magn** er uppfært. Ef um er að ræða afhendingu að hluta, getur þetta magn verið lægra en gildið í svæðinu **Magn**.
4. Valið er **Bóka** aðgerðin.

> [!NOTE]
> Ef fyrirtækið notar ekki sölupantanir gerir [!INCLUDE [prod_short](includes/prod_short.md)] ráð fyrir að allt magn hafi verið sent þegar sölureikningurinn er bókaður. Ef þessi brýtur í bága við það hvernig fyrirtækið virkar er mælt með notkun sölupantana og skráningu sendinga eins og útskýrt er í þessari grein.

## <a name="to-ship-items-with-a-warehouse-shipment"></a>Afhenda vörur með vöruhúsaafhendingu

Fyrst er stofnað afhendingarskjal frá viðskiptaupprunaskjali. Síðan er tilgreindar vörur teknar til fyrir afhendinguna.

### <a name="to-create-a-warehouse-shipment"></a>Stofna vöruhúsaafhendingu

Vanalega stofnar starfsmaðurinn sem er ábyrgur fyrir afhendingu vöruhúsaafhendingu. Eftirfarandi ferli lýsir því hvernig á að stofna sendinguna handvirkt í sjálfgefinni útgáfu af [!INCLUDE[prod_short](includes/prod_short.md)], en fyrirtækið gæti verið með sjálfvirkan hluta ferlisins, svo sem notkun handskanna eða áfestra skanna sem eru studdir af ytri veitum.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vöruhúsaafhendingar** og veldu síðan tengda tengilinn.  
2. Valið er **Nýtt** aðgerð.  

    Fyllt er út í reitina á flýtiflipanum **Almennt**. Þegar upprunaskjalalínur eru sóttar er eitthvað af upplýsingunum afritað í hverja línu.  

    Fyrir grunngerð vöruhúss með beinan frágangur og tínsla ef birgðageymslan er með sjálfgefið svæði og hólf fyrir afhendingu eru reitirnir **Svæðiskóði** og **Hólfakóði** fylltir út sjálfkrafa en hægt er að breyta þeim eftir þörfum.  

    > [!NOTE]  
    > Ef afhenda á vörur með öðrum vöruhúsaflokkskótum en flokkskóta hólfsins í reitnum **Hólfkóti** í fylgiskjalshausnum verður að eyða innihaldi reitsins **Hólfkóti** í hausnum áður en upprunaskjalslínurnar eru sóttar fyrir vörurnar.  
3. Valið er **Sækja upprunaskjöl** aðgerð. Síðan **Upprunaskjöl** opnast.

    Í nýrri eða opinni vöruhúsaafhendingu er hægt að nota síðuna **Afmörkun til að sækja upprunaskjal** til að sækja þær línur útgefna upprunaskjalsins sem segja til um hvaða vörur á að afhenda.

    1. Velja skal **Nota afmarkanir til að sækja uppr.skjöl.** aðgerðina.  
    2. Til að setja upp nýja afmörkun er lýsandi kóti færður inn í reitinn **Kóti** og smellt á **Breyta** aðgerðina.  
    3. Skilgreina hvaða gerð af upprunaskjalslínum eigi að sækja með því að fylla út viðeigandi afmörkunarreiti.  
    4. Velja skal aðgerðina **Keyra**.  

    Allar útgefnar upprunaskjalslínur sem uppfylla afmörkunarskilyrðin eru nú settar inn á síðunni **Vöruhúsaafhending** eða Vöruhúsaafhending þar sem afmörkunaraðgerðin er virkjuð.  

    Skilgreindar afmörkunarsamsetningar eru vistaðar á síðunni **Afmarkanir til að sækja upprunaskjöl** þar til þeirra er næst þörf. Hægt er að búa til ótakmarkaðan fjölda af afmörkunarsamsetningum. Hægt er að breyta skilyrði hvenær sem er með því að smella á **Breyta** aðgerðina.

4. Valin eru þau upprunaskjöl sem afhenda á vörur fyrir og smellt á **Í lagi** hnappinn.  

Línurnar úr upprunaskjölunum birtast á síðunni **Vöruhúsaafhending**. Reiturinn **Magn til afhendingar** hefur verið fylltur út með eftirstöðvum hverrar línu en hægt er að breyta magninu eftir þörfum. Ef gildinu í reitnum  **Hólfkóti** er eytt á flýtiflipanum **Almennt** áður en línurnar eru sóttar þarf að færa inn viðkomandi hólfkóta í hverri afhendingarlínu.  

> [!NOTE]  
> Ekki er hægt að afhenda fleiri vörur en talan í reitnum **Magn eftirstöðva** á upprunaskjalslínunni segir til um. Til að afhenda fleiri vörur skal sækja annað upprunaskjal sem inniheldur línu fyrir vöruna með því að nota afmörkun til að sækja upprunaskjöl með vörunni.  

Þegar línurnar sem á að senda eru komnar er hægt að hefja ferlið sem sendir línurnar til starfsmanna vöruhússins til tínslu.

### <a name="to-pick-and-ship"></a>Tínt og sent:

Vanalega stofnar starfsmaður vöruhússins, sem ber ábyrgð á tínslu, tínsluskjal eða opnar eitt slíkt sem þegar er til.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vöruhúsaafhendingar** og veldu síðan tengda tengilinn.
2. Valin er Vöruhúsaafhending sem á að Tína fyrir og veldu síðan aðgerðina **Stofna tínslu**.
3. Fylla inn í reitina á beiðnisíðunni og velja svo hnappinn **Í lagi**. Fylgiskjal Birgðatínslu vöruhúss er stofnað.

    Að öðrum kosti skal opna fyrirliggjandi vöruhúsatínslu.
4. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tínslur** og veldu síðan tengda tengilinn. Veljið vöruhúsatínsluna sem á að vinna með.

    Ef vöruhúsið er sett upp þannig að það noti hólf hefur tínslulínunum verið breytt í Taka og Setja aðgerðalínur.

    Hægt er að raða línunum, úthluta starfsmanni tínslunni, setja einingaskiptaafmörkun, ef beinn frágangur og tínsla er notuð, og prenta leiðbeiningarnar.

5. Framkvæma eiginlega vörutínslu og setja vörurnar í tilgreint afhendingarhólf, eða á afhendingarsvæðið ef engin eru hólfin.
6. Velja aðgerðina **Skrá tínslu**.

    Reiturinn **Magn til afhendingar** og reiturinn **Staða fylgiskjals** á haus afhendingarskjalsins eru uppfærðir. Vörurnar sem tíndar hafa verið eru ekki lengur tiltækar til tínslu fyrir aðrar afhendingar eða innri rekstur.
7. Prenta skal afhendingarskjölin, undirbúa afhendingarpakka og bóka síðan afhendinguna.

Nánari upplýsingar um tínslu fyrir vöruhúsaafhendingar er að finna í [Tína vörur fyrir vöruhúsaafhendingu](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Einnig er hægt að nota tínsluvinnublaðið til að sameina nokkrar tínsluleiðbeiningar í einar (fyrir fleiri en eina afhendingu) og gera þar með tínslu í vöruhúsinu skilvirkari. Frekari upplýsingar eru í [Skipuleggja tínslur á vinnublöðum](warehouse-how-to-plan-picks-in-worksheets.md).

> [!NOTE]
> Ef verið er að bíða eftir tilteknum vörum í vöruhúsinu, og hjáskipunarvirkni er notuð reiknar [!INCLUDE[prod_short](includes/prod_short.md)] í hverri afhendingar- eða tínslublaðslínu magnið af vörunni sem er í hjáskipunarhólfinu. Það uppfærir þennan reit í hvert skipti sem farið er úr afhendingarskjali eða vinnublaði eða þau opnuð. Frekari upplýsingar eru í [Hjáskipunarvörur](warehouse-how-to-cross-dock-items.md).

## <a name="see-also"></a>Sjá einnig

[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]