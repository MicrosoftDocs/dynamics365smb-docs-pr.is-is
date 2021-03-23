---
title: Skoða gagnagrunnslása
description: Kynntu þér hvernig hægt er að skoða upplýsingar um alla gagnagrunnslása beint úr viðmóti biðlara í Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 640608b810f3ad9812decc493ad4e35bcc316f98
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388150"
---
# <a name="viewing-database-locks"></a><span data-ttu-id="8e608-103">Gagnagrunnslásar skoðaðir</span><span class="sxs-lookup"><span data-stu-id="8e608-103">Viewing Database Locks</span></span>

<span data-ttu-id="8e608-104">Gagnagrunnslæsing stjórnar aðgangi margra notenda að sömu gögnunum samtímis.</span><span class="sxs-lookup"><span data-stu-id="8e608-104">Database locking controls access by multiple users to the same data at the same time.</span></span> <span data-ttu-id="8e608-105">Til að verja færslu gegn öðrum færslum sem breyta sömu gögnunum, setur fyrsta færslan lás á gögnin.</span><span class="sxs-lookup"><span data-stu-id="8e608-105">To protect a transaction against other transactions modifying the same data, the first transaction puts a lock on the data.</span></span> <span data-ttu-id="8e608-106">Lásin helst á þar til færslunni er lokið.</span><span class="sxs-lookup"><span data-stu-id="8e608-106">The lock remains until the transaction's done.</span></span>

<span data-ttu-id="8e608-107">Notendur geta verið útilokaðir frá því að ljúka við færslur á læstum gögnum.</span><span class="sxs-lookup"><span data-stu-id="8e608-107">Users may be blocked from completing transactions on the locked data.</span></span> <span data-ttu-id="8e608-108">Þeir fá gjarnan skilaboð sem gefa til kynna skilyrði lássins.</span><span class="sxs-lookup"><span data-stu-id="8e608-108">They'll typically get a message that indicates the lock condition.</span></span>

## <a name="to-view-database-locks"></a><span data-ttu-id="8e608-109">Að skoða gagnagrunnslása</span><span class="sxs-lookup"><span data-stu-id="8e608-109">To view database locks</span></span>

<span data-ttu-id="8e608-110">Veldu táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn"), sláðu inn **Gagnagrunnslásar** og veldu síðan viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="8e608-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Database Locks**, and then choose the related link.</span></span>

<span data-ttu-id="8e608-111">Síðan **Gagnagrunnslásar** sýnir skyndimynd af öllum núverandi gagnagrunnslásum.</span><span class="sxs-lookup"><span data-stu-id="8e608-111">The **Database Locks** page gives snapshot of all current database locks.</span></span>

<span data-ttu-id="8e608-112">Nánari upplýsingar er að finna í [Fylgst með gagnagrunnslásum](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) í Business Central Developer og IT Pro hjálp.</span><span class="sxs-lookup"><span data-stu-id="8e608-112">For more information about database locking, see [Monitoring Database Locks](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) in the Business Central Developer and IT Pro help.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e608-113">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="8e608-113">See Also</span></span>

[<span data-ttu-id="8e608-114">Fylgjast með gagnagrunnslásum</span><span class="sxs-lookup"><span data-stu-id="8e608-114">Monitor Database Locks</span></span>](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]