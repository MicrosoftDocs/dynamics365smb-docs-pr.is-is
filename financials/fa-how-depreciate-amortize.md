---
title: "Hvernig á að: afskrifa eða greiða af eignum | Microsoft Docs"
description: "Lýsir því hvernig á að afskrifa eða greiða af eignum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 3ea185979c2339a578149259f53aa81c18e5161b
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-depreciate-or-amortize-fixed-assets"></a>Hvernig á að: afskrifa eða greiða af eignum
Afskriftir eru notaðar til að dreifa kostnaði við eignir eins og tæki og búnað á afskriftartíma þeirra. Tilgreina verður afskriftaraðferð fyrir hverja eign.  

 Hægt er að bóka afskriftir með tvennum hætti:  

* Sjálfvirkt með því að keyra keyrsluna **Reikna afskriftir**.  
* Handvirkt með því að nota fjárhagsbók eigna.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] getur reiknað daglegar afskriftir og er því unnt að reikna afskriftir fyrir hvaða tímabil sem er. Þess vegna er til dæmis hægt að greina rekstrarafkomu hverju sinni miðað við mánuð, ársfjórðung eða ár. Útreikningurinn notar 360 daga staðalár og 30 daga staðalmánuð. Frekari upplýsingar eru í [afskriftaaðferðir](fa-depreciation-methods.md)  

Ef margar deildir nota eign er hægt að dreifa tímabilsafskriftum sjálfvirkt á deildirnar samkvæmt úthlutunartöflu sem notandi skilgreinir.  

Hægt er að hætta við færslur í afskriftabók með því að nota keyrsluna **Hætta við eignabókarfærslur**. Að því loknu er hægt að bóka rétta upphæð með því að keyra runuvinnsluna **Reikna afskriftir** aftur. Villurnar sem eru leiðréttar eru bókaðar sem rangar eignarfjárhagsfærslur.  

Endurmat er notað til að laga virði að almennum verðbreytingum. Hægt er að nota runuvinnsluna **Eignavísitala** til að endurreikna upphæðir afskrifta.  

## <a name="to-calculate-depreciation-automatically"></a>Afskriftir reiknaðar sjálfvirkt:
Hægt er að keyra keyrsluna **Reikna afskriftir** mánaðarlega eða hvenær sem óskað er. Runuvinnslan hunsar eignir sem hafa verið seldar, eignir sem eru lokaðar eða óvirkar, eða nota handvirka afskriftaraðferð.  

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Reikna afskriftir**, og velja síðan viðeigandi tengil.  
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Velja hnappinn **Í lagi**.  

    Keyrslan reiknar afskriftirnar og býr til línur í eignafjárhagsbók.  
4. Efst í hægra horninu skal velja **Leit að síðu eða skýrslu** táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið"), slá inn **Eignafjárhagsbækur** og velja svo tengdan tengil.  

    Í glugganum **eignafjárhagsbók **í reitnum **Fjöldi afskriftadaga** má sjá hve margir afskriftadagar hafa verið reiknaðir.  
5. Valið er **bóka ** aðgerð.  

## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>Að bóka afskrift handvirkt úr fjárhagsbók eigna
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Fjárhagsbók eignar**, og velja síðan viðeigandi tengil.  
2. Stofnaður er upprunaleg Færslubókarlína og reitirnir fylltir út eftir þörfum.  
3. Í reitnum **Eignabókunartegund** er valinn **afskrift**.  
4. Valið er **Setja inn mótreikn. eigna** aðgerð. Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun afskriftar. Nánari upplýsingar eru í "setja upp bókunarflokka eigna" hlutanum í [Hvernig: Setja Upp almennar upplýsingar um eignir](fa-how-setup-general.md).  
5. Á flipanum **Heim** veljið **Bóka** til að bóka færslubókina.  

Ef settir hafa verið upp eignarúthlutunarlyklar til að úthluta upphæðum til mismunandi deilda eða verkefna, verða upphæðirnar úthlutað á meðan á bókun stendur. Nánari upplýsingar sjá [Hvernig: setja upp almennar upplýsingar um eignir](fa-how-setup-general.md).  

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal"></a>Reikna út úthlutanir í eignafjárhagsbókum:
Ef margar deildir nota eign er hægt að dreifa tímabilsafskriftum sjálfvirkt á deildirnar samkvæmt úthlutunartöflu sem notandi skilgreinir.  

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Fjárhagsbók eignar**, og velja síðan viðeigandi tengil.  
2. Stofnaður er Færslubókarlína og reitirnir fylltir út eftir þörfum.
3. Í reitnum **Eignabókunartegund** er valinn **úthlutun**.  
4. Valið er **Setja inn mótreikn. eigna** aðgerð. Seinni færslubókarlína er búin til fyrir mótreiknings sem er sett upp fyrir bókun úthlutunar.  
5. Á flipanum **Heim** veljið **Bóka** til að bóka færslubókina.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Nota Afritunarlista nota til undirbúa að bóka margar afskriftabækur
Þegar fylltar eru út færslubókarlínur sem á að bóka í afskriftabók, er hægt að afrita línurnar yfir í aðgreinda bók, svo hægt sé að bóka þær í aðra afskriftabók. Nánari upplýsingar eru í "bóka færslur í mismunandi afskriftabækur" hlutanum.

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Afskriftarbækur**, og velja síðan viðeigandi tengil.  
2. Opnið afskriftarbók, og smellið síðan á gátreitinn **Hluti afritunarlista**.  

**Mikilvægt:** Ef reiturinn **Nota afritalista** hefur verið valinn skal ekki nota númeraraðir í færslubókinni. Ástæðan fyrir þessu er að númeraraðir fyrir fjárhagsbók eigna tekur ekki númeraröðinni fyrir færslubók eigna.  

## <a name="to-post-entries-to-different-depreciation-books"></a>Færslur bókaðar í mismunandi afskriftabækur
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Fjárhagsbók eignar**, og velja síðan viðeigandi tengil.  
2. Í bókinni sem á að bóka afskriftir með, skal velja **Nota Afritalista** gátreitinn.  
3. Fyllið inn í eftirstandandi reiti eftir þörfum.  
4. Valið er **bóka ** aðgerð.  
5. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Eignafærslubækur**, og velja síðan viðeigandi tengil.  

    **Athugið:**Glugginn **Eignafærslubók** inniheldur nýjar línur fyrir mismunandi afskriftabækur samkvæmt afritunarlistanum.  
6. Skoða eða breyta línunum og síðan valið **Bóka** aðgerð.  

    **Athugið:**: Einnig er hægt að afrita færslu í aðra bók með því að rita afskriftabókarkóða í reitinn **Afrit í afskriftabók** þegar bókarlína er fyllt út.  

Hægt er að nota runuvinnsluna **Afrita afskriftabók** til að afrita færslur úr einni afskriftabók í aðra. Við keyrsluna verða til bókarlínur í bókarkeyrslunni sem tilgreind var í glugganum **Eignabókaruppsetning** fyrir afskriftabókina sem á að afrita í. Nánari upplýsingar má finna hér á eftir.  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>Til að afrita eignafærslur milli afskriftabækur
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Afskriftarbækur**, og velja síðan viðeigandi tengil.  
2. Opna skal viðeigandi kort afskriftabókar og veljið síðan aðgerðina **afrita afskriftabók**.  
3. Í glugganum **afrita afskriftabók** þarf að fylla reitina út eftir þörfum.  
4. Velja hnappinn **Í lagi**.  

Afrituðu línurnar eru annaðhvort búnar til í fjárhagsbók eigna eða eignabókinni eftir því hvort afskriftabókin sem þú ert að afrita er með samþættingu við fjárhag.  

## <a name="see-also"></a>Sjá einnig
[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

