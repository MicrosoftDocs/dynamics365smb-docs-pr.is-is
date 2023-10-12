---
title: Skilgreina nákvæmari heimildir
description: Þessi grein lýsir því hvernig á að skilgreina nákvæmar heimildir og úthluta hverjum notanda heimildasamstæðum sem viðkomandi þarf til að vinna verk sín.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
---

# Úthluta leyfum til notenda og hópa

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

Öryggiskerfi [!INCLUDE[prod_short](includes/prod_short.md)] gerir þér kleift að stjórna því hvaða hluti notandi hefur aðgang að í hverjum gagnagrunni eða umhverfi fyrir sig, ásamt heimild notanda. Fyrir hvern notanda getur þú tilgreint hvort viðkomandi geti lesið, breytt eða slegið inn gögn í gagnagrunnshluti. Frekari upplýsingar eru í [Gagnaöryggi](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) í þróunar- og stjórnunarefni fyrir [!INCLUDE[prod_short](includes/prod_short.md)].

Áður en þú úthlutar heimildum til notenda og notendaflokka þarftu að skilgreina hverjir geta skráð sig inn með því að búa til notendur samkvæmt leyfi. Nánari upplýsingar er að finna í [Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md)

Í [!INCLUDE[prod_short](includes/prod_short.md)] eru tvö stig heimilda fyrir gagnagrunnshluti:

- Heildarheimildir í samræmi við leyfi, einnig nefnt réttindi.

  Leyfin innihalda sjálfgefin heimildasamstæður. Frá og með útgáfutímabili 1 árið 2022 geta stjórnendur sérsniðið þessar sjálfgefnu heimildir fyrir viðeigandi heimildategundir. Sjá [Stilla uppruna miðað við heimildir](ui-how-users-permissions.md#licensespermissions) fyrir frekari upplýsingar.  

- Ítarlegar heimildir sem þú úthlutar í [!INCLUDE[prod_short](includes/prod_short.md)].

Í greininni er lýst hvernig skilgreina á, nota og beita heimildum í  [!INCLUDE [prod_short](includes/prod_short.md)]  til að breyta sjálfgefnu samskipanin.  

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]  
Frekari upplýsingar eru í [Úthlutaður stjórnendaaðgangur að Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

[!INCLUDE [prod_short](includes/prod_short.md)] á netinu felur í sér sjálfgefna notendahópa sem eru úthlutað til notenda sjálfkrafa byggt á heimildum þeirra. Hægt er að breyta sjálfgefnu skilgreiningunni með því að breyta eða bæta við öryggisflokkum, heimildastæðum og heimildum. Eftirfarandi tafla sýnir helstu sviðsmyndir til að breyta sjálfgefnum heimildum.  

|Til  |Sjá  |
|---------|---------|
|Til að auðvelda stjórnun á heimildum margra notenda er hægt að skipuleggja þær í öryggisflokkum og úthluta þeim eða breyta einum heimildamengi fyrir marga notendur í einni aðgerð.| [Að stjórna heimildum í gegnum notendaflokka](#to-manage-permissions-through-user-groups) |
|Til að hafa umsjón með heimildasamstæðum fyrir tiltekna notendur | [Til að úthluta heimildasamstæðu á notendur](#to-assign-permission-sets-to-users) |
|Til að læra að skilgreina heimildasamstæðu|[Til að búa til heimildasamstæðu](#to-create-a-permission-set)|
|Til að skoða eða leita úrræða fyrir heimildir notanda|[Fá yfirlit yfir heimildir notanda](#to-get-an-overview-of-a-users-permissions)|
|Læra um öryggi á færslustigi|[Öryggissíur takmarka aðgang notanda að tilteknum færslum í töflu](#security-filters-limit-a-users-access-to-specific-records-in-a-table)|

> [!NOTE]
> Víðtækari leið til að skilgreina hvaða eiginleika notendur hafa aðgang að er að stilla reitinn **Upplifun** á síðunni **Fyrirtæki**. Frekari upplýsingar er að finna í [Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md).
>
> Einnig er hægt að skilgreina þá eiginleika sem standa notendum til boða í notendaviðmótinu og hvernig þeir eiga í samskiptum við þá í gegnum síður. Þetta er gert í gegnum forstillingar sem þú úthlutar til mismunandi notenda í samræmi við starfshlutverk þeirra eða deild. Frekari upplýsingar er að finna í [Vinna með forstillingar](admin-users-profiles-roles.md) og [Sérstillingar [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md).

## Til að stofna heimildasamstæðu

> [!NOTE]
> Árið 2022 á útgáfutímabili 2 gerðum við auðveldara að bæta heimildum við heimildasamstæður. Í stað þess að bæta við heimildum fyrir sig er hægt að bæta við heilum heimildasamstæðum. Ef þörf er á er svo hægt að útiloka einstakar heimildir í þeim. Fyrir frekari upplýsingar sjá [Til að bæta við öðrum heimildasamstæðum](#to-add-other-permission-sets). Til að gera það mögulegt höfum við skipt út síðu heimildasamstæðna fyrir nýja. Helsti munurinn eru nýju **Heimildasamstæðurnar** og glugginn **Niðurstöður** og upplýsingareiturinn **Innifaldar heimildir**. Til að halda áfram að nota Heimildarsíðuna sem var skipt út á síðunni **Heimildasamstæður**, skaltu velja aðgerðina **Heimildir (eldra efni)**.

Einnig er auðveldara að sinna viðhaldi. Þegar kerfisleyfi er bætt við uppfærist notandaskilgreind heimildauppsetning sjálfkrafa með öllum breytingum sem Microsoft gerir á heimildum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Heimildasamstæður** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
3. Fyllt er í reitina í nýju línunni. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Veljið aðgerðina **Heimildir**.
5. Á síðunni **Heimildasamstæða** í reitnum **Tegund** skal setja inn eða útiloka heimildir fyrir hlutinn sem hér segir:

  Til að setja inn heimildina skal velja **Innifela** og veljið síðan aðgangsstig til að veita í reitunum **Lesa heimild**, **Setja inn heimild**, **Breyta heimild**, **Eyða heimild** og **Framkvæma heimild**. Eftirfarandi tafla lýsir valkostunum.

  |Valkostur|Lýsing|Einkunn|
  |------|-----------|-------|
  |**Autt**|Notandinn getur ekki framkvæmt aðgerðina á hlutnum.|Lægstur|  
  |**Já**|Notandinn getur framkvæmt aðgerðina á hlutnum sem um ræðir.|Hæst|
  |**Óbeint**|Notandinn getur framkvæmt aðgerðina á hlutnum sem um ræðir en aðeins í gegnum aðra tengda hlut sem notandinn hefur fulla aðgang að. Frekari upplýsingar er að finna í [Dæmi - Óbein heimild](#example---indirect-permission) í þessari grein og [Eiginleiki heimilda](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property#example---indirect-permission) í hjálp fyrir þróunaraðila og hugbúnaðarsérfræðinga.|Næst hæsta|
  
  Til að útiloka heimildina eða eitt eða fleiri aðgangsstig skal velja **Útiloka** og velja svo aðgangsstigið sem á að veita. Eftirfarandi tafla lýsir valkostunum.

  |Valkostur|Lýsing|
  |------|-----------|-------|
  |**Autt**|Nota aðgangsstig miðað við stigveldi heimilda í samstæðunni.  |
  |**Útiloka**|Fjarlægja tiltekið aðgangsstig fyrir hlutinn.|
  |**Minnka í óbeint**|Breyta aðgangsstigi í Óbeint ef einhverjar heimildasamstæður veita Beinan aðgang að hlutnum. Til dæmis, veldu þennan valkost ef heimildarsamstæðan gefur þér beinan aðgang að fjárhagsfærslum en þú vilt ekki að notendur hafi fullan aðgang að færslunum.|
  
  > [!NOTE]
  > Ef heimild er í heimildaskrá sem er innifalin og er einnig í heimildaskrá sem er undanskilin, þá er heimildin undanskilin.

6. Notaðu reitina **Tegund hlutar** og **Kenni hlutar** til að tilgreina hlutinn sem þú veitir aðgang að.

  > [!TIP]
  > Nýjar línur sýna sjálfgildi. Til dæmis inniheldur reiturinn fyrir **Tegund hlutar** **Töflugögn** og reiturinn fyrir **Kenni hlutar** inniheldur **0**. Sjálfgildin eru bara staðgenglar og eru ekki notuð. Þú verður að velja tegund hlutar og hlut í reitnum fyrir **Kenni hlutar** áður en þú getur búið til nýja línu.

7. Valfrjálst: Ef þú ert að skilgreina heimildir fyrir tegund töfluhluta í reitnum **Öryggissía** getur þú síað gögnin sem notandi hefur aðgang að í reitunum á völdu töflunni. Til dæmis, þú gætir viljað leyfa notanda að fá aðeins aðgang að skrám sem innihalda upplýsingar um tiltekinn viðskiptavin. Frekari upplýsingar eru í [Öryggissíur takmarka aðgang notanda að tilteknum færslum í töfl](#security-filters-limit-a-users-access-to-specific-records-in-a-table) og [Að nota öryggissíur](/dynamics365/business-central/dev-itpro/security/security-filters).
8. Valfrjálst: Í glugganum **Heimildasamstæður** skaltu bæta við einu eða fleiri heimildasamstæðum. Fyrir frekari upplýsingar sjá [Til að bæta við öðrum heimildasamstæðum](#to-add-other-permission-sets).

> [!IMPORTANT]
> Fara skal varlega þegar **Setja inn heimild** eða **Breyta heimild** er úthlutað töflunni **9001 Meðlimur í notendahópi** eða **9003 Heimildasamstæða notendahóps**. Öllum notendum sem úthlutað er heimildasamstæðunni geta mögulega úthlutað sér í aðra notendahópa sem fyrir vikið getur veitt þeim heimildir sem þeir eiga ekki að hafa.

### Dæmi - Óbein heimild

Hægt er að úthluta Óbeinni heimild til að leyfa notanda að nota hlut, en aðeins í gegnum annan hlut. Til dæmis getur notandi haft heimild til að keyra kóðaeiningu 80, Sala-bókun. Sölubókun framkvæmir mörg verk, þar á meðal að breyta töflu 37, Sölulína. Þegar notandinn bókar söluskjal athugar Sala-Bókun kóðaeiningin, [!INCLUDE[prod_short](includes/prod_short.md)] hvort að notandinn hafi heimild til að breyta töflunni Sölulína. Ef svo er ekki getur kóðaeiningin ekki lokið við verkefni sín og þá munu villuboð birtast notandanum. Ef svo er verður kótaeiningin keyrð.

Hins vegar þarf notandi ekki að hafa ótakmarkaðan aðgang að töflunni Sölulína til að keyra kóðaeininguna. Ef notandinn hefur óbeina heimild fyrir töflunni Sölulína keyrir kóðaeiningin Sala-bókun án vandræða. Þegar notandi hefur óbeina heimild, getur sá notandi aðeins breytt töflunni Sölulína með því að keyra Sölubókun kóðaeiningunni eða annan hlut sem hefur heimild til að breyta töflunni Sölulína. Notandinn getur aðeins breytt töflunni Sölulína frá studdum forritssvæðum. Notandinn getur ekki keyrt eiginleikann óvart eða í sviksamlegum tilgangi á annan hátt.

### Til að bæta við öðrum heimildasettum

Stækkaðu heimildasamstæðu með því að bæta öðrum heimildasamstæðum við hana. Síðan er hægt að setja inn eða útiloka tilteknar heimildir, eða alla heimildasamstæðuna, í hverju setti sem þú bætir við. Þetta felur í sér heimildasamstæðum af gerðunum Kerfi og Viðbætur, sem annars er ekki leyfð. Undanþágur eiga aðeins við heimildasamstæðuna sem þú ert að stækka. Upprunalega samstæðan verður ekki fyrir áhrifum.

Á síðunni **Heimildasamstæður** skaltu bæta við heimildasamstæðu í glugganum **Heimildasamstæður**. Í glugganum **Niðurstaða** eru allar samstæður sem bætt hefur verið við. Til að skoða heimildirnar sem eru í samstæðunni sem þú bættir við velur þú stillingarnar í glugganum Niðurstöður og upplýsingakassinn **Innifaldar heimildir** sýnir heimildirnar.

Í glugganum **Niðurstöður** notar þú reitinn **Staða innfellingar** til að auðkenna heimildasamstæðu þar sem þú útilokar heimildir eða heimildasamstæður. Ef eitthvað hefur verið útilokað verður staðan **Að hluta til**.

Til að fá heildaryfirsýn yfir heimildir í heimildasamstæðu skal velja aðgerðina **Skoða allar heimildir**. Síðan **Útvíkkaðar heimildir** sýnir allar heimildir sem þegar hefur verið úthlutað í heimildasamstæðunni og heimildirnar í viðbættu heimildasamstæðunum.

Ef undanskilja á allar heimildir frá heimildarsafni  **í niðurstöðurúðunni**  skal velja línuna, velja  **Sýna fleiri valkosti** og velja  **síðan útiloka**. Þegar þú undanskilur heimildasamstæðu er búin til lína í glugganum **Heimildasamstæður** af gerðinni Útilokað. Ef þú hefur útilokað heimildasamstæðu en vilt láta það fylgja með aftur, skaltu eyða línunni í glugganum **Heimildasamstæður**.

Til að útiloka að fullu eða að hluta tiltekna heimildir í samstæðu sem þú hefur bætt við skaltu búa til línu fyrir hlutinn fyrir neðan **Heimildir**. Aðgangsstig svæðin, setja inn heimild, breyta heimild og þess háttar, munu öll innihalda  **útiloka**. Veljið viðeigandi valkost til að leyfa tiltekið aðgangsstig.

Heimild sett útilokar allar heimildir í settinu. [!INCLUDE [prod_short](includes/prod_short.md)] reiknar út heimildir á eftirfarandi hátt:

1. Reikna út heildarlista yfir innifaldar heimildir
2. Reikna út heildarlista yfir útilokaðar heimildir
3. Fjarlægja útilokaðar heimildir af listanum yfir innifaldar heimildir (að fjarlægja óbeina heimild er það sama og minnka við óbeina)

## Til að afrita heimildasamstæðu

Stofna skal nýja heimildasamstæðu með því að afrita annað. Nýja samstæðan mun innihalda allar heimildir og heimildasamstæður úr samstæðunni sem þú afritaðir. Hvernig heimildum og heimildasamstæðum er raðað í nýju heimildasamstæðuna er mismunandi, eftir því hvað þú velur í reitnum **Afritunaraðgerð**. Eftirfarandi tafla lýsir valkostunum.

|Valkostur  |Lýsing  |
|---------|---------|
|**Afrita eftir tilvísun**     | Upprunalega heimildasamstæðan og allar heimildasamstæðurnar sem bætt var við það eru skráð í glugganum **Niðurstöður**.       |
|**Flöt afritun heimilda**  | Allar heimildir frá öllum heimildasamstæðum eru á flötum lista í glugganum **Heimildir**. Heimildir eru ekki skipulagðar eftir heimildasamstæðu.        |
|**Klóna**     | Búðu til nákvæmt afrit af upprunalegu heimildasamstæðunni.        |

1. Á síðunni **heimildasamstæður** skaltu velja línuna fyrir heimildasamstæðu sem þú vilt afrita og síðan velja **Afrita heimildasamstæðu** aðgerðina.
2. Á síðunni **Afrita heimildasamstæðu** skaltu tilgreina nafn hinna nýju heimildasamstæðu.
3. Í reitnum **Afritunaraðgerð** skal tilgreina hvernig á að raða heimildum í nýju heimildasamstæðunni.
4. Valfrjálst: Ef þú bætir við heimildasamstæðu fyrir kerfið geturðu valið um að fá tilkynningu ef heiti eða efni upprunalegu heimildasamstæðunnar breytist í nýrri útgáfu. Þetta gerir þér kleift að íhuga hvort uppfæra eigi heimildasamstæðuna fyrir notanda. Kveiktu á valkostinum **Tilkynna um breyttan heimildasamstæðu** að fá tilkynningu.

> [!NOTE]
> Tilkynningin krefst þess að tilkynningin **Heimildasamstæðu upprunalegs kerfis hefur verið breytt** sé virk á síðunni **Mínar tilkynningar**.

## Að stofna eða breyta heimildum með skráning við aðgerðir þínar

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Heimildasamstæður** og velja síðan viðkomandi tengil.

    Einnig, á síðunni **Notendur**, veldu aðgerðina **Heimildarsöfn**.
2. Á síðunni **Heimildarsöfn**, veldu aðgerðina **Nýtt**.
3. Fyllið í reitina eftir þörfum í nýrri línu.
4. Veljið aðgerðina **Heimildir**.
5. Á síðunni **Heimildir** skal velja aðgerðina **Skrá heimildir** og velja svo aðgerðina **Byrja**.  
    Upptöku verður að gera annaðhvort með því að nota  **opna þessa síðu í nýjum gluggum**  (POP-Out) til að hafa  **heimildaskráningargluggann**  hlið við hlið, eða með því að vinna innan sama flipa.  
    Upptökuferli hefst nú og tekur allar aðgerðirnar með sér inn í notendaviðmótið.
6. Farðu á hinar ýmsu síður og aðgerðir í [!INCLUDE[prod_short](includes/prod_short.md)] sem þú vilt að notendur með þessa heimildasamstæðu fái aðgang að. Þú verður að ljúka verkinu sem ætlunin er að skrá heimildir fyrir.
7. Þegar á að ljúka við skráningu er farið aftur á síðuna **Heimildir** og svo valið **Stöðva** aðgerðina.
8. Velja **Já** hnappinn til að bæta skráð heimildir við nýja heimildasafnið.
9. Fyrir hvern hlut á skráningarlistanum, tilgreinið ef notendur geta sett inn, breytt eða eytt skráningum í skráningartöflunum.

### Til að flytja út og flytja inn heimildasamstæðu

Til að setja upp heimildir á skjótan máta geturðu flutt inn heimildasamstæður sem þú hefur flutt út frá öðrum [!INCLUDE[prod_short](includes/prod_short.md)] leigjanda.

Í umhverfi margra leigjenda er heimildasamstæða flutt inn í tiltekinn leigjanda. Með öðrum orðum, umfang innflutningsins er *Leigjandi*.

1. Á leigjanda 1, á síðunni **Heimildasamstæður** skaltu velja línuna eða línurnar fyrir heimildasamstæður sem á að flytja út og velja síðan aðgerðina **Flytja út heimildasamstæður**.

    XML-skrá er útbúin í niðurhalsmöppunni á tölvunni þinni. Sjálfgefið er að heitið sé *Flytja út heimildasamstæður.xml*.

2. Á leigjanda 2, á síðunni **Heimildasamstæður** skaltu aðgerðina **Flytja inn heimildasamstæður**.
3. Á síðunni **Flytja inn heimildasamstæður** þarf að íhuga hvort sameina á fyrirliggjandi heimildasamstæður nýjum heimildasamstæðum í XML-skránni.

    Ef þú velur gátreitinn **Uppfæra fyrirliggjandi heimildir** eru fyrirliggjandi heimildasamstæður sem samsvara nöfnum í XML-skránni sameinaðar innfluttum heimildasamstæðum.

    Ef þú velur ekki gátreitinn **Uppfæra fyrirliggjandi heimildir** er heimildasamstæðunum sem samsvara nöfnum í XML-skránni sleppt við innflutninginn. Í þeim tilvikum verður þér tilkynnt um heimildasamstæður sem er sleppt.

4. Á staðfestingarsíðunni **Innflutningur** skaltu finna og velja XML-skrána sem á að flytja inn og velja svo aðgerðina **Opna**.

Heimildasamstæðurnar eru fluttar inn.

## Til að fjarlægja úreltar heimildir úr öllum heimildasamstæðum

Á síðunni **Heimildasamstæður** skal velja aðgerðina **Fjarlægja úreltar heimildir**.

## Uppsetning tímaskorta fyrir notendur

Stjórnendur geta skilgreint tímabil þegar tilgreindir notendur geta bókað. Stjórnendur geta einnig tilgreint ef kerfið skráir hve mikinn tíma notendur eru skráðir inn. Á svipaðan hátt geta stjórnendur úthlutað ábyrgðarstöðvum á notendur. Frekari upplýsingar eru í [Vinna með ábyrgðarstöðvar](inventory-responsibility-centers.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning notanda** og velja síðan viðkomandi tengil.
2. Á síðunni **Notandauppsetning** opnast, skal velja **Nýtt** aðgerð.
3. Í reitnum **Kenni notanda**, skal færa inn kenni notanda, eða velja reitinn til að sjá alla núverandi Windows notendur innan kerfisins.
4. Fyllið inn reitina eftir þörfum.

## Að stjórna heimildum í gegnum notendaflokka

Notendaflokkar hjálpa við að stjórna heimildasamstæðum í fyrirtækinu. [!INCLUDE [prod_short](includes/prod_short.md)] á netinu felur í sér sjálfgefna notendahópa sem eru úthlutað til notenda sjálfkrafa byggt á heimildum þeirra. Hægt er að bæta notendum handvirkt við notendahóp og búa til nýja notendahópa sem afrit af fyrirliggjandi.  

Þú byrjar á því að stofna notendahóp. Síðan úthlutarðu heimildasamstæðum til hópsins til að skilgreina hvaða hluti notendur hópsins hafa aðgang að. Þegar þú bætir notanda í hópinn gilda heimildasamstæður sem skilgreindar eru fyrir hópinn líka fyrir notandann.

Heimildasamstæður sem úthlutað er notanda í gegnum notendahóp haldast samstilltar. Breyting á heimildum notendahópsins er sjálfkrafa birt notendum. Ef þú fjarlægir notanda úr notendahópi eru heimildir viðkomandi afturkallaðar sjálfkrafa.

### Til að bæta notendum í notendahóp

Eftirfarandi ferli útskýrir hvernig á að búa til notendaflokka handvirkt. Til að búa til notendaflokka sjálfkrafa skal skoða [Að afrita notendaflokk og allar heimildasamstæður hans](#to-copy-a-user-group-and-all-its-permission-sets).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendaflokkar** og velja síðan viðkomandi tengil.

    1. Einnig, á síðunni **Notendur**, veldu aðgerðina **Notandaflokkar**.
2. Á síðunni **Notandaflokkur** er valin aðgerðin **Meðlimir notandaflokks**.
3. Á síðunni **Meðlimir notandaflokks** er valin aðgerðin **Bæta við notendum**.

### Til að afrita notendaflokk og öll heimildarsöfn

Til að fljótt skilgreina nýja notendaflokka geturðu afritað öll heimildarsöfn frá núgildandi notendaflokki yfir í nýjan notendaflokk.

> [!NOTE]
> Meðlimir úr notendaflokki eru ekki afritaðar í nýja notendaflokkinn. Þú verður að bæta þeim við handvirkt eftir á. Nánari upplýsingar eru í hlutanum [Til að bæta notendum í notendahóp](#to-add-users-to-a-user-group).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendaflokkar** og velja síðan viðkomandi tengil.
2. Veldu notendaflokkinn sem þú vilt afrita og veldu síðan aðgerðina **Afrita notendaflokk**.
3. Í reitinn **Nýr kóði notendaflokks** skal færa inn heiti fyrir flokkinn og velja síðan hnappinn **Í lagi**.

Nýja notendaflokknum er bætt við síðuna **Notendaflokkar**. Halda áfram að bæta við notendum. Nánari upplýsingar eru í hlutanum [Til að bæta notendum í notendahóp](#to-add-users-to-a-user-group).  

> [!IMPORTANT]
> Þú færð staðfestingarvillu ef þú ert að reyna að úthluta notendahópi til notandans sem vísar í heimildasamstæðu sem var skilgreint í óuppsettri viðbót. Það er vegna þess að forritskenni viðbótarinnar er staðfest í hvert sinn sem vísað er til þess. Til að úthluta notendahóp til notanda getur þú annað hvort enduruppsett viðbótina, fjarlægt tilvísun óuppfærðu viðbótarinnar úr heimildasamstæðunni eða fjarlægt heimildasamstæðuna úr notendahópnum.

### Til að úthluta leyfishópum á notendahópa

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendaflokkar** og velja síðan viðkomandi tengil.
2. Veldu notendaflokkinn sem á að úthluta á þessum heimildum til.  

    Öll heimildasöfn sem er nú þegar úthlutuð til notandans eru birtar í upplýsingakassanum **Heimildasöfn**.
3. Veldu aðgerðina **Heimildasamstæður notanda** til að opna síðuna **Heimildasamstæður notanda**.
4. Á síðunni **Heimildasöfn notanda** skal fylla út reitina eins og þörf krefur í nýrri línu.

### Til að úthluta heimildasamstæðu á síðunni **Heimildasamstæða eftir notendahópum**

Eftirfarandi ferli útskýrir hvernig á að úthluta heimildasamstæðum til notanda á síðunni **Heimildasamstæða eftir notendahópum**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.
2. Á síðunni **Notendur** skal velja viðeigandi notanda, og þá velja aðgerðina **Heimildasamstæða eftir notendahópum**.
3. Á síðunni **heimildasamstæða eftir notanda** veldu **[nafn notendaflokks]** reitinn á línu fyrir viðkomandi heimildasamstæðu til að tengja samstæðuna við notandann.
4. Veldu **Allir notendahópar** gátreitinn til að úthluta heimildasamstæðunni til allra notendahópa.

Einnig er hægt að úthluta heimildasamstæðum beint til notanda.

## Til að úthluta heimildasamstæðu á notendur

Heimildasamstæða er safn heimilda fyrir tiltekna gagnagrunnshluti. Öllum notendum verða að hafa verið úthlutað eitt eða fleiri heimildasöfn áður en þeir geta opnað [!INCLUDE[prod_short](includes/prod_short.md)].  

[!INCLUDE[prod_short](includes/prod_short.md)] Lausn inniheldur fjölda fyrirfram skilgreindra heimildasamstæðna sem eru bætt við af Microsoft eða þjónustuveitunni þinni. Þú getur einnig bætt við nýjum heimildasamstæðum sem eru sniðin að þörfum fyrirtækisins. Nánari upplýsingar er að finna í [Til að búa til heimildasamstæðu](#to-create-a-permission-set).

> [!NOTE]
> Ef þú vilt ekki takmarka aðgang notanda meira en þegar hefur verið skilgreint með leyfi geturðu úthlutað notanda sérstakri heimildasamstæðu sem kallast SUPER. Þessi heimildasamstæða tryggir að notandinn geti fengið aðgang að öllum hlutum sem eru tilgreindir í leyfi.
>
> Notandi með nauðsynlegt leyfi og SUPER-heimildasamstæðuna hefur aðgang að meiri virkni en notendur með Team Member-leyfið og SUPER-heimildasamstæðuna.

Þú getur úthlutað heimildarhópum til notenda á tvo vegu:

- Af **Notandaspjald** síðunni með því að velja heimildasamstæður til að úthluta notandanum.
- Frá síðunni **Heimildasamstæða eftir notendum** með því að velja notendur sem heimildasamstæðu er úthlutað til.

### Til að úthluta heimildasamstæðu á notendakorti

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.
2. Veldu notandann sem á að úthluta á þessum viðskiptamanni til.
Öll heimildasöfn sem er nú þegar úthlutuð til notandans eru birtar í upplýsingakassanum **Heimildasöfn**.
3. Veldu **breyta** aðgerðina til að opna síðuna **Notandapjald** .
4. Á flýtiflipanum **Heimildasöfn notanda** skal fylla út reitina eins og þörf krefur í nýrri línu. Nánari upplýsingar er að finna í [Að búa til eða breyta heimildasamstæðum](ui-define-granular-permissions.md#to-create-a-permission-set).

### Til að úthluta heimildasamstæðu á síðunni Heimildasamstæða eftir notanda

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.
2. Á síðunni **Notendur** skal velja aðgerðina **Heimildasamstæða eftir notanda**.
3. Á síðunni **Heimildasamstæða eftir notanda** veldu **[notandanafnið]** gátreitinn á línu fyrir viðkomandi heimildasamstæðu til að úthluta notandanum samstæðuna.

    Veldu **Allir notendur** gátreitinn til að úthluta heimildasamstæðunni til allra notenda.

## Fá yfirlit yfir heimildir notanda

Aðeins er hægt að skoða virkar heimildir annarra notenda fyrir öryggi eða SUPER aðgangsheimildir. 

Í  **síðunni skilvirkar heimildir**  er að ræða viðbótarupplýsingar um uppruna hvers leyfis. Til dæmis hvort Uppruni er Öryggisflokkur, eða heimild erfist. Á síðunni er einnig dálkur þar sem stjórnendur geta farið yfir öryggisafmarkanir sem beitt er. Til að fá meiri upplýsingar um Öryggisafmarkanir er farið í  [öryggisafmarkanir til að takmarka aðgang notanda að tilteknum færslum í töflu](#security-filters-limit-a-users-access-to-specific-records-in-a-table).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.
2. Opnaðu kort viðkomandi notanda.
3. Velja **Virkar heimildir** aðgerð.

    **Heimildir** hlutinn listar allar gagnagrunnshlutir sem notandinn hefur aðgang að. Ekki er hægt að breyta þessum hluta.

    **Eftir heimildasamstæðu** hlutinn sýnir þær úthlutaðar heimildasamstæður sem notandinn fær heimildir sínar í gegnum, uppruna og gerð heimildasamstæðunnar, og að hvaða marki mismunandi aðgangsgerðir eru leyfðar.

    Fyrir hverja röð sem þú velur í **heimildir** hlutanum, sýnir **eftir heimildasamstæðu** hlutinn hvaða heimildasamstæða eða -samstæður heimildin er veitt í gegnum. Í þessum kafla er hægt að breyta gildinu í hverjum af fimm reitum aðgangsgerðar, **Lesa heimild**, **Setja inn heimild**, **Breyta heimild**, **Eyða heimild**, **Framkvæma heimild**.

    > [!NOTE]  
    > Einungis heimildasamstæður af tegund **Notandaskilgreint** geta verið breytt.
    >
    > Línur uppruna réttinda eru komnar frá áskriftarleyfinu. Heimildagildi réttindanna yfirtaka gildi í öðrum heimildasamstæðum ef þeir hafa hærri röðun. Gildi í réttindalausri heimildasamstæðu sem hefur hærra röðun en tengt gildi í réttindunum verður innan sviga til að gefa til kynna að það sé ekki virkt, þar sem það verður yfirtekið af réttindunum.
    >
    > Útskýringar á röðun er að finna í [Til að búa til heimildasamstæðu](ui-define-granular-permissions.md#to-create-a-permission-set).  

4. Til að breyta heimildasamstæðu skaltu í **Eftir heimildasamstæðu** hlutanum, á línu fyrir viðeigandi heimildasamstæðu af tegund **Notandaskilgreint**, skaltu velja einn af fimm reitum aðgangsgerðar og velja annað gildi.

5. Til að breyta einstökum heimildum innan heimildasamstæðunnar skaltu velja gildi í **heimildasamstæðu** gluttanum til að opna **Heimildir** gluggann.

> [!NOTE]  
> Þegar þú breytir heimildasamstæðu munu breytingarnar einnig eiga við um aðra notendur sem hafa heimildarsamstæðuna úthlutað.

### Öryggissíur takmarka aðgang notanda að tilteknum færslum í töflu

Fyrir öryggi á færslustigi í [!INCLUDE[prod_short](includes/prod_short.md)] notarðu öryggissíur til að takmarka aðgang notanda að gögnum í töflu. Þú býrð til öryggissíur á töflugögnum. Öryggissía lýsir færslusafni í töflu sem notandi hefur aðgangsheimild að. Þú getur til dæmis tilgreint að notandi geti aðeins lesið færslur sem innihalda upplýsingar um tiltekinn viðskiptavin. Á þennan hátt getur notandinn ekki nálgast skrárnar sem innihalda upplýsingar um aðra viðskiptavini. Sjá [Notkun öryggissía](/dynamics365/business-central/dev-itpro/security/security-filters) í efni fyrir stjórnendur fyrir frekari upplýsingar.

## Skoða fjarmælingar heimildabreytinga

Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að senda breytingar sem eru gerðar á heimild á Application Insights tilfang í Microsoft Azure. Síðan er hægt að nota Azure Monitor til að búa til skýrslur og setja upp viðvaranir í söfnuðum gögnum. Frekari upplýsingar eru í eftirfarandi hjálpargreinum í [!INCLUDE[prod_short](includes/prod_short.md)] fyrir forritara og stjórnendur:

- [Fylgjast með og greina fjarmælingar - Virkja Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Greining fjarmælinga reitarvöktunar](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## Úthlutaðir stjórnendur

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

## Sjá einnig

[Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md)  
[Vinna með forstillingar](admin-users-profiles-roles.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Sérstillir [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Stjórnun](admin-setup-and-administration.md)  
[Bæta notendum við Microsoft 365 fyrir fyrirtæki](/microsoft-365/admin/add-users/add-users)  
[Öryggi og vernd í Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) í Developer og ITPro hjálp  
[Úthluta notendum auðkenni fyrir fjarmælingu](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
