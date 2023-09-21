---
title: Greina raunverulegar og áætlaðar upphæðir
description: 'Þessi grein lýsir því hvernig eigi að greina raunverulegar upphæðir samanborið við upphæðir fjárhagsáætlunar sem leið til að safna, greina og deila gögnum fyrirtækisins.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '120, 121, 422'
ms.date: 09/14/2022
ms.author: bholtorf
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Greina raunverulegar og áætlaðar upphæðir

Hluti af því að safna saman, greina og deila upplýsingum fyrirtækis, er að skoða raunverulegar upphæðir í samanburði við áætlaðar upphæðir fyrir alla reikninga og nokkur tímabil.

Til að greina áætlaðar upphæðir verður þú fyrst að búa til almennar fjárhagsáætlanir. Frekari upplýsingar eru á [Stofna fjárhagsáætluanir](finance-how-create-budgets.md).

## <a name="view-a-gl-budget"></a>Skoða fjárhagsáætlun

Í áætlun með víddum er hægt að setja afmarkanir á færslurnar og sjá tilteknar áætlanir.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagsáætlanir**, velja síðan viðkomandi tengil.
2. Á síðunni **Fjárhagsáætlanir** skal opna fjárhagsáætlunina sem á að skoða.  
3. Efst á síðunni skal fylla inn í reitina eins og þörf krefur, til að skilgreina hvað birtist. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Ef valið var **Tímabil** annaðhvort í reitnum **Sýna sem línur** eða **Sýna sem dálka** þarf að fylla út reitinn **Skoða eftir**. Ef ekki hefur verið valið **Tímabil** í öðrum hvorum þessara reita skal slá inn viðeigandi tímabil í reitinn **Dagsetningarsía**.  

> [!NOTE]  
> Aðeins færslur úr fjárhagsáætlun með afmörkunarkóðum sem færðir eru inn á flýtiflipanum **Afmarkanir** eru teknar með í útreikninginn. Fjárhagsáætlunarfærslur án eða með öðrum síukóðum eru ekki teknar með. Á meðan afmörkunin er á síðunni sýnir fjárhagsáætlunin aðeins færslur með þessum síukóðum.  

> [!TIP]  
> Notaðu aðgerðina **Breyta fjárhagsáætlun** til að breyta henni. Á síðu fjárhagsáætlunar skal velja upphæð til að skoða undirliggjandi færslur fjárhagsáætlunarskýrslu.

## <a name="view-actual-and-budgeted-amounts-for-all-accounts"></a>Skoða raunverulegar og áætlaðar upphæðir fyrir alla reikninga

Hægt er að skoða fjárhagsáætlanir og bera þær saman við raunverulegar upphæðir í mörgum svæðum í [!INCLUDE[prod_short](includes/prod_short.md)].

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill**, velja síðan viðkomandi tengil.  
2. Á síðunni **Bókhaldslykill**, skal velja aðgerðina **Fjárhagur staða/áætlun**.
3. Í flýtiflipanum **Valkostir** skal fylla út reitina eins og þarf til að skilgreina hvað er sýnt í töflunni.  
4. Farðu með bendilinn yfir reit í töflunni til að lesa stutta lýsingu um birta upphæð.

> [!NOTE]  
> Afmarkanir sem stilltar eru á síðuhausnum verða notaðar á bæði fjárhag og fjárhagsáætlunarfærslur.

Bókhaldslykillinn er í dálkunum til vinstri. Af dálkunum fimm lengst til hægri sýna fjórir þeir fyrstu raunverulegar og áætlaðar debet- og kreditfærslur á hverjum reikningi. Fimmti dálkurinn sýnir hlutfallsleg tengsl raunverulegra og áætlaðra upphæða á fjárhagsreikningnum.  

> [!TIP]  
> Reiturinn **Skoða eftir** á síðunni **Fjárhagur - Staða/áætlun** er notaður til að velja lengd tímabils. Smellt er á reitinn  **Skoða sem** til að velja hvernig upphæðir eru reiknaðar annað hvort **Hreyfing** eða **Staða til dags**. Veljið aðgerðina **Fyrra tímabil** eða **Næsta tímabil** til að breyta tímabilinu.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Að skoða raunverulegar og áætlaðar upphæðir fyrir nokkur tímabil

Í stað þess að skoða raunverulegar og áætlaðar upphæðir á öllum reikningum innan ákveðins tímabils er hægt að skoða fjölda tímabila á stökum reikningi.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókhaldslykill**, velja síðan viðkomandi tengil.  
2. Á síðunni **Bókhaldslykill** veljið viðeigandi fjárhagsreikning, og veljið síðan aðgerðina **Fjárhagsreikningur staða/áætlun**.  
3. Í flýtiflipanum **Valkostir** skal fylla út reitina eins og þarf til að skilgreina hvað er sýnt í töflunni.  
4. Í flýtiflipanum **Línur** skal fara með bendilinn yfir reit í töflunni til að lesa stutta lýsingu um birta upphæð.  

## <a name="see-also"></a>Sjá einnig .

[Viðskiptagreind fjármála](bi.md)  
[Vinna með fjárhagsskýrslur](bi-how-work-account-schedule.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
