---
title: Leiðrétta eða hætta við bókaðan sölureikning
description: 'Þetta efnisatriði lýsir því hvernig skal leiðrétta, afturkalla eða hætta við bókaðan sölureikning og jafna sölukreditreikning.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'undo, credit memo, return'
ms.date: 02/20/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Leiðrétta eða hætta við ógreidda sölureikninga

Hægt er að leiðrétta eða hætta við ógreiddan bókaðan sölureikning ef hann hefur ekki verið afhentur að fullu. Þetta er gagnlegt þegar mistök eiga sér stað eða ef viðskiptamaðurinn biður um breytingu áður en sendingu er lokið. Í öllum öðrum tilvikum er mælt með því að stofna leiðréttan sölukreditreikning beint. Frekari upplýsingar eru í [Að stofna nýjan sölukreditreikning úr bókuðum sölureikningi](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).  

> [!NOTE]  
> Þegar bókaðaður sölureikningur hefur verið greiddur að hluta til eða að fullu, er ekki hægt að leiðrétta eða hætta við hann í bókaða sölureikningnum sjálfum. Þess i stað þarf að stofna sölukreditreikning handvirkt til að ógilda söluna og endurgreiða viðskiptamanninum, valfrjálst stjórnað með söluvöruskilapöntun. Fyrir frekar upplýsingar, sjá [Meðhöndlun söluvöruskila eða afturkallana](sales-how-process-sales-returns-cancellations.md).

Mismuninum á því að hætta við eða leiðrétta bókaðan sölureikning sem ekki er greiddur eða afhentur er lýst í eftirfarandi töflu.

| Aðgerð | Description |
| --- | --- |
| **Hætta við** |Bókaði sölureikningurinn er afturkallaður. Leiðréttur sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn. Á upphaflega bókaða sölureikningnum eru gátreitirnir **Hætt við** og **Greiddir** valdir. |
| **Leiðrétta** |Bókaði sölureikningurinn er afturkallaður. Nýr sölureikningur með sömu upplýsingum er stofnaður, nema bókaða sölupöntunin hafi verið bókuð úr sölupöntun. Í þeim tilvikum mælum við með því að þú hættir við bókaðan sölureikning í staðinn og framkvæmir leiðréttingu og haldir söluferlinu áfram úr upprunalegu sölupöntuninni. <br/><br/>Nýi sölureikningurinn hefur annað númer en upprunalegi sölureikningurinn. Leiðréttur sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn. Á upphaflega bókaða sölureikningnum eru gátreitirnir **Hætt við** og **Greiddir** valdir. |
|**Stofna leiðréttingarkreditreikning**|Nýr sölukreditreikningur er stofnaður með sömu upplýsingum. Hægt er að leiðrétta nýja sölukreditreikninginn fyrir bókun og verður hann jafnaður við upphaflega reikninginn þegar hann er bókaður. |

Þegar hinn bókaður sölureikningur er leiðréttur eða afturkallaður, er hann jafnaður við allar fjárhags- og raunbirgðafærslur sem búnar voru til við bókun hins upphaflega sölureiknings. Þetta bakfærir hinn bókaða sölureikning í fjárhagslegum færslum og lætur hina leiðréttu bókaða sölukreditreikninga í endurskoðunarrakninguna.  

> [!TIP]
> Ef búið er að bóka fyrirframgreiðslureikning fyrir sölureikning sem þá þú leiðréttir svo eða hættir við verður einnig að leiðrétta eða hætta við fyrirframgreiðsluna. Frekari upplýsingar eru í [Leiðrétta fyrirframgreiðslur](finance-how-to-correct-prepayments.md).

## Bókaður sölureikningur afturkallaður

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókaðir sölureikningar** og velja síðan viðkomandi tengil.  
2. Veljið bókaða sölureikninginn sem á að afturkalla.

    > [!NOTE]  
    > Ef gátreiturinn **Hætt við** er valinn er ekki hægt að hætta við bókaða sölureikninginn þar sem hann hefur þegar verið afturkallaður eða leiðréttur.
3. Á síðunni **Bókaður sölureikningur** er valin aðgerðin **Hætta við**.

    Sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn. Reiturinn **hætt við** á hinum upphaflega bókaða sölureikningi er breytt í **Já**.
4. Velja **sýna leiðréttan kreditreikning** til að skoða bókaða sölukreditreikninginn sem ógildir upphaflega bókaða sölureikninginn.

### Takmörkuð bókun reiknings er einnig studd

Ef Afturköllunin tengist takmarkaðri bókun á reiknings er upprunaleg sölupöntunarlína uppfærð til að endurspegla afturkallað Reikningsfært magn. Reitirnir **Magn til reikningsf.** og **Reikn.fært magn** á tengdri sölupöntunarlínu er endurstilltir á gildin fyrir takmarkaða bókun.

## Bókaður sölureikningur leiðréttur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Bókaðir sölureikningar** og velja síðan viðkomandi tengil.  
2. Veljið bókaða sölureikninginn sem á að leiðrétta.

    > [!NOTE]  
    >   Ef gátreiturinn **Hætt við** er valinn er ekki hægt að leiðrétta bókaða sölureikninginn þar sem hann hefur þegar verið leiðréttur eða hætt við hann.
3. Á síðunni **Bókaður sölureikningur** er valin aðgerðin **Leiðrétta**.  

    > [!NOTE]
    > Ef sölureikningurinn var bókaður úr sölupöntun er mælt með því að *hætt* sé við þennan sölureikning og leiðréttingin svo unnin úr upprunalegu sölupöntuninni. Ef upprunalegu sölupöntuninni hefur verið eytt, t.d. ef hún hefur verið send að fullu, er hægt að stofna nýja sölupöntun með því að nota aðgerðina **Afrita fylgiskjal**. Frekari upplýsingar eru í [Að stofna sölukreditreikning með því að afrita bókuðum sölureikningi](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice).
4. Nýr sölureikningur með sömu upplýsingum er stofnaður þar sem hægt er að gera leiðréttinguna. Reiturinn **hætt við** á hinum upphaflega bókaða sölureikningi er breytt í **Já**.

    Sölukreditreikningur er búinn til sjálfkrafa og bókaður til að ógilda upphaflega bókaða sölureikninginn.
5. velja **sýna leiðréttan kreditreikning** aðgerðina til að skoða bókaða sölukreditreikninginn sem ógildir upphaflega bókaða sölureikninginn.

## Sjá einnig .

[Sala](sales-manage-sales.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Senda skjöl í tölvupósti](ui-how-send-documents-email.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
