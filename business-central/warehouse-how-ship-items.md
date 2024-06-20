---
title: Afhenda vörur
description: Í þessari grein er því lýst hvernig á að senda vörur úr vöruhúsinu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 06/10/2024
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
ms.service: dynamics-365-business-central
---

# Afhenda vörur með vöruhúsaafhendingu

Vörur [!INCLUDE[prod_short](includes/prod_short.md)] eru tíndar og afhentar með einni af fjórum aðferðum, eins og lýst er í eftirfarandi töflu.

|Aðferð|Útleiðarferli|Krefjast tínslu|Krefjast afhendingar|Flóknarastig (Fræðast meira um [vöruhúsakerfisyfirlit](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bóka tínsluna og afhendinguna úr pöntunarlínunni|||Engin sérstök vöruhúsaaðgerð.|  
|Á|Bóka tínslu og afhendingu úr birgðatínsluskjali|Kveikt||Grunnur: Pöntun-fyrir-pöntun.|  
|U|Bóka tínslu og afhendingu úr vöruhúsaafhendingarskjali||Kveikt|Grunnur: Bókuð móttaka/sending í mörgum pöntunum.|  
|D|Tínslan er bókuð úr vöruhúsatínsluskjali og afhendingin bókuð úr vöruhúsaafhendingarskjali|Kveikt|Kveikt|Ítarlegt|  

Nánari upplýsingar um afhendingu vara eru notaðar í Vöruhúsaflæði [á útleið](design-details-outbound-warehouse-flow.md).

Þessi grein vísar til aðferða C og D í töflunni. Með báðum aðferðum er byrjað á því að stofna afhendingarskjal úr upprunaskjali viðskipta. Síðan er tilgreindar vörur teknar til fyrir afhendinguna.

Þegar birgðageymsla krefst vöruhúsaafhendinga er hægt að afhenda vörur á grundvelli upprunaskjala sem voru gefin út í vöruhúsið. Ef upprunaskjölum er sleppt eru vörurnar tilbúnar til afgreiðslu í vöruhúsinu. Eftirfarandi eru dæmi um upprunaskjöl:

* Sölupantanir
* Vöruskilapantanir innkaupa
* Millifærslupantanir
* Þjónustupantanir

Hægt er að stofna vöruhúsaafhendingu á tvo vegu:

* Á ýta tísku, þegar vinna er unnin á grundvelli pöntun fyrir hverja pöntun. Velja skal aðgerðina **Stofna vöruhúsaafhendingu** í upprunaskjalinu til að stofna vöruhúsaafhendingu fyrir skjalið.
* Á toga í tísku þar sem aðgerðin **Gefa út** í upprunaskjalinu er notuð til að gefa hana út í vöruhúsið. Starfsmaður í vöruhúsi stofnar vöruhúsaafhendingu **fyrir** eitt eða mörg útgefin upprunaskjöl. Eftirfarandi ferli lýsir því hvernig vöruhúsaafhending er stofnuð á toga í tísku.

## Vörur afhendar með vöruhúsaafhendingarskjali

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsaafhendingar**, velja síðan viðkomandi tengil.  
2. Velja **Nýtt**.  
3. Í reitnum **númer** Er valin númeraröð sem nota á til að stofna kenni fyrir afhendinguna.  
4. Í reitnum **Kóti** birgðageymslu er valin sú birgðageymsla sem verið er að afhenda. 

    Þegar upprunaskjalslínur eru sóttar afritast sumar upplýsingarnar úr birgðageymslunni í hverja línu.  
5. Ef birgðageymslan krefst hólfa er reiturinn **Hólfkóti fylltur** út. Hægt er að bæta við hólfakótanum fyrir notandann, allt eftir uppsetningunni [!INCLUDE[prod_short](includes/prod_short.md)]. Nánari upplýsingar um [svæðis- og hólfakóta](warehouse-how-ship-items.md#zone-and-bin-codes).  
6. Hægt er að sækja upprunaskjalið á tvo vegu:

    * Valið er **Sækja upprunaskjöl** aðgerð. Síðan **Upprunaskjöl - Á útleið** opnast. Hér er hægt að velja eitt eða fleiri upprunaskjöl sem gefin eru út í vöruhús sem krefst afhendingar.
    * Velja skal **Nota afmarkanir til að sækja uppr.skjöl.** aðgerðina.  **Afmarkanirnar til að sækja upprunaskjöl.** síðan opnast. Hægt er að velja upprunaskjalsafmörkun og nota hana. Öllum útgefnum upprunaskjalslínum sem uppfylla afmörkunarskilyrðin er bætt við á síðunni **Vöruhúsaafhending** . Nánari upplýsingar um hvernig afmarkanir [eru notaðar til að sækja upprunaskjöl](warehouse-how-ship-items.md#how-to-use-filters-to-get-source-documents).

    > [!NOTE]
    > Ef birgðageymslan notar hjáskipun og hólf fyrir hverja línu er hægt að fara yfir magn varanna sem settar eru í hjáskipunarhólfin. [!INCLUDE [prod_short](includes/prod_short.md)] reiknar magnið þegar reitirnir í afhendingunni eru uppfærðir. Ef það eru vörurnar í afhendingunni sem verið er að undirbúa er hægt að stofna tínslu fyrir allar vörurnar og ljúka síðan afhendingunni. Frekari upplýsingar eru á [Hjáskipa vörur](warehouse-how-to-cross-dock-items.md).

7. Stofna vöruhúsatínslu. Ef birgðageymslan krefst tínslu er hægt að stofna tínsluaðgerðir fyrir vöruhúsaafhendingar á tvo vegu:

    * Á tísku þar sem aðgerðin **Stofna tínslu** er notuð. Valdar eru línurnar sem á að tína og upplýsingar um tínslurnar tilgreindar. Til dæmis hvaða hólf á að taka úr og setja í og hversu margar einingar á að meðhöndla. Hægt er að forskilgreina hólfin fyrir vöruhúsastaðinn eða forðann.
    * Á toga í tísku, þar sem aðgerðin **Gefa út** er notuð. Á síðunni **Vinnublað** tínslu er aðgerðin **Sækja vöruhúsaskjöl** notuð til að fá úthlutaðar tínslur. Þegar vöruhúsatínslan er fullkomlega skráð eyðast línurnar á vinnublaði **tínslu**. Nánari upplýsingar um [tínsluvörur fyrir vöruhúsaafhendingu](warehouse-how-to-pick-items-for-warehouse-shipment.md).

    > [!TIP]
    > Fyrir birgðageymslu sem ekki krefst tínslu er hægt að prenta vöruhúsaafhendingu og nota hana sem tínslulista.

8. Tilgreina magnið sem á að afhenda.  

    Í birgðageymslu sem krefst tínslu er reiturinn **Magn til afhendingar** uppfærður sjálfkrafa þegar tínslan er skráð. Annars er magnið sem eftir stendur í reitnum **Magn til afhendingar** fyllt út úr hverri línu þegar vöruhúsaafhendingarlína er stofnuð.

    Hægt er að breyta magninu en ekki er hægt að afhenda fleiri vörur en talan í reitnum **Magn eftirstöðvanna** á upprunaskjalslínunni eða reitnum **Tínt** magn ef tínslu er krafist.

    Til að stilla gildið í reitnum **Magn til afhendingar** á öllum línum á núll skal velja aðgerðina **Eyða magni til afhendingar** . Til dæmis getur verið gagnlegt að stilla magnið á núll ef strikamerkisskannar er notaður til að uppfæra afhendingarmagnið. Til að bæta tiltæku magni við afhendingu skal velja aðgerðina **Sjálfg. magn til afhendingar** .

9. Afhendingin er bókuð.

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

## Hvernig afmarkanir eru notaðar til að sækja upprunaskjöl

Úr vöruhúsaafhendingu er hægt að nota **Afmarkanir til að sækja upprunaskjöl.** síðu til að sækja útgefnu upprunaskjalslínurnar sem skilgreina hvaða vörur á að afhenda.

1. Í vöruhúsaafhendingunni skal velja **Nota afmarkanir til að sækja uppr.skjól.** Aðgerð. 
2. Til að setja upp nýja afmörkun er lýsandi kóti færður inn í reitinn **Kóti** og smellt á **Breyta** aðgerðina.

    Síðan Upprunaskjal **- Síðan Afmörkun upprunaskjals - Útleið** opnast.

3. Afmarkanirnar eru notaðar til að skilgreina tegund upprunaskjalslína sem á að sækja. Til dæmis er hægt að velja tegundir upprunaskjala, t.d. sölu- eða millifærslupantanir.
4. Veljið **Keyra**.  

Öllum útgefnum upprunaskjalslínum sem uppfylla afmörkunarskilyrðin er bætt **við síðuna Vöruhúsaafhending** þar sem afmarkanirnar eru settar.

Hægt er að búa til ótakmarkaðan fjölda af afmörkunarsamsetningum. Afmarkanir eru vistaðar í **afmörkunum til að sækja upprunaskjöl.** síðuna og eru tiltækar næst þegar þörf er á þeim. Hægt er að breyta skilyrði hvenær sem er með því að smella á **Breyta** aðgerðina.

## Svæðis- og hólfakótar

Ef hólf eru áskilin í birgðageymslunni er [!INCLUDE [prod_short](includes/prod_short.md)]  stungið upp á svæðis- og hólfakóta á vöruhúsaafhendingarskjalinu.

* Fyrir ítarlegar grunnstillingar þar sem birgðageymsla notar beinan frágang og tínslu [!INCLUDE [prod_short](includes/prod_short.md)]  er hólfið sem tilgreint er í reitnum **Hólfakóti** afhendingar á **birgðageymsluspjaldinu notað**.  **Ef kóti** afhendingarhólfs er ekki tilgreindur er reiturinn auður. Ef varan og afhendingarhólfið stemma ekki er [!INCLUDE [prod_short](includes/prod_short.md)]  afhendingarhólfið skilið eftir autt.
* Í öðrum tilvikum notar [!INCLUDE [prod_short](includes/prod_short.md)]  alltaf hólfið sem tilgreint er í reitnum **Hólfakóti** afhendingar á **birgðageymsluspjaldinu** fyrst. Ef kóti afhendingarhólfs er ekki tilgreindur [!INCLUDE [prod_short](includes/prod_short.md)]  er hólfakótinn notaður úr upprunaskjalinu.

## Meðhöndlun íhluta pantanasamsetninga við vöruhúsaafhendingu

Í samsetningartilvikum skal nota reitinn **Magn til afhendingar** á vöruhúsaafhendingarlínum til að skrá hversu margar einingar eru settar saman. Magnið er bókað samsetningarfrálag þegar vöruhúsaafhendingin er bókuð. Gildið í reitnum **Magn til afhendingar** er núll fyrir aðrar vöruhúsaafhendingarlínur.

Þegar starfsmenn ljúka samsetningu einhvers eða alls magns saman í pöntun skal skrá magnið í reitinn **Magn til afhendingar** á vöruhúsaafhendingarlínunni. Síðan er aðgerðin **Bóka afhendingu** valin. Samsetningarafköstin eru bókuð, þar á meðal íhlutanotkun. Söluafhending fyrir magnið er bókuð fyrir sölupöntunina.

Í samsetningarpöntun má velja **Setja saman í p. vöruh. send. lína** til sjá vöruhúsaafhendingarlínuna.

Þegar vöruhúsaafhendingin hefur verið bókuð eru ýmsir reitir í sölupöntunarlínunni uppfærðir til að sýna framvindu í vöruhúsinu. Eftirfarandi svæði eru einnig uppfærð til að sýna hversu mikið magn samsetningarpantana á eftir að setja saman og afhenda:

* **Útistandandi magn ATO vöruhúss**
* **Útistandandi magn ATO vöruhúss (stofn)**

> [!NOTE]
> Í samsetningaraðstæðum þar sem setja þarf saman hluta af magninu og senda þarf aðra úr birgðum eru tvær vöruhúsaafhendingarlínur stofnaðar. Ein er fyrir er fyrir samsetningarpöntunarmagn, og ein er fyrir birgðamagn.
>
> Magnið sem sett er saman eftir pöntun er meðhöndlað eins og lýst er í þessari grein. Birgðamagnið er meðhöndlað sem venjuleg vöruhúsaafhendingarlína. Til að [fá nánari upplýsingar um samsetningaraðstæður er farið í Skilningur settur saman í Pöntun og settur saman til birgða](assembly-assemble-to-order-or-assemble-to-stock.md).

## Sjá einnig .

[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Yfirlitsvinna vöruhúsastjórnunar](design-details-warehouse-management.md)
[með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
