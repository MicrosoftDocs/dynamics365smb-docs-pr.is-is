---
title: Innkaupaskýrslur og greiningar
description: Finnið út hvaða innkaupaskýrslur eru í boði í staðlaðri útgáfu Business Central til að halda utan um reksturinn.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 5fc64db4120b80203f99742ed3ed834b23370c47
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216371"
---
# <a name="purchase-reports-and-analytics-in-business-central"></a>Innkaupaskýrslur og greiningar í Business Central

Innkaupaskýrslur í [!INCLUDE [prod_short](includes/prod_short.md)] gera starfsmönnum í framleiðslu og rekstri kleift að fá innsýn í og tölfræði um núverandi og fyrri innkaupagerðir.  

## <a name="reports"></a>Skýrslur

Eftirfarandi tafla lýsir sumum helstu skýrslunum í innkaupaskýrslum.

|Skýrsla |Kenni hlutar|Description  |
|---------|---------|---------|
|**Innkaupaupplýsingar**|312|Sýnir innkaupatölfræði fyrir hvern lánardrottinn. Þetta felur í sér upplýsingar fyrir fimm tímabil, frá þeim degi sem er tilgreindur.<br>
Skýrslan inniheldur heildarinnkaup, greiðslur, vaxtareikning og afslátt, þ.m.t. tekna og tapaða greiðsluafslætti. Tölfræði er reiknuð fyrir kaup sem eru gerð fyrir þann dag sem tilgreindur er, með þremur eins mánaðar millibili frá tilgreindum degi og fyrir tímabil sem inniheldur öll kaup sem gerð eru eftir þriðja eins mánaðar bilið.|
|**Lánardr. - 10 efstu**|311|Sýnir upplýsingar um innkaup frá lánardrottni á tilteknu tímabili. Hægt er að velja fjölda lánardrottna sem eru taldir með í skýrslu.<br>Lánardrottnum er raðað eftir upphæðum og hægt er að velja hvort þeim er raðað eftir innkaupaupphæð eða stöðu. Skýrslan gefur snöggt yfirlit yfir þá lánardrottna sem mest er keypt inn frá eða mest er skuldað.|
|**Vörulisti lánardrottins** eða **Birgðalisti lánardrottna**|320 eða 720|Birtir lista yfir lánardrottna fyrir tilteknar vörur eða vörur fyrir tiltekna lánardrottna. Þar kemur fram innkaupsverð, útreiknaður afhendingartími og vörunúmer viðkomandi lánardrottins fyrir hverja einstaka vöru.<br>Þessi skýrsla er ekki tiltæk í Bandaríkjunum, Kanada og Mexíkó. Í staðinn skal nota **Birgðalisti lánardrottna** (10164) skýrsluna.|
|**Lánardr. - Birgðakaup**|313|Þessi skýrsla sýnir lista yfir vörufærslur fyrir hvern lánardrottinn á tilteknu tímabili. Skýrslan felur í sér upplýsingar um reikningsfært magn, upphæð og hugsanlegan afslátt. Hana má til dæmis nota til að greina birgðainnkaup fyrirtækis og sýna hvort það sé samband milli afsláttar og birgðainnkaupa.|
|**Birgðir - Kostn.og söluv.listi**|716|Birtir lista yfir verðupplýsingar um tilteknar vörur eða birgðaeiningar: innkaupsverð, síðasta innkaupsverð, einingarverð, hagnaðarprósenta og hagnaður.|
|**Birgðir - til ráðst. skv. áætlun**|707|Til að fá yfirlit yfir tiltekna hluti/birgðahaldseiningar og framboð þeirra. Þessi skýrsla mun sýna uppsöfnuð gildi eins og brúttóþarfir, áætlaðar og fyrirhugaðar móttöku, birgðir o.s.frv. |
|**Birgðir - Innkaup lánardrottna**|714|Birtir lista yfir þá lánardrottna sem fyrirtækið hefur keypt vörur af á tilgreindu tímabili. Þar kemur fram reikningsfært magn, upphæð og afsláttur. Nota má skýrsluna við greiningu á vörukaupum fyrirtækisins.|
|**Birgðir - Innkaupapantanir**|709|Birtir lista yfir vörur sem eru í pöntun hjá lánardrottnum. Einnig eru þar upplýsingar um áætlaðan afhendingardag og magn og verð vara í biðpöntun. Skýrsluna má til dæmis nota til að sjá hvenær von er á vörum og hvort ítreka þurfi biðpantanir|
|**Tiltækar innkaupafrátekningar**|409|Sýnir tiltækar vörur til afhendingar í innkaupafylgiskjölum, til dæmis skilapöntunum. Notandi tekur ákvörðun um hvort skýrslan eigi við stöðu hvers fylgiskjals eða hverrar innkaupalínu. <br>Þegar skýrslan er prentuð er líka hægt að láta kerfið uppfæra magnið sem er tiltækt til afhendingar í reitinn **Magn til móttöku** í innkaupalínunum. Á innkaupakreditreikningum og neikvæðum innkaupapöntunarlínum inniheldur **Magn til móttöku** reiturinn magnið til sendingar. Þá má nota skýrsluna til þess að tilgreina hvaða fylgiskjöl skal afhenda. **Athugaðu**: þessi skýrsla er ekki tiltæk fyrir ítarlega virkni vöruhúss.|
<|**Sundurl. aldursgr. lánardr.**|11006| Sértækt fyrir DACH: Skýrsla sem hægt er að nota af teymisstjóra innkaupadeildarinnar og bókhaldsins. Hér færðu yfirlit yfir ógreidda reikninga lánardrottna, þar á meðal gjalddaga, gjaldmiðla og upphæðir. Grunnurinn eru opnar lánardrottnafærslur.| -->




## <a name="tasks"></a>Verk

Eftirfarandi greinar lýsa sumum lykilverkum til að greina stöðu fyrirtækisins:

* [Stofna greiningarskýrslur](bi-how-create-analysis-views-reports.md)  
* [Skoða tiltækileika vöru](inventory-how-availability-overview.md)  


## <a name="see-also"></a>Sjá einnig .

[Innkaup sett upp](purchasing-setup-purchasing.md)  
[Innkaup](purchasing-manage-purchasing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
