---
title: Hvernig á að undirbúa grunnstillingarpakka | Microsoft Docs
description: Þegar nýtt fyrirtæki er skilgreint eru töflutengsl greind og unnin. Gögn eru flutt inn og notuð í réttri röð. Víddartöflur eru einnig fluttar inn ef þær eru teknar með í grunnstillingapakkanum
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: f37ba62f786611d30b179c543855b689eb747f45
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187070"
---
# <a name="prepare-a-configuration-package"></a>Undirbúa grunnstillingarpakka
Þegar nýtt fyrirtæki er skilgreint eru töflutengsl greind og unnin. Gögn eru flutt inn og notuð í réttri röð. Víddartöflur eru einnig fluttar inn ef þær eru teknar með í grunnstillingapakkanum Nánari upplýsingar eru í [Að flytja inn gögn viðskiptamanns](admin-migrate-customer-data.md#to-import-customer-data). 

Til aðstoða viðskiptavininn við notkun á grunnstillingarpakkanum gætirðu viljað bæta við spurningalista eða spurningalistasafni við pakkann. Spurningalistinn getur aðstoða viðskiptavin í að skilja mismunandi uppsetningarvalkosti. Yfirleitt eru spurningalistar stofnaðir fyrir mikilvægar uppsetningartöflur þar sem viðskiptavinur gæti þurft frekari leiðsögn um hvernig velja skal viðeigandi stillingar. Nánari upplýsingar er að finna í [Safna uppsetningargildum viðskiptavinar](admin-gather-customer-setup-values.md).

## <a name="before-you-create-a-configuration-package"></a>Áður en grunnstillingapakki er búinn til
Vert er að hafa í huga nokkur atriði áður en grunnstillingapakki er búinn til vegna þess að þeir hafa áhrif á möguleika þína eða viðskiptamanna þinni á innflutningi hans. 

### <a name="tables-that-contain-posted-entries"></a>Töflur sem innihalda bókaðar færslur
Ekki er hægt að flytja inn gögn í töflur sem innihalda bókaðar færslur, svo sem töflur fyrir viðskiptamanna-, lánardrottna- og birgðabókafærslur, þannig að ekki ætti að taka þessi gögn með í grunnstillingapakkanum. Hægt er að bæta færslum við þessar töflur eftir að grunnstillingapakkinn hefur verið færður inn með því að nota færslubækur til að bóka færslurnar. Frekari upplýsingar er að finna í [Bókun skjala og færslubóka](ui-post-documents-journals.md).

### <a name="licensing"></a>Leyfisveiting
Leyfið verður að innihalda töflurnar sem verið er að uppfæra. Ef óvissa ríkir um þetta getur síðan **Grunnstillingarvinnublað** komið að góðum notum. Ef leyfið inniheldur töfluna er gátreiturinn **Leyfð tafla** valinn.  

### <a name="permissions"></a>Aðgangsheimildir
Ferlið við að búa til og flytja inn grunnstillingapakka felur í sér eftirfarandi virkar heimildir fyrir allar töflur í pakkanum: 

* Notandinn sem flytur út gögn fyrir grunnstillingapakka verður að hafa virku heimildina **Lesa**.
* Notandinn sem flytur inn grunnstillingapakka verður að hafa virku heimildirnar **Setja inn** og **Breyta**.

### <a name="database-schema"></a>Gagnagrunnsskema
Þegar skilgreiningarpakkar eru fluttir inn og út á milli tveggja gagnagrunna fyrirtækis ættu gagnagrunnarnir að hafa sama skema til að tryggja að öll gögn flytjist rétt yfir. Þetta merkir að gagnagrunnar ættu að hafa sama skipulag í töflum og reitum, þar sem töflur hafa sömu aðallykla og reitir hafa sama kenni og gagnagerðir.  

Hægt er að flytja inn skilgreiningapakka sem hefur verið fluttur út úr gagnagrunni sem hefur annað skemma en markgagnagrunnur. Allar töflur eða reitir sem eru í skilgreiningapakkanum en ekki í markgagnagrunninum verða hins vegar ekki fluttir inn. Töflur með öðrum aðallyklum og reitum með öðrum gagnagerðum verða heldur ekki fluttir inn. Sem dæmi má nefna að gögn munu ekki flytjast yfir ef skilgreiningapakki inniheldur töfluna **50000 Customer** sem hefur aðallykilinn **Code20** og gagnagrunnurinn sem flutt er inn í inniheldur töfluna **50000 Customer Bank Account** sem hefur aðallykilinn **Code20 + Code 20**.  

## <a name="to-create-a-configuration-package"></a>Til að búa til grunnstillingarpakka  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Grunnstillingapakkar** og veldu síðan tengda tengilinn.  
2. Valið er **Nýtt** aðgerð.  
3. Fyllt er út í reiti eftir því sem við á í flýtiflipanum **Almennt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Til að útiloka skilgreiningarspurningalista, skilgreiningarsniðmát og skilgreiningarvinnublaðatöflur úr pakkanum skal velja gátreitinn **Útiloka skilgreiningartöflur**. Annars verður þessum töflum sjálfkrafa bætt við listann yfir pakkatöflur þegar pakkinn er fluttur út.  
5. Nota skal aðgerðina **Sækja töflur**. **Sækja pakkatöflur** runuvinnslusíðan opnast.  
6. Velja reitinn **Velja töflur**. Síðan **Stilla val** opnast.  
7. Veljið aðgerðina **Velja allt** til að bæta öllum töflum við pakkann eða veljið gátreitinn **Valið** fyrir hverja töflu í listanum sem á að bæta við.
8. Velja hnappinn **Í lagi**. Fjöldi þeirra taflna sem valinn hefur verið er sýndur í svæðinu **Velja töflur**. Tilgreinið viðbótarvalréttir og veljið svo **Í lagi** hnappinn. [!INCLUDE[d365fin](includes/d365fin_md.md)] töflum er bætt við línur á síðunni **Grunnstillingarpakki**.  

    > [!NOTE]  
    >  Einnig er hægt að gera þetta í grunnstillingarvinnublaðinu. Velja skal töflurnar sem á að hafa í pakkanum og veljið svo aðgerðina **Úthluta pakka**.

9. Til að velja reitina sem á að hafa með úr töflu skal velja töfluna og svo á flipanum **Línur** skal velja aðgerðina **Reitir**.
Tilgreinið hvaða reitir eiga að vera í pakkanum. Sjálfgefið eru öll svæði innifalin.

    - Til að velja aðeins þá reiti sem á að hafa með er valin aðgerðin **Hreinsa það sem haft er með**. Til að bæta öllum reitum við skal velja aðgerðina **Safn haft með**.  
    - Til að tilgreina að svæðisgögn ætti ekki að villuleita skal hreinsa gátreitinn **Villuleita reit** fyrir reitinn.  

10. Greina hvort mögulegar villur hafi verið settar inn með því að velja aðgerðina **Villuleita pakka**. Þetta getur gerst þegar ekki eru hafðar með töflur sem nauðsynlegar eru skilgreiningunni.  
11. Velja hnappinn **Í lagi**.  

Þegar listinn yfir reiti sem taka á með úr töflu hefur verið fínstilltur, er hægt að athuga niðurstöður í Excel.  

### <a name="to-filter-and-review-your-dataset"></a>Til að afmarka og fara yfir gagnasafn  
1. Til að sía ákveðinn hóp af færslum sem á að vera með í pakkanum skal á flipanum **Línur** velja aðgerðina **Síur** og svo tilgreina viðeigandi síugildi.  
2. Á pakkaspjaldinu, á flipanum **Línur**, skal velja aðgerðina **Flytja út í Excel**.  
3. Staðfesta skilaboðin sem gera útflutning gagna í Excel virkan. Nefnda .xlsx-skráin opnast. Fara skal yfir þær færslur sem hafa verið fluttar út.  
4. Loka Excel.  

### <a name="to-include-a-template-for-application-to-a-table"></a>Til að taka með sniðmát til jöfnunar í töflu  
Fyrir tilteknar töflur, svo sem töflu sem mun innihalda aðalgögn, er hægt að tilgreina sniðmát til að nota á gögn. Sniðmátið getur innihaldið nauðsynlega reiti sem eiga að eiga við um öll aðalgögn og sem aldrei á að breyta. Til dæmis er hægt að stofna sniðmát sem hægt er að nota með gögnum um viðskiptamann. Sniðmátið getur innihaldið alla þá reiti sem nauðsynlegt er, sem leyfir samræmdan innflutning á stöðluðum upplýsingum. Upplýsingar sem ekki er hægt að staðla, svo sem nafn viðskiptamanns, eru síðan meðhöndlaðar þegar viðskiptamannagögn eru flutt inn.

1. Á síðunni **Grunnstilla pakkaspjalda** er tafla valin og síðan er valinn reiturinn **Gagnasniðmát**. Listi yfir sniðmát sem eru byggð á töflunni birtist.
2. Veljið sniðmát og smellið á hnappinn **Í lagi**.  

Eftir að lokið er við pakkann skal fylgja næsta ferli til að vista pakkann í skrá. Síðan er afhenda pakkann viðskiptamanni eða félaga.

### <a name="to-save-and-export-a-configuration-package"></a>Til að vista og flytja út grunnstillingarpakka  
- Á síðunni **Grunnstilla pakkaspjald** skal velja aðgerðina **Flytja út pakka**.  

Pakkinn er búinn til í .rapidstart skrá, sem afhendir innihald pakkans á samþjöppuðu formi. Grunnstillingarspurningalistum, grunnstillingarsniðmátum og grunnstillingarvinnublaðinu er bætt við pakka sjálfvirkt nema ákveðið hafi verið að útiloka þau.  

Hægt er að vista skjalið með nafni sem hefur sérstaka þýðingu fyrir notandann, en ekki er hægt að breyta nafnauka skráarinnar. Það hlýtur að vera rapidstart-skrá.  

### <a name="to-copy-a-configuration-package"></a>Til að afrita grunnstillingarpakka  
Þegar búið er að stofna pakka sem uppfyllir þarfir notanda er hægt að nota hann sem grunn til að stofna svipaða pakka. Þetta getur hraðað innleiðingartíma og styrkt endurtektarþátt á RapidStart Services.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Grunnstillingapakkar** og veldu síðan tengda tengilinn.  
2. Veljið pakka af listanum og veljið svo aðgerðina **Afrita pakka**.  
3. Í reitnum **Nýr sendingarkóti** er færður inn kóti fyrir nýjan pakka.  
4. Veljið gátreitinn **Afrita gögn** ef einnig á að afrita gögn úr gagnagrunni fyrirliggjandi pakka.  
5. Velja hnappinn **Í lagi**.

## <a name="to-customize-a-configuration-package"></a>Sérstilla grunnstillingarpakka
Nota skal skilgreiningarvinnublaðið til að safna og flokka upplýsingarnar sem nota skal til að skilgreina nýtt fyrirtæki, og raða töflum á rökréttan hátt. Uppsetning vinnublaðsins er byggð á einföldu stigveldi: Svæði innihalda flokka og flokkar innihalda töflur. Svæði og flokkar eru valfrjáls, en eru nauðsynleg til að geta séð yfirlit yfir grunnstillingarferlið í Mitt hlutverk RapidStart Services.

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Grunnstillingarvinnublað** og veldu síðan tengda tengilinn.  
2.  Í reitnum **Tegund línu** veljið **Svæði**. Færa skal inn lýsandi heiti í reitinn **Heiti**.  
3.  Í reitnum **Tegund línu** veljið **Flokkur**. Færa skal inn lýsandi heiti í reitinn **Heiti**.  
4.  Í reitnum **Tegund línu** veljið **Tafla**. Í reitnum **Kenni töflu** skal velja töflu sem á að taka með í vinnublaðinu.  

Nú er hægt að úthluta töflunum til tiltekinna grunnstillingarpakka sem hafa verið stofnaðir eða stendur til að stofna. Nánari upplýsingar eru í [Að úthluta töflu á grunnstillingarpakka](admin-how-to-prepare-a-configuration-package.md#to-assign-a-table-to-a-configuration-package).

## <a name="to-work-with-promoted-tables"></a>Til að vinna með stighækkaðar töflur  
1. Velja skal gátreitinn **Stighækkuð tafla** til að tilgreina töflu sem er oft notuð í uppsetningarferli fyrir hefðbundinn viðskiptavin, svo sem töfluna **Fjárhagsreikningur**. Þegar tafla hefur þetta merki, getur viðskiptavinur auðveldlega afmarkað vinnublað sitt til að sjá bara listann af stighækkuðum töflum sem þarfnast athygli.  
2. Hægt er að sjá síað yfirlit með því að velja aðgerðina **Aðeins stighækkað**. Listinn yfir töflur hefur aðeins að geyma þær töflur sem eru með gátreitinn valinn.  

## <a name="to-assign-a-table-to-a-configuration-package"></a>Til að úthluta töflu á skilgreiningarpakka  
Eftir að hafa skilgreint töflurnar sem á að fara með sem hluta af grunnstillingu notanda, er auðveldlega hægt að úthluta töflunum til grunnstillingarpakkanna. Hægt er að úthluta töflu á aðeins einn pakka. Í eftirfarandi ferli verður að úthluta pakkanum innan grunnstillingarvinnublaðs.  

> [!NOTE]  
>  Einnig er hægt að búa til pakka beint og bæta við töflum til að hann. Frekari upplýsingar er að finna í [Að stofna grunnstillingarpakka](admin-how-to-prepare-a-configuration-package.md#to-create-a-configuration-package).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Grunnstillingarvinnublað** og veldu síðan tengda tengilinn.
2. Á grunnstillingarvinnublaðinu skal velja línu eða flokk af línum sem á að úthluta á grunnstillingarpakka og svo skal velja aðgerðina **Úthluta pakka**.  
3.  Velja skal pakka af listanum eða velja aðgerðina **Nýtt** til að stofna nýjan pakka og veljið svo hnappinn **Í lagi**.  

    Ef tafla er ekki þegar í pakkanum verður henni bætt við hann. Pakkakóðareiturinn á vinnublaðslínunni verður fylltur út með kóða pakkans sem töflunni er úhlutað til.  
4. Ef fyrirliggjandi pakki er valinn má sjá hversu margar töflur eru þegar í pakkanum með því að skoða upplýsingarnar í reitnum **Fj. taflna**.

## <a name="to-review-or-customize-existing-database-data"></a>Að yfirfara eða sérstilla fyrirliggjandi gagnagrunnsgögn
Þegar grunnstillingarpakki fyrir lausn er stofnaður, er hægt að skoða og sérstilla tiltæk gagnagrunnsgögn svo þau falli betur að þörfum viðskiptavina. Gagnagrunnstaflan verður að tengjast síðu.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Grunnstillingarvinnublað** og veldu síðan tengda tengilinn.
2. Á grunnstillingarvinnublaðinu tilgreinið þær töflur sem innihalda gögn sem á að skoða eða sérstilla.  

    > [!NOTE]  
    >  Ganga þarf úr skugga um að hver tafla hafi síðukenni sem tengist henni. Fyrir staðlaðar [!INCLUDE[d365fin](includes/d365fin_md.md)] töflur er þetta gildi fyllt út sjálfkrafa. Fyrir sérsniðnar töflur þarf að gefa upp kennið.

3. Veljið aðgerðina **Gagnagrunnsgögn**. Síðan fyrir síðuna sem við á opnast.
4. Fara skal yfir upplýsingarnar. Breyta eins og nauðsyn kreufr með því að eyða skráningum sem eru ekki viðeigandi eða með því að bæta nýjum við.    

## <a name="to-copy-data-from-a-test-environment-to-a-production-environment"></a>Að afrita gögn úr prófunarumhverfi yfir í framleiðsluumhverfi  
Þegar búið er að staðfesta og prófa allar uppsetningarupplýsingar, er hægt að halda áfram með að afrita gögn í framleiðsluumhverfið. Nýtt fyrirtæki er stofnað í sama gagnagrunni.

1. Opna og ræsa nýja fyrirtækið.  
2. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Grunnstillingarvinnublað** og veldu síðan tengda tengilinn.  
3. Veljið aðgerðina **Afrita gögn úr fyrirtækinu**.  
4. Á síðunni **Afrita fyrirtækjagögn** skal velja reitinn **Afrita úr**. Síðan **Fyrirtæki** opnast.  
5. Veljið fyrirtækið sem afrita á gögn úr og veljið svo hnappinn **Í lagi**. Lista yfir töflur sem eru valdar við opnun skilgreiningarvinnublaðsins. Aðeins töflur sem innihalda færslur eru teknar með í listanum.
6. Veljið töflurnar sem á að afrita gögn úr og veljið svo aðgerðina **Afrita gögn**. Á síðunni **Afrita fyrirtækjagögn** skal velja hnappinn **Í lagi**.  

## <a name="see-also"></a>Sjá einnig  
[Safna uppsetningargildum viðskiptamanns](admin-gather-customer-setup-values.md)  
[Uppsetning grunnstillingu fyrirtækis](admin-set-up-company-configuration.md)  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)
