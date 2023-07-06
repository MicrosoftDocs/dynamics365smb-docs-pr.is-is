---
title: Skoða töfluupplýsingar
description: Kynntu þér hvernig hægt er að skoða upplýsingar um gagnagrunnstöflur í Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 8700
ms.date: 08/23/2022
ms.author: jswymer
---

# <a name="viewing-table-information"></a><a name="viewing-table-information"></a><a name="viewing-table-information"></a>Skoðun töfluupplýsinga

Síðan **8700 Töfluupplýsingar** gefur upplýsingar um færslufjölda í öllum kerfis- og viðskiptatöflum í [!INCLUDE[prod_short](includes/prod_short.md)] og hversu mikið af gögnum hver tafla inniheldur.

Þessar upplýsingar eru gagnlegar til að leysa úr vandamálum við úrræðaleit, þar sem þær sýna dreifingu á gagnamagni á milli taflna.

## <a name="viewing-table-information-1"></a><a name="viewing-table-information-1"></a><a name="viewing-table-information-1"></a>Skoða upplýsingar um málatöflu

Til að opna þessa síðu skaltu velja ![Leita að síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") táknið, fara í **Upplýsingar um töflu** og velja síðan viðkomandi tengil.

Eftirfarandi tafla lýsir upplýsingunum sem eru veittar fyrir hverja töflu:

|Dálkur|Description|
|------|-----------|
|Heiti fyrirtækis|Heiti fyrirtækisins, ef það er til staðar, sem taflan tilheyrir.|
|Töfluheiti|Heiti töflunnar.|
|Tafla nr.|Kenni töflunnar.|
|Nr. fjöldi færslna|Heildarfjöldi færslna sem eru vistaðar í töflunni.|
|Stærð færslu|Meðalstærð færslu í KB/færslu. Gildið er reiknað með eftirfarandi formúlu: 1024(Size)/(No. fjöldi færslna). |
|Stærð (KB)|Samtals geymslupláss sem taflan tekur í gagnagrunninum. Þetta gildi er samtala gildanna í reitunum fyrir gagnastærð og stærð atriðaskráar.|
|Gagnastærð (KB)|Hversu mikið pláss gögnin í töflunni taka í gagnagrunninum.|
|Stærð atriðaskráar (KB)|Hversu mikið pláss atriðaskráartöflur (lyklar) taka í gagnagrunninum.|
|Þjöppun|Tegund þjöppunar, **Lína**, **Síða** eða **Engin** sem er notuð á töflu í gagnagrunninum. Frekari upplýsingar er að finna í [Gagnaþjöppun](/sql/relational-databases/data-compression/data-compression?).|

> [!NOTE]
> Ef þú eyðir gögnum í töflu setur [!INCLUDE[prod_short](includes/prod_short.md)] í gang nokkra ferla í bakgrunni til að ganga úr skugga um að allt sé hreinsað upp í gagnagrunninum. Gildin á upplýsingasíðu töflunnar uppfærast ekki fyrr en þeim ferlum er lokið, sem getur tekið nokkurn tíma. Tíminn sem þetta tekur fer eftir stærð gagnagrunnsins.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig

[Eftirlit með síðum](across-inspect-page.md)  
[Afkastagreinar fyrir þróunaraðila](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
