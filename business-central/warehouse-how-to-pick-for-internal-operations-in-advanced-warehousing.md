---
title: Tína fyrir innri aðgerðir í ítarlegri vöruhúsaskilgreiningu
description: 'Ef birgðageymslurnar nota tínslu og afhendingu skal velja tínsluíhluti fyrir framleiðslu, samsetningu og verkaðgerðir á síðu vöruhúsatínslunnar.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 04/23/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Tína fyrir framleiðslu, samsetningu eða vinnslur í ítarlegum vöruhússkilgreiningum

Hvernig íhlutir eru tíndir fyrir framleiðslu, verk eða samsetningarpantanir fer eftir því hvernig vöruhúsið er sett upp sem birgðageymsla. Nánari upplýsingar um [uppsetningu vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Í ítarlegri vöruhúsagrunnstillingu fyrir útleiðarflæði (tínslu) er kveikt á vísbendingunum **Krefjast tínslu** og **Krefjast afhendingar** á síðunni **Birgðageymsluspjald** fyrir birgðageymsluna.

Þegar birgðageymslan er sett upp til að krefjast tínsluvinnslu og vöruhúsaafhendingarvinnslu skal nota vöruhúsatínsluskjöl til að stofna og vinna tínsluupplýsingar áður en notkun eða notkun íhluta er bókuð.  

Ekki er hægt að stofna vöruhúsatínsluskjal frá grunni. Tínslur eru hluti af verkflæði þar sem einstaklingur sem er að vinna pöntun stofnar þær á tísku eða starfsmaður vöruhússins stofnar þær á toga í tísku:

- Á ýta tísku, þar sem aðgerðin Stofna tínslu er notuð á síðunni **Framleiðslupöntun**, **Samsetningarpöntun,Verkspjald** **·**. **·**  Velja skal línurnar til að tína og undirbúa tínslurnar með því að tilgreina, til dæmis hvaða hólf á að taka úr og setja í og hversu margar einingar á að meðhöndla. Hægt er að forskilgreina hólf fyrir vöruhúsastaðinn eða forðann.
- Á toga í tísku, þar sem **Framleiðslupöntun**, **Samsetningarpöntun**, **Verkspjald** til vöruhúss gerir vörurnar tiltækar fyrir tínslu. Á síðunni **Vinnublað** tínslu geta starfsmenn vöruhússins notað aðgerðina **Sækja vöruhúsaskjöl** til að draga úthlutaðar tínslur.

Ef tína á eða flytja íhluti fyrir upprunaskjöl á toga í tísku verður að gefa út upprunaskjalið til að það sé tilbúið fyrir tínslu. Upprunaskjöl eru gefin út fyrir innri aðgerðir á eftirfarandi hátt.  

|Upprunaskjal|Losunaraðferð|  
|---------------------|--------------------|  
|Framleiðslupöntun|Breyta pöntunarstöðu í Útgefin eða stofna útgefna framleiðslupöntun strax.|  
|Samsetningarpöntun|Breyta stöðu í Útgefið.|
|Verk | Breyta stöðu í Opið eða stofnað verk með stöðuna Opið strax.|  

## Framleiðsla

Nota **vöruhúsatínsluskjöl** til að tína framleiðsluíhluti í flæði til framleiðslu.

Í birgðageymslu sem notar hólf til að færa vörur í opnar vinnusalarhólf er hægt að nota eftirfarandi aðferðir:

* Fyrir birgðageymslu sem notar beinan frágang og tínslu skal fylgja skrefunum í hlutanum [Færa vörur í ítarlegri grunnstillingu vöruhúss](warehouse-how-to-move-items-in-advanced-warehousing.md) .
* Fyrir aðrar birgðageymslur skal fylgja skrefunum í hlutnum Færa vörur innri í greininni [Grunnvörugrunnstilling vöruhúss](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) .

## Samsetning  

Nota **vöruhúsatínsluskjöl** til að flytja samsetningaríhluti í samsetningarsvæðið.

[!INCLUDE [prod_short](includes/prod_short.md)] styður samsetningar-til-lager og setja saman til pöntunar tegundir samsetningarflæðis. Nánari upplýsingar um samsetningu eftir pöntunum í vöruhúsaflæði út er farið [í Meðhöndlun samsetningarvara í vöruhúsaafhendingum](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

## Verkefnastjórnun  

Nota **vöruhúsatínsluskjöl** til að tína verkíhluti í flæðinu til verkefnastjórnunar.

> [!NOTE]
> Getu til að tína íhluti fyrir verkáætlunarlínur var bætt [!INCLUDE[d365fin](includes/d365fin_md.md)] við í 2022 útgáfubylgju 2. Til að byrja að nota möguleikann verður stjórnandi að kveikja á **Eiginleikastjórnun: Virkja birgða- og vöruhúsatínslu úr verkum** á síðunni **Eiginleikastjórnun**.
>
> Verk styðja ekki ítarlegar grunnstillingar þar sem kveikt er á beinu **tínslu- og frágangsvíkkuninni** .

## Kanna hvort vörur séu tiltækar til tínslu

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

## Tínsluskjöl stofnuð með tínsluvinnublaðinu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað tínslu** og velja síðan viðkomandi tengil.  

2. Valið er **Sækja vöruhúsaskjöl** aðgerð.  

    Listinn sýnir útgefna framleiðslu, verk, samsetningarpantanir sem hafa verið framsendar í tínsluaðgerðina. Í pöntununum eru þær sem tínsluleiðbeiningar hafa þegar verið stofnaðar fyrir. Skjöl með tínslulínur sem hafa verið tíndar og skráðar birtast ekki á þessum lista.  
3. Pantanirnar sem undirbúa á tínslu fyrir eru valdar.

    > [!NOTE]  
    > Ef valið er fylgiskjal sem þegar er með leiðbeiningar fyrir allar línur þess er [!INCLUDE [prod_short](includes/prod_short.md)]  tilkynnt að ekkert sé til meðhöndlunar. Til að sameina vöruhúsatínsluleiðbeiningarnar sem þegar hafa verið stofnaðar í eina tínsluleiðbeiningar er einstökum vöruhúsatínslum eytt fyrst.

4. Reiturinn **Röðunaraðferð** er fylltur út til að raða línunum eins og óskað er eftir.  

    > [!NOTE]  
    > Það hvernig línunum er raðað á vinnublaðinu flyst ekki sjálfkrafa í tínsluleiðbeiningarnar. Hins vegar eru sömu röðunarverkfæri tiltæk ásamt hólfaflokkun. Auðvelt er að endurgera röð línanna sem áætlaðar eru á vinnublaðinu þegar tínsluleiðbeiningarnar eru stofnaðar eða með því að raða í tínsluleiðbeiningunum.

5. Fylla inn í reitinn **Magn til afgreiðslu**. Velja aðgerðina **Færa sjálfkr. magn til afgr.** eða fyllið út reitina handvirkt.  

    Á síðunni er hægt að sjá tiltækt magn í hjáskipunarhólfum, sem er gagnlegt við áætlanagerð vinnuúthlutunar í aðstæðum hjáskipunar. [!INCLUDE[prod_short](includes/prod_short.md)] mun alltaf fyrst leggja til tiltekt úr hjáskipunarhólfi.

6. Línunum er breytt handvirkt ef með þarf. Einnig er hægt að eyða sumum línunum til að gera tínsluna skilvirkari. Ef til að mynda til eru margar línur með vörum sem eru í hjáskipunarhólfum væri hægt að stofna tínslu fyrir allar línurnar. Hjáskipunarvörurnar eru tíndar með öðrum vörum á upprunaskjalinu og hjáskipunarhólfin hafa pláss fyrir fleiri vörur á innleið.

    > [!NOTE]  
    >  Línunum er aðeins eytt af þessu vinnublaði, ekki af tínsluvallistanum.  

7. Veldu aðgerðina **Stofna tínslu**. Síðan **Stofna tínslu** opnast, þar sem hægt er að bæta við upplýsingum um tínsluna.  

    Tilgreina hvernig á að sameina tínslulínur í tínsluskjölum með því að velja einn af eftirfarandi valkostum.  

    |Valkostur|Heimildasamstæða|
    |-|-|
    |Á vöruh. Skjal|Stofnar sérstök tínsluskjöl fyrir vinnublaðslínur með sama upprunaskjali vöruhúss.|
    |E. viðskm./lánardr./birgðag.|Stofnar sérstök tínsluskjöl fyrir hvern viðskiptamann (verk)|
    |Eftir vöru|Stofnar sérstök tínsluskjöl fyrir hverja vöru á tínsluvinnublaðinu.|
    |Á frá-svæði|Stofnar sérstök tínsluskjöl fyrir hvert svæði sem vörur eru teknar frá.|
    |Eftir hólfi|Stofnar sérstök tínsluskjöl fyrir hvert hólf sem vörurnar eru teknar úr.|
    |Eftir eindaga|Stofnar sérstök tínsluskjöl fyrir upprunaskjöl sem hafa sama gjalddaga.|

    Tilgreina hvernig tínsluskjöl eru stofnuð með því að velja úr eftirfarandi valkostum.  

    |Valkostur|Heimildasamstæða|
    |-|-|
    |Max. Nr. tínslulína|Stofnar tínsluskjöl sem hafa ekki meira en tilgreindan fjölda lína í hverju fylgiskjali.|
    |Max. Nr. tínsluupprunaskjala|Stofnar tínsluskjöl sem ná til tilgreinds fjölda upprunaskjala.|
    |Úthlutað notandakenni|Stofnar tínsluskjöl eingöngu fyrir vinnublaðslínur sem eru tengdar völdum vöruhúsastarfsmanni.|
    |Röðunaraðferð f. tínslulínur|Velja skal úr tiltækum valkostum til að raða línum í tínsluskjalinu sem stofnað er.|
    |Setja einingaskiptingarafmörkun|Felur millieiningatínslulínur þegar stærri mælieiningu er breytt í smærri mælieiningu og tíndar.|
    |Ekki fylla magn til afgreiðslu|Skilur eftir auðan reitinn **Magn til afgreiðslu** í tínslulínunum sem stofnaðar voru.|
    |Prenta tínslu|Prentar tínsluskjölin þegar þau eru stofnuð. Einnig er hægt að prenta úr tínsluskjölum sem stofnuð eru.|

8. Velja hnappinn **Í lagi**.  

## Til að tína vörur fyrir framleiðslupöntun, samsetningarpöntun, verk

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tínslur** og velja síðan viðkomandi tengil.  

    Ef vinna þarf í tiltekinni tínslu er tínslan valin af listanum eða listinn afmarkaður til að finna tínslurnar sem hafa verið úthlutaðar. Tínsluspjaldið er opnað.  
2. Ef reiturinn **Úthlutað notandakenni** er auður er kenni notanda fært inn til að auðkenna sig, ef þörf krefur.  
3. Vörurnar eru tíndar.  

    Ef vöruhúsið er sett upp fyrir hólf eru sjálfgefin hólf vörunnar notuð til að leggja til hvaðan taka eigi vörurnar. Leiðbeiningarnar innihalda að minnsta kosti tvær aðskildar línur fyrir Aðgerðirnar Taka og Setja.  

    Rekstrarsvæði eins og framleiðslugólf gætu verið með sjálfgefið hólf fyrir íhluti sem þarf á að halda. Ef svo, þá er sjálfgefnum hólfakóða bætt við tínsluskjal vöruhússins til að gefa til kynna hvar á að setja vörurnar. Nánari upplýsingar eru í verkfærunum **fyrir hólfakóta** verkefnaframleiðslu, **Hólfakóti** verkefnis **og Kóti** verkefnahólfs.

    Ef vöruhúsið er sett upp til að nota beinan frágang og tínslu eru hólfaflokkanir notaðar til að reikna út bestu hólfin til að tína úr. Þessi hólf eru lögð til í tínslulínunum. Leiðbeiningarnar innihalda að minnsta kosti tvær aðskildar línur fyrir Aðgerðirnar Taka og Setja.  

    * Fyrsta línan með **Taka** í reitnum **Aðgerð** gefur til kynna hvar vörurnar eru staðsettar á tínslusvæðinu. Ef verið er að afhenda margar vörur í einni afhendingarlínu gæti þurft að tína vörurnar í mörgum hólfum þannig að taka-lína er fyrir hvert hólf.
    * Næsta lína, með **Setja** í reitnum **Aðgerð**, sýnir hvar setja á vörurnar í vöruhúsinu. Ekki er hægt að breyta svæði og hólfi í línunni.

    > [!NOTE]
    > Ef tína þarf eða setja vörur í einni línu í fleiri en eitt hólf, til dæmis vegna þess að merkta hólfið er fullt, skal nota aðgerðina **Skipta línu** á flýtiflipanum **Línur** . Aðgerðin stofnar línu fyrir eftirstandandi magn sem á að meðhöndla.

      Hægt er að raða tínslulínunum eftir ýmsum skilyrðum, til dæmis eftir vöru, hillunúmeri eða gjalddaga. Röðun getur hjálpað til við að fínstilla frágangsferlið, til dæmis:

    * Ef taka- og setja-línur fyrir hverja afhendingarlínu fylgja ekki hver annarri á ekki strax að fylgja og þess er óskað skal raða línunum með því að velja **Vara** í reitnum **Röðunaraðferð** .  
    * Ef hólfaflokkanir endurspegla raunútlit vöruhússins er röðunaraðferðin Hólfaflokkun **notuð** til að skipuleggja verkið eftir hólfastaðsetningum.

  > [!NOTE]  
  > Línum er raðað í hækkandi röð eftir völdum skilyrðum. Ef raðað er eftir fylgiskjali fer röðun fyrst eftir tegund fylgiskjals samkvæmt reitnum **Upprunaskjal vöruhúsaaðgerðar** . Ef raðað er eftir sendist-til er röðun framkvæmd fyrst eftir tegund áfangastaðar sem byggð er á reitnum **Tegund** viðtöku vöruhúss.

4. Þegar vörurnar hafa verið tíndar og settar í framleiðsluna, samsetninguna eða verksvæðið eða hólfið skal velja aðgerðina **Skrá tínslu** .  

    Nú er hægt að koma vörunum á viðeigandi svæði og bóka notkun eða notkun tíndra íhluta með því að bóka notkunarbók, samsetningarpöntun eða verkbók. Eftirfarandi greinar veita nánari upplýsingar:

    * [Skrá notkun og frálag fyrir eina línu útgefinnar framleiðslupöntunar](production-how-to-register-consumption-and-output.md)
    * [Sameina vörur](assembly-how-to-assemble-items.md)
    * [Skrá neyslu eða notkun fyrir verk](projects-how-record-job-usage.md)

## Birgðaskráning framleiðsluíhluta í ítarlegri vöruhúsaskilgreiningu

Birgðaskráningaraðferðir hafa áhrif á flæði íhluta í framleiðslu. Fræðast meira um birgðaskráningu [íhluta eftir frálagi aðgerða](production-how-to-flush-components-according-to-operation-output.md). Hægt er að tína íhluti fyrir framleiðslu om á eftirfarandi hátt, allt eftir valinni birgðaskráningaraðferð:

* Nota vöruhúsatínsluskjal **til** að skrá tínslu fyrir vörur sem nota **handvirka** birgðaskráningaraðferð. Skrá þarf notkun sérstaklega. Nánari upplýsingar um [Fjöldabóka framleiðslunotkun](production-how-to-post-consumption.md).
* Nota vöruhúsatínsluskjal **til** að skrá tínslu fyrir vörur sem nota **tínslu + Framvirkt,Tína** **+ Afturvirk** söfnunaraðferð. Notkun íhluta gerist annaðhvort sjálfkrafa þegar stöðu framleiðslupöntunarinnar er breytt eða með því að hefja eða ljúka aðgerð. Allir íhlutir sem þarf verða að vera tiltækir. Annars skal bóka birgðaskráningarnotkunarstöðvun fyrir þann íhlut.
*  **Nota vöruhúsahreyfingarskjal** án vísunar í upprunaskjal eða aðrar leiðir til að skrá hreyfingu á íhlutum sem nota birgðaskráningaraðferðina **Framvirk** eða **Afturvirk** . Íhlutir eru sjálfkrafa notaðir annaðhvort þegar stöðu framleiðslupöntunar er breytt eða aðgerð er hafin eða hún lýkur. Allir íhlutir sem þarf verða að vera tiltækir. Annars stöðvast birgðaskráning notkun fyrir þann íhlut. Nánari upplýsingar um flutning á [atriðum](warehouse-move-items.md).

### Dæmi

Framleiðslupöntun er fyrir 15 stk af vöru sp-SCM1004. Sumar af vörunum á íhlutalistanum þarf að birgðaskrá handvirkt í notkunarbók. Hægt er að tína og birgðaskrá aðrar vörur sjálfvirkt með því að nota **Tínslu + Afturvirk** birgðaskráningaraðferð.  

Eftirfarandi skref lýsa aðgerðunum sem mismunandi einstaklingar framkvæma og tengt svar:  

1. Yfirmaður vinnusalar losar framleiðslupöntunina. Vörur með **birgðaskráningaraðferð framvirkt** og enginn leiðartengill eru dregnar frá opnu vinnusalarhólfi.  
2. Yfirmaður vinnusalar velur aðgerðina **Stofna vöruhúsatínslu** á framleiðslupöntuninni. Tínsluskjal vöruhúss er stofnuð tínsla fyrir vörur með birgðaskráningaaðferðunum **Handvirkt**, **Tína + afturábak** og **Tína + Framvirk**. Þessar vörur eru settar í hólfkóða framleiðslu á útleið.  
3. Vöruhúsastjórinn úthlutar tínslunni á vöruhúsastarfsmann.  
4. Starfsmaður í vöruhúsinu tínir vörurnar úr viðeigandi hólfum og setur þær í hólf framleiðslu eða í hólfið sem tilgreint er á vöruhúsatínslunni. Hólfið getur verið vinnu- eða vélastöðvarhólf.
5. Starfsmaður vöruhússins skráir tínsluna. Magnið er flutt úr tínsluhólfinu í notkunarhólfið. Reiturinn **Tínt magn** á íhlutalistanum fyrri allar tíndar vörur er uppfærður.

    > [!NOTE]  
    >  Aðeins er hægt að nota magnið sem er tínt.  
6. Starfsmaður á vél upplýsir framleiðslustjóra um það þegar endanlegar vörur eru fullunnar.
7. Yfirmaður vinnusalar notar notkunarbókina eða framleiðslubókina til að bóka notkun íhlutavara sem annaðhvort **nota Handvirk** birgðaskráningaraðferð.
8. Yfirmaður vinnusalar notar frálagsbókina eða framleiðslubókina til að bóka frálagið. Magn íhlutavara sem nota **Tínslu + Framvirkt** eða **Tína + Afturvirk** birgðaskráningaraðferðir með leiðartenglum er dregið frá hólfinu Í framleiðslu.
9. Framleiðslustjórinn breytir stöðu framleiðslupöntunarinnar **í Lokið**. Magn íhlutavara sem nota **afturvirka** birgðaskráningaraðferð er dregið frá opnu vinnusalarhólfi og magn íhluta sem nota **Tína + Afturvirk** birgðaskráningaraðferð og enginn leiðartengill er dreginn frá hólfi framleiðslu í framleiðslu.  

Eftirfarandi mynd sýnir þegar reiturinn **Hólfkóti** á efnisþáttalista er fylltur út út frá staðsetningu notanda eða uppsetningu vinnuvélar-/vinnustöðvarmiðstöðvar.  

:::image type="content" source="media/binflow.png" alt-text="Yfirlit yfir hvenær og hvernig reiturinn Hólfkóti er fylltur út.":::

## Framleiða íhluti sem framleiða eftir pöntun (MTO) í ítarlegri vöruhúsaskilgreiningu

Í tilvikum þar sem framleidd vara samanstendur af hráefni og hálfunninni vöru með framleiðslustefnuna sem stillt er á **Eftir pöntun** er vöruhúsatínslunni fyrir þessa hálfkláraða íhluti bætt við sömu framleiðslupöntun og **reiturinn Kóti** áætlunarstigs fylltur út. Búist er við að hálfunnin vara sé tiltæk til notkunar strax og ekki þarfnast tínslu svo þær séu ekki innifaldar í vöruhúsatínsluskjalinu. Stofnaðar vöruhúsatínslur innihalda aðeins hráefni fyrir framleidda vöru og fyrir hálfkláraðar vörur.

En ef hálfunnin vara er tiltæk á lager leggur áætlunarkerfið til að þær séu notaðar í stað þess að framleiða allt magnið. Framleidd vara krefst t.d. fimm hálfunninnar íhlutar en þrír eru þegar til á lager. Í þessu tilfelli eru fimm hálfkláraðar vörur skráðar í íhluti framleiðslupöntunarinnar en aðeins tvær eru framleiddar í sömu framleiðslupöntun og aðskilin framleiðslupöntunarlína.
Slík uppsetning er ekki samhæf vöruhúsatínslum og eftir tíðni þarf annað hvort að breyta framleiðslustefnunni fyrir slíka hálfkláraða vöru í **birgðir** eða skipta íhlutalínu framleiðslupöntunarinnar handvirkt þegar tína þarf hálfunnin vörur sem framleiddar voru fyrr.


## Sjá einnig .

- [Stjórna birgðum](inventory-manage-inventory.md)  
- [Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
- [Samsetningardeild](assembly-assemble-items.md)  
- [Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)
- [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
