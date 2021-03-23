---
title: Uppsetning annarra gjaldmiðla | Microsoft Docs
description: Fjárhagurinn þinn er settur upp til að nota staðbundna gjaldmiðilinn (SGM) og annar gjaldmiðill er settur upp sem viðbótargjaldmiðill með rétt gengi stillt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9c66c9bbfe9403402238668fb1cd8df72ad21422
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391300"
---
# <a name="set-up-an-additional-reporting-currency"></a>Setja upp annan skýrslugjaldmiðil
Þar sem fyrirtæki starfa að auknum mæli í mörgum löndum/svæðum verður æ mikilvægara fyrir þau að geta skoðað eða skráð fjárhagsgögn í fleiri en einum gjaldmiðli.

Fjárhagurinn þinn er settur upp til að nota staðbundna gjaldmiðilinn (SGM), en þú getur sett hann upp til að einnig nota annan gjaldmiðil með rétt gengi stillt. Sé öðrum gjaldmiðli gefin svokölluð skilgreining Viðbótarskýrslugjaldmiðill mun [!INCLUDE[prod_short](includes/prod_short.md)] skrá upphæðirnar sjálfkrafa bæði í SGM og þessum viðbótarskýrslugjaldmiðli í hverri fjárhagsfærslu og í öðrum færslum á borð við færslur fyrir VSK.

> [!Warning]
> Aðgerðina Annar skýrslugjaldmiðill ætti ekki að nota sem grunn fyrir umreikning fjárhagslegra yfirlita. Hún er ekki verkfæri til að umreikna ársreikninga erlendra dótturfyrirtækja, sem hluti af samsteypufyrirtæki. Annan skýrslugjaldmiðil er aðeins hægt að nota til að undirbúa skýrslur í öðrum gjaldmiðli, líkt og sá gjaldmiðill væri heimagjaldmiðill fyrirtækisins.

## <a name="displaying-reports-and-amounts-in-the-additional-reporting-currency"></a>Skýrslur og upphæðir birtar í öðrum skýrslugjaldmiðli
Með því að nota annan skýrslugjaldmiðil er hægt að auðvelda skýrsluferli fyrirtækisins í eftirfarandi tilvikum:

- Fyrirtæki í löndum/svæðum utan ESB sem hafa þó stóran hluta færslna sinna milli fyrirtækja í ESB-löndum/svæðum. Í þessu tilviki gæti fyrirtækið sem er utan ESB skipt yfir í skráningu í evrum til að gera fjárhagsskýrslur sínar nytsamlegri fyrir viðskiptafélaga sína í ESB.
- Fyrirtæki sem vilja einnig birta skýrslur sínar í gjaldmiðli sem er notaður meira á alþjóðavísu en þeirra eigin.

Nokkrar fjárhagsskýrslur eru byggðar á fjárhagsfærslum. Til að birta skýrslugögn í öðrum skýrslugjaldmiðli er einfaldlega hakað í reitinn **Sýna upphæðir í öðrum skýrslugjaldmiðli** á flýtiflipanum **Valkostir** fyrir viðeigandi fjárhagsskýrslu.

## <a name="adjusting-exchange-rates"></a>Gengi leiðrétt
Vegna þess hve tíðar gengisbreytingar eru verður reglubundið að leiðrétta aðra jafngildisgjaldmiðla í kerfinu. Sé það ekki gert verða upphæðir misvísandi sem hafa verið umreiknaðar úr erlendum (eða aukalegum) gjaldmiðlum og bókaðar í fjárhag í SGM. Að auki verður að uppfæra daglegar færslur sem eru bókaðar áður en daglegt gengi er fært inn eftir að upplýsingarnar um daglegt gengi hafa verið færðar inn. Keyrslan **Stilla gengi** er notuð til að lagfæra gengi bókaðs viðskiptamanns, lánardrottins og bankareikningsfærslna. Hún getur einnig uppfært upphæðir annars skýrslugjaldmiðils í fjárhagsfærslum. Frekari upplýsingar eru í [Uppfæra gengi gjaldmiðils](finance-how-update-currencies.md).

## <a name="setting-up-an-additional-reporting-currency"></a>Uppsetning annars skýrslugjaldmiðils
Til að setja upp annan skýrslugjaldmiðil, verður þú að fylgja þessum skrefum:

-   Tilgreinið fjárhagsreikninga fyrir leiðréttingu á gengi bókana  
-   Tilgreinið aðferð gengisleiðréttingar fyrir alla fjárhagsreikninga.  
-   Tilgreinið aðferð fyrir gengisleiðréttingu í VSK-færslum  
-   Virkja annan skýrslugjaldmiðil  

### <a name="to-specify-general-ledger-accounts-for-posting-exchange-rate-adjustments"></a>Tilgreinið fjárhagsreikninga fyrir leiðréttingu á gengi bókana  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Gjaldmiðlar** og veldu síðan tengda tengilinn.  
2. Á síðunni **Gjaldmiðlar** skal fylla út eftirfarandi reiti fyrir annan skýrslugjaldmiðil.  

|Svæði|Description|  
|---------------------------------|---------------------------------------|  
|**Reikningur orðins fjárhagshagnaðar**|Fjárhagsreikningurinn sem gengishagnaður bókast í vegna leiðréttingar á milli SGM og annars skýrslugjaldmiðils verður bókaður.|  
|**Reikningur orðins fjárhagstaps**|Fjárhagsreikningurinn sem gengistap bókast í vegna leiðréttingar á milli SGM og annars skýrslugjaldmiðils verður bókaður.|  
|**Afgangsreikningur hagnaðar**|Fjárhagsreikningurinn sem kerfið bókar afgangsupphæðir sem eru hagnaður í ef bókað er í kerfishlutann Fjárhagur, í bæði SGM og öðrum skýrslugjaldmiðli.|  
|**Afgangsreikningur taps**|Fjárhagsreikningurinn sem kerfið bókar afgangsupphæðir sem eru tap í ef bókað er í kerfishlutann Fjárhagur, í bæði SGM og öðrum skýrslugjaldmiðli.|

> [!NOTE]  
>  Afgangsupphæðir geta komið fram þegar [!INCLUDE[prod_short](includes/prod_short.md)] sléttar debet- og kreditupphæðir sem hafa verið umreiknaðar úr SGM í annað skýrslugengi.  

Það verður að tilgreina hvernig á að leiðrétta upphæðir í fjárhag fyrir gengissveiflur milli SGM og hins skýrslugjaldmiðilsins fyrir hvern fjárhagsreikning.  

### <a name="to-specify-the-exchange-rate-adjustment-method-for-all-general-ledger-accounts"></a>Til að tilgreina aðferð gengisleiðréttingar fyrir alla fjárhagsreikninga  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókhaldslykill** og veldu síðan tengda tengilinn.  
2. Á síðunni **Bókhaldslykill** skal velja viðeigandi lykil og síðan velja aðgerðina **Breyta**.  
3. Á síðunni **Fjárhagsspjald** skal velja viðeigandi aðferð í reitnum **Gengisleiðrétting**.  

    Ef bókað er í öðrum skýrslugjaldmiðli er tilgreint hvernig þessi fjárhagsreikningur verður leiðréttur með tilliti til gengissveiflna milli SGM og annars skýrslugjaldmiðils í reitnum **Gengisleiðrétting**. Eftirfarandi tafla sýnir valkostina sem hægt er að velja á milli.  

    |Svæði|Lýsing|  
    |----------------------------------|---------------------------------------|  
    |**Engin leiðrétting**|Engin gengisleiðrétting er gerð í fjárhagsreikningnum. Þetta er sjálfgefni valkosturinn.<br /><br /> **Athugið:** Valkosturinn ætti að vera valinn ef gengið milli SGM og aukalega skýrslugjaldmiðilsins er alltaf fast.|  
    |**Leiðrétta upphæð**|SGM-upphæðin er leiðrétt samkvæmt öllum gengishagnaði eða tapi. Gengishagnaður eða gengistap er bókað á fjárhagsreikninginn í reitinn **Upphæð** og á þá reikninga sem voru tilgreindir fyrir hagnað eða tap í reitunum **Reikningur orðins fjárh. hagnaðar** og **Reikningur orðins fjárh. taps** á síðunni **Gjaldmiðlar**.|  
    |**Leiðrétta upphæð annars gjaldmiðils**|Annar skýrslugjaldmiðill er leiðréttur samkvæmt öllum gengishagnaði eða tapi. Gengishagnaður eða gengistap er bókað á fjárhagsreikninginn í reitinn **Upphæð annars gjaldmiðils** og á þá reikninga sem voru tilgreindir fyrir hagnað eða tap í reitunum **Reikningur orðins fjárh. hagnaðar** og **Reikningur orðins fjárh. taps** á síðunni **Gjaldmiðlar**.|  

    Gengishagnaður og gengistap er bókað þegar keyrslan **Leiðrétta gengi** er keyrð. Leiðréttingargengið er auðkennt á síðunni **Gengi gjaldmiðils** og ber það saman við upphæðina í reitunum **Upphæð** og **Upphæð annars gjaldmiðils** í fjárhagsfærslunni til að ákvarða hvort um gengishagnað eða gengistap sé að ræða. Keyrslan notar valkostinn sem var valinn í reitnum **Gengisleiðrétting** til að ákvarða hvernig skuli reikna og bóka gengishagnað eða -tap fyrir fjárhagsreikninga.  

4.  Síðunni **Fjárhagsspjald** lokað.  

### <a name="to-specify-exchange-rate-adjustment-method-for-vat-entries"></a>Tilgreina aðferð fyrir gengisleiðréttingu í VSK-færslum  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagsgrunnur** og veldu síðan tengda tengilinn.  
2. Á síðunni **Fjárhagsgrunnur** skal velja viðeigandi aðferð í reitnum **VSK-gengisleiðrétting**.  
3. Ef bókað er í öðrum skýrslugjaldmiðli má tilgreina í reitnum **VSK-gengisleiðrétting** hvernig þeir reikningar sem stofnaðir voru fyrir bókun VSK á síðunni **VSK-bókunargrunnur** eru leiðréttir fyrir gengissveiflur milli SGM og annars skýrslugjaldmiðils.  

    Þegar keyrslan **Leiðrétta gengi** er keyrð er leiðréttingargengið fundið á síðunni **Gengi gjaldmiðils** og upphæðirnar í reitunum **Upphæð** og **Upphæð annars gjaldmiðils** í VSK-færslunni bornar saman til að ákvarða hvort um gengishagnað eða gengistap sé að ræða. Keyrslan notar kostinn sem valinn var í þessum reit til að ákvarða hvernig eigi að bóka gengishagnað eða -tap vegna VSK-reikninga.  

    Sömu valkostir og í fjárhagsfærslum eru í boði en í þessu tilfelli eru færslurnar sem eru leiðréttar VSK-færslur. Eftirfarandi tafla sýnir valkostina sem hægt er að velja á milli.

    |Svæði|Description|  
    |----------------------------------|---------------------------------------|  
    |**Engin leiðrétting**|Engin gengisleiðrétting er gerð í fjárhagsreikningnum. Þetta er sjálfgefni valkosturinn.|  
    |**Leiðrétta upphæð**|SGM-upphæðin er leiðrétt samkvæmt öllum gengishagnaði eða tapi. Gengishagnaður eða gengistap er bókað á fjárhagsreikninginn í reitinn **Upphæð** og á þá reikninga sem voru tilgreindir fyrir hagnað eða tap í reitunum **Reikningur orðins fjárh. hagnaðar** og **Reikningur orðins fjárh. taps** á síðunni **Gjaldmiðlar**.|  
    |**Leiðrétta upphæð annars gjaldmiðils**|Annar skýrslugjaldmiðill er leiðréttur samkvæmt öllum gengishagnaði eða tapi. Gengishagnaður eða gengistap er bókað á fjárhagsreikninginn í reitinn **Upphæð annars gjaldmiðils** og á þá reikninga sem voru tilgreindir fyrir hagnað eða tap í reitunum **Reikningur orðins fjárh. hagnaðar** og **Reikningur orðins fjárh. taps** á síðunni **Gjaldmiðlar**.|  

### <a name="to-activate-the-additional-reporting-currency"></a>Virkja annan skýrslugjaldmiðil  
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagsgrunnur** og veldu síðan tengda tengilinn.  
2. Á síðunni **Fjárhagsgrunnur** skal velja reitinn **Annar skýrslugjaldmiðill** til að velja annan skýrslugjaldmiðil sem á að nota.  
3. Þegar farið er úr reitnum [!INCLUDE[prod_short](includes/prod_short.md)] birtast staðfestingarskilaboð sem lýsa því hvað gerist þegar annar skýrslugjaldmiðill er virkjaður.  
4. Velja hnappinn **Já** til að staðfesta að virkja eigi gjaldmiðilinn.  
5. Keyrslan **Leiðrétta annan skýrslugjaldm.** opnast.

    Keyrslan umreiknar upphæðir í sgm sem eru í gildandi færslum yfir í annan skýrslugjaldmiðil. Keyrslan notar sjálfgefið gengi sem er afritað úr því gengi sem er gilt á vinnudagsetningunni á síðunni **Gengi gjaldmiðils**. Afgangsupphæðir sem koma upp í umreikningi á SGM yfir í aukalega skýrslugjaldmiðilinn eru bókaðar í reikninga fjárhagslegs hagnaðar eða fjárhagslegs taps, sem tilgreindir eru á síðunni **Gjaldmiðlar**. Bókunardagsetningin og skjalanúmer þessara færslna eru þau sömu og í upphaflegu fjárhagsfærslunni. Eftir að allar afgangsfærslurnar hafa verið bókaðar bókar keyrslan sléttunarfærslu á lokadagsetningu hvers lokaðs árs í reikning óráðstafaðs eigin fjár. Það tryggir að lokastaða tekjureiknings hvers lokaðs árs sé 0 í bæði SGM og öðrum skýrslugjaldmiðli.
6. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
7. Veldu hnappinn **Í lagi** til að ræsa keyrsluna.  

Eftir keyrsluna verða upphæðir í eftirfarandi færslum sem fyrir eru færðar bæði í SGM og öðrum skýrslugjaldmiðli:  

- Fjárhagsfærslur  
- Birgðajöfnunarfærslur  
- VSK-færslur...  
- Verkfærslur  
- Virðisfærslur  
- Framleiðslupantanalínur  
- Fjárhagsfærslur framleiðslupöntunar  

Einnig eru allar síðari færslur af sömu gerð skráðar bæði í SGM og öðrum skýrslugjaldmiðli.  

> [!NOTE]  
>  Reiturinn **Annar skýrslugjaldmiðill** verður aðeins virkur eftir að valinn hefur verið hnappurinn **Í lagi** í keyrslunni **Leiðrétta annan skýrslugjaldmiðil**.  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig
[Uppfæra gengi](finance-how-update-currencies.md)  
[Lokaár og Tímabil](year-close-years-periods.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]