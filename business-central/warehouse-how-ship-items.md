---
title: Senda vörur
description: Í þessari grein er lýst hvernig á að senda vörur úr vöruhúsinu, eftir skilgreiningu vöruhúss fyrir afhendingarvinnslu.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531216"
---
# <a name="ship-items"></a>Senda vörur

Þegar vörur eru afhendingar úr vöruhúsi sem ekki hefur verið sett upp fyrir vöruhúsaafhendingarvinnslu er sendingin einfaldlega skráð á tengdu viðskiptaskjalið, til dæmis sölupöntun, þjónustupöntun, Vöruskilapöntun innkaupa eða flutningspöntun á útleið.

Þegar vörur eru afhendingar úr vöruhúsi sem er sett upp fyrir vöruhúsaafhendingarvinnslu er aðeins hægt að senda vörur á grundvelli upprunaskjala sem aðrar fyrirtækiseiningar hafa losað sig við vöruhúsið fyrir aðgerð.

> [!NOTE]
> Ef hjáskipun og hólf eru notuð fyrir hverja línu er hægt að skoða magn vara sem eru settar í hjáskipunarhólf í vöruhúsinu. Forritið reiknar þetta magn sjálfkrafa í hvert sinn sem Reitirnir í afhendingunni eru uppfærðir. Ef þær eru þær vörur sem eiga við sendinguna sem verið er að undirbúa er hægt að stofna tínslu fyrir allar línurnar og ljúka síðan sendingunni. Frekari upplýsingar um [hjáskipunarvörur](warehouse-how-to-cross-dock-items.md).

## <a name="ship-items-with-a-sales-order"></a>Senda vörur með sölupöntun

Eftirfarandi leiðbeiningar lýsa hvernig á að senda vörur úr sölupöntun. Skrefin eru svipuð fyrir Vöruskilapöntun innkaupa, þjónustupantanir og millifærslupantanir á útleið.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn **sölupantanir** og velja síðan tengda tengilinn.
2. Opna fyrirliggjandi sölupöntun eða stofna nýja. Læra meira at [selja vörur](sales-how-sell-products.md).
3. Í reitnum **Magn til afhendingar** er fært inn magnið sem hefur verið afhent.

    Gildið í reitnum **Afhent magn** er uppfært. Ef um er að ræða afhendingu að hluta, getur þetta magn verið lægra en gildið í svæðinu **Magn**. Frekari upplýsingar á [ferli hlutaafhendingar](sales-how-send-partial-shipments.md).
4. Valið er **Bóka** aðgerðin.

> [!NOTE]
> Ef fyrirtækið notar ekki sölupantanir, þegar sölureikningur er bókaður, [!INCLUDE [prod_short](includes/prod_short.md)] gerir ráð fyrir að heildarmagnið sé sent. Ef þessi árekstur á við hvernig fyrirtækið virkar mælum við með að sölupantanir séu notaðar og skrá afhendingar eins og útskýrt er í þessari grein.

## <a name="ship-items-with-a-warehouse-shipment"></a>Senda vörur með vöruhúsaafhendingu

Fyrst er stofnað afhendingarskjal frá viðskiptaupprunaskjali. Síðan er tilgreindar vörur teknar til fyrir afhendinguna.

### <a name="create-a-warehouse-shipment"></a>Stofna vöruhúsaafhendingu

Algengast er að starfsmaður hafi ábyrgð á sendingu. Eftirfarandi ferli lýsir því hvernig á að stofna sendinguna handvirkt í sjálfgefinni útgáfu af [!INCLUDE[prod_short](includes/prod_short.md)]. Hins vegar er hugsanlegt að fyrirtækið hafi sjálfvirka hluta ferlisins, svo sem með notkun handinns eða áföstum skanna sem studdir eru af utanaðkomandi veitum.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **vöruhúsaafhendingar** og velja síðan tengda tengilinn.  
2. Velja **Nýtt**.  

    Fyllt er út í reitina á flýtiflipanum **Almennt**. Þegar upprunaskjalalínur eru sóttar er eitthvað af upplýsingunum afritað í hverja línu.  

    Fyrir vöruhús sem er samskipað með beinum frágangi og tínslu, ef birgðageymslan er með sjálfgefið svæði og hólf fyrir afhendingar, **er fyllt út í reitina svæðiskóti** og **Kóti hólfs** sjálfkrafa, en hægt er að breyta þeim eftir því sem við á.  

    > [!NOTE]  
    > Ef afhenda á vörur með öðrum vöruhúsaflokkskótum en flokkskóta hólfsins í reitnum **Hólfkóti** í fylgiskjalshausnum verður að eyða innihaldi reitsins **Hólfkóti** í hausnum áður en upprunaskjalslínurnar eru sóttar fyrir vörurnar.  
3. Valið er **Sækja upprunaskjöl** aðgerð. Síðan **Upprunaskjöl** opnast.

    Í nýrri eða opinni vöruhúsaafhendingu er hægt að nota **afmarkanirnar til að sækja upprunaskjöl.** síða til að sækja útgefnar upprunaskjalslínur sem skilgreina hvaða vörur á að senda.

    1. Velja skal **Nota afmarkanir til að sækja uppr.skjöl.** aðgerðina.  
    2. Ef setja á upp nýja síu er lýsandi kóti færður inn í **reitinn Kóti** og síðan er aðgerðin breyta **valin**.  
    3. Skilgreinið gerð upprunaskjallínanna sem á að sækja með því að fylla út í viðeigandi afmörkunarreiti.  
    4. Velja skal aðgerðina **Keyra**.  

    Allar útgefnar upprunaskjalalínur sem uppfylla afmörkunarskilyrðin eru nú settar inn í **Vöruhúsaafhendingarsíðuna** sem síuaðgerðin var virkjuð fyrir.  

    Afmörkunarsamsetningar sem skilgreindar eru eru vistaðar á **afmörkunum til að sækja Upprunadoktora.** síða þar til næst þegar þörf er á henni. Hægt er að búa til ótakmarkaðan fjölda af afmörkunarsamsetningum. Hægt er að breyta skilyrði hvenær sem er með því að smella á **Breyta** aðgerðina.

4. Valin eru þau upprunaskjöl sem á að senda vörur í, síðan er valið **í lagi**.  

Línurnar úr upprunaskjölunum birtast á síðunni **Vöruhúsaafhending**. Reiturinn **Magn til afhendingar** hefur verið fylltur út með eftirstöðvum hverrar línu en hægt er að breyta magninu eftir þörfum. Ef gildinu í reitnum  **Hólfkóti** er eytt á flýtiflipanum **Almennt** áður en línurnar eru sóttar þarf að færa inn viðkomandi hólfkóta í hverri afhendingarlínu.  

> [!NOTE]  
> Ekki er hægt að afhenda fleiri vörur en talan í reitnum **Magn eftirstöðva** á upprunaskjalslínunni segir til um. Ef senda á fleiri vörur skal nota síuaðgerðina til að sækja annað upprunaskjal sem inniheldur línu fyrir sömu vöru.  

Þegar línurnar sem á að senda eru komnar er hægt að hefja ferlið sem sendir línurnar til starfsmanna vöruhússins til tínslu.

### <a name="pick-and-ship"></a>Taka til og skipa

Vanalega stofnar starfsmaður vöruhússins, sem ber ábyrgð á tínslu, tínsluskjal eða opnar eitt slíkt sem þegar er til.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **vöruhúsaafhendingar** og velja síðan tengda tengilinn.
2. Velja vöruhúsaafhendinguna sem á að velja fyrir og velja **síðan aðgerðina stofna tínslu**.
3. Reitirnir á beiðninnar eru fylltir út og síðan er valið **í lagi**. Fylgiskjal Birgðatínslu vöruhúss er stofnað.

    Einnig er hægt að opna fyrirliggjandi vöruhúsatínsluskjal.
4. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tínslur** og velja síðan viðkomandi tengil. Velja vöruhúsatínslu sem á að vinna með.

    Ef vöruhúsið er sett upp þannig að það noti hólf hefur tínslulínunum verið breytt í Taka og Setja aðgerðalínur.

    Ef notaður er beinn frágangur og tínsla er hægt að raða línunum, úthluta starfsmanni á tínsluna, setja upp hlémagnsafmörkun og prenta tínsluleiðbeiningarnar.

5. Framkvæma raunverulegar tiltektar vörur og setja þær í tilgreint afhendingarhólf, eða sendingarsvæði ef hólf eru ekki fyrir.
6. Velja aðgerðina **Skrá tínslu**.

    Reiturinn **Magn til afhendingar** og reiturinn **Staða fylgiskjals** á haus afhendingarskjalsins eru uppfærðir. Vörurnar sem voru tíndar eru ekki lengur tiltækar fyrir aðrar pantanir til tínslu eða innri aðgerðir.
7. Prenta skal afhendingarskjölin, undirbúa afhendingarpakka og bóka síðan afhendinguna.

Frekari upplýsingar um tiltekt í vöruhúsasendingum fást [í Tínsluvörum fyrir vöruhúsaafhendingar](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Einnig er hægt að nota tínsluvinnublaðið til að sameina nokkrar tínsluleiðbeiningar í einar (fyrir fleiri en eina afhendingu) og gera þar með tínslu í vöruhúsinu skilvirkari. Frekari upplýsingar í [áætlun tínsla í vinnublöðum](warehouse-how-to-plan-picks-in-worksheets.md).

> [!NOTE]
> Ef beðið er eftir komu tiltekinna vara í vöruhúsið og hjáskipunaraðgerðum er beitt er [!INCLUDE[prod_short](includes/prod_short.md)] hægt að reikna magn vörunnar í hjáskipunarhólfinu í hverri afhendingu eða tínslublaðslínu. Það uppfærir þennan reit í hvert skipti sem farið er úr afhendingarskjali eða vinnublaði eða þau opnuð. Frekari upplýsingar um [hjáskipunarvörur](warehouse-how-to-cross-dock-items.md).

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/ship-invoice-items-dynamics-365-business-central/).

## <a name="see-also"></a>Sjá einnig .

[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
