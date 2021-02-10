---
title: Skilgreina almenna birgðauppsetningu
description: Lýsir því hvernig á að skilgreina almenna uppsetningu birgða þannig að hægt sé að stjórna vöruhúsinu og birgðum.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e3ecf8d206e50244c19a820bdb67d2992cbefe36
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746367"
---
# <a name="set-up-general-inventory-information"></a><span data-ttu-id="75ccf-103">Setja upp almennar birgðaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="75ccf-103">Set Up General Inventory Information</span></span>

<span data-ttu-id="75ccf-104">Almennar birgðaupplýsingar eru tilgreindar á síðunni **Birgðagrunnur**.</span><span class="sxs-lookup"><span data-stu-id="75ccf-104">You specify your general inventory setup on the **Inventory Setup** page.</span></span>

## <a name="to-set-up-general-inventory-information"></a><span data-ttu-id="75ccf-105">Til að setja upp almennar birgðaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="75ccf-105">To set up general inventory information</span></span>

1. <span data-ttu-id="75ccf-106">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Birgðauppsetning** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="75ccf-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="75ccf-107">Á síðunni **Birgðagrunnur** skal fylla út reitina eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="75ccf-107">On the **Inventory Setup** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="75ccf-108">Ítarlegar upplýsingar um kostnaðarreitina **Sjálfvirk kostnaðarbókun** og **Væntanleg kostnaðarbókun á fjárhag** og **Sjálfgefin aðferð kostnaðarútreiknings** er að finna í [Afstemma birgðakostnað í fjárhag](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md) og [Hönnunarupplýsingar: Væntanleg kostnaðarfærsla](design-details-expected-cost-posting.md).</span><span class="sxs-lookup"><span data-stu-id="75ccf-108">For detailed information about the costing fields, **Automatic Cost Posting**, **Expected Cost Posting to G/L**, and **Default Costing Method**, see [Reconcile Inventory Costs with the General Ledger](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Design Details: Inventory Costing](design-details-inventory-costing.md), and [Design Details: Expected Cost Posting](design-details-expected-cost-posting.md).</span></span> <span data-ttu-id="75ccf-109">Frekari upplýsingar um almennan kostnaðarútreikning er að finna í [Stjórnun birgðakostnaðar](finance-manage-inventory-costs.md).</span><span class="sxs-lookup"><span data-stu-id="75ccf-109">For more information about costing in general, see [Managing Inventory Costs](finance-manage-inventory-costs.md).</span></span>  

<span data-ttu-id="75ccf-110">Ef afgreiðslutími á vörum inn í vöruhús á að vera tekinn með þegar reiknað er út hvenær pöntun er lofað í innkaupalínu er hægt að setja þetta upp sem sjálfgefið fyrir birgðirnar á síðunni **Birgðagrunnur** og fyrir staðsetninguna þína.</span><span class="sxs-lookup"><span data-stu-id="75ccf-110">If you want to include warehouse handling time in the order promising calculation on the purchase line, you can set it up as a default for the inventory, on the **Inventory Setup** page, and for your location.</span></span> <span data-ttu-id="75ccf-111">Nánari upplýsingar er að finna í [Reikna dagsetningar pöntunarloforða](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="75ccf-111">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="75ccf-112">Kveikt er á **Sjálfvirk kostnaðarleiðrétting** að sjálfgefnu til að tryggja að birgðavirði sé alltaf rétt í fjárhag, sem fyrir vikið heldur sölu- og hagnaðartölum uppfærðum.</span><span class="sxs-lookup"><span data-stu-id="75ccf-112">The **Automatic Cost Adjustment** toggle is turned on by default to ensure that inventory values are always correct in the general ledger, which in turn keeps your sales and profit statistics up to date.</span></span> <span data-ttu-id="75ccf-113">Kostnaðarbreytingum úr færslum á innleið, til dæmis færslur fyrir innkaup eða framleiðslufrálag, er úthlutað á tengdar færslur á útleið, t.d. sölu og flutninga.</span><span class="sxs-lookup"><span data-stu-id="75ccf-113">Cost changes from inbound entries, such as those for purchases or production output, are assigned to the related outbound entries, such as sales or transfers.</span></span> <span data-ttu-id="75ccf-114">Þetta er gagnlegt fyrir nýja [!INCLUDE[prod_short](includes/prod_short.md)] viðskiptavini og lítil fyrirtæki með tiltölulega lágt birgðafærslustig.</span><span class="sxs-lookup"><span data-stu-id="75ccf-114">This is helpful for new [!INCLUDE[prod_short](includes/prod_short.md)] customers and small businesses with relatively low inventory transaction levels.</span></span> <span data-ttu-id="75ccf-115">Þegar fyrirtæki hinsvegar stækkar og birgðastöður aukast getur þetta hægt á afköst kerfisins.</span><span class="sxs-lookup"><span data-stu-id="75ccf-115">However, as a business grows and inventory levels increase, this can slow down system performance.</span></span> <span data-ttu-id="75ccf-116">Til að lágmarka minnkuð afköst við bókun skal velja tímavalkost til að skilgreina hversu langt aftur í tímann frá vinnudagsetningu færsla á innleið getur átt sér stað til að hugsanlega ræsa leiðréttingu á tengdum virðisfærslum á útleið.</span><span class="sxs-lookup"><span data-stu-id="75ccf-116">To minimize reduced performance during posting, select a time option to define how far back in time from the work date an inbound transaction can occur to potentially trigger adjustment of related outbound value entries.</span></span> <span data-ttu-id="75ccf-117">Að öðrum kosti er handvirkt hægt að leiðrétta kostnað með reglulegu millibili með runuvinnslunni Leiðrétta kostnað - Vörufærslur.</span><span class="sxs-lookup"><span data-stu-id="75ccf-117">Alternatively, you can manually adjust costs at regular intervals with the Adjust Cost - Item Entries batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="75ccf-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="75ccf-118">See Also</span></span>
[<span data-ttu-id="75ccf-119">Setja upp birgðir</span><span class="sxs-lookup"><span data-stu-id="75ccf-119">Set Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="75ccf-120">[Hönnunarupplýsingar: Aðferð kostn.útreiknings](design-details-costing-methods.md)  </span><span class="sxs-lookup"><span data-stu-id="75ccf-120">[Design Details: Costing Methods](design-details-costing-methods.md)  </span></span>  
[<span data-ttu-id="75ccf-121">Stjórna birgðum</span><span class="sxs-lookup"><span data-stu-id="75ccf-121">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="75ccf-122">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="75ccf-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="75ccf-123">Breyta því hvaða eiginleikar eru sýndir</span><span class="sxs-lookup"><span data-stu-id="75ccf-123">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="75ccf-124">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="75ccf-124">General Business Functionality</span></span>](ui-across-business-areas.md)
