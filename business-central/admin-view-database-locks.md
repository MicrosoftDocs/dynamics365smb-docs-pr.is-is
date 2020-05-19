---
title: Skoða gagnagrunnslása
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: abee0f31d66f648f4b0be567d8599b31c536a193
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324103"
---
# <a name="viewing-database-locks"></a><span data-ttu-id="d3271-102">Gagnagrunnslásar skoðaðir</span><span class="sxs-lookup"><span data-stu-id="d3271-102">Viewing Database Locks</span></span>

## <a name="about-locks"></a><span data-ttu-id="d3271-103">Um lása</span><span class="sxs-lookup"><span data-stu-id="d3271-103">About Locks</span></span>

<span data-ttu-id="d3271-104">Gagnagrunnslæsing stjórnar aðgangi margra notenda að sömu gögnunum samtímis.</span><span class="sxs-lookup"><span data-stu-id="d3271-104">Database locking controls access by multiple users to the same data at the same time.</span></span> <span data-ttu-id="d3271-105">Til að verja færslu gegn öðrum færslum sem breyta sömu gögnunum, setur fyrsta færslan lás á gögnin.</span><span class="sxs-lookup"><span data-stu-id="d3271-105">To protect a transaction against other transactions modifying the same data, the first transaction puts a lock on the data.</span></span> <span data-ttu-id="d3271-106">Lásin helst á þar til færslunni er lokið.</span><span class="sxs-lookup"><span data-stu-id="d3271-106">The lock remains until the transaction's done.</span></span>

<span data-ttu-id="d3271-107">Notendur geta verið útilokaðir frá því að ljúka við færslur á læstum gögnum.</span><span class="sxs-lookup"><span data-stu-id="d3271-107">Users may be blocked from completing transactions on the locked data.</span></span> <span data-ttu-id="d3271-108">Þeir fá gjarnan skilaboð sem gefa til kynna skilyrði lássins.</span><span class="sxs-lookup"><span data-stu-id="d3271-108">They'll typically get a message that indicates the lock condition.</span></span>

## <a name="to-view-database-locks"></a><span data-ttu-id="d3271-109">Að skoða gagnagrunnslása</span><span class="sxs-lookup"><span data-stu-id="d3271-109">To view database locks</span></span>

<span data-ttu-id="d3271-110">Veldu táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn"), sláðu inn **Gagnagrunnslásar** og veldu síðan viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="d3271-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Database Locks**, and then choose the related link.</span></span>

<span data-ttu-id="d3271-111">Síðan **Gagnagrunnslásar** sýnir skyndimynd af öllum núverandi gagnagrunnslásum.</span><span class="sxs-lookup"><span data-stu-id="d3271-111">The **Database Locks** page gives snapshot of all current database locks.</span></span>

<span data-ttu-id="d3271-112">Nánari upplýsingar er að finna í [Fylgst með gagnagrunnslásum](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) í Business Central Developer og IT Pro hjálp.</span><span class="sxs-lookup"><span data-stu-id="d3271-112">For more information about database locking, see [Monitoring Database Locks](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) in the Business Central Developer and IT Pro help.</span></span>

## <a name="see-also"></a><span data-ttu-id="d3271-113">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d3271-113">See Also</span></span>

[<span data-ttu-id="d3271-114">Fylgjast með gagnagrunnslásum</span><span class="sxs-lookup"><span data-stu-id="d3271-114">Monitor Database Locks</span></span>](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 
