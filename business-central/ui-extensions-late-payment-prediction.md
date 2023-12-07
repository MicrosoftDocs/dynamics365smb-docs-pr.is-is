---
title: Spá fyrir um seinkun á greiðslu fyrir söluskjöl
description: Þessi grein útskýrir hvernig á að nota forspárlíkanið okkar til að spá fyrir um hvort reikningur verði greiddur á réttum tíma.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'customer, payment, invoice, sales, invoice, quote'
ms.search.form: '1950, 1951,'
ms.date: 12/06/2023
ms.custom: bap-template
---
# <a name="the-late-payment-prediction-extension"></a>Viðbót greiðsludráttarspár

Árangursrík stjórnun viðskiptakrafna er mikilvæg fyrir heildar fjárhagslega heilsu fyrirtækis. Til að draga úr útistandandi kröfum og hjálpa þér að fínstilla innheimtustefnu þína spáir framlengingin fyrir um hvort búast megi við síðbúnum greiðslum. Til dæmis, ef spá telur greiðsla vera sein, gætir þú ákveðið að lagfæra skilmála greiðslu eða greiðslumáta fyrir viðskiptamanninn.

## <a name="get-started"></a>Hefjast handa

Þegar þú opnar bókað söluskjal birtist tilkynning efst á síðunni. Til að nota síðari greiðsluframlengingu skaltu skrá þig með því að velja **Virkja** í tilkynningunni. Einnig er hægt að setja upp viðbótina handvirkt. Til dæmis, ef þú iðrast þess að hafna tilkynningunni.

Til að virkja viðbótina handvirkt skaltu fylgja þessum skrefum:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning á spám fyrir greiðsludrátt** og velja síðan viðkomandi tengil.  
2. Fyllið inn reitina eftir þörfum.

> [!NOTE]
> Ef ákveðið er að virkja viðbótina handvirkt skal hafa í huga að [!INCLUDE[prod_short](includes/prod_short.md)] leyfir þér ekki að gera það ef gæði líkansins eru léleg. Gæði líkansins gefur til kynna hversu nákvæmar spár líkansins eru líklegar til að verða. Nokkrir þættir geta haft áhrif á gæði líkansins. Til dæmis gæti verið að það hafi ekki verið nóg af gögnum eða það var ekki nægur breytileiki í gögnunum. Þú getur skoðað gæði líkansins sem þú ert að nota á síðunni **Uppsetning seint greiðslu** . Þú getur einnig tilgreint lágmarksþröskuld fyrir gæði líkansins.

## <a name="view-all-payment-predictions"></a>Skoðaðu allar greiðsluspár

Ef þú virkjar framlenginguna er **Payments Predicted to be Late** relísa tiltæk í **Business Manager** Hlutverkamiðstöðinni. Flíslan sýnir fjölda greiðslna sem spáð er að verði seint og gerir þér kleift að opna **Færslur viðskiptamanna**  þar sem þú getur grafið dýpra í bókaða reikninga. Það eru þrjár dálkar sem veita skal eftirtekt:  

* **Greiðsludráttur** - Gefur til kynna hvort dráttur verði á greiðslu reikningsins.
* **Áreiðanleiki spár** - Gefur til kynna hversu áreiðanlegt þú ættir að telja spánna vera. **Hátt** þýðir að spáin er að minnsta kosti 90% viss, **Meðal** er á milli 80% og 90% og **Low** er undir 80%.
* **Áreiðanleiki spár %** - Sýnir raunverulega prósentu á bak við áreiðanleikamatið. Sjálfgefið er að þessi dálkur er falinn en þú getur bætt honum við ef þú vilt. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

> [!TIP]
> Síðan Færslur viðskiptamannabókar sýnir staðreyndareit til hægri. Á meðan þú ert að skoða spár geta upplýsingarnar í **Upplýsingar um viðskiptavin**  verið gagnlegar. Þegar þú velur reikninginn í listanum birtir hlutinn upplýsingar um viðskiptamanninn. Það gerir þér jafnframt kleift að hefja aðgerðir strax. Ef viðskiptamaður setur til dæmis oft veskið sitt á rangan stað getur þú opnað viðskiptamannakortið frá Upplýsingakassanum og útilokað viðskiptamanninn frá framtíðarsölu.  

## <a name="design-details"></a>Hönnunarupplýsingar

Microsoft setur upp og rekur sjálfvirka vefþjónustu á öllum svæðum þar sem [!INCLUDE[prod_short](includes/prod_short.md)] er í boði. Aðgangur að þessum vefþjónustum er innifalinn í [!INCLUDE[prod_short](includes/prod_short.md)] áskriftinni. Frekari upplýsingar er að finna í Microsoft Dynamics 365 Business Central leyfishandbók. Leiðbeiningarnar eru í boði til niðurhals á vefsvæði [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Vefþjónustan virkar í þremur stillingum:

* Þjálfa líkan. Vefþjónustan þjálfar líkanið á grunni gagnamengis sem er útvegað.
* Leggja mat á líkan. Vefþjónustan athugar hvort líkanið skili áreiðanlegum gögnum fyrir uppgefið gagnamengi.
* Spá Vefþjónustan notar líkanið á uppgefið gagnamengi til að spá fyrir.

Þessar vefþjónustur eru óháðar fylkjum, sem þýðir að þær nota aðeins gögn til að reikna eftirspurnarspár. Þeir geyma ekki gögn.

> [!NOTE]  
> Einnig er hægt að nota eigin forspárþjónustu á netinu. Nánari upplýsingar er að finna í [Búa til og nota eigin forspárþjónustu á netinu fyrir spá um greiðsludrátt](#AnchorText).

### <a name="data-required-to-train-and-evaluate-the-model"></a>Gögn sem þarf til að þjálfa og meta líkanið

Fyrir hverja **Viðskiptamannafærslu** sem er með tengdan **Bókaðan sölureikning**:

* Upphæð (LCY) með skatti
* Greiðsluskilmálar í dögum eru reiknaðir sem **Gjalddagi** mínus **Bótunardagur**
* Hvort til sé beitt kreditnótu

Að auki hefur skráningin samanlögð gögn frá öðrum reikningum sem tengjast sama viðskiptavin.

- Heildarfjöldi og upphæðir á greiddum reikningum
- Heildarfjöldi og upphæðir á reikningum sem voru greiddir seint
- Heildarfjöldi og upphæðir á útistandandi reikningum
- Heildarfjöldi og upphæðir á útistandandi reikningum sem eru þegar seinkaðir
- Hversu mörgum dögum of seint að meðaltali
- Hlutfall: Fjöldi greiddra seint/greiddra reikninga
- Hlutfall: Upphæð greidd seint/greiddir reikningar
- Hlutfall: Fjöldi útistandandi seint/útfallandi reikninga
- Hlutfall: Fjárhæðir á vanskilum seint/útfallandi reikninga

> [!NOTE]
> Upplýsingarnar um viðskiptavininn eru ekki með í gagnasafninu.

### <a name="standard-model-and-my-model"></a>Staðlað líkan og Líkanið mitt

Forspárlíkan Late Payment Prediction viðbótarinnar er þjálfað á gögnum sem tákna fjölda lítilla og meðalstórra fyrirtækja. Þegar þú byrjar að bóka reikninga og taka á móti greiðslum, metur [!INCLUDE[prod_short](includes/prod_short.md)]  hvort staðlaða líkanið passi þitt viðskiptaflæði.

Ef ferlar þínir passa ekki við staðlaða líkanið geturðu notað viðbótina, en þú þarft að fá meiri gögn. Haltu bara áfram að nota [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Við notum smá af reikningstíma þínum í hverri viku þegar við metum og endurþjálfum líkanið.

[!INCLUDE[prod_short](includes/prod_short.md)] rekur þjálfun og mat sjálfkrafa þegar nægir greiddir og seinkaðir reikningar liggja fyrir. Hins vegar geturðu keyrt það handvirkt hvenær sem þú vilt.

#### <a name="to-train-and-use-your-model"></a>Að þjálfa og nota líkanið

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning á spám fyrir greiðsludrátt** og velja síðan viðkomandi tengil.  
2. Í **Valið líkan** reitinn, veldu **Mitt líkan**.
3. Veldu aðgerðina **Búa til líkanið mitt** til að þjálfa líkan í gögnunum þínum.  

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-late-payment-prediction"></a><a name="AnchorText"> </a>Búa til og nota eigin greiðsludráttarspá á netinu til að spá fyrir um greiðsludrátt

Þú getur einnig búið til þína eigin spáþjónustu á netinu sem byggir á almennu líkani sem heitir **Forspártilraun fyrir Dynamics 365 Business Central**. Þetta líkan er aðgengilegt á netinu í Azure AI. Fylgið eftirfarandi skrefum til að fá aðgang að reitunum:  

1. Opnaðu vafra og farðu á [Azure AI Gallery](https://go.microsoft.com/fwlink/?linkid=2086310).  
2. Leitaðu að **Spátilraun fyrir Dynamics 365 Business Central** og opnaðu síðan líkanið í Azure Machine Learning stúdíó.  
3. Nota á reikninginn í Microsoft að undirrita fyrir workspace er og afrita síðan líkaninu sem.  
4. Keyrslan líkaninu og út og þjónustu veftengingar.  
5. Gera API URL og API lykillinn athugasemd. Þú munt nota þessi skilríki fyrir sjóðstreymisuppsetningu.  
6. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning á spám fyrir greiðsludrátt** og velja síðan viðkomandi tengil.  
7. Veldu **Nota Azure-áskriftina mína** gátreitinn.
8. Í **Innskráningarupplýsingar fyrir líkanið mitt** flýtiflipanum, sláðu inn API slóðina og API lykil fyrir líkanið.  

## <a name="see-also"></a>Sjá einnig .

[Azure Machine Learning stúdíó skjöl](/azure/machine-learning/classic/)  
[Sérstilling Business Central með viðbótum](ui-extensions.md)  
[Velkomin til [!INCLUDE[prod_long](includes/prod_long.md)]](welcome.md)  
[Nota gervigreind í Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
