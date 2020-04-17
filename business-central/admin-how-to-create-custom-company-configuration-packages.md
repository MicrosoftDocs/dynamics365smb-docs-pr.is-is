---
title: Hvernig á að búa til sérstillta grunnstillingarpakka fyrirtækja | Microsoft Docs
description: Eftir því sem fyrirtækið vex, er líklegt að treyst verði á safn fyrirtækjategunda sem verður notað með flestum af viðskiptamönnum fyrirtækisins. Hægt er að auðvelda innleiðingarferlið með því að breyta þessum tegundum í grunnstillingarpakka fyrir fyrirtæki sem hægt er að nota aftur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 8bbd9b07976dc4d54f8bee9f5eb8c23270c5a10c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187173"
---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="8cb2a-104">Búa til sérstillta grunnstillingarpakka fyrirtækja</span><span class="sxs-lookup"><span data-stu-id="8cb2a-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="8cb2a-105">Eftir því sem fyrirtækið vex, er líklegt að treyst verði á safn fyrirtækjategunda sem verður notað með flestum af viðskiptamönnum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="8cb2a-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="8cb2a-106">Hægt er að auðvelda innleiðingarferlið með því að breyta þessum tegundum í grunnstillingarpakka fyrir fyrirtæki sem hægt er að nota aftur.</span><span class="sxs-lookup"><span data-stu-id="8cb2a-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="8cb2a-107">Almennt eru grunnstillingarpakkar stofnaðir fyrir hverja virkni, s.s. framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="8cb2a-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="8cb2a-108">Það gerir þér kleift að nota og setja upp ný svæði í fyrirtæki eftir þörfum</span><span class="sxs-lookup"><span data-stu-id="8cb2a-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="8cb2a-109">Önnur nálgun væri að stofna sendingu sem inniheldur töflur sem skilgreina uppsetningu, s. s. eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="8cb2a-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="8cb2a-110">Eignagrunnur</span><span class="sxs-lookup"><span data-stu-id="8cb2a-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="8cb2a-111">Uppsetning fjárhags</span><span class="sxs-lookup"><span data-stu-id="8cb2a-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="8cb2a-112">Birgðagrunnur</span><span class="sxs-lookup"><span data-stu-id="8cb2a-112">Inventory Setup</span></span>  
-   <span data-ttu-id="8cb2a-113">Framleiðslugrunnur</span><span class="sxs-lookup"><span data-stu-id="8cb2a-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="8cb2a-114">Innkaupagrunnur</span><span class="sxs-lookup"><span data-stu-id="8cb2a-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="8cb2a-115">Tengslastjórnunargrunnur</span><span class="sxs-lookup"><span data-stu-id="8cb2a-115">Marketing Setup</span></span>  
-   <span data-ttu-id="8cb2a-116">Þjónustukerfisgrunnur</span><span class="sxs-lookup"><span data-stu-id="8cb2a-116">Service Setup</span></span>  
-   <span data-ttu-id="8cb2a-117">Sölugrunnur</span><span class="sxs-lookup"><span data-stu-id="8cb2a-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="8cb2a-118">Vöruhúsagrunnur</span><span class="sxs-lookup"><span data-stu-id="8cb2a-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="8cb2a-119">Alm. bókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="8cb2a-119">General Posting Setup</span></span>  
-   <span data-ttu-id="8cb2a-120">VSK-bókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="8cb2a-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="8cb2a-121">Birgðabókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="8cb2a-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="8cb2a-122">Til að sjá heildarlista yfir uppsetningartöflur skaltu velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Handvirk uppsetning** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="8cb2a-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="8cb2a-123">Til að búa til sérstilltan grunnstillingarpakka fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="8cb2a-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="8cb2a-124">Búa til nýtt fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="8cb2a-124">Create a new company.</span></span> <span data-ttu-id="8cb2a-125">Frekari upplýsingar eru í [Stofna ný fyrirtæki í Business Central](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="8cb2a-125">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="8cb2a-126">Setjið upp nýja fyrirtækið á þann hátt sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="8cb2a-126">Set up the new company in the way you need.</span></span> <span data-ttu-id="8cb2a-127">Fylla út allar nauðsynlegar töflur.</span><span class="sxs-lookup"><span data-stu-id="8cb2a-127">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="8cb2a-128">Opna skal nýja fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="8cb2a-128">Open the new company.</span></span>
5. <span data-ttu-id="8cb2a-129">Opna skal síðun **Skilgreiningarvinnublað**.</span><span class="sxs-lookup"><span data-stu-id="8cb2a-129">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="8cb2a-130">Bæta töflunum sem óskað er eftir að færa á annað fyrirtæki við vinnublaðið.</span><span class="sxs-lookup"><span data-stu-id="8cb2a-130">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="8cb2a-131">Úthluta vinnublaðslínunum til pakkans.</span><span class="sxs-lookup"><span data-stu-id="8cb2a-131">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="8cb2a-132">Stofna spurningalista fyrir mest notuðu uppsetningartöflurnar.</span><span class="sxs-lookup"><span data-stu-id="8cb2a-132">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="8cb2a-133">Stofna skilgreiningarsniðmát til að auðvelda stofnun aðalgagna, svo sem viðskiptavini eða vöru.</span><span class="sxs-lookup"><span data-stu-id="8cb2a-133">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="8cb2a-134">Flytja út pakka notanda sem rapidstart-skrá.</span><span class="sxs-lookup"><span data-stu-id="8cb2a-134">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8cb2a-135">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="8cb2a-135">See Also</span></span>  
[<span data-ttu-id="8cb2a-136">Uppsetning fyrirtækis með RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="8cb2a-136">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="8cb2a-137">Stjórnun</span><span class="sxs-lookup"><span data-stu-id="8cb2a-137">Administration</span></span>](admin-setup-and-administration.md)
