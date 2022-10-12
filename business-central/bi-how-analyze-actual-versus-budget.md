---
title: Greina raunverulegar og áætlaðar upphæðir
description: Í þessari grein er lýst hvernig á að greina raunverulegar upphæðir á móti áætluðum upphæðum sem safna saman, greina og samnýta gögn fyrirtækisins.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.search.form: 120, 121, 422
ms.date: 09/14/2022
ms.author: edupont
ms.openlocfilehash: 927622bf51f4474d995cd2e35f72ec3111844886
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605273"
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Greina raunverulegar og áætlaðar upphæðir

Hluti af því að safna saman, greina og deila upplýsingum fyrirtækis, er að skoða raunverulegar upphæðir í samanburði við áætlaðar upphæðir fyrir alla reikninga og nokkur tímabil.

Til að greina áætlaðar upphæðir þarf fyrst að stofna fjárhag (fjárhagsáætlanir). Frekari upplýsingar um [stofnun fjárhagsáætlana](finance-how-create-budgets.md).

## <a name="view-a-gl-budget"></a>Skoða fjárhagsáætlun

Í áætlun með víddum er hægt að setja afmarkanir á færslurnar og sjá tilteknar áætlanir.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teikn, færa inn **fjárhagsáætlanir** og velja síðan tengda tengilinn.
2. **Á síðunni fjárhagsáætlanir** er opnuð áætlunin sem skoða á.  
3. Efst á síðunni þarf að fylla út reitina sem nauðsynlegir eru til að skilgreina hvað er sýnt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Ef valið **var tímabil** annaðhvort **í reitnum Sýna sem línur eða** Sýna sem dálka **þarf að fylla út** reitinn Skoða eftir **línum**. Ef ekki hefur verið valið **tímabil** í öðrum hvorum reitnum skal færa inn viðeigandi tímabil í **reitinn Dags. afmörkun**.  

> [!NOTE]  
> Aðeins færslur úr fjárhag fjárhagsáætlunar með afmörkunarkótum sem færðir eru inn á **flipanum afmarkanir** eru teknar með í útreikningnum. Áætlunarfærslur án þeirra eða með aðra afmörkunarkóta eru ekki innifaldar. Svo framarlega sem afmörkunin er enn á síðunni birtir áætlunin aðeins færslur með þessum afmörkunarkótum.  

> [!TIP]  
> **Notið aðgerðina Breyta áætlun** til að breyta áætluninni. Á áætlunarsíðunni er valin upphæð til að skoða undirliggjandi færslur í fjárhag.

## <a name="view-actual-and-budgeted-amounts-for-all-accounts"></a>Skoða raunverulegar og áætlaðar upphæðir fyrir alla lykla

Hægt er að skoða fjárhagsáætlanir og bera þær saman við raunverulegar upphæðir í mörgum svæðum í [!INCLUDE[prod_short](includes/prod_short.md)].

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **bókhaldslykil** og veljið síðan tengda tengilinn.  
2. Á síðunni **Bókhaldslykill**, skal velja aðgerðina **Fjárhagur staða/áætlun**.
3. **Á flipanum Valkostir** eru reitirnir fylltir út eins og þörf krefur til að skilgreina hvað birtist í töflunni.  
4. Sveigið yfir svæði á töfluna til að lesa stutta lýsingu um þá upphæð sem birt er.

> [!NOTE]  
> Afmarkanirnar sem settar eru á síðuhausinn verða jafnaðar við bæði fjárhag og áætlunarfærslur.

Bókhaldslykillinn er í dálkunum til vinstri. Af dálkunum fimm lengst til hægri sýna fjórir þeir fyrstu raunverulegar og áætlaðar debet- og kreditfærslur á hverjum reikningi. Fimmti dálkurinn sýnir hlutfallsleg tengsl raunverulegra og áætlaðra upphæða á fjárhagsreikningnum.  

> [!TIP]  
> Reiturinn **Skoða eftir** á síðunni **Fjárhagur - Staða/áætlun** er notaður til að velja lengd tímabils. **Notið yfirlitið sem** svæðið til að velja hvernig upphæðirnar verða reiknaðar út, hvort **um nettóbreytingu** eða **stöðu**. Veljið aðgerðina **Fyrra tímabil** eða **Næsta tímabil** til að breyta tímabilinu.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Að skoða raunverulegar og áætlaðar upphæðir fyrir nokkur tímabil  

Í stað þess að skoða raunverulegar og áætlaðar upphæðir á öllum reikningum innan ákveðins tímabils er hægt að skoða fjölda tímabila á stökum reikningi.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Færið inn **bókhaldslykil** og veljið síðan tengda tengilinn.  
2. **Á síðunni Bókhaldslykill** er viðkomandi Fjárhagsreikningur **valinn og aðgerðin Staða/áætlun** fjárhagsreikningsins valin.  
3. **Á flipanum Valkostir** eru reitirnir fylltir út eins og þörf krefur til að skilgreina hvað birtist í töflunni.  
4. **Á flipanum Línur** er sveigt yfir svæði í töflunni til að lesa stutta lýsingu um þá upphæð sem birt er.  

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun kl [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index).

## <a name="see-also"></a>Sjá einnig .

[Upplýsingarit um Fjármál fyrirtækja](bi.md)  
[Vinna með ársskýrslur](bi-how-work-account-schedule.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
