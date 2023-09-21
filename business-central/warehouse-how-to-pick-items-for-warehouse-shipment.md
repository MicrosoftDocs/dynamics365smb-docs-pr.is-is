---
title: Tína vörur fyrir vöruhúsaafhendingu
description: Lærðu að nota vöruhúsatínsluskjöl til að stofna og vinna úr upplýsingum um tínsluafhendingar áður en vöruhúsaafhending er bókuð.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '7335, 7339, 7345,'
---
# Tína vörur fyrir vöruhúsaafhendingu

Í  [!INCLUDE[prod_short](includes/prod_short.md)] eru tínsla og sendingarvara notuð með einni af fjórum aðferðum eins og lýst er í eftirfarandi töflu.

|Aðferð|Útleiðarferli|Krefjast tínslu|Krefjast afhendingar|Flókið stig (frekari upplýsingar um  [Vöruhúsakerfi-Yfirlit](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bóka tínslu og sendingu úr pöntunarlínu|||Engin sérstök vöruhúsaaðgerð.|  
|Á|Bóka tínslu og afhendingu úr birgðatínsluskjali|Kveikt||Grunnur: pöntun-eftir pöntun.|  
|U|Bóka tínslu og sendingu úr vöruhúsaafhendingarskjali||Kveikt|Grunnur: Samstæða móttöku/skipa bóka fyrir margar pantanir.|  
|D|Bókið tínsluna úr vöruhúsatínsluskjali og bókið sendinguna úr afhendingarskjali vöruhúss|Kveikt|Kveikt|Ítarlegt|  

Frekari upplýsingar um flæði vöruhúss á  [útleið](design-details-outbound-warehouse-flow.md).

Með þessari grein er átt við aðferð D í töflunni. Til að fræðast meira um sendingarvörur er farið í  [sendingarvörur](warehouse-how-ship-items.md).

Þegar Birgðageymsla er sett upp þannig að krafist sé vöruhúsatínslu vinnslu og vöruhúsaafhendingarvinnslu skal nota vöruhúsatínsluskjöl til að stofna og vinna úr tínsluupplýsingum áður en vöruhúsaafhending er bókuð.  

Ekki er hægt að stofna vöruhúsatínsluskjal frá grunni. Tínslur eru hluti verkflæðis þar sem sá sem sér um vinnslu pöntunar stofnar á þrýstihátt eða starfsmaður vöruhússins stofnar þá í togtísku:

- Á þrýstihátt, þar sem þú notar  **aðgerðina stofna tínslu**  á  **síðu vöruhúsaafhendingar** . Velja línurnar sem á að tína og undirbúa tínslur með því að tilgreina, til dæmis, hvaða hólf eigi að taka af og á í og hversu margar einingar eigi að afgreiða. Hólf geta verið forskilgreind fyrir vöruhúsastaðinn eða forðinn.
- Í togtísku, þar sem úttektaraðgerðin  **er notuð**  á  **síðu vöruhúsaafhendingar**  til að gera vörurnar tiltækar fyrir tiltekt. Síðan, á  **síðunni tínsluvinnublað**, geta starfsmenn vöruhúss notað  **skjölin sækja vöruhúsaskjöl**  til að draga úthlutaðar tínslur.

> [!NOTE]  
> Tiltekt á vöruhúsaafhendingu vara sem eru settar saman fyrir sölupöntun fylgir sömu skrefum og Venjuleg vöruhúsatiltekt fyrir afhendingar eins og lýst er í þessari grein. Hins vegar er fjöldi tínslulína fyrir magnið sem á að senda ef til vill margar til þeirra því þú velur íhluti, ekki sett saman vöru.  
>
> Tínslulínur vöruhúss eru stofnaðar fyrir gildið í reitnum Eftirstöðvar  **í**  línum samsetningarpöntunar sem er tengd sölupöntunarlínunni sem verið er að senda. Allir íhlutir eru teknir fyrir í einni aðgerð. Frekari upplýsingar á  [afgreiðslu setja saman vörur í Vöruhúsasendingum](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).  
>  
> Frekari upplýsingar um tiltektaríhluti fyrir samsetningar pantana, þar á meðal aðstæður þar sem samsetningarvörur eru ekki tengdar söluafhendingu, er farið í  [tínslur fyrir framleiðslu, samsetningu eða vinnslur í ítarlegri Vöruhúsafbrigðum](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## Tínsluskjöl stofnuð í fjöldavið tínsluvinnublaðið

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað tínslu** og velja síðan viðkomandi tengil.  

2. Valið er **Sækja vöruhúsaskjöl** aðgerð.  

    Í listanum eru allar sendingar sem hafa verið losaðar fyrir tiltekt, þar með talið þær sem tínsluleiðbeiningar hafa þegar verið stofnaðar fyrir. Skjöl með tínslulínum sem hafa verið tekin endanlega til og skráð eru ekki sýnd á þessum lista.  
3. Afhendingarnar sem undirbúa á tínslu fyrir eru valdar.

    > [!NOTE]  
    >  Ef þú reynir að velja afhendingu eða innanhússtínsluskjal sem þú hefur þegar útbúið leiðbeiningar fyrir allar línurnar þess færðu skilaboð sem segja eitthvað eins og er, "það er ekkert hægt að afgreiða." Til að sameina vöruhúsatínsluleiðbeiningarnar sem þegar hafa verið stofnaðar í einni tínslukennslu verður að eyða einstökum vöruhúsatínslum sem fyrst.

4.  **Reiturinn röðunaraðferð**  er fylltur út til að raða línunum.  

    > [!NOTE]  
    >  Því hvernig línunum er raðað á vinnublaðinu er ekki sjálfkrafa haldið við í tínsluleiðbeiningunum. Hins vegar eru sömu röðunartækifæri og hólfaflokkuð. Auðveldlega er hægt að endurgera línupöntunina sem er áætlun í vinnublaðinu þegar tínsluleiðbeiningarnar eru stofnaðar eða í tínsluleiðbeiningunum.

5.  **Reiturinn Magn til afgreiðslu**  er fylltur út annaðhvort handvirkt eða með því að  **nota aðgerðina autofill Qty.to** .  

    Síðan sýnir magnið sem er tiltækt í hólfum í hjáskipun. Þessar upplýsingar eru gagnlegar við skipulagningu vinnuverkefna í hjáaðstæðum. [!INCLUDE[prod_short](includes/prod_short.md)] mun alltaf fyrst leggja til tiltekt úr hjáskipunarhólfi.
6. Breytið línunum ef þörf krefur. Einnig er hægt að eyða línum til að gera tínsluna skilvirkari. Ef til að mynda til eru margar línur með vörum sem eru í hjáskipunarhólfum væri hægt að stofna tínslu fyrir allar línurnar. Hjáskipunarvörurnar verða afhentar með öðrum vörum á sendingunni og í hjásendum hólfum hafa rými fyrir fleiri aðsendar vörur.  

    > [!NOTE]  
    >  Ef línum er eytt eru þær aðeins eyddar úr vinnublaðinu. Þeim er ekki eytt af listanum velja val.  

7. Veldu aðgerðina **Stofna tínslu**.  **Síðan stofna tínslu**  opnast, þar sem hægt er að bæta meiri upplýsingum við tínsluna sem verið er að stofna. Tilgreinið hvernig eigi að sameina tínslulínur í tínsluskjöl með því að velja einn af eftirfarandi valkostum.  

    |Valkostur|Heimildasamstæða|
    |-|-|
    |Á vöruhúsaskjölum Skjal|Stofnar aðskilin tínsluskjöl fyrir vinnublaðslínur með sama upprunaskjali vöruhúss.|
    |E. viðskm./lánardr./birgðag.|Stofna aðskilin tínsluskjöl fyrir hvern viðskiptavin (sölupantanir), lánardrottin (innkaupaskilapantanir) og birgðageymslu (flutningspantanir).|
    |Eftir vöru|Stofna aðskilin tínsluskjöl fyrir hverja vöru á tínsluvinnublaðinu.|
    |Á frá-svæði|Stofna aðskilin tínsluskjöl fyrir hvert svæði sem taka á vörur úr.|
    |Eftir hólfi|Stofna aðskilin tínsluskjöl fyrir hvert hólf sem taka á vörur úr.|
    |Eftir gjalddaga|Stofna aðskilin tínsluskjöl fyrir upprunaskjöl sem hafa sama gjalddaga.|

    Tilgreinið hvernig tínsluskjöl eru stofnuð með því að velja úr eftirfarandi valkostum.

    |Valkostur|Heimildasamstæða|
    |-|-|
    |Max. Nr. Um tínslulínur|Stofnar tínsluskjöl sem hafa ekki fleiri en tilgreindan línufjölda í hverju skjali.|
    |Max. Nr. Doktors Tínslusource.|Stofnar tínsluskjöl sem hvert skjól er ekki meira en tiltekinn fjöldi upprunaskjala.|
    |Úthlutað notandakenni|Stofnar tínsluskjöl aðeins fyrir vinnublaðslínur sem er úthlutað á valinn vöruhúsastarfsmann.|
    |Röðunaraðferð f. tínslulínur|Veljið úr tiltækum valkostum til að raða línum í stofnaða tínsluskjalið.|
    |Setja einingaskiptingarafmörkun|Felur millitínslulínum einingatiltekt þegar stærri Mælieining er umbreytt í smærri mælieiningu og alveg tínd.|
    |Ekki færa magn til afgreiðslu|Fer reiturinn Magn til afgreiðslu í stofnaða tínslulínum auðar.|
    |Prenta tínslu|Prentar tínsluskjölin þegar þau eru stofnuð. Einnig er hægt að prenta úr stofnaða tínsluskjölum.|

8. Velja **Í lagi**. [!INCLUDE [prod_short](includes/prod_short.md)] stofnar tínsluna í samræmi við það sem valið var.  

## Vörur tínslur fyrir vöruhúsaafhendingu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsatínslur** og velja síðan viðkomandi tengil.  

    Ef nauðsynlegt er að vinna í tiltekinni tínslu, er tínslan valin af lista eða listi afmarkaður til að vinna tínslu sem hafa verið úthlutað notandanum sérstaklega. Tínsluspjaldið er opnað.  
2.  **Ef reiturinn úthlutað notandakenni**  er auður skal FÆRA inn kennið til að auðkenna notandann ef með þarf.  
3. Tínsla varanna.  

    Ef vöruhúsið er sett upp þannig að þau noti hólf eru sjálfgefnu hólfin í vörunum notuð til að leggja til hvaðan eigi að taka vörurnar. Leiðbeiningarnar innihalda að minnsta kosti tvær aðskildar línur til að taka og setja aðgerðir.  

    Ef vöruhúsið er sett upp til að nota beinan frágang og tínslu er hólfaflokkun notuð til að reikna út bestu hólfin til tínslu úr. Þau hólf eru lögð til á tínslulínunum. Leiðbeiningarnar innihalda að minnsta kosti tvær aðskildar línur til að taka og setja aðgerðir.  

    * Fyrsta línan, með  **taka**  í  **reitnum aðgerðargerð**, gefur til kynna hvar vörurnar eru staðsettar á tiltektarsvæðinu. Ef mikið af vörum er í einni afhendingarlínu gæti þurft að tína vörurnar í nokkrum hólfum svo það sé lína fyrir hvert hólf.
    * Næsta lína, með  **stað**  í  **reitnum Tegund**  aðgerðar, sýnir hvar verður að setja vörurnar í vöruhúsinu. Ekki er hægt að breyta svæði og hólfi í þessari línu.

    > [!NOTE]
    > Ef taka þarf vörurnar í eina línu í fleiri en einu hólfi, til dæmis vegna þess að það merkta hólfið er fullt, skal nota  **aðgerðina skipta línu**  á  **fastflipanum línur** . Aðgerðin býr til línu fyrir eftirstandandi magn sem á að afgreiða.

4. Þegar búið er að velja og setja vörurnar í sendingarsvæði eða afhendingarhólf skal velja  **aðgerðina skrá tínslu** .  

Nú er hægt að koma vörunum í afhendingarhöfnina og bóka sendinguna, þar með talið tengda upprunaskjalinu, á  **síðu vöruhúsaafhendingar** . Frekari upplýsingar um  [Sendingarvörur](warehouse-how-ship-items.md).

## Sjá einnig .

[Warehouse Management Overview](design-details-warehouse-management.md)
[Inventory](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
