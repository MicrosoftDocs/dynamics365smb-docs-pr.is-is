---
title: Word-sniðmát notuð fyrir mörg samskipti í einu | Microsoft Docs
description: Word-sniðmát geta auðveldað að búa til mörg skjöl í einu sem eru sérsniðin fyrir tilteknar einingar.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 118d8db1266bb7150965ec4d1ce44ece77638764
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788556"
---
# <a name="using-word-templates-for-bulk-communication"></a>Word-sniðmát notuð fyrir mörg samskipti í einu
Microsoft Word-sniðmát geta auðveldað mörg samskipti í einu með einingum á borð við viðskiptavini og lánardrottna. Til dæmis er hægt að búa til bæklinga til að tilkynna viðskiptavinum um söluherferð, bréf til að tilkynna lánardrottnum um nýja innkaupastefnu eða boð til að fá tengiliði til að mæta á væntanlegan viðburð.

Hægt er að nota einingar í [!INCLUDE[prod_short](includes/prod_short.md)] sem gagnagjafa sniðmátsins og bæta við innfellingarsvæðum til að sérsníða skjöl fyrir hverja einingu. Innfellingarsvæðin koma úr einingunni í [!INCLUDE[prod_short](includes/prod_short.md)]. Þegar Word-sniðmát er notað í einingu verða gögn úr innfellingarsvæðunum sett inn í skjalið.

Á síðunni **Word-sniðmát** er hægt að nota uppsetningarleiðbeiningu með hjálp til að sækja Zip-skrá sem inniheldur DataSource.txt og Word-sniðmátsskrá fyrir einingu. Þegar búið er að setja upp sniðmátið og bæta við innfellingarsvæðum er sama leiðbeiningin notuð til að hlaða upp sniðmátinu. Aðeins er hægt að nota Word-sniðmátið og skrár gagnagjafans sem sótt er af [!INCLUDE[prod_short](includes/prod_short.md)] og vista verður skrárnar í sömu staðsetningunni.

> [!NOTE]
> Þegar eining er valin þar sem á að stofna sniðmát, sýnir listinn allar einingar í [!INCLUDE[prod_short](includes/prod_short.md)]. Hins vegar er ekki hægt að stofna sniðmát fyrir allar einingar. Ef heiti einingar inniheldur sérstafi á borð við **/**, **.**, **_** eða **-** er ekki hægt að stofna sniðmát fyrir hana. Heiti einingarinnar er sýnt í dálknum **Yfirskrift hlutar**.

Þegar sniðmátið er sett upp í Word er hægt í flipanum **Sendingar** að bæta við innfellingarsvæðum með því að velja **Setja inn innfellingarsvæði**.

> [!NOTE]
> Ekki er hægt að nota innfellingarsvæði ef heiti reitsins inniheldur 40 stafi eða fleiri. Til dæmis er ekki hægt að nota reitinn Company__Information_Customs_Permit_Date vegna þess að hann er með 40 stafi. 

Þegar Word-sniðmátið er tilbúið er hægt á síðunni **Word-sniðmát** að velja **Nota** til að búa til skjölin. Annaðhvort er hægt að búa til eitt skjal sem inniheldur hluta fyrir hverja einingu eða skipta aðgerðinni til að búa til nýtt skjal fyrir hverja einingu.

## <a name="to-create-a-word-template"></a>Til að búta til Word-sniðmát
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Word sniðmát** og veldu síðan tengda tengilinn.
2. Fylgja skal skrefunum í leiðbeiningum um uppsetningu með hjálp. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Sjá einnig
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
