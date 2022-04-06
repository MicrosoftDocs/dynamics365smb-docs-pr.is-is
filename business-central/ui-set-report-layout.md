---
title: Uppsetning skýrsluútlits
description: Lærðu að stilla útlitið sem er notað á skýrslu þegar forskoða og prenta.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9652, 9650
ms.date: 03/07/2022
ms.author: jswymer
ms.openlocfilehash: 9cc827630c5acfeba2efc860d8baf67cd31bb404
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8524200"
---
# <a name="setting-the-layout-used-by-a-report"></a>Uppsetning á uppsetningu sem notuð er í skýrslu

> **Á við um:** viðskipti seðlabanka á netinu, Business Mið innanhúss 2022 út bylgju 1 og nýrri. Hér má fara [í eldri útgáfur](ui-how-change-layout-currently-used-report.md).

Skýrslusnið ákvarðar útlit skýrslu. Það stýrir því hvaða gagnasvæði skýrslugdataset kemur fram, hvernig þau raðast upp, stílað og fleira. Í skýrslu er heimilt að hafa fleiri en eitt útlit sem síðan er hægt að skipta á milli þeirra eftir þörfum.

Þegar mörg fyrirtæki eru í umsókninni eru sett á stofn skipulag á hverju fyrirtæki. Þannig að sama skýrsla í einu fyrirtæki getur haft annað skipulag í öðru fyrirtæki.

## <a name="get-started"></a>Hefjast handa

Það eru tvær leiðir til að stilla hvaða útlit á að nota skýrsluna. Ein leiðin er frá **valsíðu** skýrsluuppsetningar. Hin leiðin er af **síðu skýrsluuppsetningar**. Hver síða hefur kosti, t.d.: 

- Síðan Valsíða **fyrir** uppsetningu skýrslu Birtir lista yfir allar skýrslur.

  Á þessari síðu kemur fram hvað gildandi útlit skýrslu er. Auk þess er hægt að setja skipulag í mismunandi fyrirtæki, án þess að þurfa að skipta fyrirtækinu sem unnið er með.

- Á **síðunni skipulag uppsetningar** birtist allt tiltækt skipulag fyrir hverja skýrslu í gildandi fyrirtæki.

  Auðvelt er að finna ákveðið útlit með því að raða eða sía listann. Þegar útlitið er fundið er hægt að stilla það fyrir skýrslu með einu vali.

  > [!NOTE]
  > Ekki er hægt að nota **síðuna Uppsetning skýrslu** fyrir Word og RDLC sem voru stofnaðar með **aðgerðinni sérsnið sérsniðinnar uppsetningar**. Í raun sést ekki í þessar sérsniðnu uppsetningar sem eru skráðar á **síðu skýrsluuppsetningar**. Aðeins er hægt að stilla þær með því að nota **valsíðu** skýrsluútlits.

## <a name="set-the-layout-from-the-report-layouts-page"></a>Uppsetning er sett upp af síðu skýrsluuppsetningar

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Finndu útlitið á listanum, Veldu hann og veldu **síðan stilla sjálfgefna** aðgerð efst á síðunni.

## <a name="set-the-layout-from-report-layout-selection-page"></a>Uppsetning sett upp úr Valsíðu skýrsluuppsetningar

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Val á skýrsluútliti** og velja síðan viðkomandi tengil.
  
   Á síðunni er listi yfir allar skýrslur sem eru tiltækar fyrir fyrirtækið sem er tilgreint í **svæðinu fyrirtæki** efst á síðunni. **Reiturinn Lýsing** á útliti Tilgreinir útlitið sem skýrslan notar núna.
2. **Stillið svæðið fyrirtæki** efst á fyrirtækið sem inniheldur skýrsluna.
3. Finna og velja skýrsluna á listanum og gera eina af eftirfarandi skrefum:

   - Ef útlitið sem á að skipta í er af annarri gerð en gildandi útliti skal velja **reitinn gerð** útlits og velja síðan þá gerð útlits sem á að setja í skýrsluna. 
   - Ef útlitið sem á að skipta yfir á sömu gerð og gildandi útlit er **valið útlit** aðgerðar efst.

4. **Á síðunni Uppsetning skýrslu** er valið útlit og síðan valið **í lagi**.

## <a name="revert-to-the-original-default-layout"></a>Snúa aftur í upprunalegt sjálfgefið útlit

Skýrslum er ætlað að nota uppsetningu sem sjálfgildi. Hægt er að skipta aftur í upprunalega sjálfgefna uppsetningu úr **skýrsluuppsetningu valsíðu**. Veldu bara skýrsluna, Veldu **síðan endurheimta sjálfgefna valaðgerð** efst á síðunni.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]