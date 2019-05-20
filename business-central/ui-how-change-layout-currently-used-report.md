---
title: Breyta því hvernig skýrsla lítur út með því að velja annað útlit | Microsoft Docs
description: Þú getur notað mismunandi útlit fyrir skýrslu, og skipt á milli útlits til að breyta því hvernig skýrsla lítur út.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: f24f1cd24a31ddbd0b455b876821ae0173a677c3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1249437"
---
# <a name="change-which-layout-is-currently-used-on-a-report"></a>Breyta hvaða útlit er nú notað í skýrslu
Skýrsla getur verið sett upp með fleiri en eitt skýrsluútliti, sem þú getur svo skipt milli eins og þörf er á.

Með hliðsjón af útlitinu sem er í boði fyrir skýrslu er hægt að velja að nota innbyggt RDLC-skýrsluútlit, innbyggt Word-skýrsluútlit eða sérsniðið útlit. Frekari upplýsingar um RDLC- og Word-skýrsluútlit, innbyggð útlit, sérsniðið útlit og fleira eru í [stjórna skýrsluútliti](ui-manage-report-layouts.md).

> [!TIP]  
> Skýrslur skjala (ekki lista) sem nota Word-skýrsluútlit eru venjulega hraðari en þær sem nota RDLC-skýrsluútlit. Ef þú hefur þess vegna kost á því að velja milli Word- eða RDLC-skýrsluútlits fyrir skýrslu skjals, skaltu nota Word-skýrsluútlit fyrir bestu afköstin.  

## <a name="to-change-the-layout-that-is-used-on-a-report"></a>Til að breyta útlitinu sem er notað í skýrslu
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Val á útliti skýrslu** og veldu síðan tengda tengilinn.  
   Síðan **Val á útliti skýrslu** sýnir allar skýrslur sem eru í boði fyrir fyrirtæki sem er tiltekið í reitnum Fyrirtæki efst á síðunni.  Reiturinn valið útlit tilgreinir útlitið sem er verið að nota á skýrsluna.
2. Stilltu reitinn **Fyrirtæki** efst á síðunni á fyrirtækið með skýrsluna.
3. Til að breyta útliti sem er notað í skýrslu skal velja röðina fyrir skýrsluna í listanum og stilla svo **valið útlit** reitinn á einn af eftirfarandi valkostum:
   * RDLC (innbyggt Notar) innbyggt RDLC skýrsluútlit í skýrslunni.
   * Word (innbyggt) Notar innbyggt Word skýrsluútlit í skýrslunni.
   * Sérsniðið, Notar sérsniðið útlit í skýrslu.  
     Hægt er að sjá hvaða sérsniðin útlit eru í boði fyrir skýrsluna í  upplýsingareitnum skýrsluútlit hluti. Ef engin sérsniðin útlit eru til fyrir skýrsluna þarf að búa það til. Ef þú velur þennan valkost skaltu fara í næsta ferli til að tilgreina sérsniðið útlit´ sem þú vilt nota.

    > [!NOTE]  
    >   Ef þú velur **RDLC (innbyggt)** eða **Word (innbyggt)** og færð villuboð um að skýrslan vilji ekki útlit af sérstakri gerð, verðurðu að velja annað útlit eða búa til sérsniðin skýrsla af þeirri gerð sem þú vilt nota.

Ef þú velur innbyggt RDLC skýrsluútlit, þá þarf ekkert að gera og útlitið er notað næst þegar skýrslan er keyrð.

## <a name="to-specify-a-custom-layout-on-a-report"></a>Til að tilgreina sérsniðið útlit skýrslu
1. Þú tilgreinir hvaða sérsniðið útlit á að nota á skýrsluna af síðunni **sérsniðið skýrsluútlit**. Ef síðan **sérsniðið skýrsluútlit** er ekki opin skaltu velja leitarhnappinn í **Lýsing á útliti skýrslu**.
2. Á síðunni **Sérsniðið skýrsluútlit** skal velja línuna yfir sérsniðna útlitið sem á að nota og lokið svo síðunni.

Þú ferð til baka á síðuna **sérsniðið skýrsluútlit val**. Heiti valins sérsniðins útlits er birt í reitnum **sérsniðið skýrsluútlit**. Sérsniðið útlit verður notað í næsta skipti sem skýrslan er keyrð.

## <a name="see-also"></a>Sjá einnig
[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
