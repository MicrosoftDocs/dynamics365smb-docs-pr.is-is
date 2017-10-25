---
title: "Úthluta notandaheimild og stofna eða breyta heimildarsamstæðum | Microsoft Docs"
description: "Lýsir því hvernig skal bæta Office 365 notendum við Financials, og svo úthluta heimildum, aðgangsréttindum og öryggisstillingum."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 06/27/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a944a6135feeb81b32d1f7edcb823b9da89cd404
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-manage-users-and-permissions"></a>Hvernig á að: Stjórna notendur og heimildir
Til að bæta notendum í [!INCLUDE[d365fin](includes/d365fin_md.md)], verður kerfisstjóri Office 365 í fyrirtækinu fyrst að stofna notendur í stjórnstöð Office 365. Frekari upplýsingar, sjá [Bæta notendum við Office 365 fyrir fyrirtæki](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Þegar notendur hafa verið stofnaðir í Office 365 er hægt að flytja þá inn í gluggann **notendur** með því að velja aðgerðina **Sækja notendur úr Office 365** Notendur eru úthlutað heimildir söfn samkvæmt áætlun sem er úthlutað á notandann í Office 365.

Má því næst úthluta notendum heimildarsöfnum til að skilgreina hvaða hluti úr gagnagrunni, og þar með hvaða einingar Viðmótsins, þeir hafa aðgang að og í hvaða fyrirtækjum.

Heimildasafn er safn heimildir fyrir tiltekna hluti í gagnagrunninum. Öllum notendum verða að hafa verið úthlutað eitt eða fleiri heimildasöfn áður en þeir geta opnað [!INCLUDE[d365fin](includes/d365fin_md.md)]. Nokkur fyrirfram skilgreind heimildasöfn eru veitt sjálfvirkt. Hægt er að nota þessi heimildasöfn eins og þau eru nú þegar, breyta sjálfgefnum heimildasöfnum eða búa til önnur söfn.

Þú getur bætt notendum við notendahópa. Þannig er auðveldara að úthluta sama heimildarsöfn á mörgum notendum.

Stjórnendur geta notað **Notandauppsetningu** gluggann til að skilgreina tímabil þegar tilgreindir notendur geta bókað, og geta einnig tilgreint hvort kerfið skrái tímann sem notandinn er skráður inn.

> [!NOTE]  
>   Þessi virkni krefst þess að upplifun þín sé stillt á Suite. Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).

## <a name="to-assign-permissions-to-a-user"></a>Að úthluta notanda heimild
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Notendur** og velja svo viðeigandi tengil.
2. Veldu notandann sem á að úthluta á þessum viðskiptamanni til.
Öll heimildasöfn sem er nú þegar úthlutuð til notandans eru birtar í upplýsingakassanum **Heimildasöfn**.
3. Veldu **breyta** aðgerðina til að opna gluggann **Notandapjald** .
4. Á flýtiflipanum **Heimildasöfn notanda** skal fylla út reitina eins og þörf krefur í nýrri línu. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Til hópnotenda í notandaflokkum
Þú getur sett upp notendahópa til að hjálpa þér að stjórna heimildasamstæðum fyrir hópa notenda í fyrirtæki þínu. Hægt er að nota aðgerð til að afrita öll heimildasöfn úr núverandi notandaflokki yfir í nýja notandaflokkinn þinn. Meðlimir úr notandaflokki eru ekki afritaðar.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Notandaflokkar** og velja svo viðeigandi tengil.
2. Einnig, í glugganum **Notendur**, veldu aðgerðina **Notandaflokkar**.
3. Í glugganum **Notandahópar** er valinn er fyrirliggjandi notandahópurinn sem á að afrita og veljið svo **Afrita notandahóp** aðgerðina.
4. Í reitnum **Kóðar fyrir nýja notandahópa** er tilgreint nafn þess notanda hópinn og síðan valið **Í lagi** hnappinn.

    Í stað þess að afrita, er hægt er að velja Nýja aðgerð til að búa til nýja línu fyrir auður notandahópur, og fylla síðan út handvirkt.
5. Til að við bæta nýjum eða fleiri notendur í glugganum **Notandahópur** er valin **Meðlimir notandahóps** aðgerðin.
6. Í glugganum **Notandahópur** er í nýrri línu fyllt í reitina eftir þörfum með því að velja úr hópi notendur sem þegar eru til staðar.
7. Til að bæta nýjum eða fleiri heimildarsöfnum, velurðu í glugganum **Notandahópur** aðgerðina **Heimildarsöfn notandahóps**.
8. Í glugganum **Heimildarsöfn notandahópa** er í nýrri línu fyllt í reitina eftir þörfum með því að velja úr heimildarsöfnum sem þegar eru til staðar.

## <a name="to-create-or-modify-permission-sets"></a>Til að stofna eða breyta heimildarsöfnum
Ef sjálfgefin heimildasöfn sem fylgja með [!INCLUDE[d365fin](includes/d365fin_md.md)] eru ekki fullnægjandi eða henta ekki fyrirtækinu er hægt að búa til ný heimildarsöfn. Og ef hinar einstöku heimildir fyrir hluti sem skilgreina heimildasafn nægja ekki er hægt að breyta heimildasafninu. Hægt er að búa til heimildasöfn handvirkt, eða hægt er að nota aðgerðina skráningu sem skráir aðgerðir þínar um leið og þú ferðast í gegnum sviðsmynd og býr til nauðsynlegar heimildasöfn.

### <a name="to-create-or-modify-permission-sets-manually"></a>Til að stofna eða breyta heimildarsöfnum handvirkt
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Notendur** og velja svo viðeigandi tengil.
2. Einnig, í glugganum **Notendur**, veldu aðgerðina **Heimildarsöfn**.
3. Í glugganum **Heimildarsöfn**, veldu aðgerðina **Nýtt**.
4. Fyllið í reitina eftir þörfum í nýrri línu.
5. Veljið aðgerðina **Heimildir**.
6. Í glugganum **Heimildir** skal fylla út reitina á hausnum eins og þörf krefur.
7. Í nýrri línu skal fylla út fimm reiti fyrir tegundir mismunandi heimild, eins og lýst er í eftirfarandi töflu.

    |Valkostur|Lýsing|
    |------|-----------|
    |Autt|Tilgreinir að heimildartegundin er ekki veitt fyrir hlutinn.|
    |**Já**|Tilgreinir að heimildartegundin er veitt með beinan aðgang að hlutinn.|
    |**Óbeint**|Tilgreinir að heimildartegundin er veitt með óbeinan aðgang að hlutinn.|

    Óbeinn heimildir í töflu merkir að þú getur ekki opnað töflunni og lesa úr henni, en hægt er að skoða gögnin í töflunni gegnum aðra hlutur, eins og síðu, sem þú hefur beina heimild til að fá aðgang að. Nánari upplýsingar, sjá „Dæmi - óbein heimild“ hlutann í þessu efnisatriði.

8. Í reitnum **Öryggi Afmörkun** skal færa inn afmörkun sem þú vilt að eigi við heimildir með því að velja reiturinn sem á að takmarka aðgang notanda.

    Til dæmis ef þú vilt búa til afmörkun öryggi svo að notandi geti aðeins skoðað sölu með tilteknum sölumannskóða, velurðu reitanúmer fyrir **Sölumannskóða** reitinn. Síðan, í reitnum **Reitaafmörkun** færir þú gildið inn sem á að nota til að takmarka aðgang. Til dæmis til að takmarka aðgang notanda að öllu nema sölu Annettes Hill, færirðu inn AH.
9. Endurtaka skal þrep 7 og 8 til að bæta heimildum fyrir öðrum hluti í heimildir safn.

### <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Að stofna eða breyta heimildasöfn með skráning við aðgerðir þínar
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Notendur** og velja svo viðeigandi tengil.
2. Einnig, í glugganum **Notendur**, veldu aðgerðina **Heimildarsöfn**.
3. Í glugganum **Heimildarsöfn**, veldu aðgerðina **Nýtt**.
4. Fyllið í reitina eftir þörfum í nýrri línu.
5. Veljið aðgerðina **Heimildir**.
6. Í glugganum **Heimildir**, veldu aðgerðina **Byrja**.

    Skráningarvinnsla byrjar að ná yfir allar aðgerðir þínar í notandaviðmótinu.
7. Farðu yfir í ýmsir gluggar og aðgerðir í [!INCLUDE[d365fin](includes/d365fin_md.md)] sem þú vilt að notendum með þessa heimildasöfn fá aðgang að. Þú verður að ljúka verkinu sem ætlunin er að skrá heimildir fyrir.
8. Þegar á að ljúka við skráningu er farið aftur á **Heimildir** gluggann og velja síðan **Stöðva** aðgerðina.
9. Velja **Já** hnappinn til að bæta skráð heimildir við nýja heimildasafnið.
10. Fyrir hvern hlutar á skráningar listanum, tilgreinið ef notendur geta sett inn, breytt eða eytt skráningum í skráningartöflunum. Sjá skref 7 í hlutanum „Að stofna eða breyta heimildir söfn handvirkt“.

### <a name="example---indirect-permission"></a>Dæmi - Óbein heimild
Hægt er að úthlutað óbeinni heimild til að nota hlut aðeins í gegnum annan hlut.
Til dæmis getur notandi haft heimild til að keyra kóðaeiningu 80, **Sölur-bókun**. **Sölubókun** framkvæmir mörg verk, þar á meðal að breyta töflu 37, **Sölulína**. Þegar notandinn bókar söluskjal athugar **Sala-Bókun** kóðaeiningin, [!INCLUDE[d365fin](includes/d365fin_md.md)] hvort að notandinn hafi heimild til að breyta **Sölulína** töflunni. Ef svo er ekki getur kótaeiningin ekki lokið við verkefni sín og þá munu villuboð birtast notandanum. Ef svo er verður kótaeiningin keyrð.

Hins vegar þarf notandi ekki að hafa ótakmarkaðan aðgang að töflunni **Sölulína** til að keyra kótaeininguna. Ef notandinn hefur óbeina heimild fyrir töfluna **Sölulína** þá keyrir kóðaeiningin **Sölubókun** rétt. Þegar notandi hefur óbeina heimild, getur sá notandi aðeins breytt töflunni **Sölulína** með því að keyra **Sölubókun** kóðaeiningunni eða annan hlut sem hefur heimild til að breyta töflunni **Sölulína**. Notandinn getur aðeins breytt töflunni **Sölulína** frá studdum forritssvæðum. Notandinn getur ekki keyrt eiginleikann óvart eða í sviksamlegum tilgangi á annan hátt.

## <a name="to-set-up-user-time-constraints"></a>Til að setja upp tímaskorður notanda
Stjórnendur geta skilgreint tímabil þegar tilgreindir notendur geta bókað, og geta einnig tilgreint hvort kerfið skrái tímann sem notandinn er skráður inn. Stjórnendur geta einnig úthlutað ábyrgðarstöðvum á notendur.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Notandauppsetning** og velja svo viðeigandi tengil.
2. Í glugganum **Notandauppsetning** opnast, skal velja **Nýtt** aðgerð.
3. Í reitnum **Kenni notanda**, skal færa inn kenni notanda, eða velja reitinn til að sjá alla núverandi Windows notendur innan kerfisins.
4. Fyllið inn í reitina eftir þörfum.

## <a name="see-also"></a>Sjá einnig
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Uppsetning og stjórnun í Dynamics 365 for Financials](admin-setup-and-administration.md)  
[Velkomin(n) í [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

