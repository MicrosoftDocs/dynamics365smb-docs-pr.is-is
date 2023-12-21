---
title: Tína fyrir innri starfsemi með ítarlegum vöruhúsaskilgreiningum
description: 'Ef birgðageymslurnar nota tínslu og afhendingu skal velja tínsluíhluti fyrir framleiðslu, samsetningu og verkaðgerðir á síðu vöruhúsatínslunnar.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: null
ms.date: 09/12/2023
ms.custom: bap-template
---
# <a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a>Tínsla fyrir framleiðslu, samsetningu eða verk í ítarlegum vöruhúsastillingum

Hvernig þú velur íhluti fyrir framleiðslu, verk eða samsetningarpantanir fer eftir því hvernig vöruhúsið þitt er sett upp sem staðsetning. Lærðu meira á [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Í háþróaðri vöruhúsastillingu fyrir útstreymi (velja), kveiktu á **Krefjast tínslu** og **Krefjast sendingar** kveikja á  **Staðsetningarspjald** síðunni fyrir staðsetninguna.

Þegar staðsetningin er sett upp til að krefjast vöruhúsatínsluvinnslu og vöruhúsasendingarvinnslu, notaðu vöruhústínsluskjöl til að búa til og vinna tínsluupplýsingar áður en þú bókar notkun eða neyslu íhluta.  

Þú getur ekki búið til vöruhústínsluskjal frá grunni. Val er hluti af verkflæði þar sem aðili sem er að vinna úr pöntun býr til þær á ýttan hátt eða starfsmaður vöruhússins býr til þær á dráttarhátt:

- Á ýttu hátt, þar sem þú notar **Create Pick** aðgerðina í **framleiðslupöntuninni**, **Samsetningarpöntun**, **Starfspjald** síða. Veldu línurnar til að tína og undirbúa tínslurnar með því að tilgreina, til dæmis, hvaða tunnur á að taka úr og setja í og ​​hversu margar einingar á að meðhöndla. Hægt er að forskilgreina hólf fyrir staðsetningu vöruhúss eða tilföng.
- Á dráttarbraut, þar sem þú losar **framleiðslupöntun**, **samsetningarpöntun**, **Starf Kort** í vöruhús sem gerir hlutina tiltæka til tínslu. Síðan, á  **Velja vinnublað** síðunni, geta starfsmenn vöruhússins notað **Fá vöruhúsaskjöl** aðgerðina til að draga út valið.

Til að tína eða færa íhluti fyrir upprunaskjöl á uppdráttarhátt verður þú að losa upprunaskjalið til að gera það tilbúið til tínslu. Upprunaskjöl eru gefin út fyrir innri aðgerðir á eftirfarandi hátt.  

|Upprunaskjal|Losunaraðferð|  
|---------------------|--------------------|  
|Framleiðslupöntun|Breyttu pöntunarstöðunni í Losað eða búðu til útgefna framleiðslupöntun strax.|  
|Samsetningarpöntun|Breyta stöðu í Útgefið.|
|Verk | Breyttu stöðu í Opið eða búðu til starf með stöðu Opið strax.|  

## <a name="production"></a>Framleiðsla

Notaðu **Warehouse Pick** skjöl til að tína framleiðsluíhluti í flæði til framleiðslu.

Fyrir staðsetningu sem notar hólfa til að færa vörur í opna búðargólf, geturðu notað eftirfarandi aðferðir:

* Fyrir staðsetningu sem notar beint frágang og tínslu skaltu fylgja skrefunum í [Færa hluti í háþróuðum vöruhúsastillingum](warehouse-how-to-move-items-in-advanced-warehousing.md) greininni.
* Fyrir aðrar staðsetningar skaltu fylgja skrefunum í [Færa hluti innbyrðis í grunnstillingum vöruhúsa](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) greinarinnar.

## <a name="assembly"></a>Samsetning

Notaðu **Warehouse Pick** skjöl til að færa samsetningaríhluti á samsetningarsvæðið.

[!INCLUDE [prod_short](includes/prod_short.md)] styður gerðir af samsetningarflæði til að setja saman á lager og setja saman eftir pöntun. Til að fá frekari upplýsingar um samsetningu eftir pöntun í vöruhúsaflæði á útleið, farðu í [Meðhöndlun á samsetningu eftir pöntun í vöruhúsasendingum](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

## <a name="project-management"></a>Verkefnastjórnun

Notaðu **Warehouse Pick** skjöl til að velja verkþætti í flæðinu til verkefnastjórnunar.

> [!NOTE]
> Getan til að tína íhluti fyrir veráætlunarlínur var bætt við [!INCLUDE[d365fin](includes/d365fin_md.md)] í 2022 útgáfutímabili 2. Til að byrja að nota möguleikann verður stjórnandi að kveikja á **Eiginleikastjórnun: Virkja birgða- og vöruhúsatínslu úr verkum** á síðunni **Eiginleikastjórnun**.
>
> Störf styðja ekki háþróaðar stillingar þar sem kveikt er á **Bein vali og frágangi** rofi.

## <a name="check-whether-items-are-available-for-picking"></a>Athugaðu hvort hlutir séu tiltækir til að tína

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a>Til að búa til tínsluskjöl í lausu með tínsluvinnublaðinu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað tínslu** og velja síðan viðkomandi tengil.  

2. Valið er **Sækja vöruhúsaskjöl** aðgerð.  

    Listinn mun sýna útgefna framleiðslu, störf, samsetningarpantanir sem hafa verið sendar til tínsluaðgerðarinnar. Pantanir innihalda þær sem tínsluleiðbeiningar hafa þegar verið búnar til. Skjöl með tínslulínum sem hafa verið alveg tínd og skráð eru ekki sýnd á þessum lista.  
3. Veldu pantanir sem þú vilt undirbúa val fyrir.

    > [!NOTE]  
    > Ef þú velur skjal sem hefur nú þegar leiðbeiningar fyrir allar línur sínar, [!INCLUDE [prod_short](includes/prod_short.md)] upplýsir þig um að ekkert sé að höndla. Til að sameina þegar stofnaðar vöruhústínsluleiðbeiningar í eina tínsluleiðbeiningar skal eyða einstökum vöruhúsatínslum fyrst.

4. Reiturinn **Röðunaraðferð** er fylltur út til að raða línunum eins og óskað er eftir.  

    > [!NOTE]  
    > Hvernig línurnar eru flokkaðar í vinnublaðinu fer ekki sjálfkrafa í gegnum valleiðbeiningarnar. Samt sem áður eru sömu flokkunartæki fáanleg, ásamt röðun rusla. Þú getur auðveldlega endurskapað röð línanna sem þú skipuleggur í vinnublaðinu þegar þú býrð til tínsluleiðbeiningarnar eða með því að flokka tínsluleiðbeiningarnar.

5. Fylla inn í reitinn **Magn til afgreiðslu**. Velja aðgerðina **Færa sjálfkr. magn til afgr.** eða fyllið út reitina handvirkt.  

    Á síðunni er hægt að sjá tiltækt magn í hjáskipunarhólfum, sem er gagnlegt við áætlanagerð vinnuúthlutunar í aðstæðum hjáskipunar. [!INCLUDE[prod_short](includes/prod_short.md)] mun alltaf fyrst leggja til tiltekt úr hjáskipunarhólfi.

6. Ef þörf krefur, breyttu línunum handvirkt. Þú getur líka eytt sumum línum til að gera valið skilvirkara. Ef til að mynda til eru margar línur með vörum sem eru í hjáskipunarhólfum væri hægt að stofna tínslu fyrir allar línurnar. Hlutirnir sem eru í tengingu verða tíndir ásamt öðrum hlutum á upprunaskjalinu og hólfin sem hafa tengingu munu hafa pláss fyrir fleiri hluti sem koma inn.

    > [!NOTE]  
    >  Línunum er aðeins eytt af þessu vinnublaði, ekki úr vallista.  

7. Veldu aðgerðina **Stofna tínslu**. Síðan **Búa til val** opnast þar sem þú getur bætt frekari upplýsingum við valið.  

    Tilgreindu hvernig á að sameina tínslulínur í tínsluskjölunum með því að velja einn af eftirfarandi valkostum.  

    |Valkostur|Heimildasamstæða|
    |-|-|
    |Á Whse. Skjal|Býr til aðskilin tiltektarskjöl fyrir vinnublaðslínur með sama upprunaskjali vöruhúss.|
    |E. viðskm./lánardr./birgðag.|Býr til aðskilin valskjöl fyrir hvern viðskiptavin (störf)|
    |Eftir vöru|Býr til aðskilin tínsluskjöl fyrir hvern hlut í tínsluvinnublaðinu.|
    |Á frá-svæði|Býr til aðskilin valskjöl fyrir hvert svæði sem þú tekur hlutina frá.|
    |Eftir hólfi|Býr til aðskilin tínsluskjöl fyrir hverja bakka sem þú tekur hlutina úr.|
    |Eftir gjalddaga|Býr til aðskilin tiltektarskjöl fyrir upprunaskjöl sem hafa sama gjalddaga.|

    Tilgreindu hvernig á að búa til tiltektarskjölin með því að velja úr eftirfarandi valkostum.  

    |Valkostur|Heimildasamstæða|
    |-|-|
    |Hámark Nr. Af Pick Lines|Býr til valskjöl sem hafa ekki fleiri en tilgreindan fjölda lína í hverju skjali.|
    |Hámark Nr. Af Pick Source Docs.|Býr til valskjöl sem ná yfir allt að tilgreindan fjölda frumskjala.|
    |Úthlutað notandakenni|Stofnar tiltektarskjöl eingöngu fyrir vinnublaðslínur sem eru úthlutaðar á valda vöruhússstarfsmann.|
    |Röðunaraðferð f. tínslulínur|Veldu úr tiltækum valkostum til að raða línum í búnu tiltektarskjalinu.|
    |Setja einingaskiptingarafmörkun|Felur millihlutavallínur þegar stærri mælieiningu er breytt í minni mælieiningu og tínd að fullu.|
    |Ekki færa magn til afgreiðslu|Skilur eftir **Magn. að höndla**  reiturinn tómur á stofnuðum tínslulínum.|
    |Prenta tínslu|Prentar valskjölin þegar þau eru búin til. Þú getur líka prentað út úr tilbúnum valskjölum.|

8. Velja hnappinn **Í lagi**.  

## <a name="to-pick-items-for-a-productions-order-assembly-order-job"></a>Til að velja vörur fyrir framleiðslupöntun, samsetningarpöntun, verk

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tínslur** og velja síðan viðkomandi tengil.  

    Ef þú þarft að vinna í tilteknu vali skaltu velja valið af listanum eða sía listann til að finna valið sem hefur verið úthlutað til þín. Tínsluspjaldið er opnað.  
2. Ef **Úthlutað notandaauðkenni**  reiturinn er tómur, sláðu inn auðkenni þitt til að auðkenna þig, ef þörf krefur.  
3. Veldu hlutina.  

    Ef vöruhúsið er sett upp til að nota hólfa eru sjálfgefnar hólkar vörunnar notaðar til að benda á hvaðan á að taka vörurnar. Leiðbeiningarnar innihalda að minnsta kosti tvær aðskildar línur fyrir Taka og setja aðgerðir.  

    Rekstrarsvæði eins og framleiðslugólf gætu verið með sjálfgefið hólf fyrir íhluti sem þarf á að halda. Ef svo, þá er sjálfgefnum hólfakóða bætt við tínsluskjal vöruhússins til að gefa til kynna hvar á að setja vörurnar. Nánari upplýsingar er að finna í verkfæraleiðbeiningum fyrir **Kóði fyrir framleiðsluhólf**, hinn **Til-samsetningu ruslakóði**, hinn **To-Job Bin Code**  sviðum.

    Ef vöruhúsið er sett upp til að nota beint frágang og tínslu eru hólfaröðunin notuð til að reikna út bestu hólfin til að tína úr. Stungið er upp á þeim tunnunum á plokkunarlínunum. Leiðbeiningarnar innihalda að minnsta kosti tvær aðskildar línur fyrir Taka og setja aðgerðir.  

    * Fyrsta línan, með **Taka** í reitnum **Aðgerðagerð**, gefur til kynna hvar hlutirnir eru staðsettir á tínslusvæðinu. Ef þú ert að senda mikið af vörum á einni sendingarlínu gætirðu þurft að velja vörurnar í nokkrum hólfum, þannig að það er Taka lína fyrir hverja tunnu.
    * Næsta lína, með **Place** í reitnum **Aðgerðartegund**, sýnir hvar þú verður að staðsetja vörurnar í vöruhúsinu. Þú getur ekki breytt svæði og rusli á þessari línu.

    > [!NOTE]
    > Ef þú verður að velja eða setja hlutina fyrir eina línu í fleiri en eina tunnu, til dæmis vegna þess að tilnefnda tunnan er full, notaðu **Skipta línu** aðgerðina á **Línur** Flýtiflipi. Aðgerðin býr til línu fyrir það magn sem eftir er til að meðhöndla.

4. Eftir að þú hefur valið og sett hlutina í framleiðslu-, samsetningar- eða vinnusvæðið eða hólfuna skaltu velja **Skrá Velja** aðgerðina.  

    Þú getur nú komið með vörurnar á viðkomandi svæði og bókað notkun eða neyslu tiltekinna íhluta með því að bóka notkunarbók, samsetningarpöntun eða verkbók. Eftirfarandi greinar veita frekari upplýsingar:

    * [Skráðu neyslu og afköst fyrir eina útgefna framleiðslupöntunarlínu](production-how-to-register-consumption-and-output.md)
    * [Sameina vörur](assembly-how-to-assemble-items.md)
    * [Skrá neyslu eða notkun fyrir verk](projects-how-record-job-usage.md)

## <a name="flushing-production-components-in-an-advanced-warehouse-configuration"></a>Skola framleiðsluíhluti í háþróaðri vöruhúsauppsetningu

Skolaaðferðir hafa áhrif á flæði íhluta í framleiðslu. Lærðu meira á [Skolunaríhlutir samkvæmt aðgerðaútgangi](production-how-to-flush-components-according-to-operation-output.md). Það fer eftir völdum skolunaraðferð, þú getur valið íhluti til framleiðslu á eftirfarandi hátt:

* Notaðu **Vöruhúsval** skjal til að skrá valið fyrir vörur sem nota **Manual** skolunaraðferðina. Þú þarft að skrá neyslu sérstaklega. Frekari upplýsingar eru á [Neysla eftir framleiðslu lotu](production-how-to-post-consumption.md).
* Notaðu **Vöruhúsval** skjal til að skrá valið fyrir vörur sem nota **Velja + Áfram**, **Velja + afturábak** skoðaaðferð. Neysla á íhlutunum mun gerast sjálfkrafa annað hvort þegar þú breytir stöðu framleiðslupöntunarinnar eða með því að hefja eða ljúka aðgerð. Allir nauðsynlegir íhlutir verða að vera tiltækir. Annars, að bóka tæmd neyslustöðvun fyrir þann íhlut.
* Notaðu **Warehouse Movement** skjal án tilvísunar í upprunaskjal eða aðrar leiðir til að skrá hreyfingu íhluta sem nota **Forward** eða **Afturábak** skoðaaðferð. Íhlutir eru sjálfkrafa notaðir annað hvort þegar þú breytir stöðu framleiðslupöntunarinnar eða byrjar eða lýkur aðgerð. Allir nauðsynlegir íhlutir verða að vera tiltækir. Að öðrum kosti hættir bókun á skolaðri notkun fyrir þann íhlut. Frekari upplýsingar eru á [Flytja hluti](warehouse-move-items.md).

### <a name="example"></a>Dæmi

Þú ert með framleiðslupöntun fyrir 15 PCS af vörunni SP-SCM1004. Sum atriðanna á íhlutalistanum verður að skola handvirkt í neysludagbók. Hægt er að velja og skola aðra hluti sjálfkrafa með því að nota **Pick + Backward** skolaaðferðina.  

Eftirfarandi skref lýsa aðgerðum sem mismunandi fólk grípur til og viðbrögðunum sem þeim fylgja:  

1. Yfirmaður vinnusalar losar framleiðslupöntunina. Hlutir með **Áfram** skolunaraðferð og engan vegtengil eru dregnir frá opnu búðargólfinu.  
2. Umsjónarmaður verkstæðishæðar velur **Búa til vöruhúsval** aðgerðina á framleiðslupöntuninni. Tínsluskjal vöruhúss er stofnuð tínsla fyrir vörur með birgðaskráningaaðferðunum **Handvirkt**, **Tína + afturábak** og **Tína + Framvirk**. Þessar vörur eru settar í hólfkóða framleiðslu á útleið.  
3. Vöruhússtjóri úthlutar tínslunum til vöruhússstarfsmanns.  
4. Vöruhússtarfsmaður velur vörurnar úr viðeigandi hólfum og setur þær í Til-framleiðslu hólfið eða í hólfið sem tilgreint er á vöruhúsatínslunni. Bakkan getur verið vinnustöð eða vélamiðstöð.
5. Starfsmaður vöruhússins skráir tínsluna. Magnið er flutt úr tínslutunnunni í neyslutunnuna. Reiturinn **Tínt magn** á íhlutalistanum fyrri allar tíndar vörur er uppfærður.

    > [!NOTE]  
    >  Aðeins er hægt að neyta þess magns sem valið er.  
6. Starfsmaður á vél upplýsir framleiðslustjóra um það þegar endanlegar vörur eru fullunnar.
7. Umsjónarmaður verkstæðisgólfs notar neysludagbók eða framleiðslubók til að bóka neyslu á íhlutum sem nota annaðhvort **Manual** skolunaraðferðina.
8. Umsjónarmaður verkstæðisgólfs notar úttaksbók eða framleiðslubók til að bóka úttakið. Magn íhlutahluta sem nota **Velja + Áfram** eða **Valja + Til baka** skolunaraðferðir með leiðartenglum er dregið frá tunnuna til framleiðslu.
9. Framleiðslustjóri breytir stöðu framleiðslupöntunarinnar í **Lokið**. Magn íhluta sem nota **afturábak** skolunaraðferð er dregið frá opnu búðargólfinu og magn íhluta sem nota **Veldu + Afturábak** skolunaraðferð og enginn leiðartengill er dreginn frá To-Production ruslinu.  

Eftirfarandi mynd sýnir þegar reiturinn **Hólfkóti** á efnisþáttalista er fylltur út út frá staðsetningu notanda eða uppsetningu vinnuvélar-/vinnustöðvarmiðstöðvar.  

:::image type="content" source="media/binflow.png" alt-text="Yfirlit yfir hvenær og hvernig reiturinn Hólfkóði er fylltur út.":::

## <a name="see-also"></a>Sjá einnig .

- [Stjórna birgðum](inventory-manage-inventory.md)  
- [Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
- [Samsetningardeild](assembly-assemble-items.md)  
- [Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)
- [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
