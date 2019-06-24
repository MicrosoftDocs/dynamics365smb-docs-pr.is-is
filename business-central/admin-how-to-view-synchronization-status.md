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
ms.openlocfilehash: 11e29674c2d12031fdf4e7f66e767be4fcc74795
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620885"
---
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="a35c4-103">Skoða stöðu á samstillingu</span><span class="sxs-lookup"><span data-stu-id="a35c4-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="a35c4-104">Hægt er að skoða stöðu stakra samstillingarverka sem keyrð hafa verið fyrir [!INCLUDE[crm_md](includes/crm_md.md)]-samþættingu.</span><span class="sxs-lookup"><span data-stu-id="a35c4-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="a35c4-105">Þetta felur í sér samstillingarverk sem hafa verið í gangi frá verkröð og handvirk samstillingarverk sem voru gerðar á færslum frá [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a35c4-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a35c4-106">Þetta er gagnlegt við úrræðaleit á vandamálum samstillingar vegna þess að þú færð aðgang að upplýsingum um tilteknar villur.</span><span class="sxs-lookup"><span data-stu-id="a35c4-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-synchronization-issues-for-coupled-records"></a><span data-ttu-id="a35c4-107">Til að skoða samstillingarvandamál fyrir tengdar færslur</span><span class="sxs-lookup"><span data-stu-id="a35c4-107">To view synchronization issues for coupled records</span></span>
1. <span data-ttu-id="a35c4-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Samstillingarvilla í tengdum gögnum** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a35c4-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="a35c4-109">Síðan **Samstillingarvillur í tengdum gögnum** sýnir vandamál sem komu upp þegar tengdar færslur voru samstilltar.</span><span class="sxs-lookup"><span data-stu-id="a35c4-109">The **Coupled Data Synchronization Errors** page shows issues that occurred when you synchronized coupled records.</span></span> <span data-ttu-id="a35c4-110">Hægt er að sía og flokka færslur og grípa til aðgerða á borð við **Endurheimta** eða **Eyða færslum** til að leysa vandamál eitt af öðru.</span><span class="sxs-lookup"><span data-stu-id="a35c4-110">You can filter and sort records and take actions such as **Restore** or **Delete Records** to resolve issues one by one.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="a35c4-111">Að skoða samstillingarkladda fyrir tiltekna (handvirkt samstillta) færslu</span><span class="sxs-lookup"><span data-stu-id="a35c4-111">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="a35c4-112">Opnaðu til dæmis viðskiptamann, vöru eða einhverja aðra færslu sem samstillir gögn milli [!INCLUDE[d365fin](includes/d365fin_md.md)] og Sales</span><span class="sxs-lookup"><span data-stu-id="a35c4-112">Open, for example, a customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales.</span></span>
2. <span data-ttu-id="a35c4-113">Veldu aðgerðina **Samstillingarkladdi** til að skoða samstillingarkladda fyrir valda færslu.</span><span class="sxs-lookup"><span data-stu-id="a35c4-113">Choose the **Synchronization Log** action to view the synchronization log for a selected record.</span></span> <span data-ttu-id="a35c4-114">Til dæmis tiltekinn viðskiptavin sem var samstilltur handvirkt.</span><span class="sxs-lookup"><span data-stu-id="a35c4-114">For example, a specific customer you synchronized manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="a35c4-115">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a35c4-115">See Also</span></span>  
[<span data-ttu-id="a35c4-116">Uppsetning Dynamics 365 for Sales samþættingu í Business Central</span><span class="sxs-lookup"><span data-stu-id="a35c4-116">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="a35c4-117">Að nota Dynamics 365 for Sales úr Business Central</span><span class="sxs-lookup"><span data-stu-id="a35c4-117">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
