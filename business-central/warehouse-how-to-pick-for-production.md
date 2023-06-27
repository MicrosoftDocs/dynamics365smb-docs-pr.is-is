---
title: 'Taka til eða færa vörur fyrir framleiðslu, samsetningu eða vinnslur í Grunnvöruvöruhúsi'
description: Þegar vöruhúsið þitt krefst þess að þú vinnir úr tínslum en ekki sendum skaltu nota birgðatínslusíðuna til að skrá að íhlutir hafi verið tíndir.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.forms: '9330, 931, 990008, 89, 900, 902'
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations" />Tínsla fyrir framleiðslu, samsetningu eða verk í einfaldri vöruhúsagrunnstillingu

Val á íhlutum fyrir framleiðslu, vinnslur eða samsetningarpantanir fer eftir því hvernig vöruhúsið er sett upp sem Birgðageymsla. Frekari upplýsingar um  [uppsetningu vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Í grunnvöruhúsaleiðnum fyrir útflæði (taka til), á  **birgðageymsluspjaldinu**  fyrir birgðageymsluna, er kveikt á  **tínslunni**  en  **slökkt á krefjast afhendingar** .

Nota eftirfarandi skjöl fyrir innri aðgerðir:

* Birgðatínsla
* Birgðahreyfing

## <a name="inventory-picks" />Birgðatínslur

* Þegar Birgðatínsla er skráð fyrir innri aðgerð, til dæmis framleiðsla eða vinnsla, bókast notkun Tíndu íhlutanna samtímis.
*  **Hólfskylda**  skipta á  **síðunni Birgðageymsluspjald**  er valfrjáls.
* Þegar Birgðatínsla er  **notuð skilgreinir reiturinn Hólfakóti**  í framleiðslupöntunaríhlutalínu eða verkáætlunarlínur reitinn  *taka*  hólf. Íhlutir eru lækkaðir í taka hólfið þegar notkun er bókuð.

## <a name="inventory-movements" />Birgðahreyfingar

* Birgðahreyfingar krefjast þess að kveikt sé á  **hólfi skylda**  að skipta á  **birgðageymsluspjaldinu**  fyrir birgðageymsluna.
* Birgðahreyfingar vinna aðeins með íhlutalínur framleiðslupöntunar og pöntunarlínur samsetningar.
* Þegar birgðahreyfing er skráð fyrir innri aðgerð er aðeins skráð Efnisleg hreyfing íhlutanna í hólfi í aðgerðarsvæðinu. Þú bókar ekki neyslu.
* Þegar notaðar eru birgðafærslur er  **reiturinn Hólfakóti**  í framleiðslupöntunaríhlutalínum skilgreinir  *staðinn*  hólfið í aðgerðarsvæðinu. Staðurinn Hóll er þar sem starfsmenn vöruhúss verða að setja íhluti.
* Skrá notkun á tíndum íhlutum sérstaklega með því að bóka notkunarbók eða samsetningarpöntun.

>[!NOTE]
> Jafnvel þótt slökkt sé á tínslu til að taka til  **skipta er hægt að**  nota skjal vöruhúsatínslu  **.**  Tínsluskjöl vöruhúss eru svipuð  **og birgðatínsluskjöl** . Þetta er gagnlegt ef nota á tínslur í aðgerðum og sendingar í vöruhúsi á útleið.

### <a name="production" />Framleiðsla

Nota  **birgðatínsluskjöl**  fyrir tiltektarframleiðsluíhluti í flæði til framleiðslu.

Fyrir birgðageymslu sem notar hólf er hægt að lengja flæðið í framleiðslu með því að nota  **Birgðahreyfsluskjöl** . Birgðahreyfingar henta sérstaklega vel fyrir hlutaflúrin. Til að fræðast nánar um hvernig þáttanotkun er frátengd frá til-framleiðslu eða opnum Vinnusalarhólfum er farið  [í Birgðaframleiðsluíhluti í Grunnvöruvöruhúsi samskipa](#flushing-production-components-in-a-basic-warehouse-configuration).

### <a name="assembly" />Samsetning

Nota  **birgðahreyfingagátt**  til að færa samsetningaríhluti við samsetningarsvæðið.

> [!NOTE]
> **Skjöl birgðahreyfinga**  krefjast hólfanna.

[!INCLUDE [prod_short](includes/prod_short.md)] styður saman á lager og setja saman gerðir af samsetningarflæðigerðum. Til að fræðast meira um setja saman-pöntun í vöruhús á útleið er farið í  [meðferð með því að setja saman vörur í birgðum með birgðatínslum](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="project-management" />Verkefnastjórnun

Nota  **birgðatínsluskjöl**  til að velja vinnsluíhluti í flæði til verkefnastjórnunar.

Hægt er að lengja flæðið í vinnslum með  **Birgðahreyfunarskjölum**  til staðsetningar sem nota hólf.

> [!NOTE]
> Getan til að tína íhluti fyrir veráætlunarlínur var bætt við [!INCLUDE[d365fin](includes/d365fin_md.md)] í 2022 útgáfutímabili 2. Til að byrja að nota möguleikann verður stjórnandi að kveikja á **Eiginleikastjórnun: Virkja birgða- og vöruhúsatínslu úr verkum** á síðunni **Eiginleikastjórnun**.
>
> [!INCLUDE[prod_short](includes/prod_short.md)] notar gildið í reitnum **Eftirstöðvar** á verkáætlunarlínunni þegar það býr til birgðatínslur. Til að nota birgðatínslur fyrir verk þarftu að kveikja á **Nota notkunartengil** á síðunni **Verkspjald** fyrir verkið. Þetta gerir þér kleift að fylgjast með notkun miðað við áætlun þína. Ef þú kveikir ekki á víxlhnappnum verða eftirstöðvarnar í **0** og birgðatínslan verður ekki búin til.  [Frekari upplýsingar eru settar inn til að setja upp verknotkunarmælingar](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking).

## <a name="pick-or-move-for-production-assembly-and-jobs-in-a-basic-warehouse-configuration" />Taka til eða færa fyrir framleiðslu, samsetningu og vinnslur í grunnvöruhúsi samskipa

Hægt er að stofna birgðatínslu eða birgðahreyfingu á þrjá vegu:  

* Úr upprunaskjalinu sjálfu.  
* Fyrir nokkur upprunaskjöl á sama tíma með því að nota runuvinnslu.  
* Í tveimur skrefum. Sleppið upprunaskjalinu til að gera upprunaskjalið tilbúið til tínslu. Stofna birgðatínslu eða hreyfingu úr  **birgðatínsluskjölum**  eða  **hreyfingum**  birgða. Birgðatínslan eða-hreyfingin er byggð á upprunaskjalinu.  

### <a name="to-create-an-inventory-pick-from-the-source-document" />Birgðatínsla stofnuð í upprunaskjali:

1. Í upprunaskjalinu, sem getur verið framleiðslupöntun eða vinnsla, skal velja  **aðgerðina stofna birgðafrágang/tínslu** .  
2.  **Veljið stofna Ívt. Velja**  gátreitinn.
3. Velja hnappinn **Í lagi**.

### <a name="to-create-an-inventory-movement-from-the-source-document" />Tilfærsla birgða stofnuð úr upprunaskjalinu

1. Í upprunaskjalinu, sem getur verið framleiðslupöntun, samsetningarpöntun eða vinnsla, skal velja  **aðgerðina stofna birgðafrágang/tínslu** .  
2.  **Veljið stofna Ívt. Hreyfill**  gátkassa.
3. Velja hnappinn **Í lagi**.

### <a name="to-create-multiple-inventory-picks-or-movements-with-a-batch-job" />Til að stofna margar Birgðatínslur eða hreyfingar með runuvinnslu

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **stofna birgðafrágang/tínslu/hreyfingar** og velja síðan tengda tengilinn.  
2.  **Á flipanum vöruhúsabeiðni**, Notið  **upprunaskjalið**  og  **upprunnr.**  svæði til að afmarka eftir tegundum skjala eða afmörkunar á númerum fylgiskjala. Til dæmis er aðeins hægt að stofna tínslur fyrir framleiðslupantanir.
3.  **Á flýtiflipanum Valkostir**  er kveikt á reitnum  **Stofna ívt. Tínsla**  eða  **Stofna ívt. Víxlar hreyfinga** .
4. Velja hnappinn **Í lagi**.

### <a name="to-create-inventory-picks-or-movements-in-two-steps" />Birgðatínsla eða hreyfingar stofnaðar í tveimur skrefum

Til að taka til eða færa íhluti fyrir upprunaskjöl í tveimur skrefum verður að gefa út upprunaskjal til að gera það tilbúið til tínslu. Upprunaskjöl eru gefin út fyrir innri aðgerðir á eftirfarandi hátt.  

|Upprunaskjal|Losunaraðferð|  
|---------------------|--------------------|  
|Framleiðslupöntun| **Á síðunni áætluð framleiðslupöntun**  skal breyta stöðu pöntunar í  **Útgefin** eða nota  **útgefna framleiðslupöntun**  til að stofna útgefna framleiðslupöntun.|  
|Samsetningarpöntun|Breyta stöðu samsetningarpöntunar í  **Útgefin**.|
|Verk | Breyta stöðu starfs sem opna  **á**, eða stofna verk með stöðuna opið strax.|  

Starfsmaður í vöruhúsi sem úthlutað er á tínsluvörur getur stofnað birgðafrágangsskjal fyrir upprunaskjalið.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn  **birgðatínslu**  eða  **birgðatengingu** og veljið síðan tengda tengilinn.  
2. Valið er aðgerðin **Nýtt**.  
3.  **Í reitnum upprunaskjal**  er valin gerð upprunaskjals sem gengið er frá fyrir.

    > [!NOTE]
    > Ekki er hægt að nota  **birgðatínsluskjöl**  fyrir íhluti tiltektarsamsetningar.
4. Í reitnum **Forðanr.** er forðaskjal valið.  
5. Einnig er hægt að velja  **aðgerðina Sækja upprunaskjal**  til að velja skjalið af lista yfir upprunaskjöl á innleið sem eru tilbúin til tínslu á staðnum.  
6. Velja skal  **OK**  hnappinn til að fylla tínslulínur eða hreyfingalínur samkvæmt völdu upprunaskjali.  

## <a name="to-record-the-inventory-pick" />Birgðatínsla skráð

1.  **Á síðunni Birgðatínsla**  er skjalið opnað til að skrá tínslu.  
2.  **Í reitnum Hólfkóti**  í tínslulínum er hólfið þar sem vörurnar verða teknar úr hólfinu þar sem varan er tiltæk. Hægt er að skipta um hólf ef með þarf.
3. Tínslan er framkvæmd og síðan er tínslumagnið fært inn í  **reitinn Magn til afgreiðslu** .

    Ef velja á vörur fyrir línu úr fleiri en einu hólfi, til dæmis vegna þess að hólf innihalda ekki fullt magn, skal nota  **aðgerðina skipta línu**  á  **fastflipanum línur** . Aðgerðin býr til línu fyrir eftirstandandi magn sem á að afgreiða.  
4. Valið er **Bóka** aðgerðin.  

Eftirfarandi gerist á meðan á bókunarferlinu stendur:

* Bóka notkun á upprunaskjalslínunum sem voru tilteknar.
* Ef birgðageymslan notar hólf mun bókun stofna vöruhúsafærslur til að bóka breytingar á hólfmagninu.

[!INCLUDE [preview-posting-warehouse](includes/preview-posting-warehouse.md)]

## <a name="to-record-the-inventory-movement" />Birgðahreyfingin skráð

1.  **Opnið skjalið til að skrá hreyfingu fyrir fyrir á síðunni birgðahreyfingar** .  
2.  **Í reitnum Hólfkóti**  í hreyfingalínunum er hólfið sem á að velja lagt til samkvæmt sjálfgefnu hólfi og framboði vörunnar. Hægt er að skipta um hólf ef með þarf.  
3. Flytjið og Færið inn fært magn í  **reitinn Magn til afgreiðslu** . Gildið á línum Taka og Setja verður að vera það sama. Annars er ekki hægt að skrá hreyfinguna.

    Ef taka á vörur fyrir línu úr fleiri en einu hólfi, til dæmis vegna þess að hólf innihalda ekki fullt magn, skal nota  **aðgerðina skipta línu**  á  **fastflipanum línur** . Aðgerðin býr til línu fyrir eftirstandandi magn sem á að afgreiða.  
4.  **Veldu Register Invt. Hreyfingarleysis** .  

Eftirfarandi gerist á meðan á bókunarferlinu stendur:

* Vöruhúsafærslur gefa nú til kynna að íhlutir séu í hólfunum sem tilgreindir eru í pöntunarlínum upprunaskjalsins. Til dæmis samsetningarpöntun, framleiðsluhluti eða áætlunarlínu.

>[!NOTE]
> Ólíkt þegar íhlutir eru flutt með birgðatínslum er notkun ekki bókuð þegar birgðahreyfing er skráð. Verið er að skrá notkun sem aðskilin skref með því að bóka upprunaskjalið.

## <a name="flushing-production-components-in-a-basic-warehouse-configuration" />Birgðaframleiðsluíhlutir í grunnvöruvöruhúsi samskipa

Flúorskolun hefur áhrif á flæði íhluta í framleiðslu.  [Frekari upplýsingar um Flush-íhluti eru í samræmi við afköst](production-how-to-flush-components-according-to-operation-output.md) aðgerðar. Eftir því hvaða flæðiaðferð er valin er hægt að velja íhluti fyrir framleiðslu á eftirfarandi leiðum:

*  **Nota birgðatínsluskjal**  til að skrá tínsluna fyrir vörur sem nota  **handvirku**  flæðiaðferðina. Þegar þú skráir birgðatínslu er notkun tíndra íhluta bókuð. 
* Birgðahreyfðarskjal  **·**  er notað með tilvísun í upprunaskjal til að skrá tínslur fyrir íhluti sem nota  **handvirku**  flæðiaðferðina. Þú þarft að skrá neyslu sérstaklega. Frekari upplýsingar um  [runubókun Framleiðslunotkunar](production-how-to-post-consumption.md). 
* Birgðahreyfðarskjal  **·**  er notað með tilvísun í upprunaskjal til að skrá tínslur fyrir íhluti sem nota  **tínsluna + áfram**,  **tína + afturábak**  birgðaflæðiaðferð. Notkun íhluta mun gerast sjálfkrafa annað hvort þegar stöðu framleiðslupöntunarinnar er breytt eða með því að ræsa eða ljúka aðgerð. Allir nauðsynlegir íhlutir verða að vera tiltækir. Annars er hætt að bóka notkun fyrir þann íhlut.
* Birgðahreyfðarskjal  **·**  er notað án tilvísunar í upprunaskjali eða öðrum leiðum til að skrá hreyfingar íhluta sem nota  **fram**  -eða  **afturbirgðaskráningaraðferðina** . Notkun íhluta mun gerast sjálfkrafa annað hvort þegar breytt er um stöðu framleiðslupöntunar eða hefja eða ljúka aðgerð. Allir nauðsynlegir íhlutir verða að vera tiltækir. Að öðrum kosti er hætt að bóka hreinsað notkun fyrir þann íhlut.  [Frekari upplýsingar eru í Flytjendavörum í Grunnvöruafbrigðum](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="example" />Dæmi

Þú ert með framleiðslupöntun fyrir 15 PCS af vöru SP-SCM1004. Sumar vörurnar á íhlutaliðlistanum verður að nota handvirkt í notkunarbók og aðrar vörur er hægt að taka til sjálfkrafa með notkun  **+ afturflúðaaðferð tínsla + afturábak** .  

Eftirfarandi skref gefa dæmi um þær aðgerðir sem ólíkir einstaklingar taka og tengdum viðbrögðum:  

1. Yfirmaður vinnusalar losar framleiðslupöntunina. Vörur með  **framflæðiaðferð**  og engin leiðartenging er dregin frá opna vinnslusalarhólfi.  
2. Eftirlitsaðili í Vinnusalarstjórnun velur að búa til  **frágang/tínslu**  í birgðum í framleiðslupöntuninni og slekkur á  **Create invt. Taka**  til og  **Stofna ívt. Víxlar hreyfinga** . Skjal birgðatínslu er stofnað fyrir vörur með  **handvirkri**  Birgðaskráningaraðferð og birgðahreyfing er stofnuð fyrir vörur með  **tínslu + afturábak**  og  **tínsla + áfram**  flæðiaðferðir.
3. Vöruhúsastjórinn úthlutar tínslum og hreyfingum á vöruhúsastarfsmanni.
4. Starfsmaður í vöruhúsi tínir vörurnar úr viðeigandi hólfum og setur þær í hólf framleiðslu eða í hólfi sem er tilgreint í birgðahreyfingu. Hólfið getur verið vinnustöð eða vélastöð.  
5. Starfsmaður í vöruhúsi bókar tínslu. Magnið er dregið frá hólfunum.
6. Starfsmaður í vöruhúsi bókar hreyfinguna. Magnið er dregið frá tínsluhólfum og bætt við notkunarhólfið. Reiturinn **Tínt magn** á íhlutalistanum fyrri allar tíndar vörur er uppfærður.  
7. Starfsmaður á vél upplýsir framleiðslustjóra um það þegar endanlegar vörur eru fullunnar.  
8. Umsjónarmaður vinnslusalarhæðar notar úttaksbók eða framleiðslubók til að bóka úttakið. Fjöldi íhluta sem nota  **tínsluvörur**  eða  **tínsla + afturvirkar**  birgðaaðferðir með leiðartenglum er dreginn frá framleiðslu hólfa.
9. Framleiðustjóri breytir stöðu framleiðslupöntunarinnar í  **lokið**. Magn íhluta sem nota  **afturvirka**  birgðaaðferð er dregið frá opna vinnslusalarhólfi og magn íhlutavara sem nota  **+ afturbirgðaskráningaraðferð**  og enginn Leiðartengill er dreginn frá framleiðslu hólfa.  

 Eftirfarandi mynd sýnir þegar reiturinn **Hólfkóti** á efnisþáttalista er fylltur út út frá staðsetningu notanda eða uppsetningu vinnuvélar-/vinnustöðvarmiðstöðvar.  

:::image type="content" source="media/binflow.png" alt-text="Yfirlit um hvenær og hvernig reiturinn Hólfakóti er fylltur út.":::

## <a name="see-related-microsoft-training" />Sjá tengda [Microsoft þjálfun](/training/paths/pick-ship-items-business-central/)

## <a name="see-also" />Sjá einnig .

[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Yfirlit yfir](design-details-warehouse-management.md)
[vöruhúsastjórnun vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
