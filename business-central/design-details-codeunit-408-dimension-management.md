---
title: "Hönnunarupplýsingar - Kóðaeining 408 víddarstjórnun | Microsoft Docs"
description: "Kóðaeining 408 Víddastjórnun er aðgerðasafn sem sér um algeng verkefni sem tengjast víddum, m.a. afritun úr einni töflu í aðra eða úr einu skjali í annað."
services: project-madeira
documentationcenter: 
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
ms.openlocfilehash: 95d4afc18b0be620df2f4b2067a093237c7c4df2
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="5122c-103">Hönnunarupplýsingar: Codeunit 408 víddarstjórnun</span><span class="sxs-lookup"><span data-stu-id="5122c-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="5122c-104">Kóðaeining 408 Víddastjórnun er aðgerðasafn sem sér um algeng verkefni sem tengjast víddum, m.a. afritun úr einni töflu í aðra eða úr einu skjali í annað.</span><span class="sxs-lookup"><span data-stu-id="5122c-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="5122c-105">Þetta efnisatriði er listi yfir aðgerðir sem er breytt í Microsoft Dynamics NAV 2013 R2 og skilgreinir hvað þarf að gera við aðgerðirnar.</span><span class="sxs-lookup"><span data-stu-id="5122c-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="5122c-106">Mörgum aðgerðum er eytt vegna þess að ekki er þörf á að afrita á milli víddatafla.</span><span class="sxs-lookup"><span data-stu-id="5122c-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="5122c-107">Breyttar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="5122c-107">Modified Functions</span></span>  

|<span data-ttu-id="5122c-108">Heiti aðgerðar</span><span class="sxs-lookup"><span data-stu-id="5122c-108">Function Name</span></span>|<span data-ttu-id="5122c-109">Lýsing á breytingum</span><span class="sxs-lookup"><span data-stu-id="5122c-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="5122c-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="5122c-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="5122c-111">Ný aðgerð sem kemur í stað annarra skoðunaraðgerða og notar víddasamstæðukenni sem frumbreytu í stað víddatöflu.</span><span class="sxs-lookup"><span data-stu-id="5122c-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="5122c-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="5122c-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="5122c-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="5122c-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="5122c-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="5122c-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="5122c-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="5122c-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="5122c-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="5122c-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="5122c-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="5122c-117">CheckDimValueComb</span></span>|<span data-ttu-id="5122c-118">Eyða</span><span class="sxs-lookup"><span data-stu-id="5122c-118">Delete.</span></span> <span data-ttu-id="5122c-119">Allri notkun ætti að breyta í CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="5122c-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="5122c-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="5122c-120">GetDefaultDim</span></span>|<span data-ttu-id="5122c-121">Breytið til að skila víddasamstæðukenni í heiltölu í stað færslusafns.</span><span class="sxs-lookup"><span data-stu-id="5122c-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="5122c-122">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="5122c-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="5122c-123">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="5122c-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="5122c-124">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="5122c-125">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="5122c-126">Bryeta til að vinna með DimSetID -> ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="5122c-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="5122c-127">Eyddar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="5122c-127">Deleted Functions</span></span>  
 <span data-ttu-id="5122c-128">Aðgerðum sem er eytt út úr kóðaeiningu 408 í tengslum við eiginleikann víddasamstæðufærslur eru skráðar hér fyrir neðan.</span><span class="sxs-lookup"><span data-stu-id="5122c-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="5122c-129">Meðan á uppfærsla á forritakóðanum úr Microsoft Dynamics NAV 2009 eða fyrri útgáfum yfir í Microsoft Dynamics NAV 2016 eru eftirfarandi aðgerðir ekki tiltækar í Microsoft Dynamics NAV 2016.</span><span class="sxs-lookup"><span data-stu-id="5122c-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="5122c-130">Ef þú ert með sérstillingar sem nota einn eða fleiri aðgerðir verður að uppfæra kóðann í samræmi við það.</span><span class="sxs-lookup"><span data-stu-id="5122c-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="5122c-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="5122c-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="5122c-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="5122c-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="5122c-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="5122c-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="5122c-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="5122c-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="5122c-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="5122c-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="5122c-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-136">InsertDocDim</span></span>  

 <span data-ttu-id="5122c-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="5122c-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="5122c-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="5122c-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="5122c-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="5122c-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="5122c-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="5122c-141">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="5122c-141">InsertServContractDim</span></span>  

 <span data-ttu-id="5122c-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="5122c-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="5122c-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="5122c-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="5122c-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-144">GetDocDim</span></span>  

 <span data-ttu-id="5122c-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-145">GetProdDocDim</span></span>  

 <span data-ttu-id="5122c-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="5122c-146">TypeToTableID1</span></span>  

 <span data-ttu-id="5122c-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="5122c-147">TypeToTableID2</span></span>  

 <span data-ttu-id="5122c-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="5122c-148">TypeToTableID3</span></span>  

 <span data-ttu-id="5122c-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="5122c-149">TypeToTableID4</span></span>  

 <span data-ttu-id="5122c-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="5122c-150">TypeToTableID5</span></span>  

 <span data-ttu-id="5122c-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="5122c-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="5122c-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-152">DeleteDocDim</span></span>  

 <span data-ttu-id="5122c-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="5122c-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="5122c-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="5122c-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="5122c-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="5122c-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="5122c-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="5122c-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="5122c-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="5122c-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="5122c-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="5122c-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="5122c-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-160">ShowDocDim</span></span>  

 <span data-ttu-id="5122c-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-161">SaveDocDim</span></span>  

 <span data-ttu-id="5122c-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="5122c-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="5122c-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="5122c-164">ShowTempDim</span></span>  

 <span data-ttu-id="5122c-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="5122c-165">SaveTempDim</span></span>  

 <span data-ttu-id="5122c-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="5122c-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="5122c-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="5122c-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="5122c-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="5122c-168">SaveServContractDim</span></span>  

 <span data-ttu-id="5122c-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="5122c-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="5122c-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="5122c-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="5122c-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="5122c-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="5122c-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="5122c-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="5122c-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="5122c-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="5122c-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="5122c-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="5122c-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="5122c-177">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="5122c-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="5122c-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="5122c-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="5122c-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="5122c-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="5122c-181">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="5122c-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="5122c-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="5122c-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="5122c-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="5122c-184">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="5122c-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="5122c-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="5122c-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="5122c-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="5122c-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="5122c-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="5122c-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="5122c-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="5122c-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="5122c-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="5122c-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="5122c-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="5122c-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="5122c-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="5122c-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="5122c-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="5122c-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="5122c-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="5122c-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="5122c-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="5122c-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="5122c-198">TestDimValue</span></span>  

 <span data-ttu-id="5122c-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="5122c-199">TestNewDimValue</span></span>  

 <span data-ttu-id="5122c-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="5122c-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="5122c-201">(Eyða vegna þessa að taflan ItemBudgetDim er eytt.)</span><span class="sxs-lookup"><span data-stu-id="5122c-201">(Delete because the ItemBudgetDim Table is deleted.)</span></span>  

 <span data-ttu-id="5122c-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="5122c-202">GetServContractDim</span></span>  

 <span data-ttu-id="5122c-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="5122c-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="5122c-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="5122c-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="5122c-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="5122c-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="5122c-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="5122c-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="5122c-207">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5122c-207">See Also</span></span>
 <span data-ttu-id="5122c-208">[Hönnunarupplýsingarn: Færslur víddarsamstæða](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="5122c-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="5122c-209">[Hönnunarupplýsingar - Færslur víddarsamstæða yfirlit](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="5122c-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="5122c-210">[Hönnunarupplýsingar Leitað að víddarsamsetningum](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="5122c-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 <span data-ttu-id="5122c-211">[Hönnunarupplýsingar töfluuppbygging](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="5122c-211">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 [<span data-ttu-id="5122c-212">Hönnunarupplýsingar: Kóðadæmi um breytt mynstur í Breytingar</span><span class="sxs-lookup"><span data-stu-id="5122c-212">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

