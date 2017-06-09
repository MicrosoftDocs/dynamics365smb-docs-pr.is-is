---
title: "Hvernig á að breyta því hvaða útlit er notað á skýrslum  | Microsoft Docs"
description: "Lærðu hvernig þú getur ákveðið hvernig skýrsla lítur út."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: c35611a74e981367170bc487a107777d2ba240f2
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-change-which-layout-is-currently-used-on-a-report"></a>Hvernig á að breyta því hvaða útlit er notað á skýrslum
Skýrsla getur verið sett upp með fleiri en eitt skýrsluútliti, sem þú getur svo skipt milli eins og þörf er á.

Með hliðsjón af útlitinu sem er í boði fyrir skýrslu er hægt að velja að nota innbyggt RDLC-skýrsluútlit, innbyggt Word-skýrsluútlit eða sérsniðið útlit. Frekari upplýsingar um RDLC- og Word-skýrsluútlit, innbyggð útlit, sérsniðið útlit og fleira eru í [stjórna skýrsluútliti](ui-manage-report-layouts.md).

## <a name="to-change-the-layout-that-is-used-on-a-report"></a>Til að breyta útlitinu sem er notað í skýrslu
1. Í efra hægra horni skal velja **Leit að síðu eða skýrslu** táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Search for Page or Report icon") slá inn **Val á útliti skýrslu** og velja svo tengdan tengil.  
   Glugginn **Val á útliti skýrslu** sýnir allar skýrslur sem eru í boði fyrir fyrirtæki sem er tiltekið í reitnum Fyrirtæki efst í glugganum.  Reiturinn valið útlit tilgreinir útlitið sem er verið að nota á skýrsluna.
2. Stilltu reitinn **Fyrirtæki** efst í glugganum á fyrirtækið með skýrsluna.
3. Til að breyta útliti sem er notað í skýrslu skal velja röðina fyrir skýrsluna í listanum og stilla svo **valið útlit ** reitinn á einn af eftirfarandi valkostum:
   * RDLC (innbyggt Notar) innbyggt RDLC skýrsluútlit í skýrslunni.
   * Word (innbyggt) Notar innbyggt Word skýrsluútlit í skýrslunni.
   * Sérsniðið, Notar sérsniðið útlit í skýrslu.  
     Hægt er að sjá hvaða sérsniðin útlit eru í boði fyrir skýrsluna í  upplýsingareitnum skýrsluútlit hluti. Ef engin sérsniðin útlit eru til fyrir skýrsluna þarf að búa það til. Ef þú velur þennan valkost skaltu fara í næsta ferli til að tilgreina sérsniðið útlit´ sem þú vilt nota.
     **Athugasemd**: Ef þú velur **RDLC (innbyggt)** eða **Word (innbyggt)** og færð villuboð um að skýrslan vilji ekki útlit af sérstakri gerð, verðurðu að velja annað útlit eða búa til sérsniðin skýrsla af þeirri gerð sem þú vilt nota.

Ef þú velur innbyggt RDLC skýrsluútlit, þá þarf ekkert að gera og útlitið er notað næst þegar skýrslan er keyrð.

## <a name="to-specify-a-custom-layout-on-a-report"></a>Til að tilgreina sérsniðið útlit skýrslu
1. Þú tilgreinir hvaða sérsniðið útlit á að nota á skýrsluna úr **sérsniðið skýrsluútlit** glugganum. Ef glugginn **sérsniðið skýrsluútlit** er ekki opinn skaltu velja leitarhnappinn í **Lýsing á útliti skýrslu**.
2. Í glugganum **Sérsniðin skýrsluútlit** skal velja línuna fyrir það sérsniðna útlit sem á að nota og loka svo glugganum.

Þú ferð til baka í **sérsniðið skýrsluútlit val** gluggann. Heiti valins sérsniðins útlits er birt í reitnum **sérsniðið skýrsluútlit**. Sérsniðið útlit verður notað í næsta skipti sem skýrslan er keyrð.

## <a name="see-also"></a>Sjá einnig
[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

