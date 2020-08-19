---
title: Hvernig á að búa til opnunarstöður færslubóka | Microsoft Docs
description: Business Central inniheldur margar keyrslur sem fylgja til aðstoðar við flutningi á gömlum reikningstöðum til nýlega grunnstillts fyrirtækis. Auðvelt er að flytja þessi gögn með færslubókunum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/14/2020
ms.author: sgroespe
ms.openlocfilehash: 5360b3a8a72387cda8d0e640562a118ca1f20ff4
ms.sourcegitcommit: 89d0ea903f61ab0628f99329c762d9f1619c49a7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/14/2020
ms.locfileid: "3577127"
---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="1fdb1-104">Stofna opnunarstöður færslubókar</span><span class="sxs-lookup"><span data-stu-id="1fdb1-104">Create Journal Opening Balances</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="1fdb1-105">inniheldur margar keyrslur sem fylgja til aðstoðar við flutningi á gömlum reikningstöðum til nýlega grunnstillts fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-105">includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="1fdb1-106">Auðvelt er að flytja þessi gögn með færslubók viðskiptavinar, færslubók lánardrottins, birgðabókinni og fjárhagsbók.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="1fdb1-107">Fyrsta skrefið er að stofna grunnstillingarpakka sem inniheldur uppsetningartöflurnar fyrir þessar færslubækur.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="1fdb1-108">Eftirfarandi aðferð gerir ráð fyrir því að þessu skrefi sé lokið.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="1fdb1-109">Frekari upplýsingar eru í [Setja upp grunnstillingu fyrirtækis](admin-set-up-company-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="1fdb1-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="1fdb1-110">Ferlið lýsir næstu skrefum, en í þeim felst að nota pakkann sem samstarfsaðili veitir.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="1fdb1-111">Áður en hafist er handa þarf að ganga úr skugga um að notandi sé á hlutverkasíðu stjórnunar því hún býður upp á rétt samhengi fyrir grunnstillingarvinnuna.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-111">Before you start, make sure that you are using the Administration Role Center page because it provides the correct context for your configuration work.</span></span> <span data-ttu-id="1fdb1-112">Frekari upplýsingar eru í [Breyta grundvallarstillingum](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="1fdb1-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="1fdb1-113">Til að jafna færslurnar í færslubók við nýtt fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="1fdb1-113">To apply the entries in a journal to a new company</span></span>

1. <span data-ttu-id="1fdb1-114">Grunnstilla nýtt fyrirtæki og nota grunnstillingarpakka í því.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="1fdb1-115">Frekari upplýsingar eru í [Grunnstilla fyrirtæki með RapidStart-leiðsagnarforriti](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="1fdb1-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="1fdb1-116">Nýja fyrirtækið inniheldur ekki upplýsingar um opnunarstöður færslubóka.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="1fdb1-117">Opna grunnstillingarvinnublaðið og flytja inn fyrirliggjandi gögn um viðskiptavini, vörur, lánardrottna og fjárhag.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="1fdb1-118">Frekari upplýsingar eru í [Yfirfæra gögn viðskiptamanns](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="1fdb1-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  

    <span data-ttu-id="1fdb1-119">Nú ertu með aðalgögn á sínum stað.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-119">Now you have master data in place.</span></span> <span data-ttu-id="1fdb1-120">Næst skal bæta við opnunarstöðum.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-120">Next, you add the opening balances.</span></span> <span data-ttu-id="1fdb1-121">Eftirfarandi skref lýsa því hvernig á að stofna færslubókarlínur fyrir fjárhagsreikninga, en það sama gildir um stofnun færslubókarlína fyrir viðskiptamenn, lánardrottna og vörur.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-121">The following steps describe how to create journal lines for G/L accounts, but the same apply to creating journal lines for customers, vendors, and items.</span></span>  
3. <span data-ttu-id="1fdb1-122">Velja skal aðgerðina **Stofna fjárhagsbókarlínur fjárhagsreiknings**.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-122">Choose the **Create G/L Acct. Journal Lines** action.</span></span>  
4. <span data-ttu-id="1fdb1-123">Fylla inn í flýtiflipann **Valkostir** þar sem við á, og setja afmarkanir eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-123">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="1fdb1-124">Til dæmis í reitinn **Bókarsniðmát** er fært inn heiti.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-124">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="1fdb1-125">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-125">Choose the **OK** button.</span></span> <span data-ttu-id="1fdb1-126">Færslurnar eru nú í færslubók, en upphæðirnar eru auður.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-126">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="1fdb1-127">Flytja út færslubókartöflua í Excel og færa handvirkt inn upplýsingar um bókunina og mótreikninginn úr gömlum gögnum.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-127">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="1fdb1-128">Flytja inn og nota töfluupplýsingar í nýja fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-128">Import and apply the table information into the new company.</span></span> <span data-ttu-id="1fdb1-129">Færslubókarlínurnar eru tilbúnar til bókunar.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-129">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="1fdb1-130">Á grunnstillingarvinnublaðinu skal velja töflu færslubókarlínu og síðan velja aðgerðina **Gagnagrunnsgögn**.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-130">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="1fdb1-131">Yfirfara skal upplýsingarnar og síðan velja aðgerðina **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-131">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="1fdb1-132">Endurtaka skal skrefin til að flytja inn og bóka aðrar opnunarstöður.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-132">Repeat the steps to import and post any other opening balances.</span></span>  

> [!TIP]
> <span data-ttu-id="1fdb1-133">Hægt er að nota sömu runuvinnslur til að bæta við opnunarstöðum í hvert sinn sem nýr viðskiptamaður eða lánardrottinn sem þú hefur stundað viðskipti með áður en er ekki skráður í [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="1fdb1-133">You can use the same batch jobs to add opening balances whenever you register a new customer or vendor that you have done business with before but not registered in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="1fdb1-134">Leitið einfaldlega að viðkomandi verki og veljið síðan viðkomandi tengil.</span><span class="sxs-lookup"><span data-stu-id="1fdb1-134">Just search for the relevant task, and then choose the relevant link.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fdb1-135">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1fdb1-135">See Also</span></span>

[<span data-ttu-id="1fdb1-136">Nota skilgreiningu á ný fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="1fdb1-136">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="1fdb1-137">Uppsetning fyrirtækis með RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="1fdb1-137">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="1fdb1-138">Stjórnun</span><span class="sxs-lookup"><span data-stu-id="1fdb1-138">Administration</span></span>](admin-setup-and-administration.md)  
