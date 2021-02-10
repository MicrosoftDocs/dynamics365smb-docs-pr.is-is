---
title: Loka birgðafærslum sem voru búnar til með notkun fastrar jöfnunar
description: Lærðu hvernig þú getur stofnað handvirkt fasta jöfnun milli færslu á innleið og upphaflegrar færslu á útleið í birgðabók.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/14/2020
ms.author: edupont
ms.openlocfilehash: 2cc663d580da4738247b9fcdbe5fc4504c37fa73
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013872"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="ac3ba-103">Loka opnum færslum birgðahöfuðbókar vegna fastrar jöfnunar í birgðabók</span><span class="sxs-lookup"><span data-stu-id="ac3ba-103">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>

<span data-ttu-id="ac3ba-104">Nota skal reitinn **Jafnað frá færslu** á síðunni **Birgðabók** til að stofna fasta jöfnun milli færslu á innleið og upphaflegrar færslu á útleið.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-104">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="ac3ba-105">Til dæmis til að leiðrétta viðskipti á útleið eða til að vinna úr skilum þeirra.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-105">For example, to correct the outbound transaction or to process its return.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="ac3ba-106">Fastar jafnanir gerðar með þessum hætti nota aðeins kostnað, ekki magn.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-106">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="ac3ba-107">Í samræmi við það lokar bókaða jákvæða birgðafærslan ekki útleiðarfærslu sem er notuð og helst sjálf opin.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-107">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="ac3ba-108">Þetta á einnig við þegar föst jöfnun fyrir jákvæða færslu er bókuð í neikvæða færslu sem ekki hefur verið lokað af venjulegri jákvæðri færslu, þá haldast bæði neikvæða og jákvæða færslan opnar.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-108">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>
> <span data-ttu-id="ac3ba-109">Þetta þýðir einnig að ekki er hægt að loka birgðatímabili sé slík færsla til.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-109">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="ac3ba-110">Hægt er að breyta og endurjafna jöfnunarfærslur við ákveðnar aðstæður með því að nota síðuna **Vinnublað jöfnunar**.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-110">You can change and reapply application entries under certain conditions by using the **Application Worksheet** page.</span></span>  

<span data-ttu-id="ac3ba-111">Eftirfarandi ferli sýnir hvernig eigi að loka slíkum færslum með því að framkvæma tvær leiðréttar bókanir í birgðabókina.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-111">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="ac3ba-112">Til að loka opnum birgðahöfuðbókarfærslum sem verða til úr fastri jöfnun í birgðabókinni</span><span class="sxs-lookup"><span data-stu-id="ac3ba-112">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1. <span data-ttu-id="ac3ba-113">Nota skal reitinn **Jafnað frá færslu** til að bóka jákvæða leiðréttingu með samsvarandi magn.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-113">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="ac3ba-114">Þetta lokar upprunalegu neikvæðu leiðréttingarfærslunni með fastri jöfnun.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-114">This closes the original negative entry with a fixed application.</span></span>  

    <span data-ttu-id="ac3ba-115">Reiturinn **Jafnað frá færslu** tilgreinir númer útleiðarfærslu birgðahöfuðbókar sem hefur kostnað sem sendur er í innleiðarfærslu birgðahöfuðbókar þegar innleiðarfærsla af gerðinni **Aukning** eða **Innkaup** er bókuð í birgðabókinni.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-115">The **Applies-from Entry** field specifies the number of the outbound item ledger entry whose cost is forwarded to the inbound item ledger entry when you post an inbound transaction of type **Positive Adjmt.** or **Purchase** with the item journal.</span></span>  
2. <span data-ttu-id="ac3ba-116">Nota skal reitinn **Jafnað frá færslu** til að bóka neikvæða leiðréttingu.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="ac3ba-117">Þetta lokar upprunalegu jákvæðu leiðréttingarfærslunni með fastri jöfnun.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-117">This closes the original corrective positive entry with a fixed application.</span></span>  

    <span data-ttu-id="ac3ba-118">Reiturinn **Jafna færslu** tilgreinir ef magnið í birgðabókarlínunni á að jafnast við fylgiskjal sem þegar er bókað.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-118">The **Applies-to Entry** field specifies if the quantity in the item journal line should be applied to an already-posted document.</span></span> <span data-ttu-id="ac3ba-119">Ef svo er skal færa inn færslunúmer birgðafærslunnar sem jafna á birgðabókarlínuna við.</span><span class="sxs-lookup"><span data-stu-id="ac3ba-119">If this is the case, enter the entry number of the item ledger entry to which the item journal line should be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac3ba-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ac3ba-120">See Also</span></span>

[<span data-ttu-id="ac3ba-121">Fjarlægja og endurjafna birgðabókafærslur</span><span class="sxs-lookup"><span data-stu-id="ac3ba-121">Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
[<span data-ttu-id="ac3ba-122">Vinna söluskil eða afturkallanir</span><span class="sxs-lookup"><span data-stu-id="ac3ba-122">Process Sales Returns and Cancellations</span></span>](sales-how-process-sales-returns-cancellations.md)  
[<span data-ttu-id="ac3ba-123">Uppsetning birgðaverðmats og kostnaðar</span><span class="sxs-lookup"><span data-stu-id="ac3ba-123">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="ac3ba-124">Birgðakostnaði stjórnað</span><span class="sxs-lookup"><span data-stu-id="ac3ba-124">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="ac3ba-125">Hönnunarupplýsingar: Aðferð kostnaðarútreiknings</span><span class="sxs-lookup"><span data-stu-id="ac3ba-125">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)
