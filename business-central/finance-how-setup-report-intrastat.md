---
title: Setja upp Intrastat-skýrslugerð
description: Í greininni er útskýrt hvernig setja á upp aðgerðir Intrastat-skýrslna til að tilkynna viðskipti með fyrirtæki í öðrum löndum ESB/svæðum.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 04/05/2023
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
---
# <a name="set-up-intrastat-reporting"></a>Setja upp Intrastat-skýrslugerð

Öll fyrirtæki í löndum innan Evrópusambandsins (ESB) þurfa að gefa öðrum löndum/svæðum innan sambandsins skýrslur um viðskipti sín. Einnig þarf að gefa hagstofu viðkomandi lands/svæðis mánaðarlega skýrslu um hreyfingu vöru og skýrsluna þarf að afhenda skattayfirvöldum. Intrastat er kerfið sem notað er til að safna saman viðskiptatalnagögnum um vörur í þessum löndum/svæðum. Notið Intrastat-skýrsluna til að ljúka reglubundinni Intrastat-skýrslugerð með því að safna, taka upp og tilkynna um viðskipti með vörur samkvæmt löggjöf landsins.

Intrastat-skýrslugerð byggir á grunnreglum ESB sem gilda um öll lönd/svæði. Hins vegar eru munir innan einstakra landa/svæða. Hvert land/svæði hefur sínar reglur um hvað og hvernig á að tilkynna.

> [!NOTE]
> Upplýsingar um Intrastat eiga ekki við um tilfærslu þjónustu milli landa/svæða. Þess í stað eiga upplýsingarnar aðeins við um vörur eins og vörur og eignir. Ef stjórnvöld krefjast þess að þú skráir tilfærslu á þjónustu milli landa/svæða skaltu nota  **aðgerðina Þjónustuskýrsla** .
>
> Þessi eiginleiki er tiltækur sem App sem hægt er að hlaða niður [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). Ef nota á þessa aðgerð skal setja hana upp á  **síðunni um Framlengingarstjórnun** .

> [!IMPORTANT]
> Þessi grein fjallar um þá nýju Intrastat-reynslu sem eru í boði frá  [!INCLUDE[prod_short](includes/prod_short.md)]  útgáfu 21. Hafa skal samband við kerfisstjóra til að fá upplýsingar um hvaða útgáfu fyrirtækið á að nota og hvort eigi að virkja nýju virkjunina.
>
> Lesa Intrastat-uppsetningu og notkunargrein fyrri útgáfu,  [Setja upp og skrá Intrastat](finance-how-setup-report-intrastat-v20.md).

## <a name="enable-the-new-intrastat-experience"></a>Gera nýju Intrastat upplifunina virka

Í 2022 útgáfu bylgju 2,  [!INCLUDE[prod_short](includes/prod_short.md)]  felur í sér endurhannaðan Intrastat-reynslu sem veitir auknar aðgerðir. Ef nýi Intrastat-aðgerðin er ekki virkjuð í umhverfinu getur kerfisstjóri gert hana virka á  **síðunni Feature Management** .

> [!IMPORTANT]
> Ekki er hægt að nota gömlu og nýju upplifanirnar samhliða. Áður en framlenging er virkjuð í vinnsluumhverfi mælum við með að þú prufið hana í sandkassa umhverfi með því að nota afrit af framleiðslugögnum þínum. Eftir að ný notendareynsla hefur verið virkjuð í vinnsluumhverfinu er ekki hægt að bakfæra gömlu Intrastat-aðgerðirnar.

1.  :::image type="icon" source="media/ui-search/search_small.png" border="false"::: Velja skal teiknið, færa inn  **aðgangsstjórnun** og velja síðan tengda tengilinn.
2.  **Á síðunni Feature Management**  skal velja línuna fyrir  **uppfærslu eiginleika: skipta skal fyrirliggjandi Intrastat-aðgerðum með nýju viðaukanum** Intrastat. Frekari upplýsingar um aðgangsstjórnun fást  [með því að virkja komandi aðgerðir fram í tímann](/dynamics365/business-central/dev-itpro/administration/feature-management).
3.  **Í dálkinum virkja fyrir**  dálk skal velja  **alla notendur**.
4. Lestu útskýringuna um hvernig kerfið verður uppfært og veldu  **svo Já**  til að samþykkja það.
5. Veldu **Áfram**. Farið verður í grunnuppsetningu Intrastat. Sjá  [kaflann um Intrastat-afbrigði](#intrastat-configuration)  síðar í þessari grein til að lesa meira um uppsetningu Intrastat.
6. Þegar uppsetningu er lokið er valið  **Ljúka**  til að byrja á að nota nýju Intrastat-reynsluna.

    > [!NOTE]
    > Það mun nægja til að virkja áður lýstum aðgerðum eftir staðsetningu fyrirtækisins. Fyrir lönd/svæði sem hafa sértækar aðgerðir fyrir Intrastat-skýrslugerð skal virkja sérstakt Intrastat-App fyrir land/svæði til viðbótar við kjarna Framlengingar.

## <a name="intrastat-configuration"></a>Uppsetning Intrastat

Áður en hægt er að nota Intrastat skýrslur þarf að setja upp nokkrar stillingar.

### <a name="intrastat-reporting-setup"></a>Uppsetning Intrastat-skýrslugerðar

 **Notaðu síðuna Intrastat-Skýrsluuppsetning**  til að virkja og stilla sjálfgefna hegðun fyrir Intrastat skýrslugerð. Hægt er að tilgreina hvort þörf sé á að skrá Intrastat úr sendingum (sendingar), kvittanir (komuskjöl) eða bæði eftir þröstrunum sem settar eru af viðkomandi reglum. Einnig er hægt að stilla sjálfgefnar færslugerðir fyrir regluleg og skilaskjöl sem eru notuð við færsluskýrslugerð.

Fylgið þessum skrefum til að setja upp Intrastat-skýrslugerð.

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **Intrastat-skýrsluuppsetningu** og velja síðan tengda tengilinn.
2.  **Á flipanum Almennt**  skal velja eða færa inn Svæðisupplýsingar eins og þarf. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Eftirfarandi tafla lýsir nokkrum lykilsvæðunum.

   | Svæði | Heimildasamstæða |
   | --- | --- |
   | **Skrá kvittanir** | Tilgreinir að taka verði með mótteknar vörur sem berast í Intrastat-skýrslum. |
   | **Skrá afhendingar** | Tilgreinir að taka verði með afgreiddar vörur sem eru sendar í Intrastat-skýrslum. |
   | **Taka með beina afhendingu** | Tilgreinir hvort færslur beinnar sendingar séu innifaldar í Intrastat-skýrslum. Sjá  [vinnu með Intrastat-skýrslugerð](finance-how-report-intrastat.md) til að fá frekari upplýsingar.  |  
   | **Sendingar byggðar á**  | Tilgreinir landskótann á grundvelli þess hvaða Intrastat-skýrslulínur eru teknar.  |
   | **VSK-nr. byggt á** | Tilgreinir kóta viðskiptavinar eða lánardrottins á grundvelli þess að virðisaukandi skatturinn (VSK) sé tekinn fyrir Intrastat-skýrsluna.  |
   | **Skráð VSK-númer fyrirtækis** | Tilgreinir hvernig VSK-númer fyrirtækisins er flutt út í Intrastat-skrána.  |
   | **Skráð VSK-númer lánardrottins** | Tilgreinir hvernig VSK-númer lánardrottins er flutt út í Intrastat skrána.  |
   | **Skráð VSK-númer viðskiptamanns** | Tilgreinir hvernig VSK-númer viðskiptavinar er flutt út í Intrastat skrána.  |
   | **Fá VSK samstarfsaðila** | Tilgreinir hvaða gerð af skýrslulínu VSK-númer félaga er uppfærð. Aðeins er hægt að velja móttökulínur, aðeins afhendingarlínur eða báðar gerðir af línum eftir þörfum sveitarfélaga. |

4.  **Á flipanum sjálfgefin færslur**  skal velja eða færa inn Svæðisupplýsingar eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Eftirfarandi tafla lýsir nokkrum lykilsvæðunum.

   | Svæði | Heimildasamstæða |
   | --- | --- |
   | **Sjálfgefin færslugerð** | Tilgreinir sjálfgefna færslugerð fyrir reglulegar söluafhendingar, þjónustuafhendingar og innkaupakvittanir. |
   | **Sjálfgefin færslugerð - Skil** | Tilgreinir sjálfgefna færslugerð fyrir söluvöruskil, þjónustuskil og innkaupaskil. |
   | **Sjálfgefið VSK-nr. einstaklings** | Tilgreinir sjálfgefið númer VSK á einkaðila ef einkaaðilinn verður að hafa sérvalið VSK-númer á Intrastat-skýrslunni. |
   | **Sjálfgefið VSK-nr. þriðja aðila** | Tilgreinir sjálfgefið VSK-númer af þriggja aðila viðskiptum ef VSK-númer er ekki til. |
   | **Sjálfvalinn VSK fyrir óþekkt ríki** | Tilgreinir sjálfgefið VSK-númer fyrir óþekkt ríki. |
   | **Sjálfgefinn lands-/svæðiskóði** | Tilgreinir sjálfgefinn kóða móttökulands. |

5.  **Á flipanum skýrslugjöf**  skal velja eða færa inn Svæðisupplýsingar eins og þarf. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Eftirfarandi tafla lýsir nokkrum lykilsvæðunum.

   | Svæði | Heimildasamstæða |
   | --- | --- |
   | **Skilgreiningarkóði gagnaskipta** | Tilgreinir skilgreiningarkóða gagnaskipta til að búa til Instrastat-skrá. Þetta svæði er aðeins tiltækt ef  **reiturinn skiptar kvittanir/afhendingar**  er stilltur á  **Nr**. |
   | **Skipta skrám innhreyfinga/afhendinga** | Tilgreinir hvort tilkynna eigi móttöku og sendingar í tveimur aðskildum skrám. |
   | **Zip-skrá(-r)** | Tilgreinir hvort skýrsluskránum skuli bætt við zip-skrána. |
   | **Skilgreiningarkóði gagnaskipta - Innhreyfing** | Tilgreinir skilgreiningarkóða gagnaskipta til að búa til Instrastat-skrá fyrir mótteknar vörur. Þetta svæði er aðeins tiltækt ef  **reiturinn skiptar kvittanir/afhendingar**  er stilltur á  **Já**. |
   | **Skilgreiningarkóði gagnaskipta - Afhending** | Tilgreinir skilgreiningarkóða gagnaskipta til að búa til Instrastat-skrá fyrir sendar vörur. Þetta svæði er aðeins tiltækt ef  **reiturinn skiptar kvittanir/afhendingar**  er stilltur á  **Já**. |

6.  **Á flipanum Tölusetning**  er gildi fært inn í  **reitinn Intrastat nr** .

### <a name="set-up-a-reporting-file"></a>Setja upp skýrsluskrá

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **upplýsingar um Gengisskilgreiningar** og velja síðan tengda tengilinn.
2. Valið  **er nýtt** og síðan á  **flipanum Almennt**, Færið inn upplýsingar um gagnaskiptaskilgreininguna, gerð gagnaskrár, skiltákn dálka, tengdar kótaeiningar  XMLport og önnur svæði eftir þörfum.
3.  **Á flipanum Fastlínuskilgreiningar**  er fært inn gildi í  **reitinn Tegund**  línu til að lýsa sniði línanna í gagnaskránni og hvar þarf að skilgreina fjölda dálka fyrir þessa línu.
4. Á flýtiflipanum **Dálkskilgreiningar** er fyllt út í línuna fyrir hvern fyrirhugaðan dálk. Hægt er að skilgreina dálkheiti, gagnagerðir (til dæmis texta, dagsetningu eða aukastaf) lengd línunnar sem geymir dálkinn ef skráin er af  *fastri Textagerð*  og öðrum færibreytum.
5.  **Á flipanum Fastlínuskilgreiningar**  er valin  **vörpun** svæða.
6.  **Stofnið nýja færslu á Svæðvörpunarsíðunni** . 
7.  **Á flipanum Almennt**  skal velja  **töflukennigildið**  (fyrir  **Intrastat-skýrslulínuna**, velja  **4812**) og færa inn upplýsingar um eftirfarandi reit:

   1.  **Í reitnum Lyklavísitala**  skal tilgreina lyklavísi til að raða Upprunafærslur fyrir útflutning.
   2.  **Veljið gildi í svæðinu vörpun Codeunit** .

8.  **Á flipanum Flýtivörpun**  í svæðið skal bæta við dálkunum sem áður voru skilgreindir í  **fastflipa Dálkaskilgreininganna**  og bæta síðan eftirfarandi upplýsingum við svæði:

   1.  **TILGREINIÐ kennigildi**  svæðisins fyrir hvern dálkana.
   2.  **Tilgreinið gildi umbreytingarreglunnar**  fyrir hvern dálk eftir þörfum. Gildið Tilgreinir regluna sem umbreytir innfluttum texta í studd gildi áður en hægt er að tengja hann við tiltekið svæði í [!INCLUDE[prod_short](includes/prod_short.md)]. Þegar gildi er valið í þessum reit er nákvæmar gildi slegið inn í reitinn **Umbreytingarregla** í töflunni **Biðminni vörpunar gagnaskiptareits** töflu. (Umræðulaust þegar nákvæm virðisauki er inn í  **Svæðið umbreytingarregla**  í  **reitnum exch.** Er valið gildi í þessu svæði.)

9. Ef flokka þarf færslur út frá einhverjum dálkum skal  **velja svæðin sem óskað er eftir að nota við flokkun svæðisins** .

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] forskilgreinda gagnaskiptaskilgreiningu fyrir Intrastat fyrir öll staðbundin lönd/svæði. Frekari upplýsingar um hvernig á að stofna nýja skilgreiningu gagnaskipta er að finna  [í setja upp skilgreiningar](across-how-to-set-up-data-exchange-definitions.md) á gögnum.

### <a name="set-mandatory-fields-with-the-intrastat-report-checklist"></a>Stilltu áskilda reiti með gátlistanum fyrir Intrastat-skýrsluna

Í sumum löndum/svæðum krefjast yfirvöld þess að Intrastat-skýrslur séu til dæmis afhendingaraðferðir fyrir innkaup eða annað gildi þegar sala er yfir ákveðnum þröskuldi.

Fylgdu þessum skrefum til að setja skyldusvæði eða gildi á  **síðuna Intrastat-skýrsla** .

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **Intrastat-skýrsluuppsetningu** og velja síðan tengda tengilinn.
2. Velja  **gátlista** Intrastat-skýrslu.
3. Fylgdu þessum skrefum til að bæta við nauðsynlegum línum til að athuga:
   1. Stilltu **Reit nr.** á reit sem þarf að athuga fyrir gildi sem ekki er tómt.
   2. Færið inn gildi í  **svæðið sía segð**  ef þarf, Byggt á eftirfarandi reglum:

        1. Þegar síusíðan  **er opnuð** skal velja síuna sem nota á til að stöðva.
        2. Veljið gildi sem tengist valinni síu.
        3. Ef fylla verður á fleiri afmarkanir fyrir valið svæði er fyrri skrefin endurtekin til að bæta við annarri síu.
        4. Þegar lokið er við að færa inn afmarkanir fyrir valið svæði er valið  **í lagi**.

   3.  **Gátreiturinn bakfærða síu**  er valinn til að tilgreina að reiturinn fyrir svæðin sé aðeins keyrður á þeim línum sem samsvara ekki síunarsegðinni. Ef línan er ekki afmörkuð er þetta svæði hunsað.

> [!NOTE]
> Þegar **Síusíðan** er opnuð úr **Síusegðarínunni** er hægt að nota allar staðlaðar síusegðir í tengslum við tiltekinn reit sem á að sía.
>
> Gættu varúðar þegar villuleitarreglur eru settar upp, því þær geta verið mismunandi milli landa/svæða.

## <a name="use-custom-codeunits-in-intrastat-reporting"></a>Nota sérstillta kóðaeiningar í Intrastat-skýrslum

Ef óskað er eftir að breyta því hvernig Intrastat virkar og sjálfgefna afbrigðið nægir ekki er hægt að sérsníða kerfið með því að víkka út staðalaðgerðirnar. Ef þörf er á að breyta hegðun Intrastat frekar er hægt að þróa eigin kóðaeiningar. Þegar þú býrð til kódeunits þarft þú að gera frekari breytingar til að nota þær. Fylgdu þessum skrefum til að skilgreina kerfið til að nota eigin hluti.

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **skilgreiningu** VSK-skýrslna og velja síðan tengda tengilinn.
2. Á síðunni **Skilgreining VSK-skýrslna** er nýrri línu bætt við.
3.  **Í reitnum Tegund**  VSK-skýrslu skal velja  **Intrastat-skýrslu**.
4.  **Í reitnum útgáfureitur**  VSK-skýrslu skal tilgreina útgáfu skýrslunnar.
5. Bættu við kódeseiningum fyrir eftirfarandi valkosti:
   1.  **Í reitnum leggja til línur í kenni**  kódeunit skal tilgreina nýja kódeunit fyrir línur í Intrastat-skýrslulínunum.
   2.  **Í reitnum innihald CODEUNIT ID**  skal tilgreina nýja Codeunit fyrir útflutning gagna sem skrá með því að nota Gagnaskiptaskilgreiningu.
   3.  **Í reitnum Villuleita Kódeunit ID**  skal tilgreina nýjar kótaeiningar fyrir villuleit í línum Intrastat-skýrslu.

> [!IMPORTANT]
> Þessi lína verður að vera auð ef notaðar eru hefðbundnar kóðaeiningar. Þú ættir aðeins að búa til línu og stilla hana ef þú hefur búið til sérsniðnar kóðaeiningar.

## <a name="other-intrastat-configurations"></a>Aðrar Intrastat stillingar

Viðskiptamanna-og lánardrottnaspjöld eru  **með reitnum Tegund**  Intrastat-félaga sem hefur sama valkostagildi og  **reiturinn Tegund**  félagaraðar: 

- "" (autt)
- *Félagsins*
- *Viðkomandi*
    
 **Í reitnum Tegund**  Intrastat-félaga var skipt út  **reitnum Tegund**  félagar í Intrastat-skýrslu. Reiturinn **Gerð viðskiptafélaga** er notaður á sameiginlega evrópska greiðslusvæðinu (SEPA) til að skilgreina SEPA beingreiðslukerfið (CORE eða B2B). Reiturinn **Gerð Intrastat-viðskiptafélaga** er aðeins notaður fyrir Intrastat-skýrslugerð. Þess vegna er hægt að tilgreina mismunandi gildi fyrir svæðin tvö ef þörf krefur.

Ef reiturinn **Gerð Intrastat-viðskiptafélaga** er hafður auður er gildið úr reitnum **Gerð viðskiptafélaga** notað við Intrastat-skýrslugerð.

Auk  **uppsetningar** **Intrastat-skýrslu, skilgreiningar** á gögnum og  **Intrastat-skýrslu** verður einnig að samskipa eftirfarandi stillingum.

| Síða | Heimildasamstæða |
| ---- | ----------- |
| **Lönd/svæði** |  **Á síðunni lönd/svæði**  þarf að bæta  **við ESB-/svæðiskóta**  og  **upplýsingum um Intrastat-**  kóða til að tilgreina kóta fyrir land/svæði sem notandi er í viðskiptum við. Þessar upplýsingar verða notaðar við Intrastat-skýrslugerð. |
| **Tollflokkar** | Í mörgum löndum/svæðum koma tolla-og skattayfirvöld með átta stafa kóða fyrir ýmsar vörur. Ef gera á birgðafærslur til að innihalda nauðsynlegar upplýsingar þegar kerfið flytur þær í Intrastat-bókarlínuna skal færa inn vörukóðann á  **síðunni Tollflokkar** . Finna skal kóta varanna sem fyrirtækið hefur fjallað um og færa þær inn á  **síðuna Tollflokkar** . |
| **Flutningsmátar** | Það eru 7 1 fyrir Intrastat flutningsaðferðir:  **1**  fyrir sjó,  **2**  fyrir Rail,  **3**  fyrir veg,  **4**  fyrir loft,  **5**  fyrir innsetningar,  **7**  fyrir fastar uppsetningar og  **9**  fyrir eigin própút (til dæmis að flytja bíl með því að aka honum). [!INCLUDE[prod_short](includes/prod_short.md)] krefst ekki þessara tilteknu kóða. Við mælum hins vegar með að lýsingarnar gefi svipaða merkingu. |
| **Tegundir viðskipta** | Lönd og svæði hafa ólíka kóða fyrir tegundir Instrastat viðskipti, eins og venjuleg innkaup og sala, skipti á skilavörum, og skipti á vörum sem ekki hefur verið skilað. Setja upp alla kóða sem eiga við í þínu landi/svæði. Þessir kóðar eru síðan notaðir á flýtiflipanum **Erlend viðskipti** á sölu- og innkaupaskjölum og þegar unnið er úr skilum. |
| **Lýsingar viðskipta** | Setja upp kóða til viðbótar við lýsingar á tegundum viðskipta. |
  
> [!NOTE]
> Byrjar í janúar 2022 Intrastat krefst mismunandi kóta færslu fyrir sendingar til einka einstaklinga eða VSK skráðra fyrirtækja og VSK-skráðra fyrirtækja. Til að fara eftir þessum kröfum er mælt með því að skoða eða bæta við nýjum náttúrukóðum á  **síðunni tegundir**  viðskipta, í samræmi við kröfurnar í þínu landi. Þú ættir einnig að athuga og uppfæra reitinn **Gerð Intrastat-viðskiptafélaga** í *Einstakling* fyrir einstaklinga sem eru ekki skráðir VSK-skyldir eða fyrirtæki sem eru skráð VSK-skyld á viðkomandi síðu **Viðskiptavinar**. Ef þú ert ekki viss um rétta gerð Intrastat-félaga eða færslugerð sem á að nota, mælum við með að þú spyrjir sérfræðing á þínu landi eða svæði.

|   Svæði   |   Heimildasamstæða   |
| --------- | --------------- |
| **Nettóþyngd** | Þyngd er ein af grunnskilgreiningum sem tengjast Intrastat-skýrslugerð þar sem Heildarþyngd er skylda til skýrslugerðar. Til að vera tilbúin í þessa kröfu skal færa inn gildi í  **reitinn Nettóþyngd**  á vörunni eða eignaspjaldinu. |
| **Kóði upprunalands** | Notaðu tveggja bókstafa ISO alfa kóðana á vöru-eða eignaspjaldi fyrir land/svæði þar sem góan var fengin eða framleidd. Ef góan var framleidd í fleiri en einu landi/svæði er upprunaland/-svæði Síðasta landið/svæðið þar sem hún var verulega unnin. |
| **VSK-númer samstarfsaðila í aðildarríkinu þar sem innflutningur fer fram** | Þetta er VSK-númer samstarfsaðila í aðildarríkinu þar sem innflutningur fer fram. VSK-ID er einnig notað í skiptum innan ESB-útflutningsgagna meðal aðildarríkjanna og heimilar aðildarríkjunum að ráðstafa mótteknum gögnum til innflutningsfyrirtækja í eigin landi/á svæði. Tilkynningarskyldar vörur verða að tilgreina VSK-númer fyrirtækis sem taldi fram til tolls vegna vörukaupa í aðildarríkinu þar sem innflutningur fer fram. |

Einnig er hægt að setja upp:

* **Vörukóði**: Tolla- og skattyfirvöld hafa sett fram númerakóða sem flokka vörur og þjónustu. Hægt er að tilgreina þessa kóta á vörur.
* **Svæði**: Viðbótarupplýsingar um lönd og svæði.
* **Innsláttar-/brottfararstaðir** : Tilgreinið þá staði sem eru sendingar eða móttöku vara til eða frá öðrum löndum/svæðum. Flugstöðin er dæmi um komu-brottfararstað. Komu/brottfararstaði er hægt að færa inn í sölu- og innkaupskjöl á flýtiflipanum **Erlend viðskipti**. Þessar upplýsingar eru afritaðar úr birgðafærslum þegar Intrastatbókin er stofnuð.
* **Viðbótarmælieining**: Magn vara til Intrastat-skýrslugerðar getur verið annað hvort nettóþyngd (í kílógrömmum) eða viðbótareining. Ef þörf er á viðbótareiningum verður að stilla þær fyrir vörur og eignir.

#### <a name="set-up-transport-methods"></a>Settu upp flutningsmáta

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **flutningsaðferðir** og veljið síðan tengda tengilinn.
2. Upplýsingar í reit eru fylltar út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="set-up-transaction-nature-codes"></a>Uppsetning eðliskóða viðskipta

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **færslugerðir** og velja síðan tengda tengilinn.
2. Upplýsingar í reit eru fylltar út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="other-related-configurations"></a>Aðrar tengdar stillingar

Áður en aðgerðin Intrastat-skýrslugerð er notuð þarf að skilgreina reiti á vörunni, eignir, viðskiptavin og lánardrottnaspjöld.

#### <a name="item-cards"></a>Birgðaspjöld

Fylgið þessum skrefum til að setja upp allar nauðsynlegar upplýsingar sem tengjast Intrastat á birgðaspjöldum.

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **atriði** og veljið síðan tengda tengilinn.
2. Veldu vöru til að stilla.
3.  **Í kostnaði & að bóka**  fastflipann í  **reitunum tollnúmer**,  **fylgimælieining fyrir** vöru og  **land/svæði**, er fært inn gildi.

    > [!NOTE]
    > Ef nota á mælieiningu til viðbótar við grunnmælieiningu skal stilla aukaeininguna mælingar á  **síðunni Mælieiningar vöru** .

4.  **Á birgðaaukanum**, í  **reitnum nettóþyngd**, er fært inn gildi í tugabrotasniðinu.

> [!NOTE]
> Þegar tollskrárnúmeri er bætt við mælieiningu sem skilgreind eru fyrir vöruna  [!INCLUDE [prod_short](includes/prod_short.md)]  fyllir það sjálfkrafa út í  **reitinn fylgimælieining einingar**, samkvæmt skilgreiningu tollnúmers. Hægt er að  **breyta gildi Viðbótarmælieiningar**  í svæði eftir þörfum.

#### <a name="set-up-fixed-assets-for-intrastat"></a>Setja upp eignir fyrir Intrastat

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **eignir** og veljið síðan tengda tengilinn.
2. Veldu eignina sem á að stilla.
3.  **Á flipanum Intrastat-**  Yfirlit í reitnum  **tollnr.**,  **nettóþyngd** og  **fylgimælieining**  skal færa inn gildi.

> [!NOTE]
> Þú getur notað mismunandi mælieiningar sem viðbótarmælieiningar. Óháð því hvaða **Mælieiningarkóða** sem þú velur, verður **Magn** hans í Intrastat-skýrslum alltaf 1.

#### <a name="set-up-vendors-for-intrastat"></a>Setja upp lánardrottna fyrir Intrastat

Áður en hægt er að láta lánardrottinn fylgja Intrastat-skýrslu skal færa inn upplýsingar hans á  **kortasíðu**  lánardrottins. Tilgreinið  **til dæmis lands-/svæðiskótann**  og  **VSK-númer.** gildi.

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **lánardrottna** og veljið síðan tengda tengilinn.
2. Velja skal lánardrottinn sem á að stilla.
3.  **Á flipanum Intrastat**  -fastgerð í  **sjálfgefinni línu-, Type-gerðinni** Sjálfgildi,  **Tegund-skil**, og  **sjálfgefnum flutningsmáta**  er sett sjálfgildi fyrir hvert svæði.
4.  **Á flipanum greiðslur**  í  **reitnum Tegund**  Intrastat-félaga skal tilgreina hvort lánardrottinn er einstaklingur eða fyrirtæki.

#### <a name="set-up-customers-for-intrastat"></a>Setja upp viðskiptamenn fyrir Intrastat

Áður en hægt er að láta viðskiptavin fylgja Intrastat-skýrslu skal færa inn upplýsingar á  **síðu viðskiptamannaspjaldinu** . Til dæmis þarf að tilgreina  **lands-/Svæðiskóðagildi**  og  **VSK númer.** gildi.

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, færa inn  **viðskiptamenn** og velja síðan tengda tengilinn.
2. Veldu viðskiptavin til að stilla.
3.  **Á flipanum Intrastat**  -fastgerð í  **sjálfgefinni línu-gerðinni**,  **Sjálfgefin flutningagerð-skilum**, og  **sjálfgefnum flutningsmáta**  er sjálfgefið gildi stillt fyrir hvert svæði.
4.  **Á flipanum greiðslur**  í  **reitnum Tegund**  Intrastat-félaga skal tilgreina hvort lánardrottinn er einstaklingur eða fyrirtæki.

#### <a name="exclude-items-and-fixed-assets-from-intrastat-reporting"></a>Útiloka vörur og eignir frá Intrastat-skýrslugerð

Ef ástæða er til að útiloka tiltekna vöru eða eign frá Intrastat-skýrslugerð skal breyta valkostinum á kortilmerkingu  **þess útiloka úr Intrastat-skýrslu** . Notið þetta svæði á  **spjaldinu vörusniðmát**  til að stofna fleiri vörur að undanskildum Intrastat-skýrslugjafarskýrslunni. 

##### <a name="exclude-an-item-from-intrastat-reporting"></a>Útiloka vöru frá Intrastat-skýrslugerð

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **atriði** og veljið síðan tengda tengilinn.
2. Veljið vöruna sem á að samskipa og á  **kostnaðarflipanum & bókun**  er valinn, veljið  **gátreitinn útiloka úr Intrastat-skýrslu** .

##### <a name="exclude-a-fixed-asset-from-intrastat-reporting"></a>Útiloka eign frá Intrastat-skýrslugerð

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **eignir** og veljið síðan tengda tengilinn.
2. Veldu eignina sem á að stilla.
3.  **Á flipanum Intrastat-**  Yfirlit skal velja  **gátreitinn útiloka Intrastat-skýrslu** .

#### <a name="set-up-tariff-numbers"></a>Setja upp tollnúmer

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, Sláðu inn  **Tollskrárnúmerin** og veldu síðan tengda tengilinn.  
2.  **Á síðunni Tollflokkar**  eru upplýsingar færðar inn í reitina sem lýst er í eftirfarandi töflu.

    | Svæði | Heimildasamstæða |  
    |-------|-------------|
    | **Nr.** | Tilgreinir númer tollskrárnúmers. |
    | **Lýsing** | Tilgreinir lýsingu á tengdu tollskrárnúmeri. |
    | **Viðbótareiningar** | Tilgreinir hvort tolla og skattyfirvöld krefjist upplýsinga um magn og mælieiningu vörunnar. |
    | **Umreiknistuðull** | Tilgreinir umreiknistuðul fyrir tollflokkinn. |
    | **Mælieining** | Tilgreinir mælieiningu fyrir tollflokk. |

> [!NOTE]
> Ef viðbótarmælieiningum er bætt við er  [!INCLUDE [prod_short](includes/prod_short.md)]  spurt hvort uppfæra eigi tengdar vörur. Ef valið er að uppfæra tengdar vörur  **·**  er gildið Mælieining á  **síðunni Mælieiningar vöru**  uppfærð fyrir allar vörur sem hafa sama tollnúmer.
> 
> Þegar tollnúmeri er bætt við vöru sem hefur skilgreinda  **mælieiningu**  fyrir vöruna skal  [!INCLUDE [prod_short](includes/prod_short.md)]  Bæta sjálfkrafa nýrri mælieiningu við  **gildið fyrir mælieiningar**  vörunnar.  **Gildið magn á mælieiningu**  er byggt á  **Nákvæmnireit**  magnsléttun.

## <a name="enter-countryregion-intrastat-settings"></a>Færa inn Intrastat stillingar fyrir land/svæði

Intrastat-kröfur eru svipaðar í öllum aðildarríkjum ESB, þó eru til mikilvægar undantekningar. Fræðilega ættu reglurnar gilda á sama hátt í öllum aðildarríkjum. Hins vegar er munur á útfærslum þar sem sum aðildarríkin veita leiðbeiningar um hvernig beita á meginreglum við tilteknar aðstæður (til dæmis viðskiptaleg sýni og skil á vörum). Þessar leiðbeiningar geta valdið mismunandi árangri við ýmsar aðstæður. Þess vegna verður að færa inn upplýsingar sem lönd/svæði verða að vera mismunandi eftir og getur skráarsniðið sem þær verða að nota við skýrslugerð.

### <a name="austria"></a>Austurríki

Intrastat skýrslugerð í Austurríki þarf tvær aðrar skrár fyrir innhreyfingar og afhendingar. Fylgdu þessum skrefum til að sannprófa að uppsetningin sé rétt.

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **Intrastat-skýrsluuppsetningu** og velja síðan tengda tengilinn.  
2.  **Á flipanum skýrslugjöf**  er athugað hvort  **skiptar móttökur/afhendingar**  séu valdar. Ef svo er, er að finna tvö aðskilin  **gagnaskilgr. def. Code**   gildi skilgreind. 
3. Staðfestið  **að reiturinn zip-skrá (-s)**  sé valinn til að sjá til þess að skýrsluskrám verði bætt við zip-skrána.

Vinna við Intrastat-skýrslur er sú sama og Altæk aðgerð.

<!-- ### Belgium-->

### <a name="czech-republic"></a>Tékkland

Ný reynsla Intrastat-skýrslna fyrir Tékklands verður í boði í 2023 útgáfu bylgjunnar 1. Í millitíðinni er haldið áfram að nota  **aðgerðina intrastatbók** .

### <a name="finland"></a>Finnlandi

Í Finnlandi eru nokkur Viðbótarskref til að setja upp Intrastat. Intrastat skýrslugerð í Finnlandi þarf tvær aðrar skrár fyrir innhreyfingar og afhendingar. Einnig verður hægt að finna að það eru tvö aðskilin  **Gagnaexch. def-Code**  -gildi samskipuð.

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **Intrastat-skýrsluuppsetningu** og velja síðan tengda tengilinn.  
2.  **Á uppsetningarsíðu**  Intrastat-skýrslu, á  **fastflipanum skrár**, skal færa inn svæðisupplýsingarnar eins og lýst er í eftirfarandi töflu.

    |                 Svæði              |            Heimildasamstæða                |  
    |------------------------------------|---------------------------------------|
    | **Sérsniðinn Kóði** | Tilgreinir sérsniðinn kóða fyrir uppsetningarupplýsingar Intrastat-skrár. |
    | **Fyrirtæki raðnr.** | Tilgreinir raðnúmer fyrirtækis fyrir upplýsingar um uppsetningu Intrastat-skrár. |

3.  **Á flipanum skýrslugjöf**  er athugað hvort  **skiptar móttökur/afhendingar**  séu valdar.

Vinna við Intrastat-skýrslur er sú sama og Altæk aðgerð.

<!-- ### Germany-->

### <a name="italy"></a>Ítalíu

Ný reynsla Intrastat-skýrslna fyrir Ítalíu verður í boði sem hefst í febrúar 2023. Í tæka tíð skal halda áfram að nota  **aðgerðina intrastatbók** .

<!-- ### France-->

### <a name="sweden"></a>Svíþjóð

Intrastat-skýrsla í Svíþjóð þarfnast tveggja ólíkra skráa fyrir innhreyfingar og afhendingar. Fylgdu þessum skrefum til að sannprófa að uppsetningin sé rétt.

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **Intrastat-skýrsluuppsetningu** og velja síðan tengda tengilinn.  
2.  **Á flipanum skýrslugjöf**  er staðfest að  **skiptar móttökur/sendingar**  séu valdar. Ef svo er, er að finna tvö aðskilin  **gagnaskilgr. def. Code**  gildi skilgreind.

Ferlið við að vinna með Intrastat-skýrslur er það sama og í altækum aðgerðum.

<!-- ### United Kingdom-->

## <a name="see-also"></a>Sjá einnig .

[Intrastat-skýrslugerð í Business Central](finance-how-report-intrastat.md)  
[Fjármálastjórnun](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
