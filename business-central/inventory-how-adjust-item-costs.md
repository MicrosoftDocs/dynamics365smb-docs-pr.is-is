---
title: Leiðrétta birgðakostnað handvirkt
description: Hægt er að leiðrétta birgðavirði vöru með FIFO- eða Meðalkostnaðaraðferðum þegar kostnaður afurða breytist.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'cost adjustment, cost forwarding, costing method, inventory valuation, costing'
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Leiðrétta vörukostnað

Kostnaður vöru (birgðavirði) sem keypt er inn og síðar gæti breyst á meðan á líftíma hennar stendur, til dæmis vegna þess að flutningskostnaði er bætt við innkaupakostnað hennar eftir að varan hefur verið seld. Kostnaðaraðlögun er sérstaklega viðeigandi í aðstæðum þar sem þú selur vörur áður en þú reiknar kaupin á þeim vörum. Til að vita alltaf rétt birgðavirði þarf að leiðrétta reglulega birgðakostnað. Réttur kostnaður tryggir að sölu- og framlegðartölur séu uppfærðar og að fjárhagsleg afkastavísar séu réttir. Nánari upplýsingar, sjá [Upplýsingar um hönnun: Kostnaðarleiðrétting](design-details-cost-adjustment.md)

Gildið í reitnum **Kostnaðarverð** á birgðaspjaldinu er byggt á stöðluðu kostnaðarverði vara með aðferðina Staðlað kostnaðarútreikningur. Fyrir vörur með aðra aðferð við kostnaðarútreikning er gildið byggt á útreikningi á tiltækum birgðum (reikningsfærður kostnaður og væntanlegur kostnaður) deilt með tiltæku magni. Frekari upplýsingar er að finna í [Skilja kostnaðarútreikning einingar](inventory-how-adjust-item-costs.md#understanding-unit-cost-calculation).

Í [!INCLUDE[prod_short](includes/prod_short.md)] eru kostnaðarkostnaður sjálfkrafa leiðrétt í hvert skipti sem viðskiptin eiga sér stað, svo sem þegar þú sendir inn innkaupareikning fyrir hlut.

Einnig er hægt að leiðrétta kostnað einnar eða fleiri vara handvirkt. Handvirkar leiðréttingar eru til dæmis gagnlegar þegar vitað er að vörukostnaði er breytt af öðrum ástæðum en birgðafærslum.

Kostnaðarverð er leiðrétt með FIFO eða Meðalkostnaðaraðferð, það fer eftir vali þínu í **Uppsetning fyrirtækis** í uppsetning með aðstoð eða í reitnum **Aðferð kostnaðarútreiknings** á vöruspjaldinu. Nánari upplýsingar eru í [Skrá nýjar vörur](inventory-how-register-new-items.md).  

Kostnaðarverð vöru er raunvirði hverrar innhreyfingar vörunnar fyrir FIFO-aðferðina. Birgðir eru metnar með tilliti til þess að fyrstu vörurnar sem settar eru í birgðir eru seldar fyrst.

Ef þú notar Meðalkostnaðaraðferð, er einingaverð vara reiknað út sem meðaleiningaverð á hverjum tímapunkti eftir innkaup. Fyrir verðmat birgða, er gert ráð fyrir að allar birgðir verði seldar á sama tíma. Fyrir vörur sem nota þessa aðferð kostnaðarútreiknings geturðu valið **kostnaðarverð** reitinn á vöruspjaldinu til að skoða færslusöguna sem meðalkostnaður er reiknaður út frá

Kostnaðarleiðrétting vinnur aðeins virðisfærslur sem ekki eru leiðréttar. Þegar framsenda þarf breyttan kostnað á innleið í tengdar færslur á útleið stofnar það nýjar leiðréttingarvirðisfærslur. Leiðréttingarvirðisfærslurnar byggjast á upplýsingunum í upphaflegu virðisfærslunum en innihalda leiðréttingarupphæðina. Kostnaðarleiðréttingin notar dagsetningu bókunar upphaflegu virðisfærslunnar í leiðréttingarfærslunni nema hún sé í lokuðu birgðatímabili. Í því tilfelli notar forritið upphafsdagsetningu næsta birgðatímabils. Ef birgðatímabil eru ekki notuð tilgreinir dagsetningin í **reitnum Bókun leyfð frá** á síðunni **Fjárhagsgrunnur** hvenær leiðréttingarfærslan er bókuð.

## Til að uppfæra birgðakostnað verks handvirkt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Leiðrétta kostnað - Birgðafærslur** og velja síðan viðkomandi tengil.
2. Á síðunni **Leiðr. Kostnað - Birgðafærslur** skal tilgreina hvaða vörur á að leiðrétta kostnað fyrir.
3. Velja hnappinn **Í lagi**.

## Almennar breytingar gerðar í Innk.verð:

Ef breyta þarf innkaupaverðinu fyrir marga hluti er hægt að nota **Leiðrétta vörukostnað/verð** keyrsluna.  

Keyrslan breytir innihaldi reitsins **Einingarverð** á birgðaspjaldinu. Keyrslan breytir efni reitsins á sama hátt fyrir allar vörur eða valdar vörur. Keyrslan margfaldar gildið í reitnum með leiðréttingarstuðli sem notandi tilgreinir.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Leiðrétta vörukostnað/verð** og veldu síðan tengda tengilinn.  
2. Í reitnum **Leiðr. reit**, skal tilgreina hvaða vöru eða birgðahaldseiningarspjald reit á að leiðrétta.  
3. Í reitnum **Leiðréttingarstuðull** er tilgreindur stuðullinn sem á að leiðrétta gildið um. Til dæmis færa inn **1,5** til að hækka gildið um 50%.  
4. Á flýtiflipanum **Vara** skal setja upp afmarkanir til að tilgreina, til dæmis, hvaða vörur á að vinna með runuvinnslunni.  
5. Velja hnappinn **Í lagi**.  

## Skilningur á útreikningi kostnaðarverðs

Gildið í reitnum **Kostnaðarverð** á birgðaspjaldinu er byggt á stöðluðu kostnaðarverði vara með aðferðina Staðlað kostnaðarútreikningur. Fyrir vörur með aðrar kostnaðarútreikningsaðferðir er gildið byggt á útreikningi á tiltækum birgðum (reikningsfærður kostnaður og væntanlegur kostnaður) deilt með tiltæku magni.  

Í eftirfarandi köflum er lýst nánar hvernig reiturinn **Aðferð kostn.útreiknings** hefur áhrif á útreikning innkaupaverðs fyrir innkaup og sölu:  

## Útreikningur kostnaðarverðs fyrir innkaup  

Þegar vörur eru keyptar afritar **gildið í reitnum** Síðasta innk.verð **á birgðaspjaldinu í reitinn Innk.verð** í innkaupalínu eða **í línuna Ein.upphæð** í birgðabókarlínu.  

Það sem valið er í reitnum **Aðferð kostnaðarútreiknings** hefur áhrif á hvernig [!INCLUDE[prod_short](includes/prod_short.md)] reiknar innihald reitarins **Einingarkostnaður** á línunum.  

### FIFO, LIFO, Innslegið eða Meðalkostnaðarútreikningsaðferðir  

[!INCLUDE[prod_short](includes/prod_short.md)] notar eftirfarandi reiknireglu til að reikna út efni reitsins **Kostn.verð (SGM)** í innkaupalínunni eða það sem er í reitnum **Kostnaðarverð** í birgðabókarlínunni:  

“Kostn.verð (SGM) = (Beinn kostnaður – (Afsláttarupphæð / Magn)) x (1 + “Óbein kostnaðar % / 100) + Hlutf. sameiginl. Kostn  

### Stöðluð aðferð við kostnaðarútreikning  

Reiturinn **Kostn.verð (ISK)** á innkaupalínunni eða reiturinn **Kostnaðarverð** hefur verið fylltur út í birgðabókarlínunni með gildinu í reitnum **Kostnaðarverð** á birgðaspjaldinu. Ef stöðluð aðferð við útreikning kostnaðar er notuð er gildið alltaf byggt á stöðluðu kostnaðarverði.  

Þegar innkaup eru bókuð afritar kostnaðarverðið úr innkaupalínunni eða birgðabókarlínunni í innkaupareikningsfærsluna. Hann kemur fram á færslulista vörunnar.  

### Allar aðferðir kostn.útreiknings  

Kostnaðarverðið úr upprunaskjalslínunni er notað til að reikna gildið í reitnum **Kostnaðarupphæð (raunverul.)** eða, ef við á, reitinn **Kostnaðarupphæð (væntanl.)** sem tengist þessari birgðafærslu. Kostnaðurinn er innifalinn í útreikningnum óháð kostnaðaraðferð vörunnar.  

## Útreikningur kostnaðarverðs fyrir sölu  

Þegar vörur eru selt afritar kostnaðarverðið úr reitnum **Kostnaðarverð** á birgðaspjaldinu yfir í sölulínuna eða birgðabókarlínuna.  

Við bókun afritar kostnaðarverðið yfir í birgðafærslu sölureiknings og kemur fram á færslulista vörunnar. [!INCLUDE[prod_short](includes/prod_short.md)] notar kostnaðarverðið úr upprunaskjalslínunni til að reikna út efni reitsins **Kostnaðarupphæð (raunverul.)** eða, ef við á, **reitinn Kostnaðarupphæð (væntanl.)** í virðisfærslunni sem tengist þessari birgðafærslu.  

## Rekja kostnaðarleiðréttingar vöru

Vörukostnaður getur breyst af mörgum ástæðum og því er mikilvægt að hægt sé að fylgjast með kostnaðarleiðréttingum.  **Síðan Leiðrétting birgðakostnaðar** er notuð til að stjórna og fylgjast með kostnaðarleiðréttingarferlinu. Þessi síða birtir vörur ásamt færibreytum kostnaðarútreiknings og stöðu kostnaðarleiðréttingar. Hægt er að afmarka listann til að einbeita sér að vörum sem þarfnast leiðréttingar eða sem eru undanskildar í kostnaðarleiðréttingarferlinu. Til að fræðast meira um rakningu kostnaðarleiðréttinga er farið í [Rekja kostnaðarleiðréttingar](finance-track-inventory-costs.md) á vöru.

## Sjá einnig .

[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Birgðir](inventory-manage-inventory.md)  
[Sala](sales-manage-sales.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]