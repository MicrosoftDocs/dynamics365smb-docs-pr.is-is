---
title: Uppsetning Intrastat-skýrslugerðar
description: Þessi grein útskýrir hvernig setja á upp Intrastat-skýrslugerðaraðgerðir til að tilkynna viðskipti við fyrirtæki í öðrum ESB-löndum/svæðum.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 05/29/2024
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
---
# Uppsetning Intrastat-skýrslugerðar

Öll fyrirtæki í löndum innan Evrópusambandsins (ESB) þurfa að gefa öðrum löndum/svæðum innan sambandsins skýrslur um viðskipti sín. Einnig þarf að gefa hagstofu viðkomandi lands/svæðis mánaðarlega skýrslu um hreyfingu vöru og skýrsluna þarf að afhenda skattayfirvöldum. Intrastat er kerfið sem er notað til að safna saman viðskiptatölfræði um vörur í þessum löndum/svæðum. Nota Intrastat-skýrsluna til að ljúka reglubundnum Intrastat-skýrslum með því að safna, skrá og tilkynna viðskipti með vörur samkvæmt staðbundnum lögum.

Intrastat-skýrslugerð er byggð á grunnreglum ESB sem eiga við um öll lönd/svæði. Munur er þó á milli einstakra landa/svæða. Hvert land/svæði hefur sínar reglur um hvað og hvernig eigi að gefa skýrslu.

> [!NOTE]
> Intrastat-upplýsingar eiga ekki við um hreyfingu þjónustu milli landa/svæða. Þess í stað eiga upplýsingarnar aðeins við um vörur eins og vörur og eignir. Ef ríkisstjórnin krefst þess að þú skráir hreyfingu þjónustu milli landa/svæða skal nota aðgerðina **Þjónustuyfirlýsing** .
>
> Þessi eiginleiki er tiltækur sem forrit sem hægt er að sækja úr [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). Til að nota þessa aðgerð skal setja hana upp á síðunni **Viðbótastjórnun** .

> [!IMPORTANT]
> Þessi grein fjallar um nýju Intrastat-upplifunina sem er í boði úr [!INCLUDE[prod_short](includes/prod_short.md)] 21. útgáfu. Leita skal ráða hjá kerfisstjóranum til að komast að því hvaða útgáfa fyrirtækið er að nota og hvort virkja skuli nýju aðgerðina.
>
> Lesa Intrastat-uppsetningu og notkunargrein fyrri útgáfu, [Setja upp og skýrslu Intrastat](finance-how-setup-report-intrastat-v20.md).

## Gera nýju Intrastat upplifunina virka

Í 2022 útgáfubylgju 2 [!INCLUDE[prod_short](includes/prod_short.md)]  felur í sér endurhannaða Intrastat-upplifun sem býður upp á aukna eiginleika. Ef nýja Intrastat-aðgerðin er ekki virk í umhverfi notanda getur stjórnandi gert hana virka á síðunni **Aðgerðastjórnun** .

> [!IMPORTANT]
> Ekki er hægt að nota gömlu og nýju upplifunina samhliða. Áður en viðbótin er ræst í framleiðsluumhverfi er mælt með því að hann sé prófaður í sandkassaumhverfi með því að nota afrit af framleiðslugögnunum. Þegar ný notandaupplifun hefur verið gerð virk í framleiðsluumhverfinu er ekki hægt að snúa aftur í gömlu Intrastat-aðgerðirnar.

1. Velja skal táknið :::image type="icon" source="media/ui-search/search_small.png" border="false"::: , slá inn **Eiginleikastjórnun** og velja síðan viðeigandi tengil.
2. Á síðunni **Aðgerðastjórnun** skal velja línuna fyrir **aðgerðauppfærslu: Skipta út fyrirliggjandi Intrastat-aðgerðum fyrir nýja Intrastat-viðbótina**. Nánari upplýsingar um eiginleikastjórnun [eru í Gera væntanlega eiginleika virka fram í tímann](/dynamics365/business-central/dev-itpro/administration/feature-management).
3. Í dálknum **Gera virkt fyrir** skal velja **Allir notendur**.
4. Lesa skal skýringuna á því hvernig kerfið verður uppfært og Síðan er Já **valið** til að samþykkja.
5. Veldu **Áfram**. Grunnuppsetningin fyrir Intrastat fæst. Nánari upplýsingar um uppsetningu Intrastat eru í hlutanum Intrastat-skilgreiningarhluti [síðar](#intrastat-configuration) í þessari grein.
6. Þegar uppsetningunni er lokið skal velja **Ljúka** til að byrja að nota nýja Intrastat-upplifunina.

    > [!NOTE]
    > Það fer eftir staðsetningu fyrirtækisins hvort nægilegt er að gera eiginleikann sem var lýst virkan. Í löndum/svæðum sem hafa sérstakar aðgerðir við Intrastat-skýrslugerð skal gera forritinu/svæðis-/svæðis intrastat kleift til viðbótar við kjarnaviðbótina.

## Uppsetning Intrastat

Áður en hægt er að nota Intrastat skýrslur þarf að setja upp nokkrar stillingar.

### Uppsetning Intrastat-skýrslugerðar

Nota skal síðuna **Uppsetning** Intrastat-skýrslu til að virkja og stilla sjálfgefna hegðun fyrir Intrastat-skýrslugerð. Hægt er að tilgreina hvort gera þurfi Intrastat skýrslu um afhendingu (afgreiðslur), móttökur (komur) eða hvort tveggja, eftir þröskuldum sem reglugerðir viðkomandi lands kveða á um. Einnig er hægt að stilla sjálfgefnar tegundir viðskipta fyrir venjuleg og skilaskjöl sem notuð eru við færsluskýrslugerð.

Fylgja skal eftirfarandi skrefum til að setja upp Intrastat-skýrslugerð.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Uppsetning** Intrastat-skýrslu og velja síðan viðeigandi tengil.
2. Á flýtiflipanum **Almennt** skal velja eða færa inn reitaupplýsingar eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Eftirfarandi tafla lýsir sumum lykilreitunum.

   | Svæði | Heimildasamstæða |
   | --- | --- |
   | **Skrá kvittanir** | Tilgreinir að taka verði með mótteknar vörur sem berast í Intrastat-skýrslum. |
   | **Skrá afhendingar** | Tilgreinir að taka verði með afgreiddar vörur sem eru sendar í Intrastat-skýrslum. |
   | **Taka beina afhendingu með** | Tilgreinir hvort færslur beinnar sendingar séu innifaldar í Intrastat-skýrslum. Nánari upplýsingar eru í [Vinna með Intrastat-skýrslugerð](finance-how-report-intrastat.md).  |  
   | **Sendingar byggðar á**  | Tilgreinir landskótann sem er byggður á því hvaða Intrastat-skýrslulínur eru teknar.  |
   | **VSK-nr. byggt á** | Tilgreinir kóta viðskiptamanns eða lánardrottins sem virðisaukaskattur (VSK) er tekinn fyrir Intrastat-skýrsluna.  |
   | **Skráð VSK-númer fyrirtækis** | Tilgreinir hvernig VSK-númer fyrirtækisins er flutt út í Intrastat-skrána.  |
   | **Skráð VSK-númer lánardrottins** | Tilgreinir hvernig VSK-númer lánardrottins er flutt út í Intrastat skrána.  |
   | **Skráð VSK-númer viðskiptamanns** | Tilgreinir hvernig VSK-númer viðskiptavinar er flutt út í Intrastat skrána.  |
   | **Fá VSK samstarfsaðila** | Tilgreinir hvaða tegund Intrastat-skýrslulína VSK-númer félagans er uppfærð úr. Samkvæmt staðbundnum þörfum er aðeins hægt að velja móttökulínur, afhendingarlínur eða báðar tegundir lína. |

4. Á flýtiflipanum **Sjálfgefnar færslur** skal velja eða færa inn upplýsingar um reit eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Eftirfarandi tafla lýsir sumum lykilreitunum.

   | Svæði | Heimildasamstæða |
   | --- | --- |
   | **Sjálfgefin færslugerð** | Tilgreinir sjálfgefna færslugerð fyrir reglulegar söluafhendingar, þjónustuafhendingar og innkaupakvittanir. |
   | **Sjálfgefin færslugerð - Skil** | Tilgreinir sjálfgefna færslugerð fyrir söluvöruskil, þjónustuskil og innkaupaskil. |
   | **Sjálfgefið VSK-nr. einstaklings** | Tilgreinir sjálfgefið VSK-númer einkaaðila ef einkaaðili verður að hafa sérstakt VSK-númer í Intrastat-skýrslunni. |
   | **Sjálfgefið VSK-nr. þriðja aðila** | Tilgreinir sjálfgefið VSK-númer þriggja aðila ef VSK-númer er ekki fyrir hendi. |
   | **Sjálfvalinn VSK fyrir óþekkt ríki** | Tilgreinir sjálfgefið VSK-númer fyrir óþekkt ríki. |
   | **Sjálfgefinn lands-/svæðiskóði** | Tilgreinir sjálfgefinn kóða móttökulands. |

5. Á flýtiflipanum **Skýrslur** skal velja eða færa inn upplýsingar um reitinn eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Eftirfarandi tafla lýsir sumum lykilreitunum.

   | Svæði | Heimildasamstæða |
   | --- | --- |
   | **Skilgreiningarkóði gagnaskipta** | Tilgreinir skilgreiningarkóða gagnaskipta til að búa til Instrastat-skrá. Þessi reitur er aðeins tiltækur ef reiturinn **Skipta móttöku-/afhendingarskrám** er stilltur á **Nr**. |
   | **Skipta skrám innhreyfinga/afhendinga** | Tilgreinir hvort tilkynna skuli móttökur og sendingar í tveimur aðskildum skrám. |
   | **Zip-skrá(-r)** | Tilgreinir hvort bæta skuli skýrsluskránum við zip-skrána. |
   | **Skilgreiningarkóði gagnaskipta - Innhreyfing** | Tilgreinir skilgreiningarkóða gagnaskipta til að búa til Instrastat-skrá fyrir mótteknar vörur. Þessi reitur er aðeins tiltækur ef reiturinn **Skipta móttöku-/afhendingarskrám** er stilltur á **Já**. |
   | **Skilgreiningarkóði gagnaskipta - Afhending** | Tilgreinir skilgreiningarkóða gagnaskipta til að búa til Instrastat-skrá fyrir sendar vörur. Þessi reitur er aðeins tiltækur ef reiturinn **Skipta móttöku-/afhendingarskrám** er stilltur á **Já**. |

6. Á flýtiflipanum **Númeraröð** er fært inn gildi í reitinn **Intrastatnr.röð** .

### Setja upp skýrsluskrá

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **skilgreiningar** gagnaskipta og velja síðan viðeigandi tengil.
2. Valið er **Nýr** og á flýtiflipanum **Almennt** eru færðar inn upplýsingar um skilgreiningu gagnaskipta, tegund gagnaskrár, dálkskiltákn, tengd codeunit XMLport og aðra reiti eftir þörfum.
3. Á flýtiflipanum **Línuskilgreiningar** er fært inn gildi í reitinn **Línugerð** til að lýsa sniði lína í gagnaskránni og hvar þarf að skilgreina fjölda dálka fyrir þessa línu.
4. Á flýtiflipanum **Dálkskilgreiningar** er fyllt út í línuna fyrir hvern fyrirhugaðan dálk. Hægt er að skilgreina dálkheiti, gagnategundir (svo sem texta, dagsetningu eða aukastaf), lengd línunnar sem er með dálknum ef skráin er af gerðinni *Fastur texti* og aðrar færibreytur.
5. Á flýtiflipanum **Línuskilgreiningar** er Reitavörpun **valin**.
6. Á síðunni **Reitavörpun** skal stofna nýja færslu. 
7. Á flýtiflipanum **Almennt** skal velja **kenni töflu** (fyrir **Intrastat-skýrslulínu**, velja **4812**) og færa inn eftirfarandi upplýsingar:

   1. Í reitnum **Lykilvísir** er tilgreindur lykill til að raða upprunafærslum fyrir útflutning.
   2. Í reitnum **Vörpunarkótiunit** er valið gildi.

8. Á flýtiflipanum **Reitavörpun** skal bæta við dálkunum sem áður voru grunnstilltir á flýtiflipanum **Dálkskilgreiningar** og bæta síðan við eftirfarandi reitaupplýsingum:

   1. Tilgreina gildi reitakennis **fyrir** hvern dálk.
   2.  **Tilgreina gildi umbreytingarreglu** fyrir hvern dálk eftir þörfum. Gildið tilgreinir regluna sem umbreytir innleiddum texta í studd gildi áður en hægt er að varpa henni í tiltekinn reit í [!INCLUDE[prod_short](includes/prod_short.md)]. Þegar gildi er valið í þessum reit er nákvæmar gildi slegið inn í reitinn **Umbreytingarregla** í töflunni **Biðminni vörpunar gagnaskiptareits** borð. (Á móti þegar nákvæmt gildi er fært inn í **Reiturinn Umbreytingarregla** í **vörpun gagnareita vörpunar buf.** Er gildi valið í þessum reit.)

9. Ef flokka þarf færslur sem byggðar eru á sumum dálkum skal velja reitina sem nota á til að flokka á flýtiflipanum **Reitaflokkun** .

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] Fylgir fyrirframskilgreindri skilgreiningu gagnaskipta fyrir Intrastat fyrir öll staðfærð lönd/svæði. Nánari upplýsingar um hvernig á að stofna nýja skilgreiningu gagnaskipta eru [í Setja upp skilgreiningar á gagnaskiptum](across-how-to-set-up-data-exchange-definitions.md).

### Stilltu áskilda reiti með gátlistanum fyrir Intrastat-skýrsluna

Í sumum löndum/svæðum krefjast yfirvöld þess að Intrastat-skýrslur innihaldi t.d. afhendingarmáta fyrir innkaup eða önnur gildi þegar sala er yfir ákveðnum þröskuldi.

Til að setja áskilda reiti eða gildi á síðunni **Intrastat-skýrsla** skal fylgja þessum skrefum.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Uppsetning** Intrastat-skýrslu og velja síðan viðeigandi tengil.
2. Gátlisti **Intrastat-skýrslu er valinn**.
3. Eftirfarandi skrefum er fylgt til að bæta við nauðsynlegum línum til athugunar:
   1. Stilltu **Reit nr.** á reit sem þarf að athuga fyrir gildi sem ekki er tómt.
   2. Fært er inn gildi í reitinn **Afmörkunarsegð** ef þörf krefur, byggt á eftirfarandi reglum:

        1. Þegar afmörkunarsíðan **er opnuð** skal velja afmörkunina sem á að nota til að athuga.
        2. Velja skal gildi sem tengist valinni afmörkun.
        3. Ef fylla þarf út fleiri afmarkanir fyrir valinn reit skal endurtaka síðustu tvö þrepin til að bæta við annarri afmörkun.
        4. Þegar lokið er við að færa inn afmarkanir fyrir reitinn sem var valinn er Í lagi **valið**.

   3.  **Velja skal gátreitinn Bakfærð afmörkunarsegð** til að tilgreina að tékki fyrir reiti sé aðeins keyrður í þeim línum sem samsvara ekki afmörkunarsegðinni. Ef línan er ekki afmörkuð hunsar reiturinn.

> [!NOTE]
> Þegar **Síusíðan** er opnuð úr **Síusegðarínunni** er hægt að nota allar staðlaðar síusegðir í tengslum við tiltekinn reit sem á að sía.
>
> Farið er varlega þegar villuleitarreglur eru settar upp þar sem þær geta verið mismunandi milli landa/svæða.

## Nota sérstillta kóðaeiningar í Intrastat-skýrslum

Ef breyta á því hvernig Intrastat virkar og sjálfgefna grunnstillingin nægir ekki er hægt að sérstilla kerfið með því að framlengja staðlaða eiginleika. Ef þörf er á að breyta hegðun Intrastat frekar er hægt að þróa eigin kóðaeiningar. Þegar codeunit eru stofnuð þarf að gera viðbótarbreytingar til að nota þau. Til að grunnstilla kerfið til að nota eigin hluti skal fylgja þessum skrefum.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **skilgreiningu** VSK-skýrslna og velja síðan viðeigandi tengil.
2. Á síðunni **Skilgreining VSK-skýrslna** er nýrri línu bætt við.
3. Í reitnum **Tegund** VSK-skýrslu er Intrastat-skýrsla **valin**.
4. Í reitnum **Útgáfa VSK-skýrslu er tilgreind útgáfa** skýrslunnar.
5. Codeunit er bætt við fyrir eftirfarandi valkosti:
   1. Í reitnum **Kenni tillögulína er tilgreint** nýja codeunit fyrir tillögulínur í Intrastat-skýrslulínunum.
   2. Í reitnum **Kenni** efniskótasafns er tilgreint nýja codeunit fyrir útflutning gagna sem skrá með skilgreiningu gagnaskipta.
   3. Í reitnum **Staðfesta auðkenni codeunit** skal tilgreina nýju codeunit fyrir staðfestingu niðurstaðna í Intrastat-skýrslulínum.

> [!IMPORTANT]
> Þessi lína verður að vera auð ef notaðar eru hefðbundnar kóðaeiningar. Þú ættir aðeins að búa til línu og stilla hana ef þú hefur búið til sérsniðnar kóðaeiningar.

## Aðrar Intrastat stillingar

Á viðskiptamanna- og lánardrottnaspjöldum er reiturinn **Tegund** Intrastat-félaga sem hefur sömu gildi og reiturinn **Tegund** félaga: 

- "" (autt)
- *Fyrirtæki*
- *Persóna*
    
Reiturinn **Tegund** Intrastat-félaga kom í stað reitsins **Tegund** félaga í Intrastat-skýrslugerð. Reiturinn **Gerð viðskiptafélaga** er notaður á sameiginlega evrópska greiðslusvæðinu (SEPA) til að skilgreina SEPA beingreiðslukerfið (CORE eða B2B). Reiturinn **Gerð Intrastat-viðskiptafélaga** er aðeins notaður fyrir Intrastat-skýrslugerð. Því er hægt að tilgreina mismunandi gildi fyrir reitina tvo ef þörf krefur.

Ef reiturinn **Gerð Intrastat-viðskiptafélaga** er hafður auður er gildið úr reitnum **Gerð viðskiptafélaga** notað við Intrastat-skýrslugerð.

Auk **Uppsetningar** Intrastat-skýrslu, **skilgreininga** gagnaskipta og **Gátlista** Intrastat-skýrslu verður einnig að grunnstilla eftirfarandi stillingar.

| Síða | Heimildasamstæða |
| ---- | ----------- |
| **Lönd/svæði** | Á síðunni **Lönd/svæði** skal bæta við **upplýsingum um lands-/svæðiskóta** ESB og **Intrastat-kóta** til að tilgreina kóta fyrir landið/svæðið sem notandi á viðskipti við. Þessar upplýsingar verða notaðar við Intrastat-skýrslugerð. |
| **Tollflokkar** | Í mörgum löndum/svæðum stofna tolla- og skattayfirvöld átta stafa kóta fyrir ýmsar vörur. Til að gera birgðafærslum kleift að innihalda nauðsynlegar upplýsingar þegar kerfið flytur þær í Intrastatbókarlínu er vörukótinn færður inn á **síðuna Tollflokkar** . Finna skal kóta varanna sem fyrirtækið verslar við og færa þá inn á síðuna **Tollflokkar** . |
| **Flutningsmátar** | Það eru sjö eins stafa kótar fyrir Intrastat flutningsmáta: **1 fyrir sjó,2**  **fyrir járnbraut, 3** fyrir vegi, **4** fyrir flugi,5 **·**  **fyrir bókun,7**  **fyrir fastar uppsetningar, og** 9 **fyrir eigin knýju (til dæmis flytja bíl með því að aka honum).**  [!INCLUDE[prod_short](includes/prod_short.md)] þarfnast ekki þessara tilteknu kóta. Hins vegar er mælt með því að lýsingin gefi svipaða merkingu. |
| **Tegundir viðskipta** | Lönd og svæði hafa ólíka kóða fyrir tegundir Instrastat viðskipti, eins og venjuleg innkaup og sala, skipti á skilavörum, og skipti á vörum sem ekki hefur verið skilað. Setja upp alla kóða sem eiga við í þínu landi/svæði. Þessir kóðar eru síðan notaðir á flýtiflipanum **Erlend viðskipti** á sölu- og innkaupaskjölum og þegar unnið er úr skilum. |
| **Lýsingar viðskipta** | Setja upp kóða til viðbótar við lýsingar á tegundum viðskipta. |
  
> [!NOTE]
> Frá og með janúar 2022 krefst Intrastat mismunandi viðskiptareðliðakóta fyrir afgreiðslu til einstaklinga eða skráðra fyrirtækja sem ekki eru VSK og VSK-skráðra fyrirtækja. Til að uppfylla þessa þörf er mælt með því að þú skoðir eða bætir nýjum færslueðliskótum við á **síðunni Tegund viðskipta**, í samræmi við kröfur í landi þínu. Þú ættir einnig að athuga og uppfæra reitinn **Gerð Intrastat-viðskiptafélaga** í *Einstakling* fyrir einstaklinga sem eru ekki skráðir VSK-skyldir eða fyrirtæki sem eru skráð VSK-skyld á viðkomandi síðu **Viðskiptavinar**. Ef notandi er óviss um rétta tegund Intrastat-félaga eða tegund viðskipta til að nota er mælt með því að spurt sé um sérfræðing í landi eða svæði.

|   Svæði   |   Heimildasamstæða   |
| --------- | --------------- |
| **Nettóþyngd** | Þyngd er ein af grunnstillingunum sem tengjast Intrastat-skýrslugerð þar sem heildarþyngd er áskilin til skýrslugerðar. Tilbúið fyrir þessa þörf er fært inn gildi í reitinn **Nettóþyngd** á birgða- eða eignaspjaldinu. |
| **Kóði upprunalands** | Nota skal tveggja stafa ISO-kóta alfa á vöru- eða eignaspjaldi fyrir landið/svæðið þar sem varan var fengin eða framleidd. Ef varan var framleidd í fleiri en einu landi/svæði er landið/svæðið upprunaland síðasta landið/svæðið þar sem unnið var verulega úr henni. |
| **VSK-númer samstarfsaðila í aðildarríkinu þar sem innflutningur fer fram** | Þetta er VSK-númer samstarfsaðila í aðildarríkinu þar sem innflutningur fer fram. Vsk-kennið er einnig notað í skiptum við útflutningsgögn innan ESB-aðildarríkjanna og gerir aðildarríkjunum kleift að úthluta mótteknum gögnum til innflutningsfyrirtækis í eigin landi/svæði. Tilkynningarskyldar vörur verða að tilgreina VSK-númer fyrirtækis sem taldi fram til tolls vegna vörukaupa í aðildarríkinu þar sem innflutningur fer fram. |

Einnig er hægt að setja upp:

* **Vörukóði**: Tolla- og skattyfirvöld hafa sett fram númerakóða sem flokka vörur og þjónustu. Hægt er að tilgreina þessa kóta fyrir vörur.
* **Svæði**: Viðbótarupplýsingar um lönd og svæði.
* **Komu-/brottfararstaðir**: Tilgreina skal birgðageymslurnar þar sem vörur eru sendar eða mótteknar eða frá öðrum löndum/svæðum. Flugstöðin er dæmi um komu-brottfararstað. Komu/brottfararstaði er hægt að færa inn í sölu- og innkaupskjöl á flýtiflipanum **Erlend viðskipti**. Þessar upplýsingar eru afritaðar úr birgðafærslum þegar Intrastatbók er stofnuð.
* **Viðbótarmælieining**: Magn vara til Intrastat-skýrslugerðar getur verið annað hvort nettóþyngd (í kílógrömmum) eða viðbótareining. Ef þörf er á viðbótareiningum verður að stilla þær fyrir vörur og eignir.

#### Settu upp flutningsmáta

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **flutningsmáta** og velja síðan viðeigandi tengil.
2. Upplýsingarnar í reitnum eru fylltar út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### Uppsetning eðliskóða viðskipta

1. Velja Skal Aðgerðina ![Lightbulb sem opnar Tell Me.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **tegundir** viðskipta og velja síðan viðeigandi tengil.
2. Upplýsingarnar í reitnum eru fylltar út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Aðrar tengdar stillingar

Áður en aðgerðin Intrastat-skýrslugerð er notuð þarf að skilgreina reiti á vöru-, eigna-, viðskiptamanna- og lánardrottnaspjöldum.

#### Birgðaspjöld

Fylgið þessum skrefum til að setja upp allar nauðsynlegar upplýsingar sem tengjast Intrastat á birgðaspjöldum.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Vörur** og velja síðan viðeigandi tengil.
2. Veldu vöru til að stilla.
3. Á flýtiflipanum **Kostnaður & bókun** er fært inn gildi í reitina **Kóti tollflokks**, **viðbótarmælieiningar** og **Upprunaland/svæði upprunakóta** .

    > [!NOTE]
    > Til að nota mælieiningu til að bæta grunnmælieiningunni viðbót skal grunnstilla viðbótarmælieininguna á síðunni **Mælieiningar** vöru.

4. Á flýtiflipanum **Birgðir** í reitnum **Nettóþyngd** er fært inn gildi með tugasniði.

> [!NOTE]
> Þegar tollflokki er bætt við mælieiningu sem skilgreind er fyrir vöruna er [!INCLUDE [prod_short](includes/prod_short.md)]  reiturinn Viðbótarmælieining **sjálfkrafa fylltur** út samkvæmt grunnstillingu tollflokks. Hægt er að breyta gildinu í reitnum **Viðbótarmælieining** eftir þörfum.

#### Setja upp eignir fyrir Intrastat

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Eignir** og velja síðan viðeigandi tengil.
2. Veldu eignina sem á að stilla.
3. Á flýtiflipanum **Intrastat**, í reitunum **Tollflokksnr.**, **Nettóþyngd** og **Viðbótarmælieining**, er fært inn gildi.

> [!NOTE]
> Þú getur notað mismunandi mælieiningar sem viðbótarmælieiningar. Óháð því hvaða **Mælieiningarkóða** sem þú velur, verður **Magn** hans í Intrastat-skýrslum alltaf 1.

#### Setja upp lánardrottna fyrir Intrastat

Áður en hægt er að taka lánardrottin með í Intrastat-skýrslugerð skal færa upplýsingar þeirra inn á **síðuna Lánardrottnaspjald** . Til dæmis má tilgreina **gildi lands-/svæðiskóta** og **VSK-númer.** virði.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **lánardrottna** og velja síðan viðeigandi tengil.
2. Velja skal lánardrottinn sem á að stilla.
3. Á flýtiflipanum **Intrastat**, í reitunum **Tegund sjálfgefinnar millifærslu**, **Sjálfg. millif.tegund - Vöruskil** og **Sjálfgefinn flutningsmáti** er sett sjálfgefið gildi fyrir hvern reit.
4. Á flýtiflipanum **Greiðslur** í reitnum **Tegund** Intrastat-félaga er tilgreint hvort lánardrottinn sé einstaklingur eða fyrirtæki.

#### Setja upp viðskiptamenn fyrir Intrastat

Áður en hægt er að taka viðskiptamann með í Intrastat-skýrslugerð skal færa upplýsingar þeirra inn á síðuna **Viðskiptamannaspjald** . Til dæmis þarf að tilgreina **gildi lands-/svæðiskóta** og **VSK-númer.** virði.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Viðskiptamenn** og velja síðan viðeigandi tengil.
2. Veldu viðskiptavin til að stilla.
3. Á flýtiflipanum **Intrastat**, í reitunum **Tegund sjálfgefinnar millifærslu**, **Sjálfgefin millifærslutegund - Vöruskil** og **Sjálfgefinn flutningsmáti** er sjálfgefið gildi stillt fyrir hvern reit.
4. Á flýtiflipanum **Greiðslur** í reitnum **Tegund** Intrastat-félaga er tilgreint hvort lánardrottinn sé einstaklingur eða fyrirtæki.

#### Útiloka vörur og eignir frá Intrastat-skýrslugerð

Ef ástæða er til að útiloka tiltekna vöru eða eign úr Intrastat-skýrslugerð skal breyta valkostinum á spjaldinu sem merkir **reitinn Sleppa úr Intrastat-skýrslu** . Þessi reitur er notaður á **birgðasniðmátsspjaldinu** til að búa til fleiri vörur án Intrastat-skýrslugerðar. 

##### Útiloka vöru frá Intrastat-skýrslugerð

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Vörur** og velja síðan viðeigandi tengil.
2. Varan sem á að grunnstilla er valin og á flýtiflipanum **Kostnaður & bókun** skal velja **gátreitinn Sleppa úr Intrastat-skýrslu** .

##### Útiloka eign frá Intrastat-skýrslugerð

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Eignir** og velja síðan viðeigandi tengil.
2. Veldu eignina sem á að stilla.
3. Á flýtiflipanum **Intrastat** er gátreiturinn **Sleppa úr Intrastat-skýrslu** valinn.

#### Setja upp tollflokka

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Tollflokkar** og velja síðan viðeigandi tengil.  
2. Á síðunni **Tollflokkar** eru færðar inn upplýsingar í reitina sem lýst er í eftirfarandi töflu.

    | Svæði | Heimildasamstæða |  
    |-------|-------------|
    | **Nr.** | Tilgreinir tollflokk. |
    | **Lýsing** | Tilgreinir lýsingu á tengdu tollflokki. |
    | **Viðbótareiningar** | Tilgreinir hvort tolla- og skattayfirvöld krefjist upplýsinga um magn og mælieiningu vörunnar. |
    | **Umreiknistuðull** | Tilgreinir umreiknistuðul fyrir tollflokkinn. |
    | **Mælieining** | Tilgreinir mælieiningu fyrir tollflokk. |

> [!NOTE]
> Ef viðbótarmælieiningu [!INCLUDE [prod_short](includes/prod_short.md)]  er bætt við er spurt hvort uppfæra eigi tengdar vörur. Ef valið er að uppfæra tengdar vörur er gildið **Mælieining** á síðunni **Mælieiningar** vöru uppfært fyrir allar vörur sem hafa sama tollflokk.
>
> Þegar tollflokki sem hefur skilgreint **mælieiningargildi** við vöruna er [!INCLUDE [prod_short](includes/prod_short.md)]  sjálfkrafa bætt við nýja mælieiningu við **gildi mælieiningar** vörunnar. Gildið **Magn á mælieiningu** er byggt á reitnum **Sléttunarnákvæmni magns** .

## Færa inn Intrastat-stillingar fyrir land/svæði

Intrastatskilyrði eru svipuð í öllum aðildarríkjum ESB, þó að mikilvægar undantekningar séu gerðar. Fræðilega ættu reglurnar gilda á sama hátt í öllum aðildarríkjum. Hins vegar er munur á innleiðingu því sum aðildarríki bjóða upp á leiðbeiningar um hvernig beita skuli meginreglunum í tilteknum aðstæðum (til dæmis viðskiptasýni og vöruskilum). Þessar leiðbeiningar geta skilað mismunandi niðurstöðum í ýmsum aðstæðum. Þess vegna verða upplýsingarnar sem lönd/svæði færa inn geta verið mismunandi, eins og skráarsniðið sem þær verða að nota við skýrslugerð.

### Austurríki

Intrastat-skýrslugerð í Austurríki krefst tveggja mismunandi skráa fyrir móttökur og afhendingar. Til að staðfesta að uppsetningin sé rétt skal fylgja þessum skrefum.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Uppsetning** Intrastat-skýrslu og velja síðan viðeigandi tengil.  
2. Á flýtiflipanum **Skýrslur** er athugað hvort **Skipta móttökum/afhendingarskrám** er valið. Ef svo er finnast tvö aðskilin **gildi sjálfg. gagnaskilgreindra kóta**  . 
3. Ganga þarf úr skugga um að reiturinn **Zip-skrár sé valinn til að tryggja að skýrsluskrám verði bætt við zip-skrána** .

Vinnsla Intrastat-skýrslna er sú sama og altæki eiginleikinn.

<!-- ### Belgium-->

### Tékkland

Nýja Intrastat-skýrslan fyrir Tékkland verður tiltæk árið 2023 útgáfubylgju 1. Í millitíðinni skal halda áfram að nota aðgerðina **Intrastatbók** .

### Finnlandi

Í Finnlandi eru nokkrar viðbótarskref til að setja upp Intrastat. Intrastat-skýrslugerð í Finnlandi krefst tveggja mismunandi skráa fyrir móttökur og afhendingar. Einnig sést að tvö aðskilin gagnaskilgreind **kótagildi** eru skilgreind.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Uppsetning** Intrastat-skýrslu og velja síðan viðeigandi tengil.  
2. Á síðunni **Uppsetning** Intrastat-skýrslu á flýtiflipanum **Skráargrunnur** skal færa inn upplýsingar um reitinn eins og lýst er í eftirfarandi töflu.

    |                 Svæði              |            Heimildasamstæða                |  
    |------------------------------------|---------------------------------------|
    | **Sérsniðinn kóti** | Tilgreinir sérsniðinn kóða fyrir upplýsingar um uppsetningu Intrastatskrár. |
    | **Raðnr. fyrirtækis** | Tilgreinir raðnúmer fyrirtækis fyrir upplýsingar um uppsetningu Intrastat-skráa. |

3. Á flýtiflipanum **Skýrslur** er athugað hvort **Skipta móttökum/afhendingarskrám** er valið.

Vinnsla Intrastat-skýrslna er sú sama og altæki eiginleikinn.

<!-- ### Germany-->

### Ítalíu

Ný Intrastat-skýrslureynsla fyrir Ítalíu verður tiltæk í febrúar 2023. Í millitíðinni skal halda áfram að nota aðgerðina **Intrastatbók** .

<!-- ### France-->

### Svíþjóð

Intrastat-skýrslugerð í Svíþjóð krefst tveggja mismunandi skráa fyrir móttökur og afhendingar. Til að staðfesta að uppsetningin sé rétt skal fylgja þessum skrefum.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Uppsetning** Intrastat-skýrslu og velja síðan viðeigandi tengil.  
2. Á flýtiflipanum **Skýrslur** er staðfest að **Skipta móttökum/afhendingarskrám** hafi verið valið. Ef svo er finnast tvö aðskilin **gildi sjálfg. gagnaskilgreindra kóta** .

Vinnsla Intrastat-skýrslna er sú sama og í altækum aðgerðum.

<!-- ### United Kingdom-->

## Sjá einnig .

[Intrastat-skýrslugerð í Business Central](finance-how-report-intrastat.md)  
[Fjármálastjórnun](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
