---
title: Kynning - Stýring verkefna með verkum
description: Þessi kynning sýnir eiginleika verkefnastjórnunar í verkum sem gera þér kleift að áætla notkun á forðum fyrirtækisins og fleira.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="walkthrough-managing-projects-with-jobs" />Kynning: Stýring verkefna með verkum

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Þessi kynning kynnir verkstýringareiginleikana í verkum. Verk eru leiðir fyrir áætlunargerð um notkun á forða fyrirtækisins og rakningu á ýmsum kostnaði sem fylgir notkun forða í tilteknu verkefni. Verk ná yfir notkun á vinnutíma starfsmanna, vélastundir, birgðahluti og aðrar gerðir notkunar sem notandinn kann að vilja fylgjast með í verkferlum.  

 Kynningin nær til uppsetningar nýs verks og einnig til nokkurra algengari verkefna eins og að meðhöndlun á föstu verði, framkvæmd greiðslu með inngreiðslu, bókun sölureikninga vinnu og afritun.  

## <a name="about-this-walkthrough" />Um kynninguna

 Þessi kynning fjallar um eftirfarandi verk:  

### <a name="setting-up-a-job" />Uppsetning vinnu

 Það er mjög einfalt að stofna verk með uppsetningu skipulagningar áætlunar fyrir verk. Þessi kynning fer yfir eftirfarandi atriði:  

- Hvernig setja skal upp verkhlutalínur og áætlunarlínur.  
- Stofna tiltekið verð fyrir vörur, forða og fjárhagsreikninga.  
- Reikningsfærslu fyrir verk.  

### <a name="handling-fixed-prices" />Unnið með fast verð

 Í verkum má meðhöndla fast verð og verð fyrir þjónustu eða vörur sem er fyrirfram samþykkt við viðskiptavini. Í þessari kynningu er hægt að gera eftirfarandi:  

- Sjá hvernig samningsbundnar - og reikningsupphæðir eru ákveðnar.  
- Gera ráð fyrir viðbótarvinnu í áætluninni sem hefur ekki verið reikningsfærð.  

### <a name="copying-a-job" />Afritun verks

 Þetta dæmi sýnir hvernig á að afrita hluta eða allt verk pöntunar til að draga úr handvirkum innslætti gagna og auka á nákvæmni. Þar á meðal eftirfarandi:  

- Afritun hluta af verki í nýtt verk.  
- Afritun verðs fyrir sérstakt verk.  
- Afritun áætlunarlína.  

### <a name="making-payment-by-installment" />Framkvæma greiðslu með inngreiðslu

 Þegar stór kostnaðarsöm verk vara í langan tíma, gerir viðskiptavinurinn oft samkomulag við fyrirtækið um að greiða með inngreiðslum. Þetta dæmi sýnir hvernig greiðslur með inngreiðslum eru meðhöndlaðar og tekur til:  

- Stofna greiðslu með inngreiðslu fyrir verk.  
- Reikningsfærslu greiðslna til viðskiptavina.  
- Bókhald til notkunar í verki sem er hannað fyrir greiðslu með inngreiðslu.  

## <a name="roles" />Hlutverk

 Þessi kynning nær yfir verk fyrir eftirfarandi hlutverk:  

- Verkefnastjóri  
- Meðlimur verkefnateymis  

## <a name="prerequisites" />Frumskilyrði

 Áður en hægt er að framkvæma verk hér í kynningunni þarf að gera eftirfarandi:  

- Setja upp CRONUS sýnigagnagrunn.
- Stofna nokkur sett sýnigagna með því að nota skrefin sem koma hér á eftir.  

## <a name="story" />Ferill

Þessi kynning einblínir á fyrirtækið CRONUS, hönnunar- og ráðgjafafyrirtæki sem hannar og setur upp húsgögn, aukahluti og geymslueiningar (t.d. í fundarsölum og skrifstofum). Mest af vinnunni er verkefnatengd. Prakash, verkefnastjóri hjá  CRONUS  nýtist störfum til að fá yfirsýn yfir hvert áframhaldandi starf sem  CRONUS  hefur hafist, auk þeirra verka sem lokið er við. Prakash er yfirleitt sá sem setur upp tilboð hjá viðskiptavinum og slær inn kjarna vinnslunnar, sem er verkefna-og áætlunarlína auk verðs, inn á við [!INCLUDE[prod_short](includes/prod_short.md)]. Prakash finnur að skapa, viðhalda og endurskoða upplýsingar er einfalt. Petra kann einnig vel hvernig verk eru afrituð og inngreiðslur í [!INCLUDE[prod_short](includes/prod_short.md)].

 Trausti, meðlimur í verkefnateymi sem heyrir undir Petru, ber ábyrgð á verkinu og fylgjast með. Tricia slær eigin verk til viðbótar við þá vinnu sem unnin er af tæknimönnum á hvert verk, skráir inn vörur sem þeir hafa notað og þann kostnað sem þeir hafa fallið í.  

## <a name="preparing-sample-data" />Undirbúa sýnigögn

 Til undirbúnings fyrir þessa kynningu þarf að bæta Tinnu við sem nýjum tilföngum.  

### <a name="to-prepare-the-sample-data" />Til að undirbúa sýnigögnin

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tilföng** og velja síðan viðkomandi tengil.  
2.  Veljið aðgerðina **Nýtt** til að Búa til nýtt forðaspjald.  
3.  Á flýtiflipanum **Almennt** eru eftirfarandi upplýsingar slegnar inn:  

    - **Nr.**: **Trausti**  
    - **Nafn**: **Trausti**  
    - **Gerð**: **Einstaklingur**  

4.  Velja reitinn **Grunnmælieining**, og velja **Nýtt** aðgerð til að opna síðuna **Mælieining forða**. Í reitnum **Kóti** skal velja **Klukkustund**.  
5.  Á flýtiflipanum **Reikningsfæra** eru eftirfarandi upplýsingar slegnar inn:  

    - **Innkaupsverð**: **5**  
    - **Óbeinn kostnaður í %**: **4**  
    - **Kostnaðarverð**:**10**  
    - **Alm. vörubókunarflokkur**: **Þjónusta**  
    - **VSK vörubókunarflokkur**: **VSK 25**  

6. Lokaðu síðunni.

Í næstu aðferð er hægt að stofna verkbókarkeyrslu fyrir Tricia til að bóka notkun þeirra.  

### <a name="to-create-a-job-journal-batch" />Til að búa til verkbókarkeyrslu

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkbækur** og velja síðan viðkomandi tengil.  
2.  Á síðunni **Verkbók** veljið reitinn **Heiti keyrslu**. Síðan **Bókarkeyrsla verks** opnast.  
3.  Veljið aðgerðina **Nýtt** til að Búa til nýtt Ný lína er stofnuð með eftirfarandi upplýsingum  

    - **Nafn**: **Trausti**  
    - **Lýsing**: **Trausti**  
    - **Númeraröð**: **JJNL-GEN**  

4.  Velja hnappinn **Í lagi** til að vista breytingarnar.

## <a name="setting-up-a-job-1" />Uppsetning vinnu

 Í þessu dæmi hefur CRONUS náð samningum við viðskiptamann, Progressive Home Furnishings, um að hanna fundar- og matsal þeirra. Viðskiptamaðurinn er staðsettur í Bandaríkjunum og verkefnið krefst sérstaks hugbúnaðar. Verkefnastjóri nær samkomulagi við viðskiptamanninn og stofnar verk sem nær yfir samkomulagið.  

### <a name="to-set-up-a-job" />Uppsetning verks

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk** og velja síðan viðkomandi tengil.  
2.  Veljið aðgerðina **Nýtt** til að Búa til nýtt spjald.  
3.  Á flýtiflipanum **Almennt** eru eftirfarandi upplýsingar slegnar inn:  

    - **Lýsing**: **Ráðgjöf við uppsetningu fundarsals**  
    - **Reikningsfærist á viðskiptamenn Nr.**: **01445544**  

4.  Á flýtiflipanum **bókun** eru eftirfarandi upplýsingar slegnar inn:  

    - **Staða**: **Áætlun**  
    - **Bókunarflokkur verka**: **Uppsetning**  
    - **VÍV-aðferð**: **Kostnaðarvirði**  

5.  Á flýtiflipanum **Tímalengd** er slegin inn dagsetning dagsins í dag í reitina **Upphafsdagur** og **Lokadagur**. Þessar dagsetningar verða notaðar við umreikning gjaldmiðla þegar verkið er reikningsfært.  
6.  Á flýtiflipanum **Erlent** skal stilla gjaldmiðilskótann á **USD**. Sé USD valið í reitnum **Gjaldmiðilskóti reiknings** mun verkið verða reikningsfært í Bandaríkjadölum og áætlað í staðbundnum gjaldmiðli CRONUS.  

 Hægt er að sérsníða verð fyrir viðskiptavini á hvert verk, eftir þeim samningum sem settir hafa verið fram. Í næsta ferli tilgreinir verkefnastjórinn verð viðkomandi tíma, stillir verð fyrir þann hugbúnað sem nauðsynlegur er og bætir við ferðakostnaði sem viðkomandi hefur samþykkt að greiða.  

### <a name="to-customize-pricing" />Til að sérsníða verðlagningu

1.  Á verkspjaldinu skal velja **Forði** aðgerðina.  
2.  Á síðunni **Forðaverð verks** eru eftirfarandi upplýsingar slegnar inn:  

    - **Kóti**: **Trausti**  
    - **Einingarverð**: **20**  

3.  Lokaðu síðunni.  
4.  Velja aðgerðina **Vara**.  
5.  Á síðunni **Verð vöru** eru eftirfarandi upplýsingar slegnar inn og sérsniðið verð:  

    1.  **Vörunr.**: **80201 (teikniforrit)**  
    2.  **Einingarverð**: **200**  

6.  Lokaðu síðunni.  
7.  Veldu aðgerðina **Fjárhagsreikningur**.  
8.  Á síðunni **Fjárhagsreikningsverð verks** færið inn eftirfarandi upplýsingar og ferðakostnað, sem viðskiptavinur hefur samþykkt að greiða kostnaði og að auki 25 prósent:  

    1.  **Fjárhagsreikningur**: **8430 (Ferðir)**  
    2.  **Stuðull einingaverðs**:**1,25**  

9. Lokaðu síðunni.  

 Síðustu skrefin í uppsetningu verks eru að bæta við verkhlutana og áætlunarlínurnar sem eru hluti af hverju verki. Áætlunarlínurnar ákvarða hvað er reikningsfært á viðskiptamanninn.  

### <a name="to-add-job-tasks" />Til að bæta við verkhlutum

1.  Á spjaldinu **Verk** fyrir nýja verkið skal velja aðgerðina **Verkhlutalínur**.  
2.  Eftirfarandi tafla lýsir upplýsingunum sem ætti að færa inn í reitina.  

    |Verkhluta nr.|Description|Tegund verkhluta|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Ráðgjöf við uppsetningu á sal|Frá-tala|  
    |1010|Ráðgefandi fundir með viðskiptavini|Bókun|  
    |1020|Þróun|Bókun|  
    |1090|Ráðgjöf alls|Til-tala|  

3.  Til að sýna að ákveðin verk séu undirflokkar annarra verka er flipinn **Draga inn verkhluta verks** valinn.  

 Áætlunarlína getur verið ein af eftirfarandi tegundum:  

- **Áætlun**: Bætt við áætlun en ekki reikningsfært.  
- **Reikningshæft**: Reikningsfærður, en ekki bætt við áætlunina.  
- **Bæði fjárhagsáætlun og reikningshæft**: Reikningsfært og bætt við áætlunina.  

 Í þessari kynningu. notar verkefnastjórinn **Bæði fjárhagsáætlun og reikningshæft**. Þau útbúa þrjár áætlunarlínur fyrir verkefni 1010, og tvær áætlunarlínur fyrir verkefni 1020.  

### <a name="to-create-planning-lines" />Til að stofna áætlunarlínur

1. Veljið línu 1010 og veljið svo aðgerðina **Verkáætlunarlínur**.  

2. Stofna áætlunarlínur með eftirfarandi upplýsingum:  

    | Lína | Línugerð | Áætlunardagsetning  | Tegund        | Fj.   | Magn | Einingarverð |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Bæði fjárhagsáætlun og reikningshæft | (dagurinn í dag) | Forði | Tinna | 40        |     |
    | 2    | Bæði fjárhagsáætlun og reikningshæft | (dagurinn í dag) | Forði | Elvar | 40        |     |
    | 3    | Bæði fjárhagsáætlun og reikningshæft | (dagurinn í dag) | Fjárhagur | 8430 (ferðalög) | 2 | 400    |

     Lokaðu síðunni. Samtölurnar eru uppfærðar á síðunni **Verkhlutalínur verks**.  
3. Veljið línu 1020 og veljið svo aðgerðina **Verkáætlunarlínur**. Eftirfarandi upplýsingar eru færðar inn:  

    | Lína | Línugerð | Áætlunardagsetning  | Tegund        | Fj.   | Magn | Einingarverð |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Bæði fjárhagsáætlun og reikningshæft | (dagurinn í dag) | Forði | Tinna | 80        |     |
    | 2    | Bæði fjárhagsáætlun og reikningshæft | (dagurinn í dag) | Vara | 80201 (Myndvinnsluforrit) | 1 |     |

4. Lokaðu síðunni. Samtölur eru uppfærðar á síðunni **Verkhlutalínur verks**.  

## <a name="calculating-remaining-usage" />Útreikningur á notuðum eftirstöðvum

 Tricia, verkefnastjóri Team, hefur unnið að verkinu um hríð og vill skrá tímana sína og notkun á starfinu. Tricia hefur ekki unnið fleiri klukkustundir en samið var um við viðskiptavininn fyrirfram. Tricia notar  **keyrsluna Reikna eftirstandandi notkunarleyfi**  til að reikna eftirstandandi notkun fyrir vinnsluna í verkbók. Keyrslan reiknar út, fyrir hvert verk, mismuninn milli áætlaðrar notkunar vöru, forða og fjárhagsútgjalda, og notkunar í raun samkvæmt bókuðum verkbókarfærslum. Eftirstandandi notkun er síðan sýnd í verkbókinni, og má bóka hana þaðan.  

### <a name="to-calculate-remaining-usage" />Eftirstöðvar notkunar reiknaðar

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkbækur** og velja síðan viðkomandi tengil.  
2.  Á síðunni **Verkbók** í reitnum **Heiti keyrslu** er listinn **Verkbókarkeyrslur** opnaður. Velja skal verkbókarkeyrsluna **Trausti**.  
3.  Veljið aðgerðina **Reikna eftirstandandi notkun**.  
4.  Á síðunni **Verk - Reikna eftirstandandi notkun** á flýtiflipanum **Verkhluti** veljið reitinn **Verk nr.** og veljið viðeigandi verknúmer, yfirleitt verk J 00010.  
5.  Á flýtiflipanum **Valkostir** er **J00001** slegið inn í reitinn **Númer fylgiskjals**. Þetta gerir rakningu bókunar auðveldari á síðari stigum.  
6.  Færið inn daginn í dag sem bókunardagsetninguna.  
7.  Velja hnappinn **Í lagi**. Þetta myndar verkbókarlínurnar sem leiddar eru af áætlunarlínum sem Petra stofnaði fyrir Verkbókina.  
8.  Veldu hnappinn **Í lagi** á staðfestingarsíðunni. Mynduðum línum er bætt við verkbók.  
9. Ganga þarf úr skugga um að öll skjöl séu númeruð J00001 og velja svo **Bóka** aðgerðina. Velja **Já** til að staðfesta bókun.  

Línurnar eru bókaðar.  

## <a name="creating-and-posting-a-job-sales-invoice" />Reikningur verksölu stofnaður og bókaður

 Næst skal Trausti stofna nýjan reikning fyrir allt verkið eða fyrir hluta af verkinu. Tricia getur einnig tengt reikninginn við annan reikning sama viðskiptavinar fyrir sama starf. Þar er um að ræða Tricia reikninga fyrir allt verkið, þar sem verkefninu er nú lokið.  

### <a name="to-create-a-job-sales-invoice" />Stofnun reiknings fyrir verksölu

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk** og velja síðan viðkomandi tengil.  
2.  Veljið verkið sem var stofnað áður og veljið því næst **Stofna verksölureikningur** aðgerðina.  
3.  Á flýtiflipanum **Verkhluti verks**, skal hreinsa hverja þá afmörkun á **Verkhlutanr. verks** til að reikningsfæra verkið. Í reitnum **Verk nr.** er viðeigandi verk valið.  
4.  Í flipanum  **Valkostir** er bókunardagsetningin færð inn og skilgreint hvort stofna eigi einn reikning fyrir hvert verk eða einn fyrir öll verk.  
5.  Velja hnappinn **Í lagi** til að stofna reikninginn og velja svo **Í lagi** á staðfestingarsíðunni.  

 Eftir að reikningurinn hefur verið stofnaður getur Tricia opnað hann í  **hlutverkamiðstöð sölupöntunar**, td. 

### <a name="to-post-a-new-sales-invoice" />Nýr sölureikningur bókaður

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölureikningar** og velja síðan viðkomandi tengil.  
2.  Reikningur er valinn fyrir viðskiptamann Nr. 01445544. Sjá má upplýsingarnar sem slegnar voru inn frá áætlunarlínunum.  
3.  Valið er **Bóka** aðgerðin. Velja **Já** til að staðfesta bókun.  

### <a name="to-view-the-posted-invoice" />Bókaðir reikningar skoðaðir

1.  Opnið verkið og veljið svo aðgerðina **Verkáætlunarlínur**.  
2.  Veljið einhverja af áætlunarlínunum hafa verið reikningsfærðar og veljið síðan **Sölureikningar/kreditreikningar** aðgerðina.
3. Á síðunni **Verkreikningar** skal velja aðgerðina **Opna sölureikning/kreditreikning**.  

 Tricia hefur spurningu um verð, kostnað og hagnað sem máli skiptir varðandi þetta tiltekna starf, svo Tricia aðgætir að upplýsingum á  **tölfræðisíðunni** .  

### <a name="to-open-the-statistics-page" />Tölfræðisíðan opnuð

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk** og velja síðan viðkomandi tengil.  
2.  Veldu **Upplýsingar** aðgerðina. Hægt er að fara yfir nákvæmar upplýsingar um verkkostnað, kostnað og hagnað í bæði innlendri og erlendri mynt.  
3.  Velja hnappinn **Loka** til að loka síðunni **Verkupplýsingar**.  

## <a name="handling-fixed-prices-1" />Unnið með fast verð

 CRONUS hefur tekið að sér að setja upp fundarsali. Verkefnastjórinn Petra þarf gott yfirlit yfir verkhluta verksins ásamt kostnaðaráætlun og kostnaði sem stofnað hefur verið til fyrir hvern verkhluta. Auk þess vill Prakash vita heildarverktakinn sem verð fyrir vinnsluna og upphæðina sem hefur verið reikningsfærð á þennan punkt. Þeir hafa náð samkomulagi við viðskiptavin varðandi fasta verðlagningu á vinnslunni.  

### <a name="to-manage-fixed-pricing-in-jobs" />Föstu verði verka stýrt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk** og velja síðan viðkomandi tengil.  
2. **Guildford** verknúmerið er valið og svo er valin **Verkhlutalínur verks** aðgerðina.  
3. Lína 1120 er valin og í reitnum **Fjárhagsáætlun (heildarkostnaður)** er hægrismellt á upphæðina og valið **Köfun**.  

     Með því að skoða Verkáætlunarlínurnar er ákveðið að Prakash þurfi einnig að hafa Tricia fyrir 30 klukkustundum fyrir þetta stig verksins. Prakash samþykkir á föstu verði með viðskiptavininum.  

4. Á síðunni **Verkhlutalínur** veljið línu 1120 og veljið svo aðgerðina **Verkáætlunarlínur**. Stofna áætlunarlínu með eftirfarandi upplýsingum:  

    | Lína | Línugerð | Tegund        | Fj.   | Magn |
    |------|-----------|-------------|-------|----------|
    | 1    | Bæði fjárhagsáætlun og reikningshæft  | Forði | Tinna | 30 |

     Lokaðu síðunni.  
5. Í reitnum **Fjárhagsáætlun (heildarkostnaður)**, hægrismella á reitinn og velja **KafaNiður** aftur á síðunni **Verkhlutalínur verks**. Skoða breytingarnar á tímasetningunni. Sjá má að 30 klukkustundum hefur verið bætt við tímasetninguna.  
6. Loka síðunum.  

Þegar þú hefur bætt við áætlun fyrir þessa verklínu, vinnur Tricia verk 25 klukkustundir í verkinu, og færir Þessar stundir inn í verkbókina.  

### <a name="to-enter-hours-in-the-job-journal" />Tímum bætt í Verkbókina

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkbækur** og velja síðan viðkomandi tengil.  
2. Eftirfarandi upplýsingar eru slegnar inn á nýja línu:  

    - **Tegund línu**: **(autt)**  
    - **Dagsetning bókunar**: **(dagurinn í dag)**  
    - **Númer fylgiskjals**: **J00002**  
    - **Verk Nr.**: **Guildford**  
    - **Verkhlutanr.**: **1120**  
    - **Gerð**: **Forði**  
    - **Nr.**: **Trausti**  
    - **Magn**: **25**  

3. Valið er **Bóka** aðgerðin.  

     Nokkrum dögum síðar vinnur Tricia annan 10 tíma á starfinu, og hefur nú unnið 35 tíma í allt. Þar sem samningurinn er fyrir 30 tíma við viðskiptavininn munu aðeins fimm þessara tíma vera færðir á viðskiptavininn. Tricia bætir handvirkt við fimm klukkustunda vinna við áætlunina.  

4. Á síðunni **Verkbók** veljið aðgerðina **Reikna eftirstandandi notkun**.  
5. Á síðunni **Reiknaðar eftirstöðvar notkunar verks** á flýtiflipanum **Valkostir** þarf að færa inn eftirfarandi upplýsingar:  

    - **Númer fylgiskjals**: **J00003**  
    - **Dagsetning bókunar**: **(dagurinn í dag)**  

6. Eftirfarandi upplýsingar eru færðar inn á flýtiflipanum **Verkhluti verks**:  

    - **Verk Nr.**: **Guildford**  
    - **Verkhlutanr.**: **1120**  

7. Velja hnappinn **Í lagi** til að keyra útreikninginn.

    Fimm vinnustundir eru eftir fyrir Tinnu. Reiturinn **Línugerð** er auður sem gefur til kynna að tímarnir verða bókaðir vegna þess að vinnan hefur þegar farið fram.  

8. Í glugganum **Verkbókakeyrslur** er ný lína stofnuð með eftirfarandi upplýsingum. Ganga þarf úr skugga um að bæði verknúmer séu í réttri númeraröð miðað við þau sem þegar hafa verið notuð:  

    - **Línugerð**: **Áætlun**  
    - **Verk Nr.**: **Guildford**  
    - **Verkhlutanr.**: **1120**  
    - **Gerð**: **Forði**  
    - **Nr.**: **Trausti**  
    - **Magn**: **5**  

     Með því að nota línugerðina **Áætlun** uppfærir kerfið áætlaðan kostnað og verð án uppfærslu samningskostnaðar og verðs sem er reikningsfært á viðskiptamanninn.  

9. Valið er **Bóka** aðgerðin. Velja hnappinn **Í lagi** til að loka síðunni.  
10. Listinn **Verk** er opnaður.  
11. Veljið GUILDFORD-verkið og síðan í hlutanum **Verklínur verks** skal velja línu 1120 og í reitnum **Fjárhagsáætlun (heildarkostnaður)** skal hægrismella á upphæðina. **Köfun** er valin til að skoða upplýsingarnar.  

     Sjá má að breytingarnar færast sjálfkrafa inn í línuna fyrir Verkhlutanúmer 1120. Í heildarkostnað áætlaðrar vinnu, fimm öðrum tíma viðbótartímar Trausta hefur verið bætt við tímasetninguna.  

12. Velja hnappinn **Loka** til að loka síðunni.  
13. Hægrismella skal á upphæðina í reitnum **Samningur (heildarkostnaður)** og velja **KafaNiður** til að skoða upplýsingarnar.  

Í heildarverði samnings koma aðeins fram hinir upphaflegu 30 tímar sem voru innifaldir í verkinu vegna þess að um það var samið við viðskiptamanninn.  

## <a name="copying-jobs" />Verk afrituð

Petra hefur náð samkomulagi við viðskiptamann, Selagorian hf, um að setja upp 10 fundarsali. Samningurinn er svipaður eldri verkum. Þess vegna mun spara tíma að afrita fyrra verkið.  

Á síðunni **Afrita verk** er hægt að velja verkið og verklínurnar sem á að afrita. Einnig er hægt að velja að afrita eignafærslu upprunalega verksins, sem stofnar áætlunarlínur á grundvelli raunverulegrar notkunar og hægt er að afrita áætlunarlínu upprunalega verksins, sem afritar upprunalegar áætlunarlínur yfir í nýja verkið. Síðan er hægt að velja þá tegund áætlunarlínu eða eignafærslulínu sem á að hafa með og velja aðeins það sem á við í þessu nýja verki. Að lokum er hægt að velja verkið sem á að afrita í og tilgreina hvort afrita eigi verð og magn einnig.  

### <a name="to-copy-a-job" />Verk afritað

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Nýtt** til að Búa til nýtt verk. Eftirfarandi upplýsingar eru færðar inn:  

    - **Lýsing**: **Uppsetning tíu fundarsala**  
    - **Reikningsfærist á viðskiptamenn Nr.**: **20000**  

3. Velja aðgerðina **Afrita verkhluta verkhluta frá**.  
4. Á síðunni **Afrita verkhluta verks** færið inn eftirfarandi:  

    - **Verk Nr.**: **Guildford**  
    - **Verkhlutanr. frá**: **1000**  
    - **Uppruni**: **Áætlunarlínur verks**  
    - **Áætlunarlínutegund tekin með**: **Áætlun + Reikningshæft**  
    - **Í verk nr.**: **Guildford Uppsetning tíu fundarsala**  
    - Reitirnir **Afrita víddir** og **Afrita magn** eru valdir.  

5. Velja hnappinn **Í lagi** til að afrita verkið og velja svo **Í lagi** til að loka staðfestingarsíðunni.  

Með því að bera saman verð, verkhlutalínur og áætlunarlínur fyrir verkin tvö má sjá að það tókst að afrita upplýsingarnar.  

## <a name="making-payments-by-installments" />Framkvæma greiðslu með inngreiðslu

CRONUS hefur nýlega fengið stórt verkefni sem tekur um eitt ár að ljúka. Vegna þess hvað verkefnið þarfnast mikilla aðfanga setur verkefnastjórinn samninginn þannig upp, að farið er fram á að viðskiptamaðurinn borgi hluta af verðinu fyrirfram, hluta af verðinu þegar verkið er hálfnað og lokagreiðslu þegar því er lokið.  

### <a name="to-set-up-a-new-account" />Að setja upp nýjan reikning

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Á síðunni **Bókhaldslykill** skal velja aðgerðina **Nýtt** til að stofna nýtt spjald.  
3. Á spjaldið **Nýr fjárhagsreikningur** eru færðar inn eftirfarandi upplýsingar:  

    - **Nr.**: **40255**  
    - **Heiti**: **Greiðsla fyrir verk**  

4. Á flipanum **Bókun** er reiturinn **Alm. vörubókunarflokkur** fylltur út, velja **Þjónustur**. Lokaðu síðunni.  
5. Á síðunni **Bókhaldslykill** veljið **Nr. 40255 greiðsla fyrir verk** og svo aðgerðina **Inndráttur bókhaldslykill**. Veljið **Já** til staðfestingar.  

Eftirfarandi ferli sýnir hvernig eigi að stofna nýtt verk, stilla verðlagningu og síðan setja upp greiðslur með inngreiðslu. Í verkhlutalínu er hægt að stofna sérstakar línur fyrir greiðslur með inngreiðslum. Vinna sem lokið er við fyrir verkið sem er bætt við áætlunina eru færðar inn í notkunarlínurnar. Fyrir hverja greiðsluhlutalínu í áætlunarlínunum, er línugerðin **Rukkun**, sem þýðir að reikningur verður sendur til viðskiptamanns. Færð er inn ný lína fyrir útborgunina. Í notkunarverklínuna er hægt að færa inn upplýsingar um vörur og forða sem notuð voru í verkið, sem mun auka við áætlunina, t.d. vinnutíma starfsmanna og vörur sem notaðar voru í verkið.  

### <a name="to-make-a-payment-by-installment" />Framkvæma greiðslu með inngreiðslu

1. Nýtt verk er stofnað.  
2. Eftirfarandi upplýsingar eru færðar inn á nýja **Verk** spjaldinu:  

    - **Lýsing**: **Endurhönnun á móttöku**  
    - **Reikningsfærist á viðskiptamenn Nr.**: **30000**  
    - **Bókunarflokkur verka**: **Uppsetning**  
    - **VÍV-aðferð**: **Kostnaðarvirði**  

3. Á verkspjaldinu skal velja aðgerðina **Verk** og síðan velja aðgerðina **Tilfang**. Færi inn eftirfarandi upplýsingar:  

    - **Kóti**: **Trausti**  
    - **Einingarverð**: **10**  

     Lokaðu síðunni.  

4. Í spjaldinu **Verk**, í hlutanum **Verk**, skal bæta verkhlutalínum við eins og lýst er í eftirfarandi töflu:  

    | Lína | Númer verkhluta | Description          | Tegund verkhluta |
    |------|--------------|----------------------|---------------|
    | 1    | 1000         | Greiðsla - Útborgun | Bókun       |
    | 2    | 2000         | Notkun                | Bókun       |
    | 3    | 3 000         | Greiðsla - Hálfnað     | Bókun       |
    | 4    | 4000         | Greiðsla - Lokið | Bókun       |

5. Veljið verk 1000 og veljið svo aðgerðina **Verkáætlunarlínur**.  

6. Stofna áætlunarlínu með eftirfarandi upplýsingum:  

    | Lína | Línugerð | Áætlunardagsetning  | Tegund        | Fj.   | Magn | Einingarverð |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Rukkun  | (dagurinn í dag) | Fjárhagur | 40255 | 1        | 5000       |

     Lokaðu síðunni.  

7. Veljið verk 2000 og veljið svo aðgerðina **Verkáætlunarlínur**.  

8. Stofna áætlunarlínu með eftirfarandi upplýsingum:

    | Lína | Línugerð | Áætlunardagsetning  | Tegund     | Fj.    | Magn |
    |------|-----------|----------------|----------|--------|----------|
    | 1    | Fjárhagsáætlun    | (dagurinn í dag) | Forði | Tinna | 120      |
    | 2    | Fjárhagsáætlun    | (dagurinn í dag) | Vara     | 70104  | 10       |

     Lokaðu síðunni. Á síðunni **Verkhlutalínur** er hægt að skoða áætlaðar upphæðir sem voru uppfærðar.  

9. Veljið verk 32000 og veljið svo aðgerðina **Verkáætlunarlínur**.  

10. Stofna áætlunarlínu með eftirfarandi upplýsingum:

    | Lína | Línugerð | Áætlunardagsetning   | Tegund        | Fj.   | Magn | Einingarverð |
    |------|-----------|-----------------|-------------|-------|----------|------------|
    | 1    | Rukkun  | (dagsetning í framtíðinni) | Fjárhagur | 40255 | 1        | 5000       |

     Lokaðu síðunni.  

11. Stofna svipaða áætlunarlínufærslu fyrir verkhluta 4000.  

 Nú þegar verk- og áætlunarlínurnar eru útfylltar býr Petra til reikning fyrir fyrstu greiðsluna. Prakash gerir þetta úr verkverkslínunum til að ganga úr skugga um að reikningurinn innihaldi aðeins línurnar fyrir fyrstu greiðsluna. Hægt er að opna sölupöntunina úr áætlunarlínunum eða verklínunum.  

### <a name="to-create-an-invoice" />Til að stofna reikning

1.  Á síðunni **Verkhlutalínur** veljið línu 1000 og veljið svo aðgerðina **Stofna sölureikninga**.  
2.  Á síðunni **Stofna sölureikning** stillið dagsetninguna í dag sem bókunardagsetning, tilgreinið **Fyrir hvert verk**, og veljið hnappinn **Í lagi** til að búa til reikning með sjálfgefnum upplýsingum. Velja hnappinn **Í lagi** til að loka staðfestingarsíðunni.  
3.  Velja aðgerðina **Sölureikningur/kreditreikningur**. Á sölureikningnum sést að einungis útborgunin er innifalin í reikningnum. Nú má senda reikninginn til viðskiptamannsins eins og samið var um.  

## <a name="next-steps" />Næstu þrep

 Í kynningunni var farið yfir grunnskrefin í að vinna með verk í [!INCLUDE[prod_short](includes/prod_short.md)]. Aflað hefur verið þekkingar um hvernig á að stofna nýtt verk, hvernig afrita á verk og hvernig á að meðhöndla greiðslur. Einnig hefur gefist færi á að skoða sýning á því hvernig fylgst er með vinnustundum og reikninga stofnaðir.  

## <a name="see-related-microsoft-training" />Sjá tengda [Microsoft þjálfun](/training/paths/create-jobs/)

## <a name="see-also" />Sjá einnig .

 [Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  
 [Setja upp verkefnastjórnun](projects-setup-projects.md)  
 [Notkun tilfanga](projects-how-use-resources.md)  
 [Fylgst með framvindu og afköstum](projects-how-monitor-progress-performance.md)  
 [Reikningsfærsla verka](projects-how-invoice-jobs.md)  
 [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
