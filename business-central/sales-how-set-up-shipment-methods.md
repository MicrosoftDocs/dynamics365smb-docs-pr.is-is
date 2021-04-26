---
title: Afhendingarmátar settir upp
description: Hægt er að setja upp kóða fyrir hvern afhendingarmáta sem boðið er upp á og slá inn upplýsingar um þá.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8390c95083eb02c208e97f0309a725e8ec4d7730
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778573"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="d1d4a-103">Afhendingarmátar settir upp</span><span class="sxs-lookup"><span data-stu-id="d1d4a-103">Set Up Shipment Methods</span></span>

<span data-ttu-id="d1d4a-104">Afhendingarmáti ræðst oft af vörunni sjálfri, viðskiptamönnum eða lánardrottnum.</span><span class="sxs-lookup"><span data-stu-id="d1d4a-104">Shipment methods often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="d1d4a-105">Ef viðskiptamaður býr til dæmis á eyju getur hann valið um að fá vörur alltaf sendar með flugi eða skipi.</span><span class="sxs-lookup"><span data-stu-id="d1d4a-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="d1d4a-106">Sumir viðskiptamenn gætu þurft afhendingu næsta dag.</span><span class="sxs-lookup"><span data-stu-id="d1d4a-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="d1d4a-107">Sumir gætu viljað sækja pöntunina.</span><span class="sxs-lookup"><span data-stu-id="d1d4a-107">Some may want to pick up the order.</span></span> <span data-ttu-id="d1d4a-108">Á viðskiptamanna- og lánardrottnaspjöldunum má tilgreina hvernig afhendingin á að vera.</span><span class="sxs-lookup"><span data-stu-id="d1d4a-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="d1d4a-109">Þú setur upp lýsingu og kóða fyrir hvern afhendingarmáta á síðunni **Afhendingarmátar**.</span><span class="sxs-lookup"><span data-stu-id="d1d4a-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="d1d4a-110">Hægt er til dæmis að stofna kóðann FOB og skrá Free on Board í reitinn **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="d1d4a-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="d1d4a-111">Síðan er hægt að skrá kóðann í reitina fyrir **Kóði afhendingarmáta** annars staðar í kerfinu, t.d. á viðskiptamannaspjald.</span><span class="sxs-lookup"><span data-stu-id="d1d4a-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="d1d4a-112">Síðan þegar þú stofnar nýjar pantanir, reikninga, kreditreikninga, o.s.frv. færir kerfið inn lýsinguna sem kóðinn stendur fyrir.</span><span class="sxs-lookup"><span data-stu-id="d1d4a-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="d1d4a-113">Hægt er að breyta honum í skjalinu eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="d1d4a-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-method"></a><span data-ttu-id="d1d4a-114">afhendingarmátar settir upp</span><span class="sxs-lookup"><span data-stu-id="d1d4a-114">To set up a shipment method</span></span>

1. <span data-ttu-id="d1d4a-115">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sendingaraðferð** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="d1d4a-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="d1d4a-116">Á síðunni **Afhendingarmátar** skal velja aðgerðina **Nýr**.</span><span class="sxs-lookup"><span data-stu-id="d1d4a-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="d1d4a-117">Á nýju línunni skal tilgreina kóða og lýsingu fyrir afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="d1d4a-117">On the new line, specify a code and description for the shipment method.</span></span>

> [!TIP]
> <span data-ttu-id="d1d4a-118">Ef Incoterms er notað skal setja upp sendingaraðferðir til að tákna viðeigandi Incoterms-reglur.</span><span class="sxs-lookup"><span data-stu-id="d1d4a-118">If you use Incoterms, set up shipment methods to represent the relevant Incoterms rules.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d1d4a-119">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d1d4a-119">See Also</span></span>

[<span data-ttu-id="d1d4a-120">Uppsetning flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="d1d4a-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
[<span data-ttu-id="d1d4a-121">Finna sendingar</span><span class="sxs-lookup"><span data-stu-id="d1d4a-121">Track Packages</span></span>](sales-how-track-packages.md)  
[<span data-ttu-id="d1d4a-122">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="d1d4a-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="d1d4a-123">Birgðir</span><span class="sxs-lookup"><span data-stu-id="d1d4a-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="d1d4a-124">Vöruhúsastjórnun sett upp</span><span class="sxs-lookup"><span data-stu-id="d1d4a-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="d1d4a-125">Samsetningardeild</span><span class="sxs-lookup"><span data-stu-id="d1d4a-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="d1d4a-126">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="d1d4a-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="d1d4a-127">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d1d4a-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="d1d4a-128">Incoterms á iccwbo.org</span><span class="sxs-lookup"><span data-stu-id="d1d4a-128">Incoterms on iccwbo.org</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]