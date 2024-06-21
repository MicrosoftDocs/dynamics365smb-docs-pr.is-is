---
title: Afskrifa eða afskrifa eign
description: 'Tilgreina verður hvernig niðurfærsla, afskriftir eða afskrifa hverja eign, svo sem vélar og tæki, á afskriftartíma þeirra.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: write down
ms.search.form: '5610, 5611, 5629, 5633, 5659, 5660, 5663, 5619, 5666'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# Afskrifa eða afskrifa eignir

Afskriftir eru notaðar til að dreifa kostnaði við eignir eins og tæki og búnað á afskriftartíma þeirra. Skilgreina verður fyrir hverja eign hvernig á að afskrifa hana.  

 Hægt er að bóka afskriftir með tvennum hætti:  

* Sjálfvirkt með því að keyra keyrsluna **Reikna afskriftir**.  
* Handvirkt með því að nota fjárhagsbók eigna.  

[!INCLUDE[prod_short](includes/prod_short.md)] getur reiknað daglegar afskriftir og er því unnt að reikna afskriftir fyrir hvaða tímabil sem er. Þess vegna er til dæmis hægt að greina rekstrarafkomu hverju sinni miðað við mánuð, ársfjórðung eða ár. Útreikningurinn notar 360 daga staðalár og 30 daga staðalmánuð. Frekari upplýsingar eru í [afskriftaaðferðir](fa-depreciation-methods.md)  

Ef margar deildir nota eign er hægt að dreifa tímabilsafskriftum sjálfvirkt á deildirnar samkvæmt úthlutunartöflu sem notandi skilgreinir.  

Hægt er að hætta við færslur í afskriftabók með því að nota keyrsluna **Hætta við eignabókarfærslur**. Að því loknu er hægt að bóka rétta upphæð með því að keyra runuvinnsluna **Reikna afskriftir** aftur. Villurnar sem eru leiðréttar eru bókaðar sem rangar eignarfjárhagsfærslur.  

Endurmat er notað til að laga virði að almennum verðbreytingum. Hægt er að nota runuvinnsluna **Eignavísitala** til að endurreikna upphæðir afskrifta.  

## Afskriftir reiknaðar sjálfvirkt:

Hægt er að keyra keyrsluna **Reikna afskriftir** mánaðarlega eða hvenær sem óskað er. Keyrslan hunsar eignir sem seldar voru, er lokuð eða óvirk eða notar handvirka afskriftaaðferð.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Reikna út afskriftir** og velja síðan viðkomandi tengil.  
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Velja hnappinn **Í lagi**.  

    Keyrslan reiknar afskriftirnar og býr til línur í eignafjárhagsbók.

4. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.  

    Á síðunni **Eignafjárhagsbók**, í reitnum **Fjöldi afskriftadaga**, er hægt að sjá hversu margir dagar afskriftadagar voru reiknaðir.  
5. Valið er **Bóka** aðgerðin.  

> [!NOTE]
> Þekkt takmörkun: Ef þú stillir reitinn **Nota áskilinn fj. daga** og reiturinn **Áskilinn fj. daga** er stilltur á gildi þar sem **Bókunardagsetning** mínus niðurstöðurnar **Fjöldi daga** í dagsetningu á fyrra almanaksári leyfir kerfið þér ekki að bóka afskriftina.
> Þú getur komist hjá þessu með því að lækka gildið í reitnum **Áskilinn fj. daga** í ekki hærra en útreiknaða daga þangað til bókun dagsetningar notar 30 daga/mánuð EÐA stilla flaggið **365 daga reikningsár** í afskriftarbókinni.
> Við mælum með fyrsta valkostinum þar sem ekki er víst að þú viljir breyta því að nota 30 daga/mánuð fyrir afskrift. Frekari upplýsingar er að finna í [365 daga reikningsár](fa-how-setup-depreciation.md#fiscal-year-365-days-field-depreciation).


## Að bóka afskrift handvirkt úr fjárhagsbók eigna

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.  
2. Stofnaður er upprunaleg Færslubókarlína og reitirnir fylltir út eftir þörfum.  
3. Í reitnum **Eignabókunartegund** er valinn **afskrift**.  
4. Valið er **Setja inn mótreikn. eigna** aðgerð. Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun afskriftar. Frekari upplýsingar er að finna í [Að setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Veldu aðgerðina **Birta** til að birta færslubókina.  

**Bókfært virði** á síðunni **Eignaspjald** er uppfært til samræmis.

Ef eignaúthlutunarlyklar eru settir upp til að úthluta upphæðum á mismunandi deildir eða verkefni er upphæðunum úthlutað við bókun. Frekari upplýsingar eru í [Uppsetning almennra eignaupplýsinga](fa-how-setup-general.md).  

## Til að stjórna bókfærðu lokavirði

Í reitnum **Bókfært lokavirði** á síðunni **Eignaafskriftabækur** er hægt að tilgreina bókfært virði sem eign á að hafa í gildandi afskriftabók þegar hún hefur verið afskrifuð að fullu. Hægt er að handfæra gildið eða fylla út reitinn **Bókfært lokavirði** á tengdri **afskriftabók** . Gildið fyllir sjálfkrafa út reitinn.

> [!NOTE]
> Ef síðasta afskrift þýðir að reiturinn **Bókvirði** á **Eignarspjaldi** sé núll er þessi upphæð sjálfkrafa dregin frá síðustu afskrift.<br /><br />
> Ef gildið í **Bókfært virði** er hærra en núll eftir síðustu afskrift, til dæmis vegna sléttunarerfiðleika eða hrakvirðis, er gildið í reitnum **Bókfært lokavirði** á síðunni **Afskriftabækur** hundsað. Nánari upplýsingar er að finna í [Bóka hrakvirði með kaupverði](fa-how-acquire.md#to-post-the-salvage-value-together-with-the-acquisition-cost).

## Úthlutun eignar reiknuð


1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignabókunarflokkar** og velja síðan viðkomandi tengil.
2. Valið er **Tengdur,Bókunarflokkur,Úthlutanir** **·** **·**  og síðan valið **Afskrift.**
3. Fjárhagsreikningarnir eru fylltir út og samsvarandi úthlutunarprósentur fyrir hvern bókunarflokk og síðan síðan síðan lokað.
4. Næst skal velja ![Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagsbækur eignar** og velja síðan viðkomandi tengil.
5. Eignin er færð inn og samsvarandi eignabókunarflokkur og afskriftabók ákvarða úthlutunarlínurnar.
6. Veldu aðgerðina **Birta** til að birta færslubókina.

> [!NOTE]  
> Ef margar deildir nota eign er hægt að velja víddina í eignafjárhagsbókarlínunni.

## Nota Afritunarlista nota til undirbúa að bóka margar afskriftabækur

Þegar fylltar eru út færslubókarlínur sem á að bóka í afskriftabók, er hægt að afrita línurnar yfir í aðgreinda bók, svo hægt sé að bóka þær í aðra afskriftabók. Nánari upplýsingar eru í [bóka færslur í mismunandi afskriftabækur](fa-how-depreciate-amortize.md#to-post-entries-to-different-depreciation-books).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Afskriftabækur** og velja síðan viðkomandi tengil.  
2. Opnið afskriftarbók, og smellið síðan á gátreitinn **Hluti afritunarlista**.  

> [!IMPORTANT]  
>   Ef reiturinn **Nota afritalista** hefur verið valinn skal ekki nota númeraraðir í færslubókinni. Ástæðan fyrir þessu er að númeraraðir fyrir fjárhagsbók eigna tekur ekki númeraröðinni fyrir færslubók eigna.  

## Færslur bókaðar í mismunandi afskriftabækur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.  
2. Í bókinni sem á að bóka afskriftir með, skal velja **Nota Afritalista** gátreitinn.  
3. Fyllið inn í eftirstandandi reiti eftir þörfum.  
4. Valið er **Bóka** aðgerðin.  
5. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignabækur** og velja síðan viðkomandi tengil.  

    > [!NOTE]  
    > Síðan **Eignabók** inniheldur nýjar línur fyrir mismunandi afskriftabækur samkvæmt afritunarlista.  
6. Skoða eða breyta línunum og síðan valið **Bóka** aðgerð.  

    > [!NOTE]  
    > Einnig er hægt að afrita færslu í aðra bók með því að rita afskriftabókarkóta í reitinn **Afrit í afskriftabók** þegar bókarlína er fyllt út.  

Hægt er að nota runuvinnsluna **Afrita afskriftabók** til að afrita færslur úr einni afskriftabók í aðra. Keyrslan býr til bókarlínur í bókarkeyrslunni sem tilgreind var á síðunni **Eignabókaruppsetning** fyrir afskriftabókina sem á að afrita í. Nánari upplýsingar eru notaðar með því að fara í Til að [afrita eignafærslur milli afskriftabóka](#to-copy-fixed-asset-ledger-entries-between-depreciation-books).  

## Til að afrita eignafærslur milli afskriftabækur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Afskriftabækur** og velja síðan viðkomandi tengil.  
2. Opna skal viðeigandi kort afskriftabókar og veljið síðan aðgerðina **afrita afskriftabók**.  
3. Á síðunni **afrita afskriftabók** þarf að fylla reitina út eftir þörfum.  
4. Velja hnappinn **Í lagi**.  

Afrituðu línurnar eru annaðhvort búnar til í eignafjárhagsbókinni eða eignabókinni eftir því hvort afskriftabókin sem verið er að afrita er með samþættingu við fjárhag.  

## Sjá einnig .

[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
