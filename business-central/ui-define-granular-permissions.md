---
title: Skilgreina nákvæmari heimildir
description: Í greininni er fjallað um hvernig hægt er að skilgreina Kornastærð og úthluta hverjum notanda þeim heimildum sem leyfi setur að þeir þurfi að sinna störfum sínum.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.search.form: 1, 119, 8930, 9800, 9807, 9808, 9830, 9831
ms.date: 05/09/2022
ms.author: edupont
ms.openlocfilehash: 26dbf7e47c0159429aebd34e9167d9c3e7490ec6
ms.sourcegitcommit: 2fa712d0aabe4287ebd4454c28d142d6baf045a0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/09/2022
ms.locfileid: "8729830"
---
# <a name="assign-permissions-to-users-and-groups"></a>Úthluta leyfum til notenda og hópa

[!INCLUDE[prod_short](includes/prod_short.md)] Öryggiskerfið stjórnar hvaða hlutum notandi getur opnað innan hvers gagnagrunns eða umhverfis, ásamt leyfi notandans. Hægt er að tilgreina fyrir hvern notanda hvort þeir geti lesið, breytt eða fært inn gögn í völdum gagnagrunnshlutum. Ítarlegar upplýsingar er að finna [í gagnaöryggi](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) í efni hönnuða og stjórnsýslu fyrir [!INCLUDE[prod_short](includes/prod_short.md)].

Áður en heimildum er úthlutað á notendur og notendaflokka þarf að skilgreina hverjir geta skráð sig inn með því að stofna notendur samkvæmt leyfi sínu. Nánari upplýsingar er að finna í [Búa til notendur samkvæmt leyfum](ui-how-users-permissions.md)

Í [!INCLUDE[prod_short](includes/prod_short.md)] eru tvö stig heimilda fyrir gagnagrunnshluti:

- Heildarheimildir í samræmi við leyfi, einnig nefnt réttindi.

  Í leyfum eru sjálfgefin leyfi sett. Byrjað í 2022 1. viðurkenningar getur sérsniðið þessar sjálfgefnu heimildir að viðeigandi leyfistegundum. Nánari upplýsingar eru [í Configure aðgangsheimildir byggðar á leyfum](ui-how-users-permissions.md#licensespermissions).  

- Ítarlegri heimilda sem þeim er úthlutað innan frá [!INCLUDE[prod_short](includes/prod_short.md)].

  Í þessari grein er lýst hvernig hægt er að skilgreina, nota og beita heimildum innan [!INCLUDE [prod_short](includes/prod_short.md)] til að breyta sjálfgefnu skilgreiningunni.  

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]  
Nánari upplýsingar [fást hjá fulltrúa kerfisstjóra á netinu](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

[!INCLUDE [prod_short](includes/prod_short.md)] á netinu eru sjálfgefnir notendaflokkar sem eru úthlutaðir notendum sjálfkrafa á grundvelli leyfis. Hægt er að breyta sjálfgefnu skilgreiningunni með því að breyta eða bæta við notendaflokkum, heimildaflokkum og heimildum. Eftirfarandi tafla lýsir lykilaðstæður til að breyta sjálfgefnum heimildum.  

|Til  |Sjá  |
|---------|---------|
|Til að auðvelda stjórnun heimilda fyrir marga notendur er hægt að skipuleggja þær í notendaflokkum og úthluta þeim síðan eða breyta einum heimildarmengi fyrir marga notendur í einni aðgerð.| [Heimildir til að stjórna heimildum í gegnum notendaflokka](#to-manage-permissions-through-user-groups) |
|Að stjórna heimildastæðum fyrir ákveðna notendur | [Notendum úthlutað heimildasöfn](#to-assign-permission-sets-to-users) |
|Að læra að skilgreina heimildasafn|[Heimild sett til að stofna eða breyta](#to-create-or-modify-a-permission-set)|
|Til að stjórna tilteknum heimildum|[Heimildir stofnaðar eða þeim breytt handvirkt](#to-create-or-modify-permissions-manually)|
|Til að skoða eða leysa úr heimildum notanda|[Til að fá yfirsýn yfir heimildir notanda](#to-get-an-overview-of-a-users-permissions)|
|Fræðsla um öryggi á skráastigi|[Öryggissíur takmarka aðgang notanda að tilteknum færslum í töflu](#security-filters-limit-a-users-access-to-specific-records-in-a-table)|

> [!NOTE]
> Viðbótaraðferð við að skilgreina hvaða aðgerðir notendur hafa aðgang að er með því að **Stilla upplifunarsvæðið** á **upplýsingasíðu** fyrirtækisins. Frekari upplýsingar er að finna í [Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md).
>
> Einnig er hægt að skilgreina hvað notendur sjá í notandaviðmótinu og hvernig þeir nota heimilaða virkni sína á síðum. Þetta er gert í gegnum forstillingar sem þú úthlutar til mismunandi notenda í samræmi við starfshlutverk þeirra eða deild. Frekari upplýsingar er að finna í [Vinna með forstillingar](admin-users-profiles-roles.md) og [Sérstillingar [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md).

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
4. Veldu **Allir notendahópar** gátreitinn til að úthluta heimildasamstæðunni til allra notenda.

Einnig er hægt að úthluta heimildum sem settar eru beint til notanda.

## <a name="to-assign-permission-sets-to-users"></a>Til að úthluta heimildasamstæðu á notendur

Heimildasamstæða er safn heimilda fyrir tiltekna gagnagrunnshluti. Öllum notendum verða að hafa verið úthlutað eitt eða fleiri heimildasöfn áður en þeir geta opnað [!INCLUDE[prod_short](includes/prod_short.md)].  

[!INCLUDE[prod_short](includes/prod_short.md)] Lausn inniheldur forskilgreindar heimildasamstæður sem Microsoft eða þjónustuaðila þeirra er bætt við. Þú getur einnig bætt við nýjum heimildasamstæðum sem eru sniðin að þörfum fyrirtækisins. Frekari upplýsingar er að finna í [til að stofna eða breyta hluta heimildstæðis](#to-create-or-modify-a-permission-set).

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
4. Á flýtiflipanum **Heimildasöfn notanda** skal fylla út reitina eins og þörf krefur í nýrri línu. Nánari upplýsingar er að finna í [Að búa til eða breyta heimildasamstæðum](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Til að úthluta heimildasamstæðu á síðunni Heimildasamstæða eftir notanda

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Notendur** og velja síðan viðkomandi tengil.
2. **Á síðunni notendur** er heimildinni sem **er stillt á notandi** valið.
3. Á síðunni **heimildasamstæða eftir notanda** veldu **[notandanafnið]** gátreitinn á línu fyrir viðkomandi heimildasamstæðu til að tengja samstæðuna við notandann.

    Veldu **Allir notendur** gátreitinn til að úthluta heimildasamstæðunni til allra notenda.

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
    > Fyrir skýringu á röðun skal sjá [Að búa til eða breyta heimildum handvirkt](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

4. Til að breyta heimildasamstæðu skaltu í **Eftir heimildasamstæðu** hlutanum, á línu fyrir viðeigandi heimildasamstæðu af tegund **Notandaskilgreint**, skaltu velja einn af fimm reitum aðgangsgerðar og velja annað gildi.

5. Til að breyta einstökum heimildum innan heimildasamstæðunnar skaltu velja gildi í **heimildasamstæðu** gluttanum til að opna **Heimildir** gluggann. Fylgdu skrefunum sem er lýst í [Að búa til eða breyta heimildum](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

> [!NOTE]  
> Þegar þú breytir heimildasamstæðu munu breytingarnar einnig eiga við um aðra notendur sem hafa heimildarsamstæðuna úthlutað.

### <a name="security-filters-limit-a-users-access-to-specific-records-in-a-table"></a>Öryggissíur takmarka aðgang notanda að tilteknum færslum í töflu

Fyrir öryggi á færslustigi í [!INCLUDE[prod_short](includes/prod_short.md)] notarðu öryggissíur til að takmarka aðgang notanda að gögnum í töflu. Þú býrð til öryggissíur á töflugögnum. Öryggissía lýsir færslusafni í töflu sem notandi hefur aðgangsheimild að. Þú getur til dæmis tilgreint að notandi geti aðeins lesið færslur sem innihalda upplýsingar um tiltekinn viðskiptavin. Þannig getur notandinn ekki fengið aðgang að þeim færslum sem hafa að geyma upplýsingar um aðra viðskiptamenn. Frekari upplýsingar er að finna [í notkun öryggisafmarkanir](/dynamics365/business-central/dev-itpro/security/security-filters) í innihaldi stjórnunar.


## <a name="to-create-or-modify-a-permission-set"></a>Að búa til eða breyta heimildasamstæðu

Heimildasamstæður virka sem geymir fyrir heimildir, svo að þú getir auðveldlega stjórnað mörgum heimildum í einni skrá.

> [!NOTE]  
> [!INCLUDE[prod_short](includes/prod_short.md)] lausn inniheldur yfirleitt fjölda fyrirfram skilgreindra heimildasamstæðna sem eru bætt við af Microsoft eða hugbúnaðarveitunni þinni. Þessar heimildasamstæður eru af tegund **Kerfi** eða **Viðbót**. Þú getur ekki búið til eða breytt þessum gerðum heimildasamstæða eða heimildir innan þeirra. Hins vegar getur þú afritað þau til að skilgreina eigin heimildasamstæður og heimildir.
>
> Heimildasamstæður sem notendur búa til, ný eða sem afrit, eru af gerðinni **Notandaskilgreint** og er hægt að breyta.

### <a name="to-create-new-permission-set-from-scratch"></a>Til að stofna nýja heimildasamstæðu frá grunni

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Heimildasamstæður** og velja síðan viðkomandi tengil.
2. Til að búa til nýtt heimildasamstæðu, veldu **Nýtt** aðgerðina.
3. Fyllt er í reitina í nýju línunni. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Þegar þú hefur búið til heimildasamstæðu verður þú að bæta við raunverulegum heimildum. Nánari upplýsingar er að finna í [Að búa til eða breyta heimildum handvirkt](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-copy-a-permission-set"></a>Til að afrita heimildasamstæðu

Þú getur einnig notað afritunaraðgerð til að flytja allar heimildir annars heimildasamstæðu á nýtt heimildasamstæðu.

> [!NOTE]  
> Ef heimildasamstæða Kerfis sem þú hefur afritað er breytt, færð þú senda tilkynning (eftir vali þínu), svo að þú getir íhugað hvort breytingarnar séu viðeigandi til að afrita eða skrifa inn í notendaskilgreinda heimildasamstæðu þína.

1. Á síðunni **heimildasamstæður** skaltu velja línuna fyrir heimildasamstæðu sem þú vilt afrita og síðan velja **Afrita heimildasamstæðu** aðgerðina.
2. Á síðunni **Afrita heimildasamstæðu** skaltu tilgreina nafn hinna nýju heimildasamstæðu, og þá velja **Í lagi** hnappinn.
3. Veldu **tilkynna um breyttan heimildasamstæðu** gátreitinn ef þú vilt viðhalda tengil á milli upprunalegu og afrituðu heimildasamstæðanna. Þannig verður þú látinn vita ef nafn eða efni upprunalegu heimildabreytinga breytist í komandi útgáfu.

Nýja heimildasamstæðan, sem inniheldur öll heimildir afritaðs heimildasamstæðu, er bætt við sem ný lína á síðunni **heimildasamstæða**. Nú er hægt að breyta heimild í nýju heimildasamstæðunni. 

> [!TIP]
> Línunum er raðað í stafrófsröð innan hverrar gerðar.

### <a name="to-export-and-import-a-permission-set"></a>Til að flytja út og flytja inn heimildasamstæðu

Ef fljótlegt er að setja upp heimildir er hægt að flytja inn stilliheimildir sem fluttar voru út úr öðrum [!INCLUDE[prod_short](includes/prod_short.md)] leigjanda.

Í fjöleignarhverfum umhverfi er heimild sett til innflutnings á tilteknum leigjanda. Með öðrum orðum, umfang innflutningsins er *leigjanda*.

1. Á leigjanda 1, á síðunni **Heimildasamstæður** skaltu velja línuna eða línurnar fyrir heimildasamstæður sem á að flytja út og velja síðan aðgerðina **Flytja út heimildasamstæður**.

    XML-skrá er stofnuð í möppunni sækja í vélinni. Sjálfgefið heiti er *að flytja út heimildasöfn. XML*.

2. Á leigjanda 2, á síðunni **Heimildasamstæður** skaltu aðgerðina **Flytja inn heimildasamstæður**.
3. **Á svarsíðu innflutningsheimildalista** er bent á hvort sameina eigi fyrirliggjandi heimildir um notendamengi með nýjum heimildum í XML skránni.

    Ef valið **er gátreitinn uppfæra fyrirliggjandi heimildir munu tiltækar heimildir sem samsvara nöfnum í XML-skránni verða sameinaðar með innfluttu heimildunum**.

    Ef ekki er hakað í **gátreitinn uppfæra fyrirliggjandi heimildir** mun leyfi sem samsvara nöfnum í XML-skránni verða sleppt við innflutning. Í þeim tilfellum er þér gert viðvart um heimildasöfn sem sleppt er.

4. **Úr svarglugganum innflutningur** er hægt að finna og velja XML-skrána sem á að flytja inn og velja **síðan opnu** aðgerðina.

Heimildasamstæðurnar eru fluttar inn.

## <a name="to-create-or-modify-permissions-manually"></a>Til að stofna eða breyta heimildum handvirkt

Þetta ferli útskýrir hvernig á að bæta við eða breyta heimildum handvirkt. Einnig er hægt að hafa heimildir myndaðar sjálfkrafa úr aðgerðum í HÍ. Nánari upplýsingar er að finna í [Að búa til eða breyta heimildum með því að skrá aðgerðir þínar](ui-define-granular-permissions.md#to-create-or-modify-permissions-by-recording-your-actions).

> [!NOTE]
> Þegar þú breytir heimild og þar með tengdum heimildasamstæðu munu breytingarnar einnig eiga við um aðra notendur sem hafa heimildasamstæðu úthlutað.

1. Á síðunni **heimildasamstæður** skal velja línuna fyrir heimildasamstæðu, og þá velja **heimildir** aðgerð.
2. Á síðunni **Heimildir**, búðu til nýjan línu eða breyttu reitum á núverandi línu.

Í hverju af fimm reitum yfir aðgangstegundir, **Lesa heimild** , **Setja inn heimild**, **Breyta heimild**, **Eyða leyfi** og **Framkvæma heimildir**, þú getur valið eitt af eftirfarandi þremur heimildarvalkostum:

|Valkostur|Description|Flokkun|
|------|-----------|-------|
|**Já**|Notandinn getur framkvæmt aðgerðina á hlutnum sem um ræðir.|Hæst|
|**Óbeint**|Notandinn getur framkvæmt aðgerðina á hlutnum sem um ræðir en aðeins í gegnum aðra tengda hlut sem notandinn hefur fulla aðgang að. Frekari upplýsingar um óbeinar heimildir er að finna í [Eiginleiki heimilda](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property) í Developer og IT-Pro hjálpinni|Næst hæsta|
|**Autt**|Notandinn getur ekki framkvæmt aðgerðina í umræddri aðgerð.|Lægstur|

> [!IMPORTANT]
> Fara skal varlega þegar **Setja inn heimild** eða **Breyta heimild** er úthlutað töflunni **9001 Meðlimur í notendahópi** eða **9003 Heimildasamstæða notendahóps**. Öllum notendum sem úthlutað er heimildasamstæðunni geta mögulega úthlutað sér í aðra notendahópa sem fyrir vikið getur veitt þeim heimildir sem þeir eiga ekki að hafa.

### <a name="example---indirect-permission"></a>Dæmi - Óbein heimild

Hægt er að úthlutað óbeinni heimild til að nota hlut aðeins í gegnum annan hlut.
Til dæmis getur notandi haft heimild til að keyra kótaeiningu 80, Sala-bókun. Sölubókun framkvæmir mörg verk, þar á meðal að breyta töflu 37, Sölulína. Þegar notandinn bókar söluskjal athugar kóðaeining sölu-bókunar, [!INCLUDE[prod_short](includes/prod_short.md)], hvort að notandinn hafi heimild til að breyta töflu sölulínu. Ef svo er ekki getur Codeunit ekki klárað verk sín og notandinn fær villuskilaboð. Ef svo er verður kótaeiningin keyrð.

Notandinn þarf þó ekki að hafa fullan aðgang að töflunni Sölulína til að keyra Codeunit. Ef notandinn hefur óbeina heimild fyrir töflu sölulínu keyrir kóðaeiningin Sala-bókun án vandræða. Þegar notandi hefur óbeina heimild, getur sá notandi aðeins breytt töflunni Sölulína með því að keyra Sölubókun kóðaeiningunni eða annan hlut sem hefur heimild til að breyta töflunni Sölulína. Notandinn getur aðeins breytt töflunni Sölulína frá studdum forritssvæðum. Notandinn getur ekki keyrt aðgerðina óboðlega eða með öðrum aðferðum.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a>Að stofna eða breyta heimildum með skráning við aðgerðir þínar

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Heimildasamstæður** og velja síðan viðkomandi tengil.

    Einnig, á síðunni **Notendur**, veldu aðgerðina **Heimildarsöfn**.
2. Á síðunni **Heimildarsöfn**, veldu aðgerðina **Nýtt**.
3. Fyllið í reitina eftir þörfum í nýrri línu.
4. Veljið aðgerðina **Heimildir**.
5. Á síðunni **Heimildir** skal velja aðgerðina **Skrá heimildir** og velja svo aðgerðina **Byrja**.

    Upptökuferli hefst og tekur alla aðgerðina í notendaviðmótinu.
6. Farðu á hinar ýmsu síður og aðgerðir í [!INCLUDE[prod_short](includes/prod_short.md)] sem þú vilt að notendur með þessa heimildasamstæðu fái aðgang að. Þú verður að ljúka verkinu sem ætlunin er að skrá heimildir fyrir.
7. Þegar á að ljúka við skráningu er farið aftur á síðuna **Heimildir** og svo valið **Stöðva** aðgerðina.
8. Velja **Já** hnappinn til að bæta skráð heimildir við nýja heimildasafnið.
9. Fyrir hvern hlutar á skráningar listanum, tilgreinið ef notendur geta sett inn, breytt eða eytt skráningum í skráningartöflunum.

## <a name="to-remove-obsolete-permissions-from-all-permission-sets"></a>Til að fjarlægja úreltar heimildir úr öllum heimildasamstæðum

1. Á síðunni **Heimildasamstæður** skal velja aðgerðina **Fjarlægja úreltar heimildir**.

## <a name="to-set-up-user-time-constraints"></a>Til að setja upp tímaskorður notanda

Kerfisstjórar geta skilgreint tímatímabil sem tilgreindir notendur geta bókað. Einnig geta stjórnendur tilgreint hvort kerfið skráir hve mikinn tíma notandi er skráður inn. Á sama hátt geta kerfisstjórar úthlutað ábyrgðarstöðvum til notenda. Frekari upplýsingar eru í [Vinna með ábyrgðarstöðvar](inventory-responsibility-centers.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning notanda** og velja síðan viðkomandi tengil.
2. Á síðunni **Notandauppsetning** opnast, skal velja **Nýtt** aðgerð.
3. Í reitnum **Kenni notanda**, skal færa inn kenni notanda, eða velja reitinn til að sjá alla núverandi Windows notendur innan kerfisins.
4. Fyllið inn reitina eftir þörfum.

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