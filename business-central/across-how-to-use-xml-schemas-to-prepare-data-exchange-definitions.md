---
title: Búa til XMLports út frá XML-skemum | Microsoft Docs
description: Notaðu XML skjöl til að setja upp ramma skjalaskipta.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: b00ed408bcdc5b98a7c23a8083109b140db175ae
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305117"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="9ff61-103">Nota XML-skema til að undirbúa skilgreiningar gagnaskipta</span><span class="sxs-lookup"><span data-stu-id="9ff61-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>
<span data-ttu-id="9ff61-104">Til að virkja innflutningur/útflutningur gagna í skrá í gegnum gagnaskiptaumgjörð í [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að nota XML-skema til að tilgreina hvaða gagnastök á að skiptast á við [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9ff61-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="9ff61-105">Þessi aðgerð er gerð á síðunni **XML-skemaskoðun** með því að hlaða XML-skemaskránni, velja viðeigandi gagnastök og ræsa því næst annað hvort skilgreiningu gagnaskipta eða XMLport.</span><span class="sxs-lookup"><span data-stu-id="9ff61-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing either a data exchange definition or an XMLport.</span></span>  

 <span data-ttu-id="9ff61-106">Þegar búið er að skilgreina hvaða gagnastök á að hafa með, samkvæmt XML-skema, má nota aðgerðina **Mynda XMLport** til að stofna XMLport-hlutinn.</span><span class="sxs-lookup"><span data-stu-id="9ff61-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate XMLport** action to create the XMLport object.</span></span>  

 <span data-ttu-id="9ff61-107">Einnig er hægt að nota **Mynda gagnaskiptiskilgreiningu** aðgerð til að frumstilla gagnaskiptiskilgreiningu byggt á völdum gagnastökum sem síðan er lokið í Data Exchange Framework.</span><span class="sxs-lookup"><span data-stu-id="9ff61-107">Alternatively, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="9ff61-108">Þetta stofnar færslu á síðunni **Bókunarskilgreiningar** þar sem haldið er áfram að skilgreina hvaða einingar í SEPA skráakortinu tengjast hvaða reitum í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9ff61-108">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="9ff61-109">Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="9ff61-109">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="9ff61-110">Þetta efnisatriði inniheldur eftirfarandi ferli:</span><span class="sxs-lookup"><span data-stu-id="9ff61-110">This topic contains the following procedures:</span></span>  

-   <span data-ttu-id="9ff61-111">Til að hlaða XML-skemaskrá</span><span class="sxs-lookup"><span data-stu-id="9ff61-111">To load an XML schema file</span></span>  

-   <span data-ttu-id="9ff61-112">Að velja eða hreinsa hnúta á XML-skema</span><span class="sxs-lookup"><span data-stu-id="9ff61-112">To select or clear nodes in an XML schema</span></span>  

-   <span data-ttu-id="9ff61-113">Að búa til gagnaskiptaskilgreiningu sem byggist á XML-skema</span><span class="sxs-lookup"><span data-stu-id="9ff61-113">To generate a data exchange definition that is based on an XML schema</span></span>  

-   <span data-ttu-id="9ff61-114">Að búa til XMLport fyrir skrá sem byggir á XML-skema</span><span class="sxs-lookup"><span data-stu-id="9ff61-114">To generate an XMLport for the file that is based on an XML schema</span></span>  

-   <span data-ttu-id="9ff61-115">Að flytja inn XMLport í hlutahönnuð</span><span class="sxs-lookup"><span data-stu-id="9ff61-115">To import an XMLport into the Object Designer</span></span>  

### <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="9ff61-116">Til að hlaða XML-skemaskrá</span><span class="sxs-lookup"><span data-stu-id="9ff61-116">To load an XML schema file</span></span>  

1.  <span data-ttu-id="9ff61-117">Ganga úr skugga um að viðeigandi XML-skemaskrá sé í boði.</span><span class="sxs-lookup"><span data-stu-id="9ff61-117">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="9ff61-118">Skráarendingin er .xsd.</span><span class="sxs-lookup"><span data-stu-id="9ff61-118">The file extension is .xsd.</span></span>  

2.  <span data-ttu-id="9ff61-119">Í reitnum **Leita** skal færa inn **XML-skema** og velja síðan viðkomandi tengi.</span><span class="sxs-lookup"><span data-stu-id="9ff61-119">In the **Search** box, enter **XML Schemas**, and then choose the related link.</span></span>  

3.  <span data-ttu-id="9ff61-120">Á flipanum **Heim** í flokknum **Nýtt** skal velja **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="9ff61-120">On the **Home** tab, in the **New** group, choose **New**.</span></span>  

4.  <span data-ttu-id="9ff61-121">Fylla inn í reitina eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="9ff61-121">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="9ff61-122">Svæði</span><span class="sxs-lookup"><span data-stu-id="9ff61-122">Field</span></span>|<span data-ttu-id="9ff61-123">Lýsing</span><span class="sxs-lookup"><span data-stu-id="9ff61-123">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="9ff61-124">**Kóti**</span><span class="sxs-lookup"><span data-stu-id="9ff61-124">**Code**</span></span>|<span data-ttu-id="9ff61-125">Tilgreina kóða til að greina fyrir XML-skemað.</span><span class="sxs-lookup"><span data-stu-id="9ff61-125">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="9ff61-126">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="9ff61-126">**Description**</span></span>|<span data-ttu-id="9ff61-127">Tilgreinir lýsingu á XML-skema.</span><span class="sxs-lookup"><span data-stu-id="9ff61-127">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="9ff61-128">Reiturinn **Marknafnabil** tilgreinir hvaða nafnrými í XML-skemaskrá hefur verið hlaðið fyrir þessa línu.</span><span class="sxs-lookup"><span data-stu-id="9ff61-128">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5.  <span data-ttu-id="9ff61-129">Á flipanum **Heim** í flokknum **Vinna** skal velja **Hlaða skema** og velja síðan XML-skemaskrána.</span><span class="sxs-lookup"><span data-stu-id="9ff61-129">On the **Home** tab, in the **Process** group, choose **Load Schema**, and then select the XML schema file.</span></span>  

     <span data-ttu-id="9ff61-130">Þegar skránni er hlaðið eru allir hinir reitirnir á línunni fylltir út með upplýsingum úr skránni og gátreiturinn **Skema er hlaðið** valinn.</span><span class="sxs-lookup"><span data-stu-id="9ff61-130">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="9ff61-131">Tré hlaðins XML-skema er sjálfkrafa samanfallið.</span><span class="sxs-lookup"><span data-stu-id="9ff61-131">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="9ff61-132">Hver hnútur er stækkaður með því að velja **+** hnappinn á hnútinu.</span><span class="sxs-lookup"><span data-stu-id="9ff61-132">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="9ff61-133">Til að auka alla hnúða er valið **Stækka Allt** á borðanum.</span><span class="sxs-lookup"><span data-stu-id="9ff61-133">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="9ff61-134">Að velja eða hreinsa hnúta á XML-skema</span><span class="sxs-lookup"><span data-stu-id="9ff61-134">To select or clear nodes in an XML schema</span></span>  

1.  <span data-ttu-id="9ff61-135">Í reitnum **Leita** skal færa inn **XML-skemaskoðun** og velja síðan viðkomandi tengi.</span><span class="sxs-lookup"><span data-stu-id="9ff61-135">In the **Search** box, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="9ff61-136">Fylla inn í reitina í hausnum eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="9ff61-136">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="9ff61-137">Svæði</span><span class="sxs-lookup"><span data-stu-id="9ff61-137">Field</span></span>|<span data-ttu-id="9ff61-138">Lýsing</span><span class="sxs-lookup"><span data-stu-id="9ff61-138">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="9ff61-139">**XML-skemakóði**</span><span class="sxs-lookup"><span data-stu-id="9ff61-139">**XML Schema Code**</span></span>|<span data-ttu-id="9ff61-140">Tilgreiniað XML-skemaskrá sem var hlaðið í skrefi 5 í „Að hlaða inn XML-skemaskrá“ hlutanum.</span><span class="sxs-lookup"><span data-stu-id="9ff61-140">Specify the XML schema file that you loaded in step 5 in the “To load an XML schema file” section.</span></span>|  
    |<span data-ttu-id="9ff61-141">**Ný XMLport nr.**</span><span class="sxs-lookup"><span data-stu-id="9ff61-141">**New XMLport No.**</span></span>|<span data-ttu-id="9ff61-142">Tilgreinið númer XMLport sem er búin til úr þessu XML-skema þegar þú velur **Mynda XMLport** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="9ff61-142">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="9ff61-143">Línurnar eru nú fylltar hnútum sem tákna allar einingar í XML-skema.</span><span class="sxs-lookup"><span data-stu-id="9ff61-143">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="9ff61-144">Hnútar fyrir einingar sem eru áskyldar samkvæmt XML-skemanu eru sjálfgefið valdir.</span><span class="sxs-lookup"><span data-stu-id="9ff61-144">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3.  <span data-ttu-id="9ff61-145">Á fyrstu línunni, í dálknum **Heiti hnútar**, skal stækka hnútinn **Fylgkskjal** og stækka svo smám saman undirliggjandi hnúta sem á að skoða.</span><span class="sxs-lookup"><span data-stu-id="9ff61-145">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="9ff61-146">Að öðrum kosti skal hægrismella á hnútinn og velja svo **Stækka allt**.</span><span class="sxs-lookup"><span data-stu-id="9ff61-146">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4.  <span data-ttu-id="9ff61-147">Á flipanum **Heim**, í flokknum **Skoða**, skal velja aðra hvora eftirfarandi aðgerða til að breyta því hvaða hnútar eru birtir.</span><span class="sxs-lookup"><span data-stu-id="9ff61-147">On the **Home** tab, in the **View** group, choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="9ff61-148">**Aðgerð**</span><span class="sxs-lookup"><span data-stu-id="9ff61-148">**Action**</span></span>|<span data-ttu-id="9ff61-149">Lýsing</span><span class="sxs-lookup"><span data-stu-id="9ff61-149">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="9ff61-150">**Sýna allt**</span><span class="sxs-lookup"><span data-stu-id="9ff61-150">**Show All**</span></span>|<span data-ttu-id="9ff61-151">Allir hnútar er sýndir.</span><span class="sxs-lookup"><span data-stu-id="9ff61-151">All nodes are shown.</span></span>|  
    |<span data-ttu-id="9ff61-152">**Fela það sem ekki er áskilið**</span><span class="sxs-lookup"><span data-stu-id="9ff61-152">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="9ff61-153">Aðeins eru birtir hnútar sem standa fyrir einingar sem krafist samkvæmt XML-skemanu.</span><span class="sxs-lookup"><span data-stu-id="9ff61-153">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="9ff61-154">Þessir tengipunktar eru vanalega táknaðir með **1** í reitnum **MinOccurs**.</span><span class="sxs-lookup"><span data-stu-id="9ff61-154">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="9ff61-155">Veldu **Sýna alla** að snúa við útsýni.</span><span class="sxs-lookup"><span data-stu-id="9ff61-155">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="9ff61-156">**Fela það sem ekki er valið**</span><span class="sxs-lookup"><span data-stu-id="9ff61-156">**Hide Non-Selected**</span></span>|<span data-ttu-id="9ff61-157">Aðeins hnútar þar sem gátreiturinn **Valið** er valinn sjást.</span><span class="sxs-lookup"><span data-stu-id="9ff61-157">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="9ff61-158">Veldu **Sýna alla** að snúa við útsýni.</span><span class="sxs-lookup"><span data-stu-id="9ff61-158">Choose **Show All** to reverse the view.</span></span>|  

5.  <span data-ttu-id="9ff61-159">Á flipanum **Heim** í flokknum **Stjórna** skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="9ff61-159">On the **Home** tab, in the **Manage** group, choose **Edit**.</span></span>  

6.  <span data-ttu-id="9ff61-160">Í **Valið** gátreitnum skal tilgreina fyrir hvern hnút ef stak á að vera stutt í gagnaskiptauppsetningu fyrir viðkomandi SEPA bankaskrá.</span><span class="sxs-lookup"><span data-stu-id="9ff61-160">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="9ff61-161">Þegar þú velur áskilinn undirhnút eru allir yfirhnútar fyrir ofan undirhnútinn einnig valdir.</span><span class="sxs-lookup"><span data-stu-id="9ff61-161">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7.  <span data-ttu-id="9ff61-162">Veldu aðgerðina **Velja allar áskildar einingar** til að endurvelja alla hnúta sem tákna einingar sem eru áskildar samkvæmt XML-skema.</span><span class="sxs-lookup"><span data-stu-id="9ff61-162">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8.  <span data-ttu-id="9ff61-163">Veldu **Afvelja allt** aðgerð til að hreinsa allt val.</span><span class="sxs-lookup"><span data-stu-id="9ff61-163">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="9ff61-164">Reiturinn **Val** tilgreinir að hnúturinn hefur tvo eða fleiri systkinahnúta sem valkosti.</span><span class="sxs-lookup"><span data-stu-id="9ff61-164">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="9ff61-165">Að búa til gagnaskiptaskilgreiningu sem byggist á XML-skema</span><span class="sxs-lookup"><span data-stu-id="9ff61-165">To generate a data exchange definition that is based on an XML schema</span></span>  

1.  <span data-ttu-id="9ff61-166">Í reitnum **Leita** skal færa inn **XML-skema** og velja síðan viðkomandi tengi.</span><span class="sxs-lookup"><span data-stu-id="9ff61-166">In the **Search** box, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="9ff61-167">Veljið viðkomandi XML-skema og veljið því næst á flipanum **Heima** í **Ferli** hópnum valkostinn **Opna XML skemaskoðun**.</span><span class="sxs-lookup"><span data-stu-id="9ff61-167">Select the relevant XML schema, and then on the on the **Home** tab, in the **Process** group, choose **Open XML Schema Viewer**.</span></span>  

3.  <span data-ttu-id="9ff61-168">Gangið úr skugga um að viðeigandi hnútar séu valdir.</span><span class="sxs-lookup"><span data-stu-id="9ff61-168">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="9ff61-169">Nánari upplýsingar fást í hlutanum „Að velja eða hreinsa hnúta í XML-skema“.</span><span class="sxs-lookup"><span data-stu-id="9ff61-169">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

4.  <span data-ttu-id="9ff61-170">Á síðunni **XML-skemaskoðun** í flipanum **Heim** í flokknum **Ferli** veljið **Mynda gagnaskiptaskilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="9ff61-170">On the **XML Schema Viewer** page, on the **Home** tab, in the **Process** group, choose **Generate Data Exchange Definition**.</span></span>  

 <span data-ttu-id="9ff61-171">Gagnaskiptaskilgreining er sett upp á síðunni **Bókunarskilgreiningar**, sem hægt er að ljúka með því að tilgreina hvaða stök í skránni varpast í hvaða reiti í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9ff61-171">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="9ff61-172">Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="9ff61-172">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9ff61-173">Einnig er hægt að nota **Sækja skráaskipan** virknina á **Bókunarskilgreining** síðunni sem notar virkni **XML-skemaskoðun** til að fylla út í flýtiflipann **Dálkaskilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="9ff61-173">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a><span data-ttu-id="9ff61-174">Að búa til XMLport sem byggir á XML-skema</span><span class="sxs-lookup"><span data-stu-id="9ff61-174">To generate an XMLport that is based on an XML schema</span></span>  

1.  <span data-ttu-id="9ff61-175">Í reitnum **Leita** skal færa inn **XML-skema** og velja síðan viðkomandi tengi.</span><span class="sxs-lookup"><span data-stu-id="9ff61-175">In the **Search** box, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="9ff61-176">Veljið viðkomandi XML-skema og veljið því næst á flipanum **Heima** í **Ferli** hópnum valkostinn **Opna XML skemaskoðun**.</span><span class="sxs-lookup"><span data-stu-id="9ff61-176">Select the relevant XML schema, and then on the on the **Home** tab, in the **Process** group, choose **Open XML Schema Viewer**.</span></span>  

3.  <span data-ttu-id="9ff61-177">Í **Ný XMLport nr.**</span><span class="sxs-lookup"><span data-stu-id="9ff61-177">In the **New XMLport No.**</span></span> <span data-ttu-id="9ff61-178">reitnum skal tilgreina númer sem nýja XMLport-hlutnum verður gefið þegar hann er myndaður.</span><span class="sxs-lookup"><span data-stu-id="9ff61-178">field, specify the number that the new XMLport object will be given when it is generated.</span></span>  

4.  <span data-ttu-id="9ff61-179">Gangið úr skugga um að viðeigandi hnútar séu valdir.</span><span class="sxs-lookup"><span data-stu-id="9ff61-179">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="9ff61-180">Nánari upplýsingar fást í hlutanum „Að velja eða hreinsa hnúta í XML-skema“.</span><span class="sxs-lookup"><span data-stu-id="9ff61-180">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

5.  <span data-ttu-id="9ff61-181">Á flipanum **Heim**, í flokknum **Vinna**, skal velja **Mynda XMLport** og vista svo hlutinn sem .txt-skrá á viðeigandi stað.</span><span class="sxs-lookup"><span data-stu-id="9ff61-181">On the **Home** tab, in the **Process** group, choose **Generate XMLport**, and then save the object as a .txt file in an appropriate location.</span></span>  

6. <span data-ttu-id="9ff61-182">Flytja skal nýja XMLport í [!INCLUDE[d365fin](includes/d365fin_md.md)] þróunarumhverfið og þýða hana.</span><span class="sxs-lookup"><span data-stu-id="9ff61-182">Import the new XMLport into the [!INCLUDE[d365fin](includes/d365fin_md.md)] development environment and compile it.</span></span>

## <a name="see-also"></a><span data-ttu-id="9ff61-183">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9ff61-183">See Also</span></span>  
<span data-ttu-id="9ff61-184">[Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md) </span><span class="sxs-lookup"><span data-stu-id="9ff61-184">[Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) </span></span>  
<span data-ttu-id="9ff61-185">[Flytja út greiðslur í bankaskrá](payables-how-export-payments-bank-file.md) </span><span class="sxs-lookup"><span data-stu-id="9ff61-185">[Export Payments to a Bank File](payables-how-export-payments-bank-file.md) </span></span>  
<span data-ttu-id="9ff61-186">[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="9ff61-186">[Collect Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
[<span data-ttu-id="9ff61-187">Um gagnaskiptaramma</span><span class="sxs-lookup"><span data-stu-id="9ff61-187">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)
