---
title: 'Tína eða færa vörur fyrir framleiðslu, samsetningu eða verk í grunngrunnstillingum vöruhúss'
description: Þegar vöruhúsið þitt krefst þess að þú vinnir úr tínslum en ekki sendum skaltu nota birgðatínslusíðuna til að skrá að íhlutir hafi verið tíndir.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.forms: '9330, 931, 990008, 89, 900, 902'
---
# Tínsla fyrir framleiðslu, samsetningu eða verk í einfaldri vöruhúsagrunnstillingu

Hvernig íhlutir eru tíndir fyrir framleiðslu, verk eða samsetningarpantanir fer eftir því hvernig vöruhúsið er sett upp sem birgðageymsla. Nánari upplýsingar um [uppsetningu vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Í einfaldri vöruhúsaskilgreiningu fyrir útleiðarflæðið (tínslu) á **síðunni Birgðageymsluspjald** fyrir birgðageymsluna skal kveikja á krefjast tínsluskipta **en slökkva á** vífærinu **Krefjast afhendingar** .

Nota eftirfarandi skjöl fyrir innri aðgerðir:

* Birgðatínsla
* Birgðahreyfing

## Birgðatínslur

* Þegar birgðatínsla er skráð fyrir innanhússaðgerð, t.d. framleiðslu eða verk, er notkun tíndra íhluta bókuð samtímis.
* Hólfið **áskilið** á síðunni **Birgðageymsluspjald** er valfrjálst.
* Þegar birgðatínslur eru notaðar skilgreinir reiturinn **Hólfkóti** á íhlutalínu framleiðslupöntunar eða verkáætlunarlínur taka *hólfið* . Íhlutum er fækkað í taka-hólfi þegar notkun er bókuð.

## Birgðahreyfingar

* Birgðahreyfingar krefjast þess að kveikt sé á hólfinu **áskilin vísbending** á síðunni **Birgðageymsluspjald** fyrir birgðageymsluna.
* Birgðahreyfingar vinna aðeins með íhlutalínur framleiðslupöntunar og samsetningarpöntunarlínur.
* Þegar birgðahreyfing er skráð fyrir innri aðgerð er efnisleg hreyfing íhluta aðeins skráð í hólf á aðgerðasvæðinu. Þú bókar ekki notkun.
* Þegar birgðahreyfingar eru notaðar skilgreinir reiturinn **Hólfkóti** á íhlutalínum framleiðslupöntunar hvaða stað *hólfið er á aðgerðasvæðinu.*  Staðahólfið er þar sem starfsmenn vöruhúsa verða að setja íhlutina.
* Skrá notkun tíndra íhluta sérstaklega með því að bóka notkunarbók eða samsetningarpöntun.

>[!NOTE]
> Jafnvel þótt slökkt sé á **tínsluákvörðuninni** er hægt að nota **vöruhúsatínsluskjal** . Vöruhúsatínsluskjöl líkjast **birgðatínsluskjölum** . Þetta er gagnlegt ef nota á tínslur í aðgerðum og afhenda í vöruhúsaflæði á útleið.

### Framleiðsla

Nota birgðatínsluskjöl **fyrir** tínslu framleiðsluíhluta í flæði til framleiðslu.

Í birgðageymslu sem notar hólf er hægt að lengja flæðið til framleiðslu með því að nota **Birgðahreyfingarskjöl** . Birgðahreyfingar eru sérstaklega gagnlegar fyrir birgðaskráningu íhluta. Nánari upplýsingar um hvernig íhlutanotkun er birgðaskráð úr Verkefnaframleiðslu eða Opnum vinnusalarhólfum er farið [í Birgðaskráning framleiðsluíhluta í einfaldri vöruhúsgrunnstillingu](#flushing-production-components-in-a-basic-warehouse-configuration).

### Samsetning  

Nota **skjöl birgðahreyfingar** til að færa samsetningaríhluti í samsetningarsvæðið.

> [!NOTE]
> **Birgðahreyfingarskjöl** þurfa hólf.

[!INCLUDE [prod_short](includes/prod_short.md)] styður samsetningar-til-lager og setja saman til pöntunar tegundir samsetningarflæðis. Nánari upplýsingar um samsetningu eftir pöntunum í vöruhúsaflæði út er farið [í Meðhöndlun á vörum samsetninga á pöntunum með birgðatínslum](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### Verkefnastjórnun  

Nota **birgðatínsluskjöl** til að tína verkíhluti í flæðinu til verkefnastjórnunar.

Í birgðageymslum sem nota hólf er hægt að lengja flæði til verka með **skjölum birgðahreyfinga** .

> [!NOTE]
> Getu til að tína íhluti fyrir verkáætlunarlínur var bætt [!INCLUDE[d365fin](includes/d365fin_md.md)] við í 2022 útgáfubylgju 2. Til að byrja að nota möguleikann verður stjórnandi að kveikja á **Eiginleikastjórnun: Virkja birgða- og vöruhúsatínslu úr verkum** á síðunni **Eiginleikastjórnun**.
>
> [!INCLUDE[prod_short](includes/prod_short.md)] notar gildið í reitnum **Eftirstöðvar (magn**) í verkáætlunarlínunni þegar það stofnar birgðatínslur. Til að nota birgðatínslur fyrir verk verður að kveikja á vífærslunni **Beita notkunartengli** á **síðunni Verkspjald** fyrir verkið. Þetta gerir þér kleift að fylgjast með notkun miðað við áætlun þína. Ef þú kveikir ekki á víxlhnappnum verða eftirstöðvarnar í **0** og birgðatínslan verður ekki búin til. Nánari upplýsingar um hvernig setja á [upp notkunarrakningu verkefnis](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-project-usage-tracking).

## Tína eða flytja fyrir framleiðslu, samsetningu og verkefni í einfaldri vöruhúsaskilgreiningu

Hægt er að stofna birgðatínslu eða birgðahreyfingu á þrjá vegu:  

* Úr upprunaskjalinu sjálfu.  
* Fyrir nokkur upprunaskjöl á sama tíma með því að nota keyrslu.  
* Í tveim þrepum. Upprunaskjalið er gefið út til að gera upprunaskjalið tilbúið fyrir tínslu. Stofna birgðatínslu eða hreyfingu úr skjölunum **Birgðatínsla** eða **Birgðahreyfing** . Birgðatínslan eða hreyfingin byggist á upprunaskjalinu.  

### Birgðatínsla stofnuð í upprunaskjali:

1. Í upprunaskjalinu, sem getur verið framleiðslupöntun eða verk, skal velja aðgerðina **Stofna birgðafrágang/tínslu** .  
2. Velja skal reitinn **Stofna birgðafrávik Tínslureiturinn** .
3. Velja hnappinn **Í lagi**.

### Stofnun birgðahreyfingar úr upprunaskjalinu

1. Á upprunaskjalinu, sem getur verið framleiðslupöntun, samsetningarpöntun eða verk, skal velja aðgerðina **Stofna birgðafrágang/tínslu** .  
2. Velja skal reitinn **Stofna birgðafrávik Gátreiturinn Hreyfing** .
3. Velja hnappinn **Í lagi**.

### Til að stofna margar birgðatínslur eða hreyfingar með keyrslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn **Stofna birgðafrágang/tínslu/hreyfingu** og velja síðan viðeigandi tengil.  
2. Á flýtiflipanum **Vöruhúsabeiðni** skal nota **Upprunaskjal og** Upprunanúmer **.** til að afmarka eftir tegundum fylgiskjala eða sviðum fylgiskjalanúmera. Til dæmis er aðeins hægt að stofna tínslur fyrir framleiðslupantanir.
3. Á flýtiflipanum **Valkostir** er kveikt á reitnum **Stofna birgðafrávik. Tína eða** Stofna birgðatínslu **Hreyfingavígsla** .
4. Velja hnappinn **Í lagi**.

### Birgðatínsla eða hreyfingar stofnaðar í tveimur þrepum

Ef tína á eða flytja íhluti fyrir upprunaskjöl í tveimur skrefum þarf að gefa út upprunaskjalið til að gera það tilbúið fyrir tínslu. Upprunaskjöl eru gefin út fyrir innri aðgerðir á eftirfarandi hátt.  

|Upprunaskjal|Losunaraðferð|  
|---------------------|--------------------|  
|Framleiðslupöntun|Á síðunni **Áætluð framleiðslupöntun** er stöðu pöntunar **breytt í Útgefin** eða síðan Útgefin framleiðslupöntun **notuð** til að stofna útgefna framleiðslupöntun.|  
|Samsetningarpöntun|Breyta stöðu samsetningarpöntunar í **Útgefin**.|
|Verk | Breyta stöðu **verks í Opið** eða stofna verk með stöðuna Opið strax.|  

Starfsmaður sem tengist tínslu á vörum getur stofnað birgðafrágangsskjal fyrir upprunaskjalið.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, færa inn **Birgðatínslu** eða **Birgðahreyfingu** og velja síðan viðeigandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3. Í reitnum **Upprunaskjal** er valin tegund upprunaskjalsins sem frágangurinn er fyrir.

    > [!NOTE]
    > Ekki er hægt að nota **birgðatínsluskjöl** fyrir tínslu á samsetningaríhlutum.
4. Í reitnum **Forðanr.** er forðaskjal valið.  
5. Einnig er hægt að velja aðgerðina **Sækja upprunaskjal** til að velja skjalið af lista yfir upprunaskjöl á innleið sem eru tilbúin til tínslu í birgðageymslunni.  
6. Hnappurinn **Í lagi** er valinn til að fylla út tínslu- eða hreyfingalínurnar samkvæmt því upprunaskjali sem valið var.  

## Birgðatínsla skráð

1. Á síðunni Birgðatínsla **er** skjalið opnað til að skrá tínslu fyrir.  
2. Í reitnum **Hólfkóti** á tínslulínunum er hólfið þar sem tína þarf vörurnar úr hólfinu þar sem varan er tiltæk. Hægt er að skipta um hólf ef með þarf.
3. Tínslan er framkvæmd og tínslumagnið síðan fært inn í reitinn **Magn til afgreiðslu** .

    Ef tína þarf vörur fyrir línu úr fleiri en einu hólfi, til dæmis vegna þess að hólf hefur ekki fullt magn, er aðgerðin **Skipta línu** notuð á flýtiflipanum **Línur** . Aðgerðin stofnar línu fyrir eftirstandandi magn sem á að meðhöndla.  
4. Valið er **Bóka** aðgerðin.  

Eftirfarandi gerist í bókunarferlinu:

* Bóka notkun upprunaskjalslínanna sem voru tíndar.
* Ef hólf eru notuð í birgðageymslunni stofnar bókun vöruhúsafærslur til að bóka breytingar á hólfamagninu.

[!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## Til að skrá birgðahreyfingu

1. Á síðunni **Birgðahreyfing er** skjalið opnað til að skrá hreyfingu fyrir.  
2. Í reitnum **Hólfkóti** á hreyfingalínunum er lagt til að hólfið sem tínt er úr sé byggt á sjálfgefnu hólfi vörunnar og því hvað er til ráðstöfunar. Hægt er að skipta um hólf ef með þarf.  
3. Færið er framkvæmt og fært inn fært magnið í reitinn **Magn til afgreiðslu** . Gildið á línum Taka og Setja verður að vera það sama. Annars er ekki hægt að skrá hreyfinguna.

    Ef taka þarf vörurnar í línu úr fleiri en einu hólfi, til dæmis vegna þess að hólf hefur ekki fullt magn, skal nota aðgerðina **Skipta línu** á flýtiflipanum **Línur** . Aðgerðin stofnar línu fyrir eftirstandandi magn sem á að meðhöndla.  
4. Velja skal Reitinn **Dagbók birgða Hreyfingaaðgerð** .  

Eftirfarandi gerist í bókunarferlinu:

* Vöruhúsafærslur gefa nú til kynna að íhlutirnir séu í hólfunum sem tilgreind eru á upprunaskjalspöntunarlínunum. Til dæmis samsetningarpöntun, framleiðsluíhlut eða áætlunarlínu verkefnis.

>[!NOTE]
> Ólíkt því þegar íhlutir eru færðir með birgðatínslum er notkun ekki bókuð þegar birgðahreyfing er skráð. Notkun er skráð sem sérstakt skref með því að bóka upprunaskjalið.

## Birgðaskráning framleiðsluíhluta í einfaldri vöruhúsaskilgreiningu

Birgðaskráningaraðferðir hafa áhrif á flæði íhluta í framleiðslu. Fræðast meira um birgðaskráningu [íhluta eftir frálagi aðgerða](production-how-to-flush-components-according-to-operation-output.md). Eftir því hvaða birgðaskráningaraðferð er valin er hægt að tína íhluti fyrir framleiðslu om eftirfarandi leiðir:

* Birgðatínsluskjal **er** notað til að skrá tínslu fyrir vörur sem nota **handvirka** birgðaskráningaraðferð. Þegar þú skráir birgðatínslu er notkun tíndra íhluta bókuð. 
* Nota skjalið **Birgðahreyfing** með vísun í upprunaskjal til að skrá tínslur fyrir íhluti sem nota **handvirka** birgðaskráningaraðferð. Notandi þarf að skrá notkun sérstaklega. Nánari upplýsingar um [Fjöldabóka framleiðslunotkun](production-how-to-post-consumption.md). 
*  **Nota skjalið Birgðahreyfing** með vísun í upprunaskjal til að skrá tínslu fyrir íhluti sem nota **tínslu + Framvirkt,Tína** **+ Afturvirk** söfnunaraðferð. Notkun íhluta gerist annaðhvort sjálfkrafa þegar stöðu framleiðslupöntunarinnar er breytt eða með því að hefja eða ljúka aðgerð. Allir íhlutir sem þarf verða að vera tiltækir. Annars skal bóka birgðaskráningarnotkunarstöðvun fyrir þann íhlut.
*  **Nota birgðahreyfingarskjal** án tilvísunar í upprunaskjal eða aðrar leiðir til að skrá hreyfingu íhluta sem nota birgðaskráningaraðferðina **Framvirk** eða **Afturvirk** . Notkun íhluta gerist annaðhvort sjálfkrafa þegar stöðu framleiðslupöntunar er breytt eða hún ræst eða hún lýkur. Allir íhlutir sem þarf verða að vera tiltækir. Annars stöðvast birgðaskráning notkun fyrir þann íhlut. Fá nánari upplýsingar um [hvernig á að færa vörur innri vinnslu í einfaldri vöruhúsagrunnstillingu](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### Dæmi

Framleiðslupöntun er fyrir 15 stk af vöru sp-SCM1004. Sumar af vörunum á íhlutalistanum þarf að birgðaskrá handvirkt í notkunarbók og hægt er að tína aðrar vörur og birgðaskrá sjálfkrafa með því að nota **Tínslu + Afturvirk** birgðaskráningaraðferð.  

Eftirfarandi skref gefa dæmi um aðgerðirnar sem mismunandi einstaklingar framkvæma og tengd svör:  

1. Yfirmaður vinnusalar losar framleiðslupöntunina. Vörur með **birgðaskráningaraðferð framvirkt** og enginn leiðartengill eru dregnar frá opnu vinnusalarhólfi.  
2. Eftirlitsaðili vinnusalar velur aðgerðina **Stofna birgðafrágang/tínslu á framleiðslupöntuninni og kveikir á aðgerðinni** Stofna birgðatínslu **. Tína og** stofna birgðatínslu **Hreyfingavígsla** . Birgðatínsluskjal er stofnað fyrir vörur með **handvirka** birgðaskráningaraðferð og birgðahreyfing er stofnuð fyrir vörur með **Tína + Afturvirk** og **Tínsla + Framvirk** birgðaskráningaraðferðir.
3. Yfirmaður vöruhússins úthlutar tínslum og hreyfingum á vöruhúsastarfsmann.
4. Starfsmaður í vöruhúsinu tínir vörurnar úr viðeigandi hólfum og setur þær í hólf framleiðslu eða í hólfið sem tilgreint er í birgðahreyfingunni. Hólfið getur verið vinnu- eða vélastöðvarhólf.  
5. Starfsmaður vöruhússins bókar tínsluna. Magnið er dregið frá hólfunum.
6. Starfsmaður vöruhússins bókar hreyfinguna. Magnið er dregið frá tínsluhólfunum og bætt í notkunarhólfið. Reiturinn **Tínt magn** á íhlutalistanum fyrri allar tíndar vörur er uppfærður.  
7. Starfsmaður á vél upplýsir framleiðslustjóra um það þegar endanlegar vörur eru fullunnar.  
8. Yfirmaður vinnusalar notar frálagsbókina eða framleiðslubókina til að bóka frálagið. Magn íhlutavara sem nota **Tínslu + Framvirkt** eða **Tína + Afturvirk** birgðaskráningaraðferðir með leiðartenglum er dregið frá hólfinu Í framleiðslu.
9. Framleiðslustjórinn breytir stöðu framleiðslupöntunarinnar **í Lokið**. Magn íhlutavara sem nota **afturvirka** birgðaskráningaraðferð er dregið frá opnu vinnusalarhólfi og magn íhluta sem nota **Tína + Afturvirk** birgðaskráningaraðferð og enginn leiðartengill er dreginn frá hólfi framleiðslu í framleiðslu.  

 Eftirfarandi mynd sýnir þegar reiturinn **Hólfkóti** á efnisþáttalista er fylltur út út frá staðsetningu notanda eða uppsetningu vinnuvélar-/vinnustöðvarmiðstöðvar.  

:::image type="content" source="media/binflow.png" alt-text="Yfirlit yfir hvenær og hvernig reiturinn Hólfkóti er fylltur út.":::

## Sjá einnig .

[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Yfirlitsvinna vöruhúsastjórnunar](design-details-warehouse-management.md)
[með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
