---
title: Setja saman í verkefni
description: Læra að nota samsetningar-í-pöntun fyrir verkefni.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 08/03/2022
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Setja saman í verk

Með samsetningu verkefnis er auðveldara að bæta birgðastjórnun með því að setja aðeins saman pöntun þegar þess er krafist.

Þegar vara sem sett er saman eftir pöntun er valin á verkáætlunarlínu stofnar [!INCLUDE [prod_short](includes/prod_short.md)]  samsetningarpöntun. Samsetningarpöntunin er byggð á verkáætlunarlínunni og línur hennar eru byggðar á samsetningaruppskrift vörunnar (uppskrift). Nánari upplýsingar um samsetningaruppskriftir er farið í [Vinna með samsetningaruppskriftir](assembly-how-work-assembly-boms.md). Magn íhluta í samsetningaruppskriftinni er margfaldað með pöntunarmagninu. Síðan **Setja saman til pöntunarlínur** sýnir upplýsingar um tengdar samsetningarpöntunarlínur. Upplýsingarnar geta hjálpað til við sérsnið samsetningarvörunnar. Eins og í sölu er ekki hægt að bóka tengdar samsetningarpantanir beint. Nánari upplýsingar um samsetningarpantanir er farið í [Selja birgðavörur í flæði samsetningar-til-pantana](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).

Samsetningarpantanir eru fráteknar fyrir verk og [!INCLUDE [prod_short](includes/prod_short.md)] samstillir vörurakningu milli verkáætlunarlína og samsetningarpöntunar.

## Samþætt við vöruhúsakerfi

Setja saman við verkefni sem er samþætt vöruhúsakerfisaðgerðum til að auðvelda samsetningu og afhendingu. Ferlið hjálpar einnig til við að tryggja að flæðið frá verksamsetningu til afhendingar keyrist vel í vöruhúsaferlum innanhúss. Nánari upplýsingar um vöruhúsaflæði innanhúss fyrir verkefni er farið í [Flæði fyrir framleiðslu, samsetningu og verk](design-details-internal-warehouse-flows.md#flows-to-and-from-assembly-in-a-basic-warehouse-configuration).

Eftirfarandi tafla lýsir vöruhúsagrunnstillingunum sem settar eru saman í pantanastuðning.

|Grunnstilling  |Heimildasamstæða  |
|---------|---------|
|**Engin vöruhúsastjórnun**|Nota verkbók til að bóka fulla eða að hluta notkun. Frálag og notkun íhluta bókast sjálfkrafa fyrir samsetningarpöntunina.         |
|**Birgðatínsla**|Nota birgðatínslu til að bóka fulla eða að hluta notkun. Frálag og notkun íhluta bókast sjálfkrafa fyrir samsetningarpöntunina.          |
|**Vöruhúsatínsla**|Stofna og skrá vöruhúsatínslur fyrir íhluti og nota síðan verkbók til að bóka notkun. [!INCLUDE [prod_short](includes/prod_short.md)] staðfestir hvort notaðir samsetningaríhlutir hafi verið tíndir. Frálag og notkun íhluta bókast sjálfkrafa fyrir samsetningarpöntunina.         |

## Þekktar takmarkanir

Í þessum hluta er lýst þekktum takmörkunum sem settar eru saman við verkefni.

* Reiturinn **Magn til samsetningar í pöntun** er ekki tiltækur fyrir verkefni sem er lokað.
* Í vöruhúsatínslutilfellum **getur Magn til samsetningar í pöntun** verið annaðhvort núll eða jafnt magni. Ekki er hægt að blanda saman pöntun og setja saman á lager í verkáætlunarlínu. Stofna verður sérstakar verkáætlunarlínur.
* Samsetning pöntunar hefur ekki áhrif á reikningshæfa hluta verkefnis. Samsetning er innifalin á sölureikningum en ekki íhlutum hennar. Ekki er hægt að breyta reitnum **Magn til samsetningar í pöntun** fyrir reikningshæfar línur.
* Pantanaáætlun og áætlunarvinnublaðið hafa ekki áhrif á það vegna þess að verkefnið er ílag áætlunar. Áætlunarvélin lítur á samsetninguna sem eftirspurn.
* Ekki er hægt að færa inn neikvætt magn í reitinn **Magn til samsetningar á pöntun** .
* Ekki er hægt að afturkalla samsetningu.

## Sjá einnig .

[Verkefnastjórnun](projects-manage-projects.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Stofna verk](projects-how-create-jobs.md)
