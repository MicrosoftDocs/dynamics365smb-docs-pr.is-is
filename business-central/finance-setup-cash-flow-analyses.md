---
title: Setja upp sjóðstreymisgreiningu (inniheldur myndskeið)
description: 'Nota gröf reikninga í Mínu hlutverki til að greina sjóðstreymi í fyrirtækinu, þar á meðal útgjöld og tekjur, greiðslugetu og inngreiðslur mínus staðgreiðslur.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds'
ms.search.form: '846, 847, 849, 851, 855, 862, 869, 1818'
ms.date: 08/23/2022
ms.author: bholtorf
---
# <a name="setting-up-cash-flow-analysis"></a>Setja upp sjóðstreymisgreiningu

Ef þú vilt fá aðstoð til að ákveða hvað þú átt að gera með féð þitt, skoðaðu töflurnar á Hlutverkamiðstöð bókhaldara:

* **ferill bundins reiðufés**  
* **Tekjur og útgjöld**  
* **Sjóðstreymi**  
* **Sjóðstreymispár**  

Þessi grein lýsir hvar gögnin í töflunum koma frá og, ef nauðsyn krefur, hvað á að gera til að byrja að nota töflurnar.
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mJhc?rel=0]

## <a name="the-cash-cycle-and-income--expense-charts"></a>Gröf ferils bundins reiðufés og tekjur og útgjöld

Gröfin **Ferill reiðufjár** og **Tekjur og útgjöld** eru tilbúin til notkunar, byggt á bókhaldslyklum og fjárhagsskýrslu. Lyklarnir eru þar sem gögnin koma frá og fjárhagsskýrslur reikna út tengslin milli sölu og útistandandi. Sumir lyklar og fjárhagsskýrslur eru gefin upp. Þú getur notað þau eins og-er, breytt þeim og bætt við nýjum. Ef þú bætir fjárhagsreikningum við bókhaldslykil, til dæmis með því að flytja þá úr QuickBooks þarftu að varpa lyklunum á síðuna **Fjárhagsskýrslur** fyrir eftirfarandi skýrslur:

| Heiti fjárhagsskýrslu | Þar sem það er notað |
| --- | --- |
| **I_CACYCLE** |Ferill bundins reiðufés |
| **I_CASHFLOW** |Sjóðstreymi |
| **I_INCEXP** |Tekjur og útgjöld |
| **I_MINTRIAL** |Sem rekstrarreikningur ef þú notar ekki bókhaldslykilinn |

> [!NOTE]
> Það er góð hugmynd að geyma útreikninga sem eru gefnir upp fyrir fjárhagsskýrsluna.

Sláðu inn reikninga í reitinn **Samtals** fyrir **Heildartekjur**, **Samtala viðskiptakrafna**, **Samtala viðskiptaskulda** og **Samtals birgðir**. Til að varpa á lyklabil skal færa inn lykilnúmerin aðskilin með „..“ eins og í **1111..4444**. Til að varpa í tiltekna lykla skal færa inn lykilnúmerin aðskilin með lóðréttu striki eins og í **2222|3333|5555**.  

> [!TIP] 
> Staðfestu kortlagninguna þína með því að velja **Yfirlit** aðgerðina.  

## <a name="set-up-the-cash-flow-chart"></a>Setja upp sjóðstreymirit

Graf sjóðstreymis byggir á:  

* Myndrit sjóðstreymisreikninga.
* Eina eða fleiri uppsetningar í Uppsetning sjóðstreymis. Þessi uppsetning tilgreinir reikningana sem nota skal fyrir aðalbókina, kaupin, sölu, þjónustu og eignir.  

Til að hjálpa þér að komast, eru nokkrar reikningar og sjóðstreymisstillingar veittar. Þú getur bætt við, breytt eða fjarlægt þau.  

Til að setja upp lykla skal leita að **Graf yfir sjóðstreymisreikninga**, velja tengilinn og fylla síðan inn reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Endurtekur skrefin fyrir **Uppsetning sjóðstreymis**.

## <a name="set-up-cash-flow-forecasts"></a>Uppsetning sjóðsstreymisspáa

**Sjóðstreymisspá** notar sjóðstreymisreikninga, sjóðstreymisskipulag og sjóðstreymisspár. Sumir eru til staðar, en þú getur sett upp þitt eigið með því að nota aðstoðarmaður uppsetningarleiðbeiningar. Leiðbeiningarnar hjálpar til við að tilgreina atriði hversu oft eigi að uppfæra spá, reikningar til að byggja á, upplýsingar um þegar greiða skatta og hvort kveikja eigi á [Azure AI](https://azure.microsoft.com/overview/ai-platform/).  

Sjóðstreymisspár geta notað Azure-gervigreind til að búa til umfangsmeiri spá. Tengingin við Azure AI er þegar sett upp fyrir þig. Þú þarft bara að kveikja á því. Þegar þú skráir þig inn á [!INCLUDE[prod_short](includes/prod_short.md)] birtist tilkynning á bláum reit og veitir hlekkur til sjálfgefna sjóðstreymisuppsetningar. Tilkynningin birtist aðeins einu sinni. Ef þú lokar henni, en ákveður að kveikja á Azure-gervigreind, getur þú notað uppsetningu með hjálp eða handvirkt ferli.  

> [!NOTE]
>
> Að öðrum kosti er hægt að nota eigin fyrirsjáanlega vefþjónustu. Nánari upplýsingar er að finna í [Búa til og nota eigin fyrirsjáanlega vefþjónustu fyrir sjóðstreymisspár](#AnchorText).  

Uppsetning assisted leiðbeiningum nota til:  

1. Í Hlutverkamiðstöð bókhaldara undir **Sjóðstreymisspá** skal velja **Opna uppsetningu með hjálp** aðgerðina.
2. Fylltu út reitina í hverju skrefi leiðarvísisins. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Til baka í hlutverkamiðstöð endurskoðanda skal velja aðgerðina **Endurreikna spá** undir grafinu **Sjóðstreymisspá**.

Nota handvirkt ferli:  

1. Í hlutverkamiðstöð endurskoðanda skal velja ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sjóðstreymis**, velja síðan viðkomandi tengil.
2. Stækkaðu flýtiflipann **Azure AI** og veldu reitinn **Kveikt á Azure AI**.
3. Til baka í hlutverkamiðstöð endurskoðanda skal velja aðgerðina **Endurreikna spá** undir grafinu **Sjóðstreymisspá**.

> [!TIP]  
> Íhugaðu lengd tímabila sem þjónustan er notaður í útreikningum hennar. Frekari gögn sem veita verður því nákvæmari á predictions. Líka watch út fyrir mikið frávik í tímabil. Þeir eru einnig hefur predictions. Ef Azure AI finnur ekki næg gögn eða gögnin breytast við lotu mun þjónustan ekki framkvæma forspá.  

## <a name="design-details"></a>Hönnunarupplýsingar

Áskriftum að [!INCLUDE[prod_short](includes/prod_short.md)] fylgir aðgangur að nokkrum forspárþjónustum á netinu á öllum stöðum þar sem [!INCLUDE[prod_short](includes/prod_short.md)] er í boði. Frekari upplýsingar er að finna í leyfishandbók Microsoft Dynamics 365 Business Central. Leiðbeiningarnar eru í boði til niðurhals á vefsvæði [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Þessar vefþjónustur eru óháðar fylkjum, sem þýðir að þær nota aðeins gögn til að reikna eftirspurnarspár. Þær vita ekki gögn.

> [!NOTE]
>
> Einnig er hægt að nota eigin forspárþjónustu á netinu. Nánari upplýsingar er að finna í [Búa til og nota eigin fyrirsjáanlega vefþjónustu fyrir sjóðstreymisspár](#AnchorText).

### <a name="data-required-for-forecast"></a>Gögn eru nauðsynleg fyrir forspá

Til að spá fyrir um tekjur og útgjöld í framtíðinni þurfa vefþjónustur á eldri gögnum að halda frá útistandandi, viðskiptaskuldum og sköttum.

#### <a name="receivables"></a>Viðskiptakröfur

Reitirnir **Gjalddagi**, **Upphæð (SGM)** síðunnar **Færslur í viðskiptamannabók**, þar sem:

* Tegund skjals er *reikningur* eða *kreditreikningur*.
* Gjalddagi er á milli dagsetningar sem er reiknuð út frá gildunum í reitunum **Eldri tímabil** og **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis** og vinnudagsetningarinnar.

Áður en forspárþjónusta á netinu er notuð þjappar [!INCLUDE[prod_short](includes/prod_short.md)] færslum eftir **Gjalddaga** út frá gildinu í reitnum **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis**.

#### <a name="payables"></a>Viðskiptaskuldir

Reitirnir **Gjalddagi**, **Upphæð (SGM)** á síðunni **Lánardrottnafærslur**, þar sem:

* Tegund skjals er *reikningur* eða *kreditreikningur*.
* Gjalddagi er á milli dagsetningar sem er reiknuð út frá gildum í reitunum **Eldri tímabil** og **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis** og vinnudagsetningarinnar.

Áður en forspárþjónusta á netinu er notuð þjappar [!INCLUDE[prod_short](includes/prod_short.md)] færslum eftir **Gjalddaga** út frá gildinu í reitnum **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis**.

#### <a name="tax"></a>Skattur

Reitirnir **Dagsetning skjals**, **Upphæð** á síðunni **Fjárhagsfærslur VSK (skatts)**, þar sem:

* Tegund skjals er *sala*.
* Dagsetning skjals er á milli dagsetningar sem er reiknuð út frá gildum í reitunum **Eldri tímabil** og **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis** og vinnudagsetningarinnar.

Áður en forspárþjónusta á netinu er notuð þjappar [!INCLUDE[prod_short](includes/prod_short.md)] færslum eftir **Dagsetning skjals** út frá gildinu í reitnum **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis**.

## <a name="create-and-use-your-own-predictive-web-service-for-cash-flow-forecasts"></a><a name="AnchorText"></a>Búa til og nota eigin fyrirsjáanlega vefþjónustu fyrir sjóðstreymisspár

Þú getur einnig búið til þína eigin fyrirsjáanlega vefþjónustu byggt á opinberu líkani sem heitir **Spárlíkan fyrir Microsoft Business Central**. Þetta líkan er aðgengilegt á netinu í Azure AI. Fylgið eftirfarandi skrefum til að fá aðgang að reitunum:  

1. Opnaðu vafra og farðu á [Azure AI Gallery](https://go.microsoft.com/fwlink/?linkid=828352).  
2. Leita að **Forspármódel fyrir Microsoft Business Central** og opna svo líkanið í Microsoft Azure Machine Learning Studio.  
3. Nota á reikninginn í Microsoft að undirrita fyrir workspace er og afrita síðan líkaninu sem.  
4. Keyrslan líkaninu og út og þjónustu veftengingar.  
5. Gera API URL og API lykillinn athugasemd. Þú munt nota þessi skilríki fyrir sjóðstreymisuppsetningu.  
6. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sjóðstreymis** og velja síðan viðkomandi tengil.  
7. Stækkaðu flýtiflipann **Azure AI** og fylltu síðan út reitina, þar á meðal API-vefslóðina og API-lykilinn sem kemur úr stúdíói Azure-vélnáms. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
8. Í Hlutverkamiðstöð endurskoðanda skal velja aðgerðina **Endurreikna spá** undir grafinu **Sjóðstreymisspá**.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/forecast-cash-flow-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig .

[Greining á sjóðstreymi í fyrirtækinu þínu](finance-analyze-cash-flow.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
