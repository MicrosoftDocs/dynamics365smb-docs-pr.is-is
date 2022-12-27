---
title: Viðbót gagnasafns
description: Safnvistun gagna býr til kostnaðarlítið öryggisafrit af færslunum þínum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 630
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: 9c547b9fe73a889145aeb228e987895aeae6aa12
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/04/2022
ms.locfileid: "8382530"
---
# <a name="the-data-archive-extension"></a>Viðbót gagnasafns
Með tímanum mun fyrirtækið þitt safna umtalsverðu magni gagna og sem stjórnandi er það líklega góð hugmynd að hafa stefnu hvað varðar safnvistun gagna. Að hafa mikið af gögnum getur hægt á kerfinu, til dæmis gæti það tekið örlítið lengri tíma að búa til skýrslur eða jafnvel læsa færslum. Auk þess getur mikið gagnamagn leitt til aukins geymslukostnaðar.

Viðbót gagnasafns býður upp á grunnramma fyrir safnvistun og öryggisafritun gagna sem hluta af dagsetningaþjöppun. Þegar dagsetningaþjöppun er notuð eru tengdar færslur sameinaðar í eina færslu og þeim upprunalegu er eytt. Frekari upplýsingar er að finna í [Þjappa gögnum með dagsetningarþjöppun](admin-manage-documents.md#compress-data-with-date-compression). Hins vegar gæti borgað sig að halda gögnunum þannig að í stað þess að eyða þeim er hægt að safnvista þau til síðari notkunar.

## <a name="start-archiving-data"></a>Hefja safnvistun gagna
Viðbótin er fyrirfram uppsett og í boði í **Stjórnun viðbótar** þannig að þú þarft ekki að gera neitt til að komast af stað. Viðbótin er einnig í boði í Microsoft AppSource. 

Safnvistanir gagna eru sýndar á síðunni **Gagnalisti safnvistunar**. Hver safnvistun getur innihaldið gögn frá mörgum töflum og getur geymt allt að 10.000 færslur. Ef fleiri en 10.000 færslur eru í töflu verður búin til önnur safnvistun fyrir næstu 10.000 færslur og svo framvegis. Ef þú til dæmis safnvistar 10.100 fjárhagsfærslum býr Business Central til eitt safn sem kallast „Fjárhagsfærslur“ fyrir fyrstu 10.000 færslurnar og síðan annað safn fyrir 100 færslurnar sem eru eftir. 

Eftir að gögn hafa verið safnvistuð er hægt að skoða þau með því að nota Microsoft Excel eða sem CSV-skrá.

* Ef þú notar Excel-valkostinn mun vinnubókin innihalda eitt vinnublað fyrir hverja gagnasafnstöflu.
* Ef þú notar CSV-valkostinn færðu ZIP-skrá með einni CSV-skrá fyrir hverja gagnasafnstöflu.

> [!TIP]
> Excel og CSV-valkostirnir auðvelda þér að nota annað forrit eða þjónustu til að flytja gögnin á annan stað, svo sem Azure Blob-geymslu eða greiningarverkfæri, t.d. Microsoft Power BI.

Viðbætur gagnasafnsins eru notaðar af eftirfarandi runuvinnslum fyrir dagsetningarþjöppun.

|Runuvinnslur  |
|---------|
|Dagsþj. Birgðaáætlunarfærslur |
|Dags.þj. bankareikn.höfuðbók |
|Dags.þj. viðskm.höfuðbók |
|Dagsþj. eignahöfuðbók |
|Dags.þj. fjárhagshöfuðbók |
|Dags.þj. vátryggingahöfuðbók |
|Viðhald dagsetningarþjöppunar. Fjárhagur |
|Viðhald dagsetningarþjöppunar. Fjárhagur |
|Dags.þj. forðahöfuðbók |
|Dagsetningaþjappa VSK-færslur |
|Dags.þj. lánardr.höfuðbók |
|Vöruhús dagsetningarþjöppunar. Færslur |
|Dagsþj. Fjárhagsáætl.færslur |

Til að hefja safnvistun gagna þegar ein runuvinnslan er keyrð skal kveikja á **Safnvista eyddum færslum**.

## <a name="storage-considerations"></a>Hvað þarf að hafa í huga varðandi geymslu
Safnvistuð gögn eru geymd í töflunni **Geymslumiðill leigjanda**. Þessi tafla er ekki tekin með þegar stærð gagnagrunns er reiknuð út samkvæmt leyfisskilmálum þínum. Í staðinn telst hún vera skráageymsla. Hins vegar mælum við með því að flytja gömul gagnasöfn í til að mynda CSV-skrá og síðan eyða gömlu safnvistuðu færslunum.

## <a name="see-also"></a>Sjá einnig
[Stjórna geymslu með því að eyða skjölum eða þjappa gögnum](admin-manage-documents.md)
