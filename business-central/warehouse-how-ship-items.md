---
title: Senda vörur
description: Í þessar grein er lýst hvernig eigi að senda vörur úr vöruhúsinu eftir því hverjar skilgreiningar vöruhússins eru fyrir úrvinnslu sendingar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7335, 7337, 7339, 7340, 7341, 7362, 9008
ms.date: 09/02/2022
ms.author: edupont
ms.openlocfilehash: b66a0a0a4cad12c4f41c53569b0007c51e846de7
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531216"
---
# <a name="ship-items"></a>Senda vörur

Þegar vörur eru afhentar út frá vöruhús sem er ekki sett upp fyrir vinnslu vöruhúsaafhendingu, þarf einfaldlega að skrá afhendinguna á viðeigandi viðskiptaskjal, eins og t.d. sölupöntun, þjónustupöntun, vöruskilapöntun innkaupa, eða millifærslupöntun á útleið.

Þegar þú afhendir vörur frá vöruhúsi sem er sett upp fyrir vinnslu vöruhúsaafhendingu, er aðeins hægt að afhenda vörur á grunni upprunaskjala sem aðrar fyrirtækiseiningar hafa gefið út á vöruhúsið til aðgerðar.

> [!NOTE]
> Ef vöruhúsið notar hjáskipun og hólf fyrir hverja línu er hægt að skoða magn vara sem eru settar í hjáskipunarhólf. Forritið reiknar þetta magn sjálfkrafa í hvert sinn sem reitirnir í afhendingunni eru uppfærðir. Ef þær vörur tengjast afhendingunni sem verið er að undirbúa er hægt að stofna tínslu fyrir allar línurnar og ljúka síðan afhendingunni. Frekari upplýsingar eru á [Hjáskipa vörur](warehouse-how-to-cross-dock-items.md).

## <a name="ship-items-with-a-sales-order"></a>Afhenda vörur með sölupöntun

Eftirfarandi leiðbeiningar lýsa því hvernig skal afgreiða vörur í sölupöntun. Skrefin eru svipuð fyrir Vöruskilapöntun innkaupa, þjónustupantanir og millifærslupantanir á útleið.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir**, velja síðan viðkomandi tengil.
2. Opna sölupöntun sem þegar er til eða stofna nýja. Frekari upplýsingar má finna á [Selja vörur](sales-how-sell-products.md).
3. Í reitnum **Magn til afhendingar** er fært inn magnið sem hefur verið afhent.

    Gildið í reitnum **Afhent magn** er uppfært. Ef um er að ræða afhendingu að hluta, getur þetta magn verið lægra en gildið í svæðinu **Magn**. Frekari upplýsingar er að finna í [Vinna úr hlutaafhendingum](sales-how-send-partial-shipments.md).
4. Valið er **Bóka** aðgerðin.

> [!NOTE]
> Ef fyrirtækið notar ekki sölupantanir gerir [!INCLUDE [prod_short](includes/prod_short.md)] ráð fyrir að allt magn hafi verið sent þegar sölureikningurinn er bókaður. Ef þetta er á skjön við hvernig fyrirtækið virkar er mælt með að nota sölupantanir og skrá sendingar eins og útskýrt er í þessari grein.

## <a name="ship-items-with-a-warehouse-shipment"></a>Afhenda vörur með vöruhúsaafhendingu

Fyrst er stofnað afhendingarskjal frá viðskiptaupprunaskjali. Síðan er tilgreindar vörur teknar til fyrir afhendinguna.

### <a name="create-a-warehouse-shipment"></a>Stofna vöruhúsaafhendingu

Venjulega stofnar starfsmaður sem ber ábyrgð á afhendingu vöruhúsaafhendingu. Eftirfarandi ferli lýsir því hvernig á að búa til afhendinguna handvirkt í sjálfgefinni útgáfu af [!INCLUDE[prod_short](includes/prod_short.md)]. Fyrirtækið þitt gæti samt sem áður hafa gert hluta ferlisins sjálfvirkt, t.d. með notkun handskanna eða áfastra skanna sem ytri veitur styðja.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsaafhendingar**, velja síðan viðkomandi tengil.  
2. Velja **Nýtt**.  

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

4. Veldu upprunaskjölin sem afhenda á vörur fyrir og smelltu á **Í lagi**.  

Línurnar úr upprunaskjölunum birtast á síðunni **Vöruhúsaafhending**. Reiturinn **Magn til afhendingar** hefur verið fylltur út með eftirstöðvum hverrar línu en hægt er að breyta magninu eftir þörfum. Ef gildinu í reitnum  **Hólfkóti** er eytt á flýtiflipanum **Almennt** áður en línurnar eru sóttar þarf að færa inn viðkomandi hólfkóta í hverri afhendingarlínu.  

> [!NOTE]  
> Ekki er hægt að afhenda fleiri vörur en talan í reitnum **Magn eftirstöðva** á upprunaskjalslínunni segir til um. Til að senda fleiri vörur skal nota síuvirknina til að sækja annað upprunaskjal sem inniheldur línu fyrir sömu vöruna.  

Þegar línurnar sem á að senda eru komnar er hægt að hefja ferlið sem sendir línurnar til starfsmanna vöruhússins til tínslu.

### <a name="pick-and-ship"></a>Tína og senda

Vanalega stofnar starfsmaður vöruhússins, sem ber ábyrgð á tínslu, tínsluskjal eða opnar eitt slíkt sem þegar er til.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsaafhendingar**, velja síðan viðkomandi tengil.
2. Veldu vöruhúsaafhendinguna sem á að tína fyrir, veldu síðan aðgerðina **Stofna tínslu**.
3. Fylltu út reitina á beiðnisíðunni, veldu síðan **Í lagi**. Fylgiskjal Birgðatínslu vöruhúss er stofnað.

    Einnig er hægt að opna fyrirliggjandi tínsluskjal vöruhúss.
4. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tínslur** og velja síðan viðkomandi tengil. Veldu vöruhúsatínsluna sem á að vinna í.

    Ef vöruhúsið er sett upp þannig að það noti hólf hefur tínslulínunum verið breytt í Taka og Setja aðgerðalínur.

    Ef þú notar beinan frágang og tínslu er hægt að raða línum, úthluta starfsmanni á tínsluna, velja síu einingaskipta og prenta tínsluleiðbeiningarnar.

5. Framkvæma eiginlega vörutínslu og setja vörurnar í tilgreint afhendingarhólf, eða á afhendingarsvæðið ef engin eru hólfin.
6. Velja aðgerðina **Skrá tínslu**.

    Reiturinn **Magn til afhendingar** og reiturinn **Staða fylgiskjals** á haus afhendingarskjalsins eru uppfærðir. Vörurnar sem tíndar hafa verið eru ekki lengur tiltækar til tínslu fyrir aðrar pantanir eða innri rekstur.
7. Prenta skal afhendingarskjölin, undirbúa afhendingarpakka og bóka síðan afhendinguna.

Nánari upplýsingar um tínslu fyrir vöruhúsaafhendingar er að finna í [Tína vörur fyrir vöruhúsaafhendingu](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Einnig er hægt að nota tínsluvinnublaðið til að sameina nokkrar tínsluleiðbeiningar í einar (fyrir fleiri en eina afhendingu) og gera þar með tínslu í vöruhúsinu skilvirkari. Frekari upplýsingar má finna á [Skipuleggja tínslur á vinnublaðinu](warehouse-how-to-plan-picks-in-worksheets.md).

> [!NOTE]
> Ef þú ert að bíða eftir komu tiltekinna vara í vöruhúsið og þú notar hjáskipunarvirkni þá mun [!INCLUDE[prod_short](includes/prod_short.md)] reikna út magn vörunnar í hjáskipunarhólfinu fyrir hverja vinnublaðalínu afhendingar eða tínslu. Það uppfærir þennan reit í hvert skipti sem farið er úr afhendingarskjali eða vinnublaði eða þau opnuð. Frekari upplýsingar eru á [Hjáskipa vörur](warehouse-how-to-cross-dock-items.md).

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/ship-invoice-items-dynamics-365-business-central/).

## <a name="see-also"></a>Sjá einnig .

[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
