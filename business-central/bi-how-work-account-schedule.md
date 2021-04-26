---
title: Búa til fjárhagsskýrslur með fjárhagsskemum
description: Lýsir því hvernig skal nota fjárhagsskemu til að búa til ýmis konar yfirlit og skýrslur fyrir greiningar á afkastagögnum fjárhags.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f1e29820a3bb8254368e14ba1fa8b7dba17ed661
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786588"
---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Undirbúa fjárhagsskýrslugerð með fjárhagsskemu og lyklategundum

Notaðu reikningsáætlanir til að fá innsýn í fjárhagsupplýsingar sem eru geymdar í bókhaldslyklum. Fjárhagsskemu eru notuð til að greina upphæðir í fjárhagsreikningi og bera saman fjárhagsfærslur og færslur í fjárhagsáætlunarskýrslu. Niðurstöðurnar birtast í myndritum í Mínu hlutverki, eins og myndrit sjóðstreymis, og í skýrslum á borð við tekjuyfirlit og skýrslum efnahagsreiknings.

Þú opnar þessar tvær skýrslur til dæmis með aðgerðinni **Fjárhagsyfirlit** í Mínu hlutverki viðskiptastjórnanda og endurskoðanda.  

[!INCLUDE[prod_short](includes/prod_short.md)] veitir nokkrar sýnishornareikninga sem hægt er að nota strax eða þú getur sett upp eigin línur og dálka til að tilgreina tölurnar sem þú vilt bera saman. Notendur getur þú búið til fjárhagskema til að reikna út framlegð fyrir víddir eins og deildir eða hópa viðskiptamanna. Hægt er að búa til eins margar sérsniðnar fjárhagsskýrslur og óskað er.  

Uppsetning fjárhagsskema krefst skilnings á fjárhagsgögnum í bókhaldslyklinum. Hægt er til dæmis að skoða fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum. Þetta krefst þess að fjárhagsáætlanir séu búnar til. Frekari upplýsingar eru í [Stofna fjárhagsáætlun](finance-how-create-budgets.md).

## <a name="account-schedules"></a>Fjárhagsskema

Fjárhagsskemu eru notuð til að flokka reikninga á bókhaldslyklinum á máta sem hentar til framsetningar á upplýsingum um þá reikninga. Hægt er að setja upp margvísleg útlit til að skilgreina upplýsingarnar sem á að finna í bókhaldslyklinum. Eitt meginhlutverk fjárhagsskema er að gera útreikninga sem er ekki hægt að framkvæma beint í bókhaldslyklinum, eins og að búa til millisamtölu fyrir hóp reikninga sem má fella inn í nýjar upphæðir og síðan nota í öðrum upphæðum. Notendur geta til dæmis búið til fjárhagskema til að reikna út framlegð fyrir víddir eins og deildir eða hópa viðskiptamanna. Þar að auki er hægt að sía fjárhagsfærslur og fjárhagsáætlanafærslur, t.d. eftir hreyfingum eða debetupphæð.

Einnig er hægt að bera saman tvö eða fleiri fjárhagsskemu og dálkauppsetningar með því að nota formúlur. Með slíkum samanburði má framkvæma eftirfarandi atriði:

* Búa til sérsniðnar viðskiptaskýrslur.
* Búa til eins mörg fjárhagsskemu og þörf er á, þar sem hver þeirra ber einstakt heiti.
* Búa til uppsetningu skýrslu og prenta út skýrslurnar með núverandi tölum.

## <a name="gl-account-categories"></a>Fjárhagsreikningsflokkar

Hægt er að nota lykiltegundir fjárhagsreikninga til að breyta sniði fjárhagsskýrslna. Þegar lykiltegundir hafa verið settar upp á síðunni **Flokkar fjárhagsreikninga** og aðgerðin **Mynda fjárhagsskemu** er valin, eru undirliggjandi fjárhagsskemu fyrir kjarnaviðskiptaskýrslur uppfærð. Í næsta skipti sem ein af þessum skýrslum er keyrð, t.d. skýrsla **Stöðuyfirlits**, er nýjum samtölum og undirfærslum bætt við sem byggjast á breytingunum.

> [!NOTE]
> Lykilflokkar á efstu stigum, svo sem **Skuldir** hnútar eru fastir og ekki er hægt að bæta við eigin. Hins vegar er hægt að eyða og bæta við lykiltegundum á neðri stigum og breyta byggingu þeirra til að skilgreina hvernig tengt fjárhagsskema birtist í skýrslum.
>
> Mælt er með því að stofna og skipuleggja eigin lægri flokka fjárhagsreikninga frá grunni, í stigveldi ef þörf er á, frekar en að reyna að endurraða þeim sem fyrir eru. Til dæmis er hægt að endurhanna **Skuldir** til að innihalda nýtt **Eigið fé** og síðan **Skammtímaskuldir** og **Langtímaskuldir**.

## <a name="to-create-a-new-account-schedule"></a>Að búa til nýtt fjárhagsskema

Fjárhagsskemu eru notuð til að greina upphæðir í fjárhagsreikningi eða bera saman fjárhagsfærslur og fjárhagsáætlunarfærslur. Hægt er til dæmis að skoða fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum.

Fjárhagsskemu í stöðluðu útgáfunni af [!INCLUDE[prod_short](includes/prod_short.md)] eru grunnurinn að stöðluðu fjárhagsskýrslunum sem mögulega passa ekki þörfum reksturs þíns. Til að búa til þínar eigin fjárhagsskýrslur á fljótlegan hátt geturðu byrjað á því að afrita fyrirliggjandi fjárhagsskema. Sjá þrep 3 hér að neðan.

Á síðunni **Yfirlit fjárhagsskema** er þar sem fjárhagsskýrsla er forskoðuð sem fjárhagsskemað skilgreinir. Í eftirfarandi er mikilvægt að skilja að það sem er sett upp sem línur og dálkar fjárhagsskema er aðeins hægt að sjá og staðfesta á síðunni **Yfirlit fjárhagsskema**, sem er opnuð í fjárhagsskema með því að velja aðgerðina **Yfirlit**. Sjálf síðan **Fjárhagsskema** er aðeins uppsetningarsvæði.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagsskema** eða Lánardrottinn og veldu síðan tengda tengilinn.  
2. Á síðunni **Heiti fjárhagsskema** skal velja aðgerðina **Nýtt** til að búa til nýtt heiti á fjárhagsskema.
3. Að öðrum kosti skal velja aðgerðina **Afrita fjárhagsskema**, fylla í reitina tvo, og velja svo hnappinn **Í lagi**.
4. Fyllið inn reitina eftir þörfum. Í reitnum **Sjálfgefin dálkauppsetning** skal velja fyrirliggjandi útlit. Hægt er að breyta því síðar.

    Dálkauppsetning er notuð til að skilgreina dálka eftir ólíkum færibreytum sem fjárhagsgögn í línunum eru sýndar út frá. Til dæmis er hægt að hanna dálkauppsetningu til að bera saman nettóbreytingu og stöðu fyrir sama tímabilið á þessu ári og síðasta ári, með fjórum dálkum. Frekari upplýsingar er að finna í [Til að breyta dálkaútliti](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Veljið aðgerðina **Breyta fjárhagsskema**.
6. Búðu til línu fyrir hvern fjárhagslegan þátt sem þú vilt að birtist í skýrslunni, t.d. eina línu fyrir núverandi eignir og aðra línu fyrir annars konar eignir. Til að fá hugmyndir skal skoða fyrirliggjandi fjárhagsskema í sýnifyrirtækinu CRONUS.
7. Veljið aðgerðina **Yfirlit** til að sjá viðeigandi fjárhagsskýrslu.
8. Á síðunni **Yfirlit fjárhagsskema**, í reitnum **Heiti dálkauppsetningar** veldu aðra dálkauppsetningu til að sjá fjárhagsgögn út frá öðrum færibreytum.
9. Velja hnappinn **Í lagi**.

Þú hefur nú skilgreint grundvöll fjárhagsskemans, línur fjárhagsgagna sem eiga að birtast og fyrirliggjandi uppsetningu dálka til að sýna gögnin í línunum eftir hverri mismunandi færibreytu fyrir sig. Ef sjálfgefin dálkauppsetning sem þú valdir í skrefi 4 passar ekki áformum þínum, þá skaltu fylgja næsta ferli.

### <a name="to-edit-a-column-layout"></a>Til að breyta dálkauppsetningu

Dálkauppsetningar eru notaðar til að skilgreina dálkana sem eiga að vera í skýrslunni sem fylgir. Til dæmis er hægt að hanna uppsetningu í þeim tilgangi að bera saman breytingu og stöðu fyrir samsvarandi tímabil milli þessa árs og síðasta árs.

> [!NOTE]
> Prentuð/forskoðuð/vistuð útgáfa af fjárhagsskema getur mest sýnt fimm dálka. Ef fjárhagsskemað er aðeins ætlað til greiningar á síðunni **Yfirlit fjárhagsskema** er hægt að búa til eins marga dálka og þarf til.

1. Á síðunni **Fjárhagsskema** skal velja viðeigandi fjárhagsskema og svo aðgerðina **Breyta uppsetningu dálkaútlits**.
2. Á síðunni **Dálkauppsetning** skal búa til línu fyrir hvern dálk þar sem fjárhagsgögn eru sýnd í fjárhagsskýrslunni. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velja hnappinn **Í lagi**.
4. Opnaðu síðuna **Yfirlit fjárhagsskema** endrum og eins til að staðfesta að nýja dálkauppsetningin virki sem skyldi.

> [!NOTE]
> Dálkarnir sem þú skilgreinir í hverri línu tákna dálka 3 og upp úr á síðunni **Yfirlit fjárhagsskema**. Fyrstu tveir dálkarnir, **Dálkanr.** og **Lýsing**, eru fastar.  

### <a name="to-create-a-column-that-calculates-percentages"></a>Stofnun dálks sem reiknar prósentur:

Stundum getur verið þörf á dálkum í fjárhagsskema til að reikna prósentur heilda. Til dæmis, ef nokkrar línur skipta sölu eftir vídd kann að vera þörf á dálki sem birtir prósentu heildarsölu sem hver lína stendur fyrir.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagsskema** eða Lánardrottinn og veldu síðan tengda tengilinn.
2. Á síðunni **Heiti fjárhagsskema** veljið fjárhagsskema.  
3. Veljið aðgerðina **Breyta fjárhagsskema** til að setja upp fjárhagsskemalínu til að reikna heildina sem prósenturnar munu byggjast á.  
4. Setjið inn línu beint fyrir ofan fyrstu línuna sem birta á prósentur fyrir.  
5. Fyllið inn í reitina í línunni sem hér segir: Í **Tegund samantektar** reitnum er færður inn **Valinn stofn fyrir prósentur**. Í reitnum **Samantekt** er færð inn reikniregla fyrir heildina sem prósentan verður byggð á. T. d. ef lína 11 inniheldur heildarsölu, skal færa inn **11**.  
6. Veljið aðgerðina **Breyta uppsetningu dálkaútlits** til að setja upp dálk.  
7. Fyllið inn í reitina í línunni sem hér segir: Í **Tegund dálks** reitnum er færður inn **Formúla**. Í reitnum **Reikniregla** er færð inn reikniregla fyrir upphæðina sem reikna á prósentur fyrir, með % fyrir aftan. Til dæmis ef dálkur N inniheldur hreyfingu, er fært inn **N%**.  
8. Skref 4 til 7 eru endurtekin fyrir hvern flokk línu sem skipta á niður eftir prósentum.

## <a name="to-set-up-account-schedules-with-overviews"></a>Uppsetning fjárhagsskema með yfirlitum

Hægt er að nota fjárhagsskema til að búa til reikning sem ber saman upphæðir fjárhagsreiknings og fjárhagsáætlunar.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagsskema** eða Lánardrottinn og veldu síðan tengda tengilinn.
2. Á síðunni **Heiti fjárhagsskema** veljið fjárhagsskema.  
3. Veljið aðgerðina **Breyta fjárhagsskema**.  
4. Á síðunni **Fjárhagsskema** skal velja heiti sjálfgefins fjárhagsskema í reitnum **Heiti**.
5. Veljið aðgerðina **Setja inn reikning**.  
6. Reikningarnir sem eiga að vera í yfirlitinu eru valdir og smellt á **Í lagi**.

    Reikningarnir eru ekki settir inn í fjárhagsskemað. Einnig er hægt að breyta dálkauppsetningunni.  
7. Veljið aðgerðina **Yfirlit**.  
8. Á síðunni **Yfirlit fjárhagsskema** á flýtiflipanum **Víddarafmarkanir** skal stilla afmörkun fjárhagsáætlunar á æskilegt afmörkunarheiti.  
9. Velja hnappinn **Í lagi**.  

Nú er hægt að afrita áætlunaryfirlitið og líma það inn í töflureikni.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Samanburður á reikningstímabilum með reiknireglum tímabils

Fjárhagsskemað þitt getur borið saman niðurstöður mismunandi reikningstímabila, svo sem þessum mánuði miðað við sama mánuð í fyrra. Til að gera þetta skal opna síðuna **Dálkaútlit** og sérstilla hana með því að bæta reitnum **Reikniregla samanburðartímabils** við sem dálki. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md). Hægt er að stilla þennan reit á reiknireglu tímabils.  

Reikningstímabil þarf ekki að vera háð almanakinu, en þó verður að vera sami fjöldi reikningstímabila á öllum fjárhagsárum, þótt tímabilin geti verið mislöng.  

[!INCLUDE[prod_short](includes/prod_short.md)] nýtir reikniregluna fyrir tímabil til að reikna út upphæð frá samanburðartímabili miðað við tímabilið sem fæst við dagsetningarafmörkun á skýrslubeiðninni. Samanburðartímabilið byggir á upphafsdagsetningu dagsetningarsíunnar. Skammstafanirnar sem eiga við eru eftirfarandi:

| Skammstöfun | Description                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| T            | Tímabili                                                                                |
| ST           | Síðasta tímabil reikningsárs, hálfsárs eða ársfjórðungs.                                   |
| CP           | GT (gildandi tímabil) reikningsárs, hálfsárs eða ársfjórðungs. Notið GT í reiknireglum til að stilla tímabilið sem byrjar eða endar reikniregluna. Til dæmis RÁ\[1..GT\] sýnir tímann frá upphafi gildandi reikningsárs til gildandi tímabils.|
| RÁ           | Reikningsár. Til dæmis á RÁ\[1..3\] sýnir fyrsta fjórðung yfirstandandi reikningsárs |

Dæmi um reiknireglur:

| Reikniregla         | Description                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Yfirstandandi tímabil                                                                                  |
| \-1T            | Fyrra tímabil                                                                                 |
| \-1RÁ\[1..ST\]  | Allt fyrra reikningsár                                                                     |
| \-1RÁ           | Yfirstandandi tímabil á fyrra reikningsári                                                          |
| \-1RÁ\[1..3\]   | Fyrsti fjórðung fyrra reikningsárs                                                           |
| \-1RÁ\[1..GT\]  | Frá upphafi fyrra reikningsárs til gildandi tímabils í fyrra reikningsári, bæði tímabilin tekin með |
| \-1RÁ\[GT..ST\] | Frá gildandi tímabili á fyrra reikningsári til síðasta tímabils fyrra reikningsárs, bæði tímabilin tekin með   |

Ef þú vilt reikna eftir venjulegum tímabilum þarf í staðinn að slá inn reiknireglu í reitinn **Reikniregla samanburðartímabils**. Til dæmis ef reiturinn er stilltur á -1Á, ber [!INCLUDE [prod_short](includes/prod_short.md)] saman við tímabil einu ári á undan.

> [!NOTE]
> Það er ekki alltaf augljóst hvaða tímabil þú ert að bera saman vegna þess að þú getur stillt afmörkunardagsetningu í skýrslu sem nær yfir aðrar dagsetningar en reikningstímabilin sem endurspeglast í gögnum bókhaldslykilsins. Til dæmis stofnar þú fjárhagsskema þar sem þú vilt bera þetta tímabil saman við sama tímabil í fyrra, þannig að þú stillir reitinn **Reikniregla samanburðardagsetningar** á *-1RÁ*. Síðan keyrir þú skýrsluna 28. febrúar og setur afmörkunardagsetninguna á janúar og febrúar. Fyrir vikið ber fjárhagsskemað saman janúar og febrúar á þessu ári við janúar á síðasta ári, sem er eina reikningstímabilið sem hefur verið lokið á þessum tveimur árum.  

Frekari upplýsingar er að finna í [Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/configure-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Viðskiptaupplýsingar](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]