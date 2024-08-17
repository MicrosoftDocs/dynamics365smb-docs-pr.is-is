---
title: Leiðrétta fyrirframgreiðslur
description: Hægt er að gera leiðréttingu á pöntun eftir að búið er að bóka fyrirframgreiðslureikning fyrir pöntunina og bæta nýjum línum við pöntun eftir að hafa gefið út fyrirframgreiðslu.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '44, 48, 42, 50, 52, 9305, 9307'
ms.date: 07/24/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="correct-prepayments"></a>Leiðrétta fyrirframgreiðslur

Hægt er að gera leiðréttingu á pöntun eftir að búið er að bóka fyrirframgreiðslureikning fyrir pöntunina. Hægt er að bæta nýjum línum við pöntun eftir að búið er að gefa út fyrirframgreiðslu og bóka síðan annan fyrirframgreiðslureikning en ekki er hægt að eyða línu úr pöntun eftir að fyrirframgreiðsla hefur verið reikningsfærð fyrir línuna.  

> [!TIP]
> Ef búið er að bóka fyrirframgreiðslureikning fyrir sölureikning sem þá þú leiðréttir svo eða hættir við verður einnig að leiðrétta eða hætta við fyrirframgreiðsluna.

## <a name="to-correct-a-prepayment"></a>Til að leiðrétta fyrirframgreiðslu:

Eftirfarandi ferli sýnir hvernig gefa skal út kreditreikning fyrirframgreiðslu til að afturkalla allar reikningsfærðar fyrirframgreiðslur fyrir sölupöntun.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Viðeigandi sölupöntun er opnuð.
3. Veljið aðgerðina **Fyrirframgreiðsla** og síðan aðgerðina **Bóka kreditreikning fyrirframgreiðslu** eða **Bóka og prenta kr.reikn. fyrirframgr.** aðgerðina.  
4. Á síðunni **Kreditreikningur sölu** skal farið í leiðréttingu viðeigandi færslna, sem og alla kreditreikninga sölu. Fyrir frekar upplýsingar, sjá [Meðhöndlun söluvöruskila eða afturkallana](sales-how-process-sales-returns-cancellations.md).  

    > [!NOTE]  
    > Til að lækka upphæðina í reitnum **Upphæð línu**, verður fyrst að auka fyrirframgreiðsluprósentuna í línunni svo gildið í reitnum **fyrirfrgr. línuupphæð** sé ekki lækkuð niður fyrir gildið í reitnum **fyrirfrg. reikningsupphæð**.

5. Til að gera fyrirframgreiðslureikning fyrir nýjar línur í sölukreditreikningi, veljið aðgerðina **Fyrirframgreiðsla** og síðan aðgerðina **Bóka reikning fyrirframgreiðslu** eða **Bóka og prenta reikn. fyrirframgr.** aðgerðina.  
6. Til að gefa út auka fyrirframgreiðslureikning, skal hækka upphæð fyrirframgreiðslu í einni eða fleiri línum og bóka fyrirframgreiðslureikninginn. Nýr reikningur er stofnaður fyrir mismuninn á milli reikningsfærðra upphæða fyrirframgreiðslu og nýju fyrirframgreiðsluupphæðanna.  

## <a name="see-also"></a>Sjá einnig .

[Reikningsfærsla fyrirframgreiðslna](finance-invoice-prepayments.md)  
[Kynning: Uppsetning og reikningsfærsla fyrirframgreiðslna fyrir sölu](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Fjármál](finance.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
