---
title: Skilgreina nákvæmari heimildir
description: Í greininni er fjallað um hvernig hægt er að skilgreina Kornastærð og úthluta hverjum notanda þeim heimildum sem leyfi setur að þeir þurfi að sinna störfum sínum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.search.form: 1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862
ms.date: 09/19/2022
ms.author: bholtorf
ms.openlocfilehash: d265566e21388978f9ee7cba9372d3d337cbf97e
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9604888"
---
# <a name="assign-permissions-to-users-and-groups"></a>Úthluta leyfum til notenda og hópa

[!INCLUDE[prod_short](includes/prod_short.md)] Öryggiskerfið stjórnar hvaða hlutum notandi getur opnað innan hvers gagnagrunns eða umhverfis, ásamt leyfi notandans. Fyrir hvern notanda er hægt að tilgreina hvort þeir geti lesið, breytt eða fært inn gögn í gagnagrunnshlutum. Nánari upplýsingar [fást í gagnaöryggi](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) í efni hönnuða og stjórnsýslu fyrir [!INCLUDE[prod_short](includes/prod_short.md)].

Áður en heimildum er úthlutað á notendur og notendaflokka þarf að skilgreina hverjir geta skráð sig inn með því að stofna notendur samkvæmt leyfi sínu. Nánari upplýsingar er að finna í [Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md)

Í [!INCLUDE[prod_short](includes/prod_short.md)] eru tvö stig heimilda fyrir gagnagrunnshluti:

- Heildarheimildir í samræmi við leyfi, einnig nefnt réttindi.

  Í leyfum eru sjálfgefin leyfi sett. Byrjað í 2022 1. viðurkenningar getur sérsniðið þessar sjálfgefnu heimildir að viðeigandi leyfistegundum. Nánari upplýsingar eru [í Configure aðgangsheimildir byggðar á leyfum](ui-how-users-permissions.md#licensespermissions).  

- Nákvæmar heimildir sem úthlutað er í [!INCLUDE[prod_short](includes/prod_short.md)].

  Í þessari grein er lýst hvernig hægt er að skilgreina, nota og beita heimildum í [!INCLUDE [prod_short](includes/prod_short.md)] til að breyta sjálfgefnu skilgreiningunni.  

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]  
Nánari upplýsingar [fást hjá fulltrúa kerfisstjóra á netinu](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

[!INCLUDE [prod_short](includes/prod_short.md)] á netinu eru sjálfgefnir notendaflokkar sem eru úthlutaðir notendum sjálfkrafa á grundvelli leyfis. Hægt er að breyta sjálfgefnu skilgreiningunni með því að breyta eða bæta við notendaflokkum, heimildaflokkum og heimildum. Eftirfarandi tafla lýsir lykilaðstæður til að breyta sjálfgefnum heimildum.  

|Til  |Sjá  |
|---------|---------|
|Til að auðvelda stjórnun heimilda fyrir marga notendur er hægt að skipuleggja þær í notendaflokkum og úthluta þeim síðan eða breyta einum heimildarmengi fyrir marga notendur í einni aðgerð.| [Heimildir til að stjórna heimildum í gegnum notendaflokka](#to-manage-permissions-through-user-groups) |
|Að stjórna heimildastæðum fyrir ákveðna notendur | [Notendum úthlutað heimildasöfn](#to-assign-permission-sets-to-users) |
|Að læra að skilgreina heimildasafn|[Til að stofna heimildarsafn](#to-create-a-permission-set)|
|Til að skoða eða leysa úr heimildum notanda|[Til að fá yfirsýn yfir heimildir notanda](#to-get-an-overview-of-a-users-permissions)|
|Fræðsla um öryggi á skráastigi|[Öryggissíur takmarka aðgang notanda að tilteknum færslum í töflu](#security-filters-limit-a-users-access-to-specific-records-in-a-table)|

> [!NOTE]
> Víðari leið til að skilgreina hvaða aðgerðir notendur hafa aðgang að er með því að stilla **upplifunarsvæðið** á **upplýsingasíðu** fyrirtækisins. Frekari upplýsingar er að finna í [Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md).
>
> Einnig er hægt að skilgreina aðgerðirnar sem eru tiltækar notendum í notendaviðmótinu og hvernig þeir hafa samskipti við þá í gegnum síður. Þetta er gert í gegnum forstillingar sem þú úthlutar til mismunandi notenda í samræmi við starfshlutverk þeirra eða deild. Frekari upplýsingar er að finna í [Vinna með forstillingar](admin-users-profiles-roles.md) og [Sérstillingar [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md).

## <a name="to-create-a-permission-set"></a>Til að stofna heimildarsafn

> [!NOTE]
> Í 2022 út bylgju 2 við gerðum það auðveldara að bæta heimildum við heimildasöfn. Frekar en að bæta við heimildum sérstaklega er hægt að bæta við öllu leyfi. Ef þörf krefur er síðan hægt að útiloka einstakar heimildir í þeim. Frekari upplýsingar er að finna [í til að bæta við öðrum heimildum](#to-add-other-permission-sets). Til þess að hægt sé að koma því við er skipt um Heimildasíðu með nýrri. Lykilmunir eru nýju heimildasetur **og** niðurstöður **rúðunet og Upplýsingakassi með þeim** heimildum **.** Hægt er að velja **aðgerðina heimildir (Legacy)** til að halda áfram að nota síðuna skiptar heimildir á **síðunni heimildstillir**.

Viðhald er einnig auðveldara. Þegar kerfisleyfi er bætt við uppfærist notandaskilgreinda heimildauppsetning sjálfkrafa með öllum breytingum sem Microsoft gerir á heimildum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Heimildasamstæður** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
3. Fyllt er í reitina í nýju línunni. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Veljið aðgerðina **Heimildir**.
5. **Á síðunni heimildagerð**, í **reitnum Tegund** skal hafa eða útiloka heimildir fyrir hlutinn á eftirfarandi hátt:

  Til að taka heimildina með er hægt að velja **taka með** og velja svo stig aðgangs til að gefa í **lesheimild**, **Setja inn heimild**, **Breyta heimild**, **Eyða heimild** og **keyra heimildasvæði**. Eftirfarandi tafla lýsir valkostunum.

  |Valkostur|Lýsing|Einkunn|
  |------|-----------|-------|
  |**Autt**|Notandinn getur ekki framkvæmt aðgerðina í hlutnum.|Lægstur|  
  |**Já**|Notandinn getur framkvæmt aðgerðina í hlutnum.|Hæst|
  |**Óbeint**|Notandinn getur framkvæmt aðgerðina á hlutnum en aðeins í gegnum annan tengdan hlut sem notandinn hefur fullan aðgang að. Frekari upplýsingar er að finna [í dæmi-óbein heimild](#example---indirect-permission) í þessari grein, og [Heimildaeign](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property#example---indirect-permission) í Developer og it-Pro hjálp.|Næst hæsta|
  
  Til að útiloka heimildina eða eitt eða fleiri aðgangsstig, veljið **þá útiloka** og veljið svo aðgangsstigið sem á að gefa. Eftirfarandi tafla lýsir valkostunum.

  |Valkostur|Lýsing|
  |------|-----------|-------|
  |**Autt**|Nota aðgangsstig sem byggir á stigveldi heimilda í settinu.  |
  |**Útiloka**|Fjarlægja skal tiltekinn aðgangsstig fyrir hlutinn.|
  |**Draga úr til óbeinna**|Breyta aðgangsstigi óbeint ef einhver heimildaleit veitir beinan aðgang að hlutnum. Til dæmis er þessi kostur valinn ef heimildaleitir gefa beinan aðgang að fjárhagsfærslum, en notendur eiga ekki að hafa fullan aðgang að færslunum.|
  
  > [!NOTE]
  > Hæsta heimild sem sett er í stigveldi ákvarðar hvort heimildin er tekin með eða er undanskilin. Ef tvö mengi eru á sama stigi í stigveldinu og heimild er innifalin í einu stæðu en undanskilin í hinni er heimildin undanskilin.

6. **Notið reitina Tegund** HLUTAR og **Kenni** hlutar til að tilgreina þann hlut sem verið er að veita aðgang að.

> [!TIP]
  > Nýjar línur Sýna sjálfgefin gildi. Í reitnum Tegund **hlutar er til dæmis** að finna **töflugögn** og **reiturinn** Hlutarkenni **er 0**. Sjálfgefnu gildin eru bara frátalin og eru ekki notuð. Velja verður tegund hlutar og hlut í **REITNUM kenni** hlutar áður en hægt er að stofna nýja línu.

7. Valfrjálst: Ef notandinn skilgreinir heimildir fyrir Töflugagnahlutargerð í **reitnum öryggisafmörkun** er hægt að afmarka gögnin sem notandinn hefur aðgang að í reitum í valinni töflu. Til dæmis væri æskilegt að láta notanda aðeins fá aðgang að færslum sem innihalda upplýsingar um tiltekinn viðskiptavin. Sjá [öryggisafmarkanir takmarka aðgang notanda að tilteknum færslum í töflu](#security-filters-limit-a-users-access-to-specific-records-in-a-table) og [með öryggisafmarkanir](/dynamics365/business-central/dev-itpro/security/security-filters).
8. Valfrjálst: á **rúðunni heimildasetur** er bætt við einu eða fleiri öðrum heimildum. Frekari upplýsingar er að finna [í til að bæta við öðrum heimildum](#to-add-other-permission-sets).

> [!IMPORTANT]
> Fara skal varlega þegar **Setja inn heimild** eða **Breyta heimild** er úthlutað töflunni **9001 Meðlimur í notendahópi** eða **9003 Heimildasamstæða notendahóps**. Allir notendur sem tengjast heimildsettinu geta hugsanlega úthlutað öðrum notendaflokkum sem aftur gætu gefið óleyfilegar heimildir.

### <a name="example---indirect-permission"></a>Dæmi - Óbein heimild

Hægt er að úthluta óbeinni heimild til að leyfa notanda að nota hlut, heldur aðeins í gegnum annan hlut. Til dæmis hefur notandi heimild til að keyra Codeunit 80, Sala-Post. Sölubókun framkvæmir mörg verk, þar á meðal að breyta töflu 37, Sölulína. Þegar notandi bókar söluskjal með því að nota Codeunit, [!INCLUDE[prod_short](includes/prod_short.md)] Athugar hvort notandinn hafi heimild til að breyta töflunni Sölulína. Ef svo er ekki getur Codeunit ekki klárað verk sín og notandinn fær villuskilaboð. Ef svo er verður kótaeiningin keyrð.

Notandinn þarf þó ekki að hafa fullan aðgang að töflunni Sölulína til að keyra Codeunit. Ef notandinn hefur óbeina heimild fyrir töfluna Sölulína, keyrir Sölueiningin Codeunit. Þegar notandi hefur óbeina heimild geta þeir aðeins breytt töflunni Sölulína með því að keyra sölulínu eða annan hlut sem hefur heimild til að breyta töflunni Sölulína. Notandinn getur aðeins breytt töflunni Sölulína frá studdum forritssvæðum. Notandinn getur ekki keyrt aðgerðina óboðlega eða með öðrum aðferðum.

### <a name="to-add-other-permission-sets"></a>Að bæta við öðrum heimildum sem settar eru

Útvíkka heimildasamstæðu með því að bæta öðrum stilliheimildum við hana. Á eftir er hægt að láta eða útiloka tilteknar heimildir, eða allt það sem valið er, í hverri samstæðu sem bætt er við. Hér er fjallað um heimildir í heimildum um endingu og kerfisgerð, sem að öðru leyti er ekki heimil. Útisetur eiga aðeins við um heimildaleit sem þú stækkar. Upprunalega settið er ekki undir áhrifum.

**Á síðunni heimildagildi** er bætt við heimild sem sett er **á rúðu heimildarinnar**. **Niðurstöðurúðan** sýnir öll bætt heimildasöfn. Til að kanna heimildir sem hafðar eru með í samstæðu sem bætt hefur verið við er valið í niðurstöðurúðunni og **Upplýsingakassi með heimildum** mun sýna heimildina.

**Í niðurstöðurúðunni** er reiturinn Staða **notkunar notaður** til að auðkenna heimildstæðin sem hafa verið undanskilin. Ef eitthvað hefur verið undanskilið verður **staðan að hluta**.

Til að skoða yfirlit yfir heimildir í heimildamengi er valið **Skoða allar aðgangsheimildir**. **Síðan útvíkkuð heimildir** sýnir allar heimildir sem þegar hafa verið tengdar heimildinni og heimildin í bætt heimildinni er sett fram.

Til að útiloka heimildasamstæðu sem þú hefur bætt við að fullu, í niðurstöðurúðunni **, skaltu velja línuna, velja** Sýna fleiri valkosti **og velja** síðan útiloka **.** Þegar heimild er undanskilin er lína stofnuð á **rúðunni heimild stillir** af tegundinni sem er útilokað. Ef þú hefur útilokað heimildasamstæðu, en vilt hafa hana aftur, skaltu eyða línunni á **rúðunni heimild setur**.

Að fullu eða að hluta tiltekið leyfi í samstæðu sem bætt hefur verið við, samkvæmt **heimildum**, stofnið línu fyrir hlutinn. Aðgangsstig svæðin, setja inn heimild, breyta heimild og þess háttar, munu öll innihalda útiloka. Til að leyfa ákveðið aðgangsstig er viðeigandi kostur valinn.

## <a name="to-copy-a-permission-set"></a>Til að afrita heimildasamstæðu

Stofna nýtt heimildasafn með því að afrita annað. Nýja settið felur í sér allar heimildir og heimildir sem settar eru úr stillunni sem afrituð var. Hvernig heimildum og heimildunum er raðað í nýja heimildasettið er mismunandi eftir því hvað valið er í **reitnum afrita aðgerð**. Eftirfarandi tafla lýsir valkostunum.

|Valkostur  |Lýsing  |
|---------|---------|
|**Afrita með tilvísun**     | Upprunalega heimildaleit og öllum þeim heimildastæðum sem Stuðst var við hana eru skráð á **niðurstöðurúðuna**.       |
|**Eintak af flötu leyfi**  | Allar heimildir frá öllum heimildaleit eru hafðar með á flötum lista á **heimildarúðunni**. Heimildir eru ekki skipulagðar eftir heimildauppsetningu.        |
|**Klósett**     | Búa til nákvæmt eintak af upphaflegu heimildinni.        |

1. Á síðunni **heimildasamstæður** skaltu velja línuna fyrir heimildasamstæðu sem þú vilt afrita og síðan velja **Afrita heimildasamstæðu** aðgerðina.
2. **Á síðunni afrita heimildagildi** er heiti nýja heimildsettinu tilgreint.
3. **Í reitnum afrita aðgerð** er tilgreint hvernig eigi að raða heimild í nýja heimildsettinu.
4. Valfrjálst: Ef verið er að bæta við Kerfistilheimild gæti verið æskilegt að láta vita ef heiti eða efni upprunalegu heimildarinnar breytist í síðari útgáfu. Þetta gerir það kleift að íhuga hvort uppfæra eigi notendaskilgreinda heimildasamstæðu. Til að fá tilkynningu skal kveikja **á Tilkynningarheimildinni breyta um leyfi**.

> [!NOTE]
> Tilkynningin krefst þess að **upphaflegri kerfisheimild verði breytt** Tilkynning virkjuð á **síðunni tilkynningar** mínar.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a>Að stofna eða breyta heimildum með skráning við aðgerðir þínar

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Heimildasamstæður** og velja síðan viðkomandi tengil.

    Einnig, á síðunni **Notendur**, veldu aðgerðina **Heimildarsöfn**.
2. Á síðunni **Heimildarsöfn**, veldu aðgerðina **Nýtt**.
3. Fyllið í reitina eftir þörfum í nýrri línu.
4. Veljið aðgerðina **Heimildir**.
5. Á síðunni **Heimildir** skal velja aðgerðina **Skrá heimildir** og velja svo aðgerðina **Byrja**.

    Upptökuferli hefst og tekur allar aðgerðirnar með sér inn í notendaviðmótið.
6. Farðu á hinar ýmsu síður og aðgerðir í [!INCLUDE[prod_short](includes/prod_short.md)] sem þú vilt að notendur með þessa heimildasamstæðu fái aðgang að. Þú verður að ljúka verkinu sem ætlunin er að skrá heimildir fyrir.
7. Þegar á að ljúka við skráningu er farið aftur á síðuna **Heimildir** og svo valið **Stöðva** aðgerðina.
8. Velja **Já** hnappinn til að bæta skráð heimildir við nýja heimildasafnið.
9. Tilgreinið fyrir hvern hlut í listanum skrá hvort notendum sé kleift að setja inn, breyta eða eyða færslum í skráðum töflum.

### <a name="to-export-and-import-a-permission-set"></a>Til að flytja út og flytja inn heimildasamstæðu

Ef fljótlegt er að setja upp heimildir er hægt að flytja inn stilliheimildir sem fluttar voru út úr öðrum [!INCLUDE[prod_short](includes/prod_short.md)] leigjanda.

Í umhverfi margra leigjenda er heimildarákvæði flutt inn á ákveðinn leigjanda. Með öðrum orðum, umfang innflutningsins er *leigjanda*.

1. Á leigjanda 1, á síðunni **Heimildasamstæður** skaltu velja línuna eða línurnar fyrir heimildasamstæður sem á að flytja út og velja síðan aðgerðina **Flytja út heimildasamstæður**.

    XML-skrá er stofnuð í möppunni sækja í vélinni. Sjálfgefið heiti er *að flytja út heimildasöfn. XML*.

2. Á leigjanda 2, á síðunni **Heimildasamstæður** skaltu aðgerðina **Flytja inn heimildasamstæður**.
3. **Á svarsíðu innflutningsheimildalista** er bent á hvort sameina eigi fyrirliggjandi heimildir um notendamengi með nýjum heimildum í XML skránni.

    Ef valið **er gátreitinn uppfæra tiltækar heimildir munu tiltækar heimildir sem samsvara nöfnum í XML-skránni verða sameinaðar með innfluttu heimildunum**.

    Ef ekki er **valið gátreitinn uppfæra gildandi heimildir** setur leyfi sem samsvara nöfnum í XML-skránni út við innflutning. Í þeim tilfellum er þér gert viðvart um heimildasöfn sem sleppt er.

4. **Úr svarglugganum innflutningur** er hægt að finna og velja XML-skrána sem á að flytja inn og velja **síðan opnu** aðgerðina.

Heimildasamstæðurnar eru fluttar inn.

## <a name="to-remove-obsolete-permissions-from-all-permission-sets"></a>Til að fjarlægja úreltar heimildir úr öllum heimildasamstæðum

1. Á síðunni **Heimildasamstæður** skal velja aðgerðina **Fjarlægja úreltar heimildir**.

## <a name="to-set-up-user-time-constraints"></a>Til að setja upp tímaskorður notanda

Kerfisstjórar geta skilgreint tímatímabil sem tilgreindir notendur geta bókað. Einnig geta stjórnendur tilgreint hvort kerfið skráir hve mikinn tíma notandi er skráður inn. Á sama hátt geta kerfisstjórar úthlutað ábyrgðarstöðvum til notenda. Frekari upplýsingar eru í [Vinna með ábyrgðarstöðvar](inventory-responsibility-centers.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning notanda** og velja síðan viðkomandi tengil.
2. Á síðunni **Notandauppsetning** opnast, skal velja **Nýtt** aðgerð.
3. Í reitnum **Kenni notanda**, skal færa inn kenni notanda, eða velja reitinn til að sjá alla núverandi Windows notendur innan kerfisins.
4. Fyllið inn reitina eftir þörfum.

## <a name="to-manage-permissions-through-user-groups"></a>Að stjórna heimildum í gegnum notendaflokka

Notendaflokkar aðstoða við að stjórna heimildastæðum víðs vegar um fyrirtækið. [!INCLUDE [prod_short](includes/prod_short.md)] á netinu eru sjálfgefnir notendaflokkar sem eru úthlutaðir notendum sjálfkrafa á grundvelli leyfis. Hægt er að bæta notendum handvirkt við notendaflokk og hægt er að stofna nýja notendaflokka sem afrit af þeim sem fyrir eru.  

Þú byrjar á því að stofna notendahóp. Síðan úthlutarðu heimildasamstæðum til hópsins til að skilgreina hvaða hluti notendur hópsins hafa aðgang að. Þegar þú bætir notanda í hópinn gilda heimildasamstæður sem skilgreindar eru fyrir hópinn líka fyrir notandann.

Leyfi sett sem úthlutað er á notanda í gegnum notendaflokk dvöl samkv. Breyting á heimildum notendaflokks fer sjálfkrafa í notkun fyrir notendur. Ef þú fjarlægir notanda úr notendahópi eru heimildir viðkomandi afturkallaðar sjálfkrafa.

### <a name="to-add-users-to-a-user-group"></a>Notendum bætt við notendaflokk

Eftirfarandi ferli útskýrir hvernig á að búa til notendaflokka handvirkt. Notendaflokkur er stofnaður sjálfvirkt með því að sjá [til að afrita notendaflokk og allar heimildir](#to-copy-a-user-group-and-all-its-permission-sets) þess.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendaflokkar** og velja síðan viðkomandi tengil.

    1. Einnig, á síðunni **Notendur**, veldu aðgerðina **Notandaflokkar**.
2. Á síðunni **Notandaflokkur** er valin aðgerðin **Meðlimir notandaflokks**.
3. Á síðunni **Meðlimir notandaflokks** er valin aðgerðin **Bæta við notendum**.

### <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Til að afrita notendaflokk og öll heimildarsöfn

Til að fljótt skilgreina nýja notendaflokka geturðu afritað öll heimildarsöfn frá núgildandi notendaflokki yfir í nýjan notendaflokk.

> [!NOTE]
> Meðlimir úr notendaflokki eru ekki afritaðar í nýja notendaflokkinn. Þú verður að bæta þeim við handvirkt eftir á. Frekari upplýsingar er að finna í [til að bæta notendum við kaflann notendaflokkur](#to-add-users-to-a-user-group).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendaflokkar** og velja síðan viðkomandi tengil.
2. Veldu notendaflokkinn sem þú vilt afrita og veldu síðan aðgerðina **Afrita notendaflokk**.
3. Í reitinn **Nýr kóði notendaflokks** skal færa inn heiti fyrir flokkinn og velja síðan hnappinn **Í lagi**.

Nýja notendaflokknum er bætt við síðuna **Notendaflokkar**. Halda áfram að bæta við notendum. Frekari upplýsingar er að finna í [til að bæta notendum við kaflann notendaflokkur](#to-add-users-to-a-user-group).  

> [!IMPORTANT]
> Þú færð villuleitarvillu ef þú ert að reyna að tengja notendaflokk við notandann sem vísar í heimildasamstæðu sem var skilgreind í óuppsettri framlengingu. Það er vegna þess að App-KENNI framlengingarinnar er villuleitað þegar vísað er í það. Ef notandi á að úthluta notanda notendaflokks er annaðhvort hægt að setja hann upp aftur, fjarlægja tilvísun í fjarlægða framlengingu úr heimildasamstæðu, eða fjarlægja það leyfi sem sett er úr notendaflokki.

### <a name="to-assign-permission-sets-to-user-groups"></a>Til að úthluta leyfishópum á notendahópa

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendaflokkar** og velja síðan viðkomandi tengil.
2. Veldu notendaflokkinn sem á að úthluta á þessum heimildum til.  

    Öll heimildasöfn sem er nú þegar úthlutuð til notandans eru birtar í upplýsingakassanum **Heimildasöfn**.
3. Veldu aðgerðina **Heimildasamstæður notanda** til að opna síðuna **Heimildasamstæður notanda**.
4. Á síðunni **Heimildasöfn notanda** skal fylla út reitina eins og þörf krefur í nýrri línu.

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a>Til að úthluta heimildasamstæðu á síðunni **Heimildasamstæða eftir notendahópum**

Eftirfarandi ferli útskýrir hvernig á að úthluta heimildasamstæðum til notanda á síðunni **Heimildasamstæða eftir notendahópum**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.
2. Á síðunni **Notendur** skal velja viðeigandi notanda, og þá velja aðgerðina **Heimildasamstæða eftir notendahópum**.
3. Á því leyfi sem **sett er eftir síðunni notendaflokkur** er [notendaflokks heiti] **valið** í línu fyrir viðeigandi heimildasafn til að úthluta stillunni á notendaflokk.
4. Hakið í **gátreitinn allir notendaflokkar** til að úthluta heimildinni á alla notendaflokka.

Einnig er hægt að úthluta heimildum sem settar eru beint til notanda.

## <a name="to-assign-permission-sets-to-users"></a>Til að úthluta heimildasamstæðu á notendur

Heimildasamstæða er safn heimilda fyrir tiltekna gagnagrunnshluti. Öllum notendum verða að hafa verið úthlutað eitt eða fleiri heimildasöfn áður en þeir geta opnað [!INCLUDE[prod_short](includes/prod_short.md)].  

[!INCLUDE[prod_short](includes/prod_short.md)] Lausn inniheldur forskilgreindar heimildasamstæður sem Microsoft eða þjónustuaðila þeirra er bætt við. Þú getur einnig bætt við nýjum heimildasamstæðum sem eru sniðin að þörfum fyrirtækisins. Frekari upplýsingar er að finna í [til að búa til kaflann heimildasafn](#to-create-a-permission-set).

> [!NOTE]
> Ef þú vilt ekki takmarka aðgang notanda meira en þegar hefur verið skilgreint með leyfi geturðu úthlutað notanda sérstakri heimildasamstæðu sem kallast SUPER. Þessi heimildasamstæða tryggir að notandinn geti fengið aðgang að öllum hlutum sem eru tilgreindir í leyfi.
>
> Notandi með nauðsynlegt leyfi og SUPER-heimildasamstæðuna hefur aðgang að meiri virkni en notendur með Team Member-leyfið og SUPER-heimildasamstæðuna.

Þú getur úthlutað heimildarhópum til notenda á tvo vegu:

- Af **Notandaspjald** síðunni með því að velja heimildasamstæður til að úthluta notandanum.
- Frá síðunni **Heimildasamstæða eftir notendum** með því að velja notendur sem heimildasamstæðu er úthlutað til.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Til að úthluta heimildasamstæðu á notendakorti

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.
2. Veldu notandann sem á að úthluta á þessum viðskiptamanni til.
Öll heimildasöfn sem er nú þegar úthlutuð til notandans eru birtar í upplýsingakassanum **Heimildasöfn**.
3. Veldu **breyta** aðgerðina til að opna síðuna **Notandapjald** .
4. Á flýtiflipanum **Heimildasöfn notanda** skal fylla út reitina eins og þörf krefur í nýrri línu. Frekari upplýsingar er að finna [í til að stofna eða breyta heimildamengi](ui-define-granular-permissions.md#to-create-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Til að úthluta heimildasamstæðu á síðunni Heimildasamstæða eftir notanda

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.
2. **Á síðunni notendur** er heimildinni sem **er stillt á notandi** valið.
3. Á síðunni um leyfi sem **notandi** hefur sett upp skal velja **gátreitinn [notandanafn]** í línu fyrir viðeigandi heimildasafn til að úthluta stillunni á notandann.

    Gátreiturinn allir notendur **er** valinn til að úthluta heimildinni á alla notendur.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Fá yfirlit yfir heimildir notanda

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
    > Sjá [til þess að stofna heimildasamstæðu](ui-define-granular-permissions.md#to-create-a-permission-set) til að fá skýringu á röðun.  

4. Til að breyta heimildasamstæðu skaltu í **Eftir heimildasamstæðu** hlutanum, á línu fyrir viðeigandi heimildasamstæðu af tegund **Notandaskilgreint**, skaltu velja einn af fimm reitum aðgangsgerðar og velja annað gildi.

5. Til að breyta einstökum heimildum innan heimildasamstæðunnar skaltu velja gildi í **heimildasamstæðu** gluttanum til að opna **Heimildir** gluggann.

> [!NOTE]  
> Þegar þú breytir heimildasamstæðu munu breytingarnar einnig eiga við um aðra notendur sem hafa heimildarsamstæðuna úthlutað.

### <a name="security-filters-limit-a-users-access-to-specific-records-in-a-table"></a>Öryggissíur takmarka aðgang notanda að tilteknum færslum í töflu

Fyrir öryggi á færslustigi í [!INCLUDE[prod_short](includes/prod_short.md)] eru notaðar öryggisafmarkanir til að takmarka aðgang notanda að gögnum í töflu. Þú býrð til öryggissíur á töflugögnum. Öryggissía lýsir færslusafni í töflu sem notandi hefur aðgangsheimild að. Þú getur til dæmis tilgreint að notandi geti aðeins lesið færslur sem innihalda upplýsingar um tiltekinn viðskiptavin. Þannig getur notandinn ekki fengið aðgang að þeim færslum sem hafa að geyma upplýsingar um aðra viðskiptamenn. Frekari upplýsingar er að finna [í notkun öryggisafmarkanir](/dynamics365/business-central/dev-itpro/security/security-filters) í innihaldi stjórnunar.

## <a name="viewing-permission-changes-telemetry"></a>Skoða fjarmælingar heimildabreytinga

Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að senda breytingar sem eru gerðar á heimild á Application Insights tilfang í Microsoft Azure. Síðan er hægt að nota Azure Monitor til að búa til skýrslur og setja upp viðvaranir í söfnuðum gögnum. Nánari upplýsingar er að finna í eftirtöldum greinum í [!INCLUDE[prod_short](includes/prod_short.md)] forritaraaðstoð og stjórnun:

- [Fylgjast með og greina fjarmælingar - Virkja Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Greining fjarmælinga reitarvöktunar](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## <a name="delegated-admin-users"></a>Úthlutuðum admin-notendum

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

## <a name="see-also"></a>Sjá einnig

[Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md)  
[Vinna með forstillingar](admin-users-profiles-roles.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  
[Sérstillir [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Stjórnun](admin-setup-and-administration.md)  
[Bæta notendum við Microsoft 365 fyrir viðskipti](/microsoft-365/admin/add-users/add-users)  
[Öryggi og vernd í Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) í Developer og ITPro hjálp  
[Úthluta notendum telemetrakenni](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]