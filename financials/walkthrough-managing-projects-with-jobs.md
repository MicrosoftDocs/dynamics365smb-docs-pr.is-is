---
title: "Kynning - Stýring verkefna með verkum | Microsoft Docs"
description: "Þessi kynning kynnir verkstýringareiginleikana í verkum. Verk eru leiðir fyrir áætlunargerð um notkun á forða fyrirtækisins og rakningu á ýmsum kostnaði sem fylgir notkun forða í tilteknu verkefni. Verk ná yfir notkun á vinnutíma starfsmanna, vélastundir, birgðahluti og aðrar gerðir notkunar sem notandinn kann að vilja fylgjast með í verkferlum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2df47e6f5bcd7b02282e45757d94bd6fc0f0981d
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-managing-projects-with-jobs"></a>Kynning: Stýring verkefna með verkum
Þessi kynning kynnir verkstýringareiginleikana í verkum. Verk eru leiðir fyrir áætlunargerð um notkun á forða fyrirtækisins og rakningu á ýmsum kostnaði sem fylgir notkun forða í tilteknu verkefni. Verk ná yfir notkun á vinnutíma starfsmanna, vélastundir, birgðahluti og aðrar gerðir notkunar sem notandinn kann að vilja fylgjast með í verkferlum.  

 Kynningin nær til uppsetningar nýs verks og einnig til nokkurra algengari verkefna eins og að meðhöndlun á föstu verði, framkvæmd greiðslu með inngreiðslu, bókun sölureikninga vinnu og afritun.  

## <a name="about-this-walkthrough"></a>Um kynninguna  
 Þessi kynning fjallar um eftirfarandi verk:  

### <a name="setting-up-a-job"></a>Uppsetning vinnu  
 Það er mjög einfalt að stofna verk með uppsetningu skipulagningar áætlunar fyrir verk. Þessi kynning fer yfir eftirfarandi atriði:  

-   Hvernig setja skal upp verkhlutalínur og áætlunarlínur.  
-   Stofna tiltekið verð fyrir vörur, forða og fjárhagsreikninga.  
-   Reikningsfærslu fyrir verk.  

### <a name="handling-fixed-prices"></a>Unnið með fast verð  
 Í verkum má meðhöndla fast verð og verð fyrir þjónustu eða vörur sem er fyrirfram samþykkt við viðskiptavini. Í þessari kynningu er hægt að gera eftirfarandi:  

-   Sjá hvernig samningsbundnar - og reikningsupphæðir eru ákveðnar.  
-   Gera ráð fyrir viðbótarvinnu í áætluninni sem hefur ekki verið reikningsfærð.  

### <a name="copying-a-job"></a>Afritun verks  
 Þetta dæmi sýnir hvernig á að afrita hluta eða allt verk pöntunar til að draga úr handvirkum innslætti gagna og auka á nákvæmni. Þar á meðal eftirfarandi:  

-   Afritun hluta af verki í nýtt verk.  
-   Afritun verðs fyrir sérstakt verk.  
-   Afritun áætlunarlína.  

### <a name="making-payment-by-installment"></a>Framkvæma greiðslu með inngreiðslu  
 Þegar stór kostnaðarsöm verk vara í langan tíma, gerir viðskiptavinurinn oft samkomulag við fyrirtækið um að greiða með inngreiðslum. Þetta dæmi sýnir hvernig greiðslur með inngreiðslum eru meðhöndlaðar og tekur til:  

-   Stofna greiðslu með inngreiðslu fyrir verk.  
-   Reikningsfærslu greiðslna til viðskiptavina.  
-   Bókhald til notkunar í verki sem er hannað fyrir greiðslu með inngreiðslu.  

## <a name="roles"></a>Hlutverk  
 Þessi kynning nær yfir verk fyrir eftirfarandi hlutverk:  

-   Verkefnastjóri  
-   Meðlimur verkefnateymis  

## <a name="prerequisites"></a>Frumskilyrði  
 Áður en hægt er að framkvæma verk hér í kynningunni þarf að gera eftirfarandi:  

-   Setja upp sýnigagnagrunninn CRONUS International Ltd.
-   Stofna nokkur sett sýnigagna með því að nota skrefin sem koma hér á eftir.  

## <a name="story"></a>Ferill  
Þessi kynning einblínir á fyrirtækið CRONUS International Ltd., hönnunar- og ráðgjafafyrirtæki sem hannar og setur upp nýja innviði á borð við ráðstefnusali og skrifstofur, með húsgögn, aukahluti og geymslueiningar. Mest af vinnunni er verkefnatengd. Petra er verkefnastjóri hjá CRONUS. Hann notar verk til að fá yfirsýn yfir hvert verk sem er í gangi hjá CRONUS og lokin verk. Hann sér yfirleitt um að semja við viðskiptavini og skrá helstu atriði, þ.e. verk- og áætlunarlínur auk verðs, inn í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hann sér að það er einfalt að búa til, uppfæra og fara yfir upplýsingar. Petra kann einnig vel hvernig verk eru afrituð og inngreiðslur í [!INCLUDE[d365fin](includes/d365fin_md.md)].

 Trausti, meðlimur í verkefnateymi sem heyrir undir Petru, ber ábyrgð á verkinu og fylgjast með. Hún fyllir inn eigin vinnu, auk vinnu sem framkvæmd er af tæknifólki í hverju verki. Hún skráir vörurnar sem þeir hafa notað og kostnaðinn sem það hefur haft í för með sér.  

## <a name="preparing-sample-data"></a>Undirbúa sýnigögn  
 Til undirbúnings fyrir þessa kynningu þarf að bæta Tinnu við sem nýjum tilföngum.  

### <a name="to-prepare-the-sample-data"></a>Til að undirbúa sýnigögnin  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Forði** og velja svo viðeigandi tengil.  
2.  Veljið aðgerðina **Nýtt** til að Búa til nýtt forðaspjald.  
3.  Á flýtiflipanum **Almennt** eru eftirfarandi upplýsingar slegnar inn:  

    - **Nr.**: **Trausti**  
    - **Nafn**: **Trausti**  
    - **Gerð**: **Einstaklingur**  

4.  Velja reitinn **Grunnmælieining**, og velja **Nýtt** aðgerð til að opna gluggann **Mælieining forða**. Í reitnum **Kóti** skal velja **Klukkustund**. Velja hnappinn **Í lagi**.  
5.  Á flýtiflipanum **Reikningsfæra** eru eftirfarandi upplýsingar slegnar inn:  

    -   **Innkaupsverð**: **5**  
    -   **Óbeinn kostnaður í %**: **4**  
    -   **Kostnaðarverð**:**10**  
    -   **Alm. vörubókunarflokkur**: **Þjónusta**  
    -   **VSK vörubókunarflokkur**: **VSK 25**  

6.  Velja hnappinn **Í lagi** til að vista breytingarnar.  

 Í næsta ferli er stofnuð verkbókarkeyrsla fyrir viðkomandi ef bóka á notkun hans.  

### <a name="to-create-a-job-journal-batch"></a>Til að búa til verkbókarkeyrslu  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkbækur** og velja svo viðeigandi tengil.  
2.  Í glugganum **Verkbók** veljið reitinn **Heiti keyrslu**. Glugginn **Bókarkeyrsla verks** opnast.  
3.  Veljið aðgerðina **Nýtt** til að Búa til nýtt Ný lína er stofnuð með eftirfarandi upplýsingum  

    -   **Nafn**: **Trausti**  
    -   **Lýsing**: **Trausti**  
    -   **Númeraröð**: **JJNL-GEN**  

4.  Velja hnappinn **Í lagi** til að loka öllum opnum gluggum.  

## <a name="setting-up-a-job"></a>Uppsetning vinnu  
 Í þessu dæmi hefur CRONUS náð samningum við viðskiptamann, Progressive Home Furnishings, um að hanna fundar- og matsal þeirra. Viðskiptamaðurinn er staðsettur í Bandaríkjunum og verkefnið krefst sérstaks hugbúnaðar. Verkefnastjóri nær samkomulagi við viðskiptamanninn og stofnar verk sem nær yfir samkomulagið.  

### <a name="to-set-up-a-job"></a>Uppsetning verks  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verk** og velja svo viðeigandi tengil.  
2.  Veljið aðgerðina **Nýtt** til að Búa til nýtt spjald.  
3.  Á flýtiflipanum **Almennt** eru eftirfarandi upplýsingar slegnar inn:  

    -   **Lýsing**: **Ráðgjöf við uppsetningu fundarsals**  
    -   **Reikningsfærist á viðskiptamenn Nr.**: **01445544**  

4.  Á flýtiflipanum **bókun** eru eftirfarandi upplýsingar slegnar inn:  

    -   **Staða**: **Röð**  
    -   **Bókunarflokkur verka**: **Uppsetning**  
    -   **VÍV-aðferð**: **Kostnaðarvirði**  

5.  Á flýtiflipanum **Tímalengd** er slegin inn dagsetning dagsins í dag í reitina **Upphafsdagur** og **Lokadagur**. Þessar dagsetningar verða notaðar við umreikning gjaldmiðla þegar verkið er reikningsfært.  
6.  Á flýtiflipanum **Erlent** skal stilla gjaldmiðilskótann á **USD**. Sé USD valið í reitnum **Gjaldmiðilskóti reiknings** mun verkið verða reikningsfært í Bandaríkjadölum og áætlað í staðbundnum gjaldmiðli CRONUS aðeins.  

 Hægt er að sérsníða verð fyrir viðskiptavini á hvert verk, eftir þeim samningum sem settir hafa verið fram. Í næsta ferli tilgreinir verkefnastjórinn verð viðkomandi tíma, stillir verð fyrir þann hugbúnað sem nauðsynlegur er og bætir við ferðakostnaði sem viðkomandi hefur samþykkt að greiða.  

### <a name="to-customize-pricing"></a>Til að sérsníða verðlagningu  

1.  Á verkspjaldinu skal velja **Forði** aðgerðina.  
2.  Í glugganum **Forðaverð verks** eru eftirfarandi upplýsingar slegnar inn:  

    -   **Kóti**: **Trausti**  
    -   **Einingarverð**: **20**  

3.  Velja hnappinn **Í lagi** til að loka glugganum.  
4.  Velja aðgerðina **Vara**.  
5.  Í glugganum **Verð vöru** eru eftirfarandi upplýsingar slegnar inn og sérsniðið verð:  

    1.  **Vörunr.**: **80201 (teikniforrit)**  
    2.  **Einingarverð**: **200**  

6.  Velja hnappinn **Í lagi** til að loka glugganum.  
7.  Veldu aðgerðina **Fjárhagsreikningur**.  
8.  Í glugganum **Fjárhagsreikningsverð verks** færið inn eftirfarandi upplýsingar og ferðakostnað, sem viðskiptavinur hefur samþykkt að greiða kostnaði og að auki 25 prósent:  

    1.  **Fjárhagsreikningur**: **8430 (Ferðir)**  
    2.  **Stuðull einingaverðs**:**1,25**  

9. Velja hnappinn **Í lagi** til að loka glugganum.  

 Síðustu skrefin í uppsetningu verks eru að bæta við verkhlutana og áætlunarlínurnar sem eru hluti af hverju verki. Áætlunarlínurnar ákvarða hvað er reikningsfært á viðskiptamanninn.  

### <a name="to-add-job-tasks"></a>Til að bæta við verkhlutum  

1.  Á spjaldinu **Verk** fyrir nýja verkið skal velja aðgerðina **Verkhlutalínur**.  
2.  Eftirfarandi tafla lýsir upplýsingunum sem ætti að færa inn í reitina.  

    |Verkhluta nr.|Description|Tegund verkhluta|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Ráðgjöf við uppsetningu á sal|Frá-tala|  
    |1010|Ráðgefandi fundir með viðskiptavini|Bókun|  
    |1020|Þróun|Bókun|  
    |1090|Ráðgjöf alls|Til-tala|  

3.  Til að sýna að ákveðnir verkhlutar séu undirflokkar annarra verkhluta er farið í flipann **Aðgerðir**, flokkinn **Aðgerðir** og **Draga inn verkhluta verks** valið.  

 Áætlunarlína getur verið ein af eftirfarandi tegundum:  

-   **Áætlun**: Bætt við áætlun en ekki reikningsfært.  
-   **Samningur**: Reikningsfærður, en ekki bætt við tímasetninguna.  
-   **Bæði áætlun og samningur**: Reikningsfærð og bætt við tímasetninguna.  

 Í þessari kynningu. notar verkefnastjórinn **Bæði áætlun og samning**. Hann stofnar þrjár áætlunarlínur fyrir verk 1010 og tvær áætlunarlínur fyrir verk 1020.  

### <a name="to-create-planning-lines"></a>Til að stofna áætlunarlínur  

1.  Veljið línu 1010 og veljið svo aðgerðina **Verkáætlunarlínur**. Eftirfarandi upplýsingar eru færðar inn:  

     **Lína 1**  

    -   **Línu tegund**: **Bæði áætlun og samningur**  
    -   **Dagsetning áætlunar**: **(dagurinn í dag)**  
    -   **Gerð**: **Forði**  
    -   **Nr.**: **Trausti**  
    -   **Magn**: **40**  

     **Lína 2**  

    -   **Tegund línu**: **Bæði áætlun og samningur**  
    -   **Dagsetning áætlunar**: **(dagurinn í dag)**  
    -   **Gerð**: **Forði**  
    -   **Nr.**: **Timothy**  
    -   **Magn**: **40**  

     **Lína 3**  

    -   **Línu tegund**: **Bæði áætlun og samningur**  
    -   **Dagsetning áætlunar**: **(dagurinn í dag)**  
    -   **Gerð**: **Fjárhagsreikningur**  
    -   **Nr.**: **8430 (ferðalög)**  
    -   **Magn**: **2**  
    -   **Kostnaðarverð**:**400**  

2.  Velja hnappinn **Í lagi** til að loka glugganum. Samtölurnar eru uppfærðar í glugganum **Verkhlutalínur verks**.  
3.  Veljið línu 1020 og veljið svo aðgerðina **Verkáætlunarlínur**. Eftirfarandi upplýsingar eru færðar inn:  

     **Lína 1**  

    -   **Línu tegund**: **Bæði áætlun og samningur**  
    -   **Dagsetning áætlunar**: **(dagurinn í dag)**  
    -   **Gerð**: **Forði**  
    -   **Nr.**: **Trausti**  
    -   **Magn**: **80**  

     **Lína 2**  

    -   **Línu tegund**: **Bæði áætlun og samningur**  
    -   **Dagsetning áætlunar**: **(dagurinn í dag)**  
    -   **Tegund**: **Vara**  
    -   **Nr.**: **80201 (Myndvinnsluforrit)**  
    -   **Magn**: **1**  

4.  Velja hnappinn **Í lagi** til að loka glugganum. Samtölur eru uppfærðar í glugganum **Verkhlutalínur verks**.  

## <a name="calculating-remaining-usage"></a>Útreikningur á notuðum eftirstöðvum  
 Tinna, sem er teymismeðlimur í verkefninu, hefur unnið í verkinu í nokkurn tíma og vill skrá tímana sína og notkun á verkið. Hún hefur verið unnið fleiri klukkutíma en það sem um var samið við viðskiptavininn. Hún notar keyrsluna **Reikna notaðar eftirstöðvar** til að reikna eftirstöðvar fyrir verk í verkbók. Keyrslan reiknar út, fyrir hvert verk, mismuninn milli áætlaðrar notkunar vöru, forða og fjárhagsútgjalda, og notkunar í raun samkvæmt bókuðum verkbókarfærslum. Eftirstandandi notkun er síðan sýnd í verkbókinni, og má bóka hana þaðan.  

### <a name="to-calculate-remaining-usage"></a>Eftirstöðvar notkunar reiknaðar  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkbækur** og velja svo viðeigandi tengil.  
2.  Í glugganum **Verkbók** í reitnum **Heiti keyrslu** er listinn **Verkbókarkeyrslur** opnaður. Velja skal verkbókarkeyrsluna **Trausti**.  
3.  Veljið aðgerðina **Reikna eftirstandandi notkun**.  
4.  Í glugganum **Verk - Reikna eftirstandandi notkun** á flýtiflipanum **Verkhluti** veljið reitinn **Verk nr.** og veljið viðeigandi verknúmer, yfirleitt verk J 00010.  
5.  Á flýtiflipanum **Valkostir** er **J00001** slegið inn í reitinn **Númer fylgiskjals**. Þetta gerir rakningu bókunar auðveldari á síðari stigum.  
6.  Dagurinn í dag er færður inn sem bókunardagsetningin.  
7.  Velja hnappinn **Í lagi**. Þetta myndar verkbókarlínurnar sem leiddar eru af áætlunarlínum sem Petra stofnaði fyrir Verkbókina.  
8.  Velja hnappinn **Í lagi** í staðfestingarglugganum. Mynduðum línum er bætt við verkbók.  
9. Ganga þarf úr skugga um að öll skjöl séu númeruð J00001 og velja svo **Bóka** aðgerðina. Velja **Já** til að staðfesta bókun.  
10. Línurnar eru bókaðar. Velja hnappinn **Í lagi** til að loka glugganum.  

## <a name="creating-and-posting-a-job-sales-invoice"></a>Reikningur verksölu stofnaður og bókaður  
 Næst skal Trausti stofna nýjan reikning fyrir allt verkið eða fyrir hluta af verkinu. Einnig má hengja reikninginn við annan reikning fyrir sama viðskiptavin fyrir sama verkið. Í þessu tilfelli, er reikningar gerðir fyrir allt verkið, þar sem verkinu er lokið.  

### <a name="to-create-a-job-sales-invoice"></a>Stofnun reiknings fyrir verksölu  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verk** og velja svo viðeigandi tengil.  
2.  Veljið verkið sem var stofnað áður og veljið því næst **Stofna verksölureikningur** aðgerðina.  
3.  Á flýtiflipanum **Verkhluti verks**, skal hreinsa hverja þá afmörkun á **Verkhlutanr. verks** til að reikningsfæra verkið. Í reitnum **Verk nr.** er viðeigandi verk valið.  
4.  Í flipanum  **Valkostir** er bókunardagsetningin færð inn og skilgreint hvort stofna eigi einn reikning fyrir hvert verk eða einn fyrir öll verk.  
5.  Velja hnappinn **Í lagi** til að stofna reikninginn og velja svo **Í lagi** í staðfestingarglugganum.  

 Eftir að Tricia stofnar reikninginn getur hún nálgast hann frá **Sala og Markaðssetning** undir **Vinnsla pantana** og gert aukavinnslu.  

### <a name="to-post-a-new-sales-invoice"></a>Nýr sölureikningur bókaður  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innkaupareikningar** og velja svo viðeigandi tengil.  
2.  Reikningur er valinn fyrir viðskiptamann Nr. 01445544. Sjá má upplýsingarnar sem slegnar voru inn frá áætlunarlínunum.  
3.  Valið er **Bóka** aðgerðin. Velja **Já** til að staðfesta bókun.  

### <a name="to-view-the-posted-invoice"></a>Bókaðir reikningar skoðaðir  

1.  Opnið verkið og veljið svo aðgerðina **Verkáætlunarlínur**.  
2.  Veljið einhverja af áætlunarlínunum hafa verið reikningsfærðar og veljið síðan **Sölureikningar/kreditreikningar** aðgerðina.
3. Í glugganum **Verkreikningar** skal velja aðgerðina **Opna sölureikning/kreditreikning**.  

 Svör við spurningum varðandi verð, kostnað og ágóða í verkinu má finna í glugganum **Tölfræði**.  

### <a name="to-open-the-statistics-window"></a>Tölfræðiglugginn opnaður  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verk** og velja svo viðeigandi tengil.  
2.  Veldu **Upplýsingar** aðgerðina. Hægt er að fara yfir nákvæmar upplýsingar um verkkostnað, kostnað og hagnað í bæði innlendri og erlendri mynt.  
3.  Velja hnappinn **Loka** til að loka glugganum **Verkupplýsingar**.  

## <a name="handling-fixed-prices"></a>Unnið með fast verð  
 Cronus hefur tekið að sér að setja upp fundarsali. Verkefnastjórinn Petra þarf gott yfirlit yfir verkhluta verksins ásamt kostnaðaráætlun og kostnaði sem stofnað hefur verið til fyrir hvern verkhluta. Auk þess vill hann vita heildarverð samningsins fyrir verkið og upphæðin sem hefur verið reikningsfærð fram að þessu. Hann hefur náð samkomulagi við viðskiptamanninn varðandi fast verð fyrir verk.  

### <a name="to-manage-fixed-pricing-in-jobs"></a>Föstu verði verka stýrt  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verk** og velja svo viðeigandi tengil.  
2.  **Guildford** verknúmerið er valið og svo er valin **Verkhlutalínur verks** aðgerðina.  
3.  Lína 1120 er valin og í reitnum **Tímasetning (heildarkostnaður)** er hægrismellt á upphæðina og valið **Köfun**.  

     Með því að endurskoða verkáætlunarlínur, ákvarðar Petra að einnig þurfi að nota Trausta í 30 klukkustundir vegna þessa stigs verksins. Hann semur um fast verð við viðskiptavininn.  

4.  Í glugganum **Verkhlutalínur** veljið línu 1120 og veljið svo aðgerðina **Verkáætlunarlínur**.  
5.  Veljið aðgerðina **Nýtt** til að Búa til nýtt Ný lína er stofnuð með eftirfarandi upplýsingum:  

    -   **Línu tegund**: **Bæði áætlun og samningur**  
    -   **Gerð**: **Forði**  
    -   **Nr.**: **Trausti**  
    -   **Magn**: **30**  

7.  Velja hnappinn **Í lagi** til að loka glugganum.  
8.  Í reitnum **Tímasetning (heildarkostnaður)**, hægrismella á reitinn og velja **KafaNiður** aftur í glugganum **Verkhlutalínur verks**. Skoða breytingarnar á tímasetningunni. Sjá má að 30 klukkustundum hefur verið bætt við tímasetninguna.  
9. Velja hnappinn **Í lagi** til að loka glugganum.  

 Eftir að Trausta hefur verið bætt við tímasetninguna í þessa verkhlutalínu þá vinnur hann 25 klukkustundir við verkið. Þessar klukkustundir færir hún inn í Verkbókina.  

### <a name="to-enter-hours-in-the-job-journal"></a>Tímum bætt í Verkbókina  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkbækur** og velja svo viðeigandi tengil.  
2.  Eftirfarandi upplýsingar eru slegnar inn á nýja línu:  

    -   **Tegund línu**: **(autt)**  
    -   **Dagsetning bókunar**: **(dagurinn í dag)**  
    -   **Númer fylgiskjals**: **J00002**  
    -   **Verk Nr.**: **Guildford**  
    -   **Verkhlutanr.**: **1120**  
    -   **Gerð**: **Forði**  
    -   **Nr.**: **Trausti**  
    -   **Magn**: **25**  

3.  Valið er **Bóka** aðgerðin.  

     Nokkrum dögum síðar vinnur Trausti í aðra 10 tíma við verkið. Hann hefur nú unnið 35 tíma alls. Þar sem samningurinn er fyrir 30 tíma við viðskiptavininn munu aðeins fimm þessara tíma vera færðir á viðskiptavininn. Tinna mun bæta aukatímunum fimm sem hún vann við áætlunina handvirkt.  

4.  Í glugganum **Verkbók** veljið aðgerðina **Reikna eftirstandandi notkun**.  
5.  Í glugganum **Reiknaðar eftirstöðvar notkunar verks** á flýtiflipanum **Valkostir** þarf að færa inn eftirfarandi upplýsingar:  

    -   **Númer fylgiskjals**: **J00003**  
    -   **Dagsetning bókunar**: **(dagurinn í dag)**  

6.  Eftirfarandi upplýsingar eru færðar inn á flýtiflipanum **Verkhluti verks**:  

    -   **Verk Nr.**: **Guildford**  
    -   **Verkhlutanr.**: **1120**  

     Velja hnappinn **Í lagi** til að keyra útreikninginn. Fimm vinnustundir eru eftir fyrir Tinnu. Reiturinn **Línugerð** er auður sem gefur til kynna að tímarnir verða bókaðir vegna þess að vinnan hefur þegar farið fram.  

7.  Í glugganum **Verkbókakeyrslur** er ný lína stofnuð með eftirfarandi upplýsingum. Ganga þarf úr skugga um að bæði verknúmer séu í réttri númeraröð miðað við þau sem þegar hafa verið notuð:  

    -   **Tegund línu**: **Áætlun**  
    -   **Verk Nr.**: **Guildford**  
    -   **Verkhlutanr.**: **1120**  
    -   **Gerð**: **Forði**  
    -   **Nr.**: **Trausti**  
    -   **Magn**: **5**  

     Með því að nota línugerðina **Áætlun** uppfærir kerfið áætlaðan kostnað og verð án uppfærslu samningskostnaðar og verðs sem er reikningsfært á viðskiptamanninn.  

8.  Valið er **Bóka** aðgerðin. Velja hnappinn **Í lagi** til að loka glugganum.  
9. Listinn **Verk** er opnaður.  
10. Guildford verkið er valið og svo er valin **Verkhlutalínur verks** aðgerðina.  
11. Lína 1120 er valin og í reitnum **Tímasetning (heildarkostnaður)** er hægrismellt á upphæðina. **Köfun** er valin til að skoða upplýsingarnar.  

     Sjá má að breytingarnar færast sjálfkrafa inn í línuna fyrir Verkhlutanúmer 1120. Í heildarkostnað áætlaðrar vinnu, fimm öðrum tíma viðbótartímar Trausta hefur verið bætt við tímasetninguna.  

12. Velja hnappinn **Loka** til að loka glugganum .  
13. Hægrismella skal á upphæðina í reitnum **Samningur (heildarkostnaður)** og velja **KafaNiður** til að skoða upplýsingarnar.  

     Í heildarverði samnings koma aðeins fram hinir upphaflegu 30 tímar sem voru innifaldir í verkinu vegna þess að um það var samið við viðskiptamanninn.  

## <a name="copying-jobs"></a>Verk afrituð  
 Petra hefur náð samkomulagi við viðskiptamann, Selagorian hf, um að setja upp 10 fundarsali. Samningurinn er svipaður eldri verkum. Þess vegna mun spara tíma að afrita fyrra verkið.  

 Í glugganum **Afrita verk** er hægt að velja verkið og verklínurnar sem á að afrita. Einnig er hægt að velja að afrita eignafærslu upprunalega verksins, sem stofnar áætlunarlínur á grundvelli raunverulegrar notkunar og hægt er að afrita áætlunarlínu upprunalega verksins, sem afritar upprunalegar áætlunarlínur yfir í nýja verkið. Síðan er hægt að velja þá tegund áætlunarlínu eða eignafærslulínu sem á að hafa með og velja aðeins það sem á við í þessu nýja verki. Að lokum er hægt að velja verkið sem á að afrita í og tilgreina hvort afrita eigi verð og magn einnig.  

### <a name="to-copy-a-job"></a>Verk afritað  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verk** og velja svo viðeigandi tengil.  
2.  Veljið aðgerðina **Nýtt** til að Búa til nýtt verk. Eftirfarandi upplýsingar eru færðar inn:  

    -   **Lýsing**: **Uppsetning tíu fundarsala**  
    -   **Reikningsfærist á viðskiptamenn Nr.**: **20000**  

3.  Velja aðgerðina **Afrita verkhluta verkhluta frá**.  
4.  Í glugganum **Afrita verkhluta verks** færið inn eftirfarandi:  

    -   **Verk Nr.**: **Guildford**  
    -   **Verkhlutanr. frá**: **1000**  
    -   **Uppruni**: **Áætlunarlínur verks**  
    -   **Með gerð áætlunarlínu**: **Áætlun + Samningur**  
    -   **Í verk nr.**: **Guildford Uppsetning tíu fundarsala**  
    -   Reitirnir **Afrita víddir** og **Afrita magn** eru valdir.  

5.  Velja hnappinn **Í lagi** til að afrita verkið og velja svo **Í lagi** til að loka staðfestingarglugganum.  

     Með því að bera saman verð, verkhlutalínur og áætlunarlínur fyrir verkin tvö má sjá að það tókst að afrita upplýsingarnar.  

## <a name="making-payments-by-installments"></a>Framkvæma greiðslu með inngreiðslu  
 CONUS hefur nýlega fengið stórt verkefni sem tekur um eitt ár að ljúka. Vegna þess hvað verkefnið þarfnast mikilla aðfanga setur verkefnastjórinn samninginn þannig upp, að farið er fram á að viðskiptamaðurinn borgi hluta af verðinu fyrirfram, hluta af verðinu þegar verkið er hálfnað og lokagreiðslu þegar því er lokið.  

### <a name="to-set-up-a-new-account"></a>Að setja upp nýjan reikning  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bókhaldslykill** og velja svo viðeigandi tengil.  
2.  Í glugganum **Bókhaldslykill** skal velja aðgerðina **Nýtt** til að stofna nýtt spjald.  
3.  Á spjaldið **Nýr fjárhagsreikningur** eru færðar inn eftirfarandi upplýsingar:  

    -   **Nr.**: **6630**  
    -   **Heiti**: **Greiðsla fyrir verk**  

4.  Á flipanum **Bókun** er reiturinn **Alm. vörubókunarflokkur** fylltur út, velja **ÝMISL**. Velja hnappinn **Í lagi** til að loka glugganum.  
5.  Í glugganum **Bókhaldslykill** veljið **Nr. 6630 greiðsla fyrir verk** og svo aðgerðina **Inndráttur bókhaldslykill**. Veljið **Já** til staðfestingar.  

 Eftirfarandi ferli sýnir hvernig eigi að stofna nýtt verk, stilla verðlagningu og síðan setja upp greiðslur með inngreiðslu. Í verkhlutalínu er hægt að stofna sérstakar línur fyrir greiðslur með inngreiðslum. Vinna sem lokið er við fyrir verkið sem er bætt við áætlunina eru færðar inn í notkunarlínurnar. Fyrir hverja greiðsluhlutalínu í áætlunarlínunum, er línugerðin Samningur, sem þýðir að reikningur verður sendur til viðskiptamanns. Færð er inn ný lína fyrir útborgunina. Í notkunarverklínuna er hægt að færa inn upplýsingar um vörur og forða sem notuð voru í verkið, sem mun auka við áætlunina, t.d. vinnutíma starfsmanna og vörur sem notaðar voru í verkið.  

### <a name="to-make-a-payment-by-installment"></a>Framkvæma greiðslu með inngreiðslu  

1.  Nýtt verk er stofnað.  
2.  Eftirfarandi upplýsingar eru færðar inn á nýja **Verk** spjaldinu:  

    -   **Lýsing**: **Endurhönnun á móttöku**  
    -   **Reikningsfærist á viðskiptamenn Nr.**: **30000**  
    -   **Bókunarflokkur verka**: **Uppsetning**  
    -   **VÍV-aðferð**: **Kostnaðarvirði**  

3.  Á verkspjaldinu skal velja **Forði** aðgerðina. Eftirfarandi upplýsingar eru færðar inn:  

    -   **Kóti**: **Trausti**  
    -   **Einingarverð**: **10**  

     Velja hnappinn **Í lagi** til að loka glugganum.  

4.  Á spjaldinu **Verk** skal velja **Verkhlutalínur** aðgerðina.  

     Eftirfarandi tafla lýsir línunum sem óskað er eftir að stofna.  

    |Lína|Verkhluta nr.|Description|Tegund verkhluta|  
    |----------|------------------|---------------------------------------|-------------------|  
    |1|1000|Greiðsla - Útborgun|Bókun|  
    |2|2000|Notkun|Bókun|  
    |3|3 000|Greiðsla - Hálfnað|Bókun|  
    |4|4 000|Greiðsla - Lokið|Bókun|  

5.  Í glugganum **Verkhlutalínur** veljið verk 1000 og veljið svo aðgerðina **Verkáætlunarlínur**.  
6.  Stofna áætlunarlínu með eftirfarandi upplýsingum:  

    -   **Tegund línu**: **Samningur**  
    -   **Dagsetning áætlunar**:  **(dagurinn í dag)**  
    -   **Gerð**: **Fjárhagsreikningur**  
    -   **Nr.**: **6630**  
    -   **Magn**: **1**  
    -   **Einingarverð**: **5000**  

     Velja hnappinn **Í lagi** til að loka glugganum.  

7.  Í glugganum **Verkhlutalínur** veljið **Verk 2000** og opnið **Áætlunarlínur verks**.  

     Eftirfarandi tafla lýsir áætlunarlínunum sem óskað er eftir að stofna.  

    |Lína|Línugerð|Áætlunardagsetning|Tegund|Fj.|Magn|  
    |----------|---------------|-------------------|----------|---------|--------------|  
    |1|Tímasetning|(dagurinn í dag)|Forði|Tinna|120|  
    |2|Tímasetning|(dagurinn í dag)|Vara|70104|10|  

     Velja hnappinn **Í lagi** til að loka glugganum. Í glugganum **Verkhlutalínur** er hægt að skoða áætlaðar upphæðir sem voru uppfærðar.  

8.  Í glugganum **Verkhlutalínur verks** er verk **3000**.  
9. Stofna áætlunarlínu með eftirfarandi upplýsingum:  

    -   **Tegund línu**: **Samningur**  
    -   **Áætlunardagsetning**: **ókominn dagur**  
    -   **Gerð**: **Fjárhagsreikningur**  
    -   **Nr.**: **6630**  
    -   **Magn**: **1**  
    -   **Einingarverð**: **5000**  

     Velja hnappinn **Í lagi** til að loka glugganum.  

10. Stofna svipaða áætlunarlínufærslu fyrir verkhluta 4000.  

 Nú þegar verk- og áætlunarlínurnar eru útfylltar býr Petra til reikning fyrir fyrstu greiðsluna. Hann gerir slíkt úr verkhlutalínunum til að tryggja að reikningurinn innihaldi aðeins línur fyrir fyrstu greiðsluna. Hægt er að opna sölupöntunina úr áætlunarlínunum eða verklínunum.  

### <a name="to-create-an-invoice"></a>Til að stofna reikning  

1.  Í glugganum **Verkhlutalínur** veljið línu 1000 og veljið svo aðgerðina **Stofna sölureikninga**.  
2.  Í glugganum **Stofna sölureikning** stillið dagsetninguna í dag sem bókunardagsetning, tilgreinið **Fyrir hvert verk**, og veljið hnappinn **Í lagi** til að búa til reikning með sjálfgefnum upplýsingum. Velja hnappinn **Í lagi** til að loka staðfestingarglugganum.  
3.  Velja aðgerðina **Sölureikningur/kreditreikningur**. Á sölureikningnum sést að einungis útborgunin er innifalin í reikningnum. Nú má senda reikninginn til viðskiptamannsins eins og samið var um.  

## <a name="next-steps"></a>Næstu þrep  
 Í kynningunni var farið yfir grunnskrefin í að vinna með verk í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Aflað hefur verið þekkingar um hvernig á að stofna nýtt verk, hvernig afrita á verk og hvernig á að meðhöndla greiðslur. Einnig hefur gefist færi á að skoða sýning á því hvernig fylgst er með vinnustundum og reikninga stofnaðir.  

## <a name="see-also"></a>Sjá einnig  
 [Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)   
 [Setja upp verkefnastjórnun](projects-setup-projects.md)   
 [Notkun tilfanga](projects-how-use-resources.md)   
 [Fylgst með framvindu og afköstum](projects-how-monitor-progress-performance.md)   
 [Reikningsfærsla verka](projects-how-invoice-jobs.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

