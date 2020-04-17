---
title: Undirbúa flutning á viðskiptamannagögnum | Microsoft Docs
description: Eftir að búið er að flytja inn og nota uppsetningargögn í nýjan gagnagrunn, er hægt að hefja flutning á fyrirliggjandi aðalgögnum viðskiptamanns, t. d. vöru- og viðskiptamannanúmer og heitum. Til að tryggja að þessi gögn séu stofnuð hratt og nákvæmlega í nýja fyrirtækinu ætti að nota sniðmát til að skipuleggja gögnin.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 8d99976a5a7940cf43506503ca8d625109f540b8
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186525"
---
# <a name="prepare-to-migrate-customer-data"></a>Undirbúa flutning á viðskiptamannagögnum
Eftir að búið er að flytja inn og nota uppsetningargögn í nýjan gagnagrunn, er hægt að hefja flutning á fyrirliggjandi aðalgögnum viðskiptamanns, t. d. vöru- og viðskiptamannanúmer og heitum. Til að tryggja að þessi gögn séu stofnuð hratt og nákvæmlega í nýja fyrirtækinu ætti að nota sniðmát til að skipuleggja gögnin.  

Yfirleitt eru gagnasniðmát stofnuð fyrir eftirfarandi aðalgagnatöflur:  

-   **Tengiliður**  
-   **Viðskiptamaður**  
-   **Vara**  
-   **Lánardrottinn**  

Hins vegar hægt að stofna sniðmátsskipulag fyrir hvaða töflu sem er í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!TIP]  
>  Einnig á nota gagnasniðmát fyrir daglegar aðgerðir til að stofna nýjar færslur sem eru stofnaðar á grundvelli sniðmáts. Þessi gagnasniðmát virka aðeins fyrir studdar yfirgagnatöflur. Nánari upplýsingar má til dæmis finna í [Skrá nýjar vörur](inventory-how-register-new-items.md).  

Þegar viðskiptavinagögn eru flutt inn úr skrá, t.d. fyrir vörur, eru nauðsynlegu reitsgögnin sem tilgreind hafa verið tekin úr tengda gagnasniðmátinu. Þegar ný vara er stofnuð þarf aðeins færa inn almennar upplýsingar eins og vöruheiti, lýsingu og verð og síðan safna afganginum af nauðsynlegu gögnunum úr völdu gagnasniðmáti.

Þegar ný aðalgagnafærsla er búin til, til dæmis viðskiptavinarspjald, eru sumir reitir nauðsynlegir og það verður að fylla þá út. Hægt er að flokka flesta nauðsynlega reiti, til dæmis bókunarflokka og greiðsluskilmála, til að gera stofnun aðalgagnafærsla auðveldari og stöðugri. Til dæmis er hægt að flokka áskilda reiti fyrir töflu 18, **Viðskiptamaður**, og tegundirnar **Innlent**, **Erlent** eða **Flytja út**.

> [!NOTE]
> Ekki er hægt að flytja út/flytja inn svæði af gerðinni Blob með Excel.

## <a name="to-select-a-data-template"></a>Til að velja gagnasniðmát
Þegar valið er fyrirliggjandi gagnasniðmát þarf fyrst að meta hvort sniðmátið sem stofnað var fyrir nýja fyrirtækið sé hentugt fyrir viðskiptamanninn. Fara skal yfir reitina og gildin til að ákvarða hvaða sniðmát henta fyrirtækinu best.  

> [!TIP]  
>  Einnig er hægt að nota gagnasniðmát til að stofna nýjar færslur á skjótan hátt. Þá má nota til að stofna gögn á fljótlegri og nákvæmari hátt. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Grunnstillingarsniðmát** og veldu síðan tengda tengilinn.  
2. Á síðunni **Grunnstillingarsniðmát** skal velja gagnasniðmát af listanum og veljið svo aðgerðina **Breyta**.  

Ef sjálfgefin sniðmát uppfylla ekki þarfir fyrirtækisins er hægt að stofna ný sniðmát eða bæta reitum við sjálfgefið sniðmát. Ef sjálfgefin sniðmát eru fullnægjandi er hægt að nota þau til að stofna færslur samkvæmt aðalgagnagrunni.

## <a name="to-create-a-new-data-template"></a>Til að búa til nýtt gagnasniðmát
Hægt er að stofna nýtt gagnasniðmát ef sjálfgefin sniðmát henta ekki nýja fyrirtækinu. Ef stofna á fleiri en eitt gæti verið gagnlegt að taka upp nafnavenju fyrir reitinn **Kóði**.

Hvert sniðmát samanstendur af haus og línum. Þegar sniðmát er stofnað er hægt að tilgreina við hvaða reiti skal alltaf jafna við gögn af tiltekinni gerð. Til dæmis er hægt að stofna mismunandi sniðmát viðskiptamanns sem eiga við mismunandi tegundir viðskiptamanna. Þegar viðskiptavinurinn er stofnaður með sniðmáti er hægt að nota sniðmátsgögn til að fylla ákveðna reiti út fyrirfram.

### <a name="to-copy-an-existing-data-template"></a>Fyrirliggjandi gagnasniðmát afritað
Hægt er að búa til nýtt gagnasniðmát á einfaldan hátt með því að afrita upplýsingar úr fyrirliggjandi gagnasniðmáti sem svo er breytt.

1. Opna skal síðuna **Grunnstillingarsniðmát**.
2. Valið er **Nýtt** aðgerð.
3. Reiturinn **Kóti** er fylltur út.
4. Velja skal **Afrita skilgreiningarsniðmát**.
5. Á síðunni **Grunnstillingarsniðmát** skal velja sniðmát til að afrita og svo hnappinn **Í lagi**.

Töflukenni, töfluheiti og línur fyrirliggjanda gagnasniðmáta eru sett í nýja sniðmátið.

### <a name="to-create-a-data-template-header-manually"></a>Til að stofna gagnasniðmátshaus handvirkt
1. Opna skal síðuna **Grunnstillingarsniðmát**.
2. Valið er **Nýtt** aðgerð.
3. Reiturinn **Kóti** er fylltur út.
3. Í reitnum **Töfluauðkenni** skal færa inn töfluna sem þetta sniðmát á við um. Reiturinn **Heiti töflu** útfyllist sjálfkrafa þegar reiturinn **Töflukenni** er stilltur.

### <a name="to-create-a-data-template-line-manually"></a>Til að stofna gagnasniðmátslínu handvirkt
1. I fyrstu línunni skal velja reitinn **Heiti reits**. Síðan **Reitalisti** sýnir lista með reitum í töflunni.
2. Veljið reit og smellið á hnappinn **Í lagi**. Fyllt er út í reitinn **Yfirskrift reits** með reitarheiti.
3. Í reitnum **Sjálfgefið gildi** skal færa inn viðeigandi gildi. Í sumum getur hentað að nota gildi sem ekki er tiltækt í gagnagrunninum. Í því tilviki er hægt að velja gátreitinn **Sleppa tengslaathugun** til að hægt sé að nota gögn án villna.

    > [!TIP]  
    > Þar sem svæðið **Sjálfgefið gildi** flettir ekki upp í samsvarandi valkostum reita [!INCLUDE[d365fin](includes/d365fin_md.md)] þá afritast og límist gildið úr tengdri síðu í sniðmátið.

4. Veljið gátreitinn **Áskilið** ef notendur verða að fylla út reitina.

    > [!NOTE]
    > Gátreiturinn er einungis til upplýsinga. Enginn viðskiptagrunnur er nauðsynlegur. Til dæmis geta notendur ekki reikningsfært og bókað reikning ef bókunarflokkar hafa ekki verið settir upp. Þar sem bókunarflokka er krafist er hægt að velja gátreitinn **Áskilið** fyrir þessa reiti til að láta notanda fylla þá út og því koma í veg fyrir bókunarvillur síðar.
5. Í reitnum **Tilvísun** eru færðar inn upplýsingar um reitinn eftir þörfum.
6. Velja hnappinn **Í lagi**.

## <a name="to-export-to-a-template-in-excel"></a>Að flytja út í sniðmát í Excel
Hægt er að stofna Excel-vinnubók með fljótlegum hætti til að nota sem sniðmát sem byggt er á uppbyggingu fyrirliggjandi gagnasafnstöflu. Þá má nota sniðmát til að safna saman gögnum um viðskiptavini með samræmdum sniði fyrir síðari innflutningi í [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Grunnstillingarvinnublað** og veldu síðan tengda tengilinn.
2. Bæta töflu við listann, eða velja fyrirliggjandi töflu. Nánari upplýsingar eru í [Vinna með grunnstillingu fyrirtækis í vinnublaði](admin-how-to-manage-company-configuration-in-a-worksheet.md).
3. Skilgreina reitina úr töflunni sem á að taka með í sniðmátinu.
4. Veljið aðgerðina **Flytja út í sniðmát**.
5. Nefna og vista Excel-skrána. Excel-vinnubókin opnast sjálfkrafa.

Nú er hægt að færa inn gögn um viðskiptavini í Excel-vinnublaðið. Ef margar töflur hafa verið fluttar út verður hver tafla á eigin vinnublaði. Vistið vinnubókina áður en haldið er áfram í næsta skref.

> [!NOTE]  
> Eftirfarandi villa getur komið upp þegar ensk útgáfa Excel er notuð en svæðisstillingin er sett á annað tungumál en ensku: „Gamalt snið eða ógilt tegundasafn.“ Til að leiðrétta þessa villu þarf að tryggja að tungumálapakkinn fyrir tungumálið sem ekki er enska sé uppsettur.

## <a name="to-import-from-a-template-in-excel"></a>Til að flytja inn úr sniðmáti í Excel
1. Á síðunni **Grunnstillingarvinnublað** skal velja aðgerðina **Flytja inn úr sniðmáti**.
3. Fara í vinnublað sniðmáts sem notandi bjó til og velja síðan aðgerðina **Opna**.
4. Til að bæta samansöfnuðum viðskiptamannagögnum við gagnagrunninn skal velja aðgerðina **Nota gögn**.

Þegar gögnum er jafnað úr sniðmáti í Excel á töflu sem hefur einnig skilgreiningarsniðmát tengt við sig í skilgreiningarpakkanum eru sjálfgefnu reitsgildin úr grunnstillingarsniðmátinu líka jöfnuð.

Hvers kyns skrá með gögnum sem eru notuð á þennan hátt er lokin, vegna þess að hún samanstendur af gögnum sem færð eru inn af notanda í Excel, auk sjálfgilda sem tilgreind eru í grunnstillingarsniðmátinu.

## <a name="to-create-a-record-from-a-configuration-template"></a>Til að búa til færslu úr grunnstillingarsniðmáti
Hægt að nota skipulag gagna sem kemur fram í gagnasniðmátum til að umbreyta upplýsingum í skráningar í gagnagrunninum, eina af annarri. Til þess er notuð aðgerðin **Stofna tilvik**. Þetta er smáútgáfa af gagnaflutningsferlinu og getur verið gagnleg við gerð frumgerða eða meðhöndlun minni gagnastofnunarverkhluta.  

Eftirfarandi skref sýna hvernig eigi að stofna birgðaspjald úr vörugagnasniðmáti. Hægt er að stofna færslu frá hvaða gagnasniðmáti sem er með sömu aðferð.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Grunnstillingarsniðmát** og veldu síðan tengda tengilinn.  
2. Velja skal sniðmátið **Vara** og síðan velja aðgerðina **Breyta**. Nánari upplýsingar eru í [Að stofna gagnasniðmát](admin-use-templates-to-prepare-customer-data-for-migration.md#to-create-a-new-data-template).
3. Veljið aðgerðina **Stofna tilvik**. Birgðaspjald er stofnað.  
4. Velja hnappinn **Í lagi**.  
5. Til að yfirfara nýja birgðaspjaldið veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vörur** og veldu síðan tengda tengilinn.  
6. Opna skal nýja birgðaspjaldið.  
7. Útvíkka mismunandi flýtiflipa og staðfesta að upplýsingarnar voru rétt stofnaðar á þeim.  

## <a name="to-use-a-configuration-template-on-a-record"></a>Til að nota grunnstillingarsniðmát í færslu
Hægt er að setja inn gagnasniðmát við allar skrár sem er í [!INCLUDE[d365fin](includes/d365fin_md.md)] og nota þessa aðferð til að breyta færslu. Ef þetta er gert er skrifað yfir fyrirliggjandi gildi í færslunni með þeim úr sniðmátinu. Þar af leiðandi ætti að fara varlega þegar jöfnun sniðmát er notað á fyrirliggjandi færslur.

> [!WARNING]  
>  Aðgerðin **Nota sniðmát** skrifar yfir tiltæk gögn í færslu. Ef þessi aðgerð er notuð við flutning aðalgagna mun hún skrifa yfir innflutt gögn þegar færslur eru stofnaðar.

Eftirfarandi ferli byggist á nýju viðskiptamannaspjaldi.  

1. Stofna viðskiptavin. Frekari upplýsingar eru í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md).
2. Á síðunni **Viðskiptamannaspjald** skal velja aðgerðina **Nota sniðmát**.  
3. Á síðunni **Viðskiptamannasniðmát** skal velja eitt af sniðmátunum og síðan smella á hnappinn **Í lagi**.  

Sjálfgefin gildi í völdu viðskiptamannasniðmáti eru sett inn á viðskiptamannaspjaldið.

## <a name="see-also"></a>Sjá einnig  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)  
[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)
