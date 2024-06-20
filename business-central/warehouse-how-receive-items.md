---
title: Taka á móti vörum
description: Þessi hluti er yfirlit yfir mismunandi leiðir til að taka á móti vörum í vöruhúsi með vöruhúsamóttöku.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 06/06/2024
ms.search.form: '5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008'
ms.service: dynamics-365-business-central
---
# Taka á móti vörum með vöruhúsamóttökum

Vörur [!INCLUDE[prod_short](includes/prod_short.md)] eru mótteknar og gengið frá þeim með einni af fjórum aðferðum eins og lýst er í eftirfarandi töflu.

|Aðferð|Ferli á innleið|Krefjast móttöku|Krefjast frágangs|Flóknarastig (Fræðast meira um [vöruhúsakerfisyfirlit](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|||Engin sérstök vöruhúsaaðgerð.|  
|Á|Bóka móttöku og frágang frá birgðafrágangsskjali||Kveikt|Grunnur: Pöntun-fyrir-pöntun.|  
|U|Bóka móttöku og frágang frá vöruhúsamóttökuskjali|Kveikt||Grunnur: Bókuð móttaka/sending í mörgum pöntunum.|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali|Kveikt|Kveikt|Ítarlegt|  

Nánari upplýsingar um hvernig meðhöndla á vörur á innleið eru í [Vöruhúsaflæði á innleið](design-details-inbound-warehouse-flow.md).

Eftirfarandi grein vísar til aðferða C og D í fyrri töflu.

## Taka á móti vörum með vöruhúsamóttöku

Þegar vörur berast í vöruhús sem er sett upp til að vinna vöruhúsamóttökur verður að sækja línur útgefna upprunaskjalsins sem ræsti móttökuna. Ef hólf eru notuð er annaðhvort hægt að samþykkja sjálfgefna hólfið eða tilgreina hólfið sem setja á vörurnar í. Hið síðarnefnda getur verið nauðsynlegt þegar vara berst í fyrsta skipti. Síðan skal færa inn magn varanna sem tekið hefur verið á móti og bóka móttökuna.  

Hægt er að stofna vöruhúsamóttöku á tvo vegu:

* Á ýta tísku, þegar vinna er unnin á grundvelli pöntun fyrir hverja pöntun. Velja skal aðgerðina **Stofna vöruhúsamóttöku** í upprunaskjalinu, svo sem Innkaupapöntun, Vöruskilapöntun sölu eða Millifærslupöntun til að stofna vöruhúsamóttöku fyrir eitt upprunaskjal.
* Á toga í tísku þar sem aðgerðin **Gefa út** er notuð í upprunaskjalinu, svo sem innkaupapöntun, söluvöruskilapöntun eða millifærslupöntun til að gefa skjalið út í vöruhúsið. Starfsmaður í vöruhúsi stofnar vöruhúsamóttöku **fyrir** eitt eða mörg útgefin upprunaskjöl. Eftirfarandi ferli lýsir því hvernig vöruhúsamóttaka er stofnuð á toga í tísku. Eftirfarandi ferli lýsir því hvernig vöruhúsamóttaka er stofnuð á toga í tísku.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsamóttökur**, velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  

    Reiturinn **Kóti** birgðageymslu á flýtiflipanum **Almennt er fylltur** út. Þegar upprunaskjalalínur eru sóttar er eitthvað af upplýsingunum afritað í hverja línu.

    Í birgðageymslu þar sem krafist er hólfa er reiturinn **Hólfkóti fylltur** út. Allt eftir uppsetningunni [!INCLUDE[prod_short](includes/prod_short.md)]  er hægt að bæta við hólfakótanum fyrir notandann. Nánari upplýsingar um [svæðis- og hólfakóta](warehouse-how-receive-items.md#zone-and-bin-codes).  

3. Hægt er að sækja upprunaskjal á tvo vegu:

    1. Valið er **Sækja upprunaskjöl** aðgerð. Síðan **Upprunaskjöl - Á innleið** opnast. Hér er hægt að velja eitt eða fleiri upprunaskjöl sem gefin eru út í vöruhús sem þarfnast móttöku.
    2. Velja skal **Nota afmarkanir til að sækja uppr.skjöl.** aðgerðina. Síðan **Afmarkanir til að sækja upprunaskjöl - Á innleið** opnast. Hér er hægt að velja Upprunaskjalsafmörkun og keyra hana. Öllum útgefnum upprunaskjalslínum sem uppfylla afmörkunarskilyrðin er bætt við síðuna **Vöruhúsamóttaka** . Nánari upplýsingar um hvernig afmarkanir [eru notaðar til að sækja upprunaskjöl](warehouse-how-receive-items.md#how-to-use-filters-to-get-source-documents).

4. Stilla magnið sem á að taka á móti.

     **Í reitnum Magn til móttöku** er útistandandi magn fyrir hverja línu, en hægt er að breyta magninu eftir þörfum. 

    Til að stilla gildið í reitnum **Magn til móttöku** á öllum línum á núll skal velja aðgerðina **Eyða magni til móttöku** . Til dæmis getur verið gagnlegt að stilla magnið á núll ef strikamerkisskanni er notaður til að uppfæra magnið sem var móttekið. Til að bæta útistandandi magni úr upprunaskjalinu aftur skal velja aðgerðina **Sjálfg. magn til móttöku** .  

    Á vöruhúsamóttökuskjali þar sem móttekið magn er hærra en pantað er fært inn magnið sem var móttekið í reitinn **Magn til móttöku** . Ef aukningin er innan vikmarkanna sem tilgreind eru með úthlutaðum ofmóttökukóta **uppfærist reiturinn Magn** yfirmóttöku til að sýna magnið sem farið er fram úr gildinu í reitnum **Magn** . Ef hækkunin er yfir vikmörkunum er ofmóttakan ekki leyfð.

5. Bóka vöruhúsamóttökuna. Magnreitirnir eru uppfærðir á upprunaskjölunum og vörunum er bætt við birgðir.  

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

    > [!TIP]
    > Ef vöruhúsafrágangur er notaður, sem vísar til aðferðar D í töflunni í upphafi þessarar greinar, eru vörurnar mótteknar en ekki hægt að tína þær fyrr en gengið hefur verið frá þeim. Nánari upplýsingar um frágang á vörum eru notaðar til að [ganga frá vörum með vöruhúsafrágangi](warehouse-how-to-put-items-away-with-warehouse-put-aways.md).
    >
    > Að öðrum kosti skal íhuga aðgerðina **Bóka og prenta** . Aðgerðin bókar móttökuna og prentar hana sem frágangsleiðbeiningar sem sýna hvar á að setja vöruna.

    > [!NOTE]  
    > Ef hjáskipun er notuð í vöruhúsinu er hægt að athuga hvort hægt sé að hjáskipa vörum án þess að ganga frá þeim. Nánari upplýsingar um hjáskipun fást með því að fara í [Hjáskipunarvörur](warehouse-how-to-cross-dock-items.md).

## Hvernig afmarkanir eru notaðar til að sækja upprunaskjöl

Úr vöruhúsamóttöku er hægt að nota **Afmarkanir til að sækja upprunaskjöl.** síðu til að sækja útgefnu upprunaskjalslínurnar sem tilgreina vörurnar sem á að taka á móti.

1. Í vöruhúsamóttökunni **skal velja Nota afmarkanir til að sækja uppr.skjól.** Aðgerð.
2. Til að setja upp nýja afmörkun er lýsandi kóti færður inn í reitinn **Kóti** og smellt á **Breyta** aðgerðina.

    Síðan Upprunaskjalsafmörkunarspjald **- Síðan Á innleið** birtist.

3. Afmarkanirnar eru notaðar til að skilgreina tegund upprunaskjalslína sem á að sækja. Til dæmis er hægt að velja tegundir upprunaskjala, t.d. innkaupa- eða millifærslupantanir.
4. Veljið **Keyra**.  

Öllum útgefnum upprunaskjalslínum sem uppfylla afmörkunarskilyrðin er bætt við **síðuna Vöruhúsamóttaka** þar sem afmarkanirnar voru gerðar virkar.

Hægt er að búa til ótakmarkaðan fjölda af afmörkunarsamsetningum. Afmarkanir eru vistaðar í **afmörkunum til að sækja upprunaskjöl.** og þær eru tiltækar næst þegar þörf krefur. Hægt er að breyta skilyrði hvenær sem er með því að smella á **Breyta** aðgerðina.

## Svæðis- og hólfakótar

Ef taka á við vörum með aðra vöruhúsaflokkskóta en flokkskóta hólfsins í reitnum **Hólfkóti** á fylgiskjalshausnum er reiturinn Hólfkóti **á hausnum hreinsaður** áður en upprunaskjalslínurnar eru sóttar fyrir vörurnar.  
<!-- TBD, table with comparison of various options-->

Ef hólf eru áskilin fyrir birgðageymslu er svæðis- og hólfakótum bætt við vöruhúsamóttökuskjöl á eftirfarandi hátt:

* Fyrir ítarlegar grunnstillingar sem nota beinan frágang og tínslu [!INCLUDE [prod_short](includes/prod_short.md)]  er kóti móttökuhólfsins notaður á síðunni **Birgðageymsluspjald** fyrir birgðageymsluna. Ef móttökuhólfskóti er ekki tilgreindur er ekkert hólf tilgreint. Ef vöru- og móttökuhólfin eru ekki eins er kóti móttökuhólfsins auður.
* Í öðrum skilgreiningum, ef kóti móttökuhólfs er ekki tilgreindur, [!INCLUDE [prod_short](includes/prod_short.md)]  notar hólfakótinn úr upprunaskjalinu.

## Sjá einnig .

[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
