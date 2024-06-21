---
title: Viðbót gagnasafns
description: Safnvistun gagna býr til kostnaðarlítið öryggisafrit af færslunum þínum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 01/30/2023
ms.custom: bap-template
ms.search.form: 630
ms.service: dynamics-365-business-central
---

# Viðbót gagnasafns

Með tímanum mun fyrirtækið þitt safna umtalsverðu magni gagna og sem stjórnandi er það líklega góð hugmynd að hafa stefnu hvað varðar safnvistun gagna. Að hafa mikið af gögnum getur hægt á kerfinu, til dæmis gæti það tekið örlítið lengri tíma að búa til skýrslur eða jafnvel læsa færslum. Auk þess getur mikið gagnamagn leitt til aukins geymslukostnaðar.

Viðbót gagnasafns býður upp á grunnramma fyrir safnvistun og öryggisafritun gagna sem hluta af dagsetningaþjöppun. Dagsetningarþjöppun sameinar tengdar færslur í eina færslu og eyðir frumritunum. Fræðast meira um [þjöppun gagna með dagsetningarþjöppun](admin-manage-documents.md#compress-data-with-date-compression). Hins vegar gæti borgað sig að halda gögnunum þannig að í stað þess að eyða þeim er hægt að safnvista þau til síðari notkunar.

## Hefja safnvistun gagna

Viðbótin er fyrirfram uppsett og í boði í **Stjórnun viðbótar** þannig að þú þarft ekki að gera neitt til að komast af stað. Viðbótin er einnig tiltæk AppSource.

Safnvistanir gagna eru sýndar á síðunni **Gagnalisti safnvistunar**. Hver safnvistun getur innihaldið gögn frá mörgum töflum og getur geymt allt að 10.000 færslur. Ef fleiri en 10.000 færslur eru í töflu verður búin til önnur safnvistun fyrir næstu 10.000 færslur og svo framvegis. Ef þú til dæmis safnvistar 10.100 fjárhagsfærslum býr Business Central til eitt safn sem kallast „Fjárhagsfærslur“ fyrir fyrstu 10.000 færslurnar og síðan annað safn fyrir 100 færslurnar sem eru eftir.

Eftir að gögn hafa verið safnvistuð er hægt að skoða þau með því að nota Microsoft Excel eða sem CSV-skrá.

* Ef þú notar Excel-valkostinn mun vinnubókin innihalda eitt vinnublað fyrir hverja gagnasafnstöflu.
* Ef þú notar CSV-valkostinn færðu ZIP skrá sem inniheldur eina CSV skrá fyrir hverja gagnasafnstöflu.

> [!TIP]
> Excel- og CSV-valkostirnir auðvelda notkun annars forrits eða þjónustu til að færa gögnin á annan stað, svo sem Azure Blob geymslu, eða greiningarverkfæri, svo sem Microsoft Power BI.

Gagnasafnsviðbótin er notuð í eftirfarandi keyrslum fyrir dagsetningarþjöppun.

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

## Hvað þarf að hafa í huga varðandi geymslu

Safnvistuð gögn eru geymd í töflunni **Geymslumiðill leigjanda**. Mælt er með því að flytja gömul skjalasafn út í til dæmis CSV-skrá og eyða síðan gömlu skjalasafnsskránum.

## Sjá einnig

[Stjórna geymslu með því að eyða skjölum eða þjappa gögnum](admin-manage-documents.md)
