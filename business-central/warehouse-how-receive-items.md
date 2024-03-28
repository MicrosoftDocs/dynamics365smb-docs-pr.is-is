---
title: Móttaka vara
description: Þessi grein er yfirlit yfir mismunandi leiðir til að taka á móti vörum í vöruhúsi með vöruhúsamóttöku.
author: brentholtorf
ms.author: bholtorf
ms.topic: how-to
ms.date: 09/02/2022
ms.devlang: al
ms.search.form: '5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008'
ms.service: dynamics-365-business-central
---
# Taka við vörum með vöruhúsamóttökum

Í  [!INCLUDE[prod_short](includes/prod_short.md)] eru vörur afhentar og þær síðan notaðar með einni af fjórum aðferðum, eins og lýst er í eftirfarandi töflu.

|Aðferð|Ferli á innleið|Krefjast kvittana|Krefjandi frágangur|Flókið stig (frekari upplýsingar um  [Vöruhúsakerfi-Yfirlit](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|||Engin sérstök vöruhúsaaðgerð.|  
|Á|Bóka móttöku og frágang frá birgðafrágangsskjali||Kveikt|Grunnur: pöntun-eftir pöntun.|  
|U|Bóka móttöku og frágang frá vöruhúsamóttökuskjali|Kveikt||Grunnur: Samstæða móttöku/skipa bóka fyrir margar pantanir.|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali|Kveikt|Kveikt|Ítarlegt|  

Frekari upplýsingar um hvernig á að afgreiða vörur á innleið er að fara í  [Vöruhúsaflæði á innleið](design-details-inbound-warehouse-flow.md).

Með eftirfarandi grein er átt við aðferðir C og D í fyrri töflunni.

## Taka á móti vörum með vöruhúsamóttöku

Þegar vörur koma í vöruhús sem sett er upp til að vinna vöruhúsamóttökur verður að sækja línurnar af útgefnu upprunaskjalinu sem kveikti kvittunina. Ef hólf eru notuð er annað hvort hægt að samþykkja sjálfgefið hólf eða tilgreina hólf til að setja vörurnar í. Það síðarnefnda gæti verið nauðsynlegt þegar vara er afhent í fyrsta skipti. Því næst Færðu inn magn varanna sem þú fékkst, og bókið móttökunina.  

Hægt er að stofna vöruhúsamóttöku á tvo vegu:

* Á þrýstihátt, þegar vinna er unnin á pöntunargrunni.  **Veljið móttökuaðgerðina Móttaka**  vöruhúss í upprunaskjalinu, svo sem innkaupapöntun, Söluvöruskilapöntun eða flutningspöntun til að stofna vöruhúsamóttöku fyrir eitt upprunaskjal.
* Í togtísku, þar sem úttektaraðgerðin  **er notuð**  í upprunaskjalinu, til dæmis innkaupapöntun, Söluvöruskilapöntun eða flutningspöntun til að losa skjalið við vöruhúsið. Starfsmaður í vöruhúsi stofnar  **vöruhúsamóttöku**  fyrir eitt eða mörg Útgefin upprunaskjöl. Eftirfarandi ferli er lýst hvernig á að stofna vöruhúsamóttöku í togtísku. Eftirfarandi ferli lýsir því hvernig vöruhúsamóttaka er stofnuð í togflutningtísku.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsamóttökur**, velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  

     **Reiturinn birgðageymslukóti**  er  **fylltur út á flipanum Almennt** . Þegar upprunaskjalalínur eru sóttar er eitthvað af upplýsingunum afritað í hverja línu.

    Fyrir birgðageymslu þar sem krafist er hólfa er reiturinn Hólfakóti  **fylltur út** . Hægt er að bæta við kóta hólfakóta eftir uppsetningu [!INCLUDE[prod_short](includes/prod_short.md)] . Frekari upplýsingar á  [svæði og hólfakóta](warehouse-how-receive-items.md#zone-and-bin-codes).  

3. Hægt er að nálgast upprunaskjal á tvennan hátt:

    1. Valið er **Sækja upprunaskjöl** aðgerð.  **Upprunaskjölin-innsend**  síða opnast. Hér er hægt að velja eitt eða fleiri upprunaskjöl sem eru losuð í vöruhús sem útheimta móttöku.
    2. Velja skal **Nota afmarkanir til að sækja uppr.skjöl.** aðgerðina.  **Síur til að fá Upprunadobbin.-opnar innsíða** . Hér er hægt að velja afmörkun upprunaskjals og keyra það. Öllum útgefnum upprunaskjalslínum sem uppfylla afmörkunarskilyrðin er bætt við á  **móttökusíðu vöruhúsamóttöku** .  [Frekari upplýsingar um notkun afmörkunar til að sækja upprunaskjöl](warehouse-how-receive-items.md#how-to-use-filters-to-get-source-documents).

4. Stillið magnið sem á að taka á móti.

     **Í reitnum Magn til móttöku**  er útistandandi magn í hverri línu en hægt er að breyta magninu eftir þörfum. 

    Til að stilla gildið í  **reitnum Magn til móttöku**  í öllum línum á núlli er valið  **Eyða magni til að taka**  við aðgerðinni. Til dæmis er gagnlegt að stilla magnið á núll ef notaður er strikamerkjaskanni til að uppfæra móttekið magn. Ef bæta á útistandandi magni úr upprunaskjalinu aftur er valið  **Magn í <% til Að taka**  við aðgerðinni.  

    Í innhreyfingarskjali vöruhúss þar sem móttekið magn er hærra en pantað er fært inn magnið sem fékkst raunverulega móttekið í  **reitnum Magn til móttöku** . Ef Hækkunin er innan vikmarka sem tilgreind eru í úthlutuðu magni yfir-kvittunarkóða,  **uppfærist reiturinn yfir-innhreyfingar magn**  til að sýna magnið með því að farið er yfir gildið í  **reitnum Magn** . Ef Hækkunin er yfir vikmörkin er ekki leyfilegt að fá yfir-kvittunina.

5. Bóka vöruhúsamóttökuna. Magnsvæðin eru uppfærð á upprunaskjölunum, og vörunum er bætt við birgðir.  

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

    > [!TIP]
    > Ef vöruhúsafrágangur er notaður, sem vísar til aðferðar D í töflunni í upphafi þessarar greinar, er tekið á móti vörunum en ekki hægt að tína þær fyrr en búið er að ganga frá þeim. Til að fræðast meira um frágang vara er farið í að  [ganga frá vörum með vöruhúsafrágangi](warehouse-how-to-put-items-away-with-warehouse-put-aways.md).
    >
    > Annars skal íhuga að  **nota Post og prenta**  aðgerð. Aðgerðin bókar móttökunina og prentar hana út sem frágangsleiðbeiningar sem sýna hvar á að setja vöruna.

    > [!NOTE]  
    > Ef hjáskipun er notuð í vöruhúsinu er hægt að athuga hvort hægt sé að hjáskipunarvörum án þess að leggja þær. Frekari upplýsingar um hjáskipun er að fara í  [hjáskipunarvörur](warehouse-how-to-cross-dock-items.md).

## Hvernig afmarkanir eru notaðar til að sækja upprunaskjöl

Í vöruhúsamóttöku er hægt að nota  **afmarkanirnar til að sækja Upprundocs.** síða til að sækja útgefnar upprunaskjalslínur sem tilgreina vörur sem á að taka á móti.

1. Í vöruhúsamóttöku eru  **notaðar afmarkanir til að sækja src. docs.** aðgerð.
2. Til að setja upp nýja afmörkun er lýsandi kóti færður inn í reitinn **Kóti** og smellt á **Breyta** aðgerðina.

     **Upprunaskjalsíkortið-innsend**  síða birtist.

3. Notið afmarkanir til að skilgreina gerð upprunaskjalslínurnar sem á að sækja. Til dæmis er hægt að velja gerðir upprunaskjala, eins og innkaupa-eða millifærslupantanir.
4. Veljið **Keyra**.  

Öllum útgefnum upprunaskjalslínum sem uppfylla afmörkunarskilyrðin er bætt við á  **síðu vöruhúsamóttöku**  þar sem afmarkanirnar voru virkjaðar.

Hægt er að búa til ótakmarkaðan fjölda af afmörkunarsamsetningum. Afmarkanir eru vistaðar á  **afmörkunum til að fá Upprunadoktor.** blaðsíðu og eru þær aðgengilegar næst þegar þörf er á þeim. Hægt er að breyta skilyrði hvenær sem er með því að smella á **Breyta** aðgerðina.

## Svæði og hólfakóta

Ef taka á á móti vörum með vöruhúsaflokkakóða en klassóta hólfsins í  **reitnum Hólfakóti**  í fylgiskjalshausnum er reiturinn Kóti hólfs  **hreinsaður**  í hausnum áður en upprunaskjalslínur eru sóttar fyrir vörurnar.  
<!-- TBD, table with comparison of various options-->

Ef hólfum er skylt að eiga stað er svæði og hólfakóta bætt við innhreyfingarskjöl vöruhúss sem hér segir:

* Fyrir ítarlegar skilgreiningar sem nota beinan frágang og tínslu er  [!INCLUDE [prod_short](includes/prod_short.md)]  Kóti móttökuhólfs notaður af  **birgðageymsluspjaldinu**  fyrir birgðageymsluna. Ef kóti móttökuhólfs er ekki tilgreindur er ekkert hólf tilgreint. Ef vara og móttökuhólf stemma ekki við er kóti móttökuhólfs auður.
* Í öðrum afbrigðum er kóti móttökuhólfs ekki tilgreindur  [!INCLUDE [prod_short](includes/prod_short.md)]  með því að nota hólfakótann úr upprunaskjalinu.

## Sjá einnig .

[Warehouse Management Overview](design-details-warehouse-management.md)
[Inventory](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
