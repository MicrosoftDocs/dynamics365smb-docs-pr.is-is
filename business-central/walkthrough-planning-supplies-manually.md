---
title: "Kynning - Handvirk áætlun birgða | Microsoft Docs"
description: "Þessi kynning sýnir ferli áætlunar birgðapantana til að uppfylla nýja eftirspurn. Hægt er að hefja áætlun birgða með föstu millibili, t.d. á hverjum morgni eða á hverjum mánudegi, eða þegar tilkynning berst frá sölu eða framleiðslu, eftir því um hvers konar eftirspurn er að ræða."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2992c2a9cbd2142e69cfb59294791ec31ce4dcb1
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-planning-supplies-manually"></a><span data-ttu-id="af582-104">Kynning: Handvirk áætlun birgða</span><span class="sxs-lookup"><span data-stu-id="af582-104">Walkthrough: Planning Supplies Manually</span></span>
<span data-ttu-id="af582-105">Þessi kynning sýnir ferli áætlunar birgðapantana til að uppfylla nýja eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="af582-105">This walkthrough demonstrates the process of planning supply orders to fulfill new demand.</span></span> <span data-ttu-id="af582-106">Hægt er að hefja áætlun birgða með föstu millibili, t.d. á hverjum morgni eða á hverjum mánudegi, eða þegar tilkynning berst frá sölu eða framleiðslu, eftir því um hvers konar eftirspurn er að ræða.</span><span class="sxs-lookup"><span data-stu-id="af582-106">You can initiate supply planning at fixed intervals, for example, every morning or every Monday, or when you are notified by sales or production, depending on the type of demand.</span></span> <span data-ttu-id="af582-107">Í þessari kynningu verður notaður glugginn **Pantanaáætlun**, einfalt birgðaáætlunarverkfæri sem byggir á handvirkri ákvarðanatöku í stað sjálfvirkrar áætlanagerðar sem byggir á færibreytum.</span><span class="sxs-lookup"><span data-stu-id="af582-107">In this walkthrough you will use the **Order Planning** window, a simple supply planning tool that is based on manual decision-making instead of parameter-based automatic planning.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="af582-108">Um kynninguna</span><span class="sxs-lookup"><span data-stu-id="af582-108">About This Walkthrough</span></span>  
 <span data-ttu-id="af582-109">Þessi kynning fjallar um eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="af582-109">This walkthrough illustrates the following tasks:</span></span>  

-   <span data-ttu-id="af582-110">Áætlun um innkaupapöntun fyrir framleiðslu hluta.</span><span class="sxs-lookup"><span data-stu-id="af582-110">Planning a purchase order for manufacturing components.</span></span>  
-   <span data-ttu-id="af582-111">Áætlun um millifærslupöntun til að uppfylla eftirspurn sölu.</span><span class="sxs-lookup"><span data-stu-id="af582-111">Planning a transfer order to fulfill sales demand.</span></span>  
-   <span data-ttu-id="af582-112">Áætlun um framleiðslupöntun fyrir margþrepa atriði.</span><span class="sxs-lookup"><span data-stu-id="af582-112">Planning a production order for a multilevel item.</span></span>  

## <a name="roles"></a><span data-ttu-id="af582-113">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="af582-113">Roles</span></span>  
 <span data-ttu-id="af582-114">Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:</span><span class="sxs-lookup"><span data-stu-id="af582-114">This walkthrough demonstrates tasks performed by the following user roles:</span></span>  

-   <span data-ttu-id="af582-115">Framleiðslustjóri</span><span class="sxs-lookup"><span data-stu-id="af582-115">Production Planner</span></span>  
-   <span data-ttu-id="af582-116">Innkaupaaðili</span><span class="sxs-lookup"><span data-stu-id="af582-116">Purchasing Agent</span></span>  
-   <span data-ttu-id="af582-117">Sölupöntunarvinnsla</span><span class="sxs-lookup"><span data-stu-id="af582-117">Sales Order Processor</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="af582-118">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="af582-118">Prerequisites</span></span>  
 <span data-ttu-id="af582-119">Áður en kynningin hefst þarf að setja upp [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="af582-119">Before you begin this walkthrough, you must install the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="af582-120">Eftirtaldar breytingar þarf að gera á grunninum:</span><span class="sxs-lookup"><span data-stu-id="af582-120">The following modifications must be made to the database:</span></span>  

-   <span data-ttu-id="af582-121">Eyða öllum sölupöntunum vegna reiðhjóla.</span><span class="sxs-lookup"><span data-stu-id="af582-121">Delete all existing sales orders for bicycles.</span></span>  
-   <span data-ttu-id="af582-122">Stofna eina sölupöntun fyrir 10 reiðhjól hjá staðsetningunni BLÁTT.</span><span class="sxs-lookup"><span data-stu-id="af582-122">Create one sales order for 10 bicycles at BLUE location.</span></span>  
-   <span data-ttu-id="af582-123">Eyða öllum áætluðum og fastáætluðum framleiðsluáætlunum.</span><span class="sxs-lookup"><span data-stu-id="af582-123">Delete all planned and firm planned production orders.</span></span> <span data-ttu-id="af582-124">Ekki eyða pöntunum sem þegar eru í gangi með færslum sem þegar eru skráðar.</span><span class="sxs-lookup"><span data-stu-id="af582-124">Do not delete started orders with entries that are already posted.</span></span>  

 <span data-ttu-id="af582-125">Regla er að nota gögnin sem lagt er til í þessari kynningu vegna þess að þau gögn hafa nauðsynlegar skrár.</span><span class="sxs-lookup"><span data-stu-id="af582-125">As a rule, use the suggested data in this walkthrough because this data has the necessary records.</span></span>  

## <a name="story"></a><span data-ttu-id="af582-126">Ferill</span><span class="sxs-lookup"><span data-stu-id="af582-126">Story</span></span>  
 <span data-ttu-id="af582-127">Erla, sem er framleiðslustjóri lítils framleiðslufyrirtækis, er um það bil að fara að áætla framleiðslu og innkaupapantanir til að uppfylla nýja eftirspurn í sölu.</span><span class="sxs-lookup"><span data-stu-id="af582-127">Eduardo, the Production Planner of a small manufacturing company, is about to plan production and purchase orders to fulfill new sales demand.</span></span>  

 <span data-ttu-id="af582-128">Vegna þess að framleiðslan hefur fá stig framleiðsluuppskrifta og flæði pantana er tiltölulega hæggengt notar Erla gluggann **Pantanaáætlun** til að stofna framboðspantanir handvirkt, eitt framleiðsluskref í einu.</span><span class="sxs-lookup"><span data-stu-id="af582-128">Because the products have few BOM levels and the flow of orders is relatively low, Eduardo uses the **Order Planning** window to manually create supply orders, one product level at a time.</span></span>  

 <span data-ttu-id="af582-129">Í flóknara framleiðsluumhverfi er vinnublaðið fyrir áætlun notað til að gera áætlun um framboð sem byggir á vöruþáttum eins og enduráætlunartímabil, öryggisforskot, endurpöntunarmark og keyrslu útreikninga eftirspurnar allra framleiðslustiga sem steypt hefur verið saman.</span><span class="sxs-lookup"><span data-stu-id="af582-129">In a more complex manufacturing environment, the planning worksheet is used to plan supply based on item parameters such as rescheduling period, safety lead time, reorder point, and batch calculations of consolidated demand from all product levels.</span></span>  

## <a name="setting-up-the-sample-data"></a><span data-ttu-id="af582-130">Uppsetning sýnigagna</span><span class="sxs-lookup"><span data-stu-id="af582-130">Setting Up the Sample Data</span></span>  
 <span data-ttu-id="af582-131">Staðlaða sýnifyrirtækið CRONUS er eins og stendur með mikið af óáætlaðri eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="af582-131">The standard CRONUS demonstration company currently has lots of unplanned demand.</span></span> <span data-ttu-id="af582-132">Í ólíkum verkefnum áætlana sem eru í þessari kynningu verður að víkja frá raunverulegu viðskiptaflæði með því að hundsa kröfur sem hafa gjalddaga sem stutt er í og nota þess í stað kröfur með gjalddaga sem er síðar.</span><span class="sxs-lookup"><span data-stu-id="af582-132">During the different planning tasks in this walkthrough, you will have to deviate from the realistic business flow by ignoring demand with close due dates and instead use demand with later due dates.</span></span>  

## <a name="using-the-order-planning-window"></a><span data-ttu-id="af582-133">Glugginn Pantanaáætlun notaður</span><span class="sxs-lookup"><span data-stu-id="af582-133">Using the Order Planning Window</span></span>  

<!-- 
The **Order Planning** window can be accessed from several different locations on the **Departments** menu in the navigation pane:  

-   Manufacturing, Planning  
-   Sales & Marketing, Order Processing  
-   Purchase, Planning  
-   In addition, you can open this window for a specific production order by choosing **Planning** on the **Navigate** tab in the **Order** group.

-->  

### <a name="to-use-the-order-planning-window"></a><span data-ttu-id="af582-134">Til að nota gluggann Pantanaáætlun</span><span class="sxs-lookup"><span data-stu-id="af582-134">To use the Order Planning window</span></span>  

1.  <span data-ttu-id="af582-135">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **pantanaáætlun** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="af582-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Order Planning**, and then choose the related link.</span></span>  

     <span data-ttu-id="af582-136">Eftir að glugginn **Pantanaáætlun** opnast fyrst þarf að reikna áætlun til að sýna nýja eftirspurn frá því hún var reiknuð síðast.</span><span class="sxs-lookup"><span data-stu-id="af582-136">When the **Order Planning** window first opens, a plan must be calculated to show the new demand since it was last calculated.</span></span>  

2.  <span data-ttu-id="af582-137">Velja **Reikna áætlun** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="af582-137">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="af582-138">Áætlunarkerfið greinir hverja nýja eftirspurn sem hefur komið fram, svo sem nýja sölu eða framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="af582-138">The planning system analyzes any new demand that has been introduced, such as new sales, changed sales, or production orders.</span></span>  

     <span data-ttu-id="af582-139">Magnið sem þörf er á fyrir hverja eftirspurnarlínu er reiknað út og byggir á heildarmagni sem til ráðstöfunar er.</span><span class="sxs-lookup"><span data-stu-id="af582-139">Based on total availability, the quantity needed for each demand line is calculated.</span></span> <span data-ttu-id="af582-140">Útreikningurinn er gerður fyrir hverja pöntun fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="af582-140">This calculation is performed order-by-order.</span></span> <span data-ttu-id="af582-141">Það þýðir að pöntunin sem inniheldur eftirspurnarlínuna með fyrstu skila-/afhendingardagsetninguna er tekin fyrir fyrst.</span><span class="sxs-lookup"><span data-stu-id="af582-141">This means that the order which includes the demand line with the earliest due date or shipment date will be calculated first.</span></span> <span data-ttu-id="af582-142">Eftir það eru allar aðrar eftirspurnarlínur reiknaðar í sömu röð, óháð skila- eða afhendingardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="af582-142">After that, additional demand lines will be calculated in the same order, regardless of the due date or shipment date.</span></span>  

3.  <span data-ttu-id="af582-143">Ganga þarf úr skugga um að glugginn **Pantanaáætlun** sé stækkaður og að reitir dálka séu af þeirri stærð að þeir sýni öll sjálfgefin heiti reita.</span><span class="sxs-lookup"><span data-stu-id="af582-143">Be sure that the **Order Planning** window is maximized and that column fields are resized to show all the default field names.</span></span>  

     <span data-ttu-id="af582-144">Þegar útreikningi er lokið þá sýnir glugginn alla óuppfyllta eftirspurn sem línur pöntunarhauss sem hefur verið felldar saman, flokkað eftir nýjustu dagsetningu eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="af582-144">When the calculation is completed, the window displays all unfulfilled demand as collapsed order header lines sorted by earliest demand date.</span></span>  

     <span data-ttu-id="af582-145">Takið eftir að CRONUS hefur margar pantanir með óuppfyllta eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="af582-145">Notice that CRONUS has several orders with unfulfilled demand.</span></span> <span data-ttu-id="af582-146">Hver feitletruð áætlunarlína stendur fyrir pöntun, sölupöntun eða framleiðslupöntun; af þeim er að minnsta kosti ein pantanalína með sem uppfyllir ekki ráðstöfunarkröfur.</span><span class="sxs-lookup"><span data-stu-id="af582-146">Each bold planning line represents an order, sales order, or production order, including at least one order line with insufficient availability.</span></span>  

4.  <span data-ttu-id="af582-147">Í reitnum **Sýna eftirspurn sem** skal velja afmörkunina **Alla eftirspurn**.</span><span class="sxs-lookup"><span data-stu-id="af582-147">In the **Show Demand As** field, select the **All Demand** filter.</span></span>  

     <span data-ttu-id="af582-148">Innan reitsins **Tegund eftirspurnar** má velja hvaða tegundir pantana á að birta.</span><span class="sxs-lookup"><span data-stu-id="af582-148">With the **Demand Type** field, you can choose which order types that you want to display.</span></span>  

     <span data-ttu-id="af582-149">Pantanir sem ekki eru vandamál varðandi tiltækt magn eru ekki sýndar.</span><span class="sxs-lookup"><span data-stu-id="af582-149">Orders that do not have availability problems are not shown.</span></span> <span data-ttu-id="af582-150">Ef engar pantanir eru til staðar þegar áætlun er reiknuð birtast skilaboð og engar áætlunarlínur birtast.</span><span class="sxs-lookup"><span data-stu-id="af582-150">If no orders exist when a plan is calculated, a message will display and no planning lines will appear.</span></span>  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a><span data-ttu-id="af582-151">Innkaupapöntun áætluð til að uppfylla eftirspurn íhluta</span><span class="sxs-lookup"><span data-stu-id="af582-151">Planning a Purchase Order to Fulfill Component Demand</span></span>  
 <span data-ttu-id="af582-152">Í þessu ferli er stofnuð innkaupapöntun fyrir íhluti sem þarf til framleiðslunnar.</span><span class="sxs-lookup"><span data-stu-id="af582-152">In this procedure, you create a purchase order for needed manufacturing components.</span></span>  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><span data-ttu-id="af582-153">Til að áætla innkaupapöntun til að uppfylla þörf á íhlutum fyrir framleiðslu</span><span class="sxs-lookup"><span data-stu-id="af582-153">To plan a purchase order to fulfill component need in production</span></span>  

1.  <span data-ttu-id="af582-154">Fyrsta línan er stækkuð (veljið táknið +).</span><span class="sxs-lookup"><span data-stu-id="af582-154">Expand the first line (choose the + symbol).</span></span>  
2.  <span data-ttu-id="af582-155">Veljið fyrstu eftirspurnarlínuna, með vöru **LSU-15** og síðan **Sýna fylgiskjal** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="af582-155">Choose the first demand line, with item **LSU-15**, and then choose the **Show Document** action.</span></span>  
3.  <span data-ttu-id="af582-156">Opinni framleiðslupöntun er lokað til að fara aftur í gluggann **Pantanaáætlun**.</span><span class="sxs-lookup"><span data-stu-id="af582-156">Close the opened production order to return to the **Order Planning** window.</span></span>  
4.  <span data-ttu-id="af582-157">Í reitnum **Áfyllingarkerfið** eru **Innkaup** valin.</span><span class="sxs-lookup"><span data-stu-id="af582-157">In the **Replenishment System** field, select **Purchase**.</span></span>  

     <span data-ttu-id="af582-158">Sjálfgefna gildið er af birgðaspjaldinu eða birgðahaldseiningaspjaldinu, en því er hægt að breyta í einn af eftirtöldum valkostum:</span><span class="sxs-lookup"><span data-stu-id="af582-158">The default value is from the item card, or SKU card, but you can change it to one of the following options:</span></span>  

    -   <span data-ttu-id="af582-159">**Innkaup** – Til að búa til innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="af582-159">**Purchase** – To create a purchase order.</span></span>  
    -   <span data-ttu-id="af582-160">**Millifærsla** – til að búa til millifærslupöntun.</span><span class="sxs-lookup"><span data-stu-id="af582-160">**Transfer** – To create a transfer order.</span></span>  
    -   <span data-ttu-id="af582-161">**Framl.pöntun** – Til að búa til framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="af582-161">**Prod. Order** – To create a production order.</span></span>  

5.  <span data-ttu-id="af582-162">Í reitnum **Framboð frá** þarf að velja eitt af eftirfarandi valmöguleikum til hliðsjónar við valið áfyllingarkerfi:</span><span class="sxs-lookup"><span data-stu-id="af582-162">In the **Supply From** field, select one of the following options according to the selected replenishment system:</span></span>  

    -   <span data-ttu-id="af582-163">**Lánardrottinn** – Fyrir innkaup</span><span class="sxs-lookup"><span data-stu-id="af582-163">**Vendor** – For purchases</span></span>  
    -   <span data-ttu-id="af582-164">**Birgðageymsla** – fyrir flutning</span><span class="sxs-lookup"><span data-stu-id="af582-164">**Location** – For transfers</span></span>  

     <span data-ttu-id="af582-165">Ef reiturinn er ekki fylltur út þá koma fram villuboð þegar reynt er að stofna framboðspöntun.</span><span class="sxs-lookup"><span data-stu-id="af582-165">If the field is not filled in, an error message will display when you try to create the supply orders.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="af582-166">Hafi íhlutirnir uppsett sjálfgefin númer lánadrottna á birgðaspjaldi, þá verða línurnar endurstilltar.</span><span class="sxs-lookup"><span data-stu-id="af582-166">If the components have a default vendor number set up on the item cards, the lines will be preset.</span></span>  

6.  <span data-ttu-id="af582-167">Velja reitinn **Framboð frá**.</span><span class="sxs-lookup"><span data-stu-id="af582-167">Choose the **Supply From**  field.</span></span>  
7.  <span data-ttu-id="af582-168">Í glugganum **Vörulisti lánardrottins** skal velja aðgerðina **Nýtt** og svo er lánadrottinn **30000** valinn.</span><span class="sxs-lookup"><span data-stu-id="af582-168">In the **Item Vendor Catalogue** window, choose the **New** action, and then select vendor **30000**.</span></span>  
8.  <span data-ttu-id="af582-169">Velja hnappinn **Í lagi** til að snúa aftur í gluggann **Pantanaáætlun**.</span><span class="sxs-lookup"><span data-stu-id="af582-169">Choose the **OK** button to return to the **Order Planning** window.</span></span>  
9. <span data-ttu-id="af582-170">Afrita lánardrottinn **30000** í aðrar línur fyrir hátalaraíhlutina á þessari framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="af582-170">Copy vendor **30000** to the other lines for loudspeaker components on this production order.</span></span>  

     <span data-ttu-id="af582-171">Nú er hægt að stofna innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="af582-171">You are now ready to create a purchase order.</span></span>  

10. <span data-ttu-id="af582-172">Velja **búa til Pantanir** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="af582-172">Choose the **Make Orders** action.</span></span> <span data-ttu-id="af582-173">Glugginn **Gera framboðspantanir** opnast.</span><span class="sxs-lookup"><span data-stu-id="af582-173">The **Make Supply Orders** window opens.</span></span>  
11. <span data-ttu-id="af582-174">Í  **Pantanaáætlun** á flýtiflipanum **Gera pantanir fyrir** skal velja kostinn **Virk pöntun**.</span><span class="sxs-lookup"><span data-stu-id="af582-174">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **Active Order** option.</span></span>  
12. <span data-ttu-id="af582-175">Á flýtiflipanum **Valkostir** í reitnum **Stofna innkaupapöntun** er kosturinn **Gera innkaupapantanir** valinn.</span><span class="sxs-lookup"><span data-stu-id="af582-175">On the **Options** FastTab, in the **Create Purchase Order** field, choose the **Make Purch. Order** option.</span></span>  
13. <span data-ttu-id="af582-176">Veldu hnappinn **Í lagi** til að stofna innkaupapantanir fyrir alla íhluti pöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="af582-176">Choose the **OK** button to create purchase orders for all the components of the order.</span></span>  

     <span data-ttu-id="af582-177">Innkaupapantanirnar hafa nú verið stofnaðar og vistaðar sem síðustu pantanir í listanum yfir innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="af582-177">The purchase orders are now created and saved as the last orders in the list of purchase orders.</span></span>  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="af582-178">Millifærslupöntun áætluð til að uppfylla eftirspurn sölu</span><span class="sxs-lookup"><span data-stu-id="af582-178">Planning a Transfer Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="af582-179">Í þessu ferli er eftirspurn áætluð út frá sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="af582-179">In this procedure, you will plan for demand from a sales order.</span></span> <span data-ttu-id="af582-180">Eftirspurnarlínur gefa sölulínur til kynna en ekki íhlutalínur eins og í framleiðslueftirspurn.</span><span class="sxs-lookup"><span data-stu-id="af582-180">Demand lines represent sales lines and not component lines, as in production demand.</span></span>  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="af582-181">Áætlun um millifærslupöntun til að uppfylla eftirspurn sölu</span><span class="sxs-lookup"><span data-stu-id="af582-181">To plan a transfer order to fulfill sales demand</span></span>  

1.  <span data-ttu-id="af582-182">Bendillinn er færður á áætlunarlínu fyrir pöntun **2008**.</span><span class="sxs-lookup"><span data-stu-id="af582-182">Move the pointer to the planning line for order **2008**.</span></span>  
2.  <span data-ttu-id="af582-183">Stækka skal línuna og færa bendilinn á eftirspurnarlínu.</span><span class="sxs-lookup"><span data-stu-id="af582-183">Expand the line and move the pointer to the demand line.</span></span>  

     <span data-ttu-id="af582-184">Sölupöntun **2008** er fyrir tíu hátalara af vöru **LS-120**, pantað af John Haddock Insurance Co.</span><span class="sxs-lookup"><span data-stu-id="af582-184">Sales order **2008** is for ten loudspeakers, item **LS-120**, ordered by John Haddock Insurance Co.</span></span>  

     <span data-ttu-id="af582-185">Þá birtist skilgreint áfyllingarkerfi vörunnar og sjálfgefinn lánadrottinn.</span><span class="sxs-lookup"><span data-stu-id="af582-185">The item’s defined replenishment system and default vendor will display.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="af582-186">Neðst í glugganum eru fjórir upplýsingareitir.</span><span class="sxs-lookup"><span data-stu-id="af582-186">At the bottom of the window, there are four information fields.</span></span> <span data-ttu-id="af582-187">Í reitnum **Fyrsta tiltæka dagsetning** munu þeir tíu hlutir sem þörf er á vera til taks, fyrir framboðspöntun á innleið, níu dögum eftir núverandi lokadag.</span><span class="sxs-lookup"><span data-stu-id="af582-187">In the **Earliest Date Available** field, the ten pieces that are needed will be available, on an inbound supply order, nine days later than the current due date.</span></span> <span data-ttu-id="af582-188">Ef þetta er of seint fyrir viðskiptamanninn þá sýnir reiturinn **Tiltækt fyrir millifærslu** 13 stykki vörunnar á annarri staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="af582-188">If this is too late for the customer, the **Available for Transfer** field shows 13 pieces of the item at another location.</span></span> <span data-ttu-id="af582-189">Áætla þarf fyrir þessar birgðir.</span><span class="sxs-lookup"><span data-stu-id="af582-189">You will want to plan for this stock.</span></span>  

3.  <span data-ttu-id="af582-190">Smellt er á **Tiltækt fyrir millifærslu** til að opna gluggann **Sækja annað framboð**.</span><span class="sxs-lookup"><span data-stu-id="af582-190">Choose the **Available for Transfer** field to open the **Get Alternative Supply** window.</span></span>  
4.  <span data-ttu-id="af582-191">Veldu hnappinn **Í lagi** til að bóka þau tíu eintök sem eru tiltæk.</span><span class="sxs-lookup"><span data-stu-id="af582-191">Choose the **OK** button to book the ten items that are available.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="af582-192">Í eftirspurnarlínuna hefur innkaupatillögu verið skipt út fyrir flutning frá GRÆNNI birgðageymslu.</span><span class="sxs-lookup"><span data-stu-id="af582-192">In the demand line, the suggested purchase has been exchanged with a transfer from GREEN location.</span></span> <span data-ttu-id="af582-193">Aðgerðin **Búa til pöntun** stofnar flutning frá GRÆNNI til staðar þaðan sem eftirspurnin kemur.</span><span class="sxs-lookup"><span data-stu-id="af582-193">The **Make Orders** function creates a transfer order from GREEN to the demanded location.</span></span> <span data-ttu-id="af582-194">Reiturinn **Staðgenglar eru til** virkar á sama hátt.</span><span class="sxs-lookup"><span data-stu-id="af582-194">The **Substitutes Exists** field works in the same way.</span></span>  

5.  <span data-ttu-id="af582-195">Velja **búa til Pantanir** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="af582-195">Choose the **Make Orders** action.</span></span> <span data-ttu-id="af582-196">Glugginn **Gera framboðspantanir** opnast.</span><span class="sxs-lookup"><span data-stu-id="af582-196">The **Make Supply Orders** window opens.</span></span>  
6.  <span data-ttu-id="af582-197">Í  **Pantanaáætlun** á flýtiflipanum **Gera pantanir fyrir** skal velja kostinn **Virka pöntunin**.</span><span class="sxs-lookup"><span data-stu-id="af582-197">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **The Active Order** option.</span></span>  
7.  <span data-ttu-id="af582-198">Á flýtiflipanum **Valkostir** í reitnum **Stofna millifærslupöntun** skal velja kostinn **Gera millif.pantanir**.</span><span class="sxs-lookup"><span data-stu-id="af582-198">On the **Options** FastTab, in the **Create Transfer Order** field, select the **Make Trans. Orders** option.</span></span>  
8.  <span data-ttu-id="af582-199">Veldu hnappinn **Í lagi** til að stofna millifærslupöntun til að anna sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="af582-199">Choose the **OK** button to create the transfer order to supply the sales order.</span></span>  

     <span data-ttu-id="af582-200">Millifærslupöntun hefur nú verið gerð og vistuð í listanum sem síðasta pöntun í listanum yfir opnar millifærslupantanir.</span><span class="sxs-lookup"><span data-stu-id="af582-200">The transfer order is now created and saved in the list as the last order in the list of open transfer orders.</span></span>  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><span data-ttu-id="af582-201">Margþrepa millifærslupöntun áætluð til að uppfylla eftirspurn sölu</span><span class="sxs-lookup"><span data-stu-id="af582-201">Planning a Multilevel Production Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="af582-202">Í þessu ferli er gerð áætlun til að uppfylla eftirspurn sölu fyrir framleiðslu sem hefur mörg framleiðsluþrep þar sem hvert og eitt myndar háða eftirspurn framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="af582-202">In this procedure, you will plan to fulfill sales demand for a produced item with multiple product levels, each creating dependent production demand.</span></span>  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><span data-ttu-id="af582-203">Að áætla margra þrepa framleiðslu til að uppfylla eftirspurn sölu</span><span class="sxs-lookup"><span data-stu-id="af582-203">To plan multilevel production to fulfill sales demand</span></span>  

1.  <span data-ttu-id="af582-204">Áætlunarlína með pöntun fyrir eftirspurn sölu **1001** er valin (stofnuð áður sem frumskilyrði).</span><span class="sxs-lookup"><span data-stu-id="af582-204">Select the planning line with sales demand for order **1001**, created earlier as prerequisite data.</span></span>  

     <span data-ttu-id="af582-205">Þessi eftirspurn er sölulína en varan hefur skilgreint áfyllingarkerfi sem er **Framl.pöntun**.</span><span class="sxs-lookup"><span data-stu-id="af582-205">This demand is a sales line, but the item has a defined replenishment system of **Prod. Order**.</span></span> <span data-ttu-id="af582-206">Haldið er áfram til að bæta annarri bjöllu við íhlutaþörf hvers hjóls.</span><span class="sxs-lookup"><span data-stu-id="af582-206">Proceed to add an extra bell to the component need of each bicycle.</span></span>  

2.  <span data-ttu-id="af582-207">Veldu **Íhlutir** aðgerðina til að opna gluggann **Áætla Íhlutir** .</span><span class="sxs-lookup"><span data-stu-id="af582-207">Choose the **Components** action to open the **Planning Components** window.</span></span>  
3.  <span data-ttu-id="af582-208">Í línunni með bjölluvörunni skal breyta reitnum **Magn á** úr **1** í **2**.</span><span class="sxs-lookup"><span data-stu-id="af582-208">On the line with the Bell item, change the **Quantity per** field from **1** to **2**.</span></span>  
4.  <span data-ttu-id="af582-209">Í glugganum **Pantanaáætlun** þarf að meta möguleika fyrir pöntunina.</span><span class="sxs-lookup"><span data-stu-id="af582-209">In the **Order Planning** window, consider your planning alternatives.</span></span> <span data-ttu-id="af582-210">Í þessu tilfelli eru engar aðrar leiðir til framboðs, engir staðgenglar, millifærslur, eða síðari afhending.</span><span class="sxs-lookup"><span data-stu-id="af582-210">In this case, you have no alternative means of supply, no transfer, substitute, or later delivery.</span></span> <span data-ttu-id="af582-211">Stofna þarf birgðapöntunina sem lögð er til, framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="af582-211">You must create the suggested supply order, a production order.</span></span>  
5.  <span data-ttu-id="af582-212">Velja **búa til Pantanir** aðgerð til að stofna framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="af582-212">Choose the **Make Orders** action to create the production order.</span></span>  

     <span data-ttu-id="af582-213">Í glugganum **Pantanaáætlun** sést að áætlunarlínan fyrir sölupöntun **1001** er ekki lengur til staðar og séð hefur verið um upphaflega eftirspurn sölu.</span><span class="sxs-lookup"><span data-stu-id="af582-213">In the **Order Planning** window, notice that the planning line for sales order **1001** no longer exists and that the initial sales demand has been covered.</span></span>  

6.  <span data-ttu-id="af582-214">Glugganum **Pantanaáætlun** er lokað.</span><span class="sxs-lookup"><span data-stu-id="af582-214">Close the **Order Planning** window.</span></span>  

     <span data-ttu-id="af582-215">Nú væri hægt að velja að halda áfram í þessari valmynd og ljúka öllum áætlanagerðum.</span><span class="sxs-lookup"><span data-stu-id="af582-215">Now, you could choose to stay in this view and complete all the planning tasks.</span></span> <span data-ttu-id="af582-216">Þess í stað er nú farið í hlutverk framleiðslustjóra með því að fara í framleiðslupöntunina sem verið var að gera og opna gluggann **Pantanaáætlun**.</span><span class="sxs-lookup"><span data-stu-id="af582-216">Instead, you will now take on the Production Planner role by going to the production order that you just created and access the **Order Planning** window.</span></span>  

 <span data-ttu-id="af582-217">Framleiðslustjóri þarf að áætla sérstaka röð framleiðslupantana.</span><span class="sxs-lookup"><span data-stu-id="af582-217">As a production planner you now must plan a specific production order.</span></span>  

### <a name="to-plan-a-specific-production-order"></a><span data-ttu-id="af582-218">Til að áætla sérstaka röð framleiðslupöntunar</span><span class="sxs-lookup"><span data-stu-id="af582-218">To plan a specific production order</span></span>  

1.  <span data-ttu-id="af582-219">Opna skal framleiðslupöntunina **101001**, fyrir tíu reiðhjól, sem var stofnuð með aðgerðinni **Gera pantanir**.</span><span class="sxs-lookup"><span data-stu-id="af582-219">Open the production order **101001**, for ten bicycles, that you just created by using the **Make Orders** function.</span></span>  
2.  <span data-ttu-id="af582-220">Opna gluggann **Íhlutir framl.pöntunar** til að athuga hvort staka bjallan endurspeglist í framleiðslupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="af582-220">Open the **Prod. Order Components** window to check that the extra bell is reflected on the production order.</span></span>  
3.  <span data-ttu-id="af582-221">Veldu aðgerðina **Áætlun**.</span><span class="sxs-lookup"><span data-stu-id="af582-221">Choose the **Planning** action.</span></span>  

     <span data-ttu-id="af582-222">Glugginn **Pantanaáætlun** opnast í útliti sem er alltaf síað niður á tiltekna framleiðslueftirspurn.</span><span class="sxs-lookup"><span data-stu-id="af582-222">The **Order Planning** window opens in a view that is always filtered on the specific production demand.</span></span> <span data-ttu-id="af582-223">Eftirspurn sölu er ekki sýnd.</span><span class="sxs-lookup"><span data-stu-id="af582-223">Sales demand is not displayed.</span></span> <span data-ttu-id="af582-224">Reikna þarf áætlun áður en hægt er að sjá nokkra viðbótareftirspurn.</span><span class="sxs-lookup"><span data-stu-id="af582-224">You must calculate a plan before you can see any additional demand.</span></span>  

4.  <span data-ttu-id="af582-225">Velja **Reikna áætlun** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="af582-225">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="af582-226">Takið eftir að fjórar nýjar framleiðslupantanir koma fram sem óáætluð eftirspurn framleiðslu sem dregin er af pöntun **101001**.</span><span class="sxs-lookup"><span data-stu-id="af582-226">Notice that four new production orders appear as unplanned production demand derived from order **101001**.</span></span> <span data-ttu-id="af582-227">Nýju línurnar standa fyrir nýja eftirspurn framleiðslu frá millivörum sem þarf að stofna til að framleiða pöntunina.</span><span class="sxs-lookup"><span data-stu-id="af582-227">The new lines represent new production demand from the subassemblies that must be created to produce the order.</span></span>  

5.  <span data-ttu-id="af582-228">Veldu aðgerðina **Stækka allt** til að fá yfirlit yfir alla framleiðslueftirspurnina fyrir framleiðslupantanirnar.</span><span class="sxs-lookup"><span data-stu-id="af582-228">Choose the **Expand All** action to get an overview of all the production demand for the production orders.</span></span>  

     <span data-ttu-id="af582-229">Til að leggja fram viðbótarupplýsingar um eftirspurnarlínur gæti verið ráðlegt að bæta reitunum **Magn eftirspurnar** og **Tiltækt magn eftirspurnar** í gluggann.</span><span class="sxs-lookup"><span data-stu-id="af582-229">To provide additional information about the demand lines, you may want to add the **Demand Quantity** and **Demand Qty. Available** fields to your view.</span></span>  

     <span data-ttu-id="af582-230">Nú þarf að bjóða fram tíu stykki af hverjum íhlut.</span><span class="sxs-lookup"><span data-stu-id="af582-230">Now you must supply ten of each component.</span></span>  

     <span data-ttu-id="af582-231">Athugið að fjórar af eftirspurnarlínunum hafa framleiðslupantanir áfyllingarkerfis.</span><span class="sxs-lookup"><span data-stu-id="af582-231">Note that four of the demand lines have replenishment system Prod. Order.</span></span> <span data-ttu-id="af582-232">Þessir fjórir samsetningarhlutar eru annað framleiðslustig reiðhjólsins.</span><span class="sxs-lookup"><span data-stu-id="af582-232">These four subassemblies represent the second product level of the bicycle.</span></span>  

     <span data-ttu-id="af582-233">Sjálfgefnar stillingar áfyllingar eru þegar útfylltar og halda má áfram til að gera pantanir.</span><span class="sxs-lookup"><span data-stu-id="af582-233">The default replenishment settings are already filled in and you can proceed to make orders.</span></span>  

6.  <span data-ttu-id="af582-234">Velja **búa til Pantanir** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="af582-234">Choose the **Make Orders** action.</span></span>  

     <span data-ttu-id="af582-235">Áður er hnappurinn **Í lagi** er valinn ætti að lesa textann á flýtiflipanum **Pantanaáætlun**.</span><span class="sxs-lookup"><span data-stu-id="af582-235">Before you choose the **OK** button, notice the text on the **Order Planning** FastTab.</span></span> <span data-ttu-id="af582-236">Þessi texti er mikilvægur vegna þess að vitað er að reiðhjólið hefur nokkra framleidda íhluti—millivörur—í framleiðsluferli sínu sem gæti orðið eftirspurn eftir þegar þessi framleiðslupöntun hefur verið gerð.</span><span class="sxs-lookup"><span data-stu-id="af582-236">This text is important because you know that the bicycle has several produced components, subassemblies, in its product structure that might be in demand when you create this production order.</span></span>  

7.  <span data-ttu-id="af582-237">Í glugganum **Gera framboðspantanir** í reitnum **Gera pantanir fyrir** veljið valkostinn **Allar línur** og veljið svo hnappinn **Í lagi** til að stofna framleiðslupöntun fyrir annað framleiðslustig pöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="af582-237">In the **Make Supply Order** window, in the **Make Orders for** field, choose the **All Lines** option, and then choose the **OK** button to create production orders for the second product level of the order.</span></span>  

     <span data-ttu-id="af582-238">Athugið að eftirspurn framleiðslu á efsta stigi fyrir framleiðslupöntun 101001 er ekki lengur til.</span><span class="sxs-lookup"><span data-stu-id="af582-238">Note that the top-level production demand for production order 101001 no longer exists.</span></span> <span data-ttu-id="af582-239">Það þýðir að gerð hefur verið áætlun fyrir upphaflega eftirspurn framleiðslu fyrir millivörur.</span><span class="sxs-lookup"><span data-stu-id="af582-239">This means that the initial production demand for subassemblies has been planned for.</span></span>  

     <span data-ttu-id="af582-240">Í glugganum **Pantanaáætlun** má reikna áætlun aftur til að gera áætlun um byggingu reiðhjólsins.</span><span class="sxs-lookup"><span data-stu-id="af582-240">In the **Order Planning** window, you calculate a plan again in order to plan the bicycle structure.</span></span>  

8.  <span data-ttu-id="af582-241">Velja aðgerðina **Reikna áætlun** til að endurreikna áætlun eins og mælt er fyrir um í meðfylgjandi Hjálpartexta.</span><span class="sxs-lookup"><span data-stu-id="af582-241">Choose the **Calculate Plan** action to recalculate the plan as instructed by the embedded Help text.</span></span>  

     <span data-ttu-id="af582-242">Nýju línurnar tvær standa fyrir viðbótareftirspurn framleiðslu sem tengist millivörunum sem áætlun var gerð um í fyrri þrepum.</span><span class="sxs-lookup"><span data-stu-id="af582-242">The two new lines represent additional production demand derived from the subassemblies planned in the previous steps.</span></span> <span data-ttu-id="af582-243">Lagt er til að tvær framleiðslupantanir séu gerðar fyrir framboð á hjólnöfunum, ein fyrir 10 framnafir og ein fyrir 10 afturnafir.</span><span class="sxs-lookup"><span data-stu-id="af582-243">It is suggested that you make two production orders to supply the wheel hubs, one for 10 front hubs and one for 10 back hubs.</span></span>  

9. <span data-ttu-id="af582-244">Veldu aðgerðina **Stækka allt** til að fá yfirlit yfir alla framleiðslueftirspurnina fyrir þessar tvær framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="af582-244">Choose the **Expand All** action to get an overview of all the demand for the two production orders.</span></span>  

     <span data-ttu-id="af582-245">Tillagan um framboðið gefur til kynna að fjórar innkaupapantanir verði gerðar vegna íhlutanna.</span><span class="sxs-lookup"><span data-stu-id="af582-245">The suggested supply plan indicates that a total of four purchase orders will be created for the components.</span></span> <span data-ttu-id="af582-246">Ákveðið er að gera pantanirnar sem lagt er til.</span><span class="sxs-lookup"><span data-stu-id="af582-246">You decide to make the proposed orders.</span></span>  

10. <span data-ttu-id="af582-247">Velja **búa til Pantanir** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="af582-247">Choose the **Make Orders** action.</span></span>  
11. <span data-ttu-id="af582-248">Í reitnum **Gera pantanir fyrir** veljið valkostinn **Allar línur** og veljið svo hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="af582-248">In the **Make Orders for** field, select the **All Lines** option, and then choose the **OK** button.</span></span> <span data-ttu-id="af582-249">Athuga þarf hvort viðbótareftirspurn er til staðar vegna framleiðslu yfirvörunnar, reiðhjólsins (sem selt er samkvæmt sölupöntun 1001).</span><span class="sxs-lookup"><span data-stu-id="af582-249">Check if additional demand exists for the production of the parent item, the bicycle, which is being sold on sales order 1001.</span></span>  
12. <span data-ttu-id="af582-250">Velja **Reikna áætlun** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="af582-250">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="af582-251">Skilaboðin segja til um að allir tilskildir hlutir séu nú til staðar (að til sé framboð af þeim).</span><span class="sxs-lookup"><span data-stu-id="af582-251">The message indicates that all required items are now supplied.</span></span> <span data-ttu-id="af582-252">Staðfesta fastáætlaðar framleiðslupantanir sem eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="af582-252">Verify the firm planned production orders that are created.</span></span>  

13. <span data-ttu-id="af582-253">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Fastáætluð framleiðslupöntun** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="af582-253">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  

     <span data-ttu-id="af582-254">Í glugganum **Fastáætlað** farið yfir hvernig upphafs- og lokatími einstakra pantana er áætlaður út frá samsetningu framleiðslunnar.</span><span class="sxs-lookup"><span data-stu-id="af582-254">In the **Firm Planned Prod. Orders** window review how start times and end times of individual orders are scheduled according to the product structure.</span></span> <span data-ttu-id="af582-255">Íhlutir á neðsta þrepi eru framleiddir fyrst.</span><span class="sxs-lookup"><span data-stu-id="af582-255">The lowest-level components are produced first.</span></span> <span data-ttu-id="af582-256">Því þarf að áætla pantanir í mörgum þrepum eins og sýnt er í þessu verkflæði fyrir áætlanir.</span><span class="sxs-lookup"><span data-stu-id="af582-256">Therefore, you must plan multilevel orders as demonstrated in this planning workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="af582-257">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="af582-257">See Also</span></span>  
 <span data-ttu-id="af582-258">[Kynningar á viðskiptaferlum](walkthrough-business-process-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="af582-258">[Business Process Walkthroughs](walkthrough-business-process-walkthroughs.md) </span></span>  
 [<span data-ttu-id="af582-259">Kynning: Sjálfvirk áætlun birgða</span><span class="sxs-lookup"><span data-stu-id="af582-259">Walkthrough: Planning Supplies Automatically</span></span>](walkthrough-planning-supplies-automatically.md)

