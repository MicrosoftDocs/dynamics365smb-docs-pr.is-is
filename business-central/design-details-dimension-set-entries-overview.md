---
title: Yfirlit yfir víddasamstæðufærslur | Microsoft Docs
description: Í þessu efnisatriði er lýst hvernig víddasamstæðufærslur eru geymdar og bókaðar í Dynamics 365.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e03275c55290cccb2d8e91d7a934379184744a36
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788334"
---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="19db7-103">Yfirlit yfir víddasamstæðufærslur</span><span class="sxs-lookup"><span data-stu-id="19db7-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="19db7-104">Í þessu efnisatriði er lýst hvernig víddasamstæðufærslur eru geymdar og bókaðar í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="19db7-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="dimension-sets"></a><span data-ttu-id="19db7-105">Víddasamstæður</span><span class="sxs-lookup"><span data-stu-id="19db7-105">Dimension Sets</span></span>  
<span data-ttu-id="19db7-106">Víddasamstæða er sérstök samsetning víddargilda.</span><span class="sxs-lookup"><span data-stu-id="19db7-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="19db7-107">Er vistað sem víddasamstæðufærslur í gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="19db7-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="19db7-108">Hver víddasamstæðufærsla stendur fyrir eitt víddargildi.</span><span class="sxs-lookup"><span data-stu-id="19db7-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="19db7-109">Víddasamstæðan er auðkennd með algengum víddasamstæðukennum sem eru úthlutuð hverri víddasamstæðufærslu sem tilheyrir víddasamstæðunni.</span><span class="sxs-lookup"><span data-stu-id="19db7-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  

<span data-ttu-id="19db7-110">Eftirfarandi dæmi sýnir víddasamstæðu sem hefur þrjár víddasamstæðufærslur.</span><span class="sxs-lookup"><span data-stu-id="19db7-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="19db7-111">Víddasamstæðan er auðkennd með víddasamstæðukenni, sem er 108.</span><span class="sxs-lookup"><span data-stu-id="19db7-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  

|<span data-ttu-id="19db7-112">Auðkenni víddasamstæðu</span><span class="sxs-lookup"><span data-stu-id="19db7-112">Dimension Set ID</span></span>|<span data-ttu-id="19db7-113">Víddarkóti</span><span class="sxs-lookup"><span data-stu-id="19db7-113">Dimension Code</span></span>|<span data-ttu-id="19db7-114">Gildiskóti víddar</span><span class="sxs-lookup"><span data-stu-id="19db7-114">Dimension Value Code</span></span>|<span data-ttu-id="19db7-115">Nafn víddagildis</span><span class="sxs-lookup"><span data-stu-id="19db7-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="19db7-116">108</span><span class="sxs-lookup"><span data-stu-id="19db7-116">108</span></span>|<span data-ttu-id="19db7-117">SVÆÐI</span><span class="sxs-lookup"><span data-stu-id="19db7-117">AREA</span></span>|<span data-ttu-id="19db7-118">70</span><span class="sxs-lookup"><span data-stu-id="19db7-118">70</span></span>|<span data-ttu-id="19db7-119">Norður Ameríka</span><span class="sxs-lookup"><span data-stu-id="19db7-119">America North</span></span>|  
|<span data-ttu-id="19db7-120">108</span><span class="sxs-lookup"><span data-stu-id="19db7-120">108</span></span>|<span data-ttu-id="19db7-121">ATVGRHÓPUR</span><span class="sxs-lookup"><span data-stu-id="19db7-121">BUSINESSGROUP</span></span>|<span data-ttu-id="19db7-122">HOME</span><span class="sxs-lookup"><span data-stu-id="19db7-122">HOME</span></span>|<span data-ttu-id="19db7-123">Heimili</span><span class="sxs-lookup"><span data-stu-id="19db7-123">Home</span></span>|  
|<span data-ttu-id="19db7-124">108</span><span class="sxs-lookup"><span data-stu-id="19db7-124">108</span></span>|<span data-ttu-id="19db7-125">DEILD</span><span class="sxs-lookup"><span data-stu-id="19db7-125">DEPARTMENT</span></span>|<span data-ttu-id="19db7-126">SALA</span><span class="sxs-lookup"><span data-stu-id="19db7-126">SALES</span></span>|<span data-ttu-id="19db7-127">Sala</span><span class="sxs-lookup"><span data-stu-id="19db7-127">Sales</span></span>|  

## <a name="dimension-set-entries"></a><span data-ttu-id="19db7-128">Víddasamstæðufærslur</span><span class="sxs-lookup"><span data-stu-id="19db7-128">Dimension Set Entries</span></span>  
<span data-ttu-id="19db7-129">Víddasamstæður eru geymdar í töflunni **Víddasamstæðufærsla** sem víddasamstæðufærslur með sama víddasamstæðukenni.</span><span class="sxs-lookup"><span data-stu-id="19db7-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  

<span data-ttu-id="19db7-130">![Flæði víddasamstæðufærslna](media/dimensionentrynav7.png "Flæði víddasamstæðufærslna")</span><span class="sxs-lookup"><span data-stu-id="19db7-130">![Flow of dimension set entries](media/dimensionentrynav7.png "Flow of dimension set entries")</span></span>  

<span data-ttu-id="19db7-131">Þegar ný færslubókarlína, skjalahaus eða skjalalína er stofnuð er hægt að tilgreina samsetningu víddargilda.</span><span class="sxs-lookup"><span data-stu-id="19db7-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="19db7-132">Í stað þess að geyma hvert víddargildi í gagnagrunninum er kenni víddasamstæðu tengt færslubókarlínu, haus skjals eða línu skjals til að tilgreina víddasamstæðuna.</span><span class="sxs-lookup"><span data-stu-id="19db7-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  

<span data-ttu-id="19db7-133">Þegar síðunni **Breyta Víddasamstæðufærslum** er breytt og lokað er gerð athugun til að sjá hvort samsetning víddargildanna sé til sem víddasafn í töflunni.</span><span class="sxs-lookup"><span data-stu-id="19db7-133">When you edit and close the **Edit Dimension Set Entries** page, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="19db7-134">Ef samsetningin kemur fyrir í töflunni er samsvarandi víddasamstæðukenni tengt við færslubókarlínuna, fylgiskjalshausinn eða fylgiskjalslínuna.</span><span class="sxs-lookup"><span data-stu-id="19db7-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="19db7-135">Annars er nýrri víddasamstæðu bætt við töfluna og henni hennar bætt við línu færslubókar, haus fylgiskjals eða línu fylgiskjals.</span><span class="sxs-lookup"><span data-stu-id="19db7-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>

## <a name="codeunit-408-dimension-management"></a><span data-ttu-id="19db7-136">Codeunit 408 víddarstjórnun</span><span class="sxs-lookup"><span data-stu-id="19db7-136">Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="19db7-137">Codeunit 408, Víddastjórnun, er aðgerðasafn sem sér um algeng verkefni sem tengjast víddum, m.a. afritun úr einni töflu í aðra eða úr einu skjali í annað.</span><span class="sxs-lookup"><span data-stu-id="19db7-137">Codeunit 408, Dimension Management, is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span>

## <a name="performance-improvement"></a><span data-ttu-id="19db7-138">Bætt afköst</span><span class="sxs-lookup"><span data-stu-id="19db7-138">Performance Improvement</span></span>  
<span data-ttu-id="19db7-139">Með því að vista víddasamstæður einu sinni í gagnagrunni, er gagnagrunnsbilinu haldið við og heildarafköst eru bætt.</span><span class="sxs-lookup"><span data-stu-id="19db7-139">By storing dimension sets once in the database, database space is preserved and overall performance is improved.</span></span>  

## <a name="see-also"></a><span data-ttu-id="19db7-140">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="19db7-140">See Also</span></span>
<span data-ttu-id="19db7-141">[Hönnunarupplýsingar Leitað að víddarsamsetningum](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="19db7-141">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="19db7-142">[Hönnunarupplýsingar töfluuppbygging](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="19db7-142">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
[<span data-ttu-id="19db7-143">Hönnunarupplýsingar: Færslur víddarsamstæða</span><span class="sxs-lookup"><span data-stu-id="19db7-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
