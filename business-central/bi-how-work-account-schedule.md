---
title: Búa til fjárhagsskýrslur með fjárhagsgögnum og reikningsflokkum
description: Lýsir því hvernig skal nota fjárhagsskýrslur til að búa til ýmis konar yfirlit og skýrslur fyrir greiningar á gögnum fyrir fjárhagslega frammistöðu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
---
# <a name="prepare-financial-reporting-with-financial-data-and-account-categories"></a><a name="prepare-financial-reporting-with-financial-data-and-account-categories"></a><a name="prepare-financial-reporting-with-financial-data-and-account-categories"></a>Útbúa Financial Reporting með fjárhagsgögnum og reikningsflokkum

Fjárhagsskýrslur veita þér innsýn í fjárhagsgögn sem eru vistuð í bókhaldslyklum. Fjárhagsskýrslur greina upphæðir í fjárhagsreikningum og bera saman fjárhagsfærslur og fjárhagsáætlunarfærslur. Niðurstöðurnar birtast í myndritum og skýrslum í hlutverkamiðstöðinni, svo sem myndriti sjóðstreymis og rekstrarreikningi og skýrslum efnahagsreiknings.

Hægt er að nálgast þessar tvær skýrslur t.d. með  **aðgerðum ársreikningaskrár**  og í hlutverkamiðstöðvum viðskiptastjóra og bókara.  

[!INCLUDE[prod_short](includes/prod_short.md)] veitir sýnishorn af fjárhagsskýrslum sem hægt er að nota strax. Einnig er hægt að setja upp eigin línur og dálka til að tilgreina tölurnar sem á að bera saman. Til dæmis er hægt að stofna fjárhagsskýrslur til að reikna út hagnaðarhlutfall með því að nota víddir eins og deildir eða viðskiptavinaflokka. Fjöldi sérsniðinna fjárshagsskýrslna sem þú getur búið til er ótakmarkaður.  

Uppsetning fjárhagsskýrsla krefst skilnings á fjárhagsgögnum í bókhaldslyklinum. Hægt er til dæmis að skoða fjárhagsfærslur sem prósentuhlutfall af fjárhagsáætlunarfærslum en þú verður fyrst að stofna fjárhagsáætlun. Frekari upplýsingar eru á [Stofna fjárhagsáætluanir](finance-how-create-budgets.md).

## <a name="financial-reports"></a><a name="financial-reports"></a><a name="financial-reports"></a>Fjárhagsskýrslur

Fjárhagsskýrslur raða reikningum úr bókhaldslyklum þínum á þann hátt sem auðveldar framsetningu gagna. Hægt er að setja upp margvísleg útlit til að skilgreina upplýsingarnar á að finna í bókhaldslyklinum. Fjárhagsskýrslur eru staður fyrir útreikninga sem ekki er hægt að framkvæma beint í bókhaldslykli. Til dæmis er hægt að búa til millisamtölur fyrir reikningsflokka og setja þær inn í aðrar samtölur Annað dæmi er að reikna út hagnaðarhlutfall á víddum eins og deildum eða viðskiptavinaflokkum. Þar að auki getur þú síað fjárhagsfærslur og fjárhagsáætlanafærslur, t.d. eftir nettóbreytingum eða debetupphæð.

Einnig er hægt að bera saman tvær eða fleiri fjárhagsskýrslur og dálkskilgreiningar með því að nota formúlur og því er hægt að gera eftirfarandi:

* Búa til sérsniðnar viðskiptaskýrslur.
* Búa til eins mörg fjárhagsskýrslur og þú þarft, hver með einkvæmt heiti.
* Búa til uppsetningu skýrslu og prenta út skýrslurnar með núverandi tölum.

## <a name="gl-account-categories"></a><a name="gl-account-categories"></a><a name="gl-account-categories"></a>Fjárhagsreikningsflokkar

Hægt er að nota lykiltegundir fjárhagsreikninga til að breyta sniði fjárhagsskýrslna. Þegar þú hefur til dæmis sett upp reikningsflokka þína á síðunni **Flokkar fjárhagsreikninga** getur þú valið aðgerðina **Mynda fjárhagsskýrslur** og uppfært undirliggjandi fjárhagsskýrslur fyrir meginfjárhagsskýrslurnar. Í næsta skipti sem ein af þessum skýrslum er keyrð, t.d. skýrsla **Stöðuyfirlits**, er nýjum samtölum og undirfærslum bætt við.

> [!NOTE]
> Lykilflokkar á efstu stigum, svo sem **Skuldir** hnútar eru fastir og ekki er hægt að bæta við eigin. Hins vegar er hægt að eyða og bæta við reikningsflokkum á neðri stigum til að skilgreina hvernig tengt fjárhagsskýrsla birtist í skýrslum.
>
> Þú ættir að stofna og skipuleggja eigin lægri flokka fjárhagsreikninga frá grunni, í stigveldi ef þörf er á, frekar en að reyna að endurraða þeim sem fyrir eru. Til dæmis er hægt að endurhanna **Skuldir** til að innihalda nýtt **Eigið fé** og síðan **Skammtímaskuldir** og **Langtímaskuldir**.

## <a name="create-a-new-financial-report"></a><a name="create-a-new-financial-report"></a><a name="create-a-new-financial-report"></a>Stofna nýja fjárhagsskýrslu

Fjárhagsskýrslur eru notaðar til að greina fjárhagsreikninga eða bera saman fjárhagfærslur og fjárhagsáætlunarfærslur. Hægt er til dæmis að skoða fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum.

Ársskýrslur í staðlaðri útgáfu af  [!INCLUDE[prod_short](includes/prod_short.md)]  kunna ekki að henta þörfum fyrirtækisins. Til að búa til eigin fjárhagsskýrslur á skjótan hátt skaltu byrja á því að afrita þær sem þegar eru til, eins og lýst er í skrefi þrjú hér á eftir.

> [!TIP]
> Þegar þú hefur búið til fjárhagsskýrslu getur þú notað síðuna **Fjárhagsskýrsla** til að forskoða og staðfesta nýlega skilgreinda fjárhagsskýrslu. Til að opna síðuna skal velja aðgerðina **Breyta fjárhagsskýrslu**.  

> [!NOTE]
> Þegar fjárhagsskýrsla er opnuð í View eða breytingarham er Síuúðinn tiltækur. Þó skal ekki nota rúðuna til að setja afmarkanir á gögnin í skýrslunni. Afmarkanirnar geta valdið villum eða gætu í raun ekki afmarkað gögnin. Í staðinn er Afmörkunarreitirnir  **notaðir í valflipum valkosta**  og  **vídda** .

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.  
2. Á síðunni **Fjárhagsskýrslur** skal velja aðgerðina **Nýtt** til að búa til nýtt heiti fjárhagsskýrslu.
3. Ef þú vilt endurnýta stillingar í fyrirliggjandi fjárhagsskýrslu skaltu velja aðgerðina **Afrita fjárhagsskýrslu**.
4. Reitirnir eru fylltir út eftir þörfum. Í reitnum **Dálkskilgreining** skaltu velja fyrirliggjandi skilgreiningu sem þú getur síðar breytt ef þú vilt.

    Dálkskilgreiningar tilgreina færibreyturnar sem eru notaðar til að birta fjárhagsgögn línanna. Til dæmis getur dálkskilgreining innihaldið fjóra dálka til að bera saman nettóbreytingu og stöðu fyrir sama tímabilið á þessu ári og síðasta ári. Fáðu frekari upplýsingar í hlutanum [Breyta dálkskilgreiningu](bi-how-work-account-schedule.md#edit-a-column-definition).

5. Veldu aðgerðina **Breyta línuskilgreiningu**.
6. Veldu aðgerðirnar **Setja inn fjárhagsreikninga**, **Setja inn sjóðstreymisreikninga** og **Setja inn kostnaðartegundir** til að búa til línu fyrir hverja fjárhagslega einingu sem á að greina. Til dæmis gæti ein lína verið fyrir núverandi eignir og önnur röð fyrir eignir. Þú getur fengið innblástur af fjárhagsskýrslum CRONUS sýnifyrirtækisins.

    > [!NOTE]
    > **Línan nr.** reiturinn sýnir fyrstu 10 stafina í kennimerki, eins og reikningsnúmer. Ef þú bætir við einingum með kennimerkjum sem byrja á sömu 10 stöfunum eru endurtekningar í **Línu nr.** . Ef þörf er á er hægt að breyta kennimerkjum handvirkt eftir að þú hefur sett inn einingarnar. Öll kennimerkin eru birt í reitnum **Samantekt**.

7.  **Á síðunni ársskýrslur**  skal velja  **aðgerðina Breyta fjárhagslegri skýrslu**  til að fá aðgang að fjárhagsskýrslunni sem var í kjölfarið.
8. Á síðunni **Fjárhagsskýrsla**, í reitnum **Dálkskilgreining**, skal velja aðra skilgreiningu dálka til að kanna fjárhagsgögn samkvæmt öðrum færibreytum.
9. Velja **Í lagi**.

Nú er búið að skilgreina eftirfarandi grundvöll fjárhagsskýrslunnar, raðir fjárhagslegra gagna sem á að birta og fyrirliggjandi útlit dálka til að sýna gögnin á línunum með sérsniðnum færibreytum. Ef sjálfgefin Skilgreining á dálki sem valin var í skrefi 4 hentar ekki tilgangi skal fylgja skrefunum í  [Breyta dálkaskilgreiningu](#edit-a-column-definition).

### <a name="edit-a-column-definition"></a><a name="edit-a-column-definition"></a><a name="edit-a-column-definition"></a>Breyta dálkskilgreiningu

Nota dálkskilgreiningar til að tilgreina dálkana sem eiga að vera í skýrslunni. Til dæmis er hægt að hanna uppsetningu í þeim tilgangi að bera saman breytingu og stöðu fyrir samsvarandi tímabil milli þessa árs og síðasta árs. Hægt er að hafa allt að 15 dálka, sem gagnlegt er að segja, birta áætlanir fyrir 12 mánuði með dálki sem sýnir heildina.

> [!NOTE]
> Prentuð/forskoðuð/vistuð útgáfa fjárhagsskýrslu sýnir mest fimm dálka. Ef fjárhagsskýrsla er hins vegar aðeins ætluð til greiningar á síðunni **Fjárhagsskýrsla** er hægt að búa til eins marga dálka og óskað er.

1. Á síðunni **Fjárhagsskýrslur** skaltu velja viðeigandi fjárhagsskýrslu og velja svo aðgerðina **Breyta dálkskilgreiningu**.
2. Á síðunni **Dálkskilgreining** skal búa til línu fyrir hvern dálk þar sem fjárhagsgögn eru sýnd í fjárhagsskýrslunni. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velja **Í lagi**.
4. Opnaðu síðuna **Fjárhagsskýrsla** öðru hverju til að staðfesta að nýja dálkskilgreiningin virki eins og til er ætlast.

> [!NOTE]
> Dálkarnir sem þú skilgreinir í hverri línu tákna þrjá eða fleiri dálka á síðunni **Fjárhagsskýrsla**. Fyrstu tveir dálkarnir, **Dálkanr.** og **Lýsing**, eru fastar.  

### <a name="create-a-column-that-calculates-percentages"></a><a name="create-a-column-that-calculates-percentages"></a><a name="create-a-column-that-calculates-percentages"></a>Stofna dálk sem reiknar prósentur

Stundum getur verið þörf á dálkum í fjárhagsskýrslu til að reikna út prósentuhlutfall samtölu. Til dæmis, ef línur skipta sölu eftir vídd kann að vera þörf á dálki sem birtir prósentuhlutfall heildarsölu sem hver lína stendur fyrir.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 2.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
2. Á síðunni **Fjárhagsskýrslur** skal velja Fjármálaskýrsla.  
3. Veljið aðgerðina **Breyta fjárhagsskýrslu** til að setja upp fjárhagsskýrslulínu til að reikna samtöluna sem prósentuhlutfallið miðast við.  
4. Setjið inn línu beint fyrir ofan fyrstu línuna sem birta á prósentur fyrir.  
5. Fyllið inn í reitina í línunni sem hér segir: Í **Tegund samantektar** reitnum er færður inn **Valinn stofn fyrir prósentur**. Í reitnum **Samantekt** er færð inn formúlu fyrir samtöluna sem prósentan miðast við. T. d. ef lína 11 inniheldur heildarsölu, skal færa inn **11**.  
6. Veljið aðgerðina **Breyta dálkskilgreiningu** til að setja upp dálk.  
7. Fyllið inn í reitina í línunni sem hér segir: Í **Tegund dálks** reitnum er færður inn **Formúla**. Í reitnum **Formúla** er færð inn formúla fyrir upphæðina sem reikna á prósentuhlutfall fyrir, með prósentutákni (%) þar fyrir aftan. Til dæmis ef dálkur N inniheldur nettóbreytinguna, er fært inn **N%**.  
8. Skref 4 til 7 eru endurtekin fyrir hvern flokk línu sem skipta á niður eftir prósentum.

## <a name="set-up-financial-reports-with-overviews"></a><a name="set-up-financial-reports-with-overviews"></a><a name="set-up-financial-reports-with-overviews"></a>Setja upp fjárhagsskýrslur með yfirlitum

Hægt er að nota fjárhagsskýrslu til að búa til reikning sem ber saman upphæðir fjárhagsreiknings og fjárhagsáætlunar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
2. Á síðunni **Fjárhagsskýrslur** skal velja Fjármálaskýrsla.  
3. Veldu aðgerðina **Breyta línuskilgreiningu**  
4. Á síðunni **Línuskilgreining** í reitnum **Heiti** skal velja sjálfgefið heiti fjárhagsskýrslu.
5. Veldu aðgerðina **Setja inn fjárhagsreikninga**.  
6. Reikningarnir sem eiga að vera í yfirlitinu eru valdir og smellt á **Í lagi**.

    Reikningarnir eru núna settir inn í fjárhagsskýrsluna. Einnig er hægt að breyta dálkaskilgreiningunni ef þess er óskað.  
7. Veldu aðgerðina **Breyta fjárhagsskýrslu**.  
8. Á síðunni **Fjárhagsskýrsla** á flýtiflipanum **Víddir** stillir þú á fjárhagsáætlunarsíuna á það nafn á síunni sem þú vilt nota.  
9. Velja **Í lagi**.  

Nú er hægt að afrita áætlunaryfirlitið og líma það inn í töflureikni.  

## <a name="comparing-accounting-periods-using-period-formulas"></a><a name="comparing-accounting-periods-using-period-formulas"></a><a name="comparing-accounting-periods-using-period-formulas"></a>Samanburður á reikningstímabilum með reiknireglum tímabils

Fjárhagsskýrslan þín getur borið saman niðurstöður mismunandi reikningstímabila, svo sem síðastliðins mánaðar samanborið við sama mánuð á síðasta ári. Til að gera þetta skal opna síðuna **Dálkaskilgreining** og sérstilla hana með því að bæta reitnum **Formúla samanburðartímabils** við sem dálki. Frekari upplýsingar er að finna á [Sérstilling verksvæðis](ui-personalization-user.md). Hægt er að stilla þennan reit á reiknireglu tímabils.  

Bókhaldstímabil þarf ekki að vera í samræmi við dagatalið. Hvert fjárhagsár verður að hafa sami fjölda bókhaldstímabila á öllum fjárhagsárum, þótt hvert fjárhagsár geti verið mislangt.  

[!INCLUDE[prod_short](includes/prod_short.md)] nýtir formúluna fyrir tímabil til að reikna út lengd samanburðartímabils miðað við tímabilið sem fæst við dagsetningasíu á skýrslunni. Samanburðartímabilið byggir á upphafsdagsetningu dagsetningarsíunnar. Skammstafanirnar sem eiga við eru eftirfarandi:

| Skammstöfun | Lýsing                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| T            | Tímabil.                                                                                |
| ST           | Síðasta tímabil reikningsárs, hálfsárs eða ársfjórðungs.                                   |
| CP           | GT (gildandi tímabil) reikningsárs, hálfsárs eða ársfjórðungs. Notið GT í reiknireglum til að stilla tímabilið sem byrjar eða endar reikniregluna. Til dæmis RÁ\[1..GT\] sýnir tímann frá upphafi gildandi reikningsárs til gildandi tímabils.|
| FÁ           | Reikningsár. Til dæmis á RÁ\[1..3\] á við um fyrsta fjórðung yfirstandandi fjárhagsárs. |

Dæmi um reiknireglur:

| Formúla         | Lýsing                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Gildandi tímabil.                                                                                  |
| \-1T            | Fyrra tímabil.                                                                                 |
| \-1RÁ\[1..ST\]  | Allt fyrra reikningsár.                                                                     |
| \-1RÁ           | Yfirstandandi tímabil á fyrra reikningsári.                                                          |
| \-1RÁ\[1..3\]   | Fyrsti fjórðung fyrra reikningsárs.                                                           |
| \-1RÁ\[1..GT\]  | Frá upphafi fyrra fjárhagsárs til núverandi tímabils í fyrra reikningsári, bæði tímabilin tekin með |
| \-1RÁ\[GT..ST\] | Frá núverandi fjárhagsári til núverandi tímabils í fyrra reikningsári, bæði tímabilin tekin með   |

Ef þú vilt reikna eftir venjulegum tímabilum þarf í staðinn að slá inn reiknireglu í reitinn **Reikniregla samanburðartímabils**. Til dæmis ef reiturinn er stilltur á -1Á, ber [!INCLUDE [prod_short](includes/prod_short.md)] saman við tímabil einu ári á undan.

> [!NOTE]
> Það er ekki alltaf augljóst hvaða tímabil þú ert að bera saman vegna þess að þú getur stillt dagsetningarsíu í skýrslu sem nær yfir aðrar dagsetningar en bókhaldstímabilin sem bókhaldslykilinn sýnir. Ef þú býrð til fjárhagsskýrslu þar sem þú vilt bera þetta tímabil saman við sama tímabil í fyrra, stillir þú reitinn **Formúla samanburðardagsetningar** á *-1FY*. Síðan keyrir þú skýrsluna 28. febrúar og setur afmörkunardagsetninguna á janúar og febrúar. Fyrir vikið ber fjárhagsskýrsluna saman janúar og febrúar á þessu ári við janúar á síðasta ári, sem er eina bókhaldstímabilið af tveimur sem var lokið á síðasta ári.  

Frekari upplýsingar í [Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md)

## <a name="print-and-save-financial-reports"></a><a name="print-and-save-financial-reports"></a><a name="print-and-save-financial-reports"></a>Prenta og vista fjárhagsskýrslur

Þú getur prentað fjárhagsskýrslur með því að nota prentþjónustu tækisins þíns. [!INCLUDE[prod_short](includes/prod_short.md)] býður einnig að vista skýrslur Microsoft Excel sem vinnubækur, Microsoft Word skjöl, PDF- og XML-skrár.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
2. Á síðunni **Fjárhagsskýrslur** velurðu skýrsluna sem á að prenta og velur svo aðgerðina **Prenta**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Í reitnum **Prentari** er valið tækið sem skýrslan verður send til.
    1. Valkosturinn **(Meðhöndlað af vafra)** gefur til kynna að enginn prentari sé valinn fyrir skýrsluna. Í slíku tilfelli sér vafrinn um útprentun og sýnir stöðluð skref útprentunar þar sem hægt er velja staðbundinn prentara sem tengdur er við tækið þitt. **(Meðhöndlað af vafra)** er ekki í boði í farsímaforriti [!INCLUDE[prod_short](includes/prod_short.md)] eða forrit fyrir Microsoft Teams.
5. Velja aðgerðina **Prenta**.

### <a name="schedule-a-financial-report-or-save-as-a-pdf-word-or-excel-document"></a><a name="schedule-a-financial-report-or-save-as-a-pdf-word-or-excel-document"></a><a name="schedule-a-financial-report-or-save-as-a-pdf-word-or-excel-document"></a>Tímasetja fjárhagsskýrslu eða vista sem PDF-, Word- eða Excel-skjal

Hægt er að vista fjárlagaskýrslu sem skrá á mismunandi sniði, svo sem PDF, XML, Word eða Excel. Einnig er [!INCLUDE[prod_short](includes/prod_short.md)] hægt að stilla þetta til að búa til endurteknar fjárhagsskýrslur:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
2. Á síðunni **Fjárhagsskýrslur** skal velja aðgerðina **Prenta**.
3. Stilltu skýrsluna í samræmi við það og veldu svo aðgerðina **Senda til**.
4. Veljið skráarsnið eða aðgerðina **Tímasetja** og veljið **Í lagi**.
5. Fylltu út reitina til að búa til tímasetta eða endurtekna fjárhagsskýrslu. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
   * Þegar um endurteknar fjárhagsskýrslur er að ræða skal stilla reitina **Fyrsti upphafsdagur/tími** og **Lokadagsetning/tími** með fyrstu og síðustu dagsetningunni til að búa til fjárhagsskýrsluna. Veldu einnig á hvaða dögum skýrslan er mynduð með því að stilla reitinn fyrir **Fyrsti upphafsdagur/tími** með því að fylgja sniðinu sem útskýrt er í hlutanum [Nota dagsetningarformúlur](ui-enter-date-ranges.md#use-date-formulas).

## <a name="importing-or-exporting-financial-reports"></a><a name="importing-or-exporting-financial-reports"></a><a name="importing-or-exporting-financial-reports"></a>Innflutningur eða útflutningur fjárhagsskýrslna

Hægt er að flytja inn og út fjárhagsskýrslur sem RapidStart stillingarpakka, sem eru gagnlegar til að deila upplýsingunum með öðrum fyrirtækjum, til dæmis. Pakkinn er búinn til í .rapidstart-skrá, sem þjappar innihaldinu saman.

### <a name="import-and-export-financial-reports"></a><a name="import-and-export-financial-reports"></a><a name="import-and-export-financial-reports"></a>Flytja inn og flytja út fjárhagsskýrslur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
2. Veldu fjárhagsskýrsluna og veldu svo aðgerðina **Flytja inn fjárhagsskýrslu** eða **Flytja út fjárhagsskýrslu**, eftir því hvað á að gera.

> [!NOTE]
> Þegar þú flytur inn fjárhagsskýrslur verður fyrirliggjandi skrám með sömu heitum og þær sem þú flytur inn eytt.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/configure-financial-reports-dynamics-365-business-central/index).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Keyra og prenta skýrslur](ui-work-report.md)  
[Viðskiptagreind fjármála](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
