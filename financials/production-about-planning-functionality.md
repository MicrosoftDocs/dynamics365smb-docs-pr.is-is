---
title: "Um áætlunaraðgerðir | Microsoft Docs"
description: "Áætlunarkerfið tekur öll gögn um eftirspurn og framboð með í reikninginn, reiknar út niðurstöðurnar og kemur með tillögur að því að jafna framboðið og eftirspurnina."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: 25c32365ea662bb5c2ad1015aa03a5aab2307d17
ms.contentlocale: is-is
ms.lasthandoff: 04/16/2018

---
# <a name="about-planning-functionality"></a><span data-ttu-id="10e3c-103">Um áætlunaraðgerðir</span><span class="sxs-lookup"><span data-stu-id="10e3c-103">About Planning Functionality</span></span>
<span data-ttu-id="10e3c-104">Áætlunarkerfið tekur öll gögn um eftirspurn og framboð með í reikninginn, reiknar út niðurstöðurnar og kemur með tillögur að því að jafna framboðið og eftirspurnina.</span><span class="sxs-lookup"><span data-stu-id="10e3c-104">The planning system takes all demand and supply data into account, nets the results, and creates suggestions for balancing the supply to meet the demand.</span></span>  

<span data-ttu-id="10e3c-105">Frekari og nákvæmari upplýsingar, sjá [Hönnunarupplýsingar: Framboðsáætlun](design-details-supply-planning.md)</span><span class="sxs-lookup"><span data-stu-id="10e3c-105">For detailed information, see [Design Details: Supply Planning](design-details-supply-planning.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="10e3c-106">Fyrir öll þau svið sem minnst er á í þessu efnisatriði, lesa ábendingarnar til að skilja virkni þeirra.</span><span class="sxs-lookup"><span data-stu-id="10e3c-106">For all the fields that are mentioned in this topic, read the tooltip to understand their function.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a><span data-ttu-id="10e3c-107">Eftirspurn og Framboð</span><span class="sxs-lookup"><span data-stu-id="10e3c-107">Demand and Supply</span></span>  
<span data-ttu-id="10e3c-108">Áætlanagerð hefur tvo hluta: eftirspurn og framboð.</span><span class="sxs-lookup"><span data-stu-id="10e3c-108">Planning has two elements: demand and supply.</span></span> <span data-ttu-id="10e3c-109">Halda þarf þeim í jafnvægi til að tryggja það að eftirspurninni sé annað á tímanlegan og hagkvæman hátt.</span><span class="sxs-lookup"><span data-stu-id="10e3c-109">These must be held in balance to ensure that the demand is met in a timely and cost-efficient manner.</span></span>  

- <span data-ttu-id="10e3c-110">Eftirspurn er notað sem almennt heiti yfir hvers konar brúttóþörf eins og sölupöntun, þjónustupöntun, íhlutaþörf frá samsetningu eða framleiðslupantanir, millifærslur á útleið, standandi pöntun eða spá.</span><span class="sxs-lookup"><span data-stu-id="10e3c-110">Demand is the common term used for any kind of gross requirement such as a sales order, service order, component need from assembly or production orders, outbound transfer, blanket order or forecast.</span></span> <span data-ttu-id="10e3c-111">Þar að auki býður kerfið upp á nokkrar aðrar tæknilegar tegundir eftirspurnar - eins og neikvæða framleiðslu- eða innkaupapöntun, neikvætt birgðamat og innkaupaskil.</span><span class="sxs-lookup"><span data-stu-id="10e3c-111">In addition to these, the program allows some other technical types of demand - such as a negative production or purchase order, negative inventory, and purchase return.</span></span>  
- <span data-ttu-id="10e3c-112">Framboð er það orð sem er mest notað fyrir hvaða tegund af áfyllingu sem er, eins og birgðir, innkaupapöntun, samsetningarpöntun, framleiðslupöntun eða millifærslu á innleið.</span><span class="sxs-lookup"><span data-stu-id="10e3c-112">Supply is the common word used for any kind of replenishment such as inventory, a purchase order, assembly order, production order, or inbound transfer.</span></span> <span data-ttu-id="10e3c-113">Á sama hátt getur verið til neikvæð sölu- eða þjónustupöntun, neikvæð íhlutaþörf eða innkaupaskil – sem er allt á einhvern hátt dæmi um framboð.</span><span class="sxs-lookup"><span data-stu-id="10e3c-113">Correspondingly, there can be a negative sales or service order, negative component need or sales return – all of which in some way also represent supply.</span></span>  

<span data-ttu-id="10e3c-114">Annað markmið áætlunarkerfisins er að tryggja það að birgðamagnið hækki ekki að óþörfu.</span><span class="sxs-lookup"><span data-stu-id="10e3c-114">Another goal of the planning system is to ensure that the inventory does not grow unnecessarily.</span></span> <span data-ttu-id="10e3c-115">Í tilfelli minnkandi eftirspurnar mun áætlunarkerfið leggja til að annað hvort verði þeim áfyllingarpöntunum sem eru fyrir hendi frestað, þær minnkaðar eða afpantaðar.</span><span class="sxs-lookup"><span data-stu-id="10e3c-115">In the case of decreasing demand, the planning system will suggest that you postpone, decrease in quantity, or cancel existing replenishment orders.</span></span>  

## <a name="planning-calculation"></a><span data-ttu-id="10e3c-116">Áætlunarútreikningur</span><span class="sxs-lookup"><span data-stu-id="10e3c-116">Planning Calculation</span></span>  
<span data-ttu-id="10e3c-117">Áætlunarkerfið er knúið áfram af viðbúinni og raunverulegri eftirspurn viðskiptavina auk endurpöntunarfæribreytum birgða.</span><span class="sxs-lookup"><span data-stu-id="10e3c-117">The planning system is driven by anticipated and actual customer demand, as well as inventory reordering parameters.</span></span> <span data-ttu-id="10e3c-118">Ef áætlunarútreikningurinn er keyrður mun það leiða til þess að kerfið leggi til sérstakar aðgerðir (Aðgerðarboð) til að framkvæma varðandi mögulega áfyllingu frá lánardrottnum, millifærslur á milli vöruhúsa eða framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="10e3c-118">Running the planning calculation will result in the program suggesting specific actions (Action Messages) to take concerning possible replenishment from vendors, transfers between warehouses, or production.</span></span> <span data-ttu-id="10e3c-119">Ef áfyllingarpantanir eru þegar til gætu tillögurnar verið þess efnis að auka við pantanirnar eða flýta þeim til að koma til móts við eftirspurnarbreytingarnar.</span><span class="sxs-lookup"><span data-stu-id="10e3c-119">If replenishment orders already exist, the suggested actions could be to increase or expedite the orders to meet the changes in demand.</span></span>  

<span data-ttu-id="10e3c-120">Grundvöllur áætlunarrútínunnar er í útreikningunum frá hagnaði til taps.</span><span class="sxs-lookup"><span data-stu-id="10e3c-120">The basis of the planning routine is in the gross-to-net calculation.</span></span> <span data-ttu-id="10e3c-121">Nettóþarfir knýja áætlaða útgáfu pantana sem eru tímasettar eftir leiðarupplýsingum (framleiddar vörur) eða afhendingartíma birgðaspjaldsins (keyptar vörur).</span><span class="sxs-lookup"><span data-stu-id="10e3c-121">Net requirements drive planned order releases, which are scheduled based on the routing information (manufactured items) or the item card lead time (purchased items).</span></span> <span data-ttu-id="10e3c-122">Magn áætlaðrar útgáfu pöntunar er byggt á áætlunarútreikningunum og verður fyrir áhrifum af þeim færibreytum sem eru stilltar fyrir hvert stakt birgðaspjald.</span><span class="sxs-lookup"><span data-stu-id="10e3c-122">Planned order release quantities are based on the planning calculation, and are affected by the parameters set on the individual item cards.</span></span>  

## <a name="planning-with-manual-transfer-orders"></a><span data-ttu-id="10e3c-123">Áætlað með handvirkum millifærslupöntunum</span><span class="sxs-lookup"><span data-stu-id="10e3c-123">Planning with Manual Transfer Orders</span></span>
<span data-ttu-id="10e3c-124">Eins og sjá má í reitnum **Áfyllingarkerfið** á birgðahaldseiningarspjaldi er hægt að setja áætlunarkerfið upp til að stofna millifærslupantanir til að jafna framboð og eftirspurn á milli birgðageymslna.</span><span class="sxs-lookup"><span data-stu-id="10e3c-124">As you can see from the **Replenishment System** field on a SKU card, the planning system can be set up to create transfer orders to balance supply and demand across locations.</span></span>  

<span data-ttu-id="10e3c-125">Til viðbótar slíkum sjálfvirkum millifærslupöntunum getur stundum þurft að framkvæma almennan flutning á birgðum í aðra birgðageymslu, óháð eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="10e3c-125">In addition to such automatic transfer orders, you may sometimes need to perform a general move of inventory quantities to another location, irrespective of existing demand.</span></span> <span data-ttu-id="10e3c-126">Til þess er millifærslupöntun stofnuð handvirkt fyrir magnið sem á að flytja.</span><span class="sxs-lookup"><span data-stu-id="10e3c-126">For this purpose you would manually create a transfer order for the quantity to move.</span></span> <span data-ttu-id="10e3c-127">Til að tryggja að áætlunarkerfið breyti ekki þessari handvirku millifærslupöntun þarf að stilla reitinn **Sveigjanleiki áætlunar** í millifærslulínunum á Enginn.</span><span class="sxs-lookup"><span data-stu-id="10e3c-127">To ensure that the planning system does not try to manipulate this manual transfer order, you must set the **Planning Flexibility** on the transfer line(s) to None.</span></span>  

<span data-ttu-id="10e3c-128">Hins vegar, ef áætlunarkerfið á að leiðrétta magn og dagsetningar í millifærslupöntunum samkvæmt eftirspurn þarf að stilla reitinn **Sveigjanleiki áætlunar** á sjálfgildið, Ótakmarkað.</span><span class="sxs-lookup"><span data-stu-id="10e3c-128">Contrarily, if you do want the planning system to adjust the transfer order quantities and dates to existing demand, you must set the **Planning Flexibility** field to the default value, Unlimited.</span></span>

## <a name="planning-parameters"></a><span data-ttu-id="10e3c-129">Áætlunarfæribreytur</span><span class="sxs-lookup"><span data-stu-id="10e3c-129">Planning Parameters</span></span>  
<span data-ttu-id="10e3c-130">Áætlunarfæribreyturnar stýra því hvenær, hversu mikið og hvernig er fyllt á eftir mismunandi stillingunum á birgðaspjaldinu (eða birgðaeiningu - SKU) og framleiðsluuppsetningunni.</span><span class="sxs-lookup"><span data-stu-id="10e3c-130">The planning parameters control when, how much, and how to replenish based on the various settings on the item card (or stockkeeping unit - SKU), and the manufacturing setup.</span></span>  

<span data-ttu-id="10e3c-131">Eftirtaldar áætlunarfæribreytur eru til á vöru eða birgðahaldseiningarspjaldi:</span><span class="sxs-lookup"><span data-stu-id="10e3c-131">The following planning parameters exist on the item or SKU card:</span></span>  

-   <span data-ttu-id="10e3c-132">Hömlutímabil</span><span class="sxs-lookup"><span data-stu-id="10e3c-132">Dampener Period</span></span>  
-   <span data-ttu-id="10e3c-133">Hömlu magn</span><span class="sxs-lookup"><span data-stu-id="10e3c-133">Dampener Quantity</span></span>  
-   <span data-ttu-id="10e3c-134">Endurpöntunarstefna</span><span class="sxs-lookup"><span data-stu-id="10e3c-134">Reordering Policy</span></span>  
-   <span data-ttu-id="10e3c-135">Endurpöntunarmark</span><span class="sxs-lookup"><span data-stu-id="10e3c-135">Reorder Point</span></span>
-   <span data-ttu-id="10e3c-136">Hámarksbirgðir</span><span class="sxs-lookup"><span data-stu-id="10e3c-136">Maximum Inventory</span></span>  
-   <span data-ttu-id="10e3c-137">Yfirflæðisstig</span><span class="sxs-lookup"><span data-stu-id="10e3c-137">Overflow Level</span></span>  
-   <span data-ttu-id="10e3c-138">Tímarammi</span><span class="sxs-lookup"><span data-stu-id="10e3c-138">Time Bucket</span></span>  
-   <span data-ttu-id="10e3c-139">Lotusöfnunartímabil</span><span class="sxs-lookup"><span data-stu-id="10e3c-139">Lot Accumulation Period</span></span>  
-   <span data-ttu-id="10e3c-140">Enduráætlunartímabil</span><span class="sxs-lookup"><span data-stu-id="10e3c-140">Rescheduling Period</span></span>  
-   <span data-ttu-id="10e3c-141">Pöntunarmagn</span><span class="sxs-lookup"><span data-stu-id="10e3c-141">Reorder Quantity</span></span>  
-   <span data-ttu-id="10e3c-142">Öryggisforskot</span><span class="sxs-lookup"><span data-stu-id="10e3c-142">Safety Lead Time</span></span>  
-   <span data-ttu-id="10e3c-143">Magn í öryggisbirgðum</span><span class="sxs-lookup"><span data-stu-id="10e3c-143">Safety Stock Quantity</span></span>  
-   <span data-ttu-id="10e3c-144">Samsetningarstefna</span><span class="sxs-lookup"><span data-stu-id="10e3c-144">Assembly Policy</span></span>  
-   <span data-ttu-id="10e3c-145">Framleiðslustefna</span><span class="sxs-lookup"><span data-stu-id="10e3c-145">Manufacturing Policy</span></span>  

<span data-ttu-id="10e3c-146">Eftirfarandi pöntunarbreytur eru til á vöru eða birgðahaldseiningarspjaldi:</span><span class="sxs-lookup"><span data-stu-id="10e3c-146">The following order modifiers exist on the item or SKU card:</span></span>  

-   <span data-ttu-id="10e3c-147">Lágmarksmagn pöntunar</span><span class="sxs-lookup"><span data-stu-id="10e3c-147">Minimum Order Quantity</span></span>  
-   <span data-ttu-id="10e3c-148">Hámarksmagn pöntunar</span><span class="sxs-lookup"><span data-stu-id="10e3c-148">Maximum Order Quantity</span></span>  
-   <span data-ttu-id="10e3c-149">Fjöldapanta</span><span class="sxs-lookup"><span data-stu-id="10e3c-149">Order Multiple</span></span>  

<span data-ttu-id="10e3c-150">Á meðal uppsetningarreita altækar áætlunar í glugganum **Framleiðslugrunnur** eru:</span><span class="sxs-lookup"><span data-stu-id="10e3c-150">Global planning setup fields on the **Manufacturing Setup** window include:</span></span>  

-   <span data-ttu-id="10e3c-151">Sveigjanlegur lágstigskóti</span><span class="sxs-lookup"><span data-stu-id="10e3c-151">Dynamic Low-Level Code</span></span>  
-   <span data-ttu-id="10e3c-152">Gildandi framleiðsluspá</span><span class="sxs-lookup"><span data-stu-id="10e3c-152">Current Production Forecast</span></span>  
-   <span data-ttu-id="10e3c-153">Nota spá með staðsetningu</span><span class="sxs-lookup"><span data-stu-id="10e3c-153">Use Forecast on Locations</span></span>  
-   <span data-ttu-id="10e3c-154">Sjálfgefið öryggisforskot</span><span class="sxs-lookup"><span data-stu-id="10e3c-154">Default Safety Lead Time</span></span>  
-   <span data-ttu-id="10e3c-155">Autt yfirflæðisstig</span><span class="sxs-lookup"><span data-stu-id="10e3c-155">Blank Overflow Level</span></span>  
-   <span data-ttu-id="10e3c-156">Sameinaður MPS/MRP útreikn.</span><span class="sxs-lookup"><span data-stu-id="10e3c-156">Combined MPS/MRP Calculation</span></span>   
-   <span data-ttu-id="10e3c-157">Íhlutir á staðnum</span><span class="sxs-lookup"><span data-stu-id="10e3c-157">Components at Location</span></span>  
-   <span data-ttu-id="10e3c-158">Sjálfgefið hömlunartímabil</span><span class="sxs-lookup"><span data-stu-id="10e3c-158">Default Dampener Period</span></span>  
-   <span data-ttu-id="10e3c-159">Sjálfgefið hömlu magn</span><span class="sxs-lookup"><span data-stu-id="10e3c-159">Default Dampener Quantity</span></span>  

<span data-ttu-id="10e3c-160">Nánari upplýsingar eru í [Upplýsingar um hönnun: Áætlunarfæribreytur](design-details-planning-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="10e3c-160">For more information, see [Design Details: Planning Parameters](design-details-planning-parameters.md)</span></span>  

## <a name="other-important-planning-fields"></a><span data-ttu-id="10e3c-161">Önnur mikilvæg áætlunarsvið</span><span class="sxs-lookup"><span data-stu-id="10e3c-161">Other Important Planning Fields</span></span>
### <a name="planning-flexibility"></a><span data-ttu-id="10e3c-162">Sveigjanleiki áætlunar</span><span class="sxs-lookup"><span data-stu-id="10e3c-162">Planning Flexibility</span></span>
<span data-ttu-id="10e3c-163">Á flestum birgðapöntunum, eins og t.d. framleiðslupöntunum, getur valið **Ótakmarkaður** eða **Enginn** í **Sveigjanleiki áætlunar** reitnum.</span><span class="sxs-lookup"><span data-stu-id="10e3c-163">On most supply orders, such as production orders, you can select **Unlimited** or **None** in the **Planning Flexibility** field on the lines.</span></span>

<span data-ttu-id="10e3c-164">Tilgreinir hvort birgðir sem framleiðslupöntunarlína sýnir eru teknar með í áætlunarkerfinu þegar aðgerðarboð eru reiknuð.</span><span class="sxs-lookup"><span data-stu-id="10e3c-164">This specifies whether the supply represented by the production order line is considered by the planning system when calculating action messages.</span></span>
<span data-ttu-id="10e3c-165">Ef reiturinn inniheldur **Ótakmarkað** tekur áætlunarkerfið línuna með í reikninginn þegar aðgerðarboð eru reiknuð.</span><span class="sxs-lookup"><span data-stu-id="10e3c-165">If the field contains **Unlimited**, then the planning system includes the line when calculating action messages.</span></span> <span data-ttu-id="10e3c-166">Ef reiturinn inniheldur **Enginn** er línan föst og óbreytanleg og áætlunarkerfið tekur hana ekki með í reikninginn þegar aðgerðarboð eru reiknuð.</span><span class="sxs-lookup"><span data-stu-id="10e3c-166">If the field contains **None**, then the line is firm and unchangeable, and the planning system does not include the line when calculating action messages.</span></span>

### <a name="warning"></a><span data-ttu-id="10e3c-167">Viðvörun</span><span class="sxs-lookup"><span data-stu-id="10e3c-167">Warning</span></span>
<span data-ttu-id="10e3c-168">Upplýsingareiturinn **Viðvörun** í **Áætlunarvinnublað** glugganum lætur þig vita um allar áætlunarlínur sem gerðar eru vegna óvenjulegra með texta, sem notandinn getur smellt á til að lesa viðbótarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="10e3c-168">The **Warning** information field in the **Planning Worksheet** window informs you of any planning line created for an unusual situation with a text, which the user can choose to read additional information.</span></span> <span data-ttu-id="10e3c-169">Eftirfarandi tegundir viðvarana eru til:</span><span class="sxs-lookup"><span data-stu-id="10e3c-169">The following warning types exist:</span></span>

- <span data-ttu-id="10e3c-170">Neyð</span><span class="sxs-lookup"><span data-stu-id="10e3c-170">Emergency</span></span>
- <span data-ttu-id="10e3c-171">Frávik</span><span class="sxs-lookup"><span data-stu-id="10e3c-171">Exception</span></span>
- <span data-ttu-id="10e3c-172">Athugið</span><span class="sxs-lookup"><span data-stu-id="10e3c-172">Attention</span></span>
- <span data-ttu-id="10e3c-173">Neyð</span><span class="sxs-lookup"><span data-stu-id="10e3c-173">Emergency</span></span>

<span data-ttu-id="10e3c-174">Neyðarviðvörun birtist í tveimur aðstæðum:</span><span class="sxs-lookup"><span data-stu-id="10e3c-174">The emergency warning is displayed in two situations:</span></span>

- <span data-ttu-id="10e3c-175">Birgðir eru neikvæðar á upphafsdagsetningu áætlunar.</span><span class="sxs-lookup"><span data-stu-id="10e3c-175">The inventory is negative on the planning starting date.</span></span>
- <span data-ttu-id="10e3c-176">Framboðs- eða eftirspurnaratvik eru til aftur í tíma.</span><span class="sxs-lookup"><span data-stu-id="10e3c-176">Back-dated supply or demand events exist.</span></span>

<span data-ttu-id="10e3c-177">Ef birgðir eru neikvæðar á upphafsdegi áætlunarinnar stingur kerfið upp á neyðarpöntun með neikvæða magninu fyrir upphafsdagsetninguna.</span><span class="sxs-lookup"><span data-stu-id="10e3c-177">If an item’s inventory is negative on the planning starting date, the planning system suggests an emergency supply order for the negative quantity to arrive on the planning starting date.</span></span> <span data-ttu-id="10e3c-178">Upphafsdagsetningin og magn neyðarpöntunarinnar eru tiltekin í viðvörunartextanum.</span><span class="sxs-lookup"><span data-stu-id="10e3c-178">The warning text states the starting date and the quantity of the emergency order.</span></span>

<span data-ttu-id="10e3c-179">Allar skjalalínur með skiladagsetningar á undan upphafsdagsetningu áætlunarinnar eru settar í eina neyðarpöntun til að varan berist á áætlaðri upphafsdagsetningu.</span><span class="sxs-lookup"><span data-stu-id="10e3c-179">Any document lines with due dates before the planning starting date are consolidated into one emergency supply order for the item to arrive on the planning starting date.</span></span>

### <a name="exception"></a><span data-ttu-id="10e3c-180">Frávik</span><span class="sxs-lookup"><span data-stu-id="10e3c-180">Exception</span></span>
<span data-ttu-id="10e3c-181">Viðvörun um frávik birtist ef áætlaðar birgðir eru undir öryggismarki birgða.</span><span class="sxs-lookup"><span data-stu-id="10e3c-181">The exception warning is displayed if the projected available inventory drops below the safety stock quantity.</span></span>

<span data-ttu-id="10e3c-182">Áætlunarkerfið stingur upp á framboðspöntun til að uppfylla eftirspurnina á lokadagsetningunni.</span><span class="sxs-lookup"><span data-stu-id="10e3c-182">The planning system will suggest a supply order to meet the demand on its due date.</span></span> <span data-ttu-id="10e3c-183">Viðvörunartextinn segir til um magn í öryggisbirgðum fyrir vöruna og dagsetninguna sem það magn varð of lítið.</span><span class="sxs-lookup"><span data-stu-id="10e3c-183">The warning text states the item’s safety stock quantity and the date on which it is violated.</span></span>

<span data-ttu-id="10e3c-184">Þegar farið er undir öryggismagn í birgðum er það talið frávik þar sem það ætti ekki að gerast ef endurpöntunarmark hefur verið stillt rétt.</span><span class="sxs-lookup"><span data-stu-id="10e3c-184">Violating the safety stock level is considered an exception because it should not occur if the reorder point has been set correctly.</span></span>

> [!NOTE]
> <span data-ttu-id="10e3c-185">Framboði fyrir áætlunarlínur með viðvörunum um frávik er yfirleitt ekki breytt samkvæmt áætlunarfæribreytum.</span><span class="sxs-lookup"><span data-stu-id="10e3c-185">Supply on planning lines with Exception warnings is normally not modified according to planning parameters.</span></span> <span data-ttu-id="10e3c-186">Þess í stað stingur áætlunarkerfið einungis upp á framboði til að anna nákvæmu eftirspurnarmagni.</span><span class="sxs-lookup"><span data-stu-id="10e3c-186">Instead, the planning system only suggests a supply to cover the exact demand quantity.</span></span> <span data-ttu-id="10e3c-187">Hins vegar er hægt að stilla áætlunarkeyrsluna þannig að hún virði tilteknar áætlunarfæribreytur fyrir áætlunarlínur með viðvörunum.</span><span class="sxs-lookup"><span data-stu-id="10e3c-187">However, you can set the planning run up to respect certain planning parameters for planning lines with certain warnings.</span></span> <span data-ttu-id="10e3c-188">Nánari upplýsingar er að finna í „Virða áætlunarfæribreytur fyrir viðvaranir um frávik“ í Reikna áætlun - áætlun.</span><span class="sxs-lookup"><span data-stu-id="10e3c-188">For more information, see “Respect Planning Parameters for Exception Warnings” in Calculate Plan - Plan.</span></span> <span data-ttu-id="10e3c-189">Wksh.</span><span class="sxs-lookup"><span data-stu-id="10e3c-189">Wksh.</span></span>

### <a name="attention"></a><span data-ttu-id="10e3c-190">Athugið</span><span class="sxs-lookup"><span data-stu-id="10e3c-190">Attention</span></span>
<span data-ttu-id="10e3c-191">Viðvörunin Til athugunar birtist í tveimur aðstæðum:</span><span class="sxs-lookup"><span data-stu-id="10e3c-191">The attention warning is displayed in two situations:</span></span>

- <span data-ttu-id="10e3c-192">Upphafsdagsetning áætlunarinnar er á undan kerfisdagsetningunni.</span><span class="sxs-lookup"><span data-stu-id="10e3c-192">The planning starting date is earlier than the work date.</span></span>
- <span data-ttu-id="10e3c-193">Áætlunarlínan stingur upp á því að útgefinni innkaupa- eða framleiðslupöntun verði breytt.</span><span class="sxs-lookup"><span data-stu-id="10e3c-193">The planning line suggests to change a released purchase or production order.</span></span>

> [!NOTE]
> <span data-ttu-id="10e3c-194">Í áætlunarlínum með viðvaranir er reiturinn **Samþykkja aðgerðarboð** ekki valinn þar sem sá sem gerir áætlunina á að kanna þessar línur nánar áður en lokið er við áætlunina. </span><span class="sxs-lookup"><span data-stu-id="10e3c-194">In planning lines with warnings, the **Accept Action Message** field is not selected, because the planner is expected to further investigate these lines before carrying out the plan.</span></span>

## <a name="see-also"></a><span data-ttu-id="10e3c-195">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="10e3c-195">See Also</span></span>  
[<span data-ttu-id="10e3c-196">Hönnunarupplýsingar: framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="10e3c-196">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)  
<span data-ttu-id="10e3c-197">[Áætlun](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="10e3c-197">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="10e3c-198">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="10e3c-198">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="10e3c-199">[Framleiðsla](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="10e3c-199">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="10e3c-200">Birgðir</span><span class="sxs-lookup"><span data-stu-id="10e3c-200">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="10e3c-201">Innkaup</span><span class="sxs-lookup"><span data-stu-id="10e3c-201">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="10e3c-202">Uppsetning bestu venjur: Framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="10e3c-202">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="10e3c-203">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="10e3c-203">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

