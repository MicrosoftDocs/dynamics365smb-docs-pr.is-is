---
title: "Hönnunarupplýsingar - Kóðaeining 408 víddarstjórnun | Microsoft Docs"
description: "Kóðaeining 408 Víddastjórnun er aðgerðasafn sem sér um algeng verkefni sem tengjast víddum, m.a. afritun úr einni töflu í aðra eða úr einu skjali í annað."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 32f67c058570f03d4aa1c84d9bb32289b1f07bec
ms.contentlocale: is-is
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="4e1b4-103">Hönnunarupplýsingar: Codeunit 408 víddarstjórnun</span><span class="sxs-lookup"><span data-stu-id="4e1b4-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="4e1b4-104">Kóðaeining 408 Víddastjórnun er aðgerðasafn sem sér um algeng verkefni sem tengjast víddum, m.a. afritun úr einni töflu í aðra eða úr einu skjali í annað.</span><span class="sxs-lookup"><span data-stu-id="4e1b4-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="4e1b4-105">Þetta efnisatriði er listi yfir aðgerðir sem er breytt í Microsoft Dynamics NAV 2013 R2 og skilgreinir hvað þarf að gera við aðgerðirnar.</span><span class="sxs-lookup"><span data-stu-id="4e1b4-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="4e1b4-106">Mörgum aðgerðum er eytt vegna þess að ekki er þörf á að afrita á milli víddatafla.</span><span class="sxs-lookup"><span data-stu-id="4e1b4-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="4e1b4-107">Breyttar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="4e1b4-107">Modified Functions</span></span>  

|<span data-ttu-id="4e1b4-108">Heiti aðgerðar</span><span class="sxs-lookup"><span data-stu-id="4e1b4-108">Function Name</span></span>|<span data-ttu-id="4e1b4-109">Lýsing á breytingum</span><span class="sxs-lookup"><span data-stu-id="4e1b4-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="4e1b4-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="4e1b4-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="4e1b4-111">Ný aðgerð sem kemur í stað annarra skoðunaraðgerða og notar víddasamstæðukenni sem frumbreytu í stað víddatöflu.</span><span class="sxs-lookup"><span data-stu-id="4e1b4-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="4e1b4-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="4e1b4-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="4e1b4-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="4e1b4-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="4e1b4-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="4e1b4-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="4e1b4-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="4e1b4-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="4e1b4-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="4e1b4-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="4e1b4-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="4e1b4-117">CheckDimValueComb</span></span>|<span data-ttu-id="4e1b4-118">Eyða</span><span class="sxs-lookup"><span data-stu-id="4e1b4-118">Delete.</span></span> <span data-ttu-id="4e1b4-119">Allri notkun ætti að breyta í CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="4e1b4-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="4e1b4-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-120">GetDefaultDim</span></span>|<span data-ttu-id="4e1b4-121">Breytið til að skila víddasamstæðukenni í heiltölu í stað færslusafns.</span><span class="sxs-lookup"><span data-stu-id="4e1b4-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="4e1b4-122">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="4e1b4-123">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="4e1b4-124">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="4e1b4-125">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="4e1b4-126">Bryeta til að vinna með DimSetID -> ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="4e1b4-127">Eyddar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="4e1b4-127">Deleted Functions</span></span>  
 <span data-ttu-id="4e1b4-128">Aðgerðum sem er eytt út úr kóðaeiningu 408 í tengslum við eiginleikann víddasamstæðufærslur eru skráðar hér fyrir neðan.</span><span class="sxs-lookup"><span data-stu-id="4e1b4-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="4e1b4-129">Meðan á uppfærsla á forritakóðanum úr Microsoft Dynamics NAV 2009 eða fyrri útgáfum yfir í Microsoft Dynamics NAV 2016 eru eftirfarandi aðgerðir ekki tiltækar í Microsoft Dynamics NAV 2016.</span><span class="sxs-lookup"><span data-stu-id="4e1b4-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="4e1b4-130">Ef þú ert með sérstillingar sem nota einn eða fleiri aðgerðir verður að uppfæra kóðann í samræmi við það.</span><span class="sxs-lookup"><span data-stu-id="4e1b4-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="4e1b4-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="4e1b4-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="4e1b4-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="4e1b4-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="4e1b4-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="4e1b4-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-136">InsertDocDim</span></span>  

 <span data-ttu-id="4e1b4-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="4e1b4-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="4e1b4-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="4e1b4-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="4e1b4-141">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-141">InsertServContractDim</span></span>  

 <span data-ttu-id="4e1b4-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="4e1b4-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="4e1b4-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="4e1b4-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-144">GetDocDim</span></span>  

 <span data-ttu-id="4e1b4-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-145">GetProdDocDim</span></span>  

 <span data-ttu-id="4e1b4-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="4e1b4-146">TypeToTableID1</span></span>  

 <span data-ttu-id="4e1b4-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="4e1b4-147">TypeToTableID2</span></span>  

 <span data-ttu-id="4e1b4-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="4e1b4-148">TypeToTableID3</span></span>  

 <span data-ttu-id="4e1b4-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="4e1b4-149">TypeToTableID4</span></span>  

 <span data-ttu-id="4e1b4-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="4e1b4-150">TypeToTableID5</span></span>  

 <span data-ttu-id="4e1b4-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="4e1b4-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-152">DeleteDocDim</span></span>  

 <span data-ttu-id="4e1b4-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="4e1b4-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="4e1b4-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="4e1b4-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="4e1b4-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="4e1b4-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="4e1b4-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="4e1b4-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-160">ShowDocDim</span></span>  

 <span data-ttu-id="4e1b4-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-161">SaveDocDim</span></span>  

 <span data-ttu-id="4e1b4-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="4e1b4-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="4e1b4-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-164">ShowTempDim</span></span>  

 <span data-ttu-id="4e1b4-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-165">SaveTempDim</span></span>  

 <span data-ttu-id="4e1b4-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="4e1b4-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="4e1b4-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-168">SaveServContractDim</span></span>  

 <span data-ttu-id="4e1b4-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="4e1b4-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="4e1b4-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="4e1b4-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="4e1b4-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="4e1b4-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="4e1b4-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="4e1b4-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="4e1b4-177">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="4e1b4-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="4e1b4-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="4e1b4-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="4e1b4-181">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="4e1b4-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="4e1b4-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="4e1b4-184">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="4e1b4-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="4e1b4-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="4e1b4-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="4e1b4-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="4e1b4-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="4e1b4-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="4e1b4-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="4e1b4-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="4e1b4-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="4e1b4-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="4e1b4-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="4e1b4-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="4e1b4-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="4e1b4-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="4e1b4-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="4e1b4-198">TestDimValue</span></span>  

 <span data-ttu-id="4e1b4-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="4e1b4-199">TestNewDimValue</span></span>  

 <span data-ttu-id="4e1b4-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="4e1b4-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="4e1b4-201">(Eyða vegna þessa að taflan ItemBudgetDim er eytt.)</span><span class="sxs-lookup"><span data-stu-id="4e1b4-201">(Delete because the ItemBudgetDim Table is deleted.)</span></span>  

 <span data-ttu-id="4e1b4-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-202">GetServContractDim</span></span>  

 <span data-ttu-id="4e1b4-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="4e1b4-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="4e1b4-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="4e1b4-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="4e1b4-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="4e1b4-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="4e1b4-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="4e1b4-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="4e1b4-207">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4e1b4-207">See Also</span></span>
 <span data-ttu-id="4e1b4-208">[Hönnunarupplýsingarn: Færslur víddarsamstæða](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="4e1b4-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="4e1b4-209">[Hönnunarupplýsingar - Færslur víddarsamstæða yfirlit](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="4e1b4-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="4e1b4-210">[Hönnunarupplýsingar Leitað að víddarsamsetningum](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="4e1b4-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 <span data-ttu-id="4e1b4-211">[Hönnunarupplýsingar töfluuppbygging](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="4e1b4-211">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 [<span data-ttu-id="4e1b4-212">Hönnunarupplýsingar: Kóðadæmi um breytt mynstur í Breytingar</span><span class="sxs-lookup"><span data-stu-id="4e1b4-212">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

