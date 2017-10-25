---
title: "Hvernig á að loka opnum færslum birgðahöfuðbókar vegna fastrar jöfnunar í birgðabók | Microsoft Docs"
description: "Hægt er að nota reitinn **Jafnað frá færslu** í glugganum **Birgðabók** til að stofna fasta jöfnun milli færslu á innleið og upphaflegrar færslu á útleið. Til dæmis til að leiðrétta viðskipti á útleið eða til að vinna úr skilum þeirra."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d30a1316b48bd1b80ab4658ee99b14f0a0217478
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="f7b76-104">Hvernig á að loka opnum færslum birgðahöfuðbókar vegna fastrar jöfnunar í birgðabók</span><span class="sxs-lookup"><span data-stu-id="f7b76-104">How to: Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>
<span data-ttu-id="f7b76-105">Nota skal reitinn **Jafnað frá færslu** í **Birgðabók** til að stofna fasta jöfnun milli færslu á innleið og upphaflegrar færslu á útleið.</span><span class="sxs-lookup"><span data-stu-id="f7b76-105">You can use the **Applies-from Entry** field in the **Item Journal** window to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="f7b76-106">Til dæmis til að leiðrétta viðskipti á útleið eða til að vinna úr skilum þeirra.</span><span class="sxs-lookup"><span data-stu-id="f7b76-106">For example, to correct the outbound transaction or to process its return.</span></span> <span data-ttu-id="f7b76-107">Frekari upplýsingar eru í Jafnað frá færslu.</span><span class="sxs-lookup"><span data-stu-id="f7b76-107">For more information, see Applies-from Entry.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="f7b76-108">Fastar jafnanir gerðar með þessum hætti nota aðeins kostnað, ekki magn.</span><span class="sxs-lookup"><span data-stu-id="f7b76-108">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="f7b76-109">Í samræmi við það lokar bókaða jákvæða birgðafærslan ekki útleiðarfærslu sem er notuð og helst sjálf opin.</span><span class="sxs-lookup"><span data-stu-id="f7b76-109">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="f7b76-110">Þetta á einnig við þegar föst jöfnun fyrir jákvæða færslu er bókuð í neikvæða færslu sem ekki hefur verið lokað af venjulegri jákvæðri færslu, þá haldast bæði neikvæða og jákvæða færslan opnar.</span><span class="sxs-lookup"><span data-stu-id="f7b76-110">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>   
>  <span data-ttu-id="f7b76-111">Þetta þýðir einnig að ekki er hægt að loka birgðatímabili sé slík færsla til.</span><span class="sxs-lookup"><span data-stu-id="f7b76-111">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="f7b76-112">Eftirfarandi ferli sýnir hvernig eigi að loka slíkum færslum með því að framkvæma tvær leiðréttar bókanir í birgðabókina.</span><span class="sxs-lookup"><span data-stu-id="f7b76-112">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="f7b76-113">Til að loka opnum birgðahöfuðbókarfærslum sem verða til úr fastri jöfnun í birgðabókinni</span><span class="sxs-lookup"><span data-stu-id="f7b76-113">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1.  <span data-ttu-id="f7b76-114">Nota skal reitinn **Jafnað frá færslu** til að bóka jákvæða leiðréttingu með samsvarandi magn.</span><span class="sxs-lookup"><span data-stu-id="f7b76-114">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="f7b76-115">Þetta lokar upprunalegu neikvæðu leiðréttingarfærslunni með fastri jöfnun.</span><span class="sxs-lookup"><span data-stu-id="f7b76-115">This closes the original negative entry with a fixed application.</span></span>  
2.  <span data-ttu-id="f7b76-116">Nota skal reitinn **Jafnað frá færslu** til að bóka neikvæða leiðréttingu.</span><span class="sxs-lookup"><span data-stu-id="f7b76-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="f7b76-117">Þetta lokar upprunalegu jákvæðu leiðréttingarfærslunni með fastri jöfnun.</span><span class="sxs-lookup"><span data-stu-id="f7b76-117">This closes the original corrective positive entry with a fixed application.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f7b76-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f7b76-118">See Also</span></span>  
[<span data-ttu-id="f7b76-119">Hvernig á að: fjarlægja og endurjafna birgðabókafærslur</span><span class="sxs-lookup"><span data-stu-id="f7b76-119"> How to: Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
 <span data-ttu-id="f7b76-120">[Hvernig á að vinna úr söluskilum og afturköllunum](sales-how-process-sales-returns-cancellations.md) </span><span class="sxs-lookup"><span data-stu-id="f7b76-120">[How to: Process Sales Returns and Cancellations](sales-how-process-sales-returns-cancellations.md) </span></span>  
 <span data-ttu-id="f7b76-121">[Uppsetning birgðaverðmats og kostnaðar](finance-set-up-inventory-valuation-and-costing.md) </span><span class="sxs-lookup"><span data-stu-id="f7b76-121">[Setting Up Inventory Valuation and Costing](finance-set-up-inventory-valuation-and-costing.md) </span></span>  
 <span data-ttu-id="f7b76-122">[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="f7b76-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 [<span data-ttu-id="f7b76-123">Hönnunarupplýsingar: Aðferð kostnaðarútreiknings</span><span class="sxs-lookup"><span data-stu-id="f7b76-123">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)

