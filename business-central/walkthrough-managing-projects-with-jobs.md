---
title: Kynning - Stýring verkefna með verkefnum
description: Þessi kynning kynnir aðgerðir verkefnastjórnunar til að tímasetja notkun á forða fyrirtækisins.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 05/30/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="walkthrough-managing-projects"></a>Kynning: stjórnun verkefna

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Þessi kynning kynnir aðgerðir verkefnastjórnunar. Verkefni eru leið til að tímasetja notkun á forða fyrirtækisins og fylgjast með ýmsum kostnaði sem tengist forðanum í tilteknu verkefni. Verkefni fela í sér notkun á vinnutíma starfsmanna, vélastundir, birgðavörur og aðrar gerðir notkunar sem ætlunin er að rekja sem verkferla.  

Þessi kynning fjallar um uppsetningu nýs verks og tengdra verka:

- Meðhöndla fasta verðlagningu
- Gera greiðslur í inngreiðslum
- Bóka reikninga úr verkum
- Afrita verk

## <a name="about-this-walkthrough"></a>Um kynninguna

 Þessi kynning fjallar um eftirfarandi verk:  

### <a name="setting-up-a-project"></a>Uppsetning verks

Þegar skipulag áætlunar er sett upp fyrir verk er einfalt að stofna verk. Þessi kynning fer yfir eftirfarandi atriði:  

- Setja upp verkhlutalínur og áætlunarlínur.  
- Stofna verktengt verð fyrir vörur, forða og fjárhagsreikninga.  
- Reikningsfæra viðskiptavini fyrir verkefni.  

### <a name="handling-fixed-prices"></a>Meðhöndlun fasts verðs

 Hægt er að meðhöndla fast verð og verð fyrir þjónustu eða vörur sem samið er um fyrirfram við viðskiptamenn. Í þessari kynningu lærirðu að:  

- Sjá hvernig samningsbundnar - og reikningsupphæðir eru ákveðnar.  
- Leyfa aukavinnu í áætluninni sem er ekki reikningsfærð.  

### <a name="copying-a-project"></a>Afritun verks

 Í þessum hluta kynningarinnar er lögð áhersla á hvernig afrita skuli hluta eða allt verkefni til að draga úr handvirkum innslætti gagna og auka nákvæmni.

- Afrita hluta verks í nýtt verk.  
- Afrita verð sem sértækt fyrir verk.  
- Afrita áætlunarlínur.  

### <a name="making-payment-by-installment"></a>Framkvæma greiðslu með inngreiðslu

 Þegar stór kostnaðarsöm verk vara í langan tíma, gerir viðskiptavinurinn oft samkomulag við fyrirtækið um að greiða með inngreiðslum. Þetta dæmi sýnir hvernig greiðslur með inngreiðslum eru meðhöndlaðar og tekur til:  

- Stofna greiðslu með inngreiðslum fyrir verk.  
- Reikningsfæra greiðslur til viðskiptamanna.  
- Lykill fyrir notkun í verki sem er sett upp fyrir greiðslur með inngreiðslum.  

## <a name="roles"></a>Hlutverk

 Þessi kynning nær yfir verk fyrir eftirfarandi hlutverk:  

- Verkefnastjóri  
- Meðlimur verkefnateymis  

## <a name="prerequisites"></a>Frumskilyrði

 Áður en hægt er að framkvæma verkin í kynningunni þarf að:  

- Setja upp CRONUS sýnigagnagrunn.
- Stofna nokkur sett sýnigagna með því að nota skrefin sem koma hér á eftir.  

## <a name="story"></a>Ferill

Kynningin fjallar um CRONUS, sem er skáldskapur og ráðgjafafyrirtæki sem hannar og passar við ný innra skipulag. Til dæmis fundarsalir og skrifstofur með húsgögnum, fylgihlutum og geymslueiningum. Mest af vinnunni er verkefnatengd. Petra, verkefnastjóri hjá Verkefnum notar CRONUS verkefni til að fá yfirlit yfir hvert verk sem er í gangi og CRONUS lauk. Petra er yfirleitt sá sem sér um viðskiptamenn og færir inn kjarna verkefnisins, sem er verk- og áætlunarlínur auk verðs, inn í [!INCLUDE[prod_short](includes/prod_short.md)]. Petra finnur að stofnun, viðhald og yfirferð upplýsinga er einfalt. Petra er líka hrifin af því hvernig [!INCLUDE[prod_short](includes/prod_short.md)] gerir afritun verka og greiðslna með inngreiðslum.

 Trausti, meðlimur verkefnateymis sem heyrir undir Petru, ber ábyrgð á eftirliti með verkefninu daglega. Tinna færir inn það verk sem tæknimenn vinna við hvert verk, skráir vörurnar sem þeir notuðu og kostnaðinn sem þeir urðu til.  

## <a name="preparing-sample-data"></a>Undirbúningur sýnigagna

Til að undirbúa kynninguna þarf að bæta Trausta við sem forða.  

### <a name="to-prepare-the-sample-data"></a>Til að undirbúa sýnigögnin

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tilföng** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Nýtt** til að Búa til nýtt forðaspjald.  
3. Á flýtiflipanum **Almennt** eru eftirfarandi upplýsingar slegnar inn:  

    - **Nr.**: **Trausti**  
    - **Nafn**: **Trausti**  
    - **Gerð**: **Einstaklingur**  

4. Velja reitinn **Grunnmælieining**, og velja **Nýtt** aðgerð til að opna síðuna **Mælieining forða**. Í reitnum **Kóti** skal velja **Klukkustund**.  
5. Á flýtiflipanum **Reikningsfæra** eru eftirfarandi upplýsingar slegnar inn:  

    - **Innkaupsverð**: **5**  
    - **Óbeinn kostnaður í %**: **4**  
    - **Kostnaðarverð**:**10**  
    - **Alm. vörubókunarflokkur**: **Þjónusta**  
    - **VSK vörubókunarflokkur**: **VSK 25**  

6. Loka síðunni.

Í næsta ferli er stofnuð verkbókarkeyrsla fyrir Trausta til að bóka notkun þeirra.  

### <a name="to-create-a-project-journal-batch"></a>Til að stofna verkbókarkeyrslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **verkbækur** og velja síðan viðeigandi tengil.  
2. Á síðunni **Verkbók** skal velja reitinn **Heiti** keyrslu. Síðan **Verkbókarkeyrslur** opnast.  
3. Veljið aðgerðina **Nýtt** til að Búa til nýtt Ný lína er stofnuð með eftirfarandi upplýsingum  

    - **Nafn**: **Trausti**  
    - **Lýsing**: **Trausti**  
    - **Númeraröð**: **JJNL-GEN**  

4. Hnappurinn Í lagi **er** valinn til að vista breytingarnar.

## <a name="setting-up-a-project-1"></a>Uppsetning verks

Í þessu dæmi CRONUS , vann samning við viðskiptamann, Progressive Home Furnishings, um að hanna fundar- og matsal. Viðskiptamaðurinn er staðsettur í Bandaríkjunum og verkefnið krefst sérstaks hugbúnaðar. Verkefnastjórinn nær samkomulagi við viðskiptavininn og stofnar verkefni sem nær yfir samkomulagið.  

### <a name="to-set-up-a-project"></a>Til að setja upp verk

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.  
2. Veljið aðgerðina **Nýtt** til að Búa til nýtt spjald.  
3. Á flýtiflipanum **Almennt** eru eftirfarandi upplýsingar slegnar inn:  

    - **Lýsing**: **Ráðgjöf við uppsetningu fundarsals**  
    - **Reikningsfærist á viðskiptamenn Nr.**: **01445544**  

4. Á flýtiflipanum **bókun** eru eftirfarandi upplýsingar slegnar inn:  

    - **Staða**: **Áætlun**  
    - **Bókunarflokkur verkefnis**: **Uppsetning**  
    - **VÍV-aðferð**: **Kostnaðarvirði**  

5. Á flýtiflipanum **Tímalengd** er slegin inn dagsetning dagsins í dag í reitina **Upphafsdagur** og **Lokadagur**. Þessar dagsetningar hjálpa til við umreikning gjaldmiðla þegar verkið er reikningsfært.  
6. Á flýtiflipanum **Erlent** skal stilla gjaldmiðilskótann á **USD**. Ef USD er valið í reitnum **Gjaldmiðilskóti** reiknings er verkið reikningsfært í Bandaríkjadölum og aðeins áætlað í staðarmynt CRONUS .  

 Hægt er að sérsníða verðlagningu viðskiptamanna eftir því hvaða samningar eru gerðir. Í næsta ferli tilgreinir verkefnastjórinn kostnað fyrir tíma Trausta, setur verð fyrir nauðsynlegan hugbúnað og bætir við ferðakostnaðinum sem viðskiptamaðurinn samþykkti að greiða.  

### <a name="to-customize-pricing"></a>Til að sérsníða verðlagningu

1.  **Á Verkspjaldinu** skal velja **forðaaðgerðina** .  
2. Á síðunni **Forðaverð verks eru** eftirfarandi upplýsingar slegnar inn:  

    - **Kóti**: **Trausti**  
    - **Einingarverð**: **20**  

3. Loka síðunni.  
4. Velja aðgerðina **Vara**.  
5. Á síðunni **Vöruverð verkefnis eru eftirfarandi upplýsingar færðar** inn og sérsniðið verð:  

    1. **Vörunr.**: **80201 (teikniforrit)**  
    2. **Einingarverð**: **200**  

6. Loka síðunni.  
7. Veldu aðgerðina **Fjárhagsreikningur**.  
8. Á síðunni **Verð fjárhagsreiknings verkefnis skal færa inn eftirfarandi upplýsingar og ferðakostnað, sem viðskiptamaðurinn samþykkti að greiða kostnað fyrir plús** 25 prósent:  

    1. **Fjárhagsreikningur**: **8430 (Ferðir)**  
    2. **Stuðull einingaverðs**:**1,25**  

9. Loka síðunni.  

 Lokaskrefin við uppsetningu verks eru að bæta við verkhlutunum og áætlunarlínunum sem eru hluti af hverju verki. Áætlunarlínurnar ákvarða hvað er reikningsfært á viðskiptamanninn.  

### <a name="to-add-project-tasks"></a>Til að bæta við verkhlutum

1.  **Á Verkspjaldi** nýja verksins skal velja aðgerðina **Verkhlutalínur verks** .  
2. Eftirfarandi tafla lýsir upplýsingunum sem ætti að færa inn í reitina.  

    |Nr. verkhluta verkefnis|Heimildasamstæða|Gerð verkhluta verkefnis|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Ráðgjöf við uppsetningu á sal|Byrja-Samtals|  
    |1010|Ráðgefandi fundir með viðskiptavini|Bókun|  
    |1020|Þróun|Bókun|  
    |1090|Ráðgjöf alls|Til-tala|  

3. Til að sýna að sum verk séu undirflokkar annarra verka skal velja aðgerðina **Inndráttur** verkhluta.  

Áætlunarlína getur verið ein af eftirfarandi tegundum:  

- **Áætlun**: Bætt við áætlun en ekki reikningsfært.  
- **Reikningshæft**: Reikningsfærður, en ekki bætt við áætlunina.  
- **Bæði fjárhagsáætlun og reikningshæft**: Reikningsfært og bætt við áætlunina.  

Í þessari kynningu. notar verkefnastjórinn **Bæði fjárhagsáætlun og reikningshæft**. Þær stofna þrjár áætlunarlínur fyrir verk 1010 og tvær áætlunarlínur fyrir verk 1020.  

### <a name="to-create-planning-lines"></a>Til að stofna áætlunarlínur

1. Veljið línu 1010 og veljið svo aðgerðina Áætlunarlínur **verkefnis** .  
2. Stofna áætlunarlínur með eftirfarandi upplýsingum:  

    | Lína | Línugerð | Áætlunardagsetning  | Tegund        | Fj.   | Magn | Einingarverð |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Bæði fjárhagsáætlun og reikningshæft | (dagurinn í dag) | Forði | Tinna | 40        |     |
    | 2    | Bæði fjárhagsáætlun og reikningshæft | (dagurinn í dag) | Forði | Elvar | 40        |     |
    | 3    | Bæði fjárhagsáætlun og reikningshæft | (dagurinn í dag) | Fjárhagur | 8430 (ferðalög) | 2 | 400    |

     Loka síðunni. Samtölurnar eru uppfærðar á síðunni **Verkhlutalínur verks** .  
3. Veljið línu 1020 og veljið svo aðgerðina Áætlunarlínur **verkefnis** . Eftirfarandi upplýsingar eru færðar inn:  

    | Línurit | Línugerð | Áætlunardagsetning  | Tegund        | Fj.   | Magn | Einingarverð |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Bæði fjárhagsáætlun og reikningshæft | (dagurinn í dag) | Forði | Tinna | 80        |     |
    | 2    | Bæði fjárhagsáætlun og reikningshæft | (dagurinn í dag) | Vara | 80201 (Myndvinnsluforrit) | 1 |     |

4. Loka síðunni. Samtölur eru uppfærðar á síðunni **Verkhlutalínur verks** .  

## <a name="calculating-remaining-usage"></a>Útreikningur eftirstöðvanotkunar

Trausti, meðlimur teymisverkefnisins, hefur um tíma unnið að verkefninu og vill skrá tíma þeirra og notkun. Trausti vann ekki fleiri klukkustundir en samið var um við viðskiptavininn fyrirfram. Tinna notar keyrsluna **Reikna eftirstandandi notkun** til að reikna eftirstandandi notkun í verkbók. Fyrir hvern verkhluta reiknar keyrslan mismuninn á milli áætlaðrar notkunar vöru, forða og fjárhagsútgjalda og raunverulegrar notkunar sem bókuð er í verkfærslum. Eftirstandandi notkun er síðan sýnd í verkbókinni og Tinna getur bókað hana.  

### <a name="to-calculate-remaining-usage"></a>Eftirstöðvar notkunar reiknaðar

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **verkbækur** og velja síðan viðeigandi tengil.  
2. Á síðunni **Verkbók** í reitnum **Heiti** keyrslu er listinn Keyrslur **verkbóka** opnaður. Valin er keyrslan Trausti **verkbók**.  
3. Veljið aðgerðina **Reikna eftirstandandi notkun**.  
4. Á síðunni **Reikna eftirstöðvar notkunar** verks á flýtiflipanum **Verkhluti** verks skal velja **Verknúmer.** Og velja viðeigandi verknúmer, yfirleitt verkefni J00010.  
5. Á flýtiflipanum **Valkostir** er **J00001** slegið inn í reitinn **Númer fylgiskjals**. Þessar upplýsingar gera rakningu bókunar auðveldari í framtíðinni.  
6. Færið inn daginn í dag sem bókunardagsetninguna.  
7. Velja hnappinn **Í lagi**. Þessi aðgerð myndar verkbókarlínur byggðar á áætlunarlínum sem Petra stofnaði.  
8. Veldu hnappinn **Í lagi** á staðfestingarsíðunni. Mynduðu línunum er bætt við verkbókina.  
9. Ganga þarf úr skugga um að öll skjöl séu númeruð J00001 og velja svo **Bóka** aðgerðina. Velja **Já** til að staðfesta bókun.  

Línurnar eru bókaðar.  

## <a name="creating-and-posting-a-project-sales-invoice"></a>Stofnun og bókun sölureiknings verks

Næst getur Trausti stofnað nýjan reikning fyrir allt verkefnið eða fyrir hluta af verkefni. Tinna getur einnig hengt reikninginn við annan reikning fyrir sama viðskiptavin fyrir sama verkefnið. Þá reikningsfærir Trausti fyrir allt verkefnið þar sem verkefninu er nú lokið.  

### <a name="to-create-a-project-sales-invoice"></a>Til að stofna sölureikning verks

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.  
2. Veljið verkið sem stofnað var og veljið svo aðgerðina Stofna sölureikning **verks** .  
3. Á flýtiflipanum **Verkhluti verks** skal hreinsa hvaða afmörkun sem er á **verkhlutanúmeri.** til að reikningsfæra verkið. Í reitnum **Verknr.** Viðeigandi verkefni er valið.  
4. Í flipanum  **Valkostir** er bókunardagsetningin færð inn og skilgreint hvort stofna eigi einn reikning fyrir hvert verk eða einn fyrir öll verk.  
5. Velja hnappinn **Í lagi** til að stofna reikninginn og velja svo **Í lagi** á staðfestingarsíðunni.  

Þegar Trausti stofnar reikninginn er hann til dæmis fáanlegur frá **Mitt hlutverk Örgjörva** sölupöntunar, til dæmis.

### <a name="to-post-a-new-sales-invoice"></a>Nýr sölureikningur bókaður

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölureikningar** og velja síðan viðkomandi tengil.  
2. Reikningur er valinn fyrir viðskiptamann Nr. 01445544. Sjá má upplýsingarnar sem slegnar voru inn frá áætlunarlínunum.  
3. Valið er **Bóka** aðgerðin. Velja **Já** til að staðfesta bókun.  

### <a name="to-view-the-posted-invoice"></a>Bókaðir reikningar skoðaðir

1. Opna verkið og velja svo aðgerðina **Áætlunarlínur verks** .  
2. Velja skal einhverja af áætlunarlínunum sem voru reikningsfærðar og velja svo aðgerðina **Sölureikningur/Kreditreikningur** .
3. Á síðunni **Verkreikningar** skal velja aðgerðina **Opna sölureikning/kreditreikning** .  

Tinna hefur spurningu um verð, kostnað og framlegð sem tengist þessu tiltekna verkefni, þannig að Trausti hefur aðgang að þeim upplýsingum á **tölfræðisíðunni** .  

### <a name="to-open-the-statistics-page"></a>Tölfræðisíðan opnuð

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.  
2. Veldu **Upplýsingar** aðgerðina. Hægt er að skoða ítarlegar upplýsingar um verð, kostnað og framlegð bæði í staðbundnum og erlendum gjaldmiðlum.  
3. Velja skal hnappinn **Loka** til að loka síðunni **Upplýsingar um** verkefni.  

## <a name="handling-fixed-prices-1"></a>Meðhöndlun fasts verðs

CRONUS er samið um að setja upp fundarsali. Sem verkefnastjóri vill Petra fá góða yfirsýn yfir þau verk sem þarf fyrir verkefnið með tengdum áætluðum og kostnaði sem til hefur komið fyrir hvern verkhluta. Að auki vill Petra vita umsamið heildarverð fyrir verkefnið og upphæðina sem var reikningsfærð á þennan stað. Hann er í samkomulagi við viðskiptamanninn varðandi fast verðlagningu fyrir verkefnið.  

### <a name="to-manage-fixed-pricing-in-projects"></a>Föstu verði stjórnað í verkum

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.  
2. Guildford **verknúmerið** er valið og svo aðgerðin Verkhlutalínur **verkefnis** valin.  
3. Lína 1120 er valin og í reitnum **Fjárhagsáætlun (heildarkostnaður)** er hægrismellt á upphæðina og valið **Köfun**.  

     Með því að fara yfir áætlunarlínur verkefnisins er ákveðið að Petra þurfi Trausta í 30 klukkustundir fyrir þetta stig verkefnisins. Petra samþykkir fast verð við viðskiptamanninn.  

4. Á síðunni **Verkhlutalínur verkefnis** skal velja línu 1120 og velja svo aðgerðina Áætlunarlínur **verkefnis** . Stofna áætlunarlínu með eftirfarandi upplýsingum:  

    | Lína | Línugerð | Tegund        | Fj.   | Magn |
    |------|-----------|-------------|-------|----------|
    | 1    | Bæði fjárhagsáætlun og reikningshæft  | Forði | Tinna | 30 |

     Lokaðu síðunni.  
5. Í reitnum **Áætlun (heildarkostnaður)** er hægrismellt á reitinn og **Kafaniður** valið aftur á síðunni **Verkhlutalínur** verkefnis. Skoða breytingarnar á tímasetningunni. Sjá má að 30 klukkustundum er bætt við áætlunina.  
6. Loka síðunum.  

Eftir að áætluninni hefur verið bætt við þessa verkhlutalínu vinnur Trausti 25 klukkustundir við verkefnið og færir þessar stundir inn í verkbókina.  

### <a name="to-enter-hours-in-a-project-journal"></a>Klukkustundir færðar inn í verkbók

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **verkbækur** og velja síðan viðeigandi tengil.  
2. Eftirfarandi upplýsingar eru slegnar inn á nýja línu:  

    - **Tegund línu**: **(autt)**  
    - **Dagsetning bókunar**: **(dagurinn í dag)**  
    - **Númer fylgiskjals**: **J00002**  
    - **Verkefni Nr.**: **Guildford**  
    - **Verkhlutanr.**: **1120**  
    - **Gerð**: **Forði**  
    - **Nr.**: **Trausti**  
    - **Magn**: **25**  

3. Valið er **Bóka** aðgerðin.  

     Nokkrum dögum síðar vinnur Trausti í aðra 10 tíma við verkefnið og hefur unnið 35 tíma alls. Þar sem samkomulagið er í 30 klukkustundir við viðskiptavininn eru aðeins fimm þessara tíma gjaldfærðar á viðskiptavininn. Trausti bætir hinum fimm klukkustundunum handvirkt við áætlunina.  

4. Á síðunni Verkbók **skal velja aðgerðina** Reikna eftirstandandi notkun **.**   
5. Á síðunni **Reiknaðar eftirstöðvar notkunar** verks á flýtiflipanum **Valkostir** eru eftirfarandi upplýsingar slegnar inn:  

    - **Númer fylgiskjals**: **J00003**  
    - **Dagsetning bókunar**: **(dagurinn í dag)**  

6. Á flýtiflipanum **Verkhluti** verkefnis eru eftirfarandi upplýsingar slegnar inn:  

    - **Verkefni Nr.**: **Guildford**  
    - **Verkhlutanr.**: **1120**  

7. Velja hnappinn **Í lagi** til að keyra útreikninginn.

    Fimm vinnustundir eru eftir fyrir Tinnu. Reiturinn **Línutegund** er auður, sem gefur til kynna að aðeins eigi að bóka notkunina þar sem vinnan hefur þegar verið áætluð.  

8. Í Verkbókinni **er** stofnuð ný lína með eftirfarandi upplýsingum. Ganga þarf úr skugga um að bæði verknúmer séu í röð með númerunum sem þegar hafa verið notuð:  

    - **Línugerð**: **Áætlun**  
    - **Verkefni Nr.**: **Guildford**  
    - **Verkhlutanr.**: **1120**  
    - **Gerð**: **Forði**  
    - **Nr.**: **Trausti**  
    - **Magn**: **5**  

     Ef tegundin Áætlunarlína **er notuð** eru uppfærslur á tímasettum kostnaði og verði en engar uppfærslur á samningskostnaði og verði sem reikningsfært er á viðskiptamanninn.  

9. Valið er **Bóka** aðgerðin. Velja hnappinn **Í lagi** til að loka síðunni.  
10. Listinn Verk er **opnaður** .  
11. GUILDFORD verkefnið er valið og hægrismellt er á upphæðina í hlutanum **Verkhlutalínur** verkefnis og hægrismellt er á upphæðina í reitnum **Áætlun (heildarkostnaður).**  **Köfun** er valin til að skoða upplýsingarnar.  

     Breytingar eru sjálfkrafa færðar inn í línuna fyrir Verkhlutanúmer verks nr. 1120. Í heildarkostnaði áætlaðrar vinnu var fimm klukkustundum í viðbót af Trausta bætt við áætlunina.  

12. Velja hnappinn **Loka** til að loka síðunni.  
13. Hægrismella skal á upphæðina í reitnum **Samningur (heildarkostnaður)** og velja **KafaNiður** til að skoða upplýsingarnar.  

Í heildarverði samningsins eru aðeins 30 tímar sem upphaflegir samningar hafa verið teknir með, eins og samið var um við viðskiptamanninn.  

## <a name="copying-projects"></a>Afritun verka

Petra náði samkomulagi við viðskiptamann, Selagorian hf, um að setja upp 10 fundarsali. Samkomulagið er eins og fyrra verkefni. Þess vegna sparar það tíma að afrita það fyrra verkefni.  

Á síðunni **Afrita verk** er hægt að velja verk- og verklínurnar sem á að afrita.

- Afrita upprunaverkfærslur til að stofna áætlunarlínur byggðar á raunverulegri notkun.
- Afrita upprunaverkáætlunarlínurnar til að afrita upphaflegar áætlunarlínur yfir í nýja verkið.

Síðan er hægt að velja þá tegund áætlunarlína eða færslulínu sem taka á með og velja aðeins það sem á við um þetta nýja verkefni. Að lokum er hægt að velja verkið sem afrita á í og skilgreina hvort verð og magn skuli afritað einnig.  

### <a name="to-copy-a-project"></a>Til að afrita verk

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **Verkefni** og velja síðan viðeigandi tengil.  
2. Veljið aðgerðina **Nýtt** til að stofna nýtt verk. Eftirfarandi upplýsingar eru færðar inn:  

    - **Lýsing**: **Uppsetning tíu fundarsala**  
    - **Reikningsfærist á viðskiptamenn Nr.**: **20000**  

3.  **Velja skal Afrita verkhluta úr** aðgerð.  
4. Á síðunni **Afrita verkhluta er** eftirfarandi slegið inn:  

    - **Verkefni Nr.**: **Guildford**  
    - **Verkhlutanr. verks Frá**: **1000**  
    - **Uppruni**: **Áætlunarlínur verkefnis**  
    - **Áætlunarlínutegund tekin með**: **Áætlun + Reikningshæft**  
    - **Til Verkefnis Nr.**: **GuildfordSetting upp 10 fundarsali**  
    - Reitirnir **Afrita víddir** og **Afrita magn** eru valdir.  

5. Hnappurinn **Í lagi** er valinn til að afrita verkefnið og síðan er hnappurinn **Í lagi** valinn til að loka staðfestingarsíðunni.  

Með því að bera saman verð, verkhlutalínur og verkáætlunarlínur fyrir þessi tvö verk má sjá að upplýsingarnar voru afritaðar.  

## <a name="making-payments-by-installments"></a>Framkvæma greiðslur með inngreiðslum

CRONUS bara lenti í stóru verkefni sem tekur eitt ár að ljúka. Þar sem það krefst margs konar forða setur verkefnastjórinn upp samninginn þannig að viðskiptamaðurinn greiði hluta af verðinu fyrirfram, hluta af því þegar verkið er hálfnað og lokagreiðslu þegar því er lokið.  

### <a name="to-set-up-a-new-account"></a>Að setja upp nýjan reikning

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Á síðunni **Bókhaldslykill** skal velja aðgerðina **Nýtt** til að stofna nýtt spjald.  
3. Á spjaldið **Nýr fjárhagsreikningur** eru færðar inn eftirfarandi upplýsingar:  

    - **Nr.**: **40255**  
    - **Heiti**: **Greiðsla verkefnis**  

4. Á flipanum **Bókun** er reiturinn **Alm. vörubókunarflokkur** fylltur út, velja **Þjónustur**. Lokaðu síðunni.  
5. Á síðunni **Bókhaldslykill** veljið **Nr. 40255 greiðsla fyrir verk** og svo aðgerðina **Inndráttur bókhaldslykill**. Veljið **Já** til staðfestingar.  

Eftirfarandi ferli sýna hvernig á að stofna nýtt verk, setja verðlagningu og setja síðan upp greiðslu með inngreiðslu. Í verkhlutalínum er hægt að stofna sérstakar línur fyrir greiðslur með inngreiðslum. Öll vinna sem lokið er við fyrir verkið sem er bætt við áætlunina eru færðar inn í notkunarlínurnar. Fyrir hverja greiðsluhlutalínu í áætlunarlínunum, er línugerðin **Rukkun**, sem þýðir að reikningur verður sendur til viðskiptamanns. Færð er inn ný lína fyrir útborgunina. Í notkunarverkhlutalínuna er hægt að færa inn upplýsingar um vörur og forða sem notuð hafa verið í þetta verkefni, sem eykur við áætlunina, t.d. vinnustundir starfsmanna og vörur sem notaðar eru í verkefnið.  

### <a name="to-make-a-payment-by-installment"></a>Framkvæma greiðslu með inngreiðslu

1. Stofna nýtt verkefni.  
2. Eftirfarandi upplýsingar eru færðar inn á nýja **Verkspjaldið** :  

    - **Lýsing**: **Endurhönnun á móttöku**  
    - **Reikningsfærist á viðskiptamenn Nr.**: **30000**  
    - **Bókunarflokkur verkefnis**: **Uppsetning**  
    - **VÍV-aðferð**: **Kostnaðarvirði**  

3. Á Verkspjaldinu skal velja aðgerðina **Verð** og velja svo **forðaaðgerðina** . Eftirfarandi upplýsingar eru færðar inn:  

    - **Kóti**: **Trausti**  
    - **Einingarverð**: **10**  

     Loka síðunni.  

4.  **Á Verkspjaldinu**, í hlutanum **Verkhlutar**, er verkhlutalínum bætt við eins og lýst er í eftirfarandi töflu:  

    | Línurit | Nr. verkhluta verkefnis | Heimildasamstæða          | Gerð verkhluta verkefnis |
    |------|--------------|----------------------|---------------|
    | 1    | 1000         | Greiðsla - Útborgun | Bóka       |
    | 2    | 2000         | Notkun                | Bóka       |
    | 3    | 3 000         | Greiðsla - Hálfnað     | Bókun       |
    | 4    | 4000         | Greiðsla - Lokið | Bóka       |

5. Veljið verk 1000 og veljið svo aðgerðina Áætlunarlínur **verkefnis** .  

6. Stofna áætlunarlínu með eftirfarandi upplýsingum:  

    | Lína | Línugerð | Áætlunardagsetning  | Tegund        | Fj.   | Magn | Einingarverð |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Rukkun  | (dagurinn í dag) | Fjárhagur | 40255 | 1        | 5000       |

     Loka síðunni.  

7. Veljið verk 2000 og veljið svo aðgerðina Áætlunarlínur **verkefnis** .  

8. Stofna áætlunarlínu með eftirfarandi upplýsingum:

    | Lína | Línugerð | Áætlunardagsetning  | Tegund     | Fj.    | Magn |
    |------|-----------|----------------|----------|--------|----------|
    | 1    | Fjárhagsáætlun    | (dagurinn í dag) | Forði | Tinna | 120      |
    | 2    | Fjárhagsáætlun    | (dagurinn í dag) | Atriði     | 70104  | 10       |

     Loka síðunni. Á síðunni **Verkhlutalínur** verkefnis má sjá tímasetningarupphæðirnar hafa verið uppfærðar.  

9. Veljið verk 32000 og veljið svo aðgerðina Áætlunarlínur **verkefnis** .  

10. Stofna áætlunarlínu með eftirfarandi upplýsingum:

    | Lína | Línugerð | Áætlunardagsetning   | Tegund        | Fj.   | Magn | Einingarverð |
    |------|-----------|-----------------|-------------|-------|----------|------------|
    | 1    | Rukkun  | (dagsetning í framtíðinni) | Fjárhagur | 40255 | 1        | 5000       |

     Loka síðunni.  

11. Stofna svipaða áætlunarlínufærslu fyrir verkhluta 4000.  

 Nú þegar verk- og áætlunarlínurnar eru útfylltar býr Petra til reikning fyrir fyrstu greiðsluna. Petra gerir þetta úr verkhlutalínum verks til að ganga úr skugga um að reikningurinn innihaldi aðeins línurnar fyrir fyrstu greiðsluna. Hægt er að opna sölupöntunina úr áætlunarlínunum eða verklínunum.  

### <a name="to-create-an-invoice"></a>Til að stofna reikning

1. Á síðunni **Verkhlutalínur verkefnis** skal velja línu 1000 og velja svo aðgerðina **Stofna sölureikning** .  
2. Á síðunni **Stofna sölureikning** stillið dagsetninguna í dag sem bókunardagsetning, tilgreinið **Fyrir hvert verk**, og veljið hnappinn **Í lagi** til að búa til reikning með sjálfgefnum upplýsingum. Velja hnappinn **Í lagi** til að loka staðfestingarsíðunni.  
3. Velja aðgerðina **Sölureikningur/kreditreikningur**. Á sölureikningnum sést að einungis útborgunin er innifalin í reikningnum. Nú má senda reikninginn til viðskiptamannsins eins og samið var um.  

## <a name="summary"></a>Samantekt

Þessi kynning hefur farið í gegnum grunnþrepin til að vinna með verkefni í [!INCLUDE[prod_short](includes/prod_short.md)]. Fræðst hefur verið um hvernig stofna skuli nýtt verkefni, hvernig á að afrita verkefni og hvernig eigi að meðhöndla greiðslur. Einnig hefur gefist færi á að skoða sýning á því hvernig fylgst er með vinnustundum og reikninga stofnaðir.  

## <a name="see-also"></a>Sjá einnig .

 [Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  
 [Setja upp verkefnastjórnun](projects-setup-projects.md)  
 [Notkun tilfanga](projects-how-use-resources.md)  
 [Fylgst með framvindu og afköstum](projects-how-monitor-progress-performance.md)  
 [Reikningsfæra verk](projects-how-invoice-jobs.md)  
 [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
