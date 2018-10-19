---
title: "Hvernig á að búa til standandi sölupantanir | Microsoft Docs"
description: "Standandi pantanir eru notaðar þegar viðskiptamaður hefur samþykkt að kaupa í miklu magni sem afhenda á í nokkrum minni afhendingum á ákveðnu tímabili."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8e0668e39891f6e0924afd8d9ec3ee39af95e587
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="work-with-blanket-sales-orders"></a><span data-ttu-id="ed921-103">Vinna með standandi sölupantanir</span><span class="sxs-lookup"><span data-stu-id="ed921-103">Work with Blanket Sales Orders</span></span>
<span data-ttu-id="ed921-104">Standandi sölupöntun er rammi fyrir langtíma samning milli viðkomandi og viðskiptamanns.</span><span class="sxs-lookup"><span data-stu-id="ed921-104">A blanket sales order represents a framework for a long-term agreement between you and your customer.</span></span>

<span data-ttu-id="ed921-105">Standandi pöntun er yfirleitt stofnuð þegar viðskiptamaður hefur skuldbundið sig til kaupa á miklu magni sem afhenda á í nokkrum minni afhendingum á ákveðnu tímabili.</span><span class="sxs-lookup"><span data-stu-id="ed921-105">A blanket order is typically made when a customer has committed to purchasing large quantities that are to be delivered in several smaller shipments over a certain period of time.</span></span> <span data-ttu-id="ed921-106">Standandi pantanir ná oft eingöngu yfir eina vöru með fyrirframákveðnum afhendingardögum.</span><span class="sxs-lookup"><span data-stu-id="ed921-106">Often blanket orders cover only one item with predetermined delivery dates.</span></span> <span data-ttu-id="ed921-107">Aðalástæðan fyrir notkun standandi pantana í stað sölupantana er sú að magn sem tilgreint er á standandi pöntun hafa ekki áhrif á framboð vöru og hana er því hægt að nota sem blað fyrir eftirlit, spár eða áætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="ed921-107">The main reason for using a blanket order rather than a sales order is that quantities entered on a blanket order do not affect item availability and thus can be used as a worksheet for monitoring, forecasting, and planning purposes.</span></span>

<span data-ttu-id="ed921-108">Í standandi pöntun er hægt að setja hverja afhendingu upp sem pantanalínu sem hægt er að breyta í sölupöntun við afhendingu.</span><span class="sxs-lookup"><span data-stu-id="ed921-108">On the blanket order, each separate shipment can be set up as an order line, which can then be converted into a sales order at the time of shipping.</span></span>

<span data-ttu-id="ed921-109">Dæmi um hvenær standandi sölupöntun er hægt að nota er ef viðskiptamaður hefur samband og leggur inn pöntun upp á 1000 einingar af vörur og vill fá afhentar 250 einingar á viku næsta mánuðinn.</span><span class="sxs-lookup"><span data-stu-id="ed921-109">An example of when a blanket sales order could be used is if a customer calls and places an order of 1000 units of an item and they want the items to be delivered in 250 units every week over the next month.</span></span>

> [!NOTE]
> <span data-ttu-id="ed921-110">Standandi innkaupapöntun virka á svipaðan hátt og standandi sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="ed921-110">Blanket purchase orders work in a similar way as blanket sales orders.</span></span> <span data-ttu-id="ed921-111">Þetta fylgiskjal nær ekki yfir Standandi innkaupapantanir</span><span class="sxs-lookup"><span data-stu-id="ed921-111">This documentation does not cover blanket purchase orders.</span></span>

## <a name="to-create-a-blanket-sales-order"></a><span data-ttu-id="ed921-112">Til að búa til standandi sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="ed921-112">To create a blanket sales order</span></span>  
1. <span data-ttu-id="ed921-113">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Standandi sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="ed921-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Blanket Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ed921-114">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="ed921-114">Choose the **New** action.</span></span>  
3. <span data-ttu-id="ed921-115">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="ed921-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="ed921-116">Reiturinn **Pöntunardags.** er hafður auður.</span><span class="sxs-lookup"><span data-stu-id="ed921-116">Leave the **Order Date** field blank.</span></span> <span data-ttu-id="ed921-117">Þegar nokkrar sölupantanir eru stofnaðar úr standandi pöntun notar kerfið eiginlegu vinnudagsetninguna fyrir pöntunardagsetningu sölupöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="ed921-117">When the separate sales orders are created from the blanket order, the order date of the sales order is set to equal the actual work date.</span></span>
5. <span data-ttu-id="ed921-118">Á flýtiflipanum **Línur** skal stofna sérstaka línu fyrir hverja afhendingu.</span><span class="sxs-lookup"><span data-stu-id="ed921-118">On the **Lines** FastTab, create separate lines for each shipment.</span></span> <span data-ttu-id="ed921-119">Til dæmis ef viðskiptamaðurinn vill skipta 1000 einingum niður á fjórar vikur þarf að færa inn fjórar línur, hver upp á 250.</span><span class="sxs-lookup"><span data-stu-id="ed921-119">For instance, if your customer wants 1000 units split out equally between four weeks, you would enter four separate lines of 250 units each.</span></span>   

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a><span data-ttu-id="ed921-120">Stofnun sölupöntunar úr standandi sölupöntun</span><span class="sxs-lookup"><span data-stu-id="ed921-120">To create a sales order from a blanket sales order</span></span>  

1.  <span data-ttu-id="ed921-121">Til að stofna pöntun fyrir línurnar í standandi samsetningarpöntununum, er magnið fjarlægt úr reitnum **Magn til afhendingar** í öllum línum sem EKKI á að flytja á þessum tíma.</span><span class="sxs-lookup"><span data-stu-id="ed921-121">To create an order for any of the lines in the blanket assembly order, remove the quantity in the **Qty. to Ship** field on all the lines that you DO NOT wish to ship at this time.</span></span>  
2.  <span data-ttu-id="ed921-122">Þegar komið er að því að stofna pantanir skal velja aðgerðina **Búa til pöntun** og síðan velja **Já**.</span><span class="sxs-lookup"><span data-stu-id="ed921-122">When you are ready to create orders, choose the **Make Order**m action, and then choose **Yes**.</span></span> <span data-ttu-id="ed921-123">Skilaboð birtast um að standandi pöntunin hafi fengið pöntunarnúmer.</span><span class="sxs-lookup"><span data-stu-id="ed921-123">A message appears informing you that the blanket order has been assigned an order number.</span></span> <span data-ttu-id="ed921-124">Takið eftir að standandi pöntuninni hefur ekki verið eytt.</span><span class="sxs-lookup"><span data-stu-id="ed921-124">Note that the blanket order has not been deleted.</span></span>  
3.  <span data-ttu-id="ed921-125">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ed921-125">Choose the **OK** button.</span></span>  
4.  <span data-ttu-id="ed921-126">Til að birta niðurstöður fyrri skrefa skal velja aðgerðina **, Lína**, velja **Óbókaðar línur**, og velja síðan aðgerðina **Pantanir**.</span><span class="sxs-lookup"><span data-stu-id="ed921-126">To see the results of the preceding steps, choose the **Line** action, choose the **Unposted Lines** action, and then choose the **Orders** action.</span></span>  
5.  <span data-ttu-id="ed921-127">Í glugganum **Sölulínur** er viðeigandi sölupöntun valin, velja aðgerðina **Lína** og velja svo **Sýna fylgiskjal** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="ed921-127">In the **Sales Lines** window, select the appropriate sales order, choose the **Line** action, and then choose the **Show Document** action.</span></span>  

<span data-ttu-id="ed921-128">Eftirfarandi á við sölupantanir eftir að þær hafa verið stofnaðar úr standandi sölupöntunum:</span><span class="sxs-lookup"><span data-stu-id="ed921-128">The following applies to sales orders after they have been created from blanket sales orders:</span></span>  

- <span data-ttu-id="ed921-129">Þegar búið er að breyta standandi pöntun í sölupöntun inniheldur sölupöntunin allar línur standandi pöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="ed921-129">After the blanket order is converted into a sales order, the sales order contains all the lines from the blanket order.</span></span> <span data-ttu-id="ed921-130">Línurnar þar sem magninu í reitnum **Magn til afhendingar** var eytt birtast með reitina **Magn** auða.</span><span class="sxs-lookup"><span data-stu-id="ed921-130">The lines where the quantity in the **Qty. to Ship** field was deleted appear, but with blank **Quantity** fields.</span></span> <span data-ttu-id="ed921-131">Hægt er velja hvort línurnar haldi sér, þeim sé breytt eða þeim eytt.</span><span class="sxs-lookup"><span data-stu-id="ed921-131">You may choose to leave, edit, or delete the lines.</span></span>  
- <span data-ttu-id="ed921-132">Mikilvægt er að hafa í huga að magn sölupöntunarlínunnar má ekki vera meira en magnið í tengdri standandi pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="ed921-132">It is important to remember that the sales order line quantity must not exceed the quantity of the associated blanket order line.</span></span> <span data-ttu-id="ed921-133">Annars er ekki hægt að bóka sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="ed921-133">Otherwise, posting of the sales order will not be possible.</span></span>  
- <span data-ttu-id="ed921-134">Þegar sölupöntun er bókuð eða hún afhent og/eða reikningsfærð uppfærir kerfið reitina **Afhent magn** og **Reikningsfært magn** í tengdri standandi pöntun.</span><span class="sxs-lookup"><span data-stu-id="ed921-134">When the sales order is posted as shipped and/or invoiced, the **Quantity Shipped** and **Quantity Invoiced** fields are updated on the related blanket order.</span></span>  
- <span data-ttu-id="ed921-135">Skráð er númer standandi pöntunarinnar og línunúmer sem eiginleika sölulínunnar þegar hún er stofnuð úr standandi pöntun.</span><span class="sxs-lookup"><span data-stu-id="ed921-135">The blanket order number and line number are recorded as properties of the sales lines when created from a blanket order.</span></span>  
- <span data-ttu-id="ed921-136">Þegar innkaupapantanir eru ekki stofnaðar beint upp úr standandi pöntun en tengjast henni eigi að síður er hægt að koma á tengingu milli innkaupapöntunar og standandi pöntunar með því að skrá númer tengdrar standandi pöntunar í **Standandi pöntun nr.**</span><span class="sxs-lookup"><span data-stu-id="ed921-136">When sales orders are not created directly from the blanket order but still relate to it, a link between a sales order and a blanket order can be established by entering the associated blanket order number in the **Blanket Order No.**</span></span> <span data-ttu-id="ed921-137">reitinn í sölupöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="ed921-137">field on the sales order line.</span></span>  
- <span data-ttu-id="ed921-138">Eftir að sölupöntunin hefur verið stofnuð fyrir heildarmagn standandi pöntunarlínu, verður ekki hægt að stofna neina aðra sölupöntun fyrir sömu línu.</span><span class="sxs-lookup"><span data-stu-id="ed921-138">After the sales order has been created for the total quantity of a blanket order line, no other sales order can be created for the same line.</span></span> <span data-ttu-id="ed921-139">Notendur eru hindraðir frá því að færa magn inn í reitinn **Magn til afhendingar**.</span><span class="sxs-lookup"><span data-stu-id="ed921-139">Users are prevented from entering a quantity in the **Qty. to Ship** field.</span></span> <span data-ttu-id="ed921-140">Ef hins vegar þarf að bæta viðbótarmagni við standandi pöntun er hægt að hækka gildið í reitnum **Magn** og svo stofna viðbótarpantanir.</span><span class="sxs-lookup"><span data-stu-id="ed921-140">If, however, additional quantities need to be added to a blanket order, the value in the **Quantity** field can be increased and additional orders can then be created.</span></span>  
- <span data-ttu-id="ed921-141">Reikningsfærða standandi pöntunin er til staðar í kerfinu þangað til henni er eytt annað hvort með því að eyða hverri standandi pöntun fyrir sig eða með keyrslunni **Eyða reikningsfærðum standandi sölupöntunum**.</span><span class="sxs-lookup"><span data-stu-id="ed921-141">The invoiced blanket sales order remains in the system until it is deleted, either by deleting individual blanket orders or by running the **Delete Invoiced Blanket Sales Orders** batch job.</span></span>  
- <span data-ttu-id="ed921-142">Ef viðskiptamaður er einnig skráður sem tengiliður í kerfishlutanum Tengslagrunnur og ef kóti samskiptasniðmáts fyrir standandi söluvörupöntun hefur verið skilgreindur í glugganum **Tengslagrunnur** eru samskipti skráð sjálfkrafa í töfluna Skráningarfærsla samskipta þegar smellt er á **Prenta** til að prenta standandi söluvörupöntunina.</span><span class="sxs-lookup"><span data-stu-id="ed921-142">If a customer is also recorded as a contact in the Marketing application area, and if you have specified an interaction template code for blanket sales order in the **Marketing Setup** window, an interaction is recorded in the Interaction Log Entry table when you select **Print** to print the blanket sales order.</span></span>

## <a name="to-view-the-status-of-a-blanket-purchase-order"></a><span data-ttu-id="ed921-143">Staða standandi innkaupapantana skoðuð:</span><span class="sxs-lookup"><span data-stu-id="ed921-143">To view the status of a blanket purchase order</span></span>  
<span data-ttu-id="ed921-144">Hægt er að skoða stöðu standandi sölupantana í glugganum **Upplýsingar um standandi sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="ed921-144">You can see the status of a blanket sales order in the **Purchase Blanket Order Statistics** window.</span></span> <span data-ttu-id="ed921-145">Þetta gæti skipt máli þegar byrjað er að reikningsfæra pöntunina sem búin er til úr standandi innkaupapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="ed921-145">This may be relevant when you start to invoice the order that is created from the blanket purchase order.</span></span>  

1.  <span data-ttu-id="ed921-146">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Standandi innkaupapantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="ed921-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Blanket Purchase Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ed921-147">Velja Standandi innkaupapöntun og velja síðan aðgerðina **Upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="ed921-147">Select a blanket purchase order, and then choose the **Statistics** action.</span></span>  
3.  <span data-ttu-id="ed921-148">Í glugganum **Upplýsingar um standandi innkaupapöntun** á flýtiflipanum **Almennt** er hægt að sjá samantekt á allri pöntuninni byggða á heildarmagni í ýmsum **magnreitum** í línum standandi innkaupapöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="ed921-148">In the **Purchase Blanket Order Statistics** window, on the **General** FastTab, you can see summary information about the entire order based on the total quantity in the various **Quantity fields** on the blanket purchase order lines.</span></span>  

    - <span data-ttu-id="ed921-149">Á flýtiflipanum **Reikningsfærsla** er hægt að sjá samantekt byggða á heildarmagni í reitunum **Magn til reikningsf.** í línum standandi innkaupapöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="ed921-149">On the **Invoicing** FastTab, you can see summary information based on the total quantity in the **Qty. to Invoice** fields on the purchase blanket order lines.</span></span>  
    - <span data-ttu-id="ed921-150">Á flýtiflipanum **Afhending** er hægt að sjá samantekt byggða á heildarmagni í reitunum **Magn til móttöku** í línum standandi innkaupapöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="ed921-150">On the **Shipping** FastTab, you can see summary information based on the total quantity in the **Qty. to Receive** fields on the purchase blanket order lines.</span></span>  
    - <span data-ttu-id="ed921-151">Á flýtiflipanum **Fyrirframgreiðsla** er hægt að sjá samantekt um allar fyrirframgreiddar upphæðir.</span><span class="sxs-lookup"><span data-stu-id="ed921-151">On the **Prepayment** FastTab, you can see summary information about any prepaid amounts.</span></span>  
    - <span data-ttu-id="ed921-152">Á flýtiflipanum **Lánardrottinn** er hægt að skoða ákveðnar grunnupplýsingar um lánardrottininn.</span><span class="sxs-lookup"><span data-stu-id="ed921-152">On the **Vendor** FastTab, you can see certain basic information about the vendor.</span></span>    

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a><span data-ttu-id="ed921-153">Hvernig á að skoða óbókaðar og bókaðar línur standandi sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="ed921-153">To view unposted and posted blanket sales order lines</span></span>   
<span data-ttu-id="ed921-154">Tengingin milli standandi sölupöntunar og upphaflegrar sölupöntunar, og allra annarra söluskjala, er varðveitt eftir bókun sem listi yfir bókaðar og óbókaðar reikningslínur sölupantana.</span><span class="sxs-lookup"><span data-stu-id="ed921-154">The link between the blanket sales order and the originating sales order, and any other sales document, is retained after posting as a list of posted and unposted sales order invoice lines.</span></span>  

1. <span data-ttu-id="ed921-155">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Standandi sölupantanir** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="ed921-155">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon enter **Blanket Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="ed921-156">Opna standandi sölupöntun sem á að skoða.</span><span class="sxs-lookup"><span data-stu-id="ed921-156">Open the blanket sales order you want to view.</span></span>
3. <span data-ttu-id="ed921-157">Til að skoða óbókaðar færslur skal smella á viðkomandi línu, velja aðgerðina **Lína**, og velja síðan aðgerðina **óbókaðar línur**.</span><span class="sxs-lookup"><span data-stu-id="ed921-157">To view unposted entries, select the line in question, choose the **Line** action, and then choose the **Unposted Lines** action.</span></span> <span data-ttu-id="ed921-158">Einn af eftirfarandi kostum er valinn:</span><span class="sxs-lookup"><span data-stu-id="ed921-158">Choose one of the following options.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="ed921-159">Valkostur</span><span class="sxs-lookup"><span data-stu-id="ed921-159">Option</span></span></th>
    <th><span data-ttu-id="ed921-160">Description</span><span class="sxs-lookup"><span data-stu-id="ed921-160">Description</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="ed921-161">**Pantanir**</span><span class="sxs-lookup"><span data-stu-id="ed921-161">**Orders**</span></span></td>
    <td><span data-ttu-id="ed921-162">Tilgreinir opnar pantanir tengdar völdu línunni.</span><span class="sxs-lookup"><span data-stu-id="ed921-162">Specifies open orders associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="ed921-163">**Reikningar**</span><span class="sxs-lookup"><span data-stu-id="ed921-163">**Invoices**</span></span></td>
    <td><span data-ttu-id="ed921-164">Tilgreinir opna reikninga sem tengdir hafa verið við völdu línuna.</span><span class="sxs-lookup"><span data-stu-id="ed921-164">Specifies open invoices that have been associated with the selected line.</span></span> <span data-ttu-id="ed921-165">Opnir reikningar eru handvirkt tengdir við standandi pöntun með því færa inn standandi pöntunarnúmer í sölureikningslínuna.</span><span class="sxs-lookup"><span data-stu-id="ed921-165">Open invoices are manually associated with a blanket order by entering the blanket order number on the sales invoice line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="ed921-166">**Vöruskilapantanir**</span><span class="sxs-lookup"><span data-stu-id="ed921-166">**Return Orders**</span></span></td>
    <td><span data-ttu-id="ed921-167">Tilgreinir opnar vöruskilapantanir sem hafa verið tengdar við völdu línuna eru opnaðar.</span><span class="sxs-lookup"><span data-stu-id="ed921-167">Specifies open return orders that have been associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="ed921-168">**Kreditreikningar**</span><span class="sxs-lookup"><span data-stu-id="ed921-168">**Credit Memos**</span></span></td>
    <td><span data-ttu-id="ed921-169">Tilgreinir kreditreikninga sem tengdir hafa verið við völdu línuna.</span><span class="sxs-lookup"><span data-stu-id="ed921-169">Specifies open credit memos that have been associated with the selected line.</span></span></td>
    </tr>
    </table><span data-ttu-id="ed921-170">
4. Til að skoða bókaðar færslur skal smella á viðkomandi línu, velja aðgerðina *\*Lína*\*, og velja síðan aðgerðina *\*bókaðar línur*\*.</span><span class="sxs-lookup"><span data-stu-id="ed921-170">
4. To view posted entries, select the line in question, choose the *\*Line** action, and then choose the *\*Posted Lines** action.</span></span> <span data-ttu-id="ed921-171">Einn af eftirfarandi kostum er valinn:</span><span class="sxs-lookup"><span data-stu-id="ed921-171">Choose one of the following options.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="ed921-172">Valkostur</span><span class="sxs-lookup"><span data-stu-id="ed921-172">Option</span></span></th>
    <th><span data-ttu-id="ed921-173">Description</span><span class="sxs-lookup"><span data-stu-id="ed921-173">Description</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="ed921-174">**Afhendingar**</span><span class="sxs-lookup"><span data-stu-id="ed921-174">**Shipments**</span></span></td>
    <td><span data-ttu-id="ed921-175">Bókaðar afhendingar tengdar við völdu línuna..</span><span class="sxs-lookup"><span data-stu-id="ed921-175">Posted shipments associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="ed921-176">**Reikningar**</span><span class="sxs-lookup"><span data-stu-id="ed921-176">**Invoices**</span></span></td>
    <td><span data-ttu-id="ed921-177">Bókaðir reikningar tengdir við völdu línuna..</span><span class="sxs-lookup"><span data-stu-id="ed921-177">Posted invoices associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="ed921-178">**Vöruskilamóttökur**</span><span class="sxs-lookup"><span data-stu-id="ed921-178">**Return Receipts**</span></span></td>
    <td><span data-ttu-id="ed921-179">Bókaðar vöruskilamóttökur tengdar við völdu línuna.</span><span class="sxs-lookup"><span data-stu-id="ed921-179">Posted return receipts that have been associated with the selected line.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="ed921-180">**Kreditreikningar**</span><span class="sxs-lookup"><span data-stu-id="ed921-180">**Credit Memos**</span></span></td>
    <td><span data-ttu-id="ed921-181">Bókaðir kreditreikningar sem tengdir hafa verið við völdu línuna.</span><span class="sxs-lookup"><span data-stu-id="ed921-181">Posted credit memos that have been associated with the selected line.</span></span></td>
    </tr>
    </table><span data-ttu-id="ed921-182">
5. Í glugganum *\*Sölulínur** skal velja aðgerðina *\*Sýna fylgiskjal** til að skoða færsluna.</span><span class="sxs-lookup"><span data-stu-id="ed921-182">
5. In the *\*Sales Lines** window, choose the *\*Show Document** action to view the entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed921-183">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ed921-183">See Also</span></span>
[<span data-ttu-id="ed921-184">Sala</span><span class="sxs-lookup"><span data-stu-id="ed921-184">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="ed921-185">Uppsetning sölu</span><span class="sxs-lookup"><span data-stu-id="ed921-185">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="ed921-186">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ed921-186">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

