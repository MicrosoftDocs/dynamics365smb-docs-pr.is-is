---
title: Afskrifa eða greiða eign
description: 'Það er nauðsynlegt að skilgreina hvernig þú hyggst niðurfæra, afskrifa eða greiða af eignum þínum, svo sem vélum og búnaði á afskriftartíma þeirra.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.search.form: '5610, 5611, 5629, 5633, 5659, 5660, 5663, 5619, 5666'
ms.date: 06/15/2021
ms.author: bholtorf
---
# <a name="depreciate-or-amortize-fixed-assets"></a>Afskrifa eða greiða af eignum

Afskriftir eru notaðar til að dreifa kostnaði við eignir eins og tæki og búnað á afskriftartíma þeirra. Tilgreina verður afskriftaraðferð fyrir hverja eign.  

 Hægt er að bóka afskriftir með tvennum hætti:  

* Sjálfvirkt með því að keyra keyrsluna **Reikna afskriftir**.  
* Handvirkt með því að nota fjárhagsbók eigna.  

[!INCLUDE[prod_short](includes/prod_short.md)] getur reiknað daglegar afskriftir og er því unnt að reikna afskriftir fyrir hvaða tímabil sem er. Þess vegna er til dæmis hægt að greina rekstrarafkomu hverju sinni miðað við mánuð, ársfjórðung eða ár. Útreikningurinn notar 360 daga staðalár og 30 daga staðalmánuð. Frekari upplýsingar eru í [afskriftaaðferðir](fa-depreciation-methods.md)  

Ef margar deildir nota eign er hægt að dreifa tímabilsafskriftum sjálfvirkt á deildirnar samkvæmt úthlutunartöflu sem notandi skilgreinir.  

Hægt er að hætta við færslur í afskriftabók með því að nota keyrsluna **Hætta við eignabókarfærslur**. Að því loknu er hægt að bóka rétta upphæð með því að keyra runuvinnsluna **Reikna afskriftir** aftur. Villurnar sem eru leiðréttar eru bókaðar sem rangar eignarfjárhagsfærslur.  

Endurmat er notað til að laga virði að almennum verðbreytingum. Hægt er að nota runuvinnsluna **Eignavísitala** til að endurreikna upphæðir afskrifta.  

## <a name="to-calculate-depreciation-automatically"></a>Afskriftir reiknaðar sjálfvirkt:

Hægt er að keyra keyrsluna **Reikna afskriftir** mánaðarlega eða hvenær sem óskað er. Runuvinnslan hunsar eignir sem hafa verið seldar, eignir sem eru lokaðar eða óvirkar, eða nota handvirka afskriftaraðferð.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Reikna út afskriftir** og velja síðan viðkomandi tengil.  
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Velja hnappinn **Í lagi**.  

    Keyrslan reiknar afskriftirnar og býr til línur í eignafjárhagsbók.

4. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.  

    Á síðunni **eignafjárhagsbók** í reitnum **Fjöldi afskriftadaga** má sjá hve margir afskriftadagar hafa verið reiknaðir.  
5. Valið er **Bóka** aðgerðin.  

> [!NOTE]
> Þekkt takmörkun: Ef þú stillir reitinn **Nota áskilinn fj. daga** og reiturinn **Áskilinn fj. daga** er stilltur á gildi þar sem **Bókunardagsetning** mínus niðurstöðurnar **Fjöldi daga** í dagsetningu á fyrra almanaksári leyfir kerfið þér ekki að bóka afskriftina.
> Þú getur komist hjá þessu með því að lækka gildið í reitnum **Áskilinn fj. daga** í ekki hærra en útreiknaða daga þangað til bókun dagsetningar notar 30 daga/mánuð EÐA stilla flaggið **365 daga reikningsár** í afskriftarbókinni.
> Við mælum með fyrsta valkostinum þar sem ekki er víst að þú viljir breyta því að nota 30 daga/mánuð fyrir afskrift. Frekari upplýsingar er að finna í [365 daga reikningsár](fa-how-setup-depreciation.md#fiscal-year-365-days-field-depreciation).


## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>Að bóka afskrift handvirkt úr fjárhagsbók eigna

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.  
2. Stofnaður er upprunaleg Færslubókarlína og reitirnir fylltir út eftir þörfum.  
3. Í reitnum **Eignabókunartegund** er valinn **afskrift**.  
4. Valið er **Setja inn mótreikn. eigna** aðgerð. Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun afskriftar. Frekari upplýsingar er að finna í [Að setja upp bókunarflokka eigna](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Veldu aðgerðina **Birta** til að birta færslubókina.  

**Bókfært virði** á síðunni **Eignaspjald** er uppfært til samræmis.

Ef settir hafa verið upp eignarúthlutunarlyklar til að úthluta upphæðum til mismunandi deilda eða verkefna, verða upphæðirnar úthlutað á meðan á bókun stendur. Frekari upplýsingar eru í [Uppsetning almennra eignaupplýsinga](fa-how-setup-general.md).  

## <a name="to-manage-the-ending-book-value"></a>Til að stjórna bókfærðu lokavirði

Í reitnum **Bókfært lokavirði** á síðunni **Eignaafskriftabækur** er hægt að tilgreina bókfært virði sem þú vilt að eignin þín eigi að hafa í núverandi afskriftabók eftir að hún hefur verið afskrifuð að fullu. Þú getur gert þetta handvirkt eða þú getur fyllt inn reitinn **Sjálfg. bókf. lokavirði** á tengdri **Afskriftabók** , sem verður síðan notuð til að fylla út í reitinn sjálfkrafa.

> [!NOTE]
> Ef síðasta afskrift þýðir að reiturinn **Bókvirði** á **Eignarspjaldi** sé núll er þessi upphæð sjálfkrafa dregin frá síðustu afskrift.<br /><br />
> Ef gildið í **Bókfært virði** er hærra en núll eftir síðustu afskrift, til dæmis vegna sléttunarerfiðleika eða hrakvirðis, er gildið í reitnum **Bókfært lokavirði** á síðunni **Afskriftabækur** hundsað. Nánari upplýsingar er að finna í [Bóka hrakvirði með kaupverði](fa-how-acquire.md#to-post-the-salvage-value-together-with-the-acquisition-cost).

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal"></a>Reikna út úthlutanir í eignafjárhagsbókum:

Ef margar deildir nota eign er hægt að dreifa tímabilsafskriftum sjálfvirkt á deildirnar samkvæmt úthlutunartöflu sem notandi skilgreinir.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.  
2. Stofnaður er Færslubókarlína og reitirnir fylltir út eftir þörfum.
3. Í reitnum **Eignabókunartegund** er valinn **úthlutun**.  
4. Valið er **Setja inn mótreikn. eigna** aðgerð. Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun úthlutunar.  
5. Veldu aðgerðina **Birta** til að birta færslubókina.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Nota Afritunarlista nota til undirbúa að bóka margar afskriftabækur

Þegar fylltar eru út færslubókarlínur sem á að bóka í afskriftabók, er hægt að afrita línurnar yfir í aðgreinda bók, svo hægt sé að bóka þær í aðra afskriftabók. Nánari upplýsingar eru í [bóka færslur í mismunandi afskriftabækur](fa-how-depreciate-amortize.md#to-post-entries-to-different-depreciation-books).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Afskriftabækur** og velja síðan viðkomandi tengil.  
2. Opnið afskriftarbók, og smellið síðan á gátreitinn **Hluti afritunarlista**.  

> [!IMPORTANT]  
>   Ef reiturinn **Nota afritalista** hefur verið valinn skal ekki nota númeraraðir í færslubókinni. Ástæðan fyrir þessu er að númeraraðir fyrir fjárhagsbók eigna tekur ekki númeraröðinni fyrir færslubók eigna.  

## <a name="to-post-entries-to-different-depreciation-books"></a>Færslur bókaðar í mismunandi afskriftabækur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.  
2. Í bókinni sem á að bóka afskriftir með, skal velja **Nota Afritalista** gátreitinn.  
3. Fyllið inn í eftirstandandi reiti eftir þörfum.  
4. Valið er **Bóka** aðgerðin.  
5. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignabækur** og velja síðan viðkomandi tengil.  

    > [!NOTE]  
    >   Síðan **Eignabók** inniheldur nýjar línur fyrir mismunandi afskriftabækur samkvæmt afritunarlista.  
6. Skoða eða breyta línunum og síðan valið **Bóka** aðgerð.  

    > [!NOTE]  
    >   Einnig er hægt að afrita færslu í aðra bók með því að rita afskriftabókarkóta í reitinn **Afrit í afskriftabók** þegar bókarlína er fyllt út.  

Hægt er að nota runuvinnsluna **Afrita afskriftabók** til að afrita færslur úr einni afskriftabók í aðra. Við keyrsluna verða til bókarlínur í bókarkeyrslunni sem tilgreind var á síðunni **Eignabókaruppsetning** fyrir afskriftabókina sem á að afrita í. Nánari upplýsingar má finna hér á eftir.  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>Til að afrita eignafærslur milli afskriftabækur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Afskriftabækur** og velja síðan viðkomandi tengil.  
2. Opna skal viðeigandi kort afskriftabókar og veljið síðan aðgerðina **afrita afskriftabók**.  
3. Á síðunni **afrita afskriftabók** þarf að fylla reitina út eftir þörfum.  
4. Velja hnappinn **Í lagi**.  

Afrituðu línurnar eru annaðhvort búnar til í fjárhagsbók eigna eða eignabókinni eftir því hvort afskriftabókin sem þú ert að afrita er með samþættingu við fjárhag.  

## <a name="see-also"></a>Sjá einnig .

[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
