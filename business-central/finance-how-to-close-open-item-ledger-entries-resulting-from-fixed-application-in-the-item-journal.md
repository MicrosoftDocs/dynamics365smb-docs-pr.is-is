---
title: Hvernig á að loka opnum færslum birgðahöfuðbókar vegna fastrar jöfnunar í birgðabók | Microsoft Docs
description: Nota skal reitinn **Jafnað frá færslu** á síðunni **Birgðabók** til að stofna fasta jöfnun milli færslu á innleið og upphaflegrar færslu á útleið. Til dæmis til að leiðrétta viðskipti á útleið eða til að vinna úr skilum þeirra.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: a2ef42fd7671d32c4949046f5c0e4d783bca5dd6
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2302165"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="6a10c-104">Loka opnum færslum birgðahöfuðbókar vegna fastrar jöfnunar í birgðabók</span><span class="sxs-lookup"><span data-stu-id="6a10c-104">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>
<span data-ttu-id="6a10c-105">Nota skal reitinn **Jafnað frá færslu** á síðunni **Birgðabók** til að stofna fasta jöfnun milli færslu á innleið og upphaflegrar færslu á útleið.</span><span class="sxs-lookup"><span data-stu-id="6a10c-105">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="6a10c-106">Til dæmis til að leiðrétta viðskipti á útleið eða til að vinna úr skilum þeirra.</span><span class="sxs-lookup"><span data-stu-id="6a10c-106">For example, to correct the outbound transaction or to process its return.</span></span> <span data-ttu-id="6a10c-107">Frekari upplýsingar eru í Jafnað frá færslu.</span><span class="sxs-lookup"><span data-stu-id="6a10c-107">For more information, see Applies-from Entry.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="6a10c-108">Fastar jafnanir gerðar með þessum hætti nota aðeins kostnað, ekki magn.</span><span class="sxs-lookup"><span data-stu-id="6a10c-108">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="6a10c-109">Í samræmi við það lokar bókaða jákvæða birgðafærslan ekki útleiðarfærslu sem er notuð og helst sjálf opin.</span><span class="sxs-lookup"><span data-stu-id="6a10c-109">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="6a10c-110">Þetta á einnig við þegar föst jöfnun fyrir jákvæða færslu er bókuð í neikvæða færslu sem ekki hefur verið lokað af venjulegri jákvæðri færslu, þá haldast bæði neikvæða og jákvæða færslan opnar.</span><span class="sxs-lookup"><span data-stu-id="6a10c-110">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>   
>  <span data-ttu-id="6a10c-111">Þetta þýðir einnig að ekki er hægt að loka birgðatímabili sé slík færsla til.</span><span class="sxs-lookup"><span data-stu-id="6a10c-111">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="6a10c-112">Eftirfarandi ferli sýnir hvernig eigi að loka slíkum færslum með því að framkvæma tvær leiðréttar bókanir í birgðabókina.</span><span class="sxs-lookup"><span data-stu-id="6a10c-112">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="6a10c-113">Til að loka opnum birgðahöfuðbókarfærslum sem verða til úr fastri jöfnun í birgðabókinni</span><span class="sxs-lookup"><span data-stu-id="6a10c-113">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1.  <span data-ttu-id="6a10c-114">Nota skal reitinn **Jafnað frá færslu** til að bóka jákvæða leiðréttingu með samsvarandi magn.</span><span class="sxs-lookup"><span data-stu-id="6a10c-114">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="6a10c-115">Þetta lokar upprunalegu neikvæðu leiðréttingarfærslunni með fastri jöfnun.</span><span class="sxs-lookup"><span data-stu-id="6a10c-115">This closes the original negative entry with a fixed application.</span></span>  
2.  <span data-ttu-id="6a10c-116">Nota skal reitinn **Jafnað frá færslu** til að bóka neikvæða leiðréttingu.</span><span class="sxs-lookup"><span data-stu-id="6a10c-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="6a10c-117">Þetta lokar upprunalegu jákvæðu leiðréttingarfærslunni með fastri jöfnun.</span><span class="sxs-lookup"><span data-stu-id="6a10c-117">This closes the original corrective positive entry with a fixed application.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6a10c-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6a10c-118">See Also</span></span>  
[<span data-ttu-id="6a10c-119"> Fjarlægja og endurjafna birgðabókafærslur</span><span class="sxs-lookup"><span data-stu-id="6a10c-119"> Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
 <span data-ttu-id="6a10c-120">[Vinna söluskil eða afturkallanir](sales-how-process-sales-returns-cancellations.md) </span><span class="sxs-lookup"><span data-stu-id="6a10c-120">[Process Sales Returns and Cancellations](sales-how-process-sales-returns-cancellations.md) </span></span>  
 <span data-ttu-id="6a10c-121">[Uppsetning birgðaverðmats og kostnaðar](finance-set-up-inventory-valuation-and-costing.md) </span><span class="sxs-lookup"><span data-stu-id="6a10c-121">[Setting Up Inventory Valuation and Costing](finance-set-up-inventory-valuation-and-costing.md) </span></span>  
 <span data-ttu-id="6a10c-122">[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="6a10c-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 [<span data-ttu-id="6a10c-123">Hönnunarupplýsingar: Aðferð kostnaðarútreiknings</span><span class="sxs-lookup"><span data-stu-id="6a10c-123">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)
