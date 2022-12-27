---
title: Leiðrétta eða hætta við bókaðan sölureikning
description: Þetta efnisatriði lýsir því hvernig skal leiðrétta, afturkalla eða hætta við bókaðan sölureikning og jafna sölukreditreikning.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 95cf36a9f48b3452bcc28e049c12ae310c58e2ee
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531027"
---
# <a name="correct-or-cancel-unpaid-sales-invoices"></a>Ógreiddir sölureikningar leiðréttir eða afturkallaðir

Hægt er að leiðrétta eða hætta við ógreiddan bókaðan sölureikning, að því tilskildu að hann hafi ekki verið afhentur að fullu. Þetta er gagnlegt þegar mistök eiga sér stað eða ef viðskiptamaðurinn biður um breytingu áður en sendingu er lokið. Í öllum öðrum tilvikum er mælt með því að stofna leiðréttan sölukreditreikning beint. Frekari upplýsingar eru í [Að stofna nýjan sölukreditreikning úr bókuðum sölureikningi](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).  

> [!NOTE]  
> Þegar bókaðaður sölureikningur hefur verið greiddur að hluta til eða að fullu, er ekki hægt að leiðrétta eða hætta við hann í bókaða sölureikningnum sjálfum. Þess i stað þarf að stofna sölukreditreikning handvirkt til að ógilda söluna og endurgreiða viðskiptamanninum, valfrjálst stjórnað með söluvöruskilapöntun. Fyrir frekar upplýsingar, sjá [Meðhöndlun söluvöruskila eða afturkallana](sales-how-process-sales-returns-cancellations.md).

Mismuninum á því að hætta við eða leiðrétta bókaðan sölureikning sem ekki hefur verið greiddur eða afhentur er lýst í eftirfarandi töflu.

| Aðgerð | Description |
| --- | --- |
| **Hætta við** |Bókaði sölureikningurinn er afturkallaður. Leiðréttur sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn. Á upphaflega bókuðum sölureikningi eru gátreitirnir **Hætt við** og **Greitt** valdir. |
| **Leiðrétta** |Bókaði sölureikningurinn er afturkallaður. Nýr sölureikningur með sömu upplýsingum er stofnaður, nema bókaða sölupöntunin hafi verið bókuð úr sölupöntun. Í þeim tilvikum mælum við með því að þú hættir við bókaðan sölureikning í staðinn og framkvæmir leiðréttingu og haldir söluferlinu áfram úr upprunalegu sölupöntuninni. <br/><br/>Nýi sölureikningurinn hefur annað númer en upprunalegi sölureikningurinn. Leiðréttur sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn. Á upphaflega bókuðum sölureikningi eru gátreitirnir **Hætt við** og **Greitt** valdir. |

Þegar hinn bókaður sölureikningur er leiðréttur eða afturkallaður, er hann jafnaður við allar fjárhags- og raunbirgðafærslur sem búnar voru til við bókun hins upphaflega sölureiknings. Þetta bakfærir hinn bókaða sölureikning í fjárhagslegum færslum og lætur hina leiðréttu bókaða sölukreditreikninga í endurskoðunarrakninguna.  

> [!TIP]
> Ef búið er að bóka fyrirframgreiðslureikning fyrir sölureikning sem þá þú leiðréttir svo eða hættir við verður einnig að leiðrétta eða hætta við fyrirframgreiðsluna. Frekari upplýsingar eru í [Leiðrétta fyrirframgreiðslur](finance-how-to-correct-prepayments.md).

## <a name="to-cancel-a-posted-sales-invoice"></a>Bókaður sölureikningur afturkallaður

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókaðir sölureikningar** og velja síðan viðkomandi tengil.  
2. Veljið bókaða sölureikninginn sem á að afturkalla.

    > [!NOTE]  
    >   Ef gátreiturinn **hætt við** er valinn, er ekki hægt að hætta við þennan bókaða sölureikning þar sem þegar hefur verið hætt við hann eða hann leiðréttur.
3. Á síðunni **Bókaður sölureikningur** er valin aðgerðin **Hætta við**.

    Sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn. Reiturinn **hætt við** á hinum upphaflega bókaða sölureikningi er breytt í **Já**.
4. Velja **sýna leiðréttan kreditreikning** til að skoða bókaða sölukreditreikninginn sem ógildir upphaflega bókaða sölureikninginn.

### <a name="partial-invoice-posting-also-supported"></a>Takmörkuð bókun reiknings er einnig studd

Ef Afturköllunin tengist takmarkaðri bókun á reiknings er upprunaleg sölupöntunarlína uppfærð til að endurspegla afturkallað Reikningsfært magn. Reitirnir **Magn til reikningsf.** og **Reikn.fært magn** á tengdri sölupöntunarlínu er endurstilltir á gildin fyrir takmarkaða bókun.

## <a name="to-correct-a-posted-sales-invoice"></a>Bókaður sölureikningur leiðréttur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókaðir sölureikningar** og velja síðan viðkomandi tengil.  
2. Veljið bókaða sölureikninginn sem á að leiðrétta.

    > [!NOTE]  
    >   Ef gátreiturinn **hætt við** er valinn, er ekki hægt að leiðrétta þennan bókaða sölureikning þar sem hann hefur þegar verið leiðréttur eða hætt var við hann.
3. Á síðunni **Bókaður sölureikningur** er valin aðgerðin **Leiðrétta**.  

    > [!NOTE]
    > Ef sölureikningurinn var bókaður úr sölupöntun er mælt með því að *hætt* sé við þennan sölureikning og leiðréttingin svo unnin úr upprunalegu sölupöntuninni. Ef upprunalegu sölupöntuninni hefur verið eytt, t.d. ef hún hefur verið send að fullu, er hægt að stofna nýja sölupöntun með því að nota aðgerðina **Afrita fylgiskjal**. Frekari upplýsingar eru í [Að stofna sölukreditreikning með því að afrita bókuðum sölureikningi](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice).
4. Nýr sölureikningur með sömu upplýsingum er stofnaður þar sem hægt er að gera leiðréttinguna. Reiturinn **hætt við** á hinum upphaflega bókaða sölureikningi er breytt í **Já**.

    Sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn.
5. velja **sýna leiðréttan kreditreikning** aðgerðina til að skoða bókaða sölukreditreikninginn sem ógildir upphaflega bókaða sölureikninginn.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/ship-invoice-items-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
