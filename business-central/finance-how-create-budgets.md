---
title: Stofnun fjárhagsáætlana
description: Lýsir því hvernig á að stofna fjárhagsáætlanir til að spá fyrir um mismunandi fjármálaaðgerðir og úthluta víddum fyrir viðskiptaupplýsingar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.search.form: '113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374'
ms.date: 08/24/2022
ms.author: edupont
---
# <a name="create-gl-budgets" />Stofna fjárhagsáætlunum

Hægt er að útbúa margar áætlanir fyrir sömu tímabil með því að stofna áætlanir undir aðskildum heitum. Fyrst er heiti áætlunar sett upp og áætlunarupphæðir færðar inn. Þá er heiti áætlunarinnar haft með við allar áætlunarfærslur sem stofnaðar eru.  

Þegar fjárhagsáætlun er stofnuð er hægt að skilgreina fjórar víddir tengdar fjárhagsáætlun, kallast fjárhagsáætlunarvíddir, fyrir hverja fjárhagsáætlun. Hægt er að velja fjárhagsáætlunarvíddir fyrir hverja fjárhagsáætlun úr þeim sem þú hefur þegar sett upp. Hægt er að nota áætlanavíddir til að afmarka áætlanir og til að bæta víddaupplýsingum við áætlanafærslur. Frekari upplýsingar eru í [Vinna með víddir](finance-dimensions.md).

Fjárhagsáætlanir gegna mikilvægu hlutverki í viðskiptagreind. Sem dæmi má nefna fjárhagsyfirlit sem byggir á fjárhagsskýrslum sem innihalda færslur fjárhagsáætlunar eða þegar upphæðir fjárhagsáætlunar samanborið við raunverulegar upphæðir eru greindar í bókhaldslyklinum. Frekari upplýsingar er að finna í [Viðskiptagreind](bi.md).

Í kostnaðarbókhaldi vinnurðu með kostnaðaráætlun á svipaðan hátt. Frekari upplýsingar má finna í [Stofna kostnaðaráætlanir](finance-create-cost-budgets.md).  

## <a name="to-create-a-new-gl-budget" />Að búa til nýja fjárhagsáætlun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagsáætlanir** og velja síðan viðkomandi tengil.  
2. Veldu aðgerðina **Breyta lista**, fylltu svo út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Velja skal aðgerðina **Breyta fjárhagsáætlun**.
4. Efst á síðunni **Fjárhagsáætlun** skal fylla inn í reitina eins og þörf krefur, til að skilgreina hvað birtist.  

    Aðeins færslur sem innihalda heiti áætlunar sem þú færðir inn í reitinn **Heiti áætlunar** eru sýndar. Þar sem þú varst að búa til heiti fjárhagsáætlunar eru engar færslur sem samsvara síunni. Síðan er þar af leiðandi tóm.  
5. Til að færa inn rétta upphæð er smellt á viðeigandi reit í fylkinu. Síðan **Fjárhagsáætl.færslur** opnast.  
6. Ný lína er búin til og reiturinn **Upphæð** fylltur út. Loka síðunni **Fjárhagsáætlunarfærslur**.  
7. Skref 5 og 6 eru endurtekin þar til allar upphæðir fjárhagsáætlunar hafa verið færðar inn.  

> [!NOTE]  
> Á flýtiflipanum **Afmarkanir** geturðu afmarkað upplýsingar um fjárhagsáætlun með fjárhagsáætlunarvíddum, sem hafa verið settar upp undir heiti fjárhagsáætlunar.

## <a name="exporting-and-importing-gl-budgets-with-excel" />Útflutningur og innflutningur fjárhagsáætlana með Excel

Eins og fyrir nánast allar aðrar síður getur þú flutt út gögn á síðum fjárhagsáætlunar til Microsoft Excel til frekari vinnslu eða greiningu. Frekari upplýsingar eru í [Flutningur viðskiptagagna í Excel](about-export-data.md).

> [!NOTE]
> Bókhaldslykillinn, sem fjárhagsáætlanir fjárhags byggjast á, er með línur af lyklagerðinni yfirskrift sem inniheldur samtölu línanna hér að neðan. Þegar þú flytur út fjárhagsáætlun eru gögn í öllum línum flutt út óháð gerð lykils. Hins vegar er aðeins hægt að flytja aftur inn gögn í línum af gerð bókunarlykils. 

Í samræmi við það, þegar þú flytur inn fjárhagsáætlun, er öllum gildum í línum yfirskriftar eytt. Þetta er til að koma í veg fyrir rangar samtölur eftir innflutning gagna sem hafa verið búin til eða breytt í Excel.

### <a name="scenario" />Aðstæður

Þú veist að nýi áætlaði launakostnaðurinn kemur til með að vera 1.200.000 í staðbundnum gjaldmiðli (SGM). Þú vilt gera launadeildinni kleift að gera fjárhagsáætlun fyrir þessar þrjár tilteknu línur (af lyklagerðinni bókun) fyrir starfsmenn í fullu starfi, starfsmenn í hlutastarfi og tímabundna aðstoð. Línurnar þrjár eru flokkaðar undir fyrirsagnarlínu launa.

Þú slærð inn 1.200.000 í fyrirsagnarlínuna, flytur út fjárhagsáætlunina í Excel, sendir hana svo til launadeildarinnar og biður hana um að úthluta 1.200.000 SGM.

Launadeildin úthlutar upphæðinni á bókunarlyklana þrjá. Þegar þú flytur aftur inn í fjárhagsáætlun er fyllt út í lyklana þrjá með nýju Excel-gögnunum, sem verður samanlagt 1.200.000 SGM og fyrirsagnarlínan er auð.

## <a name="see-related-microsoft-trainingtrainingmodulesbudgets-exchange-rates-dynamics--business-centralindex" />Sjá tengda [Microsoft þjálfun](/training/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also" />Sjá einnig .

[Flutningur viðskiptagagna í Excel](about-export-data.md)  
[Fjármál](finance.md)  
[Viðskiptaupplýsingar](bi.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
