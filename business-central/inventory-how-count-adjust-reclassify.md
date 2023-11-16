---
title: 'Talning, breytingar og endurflokkun birgða'
description: Lærðu að gera efnislegar talningar og endurbreytingar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
---
# <a name="count-adjust-and-reclassify-inventory-using-journals"></a>Talning, breytingar og endurflokkun birgða með færslubókum

Telja efnislega allar vörur í birgðum til að tryggja að magnið sé rétt. Sum fyrirtæki gera árlega efnislega talningu, og aðrir telja öll eða aðeins nokkur atriði oftar. Þegar vörur eru talsverðar skal nota færslubækur til að bóka raunverulegt magn í fjárhag. Til dæmis þegar birgðir eru verðtryggð í lok tímabils.

Að telja nokkur atriði oftar en aðrir, kannski vegna þess að gildi þeirra eru notuð til tíðahrings. Fyrir ferli talningar skal úthluta sérstökum talningartímabilum á vörurnar. Lærðu meira á  [að gera tíðahringatalningu](inventory-how-count-adjust-reclassify.md#to-do-cycle-counting).

Ef stilla á magn eftir rauntalningu eða öðrum tilgangi er notuð birgðabókarbók til að breyta birgðafærslum án þess að bóka færslur. Einnig er hægt að leiðrétta magnið fyrir staka vöru á birgðaspjaldi.

Ef breyta á eigindum í birgðafærslum skal nota endurflokkunarbók vöru. Dæmigerðar eigindir til að endurflokka eru með víddir og söluherferðarkótar. Endurflokkunarfærslubækur er einnig hægt að nota fyrir millifærslur með endurflokkun hólfa og birgðageymslukóta. Sérstök skref eiga við þegar þú vilt endurflokka rað- eða lotunúmer og lokadag þeirra. Frekari upplýsingar, sjá [Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md).

> [!NOTE]
> Í Multi-þrepa ferlum eru vörur skráðar í hólfum sem vöruhúsafærslur, ekki sem birgðafærslur. Þess vegna er hægt að telja, leiðrétta og endurflokkun í vöruhúsaferningabókum sem styðja hólf. Síðan eru nýju eða breyttu vöruhúsafærslurnar samstilltar við tengdar birgðafærslur til að endurspegla breytingar á birgðamagni og virði.

[!INCLUDE [edit-in-excel](includes/edit-in-excel.md)]

## <a name="to-count-physical-inventory"></a>Að telja efnislegar birgðir

Telja efnislegar birgðir, þ.e. telja upp raunverulegar vörur á lager, til að kanna hvort skráð magn sé það sama og efnislegt magn í birgðum. Að jafnaði skal Talning gerast í lok reikningsárs en stundum er það gert oftar. Ef munur er á skal bóka raunverulegt magn á vörureikningum <!--accounts, or ledger?--> áður en birgðamat er gert.

> [!NOTE]
> Þetta ferli lýsir því hvernig raunbirgðir eru notaðar með því að nota færslubók á  **raunbirgðabókarsíðunni** . Hægt er að nota skjöl á  **efnislegu birgðapöntun**  og  **efnislegri skráningu**  birgða. Þessum skjölum bjóðast meiri stýring og stuðningur við að dreifa talningarvinnunni yfir á marga starfsmenn. Frekari upplýsingar eru í talningu birgða með því að  [nota skjöl](inventory-how-count-inventory-with-documents.md).<br /><br />
> Bent er á að ekki er hægt að nota skjalaaðgerðina til að telja vörur í hólfum eða vöruhúsafærslum.

Í talningarferlinu felst einnig að sinna eftirtöldum verkefnum:

- Reikna væntanlegar birgðir.
- Prenta skýrsluna sem á að nota við talningu.
- Færa inn og bóka raunverulegt magn.

Það fer eftir vöruhúsauppsetningunni að telja efnislegar birgðir á einni af eftirfarandi leiðum. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).  

- Ef birgðageymslan notar ekki beinan frágang og tínslu er að  **nota síðuna Raunbirgðabókarsíða** . Aðferðin svipar til efnislegra birgða án vinnslu talninga.  
- Ef birgðageymslan notar beinan frágang og tínslu eru notaðar  **blaðsíður raunbirgðabókar**  vöruhúss. Síðan skal  **nota síðuna birgðabækur**  til að keyra  **Leiðréttingaraðgerðina**  Reikna vöruhúsaaðgerð. <!--We should say what to do on each of these pages.-->

### <a name="to-calculate-expected-inventory-in-basic-warehouse-configurations"></a>Áætlaðar birgðir reiknaðar út í grunnvöruhúsafbrigðum

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **efnislegar birgðabækur** og velja síðan tengda tengilinn.
2. Veljið aðgerðina **Reikna Birgðir**.
3. Á síðunni **Reikna birgðir** tilgreinið skilyrði sem nota á til að stofna færslubókarlínur, t.d. hvort þær eigi að innihalda vörur sem hafa engar birgðir skráðar.
4. Stilla afmarkanir ef aðeins á að reikna birgðir fyrir ákveðnar vörur, hólf, birgðageymslur eða víddir.
5. Velja hnappinn **Í lagi**.

> [!NOTE]  
> Birgðafærslur eru unnar samkvæmt upplýsingunum sem tilgreindar voru og línur eru stofnaðar í raunbirgðabókinni. Taka skal eftir að  **reiturinn Magn (raunbirgðir)**  er með sama magn og  **reiturinn Magn (útreiknað)** . Ekki þarf að færa inn talda magnið fyrir vörur þar sem þessi gildi stemma. Ef magnið sem var talið frábrugðið er hins vegar fært inn magnið sem var talið.

### <a name="to-print-the-report-to-be-used-when-counting"></a>Prenta skýrsluna sem verður notuð við talningu

1.  **Á síðunni Raunbirgðabók**  með útreiknuðum áætluðum birgðum er valið  **prentaðgerðin** .
2.  **Á síðunni Raunbirgðalisti**  vöruhúss er tilgreint hvort skýrslan sýni útreiknaða magn og birgðavörur eftir rað-og lotunúmerum.
3. Setjið upp afmarkanir ef aðeins á að prenta skýrsluna fyrir ákveðnar vörur, hólf, birgðageymslur eða víddir.
4. Veldu  **Prenta**.

Starfsmenn vöruhúss geta nú treyst birgðum og skráð hvaða mismun sem er á prentuðu skýrslunni.

> [!NOTE]
> Það geta liðið nokkrir dagar áður en prentaðar skýrslur koma aftur fyrir lokavinnslu og bókun. Þegar þú tilgreinir og bókar raunverulegar birgðir leiðréttir forritið birgðir til að endurspegla muninn á milli væntanlegrar og raunverulegrar talningar. Það verður að halda upphaflega reiknaða færslubókarlínu og endurreikna ekki væntanlegar birgðir þar sem áætlaðar birgðir kunna að breytast og leiða til rangra birgðastita. Ef þú þarft að gefa út margar skýrslur, eins og fyrir mismunandi staði eða vöruhóp, verður þú að búa til og halda aðskildum bókarkeyrslum.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-basic-warehouse-configurations"></a>Til að færa inn og bóka raunverulegar taldar birgðir í grunngerð vöruhúss.

1. Í hverri línu á  **síðunni Raunbirgðabók**  þar sem raunbirgðatalningin, sem Talning efnislegra birgða, ákvarðar, er önnur en útreiknaða magnið skal færa inn raunverulegar birgðir á lager í  **reitnum Magn (raunbirgðir)** .
  
  > [!NOTE]  
  > Ef efnislegar talningar Sýna mismun af völdum vara sem bókaðar eru með röngum stöðum, skal ekki færa mismuninn inn í raunbirgðabókina. Þess í stað er notuð endurflokkunarbók eða flutningspöntun til að beina vörunum á rétta staði. 

2. Til að leiðrétta reiknað magn í raunverulegt talið magn skal velja aðgerðina **Bóka**.

    Bókun stofnar birgðafærslur og efnislegar birgðafærslur. Opnið Vörukortasíðuna fyrir vöruna til að finna efnislegar birgðafærslur. <!--Where are they shown on an item?-->

3. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.
4. Til að sannreyna talningu skaltu opna Vörukortasíðuna fyrir vöruna og velja  **raunbirgðafærslurnar** . <!--I don't see this action -->

### <a name="to-calculate-the-expected-inventory-in-advanced-warehouse-configurations"></a>Til að reikna væntanlegar birgðir í grunngerð ítarlegs vöruhúss

Samstilla birgðahöfuðbók og vöruhús <!--warehouse what?--> áður en efnislegar birgðir eru talsverðar. Að öðrum kosti er það sem bókað er í raunbirgðabók og birgðahöfuðbók mun efnislegar birgðaniðurstöður ásamt öðrum vöruhúsaleiðréttingum fyrir vörurnar.  [Frekari upplýsingar er að samstilla magn í birgðahöfuðbók og vöruhúsi](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **Raunbirgðabók** vöruhúss og velja tengdan tengil.  
2. Velja skal  **útreikning birgðaaðgerðar**  til að opna  **vöruhúsaafhendingu. Reikna Birgðasíðu** .  
3. Afmarkanirnar eru stilltar til að tilgreina vörur sem á að telja í færslubókinni og velja  **síðan í lagi**.

   [!INCLUDE [prod_short](includes/prod_short.md)] stofnar línu fyrir hvert hólf sem uppfyllir síukröfurnar. Hægt er að eyða línum en ef óskað er eftir að bóka niðurstöðurnar sem raunbirgðir skal telja vöruna í öllum hólfum sem innihalda hana.  

   Ef aðeins er um að ræða vöru í sumum hólfum en ekki öðrum er hægt að færa inn mismun og bóka þau í birgðabókina síðar með því að  **nota útreikning vöruhúsaaðgerðinnar. Leiðréttingaraðgerð** . <!--I don't see this action-->  

### <a name="to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations"></a>Til að færa inn og bóka raunverulegar taldar birgðir í grunngerð ítarlegs vöruhúss.

1.  **Í síðunni Raunbirgðabók**  vöruhúss er raunverulegt magn fært inn í  **reitinn Magn (raunbirgðir))** .  

    > [!NOTE]  
    >   **Reiturinn Magn (útreiknað)**  er fylltur út eftir hólfafærslum. Þetta magn er afritað í  **reitinn Magn (efnislegt)**  í hverri línu. Ef magnið í þessum reitum er ekki í samræmi skal færa inn raunverulegt magn.  

2. Þegar allt raunverulegt magn hefur verið fært inn skal velja  **aðgerðina skrá** .  

    Þegar færslubókin er skráð eru  [!INCLUDE [prod_short](includes/prod_short.md)]  stofnaðar tvær vöruhúsafærslur í vöruhúsadagbók fyrir hverja línu sem var talin og skráð:  

    - Ef reiknað og raunverulegt magn er mismunandi er neikvætt eða jákvætt magn skráð fyrir hólfið og jöfnunarmagn bókað í leiðréttingarhólfi staðsetningar.  
    - Ef útreiknað magn jafngildir líkamlegu magni,  [!INCLUDE [prod_short](includes/prod_short.md)]  skráir  **0**  fyrir bæði hólfið og leiðréttingarhólfið. 

Þegar efnislegar birgðir eru skráðar er ekki hægt að bóka í vöruna, efnislegar birgðir eða virðisfjárhag. Hins vegar eru færslurnar tiltækar til afstemmingar þegar þörf krefur. Til að halda magni nákvæmt, eftir að vörur hafa verið talningu í öllum hólfum, skal bóka niðurstöðurnar sem efnislegar birgðir birgða <!--physical inventory journal-->.  [Frekari upplýsingar er að samstilla magn í birgðahöfuðbók og vöruhúsi](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

## <a name="to-do-cycle-counting"></a>Talning á tíðahring

Þú getur treyst atriðum eins oft og þú vilt. Til dæmis vegna þess að þau eru verðmætari í sér, eða vegna þess að þau eru snögg að moða og stórum hluta af þínu fyrirtæki. Tilgreinið Talningatíðni með því að úthluta sérstökum talningartímabilum á vörurnar.

Hægt er að gera tíðahringatalningu á eftirfarandi hátt, allt eftir uppsetningu vöruhúss. Frekari upplýsingar um  [uppsetningu vöruhúsastjórnunar](warehouse-setup-warehouse.md).  

- Ef birgðageymslan notar ekki beinan frágang og tínslu er notuð  **Raunbirgðabókarsíða** . Skrefin eru svipuð talningu efnislegra birgða án ferlis.  
- Ef birgðageymslan notar beinan frágang og tínslu eru notaðar  **blaðsíður raunbirgðabókar**  vöruhúss. Síðan skal  **nota síðuna birgðabækur**  til að keyra  **Leiðréttingaraðgerðina**  Reikna vöruhúsaaðgerð. <!--we should say what to do on each of these pages-->  

### <a name="to-set-up-counting-periods"></a>Talningatímabil sett upp

Talning efnislegra birgða er vanalega endurtekin verk, t.d. mánaðarlega, ársfjórðungslega eða árlega. Hægt er að setja upp talningartímabil birgða og úthluta hverri vöru. Að því  **loknu skal nota aðgerðina Reikna talningartímabil**  á  **síðunni raunbirgðabókarsíða**  til að stofna sjálfkrafa línur fyrir vörurnar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **talningartímabil** raunbirgða og velja síðan tengda tengilinn.  
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-assign-a-counting-period-to-an-item"></a>Talningatímabili úthlutað á vöru

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
2. Varan sem úthluta á talningartímabili er valin.  
3.  **Í reitnum kóti**  talningartímabils Vefys invt, er talningartímabilið valið.  

> [!NOTE]
> Ef skipt er um talningartímabil birtast boð um niðurstöður breytingarinnar. Velja  **skal Já**  til að breyta kóðanum og reikna út fyrsta talningartímabilið fyrir vöruna. Næst þegar valið er að reikna út talningatímabil í raunbirgðabók vöruhúss, birtist varan sem lína á síðunni **Vöruval raunbirgða**. Þá er hægt að telja vöruna reglulega.

### <a name="to-start-a-count-based-on-counting-periods-in-basic-warehouse-configurations"></a>Talning á grundvelli talningartímabila í grunnvöruvöruhúsi afbrigðin hafin

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **Raunbirgðabók** og velja síðan tengda tengilinn.
2. Veljið **Reikna talningartímabil** aðgerðina.

     **Vefin. Invt. Vöruvalssíða**  sýnir vörur sem telja þarf í samræmi við talningatímabil þeirra.
3. Telja raunbirgðir. Frekari upplýsingar eru í  [til að telja efnislegar birgðir](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).

### <a name="to-start-a-count-based-on-counting-periods-in-advanced-warehouse-configurations"></a>Talning í byrjun byggð á talningartímabilum í ítarlegum vöruhúsaafbrigðum

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **Raunbirgðabók** vöruhúss og velja tengdan tengil.  
2. Veljið **Reikna talningartímabil** aðgerðina.

     **Vefin. Invt. Vöruvalsnámskeið**  Sýna atriði þarf að telja upp í samræmi við talningatímabil þeirra.
3. Telja raunbirgðir. Frekari upplýsingar eru í  [til að telja efnislegar birgðir](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).  

   > [!NOTE]  
   > Teljið vöruna í öllum hólfum sem innihalda hana. Ef hólfalínunum var eytt sem voru sóttar til talningar á  **birgðastöð raunbirgða**  verður Talning röng þegar hún er bókuð í raunbirgðabók.  

## <a name="to-adjust-the-quantity-of-one-item"></a>Magn einnar vöru leiðrétt

Þegar búið er að gera efnislega talningu á vöru skal nota  **leiðrétta birgðaaðgerðina**  til að skrá raunverulegt birgðamagn.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.
2. Veljið þá vöru sem leiðrétta birgðir fyrir og veldu svo **leiðrétta birgðir** aðgerðina.
3.  **Í nýju birgðasvæðinu fyrir birgðageymsluna er niðurstaða talnakinnar**  færð inn.
4. Velja hnappinn **Í lagi**.

<!-- I don't see a "Quantity on Hand" field on the Item Card page. Should this point to the options for viewing availability?

The item’s inventory is adjusted. The new quantity is shown in the **Quantity on Hand** field on the **Item Card** page.-->

Einnig er hægt að nota  **leiðrétta birgðaaðgerðina**  sem auðveld leið til að bæta keyptum vörum við birgðir ef ekki eru notaðir innkaupareikningar eða pantanir til að skrá innkaup. Frekari upplýsingar eru á [Skrá innkaup](purchasing-how-record-purchases.md).

> [!NOTE]  
> Eftir að birgðir hafa verið leiðrétt, uppfærist gildandi gildi hennar. Nánari upplýsingar eru í [Endurmat birgða](inventory-how-revalue-inventory.md).

### <a name="to-adjust-the-quantities-of-multiple-items-in-basic-warehouse-configurations"></a>Til að leiðrétta magn margra atriða í grunnvöruhúsafbrigðum

 **Á birgðabókarsíðu**  er hægt að bóka vörufærslur beint til að leiðrétta birgðir vegna innkaupa, sölu og jákvæðra eða neikvæðra breytinga án þess að nota skjöl.

Ef birgðabókin er oft notuð til að bóka sömu eða svipaðar færslubókarlínur, til dæmis fyrir efnisnotkun,  **getur staðlaða-vörubókarsíðan**  gert þessa endurteknu vinnu auðveldari. Frekari upplýsingar eru í [Vinna með Staðlaðar færslubækur](ui-work-general-journals.md#work-with-standard-journals).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðabækur** og velja síðan viðkomandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3.  **Veljið aðgerðina Bóka**  til að leiðrétta magnið.

### <a name="to-adjust-bin-quantities-in-advanced-warehouse-configurations"></a>Leiðrétta hólfamagn í grunngerð ítarlegs vöruhúss

Ef birgðageymslan notar beinan frágang og pickss skal nota  **síðuna vöruhúsakerði**  til að bóka óáætlaðar jákvæðar og neikvæðar Magnbreytingar. Til dæmis, fyrir vörur bókaðar sem vantar sem sýna óvænt, eða tap vegna rofage.  

Vörufærslubækur vöruhúsa gefa þér meira magn leiðréttinga til að gera magnið þitt nákvæmara. Vöruhúsið veit hve margar vörur eru í hendi og hvar þær eru geymdar, en hver leiðrétting er ekki bókuð á birgðabókinn. Nafnalisti eða debet eru gerð í raunhólfinu með magnleiðréttingunni. Mótfærsla er gerð í leiðréttingarhólfi. Leiðréttingarhólfið er sýndarhólf án raunverulegu atriðunum. Sýndarhólfið í  **invt er tilgreint. Reiturinn Kóti**  leiðréttingarhólfs á  **síðum Birgðageymsluspjald** .

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **vöruhúsabók** vöruhúss og velja síðan tengda tengilinn.  
2. Upplýsingar fyrir hausinn eru færðar inn.  
3. Í reitnum  **Vörunr.** Veljið vöruna í línunni.  
4. Hólfið þar sem aukavörurnar eru settar inn eða þar sem vörur vantar.  
5.  **Í reitnum Magn**, ef þú hefur fundið aukavörur, færðu inn jákvætt magn. Vanti vörur er ritað neikvætt magn.  
6. Velja aðgerðina **Skrá**.

## <a name="to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries"></a>Samstilla leiðréttar vöruhúsafærslur við tengdar birgðabókafærslur

Bóka færslur leiðréttingarhólfs í birgðahöfuðbók fyrir tímabilin sem þú skilgreinir. Sum fyrirtæki bóka Daglegar leiðréttingar á birgðahöfuðbók, á meðan aðrir temja sjaldnar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðabók** og velja síðan viðkomandi tengil.  
2. Reitirnir eru fylltir út fyrir hverja línu.  
3.  **Veljið leiðréttingaraðgerð**  vöruhúss og bætið svo við afmörkunum á  **leiðréttingarsíðu**  vöruhúss. Leiðréttingar eru aðeins reiknaðar fyrir færslurnar í leiðréttingarhólfinu sem standast síukröfurnar.  
4. Á flýtiflipanum **Valkostir** er tala færð handvirkt inn í reitinn **Númer fylgiskjals**. Þar sem engar númeraraðir hafa verið settar upp fyrir þessa keyrslu skal nota númeraskema sem sett er upp í vöruhúsinu eða færa inn dagsetninguna og upphafsstafi notanda á eftir.  
5. Velja **Í lagi**. Jákvæðu og neikvæðu leiðréttingarnar eru lagðar saman fyrir hverja vöru og línur eru stofnaðar í birgðabókarbókinni.  
6. Bóka skal línurnar til þess að færa mismun á magni inn í birgðahöfuðbók. Samsvörunum í hólfunum og birgðafjárhagnum er nú samsvara.  

## <a name="see-also"></a>Sjá einnig .

[CountInventory með skjölum](inventory-how-count-inventory-with-documents.md)  
[Birgðir](inventory-manage-inventory.md)  
[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
