---
title: Tína fyrir innri starfsemi með ítarlegum vöruhúsaskilgreiningum
description: 'Ef birgðageymslurnar nota tínslu og afhendingu skal velja tínsluíhluti fyrir framleiðslu, samsetningu og verkaðgerðir á síðu vöruhúsatínslunnar.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/02/2022
ms.author: bholtorf
---
# <a name="pick-for-production-assembly-or-jobs-in-advanced-warehouse-configurations"></a>Tínsla fyrir framleiðslu, samsetningu eða verk í ítarlegum vöruhúsastillingum

Val á íhlutum fyrir framleiðslu, vinnslur eða samsetningarpantanir fer eftir því hvernig vöruhúsið er sett upp sem Birgðageymsla. Frekari upplýsingar um  [uppsetningu vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Í ítarlegri skilgreiningu vöruhúsa fyrir flæði út (tínslu) er kveikt  **á krefjast tínslu**  og  **gerðar afhendingar**  á  **birgðageymsluspjaldinu**  fyrir birgðageymsluna.

Þegar birgðageymslan er sett upp þannig að krafist sé vöruhúsatínslu vinnslu og vöruhúsaafhendingarvinnslu eru notuð vöruhúsatínsluskjöl til að stofna og vinna úr tínsluupplýsingum áður en notkun eða notkun íhluta er bókuð.  

Ekki er hægt að stofna vöruhúsatínsluskjal frá grunni. Tínslur eru hluti af verkflæði þar sem einstaklingur sem er að vinna pöntun stofnar þá á þrýstihátt eða starfsmaður vöruhússins stofnar þá í togvinnslu:

- Á þrýstihátt, þar sem þú notar  **aðgerðina stofna tínslu**  í  **framleiðslupöntuninni**,  **á samsetningarpöntun**,  **vinnsluspjald**  -síðu. Velja línurnar til að taka til og undirbúa tínsluna með því að tilgreina, til dæmis, hvaða hólf eigi að ganga frá og setja í og hversu margar einingar eigi að afgreiða. Hólf geta verið forskilgreind fyrir vöruhúsastaðinn eða forðinn.
- Í togtísku, þar sem framleiðslupöntun  **er sleppt**,  **pöntunarpöntun**,  **vinnsluspjald**  til vöruhúss, sem gerir vörurnar tiltækar fyrir tiltekt. Síðan, á  **síðunni tínsluvinnublað**, geta starfsmenn vöruhúss notað  **skjölin sækja vöruhúsaskjöl**  til að draga úthlutaðar tínslur.

Til að taka til eða færa íhluti fyrir upprunaskjöl í togtísku þarf að gefa út upprunaskjalið til að gera það tilbúið til tínslu. Upprunaskjöl eru gefin út fyrir innri aðgerðir á eftirfarandi hátt.  

|Upprunaskjal|Losunaraðferð|  
|---------------------|--------------------|  
|Framleiðslupöntun|Breyið pöntunarstöðu til að gefa út eða stofna útgefna framleiðslupöntun.|  
|Samsetningarpöntun|Breyta stöðu í Útgefið.|
|Verk | Breyta stöðu til að opna eða stofna verk með stöðuna opið strax.|  

## <a name="production"></a>Framleiðsla

Nota  **vöruhúsatínsluskjöl**  fyrir tiltektarframleiðsluíhluti í flæði til framleiðslu.

Hægt er að nota eftirtaldar aðferðir fyrir birgðageymslu sem notar hólf til að færa vörur í opin vinnusalarhólf.

* Fyrir staðsetningu sem notar beinan frágang og tínslu er farið eftir skrefunum í  [vöruafbrigðasamskipunum í ítarlegum vöruhúsaskilgreiningum](warehouse-how-to-move-items-in-advanced-warehousing.md) .
* Fyrir aðra staði er fylgt skrefunum í Hreyfðu atriðunum sem  [eru óáætluð í skilgreiningum](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  grunnvöruhúsa.

## <a name="assembly"></a>Samsetning

Nota  **vöruhúsatínsluskjöl**  til að færa samsetningarhluta á samsetningarsvæðið.

[!INCLUDE [prod_short](includes/prod_short.md)] styður saman á lager og setja saman gerðir af samsetningarflæðigerðum. Til að fræðast meira um setja saman-pöntun í vöruhús á útleið er farið í  [meðferð með því að setja saman vörur í Vöruhúsasendingum](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

## <a name="project-management"></a>Verkefnastjórnun

Nota  **vöruhúsatínsluskjöl**  til að velja vinnsluíhluti í flæði til verkefnastjórnunar.

> [!NOTE]
> Getan til að tína íhluti fyrir veráætlunarlínur var bætt við [!INCLUDE[d365fin](includes/d365fin_md.md)] í 2022 útgáfutímabili 2. Til að byrja að nota möguleikann verður stjórnandi að kveikja á **Eiginleikastjórnun: Virkja birgða- og vöruhúsatínslu úr verkum** á síðunni **Eiginleikastjórnun**.
>
> Vinnslur styðja ekki ítarlegri skilgreiningar þar sem  **kveikt er á beini tínslu-**  og frágangsskipta.

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a>Tínsluskjöl stofnuð í fjöldavið tínsluvinnublaðið

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað tínslu** og velja síðan viðkomandi tengil.  

2. Valið er **Sækja vöruhúsaskjöl** aðgerð.  

    Listinn sýnir útgefna framleiðslu, vinnslur, samsetningarpantanir sem hafa verið framsendar í tínsluaðgerðina. Pantanirnar eru þær sem tínsluleiðbeiningar hafa þegar verið stofnaðar fyrir. Skjöl með tínslulínum sem hafa verið tekin endanlega til og skráð eru ekki sýnd á þessum lista.  
3. Veljið pantanirnar sem óskað er að undirbúa tínslu fyrir.

    > [!NOTE]  
    > Ef þú velur skjal sem hefur nú þegar leiðbeiningar fyrir allar línurnar þess,  [!INCLUDE [prod_short](includes/prod_short.md)]  upplýsir þú að ekkert sé hægt að afgreiða. Til að sameina þegar tínsluleiðbeiningar stofnaðist í eina tínslukennslu er einstökum vöruhúsatínslum eytt fyrst.

4. Reiturinn **Röðunaraðferð** er fylltur út til að raða línunum eins og óskað er eftir.  

    > [!NOTE]  
    > Því hvernig línunum er raðað á vinnublaðinu er ekki sjálfkrafa haldið við í tínsluleiðbeiningunum. Hins vegar eru sömu röðunarverkfærin tiltæk, ásamt hólfaflokkun. Auðveldlega er hægt að endurgera röð þeirra lína sem þú ætlar í vinnublaðinu þegar tínsluleiðbeiningarnar eru stofnaðar eða með því að raða í tínsluleiðbeiningarnar.

5. Fylla inn í reitinn **Magn til afgreiðslu**. Velja aðgerðina **Færa sjálfkr. magn til afgr.** eða fyllið út reitina handvirkt.  

    Á síðunni er hægt að sjá tiltækt magn í hjáskipunarhólfum, sem er gagnlegt við áætlanagerð vinnuúthlutunar í aðstæðum hjáskipunar. [!INCLUDE[prod_short](includes/prod_short.md)] mun alltaf fyrst leggja til tiltekt úr hjáskipunarhólfi.

6. Breytið línunum handvirkt ef þörf krefur. Einnig er hægt að eyða sumum línum til að gera tínsluna skilvirkari. Ef til að mynda til eru margar línur með vörum sem eru í hjáskipunarhólfum væri hægt að stofna tínslu fyrir allar línurnar. Hjáskipunarvörur skal taka með öðrum vörum sem eru á upprunaskjalinu og hjáhafnarhólfunum hafa rýmri heimild til að koma fyrir aðsendum vörum.

    > [!NOTE]  
    >  Línunum er aðeins eytt úr þessu vinnublaði, ekki úr listanum Tínsluval.  

7. Veldu aðgerðina **Stofna tínslu**.  **Síðan stofna tínslu**  opnast, þar sem hægt er að bæta meiri upplýsingum við tínsluna.  

    Tilgreinið hvernig eigi að sameina tínslulínur í tínsluskjöl með því að velja einn af eftirfarandi valkostum.  

    |Valkostur|Heimildasamstæða|
    |-|-|
    |Á vöruhúsaskjölum Skjal|Stofnar aðskilin tínsluskjöl fyrir vinnublaðslínur með sama upprunaskjali vöruhúss.|
    |E. viðskm./lánardr./birgðag.|Stofnar aðskilin tínsluskjöl fyrir hvern viðskiptavin (vinnslur)|
    |Eftir vöru|Stofnar aðskilin tínsluskjöl fyrir hverja vöru í tínsluvinnublaðinu.|
    |Á frá-svæði|Stofnar aðskilin tínsluskjöl fyrir hvert svæði sem taka á vörurnar úr.|
    |Eftir hólfi|Stofnar aðskilin tínsluskjöl fyrir hvert hólf sem taka á vörurnar úr.|
    |Eftir gjalddaga|Stofnar aðskilin tínsluskjöl fyrir upprunaskjöl sem hafa sama gjalddaga.|

    Tilgreinið hvernig á að stofna tínsluskjöl með því að velja úr eftirfarandi valkostum.  

    |Valkostur|Heimildasamstæða|
    |-|-|
    |Max. Nr. Um tínslulínur|Stofnar tínsluskjöl sem hafa ekki fleiri en tilgreindan línufjölda í hverju skjali.|
    |Max. Nr. Doktors Tínslusource.|Stofnar tínsluskjöl sem ná yfir tiltekinn fjölda upprunaskjala.|
    |Úthlutað notandakenni|Stofnar tínsluskjöl aðeins fyrir vinnublaðslínur sem er úthlutað á valinn vöruhúsastarfsmann.|
    |Röðunaraðferð f. tínslulínur|Veljið úr tiltækum valkostum til að raða línum í stofnaða tínsluskjalið.|
    |Setja einingaskiptingarafmörkun|Felur millitínslulínum einingatiltekt þegar stærri Mælieining er umbreytt í smærri mælieiningu og alveg tínd.|
    |Ekki færa magn til afgreiðslu| **Skilur reiturinn Magn til að halda**  við autt í tínslulínunum sem stofnaðar eru.|
    |Prenta tínslu|Prentar tínsluskjölin þegar þau eru stofnuð. Einnig er hægt að prenta úr stofnaða tínsluskjölum.|

8. Velja hnappinn **Í lagi**.  

## <a name="to-pick-items-for-a-productions-order-assembly-order-job"></a>Vörur tínslur til framleiðslupöntunar, samsetningarpöntun, vinnsla

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tínslur** og velja síðan viðkomandi tengil.  

    Ef vinna þarf við ákveðna tínslu er tínslan valin af listanum eða sía listann til að finna tínsluna sem hefur verið úthlutað. Tínsluspjaldið er opnað.  
2.  **Ef reiturinn úthlutað notandakenni**  er auður skal FÆRA inn kennið til að auðkenna notandann ef þörf krefur.  
3. Tínsla varanna.  

    Ef vöruhúsið er sett upp þannig að þau noti hólf eru sjálfgefnu hólfin í vörunum notuð til að leggja til hvaðan eigi að taka vörurnar. Leiðbeiningarnar innihalda að minnsta kosti tvær aðskildar línur til að taka og setja aðgerðir.  

    Rekstrarsvæði eins og framleiðslugólf gætu verið með sjálfgefið hólf fyrir íhluti sem þarf á að halda. Ef svo, þá er sjálfgefnum hólfakóða bætt við tínsluskjal vöruhússins til að gefa til kynna hvar á að setja vörurnar. Frekari upplýsingar er að finna í verkfærunum fyrir  **framl. kóti til-framleiðslu hólfs**,  **hólfkóta** til-samingar,  **í reitina til-kóti**  vinnslu.

    Ef vöruhúsið er sett upp til að nota beinan frágang og tínslu er bin fremstur notað til að reikna út bestu hólfin til tínslu úr. Þau hólf eru lögð til á tínslulínunum. Leiðbeiningarnar innihalda að minnsta kosti tvær aðskildar línur til að taka og setja aðgerðir.  

    * Fyrsta línan, með  **taka**  í  **reitnum aðgerðargerð**, gefur til kynna hvar vörurnar eru staðsettar á tiltektarsvæðinu. Ef mikið af vörum er í einni afhendingarlínu gæti þurft að tína vörurnar í nokkrum hólfum svo það sé lína fyrir hvert hólf.
    * Næsta lína, með  **stað**  í  **reitnum Tegund**  aðgerðar, sýnir hvar verður að setja vörurnar í vöruhúsinu. Ekki er hægt að breyta svæði og hólfi í þessari línu.

    > [!NOTE]
    > Ef taka þarf vörurnar í eina línu í fleiri en einu hólfi, til dæmis vegna þess að það merkta hólfið er fullt, skal nota  **aðgerðina skipta línu**  á  **fastflipanum línur** . Aðgerðin býr til línu fyrir eftirstandandi magn sem á að afgreiða.

4. Þegar búið er að velja og setja vörurnar í framleiðslu, samsetningu eða vinnslusvæði eða hólf skal velja  **aðgerðina skrá tínslu** .  

    Nú er hægt að koma vörunum á viðkomandi svæði og bóka notkun eða notkun á tíndum íhlutum með því að bóka notkunarbók, samsetningarpöntun eða verkbók. Eftirfarandi greinar veita nánari upplýsingar:

    * [Skrá notkun og úttak fyrir eina útgefna framleiðslupöntunarlínu](production-how-to-register-consumption-and-output.md)
    * [Sameina vörur](assembly-how-to-assemble-items.md)
    * [Skrá neyslu eða notkun fyrir verk](projects-how-record-job-usage.md)

## <a name="flushing-production-components-in-a-advanced-warehouse-configuration"></a>Birgðaveiðaíhlutir í ítarlegri samskipan vöruhúss

Flúorskolun hefur áhrif á flæði íhluta í framleiðslu.  [Frekari upplýsingar um Flush-íhluti eru í samræmi við afköst](production-how-to-flush-components-according-to-operation-output.md) aðgerðar. Eftir því hvaða birgðaaðferð er valin er hægt að velja íhluti fyrir framleiðslu á eftirfarandi hátt:

*  **Notið vöruhúsatínsluskjal**  til að skrá tínsluna fyrir vörur sem nota  **handvirku**  flæðiaðferðina. Þú þarft að skrá neyslu sérstaklega. Frekari upplýsingar um  [runubókun Framleiðslunotkunar](production-how-to-post-consumption.md).
*  **Nota skal skjal vöruhúsatínslu**  til að skrá tínsluna fyrir vörur sem nota  **tínsluna + áfram**,  **tína + afturábak**  birgðaflæðiaðferð. Notkun íhluta mun gerast sjálfkrafa annað hvort þegar stöðu framleiðslupöntunarinnar er breytt eða með því að ræsa eða ljúka aðgerð. Allir nauðsynlegir íhlutir verða að vera tiltækir. Annars er hætt að bóka notkun fyrir þann íhlut.
*  **Vöruhúsahreyfingskjal**  er notað án tilvísunar í upprunaskjali eða öðrum leiðum til að skrá hreyfingar þeirra íhluta sem nota  **framvirka**  eða  **afturvirku**  birgðaaðferðina. Íhlutir eru sjálfkrafa notaðir annaðhvort við breytingu á stöðu framleiðslupöntunar eða hefja eða enda á aðgerð. Allir nauðsynlegir íhlutir verða að vera tiltækir. Að öðrum kosti er hætt að bóka hreinsað notkun fyrir þann íhlut. Lærðu meira að  [flytja atriði](warehouse-move-items.md).

### <a name="example"></a>Dæmi

Þú ert með framleiðslupöntun fyrir 15 PCS af vöru SP-SCM1004. Sumar vörurnar á íhlutaliði verða að vera í Hreinsun handvirkt í notkunarbók. Aðrar vörur er hægt að taka til og sjálfvirkt með því að  **nota aðferðina tína + afturábak**  birgðaaðferð.  

Í eftirfarandi skrefum er lýst þeim aðgerðum sem ólíkir einstaklingar taka og tengdu viðbrögðin:  

1. Yfirmaður vinnusalar losar framleiðslupöntunina. Vörur með  **framflæðiaðferð**  og engin leiðartenging er dregin frá opna vinnslusalarhólfi.  
2. Eftirlitsaðili í Vinnusalarstjórnun velur  **aðgerðina stofna vöruhúsatínslu**  í framleiðslupöntuninni. Tínsluskjal vöruhúss er stofnuð tínsla fyrir vörur með birgðaskráningaaðferðunum **Handvirkt**, **Tína + afturábak** og **Tína + Framvirk**. Þessar vörur eru settar í hólfkóða framleiðslu á útleið.  
3. Vöruhúsastjórinn úthlutar starfsmanni í vöruhúsi.  
4. Starfsmaður í vöruhúsi tínir vörurnar úr viðeigandi hólfum og setur þær í framleiðsluhólfið eða í hólfið sem tilgreint er í vöruhúsatínslu. Hólfið getur verið vinnustöð eða vélastöð.
5. Starfsmaður í vöruhúsi skráir tínsluna. Magnið er flutt úr tínsluhólfinu í neysluhólfið. Reiturinn **Tínt magn** á íhlutalistanum fyrri allar tíndar vörur er uppfærður.

    > [!NOTE]  
    >  Aðeins er hægt að nota magnið sem er valið.  
6. Starfsmaður á vél upplýsir framleiðslustjóra um það þegar endanlegar vörur eru fullunnar.
7. Umsjónarmaður vinnslusalarhæðar notar notkunarbókina eða framleiðslubókina til að bóka notkun íhluta sem nota annaðhvort  **handvirka**  flæðiaðferð.
8. Umsjónarmaður vinnslusalarhæðar notar úttaksbók eða framleiðslubók til að bóka úttakið. Fjöldi íhluta sem nota  **tínsluvörur**  eða  **tínsla + afturvirkar**  birgðaaðferðir með leiðartenglum er dreginn frá framleiðslu hólfa.
9. Framleiðustjóri breytir stöðu framleiðslupöntunarinnar í  **lokið**. Magn íhluta sem nota  **afturvirka**  birgðaaðferð er dregið frá opna vinnslusalarhólfi og magn íhlutavara sem nota  **+ afturbirgðaskráningaraðferð**  og enginn Leiðartengill er dreginn frá framleiðslu hólfa.  

Eftirfarandi mynd sýnir þegar reiturinn **Hólfkóti** á efnisþáttalista er fylltur út út frá staðsetningu notanda eða uppsetningu vinnuvélar-/vinnustöðvarmiðstöðvar.  

:::image type="content" source="media/binflow.png" alt-text="Yfirlit um hvenær og hvernig reiturinn Hólfakóti er fylltur út.":::

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Warehouse Management Overview](design-details-warehouse-management.md)
[Work with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
