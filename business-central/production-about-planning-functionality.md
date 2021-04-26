---
title: Um áætlunaraðgerðir | Microsoft Docs
description: Áætlunarkerfið tekur öll gögn um eftirspurn og framboð með í reikninginn, reiknar út niðurstöðurnar og kemur með tillögur að því að jafna framboðið og eftirspurnina.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dc3ef67f2f7578d81878b24662b97e47bc87a327
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782039"
---
# <a name="about-planning-functionality"></a><span data-ttu-id="16f61-103">Um áætlunaraðgerðir</span><span class="sxs-lookup"><span data-stu-id="16f61-103">About Planning Functionality</span></span>

<span data-ttu-id="16f61-104">Áætlunarkerfið tekur öll gögn um eftirspurn og framboð með í reikninginn, reiknar út niðurstöðurnar og kemur með tillögur að því að jafna framboðið og eftirspurnina.</span><span class="sxs-lookup"><span data-stu-id="16f61-104">The planning system takes all demand and supply data into account, nets the results, and creates suggestions for balancing the supply to meet the demand.</span></span>  

<span data-ttu-id="16f61-105">Frekari og nákvæmari upplýsingar, sjá [Hönnunarupplýsingar: Framboðsáætlun](design-details-supply-planning.md)</span><span class="sxs-lookup"><span data-stu-id="16f61-105">For detailed information, see [Design Details: Supply Planning](design-details-supply-planning.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="16f61-106">Fyrir öll þau svið sem minnst er á í þessu efnisatriði, lesa ábendingarnar til að skilja virkni þeirra.</span><span class="sxs-lookup"><span data-stu-id="16f61-106">For all the fields that are mentioned in this topic, read the tooltip to understand their function.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a><span data-ttu-id="16f61-107">Eftirspurn og Framboð</span><span class="sxs-lookup"><span data-stu-id="16f61-107">Demand and Supply</span></span>

<span data-ttu-id="16f61-108">Áætlanagerð hefur tvo hluta: eftirspurn og framboð.</span><span class="sxs-lookup"><span data-stu-id="16f61-108">Planning has two elements: demand and supply.</span></span> <span data-ttu-id="16f61-109">Halda þarf þeim í jafnvægi til að tryggja það að eftirspurninni sé annað á tímanlegan og hagkvæman hátt.</span><span class="sxs-lookup"><span data-stu-id="16f61-109">These must be held in balance to ensure that the demand is met in a timely and cost-efficient manner.</span></span>  

- <span data-ttu-id="16f61-110">Eftirspurn er notað sem almennt heiti yfir hvers konar brúttóþörf eins og sölupöntun, þjónustupöntun, íhlutaþörf frá samsetningu eða framleiðslupantanir, millifærslur á útleið, standandi pöntun eða spá.</span><span class="sxs-lookup"><span data-stu-id="16f61-110">Demand is the common term used for any kind of gross requirement such as a sales order, service order, component need from assembly or production orders, outbound transfer, blanket order or forecast.</span></span> <span data-ttu-id="16f61-111">Þar að auki býður forritið upp á nokkrar aðrar tæknilegar tegundir eftirspurnar - eins og neikvæða framleiðslu- eða innkaupapöntun, neikvætt birgðamat og innkaupaskil.</span><span class="sxs-lookup"><span data-stu-id="16f61-111">In addition to these, application allows some other technical types of demand - such as a negative production or purchase order, negative inventory, and purchase return.</span></span>  
- <span data-ttu-id="16f61-112">Framboð er það orð sem er mest notað fyrir hvaða tegund af áfyllingu sem er, eins og birgðir, innkaupapöntun, samsetningarpöntun, framleiðslupöntun eða millifærslu á innleið.</span><span class="sxs-lookup"><span data-stu-id="16f61-112">Supply is the common word used for any kind of replenishment such as inventory, a purchase order, assembly order, production order, or inbound transfer.</span></span> <span data-ttu-id="16f61-113">Á sama hátt getur verið til neikvæð sölu- eða þjónustupöntun, neikvæð íhlutaþörf eða innkaupaskil – sem er allt á einhvern hátt dæmi um framboð.</span><span class="sxs-lookup"><span data-stu-id="16f61-113">Correspondingly, there can be a negative sales or service order, negative component need or sales return – all of which in some way also represent supply.</span></span>  

<span data-ttu-id="16f61-114">Annað markmið áætlunarkerfisins er að tryggja það að birgðamagnið hækki ekki að óþörfu.</span><span class="sxs-lookup"><span data-stu-id="16f61-114">Another goal of the planning system is to ensure that the inventory does not grow unnecessarily.</span></span> <span data-ttu-id="16f61-115">Í tilfelli minnkandi eftirspurnar mun áætlunarkerfið leggja til að annað hvort verði þeim áfyllingarpöntunum sem eru fyrir hendi frestað, þær minnkaðar eða afpantaðar.</span><span class="sxs-lookup"><span data-stu-id="16f61-115">In the case of decreasing demand, the planning system will suggest that you postpone, decrease in quantity, or cancel existing replenishment orders.</span></span>  

## <a name="planning-calculation"></a><span data-ttu-id="16f61-116">Áætlunarútreikningur</span><span class="sxs-lookup"><span data-stu-id="16f61-116">Planning Calculation</span></span>

<span data-ttu-id="16f61-117">Áætlunarkerfið er knúið áfram af viðbúinni og raunverulegri eftirspurn viðskiptavina auk endurpöntunarfæribreytum birgða.</span><span class="sxs-lookup"><span data-stu-id="16f61-117">The planning system is driven by anticipated and actual customer demand, as well as inventory reordering parameters.</span></span> <span data-ttu-id="16f61-118">Ef áætlunarútreikningurinn er keyrður mun það leiða til þess að forritið leggi til sérstakar aðgerðir (Aðgerðarboð) til að framkvæma varðandi mögulega áfyllingu frá lánardrottnum, millifærslur á milli vöruhúsa eða framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="16f61-118">Running the planning calculation will result in application suggesting specific actions (Action Messages) to take concerning possible replenishment from vendors, transfers between warehouses, or production.</span></span> <span data-ttu-id="16f61-119">Ef áfyllingarpantanir eru þegar til gætu tillögurnar verið þess efnis að auka við pantanirnar eða flýta þeim til að koma til móts við eftirspurnarbreytingarnar.</span><span class="sxs-lookup"><span data-stu-id="16f61-119">If replenishment orders already exist, the suggested actions could be to increase or expedite the orders to meet the changes in demand.</span></span>  

<span data-ttu-id="16f61-120">Grundvöllur áætlunarrútínunnar er í útreikningunum frá hagnaði til taps.</span><span class="sxs-lookup"><span data-stu-id="16f61-120">The basis of the planning routine is in the gross-to-net calculation.</span></span> <span data-ttu-id="16f61-121">Nettóþarfir knýja áætlaða útgáfu pantana sem eru tímasettar eftir leiðarupplýsingum (framleiddar vörur) eða afhendingartíma birgðaspjaldsins (keyptar vörur).</span><span class="sxs-lookup"><span data-stu-id="16f61-121">Net requirements drive planned order releases, which are scheduled based on the routing information (manufactured items) or the item card lead time (purchased items).</span></span> <span data-ttu-id="16f61-122">Magn áætlaðrar útgáfu pöntunar er byggt á áætlunarútreikningunum og verður fyrir áhrifum af þeim færibreytum sem eru stilltar fyrir hvert stakt birgðaspjald.</span><span class="sxs-lookup"><span data-stu-id="16f61-122">Planned order release quantities are based on the planning calculation, and are affected by the parameters set on the individual item cards.</span></span>  

## <a name="planning-with-manual-transfer-orders"></a><span data-ttu-id="16f61-123">Áætlað með handvirkum millifærslupöntunum</span><span class="sxs-lookup"><span data-stu-id="16f61-123">Planning with Manual Transfer Orders</span></span>

<span data-ttu-id="16f61-124">Eins og sjá má í reitnum **Áfyllingarkerfið** á birgðahaldseiningarspjaldi er hægt að setja áætlunarkerfið upp til að stofna millifærslupantanir til að jafna framboð og eftirspurn á milli birgðageymslna.</span><span class="sxs-lookup"><span data-stu-id="16f61-124">As you can see from the **Replenishment System** field on a SKU card, the planning system can be set up to create transfer orders to balance supply and demand across locations.</span></span>  

<span data-ttu-id="16f61-125">Til viðbótar slíkum sjálfvirkum millifærslupöntunum getur stundum þurft að framkvæma almennan flutning á birgðum í aðra birgðageymslu, óháð eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="16f61-125">In addition to such automatic transfer orders, you may sometimes need to perform a general move of inventory quantities to another location, irrespective of existing demand.</span></span> <span data-ttu-id="16f61-126">Til þess er millifærslupöntun stofnuð handvirkt fyrir magnið sem á að flytja.</span><span class="sxs-lookup"><span data-stu-id="16f61-126">For this purpose you would manually create a transfer order for the quantity to move.</span></span> <span data-ttu-id="16f61-127">Til að tryggja að áætlunarkerfið breyti ekki þessari handvirku millifærslupöntun þarf að stilla reitinn **Sveigjanleiki áætlunar** í millifærslulínunum á Enginn.</span><span class="sxs-lookup"><span data-stu-id="16f61-127">To ensure that the planning system does not try to manipulate this manual transfer order, you must set the **Planning Flexibility** on the transfer line(s) to None.</span></span>  

<span data-ttu-id="16f61-128">Hins vegar, ef áætlunarkerfið á að leiðrétta magn og dagsetningar í millifærslupöntunum samkvæmt eftirspurn þarf að stilla reitinn **Sveigjanleiki áætlunar** á sjálfgildið, Ótakmarkað.</span><span class="sxs-lookup"><span data-stu-id="16f61-128">Contrarily, if you do want the planning system to adjust the transfer order quantities and dates to existing demand, you must set the **Planning Flexibility** field to the default value, Unlimited.</span></span>

## <a name="planning-parameters"></a><span data-ttu-id="16f61-129">Áætlunarfæribreytur</span><span class="sxs-lookup"><span data-stu-id="16f61-129">Planning Parameters</span></span>

<span data-ttu-id="16f61-130">Áætlunarfæribreyturnar stýra því hvenær, hversu mikið og hvernig er fyllt á eftir mismunandi stillingunum á birgðaspjaldinu (eða birgðaeiningu - SKU) og framleiðsluuppsetningunni.</span><span class="sxs-lookup"><span data-stu-id="16f61-130">The planning parameters control when, how much, and how to replenish based on the various settings on the item card (or stockkeeping unit - SKU), and the manufacturing setup.</span></span>  

<span data-ttu-id="16f61-131">Eftirtaldar áætlunarfæribreytur eru til á vöru eða birgðahaldseiningarspjaldi:</span><span class="sxs-lookup"><span data-stu-id="16f61-131">The following planning parameters exist on the item or SKU card:</span></span>  

- <span data-ttu-id="16f61-132">Hömlutímabil</span><span class="sxs-lookup"><span data-stu-id="16f61-132">Dampener Period</span></span>  
- <span data-ttu-id="16f61-133">Hömlu magn</span><span class="sxs-lookup"><span data-stu-id="16f61-133">Dampener Quantity</span></span>  
- <span data-ttu-id="16f61-134">Endurpöntunarstefna</span><span class="sxs-lookup"><span data-stu-id="16f61-134">Reordering Policy</span></span>  
- <span data-ttu-id="16f61-135">Endurpöntunarmark</span><span class="sxs-lookup"><span data-stu-id="16f61-135">Reorder Point</span></span>
- <span data-ttu-id="16f61-136">Hámarksbirgðir</span><span class="sxs-lookup"><span data-stu-id="16f61-136">Maximum Inventory</span></span>  
- <span data-ttu-id="16f61-137">Yfirflæðisstig</span><span class="sxs-lookup"><span data-stu-id="16f61-137">Overflow Level</span></span>  
- <span data-ttu-id="16f61-138">Tímarammi</span><span class="sxs-lookup"><span data-stu-id="16f61-138">Time Bucket</span></span>  
- <span data-ttu-id="16f61-139">Lotusöfnunartímabil</span><span class="sxs-lookup"><span data-stu-id="16f61-139">Lot Accumulation Period</span></span>  
- <span data-ttu-id="16f61-140">Enduráætlunartímabil</span><span class="sxs-lookup"><span data-stu-id="16f61-140">Rescheduling Period</span></span>  
- <span data-ttu-id="16f61-141">Pöntunarmagn</span><span class="sxs-lookup"><span data-stu-id="16f61-141">Reorder Quantity</span></span>  
- <span data-ttu-id="16f61-142">Öryggisforskot</span><span class="sxs-lookup"><span data-stu-id="16f61-142">Safety Lead Time</span></span>  
- <span data-ttu-id="16f61-143">Magn í öryggisbirgðum</span><span class="sxs-lookup"><span data-stu-id="16f61-143">Safety Stock Quantity</span></span>  
- <span data-ttu-id="16f61-144">Samsetningarstefna</span><span class="sxs-lookup"><span data-stu-id="16f61-144">Assembly Policy</span></span>  
- <span data-ttu-id="16f61-145">Framleiðslustefna</span><span class="sxs-lookup"><span data-stu-id="16f61-145">Manufacturing Policy</span></span>  

<span data-ttu-id="16f61-146">Eftirfarandi pöntunarbreytur eru til á vöru eða birgðahaldseiningarspjaldi:</span><span class="sxs-lookup"><span data-stu-id="16f61-146">The following order modifiers exist on the item or SKU card:</span></span>  

- <span data-ttu-id="16f61-147">Lágmarksmagn pöntunar</span><span class="sxs-lookup"><span data-stu-id="16f61-147">Minimum Order Quantity</span></span>  
- <span data-ttu-id="16f61-148">Hámarksmagn pöntunar</span><span class="sxs-lookup"><span data-stu-id="16f61-148">Maximum Order Quantity</span></span>  
- <span data-ttu-id="16f61-149">Fjöldapanta</span><span class="sxs-lookup"><span data-stu-id="16f61-149">Order Multiple</span></span>  

<span data-ttu-id="16f61-150">Á meðal uppsetningarreita altækrar áætlunar á síðunni **Framleiðsluuppsetning** eru:</span><span class="sxs-lookup"><span data-stu-id="16f61-150">Global planning setup fields on the **Manufacturing Setup** page include:</span></span>  

- <span data-ttu-id="16f61-151">Kvikur lágstigskóti</span><span class="sxs-lookup"><span data-stu-id="16f61-151">Dynamic Low-Level Code</span></span>  
- <span data-ttu-id="16f61-152">Núgildandi eftirspurnarspá</span><span class="sxs-lookup"><span data-stu-id="16f61-152">Current Demand Forecast</span></span>  
- <span data-ttu-id="16f61-153">Nota spá með staðsetningu</span><span class="sxs-lookup"><span data-stu-id="16f61-153">Use Forecast on Locations</span></span>  
- <span data-ttu-id="16f61-154">Sjálfgefið öryggisforskot</span><span class="sxs-lookup"><span data-stu-id="16f61-154">Default Safety Lead Time</span></span>  
- <span data-ttu-id="16f61-155">Autt yfirflæðisstig</span><span class="sxs-lookup"><span data-stu-id="16f61-155">Blank Overflow Level</span></span>  
- <span data-ttu-id="16f61-156">Sameinaður MPS/MRP útreikn.</span><span class="sxs-lookup"><span data-stu-id="16f61-156">Combined MPS/MRP Calculation</span></span>
- <span data-ttu-id="16f61-157">Íhlutir á staðnum</span><span class="sxs-lookup"><span data-stu-id="16f61-157">Components at Location</span></span>  
- <span data-ttu-id="16f61-158">Sjálfgefið hömlunartímabil</span><span class="sxs-lookup"><span data-stu-id="16f61-158">Default Dampener Period</span></span>  
- <span data-ttu-id="16f61-159">Sjálfgefið hömlu magn</span><span class="sxs-lookup"><span data-stu-id="16f61-159">Default Dampener Quantity</span></span>  

<span data-ttu-id="16f61-160">Nánari upplýsingar eru í [Upplýsingar um hönnun: Áætlunarfæribreytur](design-details-planning-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="16f61-160">For more information, see [Design Details: Planning Parameters](design-details-planning-parameters.md)</span></span>  

## <a name="other-important-planning-fields"></a><span data-ttu-id="16f61-161">Önnur mikilvæg áætlunarsvið</span><span class="sxs-lookup"><span data-stu-id="16f61-161">Other Important Planning Fields</span></span>

### <a name="planning-flexibility"></a><span data-ttu-id="16f61-162">Sveigjanleiki áætlunar</span><span class="sxs-lookup"><span data-stu-id="16f61-162">Planning Flexibility</span></span>

<span data-ttu-id="16f61-163">Á flestum birgðapöntunum, eins og t.d. framleiðslupöntunum, getur valið **Ótakmarkaður** eða **Enginn** í **Sveigjanleiki áætlunar** reitnum.</span><span class="sxs-lookup"><span data-stu-id="16f61-163">On most supply orders, such as production orders, you can select **Unlimited** or **None** in the **Planning Flexibility** field on the lines.</span></span>

<span data-ttu-id="16f61-164">Tilgreinir hvort birgðir sem framleiðslupöntunarlína sýnir eru teknar með í áætlunarkerfinu þegar aðgerðarboð eru reiknuð.</span><span class="sxs-lookup"><span data-stu-id="16f61-164">This specifies whether the supply represented by the production order line is considered by the planning system when calculating action messages.</span></span>
<span data-ttu-id="16f61-165">Ef reiturinn inniheldur **Ótakmarkað** tekur áætlunarkerfið línuna með í reikninginn þegar aðgerðarboð eru reiknuð.</span><span class="sxs-lookup"><span data-stu-id="16f61-165">If the field contains **Unlimited**, then the planning system includes the line when calculating action messages.</span></span> <span data-ttu-id="16f61-166">Ef reiturinn inniheldur **Enginn** er línan föst og óbreytanleg og áætlunarkerfið tekur hana ekki með í reikninginn þegar aðgerðarboð eru reiknuð.</span><span class="sxs-lookup"><span data-stu-id="16f61-166">If the field contains **None**, then the line is firm and unchangeable, and the planning system does not include the line when calculating action messages.</span></span>

### <a name="warning"></a><span data-ttu-id="16f61-167">Viðvörun</span><span class="sxs-lookup"><span data-stu-id="16f61-167">Warning</span></span>

<span data-ttu-id="16f61-168">Upplýsingareiturinn **Viðvörun** í **Áætlunarvinnublað** síðunni lætur þig vita um allar áætlunarlínur sem gerðar eru vegna óvenjulegra með texta, sem notandinn getur smellt á til að lesa viðbótarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="16f61-168">The **Warning** information field on the **Planning Worksheet** page informs you of any planning line created for an unusual situation with a text, which the user can choose to read additional information.</span></span> <span data-ttu-id="16f61-169">Eftirfarandi tegundir viðvarana eru til:</span><span class="sxs-lookup"><span data-stu-id="16f61-169">The following warning types exist:</span></span>

- <span data-ttu-id="16f61-170">Neyð</span><span class="sxs-lookup"><span data-stu-id="16f61-170">Emergency</span></span>
- <span data-ttu-id="16f61-171">Frávik</span><span class="sxs-lookup"><span data-stu-id="16f61-171">Exception</span></span>
- <span data-ttu-id="16f61-172">Athugið</span><span class="sxs-lookup"><span data-stu-id="16f61-172">Attention</span></span>
- <span data-ttu-id="16f61-173">Neyð</span><span class="sxs-lookup"><span data-stu-id="16f61-173">Emergency</span></span>

<span data-ttu-id="16f61-174">Neyðarviðvörun birtist í tveimur aðstæðum:</span><span class="sxs-lookup"><span data-stu-id="16f61-174">The emergency warning is displayed in two situations:</span></span>

- <span data-ttu-id="16f61-175">Birgðir eru neikvæðar á upphafsdagsetningu áætlunar.</span><span class="sxs-lookup"><span data-stu-id="16f61-175">The inventory is negative on the planning starting date.</span></span>
- <span data-ttu-id="16f61-176">Framboðs- eða eftirspurnaratvik eru til aftur í tíma.</span><span class="sxs-lookup"><span data-stu-id="16f61-176">Back-dated supply or demand events exist.</span></span>

<span data-ttu-id="16f61-177">Ef birgðir vöru eru neikvæðar á upphafsdegi áætlunarinnar stingur kerfið upp á neyðarpöntun á birgðum með neikvæða magninu sem á að koma á upphafsdagsetningu áætlunarinnar.</span><span class="sxs-lookup"><span data-stu-id="16f61-177">If an item's inventory is negative on the planning starting date, the planning system suggests an emergency supply order for the negative quantity to arrive on the planning starting date.</span></span> <span data-ttu-id="16f61-178">Upphafsdagsetningin og magn neyðarpöntunarinnar eru tiltekin í viðvörunartextanum.</span><span class="sxs-lookup"><span data-stu-id="16f61-178">The warning text states the starting date and the quantity of the emergency order.</span></span>

<span data-ttu-id="16f61-179">Allar skjalalínur með skiladagsetningar á undan upphafsdagsetningu áætlunarinnar eru settar í eina neyðarpöntun til að varan berist á áætlaðri upphafsdagsetningu.</span><span class="sxs-lookup"><span data-stu-id="16f61-179">Any document lines with due dates before the planning starting date are consolidated into one emergency supply order for the item to arrive on the planning starting date.</span></span>

### <a name="exception"></a><span data-ttu-id="16f61-180">Frávik</span><span class="sxs-lookup"><span data-stu-id="16f61-180">Exception</span></span>

<span data-ttu-id="16f61-181">Viðvörun um frávik birtist ef áætlaðar birgðir eru undir öryggismarki birgða.</span><span class="sxs-lookup"><span data-stu-id="16f61-181">The exception warning is displayed if the projected available inventory drops below the safety stock quantity.</span></span>

<span data-ttu-id="16f61-182">Áætlunarkerfið stingur upp á framboðspöntun til að uppfylla eftirspurnina á lokadagsetningunni.</span><span class="sxs-lookup"><span data-stu-id="16f61-182">The planning system will suggest a supply order to meet the demand on its due date.</span></span> <span data-ttu-id="16f61-183">Viðvörunartextinn segir til um magn í öryggisbirgðum fyrir vöruna og dagsetninguna sem það magn varð of lítið.</span><span class="sxs-lookup"><span data-stu-id="16f61-183">The warning text states the item's safety stock quantity and the date on which it is violated.</span></span>

<span data-ttu-id="16f61-184">Þegar farið er undir öryggismagn í birgðum er það talið frávik þar sem það ætti ekki að gerast ef endurpöntunarmark hefur verið stillt rétt.</span><span class="sxs-lookup"><span data-stu-id="16f61-184">Violating the safety stock level is considered an exception because it should not occur if the reorder point has been set correctly.</span></span>

> [!NOTE]
> <span data-ttu-id="16f61-185">Framboði fyrir áætlunarlínur með viðvörunum um frávik er yfirleitt ekki breytt samkvæmt áætlunarfæribreytum.</span><span class="sxs-lookup"><span data-stu-id="16f61-185">Supply on planning lines with Exception warnings is normally not modified according to planning parameters.</span></span> <span data-ttu-id="16f61-186">Þess í stað stingur áætlunarkerfið einungis upp á framboði til að anna nákvæmu eftirspurnarmagni.</span><span class="sxs-lookup"><span data-stu-id="16f61-186">Instead, the planning system only suggests a supply to cover the exact demand quantity.</span></span> <span data-ttu-id="16f61-187">Hins vegar er hægt að stilla áætlunarkeyrsluna þannig að hún virði tilteknar áætlunarfæribreytur fyrir áætlunarlínur með viðvörunum.</span><span class="sxs-lookup"><span data-stu-id="16f61-187">However, you can set the planning run up to respect certain planning parameters for planning lines with certain warnings.</span></span> <span data-ttu-id="16f61-188">Frekari upplýsingar er að finna í lýsingunni fyrir reitinn **Virða áætlunarfæribreytur fyrir viðvaranir um frávik** í greininni [Keyra fulla áætlunargerð, MPS eða MRP](production-how-to-run-mps-and-mrp.md).</span><span class="sxs-lookup"><span data-stu-id="16f61-188">For more information, see the description for the **Respect Planning Parameters for Exception Warnings** field in the [Run Full Planning, MPS or MRP](production-how-to-run-mps-and-mrp.md) article.</span></span>

### <a name="attention"></a><span data-ttu-id="16f61-189">Athugið</span><span class="sxs-lookup"><span data-stu-id="16f61-189">Attention</span></span>

<span data-ttu-id="16f61-190">Viðvörunin Til athugunar birtist í tveimur aðstæðum:</span><span class="sxs-lookup"><span data-stu-id="16f61-190">The attention warning is displayed in two situations:</span></span>

- <span data-ttu-id="16f61-191">Upphafsdagsetning áætlunarinnar er á undan kerfisdagsetningunni.</span><span class="sxs-lookup"><span data-stu-id="16f61-191">The planning starting date is earlier than the work date.</span></span>
- <span data-ttu-id="16f61-192">Áætlunarlínan stingur upp á því að útgefinni innkaupa- eða framleiðslupöntun verði breytt.</span><span class="sxs-lookup"><span data-stu-id="16f61-192">The planning line suggests to change a released purchase or production order.</span></span>

> [!NOTE]
> <span data-ttu-id="16f61-193">Í áætlunarlínum með viðvaranir er reiturinn **Samþykkja aðgerðarboð** ekki valinn þar sem sá sem gerir áætlunina á að kanna þessar línur nánar áður en lokið er við áætlunina.</span><span class="sxs-lookup"><span data-stu-id="16f61-193">In planning lines with warnings, the **Accept Action Message** field is not selected, because the planner is expected to further investigate these lines before carrying out the plan.</span></span>

## <a name="planning-worksheets-and-requisition-worksheets"></a><span data-ttu-id="16f61-194">Áætlunarvinnublöð og vinnublöð innkaupatillagna</span><span class="sxs-lookup"><span data-stu-id="16f61-194">Planning worksheets and requisition worksheets</span></span>

<span data-ttu-id="16f61-195">Eins og lýst er í [Áætlanagerð](production-planning.md) er hægt að velja milli tveggja vinnublaða fyrir flesta verkþætti áætlanagerðar, áætlunarvinnublaðið og vinnublað innkaupatillögu.</span><span class="sxs-lookup"><span data-stu-id="16f61-195">As described in [Planning](production-planning.md), you can choose between two worksheets for most planning activities, the planning worksheet and the requisition worksheet.</span></span> <span data-ttu-id="16f61-196">Flest ferlum er lýst samkvæmt áætlunarvinnublaði, en til eru nokkrar atburðarásir þar sem vinnublað innkaupatillögu er betra.</span><span class="sxs-lookup"><span data-stu-id="16f61-196">Most processes are described based on the planning worksheet, but there are a couple of scenarios where the requisition worksheet is preferred.</span></span>

### <a name="requisition-worksheet"></a><span data-ttu-id="16f61-197">Innkaupatillögublað</span><span class="sxs-lookup"><span data-stu-id="16f61-197">Requisition worksheet</span></span>

<span data-ttu-id="16f61-198">Síðan **Innkaupatillögublað** sýnir vörur sem þú vilt panta.</span><span class="sxs-lookup"><span data-stu-id="16f61-198">The **Requisition Worksheet** page lists items that you want to order.</span></span> <span data-ttu-id="16f61-199">Hægt er að setja vörur inn í vinnublaðið á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="16f61-199">You can enter items in the worksheet in the following ways:</span></span>

- <span data-ttu-id="16f61-200">Færa vörurnar handvirkt inn í vinnublaðið og fylla út viðkomandi reiti.</span><span class="sxs-lookup"><span data-stu-id="16f61-200">Enter the items manually in the worksheet and fill in the relevant fields.</span></span>

- <span data-ttu-id="16f61-201">Nota runuvinnsluna **Reikna áætlun**.</span><span class="sxs-lookup"><span data-stu-id="16f61-201">Use the **Calculate Plan** batch job.</span></span> <span data-ttu-id="16f61-202">Þá er reiknuð áfyllingaráætlun fyrir vörur og birgðahaldseiningar sem hafa verið settar upp með innkaupatillögukerfi fyrir **innkaup** eða **millifærslu**.</span><span class="sxs-lookup"><span data-stu-id="16f61-202">This calculates a replenishment plan for items and stockkeeping units that have been set up with a replenishment system of **Purchase** or **Transfer**.</span></span> <span data-ttu-id="16f61-203">Þegar keyrslan er keyrð færir forritið sjálfkrafa í reitinn **Aðgerðaboð** tillögu um aðgerð sem nota má til að fylla á birgðirnar.</span><span class="sxs-lookup"><span data-stu-id="16f61-203">When you use this batch job, the program automatically fills in the **Action Message** field with a suggestion for an action you can take to replenish the item.</span></span> <span data-ttu-id="16f61-204">Þetta gæti verið að auka magn vörunnar í fyrirliggjandi pöntun eða að stofna nýja pöntun, t.d.</span><span class="sxs-lookup"><span data-stu-id="16f61-204">This could be increasing the item quantity on an existing order or creating a new order, for example.</span></span>

- <span data-ttu-id="16f61-205">Ef notuð var keyrslan **Reikna áætlun** á síðunni **Áætlunarvinnublað** til að reikna út áfyllingaráætlun er hægt að nota runuvinnsluna **Framkvæma aðgerðaboð** til að afrita innkaupa- og millifærslupöntunartillögur úr áætlunarvinnublaðinu í innkaupatillögublaðið.</span><span class="sxs-lookup"><span data-stu-id="16f61-205">If you have used the **Calculate Plan** batch job from the **Planning Worksheet** page to calculate a replenishment plan, you can use the **Carry Out Action Message** batch job to copy purchase and transfer order proposals from the planning worksheet to the requisition worksheet.</span></span> <span data-ttu-id="16f61-206">Þetta kemur sér vel ef notendur sem sjá um framleiðslupantanir og innkaupa-/millifærslupantanir eru ekki þeir sömu.</span><span class="sxs-lookup"><span data-stu-id="16f61-206">This is practical if separate users are responsible for handling production orders and purchase/transfer orders.</span></span>

- <span data-ttu-id="16f61-207">Hægt er að nota aðgerðina **Bein sending** til að færa inn í línur innkaupatillögublaðsins.</span><span class="sxs-lookup"><span data-stu-id="16f61-207">You can use the **Drop Shipment** action to fill in the requisition worksheet lines.</span></span> <span data-ttu-id="16f61-208">Þessi aðgerð notar runuvinnsluna **Sækja sölupantanir** til að ákveða hvaða sölupöntunarlínur eigi að úthluta fyrir beina sendingu.</span><span class="sxs-lookup"><span data-stu-id="16f61-208">This action uses the **Get Sales Orders** batch job to determine the sales order lines that you want to designate for a drop shipment.</span></span>

- <span data-ttu-id="16f61-209">Hægt er að nota aðgerðina **Sérpöntun** til að færa inn í línur innkaupatillögublaðsins.</span><span class="sxs-lookup"><span data-stu-id="16f61-209">You can use the **Special Order** action to fill in the requisition worksheet lines.</span></span> <span data-ttu-id="16f61-210">Þessi aðgerð notar runuvinnsluna **Sækja sölupantanir** til að ákveða hvaða sölupöntunarlínur eigi að úthluta fyrir sérpöntun.</span><span class="sxs-lookup"><span data-stu-id="16f61-210">This action uses the **Get Sales Orders** batch job to determine the sales order lines that you want to designate for a special order.</span></span>

<span data-ttu-id="16f61-211">Innkaupatillögulínur eru með nákvæmum upplýsingum um vörurnar sem þarf að endurpanta.</span><span class="sxs-lookup"><span data-stu-id="16f61-211">Requisition worksheet lines contain detailed information about the items that need to be reordered.</span></span> <span data-ttu-id="16f61-212">Hægt er að breyta og eyða línunum til að leiðrétta áfyllingaráætlunina og vinna frekar úr línunum með því að nota keyrsluna **Framkvæma aðgerðarboð**.</span><span class="sxs-lookup"><span data-stu-id="16f61-212">You can edit and delete the lines to adjust your replenishment plan, and you can further process the lines by using the **Carry Out Action Message** batch job.</span></span>

<span data-ttu-id="16f61-213">Upplýsingar um áætlanagerð með birgðageymslum og flutningum er að finna í [Áætlanagerð með eða án birgðageymslna](production-planning-with-without-locations.md).</span><span class="sxs-lookup"><span data-stu-id="16f61-213">For details about planning with locations and transfers, see [Planning With or Without Locations](production-planning-with-without-locations.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="16f61-214">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="16f61-214">See Also</span></span>

[<span data-ttu-id="16f61-215">Hönnunarupplýsingar: framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="16f61-215">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)  
[<span data-ttu-id="16f61-216">Áætlun</span><span class="sxs-lookup"><span data-stu-id="16f61-216">Planning</span></span>](production-planning.md)  
[<span data-ttu-id="16f61-217">Uppsetning framleiðslu</span><span class="sxs-lookup"><span data-stu-id="16f61-217">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="16f61-218">Framleiðsla</span><span class="sxs-lookup"><span data-stu-id="16f61-218">Manufacturing</span></span>](production-manage-manufacturing.md)  
[<span data-ttu-id="16f61-219">Birgðir</span><span class="sxs-lookup"><span data-stu-id="16f61-219">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="16f61-220">Innkaup</span><span class="sxs-lookup"><span data-stu-id="16f61-220">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="16f61-221">Uppsetning bestu venjur: Framboðsáætlun</span><span class="sxs-lookup"><span data-stu-id="16f61-221">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="16f61-222">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="16f61-222">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]