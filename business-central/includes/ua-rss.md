---
author: edupont04
ms.topic: include
ms.date: 08/16/2022
ms.author: edupont
ms.openlocfilehash: 4bae039a18c56ee2cd92c8c9a474a0b422374e0d
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529002"
---
Til að gerast áskrifandi að RSS-straum (Really Simple Syndication) allra uppfærslna á efni viðskiptaaðgerða á learn.microsoft.comfyrir [!INCLUDE [prod_short](prod_short.md)] skaltu nota eftirfarandi tengil:

[RSS-straumur](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-bc-app%27)&locale=en-us)

> [!NOTE]
> RSS-straumurinn skilar lista yfir 100 nýjustu greinarnar. Listanum er raðað eftir dagsetningu en það getur liðið allt að vika þar til nýjustu uppfærðu greinarnar komast á listann.  
