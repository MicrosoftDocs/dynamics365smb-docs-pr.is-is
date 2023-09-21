---
title: Vinna úr hlutaafhendingum
description: Hægt er að vinna úr afhendingu sölupantana í Business Central með hlutaafhendingum með því að nota reitina „Ráðlegging um sendingu“ og „Magn til afhendingar“.
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'shipping advice, partial shipments, partial deliveries, trade, customer sales order'
ms.date: 08/12/2022
ms.author: bholtorf
---
# Vinna úr hlutaafhendingum

Í hlutaafhendingu er pöntun ekki send öll í einu. Til dæmis þegar 40 einingar af 100 eininga pöntun eru afhentar strax og 60 einingar síðar. Engar takmarkanir eru á fjölda afhendinga fyrir hverja pöntun.

Áður en þú getur notað hlutaafhendingar í [!INCLUDE [prod_short](includes/prod_short.md)] þarftu hins vegar að tilgreina að viðskiptamaðurinn samþykki hlutaafhendingar með því að stilla reitinn **Ráðlegging um sendingu** á síðunni **Viðskiptamannaspjald**. Að öðrum kosti, ef viðskiptamaðurinn samþykkir yfirleitt aðeins fullar afhendingar en óskar síðan eftir eða samþykkir hlutaafhendingu fyrir tiltekna sölupöntun, er hægt að breyta reitnum **Ráðlegging um sendingu** fyrir bókun.

[!INCLUDE [prod_short](includes/prod_short.md)] stillir reitinn að sjálfgefnu á síðunni **Viðskiptamannaspjald** sem **Að hluta til**, sem leyfir hlutaafhendingar. Ef reiturinn hefur hins vegar verið lagaður til að gefa til kynna **Fullbúið** verður reiturinn **Magn til afhendingar** útilokað í sölupöntunum fyrir þann viðskiptamann.

[!INCLUDE [order-ship-invoice_md](includes/order-ship-invoice.md)]

## Sjá einnig .

[Selja vörur með sölupöntun viðskiptavinar](sales-how-sell-products.md)  
[Senda vörur](warehouse-how-ship-items.md)  
[Beinar sendingar](sales-how-drop-shipment.md)  
[Sala](sales-manage-sales.md)  
[Undirbúningur fyrir viðskipti](ui-get-ready-business.md)  
[Stjórnun](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
