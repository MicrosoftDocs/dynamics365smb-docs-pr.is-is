---
title: 'Bókuðum reikningum og kreditreikningum [IS] eytt'
description: 'Á Íslandi, í samræmi við löggjöf, er ekki hægt að eyða bókuðum sölu- og innkaupareikningum og kreditreikningum.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'Iceland, post, invoice, credit memo'
ms.date: 04/03/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="delete-posted-invoices-and-credit-memos-in-the-icelandic-version"></a>Eyða bókuðum reikningum og kreditreikningum í íslensku útgáfunni

## <a name="before-v240"></a>Fyrir v24.0

Á Íslandi, í samræmi við löggjöf, er ekki hægt að eyða sölu- og innkaupareikningum og kreditreikningum eftir að þeir hafa verið bókaðir. Í [!INCLUDE[prod_short](../../includes/prod_short.md)], skipunin **Eyða** er ekki tiltæk fyrir þessar tegundir bókaðra skjala. 

## <a name="after-v240"></a>Eftir v24.0

Ef nýja [íslenska staðfæringin er virkjuð á grundvelli W1-grunnforritsins](iceland-global-core-app.md) er hægt að eyða sölu-, innkaupareikningum og kreditreikningum en þó aðeins þegar þeir eru eldri en sjö ára í upphafi nýja reikningsársins. 

> [!NOTE]
> Tæknilega er þessu stýrt með nýja upptalningarreitnum **Varðveita skjala á** síðunni **Fjárhagsgrunnur** . Þessi reitur er falinn og hefur sjálfgefið valkostinn **Varðveislutímabil** IS skj. með því að gera þessa stýringu virka.

## <a name="see-also"></a>Sjá einnig .

[Reikningsfæra sölur](../../sales-how-invoice-sales.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
