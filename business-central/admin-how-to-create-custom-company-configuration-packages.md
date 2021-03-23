---
title: Hvernig á að búa til sérstillta grunnstillingarpakka fyrirtækja | Microsoft Docs
description: Eftir því sem fyrirtækið vex, er líklegt að treyst verði á safn fyrirtækjategunda sem verður notað með flestum af viðskiptamönnum fyrirtækisins. Hægt er að auðvelda innleiðingarferlið með því að breyta þessum tegundum í grunnstillingarpakka fyrir fyrirtæki sem hægt er að nota aftur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a1b1bfd5dd685eb57e291842d7b6d2e3691482fc
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378299"
---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="0992b-104">Búa til sérstillta grunnstillingarpakka fyrirtækja</span><span class="sxs-lookup"><span data-stu-id="0992b-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="0992b-105">Eftir því sem fyrirtækið vex, er líklegt að treyst verði á safn fyrirtækjategunda sem verður notað með flestum af viðskiptamönnum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="0992b-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="0992b-106">Hægt er að auðvelda innleiðingarferlið með því að breyta þessum tegundum í grunnstillingarpakka fyrir fyrirtæki sem hægt er að nota aftur.</span><span class="sxs-lookup"><span data-stu-id="0992b-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="0992b-107">Almennt eru grunnstillingarpakkar stofnaðir fyrir hverja virkni, s.s. framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="0992b-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="0992b-108">Það gerir þér kleift að nota og setja upp ný svæði í fyrirtæki eftir þörfum</span><span class="sxs-lookup"><span data-stu-id="0992b-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="0992b-109">Önnur nálgun væri að stofna sendingu sem inniheldur töflur sem skilgreina uppsetningu, s. s. eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="0992b-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="0992b-110">Eignagrunnur</span><span class="sxs-lookup"><span data-stu-id="0992b-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="0992b-111">Uppsetning fjárhags</span><span class="sxs-lookup"><span data-stu-id="0992b-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="0992b-112">Birgðagrunnur</span><span class="sxs-lookup"><span data-stu-id="0992b-112">Inventory Setup</span></span>  
-   <span data-ttu-id="0992b-113">Framleiðslugrunnur</span><span class="sxs-lookup"><span data-stu-id="0992b-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="0992b-114">Innkaupagrunnur</span><span class="sxs-lookup"><span data-stu-id="0992b-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="0992b-115">Tengslastjórnunargrunnur</span><span class="sxs-lookup"><span data-stu-id="0992b-115">Marketing Setup</span></span>  
-   <span data-ttu-id="0992b-116">Þjónustukerfisgrunnur</span><span class="sxs-lookup"><span data-stu-id="0992b-116">Service Setup</span></span>  
-   <span data-ttu-id="0992b-117">Sölugrunnur</span><span class="sxs-lookup"><span data-stu-id="0992b-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="0992b-118">Vöruhúsagrunnur</span><span class="sxs-lookup"><span data-stu-id="0992b-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="0992b-119">Alm. bókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="0992b-119">General Posting Setup</span></span>  
-   <span data-ttu-id="0992b-120">VSK-bókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="0992b-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="0992b-121">Birgðabókunargrunnur</span><span class="sxs-lookup"><span data-stu-id="0992b-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="0992b-122">Til að sjá heildarlista yfir uppsetningartöflur skaltu velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Handvirk uppsetning** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="0992b-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="0992b-123">Farðu varlega ef þú velur töflur eða reiti sem hafa sama tímabundna heitið en eru aðgreind með sérstöfum, t.d. %, &, <, >, (, og ).</span><span class="sxs-lookup"><span data-stu-id="0992b-123">Use caution if you choose tables or fields that have the same temporal name but are differentiated by special characters, such as %, &, <, >, (, and ).</span></span> <span data-ttu-id="0992b-124">Til dæmis getur taflan "XYZ" innihaldið reitina „Svæði 1“ og „Svæði 1%“.</span><span class="sxs-lookup"><span data-stu-id="0992b-124">For example, table "XYZ" might contain the "Field 1" and "Field 1%" fields.</span></span>
>
> <span data-ttu-id="0992b-125">XML-úrvinnslan samþykkir aðeins suma sérstafi og fjarlægir þá sem hún samþykkir ekki.</span><span class="sxs-lookup"><span data-stu-id="0992b-125">The XML processor accepts only some special characters, and will remove those it does not.</span></span> <span data-ttu-id="0992b-126">Ef sértákn á borð við %-merkið í „Svæði 1%“ er fjarlægt, verða til tvær eða fleiri töflur eða reitir með sama heitinu og villa kemur upp þegar grunnstillingapakki er fluttur út eða inn.</span><span class="sxs-lookup"><span data-stu-id="0992b-126">If removing a special character, such as the % sign in "Field 1%," results in two or more tables or fields with the same name an error will occur when you export or import a configuration package.</span></span>

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="0992b-127">Til að búa til sérstilltan grunnstillingarpakka fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="0992b-127">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="0992b-128">Búa til nýtt fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="0992b-128">Create a new company.</span></span> <span data-ttu-id="0992b-129">Frekari upplýsingar eru í [Stofna ný fyrirtæki í Business Central](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="0992b-129">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="0992b-130">Setjið upp nýja fyrirtækið á þann hátt sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="0992b-130">Set up the new company in the way you need.</span></span> <span data-ttu-id="0992b-131">Fylla út allar nauðsynlegar töflur.</span><span class="sxs-lookup"><span data-stu-id="0992b-131">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="0992b-132">Opna skal nýja fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="0992b-132">Open the new company.</span></span>
5. <span data-ttu-id="0992b-133">Opna skal síðun **Skilgreiningarvinnublað**.</span><span class="sxs-lookup"><span data-stu-id="0992b-133">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="0992b-134">Bæta töflunum sem óskað er eftir að færa á annað fyrirtæki við vinnublaðið.</span><span class="sxs-lookup"><span data-stu-id="0992b-134">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="0992b-135">Úthluta vinnublaðslínunum til pakkans.</span><span class="sxs-lookup"><span data-stu-id="0992b-135">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="0992b-136">Stofna spurningalista fyrir mest notuðu uppsetningartöflurnar.</span><span class="sxs-lookup"><span data-stu-id="0992b-136">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="0992b-137">Stofna skilgreiningarsniðmát til að auðvelda stofnun aðalgagna, svo sem viðskiptavini eða vöru.</span><span class="sxs-lookup"><span data-stu-id="0992b-137">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="0992b-138">Flytja út pakka notanda sem rapidstart-skrá.</span><span class="sxs-lookup"><span data-stu-id="0992b-138">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0992b-139">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0992b-139">See Also</span></span>  
[<span data-ttu-id="0992b-140">Uppsetning fyrirtækis með RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="0992b-140">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="0992b-141">Stjórnun</span><span class="sxs-lookup"><span data-stu-id="0992b-141">Administration</span></span>](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]