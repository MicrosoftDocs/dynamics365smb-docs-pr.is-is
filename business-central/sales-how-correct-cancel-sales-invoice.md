---
title: "Leiðrétta eða hætta við bókaðan sölureikning | Microsoft Docs"
description: "Lýsir því hvernig skal leiðrétta, afturkalla eða hætta við bókaðan sölureikning og jafna sölukreditreikning."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 9397574b6f39092550f6ba097783e3ffa15b8992
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a>Ógreiddir sölureikningar leiðréttir eða afturkallaðir
Hægt er að leiðrétta eða afturkalla bókaðann sölureikning. Þetta er gagnlegt þegar mistök eiga sér stað eða ef viðskiptamaðurinn biður um breytingu.

> [!NOTE]  
>   Þegar bókaðaður sölureikningur hefur verið greiddur að hluta til eða að fullu, er ekki hægt að leiðrétta eða hætta við hann í bókaða sölureikningnum sjálfum. Þess i stað þarf að stofna sölukreditreikning handvirkt til að ógilda söluna og endurgreiða viðskiptamanninum, valfrjálst stjórnað með söluvöruskilapöntun. Fyrir frekar upplýsingar, sjá [Meðhöndlun söluvöruskila eða afturkallana](sales-how-process-sales-returns-cancellations.md).

Í glugganum **Bókaður sölureikningur** er hægt að velja aðgerðina **Leiðrétting** eða aðgerina **Hætta við** til að framkvæma aðgerðirnar sem lýst er í eftirfarandi töflu.

| Aðgerð | Lýsing |
| --- | --- |
| **Leiðrétta** |Bókaði sölureikningurinn er afturkallaður. Nýr sölureikingur með sömu upplýsingum er stofnaður. Hægt er að leiðrétta og halda svo áfram söluferlinu. Nýi sölureikningurinn hefur annað númer en upprunalegi sölureikningurinn. Leiðréttur sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn. Á upphaflega bókuðum sölureikningi eru gátreitirnir  hætt við og  greitt valdir. |
| **Hætta við** |Bókaði sölureikningurinn er afturkallaður. Leiðréttur sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn. Á upphaflega bókuðum sölureikningi eru gátreitirnir  hætt við og  greitt valdir. |

Þegar hinn bókaður sölureikningur er leiðréttur eða afturkallaður, er hann jafnaður við allar fjárhags- og raunbirgðafærslur sem búnar voru til við bókun hins upphaflega sölureiknings. Þetta bakfærir hinn bókaða sölureikning í fjárhagslegum færslum og lætur hina leiðréttu bókaða sölukreditreikninga í endurskoðunarrakninguna.

## <a name="to-correct-a-posted-sales-invoice"></a>Bókaður sölureikningur leiðréttur
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Bókaðir sölureikningar** og velja svo viðeigandi tengil.  
2. Veljið bókaða sölureikninginn sem á að leiðrétta.

    > [!NOTE]  
    >   Ef gátreiturinn **hætt við** er valinn, er ekki hægt að leiðrétta þennan bókaða sölureikning þar sem hann hefur þegar verið leiðréttur eða hætt var við hann.
3. Í reitnum **Bókaður Sölureikningur** er valið **leiðrétta** aðgerð.  
4. Nýr sölureikningur með sömu upplýsingum er stofnaður þar sem hægt er að gera leiðréttinguna. Reiturinn **hætt við** á hinum upphaflega bókaða sölureikningi er breytt í **Já**.

    Sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn.
5. velja **sýna leiðréttan kreditreikning** aðgerðina til að skoða bókaða sölukreditreikninginn sem ógildir upphaflega bókaða sölureikninginn.

## <a name="to-cancel-a-posted-sales-invoice"></a>Bókaður sölureikningur afturkallaður
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Bókaðir sölureikningar** og velja svo viðeigandi tengil.  
2. Veljið bókaða sölureikninginn sem á að afturkalla.

    > [!NOTE]  
    >   Ef gátreiturinn **hætt við** er valinn, er ekki hægt að hætta við þennan bókaða sölureikning þar sem þegar hefur verið hætt við hann eða hann leiðréttur.
3. Í reitnum **Bókaður Sölureikningur** er valið **hætta við** aðgerð.

    Sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn. Reiturinn **hætt við** á hinum upphaflega bókaða sölureikningi er breytt í **Já**.
4. Velja **sýna leiðréttan kreditreikning** til að skoða bókaða sölukreditreikninginn sem ógildir upphaflega bókaða sölureikninginn.

## <a name="see-also"></a>Sjá einnig
[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

