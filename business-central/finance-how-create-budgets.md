---
title: Stofnun fjárhagsáætlana
description: Lýsir því hvernig áætlanir eru stofnaðar til að spá fyrir um ólíka fjárhagslega verkþætti og úthluta víddum fyrir viðskiptagreindartilgang.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.search.form: 113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374
ms.date: 08/24/2022
ms.author: edupont
ms.openlocfilehash: 229d7b06bc1ec366906531c34a6dfc0deee40c26
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605543"
---
# <a name="create-gl-budgets"></a>Stofna fjárhagsáætlunum

Hægt er að útbúa margar áætlanir fyrir sömu tímabil með því að stofna áætlanir undir aðskildum heitum. Fyrst er heiti áætlunar sett upp og áætlunarupphæðir færðar inn. Þá er heiti áætlunarinnar haft með við allar áætlunarfærslur sem stofnaðar eru.  

Þegar fjárhagsáætlun er stofnuð er hægt að skilgreina fjórar tilteknar víddir fjárhagsáætlunar sem kallast áætlunarvíddir fyrir hverja áætlun. Hægt er að velja áætlanavíddir fyrir hverja áætlun úr þeim sem er búið að setja upp. Hægt er að nota áætlanavíddir til að afmarka áætlanir og til að bæta víddaupplýsingum við áætlanafærslur. Lærðu meira í [vinnunni með víddum](finance-dimensions.md).

Fjárhagsáætlanir gegna mikilvægu hlutverki í viðskiptagreind. Sem dæmi má nefna fjárhagsskýrslu sem byggist á fjárhagsskýrslum sem hafa að geyma áætlunarfærslur eða þegar greint er frá áætluðum miðað við raunverulegar upphæðir í bókhaldslyklum. Frekari upplýsingar á [viðskiptagreind](bi.md).

Í kostnaðarbókhaldi vinnurðu með kostnaðaráætlun á svipaðan hátt. Frekari upplýsingar um [stofnun Kostnaðaráætlana](finance-create-cost-budgets.md).  

## <a name="to-create-a-new-gl-budget"></a>Að búa til nýja fjárhagsáætlun

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagsáætlanir** og velja síðan viðkomandi tengil.  
2. **Velja skal aðgerðina Breytingaskrá** og fylla síðan svæðin út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Velja skal aðgerðina **Breyta fjárhagsáætlun**.
4. Efst á síðunni **Fjárhagsáætlun** skal fylla inn í reitina eins og þörf krefur, til að skilgreina hvað birtist.  

    Aðeins færslur sem innihalda heiti áætlunar sem fært var inn í **reitinn Heiti** áætlunar eru sýndar. Þar sem þú hefur bara stofnað Áætlunarheitið eru engar færslur sem samsvara afmörkuninni. Síðan er þar af leiðandi tóm.  
5. Til að færa inn rétta upphæð er smellt á viðeigandi reit í fylkinu. Síðan **Fjárhagsáætl.færslur** opnast.  
6. Ný lína er búin til og reiturinn **Upphæð** fylltur út. Loka síðunni **Fjárhagsáætlunarfærslur**.  
7. Endurtakið skref 5 og 6 þar til allar áætlunarupphæðirnar hafa verið færðar inn.  

> [!NOTE]  
> **Á flipanum afmarkanir** er hægt að afmarka áætlunarupplýsingarnar eftir þeim áætlunarvíddum sem settar eru upp undir Heiti áætlunar.

## <a name="exporting-and-importing-gl-budgets-with-excel"></a>Útflutningur og G-áætlanir fluttar út með Excel

Eins og á öllum öðrum síðum er hægt að flytja út gögn á áætlunarsíðum til að Microsoft Excel vinna frekari vinnslu eða greiningu. Frekari upplýsingar um útflutning á [Viðskipagögnum í Excel](about-export-data.md).

> [!NOTE]
> Bókhaldslykillinn, sem fjárhagsáætlanirnar sem fjárhag (fjárhags) byggist á, hefur línur af gerð Höfuðreikningsins sem inniheldur samtölu línanna fyrir neðan hana. Þegar þú flytur út fjárhagsáætlun eru gögn í öllum línum flutt út óháð gerð lykils. Hins vegar er hægt að flytja inn gögn í línum af gerðinni bókunarreikningur aftur inn. 

Þegar Fjárhagsáætlanagerð er flutt inn er öllum gildum á fyrirsögnum línum eytt. Þetta er til að koma í veg fyrir rangar samtölur eftir innflutning gagna sem hafa verið búin til eða breytt í Excel.

### <a name="scenario"></a>Aðstæður

Vitað er að nýr Áætlaður launakostnaður verður staðbundinn Gjaldmiðill (ISK) 1.200.000. Til að gera launadeilumennina virka á áætlun fyrir þrjár tilteknar línur (af gerðinni bókun lykils) fyrir starfsmenn í fullu skipti, starfsmenn í hlutastarfi og tímabundna aðstoð. Línurnar þrjár eru flokkaðar undir fyrirsagnarlínu launa.

Þú slærð inn 1.200.000 í fyrirsögnina lína, útfærir fjárhagsáætlun í Excel, sendir hana síðan í launadeild, segir þeim að dreifa 1.200.000 ISK.

Launadeildin úthlutar upphæðinni á bókunarlyklana þrjá. Þegar þú flytur aftur inn í fjárhagsáætlun er fyllt út í lyklana þrjá með nýju Excel-gögnunum, sem verður samanlagt 1.200.000 SGM og fyrirsagnarlínan er auð.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig .

[Flutningur viðskiptagagna í Excel](about-export-data.md)  
[Fjármál](finance.md)  
[Viðskiptaupplýsingar](bi.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
