---
author: brentholtorf
ms.topic: include
ms.date: 08/16/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Til að gerast áskrifandi að RSS-straum (Really Simple Syndication) allra uppfærslna á efni viðskiptaaðgerða á learn.microsoft.comfyrir [!INCLUDE [prod_short](prod_short.md)] skaltu nota eftirfarandi tengil:

[RSS-straumur](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-bc-app%27)&locale=en-us)

> [!NOTE]
> RSS-straumurinn skilar lista yfir 100 nýjustu greinarnar. Listanum er raðað eftir dagsetningu en það getur liðið allt að vika þar til nýjustu uppfærðu greinarnar komast á listann.  
