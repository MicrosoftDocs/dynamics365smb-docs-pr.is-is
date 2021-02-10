---
title: Nota XML-skema til að undirbúa skilgreiningar gagnaskipta
description: Notaðu XML skjöl til að setja upp ramma skjalaskipta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 78aa941b8b886ed37dbed0d83a35d13b0e427421
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754618"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="a4d23-103">Nota XML-skema til að undirbúa skilgreiningar gagnaskipta</span><span class="sxs-lookup"><span data-stu-id="a4d23-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>

<span data-ttu-id="a4d23-104">Til að virkja innflutningur/útflutningur gagna í skrá í gegnum gagnaskiptaumgjörð í [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að nota XML-skema til að tilgreina hvaða gagnastök á að skiptast á við [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="a4d23-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[prod_short](includes/prod_short.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="a4d23-105">Þessi aðgerð er gerð á síðunni **XML-skemaskoðun** með því að hlaða XML-skemaskránni, velja viðeigandi gagnastök og ræsa skilgreiningu gagnaskipta.</span><span class="sxs-lookup"><span data-stu-id="a4d23-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing a data exchange definition.</span></span>  

 <span data-ttu-id="a4d23-106">Þegar búið er að skilgreina hvaða gagnastök á að hafa með er hægt að nota **Mynda skilgreiningu gagnaskipta** aðgerð til að frumstilla gagnaskiptiskilgreiningu byggt á völdum gagnastökum sem síðan er lokið í Data Exchange Framework.</span><span class="sxs-lookup"><span data-stu-id="a4d23-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="a4d23-107">Þetta stofnar færslu á síðunni **Bókunarskilgreiningar** þar sem haldið er áfram að skilgreina hvaða einingar í SEPA skráakortinu tengjast hvaða reitum í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="a4d23-107">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="a4d23-108">Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="a4d23-108">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="a4d23-109">Þetta efnisatriði inniheldur eftirfarandi ferli:</span><span class="sxs-lookup"><span data-stu-id="a4d23-109">This topic contains the following procedures:</span></span>  

- <span data-ttu-id="a4d23-110">Til að hlaða XML-skemaskrá</span><span class="sxs-lookup"><span data-stu-id="a4d23-110">To load an XML schema file</span></span>  

- <span data-ttu-id="a4d23-111">Að velja eða hreinsa hnúta á XML-skema</span><span class="sxs-lookup"><span data-stu-id="a4d23-111">To select or clear nodes in an XML schema</span></span>  

- <span data-ttu-id="a4d23-112">Að búa til gagnaskiptaskilgreiningu sem byggist á XML-skema</span><span class="sxs-lookup"><span data-stu-id="a4d23-112">To generate a data exchange definition that is based on an XML schema</span></span>  

## <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="a4d23-113">Til að hlaða XML-skemaskrá</span><span class="sxs-lookup"><span data-stu-id="a4d23-113">To load an XML schema file</span></span>

1. <span data-ttu-id="a4d23-114">Ganga úr skugga um að viðeigandi XML-skemaskrá sé í boði.</span><span class="sxs-lookup"><span data-stu-id="a4d23-114">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="a4d23-115">Skráarendingin er .xsd.</span><span class="sxs-lookup"><span data-stu-id="a4d23-115">The file extension is .xsd.</span></span>  

2. <span data-ttu-id="a4d23-116">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **XML-skema** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a4d23-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schemas**, and then choose the related link.</span></span>  

3. <span data-ttu-id="a4d23-117">Valið er aðgerðin **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a4d23-117">Choose the **New** action.</span></span>  

4. <span data-ttu-id="a4d23-118">Fylla inn í reitina eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="a4d23-118">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="a4d23-119">Svæði</span><span class="sxs-lookup"><span data-stu-id="a4d23-119">Field</span></span>|<span data-ttu-id="a4d23-120">Lýsing</span><span class="sxs-lookup"><span data-stu-id="a4d23-120">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a4d23-121">**Kóti**</span><span class="sxs-lookup"><span data-stu-id="a4d23-121">**Code**</span></span>|<span data-ttu-id="a4d23-122">Tilgreina kóða til að greina fyrir XML-skemað.</span><span class="sxs-lookup"><span data-stu-id="a4d23-122">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="a4d23-123">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="a4d23-123">**Description**</span></span>|<span data-ttu-id="a4d23-124">Tilgreinir lýsingu á XML-skema.</span><span class="sxs-lookup"><span data-stu-id="a4d23-124">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="a4d23-125">Reiturinn **Marknafnabil** tilgreinir hvaða nafnrými í XML-skemaskrá hefur verið hlaðið fyrir þessa línu.</span><span class="sxs-lookup"><span data-stu-id="a4d23-125">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5. <span data-ttu-id="a4d23-126">Veldu aðgerðina **Hlaða skema** og veldu síðan XML-skemaskrána.</span><span class="sxs-lookup"><span data-stu-id="a4d23-126">Choose the **Load Schema** action, and then select the XML schema file.</span></span>  

     <span data-ttu-id="a4d23-127">Þegar skránni er hlaðið eru allir hinir reitirnir á línunni fylltir út með upplýsingum úr skránni og gátreiturinn **Skema er hlaðið** valinn.</span><span class="sxs-lookup"><span data-stu-id="a4d23-127">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a4d23-128">Tré hlaðins XML-skema er sjálfkrafa samanfallið.</span><span class="sxs-lookup"><span data-stu-id="a4d23-128">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="a4d23-129">Hver hnútur er stækkaður með því að velja **+** hnappinn á hnútinu.</span><span class="sxs-lookup"><span data-stu-id="a4d23-129">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="a4d23-130">Til að auka alla hnúða er valið **Stækka Allt** á borðanum.</span><span class="sxs-lookup"><span data-stu-id="a4d23-130">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="a4d23-131">Að velja eða hreinsa hnúta á XML-skema</span><span class="sxs-lookup"><span data-stu-id="a4d23-131">To select or clear nodes in an XML schema</span></span>  

1. <span data-ttu-id="a4d23-132">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **XML-skemaskoðun** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a4d23-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2. <span data-ttu-id="a4d23-133">Fylla inn í reitina í hausnum eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="a4d23-133">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="a4d23-134">Svæði</span><span class="sxs-lookup"><span data-stu-id="a4d23-134">Field</span></span>|<span data-ttu-id="a4d23-135">Lýsing</span><span class="sxs-lookup"><span data-stu-id="a4d23-135">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a4d23-136">**XML-skemakóði**</span><span class="sxs-lookup"><span data-stu-id="a4d23-136">**XML Schema Code**</span></span>|<span data-ttu-id="a4d23-137">Tilgreinið XML-skemaskrá sem var hlaðið í skrefi 5 í „Að hlaða inn XML-skemaskrá“ hlutanum.</span><span class="sxs-lookup"><span data-stu-id="a4d23-137">Specify the XML schema file that you loaded in step 5 in the "To load an XML schema file" section.</span></span>|  
    |<span data-ttu-id="a4d23-138">**Ný XMLport nr.**</span><span class="sxs-lookup"><span data-stu-id="a4d23-138">**New XMLport No.**</span></span>|<span data-ttu-id="a4d23-139">Tilgreinið númer XMLport sem er búin til úr þessu XML-skema þegar þú velur **Mynda XMLport** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="a4d23-139">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="a4d23-140">Línurnar eru nú fylltar hnútum sem tákna allar einingar í XML-skema.</span><span class="sxs-lookup"><span data-stu-id="a4d23-140">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="a4d23-141">Hnútar fyrir einingar sem eru áskyldar samkvæmt XML-skemanu eru sjálfgefið valdir.</span><span class="sxs-lookup"><span data-stu-id="a4d23-141">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3. <span data-ttu-id="a4d23-142">Á fyrstu línunni, í dálknum **Heiti hnútar**, skal stækka hnútinn **Fylgkskjal** og stækka svo smám saman undirliggjandi hnúta sem á að skoða.</span><span class="sxs-lookup"><span data-stu-id="a4d23-142">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="a4d23-143">Að öðrum kosti skal hægrismella á hnútinn og velja svo **Stækka allt**.</span><span class="sxs-lookup"><span data-stu-id="a4d23-143">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4. <span data-ttu-id="a4d23-144">Veldu aðra hvora eftirfarandi aðgerða til að breyta því hvaða hnútar eru birtir.</span><span class="sxs-lookup"><span data-stu-id="a4d23-144">Choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="a4d23-145">**Aðgerð**</span><span class="sxs-lookup"><span data-stu-id="a4d23-145">**Action**</span></span>|<span data-ttu-id="a4d23-146">Lýsing</span><span class="sxs-lookup"><span data-stu-id="a4d23-146">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="a4d23-147">**Sýna allt**</span><span class="sxs-lookup"><span data-stu-id="a4d23-147">**Show All**</span></span>|<span data-ttu-id="a4d23-148">Allir hnútar er sýndir.</span><span class="sxs-lookup"><span data-stu-id="a4d23-148">All nodes are shown.</span></span>|  
    |<span data-ttu-id="a4d23-149">**Fela það sem ekki er áskilið**</span><span class="sxs-lookup"><span data-stu-id="a4d23-149">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="a4d23-150">Aðeins eru birtir hnútar sem standa fyrir einingar sem krafist samkvæmt XML-skemanu.</span><span class="sxs-lookup"><span data-stu-id="a4d23-150">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="a4d23-151">Þessir tengipunktar eru vanalega táknaðir með **1** í reitnum **MinOccurs**.</span><span class="sxs-lookup"><span data-stu-id="a4d23-151">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="a4d23-152">Veldu **Sýna alla** að snúa við útsýni.</span><span class="sxs-lookup"><span data-stu-id="a4d23-152">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="a4d23-153">**Fela það sem ekki er valið**</span><span class="sxs-lookup"><span data-stu-id="a4d23-153">**Hide Non-Selected**</span></span>|<span data-ttu-id="a4d23-154">Aðeins hnútar þar sem gátreiturinn **Valið** er valinn sjást.</span><span class="sxs-lookup"><span data-stu-id="a4d23-154">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="a4d23-155">Veldu **Sýna alla** að snúa við útsýni.</span><span class="sxs-lookup"><span data-stu-id="a4d23-155">Choose **Show All** to reverse the view.</span></span>|  

5. <span data-ttu-id="a4d23-156">Veldu aðgerðina **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="a4d23-156">Choose the **Edit** action.</span></span>  

6. <span data-ttu-id="a4d23-157">Í **Valið** gátreitnum skal tilgreina fyrir hvern hnút ef stak á að vera stutt í gagnaskiptauppsetningu fyrir viðkomandi SEPA bankaskrá.</span><span class="sxs-lookup"><span data-stu-id="a4d23-157">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="a4d23-158">Þegar þú velur áskilinn undirhnút eru allir yfirhnútar fyrir ofan undirhnútinn einnig valdir.</span><span class="sxs-lookup"><span data-stu-id="a4d23-158">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7. <span data-ttu-id="a4d23-159">Veldu aðgerðina **Velja allar áskildar einingar** til að endurvelja alla hnúta sem tákna einingar sem eru áskildar samkvæmt XML-skema.</span><span class="sxs-lookup"><span data-stu-id="a4d23-159">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8. <span data-ttu-id="a4d23-160">Veldu **Afvelja allt** aðgerð til að hreinsa allt val.</span><span class="sxs-lookup"><span data-stu-id="a4d23-160">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="a4d23-161">Reiturinn **Val** tilgreinir að hnúturinn hefur tvo eða fleiri systkinahnúta sem valkosti.</span><span class="sxs-lookup"><span data-stu-id="a4d23-161">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="a4d23-162">Að búa til gagnaskiptaskilgreiningu sem byggist á XML-skema</span><span class="sxs-lookup"><span data-stu-id="a4d23-162">To generate a data exchange definition that is based on an XML schema</span></span>  

1. <span data-ttu-id="a4d23-163">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **XML-skema** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="a4d23-163">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2. <span data-ttu-id="a4d23-164">Veldu viðeigandi XML-skema og veldu svo aðgerðina **Opna XML-skemaskoðun**.</span><span class="sxs-lookup"><span data-stu-id="a4d23-164">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3. <span data-ttu-id="a4d23-165">Gangið úr skugga um að viðeigandi hnútar séu valdir.</span><span class="sxs-lookup"><span data-stu-id="a4d23-165">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="a4d23-166">Nánari upplýsingar fást í hlutanum „Að velja eða hreinsa hnúta í XML-skema“.</span><span class="sxs-lookup"><span data-stu-id="a4d23-166">For more information, see the "To select or clear nodes in an XML schema" section.</span></span>  

4. <span data-ttu-id="a4d23-167">Á síðunni **XML-skemaskoðun** skaltu velja aðgerðina **Mynda skilgreiningu gagnaskipta**.</span><span class="sxs-lookup"><span data-stu-id="a4d23-167">On the **XML Schema Viewer** page, choose the **Generate Data Exchange Definition** action.</span></span>  

 <span data-ttu-id="a4d23-168">Gagnaskiptaskilgreining er sett upp á síðunni **Bókunarskilgreiningar**, sem hægt er að ljúka með því að tilgreina hvaða stök í skránni varpast í hvaða reiti í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="a4d23-168">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="a4d23-169">Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="a4d23-169">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="a4d23-170">Einnig er hægt að nota **Sækja skráaskipan** virknina á **Bókunarskilgreining** síðunni sem notar virkni **XML-skemaskoðun** til að fylla út í flýtiflipann **Dálkaskilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="a4d23-170">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

> [!NOTE]
> <span data-ttu-id="a4d23-171">Í 2019 útgáfutímabili 1 og fyrri útgáfum var hægt að búa til XMLport sem byggðist á skemanu og síðan flutt inn í lausnina.</span><span class="sxs-lookup"><span data-stu-id="a4d23-171">In 2019 release wave 1 and earlier versions, you could generate an XMLport that was based on the schema and then import that into your solution.</span></span> <span data-ttu-id="a4d23-172">Þetta er ekki lengur stutt.</span><span class="sxs-lookup"><span data-stu-id="a4d23-172">This is no longer supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4d23-173">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a4d23-173">See Also</span></span>

[<span data-ttu-id="a4d23-174">Setja upp skilgreiningar gagnaskipta</span><span class="sxs-lookup"><span data-stu-id="a4d23-174">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="a4d23-175">Flytja út greiðslur í bankaskrá</span><span class="sxs-lookup"><span data-stu-id="a4d23-175">Export Payments to a Bank File</span></span>](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[<span data-ttu-id="a4d23-176">Innheimta greiðslur með SEPA-beingreiðslum</span><span class="sxs-lookup"><span data-stu-id="a4d23-176">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="a4d23-177">Um gagnaskiptaramma</span><span class="sxs-lookup"><span data-stu-id="a4d23-177">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)  
