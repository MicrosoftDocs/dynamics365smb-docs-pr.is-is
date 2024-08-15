---
title: Spá fyrir um seingreiðslur fyrir söluskjöl
description: Þessi grein útskýrir hvernig á að nota fyrirsjáanlegt líkan okkar til að spá fyrir um hvort viðskiptamaður muni borga reikning á réttum tíma.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'customer, payment, invoice, sales, invoice, quote'
ms.search.form: '1950, 1951,'
ms.date: 07/11/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Framlenging á spá um síðbúna greiðslu

Árangursrík stjórnun viðskiptakrafna er mikilvæg fyrir heildar fjárhagslega heilsu fyrirtækis. Til að draga úr útistandandi útistandandi skuldum og hjálpa þér að fínstilla innheimtuáætlun þína spáir viðbótin um hvort búast megi við seingreiðslum. Til dæmis, ef spá telur greiðsla vera sein, gætir þú ákveðið að lagfæra skilmála greiðslu eða greiðslumáta fyrir viðskiptamanninn.

## Hefjast handa

Þegar bókað söluskjal er opnað birtist tilkynning efst á síðunni. Til að nota viðbót við síðbúna greiðsluspá, skal velja Gera virkt **í** tilkynningunni. Einnig er hægt að setja upp viðbótina handvirkt. Til dæmis, ef þú iðrast þess að hafna tilkynningunni.

Til að virkja viðbótina handvirkt skaltu fylgja þessum skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning á spám fyrir greiðsludrátt** og velja síðan viðkomandi tengil.  
2. Fyllið inn reitina eftir þörfum.

> [!NOTE]
> Ef ákveðið er að virkja viðbótina handvirkt skal hafa í huga að [!INCLUDE[prod_short](includes/prod_short.md)] leyfir þér ekki að gera það ef gæði líkansins eru léleg. Gæði líkansins gefur til kynna hversu nákvæmar spár líkansins eru líklegar til að verða. Nokkrir þættir geta haft áhrif á gæði líkansins. Til dæmis gæti hafa nægileg gögn verið nægileg eða ekki var nægilegt tilbrigði við gögnin. Hægt er að skoða gæði líkansins sem þú notar á síðunni Uppsetning **síðbúinnar** greiðsluspár. Þú getur einnig tilgreint lágmarksþröskuld fyrir gæði líkansins.

## Skoða allar greiðsluspár

Ef viðbótin **er gerð virk eru greiðslur sem spáð er að séu Seint** tiltækar í **Mitt hlutverk viðskiptastjóra** . Reiturinn sýnir fjölda greiðslna sem spáð er að verði of seint og gerir kleift að opna **síðuna Viðskm.færslur** þar sem hægt er að grafa dýpra í bókaða reikninga. Það eru þrjár dálkar sem veita skal eftirtekt:  

* **Greiðsludráttur** - Gefur til kynna hvort dráttur verði á greiðslu reikningsins.
* **Áreiðanleiki spár** - Gefur til kynna hversu áreiðanlegt þú ættir að telja spánna vera. **Mikil** merkir að spáin er að minnsta kosti 90% viss,Miðlungs **er á bilinu** 80% til 90% og **lítill** er undir 80%.
* **Áreiðanleiki spár %** - Sýnir raunverulega prósentu á bak við áreiðanleikamatið. Sjálfgefið er að þessi dálkur sé falinn en hægt er að bæta honum við ef þess er óskað. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

> [!TIP]
> Síðan Viðskm.færslur sýnir upplýsingakassa. Þó að þú sért að fara yfir spár geta upplýsingarnar í hlutanum **Upplýsingar um viðskiptamenn verið gagnlegar** . Þegar þú velur reikninginn í listanum birtir hlutinn upplýsingar um viðskiptamanninn. Það gerir þér jafnframt kleift að hefja aðgerðir strax. Ef viðskiptamaður setur til dæmis oft veskið sitt á rangan stað getur þú opnað viðskiptamannakortið frá Upplýsingakassanum og útilokað viðskiptamanninn frá framtíðarsölu.  

## Hönnunarupplýsingar

Microsoft notar og notar fyrirsjáanlega vefþjónustu á öllum svæðum þar sem [!INCLUDE[prod_short](includes/prod_short.md)] er í boði. Aðgangur að þessum vefþjónustum er innifalinn í [!INCLUDE[prod_short](includes/prod_short.md)] áskriftinni. Frekari upplýsingar er að finna í Microsoft Dynamics 365 Business Central leyfishandbók. Leiðbeiningarnar eru í boði til niðurhals á vefsvæði [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Vefþjónustan vinnur í þremur stillingum:

* Þjálfa líkan. Vefþjónustan þjálfar líkanið á grunni gagnamengis sem er útvegað.
* Leggja mat á líkan. Vefþjónustan athugar hvort líkanið skili áreiðanlegum gögnum fyrir uppgefið gagnamengi.
* Spá Vefþjónustan notar líkanið á uppgefið gagnamengi til að spá fyrir.

Þessar vefþjónustur eru óháðar fylkjum, sem þýðir að þær nota aðeins gögn til að reikna eftirspurnarspár. Þau geyma ekki gögn.

> [!NOTE]  
> Einnig er hægt að nota eigin forspárþjónustu á netinu. Nánari upplýsingar er að finna í [Búa til og nota eigin forspárþjónustu á netinu fyrir spá um greiðsludrátt](#AnchorText).

### Gögn sem þarf til að þjálfa og meta líkanið

Fyrir hverja **Viðskiptamannafærslu** sem er með tengdan **Bókaðan sölureikning**:

* Upphæð í staðbundinn gjaldmiðill, með skatti
* Greiðsluskilmálar í dögum eru reiknaðir sem **Gjalddagi** mínus **bókunardagur**
* Hvort um er að ræða jafnaðan kreditreikning

Auk þess hefur færslan samanlagt gögn frá öðrum reikningum sem tengjast sama viðskiptamanni.

- Heildarfjöldi og upphæðir á greiddum reikningum
- Heildarfjöldi og upphæðir á reikningum sem voru greiddar seint
- Heildarfjöldi og upphæðir á útistandandi reikningum
- Heildarfjöldi og upphæðir á útistandandi reikningum sem þegar eru of sein
- Hversu mörgum dögum of seint að meðaltali
- Hlutfall: Fjöldi greiddra reikninga síðbúinna/greiddra reikninga
- Hlutfall: Upphæð greiddra síðbúinna/greiddra reikninga
- Hlutfall: Fjöldi útistandandi reikninga síðbúinna/útistandandi reikninga
- Hlutfall: Upphæðir á útistandandi síðbúnum/útistandandi reikningum

> [!NOTE]
> Upplýsingarnar um viðskiptamanninn eru ekki í gagnasafninu.

### Staðlað líkan og Líkanið mitt

Fyrirsjáanlegt líkan síðbúinnar greiðsluspár er þjálfað í gögnum sem tákna svið lítilla fyrirtækja í meðalstórum fyrirtækjum. Þegar byrjað er að bóka reikninga og taka á móti greiðslum er [!INCLUDE[prod_short](includes/prod_short.md)]  metið hvort staðlaða líkanið passi við viðskiptaflæðið.

Ef ferlin passa ekki við staðlaða líkanið er hægt að nota viðbótina en fá þarf fleiri gögn. Haltu bara áfram að nota [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Við notum smá af reikningstíma þínum í hverri viku þegar við metum og endurþjálfum líkanið.

[!INCLUDE[prod_short](includes/prod_short.md)] keyrir þjálfun og mat sjálfkrafa þegar nægir greiddir og síðbúnir reikningar eru tiltækir. Hins vegar er hægt að keyra hana handvirkt þegar óskað er.

#### Að þjálfa og nota líkanið

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning á spám fyrir greiðsludrátt** og velja síðan viðkomandi tengil.  
2. Í **Valið líkan** reitinn, veldu **Mitt líkan**.
3. Veldu aðgerðina **Búa til líkanið mitt** til að þjálfa líkan í gögnunum þínum.  

## <a name="AnchorText"> </a>Búa til og nota eigin greiðsludráttarspá á netinu til að spá fyrir um greiðsludrátt

Fyrir [!INCLUDE[prod_short](includes/prod_short.md)] netið er líkanið gefið út af Microsoft og tengt við Microsoft-áskriftina. Fyrir aðra virkjunarkosti þarf að búa til vélarnámsforða í eigin Azure áskrift. Hægt er að finna sýniskref í [sýnishorninu](https://github.com/microsoft/BCTech/tree/master/samples/MachineLearning). Tilgangur þessa verks er að fá API-URI og API-lykil.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning á spám fyrir greiðsludrátt** og velja síðan viðkomandi tengil.  
2. Veldu **Nota Azure-áskriftina mína** gátreitinn.
3. Á flýtiflipanum **Nota Azure-áskrift** mína skal slá inn API-URL og API lykil fyrir líkanið.  

## Sjá einnig .

[Sérstilling Business Central með viðbótum](ui-extensions.md)    
[Velkomin í [!INCLUDE[prod_long](includes/prod_long.md)]](welcome.md)    
[Nota gervigreind í Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)    
[Yfirlit spár-API](/dynamics365/business-central/dev-itpro/developer/ml-prediction-api-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
