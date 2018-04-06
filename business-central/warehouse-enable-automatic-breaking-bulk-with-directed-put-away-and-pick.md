---
title: "Sjálfvirk einingaskipti með beinum frágangi og tínslu | Microsoft Docs"
description: "Í birgðageymslum sem nota beinan frágang og tínslu er hægt að skipta stærri mælieiningum í smærri þegar stofnaðar eru vöruhúsaleiðbeiningar sem uppfylla þarfir upprunaskjala, framleiðslupantana eða tínslu og frágangs innanhúss."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 20293bc9e17fd3fe03466a55d0b74b5104cd17f2
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a><span data-ttu-id="f2ca2-103">Virkja sjálfvirk einingaskipti með beinum frágangi og tínslu</span><span class="sxs-lookup"><span data-stu-id="f2ca2-103">Enable Automatic Breaking Bulk with Directed Put-away and Pick</span></span>
<span data-ttu-id="f2ca2-104">Í birgðageymslum sem nota beinan frágang og tínslu er hægt að skipta einingum sjálfkrafa í [!INCLUDE[d365fin](includes/d365fin_md.md)], það er, skipta stærri mælieiningum í smærri þegar stofnaðar eru vöruhúsaleiðbeiningar sem uppfylla þarfir upprunaskjala, framleiðslupantana eða tínslu og frágangs innanhúss.</span><span class="sxs-lookup"><span data-stu-id="f2ca2-104">For locations that use directed put-away and pick, [!INCLUDE[d365fin](includes/d365fin_md.md)] can, in various situations, automatically breakbulk, that is, break a larger unit of measure into smaller units of measure, when it creates warehouse instructions that fulfill the needs of source documents, production orders, or internal picks and put-aways.</span></span> <span data-ttu-id="f2ca2-105">Að skipta einingum getur stundum einnig þýtt að safna saman smærri mælieiningum, ef með þarf, til að mæta útleiðarbeiðnum með því að skipta stærri mælieiningum upprunaskjalsins eða framleiðslupöntunarinnar í smærri mælieiningar sem tiltækar eru í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="f2ca2-105">To breakbulk sometimes also means gathering smaller units of measure, if necessary, to meet outbound requests by breaking the larger unit of measure on the source document or production order into the smaller units of measure that are available in the warehouse.</span></span>   

## <a name="breakbulking-in-picks"></a><span data-ttu-id="f2ca2-106">Einingum er skipt í tínslum</span><span class="sxs-lookup"><span data-stu-id="f2ca2-106">Breakbulking in Picks</span></span>  
<span data-ttu-id="f2ca2-107">Ef geyma á vörur í nokkrum mismunandi mælieiningum og leyfa að sameina þær sjálfkrafa í tínsluferlinu, skal velja reitinn **Leyfa einingaskipti** á birgðageymsluspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="f2ca2-107">If you want to store items in several different units of measure and allow them to be automatically combined as needed in the picking process, select the **Allow Breakbulk** field on the location card.</span></span>  

<span data-ttu-id="f2ca2-108">Til að ljúka verki er sjálfkrafa leitað að vöru með sömu mælieiningu.</span><span class="sxs-lookup"><span data-stu-id="f2ca2-108">To fulfill a task, the program automatically looks for an item in the same unit of measure.</span></span> <span data-ttu-id="f2ca2-109">En ef ekki er hægt að finna vöruna með þeim forsendum og reitur er valinn, verður lagt til í kerfinu að skipta stærri mælieiningu í mælieininguna sem þörf er á.</span><span class="sxs-lookup"><span data-stu-id="f2ca2-109">But if it cannot find this form of the item, and this field is selected, the program will suggest that you break a larger unit of measure into the unit of measure that is needed.</span></span>  

<span data-ttu-id="f2ca2-110">Ef kerfið finnur aðeins smærri mælieiningar er lagt til að vöru sé safnað saman til að fylla upp í magnið í afhendingunni eða framleiðslupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="f2ca2-110">If the system can only find smaller units of measure, it will suggest that you gather items to fulfill the quantity on the shipment or production order.</span></span> <span data-ttu-id="f2ca2-111">Í raun er stærri mælieiningunum á upprunaskjalinu í smærri einingar fyrir tínslu.</span><span class="sxs-lookup"><span data-stu-id="f2ca2-111">In effect, it breaks the larger unit of measure on the source document into smaller units for picking.</span></span>  

## <a name="breakbulking-in-put-aways"></a><span data-ttu-id="f2ca2-112">Einingum skipt í frágangi</span><span class="sxs-lookup"><span data-stu-id="f2ca2-112">Breakbulking in Put-aways</span></span>  
<span data-ttu-id="f2ca2-113">Í vöruhúsafrágangi eru sjálfkrafa lagðar til Setja-aðgerðarlínur í mælieiningu frágangs, til dæmis stykkjum, jafnvel þótt vörurnar berist með annarri mælieiningu.</span><span class="sxs-lookup"><span data-stu-id="f2ca2-113">In the warehouse put-away, the program automatically suggests Place action lines in the put-away unit of measure, for example, pieces, even though the items arrive in a different unit of measure.</span></span>  

## <a name="breakbulking-in-movements"></a><span data-ttu-id="f2ca2-114">Einingum skipt í hreyfingum</span><span class="sxs-lookup"><span data-stu-id="f2ca2-114">Breakbulking in Movements</span></span>  
<span data-ttu-id="f2ca2-115">Kerfið skiptir einingum einnig sjálfkrafa í áfyllingarhreyfingum ef sjálfgefna gátmerkið í reitnum **Leyfa einingaskipti** á flýtiflipanum **Valkostur** í glugganum **Reikna áfyllingu hólfs** er ekki fjarlægt.</span><span class="sxs-lookup"><span data-stu-id="f2ca2-115">The program also breakbulks automatically in replenishment movements, if the **Allow Breakbulk** field is selected on the **Option** FastTab in the **Calculate Bin Replenishment** window.</span></span>  

<span data-ttu-id="f2ca2-116">Hægt er að skoða niðurstöðu umreikninga úr einni mælieiningu í aðra í einingaskiptalínum í frágangs-, tínslu- eða hreyfingaleiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="f2ca2-116">You can view the results of the conversion process from one unit of measure to another as intermediate breakbulk lines in the put-away, pick, or movement instructions.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f2ca2-117">Ef reiturinn **Einingaskiptaafmörkun** er valinn í haus vöruhúsaleiðbeininga mun kerfið fela einingaskiptalínur þegar stærri mælieiningin mun verða notuð að fullu.</span><span class="sxs-lookup"><span data-stu-id="f2ca2-117">If you select the **Set Breakbulk Filter** field on the warehouse instruction header, the program will hide the breakbulk lines whenever the larger unit of measure is going to be completely used.</span></span> <span data-ttu-id="f2ca2-118">Ef 12 stykki eru á bretti og nota á öll 12 stykkin er notandanum bent á að taka 1 bretti og setja 12 stykki.</span><span class="sxs-lookup"><span data-stu-id="f2ca2-118">For example, if a pallet is 12 pieces and you are going to use all 12 pieces, the pick will then direct you to take 1 pallet and place 12 pieces.</span></span> <span data-ttu-id="f2ca2-119">Þurfi hins vegar aðeins að tína 9 stykki eru einingaskiptalínurnar ekki faldar, jafnvel þó reiturinn **Einingaskiptaafmörkun** sé valinn því að einhvers staðar þarf að setja hin þrjú stykkin í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="f2ca2-119">However, if you have to pick only 9 pieces, then the breakbulk lines will not be hidden, even if you have selected the **Breakbulk Filter** field, because you have to place the remaining three pieces somewhere in the warehouse.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f2ca2-120">Ef mælieiningarnar eiga að skila hámarksafköstum í vöruhúsinu, einnig í tengslum við einingaskiptaaðgerðir, skal reyna eins og kostur er að:</span><span class="sxs-lookup"><span data-stu-id="f2ca2-120">If you want your units of measure to perform optimally in the warehouse, also in connection with the breakbulk functionality, you should wherever possible try to:</span></span>  
>   
> - <span data-ttu-id="f2ca2-121">Setja upp grunnmælieiningu sem minnstu mælieininguna sem búist er við að unnið verði með í vöruhúsaferlum.</span><span class="sxs-lookup"><span data-stu-id="f2ca2-121">Set up the base unit of measure for an item as the smallest unit of measure that you expect to handle in your warehouse processes.</span></span>  
> - <span data-ttu-id="f2ca2-122">Setja upp aukamælieiningar fyrir vöruna sem er margfeldi af grunnmælieiningunni.</span><span class="sxs-lookup"><span data-stu-id="f2ca2-122">Set up your alternative units of measure for the item as multiples of the base unit of measure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f2ca2-123">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f2ca2-123">See Also</span></span>  
[<span data-ttu-id="f2ca2-124">Vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="f2ca2-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="f2ca2-125">Birgðir</span><span class="sxs-lookup"><span data-stu-id="f2ca2-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="f2ca2-126">[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="f2ca2-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="f2ca2-127">[Samsetningardeild](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="f2ca2-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="f2ca2-128">Hönnunarupplýsingar vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="f2ca2-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="f2ca2-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f2ca2-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

