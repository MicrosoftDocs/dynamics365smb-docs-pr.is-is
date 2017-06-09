---
title: "Hvernig á að: Ógreiddir sölureikningar leiðréttir eða afturkallaðir | Microsoft Docs"
description: "Ógreiddir sölureikningar leiðréttir eða afturkallaðir"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 9289aeb9b44ec300646fbe6e6fdbf77e72cd7b08
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-correct-or-cancel-unpaid-sales-invoices"></a>Ógreiddir sölureikningar leiðréttir eða afturkallaðir
Hægt er að leiðrétta eða afturkalla bókaðann sölureikning. Þetta er gagnlegt þegar mistök eiga sér stað eða ef viðskiptamaðurinn biður um breytingu.

**Athugasemd**: Þegar bókaðaður sölureikningur hefur verið greiddur að hluta til eða að fullu, er ekki hægt að leiðrétta eða hætta við hann í bókaða sölureikningnum sjálfum. Þess i stað þarf að stofna sölukreditreikning handvirkt til að ógilda söluna og endurgreiða viðskiptamanninum. Fyrir frekar upplýsingar, sjá [hvernig á að: Meðhöndlun söluvöruskila eða afturkallana](sales-how-process-sales-returns-cancellations.md)

Í glugganum **Bókaður sölureikningur** er hægt að velja aðgerðina **Leiðrétting** eða aðgerina **Hætta við** til að framkvæma aðgerðirnar sem lýst er í eftirfarandi töflu.

| Aðgerð | Lýsing |
| --- | --- |
| **Leiðrétta** |Bókaði sölureikningurinn er afturkallaður. Nýr sölureikingur með sömu upplýsingum er stofnaður. Hægt er að leiðrétta og halda svo áfram söluferlinu. Nýi sölureikningurinn hefur annað númer en upprunalegi sölureikningurinn. Leiðréttur sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn. Á upphaflega bókuðum sölureikningi eru gátreitirnir  hætt við og  greitt valdir. |
| **Hætta við** |Bókaði sölureikningurinn er afturkallaður. Leiðréttur sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn. Á upphaflega bókuðum sölureikningi eru gátreitirnir  hætt við og  greitt valdir. |

Þegar hinn bókaður sölureikningur er leiðréttur eða afturkallaður, er hann jafnaður við allar fjárhags- og raunbirgðafærslur sem búnar voru til við bókun hins upphaflega sölureiknings. Þetta bakfærir hinn bókaða sölureikning í fjárhagslegum færslum og lætur hina leiðréttu bókaða sölukreditreikninga í endurskoðunarrakninguna.

## <a name="to-correct-a-posted-sales-invoice"></a>Bókaður sölureikningur leiðréttur
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Bókaðir sölureikningar**, og velja síðan viðeigandi tengil.  
2. Veljið bókaða sölureikninginn sem á að leiðrétta.

    **Athugasemd**: Ef gátreiturinn **hætt við** er valinn, er ekki hægt að leiðrétta þennan bókaða sölureikning þar sem hann hefur þegar verið leiðréttur eða afturkallaður.
3. Í reitnum **Bókaður Sölureikningur** er valið **leiðrétta** aðgerð.  
4. Nýr sölureikningur með sömu upplýsingum er stofnaður þar sem hægt er að gera leiðréttinguna. Reiturinn **hætt við** á hinum upphaflega bókaða sölureikningi er breytt í **Já**.

    Sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn.
5. velja **sýna leiðréttan kreditreikning** aðgerðina til að skoða bókaða sölukreditreikninginn sem ógildir upphaflega bókaða sölureikninginn.

## <a name="to-cancel-a-posted-sales-invoice"></a>Bókaður sölureikningur afturkallaður
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Bókaðir sölureikningar**, og velja síðan viðeigandi tengil.  
2. Veljið bókaða sölureikninginn sem á að afturkalla.

    **Athugasemd**: Ef gátreiturinn  **hætt við** er valinn, er ekki hægt að hætta við þennan bókaða sölureikning þar sem hann hefur þegar verið leiðréttur eða afturkallaður.
3. Í reitnum **Bókaður Sölureikningur** er valið **hætta við** aðgerð.

    Sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn. Reiturinn **hætt við** á hinum upphaflega bókaða sölureikningi er breytt í **Já**.
4. Velja **sýna leiðréttan kreditreikning** til að skoða bókaða sölukreditreikninginn sem ógildir upphaflega bókaða sölureikninginn.

## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Hvernig á að: Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

