---
title: Búa til fjárhagsskýrslur með fjárhagsskemum
description: Lýsir því hvernig skal nota fjárhagsskemu til að búa til ýmis konar yfirlit og skýrslur fyrir greiningar á afkastagögnum fjárhags.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.search.form: 103, 104, 197, 196, 195, 198, 490, 764, 765, 766
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8984d007f2082c6a21a3d2226a20f2ad585b131a
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129733"
---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Undirbúa fjárhagsskýrslugerð með fjárhagsskemu og lyklategundum

Notaðu reikningsáætlanir til að fá innsýn í fjárhagsupplýsingar sem eru geymdar í bókhaldslyklum. Fjárhagsskemu eru notuð til að greina upphæðir í fjárhagsreikningi og bera saman fjárhagsfærslur og færslur í fjárhagsáætlunarskýrslu. Niðurstöðurnar birta í sjókortum og skýrslum á mitt hlutverkamiðstöð, svo sem sjóðstreymissrit og rekstraryfirlit efnahags-og Efnahagsskýrslu.

Þú opnar þessar tvær skýrslur til dæmis með aðgerðinni **Fjárhagsyfirlit** í Mínu hlutverki viðskiptastjórnanda og endurskoðanda.  

[!INCLUDE[prod_short](includes/prod_short.md)] gefur til sýnis fjárhagsskema sem nota má strax. Einnig er hægt að setja upp eigin línur og dálka til að tilgreina tölurnar til að bera saman. Til dæmis er hægt að stofna fjárhagsskema til að reikna út hagnaðarframlegð á víddir eins og deildir eða viðskiptavinaflokka. Fjöldi sérsniðinna fjárhagsfullyrðinga sem hægt er að stofna er ótakmarkaður.  

Uppsetning fjárhagsskema krefst skilnings á fjárhagsgögnum í bókhaldslyklinum. Til dæmis er hægt að skoða fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum, en það krefst þess að stofnaðar séu áætlanir. Frekari upplýsingar eru í [Stofna fjárhagsáætlun](finance-how-create-budgets.md).

## <a name="account-schedules"></a>Fjárhagsskemu

Fjárhagsskema skipuleggur reikninga frá bókhaldslykli á vegu sem gerir gögn auðveld í gjöf. Hægt er að setja upp margvísleg útlit til að skilgreina upplýsingarnar sem á að finna í bókhaldslyklinum. Fjárhagsskema bjóða upp á stað fyrir útreikninga sem ekki er hægt að gera beint í bókhaldslyklum. Til dæmis er hægt að stofna millisamtölur fyrir flokka lykla og þá fela það samtölu í öðrum samtölum. Annað dæmi er að reikna út hagnaðarspássíur á víddir eins og deildir eða viðskiptavinaflokka. Þar að auki er hægt að afmarka fjárhagsfærslur og áætlunarfærslur fjárhags, til dæmis með nettóbreytingu eða debetupphæð.

Einnig er hægt að bera saman tvö eða fleiri fjárhagsskema og dálkauppsetningar með því að nota formúlur sem gerir kleift að grípa eftirfarandi aðgerðir:

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

Fjárhagsskemu í stöðluðu útgáfunni af [!INCLUDE[prod_short](includes/prod_short.md)] eru grunnurinn að stöðluðu fjárhagsskýrslunum sem mögulega passa ekki þörfum reksturs þíns. Til að stofna eigin fjárhagsskýrslur er hægt að byrja á því að afrita fyrirliggjandi fjárhagsskema eins og lýst er í skrefi 3.

> [!TIP]
> Eftir að fjárhagsskema hefur verið stofnað er hægt að nota **síðuna Fjárhagsskemayfirlit** til að forskoða og Villuleita fjárhagsskýrsluna sem fjárhagsáætlunin skilgreinir. Til að opna síðuna skaltu velja **yfirlitsaðgerðina**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagsskema** og svo velja viðeigandi tengil.  
2. Á síðunni **Heiti fjárhagsskema** skal velja aðgerðina **Nýtt** til að búa til nýtt heiti á fjárhagsskema.
3. Ef óskað er eftir að endurnýta stillingar í fjárhagsskema sem þegar er til skal velja **aðgerðina afrita fjárhagsskema**.
4. Fyllið inn reitina eftir þörfum. **Í svæðinu sjálfgefin Dálkauppsetning** er fyrirliggjandi útlit valið. Hægt er að breyta því síðar.

    Dálkauppsetningar skilgreina dálka fyrir færibreyturnar sem fjárhagsgögnin í línunum eru sýndar í. Til dæmis gæti Dálkauppsetning innihaldið fjóra dálka sem gera samanburð nettó breytingu og stöðu fyrir sama tímabil á þessu ári og síðasta ári. Frekari upplýsingar er að finna í [Til að breyta dálkaútliti](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Veljið aðgerðina **Breyta fjárhagsskema**.
6. Eftir því hvað á að greina er best að velja **Setja inn fjárhagsreikninga**, **Setja inn CF-reikninga** og **Setja inn aðgerðir kostnaðargerða** til að stofna línu fyrir hverja fjármálseiningu. Til dæmis gæti verið ein lína fyrir núverandi eignir og aðra línu fyrir eignir. Til innblásturs má sjá fjárhagsskemu í CRONUS sýnifyrirtækinu.

    > [!NOTE]
    > Reitnum **Línustengur.** Reitur sýnir fyrstu 10 stafi auðkennis, til dæmis lykilnúmer. Ef bætt er við einingum með kennum sem byrja á sömu 10 stöfum eru tvítekningar í reitnum **línustilur.** . Ef þörf krefur er hægt að breyta handvirkt identnarar eftir að einingarnar hafa verið settar inn. Auðkenni eru birt í **reitnum Samantekt**.

7. Veljið aðgerðina **Yfirlit** til að sjá viðeigandi fjárhagsskýrslu.
8. Á síðunni **Yfirlit fjárhagsskema**, í reitnum **Heiti dálkauppsetningar** veldu aðra dálkauppsetningu til að sjá fjárhagsgögn út frá öðrum færibreytum.
9. Velja hnappinn **Í lagi**.

Nú er búið að skilgreina grundvöll fjárhagsskemunar, línur fjárhagsgagna sem á að birta og fyrirliggjandi útlit dálka til að sýna gögnin á línunum á mismunandi færibreytum. Ef sjálfgefna dálkaútlitið sem var valið í skrefi 4 henti ekki tilgangi þínum er næsta ferli fylgt.

### <a name="to-edit-a-column-layout"></a>Til að breyta dálkauppsetningu

Dálkauppsetningar eru notaðar til að skilgreina dálkana sem eiga að vera í skýrslunni sem fylgir. Til dæmis er hægt að hanna uppsetningu í þeim tilgangi að bera saman breytingu og stöðu fyrir samsvarandi tímabil milli þessa árs og síðasta árs. Hægt er að hafa allt að 15 dálka, sem hentar vel t.d. til að skoða áætlanir í 12 mánuði með dálki sem sýnir heildina.

> [!NOTE]
> Prentuð/forskoðuð/vistuð útgáfa af fjárhagsskema getur mest sýnt fimm dálka. Ef fjárhagsskemað er aðeins ætlað til greiningar á síðunni **Yfirlit fjárhagsskema** er hægt að búa til eins marga dálka og þarf til.

1. Á síðunni **Fjárhagsskema** skal velja viðeigandi fjárhagsskema og svo aðgerðina **Breyta uppsetningu dálkaútlits**.
2. Á síðunni **Dálkauppsetning** skal búa til línu fyrir hvern dálk þar sem fjárhagsgögn eru sýnd í fjárhagsskýrslunni. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velja hnappinn **Í lagi**.
4. Opnaðu síðuna **Yfirlit fjárhagsskema** endrum og eins til að staðfesta að nýja dálkauppsetningin virki sem skyldi.

> [!NOTE]
> Dálkarnir sem þú skilgreinir í hverri línu tákna dálka 3 og upp úr á síðunni **Yfirlit fjárhagsskema**. Fyrstu tveir dálkarnir, **Dálkanr.** og **Lýsing**, eru fastar.  

### <a name="to-create-a-column-that-calculates-percentages"></a>Stofnun dálks sem reiknar prósentur:

Stundum getur verið þörf á dálkum í fjárhagsskema til að reikna prósentur heilda. Ef til dæmis eru raðir sem brjóta niður sölu eftir víddum gæti dálkurinn óskað eftir að tilgreina prósentu heildarsölu í hverri línu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 2.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagsskema** og svo velja viðeigandi tengil.
2. Á síðunni **Heiti fjárhagsskema** veljið fjárhagsskema.  
3. Veljið aðgerðina **Breyta fjárhagsskema** til að setja upp fjárhagsskemalínu til að reikna heildina sem prósenturnar munu byggjast á.  
4. Setjið inn línu beint fyrir ofan fyrstu línuna sem birta á prósentur fyrir.  
5. Fyllið inn í reitina í línunni sem hér segir: Í **Tegund samantektar** reitnum er færður inn **Valinn stofn fyrir prósentur**. Í reitnum **Samantekt** er færð inn reikniregla fyrir heildina sem prósentan verður byggð á. T. d. ef lína 11 inniheldur heildarsölu, skal færa inn **11**.  
6. Veljið aðgerðina **Breyta uppsetningu dálkaútlits** til að setja upp dálk.  
7. Fyllið inn í reitina í línunni sem hér segir: Í **Tegund dálks** reitnum er færður inn **Formúla**. Í reitnum **Reikniregla** er færð inn reikniregla fyrir upphæðina sem reikna á prósentur fyrir, með % fyrir aftan. Til dæmis ef dálkur N inniheldur hreyfingu, er fært inn **N%**.  
8. Skref 4 til 7 eru endurtekin fyrir hvern flokk línu sem skipta á niður eftir prósentum.

## <a name="to-set-up-account-schedules-with-overviews"></a>Uppsetning fjárhagsskema með yfirlitum

Hægt er að nota fjárhagsskema til að stofna uppgjörsskýrslu sem ber saman almennar fjárhagstölur og upphæðir í fjárhagsáætlun.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagsskema** og svo velja viðeigandi tengil.
2. Á síðunni **Heiti fjárhagsskema** veljið fjárhagsskema.  
3. Veljið aðgerðina **Breyta fjárhagsskema**.  
4. Á síðunni **Fjárhagsskema** skal velja heiti sjálfgefins fjárhagsskema í reitnum **Heiti**.
5. **Veljið aðgerðina Setja inn fjárhagsreikninga**.  
6. Reikningarnir sem eiga að vera í yfirlitinu eru valdir og smellt á **Í lagi**.

    Reikningarnir eru ekki settir inn í fjárhagsskemað. Einnig er hægt að breyta dálkaútlitinu ef þess er óskað.  
7. Veljið aðgerðina **Yfirlit**.  
8. **Á fjárhagsskemayfirlitssíðu**, á **flipanum víddir** fastflipann, Stillið áætlunarafmörkunina á síuheitið sem á að nota.  
9. Velja hnappinn **Í lagi**.  

Nú er hægt að afrita áætlunaryfirlitið og líma það inn í töflureikni.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Samanburður á reikningstímabilum með reiknireglum tímabils

Fjárhagsskemað þitt getur borið saman niðurstöður mismunandi reikningstímabila, svo sem þessum mánuði miðað við sama mánuð í fyrra. Til að gera þetta skal opna síðuna **Dálkaútlit** og sérstilla hana með því að bæta reitnum **Reikniregla samanburðartímabils** við sem dálki. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md). Hægt er að stilla þennan reit á reiknireglu tímabils.  

Reikningstímabil þarf ekki að samræmast dagatalinu. Hins vegar verður hvert reikningsár að hafa sama fjölda bókhaldstímabila þó að hvert tímabil geti verið mismunandi eftir Lengdum.  

[!INCLUDE[prod_short](includes/prod_short.md)] notar tímabilsjöfuna til að reikna upphæðina út frá samanburðartímabili miðað við tímabil sem afmörkun skýrslunnar stóð yfir í skýrslunni. Samanburðartímabilið byggir á upphafsdagsetningu dagsetningarsíunnar. Skammstafanirnar sem eiga við eru eftirfarandi:

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

Nánari upplýsingar um dagsetningarformúlur [fást með því að vinna með dagsetningar og tíma](ui-enter-date-ranges.md) dagatals.  

## <a name="import-or-export-account-schedules"></a>Flytja fjárhagsskemu inn eða út
Hægt er að flytja fjárhagsskemu inn og út sem RapidStart skilgreiningarpakka. Til dæmis er skilgreiningarpakkar gagnlegir til að samnýta þær með öðrum fyrirtækjum. Pakkinn er búinn til í .rapidstart skrá, sem afhendir innihald pakkans á samþjöppuðu formi.

### <a name="to-import-and-export-account-schedules"></a>Reikningsáætlanir innflutnings og útflutnings
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagsskema** og svo velja viðeigandi tengil.
2. Velja skal fjárhagsskema og velja **síðan áætlun** innflutningsreiknings eða **Flytja út fjárhagsskemað** Aðgerðir, eftir því hvað á að gera. 

> [!NOTE]
> Þegar fjárhagsskemu eru flutt inn verða fyrirliggjandi færslur sem hafa sama heiti og þær sem verið er að flytja inn.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/modules/configure-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Viðskiptaupplýsingar](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]