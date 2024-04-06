---
title: Búa til fjárhagsskýrslur með fjárhagsgögnum og reikningsflokkum
description: Lýsir því hvernig skal nota fjárhagsskýrslur til að búa til ýmis konar yfirlit og skýrslur fyrir greiningar á gögnum fyrir fjárhagslega frammistöðu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---
# <a name="prepare-financial-reporting-with-financial-data-and-account-categories"></a>Undirbúa fjárhagsskýrslugerð með fjárhagsgögnum og lykilflokkum

Eiginleikinn **Ársskýrslur** veitir innsýn í fjárhagsgögnin sem birtast í bókhaldslyklinum (COA). Hægt er að setja upp fjárhagsskýrslur til að greina tölur á fjárhagsreikningum og bera saman fjárhagsfærslur og áætlunarfærslur. Niðurstöðurnar birtast í myndritum og skýrslum í Hlutverkamiðstöðinni, t.d. sjóðstreymisritinu og rekstrarreikningi og efnahagsskýrslum. Þessar tvær skýrslur eru opnaðar, til dæmis með aðgerðinni **Ársreikningar** á heimasíðum viðskiptastjóra og endurskoðanda.  

[!INCLUDE[prod_short](includes/prod_short.md)] veitir sýnishorn fjárhagsskýrslna sem hægt er að nota strax sem sniðmát. Einnig er hægt að setja upp eigin skýrslur til að tilgreina tölurnar sem á að bera saman. Til dæmis er hægt að stofna fjárhagsskýrslur til að reikna út hagnaðarhlutfall með því að nota víddir eins og deildir eða viðskiptavinaflokka. Fjöldi fjárhagsskýrslna sem hægt er að búa til er ótakmarkaður og þarfnast ekki þátttöku forritara.  

## <a name="prerequisites-for-financial-reporting"></a>Skilyrði fyrir fjárhagsskýrslugerð

Uppsetning fjárhagsskýrslna krefst skilnings á skipulagi bókhaldslykilsins. Það eru þrjú lykilhugtök sem líklega þarf að vekja athygli á áður en fjárhagsskýrslurnar eru hannaðar:

- Varpa fjárhagsbókunarreikningum í fjárhagsreikningsflokka.
- Hanna hvernig víddir eru notaðar.
- Setja upp fjárhagsáætlanir.

Fjárhagsreikningsflokkar einfaldar skilgreiningar fjárhagsskýrslunnar og auðvelda breytingum í uppbyggingu bókhaldslykils. Fá nánari upplýsingar í [Nota fjárhagsreikningsflokka til að breyta útliti ársreikninga](#use-gl-account-categories-to-change-the-layout-of-your-financial-statements).

Með uppsetningu vídda er hægt að sneiða og teninga fjárhagsgögnin á þann hátt sem fyrirtæki notanda skiptir máli. Frekari upplýsingar eru í [Vinna með víddir](finance-dimensions.md). 

Ef skoða á fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum þarf að búa til fjárhagsáætlanir. Frekari upplýsingar eru á [Stofna fjárhagsáætluanir](finance-how-create-budgets.md).

## <a name="financial-reports"></a>Fjárhagsskýrslur

Fjárhagsskýrslur raða reikningum úr bókhaldslyklum þínum á þann hátt sem auðveldar framsetningu gagna. Hægt er að setja upp margvísleg útlit til að skilgreina upplýsingarnar á að finna í bókhaldslyklinum. Fjárhagsskýrslur koma einnig fram staður fyrir útreikninga sem ekki er hægt að gera beint í bókhaldslyklinum. Til dæmis er hægt að búa til millisamtölur fyrir reikningsflokka og setja þær inn í aðrar samtölur Annað dæmi er að reikna út hagnaðarhlutfall á víddum eins og deildum eða viðskiptavinaflokkum. Þar að auki getur þú síað fjárhagsfærslur og fjárhagsáætlanafærslur, t.d. eftir nettóbreytingum eða debetupphæð.

> [!NOTE] 
> Í stærðfræði er fjárhagsskýrsla skilgreind eins og hún er skilgreind:
>
> - Vektor línuskilgreininga sem skilgreina hvað þarf að reikna.
> - Vektor dálkskilgreininga sem skilgreinir gögnin fyrir útreikninginn.
>
> Fjárhagsskýrslan er síðan ytri vara þessara tveggja vektora, þar sem hvert reitsgildi er reiknað samkvæmt reiknireglunni í línunni sem notuð er fyrir skilgreiningu gagna úr dálknum.

:::image type="content" source="media/financial-report-definition.svg" alt-text="Sýnir hvernig fjárhagsskýrsla er sett upp úr línuskilgreiningu og dálkskilgreiningu." lightbox="media/financial-report-definition.svg":::

Síðan **Ársskýrslur** sýnir hvernig öllum fjárhagsskýrslum fylgir mynstur sem samanstendur af eftirfarandi eigindum:

* Heiti (kóti)
* Heimildasamstæða
* Línuskilgreining
* Dálkskilgreining

:::image type="content" source="media/financial-reports.png" alt-text="Sýnir hvernig allar fjárhagsskýrslur eru settar upp úr línuskilgreiningu og dálkskilgreiningu." lightbox="media/financial-reports.png":::

> [!NOTE]
> Sýnishornaskýrslurnar í [!INCLUDE[prod_short](includes/prod_short.md)] eru ekki tilbúnar til notkunar úr kassanum. Eftir því hvernig fjárhagsreikningar, víddir, fjárhagsreikningaflokkar og áætlanir eru settir upp þarf að leiðrétta sýnilínu- og dálkskilgreiningar og fjárhagsskýrslurnar sem þeir eru notaðir í til að uppfylla uppsetninguna.

Einnig er hægt að nota reiknireglur til að bera saman tvær eða fleiri fjárhagsskýrslur og dálkskilgreiningar. Samanburður gerir kleift að gera eftirfarandi hluti:

* Búa til sérsniðnar viðskiptaskýrslur.
* Búa til eins mörg fjárhagsskýrslur og þú þarft, hver með einkvæmt heiti.
* Búa til uppsetningu skýrslu og prenta út skýrslurnar með núverandi tölum.

## <a name="learning-path-create-financial-reports-in-microsoft-dynamics-365-business-central"></a>Námsslóð: Búa til fjárhagsskýrslur í Microsoft Dynamics 365 Business Central

Viltu fræðast um hvernig á að stofna áætlanir og nota síðan fjárhagsskýrslur, víddir og línu- og dálkaskilgreiningar til að búa til fjárhagsskýrslur sem yfirleitt eru nauðsynlegar fyrir flest fyrirtæki?

Hefja nám á námsleiðinni [Búa til fjárhagsskýrslur í Microsoft Dynamics 365 Business Central](/training/paths/create-financial-reports-dynamics-365-business-central)

## <a name="create-a-new-financial-report"></a>Stofna nýja fjárhagsskýrslu

Fjárhagsskýrslur eru notaðar til að greina fjárhagsreikninga eða bera saman fjárhagfærslur og fjárhagsáætlunarfærslur. Hægt er til dæmis að skoða fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum.

Fjárhagsskýrslurnar í stöðluðu útgáfunni [!INCLUDE[prod_short](includes/prod_short.md)] henta hugsanlega ekki viðskiptaþörfum. Til að búa til eigin fjárhagsskýrslur á skjótan hátt skaltu byrja á því að afrita þær sem þegar eru til, eins og lýst er í skrefi þrjú hér á eftir.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.  
1. Á síðunni **Fjárhagsskýrslur** skal velja aðgerðina **Nýtt** til að búa til nýtt heiti fjárhagsskýrslu. Einnig er hægt að nota aftur stillingar úr fyrirliggjandi fjárhagsskýrslu með því að velja aðgerðina **Afrita fjárhagsskýrslu** .
1. Fært er inn stutt heiti skýrslunnar (því er ekki hægt að breyta) og lýsingu.
1. Velja línuskilgreiningu og dálkaskilgreiningu.
1. Valfrjálst er að velja greiningaryfirlit fyrir línu- og dálkaskilgreiningar.
1. Veljið aðgerðina **Breyta fjárhagsskýrslu** til að fá aðgang að fleiri eiginleikum fjárhagsskýrslunnar.
1. Á flýtiflipanum **Valkostir** er hægt að breyta skýrslulýsingunni, breyta línu- og dálkaskilgreiningum og skilgreina hvernig eigi að sýna dagsetningar. Dagsetningar geta verið dag- og viku-/mánaðar-/ársfjórðungs-/ársfjórðungsstigveldi eða notað reikningstímabil. Nánari upplýsingar eru notaðar í Samanburður á reikningstímabilum með því að [nota reiknireglur tímabila](#comparing-accounting-periods-using-period-formulas).
1. Á flýtiflipanum **Víddir** er hægt að skilgreina víddarafmarkanir fyrir skýrsluna.
1. Hægt er að forskoða skýrsluna á svæðinu fyrir neðan **flýtiflipann Víddir** .

> [!TIP]
> Þegar búið er að stofna fjárhagsskýrslu er hægt að nota síðuna **Fjárhagsskýrsla** til að forskoða og staðfesta hana. Til að opna síðuna skal velja aðgerðina **Skoða fjárhagsskýrslu** .  

> [!NOTE]
> Þegar fjárhagsskýrsla er opnuð í Skoða eða Breyta stillingu er afmörkunarsvæðið tiltækt. Ekki nota afmörkunarsvæðið til að setja afmarkanir á gögnin í skýrslunni. Slíkar afmarkanir geta valdið villum eða hugsanlega afmarka gögnin ekki í raun. Þess í stað eru reitirnir á flýtiflipunum **Valkostir** og **Víddir notaðir** til að setja upp afmarkanir fyrir skýrsluna.

### <a name="create-or-edit-a-row-definition"></a>Stofna eða breyta línuskilgreiningu

Línuskilgreiningar í fjárhagsskýrslum eru staður fyrir útreikninga sem ekki er hægt að gera beint í bókhaldslyklinum. Til dæmis er hægt að búa til millisamtölur fyrir reikningsflokka og setja þær inn í aðrar samtölur Einnig er hægt að reikna milliskref sem ekki eru sýnd í lokaskýrslunni.

1. Á síðunni **Fjárhagsskýrslur** skal velja viðeigandi fjárhagsskýrslu og velja svo aðgerðina **Breyta línuskilgreiningu** .
1. Veldu aðgerðirnar **Setja inn fjárhagsreikninga**, **Setja inn sjóðstreymisreikninga** og **Setja inn kostnaðartegundir** til að búa til línu fyrir hverja fjárhagslega einingu sem á að greina. Til dæmis gæti ein lína verið fyrir núverandi eignir og önnur röð fyrir eignir. Skoðaðu fjármálaskýrslurnar í CRONUS sýnifyrirtækinu til að fá innblástur.

    > [!NOTE]
    > **Línan nr.** reiturinn sýnir fyrstu 10 stafina í kennimerki, eins og reikningsnúmer. Ef einingum með kennum sem byrja á sömu 10 stöfum er bætt við eru tvítekningar í reitnum **Línunr.** . Ef þörf er á er hægt að breyta kennimerkjum handvirkt eftir að þú hefur sett inn einingarnar. Öll kennimerkin eru birt í reitnum **Samantekt**.

> [!NOTE]
> Dálkarnir sem eru skilgreindir í hverri línu í línuskilgreiningunni tákna dálka þrjá og upp á síðunni **Fjárhagsskýrsla** . Fyrstu tveir dálkarnir, **Dálkanr.** og **Lýsing**, eru fastar.  

### <a name="create-or-edit-a-column-definition"></a>Stofna eða breyta dálkaskilgreiningu

Nota dálkaskilgreiningar til að tilgreina dálkana sem á að hafa með í skýrslunni. Til dæmis er hægt að hanna skýrsluuppsetningu til að bera saman breytingu og stöðu fyrir sama tímabil á þessu ári og síðasta ári. Hægt er að hafa allt að 15 dálka í dálkskilgreiningu. Til dæmis eru margir dálkar gagnlegir til að birta áætlanir í 12 mánuði með dálki sem sýnir samtöluna.

> [!NOTE]
> Prentuð/forskoðuð/vistuð útgáfa fjárhagsskýrslu sýnir mest fimm dálka. Ef fjárhagsskýrsla er hins vegar aðeins ætluð til greiningar á síðunni **Fjárhagsskýrsla** er hægt að búa til eins marga dálka og óskað er.

1. Á síðunni **Fjárhagsskýrslur** skaltu velja viðeigandi fjárhagsskýrslu og velja svo aðgerðina **Breyta dálkskilgreiningu**.
1. Á síðunni **Dálkskilgreining** skal búa til línu fyrir hvern dálk þar sem fjárhagsgögn eru sýnd í fjárhagsskýrslunni. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Velja **Í lagi**.
1. Opnaðu síðuna **Fjárhagsskýrsla** öðru hverju til að staðfesta að nýja dálkskilgreiningin virki eins og til er ætlast.

### <a name="create-a-column-definition-to-calculate-percentages"></a>Stofna dálkaskilgreiningu til að reikna prósentur

Hugsanlega þarf að vera dálkur í fjárhagsskýrslu til að reikna prósentur af samtölu. Til dæmis, ef línur skipta sölu eftir vídd kann að vera þörf á dálki sem birtir prósentuhlutfall heildarsölu sem hver lína stendur fyrir.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 2.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
1. Á síðunni **Fjárhagsskýrslur** skal velja Fjármálaskýrsla.  
1. Veljið aðgerðina **Breyta fjárhagsskýrslu** til að setja upp fjárhagsskýrslulínu til að reikna út samtöluna sem prósenturnar byggjast á.  
1. Línu er bætt við fyrir ofan fyrstu línuna sem á að birta prósentu fyrir.  
1. Fyllið inn í reitina í línunni sem hér segir: Í **Tegund samantektar** reitnum er færður inn **Valinn stofn fyrir prósentur**. Í reitnum **Samantekt** er færð inn formúlu fyrir samtöluna sem prósentan miðast við. T. d. ef lína 11 inniheldur heildarsölu, skal færa inn **11**.  
1. Veljið aðgerðina **Breyta dálkskilgreiningu** til að setja upp dálk.  
1. Reitirnir í línunni eru fylltir út sem hér segir. Í reitnum **Dálktegund** er valin **Reikniregla**. Í reitnum **Formúla** er færð inn formúla fyrir upphæðina sem reikna á prósentuhlutfall fyrir, með prósentutákni (%) þar fyrir aftan. Til dæmis ef dálkur N inniheldur nettóbreytinguna, er fært inn **N%**.  
1. Skref 4 til 7 eru endurtekin fyrir hvern flokk línu sem skipta á niður eftir prósentum.

## <a name="use-gl-account-categories-to-change-the-layout-of-your-financial-statements"></a>Nota flokka fjárhagsreikninga til að breyta útliti ársreikninga

Hægt er að nota lykiltegundir fjárhagsreikninga til að breyta sniði fjárhagsskýrslna. T.d. þegar reikningaflokkar hafa verið settir upp á síðunni **Flokkar** fjárhagsreikninga, er hægt að velja aðgerðina **Mynda fjárhagsskýrslu** og uppfæra undirliggjandi fjárhagsskýrslur fyrir almennar fjárhagsskýrslur. Næst þegar keyrð er önnur þessara skýrslna, svo sem **skýrslan Stöðuyfirlit**, nýjar samtölur og undirfærslur er bætt við.

Annar ávinningur af því að nota fjárhagsreikningaflokka yfir hráa fjárhagsreikninga í línuskilgreiningum er að breyting á uppbyggingu bókhaldslykils hefur engin áhrif á fjárhagsskýrslur.

> [!NOTE]
> Efsta stigs reikningsflokkarnir, svo sem **Skuldahnútur**, eru fastir og ekki er hægt að bæta við eigin. Hins vegar er hægt að eyða og bæta við reikningsflokkum á neðri stigum til að skilgreina hvernig tengt fjárhagsskýrsla birtist í skýrslum.
>
> Þú ættir að stofna og skipuleggja eigin lægri flokka fjárhagsreikninga frá grunni, í stigveldi ef þörf er á, frekar en að reyna að endurraða þeim sem fyrir eru. Til dæmis er hægt að endurhanna **Skuldir** til að innihalda nýtt **Eigið fé** og síðan **Skammtímaskuldir** og **Langtímaskuldir**. Nánari upplýsingar um [vörpun fjárhagsreikninga í lykilflokka](finance-general-ledger.md#account-categories).

## <a name="using-dimensions-in-financial-reports"></a>Notkun vídda í fjárhagsskýrslum

Í fjárhagsgreiningu er vídd tiltekin gögn sem má bæta við færslu sem einskonar merki. Þessi gögn eru notuð til að flokka saman færslur með svipuð einkenni, eins og viðskiptamenn, svæði, vörur og sölumenn og sækja þessa hópa á auðveldan hátt til greiningar. Hægt er að nota víddir í færslum í færslubókum, fylgiskjölum og áætlunum.

Hver vídd lýsir áherslu greiningar. Tvívíð greining gæti því til dæmis verið sala eftir svæðum. Með því að nota fleiri en tvær víddir þegar færsla er stofnuð er hægt að framkvæma flóknari greiningar. Dæmi um flókna greiningu er að kanna sölu á hverja söluherferð fyrir hvern viðskiptamannaflokk á hvert svæði. Það veitir meiri innsýn í reksturinn, svo sem hversu vel fyrirtækið þitt starfar, hvar það er eða ekki þrífst ekki og hvar þú ættir að ráðstafa meiri fjármunum. Innsýnin hjálpar þér að taka upplýstar viðskiptaákvarðanir. Frekari upplýsingar eru í [Vinna með víddir](finance-dimensions.md).

## <a name="set-up-financial-reports-with-overviews"></a>Setja upp fjárhagsskýrslur með yfirlitum

Hægt er að nota fjárhagsskýrslu til að búa til yfirlit sem ber fjárhagstölur saman við áætlunartölur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 3.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
1. Á síðunni **Fjárhagsskýrslur** skal velja Fjármálaskýrsla.  
1. Veldu aðgerðina **Breyta línuskilgreiningu**  
1. Á síðunni **Línuskilgreining** í reitnum **Heiti** skal velja sjálfgefið heiti fjárhagsskýrslu.
1. Veldu aðgerðina **Setja inn fjárhagsreikninga**.  
1. Reikningarnir sem eiga að vera í yfirlitinu eru valdir og smellt á **Í lagi**.

    Reikningarnir eru settir inn í fjárhagsskýrsluna. Einnig er hægt að breyta dálkaskilgreiningunni ef þess er óskað.  
1. Veldu aðgerðina **Breyta fjárhagsskýrslu**.  
1. Á síðunni **Fjárhagsskýrsla** á flýtiflipanum **Víddir** stillir þú á fjárhagsáætlunarsíuna á það nafn á síunni sem þú vilt nota.  
1. Velja **Í lagi**.  

Nú er hægt að afrita áætlunaryfirlitið og líma það inn í töflureikni.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Samanburður á reikningstímabilum með reiknireglum tímabils

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

## <a name="print-and-save-financial-reports"></a>Prenta og vista fjárhagsskýrslur

Þú getur prentað fjárhagsskýrslur með því að nota prentþjónustu tækisins þíns. [!INCLUDE[prod_short](includes/prod_short.md)] Býður einnig upp á möguleika á að vista skýrslur sem Excel vinnubækur, Word skjöl, PDF og XML skrár.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
1. Á síðunni **Fjárhagsskýrslur** velurðu skýrsluna sem á að prenta og velur svo aðgerðina **Prenta**.
1. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Í reitnum **Prentari** er valið tækið sem skýrslan verður send til.
    1. Valkosturinn **(Meðhöndlað af vafra)** gefur til kynna að enginn prentari sé valinn fyrir skýrsluna. Í slíku tilfelli sér vafrinn um útprentun og sýnir stöðluð skref útprentunar þar sem hægt er velja staðbundinn prentara sem tengdur er við tækið þitt. **(Meðhöndlaður af vafranum)** er ekki tiltækt í farsímaforritinu [!INCLUDE[prod_short](includes/prod_short.md)] eða forritinu fyrir teymi.
1. Velja aðgerðina **Prenta**.

### <a name="schedule-a-financial-report-or-save-as-a-pdf-word-or-excel-document"></a>Tímasetja fjárhagsskýrslu eða vista sem PDF-, Word- eða Excel-skjal

Hægt er að vista fjárlagaskýrslu sem skrá á mismunandi sniði, svo sem PDF, XML, Word eða Excel.  [!INCLUDE[prod_short](includes/prod_short.md)] Einnig er hægt að búa til ítrekaðar fjárhagsskýrslur:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
1. Á síðunni **Fjárhagsskýrslur** skal velja aðgerðina **Prenta**.
1. Stilltu skýrsluna í samræmi við það og veldu svo aðgerðina **Senda til**.
1. Veljið skráarsnið eða aðgerðina **Tímasetja** og veljið **Í lagi**.
1. Fylltu út reitina til að búa til tímasetta eða endurtekna fjárhagsskýrslu. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].<br><br>Þegar um endurteknar fjárhagsskýrslur er að ræða skal stilla reitina **Fyrsti upphafsdagur/tími** og **Lokadagsetning/tími** með fyrstu og síðustu dagsetningunni til að búa til fjárhagsskýrsluna. Veldu einnig á hvaða dögum skýrslan er mynduð með því að stilla reitinn fyrir **Fyrsti upphafsdagur/tími** með því að fylgja sniðinu sem útskýrt er í hlutanum [Nota dagsetningarformúlur](ui-enter-date-ranges.md#use-date-formulas).

## <a name="importing-or-exporting-financial-report-definitions"></a>Innflutningur eða útflutningur fjárhagsskýrsluskilgreininga

Hægt er að flytja inn og út fjárhagsskýrslu/línuskilgreiningar sem RapidStart skilgreiningarpakka sem henta vel til að deila upplýsingum með öðrum fyrirtækjum. Pakkinn er búinn til í .rapidstart-skrá, sem þjappar innihaldinu saman.

> [!NOTE]
> Þegar fjárhagsskýrslu/línuskilgreiningar eru fluttar inn koma fyrirliggjandi færslur með sömu heitum og þær sem verið er að flytja inn í stað nýju skilgreininganna. Athuga skal að skilgreiningarpakkinn fyrir skýrsluskilgreiningu skrifar ekki yfir fyrirliggjandi línu- eða dálkskilgreiningar sem eru notaðar í skýrsluskilgreiningunni.

Til að flytja inn eða út fjárhagsskýrsluskilgreiningar skal fylgja eftirfarandi skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") veldu táknið, sláðu inn **Fjárhagsskýrslur** og veldu síðan viðkomandi tengil.
1. Veldu fjárhagsskýrsluna og veldu svo aðgerðina **Flytja inn fjárhagsskýrslu** eða **Flytja út fjárhagsskýrslu**, eftir því hvað á að gera.

Til að flytja inn og út línuskilgreiningar fjárhagsskýrslu skal fylgja eftirfarandi skrefum:

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleika 4.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **línuskilgreiningar** og velja síðan viðeigandi tengil.
1. Veljið línuskilgreininguna og veljið svo aðgerðina **Flytja inn** línuskilgreiningu eða **Útflutningslínuskilgreiningu** eftir því hvað á að gera.

## <a name="see-also"></a>Sjá einnig .

[Skoða og prenta skýrslur](ui-work-report.md)  
[Viðskiptagreind fjármála](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
