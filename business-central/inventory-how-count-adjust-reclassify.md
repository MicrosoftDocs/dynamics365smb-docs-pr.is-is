---
title: 'Telja, leiðrétta og endurflokka birgðir'
description: Læra að gera efnislega talningu og gera leiðréttingar og endurflokkanir.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 05/24/2024
ms.custom: bap-template
---
# Telja, leiðrétta og endurflokka birgðir með því að nota færslubækur

Til að tryggja að magn notanda sé rétt er talið efnislega allar vörur í birgðaskrá. Sum fyrirtæki telja árlega raunbirgðatalningu og önnur telja öll eða aðeins sumar vörur oftar. Þegar vörur hafa verið taldar skal nota færslubækur til að bóka raunverulegt magn í fjárhag. Til dæmis þegar birgðir eru metnar í lok tímabils.

Ef telja á sumar vörur oftar en aðrar, ef til vill vegna virðis þeirra, er reglubundin talning notuð. Til að telja reglubundna talningu skal úthluta vörunum sérstökum talningatímabilum. Fræðast meira um [reglubundna talningu](inventory-how-count-adjust-reclassify.md#to-do-cycle-counting).

Til að leiðrétta magn eftir raunbirgðatalningu eða annan tilgang er birgðabók notuð til að breyta birgðafærslum án þess að bóka viðskipti. Einnig er hægt að leiðrétta magn einnar vöru á birgðaspjaldi.

Nota skal endurflokkunarbók til að breyta eigindum birgðafærslna. Dæmigerðar eigindir til endurflokkunar eru víddir og söluherferðarkótar. Einnig er hægt að nota endurflokkunarbækur til millifærslu með því að endurflokka hólfa- og birgðageymslukóta. Sérstök skref eiga við þegar þú vilt endurflokka rað- eða lotunúmer og lokadag þeirra. Frekari upplýsingar, sjá [Vinna með rað- og lotunúmer](inventory-how-work-item-tracking.md).

> [!NOTE]
> Í mörgum þrepum eru vörur skráðar í hólf sem vöruhúsafærslur, ekki sem birgðafærslur. Þess vegna er talning, leiðrétt og endurflokkun í vöruhúsabókum sem styðja hólf. Síðan er nýju eða breyttu vöruhúsafærslurnar samstilltar við tengdar birgðafærslur til að endurspegla breytingar á birgðamagni og gildum.

[!INCLUDE [edit-in-excel](includes/edit-in-excel.md)]

## Talning raunbirgða

Til að kanna hvort skráð magn sé það sama og raunbirgðir á lager er talið raunbirgðir taldar. Það er að telja raunverulegar vörur á lager. Telja gerast yfirleitt í lok reikningsárs en sum fyrirtæki telja vörur oftar. Ef munur er á því er raunverulegt magn bókað á birgðareikningana áður en birgðir eru verðmetnar.

> [!NOTE]
> Í þessu ferli er því lýst hvernig á að gera raunbirgðir með því að nota færslubók á síðunni **Raunbirgðabók** . Hægt er að nota skjöl á síðunum **Raunbirgðapöntun** og **Raunbirgðaskráning** . Þessi skjöl bjóða upp á meiri stjórn og stuðning við að dreifa talningarvinnu til margra starfsmanna. Nánari upplýsingar um [talningu birgða með skjölum](inventory-how-count-inventory-with-documents.md).<br /><br />
> Bent er á að ekki er hægt að nota skjalamiðuðu aðgerðina til að telja vörur í hólfum eða vöruhúsafærslum.

Talningarferlið felur einnig í sér eftirfarandi verkhluta:

- Reikna væntanlegar birgðir.
- Prenta skýrsluna sem á að nota við talninguna.
- Færa inn og bóka raunverulegt magn.

Telja raunbirgðir á einn af eftirfarandi leiðum, allt eftir uppsetningu vöruhússins. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).  

- Ef birgðageymslan notar ekki beinan frágang og tínslu skal nota síðuna **Raunbirgðabók** . Ferlið er svipað raunbirgðum án reglubundinnar talningar.  
- Ef birgðageymslan notar beinan frágang og tínslu er síðan Raunbirgðabók **vöruhúss** notuð. Síðan Birgðabækur er síðan notuð **til að keyra aðgerðina** Reikna vöruhúsaleiðréttingu **.**  <!--We should say what to do on each of these pages.-->

### Væntanlegar birgðir reiknaðar í grunnskilgreiningum vöruhúss

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **raunbirgðabækur** og velja síðan viðeigandi tengil.
2. Veljið aðgerðina **Reikna Birgðir**.
3. Á síðunni **Reikna birgðir** tilgreinið skilyrði sem nota á til að stofna færslubókarlínur, t.d. hvort þær eigi að innihalda vörur sem hafa engar birgðir skráðar.
4. Stilla afmarkanir ef aðeins á að reikna birgðir fyrir ákveðnar vörur, hólf, birgðageymslur eða víddir.
5. Velja hnappinn **Í lagi**.

> [!NOTE]  
> Birgðafærslur eru unnar samkvæmt upplýsingunum sem voru tilgreindar og línur eru stofnaðar í raunbirgðabókinni. Bent er á að reiturinn **Magn (raunbirgðir)** hefur sama magn og reiturinn **Magn (reiknað)** . Ekki þarf að færa inn talið magn vara þar sem þessi gildi samsvara. Ef magnið sem talið er er hins vegar frábrugðið er fært inn magnið sem talið var.

### Prenta skýrsluna sem verður notuð við talningu

1. Á síðunni **Raunbirgðabók** sem inniheldur reiknaðar væntanlegar birgðir er aðgerðin **Prenta** valin.
2. Á síðunni **Raunbirgðalisti** vöruhúss er tilgreint hvort skýrslan sýni reiknað magn og birgðir eftir rað- og lotunúmerum.
3. Setjið upp afmarkanir ef aðeins á að prenta skýrsluna fyrir ákveðnar vörur, hólf, birgðageymslur eða víddir.
4. Valið er **Prenta**.

Starfsmenn vöruhúss geta nú talið birgðir og skráð mismun á prentuðu skýrslunni.

> [!NOTE]
> Það geta liðið nokkrir dagar áður en prentaðar skýrslur koma aftur fyrir lokavinnslu og bókun. Þegar þú tilgreinir og bókar raunverulegar birgðir leiðréttir forritið birgðir til að endurspegla muninn á milli væntanlegrar og raunverulegrar talningar. Halda verður upphaflega útreiknuðum færslubókarlínum og ekki endurreikna áætlaðar birgðir þar sem áætlaðar birgðir geta breyst og leitt til ranga birgðastiga. Ef þú þarft að gefa út margar skýrslur, eins og fyrir mismunandi staði eða vöruhóp, verður þú að búa til og halda aðskildum bókarkeyrslum.

### Til að færa inn og bóka raunverulegar taldar birgðir í grunngerð vöruhúss.

1. Í hverri línu á síðunni **Raunbirgðabók** þar sem tiltækar birgðir, eins og raunbirgðatalningin ákvarðar, er önnur en reiknað magn, eru tiltækar raunbirgðir færðar í reitinn **Magn (raunbirgðir).** .
  
  > [!NOTE]  
  > Ef raunbirgðatalning sýnir mismun vegna vara sem bókaðar eru með röngum birgðageymslum er mismunurinn ekki færður inn í raunbirgðabókina. Þess í stað skal nota endurflokkunarbók eða millifærslupöntun til að beina vörunum á réttar birgðageymslur. 

2. Til að leiðrétta reiknað magn í raunverulegt talið magn skal velja aðgerðina **Bóka**.

    Bókun stofnar birgðafærslur og raunbirgðafærslur. Opna skal síðuna Birgðaspjald fyrir vöruna til að finna raunbirgðafærslur hennar. <!--Where are they shown on an item?-->

3. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.
4. Til að votta talningu er síðan Birgðaspjald fyrir vöruna opnuð og aðgerðin **Raunbirgðafærslur** valin. <!--I don't see this action -->

### Til að reikna væntanlegar birgðir í grunngerð ítarlegs vöruhúss

Samstilla birgðabók og vöruhús <!--warehouse what?--> áður en taldar eru raunbirgðir. Annars er það sem bókað er í raunbirgðabókina og birgðabókin niðurstöður raunbirgðabókarinnar ásamt öðrum vöruhúsaleiðréttingum fyrir vörurnar. Fræðast meira um [samstillingu magns í birgðahöfuðbók og vöruhúsi](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Raunbirgðabók** vöruhúss og velja viðeigandi tengil.  
2. Velja skal aðgerðina **Reikna birgðir** til að opna vöruhúsaaðgerðina **. Síðuna Reikna birgðir** .  
3. Afmarkanirnar eru stilltar til að tilgreina vörurnar sem telja á í færslubókinni og velja **síðan Í lagi**.

   [!INCLUDE [prod_short](includes/prod_short.md)] stofnar línu fyrir hvert hólf sem uppfyllir afmörkunarþarfirnar. Hægt er að eyða línum en ef bóka á niðurstöðurnar sem raunbirgðir skal telja vöruna í öllum hólfum með henni.  

   Ef aðeins er talin vara í sumum hólfum en ekki öðrum er hægt að færa inn mismun og bóka þær á **síðuna Birgðabók** síðar með aðgerðinni **Reikna vöruhúsaleiðréttingu** .  

### Til að færa inn og bóka raunverulegar taldar birgðir í grunngerð ítarlegs vöruhúss.

1. Á síðunni **Raunbirgðabók** vöruhúss er magnið fært inn í reitinn **Magn (raunbirgðir).** .  

    > [!NOTE]  
    > Reiturinn **Magn (reiknað)** er fylltur út samkvæmt hólfafærslum. Þetta magn er afritað í reitinn **Magn (raunbirgðir)** í hverri línu. Ef magnið í þessum reitum stemmir ekki er magnið fært inn.  

2. Þegar allt raunverulegt magn hefur verið fært inn skal velja aðgerðina **Dagbók** .  

    Þegar færslubókin [!INCLUDE [prod_short](includes/prod_short.md)]  er skráð eru tvær vöruhúsafærslur stofnaðar í vöruhúsadagbók fyrir hverja línu sem var talin og skráð:  

    - Ef reiknað og raunverulegt magn er annað er neikvætt eða jákvætt magn skráð fyrir hólfið og jöfnunarmagn bókað í leiðréttingarhólf birgðageymslunnar.  
    - Ef reiknaða magnið er jafnt raunmagni skal [!INCLUDE [prod_short](includes/prod_short.md)]  skrá **0** fyrir bæði hólfið og leiðréttingarhólfið. 

Þegar raunbirgðir eru skráðar er ekki bókað á vöruna, raunbirgðirnar eða virðisbókirnar. Færslurnar eru hins vegar tiltækar til afstemmingar eftir þörfum. Til að halda magni nákvæmum skal bóka niðurstöðurnar eftir að vörur eru taldar í öllum hólfum.<!--physical inventory journal--> Fræðast meira um [samstillingu magns í birgðahöfuðbók og vöruhúsi](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

## Regluleg talning

Hægt er að telja vörur eins oft og óskað er eftir. Til dæmis vegna þess að þeir eru verðmætari eða sölumenn. Tilgreina talningartíðnina með því að úthluta vörum sérstökum talningartímabilum.

Hægt er að telja reglubundna talningu á eftirfarandi hátt, allt eftir uppsetningu vöruhússins. Nánari upplýsingar um [uppsetningu vöruhúsastjórnunar](warehouse-setup-warehouse.md).  

- Ef birgðageymslan notar ekki beinan frágang og tínslu er síðan Raunbirgðabók **notuð** . Skrefin eru svipuð talningu raunbirgða án reglubundinnar talningar.  
- Ef birgðageymslan notar beinan frágang og tínslu er síðan Raunbirgðabók **vöruhúss** notuð. Síðan Birgðabækur er síðan notuð **til að keyra aðgerðina** Reikna vöruhúsaleiðréttingu **.**  <!--we should say what to do on each of these pages-->  

### Talningatímabil sett upp

Talning raunbirgða er yfirleitt ítrekunarverkhluti, til dæmis mánaðarlega, ársfjórðungslega eða árlega. Hægt er að setja upp birgðatalningartímabilin sem þörf er á og úthluta einu á hverja vöru. Síðan skal nota aðgerðina **Reikna talningartímabil** á síðunni **Raunbirgðabók** til að stofna sjálfkrafa línur fyrir vörurnar.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **talningartímabil raunbirgða** og velja síðan viðeigandi tengil.  
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Talningatímabili úthlutað á vöru

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
2. Varan sem úthluta á talningartímabili er valin.  
3. Í reitnum **Kóti** talningartímabils raunbirgða er talningartímabilið valið.  

> [!NOTE]
> Ef talningartímabili er breytt birtast upplýsingar um niðurstöður breytingarinnar. Já **er** valið til að breyta kótanum og reikna út fyrsta talningartímabil vörunnar. Næst þegar valið er að reikna út talningatímabil í raunbirgðabók vöruhúss, birtist varan sem lína á síðunni **Vöruval raunbirgða**. Síðan er hægt að telja vöruna reglubundið.

### Talning hafin á talningartímabilum í grunnskilgreiningum vöruhúsa

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **raunbirgðabók** og velja síðan viðeigandi tengil.
2. Veljið **Reikna talningartímabil** aðgerðina.

    Reitirnir **Raunbirgðabirgðir Síðan Vöruval** sýnir vörur sem þarf að telja samkvæmt talningatímabilum þeirra.
3. Telja raunbirgðirnar. Nánari upplýsingar um [talningu raunbirgða](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).

### Telja hafin á talningartímabilum í ítarlegum vöruhúsaskilgreiningum

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Raunbirgðabók** vöruhúss og velja viðeigandi tengil.  
2. Veljið **Reikna talningartímabil** aðgerðina.

    Reitirnir **Raunbirgðabirgðir Síðan Vöruval** sýnir vörur sem þarf að telja samkvæmt talningartímabilum þeirra.
3. Telja raunbirgðirnar. Nánari upplýsingar um [talningu raunbirgða](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).  

   > [!NOTE]  
   > Varan er talin í öllum hólfum með henni. Ef hólfalínum sem voru sóttar til talningar á síðunni **Vöruh. - Raunbirgðir** er eytt verða talningin röng þegar hún er bókuð í raunbirgðabók.  

## Magn einnar vöru leiðrétt

Þegar talning vöru hefur verið talin er aðgerðin **Leiðrétta birgðir** notuð til að skrá raunverulegt birgðamagn.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.
2. Veljið þá vöru sem leiðrétta birgðir fyrir og veldu svo **leiðrétta birgðir** aðgerðina.
3. Í reitinn **Nýjar birgðir** fyrir birgðageymsluna er talningin færð inn.
4. Velja hnappinn **Í lagi**.

<!-- I don't see a "Quantity on Hand" field on the Item Card page. Should this point to the options for viewing availability?

The item’s inventory is adjusted. The new quantity is shown in the **Quantity on Hand** field on the **Item Card** page.-->

Einnig er hægt að nota aðgerðina **Leiðrétta birgðir** sem einfalda leið til að bæta keyptum vörum við birgðir ef ekki eru notaðir innkaupareikningar eða pantanir til að skrá innkaup. Frekari upplýsingar eru á [Skrá innkaup](purchasing-how-record-purchases.md).

> [!NOTE]  
> Þegar birgðir hafa verið leiðréttar er gildandi virði hennar uppfært. Nánari upplýsingar eru í [Endurmat birgða](inventory-how-revalue-inventory.md).

### Til að leiðrétta magn margra vara í einfaldri vöruhúsagrunnstillingu

Á síðunni **Birgðabók** er hægt að bóka birgðafærslur beint til að leiðrétta birgðir vegna innkaupa, sölu og jákvæðra eða neikvæðra breytinga án þess að nota fylgiskjöl.

Ef birgðabókin er oft notuð til að bóka sömu eða svipaðar færslubókarlínur, til dæmis til efnisnotkunar, **getur síðan Stöðluð birgðabók** auðveldað þessa endurteknu vinnu. Frekari upplýsingar eru í [Vinna með Staðlaðar færslubækur](ui-work-general-journals.md#work-with-standard-journals).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðabækur** og velja síðan viðkomandi tengil.
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velja skal aðgerðina **Bóka** til að leiðrétta magnið.

### Leiðrétta hólfamagn í grunngerð ítarlegs vöruhúss

Ef birgðageymslan notar beinan frágang og tínslu er síðan Birgðabók **vöruhúss notuð** til að bóka óáætlaðar jákvæðar og neikvæðar magnbreytingar. Til dæmis, fyrir vörur sem bókaðar eru sem vantar sem birtast óvænt eða tap vegna brots.  

Birgðabækur vöruhúss gera magntölur nákvæmari. Í vöruhúsinu er vitað hversu margar vörur eru tiltækar og hvar þær eru geymdar en hver leiðrétting er ekki bókuð í birgðahöfuðbók. Kredit eða debetfærslur eru gerðar í raunverulega hólfinu með magnleiðréttingunni. Mótfærsla er gerð í leiðréttingarhólfi. Leiðréttingarhólfið er sýndarhólf án raunverulegra vara. Sýndarhólfið er tilgreint í birgðah. **Reiturinn Kóti** leiðréttingarhólfs á **birgðageymsluspjaldssíðum** .

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Birgðabók** vöruhúss og velja síðan viðeigandi tengil.  
2. Upplýsingar fyrir hausinn eru færðar inn.  
3. Í reitnum Vörunr **.** í línunni er varan valin.  
4. Hólfið þar sem viðbótarvörurnar eru settar eða þar sem vörur vantar er fært inn.  
5. Í reitinn **Magn** er fært inn jákvætt magn ef viðbótarvörur finnast. Vanti vörur er ritað neikvætt magn.  
6. Velja aðgerðina **Skrá**.

## Samstilla leiðréttar vöruhúsafærslur við tengdar birgðabókafærslur

Bóka færslur leiðréttingarhólfs í birgðahöfuðbók fyrir tilgreind tímabil. Sum fyrirtæki bóka daglegar leiðréttingar á birgðahöfuðbók á meðan önnur stemma sjalna af.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Birgðabók** og velja síðan viðkomandi tengil.  
2. Reitirnir eru fylltir út fyrir hverja línu.  
3. Veljið aðgerðina **Reikna vöruhúsaleiðréttingu** og bætið síðan við afmörkunum á síðunni **Reikna vöruhúsaleiðréttingu** . Leiðréttingar eru aðeins reiknaðar fyrir færslurnar í leiðréttingarhólfinu sem uppfylla skilyrði afmörkunarinnar.  
4. Á flýtiflipanum **Valkostir** er fyllt út í reitinn Númer fylgiskjals **.** með númeri. Númerið birtist í birgðabókarlínunum.
5. Velja **Í lagi**. Jákvæðar og neikvæðar leiðréttingar eru lagðar saman fyrir hverja vöru og línur eru stofnaðar í birgðabókinni.  
6. Bóka skal línurnar til þess að færa mismun á magni inn í birgðahöfuðbók. Magnið í hólfunum og birgðahöfuðbókinni passa nú.  

## Sjá einnig .

[CountInventory með skjölum](inventory-how-count-inventory-with-documents.md)  
[Birgðir](inventory-manage-inventory.md)  
[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
