---
title: Hvernig á að búa til opnunarstöður færslubóka | Microsoft Docs
description: Business Central inniheldur margar keyrslur sem fylgja til aðstoðar við flutningi á gömlum reikningstöðum til nýlega grunnstillts fyrirtækis. Auðvelt er að flytja þessi gögn með færslubókunum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9e1d936901f1a42991895c9e4b797a3238a24710
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378274"
---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="20267-104">Stofna opnunarstöður færslubókar</span><span class="sxs-lookup"><span data-stu-id="20267-104">Create Journal Opening Balances</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="20267-105">inniheldur margar keyrslur sem fylgja til aðstoðar við flutningi á gömlum reikningstöðum til nýlega grunnstillts fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="20267-105">includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="20267-106">Auðvelt er að flytja þessi gögn með færslubók viðskiptavinar, færslubók lánardrottins, birgðabókinni og fjárhagsbók.</span><span class="sxs-lookup"><span data-stu-id="20267-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="20267-107">Fyrsta skrefið er að stofna grunnstillingarpakka sem inniheldur uppsetningartöflurnar fyrir þessar færslubækur.</span><span class="sxs-lookup"><span data-stu-id="20267-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="20267-108">Eftirfarandi aðferð gerir ráð fyrir því að þessu skrefi sé lokið.</span><span class="sxs-lookup"><span data-stu-id="20267-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="20267-109">Frekari upplýsingar eru í [Setja upp grunnstillingu fyrirtækis](admin-set-up-company-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="20267-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="20267-110">Ferlið lýsir næstu skrefum, en í þeim felst að nota pakkann sem samstarfsaðili veitir.</span><span class="sxs-lookup"><span data-stu-id="20267-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="20267-111">Áður en hafist er handa þarf að ganga úr skugga um að notandi sé á hlutverkasíðu stjórnunar því hún býður upp á rétt samhengi fyrir grunnstillingarvinnuna.</span><span class="sxs-lookup"><span data-stu-id="20267-111">Before you start, make sure that you are using the Administration Role Center page because it provides the correct context for your configuration work.</span></span> <span data-ttu-id="20267-112">Frekari upplýsingar eru í [Breyta grundvallarstillingum](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="20267-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="20267-113">Til að jafna færslurnar í færslubók við nýtt fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="20267-113">To apply the entries in a journal to a new company</span></span>

1. <span data-ttu-id="20267-114">Grunnstilla nýtt fyrirtæki og nota grunnstillingarpakka í því.</span><span class="sxs-lookup"><span data-stu-id="20267-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="20267-115">Frekari upplýsingar eru í [Grunnstilla fyrirtæki með RapidStart-leiðsagnarforriti](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="20267-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="20267-116">Nýja fyrirtækið inniheldur ekki upplýsingar um opnunarstöður færslubóka.</span><span class="sxs-lookup"><span data-stu-id="20267-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="20267-117">Opna grunnstillingarvinnublaðið og flytja inn fyrirliggjandi gögn um viðskiptavini, vörur, lánardrottna og fjárhag.</span><span class="sxs-lookup"><span data-stu-id="20267-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="20267-118">Frekari upplýsingar eru í [Yfirfæra gögn viðskiptamanns](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="20267-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  

    <span data-ttu-id="20267-119">Nú ertu með aðalgögn á sínum stað.</span><span class="sxs-lookup"><span data-stu-id="20267-119">Now you have master data in place.</span></span> <span data-ttu-id="20267-120">Næst skal bæta við opnunarstöðum.</span><span class="sxs-lookup"><span data-stu-id="20267-120">Next, you add the opening balances.</span></span> <span data-ttu-id="20267-121">Eftirfarandi skref lýsa því hvernig á að stofna færslubókarlínur fyrir fjárhagsreikninga, en það sama gildir um stofnun færslubókarlína fyrir viðskiptamenn, lánardrottna og vörur.</span><span class="sxs-lookup"><span data-stu-id="20267-121">The following steps describe how to create journal lines for G/L accounts, but the same apply to creating journal lines for customers, vendors, and items.</span></span>  
3. <span data-ttu-id="20267-122">Velja skal aðgerðina **Stofna fjárhagsbókarlínur fjárhagsreiknings**.</span><span class="sxs-lookup"><span data-stu-id="20267-122">Choose the **Create G/L Acct. Journal Lines** action.</span></span>  
4. <span data-ttu-id="20267-123">Fylla inn í flýtiflipann **Valkostir** þar sem við á, og setja afmarkanir eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="20267-123">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="20267-124">Til dæmis í reitinn **Bókarsniðmát** er fært inn heiti.</span><span class="sxs-lookup"><span data-stu-id="20267-124">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="20267-125">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="20267-125">Choose the **OK** button.</span></span> <span data-ttu-id="20267-126">Færslurnar eru nú í færslubók, en upphæðirnar eru auður.</span><span class="sxs-lookup"><span data-stu-id="20267-126">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="20267-127">Flytja út færslubókartöflua í Excel og færa handvirkt inn upplýsingar um bókunina og mótreikninginn úr gömlum gögnum.</span><span class="sxs-lookup"><span data-stu-id="20267-127">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="20267-128">Flytja inn og nota töfluupplýsingar í nýja fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="20267-128">Import and apply the table information into the new company.</span></span> <span data-ttu-id="20267-129">Færslubókarlínurnar eru tilbúnar til bókunar.</span><span class="sxs-lookup"><span data-stu-id="20267-129">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="20267-130">Á grunnstillingarvinnublaðinu skal velja töflu færslubókarlínu og síðan velja aðgerðina **Gagnagrunnsgögn**.</span><span class="sxs-lookup"><span data-stu-id="20267-130">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="20267-131">Yfirfara skal upplýsingarnar og síðan velja aðgerðina **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="20267-131">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="20267-132">Endurtaka skal skrefin til að flytja inn og bóka aðrar opnunarstöður.</span><span class="sxs-lookup"><span data-stu-id="20267-132">Repeat the steps to import and post any other opening balances.</span></span>  

> [!TIP]
> <span data-ttu-id="20267-133">Hægt er að nota sömu runuvinnslur til að bæta við opnunarstöðum í hvert sinn sem nýr viðskiptamaður eða lánardrottinn sem þú hefur stundað viðskipti með áður en er ekki skráður í [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="20267-133">You can use the same batch jobs to add opening balances whenever you register a new customer or vendor that you have done business with before but not registered in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="20267-134">Leitið einfaldlega að viðkomandi verki og veljið síðan viðkomandi tengil.</span><span class="sxs-lookup"><span data-stu-id="20267-134">Just search for the relevant task, and then choose the relevant link.</span></span>

## <a name="see-also"></a><span data-ttu-id="20267-135">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="20267-135">See Also</span></span>

[<span data-ttu-id="20267-136">Nota skilgreiningu á ný fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="20267-136">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="20267-137">Uppsetning fyrirtækis með RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="20267-137">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="20267-138">Stjórnun</span><span class="sxs-lookup"><span data-stu-id="20267-138">Administration</span></span>](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]