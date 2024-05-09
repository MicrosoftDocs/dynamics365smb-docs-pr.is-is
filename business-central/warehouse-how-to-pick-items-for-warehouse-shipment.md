---
title: Tína vörur fyrir vöruhúsaafhendingu
description: Fræðast um notkun vöruhúsatínsluskjala til að stofna og vinna tínsluupplýsingar áður en vöruhúsaafhending er bókuð.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 04/23/2024
ms.custom: bap-template
ms.search.forms: '7335, 7339, 7345,'
---
# <a name="pick-items-for-warehouse-shipment"></a>Tína vörur fyrir vöruhúsaafhendingu

Vörur [!INCLUDE[prod_short](includes/prod_short.md)] eru tíndar og afhentar með einni af fjórum aðferðum, eins og lýst er í eftirfarandi töflu.

|Aðferð|Útleiðarferli|Krefjast tínslu|Krefjast afhendingar|Flóknarastig (Fræðast meira um [vöruhúsakerfisyfirlit](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bóka tínsluna og afhendinguna úr pöntunarlínunni|||Engin sérstök vöruhúsaaðgerð.|  
|Á|Bóka tínslu og afhendingu úr birgðatínsluskjali|Kveikt||Grunnur: Pöntun-fyrir-pöntun.|  
|U|Bóka tínslu og afhendingu úr vöruhúsaafhendingarskjali||Kveikt|Grunnur: Bókuð móttaka/sending í mörgum pöntunum.|  
|D|Tínslan er bókuð úr vöruhúsatínsluskjali og afhendingin bókuð úr vöruhúsaafhendingarskjali|Kveikt|Kveikt|Ítarlegt|  

Nánari upplýsingar í Vöruhúsaflæði á [útleið](design-details-outbound-warehouse-flow.md).

Þessi grein vísar til aðferðar D í töflunni. Nánari upplýsingar um afhendingu vara eru notaðar til að afhenda [vörur](warehouse-how-ship-items.md).

Þegar birgðageymsla er sett upp til að krefjast tínsluvinnslu og vöruhúsaafhendingarvinnslu skal nota vöruhúsatínsluskjöl til að stofna og vinna tínsluupplýsingar áður en vöruhúsaafhendingin er bókuð.  

Ekki er hægt að stofna vöruhúsatínsluskjal frá grunni. Tínslur eru hluti af verkflæði þar sem einstaklingurinn sem vinnur pöntun stofnar þær á tísku, eða starfsmaður vöruhússins stofnar þær á toga í tísku:

- Á ýta tísku, þar sem aðgerðin **Stofna tínslu** er notuð á síðunni **Vöruhúsaafhending** . Línurnar sem á að tína eru valdar og tínslan undirbúin með því að tilgreina, til dæmis hvaða hólf á að taka úr og setja í og hversu margar einingar á að meðhöndla. Hægt er að forskilgreina hólf fyrir vöruhúsastaðinn eða forðann.
- Á toga í tísku, þar sem aðgerðin **Gefa út** á síðunni **Vöruhúsaafhending** er notuð til að gera vörurnar tiltækar fyrir tínslu. Á síðunni **Vinnublað** tínslu geta starfsmenn vöruhússins notað aðgerðina **Sækja vöruhúsaskjöl** til að draga úthlutaðar tínslur.

> [!NOTE]  
> Tínsla á vöruhúsaafhendingu vara sem settar eru saman fyrir sölupöntun fylgir sömu skrefum og fyrir venjulegar vöruhúsatínslur fyrir afhendingar, eins og lýst er í þessari grein. Þó getur fjöldi tínslulína fyrir magnið sem á að afhenda verið margir fyrir einn vegna þess að íhlutirnir eru tíndir en ekki samsetta varan.  
>
> Vöruhúsatínslulínur eru stofnaðar fyrir gildið í reitnum **Eftirstöðvar (magn**) í línum samsetningarpöntunarinnar sem tengjast sölupöntunarlínunni sem verið er að afhenda. Allir íhlutir eru tíndir í einni aðgerð. Fræðast meira um [vöru með samsetningu á pöntun í vöruhúsaafhendingum](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).  
>  
> Nánari upplýsingar um tínslu íhluta fyrir samsetningarpantanir, þar á meðal aðstæður þar sem samsetningarvörur tengjast ekki söluafhendingu, er farið [í Tína fyrir framleiðslu, samsetningu eða Verk í ítarlegri vöruhúsagrunnstillingu](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="check-whether-items-are-available-for-picking"></a>Kanna hvort vörur séu tiltækar til tínslu

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a>Tínsluskjöl stofnuð með tínsluvinnublaðinu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað tínslu** og velja síðan viðkomandi tengil.  

2. Valið er **Sækja vöruhúsaskjöl** aðgerð.  

    Á listanum verða allar afhendingar sem hafa verið gefnar út fyrir tínslu, þar á meðal þær sem tínsluleiðbeiningar hafa þegar verið stofnaðar fyrir. Skjöl með tínslulínur sem hafa verið tíndar að fullu og skráðar birtast ekki á þessum lista.  
3. Afhendingarnar sem undirbúa á tínslu fyrir eru valdar.

    > [!NOTE]  
    >  Ef reynt er að velja afhendingar- eða innanhússtínsluskjal þar sem leiðbeiningar hafa þegar verið stofnaðar fyrir allar línur fær notandi skilaboð sem segja eitthvað slíkt: "Það er ekkert til að meðhöndla." Ef sameina á vöruhúsatínsluleiðbeiningar sem þegar hafa verið stofnaðar í eina tínsluleiðbeiningar þarf fyrst að eyða einstökum vöruhúsatínslum.

4. Reiturinn **Röðunaraðferð** er fylltur út til að raða línunum.  

    > [!NOTE]  
    >  Það hvernig línunum er raðað á vinnublaðinu flyst ekki sjálfkrafa í tínsluleiðbeiningarnar. Sömu röðun og hólfaflokkunarmöguleikar eru hins vegar til. Auðvelt er að endurgera línupöntunina sem áætluð er á vinnublaðinu þegar tínsluleiðbeiningarnar eru stofnaðar eða raðað í tínsluleiðbeiningunum.

5. Reiturinn **Magn til afgreiðslu** er fylltur út annaðhvort handvirkt eða með aðgerðinni **Sjálfvirk fylla út Qty.to Afgreiðsla** .  

    Síðan sýnir tiltækt magn í hjáskipunarhólfum. Þessar upplýsingar koma að gagni við skipulagningu vinnuúthlutunar við hjáskipunaraðstæður. [!INCLUDE[prod_short](includes/prod_short.md)] mun alltaf fyrst leggja til tiltekt úr hjáskipunarhólfi.
6. Línunum er breytt ef með þarf. Einnig er hægt að eyða línum til að gera tínsluna skilvirkari. Ef til að mynda til eru margar línur með vörum sem eru í hjáskipunarhólfum væri hægt að stofna tínslu fyrir allar línurnar. Hjáskipunarvörurnar verða afhentar með öðrum vörum í afhendingunni og hjáskipunarhólfin hafa pláss fyrir fleiri vörur á innleið.  

    > [!NOTE]  
    >  Ef línum er eytt er þeim aðeins eytt af vinnublaðinu. Þeim er ekki eytt úr tínsluvallistanum.  

7. Veldu aðgerðina **Stofna tínslu**. Síðan **Stofna tínslu** opnast, þar sem hægt er að bæta við upplýsingum um tínsluna sem verið er að stofna. Tilgreina hvernig á að sameina tínslulínur í tínsluskjölum með því að velja einn af eftirfarandi valkostum.  

    |Valkostur|Heimildasamstæða|
    |-|-|
    |Á vöruh. Skjal|Stofnar sérstök tínsluskjöl fyrir vinnublaðslínur með sama upprunaskjali vöruhúss.|
    |E. viðskm./lánardr./birgðag.|Stofna sérstök tínsluskjöl fyrir hvern viðskiptamann (sölupantanir), lánardrottinn (innkaupaskilapantanir) og birgðageymslu (millifærslupantanir).|
    |Eftir vöru|Stofna sérstök tínsluskjöl fyrir hverja vöru á tínsluvinnublaðinu.|
    |Á frá-svæði|Stofna skal sérstök tínsluskjöl fyrir hvert svæði sem vörur eru teknar af.|
    |Eftir hólfi|Stofna sérstök tínsluskjöl fyrir hvert hólf sem vörur eru teknar úr.|
    |Eftir eindaga|Stofna sérstök tínsluskjöl fyrir upprunaskjöl sem hafa sama gjalddaga.|

    Tilgreina hvernig tínsluskjöl eru stofnuð með því að velja úr eftirfarandi valkostum.

    |Valkostur|Heimildasamstæða|
    |-|-|
    |Max. Nr. tínslulína|Stofnar tínsluskjöl sem hafa ekki meira en tilgreindan fjölda lína í hverju fylgiskjali.|
    |Max. Nr. tínsluupprunaskjala|Stofnar tínsluskjöl sem hvert nær yfir ekki meira en tilgreindan fjölda upprunaskjala.|
    |Úthlutað notandakenni|Stofnar tínsluskjöl eingöngu fyrir vinnublaðslínur sem eru tengdar völdum vöruhúsastarfsmanni.|
    |Röðunaraðferð f. tínslulínur|Velja skal úr tiltækum valkostum til að raða línum í tínsluskjalinu sem stofnað er.|
    |Setja einingaskiptingarafmörkun|Felur millieiningatínslulínur þegar stærri mælieiningu er breytt í smærri mælieiningu og tínd að fullu.|
    |Ekki færa magn til afgreiðslu|Skilur eftir auðan reitinn Magn til afgreiðslu í tínslulínunum sem stofnaðar voru.|
    |Prenta tínslu|Prentar tínsluskjölin þegar þau eru stofnuð. Einnig er hægt að prenta úr tínsluskjölum sem stofnuð eru.|

8. Velja **Í lagi**. [!INCLUDE [prod_short](includes/prod_short.md)] tínslan er stofnuð eftir því sem valið er.  

## <a name="to-pick-items-for-a-warehouse-shipment"></a>Vörur tíndar fyrir vöruhúsaafhendingu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsatínslur** og velja síðan viðkomandi tengil.  

    Ef nauðsynlegt er að vinna í tiltekinni tínslu, er tínslan valin af lista eða listi afmarkaður til að vinna tínslu sem hafa verið úthlutað notandanum sérstaklega. Tínsluspjaldið er opnað.  
2. Ef reiturinn **Úthlutað notandakenni** er auður er kenni notanda fært inn til að auðkenna sig ef þörf krefur.  
3. Vörurnar eru tíndar.  

    Ef vöruhúsið er sett upp fyrir hólf eru sjálfgefin hólf vörunnar notuð til að leggja til hvaðan taka eigi vörurnar. Leiðbeiningarnar innihalda að minnsta kosti tvær aðskildar línur fyrir Aðgerðirnar Taka og Setja.  

    Ef vöruhúsið er sett upp fyrir beinan frágang og tínslu er hólfaflokkun notuð til að reikna út bestu hólfin til að tína úr. Þessi hólf eru lögð til í tínslulínunum. Leiðbeiningarnar innihalda að minnsta kosti tvær aðskildar línur fyrir Aðgerðirnar Taka og Setja.  

    * Fyrsta línan með **Taka** í reitnum **Aðgerð** gefur til kynna hvar vörurnar eru staðsettar á tínslusvæðinu. Ef verið er að afhenda margar vörur í einni afhendingarlínu gæti þurft að tína vörurnar í mörgum hólfum þannig að taka-lína er fyrir hvert hólf.
    * Næsta lína, með **Setja** í reitnum **Aðgerð**, sýnir hvar setja á vörurnar í vöruhúsinu. Ekki er hægt að breyta svæði og hólfi í línunni.

    > [!NOTE]
    > Ef tína þarf eða setja vörur í einni línu í fleiri en eitt hólf, til dæmis vegna þess að merkta hólfið er fullt, skal nota aðgerðina **Skipta línu** á flýtiflipanum **Línur** . Aðgerðin stofnar línu fyrir eftirstandandi magn sem á að meðhöndla.
        
    Hægt er að raða tínslulínunum eftir ýmsum skilyrðum, til dæmis eftir vöru, hillunúmeri eða gjalddaga. Röðun getur hjálpað til við að fínstilla frágangsferlið, til dæmis:

    * Ef Taka- og Setja-línur fyrir hverja afhendingarlínu fylgja ekki hver annarri á ekki strax að fylgja og þess er óskað er raðað með því að velja **Vara** í reitnum **Röðunaraðferð** .  
    * Ef hólfaflokkanir endurspegla raunútlit vöruhússins er röðunaraðferðin Hólfaflokkun **notuð** til að skipuleggja verkið eftir hólfastaðsetningum.

  > [!NOTE]  
  > Línum er raðað í hækkandi röð eftir völdum skilyrðum. Ef raðað er eftir fylgiskjali fer röðun fyrst eftir tegund fylgiskjals samkvæmt reitnum **Upprunaskjal vöruhúsaaðgerðar** . Ef raðað er eftir sendist-til er röðun framkvæmd fyrst eftir tegund áfangastaðar sem byggð er á reitnum **Tegund** viðtöku vöruhúss.

4. Þegar vörurnar hafa verið tíndar og settar á afhendingarsvæðið eða í afhendingarhólfið skal velja aðgerðina **Skrá tínslu** .  

Nú er hægt að koma vörunum í afhendingarbryggjuna og bóka afhendinguna, þar á meðal viðkomandi upprunaskjal, á síðunni **Vöruhúsaafhending** . Nánari upplýsingar um [afhenda vörur](warehouse-how-ship-items.md).

## <a name="see-also"></a>Sjá einnig .

- [Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)
- [Stjórna birgðum](inventory-manage-inventory.md)  
- [Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
- [Samsetningardeild](assembly-assemble-items.md)    
- [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
