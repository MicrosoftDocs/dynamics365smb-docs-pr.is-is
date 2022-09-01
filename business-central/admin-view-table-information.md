---
title: Skoða töfluupplýsingar
description: Nánar um hvernig hægt er að skoða upplýsingar um gagnagrunnstöflurnar í Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 8700
ms.date: 08/23/2022
ms.author: jswymer
ms.openlocfilehash: 990a8f56108bacfe82e6fe591858d238396f16be
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/29/2022
ms.locfileid: "9362163"
---
# <a name="viewing-table-information"></a>Skoðun töfluupplýsinga

Í upplýsingasíðunni **8700 er** að finna upplýsingar um fjölda færslna í öllum kerfiog viðskiptatöflum í [!INCLUDE[prod_short](includes/prod_short.md)] og hversu mikið gögn hver tafla inniheldur.

Þessar upplýsingar eru gagnlegar til að leysa úr vandamálum við úrræðaleit, þar sem þær sýna dreifingu á gagnamagni á milli taflna.

## <a name="viewing-table-information"></a>Skoða upplýsingar um málatöflu

Til að opna þessa síðu skaltu velja ![Leita að síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") táknið, fara í **Upplýsingar um töflu** og velja síðan viðkomandi tengil.

Eftirfarandi tafla lýsir upplýsingunum sem eru veittar fyrir hverja töflu:

|Dálkur|Description|
|------|-----------|
|Heiti fyrirtækis|Heiti fyrirtækisins, ef það er til staðar, sem taflan tilheyrir.|
|Töfluheiti|Heiti töflunnar.|
|Tafla nr.|KENNI töflunnar.|
|Nr. fjöldi færslna|Heildarfjöldi færslna sem eru vistaðar í töflunni.|
|Stærð færslu|Meðalstærð færslu í KB/færslu. Gildið er reiknað með eftirfarandi formúlu: 1024(Size)/(No. Af plötum). |
|Stærð (KB)|Heildarfjárhæð þess rýmis sem taflan er í í gagnagrunninum. Þetta gildi er summa gildanna í reitunum Gagnastærð og Vísistærð.|
|Gagnastærð (KB)|Hversu mikið pláss gögnin í töflunni starfa í gagnagrunninum.|
|Stærð atriðaskráar (KB)|Hversu mikið pláss töfluvísarnir (lyklarnir) starfa í gagnagrunninum.|
|Þjöppun|Gerð þjöppunar, **raðar**, **síðu** eða **ekkert** sem er notuð við töfluna í gagnagrunninum. Frekari upplýsingar er að finna [í gagnapþjöppun](/sql/relational-databases/data-compression/data-compression?).|

> [!NOTE]
> Ef gögnum er eytt í töflu er [!INCLUDE[prod_short](includes/prod_short.md)] byrjað á nokkrum ferlum bak við tjöldin til að ganga úr skugga um að allt sé hreinsað í gagnagrunninum. Gildin á upplýsingasíðu töflunnar verða ekki uppfærð fyrr en þeim ferlum er lokið sem geta tekið nokkurn tíma. Tíminn sem beðið er eftir getur verið breytilegur og fer eftir stærð gagnagrunnsins.

## <a name="see-also"></a>Sjá einnig

[Eftirlit með síðum](across-inspect-page.md)  
[Afkastagreinar fyrir þróunaraðila](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]