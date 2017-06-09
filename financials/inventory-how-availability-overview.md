---
title: "Hvernig á að: Sækja yfirlit yfir aðgengi | Microsoft Docs"
description: "Lýsir því hvernig eigi að skoða tiltækar vörur milli birgðageymslna fyrir hverja sölu eða innkaupa atburðir, eftir tímabili eða eftir staðsetningu vörunnar í samsetningu Uppskriftar."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: stock
ms.date: 03/28/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 47071e5e325de8a31663b8d5a59d1ce93e5d0111
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-get-an-availability-overview"></a>Hvernig á að: Sækja yfirlit yfir aðgengi
Þegar um er að ræða viðskiptatengd verkefni er hægt að fá ítarlegar upplýsingar um hvenær og hvar vara er fáanleg, til dæmis þegar verið er að ræða við viðskiptavin um afhendingardag.

Hægt er að skoða tiltækileika alla vara eftir staðsetningu, og hægt er að skoða tiltækileika hverrar vöru eftir atburði, tímabili eða staðsetningu. Með atburði er átt við allar áætlaðar vörufærslur, svo sem söluafhendingu eða flutningsinnhreyfingu á innleið.

**Takið eftir**: Ef óskað er eftir að sjá tiltækileika eftir staðsetningu þarf að hafa birgðir á fleiri en einum stað. Nánari upplýsingar er að finna í [Hvernig á að: Setja upp staðsetningar](inventory-how-setup-locations.md).

Þegar verið er að [Nota [!INCLUDE[d365fin](includes/d365fin_md.md)], eru tölur um framboð sýndar í tveimur mismunandi reitum, hvort um sig með mismunandi skilgreiningu:

* Svæðið **Magn á lager** sýnir raunverulegt magn dagsins í dag samkvæmt bókuðum birgðafærslum.
* Svæðið **Áætluð staða til ráðstöfunar** er reiknað út og sýnir magn á lager ásamt tímasettum móttökum að frádreginni brúttóþörf. (Þegar verið er að [Nota [!INCLUDE[d365fin](includes/d365fin_md.md)], fela tímasettar móttökur í sér magn á innkaupapöntun og flutningspantanir á innleið. Brúttóþörf felur í sér magn á sölupöntunum og flutningspantanir á útleið.)

**Ábending**: Sérstaklega mikilvægt er að skoða Áætlaða stöðu til ráðstöfunar í gluggunum **Til ráðstöfunar eftir tímabili** og **Til ráðstöfunar eftir atviki** þar sem þeir innihalda dagsetningarvíddirnar.  

**Athugasemd**: Eftirfarandi ferli lýsa því hvernig á að skoða ítarlegar upplýsingar um tiltækileika á birgðalista og birgðaspjaldi. Einnig er hægt að nálgast upplýsingarnar úr söluskjalslínum, fyrir vöruna sem tilheyrir þeirri línu. Nánari upplýsingar eru í [Hvernig á að: selja vörur.](sales-how-sell-products.md)

## <a name="to-view-the-availability-of-an-item-according-to-when-it-will-be-received-or-shipped"></a>Að skoða tiltækileika vöru samkvæmt því hvenær hún berst eða verður afgreidd
Hægt er að skoða tiltækileika vöru samkvæmt áætluðum vörufærslum í glugganum **Til ráðstöfunar eftir atviki**.

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Vörur**, og velja síðan viðeigandi tengil.
2. Opnið spjald þeirrar vöru sem á að skoða ráðstöfun fyrir.
3. Veljið aðgerðina **Vara til ráðstöfunar eftir** og veljið svo aðgerðina **Atvik**.

    Glugginn **Vara til ráðstöfunar eftir atviki** sýnir hvernig birgðamagn vöru þróast yfir tíma samkvæmt áætluðum sendingum og innhreyfingarskjölum. Glugginn býður upp á samantekið yfirlit sem birtir eina línu af uppsöfnuðum upplýsingum fyrir hvert tímabil þar sem birgðamagn breytist. Tímabil þar sem ekkert tilvik varð eru ekki sýndar. Hægt er að stækka hverja línu svo hún sýni upplýsingar um tilvik sem valdið hafa uppsöfnuðu magni í línunni.
4. Veljið gildið á svæðinu **Áætluð staða til ráðstöfunar** til að skoða birgðafærslur eða opna skjöl sem mynda gildið.

## <a name="to-view-the-availability-of-an-item-in-different-periods"></a>Að skoða tiltækileika vöru á mismunandi tímabilum
Hægt er að skoða tiltækileika vöru samkvæmt tilgreindum tímabilum í glugganum **Til ráðstöfunar eftir tímabilum**.

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Vörur**, og velja síðan viðeigandi tengil.
2. Opnið spjald þeirrar vöru sem á að skoða ráðstöfun fyrir.
3. Veljið aðgerðina **Vara til ráðstöfunar eftir** og veljið svo aðgerðina **Tímabil**.

    Glugginn **Vara til ráðstöfunar eftir tímabilum** sýnir hvernig birgðamagn vöru þróast yfir tíma, sett upp eftir því tímabili sem valið er, svo sem dagur, vika eða ársfjórðungur.
4. Veljið gildið á svæðinu **Áætluð staða til ráðstöfunar** til að skoða birgðafærslur eða opna skjöl sem mynda gildið.

## <a name="to-view-the-availability-of-an-item-at-the-locations-where-it-is-stored"></a>Að skoða tiltækileika vöru eftir staðsetningunni sem hún er geymd á
Tiltækileika vöru eftir staðsetningunni sem hún er geymd á má sjá í glugganum **Vara til ráðstöfunar eftir staðsetningu**.

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Vörur**, og velja síðan viðeigandi tengil.
2. Opnið spjald þeirrar vöru sem á að skoða ráðstöfun fyrir.
3. Veljið aðgerðina **Vara til ráðstöfunar eftir** og veljið svo aðgerðina **Staðsetning**.

    Glugginn **Vara til ráðstöfunar eftir staðsetningu** sýnir hvernig birgðamagn vöru þróast yfir tíma á hverjum stað sem hún er geymd.
4. Veljið gildið á svæðinu **Magn á lager** til að skoða birgðafærslur sem mynda gildið.
5. Veljið gildið á svæðinu **Áætluð staða til ráðstöfunar** til að skoða birgðafærslur eða opna skjöl sem mynda gildið.

## <a name="to-view-the-availability-of-all-items-by-the-location-where-they-are-stored"></a>Að skoða tiltækileika allra vara eftir staðsetningunni sem þær eru geymdar á
Hægt er að sjá tiltækileika allra vara á öllum stöðum í glugganum **Vörur eftir staðsetningu**.

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Vörur**, og velja síðan viðeigandi tengil.
2. Veljið aðgerðina **Vörur eftir staðsetningu**.

    Glugginn **Vörur eftir staðsetningu** sýnir hve margar vörur af hverri tegund fyrir sig eru tiltækar á öllum staðsetningum.
3. Veljið gildið á svæðinu **Magn á lager** til að skoða birgðafærslur sem mynda gildið.

## <a name="to-view-the-availability-of-an-item-by-its-use-in-assembly-boms"></a>Að skoða framboð vöru eftir notkun hennar í samsetningu Uppskrifta
Ef til er vara í samsetningu Uppskriftir, annaðhvort sem yfirvöru eða íhlutur, þá er hægt að skoða hversu margar einingar af henni sé krafist í **Framboð vöru eftir Uppskriftarstigi** glugganum. Glugginn sýnir hve margar einingar af yfirvöru er hægt að gera á grundvelli framboðs undirvara á undirliggjandi línum. Allar vörur sem hafa samsetningu Uppskriftarinnar birtast í glugganum sem samanbrjótanleg línu. Hægt er að stækka línuna til að birta undirliggjandi íhluti og undirsamsetningar á lægri stigum ásamt eigin uppskriftum.

Hægt er að nota þennan glugga til að athuga hvort hægt sé að anna sölupöntun fyrir vöru á tiltekinni dagsetningu með því að skoða núverandi framboð ásamt magni sem íhlutir hennar geta annað. Einnig er hægt að nota gluggann til að auðkenna flöskuhálsa í tengdum samsetningum uppskrifta.

Í hverri línu í glugganum fyrir bæði yfir- og undirvörur, tilgreinið tölur til ráðstöfunar i eftirfarandi lykilsvæðum. Hægt er að nota þessar tölur til að gefa fyrirheit um hversu margar einingar af yfirvöru hægt er að afhenda ef tengt samsetningarferli er ræst.

|Svæði|Lýsing|
|------|-----------|
|**Get gert yfirmerki**|Sýnir hversu margar einingar hægt er að gera í undirsamsetningum í efstu vörunni. Reiturinn tilgreinir hversu margar tafarlausar yfireiningar hægt er að setja saman. Gildið er samkvæmt framboði vörunnar í línunni.|
|**Get gert aðalvöru**|Sýnir hversu margar einingar efstu vörunnar hægt er að gera. Reiturinn tilgreinir hversu margar einingar af aðaluppskriftarvöru hægt er að setja saman. Gildið er samkvæmt framboði vörunnar í línunni.|

**Framboð vöru eftir uppskriftarstigi** glugginn sýnir upplýsingar um vöruna á línu spjalds eða skjals sem glugginn er opnaður fyrir. Varan er alltaf sýnd í efstu línunni. Hægt er að skoða upplýsingar um aðrar vörur eða allar vörur með því að breyta gildinu í **Afmörkun vöru** reitnum.

**Athugið**: Sjálfvirkt, sýna framboðstölur á línunum heildarframboð allra vara undir aðalvörunni. Þessar tölur eru birtar í **Framboðsmagn** reitnum, og áherslan er á aðalvöruna. Hins vegar geta upplýsingar um hversu margar millivörur er hægt að búa til verið misvísandi. Til að fá raunverulega mynd af því hversu margar af birtum undirsamsetningum er hægt að búa til, þarf að hreinsa **Sýna heildarframboð** gátreitinn og skoða svo töluna í **Get gert yfirmerki** reitnum .

Reiturinn **Flöskuháls** tilgreinir hvaða vara í skipulagi uppskriftarinnar kemur í veg fyrir að gert sé meira magn en það sem sýnt er í reitnum **Get gert aðalvöru**. Til dæmis getur flöskuhálsvaran verið innkeyptur íhlutur með áætlaðri móttökudagsetningu sem er kemur of seint til að gera viðbótareiningar af aðalvörunni fyrir dagsetninguna í reitnum **Verður að vera tilbúið fyrir þessa dagsetningu**.

## <a name="see-also"></a>Sjá einnig
[Stjórna birgðum](inventory-manage-inventory.md)  
[Hvernig á að: Vinna með uppskriftir](inventory-how-work-BOMs.md)    
[Hvernig á að: Setja upp birgðageymslur](inventory-how-setup-locations.md)  
[Hvernig á að: Flytja birgðir milli birgðageymslna](inventory-how-transfer-between-locations.md)  
[Hvernig á að: Selja vörur](sales-how-sell-products.md)      
[Aðfangakeðja](madeira-supply-chain.md)  
[Unnið með Financials](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)

