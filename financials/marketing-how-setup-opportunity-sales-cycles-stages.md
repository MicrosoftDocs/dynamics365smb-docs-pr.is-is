---
title: "Setja upp söluferla tækifæris og söluþrep| Microsoft Docs"
description: "Lýsir því hvernig skal skilgreina söluþrep, frá upphaflegum tengilið til lokunar, stofna söluferla og úthluta þeim til tækifæra í Financials."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 29f9caa8f01fe8e4cfd0f65cc290d82a49fb36bb
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-opportunity-sales-cycles-and-cycle-stages"></a>Hvernig á að setja upp söluferla tækifæris og söluþrep
Áður en hægt er að hefja notkun sölutækifæri þarf að setja upp söluferli og þrep söluferla. Söluferli samanstendur af röð þrepa sem fara frá fyrstu samskiptum til lokunar sölu. Hvert þrep hefur ákveðnar kröfur sem uppfylla þarf, til dæmis þarfnast sölutilboð áður en tækifæri getur farið á næsta þrep. Einnig er hægt að tilgreina sleppa megi þrepi. Hægt er að setja upp eins mörg söluferli og þarf, og hægt er að setja upp eins mörg þrep söluferla og þarf innan söluferlis.

Innleiðing söluferla fyrir tækifæri felur í sér að setja upp söluferli, sem skilgreina mismunandi þrep í ferli, og síðan úthluta ferlinu á tækifæri. Úthlutun viðeigandi aðgerð eða verkhlutum til tækifærisins getur líka verið hluti af uppsetningu söluferlis.

Þetta efnisatriði lýsir því líka hvernig skal setja upp verkhluta og aðgerðir og hvernig skal úthluta verkhlutum og aðgerðum. Nánari upplýsingar er að finna í „Að setja upp aðgerðir með verkhlutum" liðnum.

## <a name="to-set-up-opportunity-sales-cycle-codes"></a>Uppsetning söluferlakóða tækifæris
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Söluferli** og velja svo viðeigandi tengil. **Söluferli** glugganum opnast og birtir lista yfir öll fyrirliggjandi söluferlum.
2. Valið er **Nýtt** aðgerð og fyllt er inn í reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Þessi skref eru endurtekin til að setja upp eins mörg söluferli og óskað er eftir. Þegar söluferli tækifæra hafa verið settir upp gæti verið ráðlegt að setja upp mismunandi þrep innan hvers ferils.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Skilgreina Söluferlisþrep tækifæra
1. Í glugganum **söluferli** skal velja söluferli tækifæris fyrir hvað þú vilt setja upp þrep, og velja síðan aðgerðina **þrep**. Glugginn **Söluferlisþrep** birtist.
2. Smellt er á aðgerina **Nýtt** til að færa inn nýtt þrep í söluferlið.

Skrefin eru endurtekin til að setja upp eins mörg þrep og óskað er eftir innan söluferlisins.

## <a name="to-assign-stage-cycles-to-opportunities"></a>Að úthluta þrepaferli á tækifæri
Eftir að þú bætir við þrepaferli tækifæris geturðu byrjað að bæta við sölutækifærum, og síðan úthluta þrepaferli á tækifæri með því að stilla reitinn **söluferliskóði**. Frekari upplýsingar eru í [Hvernig á að stofna sölutækifæri](marketing-how-create-opportunities.md).

## <a name="to-set-up-activities-with-tasks"></a>Uppsetning aðgerða með verkhlutum
Þú getur sameinað marga verkhluta í aðgerðum, t.d. verkhluta sem hver og einn fela í sér eitt skref. Aðgerðaverkhlutar tengjast hverjum öðrum í gegnum dagsetningarformúlu. Hægt er að úthluta aðgerðum á tækifæri, sölufólk eða tengiliði.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **aðgerðir** og velja svo viðeigandi tengil.
2. Valið er **Nýtt** aðgerð og fyllt er inn í reitina eins og þörf krefur.
3. Á flýtiflipanum **línur** er fyllt út í reiti eftir því sem er nauðsynlegt er til að skilgreina einn eða fleiri verkhluta í aðgerðinni.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities"></a>Úthlutun verkhluta eða aðgerðum verkhluta til tækifæra
Þegar settur er upp verkhluti, geturðu úthlutað honum til sölutækifæra og þar með úthlutað aðgerðinni sem verkhlutinn tilheyrir.

> [!NOTE]  
>   Þetta ferli lýsir því hvernig skal úthluta aðgerðarverkhlutum til tækifæra. skrefin eru sambærileg við það þegar verkhlutum er úthlutað til sölufólks og tengiliða.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Tækifæri** og velja svo viðeigandi tengil.
2. Veljið tækifæri og veljið svo aðgerðina **Verkhlutar**.
3. Í **Verkhlutalisti** velurðu aðgerðina **Búa til Verkhluti**.
4.  Í glugganum **Stofna verkhluta** skal fylla inn í reitina eins og þörf krefur.

    Athugið að reitnum **Tækifæri** er sjálfkrafa úthlutað á tækifærið sem um ræðir.
5. Velja hnappinn **Í lagi**.
6. Í **Verkhlutalisti** glugganum, valin er nýr verkhluti og síðan **úthluta aðgerðir** aðgerð.
7. Í glugganum **Úthluta aðgerð** skal fylla út reitina eftir þörfum og velja síðan hnappinn **Í lagi**.

## <a name="see-also"></a>Sjá einnig
[Meðhöndla sölutækifæri](marketing-processing-sales-opportunities.md)  
[Sala](sales-manage-sales.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

