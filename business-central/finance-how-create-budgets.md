---
title: Stofna fjárhagsáætlanir| Microsoft Docs
description: Lýsir því hvernig stofna skal fjárhagsáætlanir til að spá fyrir um mismunandi fjármálaaðgerðir og úthluta víddum fyrir viðskiptaupplýsingar.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 525cc099b2a9b2630395a092761e0526f4760356
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6444663"
---
# <a name="create-gl-budgets"></a>Stofna fjárhagsáætlunum
Hægt er að útbúa margar áætlanir fyrir sömu tímabil með því að stofna áætlanir undir aðskildum heitum. Fyrst er heiti áætlunar sett upp og áætlunarupphæðir færðar inn. Þá er heiti áætlunarinnar haft með við allar áætlunarfærslur sem stofnaðar eru.  

Þegar áætlun er stofnuð er hægt að skilgreina fjórar víddir fyrir hverja áætlun. Þessar áætlanatengdu víddir kallast áætlanavíddir. Hægt er að velja áætlanavíddir fyrir hverja áætlun úr víddunum sem þegar hafa verið settar upp. Hægt er að nota áætlanavíddir til að afmarka áætlanir og til að bæta víddaupplýsingum við áætlanafærslur. Frekari upplýsingar er að finna í [Unnið með víddir](finance-dimensions.md).

Fjárhagsáætlanir spila stórt hlutverk þegar kemur að viðskiptaupplýsingum, eins og í fjárhagsskýrslu sem byggir á fjárhagsskema sem innihalda fjárhagsáætlanafærslur eða þegar verið er að greina áætlaðar og raunverulegar upphæðir í bókhaldslyklunum. Frekari upplýsingar eru í [Viðskiptaupplýsingar](bi.md).

Í kostnaðarbókhaldi vinnurðu með kostnaðaráætlun á svipaðan hátt. Frekari upplýsingar eru í [Stofna kostnaðaráætlun](finance-create-cost-budgets.md).    

## <a name="to-create-a-new-gl-budget"></a>Að búa til nýja fjárhagsáætlun  
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagsáætlanir** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Breyta lista** og fyllið svo út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Velja skal aðgerðina **Breyta fjárhagsáætlun**.
4. Efst á síðunni **Fjárhagsáætlun** skal fylla inn í reitina eins og þörf krefur, til að skilgreina hvað birtist.  

    Aðeins færslur sem innihalda heiti áætlunar sem þú færðir inn í reitinn **Heiti áætlunar** eru sýndar. Þar sem heiti áætlunar er nýstofnað eiga engar áætlanir við afmörkunina. Síðan er þar af leiðandi tóm.  
5. Til að færa inn rétta upphæð er smellt á viðeigandi reit í fylkinu. Síðan **Fjárhagsáætl.færslur** opnast.  
6. Ný lína er búin til og reiturinn **Upphæð** fylltur út. Loka síðunni **Fjárhagsáætlunarfærslur**.  
7. Skref 5 og 6 eru endurtekin þar til allar áætlaðar upphæðir eru færðar inn.  

> [!NOTE]  
>  Á flýtiflipanum **Afmarkanir** geturðu afmarkað upplýsingar um fjárhagsáætlun með áætlunarvíddum, sem hafa verið settar upp undir heiti áætlunar.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>Útflutningur og innflutningur fjárhagsáætlana með Excel
Eins og fyrir nánast allar aðrar síður getur þú flutt út gögn á síðum fjárhagsáætlunar til Excel til frekari vinnslu eða greiningu. Frekari upplýsingar eru í [Flytja út viðskiptagögn í Excel](about-export-data.md).

> [!NOTE]
> Bókhaldslykillinn, sem fjárhagsáætlanir byggjast á, eru með línum af lyklagerðinni Fyrirsögn sem innihalda samtölu línanna fyrir neðan. Þegar þú flytur út fjárhagsáætlun eru gögn í öllum línum flutt út óháð gerð lykils. Hins vegar er aðeins hægt að flytja aftur inn gögn í línum af lyklagerðinni Bókun. Samkvæmt því: <br /><br /> **Þegar þú flytur inn fjárhagsáætlun verður öllum gildum sem voru til í fyrirsagnarlínum eytt.** <br /><br /> Þetta er til að koma í veg fyrir rangar samtölur eftir innflutning gagna sem hafa verið búin til eða breytt í Excel.<br /><br /> **Atburðarás**: Þú veist að nýi áætlaði launakostnaðurinn kemur til með að vera 1.200.000 SGM. Þú vilt að launadeildin áætli fyrir þessar þrjár tilteknu línur (af lyklagerðinni Bókun) fyrir starfsmenn í fullu starfi, starfsmenn í hlutastarfi og tímabundin aðstoð. Línurnar þrjár eru flokkaðar undir fyrirsagnarlínu launa.<br /><br />Þú slærð inn 1.200.000 í fyrirsagnarlínuna, flytur út fjárhagsáætlunina í Excel og sendir hana svo til launadeildarinnar og biður hana um að úthluta 1.200.000 SGM.<br /><br /> Launadeildin úthlutar upphæðinni á bókunarlyklana þrjá. Þegar þú flytur aftur inn í fjárhagsáætlun er fyllt út í lyklana þrjá með nýju Excel-gögnunum, sem verður samanlagt 1.200.000 SGM og fyrirsagnarlínan er auð.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig
[Flutningur viðskiptagagna í Excel](about-export-data.md)  
[Fjármál](finance.md)  
[Viðskiptaupplýsingar](bi.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]