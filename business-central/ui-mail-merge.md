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
ms.openlocfilehash: c624d718d27de607aed49a82a506f81eec57247c
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588908"
---
# <a name="using-word-templates-for-bulk-communication"></a>Word-sniðmát notuð fyrir mörg samskipti í einu
Microsoft Word-sniðmát geta auðveldað mörg samskipti í einu á prenti eða í tölvupósti með einingum á borð við tengiliði, viðskiptamenn og lánardrottna. Til dæmis er hægt að búa til bæklinga til að tilkynna viðskiptavinum um söluherferð, bréf til að tilkynna lánardrottnum um nýja innkaupastefnu eða boð til að fá tengiliði til að mæta á væntanlegan viðburð.

> [!NOTE]
> Þú getur eingöngu notað Word-sniðmát á tækjum með Microsoft Word 2019 og Windows-stýrikerfinu uppsettu.

Hægt er að nota einingar í [!INCLUDE[prod_short](includes/prod_short.md)] sem gagnagjafa sniðmátsins og bæta við innfellingarsvæðum til að sérsníða skjöl fyrir hverja einingu. Innfellingarsvæðin koma úr einingunni í [!INCLUDE[prod_short](includes/prod_short.md)]. Þegar Word-sniðmát er notað í einingu verða gögn úr innfellingarsvæðunum sett inn í skjalið.

Á síðunni **Word-sniðmát** er hægt að búa til nýtt sniðmát til að nota uppsetningarleiðbeiningu með hjálp til að sækja Zip-skrá sem inniheldur DataSource.xlsx og Word-sniðmátsskrá fyrir eininguna. Gagnagjafaskráin býður upp á reitina sem hægt er að nota í sniðmátinu. Ekki breyta gagnagjafaskránni. Aðeins er hægt að nota Word-sniðmátið og skrár gagnagjafans sem sótt er af [!INCLUDE[prod_short](includes/prod_short.md)] og vista verður skrárnar í sömu staðsetningunni.

Þegar búið er að setja upp sniðmátið og bæta við innfellingarsvæðum er sama leiðbeiningin notuð til að hlaða upp sniðmátinu.

## <a name="setting-up-the-template-in-word"></a>Uppsetning sniðmátsins í Word
Þegar sniðmát er sett upp í Word er hægt í flipanum **Sendingar tölvupósts** að bæta við innfellingarsvæðum með því að velja **Setja inn innfellingarsvæði**. Tiltæk innfellingarsvæði koma frá gagnagjafaskránni sem þú sóttir fyrir eininguna. Þau virka sem staðgenglar sem segja Word hvar í skjalinu á að setja upplýsingarnar um eininguna. 

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Innfellingarsvæðum bætt við í Microsoft Word":::

## <a name="adding-related-entities"></a>Tengdum einingum bætt við
Auk þess að bæta við gögnum fyrir upprunalegu eininguna, þ.e. eininguna sem þú notar til að búa til sniðmátið, getur þú einnig sameinað gögn úr einingum sem tengjast henni. Ef uppruninn er til dæmis viðskiptamannaeining er einnig hægt að sameina gögn úr reitum í einingunni viðskiptamaður/innkaupandi vegna þess að báðar einingarnar eru með einn sameiginlegan reit.

Tengdar einingar deila reit, sem er oft kennimerki á borð við heiti, kóða eða auðkenni, með upprunaeiningunni. Þegar sniðmát er sett upp eru einfaldir og ítarlegir valkostir til að velja tengdar einingar:

* Einfalt - Bættu þekktum tengslum við sem [!INCLUDE[prod_short](includes/prod_short.md)] gerir sjálfgefið aðgengileg.
* Ítarlegt - Bættu óhefðbundnum tengslum á borð við þeim sem viðbætur eða sérstillingar hafa bætt við. Þetta krefst þess að þú þekkir reitina sem einingarnar deila.

Þegar þú bætir tengdri einingu við þarftu að tilgreina forskeyti fyrir heiti reitsins. Þegar reitum er bætt við sniðmátið getur forskeytið auðveldað að gera greinarmun á reitum úr upprunaeiningunni og reitum úr tengdum einingum.

## <a name="to-create-a-word-template-in-business-central"></a>Búa til Word-sniðmát í Business Central
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Word-sniðmát** og velja síðan viðkomandi tengil.
2. Veldu **Nýtt**, síðan **Búa til sniðmát** og fylgdu síðan eftirfarandi skrefum í uppsetningu með hjálp. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Einnig er hægt að búa til sniðmát beint af síðunni fyrir einingu með því að velja aðgerðina **Nota Word-sniðmát** til að opna hjálparuppsetninguna og síðan **Nýtt sniðmát**. Þegar þú gerir það er gagnagjafinn valinn fyrir þig út frá gerð einingarinnar.

## <a name="applying-a-template"></a>Sniðmát notað
Þegar Word-sniðmátið er tilbúið er hægt á síðunni **Word-sniðmát** að velja **Nota** til að búa til skjölin. Þegar Word-sniðmát er notað í einingu verða gögn úr innfellingarsvæðunum sett inn í skjalið. Annaðhvort er hægt að búa til eitt skjal sem inniheldur hluta fyrir hverja einingu eða valið **Skipta upp** til að búa til nýtt skjal fyrir hverja einingu.

Hægt er að nota sniðmát í eina eða fleiri gerðir einingar, t.d. tengilið, beint af þessari síðu eða af síðu Word-sniðmátsins til að nota sniðmátið í öllum einingum af þeirri gerð.

## <a name="using-word-templates-with-email"></a>Nota Word-sniðmát með tölvupósti
Þú getur notað Word-sniðmát til að bæta efni við tölvupóstskeyti. Þegar úr býrð til tölvupóst getur þú valið aðgerðina **Nota Word-sniðmát** til að nota efnið úr sniðmáti fyrir skilaboðin. Þá þarftu að hafa búið til eitt eða fleiri sniðmát fyrir eininguna. Hægt er að nota eitt sniðmát í einu og þegar skipt er á milli sniðmáta breytast skilaboðin til að endurspegla efnið úr völdu sniðmáti.

Þar að auki er hægt að nota aðgerðina **Bæta við skrá úr Word-sniðmáti** til að hengja efni sniðmátsins við tölvupóstinn sem skrá. Skráin mun nota sniðið sem þú tilgreindir fyrir úttak sniðmátsins.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Valmöguleikar við notkun efnis úr Word-sniðmáti í tölvupósti":::

## <a name="see-also"></a>Sjá einnig
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
