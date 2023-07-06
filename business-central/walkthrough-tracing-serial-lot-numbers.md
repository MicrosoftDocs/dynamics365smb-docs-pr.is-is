---
title: 'Vinna með Kynning: Rekja rað- og lotunúmer'
description: Þetta efnisatriði lýsir aðgerðunum sem þarf að grípa til til að koma í veg fyrir að selja gallaða vöru og einnig hvernig á að rekja og endurkalla vörur þegar þess gerist þörf.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
---
# <a name="walkthrough-tracing-seriallot-numbers"></a><a name="walkthrough-tracing-seriallot-numbers"></a><a name="walkthrough-tracing-seriallot-numbers"></a>Kynning: Rað-/lotunúmerarakning

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Þegar vörugallar koma upp þarf að greina villurnar og koma í veg fyrir að fyrirtækið sendi frá sér gölluðu vörurnar. Ef gölluð vara hefur þegar verið send út verður að rekja hana til þeirra sem fengu hana senda og innkalla vörurnar, ef þörf krefur.  

Fyrsti verkhluti gallastjórnunar er að rannsaka hvaðan gölluðu vörurnar komu og hvar þær voru notaðar. Rannsóknin byggir á fyrri gögnum og er einfölduð með því að leita í vörurakningarfærslum á síðunni **Vörurakning**.  

Næsta verk gallastjórnunar er að ákvarða hvort röktu vörunum hefur verið ráðstafað í opnum skjölum, svo sem sölupöntunum sem eftir á að bóka eða notkunarbókum. Þessi vinna er framkvæmd á síðunni **Finna færslur**. Hægt er að nota eiginleikann Leita að færslum til að leita að alls kyns færslum í gagnagrunni.  

## <a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a>Um kynninguna

Þessi kynning sýnir hvernig greina á hvaða vörur eru gallaðar, frá hvaða lánadrottni þær komu og hvar þær eru notaðar svo hægt sé að stöðva eða innkalla pantanirnar.  

Þessi kynning fjallar um eftirfarandi verk:  

- Rekja notkun til uppruna  
- Rekja uppruna til notkunar  
- Leita að öllum skrám sem innihalda rakta rað-/lotunúmerið.  

## <a name="roles"></a><a name="roles"></a><a name="roles"></a>Hlutverk

Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:  

- Gæðastjóri  
- Yfirmaður vöruhúss  
- Pantanavinnsla  
- Innkaupaaðili  

## <a name="prerequisites"></a><a name="prerequisites"></a><a name="prerequisites"></a>Frumskilyrði

Til að ljúka þessari kynningu þarf:  

- [!INCLUDE[prod_short](includes/prod_short.md)] Fyrirtækið.  
<!-- - To create new items and several business transactions by following the [Prepare Sample Data](walkthrough-tracing-serial-lot-numbers.md#prepare-sample-data).   -->

## <a name="story"></a><a name="story"></a><a name="story"></a>Ferill

Gæðastjórinn Ríkharður er að sinna söluvöruskilum á vöru 1002, kappaksturshjóli. Viðskiptamaðurinn, Selangorian hf., kvartaði undan gallaðri logsuðu á grindinni. Verkfræðingar í gæðastjórnun hafa staðfest að grindin á hjólinu sem skilað var sé gölluð. Gæðastjórinn þarf nú að ákvarða:  

- Hvaða lota grinda var gölluð.  
- Á hvaða innkaupapöntun gallaða lotan var móttekin.  

Gæðastjórinn hefur þær upplýsingar frá söludeildinni að kappaksturshjólið sem skilað var, vara 1002, hafði raðnúmerið RAÐNR1. Með því að nota þessar grunnupplýsingar verða þær að ákvarða hvar lokið Racing reiðhjól var síðast notað, og þá verða þau að rekja afturábak til elsta upprunans til að koma til móts við hvaða lotunúmer gallaða þátturinn, kappakstursbílnum, kom frá.  

Niðurstöður þessarar fyrstu vörurakningar sýna hvaða grindur voru gallaðar, og frá hvaða lánadrottni þær komu. Því næst, en innan sama heildarrakningarferlisins, þarf gæðastjórinn að finna öll seldu kappaksturshjólin sem innihéldu grindur úr gölluðu lotunni svo hægt sé að stöðva eða innkalla þær pantanir. Að lokum þarf gæðastjórinn að finna öll opin skjöl þar sem gallaða lotan er notuð svo engar fleiri færslur séu framkvæmdar.  

Tvö fyrstu gallastjórnunarverkin eru framkvæmd á síðunni **Vörurakning**. Síðasta verkið er framkvæmt á síðunni **Leita að færslum** í samþættingu við gluggann **Vörurakning**.  

## <a name="prepare-sample-data"></a><a name="prepare-sample-data"></a><a name="prepare-sample-data"></a>Undirbúa sýnigögn

Stofna þarf eftirfarandi nýjar vörur:  

- 2000, Grind: loturakning, íhlutur í 1002  
- 1002, kappaksturshjól: raðnúmersrakning  

Síðan þarf að búa til ýmsar innkaupa-, framleiðslu- og sölupantanir með vörunum tveimur.  

### <a name="to-create-the-items"></a><a name="to-create-the-items"></a><a name="to-create-the-items"></a>Þjónustuvörur stofnaðar:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3. Í reitnum **númer** Í reitinn  er talan **2000** færð inn og síðan eru eftirfarandi reitir fylltir út.  

    |Lýsing|Grunnmælieining|Almenn Vörubókunarflokkur|VSK vörubókunarflokkur|Birgðabókunarflokkur|Vörurakningarkóti|  
    |-----------|--------------------|------------------------|-----------------------|--------------------|------------------|  
    |Grind|STYKKI|HRÁEFNI|VSK25|HRÁEFNI|LOTALL|  

    > [!NOTE]  
    >  Til að færa inn grunnmælieininguna skal velja hnappinn **Nýtt** og velja **Þjónustumiðstöð samstarfsaðila** á síðunni **Mælieiningar vöru**.  

4. Allir aðrir reitir innihalda viðeigandi sjálfgefin gögn eða þurfa ekki að vera fylltir út.  
5. Velja hnappinn **Í lagi** til að stofna fyrsta nýja birgðaspjaldið, 2000.  
6. Velja **Nýtt**.  
7. Í reitnum **númer** Í reitinn  er talan **1002** færð inn og síðan eru eftirfarandi reitir fylltir út.  

    |Lýsing|Grunnmælieining|Almenn Vörubókunarflokkur|VSK vörubókunarflokkur|Birgðabókunarflokkur|Áfyllingarkerfi|Vörurakningarkóti|  
    |-----------------|--------------------------|------------------------------|-----------------------------|-----------------------------|--------------------------|------------------------|  
    |Kappaksturshjól|STYKKI|SMÁSALA|VSK25|LOKIÐ|Framl.pöntun|SNALLT|  

    > [!NOTE]  
    >  Til að færa inn grunnmælieininguna skal velja hnappinn **Nýtt** og velja **Þjónustumiðstöð samstarfsaðila** á síðunni **Mælieiningar vöru**.  

    Síðan skal skilgreina framleiðslugrunn vörunnar.

8. Á flýtiflipanum **Áfylling**, í reitinn **Leið nr.**, skal færa inn **1000**.  
9. Velja reitinn **Framleiðsluuppskrift nr.** og svo **Ítarlegt**.  
10. Á síðunni **Framleiðsluuppskriftarlisti** veljið fyrstu línuna **1000** og veljið svo aðgerðina **Breyta**.  
11. Á síðunni **Framleiðsluuppskrift** er gildinu í reitnum **Staða** breytt **Í þróun**.  
12. Farið er í auða línu er færð inn **2000** í reitnum **nr.** Og svo **1** í reitnum **Magn á** reit.  
13. Gildinu í reitnum **Staða** er breytt aftur í **Vottuð**.  
14. Velja **Í lagi** til að setja inn framleiðsluuppskriftina á birgðaspjaldið og loka síðunni **Framleiðsluuppskrift**.  

    Næst skal kaupa grindur frá Custom Metals incorporated.  

### <a name="to-purchase-components"></a><a name="to-purchase-components"></a><a name="to-purchase-components"></a>Til að kaupa íhluti

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.  
2. Valið er **Nýtt** aðgerð.  
3. Stofna innkaupapöntun fyrir lánardrottin, Custom Metals Incorporated, með því að fylla út í eftirfarandi línur.  

    |Atriði|Magn|Lotunr.|  
    |----|--------|-------|  
    |2000|10|LOTA1|  

4. Til að færa inn lotunúmerið skal velja aðgerðina **Vörurakningarlínur**  
5. Á síðunni **Vörurakningarlínur** skal fylla inn í reitina **lotunúmer** og **Magn (grunnur)** og loka svo síðunni.  
6. Fyllt er í reitinn **Lánardrottnareikningsnr.** hvaða gildi sem er.  
7. Veldu aðgerðina **Bóka**, veldu **Móttaka og reikningur** valkostinn og veldu síðan **Í lagi** hnappinn.  

    Næst skal kaupa grindur frá Coolwood Technologies.  
8. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.  
9. Valið er **Nýtt** aðgerð.
10. Stofna innkaupapöntun fyrir lánardrottin, Coolwood Technologies, með því að fylla út í eftirfarandi línur.  

    |Vara|Magn|Lotunr.|  
    |----------|--------------|-------------|  
    |2000|11|LOTA2|  

11. Til að færa inn lotunúmerið skal á flýtiflipanum **Línur**, í flokknum **Lína** velja **Vörurakningarlínur** aðgerðina.  
12. Á síðunni **Vörurakningarlínur** skal fylla inn í reitina **lotunúmer** og **Magn (grunnur)** og loka svo síðunni.  
13. Fyllt er í reitinn **Lánardrottnareikningsnr.** hvaða gildi sem er.  
14. Veldu aðgerðina **Bóka**, veldu **Móttaka og reikningsfæra** valkostinn og veldu síðan **Í lagi** hnappinn.  

    Næst skal framleiða tvö kappaksturshjól, RAÐ1 og RAÐ2.  

### <a name="to-produce-end-items"></a><a name="to-produce-end-items"></a><a name="to-produce-end-items"></a>Til að framleiða lokavörur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Losaðar framleiðslupantanir** og velja síðan viðkomandi tengil.  
2. Valið er **Nýtt** flokkur.  
3. Stofna nýja útgefna framleiðslupöntun með því að fylla út eftirfarandi reiti.  

    |Upprunanúmer|Magn|Raðnr.|  
    |----------|--------|----------|  
    |1002|2|SN1|  
    |1002|2|SN2|  

4. Velja aðgerðina **Endurnýja framleiðslupöntun**, og veljið síðan hnappinn **Í lagi** til að fylla inn í línuna.  
5. Til að færa inn raðnúmerið skal velja aðgerðina **Vörurakningarlínur**  
6. Á síðunni **Vörurakningarlínur** skal fylla inn í reitina **raðnúmer** og **Magn (grunnur)** og loka svo síunni.  

    Næst skal bóka notkun grinda úr LOTA1.  
7. Á síðunni **Útgefin framleiðslupöntun** skal velja aðgerðina **Framleiðslubók**.  
8. Á síðunni **Framleiðslubók** skal velja notkunarlínuna fyrir vöru 2000, smella á **Vörurakningarlínur.** aðgerðina.
9. Á síðunni **Vörurakningarlínur** veljið **Lotunr.** veljið **LOTA1** og veljið svo hnappinn **Í lagi**.  
10. Láta skal öll önnur sjálfgefin gildi á síðunni **Framleiðslubókinni** óhreyfð og veljið svo aðgerðina **Bóka**.  

    Næst skal framleiða tvö kappaksturshjól í viðbót, RAÐ3 og RAÐ4.  

11. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Losaðar framleiðslupantanir** og velja síðan viðkomandi tengil.  
12. Valið er **Nýtt** aðgerð.  
13. Stofna nýja útgefna framleiðslupöntun með því að fylla út eftirfarandi reiti í hausnum.  

    |Upprunanúmer|Magn|Raðnr.|  
    |----------------|--------------|----------------|  
    |1002|2|RAÐ3|  
    |1002|2|RAÐ4|  

14. Velja aðgerðina **Endurnýja framleiðslupöntun** til að fylla inn í línuna.  
15. Til að færa inn raðnúmerin skal velja aðgerðina **Vörurakningarlínur**, og síðan númerin á tveimur línum í reitnum **Raðnr.** á síðunni **Vörurakningarlínur**.  

    Næst skal bóka meiri notkun grinda úr LOTA1.  
16. Á síðunni **Útgefin framleiðslupöntun** skal velja aðgerðina **Framleiðslubók**.  
17. Á síðunni **Framleiðslubók** skal velja notkunarlínuna fyrir vöru 2000, smella á **Vörurakningarlínur.** aðgerðina.
18. Á síðunni **Vörurakningarlínur** veljið **Lotunr.** veljið **LOTA1** og veljið svo hnappinn **Í lagi**.  
19. Láta skal öll önnur sjálfgefin gildi á síðunni **Framleiðslubókinni** óhreyfð og veljið svo aðgerðina **Bóka**.  

    Fjögur kappaksturshjól, SN1 og SN4 hafa verið framleidd, fjórar af tíu keppnisgrindum notaðar úr LOT1, tvær grindur í hvorri framleiðslupöntun.  

20. Loka skal framleiðslubókinni og framleiðslupöntununum.  

    Næst skal selja kappaksturshjól. Selja fyrst kappaksturshjólið SN1 til Selangorian hf.  

### <a name="to-sell-the-end-items"></a><a name="to-sell-the-end-items"></a><a name="to-sell-the-end-items"></a>Til að selja lokavörurnar

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2.  Velja aðgerðina **Nýtt**, og síðan stofna sölupöntun með því að fylla í eftirfarandi reiti.  

    |Viðskiptamaður|Vara|Magn|Raðnr.|  
    |--------------|----------|----------|----------------|  
    |Silfurbúðin ehf.|1002|1|SN1|  

3.  Til að færa inn raðnúmerin skal velja aðgerðina **Vörurakningarlínur**, og síðan númerin í reitnum **Raðnr.** á síðunni **Vörurakningarlínur**.  
4.  Veldu aðgerðina **Bóka**, veldu **Móttaka og reikningur** valkostinn og veldu síðan **Í lagi** hnappinn.  

    Næst skal selja The Cannon Group PLC kappaksturshjólið með RAÐ2.  

5.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
6.  Velja aðgerðina **Nýtt**, og síðan stofna sölupöntun með því að fylla í eftirfarandi reiti.  

    |Viðskiptamaður|Vara|Magn|Raðnr.|  
    |--------------|----------|----------|----------------|  
    |Navision Ísland hf.|1002|1|SN2|  

7.  Til að færa inn raðnúmerin skal velja aðgerðina **Vörurakningarlínur**, og síðan númerin í reitnum **Raðnr.** á síðunni **Vörurakningarlínur**.  
8.  Veldu aðgerðina **Bóka**, veldu **Afhenda og reikningsfæra** valkostinn og veldu síðan **Í lagi** hnappinn.  

    Að lokum skal selja nokkrar grindur sérstaklega. Navision Ísland hf. einnig fjórar stakar grindur fyrir sína eigin framleiðslulínu.  

9. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
10. Velja aðgerðina **Nýtt**, og síðan stofna sölupöntun með því að fylla í eftirfarandi reiti.  

    |Viðskiptamaður|Vara|Magn|Raðnr.|  
    |--------------|----------|----------|----------------|  
    |Navision Ísland hf.|2000|5|LOTA1|  

11. Til að færa inn raðnúmerin, á flýtiflipanum **Línur**, í flokknum **Lína**, skal velja aðgerðina **Vörurakningarlínur**, og síðan númerin í reitnum **Raðnr.** á síðunni **Vörurakningarlínur**.  

    > [!NOTE]  
    >  Ekki bóka síðustu sölupöntunina á fimm grindum.  

    Hér með lýkur undirbúningi gagna fyrir sýnikennslu fyrir eiginleikana Vörurakningu og Leit að færslum.  

## <a name="tracing-from-usage-to-origin"></a><a name="tracing-from-usage-to-origin"></a><a name="tracing-from-usage-to-origin"></a>Rekja frá notkun til uppruna

 Gæðastjórinn hefur þær upplýsingar frá söludeildinni að kappaksturshjólið sem skilað var, vara 1002, hafði raðnúmerið RAÐ1. Með því að nota þessar grunnupplýsingar geta þeir ákvarðað hvar lokið Racing reiðhjól var síðast notað, í þessu tilviki, á sölusendingunni til Selangorian ehf. Síðan þarf hann að rekja slóð þess aftur að elsta upprunastaðnum til að komast að því úr hvaða lotu gallaða grindin kom og frá hvaða lánadrottni.  

### <a name="to-determine-which-lot-included-the-faulty-frame-and-who-supplied-it"></a><a name="to-determine-which-lot-included-the-faulty-frame-and-who-supplied-it"></a><a name="to-determine-which-lot-included-the-faulty-frame-and-who-supplied-it"></a>Til að komast að því hvaða lota innihélt gölluðu grindina og hvaðan hún kom

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörurakning** og velja síðan viðkomandi tengil.  
2.  Á síðunni **Vörurakning** er **RAÐ1** fært inn í reitinn **Raðnr.** og **1002** inn í reitinn **Birgðaafmörkun**.  
3.  Halda skal sjálfgefnu stillingunni **Vara-eingöngu rakin** í reitnum **Sýna íhluti**, og halda sjálfgefnu rakningaraðferðinni **Notkun - uppruni** í **Rakningaraðferð**.  
4.  Velja skal **Rekja** aðgerðina.  

    Bent er á að einn söluafhendingarhaus uppfyllir leitarskilyrðin. Áður en rakningunni er haldið áfram skal gengið úr skugga um að afhendingin sé sú sem sendi gallaða kappaksturshjólið til Selangorian hf.  

5.  Veljið fyrstu rakningarlínuna, og síðan **Sýna fylgiskjal** aðgerðina.  

    Nú skal haldið áfram að rekja uppruna söluafhendingar kappaksturshjólsins með númerið RAÐ1.  
6.  Smellt er á + táknið á rakningarlínunum til að stækka smám saman og rekja til baka í færslukeðjunni sem söluafhendingin kom frá.  

    Hægt er að rekja eftirfarandi færslusögu:  

    - Fyrsta bókaða skjal aftur á bak í færslukeðjunni er frálagsbókun RAÐ1 fyrir fyrstu útgefnu framleiðslupöntunina.  
    - Næsta bókaða skjal á undan því er notkunarbókunin úr fyrstu útgefnu framleiðslupöntuninni. Hér sér gæðastjórinn að grind úr LOTA1 var notuð.  
    - Aftasta bókaða skjalið í keðjunni er bókaða innkaupakvittunin fyrir grindur úr LOTA1 þegar þær voru færðar inn í birgðir.  

    Gæðastjóri hefur nú komið því á framfæri hvaða mikið af kappaksturrömmum var gölluð og þeir geta leitað til síðustu rakvélarlínu til að sjá hvaða söluaðili útvegaði þeim þ.e. sérsniðna málma felld.  

    > [!NOTE]  
    >  Ekki gera neinar frekari breytingar á niðurstöðum rakningarinnar, þar sem þær verða notaðar í næsta hluta.  

     Svona lýkur fyrsta gallastjórnunarverkinu á síðunni **Vörurakning**. Gæðastjórinn þarf nú að ákvarða hvort önnur bókuð skjöl hafa unnið með grindur úr LOTA1.  

## <a name="tracing-from-origin-to-usage"></a><a name="tracing-from-origin-to-usage"></a><a name="tracing-from-origin-to-usage"></a>Rekja frá uppruna til notkunar

 Gæðastjórinn hefur komist að því að gölluðu grindurnar komu úr LOTA1. Þeir verða nú að finna önnur kynþokkafult hjól sem innihalda Racing ramma úr gallabuxnum mikið þannig að þau hjól megi stoppa eða muna.  

 Ein leið til að undirbúa þetta rakningarfærsluverk á síðunni **Vörurakning** er að færa inn handvirkt LOTA1 í reitinn **Lotunr. - Afmörkun** og 2000 í reitinn **Vöruafmörkun**. Hins vegar verður aðgerðin **Rekja gagnstætt - frá línu** notuð í þessari kynningu.  

### <a name="to-find-all-usage-of-the-faulty-lot"></a><a name="to-find-all-usage-of-the-faulty-lot"></a><a name="to-find-all-usage-of-the-faulty-lot"></a>Til að finna alla notkun á gölluðu lotunni

1.  Á síðunni **Vörurakning** skal velja línu innkaupakvittunarinnar, síðustu rakningarlínuna, og velja svo **Rekja andstætt - frá línu**.  

    Rakningarniðurstöðurnar byggjast nú á afmörkunum rakningarlínunnar fyrir innkaupakvittunina, LOTA1 og vöru 2000, og útkoman byggist á rakningaraðferðinni **Uppruni - notkun**.  

    Til að fá yfirlit yfir alla notkun vöru 2000 með LOTA1 skal haldið áfram að stækka allar rakningarlínur.  

2.  Velja skal **Stækka allt** aðgerðina.  

    Fyrstu fjórar rakningarlínurnar vísa í söluafhendinguna til Selangorian hf., sem hefur þegar verið leyst. Síðasta línan sýnir að eitt kappaksturshjól enn, RAÐ2, var framleitt í sömu útgefnu framleiðslupöntun og síðan selt og afhent í annarri söluafhendingu.  

    Gæðastjórinn lætur söludeildina tafarlaust vita svo hægt sé að innkalla gallaða kappaksturshjólið frá viðskiptamanninum, Cannon Group PLC.  

    Á sama tíma geta þeir séð af síðustu þremur rakningarlínunum að annar tveggja atriða, SN3 og SN4, hafa verið framleidd á grundvelli kappaksturrömmum frá LOT1. Þau grípa til aðgerða til að loka fyrir þessar vörur í birgðum.  

    Svona lýkur öðru gallastjórnunarverkinu sem notar síðuna **Vörurakning** fyrir gallastjórnun. Þar sem síðan **Vörurakning** byggir einungis á bókuðum færslum þarf gæðastjórinn að halda áfram í gluggann **Leit að færslum** til að tryggja að LOTA1 sé ekki notuð í óbókuðum skjölum.  

## <a name="finding-all-records-of-a-seriallot-number"></a><a name="finding-all-records-of-a-seriallot-number"></a><a name="finding-all-records-of-a-seriallot-number"></a>Finna allar skrár rað-/lotunúmers

 Á síðunni **Vörurakning** komst gæðastjórinn að því að LOTA1 innhélt gölluðu grindurnar, frá hvaða lánadrottni þær komu og í hvaða bókuðu færslum þær voru notaðar. Þeir verða nú að ákvarða hvort LOT1 sé í opnum skjölum með því að samþætta í kjölfarið við  **finna færslur**  síðan þær geta framkvæmt leit í gegnum allar gagnagrunnsfærslur.  

### <a name="to-find-all-occurrences-of-lot1-in-non-posted-records-such-as-open-orders"></a><a name="to-find-all-occurrences-of-lot1-in-non-posted-records-such-as-open-orders"></a><a name="to-find-all-occurrences-of-lot1-in-non-posted-records-such-as-open-orders"></a>Til að finna öll tilfelli LOTA1 í skrám sem eftir á að bóka, svo sem opnum pöntunum

1.  Á síðunni **Vörurakning** skal velja bendilinn í fyrstu rakningarlínunni, innkaupakvittun LOTA1.  
2.  Veljið aðgerðina **Leita að færslum**.  

    Síðan **Leita að færslum** er forstillt með leitarsíum sem byggðar eru á rakningarniðurstöðunum fyrir LOTA1. Gæðastjórinn sér að flestar skrárnar snúa að skjölum sem þegar hafa verið auðkenndar á síðunni **Vörurakning** . Til dæmis vísar síðasta lína færsluleitarinnar af gerðinni Framleiðslupöntun til útgefnu framleiðslupantananna tveggja sem notuðu grindur úr LOTA1.  

    Önnur lína færsluleitarinnar af gerðinni **Sölulína** er skjalalína sem ekki hefur verið bókuð, svo gæðastjórinn kannar málið.  

3.  Til að opna sölulínuskrána skal velja aðra línu færsluleitarinnar, og velja síðan aðgerðina **Sýna**. Einnig er hægt að velja gildið í reitnum **Fjöldi færslna**.  

    Hér sér gæðastjórinn eina opna sölulínu fyrir gölluðu grindurnar. Þeir benda strax á að söludeild sem þessi pöntun sé afturkölluð og ný framleiðslupöntun, byggð á góðum kappaksturrömmum, sé hafin.  

 Hér með lýkur kynningunni á hvernig síðan **Leita að færslum** er notuð við gallastjórnun í samþættingu við síðuna **Vörurakning**.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/paths/use-serial-lot-numbers/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md)  
[Rekja vöruraktar vörur](inventory-how-to-trace-item-tracked-items.md)  
[Finna færslur](ui-find-entries.md)  
[Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
