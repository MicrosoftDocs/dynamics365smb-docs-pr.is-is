---
author: edupont04
ms.topic: include
ms.date: 08/16/2022
ms.author: edupont
ms.openlocfilehash: 6b39504ecbed35bae4dea2afa5eedba816821b89
ms.sourcegitcommit: b353f06e0c91aa6e725d59600f90329774847ece
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/19/2022
ms.locfileid: "9317408"
---
Til að gerast áskrifandi að RSS-straum (Really Simple Syndication) allra uppfærslna á efni viðskiptaaðgerða á docs.microsoft.com fyrir [!INCLUDE [prod_short](prod_short.md)] skaltu nota eftirfarandi tengil:

[RSS-straumur](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-bc-app%27)&locale=en-us)

> [!NOTE]
> RSS-straumurinn skilar lista yfir 100 nýjustu greinarnar. Listanum er raðað eftir dagsetningu en það getur tekið allt að viku áður en nýuppfærðar greinar gera hana að listanum.  
