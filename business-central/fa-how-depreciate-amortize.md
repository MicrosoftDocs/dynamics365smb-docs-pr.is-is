---
title: Afskrifa eða greiða eign| Microsoft Docs
description: Það er nauðsynlegt að skilgreina hvernig þú hyggst niðurfæra, afskrifa eða greiða af eignum þínum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 46a138d7168c48e47f9db823108abc6d6af280ab
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380582"
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

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Reikna afskriftir** eða Lánardrottinn og veldu síðan tengda tengilinn.  
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Velja hnappinn **Í lagi**.  

    Keyrslan reiknar afskriftirnar og býr til línur í eignafjárhagsbók.

4. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignafjárhagsbækur** og veldu síðan tengda tengilinn.  

    Á síðunni **eignafjárhagsbók** í reitnum **Fjöldi afskriftadaga** má sjá hve margir afskriftadagar hafa verið reiknaðir.  
5. Valið er **Bóka** aðgerðin.  

## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>Að bóka afskrift handvirkt úr fjárhagsbók eigna
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignafjárhagsbók** og veldu síðan tengda tengilinn.  
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

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignafjárhagsbók** og veldu síðan tengda tengilinn.  
2. Stofnaður er Færslubókarlína og reitirnir fylltir út eftir þörfum.
3. Í reitnum **Eignabókunartegund** er valinn **úthlutun**.  
4. Valið er **Setja inn mótreikn. eigna** aðgerð. Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun úthlutunar.  
5. Veldu aðgerðina **Birta** til að birta færslubókina.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Nota Afritunarlista nota til undirbúa að bóka margar afskriftabækur
Þegar fylltar eru út færslubókarlínur sem á að bóka í afskriftabók, er hægt að afrita línurnar yfir í aðgreinda bók, svo hægt sé að bóka þær í aðra afskriftabók. Nánari upplýsingar eru í [bóka færslur í mismunandi afskriftabækur](fa-how-depreciate-amortize.md#to-post-entries-to-different-depreciation-books).

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Afskriftabækur** og veldu síðan tengda tengilinn.  
2. Opnið afskriftarbók, og smellið síðan á gátreitinn **Hluti afritunarlista**.  

> [!IMPORTANT]  
>   Ef reiturinn **Nota afritalista** hefur verið valinn skal ekki nota númeraraðir í færslubókinni. Ástæðan fyrir þessu er að númeraraðir fyrir fjárhagsbók eigna tekur ekki númeraröðinni fyrir færslubók eigna.  

## <a name="to-post-entries-to-different-depreciation-books"></a>Færslur bókaðar í mismunandi afskriftabækur
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignafjárhagsbók** og veldu síðan tengda tengilinn.  
2. Í bókinni sem á að bóka afskriftir með, skal velja **Nota Afritalista** gátreitinn.  
3. Fyllið inn í eftirstandandi reiti eftir þörfum.  
4. Valið er **Bóka** aðgerðin.  
5. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignabækur** og veldu síðan tengda tengilinn.  

    > [!NOTE]  
    >   Síðan **Eignabók** inniheldur nýjar línur fyrir mismunandi afskriftabækur samkvæmt afritunarlista.  
6. Skoða eða breyta línunum og síðan valið **Bóka** aðgerð.  

    > [!NOTE]  
    >   Einnig er hægt að afrita færslu í aðra bók með því að rita afskriftabókarkóta í reitinn **Afrit í afskriftabók** þegar bókarlína er fyllt út.  

Hægt er að nota runuvinnsluna **Afrita afskriftabók** til að afrita færslur úr einni afskriftabók í aðra. Við keyrsluna verða til bókarlínur í bókarkeyrslunni sem tilgreind var á síðunni **Eignabókaruppsetning** fyrir afskriftabókina sem á að afrita í. Nánari upplýsingar má finna hér á eftir.  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>Til að afrita eignafærslur milli afskriftabækur
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Afskriftabækur** og veldu síðan tengda tengilinn.  
2. Opna skal viðeigandi kort afskriftabókar og veljið síðan aðgerðina **afrita afskriftabók**.  
3. Á síðunni **afrita afskriftabók** þarf að fylla reitina út eftir þörfum.  
4. Velja hnappinn **Í lagi**.  

Afrituðu línurnar eru annaðhvort búnar til í fjárhagsbók eigna eða eignabókinni eftir því hvort afskriftabókin sem þú ert að afrita er með samþættingu við fjárhag.  

## <a name="see-also"></a>Sjá einnig
[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]