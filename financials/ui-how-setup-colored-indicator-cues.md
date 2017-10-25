---
title: "Tilgreina litaða vísa til að sérstilla sjónræn merki um virkni bendingar | Microsoft Docs"
description: "Setja upp litaðan vísi á ramma bendingar til að útvega sérsniðið sjónrænt merki um virkni bendingar."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0cb10770954f485d9c0a3474615e6c69411de321
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-a-colored-indicator-on-cues"></a><span data-ttu-id="983d2-103">Hvernig á að setja upp litaðan vísi á bunka</span><span class="sxs-lookup"><span data-stu-id="983d2-103">How to: Set Up a Colored Indicator on Cues</span></span>
<span data-ttu-id="983d2-104">Þú getur sett upp Bunka sem birtast í **heimasíðu** þannig að þeir innihaldi vísi sem breytir um lit eftir gagnagildum í bunkum.</span><span class="sxs-lookup"><span data-stu-id="983d2-104">You can set up Cues that appear on the **Home** page to include an indicator that changes color based on the data values in the Cues.</span></span>

<span data-ttu-id="983d2-105">Vísirinn birtist sem stika efst í ramma bendingarinnar.</span><span class="sxs-lookup"><span data-stu-id="983d2-105">The indicator appears as a colored bar along the top border of the Cue tile.</span></span> <span data-ttu-id="983d2-106">Veitir sjónrænt merki um virknistöðu bendingarinnar sem getur táknað hagstæð eða óhagstæð skilyrði sem kalla á viðbrögð frá notanda.</span><span class="sxs-lookup"><span data-stu-id="983d2-106">It provides a visual signal of the status of the Cue's activity, which can indicate favorable or unfavorable conditions to prompt the user to take action.</span></span> <span data-ttu-id="983d2-107">Ef bunki birtir til dæmis viðvarandi sölureikninga er hægt að stilla vísinn á að vera grænn (jákvætt) þegar heildarfjöldi viðvarandi sölureikninga er undir 10 og rauður (óæskilegt) þegar samtalan er yfir 20.</span><span class="sxs-lookup"><span data-stu-id="983d2-107">For example, if a Cue displays ongoing sales invoices, you can set up the indicator to appear green (favorable) when total number of ongoing sales invoices is below 10, and appears red (unfavorable) when the total is greater than 20.</span></span>

<span data-ttu-id="983d2-108">Í glugganum **uppsetning bunka** seturðu setja upp vísa fyrir allar bendingar sem eru tiltækar í gagnagrunni fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="983d2-108">From the **Cue Setup** window, you set up indicators for all the Cues that are available in the company database.</span></span>

<span data-ttu-id="983d2-109">Til að setja upp vísi tilgreinirðu allt að tvö þröskuldsgildi sem tilgreina þrjú svið gagnagilda (lágt, miðlungs og hátt) sem hægt er að nota annan lit (eða stíl) við.</span><span class="sxs-lookup"><span data-stu-id="983d2-109">To set up the indicator, you specify up to two threshold values that define three ranges of data values (low, middle, and high) to which you can apply a different color (or style).</span></span>

## <a name="to-set-up-colored-indicators-on-cues"></a><span data-ttu-id="983d2-110">Til að setja upp litaða vísa í bendingum</span><span class="sxs-lookup"><span data-stu-id="983d2-110">To set up colored indicators on Cues</span></span>
1. <span data-ttu-id="983d2-111">Undir **Aðgerðir** í notanda **Heimasíðu** , velja **Setja Upp bunka**.</span><span class="sxs-lookup"><span data-stu-id="983d2-111">Under **Activities** on your **Home** page, choose **Set Up Cues**.</span></span>  
   <span data-ttu-id="983d2-112">Glugginn **uppsetning bunka** birtist.</span><span class="sxs-lookup"><span data-stu-id="983d2-112">The **Cue Setup** window appears.</span></span> <span data-ttu-id="983d2-113">Glugginn birtir vísana sem nú eru uppsettir í bunkum.</span><span class="sxs-lookup"><span data-stu-id="983d2-113">The window lists the indicators that are currently setup up on Cues.</span></span>
2. <span data-ttu-id="983d2-114">Til að breyta vísi, breyta reitunum og breyta, t.d. gildi fyrir mismunandi þröskulda.</span><span class="sxs-lookup"><span data-stu-id="983d2-114">To modify an indicator, edit the fields and modify, for example, the values for the different thresholds.</span></span>  

<span data-ttu-id="983d2-115">Eftirfarandi tafla sýnir liti sem samsvara valkostir af sem **lágsviðsstíll**, **millisviðsstíll**, og **hásviðsstíll** reiti.</span><span class="sxs-lookup"><span data-stu-id="983d2-115">The following table lists the colors that correspond to the options of the **Low Range Style**, **Middle Range Style**, and **High Range Style** fields.</span></span>

| <span data-ttu-id="983d2-116">Valkostur</span><span class="sxs-lookup"><span data-stu-id="983d2-116">Option</span></span> | <span data-ttu-id="983d2-117">Litur</span><span class="sxs-lookup"><span data-stu-id="983d2-117">Color</span></span> |
| --- | --- |
| <span data-ttu-id="983d2-118">**Ekkert**</span><span class="sxs-lookup"><span data-stu-id="983d2-118">**None**</span></span> |<span data-ttu-id="983d2-119">Enginn litur (sami litur og í bunkareit)</span><span class="sxs-lookup"><span data-stu-id="983d2-119">No color (same color as the Cue tile</span></span> |
| <span data-ttu-id="983d2-120">**Hagstæð**</span><span class="sxs-lookup"><span data-stu-id="983d2-120">**Favorable**</span></span> |<span data-ttu-id="983d2-121">Grænt</span><span class="sxs-lookup"><span data-stu-id="983d2-121">Green</span></span> |
| <span data-ttu-id="983d2-122">**Óæskilegt**</span><span class="sxs-lookup"><span data-stu-id="983d2-122">**Unfavorable**</span></span> |<span data-ttu-id="983d2-123">Rautt</span><span class="sxs-lookup"><span data-stu-id="983d2-123">Red</span></span> |
| <span data-ttu-id="983d2-124">**Tvírætt**</span><span class="sxs-lookup"><span data-stu-id="983d2-124">**Ambiguous**</span></span> |<span data-ttu-id="983d2-125">Gult</span><span class="sxs-lookup"><span data-stu-id="983d2-125">Yellow</span></span> |
| <span data-ttu-id="983d2-126">**Undirstig**</span><span class="sxs-lookup"><span data-stu-id="983d2-126">**Subordinate**</span></span> |<span data-ttu-id="983d2-127">Grár</span><span class="sxs-lookup"><span data-stu-id="983d2-127">Gray</span></span> |

## <a name="see-also"></a><span data-ttu-id="983d2-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="983d2-128">See Also</span></span>
<span data-ttu-id="983d2-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="983d2-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

