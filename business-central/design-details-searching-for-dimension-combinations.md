---
title: Hönnunarupplýsingar - Leitað að víddarsamsetningum | Microsoft Docs
description: Þegar þú lokar síðu eftir að hafa breytt víddasamstæðu metur Business Central hvort þessi breytta víddasamstæða sé til. Ef samstæðan er ekki til er ný samstæða búin til og víddarsamsetningarkenninu er skilað.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c3867c45f659f054a3bdee1605f2d8541e72dec1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751131"
---
# <a name="design-details-searching-for-dimension-combinations"></a><span data-ttu-id="5b6f9-104">Hönnunarupplýsingar Leitað að víddarsamsetningum</span><span class="sxs-lookup"><span data-stu-id="5b6f9-104">Design Details: Searching for Dimension Combinations</span></span>
<span data-ttu-id="5b6f9-105">Þegar þú lokar síðu eftir að hafa breytt víddasamstæðu metur [!INCLUDE[prod_short](includes/prod_short.md)] hvort þessi breytta víddasamstæða sé til.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-105">When you close a page after you edit a set of dimensions, [!INCLUDE[prod_short](includes/prod_short.md)] evaluates whether the edited set of dimensions exists.</span></span> <span data-ttu-id="5b6f9-106">Ef samstæðan er ekki til er ný samstæða búin til og víddarsamsetningarkenninu er skilað.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-106">If the set does not exist, a new set is created and the dimension combination ID is returned.</span></span>  

## <a name="building-search-tree"></a><span data-ttu-id="5b6f9-107">Byggir leitartré</span><span class="sxs-lookup"><span data-stu-id="5b6f9-107">Building Search Tree</span></span>  
 <span data-ttu-id="5b6f9-108">Tafla 481 **Víddasamstæðutrjáhnútu** er notað þegar [!INCLUDE[prod_short](includes/prod_short.md)] metur hvort víddasamstæðamál er þegar til í töflu 480 **Víddasamstæðufærsla**.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-108">Table 481 **Dimension Set Tree Node** is used when [!INCLUDE[prod_short](includes/prod_short.md)] evaluates whether a set of dimensions already exists in table 480 **Dimension Set Entry** table.</span></span> <span data-ttu-id="5b6f9-109">Matið er framkvæmt með því fara yfir leitartré frá efsta stig 0.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-109">The evaluation is performed by recursively traversing the search tree starting at the top level numbered 0.</span></span> <span data-ttu-id="5b6f9-110">Efsta stig 0 táknar víddasamstæðu án víddasamstæðufærslna.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-110">The top level 0 represents a dimension set with no dimension set entries.</span></span> <span data-ttu-id="5b6f9-111">Undireiningar þessarar víddasamstæðu tákna víddasamstæður með einni víddasamstæðufærslu.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-111">The children of this dimension set represent dimension sets with only one dimension set entry.</span></span> <span data-ttu-id="5b6f9-112">Undireiningar þessara víddasamstæða standa fyrir tvær undireiningar og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-112">The children of these dimension sets represent dimension sets with two children, and so on.</span></span>  

### <a name="example-1"></a><span data-ttu-id="5b6f9-113">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="5b6f9-113">Example 1</span></span>  
 <span data-ttu-id="5b6f9-114">Eftirfarandi skýringarmynd leitartré með sex víddasamstæðum.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-114">The following diagram represents a search tree with six dimension sets.</span></span> <span data-ttu-id="5b6f9-115">Aðeins eru einkennandi víddasamstæðufærslur sýndar á myndinni.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-115">Only the distinguishing dimension set entry is displayed in the diagram.</span></span>  

 <span data-ttu-id="5b6f9-116">![Dæmi um víddartrjáskipulag](media/nav2013_dimension_tree.png "Dæmi um trjáskipulag víddar")</span><span class="sxs-lookup"><span data-stu-id="5b6f9-116">![Example of dimension tree structure](media/nav2013_dimension_tree.png "Example of dimension tree structure")</span></span>  

 <span data-ttu-id="5b6f9-117">Eftirfarandi tafla lýsir a fullgerðum lista víddasamstæðufærsla sem mynda hverja víddasamstæðu.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-117">The following table describes a complete list of dimension set entries that make up each dimension set.</span></span>  

|<span data-ttu-id="5b6f9-118">Víddasamstæður</span><span class="sxs-lookup"><span data-stu-id="5b6f9-118">Dimension Sets</span></span>|<span data-ttu-id="5b6f9-119">Víddasamstæðufærslur</span><span class="sxs-lookup"><span data-stu-id="5b6f9-119">Dimension Set Entries</span></span>|  
|--------------------|---------------------------|  
|<span data-ttu-id="5b6f9-120">Sett 0</span><span class="sxs-lookup"><span data-stu-id="5b6f9-120">Set 0</span></span>|<span data-ttu-id="5b6f9-121">Ekkert</span><span class="sxs-lookup"><span data-stu-id="5b6f9-121">None</span></span>|  
|<span data-ttu-id="5b6f9-122">Sett 1</span><span class="sxs-lookup"><span data-stu-id="5b6f9-122">Set 1</span></span>|<span data-ttu-id="5b6f9-123">AREA 30</span><span class="sxs-lookup"><span data-stu-id="5b6f9-123">AREA 30</span></span>|  
|<span data-ttu-id="5b6f9-124">Sett 2</span><span class="sxs-lookup"><span data-stu-id="5b6f9-124">Set 2</span></span>|<span data-ttu-id="5b6f9-125">AREA 30, DEPT ADM</span><span class="sxs-lookup"><span data-stu-id="5b6f9-125">AREA 30, DEPT ADM</span></span>|  
|<span data-ttu-id="5b6f9-126">Sett 3</span><span class="sxs-lookup"><span data-stu-id="5b6f9-126">Set 3</span></span>|<span data-ttu-id="5b6f9-127">AREA 30, DEPT PROD</span><span class="sxs-lookup"><span data-stu-id="5b6f9-127">AREA 30, DEPT PROD</span></span>|  
|<span data-ttu-id="5b6f9-128">Sett 4</span><span class="sxs-lookup"><span data-stu-id="5b6f9-128">Set 4</span></span>|<span data-ttu-id="5b6f9-129">AREA 30, DEPT ADM, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="5b6f9-129">AREA 30, DEPT ADM, PROJ VW</span></span>|  
|<span data-ttu-id="5b6f9-130">Sett 5</span><span class="sxs-lookup"><span data-stu-id="5b6f9-130">Set 5</span></span>|<span data-ttu-id="5b6f9-131">AREA 40</span><span class="sxs-lookup"><span data-stu-id="5b6f9-131">AREA 40</span></span>|  
|<span data-ttu-id="5b6f9-132">Sett 6</span><span class="sxs-lookup"><span data-stu-id="5b6f9-132">Set 6</span></span>|<span data-ttu-id="5b6f9-133">AREA 40, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="5b6f9-133">AREA 40, PROJ VW</span></span>|  

### <a name="example-2"></a><span data-ttu-id="5b6f9-134">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="5b6f9-134">Example 2</span></span>  
 <span data-ttu-id="5b6f9-135">Þetta dæmi sýnir hvernig [!INCLUDE[prod_short](includes/prod_short.md)] metur hvort víddarsamstæða sem samanstendur af færslum AREA 40, DEPT PROD sé til.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-135">This example shows how [!INCLUDE[prod_short](includes/prod_short.md)] evaluates whether a dimension set that consists of the dimension set entries AREA 40, DEPT PROD exists.</span></span>  

 <span data-ttu-id="5b6f9-136">Fyrst mun [!INCLUDE[prod_short](includes/prod_short.md)] einnig uppfæra töfluna **Trjáhnútur víddasamstæðu** til að tryggja að leitartréð líti eins út og eftirfarandi teikning.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-136">First, [!INCLUDE[prod_short](includes/prod_short.md)] also updates the **Dimension Set Tree Node** table to make sure that the search tree looks like the following diagram.</span></span> <span data-ttu-id="5b6f9-137">Því verður víddasamstæða 7 undireining víddasamstæðu 5.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-137">Thus dimension set 7 becomes a child of the dimension set 5.</span></span>  

 <span data-ttu-id="5b6f9-138">![Dæmi um  trjáskipulag víddar í NAV 2013](media/nav2013_dimension_tree_example2.png "Dæmi um  trjáskipulag víddar í NAV 2013")</span><span class="sxs-lookup"><span data-stu-id="5b6f9-138">![Example of dimension tree structure in NAV 2013](media/nav2013_dimension_tree_example2.png "Example of dimension tree structure in NAV 2013")</span></span>  

### <a name="finding-dimension-set-id"></a><span data-ttu-id="5b6f9-139">Finna auðkenni víddasamstæðu</span><span class="sxs-lookup"><span data-stu-id="5b6f9-139">Finding Dimension Set ID</span></span>  
 <span data-ttu-id="5b6f9-140">Á hugmyndastigi eru **Yfireining**, **Vídd og** **Víddargildi** í leitartrénu sameinuð og notuð sem aðallykill vegna þess að [!INCLUDE[prod_short](includes/prod_short.md)] fer yfir tréð á sama hátt og víddarfærslurnar.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-140">At a conceptual level, **Parent ID**, **Dimension**, and **Dimension Value**, in the search tree, are combined and used as the primary key because [!INCLUDE[prod_short](includes/prod_short.md)] traverses the tree in the same order as the dimension entries.</span></span> <span data-ttu-id="5b6f9-141">GET-eiginleikinn (skrá) er notaður til að leita að auðkenni víddasamstæðu.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-141">The GET function (record) is used to search for dimension set ID.</span></span> <span data-ttu-id="5b6f9-142">Eftirfarandi kóðadæmi sýnir hvernig á að finna auðkenni víddasamstæðu þegar það eru víddagildi eru þrjú.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-142">The following code example shows how to find the dimension set ID when there are three dimension values.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

<span data-ttu-id="5b6f9-143">Hins vegar, til að varðveita getu [!INCLUDE[prod_short](includes/prod_short.md)] til að endurnefna bæði vídd og víddargildi, er aukið við töflu 349 **Víddargildi** með heiltölureitnum **Víddargildiskenni**.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-143">However, to preserve the ability of [!INCLUDE[prod_short](includes/prod_short.md)] to rename both a dimension and a dimension value, table 349, **Dimension Value**, is extended with an integer field, **Dimension Value ID**.</span></span> <span data-ttu-id="5b6f9-144">Taflan breytir reitaparinu **Vídd** og **Víddargildi** í heiltölu gildi.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-144">This table converts the field pair, **Dimension** and **Dimension Value**, to an integer value.</span></span> <span data-ttu-id="5b6f9-145">Þegar þú endurnefnir víddir og víddargildi er gilum í heilum tölum ekki breytt.</span><span class="sxs-lookup"><span data-stu-id="5b6f9-145">When you rename the dimension and dimension value, the integer value is not changed.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a><span data-ttu-id="5b6f9-146">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5b6f9-146">See Also</span></span>  
 <span data-ttu-id="5b6f9-147">[GET Eiginleiki (Skrá)](/dynamics-nav/GET-Function--Record-)  </span><span class="sxs-lookup"><span data-stu-id="5b6f9-147">[GET Function (Record)](/dynamics-nav/GET-Function--Record-)  </span></span>  
 <span data-ttu-id="5b6f9-148">[Hönnunarupplýsingarn: Færslur víddarsamstæða](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="5b6f9-148">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="5b6f9-149">[Yfirlit yfir víddasamstæðufærslur](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="5b6f9-149">[Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 [<span data-ttu-id="5b6f9-150">Hönnunarupplýsingar töfluuppbygging</span><span class="sxs-lookup"><span data-stu-id="5b6f9-150">Design Details: Table Structure</span></span>](design-details-table-structure.md)   
 
