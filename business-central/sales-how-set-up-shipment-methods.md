---
title: Hvernig á að setja upp afhendingarmáta | Microsoft Docs
description: Hægt er að setja upp kóða fyrir hvern afhendingarmáta sem boðið er upp á og slá inn upplýsingar um þá.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 75a3e689083e64f446e84b2bc3b1d26961e3d898
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877544"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="5e553-103">Afhendingarmátar settir upp</span><span class="sxs-lookup"><span data-stu-id="5e553-103">Set Up Shipment Methods</span></span>
<span data-ttu-id="5e553-104">Afhendingarmátar, einnig kallaðir inco-skilmálar, ráðast oft á vörunum, viðskiptamönnum og lánardrottnum.</span><span class="sxs-lookup"><span data-stu-id="5e553-104">Shipment methods, also called incoterms, often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="5e553-105">Ef viðskiptamaður býr til dæmis á eyju getur hann valið um að fá vörur alltaf sendar með flugi eða skipi.</span><span class="sxs-lookup"><span data-stu-id="5e553-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="5e553-106">Sumir viðskiptamenn gætu þurft afhendingu næsta dag.</span><span class="sxs-lookup"><span data-stu-id="5e553-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="5e553-107">Sumir gætu viljað sækja pöntunina.</span><span class="sxs-lookup"><span data-stu-id="5e553-107">Some may want to pick up the order.</span></span> <span data-ttu-id="5e553-108">Á viðskiptamanna- og lánardrottnaspjöldunum má tilgreina hvernig afhendingin á að vera.</span><span class="sxs-lookup"><span data-stu-id="5e553-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="5e553-109">Þú setur upp lýsingu og kóða fyrir hvern afhendingarmáta á síðunni **Afhendingarmátar**.</span><span class="sxs-lookup"><span data-stu-id="5e553-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="5e553-110">Hægt er til dæmis að stofna kóðann FOB og skrá Free on Board í reitinn **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="5e553-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="5e553-111">Síðan er hægt að skrá kóðann í reitina fyrir **Kóði afhendingarmáta** annars staðar í kerfinu, t.d. á viðskiptamannaspjald.</span><span class="sxs-lookup"><span data-stu-id="5e553-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="5e553-112">Síðan þegar þú stofnar nýjar pantanir, reikninga, kreditreikninga, o.s.frv. færir kerfið inn lýsinguna sem kóðinn stendur fyrir.</span><span class="sxs-lookup"><span data-stu-id="5e553-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="5e553-113">Hægt er að breyta honum í skjalinu eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="5e553-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-code"></a><span data-ttu-id="5e553-114">Uppsetning afhendingarkóða</span><span class="sxs-lookup"><span data-stu-id="5e553-114">To set up a shipment code</span></span>
1. <span data-ttu-id="5e553-115">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sendingaraðferð** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="5e553-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="5e553-116">Á síðunni **Afhendingarmátar** skal velja aðgerðina **Nýr**.</span><span class="sxs-lookup"><span data-stu-id="5e553-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="5e553-117">Á nýju línunni skal tilgreina kóða og lýsingu fyrir afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="5e553-117">On the new line, specify a code and description for the shipment method.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e553-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5e553-118">See Also</span></span>
[<span data-ttu-id="5e553-119">Inco-skilmálar</span><span class="sxs-lookup"><span data-stu-id="5e553-119">Incoterms</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  
[<span data-ttu-id="5e553-120">Uppsetning flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="5e553-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
<span data-ttu-id="5e553-121">[Finna sendingar](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="5e553-121">[Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="5e553-122">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="5e553-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="5e553-123">Birgðir</span><span class="sxs-lookup"><span data-stu-id="5e553-123">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5e553-124">[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="5e553-124">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="5e553-125">[Samsetningardeild](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="5e553-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="5e553-126">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="5e553-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="5e553-127">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5e553-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
