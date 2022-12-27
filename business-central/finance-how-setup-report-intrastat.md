---
title: Setja upp Intrastat skýrslugerð
description: Lærið hvernig skal setja upp Intrastat skýrslugerð og hvernig skal skrá viðskipti við fyrirtæki í öðrum ESB-löndum.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605489"
---
# <a name="set-up-intrastat-reporting"></a>Setja upp Intrastat skýrslugerð

Öll fyrirtæki í löndum innan Evrópusambandsins (ESB) þurfa að gefa öðrum löndum/svæðum innan sambandsins skýrslur um viðskipti sín. Einnig þarf að gefa hagstofu viðkomandi lands/svæðis mánaðarlega skýrslu um hreyfingu vöru og skýrsluna þarf að afhenda skattayfirvöldum. Intrastat er kerfið til að safna saman tölfræði um vöruviðskipti innan þessara landa/svæða. Þú notar **Intrastat-skýrsla** til að ljúka reglubundinni Intrastat skýrslugerð (yfirleitt mánaðarlega), söfnun, skráningu og skýrslugerð vegna vöruviðskipta í samræmi við löggjöf á hverjum stað.

Intrastat skýrslugerð er byggð á grunnreglugerðum ESB sem gilda í öllum löndum, hins vegar er í reynd þó nokkur munur á milli landanna. Í hverju landi gilda sérstakar reglur um hvað nákvæmlega á að tilkynna og hvernig.

> [!NOTE]
> Intrastat upplýsingar eiga ekki við um þjónustuflutninga milli landa, heldur aðeins vörur (vörur og eignir). Ef stjórnvöld á staðnum gera kröfu um að hreyfing þjónustu sé skráð milli landa er hægt að gera það með því að nota eiginleikann **Þjónustuyfirlýsing**.
>
> Gert er ráð fyrir að þessi eiginleiki verði í boði frá og með nóvember 2022 sem forrit á [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646) svo ef þú vilt nota hann þarftu fyrst að setja hann upp á síðunni **Viðbótastjórnun**.

> [!IMPORTANT]
> Þessi grein fjallar um nýja Intrastat reynslu í boði frá [!INCLUDE[prod_short](includes/prod_short.md)] útgáfu 21. Hafðu samband við kerfisstjóra til að fá upplýsingar um hvaða útgáfu fyrirtækið notar og til að virkja nýja eiginleikann.
>
> Lestu fyrri útgáfu af Intrastat uppsetningar- og notkunargrein á [Setja upp og skrá Intrastat](finance-how-setup-report-intrastat-v20.md).

## <a name="enable-the-new-intrastat-experience"></a>Gera nýju Intrastat upplifunina virka

Útgáfutímabil 2 árið 2022 [!INCLUDE[prod_short](includes/prod_short.md)] felur í sér endurhannaða Intrastat upplifun með ítarlega eiginleika. Ef nýi Intrastat eiginleikinn er ekkiur virk í umhverfinu þínu getur stjórnandi virkjað hana handvirkt á síðunni **Eiginleikastjórnun**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eiginleikastjórnun** og velja síðan viðkomandi tengil.
2. Á síðunni **Eiginleikastjórnun** skaltu velja **Eiginleikauppfærsla: Skipta út núverandi Intrastat-virkni fyrir nýja Intrastat-viðbótarlínu**. Frekari upplýsingar um eiginleikastjórnun hjá [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management) í efni fyrir stjórnendur.
3. Á dálknum **Virkja fyrir** skal velja **Alla notendur**.
4. Lestu útskýringuna á því hvernig kerfið verður uppfært og veldu **Já** ef þú samþykkir það.
5. Veldu **Áfram** og þá færðu grunnuppsetningu fyrir Intrastat. Lestu meira um uppsetningu Intrastat í hlutanum [Stilling Intrastat](#intrastat-configuration).
6. Eftir að uppsetningu er lokið skaltu velja **Ljúka** til að byrja að nota nýju Intrastat upplifunina.

> [!IMPORTANT]
> Hafðu í huga að þú getur ekki notað gamlar og nýjar upplifanir samhliða. Áður en viðbótin er virkjuð í framleiðsluumhverfi er mælt með því að þessi eiginleiki sé fyrst virkjaður og prófaður í sandkassaumhverfi með afriti af framleiðslugögnum áður en þetta er gert í framleiðsluumhverfi. Þegar þú hefur virkjað nýja notendaupplifun í framleiðsluumhverfinu getur þú ekki farið aftur í gömlu Intrastat-aðgerðirnar.

> [!NOTE]
> Það fer eftir staðsetningu fyrirtækisins hvort nóg sé að virkja eiginleikann sem lýst er hér að ofan. Í löndum með sérstaka eiginleika fyrir Intrastat skýrslugerð, ættir þú að virkja svæðisbundna Intrastat-forritið viðbótar við meginviðbótina.

## <a name="intrastat-configuration"></a>Uppsetning Intrastat

Áður en hægt er að nota Intrastat skýrslur þarf að setja upp nokkrar stillingar.

### <a name="intrastat-reporting-setup"></a>Uppsetning Intrastat-skýrslugerðar

Síðan **Uppsetning Intrastat-skýrslugerðar** er notuð til að virkja Intrastat-skýrslugerð og velja sjálfgefnar stillingar fyrir hana. Hægt er að tilgreina hvort eigi að gefa Intrastat-skýrslu um afhendingum (sendingum), kvittunum (komum) eða bæði, háð mörkum sem staðbundnar reglugerðir segja til um. Einnig er hægt að velja sjálfgefnar færslugerðir fyrir venjuleg fylgiskjöl eða fylgiskjöl vöruskila, notaðar samkvæmt einkennum skýrslugerðar fyrir færslur.

Svona á að setja upp Intrastat-skýrslugerð:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning Intrastat-skýrslu** og velja síðan viðkomandi tengil.
2. Opnaðu flýtiflipann **Almennt** og fylltu út reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Taflan hér að neðan lýsir nokkrum lykilreitum:

   | Svæði | Lýsing |
   | --- | --- |
   | **Skrá kvittanir** | Tilgreinir að taka verði með mótteknar vörur sem berast í Intrastat-skýrslum. |
   | **Skrá afhendingar** | Tilgreinir að taka verði með afgreiddar vörur sem eru sendar í Intrastat-skýrslum. |
   | **Sendingar byggðar á**  | Tilgreinir landskóða fyrir Intrastat-skýrslulínur. Hægt er að velja um einn af eftirfarandi kostum: **Selt-til – Land**, **Reikningsfærist á - Heiti lands** eða **Sendist til - Heiti lands**. |
   | **VSK-nr. byggt á** | Tilgreinir á grundvelli hvaða viðskiptavinar/lánardrottins VSK-númer er tekið fyrir Intrastat-skýrsluna. Hægt er að velja um einn af eftirfarandi valkostum: **Selt-til – VSK** eða **Reikningsfærslu-VSK**. |
   | **Skráð VSK-númer fyrirtækis** | Tilgreinir hvernig VSK-númer fyrirtækisins er flutt út í Intrastat skrána. Þú getur valið einn af eftirfarandi valkostum: VSK-númer með því að bæta við ESB-landskóða sem forskeyti og fjarlægja ESB-landskóða úr VSK-númeri. |
   | **Skráð VSK-númer lánardrottins** | Tilgreinir hvernig VSK-númer lánardrottins er flutt út í Intrastat skrána. Þú getur valið einn af eftirfarandi valkostum: VSK-númer með því að bæta við ESB-landskóða sem forskeyti og fjarlægja ESB-landskóða úr VSK-númeri. |
   | **Skráð VSK-númer viðskiptamanns** | Tilgreinir hvernig VSK-númer viðskiptavinar er flutt út í Intrastat skrána. Þú getur valið einn af eftirfarandi valkostum: VSK-númer með því að bæta við ESB-landskóða sem forskeyti og fjarlægja ESB-landskóða úr VSK-númeri. |
   | **Fá VSK samstarfsaðila** | Tilgreinir frá hvaða tegund **Intrastat-skýrslulínu** VSK-númer samstarfsaðila er uppfært. Þú getur valið aðeins fyrir kvittun, aðeins fyrir sendingu eða báðar tegundir línu, allt eftir kröfum á hverjum stað fyrir sig. |
3. Opnaðu flýtiflipann **Sjálfgefnar færslur** og fylltu út reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Taflan hér að neðan lýsir nokkrum lykilreitum:

   | Svæði | Lýsing |
   | --- | --- |
   | **Sjálfgefin færslugerð** | Tilgreinir sjálfgefna færslugerð fyrir reglulegar söluafhendingar, þjónustuafhendingar og innkaupakvittanir. |
   | **Sjálfgefin færslugerð - Skil** | Tilgreinir sjálfgefna færslugerð fyrir söluvöruskil, þjónustuskil og innkaupaskil. |
   | **Sjálfgefið VSK-nr. einstaklings** | Tilgreinir sjálfgefið VSK-númer einstaklings, ef viðkomandi einstaklingur verður að vera með sérstakt VSK-númer í Intrastat-skýrslunni. |
   | **Sjálfgefið VSK-nr. þriðja aðila** | Tilgreinir sjálfgefið VSK-númer þriðja aðila ef þú hefur ekki VSK-númer viðkomandi. |
   | **Sjálfvalinn VSK fyrir óþekkt ríki** | Tilgreinir sjálfgefið VSK-númer fyrir óþekkt ríki. |
   | **Sjálfgefinn lands-/svæðiskóði** | Tilgreinir sjálfgefinn kóða móttökulands. |
4. Opnaðu flýtiflipann **Skýrslugerð** og fyllið út reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Taflan hér að neðan lýsir nokkrum lykilreitum:

   | Svæði | Lýsing |
   | --- | --- |
   | **Skilgreiningarkóði gagnaskipta** | Tilgreinir skilgreiningarkóða gagnaskipta til að búa til Instrastat-skrá. Það virkar aðeins ef reiturinn **Skipta skrám innhreyfinga/afhendinga** er stilltur á **Nei**. |
   | **Skipta skrám innhreyfinga/afhendinga** | Tilgreinir hvort tilkynna skuli um innhreyfingar og afhendingar í tveimur aðskildum skrám. |
   | **Zip-skrá(-r)** | Tilgreinir hvort bæta eigi skýrsluskrá(m) við .zip-skrá. |
   | **Skilgreiningarkóði gagnaskipta - Innhreyfing** | Tilgreinir skilgreiningarkóða gagnaskipta til að búa til Instrastat-skrá fyrir mótteknar vörur. Þetta virkar einungis ef reiturinn **Skipta skrám innhreyfinga/afhendinga** á **Já**. |
   | **Skilgreiningarkóði gagnaskipta - Afhending** | Tilgreinir skilgreiningarkóða gagnaskipta til að búa til Instrastat-skrá fyrir sendar vörur. Þetta virkar einungis ef reiturinn **Skipta skrám innhreyfinga/afhendinga** á **Já**. |
5. Opnaðu flýtiflipann **Tölusetning** til að setja upp **Intrastat-númer**.

### <a name="set-up-a-reporting-file"></a>Setja upp skýrsluskrá

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið og færsa inn **Skilgreiningar gagnaskipta** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
3. Á flýtiflipanum **Almennt** skal lýsa skilgreiningu á gagnaskiptum, gerð gagnaskrár, skiltákni, tengdum kóðaeiningum, XMLport, og öðrum reitum með því að fylla út reitina.
4. Á flýtiflipanum **Línuskilgreiningar** skal lýsa sniði lína í gagnaskránni með því að fylla út reitina sem byggðir eru reitnum **Línugerð** og þar þarf að skilgreina fjölda dálka fyrir þessa línu.
5. Á flýtiflipanum **Dálkskilgreiningar** er fyllt út í línuna fyrir hvern fyrirhugaðan dálk. Þú getur skilgreint heiti dálka, gagnagerðir (*Texti*, *Dagsetning*, eða *Tugabrot*), lengd línu af fastri breidd sem inniheldur dálkinn ef skráin er af gerðinni Fastur texti og nokkrar færibreytur til viðbótar.
6. Veldu aðgerðina **Reitavörpun** á flýtiflipanum **Línuskilgreiningar** til að opna síðuna **Reitavörpun**.
7. Búa til nýju færsluna og á flýtiflipanum **Almennt** velurðu rétt **Töflukenni** (fyrir **Línu Intrastat-skýrslu**, veldu 4812) og fyllir síðan út í fleiri reiti:
   1. Tilgreina lykilvísi til að raða upprunafærslum fyrir útflutning í reitnum **Lykilvísir**.
   2. Veljið viðeigandi **Vörpunarkóðaeiningu**.
8. Á flýtiflipanum **Reitavörpum** bætið þið við dálkum sem þið höfðuð áður stillt á flýtiflipanum **Dálkskilgreiningar** og bætið svo eftirfarandi við:
   1. Tilgreinið **Auðkenni reitar** fyrir hvern dálk.
   2. Tilgreindu **Umbreytingarreglu** dálk sem þú þarft á að halda. Tilgreinir reglu sem umbreytir innfluttum texta í stutt gildi áður en hægt er varpa því á tiltekinn reiti í [!INCLUDE[prod_short](includes/prod_short.md)]. Þegar gildi er valið í þessum reit er nákvæmar gildi slegið inn í reitinn **Umbreytingarregla** í töflunni **Biðminni vörpunar gagnaskiptareits** og öfugt.
9. Ef þú þarft að flokka færslur út frá einhverjum dálkum, á flýtiflipanum **Flokkun reits**, veldu reitina sem þú vilt nota fyrir hópun.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] kemur með forstilltri skilgreiningu gagnaskipta fyrir Intrastat fyrir öll staðbundin lönd. Frekari upplýsingar um hvernig á að búa til nýja skilgreiningu gagnaskipta er að finna í greininni [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).

### <a name="set-mandatory-fields-with-the-intrastat-report-checklist"></a>Stilltu áskilda reiti með gátlistanum fyrir Intrastat-skýrsluna

Í sumum löndum krefjast yfirvöld að Intrastat-skýrslur innihaldi til dæmis sendingaraðferðina fyrir kaup eða nokkur önnur gildi þegar salan er yfir ákveðnum mörkum.

Gerðu eftirfarandi til að stilla áskilda reiti og/eða gildi á **Intrasat-skýrslusíðunni**:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, opna **Uppsetningu Intrastat-skýrsla** og velja síðan viðkomandi tengil.
2. Veldu aðgerðina **Gátlisti fyrir Intrastat-skýrslu**.
3. Bættu við áskildum línum til að athuga með því að nota eftirfarandi leiðbeiningar:
   1. Stilltu **Reit nr.** á reit sem þarf að athuga fyrir gildi sem ekki er tómt.
   2. Fylltu út reitinn **Segðargerð síu** ef þörf krefur, í samræmi við eftirfarandi reglur:
      1. Þegar **Síusíðan** er opnuð skaltu velja **Síuna** þú þarft að nota við athugunina.
      2. Veldu gildi sem tengist **Síunni** sem þú notaðir næsta skrefi.
      3. Ef þú ert með fleiri síur sem þú þarft að fylla í fyrir þennan tiltekna reit getur þú bætt annarri síu við með því að fylgja sömu skrefum.
      4. Þegar þú klárar að slá inn síurnar fyrir valda reitinn, veldu **Í lagi**.
   3. Veldu reitinn **Öfug segð afmörkunar** til að tilgreina að athugun á reitum sé aðeins keyrð á þær línur sem samsvara ekki segðargerð síu. Ef línan er ekki síuð er þessi reitur hunsaður.

> [!NOTE]
> Þegar **Síusíðan** er opnuð úr **Síusegðarínunni** er hægt að nota allar staðlaðar síusegðir í tengslum við tiltekinn reit sem á að sía.
>
> Farðu varlega í að setja upp villuleitarreglur þar sem þær geta verið mismunandi eftir löndum.

## <a name="use-custom-codeunits-in-intrastat-reporting"></a>Nota sérstillta kóðaeiningar í Intrastat-skýrslum

Ef þú vilt breyta því hvernig Intrastat virkar og sjálfgefnar stillingar duga ekki getur þú sérsniðið kerfið með því að bæta við stöðluðu eiginleikana. Ef þörf er á að breyta hegðun Intrastat frekar er hægt að þróa eigin kóðaeiningar. Þegar þú býrð til kóðaeiningar þarftu hins vegar að gera fleiri breytingar til að nota þær. Til að skilgreina kerfið til að nota eigin hluti:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skilgreining VSK-skýrslna** og velja síðan viðkomandi tengil.
2. Á síðunni **Skilgreining VSK-skýrslna** er nýrri línu bætt við.
3. Í reitnum **Gerð VSK-skýrslu** skal velja valkostinn **Intrastat-skýrsla**.
4. Í reitnum **Útgáfa VSK-skýrslu** skal tilgreina útgáfu skýrslunnar.
5. Eftir það er hægt að bæta við kóðaeiningum þínum fyrir eftirfarandi valkosti: a. Á reitnum **Kenni kóðaeiningar tillögulína**, tilgreindu nýju kóðaeininguna til að stinga upp á línum í Intrastat-skýrslulínunum.
   b. Í reitnum **Kenni kóðaeiningar efnis** skaltu tilgreina nýju kóðaeininguna til að flytja gögn út sem skrá með því að nota skilgreiningu gagnaskipta.
   c. Í reitnum **Staðfesta kenni kóðaeiningar** tilgreindu nýju kóðaeiningarnar til að staðfesta niðurstöður í Intrastat-skýrslulínunum.

> [!IMPORTANT]
>
> Þessi lína verður að vera auð ef notaðar eru hefðbundnar kóðaeiningar. Þú ættir aðeins að búa til línu og stilla hana ef þú hefur búið til sérsniðnar kóðaeiningar.

## <a name="other-intrastat-configurations"></a>Aðrar Intrastat stillingar

> [!IMPORTANT]
> Á viðskiptavina- og lánardrottnaspjöldum er reitur, **Gerð Intrastat-viðskiptafélaga**, sem hefur sömu valkosti og reiturinn **Gerð viðskiptafélaga**: „“ (tómt), *Fyrirtæki* og *Einstaklingur*. Reiturinn **Gerð Intrastat-viðskiptafélaga** hefur komið í stað reitsins **Gerð viðskiptafélaga** í Intrastat-skýrslugerð. Reiturinn **Gerð viðskiptafélaga** er notaður á sameiginlega evrópska greiðslusvæðinu (SEPA) til að skilgreina SEPA beingreiðslukerfið (CORE eða B2B). Reiturinn **Gerð Intrastat-viðskiptafélaga** er aðeins notaður fyrir Intrastat-skýrslugerð. Þannig er hægt að tilgreina mismunandi gildi fyrir reitina tvo ef þörf krefur.
>
> Ef reiturinn **Gerð Intrastat-viðskiptafélaga** er hafður auður er gildið úr reitnum **Gerð viðskiptafélaga** notað við Intrastat-skýrslugerð.

Fyrir utan **Uppsetning Intrastat-skýrslu**, **Skilgreiningar gagnaskipta** og **Gátlisti Intrastat-skýrslu** þarftu einnig að stilla aðrar stillingar:

| Síða | Lýsing |
| ---- | ----------- |
| **Lönd/svæði** | Áður en byrjað er að nota Intrastat-skýrslur þarf einnig að setja upp síðu **landa/svæða**. Á þessari síðu verður þú að bæta við kóða **Lands-/svæðakóti í ESB** og **Intrastat-kóða** til að tilgreina kóða fyrir landið/svæðið sem stunduð eru viðskipti, þar sem hann verður notaður við Intrastat-skýrslugerð. |
| **Tollflokkar** | Í mörgum löndum hafa tolla- og skattayfirvöld komið á 8 stafa kóða vegna ýmiss konar vörur. Ef birgðafærslur eiga að fela í sér áskildar upplýsingar þegar kerfið flytur þær í Intrastat-bókarlínu verður fyrst að færa inn vörukóði á síðunni **Tollflokkar**. Finna skal kóða þeirra vörutegunda sem fyrirtæki notanda verslar með og færa þá inn á síðunni **Tollflokkar**. |
| **Flutningsmátar** | Það eru sjö einstölu kóðar fyrir Intrastat flutningsmáta. **1** fyrir sjóleið, **2** fyrir lest, **3** fyrir akstur, **4** fyrir flug, **5** fyrir póstsendingar, **7** fyrir fastar uppsetningar, og **9** fyrir eigin knúningsafl (t.d., flytja bíl með því að aka honum). [!INCLUDE[prod_short](includes/prod_short.md)] fer ekki fram á þessa tilgreindu kóða, en við mælum engu að síður með því að lýsingarnar beri með sér svipaða merkingu. |
| **Tegundir viðskipta** | Lönd og svæði hafa ólíka kóða fyrir tegundir Instrastat viðskipti, eins og venjuleg innkaup og sala, skipti á skilavörum, og skipti á vörum sem ekki hefur verið skilað. Setja upp alla kóða sem eiga við í þínu landi/svæði. Þessir kóðar eru síðan notaðir á flýtiflipanum **Erlend viðskipti** á sölu- og innkaupaskjölum og þegar unnið er úr skilum. |
| **Lýsingar viðskipta** | Setja upp kóða til viðbótar við lýsingar á tegundum viðskipta. |
  > [!NOTE]
  > Intrastat gerir frá og með janúar 2022 kröfu um mismunandi eðliskóða viðskipta fyrir sendingar til einstaklinga sem eru ekki skráðir VSK-skyldir eða fyrirtækja sem eru skráð VSK-skyld. Við mælum með því að yfirfara og/eða bæta við nýjum eðliskóðum viðskipta á síðunni **Tegundir viðskipta** í samræmi við kröfurnar í þínu landi. Þú ættir einnig að athuga og uppfæra reitinn **Gerð Intrastat-viðskiptafélaga** í *Einstakling* fyrir einstaklinga sem eru ekki skráðir VSK-skyldir eða fyrirtæki sem eru skráð VSK-skyld á viðkomandi síðu **Viðskiptavinar**. Ef þú ert ekki viss um rétta tegund Intrastat-viðskiptafélaga eða tegund viðskipta sem á að nota mælum við með því að þú spyrjir sérfræðing í þínu landi eða svæði.

| **Reitur** | **Lýsing** |
| --------- | --------------- |
| **Nettóþyngd** | Þyngd er ein af grunnstillingum sem tengjast Intrastat-skýrslugerð þar sem **Heildarþyngdin** er áskilin við skýrslugerð. Til að vera tilbúinn fyrir þessa kröfu verður einnig að fylla út í reitinn **Nettóþyngd** á birgðar- eða eignarspjaldinu. |
| **Kóði upprunalands** | Notaðu tveggja bókstafa ISO-alfakóða birgðar- eða eignaspjaldinu fyrir landið þar sem varan var fengin eða framleidd. Ef varan var framleidd í fleiri en einu landi er upprunalandið síðasta landið þar sem töluvert var unnið með hana. |
| **VSK-númer samstarfsaðila í aðildarríkinu þar sem innflutningur fer fram** | Þetta er VSK-númer samstarfsaðila í aðildarríkinu þar sem innflutningur fer fram. VSK-númerið er einnig notað til að skiptast á upplýsingum um útflutning milli aðildarríkja ESB og gerir aðildarríkjunum kleift að úthluta mótteknum gögnum til innflutningsfyrirtækisins í eigin landi. Tilkynningarskyldar vörur verða að tilgreina VSK-númer fyrirtækis sem taldi fram til tolls vegna vörukaupa í aðildarríkinu þar sem innflutningur fer fram. |

Einnig er hægt að setja upp:

* **Vörukóði**: Tolla- og skattyfirvöld hafa sett fram númerakóða sem flokka vörur og þjónustu. Þú tiltekur þessa kóða á vörum.
* **Svæði**: Viðbótarupplýsingar um lönd og svæði.
* **Komu/brottfarastaðir**: Tilgreina staðsetningar þar sem vöruafhending og móttaka fara fram í viðskiptum við önnur lönd. Flugstöðin er dæmi um komu-brottfararstað. Komu/brottfararstaði er hægt að færa inn í sölu- og innkaupskjöl á flýtiflipanum **Erlend viðskipti**. Þessar upplýsingar verða einnig afritaðar úr birgðafærslum þegar Intrastatbók er stofnuð.
* **Viðbótarmælieining**: Magn vara til Intrastat-skýrslugerðar getur verið annað hvort nettóþyngd (í kílógrömmum) eða viðbótareining. Ef þörf er á viðbótareiningum verður að stilla þær fyrir vörur og eignir.

#### <a name="set-up-transport-methods"></a>Settu upp flutningsmáta

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Flutningsmátar** og velja síðan viðkomandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="set-up-transaction-nature-codes"></a>Uppsetning eðliskóða viðskipta

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu **Tegundir viðskipta** og veldu síðan viðkomandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="other-related-configurations"></a>Aðrar tengdar stillingar

Áður en þú notar eiginleika Intrastat-skýrslugerðar þarftu að stilla nokkra reiti á birgða-, eignar-, viðskiptavina- og lánardrottnaspjaldi.

#### <a name="item-cards"></a>Birgðaspjöld

Gerðu eftirfarandi til að setja upp allar áskildar upplýsingar er tengjast Intrastat á birgðarpjöldum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur**, velja síðan viðkomandi tengil.
2. Veldu vöru til að stilla.
3. Stækkaðu flýtiflipann **Kostnaður og bókanir** og fylltu út reitina **Tollflokkskóði**, **Viðbótarmælieining** og **Kóði upprunalands/-svæðis**.
4. Stækkaðu flýtiflipann **Birgðir** og sláðu inn tölugildið í reitinn **Nettóþyngd**.

> [!NOTE]
> Þú getur notað mismunandi mælieiningar sem viðbótarmælieiningar. Ef hún er ekki sú sama og **Grunnmælieiningin** þarftu að stilla þessa mælieiningu á síðunni **Mælieiningar**.

#### <a name="fixed-asset-cards"></a>Eignaspjöld

Gerðu eftirfarandi til að setja upp allar áskildar upplýsingar er tengjast Intrastat á eignaspjöldum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignir** og velja síðan viðkomandi tengil.
2. Veldu eignina sem á að stilla.
3. Stækkaðu flýtiflipann **Intrastat** og fylltu út reitina **Tollflokkskóði**, **Nettóþyngd** og **Viðbótarmælieining**.

> [!NOTE]
> Þú getur notað mismunandi mælieiningar sem viðbótarmælieiningar. Óháð því hvaða **Mælieiningarkóða** sem þú velur, verður **Magn** hans í Intrastat-skýrslum alltaf 1.

#### <a name="vendor-cards"></a>Lánardrottnaspjöld

Áður en þú notar lánardrottinn í Intrastat-skýrslugerð verður þú að vera með sérstakan **Lands-/svæðiskóða** og **VSK-númer** auk frekari upplýsinga á síðunni **Lánardrottnaspjald**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lánardrottnar** og síðan velja viðkomandi tengil.
2. Velja skal lánardrottinn sem á að stilla.
3. Á flýtiflipanum **Intrastat** er hægt að stilla sjálfgefin gildi í reitunum **Sjálfgefna tegund viðskipta**, **Tegund viðskipta - Skil** og **Sjálfgefinn flutningsmáti**.
4. Stækkaðu flýtiflipann **Greiðslur** og veldu valkostinn í reitnum **Gerð Intrastat-viðskiptafélaga** til að tilgreina hvort lánardrottinn er einstaklingur eða fyrirtæki í Intrastat-skýrslugerð.

#### <a name="customer-cards"></a>Kort viðskiptavina

Áður en viðskiptavinur er notaður í Intrastat-skýrslugerð verður hann að vera með sérstakan **Lands-/svæðiskóða** og **VSK-númer** fyrir hvern og einn til viðbótar við frekari upplýsingar á síðunni fyrir **Kort viðskiptavina**:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinir** og velja síðan viðkomandi tengil.
2. Veldu viðskiptavin til að stilla.
3. Á flýtiflipanum **Intrastat** er hægt að stilla sjálfgefin gildi í reitunum **Sjálfgefna tegund viðskipta**, **Tegund viðskipta - Skil** og **Sjálfgefinn flutningsmáti**.
4. Stækkaðu flýtiflipann **Greiðslur** og veldu valkostinn í reitnum **Gerð Intrastat-viðskiptafélaga** til að tilgreina hvort lánardrottinn er einstaklingur eða fyrirtæki í Intrastat-skýrslugerð.

#### <a name="exclude-items-and-fixed-assets-from-intrastat-reporting"></a>Útiloka vörur og eignir frá Intrastat-skýrslugerð

Ef ástæða er til að útiloka tiltekna vöru eða eign frá Intrastat-skýrslugerð þarftu að breyta valkosti á korti viðkomandi.

##### <a name="exclude-an-item-from-intrastat-reporting"></a>Útiloka vöru frá Intrastat-skýrslugerð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur**, velja síðan viðkomandi tengil.
2. Veldu vöru til að stilla.
3. Stækkaðu flýtiflipann **Kostnaður og bókanir** og veldu svo reitinn **Útiloka frá Intrastat-skýrslu**.

##### <a name="exclude-a-fixed-asset-from-intrastat-reporting"></a>Útiloka eign frá Intrastat-skýrslugerð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignir** og velja síðan viðkomandi tengil.
2. Veldu eignina sem á að stilla.
3. Stækkaðu flýtiflipann **Intrastat** og veldu svo reitinn **Útiloka frá Intrastat-skýrslu**.

## <a name="country-specific-intrastat-setup"></a>Intrastat-uppsetning háð landi

<!-- PM's note: Currently, we will add only the 'Overview' topic; the topic 'Manage Intrastat Country Specifics' and country details will wait until 21.1 when I update with all country-based details -->

Krafa Intrastat er svipuð í öllum aðildarríkjum ESB, en á því eru mikilvægar undantekningar. Fræðilega ættu reglurnar gilda á sama hátt í öllum aðildarríkjum. Hins vegar er munur á innleiðingu vegna þess að sum aðildarríki gefa leiðbeiningar um hvernig beita skuli almennum reglum í reglugerðinni við tilteknar aðstæður (t.d. sýnishornum af vörum, vöruskil o.s.frv.). Þessar leiðbeiningar kunna að skila mismunandi niðurstöður við ýmsar aðstæður í aðildarríkjum ESB. Þess vegna eru sum lönd með einhverjar sérstakar viðbótarupplýsingar aðgreindar frá öðrum löndum og þau eru einnig með annað skráarsnið fyrir skýrslugerð.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a>Sjá einnig .

[Intrastat-skýrslugerð í Business Central](finance-how-report-intrastat.md)  
[Fjármálastjórnun](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
