---
title: Kynning - Handvirk áætlun birgða | Microsoft Docs
description: Þessi kynning sýnir ferli áætlunar birgðapantana til að uppfylla nýja eftirspurn. Hægt er að hefja áætlun birgða með föstu millibili, t.d. á hverjum morgni eða á hverjum mánudegi, eða þegar tilkynning berst frá sölu eða framleiðslu, eftir því um hvers konar eftirspurn er að ræða.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f8c20f51997ca2ec056423b9089b645e5a258235
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "925741"
---
# <a name="walkthrough-planning-supplies-manually"></a><span data-ttu-id="224b2-104">Kynning: Handvirk áætlun birgða</span><span class="sxs-lookup"><span data-stu-id="224b2-104">Walkthrough: Planning Supplies Manually</span></span>

<span data-ttu-id="224b2-105">**Athugið**: Framkvæma verður þessa kynningu í sýnifyrirtæki með valkostinum **Fullt mat - öll sýnigögn** sem er í boði í sandkassaumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="224b2-105">**Note**: This walkthrough must be performed on a demonstration company with the **Full Evaluation - Complete Sample Data** option, which is available in the Sandbox environment.</span></span> <span data-ttu-id="224b2-106">Nánari upplýsingar eru í [Sandkassaumhverfi stofnað](across-how-create-sandbox-environment.md).</span><span class="sxs-lookup"><span data-stu-id="224b2-106">For more information, see [Creating a Sandbox Environment](across-how-create-sandbox-environment.md).</span></span>

<span data-ttu-id="224b2-107">Þessi kynning sýnir ferli áætlunar birgðapantana til að uppfylla nýja eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="224b2-107">This walkthrough demonstrates the process of planning supply orders to fulfill new demand.</span></span> <span data-ttu-id="224b2-108">Hægt er að hefja áætlun birgða með föstu millibili, t.d. á hverjum morgni eða á hverjum mánudegi, eða þegar tilkynning berst frá sölu eða framleiðslu, eftir því um hvers konar eftirspurn er að ræða.</span><span class="sxs-lookup"><span data-stu-id="224b2-108">You can initiate supply planning at fixed intervals, for example, every morning or every Monday, or when you are notified by sales or production, depending on the type of demand.</span></span> <span data-ttu-id="224b2-109">Í þessari kynningu verður notuð síðan **Pantanaáætlun**, einfalt birgðaáætlunarverkfæri sem byggir á handvirkri ákvarðanatöku í stað sjálfvirkrar áætlanagerðar sem byggir á færibreytum.</span><span class="sxs-lookup"><span data-stu-id="224b2-109">In this walkthrough you will use the **Order Planning** page, a simple supply planning tool that is based on manual decision-making instead of parameter-based automatic planning.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="224b2-110">Um kynninguna</span><span class="sxs-lookup"><span data-stu-id="224b2-110">About This Walkthrough</span></span>  
 <span data-ttu-id="224b2-111">Þessi kynning fjallar um eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="224b2-111">This walkthrough illustrates the following tasks:</span></span>  

-   <span data-ttu-id="224b2-112">Áætlun um innkaupapöntun fyrir framleiðslu hluta.</span><span class="sxs-lookup"><span data-stu-id="224b2-112">Planning a purchase order for manufacturing components.</span></span>  
-   <span data-ttu-id="224b2-113">Áætlun um millifærslupöntun til að uppfylla eftirspurn sölu.</span><span class="sxs-lookup"><span data-stu-id="224b2-113">Planning a transfer order to fulfill sales demand.</span></span>  
-   <span data-ttu-id="224b2-114">Áætlun um framleiðslupöntun fyrir margþrepa atriði.</span><span class="sxs-lookup"><span data-stu-id="224b2-114">Planning a production order for a multilevel item.</span></span>  

## <a name="roles"></a><span data-ttu-id="224b2-115">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="224b2-115">Roles</span></span>  
 <span data-ttu-id="224b2-116">Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:</span><span class="sxs-lookup"><span data-stu-id="224b2-116">This walkthrough demonstrates tasks performed by the following user roles:</span></span>  

-   <span data-ttu-id="224b2-117">Framleiðslustjóri</span><span class="sxs-lookup"><span data-stu-id="224b2-117">Production Planner</span></span>  
-   <span data-ttu-id="224b2-118">Innkaupaaðili</span><span class="sxs-lookup"><span data-stu-id="224b2-118">Purchasing Agent</span></span>  
-   <span data-ttu-id="224b2-119">Sölupöntunarvinnsla</span><span class="sxs-lookup"><span data-stu-id="224b2-119">Sales Order Processor</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="224b2-120">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="224b2-120">Prerequisites</span></span>  
 <span data-ttu-id="224b2-121">Áður en kynningin hefst þarf að setja upp [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="224b2-121">Before you begin this walkthrough, you must install the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="224b2-122">Eftirtaldar breytingar þarf að gera á grunninum:</span><span class="sxs-lookup"><span data-stu-id="224b2-122">The following modifications must be made to the database:</span></span>  

-   <span data-ttu-id="224b2-123">Eyða öllum sölupöntunum vegna reiðhjóla.</span><span class="sxs-lookup"><span data-stu-id="224b2-123">Delete all existing sales orders for bicycles.</span></span>  
-   <span data-ttu-id="224b2-124">Stofna eina sölupöntun fyrir 10 reiðhjól hjá staðsetningunni BLÁTT.</span><span class="sxs-lookup"><span data-stu-id="224b2-124">Create one sales order for 10 bicycles at BLUE location.</span></span>  
-   <span data-ttu-id="224b2-125">Eyða öllum áætluðum og fastáætluðum framleiðsluáætlunum.</span><span class="sxs-lookup"><span data-stu-id="224b2-125">Delete all planned and firm planned production orders.</span></span> <span data-ttu-id="224b2-126">Ekki eyða pöntunum sem þegar eru í gangi með færslum sem þegar eru skráðar.</span><span class="sxs-lookup"><span data-stu-id="224b2-126">Do not delete started orders with entries that are already posted.</span></span>  

 <span data-ttu-id="224b2-127">Regla er að nota gögnin sem lagt er til í þessari kynningu vegna þess að þau gögn hafa nauðsynlegar skrár.</span><span class="sxs-lookup"><span data-stu-id="224b2-127">As a rule, use the suggested data in this walkthrough because this data has the necessary records.</span></span>  

## <a name="story"></a><span data-ttu-id="224b2-128">Ferill</span><span class="sxs-lookup"><span data-stu-id="224b2-128">Story</span></span>  
 <span data-ttu-id="224b2-129">Erla, sem er framleiðslustjóri lítils framleiðslufyrirtækis, er um það bil að fara að áætla framleiðslu og innkaupapantanir til að uppfylla nýja eftirspurn í sölu.</span><span class="sxs-lookup"><span data-stu-id="224b2-129">Eduardo, the Production Planner of a small manufacturing company, is about to plan production and purchase orders to fulfill new sales demand.</span></span>  

 <span data-ttu-id="224b2-130">Vegna þess að framleiðslan hefur fá stig framleiðsluuppskrifta og flæði pantana er tiltölulega hæggengt notar Erla síðuna **Pantanaáætlun** til að stofna framboðspantanir handvirkt, eitt framleiðsluskref í einu.</span><span class="sxs-lookup"><span data-stu-id="224b2-130">Because the products have few BOM levels and the flow of orders is relatively low, Eduardo uses the **Order Planning** page to manually create supply orders, one product level at a time.</span></span>  

 <span data-ttu-id="224b2-131">Í flóknara framleiðsluumhverfi er vinnublaðið fyrir áætlun notað til að gera áætlun um framboð sem byggir á vöruþáttum eins og enduráætlunartímabil, öryggisforskot, endurpöntunarmark og keyrslu útreikninga eftirspurnar allra framleiðslustiga sem steypt hefur verið saman.</span><span class="sxs-lookup"><span data-stu-id="224b2-131">In a more complex manufacturing environment, the planning worksheet is used to plan supply based on item parameters such as rescheduling period, safety lead time, reorder point, and batch calculations of consolidated demand from all product levels.</span></span>  

## <a name="setting-up-the-sample-data"></a><span data-ttu-id="224b2-132">Uppsetning sýnigagna</span><span class="sxs-lookup"><span data-stu-id="224b2-132">Setting Up the Sample Data</span></span>  
 <span data-ttu-id="224b2-133">Staðlaða CRONUS sýnifyrirtækið er eins og stendur með mikið af óáætlaðri eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="224b2-133">The standard CRONUS demonstration company currently has lots of unplanned demand.</span></span> <span data-ttu-id="224b2-134">Í ólíkum verkefnum áætlana sem eru í þessari kynningu verður að víkja frá raunverulegu viðskiptaflæði með því að hundsa kröfur sem hafa gjalddaga sem stutt er í og nota þess í stað kröfur með gjalddaga sem er síðar.</span><span class="sxs-lookup"><span data-stu-id="224b2-134">During the different planning tasks in this walkthrough, you will have to deviate from the realistic business flow by ignoring demand with close due dates and instead use demand with later due dates.</span></span>  

## <a name="using-the-order-planning-page"></a><span data-ttu-id="224b2-135">Síðan Pantanaáætlun notuð</span><span class="sxs-lookup"><span data-stu-id="224b2-135">Using the Order Planning Page</span></span>  

<!--
The **Order Planning** page can be accessed from several different locations on the **Departments** menu in the navigation pane:  

-   Manufacturing, Planning  
-   Sales & Marketing, Order Processing  
-   Purchase, Planning  
-   In addition, you can open this page for a specific production order by choosing **Planning** on the **Navigate** tab in the **Order** group.

-->  

### <a name="to-use-the-order-planning-page"></a><span data-ttu-id="224b2-136">Að nota síðuna „Pantanaáætlun“</span><span class="sxs-lookup"><span data-stu-id="224b2-136">To use the Order Planning page</span></span>  

1.  <span data-ttu-id="224b2-137">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **pantanaáætlun** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="224b2-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Order Planning**, and then choose the related link.</span></span>  

     <span data-ttu-id="224b2-138">Eftir að síðan **Pantanaáætlun** opnast fyrst þarf að reikna áætlun til að sýna nýja eftirspurn frá því hún var reiknuð síðast.</span><span class="sxs-lookup"><span data-stu-id="224b2-138">When the **Order Planning** page first opens, a plan must be calculated to show the new demand since it was last calculated.</span></span>  

2.  <span data-ttu-id="224b2-139">Velja **Reikna áætlun** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="224b2-139">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="224b2-140">Áætlunarkerfið greinir hverja nýja eftirspurn sem hefur komið fram, svo sem nýja sölu eða framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="224b2-140">The planning system analyzes any new demand that has been introduced, such as new sales, changed sales, or production orders.</span></span>  

     <span data-ttu-id="224b2-141">Magnið sem þörf er á fyrir hverja eftirspurnarlínu er reiknað út og byggir á heildarmagni sem til ráðstöfunar er.</span><span class="sxs-lookup"><span data-stu-id="224b2-141">Based on total availability, the quantity needed for each demand line is calculated.</span></span> <span data-ttu-id="224b2-142">Útreikningurinn er gerður fyrir hverja pöntun fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="224b2-142">This calculation is performed order-by-order.</span></span> <span data-ttu-id="224b2-143">Það þýðir að pöntunin sem inniheldur eftirspurnarlínuna með fyrstu skila-/afhendingardagsetninguna er tekin fyrir fyrst.</span><span class="sxs-lookup"><span data-stu-id="224b2-143">This means that the order which includes the demand line with the earliest due date or shipment date will be calculated first.</span></span> <span data-ttu-id="224b2-144">Eftir það eru allar aðrar eftirspurnarlínur reiknaðar í sömu röð, óháð skila- eða afhendingardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="224b2-144">After that, additional demand lines will be calculated in the same order, regardless of the due date or shipment date.</span></span>  

3.  <span data-ttu-id="224b2-145">Ganga þarf úr skugga um að síðan **Pantanaáætlun** sé stækkuð og að reitir dálka séu af þeirri stærð að þeir sýni öll sjálfgefin heiti reita.</span><span class="sxs-lookup"><span data-stu-id="224b2-145">Be sure that the **Order Planning** page is maximized and that column fields are resized to show all the default field names.</span></span>  

     <span data-ttu-id="224b2-146">Þegar útreikningi er lokið þá sýnir síðan alla óuppfyllta eftirspurn sem línur pöntunarhauss sem hafa verið felldar saman, flokkað eftir nýjustu dagsetningu eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="224b2-146">When the calculation is completed, the page displays all unfulfilled demand as collapsed order header lines sorted by earliest demand date.</span></span>  

     <span data-ttu-id="224b2-147">Takið eftir að CRONUS hefur margar pantanir með óuppfyllta eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="224b2-147">Notice that CRONUS has several orders with unfulfilled demand.</span></span> <span data-ttu-id="224b2-148">Hver feitletruð áætlunarlína stendur fyrir pöntun, sölupöntun eða framleiðslupöntun; af þeim er að minnsta kosti ein pantanalína með sem uppfyllir ekki ráðstöfunarkröfur.</span><span class="sxs-lookup"><span data-stu-id="224b2-148">Each bold planning line represents an order, sales order, or production order, including at least one order line with insufficient availability.</span></span>  

4.  <span data-ttu-id="224b2-149">Í reitnum **Sýna eftirspurn sem** skal velja afmörkunina **Alla eftirspurn**.</span><span class="sxs-lookup"><span data-stu-id="224b2-149">In the **Show Demand As** field, select the **All Demand** filter.</span></span>  

     <span data-ttu-id="224b2-150">Innan reitsins **Tegund eftirspurnar** má velja hvaða tegundir pantana á að birta.</span><span class="sxs-lookup"><span data-stu-id="224b2-150">With the **Demand Type** field, you can choose which order types that you want to display.</span></span>  

     <span data-ttu-id="224b2-151">Pantanir sem ekki eru vandamál varðandi tiltækt magn eru ekki sýndar.</span><span class="sxs-lookup"><span data-stu-id="224b2-151">Orders that do not have availability problems are not shown.</span></span> <span data-ttu-id="224b2-152">Ef engar pantanir eru til staðar þegar áætlun er reiknuð birtast skilaboð og engar áætlunarlínur birtast.</span><span class="sxs-lookup"><span data-stu-id="224b2-152">If no orders exist when a plan is calculated, a message will display and no planning lines will appear.</span></span>  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a><span data-ttu-id="224b2-153">Innkaupapöntun áætluð til að uppfylla eftirspurn íhluta</span><span class="sxs-lookup"><span data-stu-id="224b2-153">Planning a Purchase Order to Fulfill Component Demand</span></span>  
 <span data-ttu-id="224b2-154">Í þessu ferli er stofnuð innkaupapöntun fyrir íhluti sem þarf til framleiðslunnar.</span><span class="sxs-lookup"><span data-stu-id="224b2-154">In this procedure, you create a purchase order for needed manufacturing components.</span></span>  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><span data-ttu-id="224b2-155">Til að áætla innkaupapöntun til að uppfylla þörf á íhlutum fyrir framleiðslu</span><span class="sxs-lookup"><span data-stu-id="224b2-155">To plan a purchase order to fulfill component need in production</span></span>  

1.  <span data-ttu-id="224b2-156">Fyrsta línan er stækkuð (veljið táknið +).</span><span class="sxs-lookup"><span data-stu-id="224b2-156">Expand the first line (choose the + symbol).</span></span>  
2.  <span data-ttu-id="224b2-157">Veljið fyrstu eftirspurnarlínuna, með vöru **LSU-15** og síðan **Sýna fylgiskjal** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="224b2-157">Choose the first demand line, with item **LSU-15**, and then choose the **Show Document** action.</span></span>  
3.  <span data-ttu-id="224b2-158">Opinni framleiðslupöntun er lokað til að fara aftur á síðuna **Pantanaáætlun**.</span><span class="sxs-lookup"><span data-stu-id="224b2-158">Close the opened production order to return to the **Order Planning** page.</span></span>  
4.  <span data-ttu-id="224b2-159">Í reitnum **Áfyllingarkerfið** eru **Innkaup** valin.</span><span class="sxs-lookup"><span data-stu-id="224b2-159">In the **Replenishment System** field, select **Purchase**.</span></span>  

     <span data-ttu-id="224b2-160">Sjálfgefna gildið er af birgðaspjaldinu eða birgðahaldseiningaspjaldinu, en því er hægt að breyta í einn af eftirtöldum valkostum:</span><span class="sxs-lookup"><span data-stu-id="224b2-160">The default value is from the item card, or SKU card, but you can change it to one of the following options:</span></span>  

    -   <span data-ttu-id="224b2-161">**Innkaup** – Til að búa til innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="224b2-161">**Purchase** – To create a purchase order.</span></span>  
    -   <span data-ttu-id="224b2-162">**Millifærsla** – til að búa til millifærslupöntun.</span><span class="sxs-lookup"><span data-stu-id="224b2-162">**Transfer** – To create a transfer order.</span></span>  
    -   <span data-ttu-id="224b2-163">**Framl.pöntun** – Til að búa til framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="224b2-163">**Prod. Order** – To create a production order.</span></span>  

5.  <span data-ttu-id="224b2-164">Í reitnum **Framboð frá** þarf að velja eitt af eftirfarandi valmöguleikum til hliðsjónar við valið áfyllingarkerfi:</span><span class="sxs-lookup"><span data-stu-id="224b2-164">In the **Supply From** field, select one of the following options according to the selected replenishment system:</span></span>  

    -   <span data-ttu-id="224b2-165">**Lánardrottinn** – Fyrir innkaup</span><span class="sxs-lookup"><span data-stu-id="224b2-165">**Vendor** – For purchases</span></span>  
    -   <span data-ttu-id="224b2-166">**Birgðageymsla** – fyrir flutning</span><span class="sxs-lookup"><span data-stu-id="224b2-166">**Location** – For transfers</span></span>  

     <span data-ttu-id="224b2-167">Ef reiturinn er ekki fylltur út þá koma fram villuboð þegar reynt er að stofna framboðspöntun.</span><span class="sxs-lookup"><span data-stu-id="224b2-167">If the field is not filled in, an error message will display when you try to create the supply orders.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="224b2-168">Hafi íhlutirnir uppsett sjálfgefin númer lánadrottna á birgðaspjaldi, þá verða línurnar endurstilltar.</span><span class="sxs-lookup"><span data-stu-id="224b2-168">If the components have a default vendor number set up on the item cards, the lines will be preset.</span></span>  

6.  <span data-ttu-id="224b2-169">Velja reitinn **Framboð frá**.</span><span class="sxs-lookup"><span data-stu-id="224b2-169">Choose the **Supply From**  field.</span></span>  
7.  <span data-ttu-id="224b2-170">Á síðunni **Vörulisti lánardrottins** skal velja aðgerðina **Nýtt** og svo er lánadrottinn **30000** valinn.</span><span class="sxs-lookup"><span data-stu-id="224b2-170">On the **Item Vendor Catalogue** page, choose the **New** action, and then select vendor **30000**.</span></span>  
8.  <span data-ttu-id="224b2-171">Velja hnappinn **Í lagi** til að fara aftur á síðuna **Pantanaáætlun**.</span><span class="sxs-lookup"><span data-stu-id="224b2-171">Choose the **OK** button to return to the **Order Planning** page.</span></span>  
9. <span data-ttu-id="224b2-172">Afrita lánardrottinn **30000** í aðrar línur fyrir hátalaraíhlutina á þessari framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="224b2-172">Copy vendor **30000** to the other lines for loudspeaker components on this production order.</span></span>  

     <span data-ttu-id="224b2-173">Nú er hægt að stofna innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="224b2-173">You are now ready to create a purchase order.</span></span>  

10. <span data-ttu-id="224b2-174">Velja **búa til Pantanir** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="224b2-174">Choose the **Make Orders** action.</span></span> <span data-ttu-id="224b2-175">Síðan **Gera framboðspantanir** opnast.</span><span class="sxs-lookup"><span data-stu-id="224b2-175">The **Make Supply Orders** page opens.</span></span>  
11. <span data-ttu-id="224b2-176">Í  **Pantanaáætlun** á flýtiflipanum **Gera pantanir fyrir** skal velja kostinn **Virk pöntun**.</span><span class="sxs-lookup"><span data-stu-id="224b2-176">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **Active Order** option.</span></span>  
12. <span data-ttu-id="224b2-177">Á flýtiflipanum **Valkostir** í reitnum **Stofna innkaupapöntun** er kosturinn **Gera innkaupapantanir** valinn.</span><span class="sxs-lookup"><span data-stu-id="224b2-177">On the **Options** FastTab, in the **Create Purchase Order** field, choose the **Make Purch. Order** option.</span></span>  
13. <span data-ttu-id="224b2-178">Veldu hnappinn **Í lagi** til að stofna innkaupapantanir fyrir alla íhluti pöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="224b2-178">Choose the **OK** button to create purchase orders for all the components of the order.</span></span>  

     <span data-ttu-id="224b2-179">Innkaupapantanirnar hafa nú verið stofnaðar og vistaðar sem síðustu pantanir í listanum yfir innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="224b2-179">The purchase orders are now created and saved as the last orders in the list of purchase orders.</span></span>  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="224b2-180">Millifærslupöntun áætluð til að uppfylla eftirspurn sölu</span><span class="sxs-lookup"><span data-stu-id="224b2-180">Planning a Transfer Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="224b2-181">Í þessu ferli er eftirspurn áætluð út frá sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="224b2-181">In this procedure, you will plan for demand from a sales order.</span></span> <span data-ttu-id="224b2-182">Eftirspurnarlínur gefa sölulínur til kynna en ekki íhlutalínur eins og í framleiðslueftirspurn.</span><span class="sxs-lookup"><span data-stu-id="224b2-182">Demand lines represent sales lines and not component lines, as in production demand.</span></span>  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="224b2-183">Áætlun um millifærslupöntun til að uppfylla eftirspurn sölu</span><span class="sxs-lookup"><span data-stu-id="224b2-183">To plan a transfer order to fulfill sales demand</span></span>  

1.  <span data-ttu-id="224b2-184">Bendillinn er færður á áætlunarlínu fyrir pöntun **2008**.</span><span class="sxs-lookup"><span data-stu-id="224b2-184">Move the pointer to the planning line for order **2008**.</span></span>  
2.  <span data-ttu-id="224b2-185">Stækka skal línuna og færa bendilinn á eftirspurnarlínu.</span><span class="sxs-lookup"><span data-stu-id="224b2-185">Expand the line and move the pointer to the demand line.</span></span>  

     <span data-ttu-id="224b2-186">Sölupöntun **2008** er fyrir tíu hátalara af vöru **LS-120**, pantað af John Haddock Insurance Co.</span><span class="sxs-lookup"><span data-stu-id="224b2-186">Sales order **2008** is for ten loudspeakers, item **LS-120**, ordered by John Haddock Insurance Co.</span></span>  

     <span data-ttu-id="224b2-187">Þá birtist skilgreint áfyllingarkerfi vörunnar og sjálfgefinn lánadrottinn.</span><span class="sxs-lookup"><span data-stu-id="224b2-187">The item’s defined replenishment system and default vendor will display.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="224b2-188">Neðst á síðunni eru fjórir upplýsingareitir.</span><span class="sxs-lookup"><span data-stu-id="224b2-188">At the bottom of the page, there are four information fields.</span></span> <span data-ttu-id="224b2-189">Í reitnum **Fyrsta tiltæka dagsetning** munu þeir tíu hlutir sem þörf er á vera til taks, fyrir framboðspöntun á innleið, níu dögum eftir núverandi lokadag.</span><span class="sxs-lookup"><span data-stu-id="224b2-189">In the **Earliest Date Available** field, the ten pieces that are needed will be available, on an inbound supply order, nine days later than the current due date.</span></span> <span data-ttu-id="224b2-190">Ef þetta er of seint fyrir viðskiptamanninn þá sýnir reiturinn **Tiltækt fyrir millifærslu** 13 stykki vörunnar á annarri staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="224b2-190">If this is too late for the customer, the **Available for Transfer** field shows 13 pieces of the item at another location.</span></span> <span data-ttu-id="224b2-191">Áætla þarf fyrir þessar birgðir.</span><span class="sxs-lookup"><span data-stu-id="224b2-191">You will want to plan for this stock.</span></span>  

3.  <span data-ttu-id="224b2-192">Smellt er á **Tiltækt fyrir millifærslu** til að opna síðuna **Sækja annað framboð**.</span><span class="sxs-lookup"><span data-stu-id="224b2-192">Choose the **Available for Transfer** field to open the **Get Alternative Supply** page.</span></span>  
4.  <span data-ttu-id="224b2-193">Veldu hnappinn **Í lagi** til að bóka þau tíu eintök sem eru tiltæk.</span><span class="sxs-lookup"><span data-stu-id="224b2-193">Choose the **OK** button to book the ten items that are available.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="224b2-194">Í eftirspurnarlínuna hefur innkaupatillögu verið skipt út fyrir flutning frá GRÆNNI birgðageymslu.</span><span class="sxs-lookup"><span data-stu-id="224b2-194">In the demand line, the suggested purchase has been exchanged with a transfer from GREEN location.</span></span> <span data-ttu-id="224b2-195">Aðgerðin **Búa til pöntun** stofnar flutning frá GRÆNNI til staðar þaðan sem eftirspurnin kemur.</span><span class="sxs-lookup"><span data-stu-id="224b2-195">The **Make Orders** function creates a transfer order from GREEN to the demanded location.</span></span> <span data-ttu-id="224b2-196">Reiturinn **Staðgenglar eru til** virkar á sama hátt.</span><span class="sxs-lookup"><span data-stu-id="224b2-196">The **Substitutes Exists** field works in the same way.</span></span>  

5.  <span data-ttu-id="224b2-197">Velja **búa til Pantanir** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="224b2-197">Choose the **Make Orders** action.</span></span> <span data-ttu-id="224b2-198">Síðan **Gera framboðspantanir** opnast.</span><span class="sxs-lookup"><span data-stu-id="224b2-198">The **Make Supply Orders** page opens.</span></span>  
6.  <span data-ttu-id="224b2-199">Í  **Pantanaáætlun** á flýtiflipanum **Gera pantanir fyrir** skal velja kostinn **Virka pöntunin**.</span><span class="sxs-lookup"><span data-stu-id="224b2-199">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **The Active Order** option.</span></span>  
7.  <span data-ttu-id="224b2-200">Á flýtiflipanum **Valkostir** í reitnum **Stofna millifærslupöntun** skal velja kostinn **Gera millif.pantanir**.</span><span class="sxs-lookup"><span data-stu-id="224b2-200">On the **Options** FastTab, in the **Create Transfer Order** field, select the **Make Trans. Orders** option.</span></span>  
8.  <span data-ttu-id="224b2-201">Veldu hnappinn **Í lagi** til að stofna millifærslupöntun til að anna sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="224b2-201">Choose the **OK** button to create the transfer order to supply the sales order.</span></span>  

     <span data-ttu-id="224b2-202">Millifærslupöntun hefur nú verið gerð og vistuð í listanum sem síðasta pöntun í listanum yfir opnar millifærslupantanir.</span><span class="sxs-lookup"><span data-stu-id="224b2-202">The transfer order is now created and saved in the list as the last order in the list of open transfer orders.</span></span>  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><span data-ttu-id="224b2-203">Margþrepa millifærslupöntun áætluð til að uppfylla eftirspurn sölu</span><span class="sxs-lookup"><span data-stu-id="224b2-203">Planning a Multilevel Production Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="224b2-204">Í þessu ferli er gerð áætlun til að uppfylla eftirspurn sölu fyrir framleiðslu sem hefur mörg framleiðsluþrep þar sem hvert og eitt myndar háða eftirspurn framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="224b2-204">In this procedure, you will plan to fulfill sales demand for a produced item with multiple product levels, each creating dependent production demand.</span></span>  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><span data-ttu-id="224b2-205">Að áætla margra þrepa framleiðslu til að uppfylla eftirspurn sölu</span><span class="sxs-lookup"><span data-stu-id="224b2-205">To plan multilevel production to fulfill sales demand</span></span>  

1.  <span data-ttu-id="224b2-206">Áætlunarlína með pöntun fyrir eftirspurn sölu **1001** er valin (stofnuð áður sem frumskilyrði).</span><span class="sxs-lookup"><span data-stu-id="224b2-206">Select the planning line with sales demand for order **1001**, created earlier as prerequisite data.</span></span>  

     <span data-ttu-id="224b2-207">Þessi eftirspurn er sölulína en varan hefur skilgreint áfyllingarkerfi sem er **Framl.pöntun**.</span><span class="sxs-lookup"><span data-stu-id="224b2-207">This demand is a sales line, but the item has a defined replenishment system of **Prod. Order**.</span></span> <span data-ttu-id="224b2-208">Haldið er áfram til að bæta annarri bjöllu við íhlutaþörf hvers hjóls.</span><span class="sxs-lookup"><span data-stu-id="224b2-208">Proceed to add an extra bell to the component need of each bicycle.</span></span>  

2.  <span data-ttu-id="224b2-209">Veldu **Íhlutir** aðgerðina til að opna síðuna **Áætla Íhlutir** .</span><span class="sxs-lookup"><span data-stu-id="224b2-209">Choose the **Components** action to open the **Planning Components** page.</span></span>  
3.  <span data-ttu-id="224b2-210">Í línunni með bjölluvörunni skal breyta reitnum **Magn á** úr **1** í **2**.</span><span class="sxs-lookup"><span data-stu-id="224b2-210">On the line with the Bell item, change the **Quantity per** field from **1** to **2**.</span></span>  
4.  <span data-ttu-id="224b2-211">Á síðunni **Pantanaáætlun** þarf að meta möguleika fyrir pöntunina.</span><span class="sxs-lookup"><span data-stu-id="224b2-211">On the **Order Planning** page, consider your planning alternatives.</span></span> <span data-ttu-id="224b2-212">Í þessu tilfelli eru engar aðrar leiðir til framboðs, engir staðgenglar, millifærslur, eða síðari afhending.</span><span class="sxs-lookup"><span data-stu-id="224b2-212">In this case, you have no alternative means of supply, no transfer, substitute, or later delivery.</span></span> <span data-ttu-id="224b2-213">Stofna þarf birgðapöntunina sem lögð er til, framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="224b2-213">You must create the suggested supply order, a production order.</span></span>  
5.  <span data-ttu-id="224b2-214">Velja **búa til Pantanir** aðgerð til að stofna framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="224b2-214">Choose the **Make Orders** action to create the production order.</span></span>  

     <span data-ttu-id="224b2-215">Á síðunni **Pantanaáætlun** sést að áætlunarlínan fyrir sölupöntun **1001** er ekki lengur til staðar og séð hefur verið um upphaflega eftirspurn sölu.</span><span class="sxs-lookup"><span data-stu-id="224b2-215">On the **Order Planning** page, notice that the planning line for sales order **1001** no longer exists and that the initial sales demand has been covered.</span></span>  

6.  <span data-ttu-id="224b2-216">Glugganum **Pantanaáætlun** er lokað.</span><span class="sxs-lookup"><span data-stu-id="224b2-216">Close the **Order Planning** page.</span></span>  

     <span data-ttu-id="224b2-217">Nú væri hægt að velja að halda áfram í þessari valmynd og ljúka öllum áætlanagerðum.</span><span class="sxs-lookup"><span data-stu-id="224b2-217">Now, you could choose to stay in this view and complete all the planning tasks.</span></span> <span data-ttu-id="224b2-218">Þess í stað er nú farið í hlutverk framleiðslustjóra með því að fara í framleiðslupöntunina sem verið var að gera og opna síðuna **Pantanaáætlun**.</span><span class="sxs-lookup"><span data-stu-id="224b2-218">Instead, you will now take on the Production Planner role by going to the production order that you just created and access the **Order Planning** page.</span></span>  

 <span data-ttu-id="224b2-219">Framleiðslustjóri þarf að áætla sérstaka röð framleiðslupantana.</span><span class="sxs-lookup"><span data-stu-id="224b2-219">As a production planner you now must plan a specific production order.</span></span>  

### <a name="to-plan-a-specific-production-order"></a><span data-ttu-id="224b2-220">Til að áætla sérstaka röð framleiðslupöntunar</span><span class="sxs-lookup"><span data-stu-id="224b2-220">To plan a specific production order</span></span>  

1.  <span data-ttu-id="224b2-221">Opna skal framleiðslupöntunina **101001**, fyrir tíu reiðhjól, sem var stofnuð með aðgerðinni **Gera pantanir**.</span><span class="sxs-lookup"><span data-stu-id="224b2-221">Open the production order **101001**, for ten bicycles, that you just created by using the **Make Orders** function.</span></span>  
2.  <span data-ttu-id="224b2-222">Opna síðuna **Íhlutir framl.pöntunar** til að athuga hvort staka bjallan endurspeglist í framleiðslupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="224b2-222">Open the **Prod. Order Components** page to check that the extra bell is reflected on the production order.</span></span>  
3.  <span data-ttu-id="224b2-223">Veldu aðgerðina **Áætlun**.</span><span class="sxs-lookup"><span data-stu-id="224b2-223">Choose the **Planning** action.</span></span>  

     <span data-ttu-id="224b2-224">Síðan **Pantanaáætlun** opnast í útliti sem er alltaf síað niður á tiltekna framleiðslueftirspurn.</span><span class="sxs-lookup"><span data-stu-id="224b2-224">The **Order Planning** page opens in a view that is always filtered on the specific production demand.</span></span> <span data-ttu-id="224b2-225">Eftirspurn sölu er ekki sýnd.</span><span class="sxs-lookup"><span data-stu-id="224b2-225">Sales demand is not displayed.</span></span> <span data-ttu-id="224b2-226">Reikna þarf áætlun áður en hægt er að sjá nokkra viðbótareftirspurn.</span><span class="sxs-lookup"><span data-stu-id="224b2-226">You must calculate a plan before you can see any additional demand.</span></span>  

4.  <span data-ttu-id="224b2-227">Velja **Reikna áætlun** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="224b2-227">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="224b2-228">Takið eftir að fjórar nýjar framleiðslupantanir koma fram sem óáætluð eftirspurn framleiðslu sem dregin er af pöntun **101001**.</span><span class="sxs-lookup"><span data-stu-id="224b2-228">Notice that four new production orders appear as unplanned production demand derived from order **101001**.</span></span> <span data-ttu-id="224b2-229">Nýju línurnar standa fyrir nýja eftirspurn framleiðslu frá millivörum sem þarf að stofna til að framleiða pöntunina.</span><span class="sxs-lookup"><span data-stu-id="224b2-229">The new lines represent new production demand from the subassemblies that must be created to produce the order.</span></span>  

5.  <span data-ttu-id="224b2-230">Veldu aðgerðina **Stækka allt** til að fá yfirlit yfir alla framleiðslueftirspurnina fyrir framleiðslupantanirnar.</span><span class="sxs-lookup"><span data-stu-id="224b2-230">Choose the **Expand All** action to get an overview of all the production demand for the production orders.</span></span>  

     <span data-ttu-id="224b2-231">Til að leggja fram viðbótarupplýsingar um eftirspurnarlínur gæti verið ráðlegt að bæta reitunum **Magn eftirspurnar** og **Tiltækt magn eftirspurnar** í gluggann.</span><span class="sxs-lookup"><span data-stu-id="224b2-231">To provide additional information about the demand lines, you may want to add the **Demand Quantity** and **Demand Qty. Available** fields to your view.</span></span>  

     <span data-ttu-id="224b2-232">Nú þarf að bjóða fram tíu stykki af hverjum íhlut.</span><span class="sxs-lookup"><span data-stu-id="224b2-232">Now you must supply ten of each component.</span></span>  

     <span data-ttu-id="224b2-233">Athugið að fjórar af eftirspurnarlínunum hafa framleiðslupantanir áfyllingarkerfis.</span><span class="sxs-lookup"><span data-stu-id="224b2-233">Note that four of the demand lines have replenishment system Prod. Order.</span></span> <span data-ttu-id="224b2-234">Þessir fjórir samsetningarhlutar eru annað framleiðslustig reiðhjólsins.</span><span class="sxs-lookup"><span data-stu-id="224b2-234">These four subassemblies represent the second product level of the bicycle.</span></span>  

     <span data-ttu-id="224b2-235">Sjálfgefnar stillingar áfyllingar eru þegar útfylltar og halda má áfram til að gera pantanir.</span><span class="sxs-lookup"><span data-stu-id="224b2-235">The default replenishment settings are already filled in and you can proceed to make orders.</span></span>  

6.  <span data-ttu-id="224b2-236">Velja **búa til Pantanir** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="224b2-236">Choose the **Make Orders** action.</span></span>  

     <span data-ttu-id="224b2-237">Áður er hnappurinn **Í lagi** er valinn ætti að lesa textann á flýtiflipanum **Pantanaáætlun**.</span><span class="sxs-lookup"><span data-stu-id="224b2-237">Before you choose the **OK** button, notice the text on the **Order Planning** FastTab.</span></span> <span data-ttu-id="224b2-238">Þessi texti er mikilvægur vegna þess að vitað er að reiðhjólið hefur nokkra framleidda íhluti—millivörur—í framleiðsluferli sínu sem gæti orðið eftirspurn eftir þegar þessi framleiðslupöntun hefur verið gerð.</span><span class="sxs-lookup"><span data-stu-id="224b2-238">This text is important because you know that the bicycle has several produced components, subassemblies, in its product structure that might be in demand when you create this production order.</span></span>  

7.  <span data-ttu-id="224b2-239">Á síðunni **Gera framboðspantanir** í reitnum **Gera pantanir fyrir** veljið valkostinn **Allar línur** og veljið svo hnappinn **Í lagi** til að stofna framleiðslupöntun fyrir annað framleiðslustig pöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="224b2-239">On the **Make Supply Order** page, in the **Make Orders for** field, choose the **All Lines** option, and then choose the **OK** button to create production orders for the second product level of the order.</span></span>  

     <span data-ttu-id="224b2-240">Athugið að eftirspurn framleiðslu á efsta stigi fyrir framleiðslupöntun 101001 er ekki lengur til.</span><span class="sxs-lookup"><span data-stu-id="224b2-240">Note that the top-level production demand for production order 101001 no longer exists.</span></span> <span data-ttu-id="224b2-241">Það þýðir að gerð hefur verið áætlun fyrir upphaflega eftirspurn framleiðslu fyrir millivörur.</span><span class="sxs-lookup"><span data-stu-id="224b2-241">This means that the initial production demand for subassemblies has been planned for.</span></span>  

     <span data-ttu-id="224b2-242">Á síðunni **Pantanaáætlun** má reikna áætlun aftur til að gera áætlun um byggingu reiðhjólsins.</span><span class="sxs-lookup"><span data-stu-id="224b2-242">On the **Order Planning** page, you calculate a plan again in order to plan the bicycle structure.</span></span>  

8.  <span data-ttu-id="224b2-243">Velja aðgerðina **Reikna áætlun** til að endurreikna áætlun eins og mælt er fyrir um í meðfylgjandi Hjálpartexta.</span><span class="sxs-lookup"><span data-stu-id="224b2-243">Choose the **Calculate Plan** action to recalculate the plan as instructed by the embedded Help text.</span></span>  

     <span data-ttu-id="224b2-244">Nýju línurnar tvær standa fyrir viðbótareftirspurn framleiðslu sem tengist millivörunum sem áætlun var gerð um í fyrri þrepum.</span><span class="sxs-lookup"><span data-stu-id="224b2-244">The two new lines represent additional production demand derived from the subassemblies planned in the previous steps.</span></span> <span data-ttu-id="224b2-245">Lagt er til að tvær framleiðslupantanir séu gerðar fyrir framboð á hjólnöfunum, ein fyrir 10 framnafir og ein fyrir 10 afturnafir.</span><span class="sxs-lookup"><span data-stu-id="224b2-245">It is suggested that you make two production orders to supply the wheel hubs, one for 10 front hubs and one for 10 back hubs.</span></span>  

9. <span data-ttu-id="224b2-246">Veldu aðgerðina **Stækka allt** til að fá yfirlit yfir alla framleiðslueftirspurnina fyrir þessar tvær framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="224b2-246">Choose the **Expand All** action to get an overview of all the demand for the two production orders.</span></span>  

     <span data-ttu-id="224b2-247">Tillagan um framboðið gefur til kynna að fjórar innkaupapantanir verði gerðar vegna íhlutanna.</span><span class="sxs-lookup"><span data-stu-id="224b2-247">The suggested supply plan indicates that a total of four purchase orders will be created for the components.</span></span> <span data-ttu-id="224b2-248">Ákveðið er að gera pantanirnar sem lagt er til.</span><span class="sxs-lookup"><span data-stu-id="224b2-248">You decide to make the proposed orders.</span></span>  

10. <span data-ttu-id="224b2-249">Velja **búa til Pantanir** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="224b2-249">Choose the **Make Orders** action.</span></span>  
11. <span data-ttu-id="224b2-250">Í reitnum **Gera pantanir fyrir** veljið valkostinn **Allar línur** og veljið svo hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="224b2-250">In the **Make Orders for** field, select the **All Lines** option, and then choose the **OK** button.</span></span> <span data-ttu-id="224b2-251">Athuga þarf hvort viðbótareftirspurn er til staðar vegna framleiðslu yfirvörunnar, reiðhjólsins (sem selt er samkvæmt sölupöntun 1001).</span><span class="sxs-lookup"><span data-stu-id="224b2-251">Check if additional demand exists for the production of the parent item, the bicycle, which is being sold on sales order 1001.</span></span>  
12. <span data-ttu-id="224b2-252">Velja **Reikna áætlun** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="224b2-252">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="224b2-253">Skilaboðin segja til um að allir tilskildir hlutir séu nú til staðar (að til sé framboð af þeim).</span><span class="sxs-lookup"><span data-stu-id="224b2-253">The message indicates that all required items are now supplied.</span></span> <span data-ttu-id="224b2-254">Staðfesta fastáætlaðar framleiðslupantanir sem eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="224b2-254">Verify the firm planned production orders that are created.</span></span>  

13. <span data-ttu-id="224b2-255">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fastáætluð framl.pantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="224b2-255">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  

     <span data-ttu-id="224b2-256">Á síðunni **Fastáætlað** farið yfir hvernig upphafs- og lokatími einstakra pantana er áætlaður út frá samsetningu framleiðslunnar.</span><span class="sxs-lookup"><span data-stu-id="224b2-256">On the **Firm Planned Prod. Orders** page review how start times and end times of individual orders are scheduled according to the product structure.</span></span> <span data-ttu-id="224b2-257">Íhlutir á neðsta þrepi eru framleiddir fyrst.</span><span class="sxs-lookup"><span data-stu-id="224b2-257">The lowest-level components are produced first.</span></span> <span data-ttu-id="224b2-258">Því þarf að áætla pantanir í mörgum þrepum eins og sýnt er í þessu verkflæði fyrir áætlanir.</span><span class="sxs-lookup"><span data-stu-id="224b2-258">Therefore, you must plan multilevel orders as demonstrated in this planning workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="224b2-259">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="224b2-259">See Also</span></span>  
 <span data-ttu-id="224b2-260">[Kynningar á viðskiptaferlum](walkthrough-business-process-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="224b2-260">[Business Process Walkthroughs](walkthrough-business-process-walkthroughs.md) </span></span>  
 [<span data-ttu-id="224b2-261">Kynning: Sjálfvirk áætlun birgða</span><span class="sxs-lookup"><span data-stu-id="224b2-261">Walkthrough: Planning Supplies Automatically</span></span>](walkthrough-planning-supplies-automatically.md)
