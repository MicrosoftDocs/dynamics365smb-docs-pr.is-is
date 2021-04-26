---
title: Hvernig á að prenta birgðatínslulista úr sölupöntun
description: Hægt er að nota tiltektarlista birgða beint úr sölupöntun, sölu, reikningi og öðrum söluskjölum á útleið.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 705302fac91b29592c26b82d3e64a49bdc001d02
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778723"
---
# <a name="print-the-picking-list"></a><span data-ttu-id="4fa85-103">Prenta tiltektarlistann.</span><span class="sxs-lookup"><span data-stu-id="4fa85-103">Print the Picking List</span></span>
<span data-ttu-id="4fa85-104">Hægt er að hlaða tiltektarlista beint úr sölupöntun, sölureikningi eða öðru skjali sem ræsir vörur.</span><span class="sxs-lookup"><span data-stu-id="4fa85-104">You can print an inventory picking list directly from a sales order, a sales invoice, or any other document that initiates shipment of items.</span></span>

<span data-ttu-id="4fa85-105">Þessi skýrsla er yfirleitt notuð í fyrirtækjum án sérhæfðrar virkni fyrir vöruhúsastjórnun, þannig að birgðastarfsmaður getur einfaldlega skoðað eða prentað tínslulistann úr tengdu söluskjali.</span><span class="sxs-lookup"><span data-stu-id="4fa85-105">This report is typically used in companies without dedicated functionality for warehouse management, so that an inventory worker can simply view or print the picking list from the related sales document.</span></span> <span data-ttu-id="4fa85-106">Í fyrirtækjum með meiri veltu eða flóknari ferli er tiltekt áætluð og framkvæmd í sérstökum vöruhúsaskjölum.</span><span class="sxs-lookup"><span data-stu-id="4fa85-106">In companies with higher volume or more complex processes, picking is planned and performed in dedicated warehouse documents.</span></span> <span data-ttu-id="4fa85-107">Frekari upplýsingar má sjá í [Tína til vörur](warehouse-pick-items.md).</span><span class="sxs-lookup"><span data-stu-id="4fa85-107">For more information, see [Pick Items](warehouse-pick-items.md).</span></span>

## <a name="to-print-a-picking-list-from-a-sales-order"></a><span data-ttu-id="4fa85-108">Til að prenta tínslulista úr sölupöntun</span><span class="sxs-lookup"><span data-stu-id="4fa85-108">To print a picking list from a sales order</span></span>  
<span data-ttu-id="4fa85-109">Eftirfarandi ferli byggist á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="4fa85-109">The following procedure is based on a sales order.</span></span> <span data-ttu-id="4fa85-110">Skrefin eru svipuð fyrir öll söluskjöl sem hægt er að nota til að hefja sendingu á vörum.</span><span class="sxs-lookup"><span data-stu-id="4fa85-110">The steps are similar for all sales documents that can be used to initiate shipment of items.</span></span>

1. <span data-ttu-id="4fa85-111">Veldu ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") tákn, sláðu inn **Sölupantanir** og veldu svo tengdan tengil.</span><span class="sxs-lookup"><span data-stu-id="4fa85-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="4fa85-112">Opnaðu sölupöntunina sem þú vilt tína vörur fyrir.</span><span class="sxs-lookup"><span data-stu-id="4fa85-112">Open the sales order that you want to pick items for.</span></span>  
3. <span data-ttu-id="4fa85-113">Veldu aðgerðina **Skýrsla** og svo **Tínslulisti eftir pöntun**.</span><span class="sxs-lookup"><span data-stu-id="4fa85-113">Choose the **Report** action, and then choose the **Picking List by Order** action.</span></span>  
4. <span data-ttu-id="4fa85-114">Velja hnappinn **Prenta** til þess að prenta skýrslu eða velja hnappinn **Forskoðun** til að birta hana á skjánum.</span><span class="sxs-lookup"><span data-stu-id="4fa85-114">Choose the **Print** button to print the picking list or choose the **Preview** button to view it on the screen.</span></span>

<span data-ttu-id="4fa85-115">Einnig er hægt að vista tiltektarlistann sem skjal, til dæmis til að senda til einhvers eða til að bæta við sem viðhengi á sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="4fa85-115">You can also save the picking list as a document, for example, to send to someone or to add as an attachment to the sales order.</span></span> <span data-ttu-id="4fa85-116">Frekari upplýsingar er að finna í [Stjórna viðhengjum, tenglum og athugasemdum á spjöldum og fylgiskjölum](ui-how-add-link-to-record.md).</span><span class="sxs-lookup"><span data-stu-id="4fa85-116">For more information, see [Manage Attachments, Links, and Notes on Cards and Documents](ui-how-add-link-to-record.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4fa85-117">Ef þú notaðir aðgerðina **Opna uppskrift** á sölupöntuninni eru aðeins þættir tengds samsetningaríhlutar birtir í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="4fa85-117">If you used the **Explode BOM** function on the sales order, then only the components of the related assembly item are shown in the report.</span></span> <span data-ttu-id="4fa85-118">Nánari upplýsingar er að finna í [Vinna með uppskrift.](inventory-how-work-BOMs.md)</span><span class="sxs-lookup"><span data-stu-id="4fa85-118">For more information, see [Work with Bills of Material](inventory-how-work-BOMs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4fa85-119">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4fa85-119">See Also</span></span>  
[<span data-ttu-id="4fa85-120">Birgðir</span><span class="sxs-lookup"><span data-stu-id="4fa85-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="4fa85-121">Tína til vörur</span><span class="sxs-lookup"><span data-stu-id="4fa85-121">Pick Items</span></span>](warehouse-pick-items.md)  
<span data-ttu-id="4fa85-122">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4fa85-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>   


[!INCLUDE[footer-include](includes/footer-banner.md)]