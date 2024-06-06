---
title: Komast yfir eignir
description: 'Hægt er að setja upp eign, úthluta afskriftabók, og skrá kaupverð eignarinnar.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: purchase fixed asset
ms.search.form: '5605, 5551, 5600, 5628, 5629, 5633'
ms.date: 05/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Komast yfir eignir

Nota síðuna **Eignaspjald** til að færa inn upplýsingar um eign. Hægt er að setja byggingar eða framleiðslubúnað sem aðaleign með íhlutalista upp og hægt er að flokka þær á ýmsa vegu, eins og eftir flokki, deild eða staðsetningu. Setja verður upp og úthluta hverri eign afskriftabók áður en hægt er að eignast hana.

Þegar eign hefur verið sett upp og afskriftabók er úthlutað verður að eignast eignina. Til að komast yfir eign, skráirðu kaupferð hennar í viðeigandi Fjárhagsreikning, bankareikning, eða lánardrottin með því að bóka kaupfærslu af síðunni **Fjárhagsbók eigna** . Þú getur notað síðuna **Aðstoð við eignakaup** til að stofna og bóka nauðsynlegar færslubókarlínur sjálfvirkt.

Nota endurmat til að leiðrétta gildi fyrir almennar verðbreytingar. Keyrslan **Endurmat eigna er** notuð til að reikna stofnkostnað og endurnýjunarkostnað.

## Bæta eign við eignalistann

Áður en hægt er að eignast eign verður að bæta henni við eignalistann. Nokkrar leiðir eru til að bæta eignum við listann:

* Færa inn upplýsingar um eignirnar á síðunni **Eignaspjald** .
* Nota skal aðgerðina **Breyta í Excel** til að sækja lista yfir eignir á vinnublað, bæta nýjum eignum við listann og birta svo uppfærsluna [!INCLUDE [prod_short](includes/prod_short.md)].
* Nota innkaupapöntun til að bæta við eignum.
* Nota aðgerðina **Afrita eign** .

Þegar eignum hefur verið bætt við listann er næsta skref að eignast þær þannig að hægt sé að nota þær í viðskiptum. Fræðast meira um [eign](#acquire-fixed-assets).

### Bæta við eign á síðunni Eignaspjald

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignir** og velja síðan viðkomandi tengil.  
2. Velja sem **Nýtt** aðgerð og síðan fyllt út í reitina á **Almenna** Flýtiflipanum eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Fyllt er út í reiti eftir því sem við á í flýtiflipanum **afskriftabók**. Þetta skref úthlutar afskriftabók á eigninni.  
4. Ef það þarf að úthluta fleiri en einni afskriftabók á eign skal velja **bæta Við Fleiri Afskriftabækur** aðgerð. Nánari upplýsingar eru notaðar með því að [fara í Úthlutun afskriftabókar á eign](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

    Þegar fyllt hefur verið í þá reiti **sem þarf er hægt að eignast eignina.** Tilkynningin birtist efst á síðunni. Ef notandi er tilbúinn að eignast eignina núna skal velja Aðgerðin **Kaup** . Fylgdu skrefunum á síðunni **Aðstoð við eignakaup** til að ljúka kaupunum. Ef notandi er ekki tilbúinn er alltaf hægt að eignast eignina síðar.

### Nota Breyta í Excel til að bæta við eignum

Ef bæta á við fjölda eigna er Ritfærsla í Excel frábært verkfæri til að nota. Verkfærið sækir núverandi eignalista á vinnublaði sem inniheldur flesta reiti sem tiltækir eru á eignaspjaldssíðunni. Hægt er að fylla út suma eða alla reiti í línu fyrir hverja eign og birta breytingarnar þannig að þeim verði bætt við [!INCLUDE [prod_short](includes/prod_short.md)] listann. Ef ekki er hægt að fylla út allan nauðsynlegan reit er það í lagi. Hægt er að uppfæra þær þegar [!INCLUDE [prod_short](includes/prod_short.md)] þær eru tilbúnar.

> [!NOTE]
> Ef nota á aðgerðina Breyta í Excel verður Office-innbót að vera Microsoft Dynamics uppsett. Innbótin býr til tengingu milli Excel og [!INCLUDE [prod_short](includes/prod_short.md)]. Til að fá nánari upplýsingar er farið í [Sækja Business Central Innbót fyrir Excel](admin-deploy-excel-addin.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignir** og velja síðan viðkomandi tengil.
2. Veldu Deildu :::image type="content" source="media/share-icon.png" alt-text="þessari síðu með öðrum notendum eða forritum."::: Og velja **svo Breyta í Excel**.
3. Skráin sem hefur verið sótt er opnuð og upplýsingar um nýju eignirnar færðar inn.

   > [!TIP]
   > Ekki þarf að færa inn kenni í reitinn **Nr.** Dálk. Þegar uppfærslan [!INCLUDE [prod_short](includes/prod_short.md)]  er birt er kenni úthlutað sem byggir á númeraröðinni sem notuð er fyrir eignir.

4. Til að uppfæra [!INCLUDE [prod_short](includes/prod_short.md)] skal velja **Microsoft Dynamics** Útgáfa **á svæðinu**.

### Bæta við eign úr innkaupapöntun eða reikningi

Eftirfarandi skref útskýra hvernig á að bæta eign við innkaupapöntun. Skrefin eru svipuð fyrir innkaupareikning.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupapantanir** og velja síðan viðkomandi tengil.
2. Velja skal **Ný** til að stofna nýja innkaupapöntun.
3. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]
4. Á flýtiflipanum **Línur** í reitnum **Tegund** skal velja **Eign**.
5. Í reitnum **númer** Annaðhvort skal velja fyrirliggjandi eign til að bæta við kostnaði eða velja **Nýtt** til að bæta nýrri eign við.
6. Þegar upplýsingar um nýju eignina og innkaupapöntunina hafa verið færðar inn skal velja **Bóka**.

## Eignast með því að nota eignafjárhagsbók

Eftirfarandi ferli lýsir því hvernig á að eignast með því að stofna og bóka nauðsynlegar eignafjárhagsbókarlínur. Hægt er að einnig að stofna og bóka færslubókarlínurnar handvirkt. Nánari upplýsingar eru notaðar í Eignafjárhagsbók með því að [nota eignafjárhagsbók](#acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignir** og velja síðan viðkomandi tengil.
1. Velja skal eignina sem á að eigna og velja svo aðgerðina **Kaup** .
1. Fylgdu skrefunum á síðunni **Aðstoð við eignakaup** til að ljúka kaupunum.

> [!NOTE]  
> Einnig má bóka kaupverð sem lánsfé. Í því tilfelli skal muna að gildið í reitnum **kaupverð með VSK** á að vera með mínusmerki til að tilgreina lánið.

Þegar lokið er **valið** **er fyllt út í reitinn Bókfært virði** á **eignaspjaldinu**, sem gefur til kynna að eignin hafi verið keypt á tilgreindum stofnkostnaði.  

## Eignakaup bókuð handvirkt með eignafjárhagsbók

Eftirfarandi ferli sýnir hvernig á að komast yfir eign handvirkt með því að stofna og bóka línur á síðunni **Fjárhagsbók eigna**. Einnig er hægt að eignast eign sjálfkrafa á síðunni **Eignaspjald** með því að velja aðgerðina **Kaup eigna** . Nánari upplýsingar er farið í [Eignaeign](#acquire-fixed-assets).

> [!NOTE]  
> Einnig má bóka kaupverð sem lánsfé. Í því tilfelli muna sem gildið í reitnum **upphæð** að vera með mínusmerki til að tilgreina kredit.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagsbækur eignar** og velja síðan viðkomandi tengil.
2. Á síðunni **Fjárhagsbók eigna** í reitnum **Eignabókunartegund** er valið **Kaupverð**.
3. Fyllið inn í eftirstandandi reiti eftir þörfum.
4. Valið er **Bóka** aðgerðin.  

> [!TIP]  
> Ef fært er í reitinn Vátryggingarnúmer er fært inn í reitinn **Vátryggingarnúmer.**  [!INCLUDE[prod_short](includes/prod_short.md)] einnig bókar stofnkostnað eignarinnar í vátryggingasviðsbókina. Nánari upplýsingar eru notaðar með því að [fara í Tryggingareignir](fa-how-insure.md).

## Uppsetning íhlutalista fyrir aðaleignir:

Hægt er að flokka eignir í aðaleignir og íhluti þeirra. Til dæmis gæti verið til framleiðsluvél sem samanstendur af nokkrum hlutum sem á að flokka með þessum hætti.  

Setja verður upp aðaleign og alla íhluti hennar sem einstakar eignir. Þegar íhlutalisti [!INCLUDE[prod_short](includes/prod_short.md)]  hefur verið settur upp fyllir sjálfkrafa í reitina **Aðaleign/Íhlutur og** Íhlutir **aðaleignar** á eignunum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignir** og velja síðan viðkomandi tengil.
2. Valin er eignin sem er aðaleignin er valin síðan **íhlutir aðaleignar** aðgerð.
3. Á síðunni **Íhlutir aðaleignar** skal velja reitinn **Eignanr.** og síðan valið eignin sem á að bæta við sem íhlut aðaleignar.
4. Lokaðu síðunni.
5. Endurtaktu þrep 3 og 4 fyrir hverja íhlut eignar sem ætlunin er að bæta við.
6. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning eignar** og velja síðan viðkomandi tengil.
7. Kveikja á því **að Leyfa bókun á aðaleignir** .

## Ógilding bókunar kaupverðs fyrir eina eign

Ef villa á sér stað við bókun stofnkostnaðar er hægt að fjarlægja færsluna með keyrslunni **Afturkalla eignafærslur** og bóka síðan rétta stofnkostnaðarfærslu. Röngu færslurnar eru fluttar á síðuna **Rangar eignafærslur.**

Ef kaup eru til dæmis bókuð með rangri dagsetningu þarf að leiðrétta hana eins fljótt og unnt er þar sem bókunardagsetning eigna er notuð fyrir marga mikilvæga útreikninga.

> [!IMPORTANT]  
> Ekki er hægt að nota aðgerðina **Bakfæra færslur** fyrir eignafærslur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Eignafærslur** og veldu síðan viðeigandi tengil.  
2. Á síðunni **Eignafærslur** skal velja færslu eða færslur sem á að hætta við.  
3. Veldu valmyndina **Aðgerðir** og veldu síðan aðgerðina **Hætta við færslur**.
4. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Veldu hnappinn **Í lagi** til að ræsa keyrsluna.
6. Þegar röng færsla eða færslur eru ógiltir, skal halda áfram og bóka rétt kaupverð.

## Bóka hrakvirði með kaupverði.

Hrakvirði er afgangsvirði eignar þegar ekki er lengur hægt að nota hana. Hægt er að bóka hrakvirðið um leið og stofnkostnaður er bókaður. Nánari upplýsingar eru notaðar með því að fara í [Afskrift eða Afskrifa eignir](fa-how-depreciate-amortize.md).

Hægt er að bóka hrakvirði með stofnkostnaði af færslubók eigna.

> [!NOTE]
> Þetta ferli gæti krafist þess að þú færslubókasíðu eigna með því að bæta við reitnum Hrakvirði. Reiturinn er ekki sjálfgefið sýndur á síðunni. Nánari upplýsingar eru notaðar til að [sérstilla vinnusvæðið](ui-personalization-user.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Færslubækur eigna** og velja síðan viðkomandi tengil.
2. Á síðunni **Eignabækur** skaltu búa til kauplínuna. Nánari upplýsingar eru notaðar til að [bóka eignakaup handvirkt með eignafjárhagsbók](#to-post-a-fixed-asset-acquisition-manually-with-a-fixed-asset-gl-journal).
3. Í reitinn **Hrakvirði** í færslubókarlínunni skal færa inn upphæð hrakvirðis sem kreditfærslu (settu mínusmerki að framan, t.d. **-** 100).
4. Valið er **Bóka** aðgerðin.

> [!NOTE]
> Ef hrakvirði er til fyrir eign er það virði notað við afskriftabókun í stað gildsins í reitnum **Bókfært lokavirði** á síðunni **Eignaafskriftabækur** . Nánari upplýsingar eru notaðar með því að [fara í Bókfært lokavirði](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## Sjá einnig .

[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Hönnunarupplýsingar um ófrádráttarbær VSK-áhrif á eignir](design-details-nondeductible-vat.md)  
[Fjármál](finance.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
