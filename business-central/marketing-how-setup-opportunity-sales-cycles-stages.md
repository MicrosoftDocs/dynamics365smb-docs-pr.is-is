---
title: Setja upp söluferla tækifæris og söluþrep| Microsoft Docs
description: Lýsir því hvernig skal skilgreina söluþrep, frá upphaflegum tengilið til lokunar, stofna söluferla og úthluta þeim til tækifæra í Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 9ed05b047732a171970219c9a24f5fdd6f96f0b1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755393"
---
# <a name="set-up-opportunity-sales-cycles-and-cycle-stages"></a>Setja upp söluferla tækifæris og söluþrep
Áður en hægt er að hefja notkun sölutækifæri þarf að setja upp söluferli og þrep söluferla. Söluferli samanstendur af röð þrepa sem fara frá fyrstu samskiptum til lokunar sölu. Hvert þrep hefur ákveðnar kröfur sem uppfylla þarf, til dæmis þarfnast sölutilboð áður en tækifæri getur farið á næsta þrep. Einnig er hægt að tilgreina sleppa megi þrepi. Hægt er að setja upp eins mörg söluferli og þarf, og hægt er að setja upp eins mörg þrep söluferla og þarf innan söluferlis.

Innleiðing söluferla fyrir tækifæri felur í sér að setja upp söluferli, sem skilgreina mismunandi þrep í ferli, og síðan úthluta ferlinu á tækifæri. Úthlutun viðeigandi aðgerð eða verkhlutum til tækifærisins getur líka verið hluti af uppsetningu söluferlis.

Þetta efnisatriði lýsir því líka hvernig skal setja upp verkhluta og aðgerðir og hvernig skal úthluta verkhlutum og aðgerðum. Nánari upplýsingar er að finna í [Að setja upp verkþætti með verkum](marketing-how-setup-opportunity-sales-cycles-stages.md#to-set-up-activities-with-tasks).

## <a name="to-set-up-opportunity-sales-cycle-codes"></a>Uppsetning söluferlakóða tækifæris
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Söluferli** og veldu síðan tengda tengilinn. Síðan **Söluferli** opnast og birtir lista yfir öll fyrirliggjandi söluferli.
2. Valið er **Nýtt** aðgerð og fyllt er inn í reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Þessi skref eru endurtekin til að setja upp eins mörg söluferli og óskað er eftir. Þegar söluferli tækifæra hafa verið settir upp gæti verið ráðlegt að setja upp mismunandi þrep innan hvers ferils.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Skilgreina Söluferlisþrep tækifæra
1. Á síðunni **Söluferli** skal velja söluferli tækifæris fyrir hvað þú vilt setja upp þrep, og velja síðan aðgerðina **Þrep**. Síðan **Söluferlisþrep** birtist.
2. Smellt er á aðgerina **Nýtt** til að færa inn nýtt þrep í söluferlið.

Skrefin eru endurtekin til að setja upp eins mörg þrep og óskað er eftir innan söluferlisins.

## <a name="to-assign-stage-cycles-to-opportunities"></a>Að úthluta þrepaferli á tækifæri
Eftir að þú bætir við þrepaferli tækifæris geturðu byrjað að bæta við sölutækifærum, og síðan úthluta þrepaferli á tækifæri með því að stilla reitinn **söluferliskóði**. Nánari upplýsingar sjá [Búa til sölutækifæri](marketing-how-create-opportunities.md).

## <a name="to-set-up-activities-with-tasks"></a>Uppsetning aðgerða með verkhlutum
Þú getur sameinað marga verkhluta í aðgerðum, t.d. verkhluta sem hver og einn fela í sér eitt skref. Aðgerðaverkhlutar tengjast hverjum öðrum í gegnum dagsetningarformúlu. Hægt er að úthluta aðgerðum á tækifæri, sölufólk eða tengiliði.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Aðgerðir** og veldu síðan tengda tengilinn.
2. Valið er **Nýtt** aðgerð og fyllt er inn í reitina eins og þörf krefur.
3. Á flýtiflipanum **línur** er fyllt út í reiti eftir því sem er nauðsynlegt er til að skilgreina einn eða fleiri verkhluta í aðgerðinni.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities"></a>Úthlutun verkhluta eða aðgerðum verkhluta til tækifæra
Þegar settur er upp verkhluti, geturðu úthlutað honum til sölutækifæra og þar með úthlutað aðgerðinni sem verkhlutinn tilheyrir.

> [!NOTE]  
>   Þetta ferli lýsir því hvernig skal úthluta aðgerðarverkhlutum til tækifæra. skrefin eru sambærileg við það þegar verkhlutum er úthlutað til sölufólks og tengiliða.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Tækifæri** og veldu síðan tengda tengilinn.
2. Veljið tækifæri og veljið svo aðgerðina **Verkhlutar**.
3. Á síðunni **Verkhlutalisti** velurðu aðgerðina **Stofna verkhluta**.
4.  Á síðunni **Stofna verkhluta** skal fylla inn í reitina eins og þörf krefur.

    Athugið að reitnum **Tækifæri** er sjálfkrafa úthlutað á tækifærið sem um ræðir.
5. Velja hnappinn **Í lagi**.
6. Á síðunni **Verkhlutalisti** skal velja nýjan verkhluta og síðan aðgerðina **Úthluta aðgerðum**.
7. Á síðunni **Úthluta aðgerð** skal fylla út reitina eftir þörfum og smellið veljið síðan hnappinn **Í lagi**.

## <a name="see-also"></a>Sjá einnig
[Meðhöndla sölutækifæri](marketing-processing-sales-opportunities.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
