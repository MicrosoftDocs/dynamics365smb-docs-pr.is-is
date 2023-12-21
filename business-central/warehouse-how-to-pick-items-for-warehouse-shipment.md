---
title: Tína vörur fyrir vöruhúsaafhendingu
description: Lærðu um notkun vöruhúsatínslugagna til að búa til og vinna úr tínsluupplýsingum áður en vöruhúsasending er bókuð.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 09/11/2023
ms.custom: bap-template
ms.search.forms: '7335, 7339, 7345,'
---
# <a name="pick-items-for-warehouse-shipment"></a>Tína vörur fyrir vöruhúsaafhendingu

Í [!INCLUDE[prod_short](includes/prod_short.md)] velur þú og sendir vörur með einni af fjórum aðferðum, eins og lýst er í eftirfarandi töflu.

|Aðferð|Útleiðarferli|Krefjast tínslu|Krefjast afhendingar|Flækjustig (Frekari upplýsingar á [yfirlit yfir vöruhússtjórnun](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bókaðu tínslu og sendingu úr pöntunarlínunni|||Engin sérstök vöruhúsaaðgerð.|  
|Á|Bókaðu tínslu og sendingu úr birgðatínsluskjali|Kveikt á||Basic: Panta-fyrir-pöntun.|  
|U|Bókaðu tínslu og sendingu úr vöruhúsasendingarskjali||Kveikt á|Basic: Samþætt móttöku/sendingabókun fyrir margar pantanir.|  
|D|Bókaðu tínsluna úr vöruhúsatínsluskjali og bókaðu sendinguna úr vöruhúsasendingarskjali|Kveikt á|Kveikt á|Ítarlegt|  

Frekari upplýsingar á [Útleið vöruhúsaflæði](design-details-outbound-warehouse-flow.md).

Þessi grein vísar til aðferðar D í töflunni. Til að læra meira um sendingarvörur skaltu fara á [Sendingarvörur](warehouse-how-ship-items.md).

Þegar staðsetning er sett upp til að krefjast vöruhúsatínsluvinnslu og vöruhúsasendingarvinnslu, notaðu vöruhústínsluskjöl til að búa til og vinna úr tínsluupplýsingum áður en þú bókar vöruhúsasendinguna.  

Þú getur ekki búið til vöruhústínsluskjal frá grunni. Val eru hluti af verkflæði þar sem sá sem vinnur úr pöntun býr til þær á ýttan hátt eða starfsmaður vöruhússins býr til þær á dráttarhátt:

- Á ýttan hátt, þar sem þú notar **Create Pick** aðgerðina á **Vöruhússending** síðunni. Veldu línurnar sem á að tína og undirbúið tínslurnar með því að tilgreina td hvaða tunnur á að taka úr og setja í og ​​hversu margar einingar á að meðhöndla. Hægt er að forskilgreina hólf fyrir staðsetningu vöruhúss eða tilföng.
- Á dráttarbraut, þar sem þú notar **Sleppa** aðgerðina á **Vöruhúsasendingu** síðunni til að gera hlutina aðgengilega fyrir tína. Síðan, á  **Velja vinnublað** síðunni, geta starfsmenn vöruhússins notað **Fá vöruhúsaskjöl** aðgerðina til að draga út valið.

> [!NOTE]  
> Tínsla fyrir vöruhúsasendingu á vörum sem eru settar saman fyrir sölupöntun fylgir sömu skrefum og fyrir venjulega vöruhúsatínslu fyrir sendingar, eins og lýst er í þessari grein. Hins vegar getur fjöldi tínslulína fyrir magnið sem á að senda verið margir á móti einni vegna þess að þú velur íhlutina, ekki samsetta vöruna.  
>
> Vöruhústínslulínur eru búnar til fyrir gildið í reitnum **Afstandandi magn**  á línum samsetningarpöntunarinnar sem er tengd við sölupöntunarlínuna sem verið er að senda. Allir íhlutir eru valdir í einni aðgerð. Frekari upplýsingar er að finna á [Meðhöndlun samsettra vara í vöruhúsasendingum](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).  
>  
> Til að læra meira um að velja íhluti fyrir samsetningarpantanir, þar á meðal aðstæður þar sem samsetningarvörur tengjast ekki sölusendingu, farðu á [Veldu fyrir framleiðslu, samsetningu eða störf í háþróuðum vöruhúsastillingum](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).  

## <a name="check-whether-items-are-available-for-picking"></a>Athugaðu hvort hlutir séu tiltækir til að tína

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a>Til að búa til tínsluskjöl í lausu með tínsluvinnublaðinu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað tínslu** og velja síðan viðkomandi tengil.  

2. Valið er **Sækja vöruhúsaskjöl** aðgerð.  

    Listinn mun innihalda allar sendingar sem hafa verið gefnar út til tínslu, einnig þær sem tínsluleiðbeiningar hafa þegar verið búnar til. Skjöl með tínslulínum sem hafa verið alveg tínd og skráð eru ekki sýnd á þessum lista.  
3. Afhendingarnar sem undirbúa á tínslu fyrir eru valdar.

    > [!NOTE]  
    >  Ef þú reynir að velja sendingu eða innra tínsluskjal sem þú hefur þegar búið til leiðbeiningar fyrir allar línur þess færðu skilaboð sem segja eitthvað eins og, "það er ekkert að höndla." Til að sameina vöruhústínsluleiðbeiningar sem þú hefur þegar búið til í eina tínsluleiðbeiningar verður þú fyrst að eyða einstökum vöruhúsatínslum.

4. Fylltu út **Röðunaraðferð** reitinn til að raða línunum.  

    > [!NOTE]  
    >  Hvernig línurnar eru flokkaðar í vinnublaðinu fer ekki sjálfkrafa í gegnum valleiðbeiningarnar. Hins vegar eru sömu möguleikar til að flokka og röðun í ruslakörfu. Þú getur auðveldlega endurskapað línuröðina sem þú skipuleggur í vinnublaðinu þegar þú býrð til tínsluleiðbeiningarnar eða flokkar í tínsluleiðbeiningarnar.

5. Fylltu út **magnið. til að meðhöndla** reitinn annað hvort handvirkt eða með því að nota **Sjálfvirk útfylling Qty.to Handle** aðgerð.  

    Síðan sýnir magnið sem er tiltækt í flutningshólfum. Þessar upplýsingar eru gagnlegar til að skipuleggja vinnuverkefni í flutningsaðstæðum. [!INCLUDE[prod_short](includes/prod_short.md)] mun alltaf fyrst leggja til tiltekt úr hjáskipunarhólfi.
6. Ef þörf krefur, breyttu línunum. Þú getur líka eytt línum til að gera valið skilvirkara. Ef til að mynda til eru margar línur með vörum sem eru í hjáskipunarhólfum væri hægt að stofna tínslu fyrir allar línurnar. Hlutirnir sem eru í flutningi verða sendir með öðrum hlutum í sendingunni og í tunnunum sem fara yfir bryggju verður pláss fyrir fleiri hluti sem koma inn.  

    > [!NOTE]  
    >  Ef þú eyðir línum er þeim aðeins eytt af vinnublaðinu. Þeim er ekki eytt af vallistanum.  

7. Veldu aðgerðina **Stofna tínslu**. Síðan **Búa til val** opnast þar sem þú getur bætt frekari upplýsingum við valið sem þú ert að búa til. Tilgreindu hvernig á að sameina tínslulínur í tínsluskjölunum með því að velja einn af eftirfarandi valkostum.  

    |Valkostur|Heimildasamstæða|
    |-|-|
    |Á Whse. Skjal|Býr til aðskilin tiltektarskjöl fyrir vinnublaðslínur með sama upprunaskjali vöruhúss.|
    |E. viðskm./lánardr./birgðag.|Búðu til aðskilin tínsluskjöl fyrir hvern viðskiptavin (sölupantanir), söluaðila (skilapantanir innkaupa) og staðsetningu (flutningspantanir).|
    |Eftir vöru|Búðu til aðskilin tínsluskjöl fyrir hvern hlut á tínsluvinnublaðinu.|
    |Á frá-svæði|Búðu til aðskilin tiltektarskjöl fyrir hvert svæði sem þú tekur hluti frá.|
    |Eftir hólfi|Búðu til aðskilin tínsluskjöl fyrir hverja hólf sem þú tekur hluti úr.|
    |Eftir gjalddaga|Búðu til aðskilin tiltektarskjöl fyrir upprunaskjöl sem hafa sama gjalddaga.|

    Tilgreindu hvernig tiltektarskjölin eru búin til með því að velja úr eftirfarandi valkostum.

    |Valkostur|Heimildasamstæða|
    |-|-|
    |Hámark Nr. Af Pick Lines|Býr til valskjöl sem hafa ekki fleiri en tilgreindan fjölda lína í hverju skjali.|
    |Hámark Nr. Af Pick Source Docs.|Býr til valskjöl sem hver um sig nær ekki yfir meira en tilgreindan fjölda frumskjala.|
    |Úthlutað notandakenni|Stofnar tiltektarskjöl eingöngu fyrir vinnublaðslínur sem eru úthlutaðar á valda vöruhússstarfsmann.|
    |Röðunaraðferð f. tínslulínur|Veldu úr tiltækum valkostum til að raða línum í búnu tiltektarskjalinu.|
    |Setja einingaskiptingarafmörkun|Felur millihlutavallínur þegar stærri mælieiningu er breytt í minni mælieiningu og tínd að fullu.|
    |Ekki færa magn til afgreiðslu|Skilur eftir Magn. til að meðhöndla reitinn í stofnuðum tínslulínum tómum.|
    |Prenta tínslu|Prentar tiltektarskjölin þegar þau eru búin til. Þú getur líka prentað út úr tilbúnum valskjölum.|

8. Velja **Í lagi**. [!INCLUDE [prod_short](includes/prod_short.md)] mun búa til valið í samræmi við val þitt.  

## <a name="to-pick-items-for-a-warehouse-shipment"></a>Til að velja vörur fyrir vöruhússendingu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vöruhúsatínslur** og velja síðan viðkomandi tengil.  

    Ef nauðsynlegt er að vinna í tiltekinni tínslu, er tínslan valin af lista eða listi afmarkaður til að vinna tínslu sem hafa verið úthlutað notandanum sérstaklega. Tínsluspjaldið er opnað.  
2. Ef reiturinn **Úthlutað notandaauðkenni** er auður skaltu slá inn auðkenni þitt til að auðkenna þig ef þörf krefur.  
3. Veldu hlutina.  

    Ef vöruhúsið er sett upp til að nota hólfa eru sjálfgefnar hólkar vörunnar notaðar til að benda á hvaðan á að taka vörurnar. Leiðbeiningarnar innihalda að minnsta kosti tvær aðskildar línur fyrir Taka og setja aðgerðir.  

    Ef vöruhúsið er sett upp til að nota beint frágang og tínslu, er röðun hólfa notuð til að reikna út bestu hólfin til að tína úr. Stungið er upp á þeim tunnunum á plokkunarlínunum. Leiðbeiningarnar innihalda að minnsta kosti tvær aðskildar línur fyrir Taka og setja aðgerðir.  

    * Fyrsta línan, með **Taka** í reitnum **Aðgerðagerð**, gefur til kynna hvar hlutirnir eru staðsettir á tínslusvæðinu. Ef þú ert að senda mikið af vörum á einni sendingarlínu gætirðu þurft að velja vörurnar í nokkrum hólfum, þannig að það er Taka lína fyrir hverja tunnu.
    * Næsta lína, með **Place** í reitnum **Aðgerðartegund**, sýnir hvar þú verður að staðsetja vörurnar í vöruhúsinu. Þú getur ekki breytt svæði og rusli á þessari línu.

    > [!NOTE]
    > Ef þú verður að velja eða setja hlutina fyrir eina línu í fleiri en eina tunnu, til dæmis vegna þess að tilnefnda tunnan er full, notaðu **Skipta línu** aðgerðina á **Línur** Flýtiflipi. Aðgerðin býr til línu fyrir það magn sem eftir er til að meðhöndla.

4. Eftir að þú hefur valið og sett hlutina á sendingarsvæðið eða sendingartunnuna skaltu velja **Skráðu Pick**  aðgerð.  

Þú getur nú komið með vörurnar á sendingarbryggjuna og sent sendinguna, þar á meðal tengda upprunaskjalið, á **Vöruhúsasending**  síðu. Frekari upplýsingar á [Skipahlutir](warehouse-how-ship-items.md).

## <a name="see-also"></a>Sjá einnig .

- [Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)
- [Stjórna birgðum](inventory-manage-inventory.md)  
- [Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
- [Samsetningardeild](assembly-assemble-items.md)    
- [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
