---
title: Hvernig á að fjöldabóka notkun | Microsoft Docs
description: Ef flæðiaðferðin er stillt á **Handvirk** þarf að bóka íhlutina handvirkt með notkunarbók.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 821130831015d18e73557eb157241bc3415b97ac
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785497"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="a7a18-103">Fjöldabóka framleiðslunotkun</span><span class="sxs-lookup"><span data-stu-id="a7a18-103">Batch Post Production Consumption</span></span>
<span data-ttu-id="a7a18-104">Ef flæðiaðferðin er stillt á **Handvirk** þarf að bóka íhlutina handvirkt með notkunarbók.</span><span class="sxs-lookup"><span data-stu-id="a7a18-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>

<span data-ttu-id="a7a18-105">Þú getur einnig stillt kerfið þannig að það bóki sjálfvirkt (*flæða*) íhluti þegar byrjar eða endar framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="a7a18-105">You can also set the system up to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="a7a18-106">Nánari upplýsingar eru í [Leyfa flæði íhluta samkvæmt frálagi aðgerða](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="a7a18-106">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="a7a18-107">Bóka notkun fyrir eina eða fleiri framleiðslupantanalínur</span><span class="sxs-lookup"><span data-stu-id="a7a18-107">To post consumption for one or more production order lines</span></span>  
1.  <span data-ttu-id="a7a18-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notkunarbók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a7a18-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a7a18-109">Reitirnir eru fylltir út með framleiðslupöntunargögnunum og notkunargögnunum.</span><span class="sxs-lookup"><span data-stu-id="a7a18-109">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="a7a18-110">Ef vörugeymslan þar sem íhlutirnir eru geymdir er sett upp þannig að hún noti hólf en krefjist ekki tínslu skal tengja kóta hólfs bókarlínunni inn í reitinn til að sýna hvaðan eigi að taka vörurnar í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="a7a18-110">If the warehouse location where the components are stored is set up to use bins but does not require pick processing, assign a bin code to the journal line to indicate where the items should be taken from in the warehouse.</span></span> <span data-ttu-id="a7a18-111">Frekari upplýsingar eru í [Taka til fyrir framleiðslu eða samsetningu](warehouse-how-to-pick-for-production.md).</span><span class="sxs-lookup"><span data-stu-id="a7a18-111">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  
3.  <span data-ttu-id="a7a18-112">Velja **Bóka** aðgerðina til að bóka notkunina.</span><span class="sxs-lookup"><span data-stu-id="a7a18-112">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="a7a18-113">Tengdar birgðabókafærslur eru skertar.</span><span class="sxs-lookup"><span data-stu-id="a7a18-113">The related item ledger entries are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7a18-114">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a7a18-114">See Also</span></span>  
<span data-ttu-id="a7a18-115">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="a7a18-115">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="a7a18-116">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="a7a18-116">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="a7a18-117">[Áætlun](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="a7a18-117">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="a7a18-118">Birgðir</span><span class="sxs-lookup"><span data-stu-id="a7a18-118">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="a7a18-119">Innkaup</span><span class="sxs-lookup"><span data-stu-id="a7a18-119">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="a7a18-120">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a7a18-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
