---
author: edupont04
ms.topic: include
ms.date: 07/14/2021
ms.author: edupont
ms.openlocfilehash: 78a4f013ea7afd54fdbca64c8712be58a920cca1
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8135777"
---
Til að gerast áskrifandi að RSS-straum (Really Simple Syndication) allra uppfærslna á efni viðskiptaaðgerða á docs.microsoft.com fyrir [!INCLUDE [prod_short](prod_short.md)] skaltu nota eftirfarandi tengil:

[RSS-straumur](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-bc-app%27)&locale=en-us)

> [!NOTE]
> RSS-straumurinn skilar lista yfir 100 nýjustu greinarnar. Listanum er ekki raðað eftir dagsetningu.  