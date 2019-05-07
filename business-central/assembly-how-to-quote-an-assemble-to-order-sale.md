---
title: Hvernig á að búa til tilboð með samsetningarpöntun | Microsoft Docs
description: Hægt er að nota samsetningarstjórnun til að sérsníða samsetningaríhlut eftir beiðni viðskiptavinar á meðan söluferlinu stendur.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: b69433a365e6c67f31863f8289cddb21d0f7f4b7
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "936484"
---
# <a name="quote-an-assemble-to-order-sale"></a><span data-ttu-id="45903-103">Búa til tilboð með samsetningarpöntun</span><span class="sxs-lookup"><span data-stu-id="45903-103">Quote an Assemble-to-Order Sale</span></span>
<span data-ttu-id="45903-104">Hægt er að nota samsetningarstjórnun til að sérsníða samsetningaríhlut eftir beiðni viðskiptavinar á meðan söluferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="45903-104">You can use assembly management to customize an assembly item to a customer’s request during the sales process.</span></span> <span data-ttu-id="45903-105">Frekari upplýsingar eru í [Selja hluti sem eru settir saman í pöntun](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="45903-105">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

<span data-ttu-id="45903-106">Eins og þegar seld er hvers kyns önnur tegund af vöru, er einnig hægt að stofna sölutilboð fyrir sérsniðna samsetningarvöru áður en henni er umbreytt í sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="45903-106">As when you sell any other type of item, you can also create a sales quote for a customized assembly item before converting it to a sales order.</span></span> <span data-ttu-id="45903-107">Þetta ferli felur í sér nokkur aukaskref í samanburði við stofnun venjulegs standandi sölutilboðs, og notar afbrigði tengdrar samsetningarpöntunar, sem er samsetningartilboð.</span><span class="sxs-lookup"><span data-stu-id="45903-107">This process involves several extra steps when you compare it to creating a regular sales quote, and it uses a variation of a linked assembly order, which is an assembly quote.</span></span>

> [!NOTE]  
>  <span data-ttu-id="45903-108">Eins og allar gerðir á tilboðum er magn samsetningartilboða ekki notað til ráðstöfunar, í áætlun eða frátekt.</span><span class="sxs-lookup"><span data-stu-id="45903-108">Like all types of quotes, the quantities on assembly quotes are not used in availability, planning, or reservations.</span></span>  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a><span data-ttu-id="45903-109">Til að stofna sölutilboð fyrir vöru sem setja skal saman í pöntun</span><span class="sxs-lookup"><span data-stu-id="45903-109">To create a sales quote for an assemble-to-order item</span></span>  
1.  <span data-ttu-id="45903-110">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **sölutilboð** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="45903-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Quote**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="45903-111">Stofna nýja sölupöntunarlínu með eina línu fyrir samsetningaríhlut.</span><span class="sxs-lookup"><span data-stu-id="45903-111">Create a sales quote line with one line for an assembly item.</span></span> <span data-ttu-id="45903-112">Frekari upplýsingar er að finna í [Búa til sölutilboð](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="45903-112">For more information, see [Make Sales Quotes](sales-how-make-offers.md).</span></span>  
3.  <span data-ttu-id="45903-113">Í reitnum **Magn til samsetningar til pöntunar** skal færa inn fullt magn.</span><span class="sxs-lookup"><span data-stu-id="45903-113">In the **Qty. to Assemble to Order** field, enter the full quantity.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="45903-114">Ekki ætti að gera tilboð í hlutamagn.</span><span class="sxs-lookup"><span data-stu-id="45903-114">You should not quote a partial quantity.</span></span> <span data-ttu-id="45903-115">Því verður að færa inn sama magn og fært var inn í reitinn **Magn** í sölutilboðslínunni.</span><span class="sxs-lookup"><span data-stu-id="45903-115">Therefore, you must enter the same quantity that you entered in the **Quantity** field on the sales quote line.</span></span>  

4.  <span data-ttu-id="45903-116">Á flýtiflipanum skal velja **Línur**, velja **Lína**, velja **Samsetning til pöntunar** og síðan **Setja saman í pöntunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="45903-116">On the **Lines** FastTab, choose **Line**, choose **Assemble to Order**, and then choose **Assemble-to-Order Lines**.</span></span> <span data-ttu-id="45903-117">Að öðrum kosti skal velja reitinn **Magn til samsetningar til pöntunar** í línunni.</span><span class="sxs-lookup"><span data-stu-id="45903-117">Alternatively, choose the **Qty. to Assemble to Order** field on the line.</span></span>  
5.  <span data-ttu-id="45903-118">Á síðunni **Setja saman í pöntunarlínu** endurskoðið og breytið samsetningu pöntunalína samkvæmt tilboði standandi pöntunar sem viðskiptamaðurinn hefur farið fram á.</span><span class="sxs-lookup"><span data-stu-id="45903-118">On the **Assemble-to-Order Lines** page, review or modify the assembly order lines according to the quote that the customer is requesting.</span></span> <span data-ttu-id="45903-119">Ef skoða á nánari upplýsingar skal velja aðgerðina **Sýna fylgiskjal** til að opna tilboð standandi pöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="45903-119">If you want to view more information, choose the **Show Document** action to open the complete blanket quote order.</span></span> <span data-ttu-id="45903-120">Ekki er hægt að breyta innihaldi i flestum reitum, og ekki er hægt að bóka.</span><span class="sxs-lookup"><span data-stu-id="45903-120">You cannot change the contents of most fields, and you cannot post.</span></span>  
6.  <span data-ttu-id="45903-121">Þegar búið er að leiðrétta samsetningarpöntunarlínur samkvæmt tilboðinu skal loka síðunni **Sameina-í-pöntun línur** til að fara aftur á síðuna **Sölutilboð** .</span><span class="sxs-lookup"><span data-stu-id="45903-121">When you have adjusted the assembly order lines according to the quote, close the **Assemble-to-Order Lines** page to return to the **Sales Quote** page.</span></span>  
7.  <span data-ttu-id="45903-122">Ef viðskiptamaðurinn samþykkir tilboðið skal stofna sölupöntun fyrir samsetningaríhlut tilboðsins.</span><span class="sxs-lookup"><span data-stu-id="45903-122">If the customer accepts the quote, then create a sales order for the quoted assembly item.</span></span> <span data-ttu-id="45903-123">Frekari upplýsingar er að finna í [Búa til sölutilboð](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="45903-123">For more information, see [Make Sales Quotes](sales-how-make-offers.md).</span></span> <span data-ttu-id="45903-124">Tengt samsetningartilboð og allar sérstillingar tengjast við þessa nýju sölupöntun til undirbúnings á samsetningu vöru eða vörum sem á að selja.</span><span class="sxs-lookup"><span data-stu-id="45903-124">The linked assembly quote and any customizations are linked to that new sales order to prepare for assembly of the item or items to be sold.</span></span>  

## <a name="see-also"></a><span data-ttu-id="45903-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="45903-125">See Also</span></span>  
[<span data-ttu-id="45903-126">Samsetningardeild</span><span class="sxs-lookup"><span data-stu-id="45903-126">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="45903-127">Vinna með uppskriftir</span><span class="sxs-lookup"><span data-stu-id="45903-127">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="45903-128">Birgðir</span><span class="sxs-lookup"><span data-stu-id="45903-128">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="45903-129">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="45903-129">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="45903-130">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="45903-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
