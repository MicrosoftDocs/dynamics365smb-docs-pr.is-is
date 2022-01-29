---
title: Fá yfirlit yfir tiltækileika
description: Hægt er að fá upplýsingar um tiltækar vörur milli birgðageymslna fyrir hverja sölu eða innkaupa atburðir eftir tímabili og fleiru.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: stock
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 5a65e56a58f0224230770dd9d2c847b754125d20
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012316"
---
# <a name="view-the-availability-of-items"></a>Skoða tiltækileika vöru
Þegar um er að ræða viðskiptatengd verkefni er hægt að fá ítarlegar upplýsingar um hvenær og hvar vara er fáanleg, til dæmis þegar verið er að ræða við viðskiptavin um afhendingardag.

Hægt er að skoða tiltækileika alla vara eftir staðsetningu, og hægt er að skoða tiltækileika hverrar vöru eftir atburði eða líka tímabili. Með atburði er átt við allar áætlaðar vörufærslur, svo sem söluafhendingu eða flutningsinnhreyfingu á innleið.

> [!NOTE]  
>   Ef óskað er eftir að sjá tiltækileika eftir staðsetningu þarf að hafa birgðir á fleiri en einum stað. Nánari upplýsingar er að finna í [Setja upp birgðageymslur](inventory-how-setup-locations.md).

Ef þú notar vöruhúsaaðgerðir, eru framboð mismunandi eftir úthlutun á þeim hólfastigum þegar vöruhúsaaðgerðir, t.d. tiltektir og hreyfingar eiga sér stað og þegar frátekningarkerfið setur takmarkanir. Frekar flókið reiknirit staðfestir að öllu skilyrði eru uppfyllt áður en magni er úthlutað í tínslu fyrir útleiðarflæði. Nánari upplýsingar eru í [Upplýsingar um hönnun: Til ráðstöfunar í vöruhúsi](design-details-availability-in-the-warehouse.md).

Í [!INCLUDE[prod_short](includes/prod_short.md)], eru tölur um framboð yfirleitt sýndar í tveimur mismunandi reitum, hvor um sig með mismunandi skilgreiningu:

* Svæðið **Magn á lager** á sumum stöðum kallað **Birgðir** sýnir raunverulegt magn dagsins í dag samkvæmt bókuðum birgðafærslum.
* Svæðið **Áætluð staða til ráðstöfunar** er reiknað út og sýnir magn á lager ásamt tímasettum móttökum að frádreginni brúttóþörf. (Í [!INCLUDE[prod_short](includes/prod_short.md)], fela tímasettar móttökur í sér magn á innkaupapöntun og flutningspantanir á innleið. Brúttóþörf felur í sér magn á sölupöntunum og flutningspantanir á útleið.)

> [!TIP]  
>   Sérstaklega mikilvægt er að skoða Áætlaða stöðu til ráðstöfunar á síðunum **Tiltækileiki vöru eftir tímabili** og **Tiltækileiki vöru eftir atviki** þar sem þeir innihalda dagsetningarvíddirnar.  

> [!NOTE]  
>   Eftirfarandi ferli lýsa því hvernig á að skoða ítarlegar upplýsingar um tiltækileika á birgðalista og birgðaspjaldi. Einnig er hægt að nálgast upplýsingarnar úr söluskjalslínum, fyrir vöruna sem tilheyrir þeirri línu. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).

## <a name="to-view-the-availability-of-an-item-according-to-when-it-will-be-received-or-shipped"></a>Að skoða tiltækileika vöru samkvæmt því hvenær hún berst eða verður afgreidd
Hægt er að skoða tiltækileika vöru samkvæmt áætluðum vörufærslum á síðunni **Til ráðstöfunar eftir atviki**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.
2. Opnið spjald þeirrar vöru sem á að skoða ráðstöfun fyrir.
3. Veljið aðgerðina **Vara til ráðstöfunar eftir** og veljið svo aðgerðina **Atvik**.

    Síðan **Vara til ráðstöfunar eftir atviki** sýnir hvernig birgðamagn vöru þróast yfir tíma samkvæmt áætluðum sendingum og innhreyfingarskjölum. Síðan býður upp á samantekið yfirlit sem birtir eina línu af uppsöfnuðum upplýsingum fyrir hvert tímabil þar sem birgðamagn breytist. Tímabil þar sem ekkert tilvik varð eru ekki sýndar. Hægt er að stækka hverja línu svo hún sýni upplýsingar um tilvik sem valdið hafa uppsöfnuðu magni í línunni.
4. Veljið gildið á svæðinu **Áætluð staða til ráðstöfunar** til að skoða birgðafærslur eða opna skjöl sem mynda gildið.

## <a name="to-view-the-availability-of-an-item-in-different-periods"></a>Að skoða tiltækileika vöru á mismunandi tímabilum
Hægt er að skoða tiltækileika vöru samkvæmt tilgreindum tímabilum á síðunni **Til ráðstöfunar eftir tímabilum**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.
2. Opnið spjald þeirrar vöru sem á að skoða ráðstöfun fyrir.
3. Veljið aðgerðina **Vara til ráðstöfunar eftir** og veljið svo aðgerðina **Tímabil**.

    Síðan **Vara til ráðstöfunar eftir tímabilum** sýnir hvernig birgðamagn vöru þróast yfir tíma, sett upp eftir því tímabili sem valið er, svo sem dagur, vika eða ársfjórðungur.
4. Veljið gildið á svæðinu **Áætluð staða til ráðstöfunar** til að skoða birgðafærslur eða opna skjöl sem mynda gildið.

## <a name="to-view-the-availability-of-an-item-at-the-locations-where-it-is-stored"></a>Að skoða tiltækileika vöru eftir staðsetningunni sem hún er geymd á
Tiltækileika vöru eftir staðsetningunni sem hún er geymd á má sjá á síðunni **Vara til ráðstöfunar eftir staðsetningu**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.
2. Opnið spjald þeirrar vöru sem á að skoða ráðstöfun fyrir.
3. Veljið aðgerðina **Vara til ráðstöfunar eftir** og veljið svo aðgerðina **Staðsetning**.

    Síðan **Vara til ráðstöfunar eftir staðsetningu** sýnir hvernig birgðamagn vöru þróast yfir tíma á hverjum stað sem hún er geymd.
4. Veljið gildið á svæðinu **Magn á lager** til að skoða birgðafærslur sem mynda gildið.
5. Veljið gildið á svæðinu **Áætluð staða til ráðstöfunar** til að skoða birgðafærslur eða opna skjöl sem mynda gildið.

## <a name="to-view-the-availability-of-all-items-by-the-location-where-they-are-stored"></a>Að skoða tiltækileika allra vara eftir staðsetningunni sem þær eru geymdar á
Hægt er að sjá tiltækileika allra vara á öllum stöðum á síðunni **Vörur eftir staðsetningu**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.
2. Veljið aðgerðina **Vörur eftir staðsetningu**.

    Síðan **Vörur eftir staðsetningu** sýnir hve margar vörur af hverri tegund fyrir sig eru tiltækar á öllum staðsetningum.
3. Veljið gildið á svæðinu **Magn á lager** til að skoða birgðafærslur sem mynda gildið.

## <a name="to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms"></a>Að skoða framboð vöru eftir notkun hennar í samsetningu eða uppskrifta
Ef atriði er hluti af samsetningum eða framleiðsluuppskriftum sem annaðhvort yfirvara eða íhlutur er hægt að sjá hversu margar einingar eru nauðsynlegar á síðunni **Vara til ráðstöfunar eftir uppskriftarstigi**. Síðan sýnir hve margar einingar af yfirvöru er hægt að gera á grundvelli framboðs undirvara á undirliggjandi línum. Allar vörur sem hafa samsetningu eða framleiðsluuppskrift birtast á síðunni sem samanbrjótanleg línu. Hægt er að stækka línuna til að birta undirliggjandi íhluti og undirsamsetningar á lægri stigum ásamt eigin uppskriftum.

Hægt er að nota þennan glugga til að athuga hvort hægt sé að anna sölupöntun fyrir vöru á tiltekinni dagsetningu með því að skoða núverandi framboð ásamt magni sem íhlutir hennar geta annað. Einnig er hægt að nota síðuna til að auðkenna flöskuhálsa í tengdum uppskriftum.

Í hverri línu á síðunni fyrir bæði yfir- og undirvörur, tilgreinið tölur til ráðstöfunar i eftirfarandi lykilsvæðum. Hægt er að nota þessar tölur til að gefa fyrirheit um hversu margar einingar af yfirvöru hægt er að afhenda ef tengt samsetningarferli er ræst.

|Svæði|Lýsing|
|------|-----------|
|**Get gert yfirmerki**|Sýnir hversu margar einingar hægt er að gera í undirsamsetningum í efstu vörunni. Reiturinn tilgreinir hversu margar tafarlausar yfireiningar hægt er að setja saman. Gildið er samkvæmt framboði vörunnar í línunni.|
|**Get gert aðalvöru**|Sýnir hversu margar einingar efstu vörunnar hægt er að gera. Reiturinn tilgreinir hversu margar einingar af aðaluppskriftarvöru hægt er að setja saman. Gildið er samkvæmt framboði vörunnar í línunni.|

### <a name="to-view-the-availability-of-an-item-according-to-demand-for-its-parent"></a>Til að skoða framboð vöru samkvæmt eftirspurn fyrir yfireiningu hennar
Síðan **Framboð vöru eftir uppskriftarstigi** sýnir upplýsingar um vöruna á línu spjalds eða skjals sem glugginn er opnaður fyrir. Varan er alltaf sýnd í efstu línunni. Hægt er að skoða upplýsingar um aðrar vörur eða allar vörur með því að breyta gildinu í **Afmörkun vöru** reitnum.

> [!NOTE]  
>   Sjálfgefið sýna ráðstöfunartölur á línunum heildarráðstöfun allra vara undir söluhæstu vörunni Þessar tölur eru birtar í **Framboðsmagn** reitnum, og áherslan er á aðalvöruna. Hins vegar geta upplýsingar um hversu margar millivörur er hægt að búa til verið misvísandi. Til að fá raunverulega mynd af því hversu margar af birtum undirsamsetningum er hægt að búa til, þarf að hreinsa **Sýna heildarframboð** gátreitinn og skoða svo töluna í **Get gert yfirmerki** reitnum .

Reiturinn **Flöskuháls** tilgreinir hvaða vara í skipulagi uppskriftarinnar kemur í veg fyrir að gert sé meira magn en það sem sýnt er í reitnum **Get gert aðalvöru**. Til dæmis getur flöskuhálsvaran verið innkeyptur íhlutur með áætlaðri móttökudagsetningu sem er kemur of seint til að gera viðbótareiningar af aðalvörunni fyrir dagsetninguna í reitnum **Verður að vera tilbúið fyrir þessa dagsetningu**.

## <a name="to-view-the-availability-of-an-item-by-its-units-of-measure"></a>Til að skoða framboð vöru eftir mælieiningum hennar
Síðan **Framboð á vöru eftir mælieiningu** sýnir vöruframboð eftir mælieiningum sem varan er geymd í.

> [!NOTE]  
> Til að halda þessum upplýsingum nákvæmum verður þú að umreikna mælieiningar vörunnar. Ef þú kaupir til dæmis vöru á einni mælieiningu, eins og kassa, og þú selur vörur í annarri einingu, eins og stykkjum, verður þú að nota birgðabók til að umbreyta mælieiningum eða „taka vörurnar úr kassanum“. Hægt er að nota neikvæða leiðréttingarvörulínu til að minnka birgðir á mælieiningu innkaupa, til dæmis reiti, og jákvæða leiðréttingu til að auka birgðir á mælieiningu sölu, til dæmis stykki. 

## <a name="assembly-availability-page"></a>Síðan „Samsetningarráðstöfun“
Síðan **Samsetningaráðstöfun** birtir sundurliðaðar ráðstöfunarupplýsingarnar fyrir samsetningaríhluti. Það opnast:

- Sjálfkrafa úr sölupöntunarlínu í samsetningarpöntunaraðstæður þegar magn er fært inn sem veldur vandamálum með ráðstöfun íhlutar.
- Sjálfkrafa úr samsetningarpöntunarhaus þegar gildi er fært inn í reitinn Magn sem veldur vandamálum með ráðstöfun íhlutar.
- Handvirkt þegar hann er opnaður í samsetningarpöntun. Á flipanum Aðgerðir í flokknum Eiginleikar veljið Sýna framboð.

Flýtiflipinn **Upplýsingar** sýnir sundurliðaðar ráðstöfunarupplýsingarnar fyrir samsetningarvöruna, þar með talið hversu mikið af samsetningarpöntuninni er hægt að setja saman fyrir skiladagsetninguna út frá nauðsynlegum íhlutum til ráðstöfunar. Þetta birtist í reitnum Hægt að setja saman í flýtiflipanum Upplýsingar.

Gildið í reitnum **Hægt að setja saman** er með rauðu letri ef magnið er undir magninu í reitnum **Eftirstandandi magn** sem gefur til kynna að ekki eru nógu margir íhlutir tiltækir til að setja saman fullt magn.

Flýtiflipinn **Línur** birtir sundurliðaðar ráðstöfunarupplýsingarnar fyrir samsetningaríhluti.

Ef einn eða fleiri samsetningaríhlutir eru ekki tiltækir endurspeglast það í reitnum **Hægt að setja saman** í viðkomandi línu sem magn sem er minna en magnið í **Eftirstöðvar (magn)** á flýtiflipanum **Upplýsingar**.

## <a name="see-also"></a>Sjá einnig
[Stjórna birgðum](inventory-manage-inventory.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Unnið með uppskriftir](inventory-how-work-BOMs.md)    
[Uppsetning birgðageymsla](inventory-how-setup-locations.md)  
[Flytja birgðir milli birgðageymslna](inventory-how-transfer-between-locations.md)  
[Selja vörur](sales-how-sell-products.md)      
[Unnið með Business Central](ui-work-product.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]