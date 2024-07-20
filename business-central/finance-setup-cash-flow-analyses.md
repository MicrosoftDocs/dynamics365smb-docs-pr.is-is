---
title: Uppsetning sjóðstreymisgreiningar
description: 'Nota gröf reikninga í Mínu hlutverki til að greina sjóðstreymi í fyrirtækinu, þar á meðal útgjöld og tekjur, greiðslugetu og inngreiðslur mínus staðgreiðslur.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds'
ms.search.form: '846, 847, 849, 851, 855, 862, 869, 1818'
ms.date: 07/01/2024
ms.service: dynamics-365-business-central
---
# Uppsetning sjóðstreymisgreiningar

Ef þú vilt fá aðstoð til að ákveða hvað þú átt að gera með féð þitt, skoðaðu töflurnar á Hlutverkamiðstöð bókhaldara:

* **ferill bundins reiðufés**  
* **Tekjur og útgjöld**  
* **Sjóðstreymi**  
* **Sjóðstreymispár**  

Þessi grein lýsir hvar gögnin í töflunum koma frá og, ef nauðsyn krefur, hvað á að gera til að byrja að nota töflurnar.
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mJhc?rel=0]

## Gröf ferils bundins reiðufés og tekjur og útgjöld

Gröfin **Ferill reiðufjár** og **Tekjur og útgjöld** eru tilbúin til notkunar, byggt á bókhaldslyklum og fjárhagsskýrslu. Lyklarnir eru þar sem gögnin koma frá og fjárhagsskýrslur reikna út tengslin milli sölu og útistandandi. Sumir lyklar og fjárhagsskýrslur eru gefin upp. Þú getur notað þau eins og-er, breytt þeim og bætt við nýjum. Ef fjárhagsreikningum er bætt við bókhaldslykilinn, til dæmis með því að flytja þá inn úr Flýtibókum, er reikningunum varpað á **síðuna Fjárhagsskýrslur** fyrir eftirfarandi skýrslur:

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

## Setja upp sjóðstreymirit

Graf sjóðstreymis byggir á:  

* Myndrit sjóðstreymisreikninga.
* Eina eða fleiri uppsetningar í Uppsetning sjóðstreymis. Þessi uppsetning tilgreinir reikningana sem nota skal fyrir aðalbókina, kaupin, sölu, þjónustu og eignir.  

Til að hjálpa þér að fara,veitir [!INCLUDE [prod_short](includes/prod_short.md)]  nokkra reikninga og uppsetningu sjóðstreymis. Þú getur bætt við, breytt eða fjarlægt þau.  

Til að setja upp lykla skal leita að **Graf yfir sjóðstreymisreikninga**, velja tengilinn og fylla síðan inn reitina. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Endurtekur skrefin fyrir **Uppsetning sjóðstreymis**.

## Uppsetning sjóðsstreymisspáa

**Sjóðstreymisspá** notar sjóðstreymisreikninga, sjóðstreymisskipulag og sjóðstreymisspár. Sumir eru til staðar, en þú getur sett upp þitt eigið með því að nota aðstoðarmaður uppsetningarleiðbeiningar. Leiðsögumaðurinn hjálpar til við að tilgreina hluti eins og:

* Hvenær á að uppfæra spána
* Á hvaða reikninga á að byggja hana á
* Þegar skattar eru greiddir
* Hvort kveikja eigi á [Azure AI](https://azure.microsoft.com/overview/ai-platform/).  

Sjóðstreymisspár geta notað Azure-gervigreind til að búa til umfangsmeiri spá. Tengingin við Azure AI er þegar sett upp fyrir þig. Þú þarft bara að kveikja á því. Þegar þú skráir þig inn á [!INCLUDE[prod_short](includes/prod_short.md)] birtist tilkynning á bláum reit og veitir hlekkur til sjálfgefna sjóðstreymisuppsetningar. Tilkynningin birtist aðeins einu sinni. Ef henni er lokað, en síðan er ákveðið að kveikja á Azure AI er hægt að nota leiðsagnarforritið leiðsagnarforrit með aðstoð eða handvirku ferli.  

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

## Hönnunarupplýsingar

Áskriftum að [!INCLUDE[prod_short](includes/prod_short.md)] fylgir aðgangur að nokkrum forspárþjónustum á netinu á öllum stöðum þar sem [!INCLUDE[prod_short](includes/prod_short.md)] er í boði. Frekari upplýsingar er að finna í leyfishandbók Microsoft Dynamics 365 Business Central. Leiðbeiningarnar eru í boði til niðurhals á vefsvæði [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Þessar vefþjónustur eru óháðar fylkjum, sem þýðir að þær nota aðeins gögn til að reikna eftirspurnarspár. Þau geyma ekki gögn.

> [!NOTE]
>
> Einnig er hægt að nota eigin forspárþjónustu á netinu. Nánari upplýsingar er að finna í [Búa til og nota eigin fyrirsjáanlega vefþjónustu fyrir sjóðstreymisspár](#AnchorText).

### Gögn eru nauðsynleg fyrir forspá

Til að spá fyrir um tekjur og útgjöld í framtíðinni þurfa vefþjónustur á eldri gögnum að halda frá útistandandi, viðskiptaskuldum og sköttum.

#### Viðskiptakröfur

Reitirnir **Gjalddagi**, **Upphæð (SGM)** síðunnar **Færslur í viðskiptamannabók**, þar sem:

* Tegund skjals er *reikningur* eða *kreditreikningur*.
* Gjalddagi er á milli dagsetningar sem er reiknuð út frá gildunum í reitunum **Eldri tímabil** og **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis** og vinnudagsetningarinnar.

Áður en hún notar fyrirsjáanlega vefþjónustu þjappar [!INCLUDE[prod_short](includes/prod_short.md)]  hún færslum eftir **Gjalddaga** samkvæmt gildinu í reitnum **Tegund** tímabils á síðunni **Uppsetning sjóðstreymis** .

#### Viðskiptaskuldir

Reitirnir **Gjalddagi**, **Upphæð (SGM)** á síðunni **Lánardrottnafærslur**, þar sem:

* Tegund skjals er *reikningur* eða *kreditreikningur*.
* Gjalddagi er á milli dagsetningar sem er reiknuð út frá gildum í reitunum **Eldri tímabil** og **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis** og vinnudagsetningarinnar.

Áður en hún notar fyrirsjáanlega vefþjónustu þjappar [!INCLUDE[prod_short](includes/prod_short.md)]  hún færslum eftir **Gjalddaga** samkvæmt gildinu í reitnum **Tegund** tímabils á síðunni **Uppsetning sjóðstreymis** .

#### Skattur

Reitirnir **Dagsetning skjals**, **Upphæð** á síðunni **Fjárhagsfærslur VSK (skatts)**, þar sem:

* Tegund skjals er *sala*.
* Dagsetning skjals er á milli dagsetningar sem er reiknuð út frá gildum í reitunum **Eldri tímabil** og **Tímabilsgerð** á síðunni **Uppsetning sjóðstreymis** og vinnudagsetningarinnar.

Áður en hún notar fyrirsjáanlega vefþjónustu þjappar [!INCLUDE[prod_short](includes/prod_short.md)]  hún færslum eftir **Dagsetning** fylgiskjals eftir gildinu í reitnum **Tegund** tímabils á síðunni **Uppsetning sjóðstreymis** .

## <a name="AnchorText"></a>Búa til og nota eigin fyrirsjáanlega vefþjónustu fyrir sjóðstreymisspár

Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] netið er líkanið gefið út af Microsoft og tengt við Microsoft-áskriftina. Fyrir aðra virkjunarkosti þarf að búa til vélarnámsforða í eigin Azure áskrift. Hægt er að finna sýniskref í [sýnishorninu](https://github.com/microsoft/BCTech/tree/master/samples/MachineLearning). Tilgangur þessa verks er að fá API-URI og API-lykil.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sjóðstreymis** og velja síðan viðkomandi tengil.  
2. Stækkaðu flýtiflipann **Azure AI** og fylltu síðan út reitina, þar á meðal API-vefslóðina og API-lykilinn sem kemur úr stúdíói Azure-vélnáms. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Í Hlutverkamiðstöð endurskoðanda skal velja aðgerðina **Endurreikna spá** undir grafinu **Sjóðstreymisspá**.

## Sjá einnig .

[Greining á sjóðstreymi í fyrirtækinu þínu](finance-analyze-cash-flow.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Yfirlit yfir API spár](/dynamics365/business-central/dev-itpro/developer/ml-forecasting-api-overview)

[!INCLUDE[footer-include](includes/footer-banner.md)]
