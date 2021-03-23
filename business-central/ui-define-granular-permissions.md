---
title: Skilgreina nákvæmari heimildir | Microsoft Docs
description: Lýsir því hvernig á að veita notendum aðgang að hlutum með því að úthluta þeim heimildasamstæðum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 48547fbe3cb2bb7cf509c1b0720cb6ccfc58cd97
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385875"
---
# <a name="assign-permissions-to-users-and-groups"></a>Úthluta leyfum til notenda og hópa

[!INCLUDE[prod_short](includes/prod_short.md)] öryggiskerfið gerir þér kleift að stjórna því hvaða hluti notandi hefur aðgang að í hverjum gagnagrunni eða umhverfi fyrir sig. Þú getur tilgreint fyrir hvern notanda hvort hann geti lesið, breytt eða slegið inn gögn í valda gagnagrunnshluti. Frekari upplýsingar er að finna í [Gagnaöryggi](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) í hjálp Developer and ITPro fyrir [!INCLUDE[prod_short](includes/prod_short.md)].

Áður en þú úthlutar heimildum til notenda og notendaflokka þarftu að skilgreina hverjir geta skráð sig inn með því að búa til notendur samkvæmt leyfi eins og skilgreint er í stjórnendamiðstöð Microsoft 365. Nánari upplýsingar er að finna í [Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md)

Í [!INCLUDE[prod_short](includes/prod_short.md)] eru tvö stig heimilda fyrir gagnagrunnshluti:

- Heildarheimildir í samræmi við leyfi, einnig nefnt réttindi.
- Nákvæmari heimildir eins og þeim er úthlutað innan [!INCLUDE[prod_short](includes/prod_short.md)].

Til að auðvelda þér að stjórna heimildum fyrir marga notendur geturðu raðað þeim í notendaflokka og þar með úthlutað eða breytt einni heimildasamstæðu fyrir marga notendur í einni aðgerð. Frekari upplýsingar er að finna á[Til að stjórna heimildum í gegnum notendaflokka](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups).

> [!NOTE]
> Viðbótaraðferð við að skilgreina hvaða eiginleika notandi hefur aðgang að er með því að stilla reitinn **Upplifun** á síðunni **Fyrirtækjaupplýsingar**. Frekari upplýsingar er að finna í [Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md).
>
> Einnig er hægt að skilgreina hvað notendur sjá í notandaviðmótinu og hvernig þeir nota heimilaða virkni sína á síðum. Þetta er gert í gegnum forstillingar sem þú úthlutar til mismunandi notenda í samræmi við starfshlutverk þeirra eða deild. Frekari upplýsingar er að finna í [Vinna með forstillingar](admin-users-profiles-roles.md) og [Sérstillingar [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md).

## <a name="to-assign-permission-sets-to-users"></a>Til að úthluta heimildasamstæðu á notendur

Heimildasamstæða er safn heimilda fyrir tiltekna gagnagrunnshluti. Öllum notendum verða að hafa verið úthlutað eitt eða fleiri heimildasöfn áður en þeir geta opnað [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE[prod_short](includes/prod_short.md)] lausn inniheldur fjölda fyrirfram skilgreindra heimildasamstæðna sem eru bætt við af Microsoft eða þjónustuveitunni þinni. Þú getur einnig bætt við nýjum heimildasamstæðum sem eru sniðin að þörfum fyrirtækisins. Nánari upplýsingar er að finna í [Að búa til eða breyta heimildasamstæðum](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

> [!NOTE]
> Ef þú vilt ekki takmarka aðgang notanda meira en þegar hefur verið skilgreint með leyfi geturðu úthlutað notanda sérstakri heimildasamstæðu sem kallast SUPER. Þessi heimildasamstæða tryggir að notandinn geti fengið aðgang að öllum hlutum sem eru tilgreindir í leyfi.
>
> Notandi með nauðsynlegt leyfi og SUPER-heimildasamstæðuna hefur aðgang að meiri virkni en notendur með Team Member-leyfið og SUPER-heimildasamstæðuna.

Þú getur úthlutað heimildarhópum til notenda á tvo vegu:

- Af **Notandaspjald** síðunni með því að velja heimildasamstæður til að úthluta notandanum.
- Frá síðunni **Heimildasamstæða eftir notendum** með því að velja notendur sem heimildasamstæðu er úthlutað til.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Til að úthluta heimildasamstæðu á notendakorti

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.
2. Veldu notandann sem á að úthluta á þessum viðskiptamanni til.
Öll heimildasöfn sem er nú þegar úthlutuð til notandans eru birtar í upplýsingakassanum **Heimildasöfn**.
3. Veldu **breyta** aðgerðina til að opna síðuna **Notandapjald** .
4. Á flýtiflipanum **Heimildasöfn notanda** skal fylla út reitina eins og þörf krefur í nýrri línu. Nánari upplýsingar er að finna í [Að búa til eða breyta heimildasamstæðum](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Til að úthluta heimildasamstæðu á síðunni Heimildasamstæða eftir notanda

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.
2. Á síðunni **Notendur** skal velja viðeigandi notanda, og þá velja aðgerðina **Heimildasamstæða eftir notanda**.
3. Á síðunni **heimildasamstæða eftir notanda** veldu **[notandanafnið]** gátreitinn á línu fyrir viðkomandi heimildasamstæðu til að tengja samstæðuna við notandann.
4. Veldu **Allir notendur** gátreitinn til að úthluta heimildasamstæðunni til allra notenda.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Fá yfirlit yfir heimildir notanda

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.
2. Opnaðu kort viðkomandi notanda.
3. Velja **Virkar heimildir** aðgerð.

    **Heimildir** hlutinn listar allar gagnagrunnshlutir sem notandinn hefur aðgang að. Þú getur ekki breytt þessum hluta.

    **Eftir heimildasamstæðu** hlutinn sýnir þær úthlutaðar heimildasamstæður sem notandinn fær heimildir sínar í gegnum, uppruna og gerð heimildasamstæðunnar, og að hvaða marki mismunandi aðgangsgerðir eru leyfðar.

    Fyrir hverja röð sem þú velur í **heimildir** hlutanum, sýnir **eftir heimildasamstæðu** hlutinn hvaða heimildasamstæða eða -samstæður heimildin er veitt í gegnum. Í þessum kafla er hægt að breyta gildinu í hverjum af fimm reitum aðgangsgerðar, **Lesa heimild**, **Setja inn heimild**, **Breyta heimild**, **Eyða heimild**, **Framkvæma heimild**.

    > [!NOTE]  
    > Einungis heimildasamstæður af tegund **Notandaskilgreint** geta verið breytt.
    >
    > Línur uppruna réttinda eru komnar frá áskriftarleyfinu. Heimildagildi réttindanna yfirtaka gildi í öðrum heimildasamstæðum ef þeir hafa hærri röðun. Gildi í réttindalausri heimildasamstæðu sem hefur hærra röðun en tengt gildi í réttindunum verður innan sviga til að gefa til kynna að það sé ekki virkt, þar sem það verður yfirtekið af réttindunum.
    >
    > Fyrir skýringu á röðun skal sjá [Að búa til eða breyta heimildum handvirkt](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

4. Til að breyta heimildasamstæðu skaltu í **Eftir heimildasamstæðu** hlutanum, á línu fyrir viðeigandi heimildasamstæðu af tegund **Notandaskilgreint**, skaltu velja einn af fimm reitum aðgangsgerðar og velja annað gildi.

5. Til að breyta einstökum heimildum innan heimildasamstæðunnar skaltu velja gildi í **heimildasamstæðu** gluttanum til að opna **Heimildir** gluggann. Fylgdu skrefunum sem er lýst í [Að búa til eða breyta heimildum](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

> [!NOTE]  
> Þegar þú breytir heimildasamstæðu munu breytingarnar einnig eiga við um aðra notendur sem hafa heimildarsamstæðuna úthlutað.

## <a name="to-create-or-modify-a-permission-set"></a>Að búa til eða breyta heimildasamstæðu

Heimildasamstæður virka sem geymir fyrir heimildir, svo að þú getir auðveldlega stjórnað mörgum heimildum í einni skrá.

> [!NOTE]  
> [!INCLUDE[prod_short](includes/prod_short.md)] lausn inniheldur yfirleitt fjölda fyrirfram skilgreindra heimildasamstæðna sem eru bætt við af Microsoft eða hugbúnaðarveitunni þinni. Þessar heimildasamstæður eru af tegund **Kerfi** eða **Viðbót**. Þú getur ekki búið til eða breytt þessum gerðum heimildasamstæða eða heimildir innan þeirra. Hins vegar getur þú afritað þau til að skilgreina eigin heimildasamstæður og heimildir.
>
> Heimildasamstæður sem notendur búa til, ný eða sem afrit, eru af gerðinni **Notandaskilgreint** og er hægt að breyta.

### <a name="to-create-new-permission-set-from-scratch"></a>Til að stofna nýja heimildasamstæðu frá grunni

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Heimildasamstæður** og veldu síðan tengda tengilinn.
2. Til að búa til nýtt heimildasamstæðu, veldu **Nýtt** aðgerðina.
3. Fyllt er í reitina í nýju línunni. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Þegar þú hefur búið til heimildasamstæðu verður þú að bæta við raunverulegum heimildum. Nánari upplýsingar er að finna í [Að búa til eða breyta heimildum handvirkt](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-copy-a-permission-set"></a>Til að afrita heimildasamstæðu

Þú getur einnig notað afritunaraðgerð til að flytja allar heimildir annars heimildasamstæðu á nýtt heimildasamstæðu.

> [!NOTE]  
> Ef heimildasamstæða Kerfis sem þú hefur afritað er breytt, færð þú senda tilkynning (eftir vali þínu), svo að þú getir íhugað hvort breytingarnar séu viðeigandi til að afrita eða skrifa inn í notendaskilgreinda heimildasamstæðu þína.

1. Á síðunni **heimildasamstæður** skaltu velja línuna fyrir heimildasamstæðu sem þú vilt afrita og síðan velja **Afrita heimildasamstæðu** aðgerðina.
2. Á síðunni **Afrita heimildasamstæðu** skaltu tilgreina nafn hinna nýju heimildasamstæðu, og þá velja **Í lagi** hnappinn.
3. Veldu **tilkynna um breyttan heimildasamstæðu** gátreitinn ef þú vilt viðhalda tengil á milli upprunalegu og afrituðu heimildasamstæðanna. Tengillinn er síðan notaður til að láta þig vita ef nafnið eða innihald upprunalegu heimildasamstæðu breytist í framtíðarútgáfunni sem lausnin er uppfærð í seinna.

Nýja heimildasamstæðan, sem inniheldur öll heimildir afritaðs heimildasamstæðu, er bætt við sem ný lína á síðunni **heimildasamstæða**. Nú er hægt að breyta heimild í nýju heimildasamstæðunni. Athugaðu að línurnar eru flokkaðar í stafrófsröð innan hvers tegundar.

### <a name="to-export-and-import-a-permission-set"></a>Til að flytja út og flytja inn heimildasamstæðu

Til að setja upp heimildir á skjótan máta geturðu flutt inn heimildasamstæður sem þú hefur flutt út frá öðrum [!INCLUDE[prod_short](includes/prod_short.md)]-leigjanda.

Í umhverfi margra leigjenda er heimildasamstæða flutt inn í tiltekinn leigjanda, þ.e. umfang innflutningsins er „Leigjandi“.

1. Á leigjanda 1, á síðunni **Heimildasamstæður** skaltu velja línuna eða línurnar fyrir heimildasamstæður sem á að flytja út og velja síðan aðgerðina **Flytja út heimildasamstæður**.

    XML-skrá er útbúin í niðurhalsmöppunni á tölvunni þinni. Hún er sjálfgefið nefnd „Export Permission Sets.xml“

2. Á leigjanda 2, á síðunni **Heimildasamstæður** skaltu aðgerðina **Flytja inn heimildasamstæður**.
3. Á síðunni **Flytja inn heimildasamstæður** þarf að íhuga hvort sameina á fyrirliggjandi heimildasamstæður nýjum heimildasamstæðum í XML-skránni.

    Ef þú velur ekki gátreitinn **Uppfæra fyrirliggjandi heimildir** eru fyrirliggjandi heimildir með sama heiti og þær sem eru í XML-skránni sameinaðar innfluttum heimildasamstæðum.

    Ef þú velur ekki gátreitinn **Uppfæra fyrirliggjandi heimildir** er heimildunum með sama heiti og þeim sem eru til í XML-skránni sleppt við innflutninginn. Í þeim tilvikum verður þér tilkynnt um heimildasamstæður sem er sleppt.

4. Á staðfestingarsíðunni **Innflutningur** skaltu finna og velja xml-skrána sem á að flytja inn og velja svo aðgerðina **Opna**.

Heimildasamstæðurnar eru fluttar inn.

## <a name="to-create-or-modify-permissions-manually"></a>Til að stofna eða breyta heimildum handvirkt

Þetta ferli útskýrir hvernig á að bæta við eða breyta heimildum handvirkt. Þú getur einnig fengið heimildir sem eru myndaðar sjálfkrafa úr aðgerðum þínum í notendaviðmótinu. Nánari upplýsingar er að finna í [Að búa til eða breyta heimildum með því að skrá aðgerðir þínar](ui-define-granular-permissions.md#to-create-or-modify-permissions-by-recording-your-actions).

> [!NOTE]
> Þegar þú breytir heimild og þar með tengdum heimildasamstæðu munu breytingarnar einnig eiga við um aðra notendur sem hafa heimildasamstæðu úthlutað.

1. Á síðunni **heimildasamstæður** skal velja línuna fyrir heimildasamstæðu, og þá velja **heimildir** aðgerð.
2. Á síðunni **Heimildir**, búðu til nýjan línu eða breyttu reitum á núverandi línu.

Í hverju af fimm reitum yfir aðgangstegundir, **Lesa heimild** , **Setja inn heimild**, **Breyta heimild**, **Eyða leyfi** og **Framkvæma heimildir**, þú getur valið eitt af eftirfarandi þremur heimildarvalkostum:

|Valkostur|Description|Flokkun|
|------|-----------|-------|
|**Já**|Notandinn getur framkvæmt aðgerðina á hlutnum sem um ræðir.|Hæst|
|**Óbeint**|Notandinn getur framkvæmt aðgerðina á hlutnum sem um ræðir en aðeins í gegnum aðra tengda hlut sem notandinn hefur fulla aðgang að. Frekari upplýsingar um óbeinar heimildir er að finna í [Eiginleiki heimilda](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property) í Developer og IT-Pro hjálpinni|Næst hæsta|
|**Autt**|Notandinn getur ekki framkvæmt aðgerðina á hlutnum sem um ræðir.|Lægstur|

### <a name="example---indirect-permission"></a>Dæmi - Óbein heimild

Hægt er að úthlutað óbeinni heimild til að nota hlut aðeins í gegnum annan hlut.
Til dæmis getur notandi haft heimild til að keyra kótaeiningu 80, Sala-bókun. Sölubókun framkvæmir mörg verk, þar á meðal að breyta töflu 37, Sölulína. Þegar notandinn bókar söluskjal athugar kóðaeining sölu-bókunar, [!INCLUDE[prod_short](includes/prod_short.md)], hvort að notandinn hafi heimild til að breyta töflu sölulínu. Ef svo er ekki getur kótaeiningin ekki lokið við verkefni sín og þá munu villuboð birtast notandanum. Ef svo er verður kótaeiningin keyrð.

Hins vegar þarf notandi ekki að hafa ótakmarkaðan aðgang að töflunni Sölulína til að keyra kótaeininguna. Ef notandinn hefur óbeina heimild fyrir töflu sölulínu keyrir kóðaeiningin Sala-bókun án vandræða. Þegar notandi hefur óbeina heimild, getur sá notandi aðeins breytt töflunni Sölulína með því að keyra Sölubókun kóðaeiningunni eða annan hlut sem hefur heimild til að breyta töflunni Sölulína. Notandinn getur aðeins breytt töflunni Sölulína frá studdum forritssvæðum. Notandinn getur ekki keyrt eiginleikann óvart eða í sviksamlegum tilgangi á annan hátt.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a>Að stofna eða breyta heimildum með skráning við aðgerðir þínar

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Heimildasamstæður** og veldu síðan tengda tengilinn.
2. Einnig, á síðunni **Notendur**, veldu aðgerðina **Heimildarsöfn**.
3. Á síðunni **Heimildarsöfn**, veldu aðgerðina **Nýtt**.
4. Fyllið í reitina eftir þörfum í nýrri línu.
5. Veljið aðgerðina **Heimildir**.
6. Á síðunni **Heimildir** skal velja aðgerðina **Skrá heimildir** og velja svo aðgerðina **Byrja**.

    Þetta setur af stað skráningarferli sem heldur utan um allar aðgerðir þínar í notandaviðmótinu.
7. Farðu á hinar ýmsu síður og aðgerðir í [!INCLUDE[prod_short](includes/prod_short.md)] sem þú vilt að notendur með þessa heimildasamstæðu fái aðgang að. Þú verður að ljúka verkinu sem ætlunin er að skrá heimildir fyrir.
8. Þegar á að ljúka við skráningu er farið aftur á síðuna **Heimildir** og svo valið **Stöðva** aðgerðina.
9. Velja **Já** hnappinn til að bæta skráð heimildir við nýja heimildasafnið.
10. Fyrir hvern hlutar á skráningar listanum, tilgreinið ef notendur geta sett inn, breytt eða eytt skráningum í skráningartöflunum.

## <a name="security-filters---to-limit-a-users-access-to-specific-records-in-a-table"></a>Öryggisafmarkanir - Að takmarka aðgang notanda að tilteknum færslum í töflu

Fyrir öryggi á færslustigi í [!INCLUDE[prod_short](includes/prod_short.md)] notarðu öryggissíur til að takmarka aðgang notanda að gögnum í töflu. Þú býrð til öryggissíur á töflugögnum. Öryggissía lýsir færslusafni í töflu sem notandi hefur aðgangsheimild að. Þú getur til dæmis tilgreint að notandi geti aðeins lesið færslur sem innihalda upplýsingar um tiltekinn viðskiptavin. Þetta þýðir að notandinn getur ekki nálgast færslur sem innihalda upplýsingar um aðra viðskiptavini. Nánari upplýsingar eru í [Að nota öryggissíur](/dynamics365/business-central/dev-itpro/security/security-filters) í Developer og IT Pro hjálpinni.

## <a name="to-manage-permissions-through-user-groups"></a>Að stjórna heimildum í gegnum notendaflokka

Þú getur sett upp notendahópa til að hjálpa þér að stjórna heimildasamstæðum fyrir hópa notenda í fyrirtæki þínu.

Þú byrjar á því að stofna notendahóp. Síðan úthlutarðu heimildasamstæðum til hópsins til að skilgreina hvaða hluti notendur hópsins hafa aðgang að. Þegar þú bætir notanda í hópinn gilda heimildasamstæður sem skilgreindar eru fyrir hópinn líka fyrir notandann.

Heimildasett sem er úthlutað til notanda í gegnum notendahóp er áfram samstillt þannig að breyting á heimildum notendahópsins ná sjálfkrafa til notandans. Ef þú fjarlægir notanda úr notendahópi eru heimildir viðkomandi afturkallaðar sjálfkrafa.

### <a name="to-group-users-in-user-groups"></a>Til hópnotenda í notandaflokkum

Eftirfarandi ferli útskýrir hvernig á að búa til notendaflokka handvirkt. Til að búa til notendaflokka sjálfkrafa skal skoða [Að afrita notendaflokk og allar heimildasamstæður hans](ui-define-granular-permissions.md#to-copy-a-user-group-and-all-its-permission-sets).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendahópar** og veldu síðan tengda tengilinn.
2. Einnig, á síðunni **Notendur**, veldu aðgerðina **Notandaflokkar**.
3. Á síðunni **Notandaflokkur** er valin aðgerðin **Meðlimir notandaflokks**.
4. Á síðunni **Meðlimir notandaflokks** er valin aðgerðin **Bæta við notendum**.

### <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Til að afrita notendaflokk og öll heimildarsöfn

Til að fljótt skilgreina nýja notendaflokka geturðu afritað öll heimildarsöfn frá núgildandi notendaflokki yfir í nýjan notendaflokk.

> [!NOTE]
> Meðlimir úr notendaflokki eru ekki afritaðar í nýja notendaflokkinn. Þú verður að bæta þeim við handvirkt eftir á. Nánari upplýsingar er að finna í [Að flokka notendur í notendaflokka](ui-define-granular-permissions.md#to-group-users-in-user-groups).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendahópar** og veldu síðan tengda tengilinn.
2. Veldu notendaflokkinn sem þú vilt afrita og veldu síðan aðgerðina **Afrita notendaflokk**.
3. Í reitinn **Nýr kóði notendaflokks** skal færa inn heiti fyrir flokkinn og velja síðan hnappinn **Í lagi**.

Nýja notendaflokknum er bætt við síðuna **Notendaflokkar**. Halda áfram að bæta við notendum. Nánari upplýsingar er að finna í [Að flokka notendur í notendaflokka](ui-define-granular-permissions.md#to-group-users-in-user-groups).  

### <a name="to-assign-permission-sets-to-user-groups"></a>Til að úthluta leyfishópum á notendahópa

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendahópar** og veldu síðan tengda tengilinn.
2. Veldu notendaflokkinn sem á að úthluta á þessum heimildum til.
Öll heimildasöfn sem er nú þegar úthlutuð til notandans eru birtar í upplýsingakassanum **Heimildasöfn**.
3. Veldu aðgerðina **Heimildasamstæður notanda** til að opna síðuna **Heimildasamstæður notanda**.
4. Á síðunni **Heimildasöfn notanda** skal fylla út reitina eins og þörf krefur í nýrri línu.

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a>Til að úthluta heimildasamstæðu á síðunni **Heimildasamstæða eftir notendahópum**

Eftirfarandi ferli útskýrir hvernig á að úthluta heimildasamstæðum til notanda á síðunni **Heimildasamstæða eftir notendahópum**.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notendur** og veldu síðan tengda tengilinn.
2. Á síðunni **Notendur** skal velja viðeigandi notanda, og þá velja aðgerðina **Heimildasamstæða eftir notendahópum**.
3. Á síðunni **heimildasamstæða eftir notanda** veldu **[nafn notendaflokks]** gátreitinn á línu fyrir viðkomandi heimildasamstæðu til að tengja samstæðuna við notandann.
4. Veldu **Allir notendahópar** gátreitinn til að úthluta heimildasamstæðunni til allra notenda.

## <a name="to-remove-obsolete-permissions-from-all-permission-sets"></a>Til að fjarlægja úreltar heimildir úr öllum heimildasamstæðum

1. Á síðunni **Heimildasamstæður** skal velja aðgerðina **Fjarlægja úreltar heimildir**.

## <a name="to-set-up-user-time-constraints"></a>Til að setja upp tímaskorður notanda

Stjórnendur geta skilgreint tímabil þegar tilgreindir notendur geta bókað, og geta einnig tilgreint hvort kerfið skrái tímann sem notandinn er skráður inn. Stjórnendur geta einnig úthlutað ábyrgðarstöðvum á notendur. Frekari upplýsingar eru í [Vinna með ábyrgðarstöðvar](inventory-responsibility-centers.md).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notandauppsetning** og veldu síðan tengda tengilinn.
2. Á síðunni **Notandauppsetning** opnast, skal velja **Nýtt** aðgerð.
3. Í reitnum **Kenni notanda**, skal færa inn kenni notanda, eða velja reitinn til að sjá alla núverandi Windows notendur innan kerfisins.
4. Fyllið inn reitina eftir þörfum.


## <a name="viewing-permission-changes-telemetry"></a>Skoða fjarmælingar heimildabreytinga 

Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að senda breytingar sem eru gerðar á heimild á Application Insights tilfang í Microsoft Azure. Síðan er hægt að nota Azure Monitor til að búa til skýrslur og setja upp viðvaranir í söfnuðum gögnum. Frekari upplýsingar eru í eftirfarandi greinum í [!INCLUDE[prod_short](includes/prod_short.md)] Developer og IT Pro Help:

- [Fylgjast með og greina fjarmælingar - Virkja Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Greining fjarmælinga reitarvöktunar](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## <a name="see-also"></a>Sjá einnig

[Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md)  
[Vinna með forstillingar](admin-users-profiles-roles.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Sérstillir [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Stjórnun](admin-setup-and-administration.md)  
[Bæta notendum við Microsoft 365 for Business](https://aka.ms/CreateOffice365Users)  
[Öryggi og vernd í Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) í Developer og ITPro hjálp


[!INCLUDE[footer-include](includes/footer-banner.md)]