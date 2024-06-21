---
title: Setja upp aðra gjaldmiðla
description: Fjárhagurinn þinn er settur upp til að nota staðbundna gjaldmiðilinn (SGM) og annar gjaldmiðill er settur upp sem viðbótargjaldmiðill með rétt gengi stillt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'multiple currencies, foreign exchange rates'
ms.search.form: '5, 16,118, 483, 495'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Setja upp annan skýrslugjaldmiðil

Þar sem fyrirtæki starfa sífellt fleiri lönd/svæði verður mikilvægara að þau geti skoðað og tilkynnt fjárhagsgögn í fleiri en einum gjaldmiðli.

> [!NOTE]  
> Ef [!INCLUDE[prod_short](includes/prod_short.md)] leitað er að upplýsingum um gengi í rauntíma um gengi erlendra gjaldeyria eða sögulegt gengi er það kallað gjaldmiðill. Auk þessarar greinar geturðu skoðað [Uppfæra gengi gjaldmiðla](finance-how-update-currencies.md).

Fjárhagurinn þinn er settur upp til að nota staðbundna gjaldmiðilinn (SGM), en þú getur sett hann upp til að einnig nota annan gjaldmiðil með rétt gengi stillt. Ef annar gjaldmiðill er tilgreindur sem annar skýrslugjaldmiðill (AGM) [!INCLUDE[prod_short](includes/prod_short.md)]  skráir sjálfkrafa upphæðir bæði í SGM og SGM í hverja fjárhagsfærslu og öðrum færslum, svo sem VSK-færslum.

> [!Warning]
> Ekki ætti að nota eiginleikann AGM sem grunn fyrir þýðingu fjárhagsskýrslna nema skilja eigi takmarkanir á honum. Það getur ekki umreiknað ársreikninga erlendra dótturfyrirtækja sem hluta af samsteypufyrirtæki. Aðeins er hægt að nota AGM til að undirbúa skýrslur í öðrum gjaldmiðli, líkt og sá gjaldmiðill væri SGM fyrirtækisins.
>
> Til dæmis er um að ræða mikið magn af útistandandi reikningum í breskum pundum (GBP) og AGM hefur verið sett upp þannig að hann sé GBP. Í þessu dæmi eru upphæðir í útistandandi reikningum sem nota GBP ekki leiðréttar fyrir gengishagnað/tap í AGM, aðeins upphæðir í útistandandi reikningum sem eru í öðrum gjaldmiðlum. Það þýðir að ef þú notar ACY til að gefa upp fjárhagsskýrslurnar gæti það leitt til of lágrar eða of hárrar útistandandi stöðu á viðskiptakröfum.

## Birting skýrslna og upphæða í AGM

Notkun AGM getur aðstoðað skýrslugerðarferli fyrirtækis í eftirfarandi tilvikum:

- Fyrirtæki í löndum/svæðum utan ESB sem hafa þó stóran hluta færslna sinna milli fyrirtækja í ESB-löndum/svæðum. Í þessu tilviki gæti fyrirtækið sem er utan ESB einnig viljað gefa skýrslu í evrum til að gera fjárhagsskýrslur sínar hæfari fyrir viðskiptafélaga í ESB.
- Fyrirtæki sem vilja einnig birta skýrslur sínar í gjaldmiðli sem er notaður meira á alþjóðavísu en þeirra eigin.

Nokkrar fjárhagsskýrslur eru byggðar á fjárhagsfærslum. Til að birta skýrslugögn í AGM skal velja gátreitinn **Sýna upphæðir í öðrum skýrslugjaldmiðli** á flýtiflipanum **Valkostir** fyrir viðeigandi fjárhagsskýrslu.

## Leiðrétting á gengi

Vegna þess að gengi sveiflast stöðugt verður að leiðrétta AGM-jafngildi í kerfinu reglulega. Ef þessar leiðréttingar eru ekki gerðar geta upphæðir sem umreiknaðar eru úr erlendum (eða viðbótar-) gjaldmiðlum og bókaðar í fjárhag í SGM verið misvísandi. Að auki verður að uppfæra daglegar færslur sem eru bókaðar áður en daglegt gengi er fært inn eftir að upplýsingarnar um daglegt gengi hafa verið færðar inn.  **Keyrslan** Leiðrétta gengi er notuð til að leiðrétta gengi bókaðra viðskiptamanna, lánardrottins og bankareikningsfærslna. Hann getur einnig uppfært upphæðir ÍSM í fjárhagsfærslum. Frekari upplýsingar eru í [Uppfæra gengi gjaldmiðils](finance-how-update-currencies.md).

## Uppsetning AGM

Til að setja upp AGM skal fylgja eftirfarandi skrefum:

- Tilgreinið fjárhagsreikninga fyrir leiðréttingu á gengi bókana  
- Tilgreinið aðferð gengisleiðréttingar fyrir alla fjárhagsreikninga.  
- Tilgreinið aðferð fyrir gengisleiðréttingu í VSK-færslum  
- Virkja AGM.  

### Tilgreinið fjárhagsreikninga fyrir leiðréttingu á gengi bókana  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Gjaldmiðlar** og velja síðan viðkomandi tengil.  
2. Á síðunni **Gjaldmiðlar skal** fylla út eftirfarandi reiti fyrir AGM.  

|Svæði|Heimildasamstæða|  
|---------------------------------|---------------------------------------|  
|**Reikningur orðins fjárhagshagnaðar**|Fjárhagsreikningurinn sem gengishagnaður er bókaður á vegna gengisleiðréttinga á milli SGM og AGM.|  
|**Reikningur orðins fjárhagstaps**|Fjárhagsreikningurinn sem gengistap vegna gengisleiðréttinga á milli SGM og AGM er bókað á.|  
|**Afgangsreikningur hagnaðar**|Fjárhagsreikningurinn sem afgangsupphæðir sem eru hagnaður eru bókaðar á ef bókað er í kerfishlutanum Fjárhagur bæði í SGM og SGM.|  
|**Afgangsreikningur taps**|Fjárhagsreikningurinn sem afgangsupphæðir sem eru tap eru bókaðar á ef bókað er í kerfishlutanum Fjárhagur bæði í SGM og AGM.|

> [!NOTE]  
> Afgangsupphæðir geta orðið við [!INCLUDE[prod_short](includes/prod_short.md)] sléttun debet- og kreditupphæða sem hafa verið umreiknaðar úr SGM í SGM.  

Fyrir hvern fjárhagsreikning þarf að tilgreina hvernig fjárhagsupphæðir fyrir þann reikning eru leiðréttar vegna gengissveiflna milli SGM og AGM.  

### Til að tilgreina aðferð gengisleiðréttingar fyrir alla fjárhagsreikninga

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill** og velja síðan viðkomandi tengil.  
2. Á síðunni **Bókhaldslykill** skal velja viðeigandi lykil og síðan velja aðgerðina **Breyta**.  
3. Á síðunni **Fjárhagsspjald** skal velja viðeigandi aðferð í reitnum **Gengisleiðrétting**.  

    Ef bókað er í AGM í reitnum **Gengisleiðrétting** skal tilgreina hvernig þessi fjárhagsreikningur er leiðréttur vegna gengissveiflna milli SGM og AGM. Eftirfarandi tafla lýsir valkostunum.  

    |Svæði|Heimildasamstæða|  
    |----------------------------------|---------------------------------------|  
    |**Engin leiðrétting**|Engin gengisleiðrétting er gerð í fjárhagsreikningnum. Þessi stilling er sjálfgefni valkosturinn.<br /><br /> **ATH:** Þessi kostur er valinn ef gengið milli SGM og AGM er alltaf fast.|  
    |**Leiðrétta upphæð**|SGM-upphæðin er leiðrétt samkvæmt öllum gengishagnaði eða tapi. Gengishagnaður eða gengistap er bókað á fjárhagsreikninginn í reitinn **Upphæð** og á þá reikninga sem voru tilgreindir fyrir hagnað eða tap í reitunum **Reikningur orðins fjárh. hagnaðar** og **Reikningur orðins fjárh. taps** á síðunni **Gjaldmiðlar**.|  
    |**Leiðrétta upphæð annars gjaldmiðils**|AGM er leiðrétt samkvæmt gengishagnaði eða -tapi. Gengishagnaður eða gengistap er bókað á fjárhagsreikninginn í reitinn **Upphæð annars gjaldmiðils** og á þá reikninga sem voru tilgreindir fyrir hagnað eða tap í reitunum **Reikningur orðins fjárh. hagnaðar** og **Reikningur orðins fjárh. taps** á síðunni **Gjaldmiðlar**.|  

    Gengishagnaður og gengistap er bókað þegar keyrslan **Leiðrétta gengi** er keyrð. Í þeirri keyrslu er leiðréttingargengið auðkennt á síðunni **Gengi gjaldmiðils** og síðan eru upphæðirnar í reitunum **Upphæð** og **Annar gjaldmiðill, upphæð** í fjárhagsfærslunni bornar saman til að ákvarða hvort um gengishagnað eða gengistap sé að ræða. Keyrslan notar valkostinn sem var valinn í reitnum **Gengisleiðrétting** til að ákvarða hvernig skuli reikna og bóka gengishagnað eða -tap fyrir fjárhagsreikninga.  

4.  Síðunni **Fjárhagsspjald** lokað.  

### Tilgreina aðferð fyrir gengisleiðréttingu í VSK-færslum

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning fjárhags** og velja síðan viðkomandi tengil.  
2. Á síðunni **Fjárhagsgrunnur** skal velja viðeigandi aðferð í reitnum **VSK-gengisleiðrétting**.  
3. Ef bókað er í AGM **er** hægt að tilgreina hvernig reikningarnir sem settir eru upp fyrir VSK-bókun á **síðunni VSK-bókunargrunnur** eru leiðréttir fyrir gengissveiflur milli SGM og AGM.  

    Þegar keyrslan **Leiðrétta gengi er keyrð** er leiðréttingargengið auðkennt á síðunni **Gengi** gjaldmiðils og síðan eru upphæðirnar í reitunum **Upphæð** og **Annar gjaldmiðill, upphæð** í VSK-færslunni bornar saman til að ákvarða hvort um gengishagnað eða gengistap sé að ræða. Keyrslan notar kostinn sem valinn var í þessum reit til að ákvarða hvernig eigi að bóka gengishagnað eða -tap vegna VSK-reikninga.  

    Sömu valkostir eru í boði og með fjárhagsfærslur en í þessu tilviki eru færslurnar sem eru leiðréttar VSK-færslurnar. Eftirfarandi tafla lýsir valkostunum.

    |Svæði|Heimildasamstæða|  
    |----------------------------------|---------------------------------------|  
    |**Engin leiðrétting**|Engin gengisleiðrétting er gerð í fjárhagsreikningnum. Þessi stilling er sjálfgefni valkosturinn.|  
    |**Leiðrétta upphæð**|SGM-upphæðin er leiðrétt samkvæmt öllum gengishagnaði eða tapi. Gengishagnaður eða gengistap er bókað á fjárhagsreikninginn í reitinn **Upphæð** og á þá reikninga sem voru tilgreindir fyrir hagnað eða tap í reitunum **Reikningur orðins fjárh. hagnaðar** og **Reikningur orðins fjárh. taps** á síðunni **Gjaldmiðlar**.|  
    |**Leiðrétta upphæð annars gjaldmiðils**|AGM er leiðrétt samkvæmt gengishagnaði eða -tapi. Gengishagnaður eða gengistap er bókað á fjárhagsreikninginn í reitinn **Upphæð annars gjaldmiðils** og á þá reikninga sem voru tilgreindir fyrir hagnað eða tap í reitunum **Reikningur orðins fjárh. hagnaðar** og **Reikningur orðins fjárh. taps** á síðunni **Gjaldmiðlar**.|  

### Til að virkja AGM  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning fjárhags** og velja síðan viðkomandi tengil.  
2. Á síðunni **Fjárhagsgrunnur**, í reitnum **Annar skýrslugjaldmiðill**, skal velja annan gjaldmiðil sem á að gefa skýrslu í.  
3. Þegar farið er úr reitnum [!INCLUDE[prod_short](includes/prod_short.md)]  birtast staðfestingarboð sem lýsa áhrifum þess að virkja AGM.  
4. Velja hnappinn **Já** til að staðfesta að virkja eigi gjaldmiðilinn.  
5. Keyrslan **Leiðrétta annan skýrslugjaldm.** opnast.

    Þessi keyrsla umreiknar upphæðir í SGM í færslum sem fyrir eru í SGM. Keyrslan notar sjálfgefið gengi sem er afritað úr því gengi sem er gilt á vinnudagsetningunni á síðunni **Gengi gjaldmiðils**. Afgangsupphæðir sem eiga sér stað við umbreytingu á SGM í AGM eru bókaðar á reikninga afgangs hagnaðar og taps sem tilgreindir eru á síðunni **Gjaldmiðlar** . Bókunardagsetningin og skjalanúmer þessara færslna eru þau sömu og í upphaflegu fjárhagsfærslunni. Þegar allar afgangsfærslur hafa verið bókaðar bókar keyrslan sléttunarfærslu á lokadagsetningu hvers lokaðs árs á reikning óinnleystra eigin fjár. Þessi bókun tryggir að lokastaða rekstrarreiknings hvers lokaðs árs sé 0 bæði í SGM og AGM.
6. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
7. Veldu hnappinn **Í lagi** til að ræsa keyrsluna.  

Þegar keyrslan hefur verið notuð eru upphæðir í eftirfarandi færslum bæði í SGM og AGM:  

- Fjárhagsfærslur  
- Birgðajöfnunarfærslur  
- VSK-færslur...  
- Verkfærslur  
- Virðisfærslur  
- Framleiðslupantanalínur  
- Fjárhagsfærslur framleiðslupöntunar  

Þar að auki hafa allar framtíðarfærslur sömu tegundar skráðar bæði í SGM og AGM.  

> [!NOTE]  
> Reiturinn **Annar skýrslugjaldmiðill** verður aðeins virkur eftir að valinn hefur verið hnappurinn **Í lagi** í keyrslunni **Leiðrétta annan skýrslugjaldmiðil**.  

## Sjá einnig .

[Uppfæra gengi](finance-how-update-currencies.md)  
[Lokaár og Tímabil](year-close-years-periods.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
