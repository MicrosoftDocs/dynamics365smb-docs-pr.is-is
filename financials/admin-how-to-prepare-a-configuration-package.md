---
title: "Hvernig á að undirbúa grunnstillingarpakka | Microsoft Docs"
description: "Þegar nýtt fyrirtæki er skilgreint eru töflutengsl greind og unnin. Gögn eru flutt inn og notuð í réttri röð. Víddartöflur eru einnig fluttar inn ef þær eru teknar með í grunnstillingapakkanum"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 02192888f95f8136e349764227e0bf1aac91c5d1
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="prepare-a-configuration-package"></a>Undirbúa grunnstillingarpakka
Þegar nýtt fyrirtæki er skilgreint eru töflutengsl greind og unnin. Gögn eru flutt inn og notuð í réttri röð. Víddartöflur eru einnig fluttar inn ef þær eru teknar með í grunnstillingapakkanum  

Til aðstoða viðskiptavininn við notkun á grunnstillingarpakkanum gætirðu viljað bæta við spurningalista eða spurningalistasafni við pakkann. Spurningalistinn getur aðstoða viðskiptavin í að skilja mismunandi uppsetningarvalkosti. Yfirleitt eru spurningalistar stofnaðir fyrir mikilvægar uppsetningartöflur þar sem viðskiptavinur gæti þurft frekari leiðsögn um hvernig velja skal viðeigandi stillingar. Nánari upplýsingar er að finna í [Safna uppsetningargildum viðskiptavinar](admin-gather-customer-setup-values.md).

Ganga þarf úr skugga um að notandi sé á Mitt hlutverk RapidStart Services innleiðara. Nánari upplýsingar eru í [Nota Mitt hlutverk RapidStart Services innleiðara](admin-how-to-use-the-rapidstart-services-role-center-to-track-progress.md).

> [!IMPORTANT]  
>  Þegar skilgreiningarpakkar eru fluttir inn og út á milli tveggja gagnagrunna fyrirtækis ættu gagnagrunnarnir að hafa sama skema til að tryggja að öll gögn flytjist rétt yfir. Þetta merkir að gagnagrunnar ættu að hafa sama skipulag í töflum og reitum, þar sem töflur hafa sömu aðallykla og reitir hafa sama kenni og gagnagerðir.  
>   
>  Hægt er að flytja inn skilgreiningapakka sem hefur verið fluttur út úr gagnagrunni sem hefur annað skemma en markgagnagrunnur. Allar töflur eða reitir sem eru í skilgreiningapakkanum en ekki í markgagnagrunninum verða hins vegar ekki fluttir inn. Töflur með öðrum aðallyklum og reitum með öðrum gagnagerðum verða heldur ekki fluttir inn. Sem dæmi má nefna að gögn munu ekki flytjast yfir ef skilgreiningapakki inniheldur töfluna **50000 Customer** sem hefur aðallykilinn **Code20** og gagnagrunnurinn sem flutt er inn í inniheldur töfluna **50000 Customer Bank Account** sem hefur aðallykilinn **Code20 + Code 20**.  

## <a name="to-create-a-configuration-package"></a>Til að búa til grunnstillingarpakka  
1. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarpakkar** og velja svo viðeigandi tengil.  
2. Valið er **Nýtt** aðgerð.  
3. Fyllt er út í reiti eftir því sem við á í flýtiflipanum **Almennt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Til að útiloka skilgreiningarspurningalista, skilgreiningarsniðmát og skilgreiningarvinnublaðatöflur úr pakkanum skal velja gátreitinn **Útiloka skilgreiningartöflur**. Annars verður þessum töflum sjálfkrafa bætt við listann yfir pakkatöflur þegar pakkinn er fluttur út.  
5. Nota skal aðgerðina **Sækja töflur**. Glugginn **Sækja pakkatöflur** runuvinnsla opnast.  
6. Velja reitinn **Velja töflur**. Glugginn **Stilla val** opnast.  
7. Veljið aðgerðina **Velja allt** til að bæta öllum töflum við pakkann eða veljið gátreitinn **Valið** fyrir hverja töflu í listanum sem á að bæta við.
8. Velja hnappinn **Í lagi**. Fjöldi þeirra taflna sem valinn hefur verið er sýndur í svæðinu **Velja töflur**. Tilgreinið viðbótarvalréttir og veljið svo **Í lagi** hnappinn. [!INCLUDE[d365fin](includes/d365fin_md.md)] töflum er bætt við línur í glugganum **Grunnstillingarpakki**.  

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

1. Í glugganum **Grunnstilla pakkaspjalda** er tafla valin og síðan er valinn reiturinn **Gagnasniðmát**. Listi yfir sniðmát sem eru byggð á töflunni birtist.
2. Veljið sniðmát og smellið á hnappinn **Í lagi**.  

Eftir að lokið er við pakkann skal fylgja næsta ferli til að vista pakkann í skrá. Síðan er afhenda pakkann viðskiptamanni eða félaga.

### <a name="to-save-and-export-a-configuration-package"></a>Til að vista og flytja út grunnstillingarpakka  
- Í glugganum **Grunnstilla pakkaspjald** skal velja aðgerðina **Flytja út pakka**.  

Pakkinn er búinn til í .rapidstart skrá, sem afhendir innihald pakkans á samþjöppuðu formi. Grunnstillingarspurningalistum, grunnstillingarsniðmátum og grunnstillingarvinnublaðinu er bætt við pakka sjálfvirkt nema ákveðið hafi verið að útiloka þau.  

Hægt er að vista skjalið með nafni sem hefur sérstaka þýðingu fyrir notandann, en ekki er hægt að breyta nafnauka skráarinnar. Það hlýtur að vera rapidstart-skrá.  

### <a name="to-copy-a-configuration-package"></a>Til að afrita grunnstillingarpakka  
Þegar búið er að stofna pakka sem uppfyllir þarfir notanda er hægt að nota hann sem grunn til að stofna svipaða pakka. Þetta getur hraðað innleiðingartíma og styrkt endurtektarþátt á RapidStart Services.

1. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarpakkar** og velja svo viðeigandi tengil.  
2. Veljið pakka af listanum og veljið svo aðgerðina **Afrita pakka**.  
3. Í reitnum **Nýr sendingarkóti** er færður inn kóti fyrir nýjan pakka.  
4. Veljið gátreitinn **Afrita gögn** ef einnig á að afrita gögn úr gagnagrunni fyrirliggjandi pakka.  
5. Velja hnappinn **Í lagi**.

## <a name="to-customize-a-configuration-package"></a>Sérstilla grunnstillingarpakka
Nota skal skilgreiningarvinnublaðið til að safna og flokka upplýsingarnar sem nota skal til að skilgreina nýtt fyrirtæki, og raða töflum á rökréttan hátt. Uppsetning vinnublaðsins er byggð á einföldu stigveldi: Svæði innihalda flokka og flokkar innihalda töflur. Svæði og flokkar eru valfrjáls, en eru nauðsynleg til að geta séð yfirlit yfir grunnstillingarferlið í Mitt hlutverk RapidStart Services.

1.  Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarvinnublað** og velja svo viðeigandi tengil.  
2.  Í reitnum **Tegund línu** veljið **Svæði**. Færa skal inn lýsandi heiti í reitinn **Heiti**.  
3.  Í reitnum **Tegund línu** veljið **Flokkur**. Færa skal inn lýsandi heiti í reitinn **Heiti**.  
4.  Í reitnum **Tegund línu** veljið **Tafla**. Í reitnum **Kenni töflu** skal velja töflu sem á að taka með í vinnublaðinu.  

Nú er hægt að úthluta töflunum til tiltekinna grunnstillingarpakka sem hafa verið stofnaðir eða stendur til að stofna. Nánari upplýsingar eru í kaflanum „Að úthluta töflu á grunnstillingarpakka.“

## <a name="to-work-with-promoted-tables"></a>Til að vinna með stighækkaðar töflur  
1. Velja skal gátreitinn **Stighækkuð tafla** til að tilgreina töflu sem er oft notuð í uppsetningarferli fyrir hefðbundinn viðskiptavin, svo sem töfluna **Fjárhagsreikningur**. Þegar tafla hefur þetta merki, getur viðskiptavinur auðveldlega afmarkað vinnublað sitt til að sjá bara listann af stighækkuðum töflum sem þarfnast athygli.  
2. Hægt er að sjá síað yfirlit með því að velja aðgerðina **Aðeins stighækkað**. Listinn yfir töflur hefur aðeins að geyma þær töflur sem eru með gátreitinn valinn.  

## <a name="to-assign-a-table-to-a-configuration-package"></a>Til að úthluta töflu á skilgreiningarpakka  
Eftir að hafa skilgreint töflurnar sem á að fara með sem hluta af grunnstillingu notanda, er auðveldlega hægt að úthluta töflunum til grunnstillingarpakkanna. Hægt er að úthluta töflu á aðeins einn pakka. Í eftirfarandi ferli verður að úthluta pakkanum innan grunnstillingarvinnublaðs.  

> [!NOTE]  
>  Einnig er hægt að búa til pakka beint og bæta við töflum til að hann. Nánari upplýsingar eru í kaflanum „Að stofna grunnstillingarpakka.“

1. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarvinnublað** og velja svo viðeigandi tengil.
2. Á grunnstillingarvinnublaðinu skal velja línu eða flokk af línum sem á að úthluta á grunnstillingarpakka og svo skal velja aðgerðina **Úthluta pakka**.  
3.  Velja skal pakka af listanum eða velja aðgerðina **Nýtt** til að stofna nýjan pakka og veljið svo hnappinn **Í lagi**.  

    Ef tafla er ekki þegar í pakkanum verður henni bætt við hann. Pakkakóðareiturinn á vinnublaðslínunni verður fylltur út með kóða pakkans sem töflunni er úhlutað til.  
4. Ef fyrirliggjandi pakki er valinn má sjá hversu margar töflur eru þegar í pakkanum með því að skoða upplýsingarnar í reitnum **Fj. taflna**.

## <a name="to-review-or-customize-existing-database-data"></a>Að yfirfara eða sérstilla fyrirliggjandi gagnagrunnsgögn
Þegar grunnstillingarpakki fyrir lausn er stofnaður, er hægt að skoða og sérstilla tiltæk gagnagrunnsgögn svo þau falli betur að þörfum viðskiptavina. Gagnagrunnstaflan verður að tengjast síðu.  

1. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarvinnublað** og velja svo viðeigandi tengil.
2. Á grunnstillingarvinnublaðinu tilgreinið þær töflur sem innihalda gögn sem á að skoða eða sérstilla.  

    > [!NOTE]  
    >  Ganga þarf úr skugga um að hver tafla hafi síðukenni sem tengist henni. Fyrir staðlaðar [!INCLUDE[d365fin](includes/d365fin_md.md)] töflur er þetta gildi fyllt út sjálfkrafa. Fyrir sérsniðnar töflur þarf að gefa upp kennið.

3. Veljið aðgerðina **Gagnagrunnsgögn**. Glugginn fyrir síðuna sem við á opnast.
4. Fara skal yfir upplýsingarnar. Breyta eins og nauðsyn kreufr með því að eyða skráningum sem eru ekki viðeigandi eða með því að bæta nýjum við.    

## <a name="to-copy-data-from-a-test-environment-to-a-production-environment"></a>Að afrita gögn úr prófunarumhverfi yfir í framleiðsluumhverfi  
Þegar búið er að staðfesta og prófa allar uppsetningarupplýsingar, er hægt að halda áfram með að afrita gögn í framleiðsluumhverfið. Nýtt fyrirtæki er stofnað í sama gagnagrunni.

1. Opna og ræsa nýja fyrirtækið.  
2. Velja skal táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Grunnstillingarvinnublað** og velja svo viðeigandi tengil.  
3. Veljið aðgerðina **Afrita gögn úr fyrirtækinu**.  
4. Í **Afrita fyrirtækjagögn** velurðu reitinn **Afrita úr**. Glugginn **Fyrirtæki** opnast.  
5. Veljið fyrirtækið sem afrita á gögn úr og veljið svo hnappinn **Í lagi**. Lista yfir töflur sem eru valdar við opnun skilgreiningarvinnublaðsins. Aðeins töflur sem innihalda færslur eru teknar með í listanum.
6. Veljið töflurnar sem á að afrita gögn úr og veljið svo aðgerðina **Afrita gögn**. Í **Afrita fyrirtækjagögn** velurðu hnappinn **Í lagi**.  

## <a name="see-also"></a>Sjá einnig  
[Safna uppsetningargildum viðskiptamanns](admin-gather-customer-setup-values.md)  
[Uppsetning grunnstillingu fyrirtækis](admin-set-up-company-configuration.md)  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)
