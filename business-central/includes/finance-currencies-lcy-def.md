---
author: edupont04
ms.topic: include
ms.date: 03/15/2022
ms.author: edupont
ms.openlocfilehash: c391e7d6492a722de10801212ccd04a532f8a971
ms.sourcegitcommit: 521735f8e27d8bff2d2dfbe94d240c09dcdaec29
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/15/2022
ms.locfileid: "8419525"
---
Þar sem fyrirtæki starfa í mörgum löndum/svæðum er nauðsynlegt fyrir þau að geta stundað viðskipti og skráð fjárhagslegar upplýsingar í fleiri en einum gjaldmiðli. Staðbundinn Gjaldmiðill (ISK) er skilgreindur í **fjárhagsuppsetningarsíðu** eins og lýst er í greininni [sem skilur fjárhag og bókhaldslykla](../finance-general-ledger.md). Þegar staðbundinn gjaldmiðill hefur verið skilgreindur verður hann tómur gjaldmiðill. Þegar reiturinn **Gjaldmiðill** er auður merkir það að gjaldmiðillinn er SGM.  

Því næst þarf að setja upp gjaldmiðilskóða fyrir hvern gjaldmiðil sem er notaður ef keypt er eða selt er í öðrum gjaldmiðlum en staðbundnum gjaldmiðli (SGM). Einnig er hægt að stofna bankareikninga með gjaldmiðlum. Hægt er að skrá fjárhagsfærslur í mismunandi gjaldmiðlum, en fjárhagsfærslan verður ávallt færð í staðbundnum gjaldmiðli (SGM).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Fjárhagurinn þinn er settur upp til að nota staðbundna gjaldmiðilinn (SGM), en þú getur sett hann upp til að einnig nota annan gjaldmiðil með gengi stillt. Með því að tilnefna annan gjaldmiðil sem svokallað annan skýrslugjaldmiðli [!INCLUDE[prod_short](prod_short.md)] mun skrá sjálfkrafa upphæðir bæði í ISK og þessum öðrum skýrslugjaldmiðli í hverri fjárhagsfærslu og öðrum færslum, svo sem VSK-færslum. Sjá [Setja upp frekari skýrslugjaldmiðli fyrir frekari upplýsingar](../finance-how-setup-additional-currencies.md). Viðbótarskýrslugjaldmiðillinn er oftast notaður til að auðvelda fjárhagsskýrslugerð til eigenda sem búa í löndum/svæðum sem nota annan gjaldmiðil en staðbundinn gjaldmiðill (SGM).  

> [!IMPORTANT]
> Ef þú vilt nota annan skýrslugjaldmiðil fyrir fjárhagsskýrslur skaltu ganga úr skugga um að þú skiljir takmarkanirnar. Sjá [Setja upp frekari skýrslugjaldmiðli fyrir frekari upplýsingar](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Þegar notaður er bókaður í fjárhag með gjaldmiðilskóta, svo sem að bóka útgjöld í færslubók með því að nota gjaldmiðilskóða, er færslunni umbreytt í ISK með því að nota gengi gjaldmiðilsins fyrir bókunardagsetninguna. Fjárhagsfærslan mun ekki innihalda upplýsingar um hvaða gjaldmiðill var notaður, aðeins gildi hans í ISK. Ef fylgjast á með upphaflegum gjaldmiðli, svo sem fyrir reikning, verður að nota sölu-og innkaupaskjöl sem og bankareikninga sem geyma upplýsingar um gjaldmiðilskóða fyrir færslurnar.
