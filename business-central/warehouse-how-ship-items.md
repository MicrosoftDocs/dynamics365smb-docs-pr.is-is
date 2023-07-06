---
title: Senda vörur
description: Í þessari grein er lýst hvernig á að senda vörur úr vöruhúsinu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
---

# <a name="ship-items-with-a-warehouse-shipment"></a><a name="ship-items-with-a-warehouse-shipment"></a><a name="ship-items-with-a-warehouse-shipment"></a>Senda vörur með vöruhúsaafhendingu

Í  [!INCLUDE[prod_short](includes/prod_short.md)] eru tínsla og sendingarvara notuð með einni af fjórum aðferðum eins og lýst er í eftirfarandi töflu.

|Aðferð|Útleiðarferli|Krefjast tínslu|Krefjast afhendingar|Flókið stig (frekari upplýsingar um  [Vöruhúsakerfi-Yfirlit](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bóka tínslu og sendingu úr pöntunarlínu|||Engin sérstök vöruhúsaaðgerð.|  
|B|Bóka tínslu og afhendingu úr birgðatínsluskjali|Kveikt||Grunnur: pöntun-eftir pöntun.|  
|N|Bóka tínslu og sendingu úr vöruhúsaafhendingarskjali||Kveikt|Grunnur: Samstæða móttöku/skipa bóka fyrir margar pantanir.|  
|D|Bókið tínsluna úr vöruhúsatínsluskjali og bókið sendinguna úr afhendingarskjali vöruhúss|Kveikt|Kveikt|Ítarlegt|  

Til að fræðast meira um sendingarvörur er farið í Vöruhúsaflæði á  [útleið](design-details-outbound-warehouse-flow.md).

Með þessari grein er átt við aðferðir C og D í töflunni. Í báðum aðferðum er byrjað á því að stofna afhendingarskjal úr upprunaskjali. Síðan er tilgreindar vörur teknar til fyrir afhendinguna.

Þegar Birgðageymsla krefst vöruhúsasendinga er hægt að senda vörur á grundvelli upprunaskjala sem hafa verið losuð í vöruhúsið. Gefa út upprunaskjöl gerir vörurnar á þeim tilbúnar til reiðu í vöruhúsinu. Eftirfarandi eru dæmi um upprunaskjöl:

* Sölupantanir
* Vöruskilapantanir innkaupa
* Flutningspöntunum
* Þjónustupöntunum

Hægt er að stofna vöruhúsaafhendingu á tvennan hátt:

* Á þrýstihátt, þegar vinna er unnin á pöntunargrunni.  **Velja afhendingaraðgerðina vöruhúsaafhendingu**  í upprunaskjalinu til að stofna vöruhúsaafhendingu fyrir skjalið.
* Í togtísku, þar sem úttektaraðgerðin  **er notuð**  í upprunaskjalinu til að losa hana í vöruhúsið. Starfsmaður í vöruhúsi stofnar  **vöruhúsaafhendingu**  fyrir eitt eða mörg Útgefin upprunaskjöl. Eftirfarandi ferli lýsir því hvernig vöruhúsaafhending er stofnuð í togflutningtísku.

## <a name="to-ship-items-using-a-warehouse-shipment-document"></a><a name="to-ship-items-using-a-warehouse-shipment-document"></a><a name="to-ship-items-using-a-warehouse-shipment-document"></a>Vörur sendingar með vöruhúsaafhendingarskjali

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsaafhendingar**, velja síðan viðkomandi tengil.  
2. Velja **Nýtt**.  
3. Í reitnum **númer** Er valin sú númeraröð sem á að nota til að stofna KENNI fyrir afhendinguna.  
4.  **Í reitnum Kóti birgðageymslu**  er valinn birgðageymslan sem verið er að skipuleggjum. 

    Þegar upprunaskjalslínur eru sóttar eru sumar upplýsingarnar frá birgðageymslunni afritaðar í hverja línu.  
5. Ef birgðageymslan krefst hólfa er reiturinn Hólfakóti  **fylltur út** . Hægt er að bæta við hólfakótanum fyrir það eftir uppsetningu [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar á  [svæði og hólfakóta](warehouse-how-ship-items.md#zone-and-bin-codes).  
6. Hægt er að nálgast upprunaskjalið á tvennan hátt:

    * Valið er **Sækja upprunaskjöl** aðgerð. Upprunaskjölin-á  **útleið**  opnast. Hér er hægt að velja eitt eða fleiri upprunaskjöl sem eru losuð í vöruhús sem þarfnast afhendingar.
    * Velja skal **Nota afmarkanir til að sækja uppr.skjöl.** aðgerðina.  **Síur til að fá Upprunadoktora.**  síða opnast. Hægt er að velja afmörkun upprunaskjals og nota það. Öllum útgefnum upprunaskjalslínum sem uppfylla afmörkunarskilyrðin er bætt við á  **síðu vöruhúsaafhendingar** .  [Frekari upplýsingar um notkun afmörkunar til að sækja upprunaskjöl](warehouse-how-ship-items.md#how-to-use-filters-to-get-source-documents).

    > [!NOTE]
    > Ef hjáskipun og hólf eru notuð fyrir hverja línu er hægt að fara yfir magn vara sem eru settar í hjáskipunarhólf. [!INCLUDE [prod_short](includes/prod_short.md)]  reiknar út magnið þegar reitirnir í afhendingunni eru uppfærðir. Ef þeir eru vörurnar í sendingunni sem verið er að undirbúa er hægt að stofna tínslu fyrir allar vörurnar og ljúka síðan sendingunni. Frekari upplýsingar eru á [Hjáskipa vörur](warehouse-how-to-cross-dock-items.md).

7. Vöruhúsatiltekt er stofnuð. Ef birgðageymslan krefst tínslu er hægt að stofna tínsluaðgerðir fyrir vöruhúsaafhendingar á tvo vegu:

    * Á þrýstihátt, þar sem þú notar  **aðgerðina stofna tínslu** . Velja línurnar sem á að velja og tilgreina upplýsingar um tínsluna. Til dæmis hvaða hólf á að taka af og setja í, og hve margar einingar á að afgreiða. Hólfin geta verið fyrirfram skilgreind fyrir vöruhúsastaðinn eða forðinn.
    * Á togtísku, þar sem notuð  **er úttektaraðgerð** .  **Á síðunni tínsluvinnublað**  skal nota  **aðgerðina Sækja vöruhúsaskjöl**  til að fá úthlutaða tínslur. Þegar vöruhúsatínslan er fullskráð er línunum á  **tínsluvinnublaðinu**  eytt.  [Frekari upplýsingar um tínsluvörur fyrir vöruhúsaafhendingar](warehouse-how-to-pick-items-for-warehouse-shipment.md).

    > [!TIP]
    > Fyrir birgðageymslu sem þarfnast ekki tiltektar er hægt að prenta vöruhúsaafhendingu og nota hann sem tiltektarlista.

8. Tilgreinið magnið sem á að senda.  

    Fyrir birgðageymslu sem þarfnast tiltektar,  **er reiturinn Magn til sendingar**  uppfærður sjálfkrafa þegar Tínslan er skráð.  **Annars er reiturinn Magn til afhendingar**  fylltur út með útistandandi magni í hverri línu þegar afhendingarlína vöruhúss er stofnuð.

    Hægt er að breyta magninu en ekki er hægt að senda fleiri vörur en númerið í  **reitinn Magn útistandandi**  í upprunaskjalslínunni eða  **reitnum magn tekið**  til ef tiltekt er þörf.

    Til að stilla gildið í  **reitnum Magn til sendingar**  í öllum línum á núlli er valið  **Eyða magni til**  -aðgerða. Til dæmis er gagnlegt að stilla magnið á núll ef notaður er strikamerkjaskanni til að uppfæra Sendingarmagnið. Til að bæta við magninu sem er tiltækt fyrir sendingu er hægt að  **velja magn til að senda** .

9. Afhendingin er bókuð.

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

## <a name="how-to-use-filters-to-get-source-documents"></a><a name="how-to-use-filters-to-get-source-documents"></a><a name="how-to-use-filters-to-get-source-documents"></a>Hvernig afmarkanir eru notaðar til að sækja upprunaskjöl

Í vöruhúsaafhendingu er hægt að nota  **afmarkanirnar til að sækja Upprundocs.**  síða til að sækja útgefnar upprunaskjalslínur sem skilgreina hvaða vörur á að senda.

1. Í vöruhúsaafhendingunni skal velja  **notaðar afmarkanir til að sækja src. docs.**  aðgerð. 
2. Til að setja upp nýja afmörkun er lýsandi kóti færður inn í reitinn **Kóti** og smellt á **Breyta** aðgerðina.

    Upprunaskjalsíkort-á  **útleið**  opnast.

3. Notið afmarkanir til að skilgreina gerð upprunaskjalslínurnar sem á að sækja. Til dæmis er hægt að velja gerðir upprunaskjala eins og sölu-eða millifærslupantanir.
4. Veljið **Keyra**.  

Öllum útgefnum upprunaskjalslínum sem uppfylla afmörkunarskilyrðin er bætt við á  **síðu vöruhúsaafhendingar**  þar sem Afmarkanirnar eru stilltar.

Hægt er að búa til ótakmarkaðan fjölda af afmörkunarsamsetningum. Afmarkanir eru vistaðar á  **afmörkunum til að fá Upprunadoktor.**  síðu og eru aðgengilegar næst þegar þörf er á þeim. Hægt er að breyta skilyrði hvenær sem er með því að smella á **Breyta** aðgerðina.

## <a name="zone-and-bin-codes"></a><a name="zone-and-bin-codes"></a><a name="zone-and-bin-codes"></a>Svæði og hólfakóta

Ef hólfum er skylt á staðnum er  [!INCLUDE [prod_short](includes/prod_short.md)]  stungið upp á svæði og hólfakóta á vöruhúsaafhendingarskjalinu.

* Fyrir ítarlegri afbrigði þar sem birgðageymslan notar beinan frágang og tínslu  [!INCLUDE [prod_short](includes/prod_short.md)]  notar hólfið sem er tilgreint í  **reitnum kóti**  afhendingarhólfs á  **birgðageymsluspjaldinu**.  **Ef kóti**  sendingarhólfs er ekki tilgreindur er reiturinn auður. Ef vöru-og afhendingarhólfið er  [!INCLUDE [prod_short](includes/prod_short.md)]  ekki í samræmi skilur afhendingarhólfið auð.
* Í öðrum tilvikum þarf  [!INCLUDE [prod_short](includes/prod_short.md)]  alltaf að nota hólfið sem tilgreint er í  **reitnum**  **kóti**  afhendingarhólfs fyrst. Ef kóti sendingarhólfs er ekki tilgreindur  [!INCLUDE [prod_short](includes/prod_short.md)]  notar hólfakótinn úr upprunaskjalinu.

## <a name="handling-assemble-to-order-items-in-warehouse-shipments"></a><a name="handling-assemble-to-order-items-in-warehouse-shipments"></a><a name="handling-assemble-to-order-items-in-warehouse-shipments"></a>Meðhöndlun íhluta pantanasamsetninga við vöruhúsaafhendingu

Í setja saman pöntunaraðstæður til að nota  **reitinn Magn til**  afhendingar í vöruhúsaafhendingarlínum til að skrá hversu margar einingar eru settar saman. Magnið er bókað sem samsetningarframleiðsla þegar vöruhúsaafhendingin er bókuð. Gildið í  **reitnum Magn til afhendingar**  er núll fyrir aðrar afhendingarlínur vöruhúss.

Þegar starfsmenn ljúka við að setja saman eitthvert eða allt magn af samsetningum sem á að panta skal skrá magnið  **í reitnum Magn til afhendingar**  í vöruhúsaafhendingarlínunni. Veljið  **síðan aðgerðina Bóka sending** . Samsetningarúttak er bókað, þar með talið þáttanotkun. Söluafhending fyrir magnið er bókuð fyrir sölupöntunina.

Í samsetningarpöntun má velja **Setja saman í p. vöruh. send. lína** til sjá vöruhúsaafhendingarlínuna.

Eftir að vöruhúsaafhending hefur verið bókuð eru mismunandi svæði í sölupöntunarlínunni uppfærð til að sýna framvindu í vöruhúsinu. Eftirfarandi svæði eru einnig uppfærð til að sýna hversu mikið magn samsetningarpantana á eftir að setja saman og afhenda:

* **Útistandandi magn ATO vöruhúss**
* **Útistandandi magn ATO vöruhúss (stofn)**

> [!NOTE]
> Í samsettri atburðarás þar sem hluti af magninu verður að vera settur saman og annað verður að senda úr birgðum eru stofnaðar tvær vöruhúsaafhendingarlínur. Ein er fyrir er fyrir samsetningarpöntunarmagn, og ein er fyrir birgðamagn.
>
> Magn í samsetningum er afgreitt eins og lýst er í þessari grein. Birgðamagn er afgreitt sem venjuleg vöruhúsaafhendingarlína. Til að fræðast meira um samsetningu atburðarásar er farið í  [skilning á að setja saman og setja saman við birgðir](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/ship-invoice-items-dynamics-365-business-central/).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Yfirlit yfir](design-details-warehouse-management.md)
[vöruhúsastjórnun vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
