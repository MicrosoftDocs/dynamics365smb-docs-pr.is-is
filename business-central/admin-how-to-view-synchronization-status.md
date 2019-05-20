---
title: Skoða stöðu á samstillingu | Microsoft Docs
description: Kynntu þér hvernig á að skoða stöðuna á stökum samstillingarverkum.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: d55d8d5ab916cee6600deaf891702a625d76d7ee
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245686"
---
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="1390d-103">Skoða stöðu á samstillingu</span><span class="sxs-lookup"><span data-stu-id="1390d-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="1390d-104">Hægt er að skoða stöðu stakra samstillingarverka sem keyrð hafa verið fyrir [!INCLUDE[crm_md](includes/crm_md.md)]-samþættingu.</span><span class="sxs-lookup"><span data-stu-id="1390d-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="1390d-105">Þetta felur í sér samstillingarverk sem hafa verið í gangi frá verkröð og handvirk samstillingarverk sem voru gerðar á færslum frá [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1390d-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="1390d-106">Þetta er gagnlegt við úrræðaleit á vandamálum samstillingar vegna þess að þú færð aðgang að upplýsingum um tilteknar villur.</span><span class="sxs-lookup"><span data-stu-id="1390d-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-all-synchronization-issues"></a><span data-ttu-id="1390d-107">Að skoða öll vandamál samstillingar</span><span class="sxs-lookup"><span data-stu-id="1390d-107">To view all synchronization issues</span></span>
1. <span data-ttu-id="1390d-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Samstillingarvilla í tengdum gögnum** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="1390d-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="1390d-109">Á síðunni **Samstillingarvillur í tengdum gögnum** er hægt að skoða öll vandamál sem komu upp í samstillingu á gögnum milli [!INCLUDE[crm_md](includes/crm_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)], afmarka og raða færslum á síðunni eftir töflu, villuboð og gripið til aðgerða á borð við **Reyna aftur** eða **Fjarlægja tengingu** til að leysa úr vandamálum, einu í einu eða mörgum í einu.</span><span class="sxs-lookup"><span data-stu-id="1390d-109">On the **Coupled Data Synchronization Errors** page you can view of all issues that occurred in synchronization of data between [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)], filter and sort records in the page by table, error message and take actions such as **Retry** or **Remove Coupling** to resolve issues one by one or in bulk.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="1390d-110">Að skoða samstillingarkladda fyrir tiltekna (handvirkt samstillta) færslu</span><span class="sxs-lookup"><span data-stu-id="1390d-110">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="1390d-111">Opnaðu til dæmis viðskiptamann, vöru eða einhverja aðra færslu sem samstillir gögn milli [!INCLUDE[d365fin](includes/d365fin_md.md)] og Sales</span><span class="sxs-lookup"><span data-stu-id="1390d-111">Open, for example, customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales</span></span>
2. <span data-ttu-id="1390d-112">Veldu aðgerðina **Samstillingarkladdi** til að skoða samstillingarkladdann fyrir valda færslu, t.d. tiltekinn viðskiptamann sem var samstilltur handvirkt</span><span class="sxs-lookup"><span data-stu-id="1390d-112">Choose **Synchronization Log** action to view the synchronization log for selected record, for example, specific customer you synchronized manually</span></span>

## <a name="see-also"></a><span data-ttu-id="1390d-113">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1390d-113">See Also</span></span>  
[<span data-ttu-id="1390d-114">Uppsetning Dynamics 365 for Sales samþættingu í Business Central</span><span class="sxs-lookup"><span data-stu-id="1390d-114">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="1390d-115">Að nota Dynamics 365 for Sales úr Business Central</span><span class="sxs-lookup"><span data-stu-id="1390d-115">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
