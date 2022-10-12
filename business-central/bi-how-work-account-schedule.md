---
title: Byggja upp ársskýrslur með fjárhagslegum gögnum og lykiltegundum
description: Lýsir því hvernig nota á ársskýrslur til að búa til ýmis Yfirlit og skýrslur til að greina gögn um Fjárhagsleg afköst.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI, account schedule, financial report
ms.search.form: 103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766
ms.date: 08/12/2022
ms.author: edupont
ms.openlocfilehash: 3b71bec5ca7f1c903913b4244eb176dbf1c53c86
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605246"
---
# <a name="prepare-financial-reporting-with-financial-data-and-account-categories"></a>Undirbúa fjárhagsskýrslugerð með fjárhagslegum gögnum og lykilflokkum

Ársskýrslur gefa þér innsýn inn í fjárhagsgögnin sem geymd eru í bókhaldslykli þínum (COA). Ársskýrslur greina tölur í fjárhag (fjárhags-og L. reikningar) og bera saman fjárhagsfærslur með áætlunarfærslum. Niðurstöðurnar sýna í sjókortum og skýrslum í hlutverkamiðstöð þinni, svo sem mynd sjóðstreymis og rekstraryfirlit og efnahagsskýrslur.

Þessar tvær skýrslur eru til dæmis með **uppgjöri** Financials í hlutverkamiðstöðvum viðskiptastjóra og bókhaldara.  

[!INCLUDE[prod_short](includes/prod_short.md)] gefur dæmi um ársskýrslur sem nota má strax. Einnig er hægt að setja upp eigin línur og dálka til að tilgreina tölurnar til að bera saman. Til dæmis er hægt að stofna fjárhagsskýrslur til að reikna út hagnaðarframlegð með því að nota víddir eins og deildir eða viðskiptavinaflokka. Fjöldi sérsniðinna fjárhagsfullyrðinga sem hægt er að stofna er ótakmarkaður.  

Uppsetning fjárhagsskýrslna krefst skilnings á fjárhagslegum gögnum í bókhaldslyklum. Til dæmis er hægt að skoða fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum, en það krefst þess að stofnaðar séu áætlanir. Frekari upplýsingar um [stofnun fjárhagsáætlana](finance-how-create-budgets.md).

## <a name="financial-reports"></a>Ársskýrslur

Ársskýrslur raða reikningum frá bókhaldslykli á vegu sem gerir gögn auðveldari að gjöf. Hægt er að setja upp mismunandi útlit til að skilgreina upplýsingarnar sem á að draga út úr bókhaldslyklinum. Ársskýrslur gefa út í stað útreikninga sem ekki er hægt að gera beint í bókhaldslykla. Til dæmis er hægt að stofna millisamtölur fyrir flokka lykla og þá fela það samtölu í öðrum samtölum. Annað dæmi er að reikna út hagnaðarspássíur á víddir eins og deildir eða viðskiptavinaflokka. Þar að auki er hægt að afmarka fjárhagsfærslur og áætlunarfærslur, til dæmis með nettóbreytingu eða debetupphæð.

Einnig er hægt að bera saman tvær eða fleiri ársskýrslur og dálkaskilgreiningar með því að nota formúlur, þannig er hægt að gera eftirfarandi atriði:

* Búa til sérsniðnar viðskiptaskýrslur.
* Búðu til eins margar fjárhagsskýrslur og þú þarft, hver með einstakt heiti.
* Búa til uppsetningu skýrslu og prenta út skýrslurnar með núverandi tölum.

## <a name="gl-account-categories"></a>Tegundir fjárhagsreikninga

Hægt er að nota lykiltegundir fjárhagsreikninga til að breyta sniði fjárhagsskýrslna. Þegar til dæmis hefur verið sett upp lykiltegundir á **síðunni fjárhagsskýrslur** **er hægt að** Velja aðgerðina mynda fjárhagsuppfærslur og uppfæra undirliggjandi ársskýrslur fyrir kjarna fjárhagsskýrslna. Næst þegar ein af þessum skýrslum er keyrð, eins og **stöðuskýrsla** skýrslunnar, er nýjum samtölum og undirtilraunum bætt við.

> [!NOTE]
> Lykiltegundir í efstu hæð, eins og **skuldunauta** -hnúturinn, eru fastar og ekki er hægt að bæta við eigin. Hins vegar er hægt að eyða og bæta við lykiltegundum á neðri stigum og skilgreina hvernig tengd fjárhagsskýrsla birtist í skýrslum.
>
> Þú skalt stofna og skipuleggja eigin neðri G-flokka fjárhagsreikninga frá grunni, í stigveldi ef þarf, frekar en að reyna að endurraða þeim sem fyrir eru. Til dæmis er hægt að endurhanna **Skuldir** til að innihalda nýtt **Eigið fé** og síðan **Skammtímaskuldir** og **Langtímaskuldir**.

## <a name="create-a-new-financial-report"></a>Stofna nýja ársskýrslu

Fjárhagsskýrslur eru notaðar til að greina fjárhagsreikninga eða til að bera saman fjárhagsfærslur með áætlunarfærslum. Hægt er til dæmis að skoða fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum.

Ársskýrslur í staðlaðri útgáfu [!INCLUDE[prod_short](includes/prod_short.md)] mega ekki henta þörfum fyrirtækja. Ef fljótlegt er að stofna eigin ársskýrslur skal byrja á því að afrita fyrirliggjandi eina, eins og lýst er í skrefi þrjú hér á eftir.

> [!TIP]
> Þegar búið er að stofna fjárhagsskýrslu er hægt að nota **síðuna fjárhagsskýrsla** til að forskoða og Villuleita nýskilgreinda fjárhagsskýrslu. Til að opna síðuna skal velja **aðgerðina Breyta fjárhagslegri skýrslu**.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **ársskýrslur** og velja síðan tengda tengilinn.  
2. **Veljið** nýja **aðgerð til að stofna nýtt fjármálaskýrsluheiti, á síðu fjárhagsskýrslna**.
3. Eigi að endurnýta stillingar úr fyrirliggjandi fjárhagsskýrslu skal velja **aðgerðina afrita fjárhagsskýrslu**.
4. Reitirnir eru fylltir út eftir þörfum. **Í reitnum Skilgreining** dálks er fyrirliggjandi Skilgreining valin sem er hægt að breyta síðar ef þess er óskað.

    Dálkskilgreiningar tilgreina færibreyturnar sem fjárhagsgögnin í línunum eru sýndar í. Til dæmis gæti dálkaskilgreining innihaldið fjóra dálka sem hægt er að nota til að bera saman nettóbreytingu og stöðu á sama tímabili í ár og á síðasta ári. Frekari upplýsingar í [hlutanum breyta dálkaskilgreiningu](bi-how-work-account-schedule.md#edit-a-column-definition).

5. Velja skal **aðgerðina Breyta línuskilgreiningu**.
6. Velja skal **fjárhagsreikninga**, **Setja inn CF-reikninga** og **Setja inn aðgerðir kostnaðargerða** til að stofna röð fyrir hverja fjárhagslega einingu sem á að greina. Til dæmis gæti verið ein lína fyrir núverandi eignir og aðra línu fyrir eignir. Til innblásturs má sjá ársskýrslur í CRONUS sýniafélaginu.

    > [!NOTE]
    > Reitnum **Línustengur.** Sýnir fyrstu 10 stafi auðkennis, til dæmis lykilnúmer. Ef bætt er við einingum með kennum sem byrja á sömu 10 stöfum eru tvítekningar í reitnum **línustilur.** . Ef þörf krefur er hægt að breyta auðkennum handvirkt eftir að einingarnar hafa verið settar inn. Auðkenni eru birt í **reitnum Samantekt**.

7. **Á síðunni ársskýrslur** er hægt að **Velja aðgerðina Breyta fjárhagslegri skýrslu** til að sjá meðfylgjandi fjárhagsskýrslu.
8. **Á síðunni Fjármálaskýrsla**, í **reitnum Skilgreining** dálks er valin önnur dálkskilgreining til að kanna Fjárhagsleg gögn eftir öðrum færibreytum.
9. Velja **Í lagi**.

Nú er búið að skilgreina grundvöll fjárhagsskýrslunnar; línur fjárhagsgagna sem á að birta; og fyrirliggjandi útlit dálka til að sýna gögnin í línunum með sérsniðnum færibreytum. Ef sjálfgefin dálkskilgreiningin sem valin var í skrefi 4 henti ekki tilgangi þínum er næsta ferli fylgt.

### <a name="edit-a-column-definition"></a>Breyta dálkaskilgreiningu

Dálkskilgreiningar eru notaðar til að tilgreina dálkana sem eru hafðir með í skýrslunni. Til dæmis er hægt að hanna uppsetningu í þeim tilgangi að bera saman breytingu og stöðu fyrir samsvarandi tímabil milli þessa árs og síðasta árs. Hægt er að hafa allt að 15 dálka, sem gagnlegt er að segja, skoða áætlanir í 12 mánuði með dálki sem sýnir heildina.

> [!NOTE]
> Útprentanleg/forskoðuð/vistuð útgáfa af ársskýrslu sýnir hámark fimm dálka. Ef fjárhagsskýrsla er einungis ætluð til greiningar á **síðu fjárhagsskýrslunnar** er hægt að stofna eins marga dálka og óskað er eftir.

1. **Á síðunni ársskýrslur** skal velja viðeigandi fjárhagsskýrslu og velja **svo aðgerðina Breyta dálkskilgreiningu**.
2. **Á síðunni Skilgreining** dálks skal stofna línu fyrir hvern dálk fjárhagsgagnanna sem sýnd er í fjárhagsskýrslunni. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velja **Í lagi**.
4. **Opnaðu síðuna Fjármálaskýrsla** frá tíma til að staðfesta að nýju dálkaskilgreiningarnar séu fyrirhugaðar.

> [!NOTE]
> Dálkarnir sem skilgreindir eru í hverri línu tákna dálka þrjá og upp á **síðu fjárhagsskýrslunnar**. Fyrstu tveir dálkarnir, **Dálkanr.** og **Lýsing**, eru fastar.  

### <a name="create-a-column-that-calculates-percentages"></a>Stofna dálk sem reiknar prósentur

Stundum getur verið æskilegt að hafa dálk í ársskýrslu til að reikna prósentur af Heildun. Ef til dæmis eru raðir sem brjóta niður sölu eftir víddum gæti dálkurinn óskað eftir að tilgreina prósentu heildarsölu í hverri línu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 2.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **ársskýrslur** og velja síðan tengda tengilinn.
2. **Veljið ársskýrslu á síðunni fjárhagsskýrslur**.  
3. **Veljið aðgerðina Breyta fjárhagslegri skýrslu** til að setja upp línu í fjárhagsskýrslu til að reikna út samtölu þess hlutfalls sem byggt verður á.  
4. Setjið inn línu beint fyrir ofan fyrstu línuna sem birta á prósentur fyrir.  
5. Fyllið inn í reitina í línunni sem hér segir: Í **Tegund samantektar** reitnum er færður inn **Valinn stofn fyrir prósentur**. **Í reitinn Samantekt** er færð inn Formúla fyrir heildina í prósentuna sem prósentan verður byggð á. T. d. ef lína 11 inniheldur heildarsölu, skal færa inn **11**.  
6. **Velja aðgerðina Breyta dálkskilgreiningu** til að setja upp dálk.  
7. Fyllið inn í reitina í línunni sem hér segir: Í **Tegund dálks** reitnum er færður inn **Formúla**. **Í reitinn Formúla** er færð inn Formúla fyrir upphæðina sem á að reikna prósentu fyrir og síðan prósentutáknið (%). Þannig að ef dálknúmer N inniheldur hreyfingar, Færið inn **N%**.  
8. Endurtakið skref 4 til 7 fyrir hvern flokk af línum sem á að brjóta niður eftir prósentum.

## <a name="set-up-financial-reports-with-overviews"></a>Setja upp ársskýrslur með yfirlitum

Hægt er að nota ársskýrslu til að stofna uppgjörsyfirlit fyrir samanburð á almennum fjárhagstölum og áætlunartölum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **ársskýrslur** og velja síðan tengda tengilinn.
2. **Veljið ársskýrslu á síðunni fjárhagsskýrslur**.  
3. Velja skal **aðgerðina Breyta línuskilgreiningu**  
4. **Á Línuskilgreiningsíðunni**, í **reitnum Nafn**, er sjálfgefið heiti fjárhagsskýrslunnar valið.
5. **Veljið aðgerðina Setja inn fjárhagsreikninga**.  
6. Valdir eru þeir lyklar sem eiga að vera í yfirlitinu og velja **svo í lagi**.

    Reikningarnir eru nú settir inn í fjárhagsskýrsluna þína. Einnig er hægt að breyta skilgreiningu dálksins ef þess er óskað.  
7. **Veljið aðgerðina Breyta fjárhagslegri skýrslu**.  
8. **Á síðunni fjárhagsskýrsla**, á **fastflipanum víddir**, Stillið afmörkun áætlunar á síuheitið sem á að nota.  
9. Velja **Í lagi**.  

Nú er hægt að afrita áætlunaryfirlitið og líma það inn í töflureikni.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Bera saman bókhaldstímabil með reiknireglum tímabila

Í ársskýrslu þinni er hægt að bera saman niðurstöður ólíkra reikningstímabila, svo sem liðinn mánuður á móti sama mánuði í fyrra. Til að gera það þarf að opna **Dálkskilgreiningarsíðuna** og sérsníða hana með því að bæta **formúlutímabili** samanburðar við sem dálk. Frekari upplýsingar er að sérsníða á [vinnusvæðinu](ui-personalization-user.md). Hægt er að stilla þennan reit á reiknireglu tímabils.  

Reikningstímabil þarf ekki að stemma við dagatalið. Hins vegar verður hvert reikningsár að hafa sama fjölda bókhaldstímabila þó að hvert tímabil geti verið mismunandi eftir Lengdum.  

[!INCLUDE[prod_short](includes/prod_short.md)] notar tímabilsjöfuna til að reikna tímalengd samanburðartímabils miðað við tímabil sem afmörkun skýrslunnar stóð yfir í skýrslunni. Samanburðartímabilið byggir á upphafsdagsetningu dagsetningarsíunnar. Skammstafanirnar sem eiga við eru eftirfarandi:

| Skammstöfun | Lýsing                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| T            | Tímabili.                                                                                |
| ST           | Síðasta tímabil reikningsárs, hálfsárs eða ársfjórðungs.                                   |
| CP           | GT (gildandi tímabil) reikningsárs, hálfsárs eða ársfjórðungs. Notið GT í reiknireglum til að stilla tímabilið sem byrjar eða endar reikniregluna. Til dæmis RÁ\[1..GT\] sýnir tímann frá upphafi gildandi reikningsárs til gildandi tímabils.|
| FÁ           | Reikningsár. Til dæmis FY \[1.. 3 \] sem er fyrsti ársfjórðungur yfirstandandi reikningsárs. |

Dæmi um reiknireglur:

| Formúla         | Lýsing                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Yfirstandandi tímabil.                                                                                  |
| \-1T            | Fyrra tímabili.                                                                                 |
| \-1RÁ\[1..ST\]  | Allt Fyrra reikningsár.                                                                     |
| \-1RÁ           | Yfirstandandi tímabil á fyrra reikningsári.                                                          |
| \-1RÁ\[1..3\]   | Fyrsta fjórðungi fyrra reikningsárs.                                                           |
| \-1RÁ\[1..GT\]  | Frá upphafi reikningsárs til yfirstandandi tímabils á undangengnu fjárhagsári, þar með talið á báðum tímabilum. |
| \-1RÁ\[GT..ST\] | Frá yfirstandandi tímabili í fyrra reikningsár til Síðasta tímabils fyrra reikningsárs, þar með talið á báðum tímabilum.   |

Ef þú vilt reikna eftir venjulegum tímabilum þarf í staðinn að slá inn reiknireglu í reitinn **Reikniregla samanburðartímabils**. Til dæmis, ef svæðið er stillt á-1Y, [!INCLUDE [prod_short](includes/prod_short.md)] ber saman við sama tímabil einu ári fyrr.

> [!NOTE]
> Það er ekki alltaf gagnstætt hvaða tímabilum er verið að bera saman því hægt er að setja Dagsetningarafmörkun á skýrslu sem spannar mismunandi dagsetningar en fjárhagstímabilin sem endurspeglast í bókhaldslyklum. Ef þú stofnar fjárhagsskýrslu þar sem á að bera saman tímabilið á sama tímabili í fyrra, þá er formúla **samanburðardagsetningarinnar stillt** á *-1fy*. Síðan keyrir þú skýrsluna 28. febrúar og setur afmörkunardagsetninguna á janúar og febrúar. Í kjölfar fjármálaskýrslunnar saman Janúar og febrúar á þessu ári til Janúar í fyrra sem er eina útfyllta bókhaldstímabilið af tveimur fyrir Síðasta ár.  

Frekari upplýsingar í [vinnu með dagsetningar og tímasetningar](ui-enter-date-ranges.md) dagatals.

## <a name="print-and-save-financial-reports"></a>Prenta og vista ársskýrslur

Hægt er að prenta út ársskýrslur með prentþjónustum tækisins. [!INCLUDE[prod_short](includes/prod_short.md)] býður einnig upp á þann valkost að vista skýrslur sem Microsoft Excel vinnubækur, Microsoft Word SKJÖL, PDF og XML skrár.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **ársskýrslur** og velja síðan tengda tengilinn.
2. **Á** síðunni ársskýrslur skal velja skýrsluna sem á að prenta og velja **síðan prentiðaðgerðina**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. **Í reitnum prentari** er valið tækið sem skýrslan verður send til.
    1. **Valkosturinn (meðhöndlaði vafrinn)** gefur til kynna að enginn merktur prentari sé til skýrslunnar. Í því tilviki mun vafrinn sjá um útprentunina og birta staðlaða prentskrefa, þar sem þú getur valið staðbundna prentara tengda tækinu þínu. **(Meðhöndlað af vafra)** er ekki í boði í farsímaforriti [!INCLUDE[prod_short](includes/prod_short.md)] eða forrit fyrir Microsoft Teams.
5. **Velja prentaðgerðina**.

### <a name="schedule-a-financial-report-or-save-as-a-pdf-word-or-excel-document"></a>Stundaðu ársskýrslu eða Vistaðu sem PDF, Word eða Excel skjal

Hægt er að vista ársskýrslu sem skrá á mismunandi sniðum, svo sem PDF, XML, Word eða Excel. Einnig er [!INCLUDE[prod_short](includes/prod_short.md)] hægt að stilla til að búa til endurteknar ársskýrslur:

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **ársskýrslur** og velja síðan tengda tengilinn.
2. **Á síðunni ársskýrslur** er prenthaðgerðin **valin**.
3. Stillið skýrsluna út og veljið **síðan aðgerðina senda til** aðgerðar.
4. Veldu skrársnið eða **áætlunaraðgerðina** og veldu **í lagi**.
5. Til að mynda áætlaða eða endurtekna ársskýrslu skal fylla út reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
   * Fyrir endurteknar ársskýrslur skal stilla **fyrstu upphafsdagsetningu/-tíma** og **gildistíma/-tíma** -reiti með fyrsta og Síðasta dagsetningunni, eftir því, til að mynda fjárhagsskýrsluna. Einnig skal velja á hvaða dögum skýrslan er mynduð með því að setja **næsta Keyrsludagsetningarformúlu** í reit eftir sniðinu sem útskýrt er í [kaflanum notkunardagsetningarformúlur](ui-enter-date-ranges.md#use-date-formulas).

## <a name="importing-or-exporting-financial-reports"></a>Innflutningur eða útflutningur ársskýrslna

Hægt er að flytja út ársskýrslur sem RapidStart skilgreiningarpakka sem gagnast við að samnýta upplýsingar með öðrum fyrirtækjum t.d. Pakkinn er stofnaður í. RapidStart-skrá, sem þjappar innihaldi.

### <a name="import-and-export-financial-reports"></a>Flytja inn og út ársskýrslur

1. Veldu þá ![ljósaperu sem opnast Segðu mér lögun 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **ársskýrslur** og velja síðan tengda tengilinn.
2. Veldu fjárhagsskýrsluna, Veldu **síðan Import fjármálaskýrslu** eða **útflutningsskýrslu** til aðgerða, allt eftir því hvað þú vilt gera.

> [!NOTE]
> Þegar fjárhagslegar skýrslur eru fluttar inn eru fyrirliggjandi færslur með sama heiti og þær sem verið er að flytja inn eytt.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/configure-financial-reports-dynamics-365-business-central/index).

## <a name="see-also"></a>Sjá einnig .

[Keyra og prenta skýrslur](ui-work-report.md)  
[Upplýsingarit um Fjármál fyrirtækja](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
