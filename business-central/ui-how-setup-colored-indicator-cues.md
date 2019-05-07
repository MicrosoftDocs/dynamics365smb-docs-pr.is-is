---
title: Sérstilla sjónræn merki um virkni bendingar | Microsoft Docs
description: Setja upp litaðan vísi á ramma bendingar til að útvega sérsniðið sjónrænt merki um virkni bendingar.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 04/01/2019
ms.author: solsen
redirect_url: admin-how-set-up-colored-indicator-on-cues
ms.openlocfilehash: f79f1a65ee17d8ca46a8ecf1cd9d49c5246bef63
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "923439"
---
# <a name="set-up-a-colored-indicator-on-cues"></a><span data-ttu-id="e4f81-103">Setja upp litaðan vísi á bunka</span><span class="sxs-lookup"><span data-stu-id="e4f81-103">Set Up a Colored Indicator on Cues</span></span>
<span data-ttu-id="e4f81-104">Þú getur sett upp Bunka sem birtast í Mitt hlutverk þannig að þeir innihaldi vísi sem breytir um lit eftir gagnagildum í bunkum.</span><span class="sxs-lookup"><span data-stu-id="e4f81-104">You can set up Cues that appear on the Role Center to include an indicator that changes color based on the data values in the Cues.</span></span>

<span data-ttu-id="e4f81-105">Vísirinn birtist sem stika efst í ramma bendingarinnar.</span><span class="sxs-lookup"><span data-stu-id="e4f81-105">The indicator appears as a colored bar along the top border of the Cue tile.</span></span> <span data-ttu-id="e4f81-106">Veitir sjónrænt merki um virknistöðu bendingarinnar sem getur táknað hagstæð eða óhagstæð skilyrði sem kalla á viðbrögð frá notanda.</span><span class="sxs-lookup"><span data-stu-id="e4f81-106">It provides a visual signal of the status of the Cue's activity, which can indicate favorable or unfavorable conditions to prompt the user to take action.</span></span> <span data-ttu-id="e4f81-107">Ef bunki birtir til dæmis viðvarandi sölureikninga er hægt að stilla vísinn á að vera grænn (jákvætt) þegar heildarfjöldi viðvarandi sölureikninga er undir 10 og rauður (óæskilegt) þegar samtalan er yfir 20.</span><span class="sxs-lookup"><span data-stu-id="e4f81-107">For example, if a Cue displays ongoing sales invoices, you can set up the indicator to appear green (favorable) when total number of ongoing sales invoices is below 10, and appears red (unfavorable) when the total is greater than 20.</span></span>

<span data-ttu-id="e4f81-108">Á síðunni **uppsetning bunka** seturðu setja upp vísa fyrir allar bendingar sem eru tiltækar í gagnagrunni fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="e4f81-108">From the **Cue Setup** page, you set up indicators for all the Cues that are available in the company database.</span></span>

<span data-ttu-id="e4f81-109">Til að setja upp vísi tilgreinirðu allt að tvö þröskuldsgildi sem tilgreina þrjú svið gagnagilda (lágt, miðlungs og hátt) sem hægt er að nota annan lit (eða stíl) við.</span><span class="sxs-lookup"><span data-stu-id="e4f81-109">To set up the indicator, you specify up to two threshold values that define three ranges of data values (low, middle, and high) to which you can apply a different color (or style).</span></span>

## <a name="to-set-up-colored-indicators-on-cues"></a><span data-ttu-id="e4f81-110">Til að setja upp litaða vísa í bendingum</span><span class="sxs-lookup"><span data-stu-id="e4f81-110">To set up colored indicators on Cues</span></span>
1. <span data-ttu-id="e4f81-111">Undir **Aðgerðir** í Mitt hlutverk , velja **Setja Upp bunka**.</span><span class="sxs-lookup"><span data-stu-id="e4f81-111">Under **Activities** on your Role Center, choose **Set Up Cues**.</span></span>  
   <span data-ttu-id="e4f81-112">Síðan **Uppsetning bunka** birtist.</span><span class="sxs-lookup"><span data-stu-id="e4f81-112">The **Cue Setup** page appears.</span></span> <span data-ttu-id="e4f81-113">Síðan birtir vísana sem nú eru uppsettir í bunkum.</span><span class="sxs-lookup"><span data-stu-id="e4f81-113">The page lists the indicators that are currently setup up on Cues.</span></span>
2. <span data-ttu-id="e4f81-114">Til að breyta vísi, breyta reitunum og breyta, t.d. gildi fyrir mismunandi þröskulda.</span><span class="sxs-lookup"><span data-stu-id="e4f81-114">To modify an indicator, edit the fields and modify, for example, the values for the different thresholds.</span></span>  

<span data-ttu-id="e4f81-115">Eftirfarandi tafla sýnir liti sem samsvara valkostir af sem **lágsviðsstíll**, **millisviðsstíll**, og **hásviðsstíll** reiti.</span><span class="sxs-lookup"><span data-stu-id="e4f81-115">The following table lists the colors that correspond to the options of the **Low Range Style**, **Middle Range Style**, and **High Range Style** fields.</span></span>

| <span data-ttu-id="e4f81-116">Valkostur</span><span class="sxs-lookup"><span data-stu-id="e4f81-116">Option</span></span> | <span data-ttu-id="e4f81-117">Litur</span><span class="sxs-lookup"><span data-stu-id="e4f81-117">Color</span></span> |
| --- | --- |
| <span data-ttu-id="e4f81-118">**Ekkert**</span><span class="sxs-lookup"><span data-stu-id="e4f81-118">**None**</span></span> |<span data-ttu-id="e4f81-119">Enginn litur (sami litur og í bunkareit)</span><span class="sxs-lookup"><span data-stu-id="e4f81-119">No color (same color as the Cue tile)</span></span>|
| <span data-ttu-id="e4f81-120">**Hagstæð**</span><span class="sxs-lookup"><span data-stu-id="e4f81-120">**Favorable**</span></span> |<span data-ttu-id="e4f81-121">Grænt</span><span class="sxs-lookup"><span data-stu-id="e4f81-121">Green</span></span> |
| <span data-ttu-id="e4f81-122">**Slæmt**</span><span class="sxs-lookup"><span data-stu-id="e4f81-122">**Unfavorable**</span></span> |<span data-ttu-id="e4f81-123">Rautt</span><span class="sxs-lookup"><span data-stu-id="e4f81-123">Red</span></span> |
| <span data-ttu-id="e4f81-124">**Tvírætt**</span><span class="sxs-lookup"><span data-stu-id="e4f81-124">**Ambiguous**</span></span> |<span data-ttu-id="e4f81-125">Gult</span><span class="sxs-lookup"><span data-stu-id="e4f81-125">Yellow</span></span> |
| <span data-ttu-id="e4f81-126">**Undirstig**</span><span class="sxs-lookup"><span data-stu-id="e4f81-126">**Subordinate**</span></span> |<span data-ttu-id="e4f81-127">Grár</span><span class="sxs-lookup"><span data-stu-id="e4f81-127">Gray</span></span> |

## <a name="see-also"></a><span data-ttu-id="e4f81-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e4f81-128">See Also</span></span>
<span data-ttu-id="e4f81-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e4f81-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
