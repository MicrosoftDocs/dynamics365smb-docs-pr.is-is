---
title: Setja upp Intrastat-skýrslugerð
description: Lærðu að setja upp Intrastat-skýrslugerðaraðgerðir til að tilkynna viðskipti með fyrirtæki í öðrum löndum ESB.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.search.form: 308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077
ms.date: 09/02/2022
ms.author: altotovi
ms.openlocfilehash: b6adddb338af36f07abe4c6cb67c8113657ccb7c
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605489"
---
# <a name="set-up-intrastat-reporting"></a>Setja upp Intrastat-skýrslugerð

Öll fyrirtæki Evrópusambandsins (ESB) verða að tilkynna viðskipti sín með öðrum ríkjum ESB/svæðum. Fyrirtæki þurfa að tilkynna flutning vöru til tölfræðiyfirvalda í heimalandi sínu mánaðarlega og skila þarf skýrslu til skattyfirvalda. Intrastat er kerfið til að safna talnagögnum um vörur í þessum löndum/svæðum. Intrastat-skýrsla **er notuð** til að ljúka reglubundinni Intrastat-skýrslugerð (að jafnaði mánaðarlega), söfnun, upptöku og skýrslugerð um viðskipti með vörur samkvæmt löggjöf landsins.

Intrastat-skýrslugerð byggir á grunnreglum ESB sem gilda um öll lönd; í reynd er þó einhver munur innan einstakra landa. Hvert land hefur sínar reglur um hvað nákvæmlega og hvernig á að tilkynna.

> [!NOTE]
> Upplýsingar um Intrastat eiga ekki við um tilfærslu þjónustu milli landa heldur einungis á vörum (vörum og eignum). Ef staðbundin stjórnvöld krefjast skráningar á þjónustu á milli landa er hægt að gera það með **aðgerðinni Þjónustuskýrsla**.
>
> Gert er ráð fyrir að þessi eiginleiki verði fáanlegur frá nóvember 2022 sem app á [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646) þannig að ef þú vilt nota hann þarftu fyrst að setja hann upp á **síðu Framlengingarstjórnunar**.

> [!IMPORTANT]
> Þessi grein fjallar um nýja Intrastat-reynslu sem fáanleg er frá [!INCLUDE[prod_short](includes/prod_short.md)] útgáfu 21. Hafa skal samband við kerfisstjóra til að fá upplýsingar um hvaða útgáfu fyrirtækið á að nota og til að virkja nýju virkjunina.
>
> Lesa Intrastat-uppsetningu og notkunargrein síðustu útgáfu með [því að setja upp og Intrastat-](finance-how-setup-report-intrastat-v20.md) skýrslu.

## <a name="enable-the-new-intrastat-experience"></a>Gera nýja Intrastat-reynslu

Í 2022-2, [!INCLUDE[prod_short](includes/prod_short.md)] felur í sér endurhannaðan Intrastat-reynslu með auknum eiginleikum. Ef nýi Intrastat-aðgerðin er ekki virkjuð í umhverfi notanda er hægt að gera hana virka handvirkt af stjórnanda á **síðunni Feature Management**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **aðgangsstjórnun** og veljið síðan tengda tengilinn.
2. **Á síðunni Feature Management** er aðgerðin uppfærsla valin **: skipta skal fyrirliggjandi Intrastat-aðgerðum með nýju viðaukalínunni** Intrastat. Frekari upplýsingar um aðgangsstýringu til að [Virkja komandi möguleika fram í tímann](/dynamics365/business-central/dev-itpro/administration/feature-management) í efni stjórnunar.
3. **Í dálkinum virkt fyrir** dálk skal velja **alla notendur**.
4. Lestu skýringu á hvernig kerfið verður uppfært og veldu **Já** ef þú samþykkir.
5. Veldu **áfram** og þú munt fá grunnuppsetningu fyrir Intrastat. Lesa meira um Intrastat-uppsetninguna í [kaflanum Intrastat-afbrigði](#intrastat-configuration).
6. Eftir að uppsetningu lýkur er valið **Ljúka** til að byrja að nota nýju Intrastat-reynsluna.

> [!IMPORTANT]
> Hafðu í huga að ekki er hægt að nota gamlar og nýjar upplifanir samhliða. Áður en framlenging er gerð í framleiðsluumhverfi er mælt með því að gera fyrst og prófa þessa aðgerð í sandkassa umhverfi með afriti af framleiðslugögnum áður en þetta er gert í vinnsluumhverfi. Þegar ný notendareynsla er virkjuð í vinnsluumhverfinu er ekki hægt að snúa aftur í gömlu Intrastat-aðgerðirnar.

> [!NOTE]
> Það veltur á staðsetningu fyrirtækisins að aðgerðin sem lýst er hér að ofan verði næg. Til að landa með sértækar aðgerðir fyrir Intrastat-skýrslugerð ætti að gera Intrastat-App kleift að auki að auka við kjarnann.

## <a name="intrastat-configuration"></a>Skilgreining Intrastat

Áður en hægt er að nota Intrastat skýrslur eru nokkrar skilgreiningar sem þarf að setja upp.

### <a name="intrastat-reporting-setup"></a>Uppsetning Intrastat-tilkynninga

**Síðan Uppsetning** Intrastat-tilkynninga er notuð til að virkja Intrastat-skýrslugerð og stilla sjálfgildi fyrir hana. Hægt er að tilgreina hvort þörf sé á að skrá Intrastat úr sendingum (sendingar), kvittanir (komur) eða hvort tveggja eftir því sem þrösspokar eru settir af viðkomandi reglugerðum. Einnig er hægt að stilla sjálfgefnar færslugerðir fyrir regluleg og skilageg skjöl, notuð fyrir eðli færslutilkynninga.

Uppsetning Intrastat-skýrslugerðar:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **uppsetningu** Intrastat-skýrslu og veljið síðan tengda tengilinn.
2. **Opnið almenna** fastflipann og fyllið svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Taflan hér að neðan lýsir nokkrum helstu svæðunum:

   | Svæði | Lýsing |
   | --- | --- |
   | **Skýrslutökur** | Tilgreinir að taka verði með mótteknar vörur sem berast í Intrastat-skýrslum. |
   | **Tilkynna vörusendingar** | Tilgreinir að taka verði með afgreiddar vörur sem eru sendar í Intrastat-skýrslum. |
   | **Sendingar á grundvelli**  | Tilgreinir landskóða fyrir Intrastat-skýrslulínur. Hægt er að velja einn af valkostunum: **Selt-til lands**, **Reikn-lands** eða **Sendist-til-** land. |
   | **VSK nr. Byggður á** | Tilgreinir á grundvelli hvaða kóta viðskiptavinar/lánardrottins Virðisaukaskattur (VSK) er tekinn fyrir Intrastat-skýrsluna. Hægt er að velja einn af valkostunum: **Selt-til VSK** eða **Reikn**. |
   | **Fyrirtæki VSK nr. á skrá** | Tilgreinir hvernig VSK-númer fyrirtækis flytur út í Intrastat-skrána. Hægt er að velja einn af valkostunum: VSK-reg. nr., bæta við landskóta ESB sem forskeyti og fjarlægja ESB-landskóta úr VSK-reg. nr. |
   | **VSK númer lánardrottins á skrá** | Tilgreinir hvernig VSK-númer lánardrottins er flutt út í Intrastat-skrána. Hægt er að velja einn af valkostunum: VSK-reg. nr., bæta við landskóta ESB sem forskeyti og fjarlægja ESB-landskóta úr VSK-reg. nr. |
   | **Viðskiptavild VSK nr. á skrá** | Tilgreinir hvernig VSK-númer viðskiptavinar er flutt út í Intrastat-skrána. Hægt er að velja einn af valkostunum: VSK-reg. nr., bæta við landskóta ESB sem forskeyti og fjarlægja ESB-landskóta úr VSK-reg. nr. |
   | **Fá VSK fyrir félaga** | Tilgreinir hvaða gerð af **skýrslulínu** VSK-númer félaga er uppfærð. Aðeins er hægt að velja um innhreyfingar, aðeins fyrir sendingu eða báðar tegundir af línum, allt eftir staðbundnum þörfum. |
3. Opnið sjálfgefna fastflipann fyrir **færslur** og fyllið svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Taflan hér að neðan lýsir nokkrum helstu svæðunum:

   | Svæði | Lýsing |
   | --- | --- |
   | **Sjálfgefin Trans-gerð** | Tilgreinir sjálfgefna færslugerð fyrir reglulegar söluafhendingar, þjónustuafhendingar og innkaupakvittanir. |
   | **Sjálfgefin Trans-gerð – skil** | Tilgreinir sjálfgefna færslugerð fyrir söluskil, þjónustuskil og innkaupaskil. |
   | **Sjálfgefinn Einkabímaður VSK nr.** | Tilgreinir sjálfgefinn einka VSK númer ef einkaaðilinn verður að hafa sérvalið VSK-númer á Intrastat-skýrslunni. |
   | **Sjálfgefin 3-aðila viðskipti VSK nr.** | Tilgreinir sjálfgefið númer þriggja aðila á viðskiptum VSK ef VSK númer er ekki til. |
   | **Sjálfgefinn VSK fyrir Óþekkt ríki** | Tilgreinir sjálfgefið VSK-númer af óþekktri stöðu. |
   | **Sjálfgefinn Lands-/svæðiskóti** | Tilgreinir sjálfgefna viðtökulandskótann. |
4. **Opnið skýrslugerðarfastflipann** og fyllið svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Taflan hér að neðan lýsir nokkrum helstu svæðunum:

   | Svæði | Lýsing |
   | --- | --- |
   | **Aff. Kóði gagnaexi.** | Tilgreinir skilgreiningarkóta gagnaskipta til að búa til Intrastat-skrána. Það virkar aðeins ef **reiturinn skiptar kvittanir/afhendingar** er stilltur sem **Nr**. |
   | **Skipta út kvittunum/afhendingum skrám** | Tilgreinir hvort skrá eigi inn innhreyfingar og sendingar í tveimur aðskildum skrám. |
   | **Zip-skrá (-ar)** | Tilgreinir hvort skýrsluskráin (-s) skuli bætast við. zip skrána. |
   | **Data Exch. def. Code – kvittun** | Tilgreinir skilgreiningarkóta gagnaskipta til að búa til Intrastat-skrá fyrir mótteknar vörur. Það virkar aðeins ef **reiturinn skiptar kvittanir/afhendingar** er stilltur sem **Já**. |
   | **Data Exch. def. Code – sending** | Tilgreinir skilgreiningarkóta gagnaskipta sem mynda Intrastat-skrá fyrir afhentar vörur. Það virkar aðeins ef **reiturinn skiptar kvittanir/afhendingar** er stilltur sem **Já**. |
5. **Opnið númerfastflipann** til að setja upp **Intrastat-nr**.

### <a name="set-up-a-reporting-file"></a>Setja upp skýrslugerðarskrá

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **upplýsingar um Gengisskilgreiningar** og velja síðan tengda tengilinn.
2. Valið er aðgerðin **Nýtt**.
3. **Á flipanum Almennt** skal lýsa gagnaskiptaskilgreiningu, gerð gagnaskráa, skiltákn dálka, tengd kódeunits, XMLport og öðrum svæðum með því að fylla út reitina.
4. **Í flipanum Fastlínuskilgreiningar** skal lýsa sniði línanna í gagnaskránni með því að fylla út svæðin **eftir reitnum Tegund** línu og þar sem skilgreina þarf fjölda dálka fyrir þessa línu.
5. **Á flipanum fastir í Dálkaskilgreiningum** er fyllt út í línuna fyrir hvern áætlaðan dálk. Hægt er að skilgreina dálkheiti, gagnagerðir (*texta*, *dagsetningu* eða *aukastafi*), lengd línunnar með fastri breidd sem geymir dálkinn ef skráin er af gerðinni fastur texti og nokkrar aðrar færibreytur.
6. Svæðvörpun **svæða** er valin í fastflipa línuskilgreiningar **til að opna** síðuna vörpun **svæða.**
7. Ný færsla er stofnuð og á **flipanum Almennt** skal velja RÉTTA **töflukennið** (fyrir **Intrastat-skýrslulínuna**, velja 4812) og fylla síðan út fleiri reiti:
   1. Tilgreinið lyklaatriðaskrá til að raða Upprunafærslur fyrir útflutning í **reitnum lyklaatriðaskrá**.
   2. Velja rétta **vörpun Kódeseiningar**.
8. **Á flipanum Flýtivörpun í Svæðarpun** bætast við dálkar sem áður voru skilgreindir í **fastflipa Dálkaskilgreininganna**, síðan er eftirfarandi bætt við:
   1. **TILGREINIÐ kenni** svæðis fyrir hvern dálk.
   2. Tilgreinið umbreytingarregluna **fyrir hvern dálk sem þörf er á**. Hún Tilgreinir regluna sem umbreytir innfluttum texta í studd gildi áður en hægt er að tengja hann við tiltekið svæði í [!INCLUDE[prod_short](includes/prod_short.md)]. Þegar gildi er valið í þessu svæði er nákvæmt gildið fært inn í **reitinn umbreytingarregla** í **Reitun Exch. Field vörpun svæði buf.** Töflu og öfugt.
9. Ef flokka þarf færslur út frá einhverjum dálkum skal **Velja reitina sem á að nota við flokkun svæðisins**.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] forskilgreinda gagnaskiptaskilgreiningu fyrir Intrastat fyrir öll staðbundin lönd. Frekari upplýsingar um stofnun nýrra skilgreininga [á gagnaskiptum við uppsetningu á settum gögnum gr. um](across-how-to-set-up-data-exchange-definitions.md) gagnaskipti.

### <a name="set-mandatory-fields-with-the-intrastat-report-checklist"></a>Setja skyldusvæði með gátlista Intrastat-skýrslu

Í sumum löndum krefjast yfirvöld þess að Intrastat-skýrslur séu til dæmis afhendingaraðferðir vegna innkaupa eða annað gildi þegar Sala fer yfir ákveðinn þröskuld.

Til að stilla skyldusvæði og/eða gildi á **síðu Intrastat-skýrslu**:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **uppsetningu** Intrastat-skýrslu, velja síðan tengda tengilinn.
2. **Veljið aðgerðina Gátlisti** Intrastat-skýrslu.
3. Bæta nauðsynlegum línum til að athuga með eftirfarandi leiðbeiningum:
   1. Reiturinn Nr. **er** stilltur á svæði sem þarf að athuga fyrir gildi sem ekki eru tóm.
   2. **Reiturinn sía segð** er fylltur út ef þörf krefur, samkvæmt eftirfarandi reglum:
      1. Þegar Síusíðan **er opnuð** skal velja **síuna** sem nota á til að stöðva.
      2. Í næsta skrefi skal velja gildi sem tengist **afmörkuninni** sem notuð var.
      3. Ef fleiri afmarkanir er þörf til að fylla á þennan tiltekna reit er hægt að bæta annarri síu við eftir sömu skrefum.
      4. Þegar lokið er við að færa inn afmarkanir fyrir valið svæði er valið **í lagi**.
   3. **Gátreiturinn bakfærða síu** er valinn til að tilgreina að reiturinn fyrir svæðin sé aðeins keyrður á þeim línum sem stemma ekki við síunarsegðina. Ef línan er ekki afmörkuð er þetta svæði hunsað.

> [!NOTE]
> Þegar Afmörkunarsíðan **er opnuð** úr **afmörkunarsegðalínunni** er hægt að nota allar staðlaðar síusegðar sem tengjast reitnum sem á að afmarka.
>
> Gæta skal varúðar við uppsetningu villuleitarreglna, þar sem þær geta verið mismunandi hér á landi.

## <a name="use-custom-codeunits-in-intrastat-reporting"></a>Nota sérsniðna kódeseiningar við Intrastat-skýrslugerð

Ef óskað er eftir að breyta því hvernig Intrastat virkar og sjálfgefið afbrigði er ekki nægilegt er hægt að sérsníða kerfið með því að víkka út staðalaðgerðirnar. Ef þörf er á frekari breytingum á virkni Intrastat er hægt að þróa eigin kódeunits. Þegar kódeunits er stofnað þarf þó að gera frekari breytingar til að nota þær. Að stilla kerfið þannig að það noti eigin hluti:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **skilgreiningu** VSK-skýrslna og velja síðan tengda tengilinn.
2. **Á skilgreiningarsíðunni** VSK-skýrslur skal bæta við nýrri línu.
3. **Í reitnum Tegund** VSK-skýrslu skal velja **valkostinn Intrastat-** skýrsla.
4. **Í reitnum útgáfureitur** VSK-skýrslu skal tilgreina útgáfu skýrslunnar.
5. Að því loknu er hægt að bæta við kódeseiningum fyrir eftirfarandi valkosti: a. **Í reitnum leggja til línur í kenni** kódeunit skal tilgreina nýja kódeunit fyrir línur í Intrastat-skýrslulínunum.
   b. **Í REITNUM kenni** innihalds kódeunit skal tilgreina nýja Codeunit fyrir útflutning gagna sem skrá með því að nota skilgreiningu gagnaskipta.
   c. **Í reitnum Villuleita Kódeunit ID** skal tilgreina nýju kódeeiningarnar fyrir villuleit í línum Intrastat-skýrslu.

> [!IMPORTANT]
>
> Þessi lína verður að vera auð ef stöðluð kódeunits er notuð. Aðeins ætti að stofna línu og samskipa henni ef séreiningar hafa verið þróaðar.

## <a name="other-intrastat-configurations"></a>Aðrar Intrastat-skilgreiningar

> [!IMPORTANT]
> Viðskiptamanna-og lánardrottnaspjöld eru svæði, **gerð** Intrastat-félaga sem hefur sömu valkostagildi og **reiturinn félagagerð** : "" (autt), *fyrirtæki* og *einstaklingur*. **Reiturinn Tegund** Intrastat-félaga hefur skipt út **reitnum Tegund** félagar í Intrastat-skýrslu. **Reiturinn Félagagerð** er notaður í svæðinu fyrir eitt Evrugreiðslusvæði (SEPA) til að skilgreina SEPA-beina Debetskemað (CORE eða B2B). **Reiturinn Tegund** Intrastat-félaga er eingöngu notaður fyrir Intrastat-skýrslugerð. Þannig er hægt að tilgreina mismunandi gildi fyrir svæðin tvö ef þörf krefur.
>
> **Ef reiturinn Tegund** Intrastat-félaga er hafður auður er gildið úr **reitnum Tegund** félaga notað við Intrastat-skýrslugerð.

Fyrir **utan uppsetningu** Intrastat-skýrslu, **skilgreiningar** á gögnum og **gátlista** Intrastat-skýrslu þarf einnig að samskipa öðrum stillingum:

| Síða | Lýsing |
| ---- | ----------- |
| **Lönd/svæði** | Áður en byrjað er að nota Intrastat skýrslur verður einnig að setja upp **síðuna lönd/svæði**. Á þessari síðu þarf að bæta við **lands-/svæðiskóði** og **Intrastat-kóða** til að tilgreina kóta fyrir land/svæði sem á að eiga viðskipti við, þar sem það verður notað við Intrastat skýrslugerð. |
| **Tollskrárnúmerum** | Víða um land koma toll-og skattyfirvöld í 8 stafa kóða fyrir ýmsar vörur. Ef birgðafærslur eiga að innihalda nauðsynlegar upplýsingar þegar kerfið flytur þær í Intrastat-bókarlínuna verður að færa inn vörukóðann á **síðunni Tollflokkar**. Finndu kótana fyrir vörurnar sem fyrirtækið tekur við og Sláðu þær inn á **síðuna Tollflokkar**. |
| **Samgöngumáta** | Það eru 7 1-stafa kóðar fyrir Intrastat-flutningsaðferðir. **1** fyrir fjöðrun **, 2** fyrir Rail, **3** fyrir veg, **4** fyrir loft, **5** fyrir innsetningar, **7** fyrir fastar uppsetningar og **9** fyrir eigin própút (til dæmis að flytja bíl með því að aka honum). [!INCLUDE[prod_short](includes/prod_short.md)] krefst ekki þessara tilteknu kóða; Við mælum hins vegar með að lýsingarnar gefi svipaða merkingu. |
| **Færslugerðir** | Lönd og svæði hafa mismunandi kóða fyrir gerðir Intrastat-færslna, svo sem venjulega kaup og sölu, skipti á skilavörum og skipti á vörum sem ekki er skilað. Setja upp alla kóta sem eiga við um land/svæði notanda. Þessir kótar eru síðan notaðir **í fastflipanum erlend viðskipti** í sölu-og innkaupaskjölum og þegar vinnslu er skilað. |
| **Færslulýsingar** | Setja upp kóða fyrir viðauka lýsingar færslugerðarinnar. |
  > [!NOTE]
  > Byrjar í janúar 2022 Intrastat þarf að hafa mismunandi kóta fyrir færslur fyrir sendingar til einstaklinga eða VSK skráðra fyrirtækja og VSK skráðra fyrirtækja. Til samræmis við þessa kröfu er mælt með því að endurskoða og/eða bæta við nýjum eðli viðskipta á **síðunni tegundir** viðskipta í samræmi við kröfur í þínu landi. Einnig ætti að athuga í reitnum Tegund Intrastat-félaga og uppfæra **einstakling** fyrir einstaka eða ekki VSK-skráða viðskiptaviðskiptavini á viðkomandi *viðskiptavinasíðu* . **·** Ef þú ert ekki viss um rétta gerð Intrastat-félaga eða færslugerð sem á að nota, mælum við með að þú spyrjir sérfræðing á þínu landi eða svæði.

| **Sviði** | **Lýsing** |
| --------- | --------------- |
| **Nettóþyngd** | Þyngd er ein af grunnskilgreiningum sem tengjast Intrastat-skýrslugerð þar sem **Heildarþyngd** er skylda til skýrslugerðar. Til að vera tilbúin í þessa kröfu þarf einnig að fylla út **reitinn Nettóþyngd** á vörunni eða eignaspjaldinu. |
| **Kóði upprunakóða** | Notaðu tveggja bókstafa ISO alfa kóðana á vöru-eða eignaspjaldi fyrir landið þar sem góan var fengin eða framleidd. Ef góðkunni var framleitt í fleiri en einu landi, þá var upprunaland í landinu þar sem það var verulega unnið. |
| **VSK-númer kennitölu félagasamfélags í aðildarríkinu innflutnings** | Þá er VSK-kennitala meðrekstraraðila í aðildarríkinu í innflutningi. VSK-ID er einnig notað við skipti innan ESB-útflutningsgagna meðal aðildarríkjanna og heimilar aðildarríkjunum að ráðstafa mótteknum gögnum til innflutningsfyrirtækja í eigin landi. Tilkynningarskyldir aðilar þurfa að tilkynna sig á VSK-AUÐKENNI félagsins sem lýsti innan sambandsins kaupum á vörum í aðildarríkinu vegna innflutnings. |

Einnig er hægt að setja upp:

* **Vörukóði**: Tolla- og skattyfirvöld hafa sett fram númerakóða sem flokka vörur og þjónustu. Þú tiltekur þessa kóða á vörum.
* **Svæði** : viðbótarupplýsingar um lönd og svæði.
* **Innsláttar-/brottfararstaðir** : Tilgreinið þá staði sem eru sendingar eða móttöku vara til eða frá öðrum löndum. Flugvöllur er dæmi um innslátt eða brottfararstað. Komu/brottfararstaði er hægt að færa inn í sölu- og innkaupskjöl á flýtiflipanum **Erlend viðskipti**. Þessar upplýsingar verða einnig afritaðar úr birgðafærslum þegar Intrastatbók er stofnuð.
* **Viðbótarmælieining** : magn vöru fyrir Intrastat skýrslugerð getur verið annað hvort nettóvigt (í kílóum) eða fylgieining. Ef viðbótareiningar eru nauðsynlegar verður að skilgreina þær fyrir vöru og eignir.

#### <a name="set-up-transport-methods"></a>Setja upp flutningsaðferðir

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn **flutningsaðferðir**, veldu síðan tengda tengilinn.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="set-up-transaction-nature-codes"></a>Setja upp náttúrukóða færslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **færslugerðir** og velja tengdan tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="other-related-configurations"></a>Aðrar tengdar skilgreiningar

Áður en Intrastat-skýrsluaðgerðin er notuð þarf að skilgreina Sum svæði á vörunni, eignir, viðskiptavin og lánardrottnaspjöld.

#### <a name="item-cards"></a>Birgðaspjöld

Allar nauðsynlegar upplýsingar tengdar Intrastat á birgðaspjöldum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **atriði** og veljið síðan tengda tengilinn.
2. Velja atriðið sem á að samskipa.
3. **Útvíkkið kostnaðinn & bókun** og fyllið út **reitina Gjaldsvæði**, **viðbótarmælieining**, Kóti lands/svæðis og **upprunakóða**.
4. **Útvíkka birgðafastann** **og færa inn tugagildi í** reitinn Nettóþyngd.

> [!NOTE]
> Hægt er að nota mismunandi mælieiningar sem viðbótarmælieiningar. Ef þetta er ekki það sama og **grunnmælieiningin** þarf að skilgreina þessar mælieiningar á **síðunni Mælieiningar vöru**.

#### <a name="fixed-asset-cards"></a>Eignaspjöll

Að setja upp allar nauðsynlegar upplýsingar sem tengjast Intrastat á eignaspjöldum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn **eignir** og veldu síðan tengda tengilinn.
2. Velja eignina sem á að samskipa.
3. Útvíkka þarf **fastflipann Intrastat** og fylla út **reitina tollverð**, **nettóþyngd** og **viðbótarmælieining**.

> [!NOTE]
> Hægt er að nota mismunandi mælieiningar sem viðbótarmælieiningar. En hvaða **Mælieiningarkóti** sem valin er, verður magn **hans** í Intrastat-skýrslum alltaf 1.

#### <a name="vendor-cards"></a>Lánardrottnaspjöldum

Áður en lánardrottinn er notaður við Intrastat-skýrslugerð þarf að vera búið að sérmerkja **lands-/svæðiskóða** og **VSK-númer.** fyrir hvern þeirra eru auk frekari upplýsinga á kortasíðu **lánardrottna þeirra**:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **lánardrottna** og veljið síðan tengda tengilinn.
2. Veljið þann lánardrottinn sem á að samskipa.
3. **Á flipanum Intrastat-** fastvirði er hægt að stilla sjálfgefin gildi fyrir **sjálfgefna gerð. tegund**, **Sjálfgefin Flutningstillagerð-skil**, og **sjálfgefna flutningsmáta**.
4. **Útvíkkið fastflipann greiðslur** og Veljið valkostinn í **reitnum Intrastat-félagagerð** til að tilgreina hvort lánardrottinn er einstaklingur eða fyrirtæki í Intrastat-skýrslugerð.

#### <a name="customer-cards"></a>Viðskiptamannaspjöld

Áður en viðskiptavinur er notaður við Intrastat-skýrslugerð verður að vera búið að sérvera **lands-/svæðiskóta** og **VSK-númer.** fyrir hvern þeirra, auk frekari upplýsinga á kortasíðu **þeirra** viðskiptavina:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **viðskiptamenn** og veljið síðan tengda tengilinn.
2. Velja viðskiptavininn sem á að samskipa.
3. **Á flipanum Intrastat-** fastvirði er hægt að stilla sjálfgefin gildi fyrir **sjálfgefna gerð. tegund**, **Sjálfgefin Flutningstillagerð-skil**, og **sjálfgefna flutningsmáta**.
4. **Útvíkkið fastflipann greiðslur** og Veljið valkostinn í **reitnum Intrastat-félagagerð** til að tilgreina hvort lánardrottinn er einstaklingur eða fyrirtæki í Intrastat-skýrslugerð.

#### <a name="exclude-items-and-fixed-assets-from-intrastat-reporting"></a>Útiloka vörur og eignir úr Intrastat-skýrslugerð

Ef ástæða er til að undanskilja tiltekna vöru eða eign sem útiloka á Intrastat-skýrslugerð frá þarf að breyta um valkost á spjaldinu þeirra.

##### <a name="exclude-an-item-from-intrastat-reporting"></a>Útiloka vöru frá Intrastat-skýrslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **atriði** og veljið síðan tengda tengilinn.
2. Velja atriðið sem á að samskipa.
3. **Útvíkka kostnaðinn & bókun** og velja **síðan reitinn útiloka Intrastat-skýrslu**.

##### <a name="exclude-a-fixed-asset-from-intrastat-reporting"></a>Útiloka eign úr Intrastat-skýrslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn **eignir** og veldu síðan tengda tengilinn.
2. Velja eignina sem á að samskipa.
3. **Útvíkka Intrastat-** fastflipann og velja **síðan reitinn útiloka Intrastat-skýrslu**.

## <a name="country-specific-intrastat-setup"></a>Uppsetning Intrastat-sérlands

<!-- PM's note: Currently, we will add only the 'Overview' topic; the topic 'Manage Intrastat Country Specifics' and country details will wait until 21.1 when I update with all country-based details -->

Kröfur um Intrastat eru svipaðar í öllum aðildarríkjum EB, þótt þar séu mikilvægar undantekningar. Við kenningarskyldu skal vera einvörðungu beitt í öllum aðildarríkjunum. Hins vegar er munur á framkvæmd þar sem sum aðildarríkin veita leiðbeiningar um hvernig almennum meginreglum í reglugerðinni skuli beitt við tilteknar aðstæður (t.d. viðskiptaleg sýni, skil á vörum o. s. frv.). Þessar leiðbeiningar gætu valdið mismunandi árangri við ýmsar aðstæður í aðildarríkjum ESB. Vegna þess að í sumum löndum hafa sumir aukalega ákveðnar upplýsingar aðskildar frá öðrum löndum og þeir hafa einnig annað skráarsnið fyrir skýrslugerð.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun kl [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a>Sjá einnig .

[Intrastat-skýrsla í Viðskiptamiðinu](finance-how-report-intrastat.md)  
[Fjármálastjórnun](finance.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
