---
title: Umsjón með ástæðu aðgangs að gagnagrunni í Business Central | Microsoft Docs
description: Breyta ástæðu aðgangs að gagnagrunni fyrir skýrslur, API-síður og fyrirspurnir.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 5fe04fc290f10324105d4d9ca01e13166bf2ad8f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773080"
---
# <a name="managing-database-access-intent"></a><span data-ttu-id="2094b-103">Umsjón með ástæðu aðgangs að gagnagrunni</span><span class="sxs-lookup"><span data-stu-id="2094b-103">Managing Database Access Intent</span></span> 

<span data-ttu-id="2094b-104">Sem yfirnotandi eða stjórnandi er hægt að breyta ástæðu aðgangs að gagnagrunni fyrir skýrslur, síður af API-gerð og fyrirspurnir til að auka afköst þjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="2094b-104">As a super user or administrator, you can change the database access intent on reports, pages of the type API, and queries to improve performance of the service.</span></span>

## <a name="overview"></a><span data-ttu-id="2094b-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="2094b-105">Overview</span></span>

<span data-ttu-id="2094b-106">Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að nota skrifvarðar eftirlíkingar af aðalgagnagrunninum (skrifa-lesa).</span><span class="sxs-lookup"><span data-stu-id="2094b-106">[!INCLUDE[prod_short](includes/prod_short.md)] can be set up to use read-only replicas of the primary (read-write) database.</span></span> <span data-ttu-id="2094b-107">Að nota eftirlíkingu gagnagrunns dregur úr álagi á aðalgagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="2094b-107">Using the database replica reduces the load on the primary database.</span></span> <span data-ttu-id="2094b-108">Í sumum tilfellum eykur það einnig afköst þegar gögn eru skoðuð í biðlaranum.</span><span class="sxs-lookup"><span data-stu-id="2094b-108">In some cases, it will also improve the performance when viewing data in the client.</span></span> <span data-ttu-id="2094b-109">Eftirlíkingar eru gagnlegar fyrir hluti á borð við skýrslur, fyrirspurnir og API-síður, sem eru notaðar til að skoða gögn eingöngu, ekki til að breyta gögnum.</span><span class="sxs-lookup"><span data-stu-id="2094b-109">Replicas are beneficial for objects, like reports, queries, and API pages, that are used for viewing data only, not modifying data.</span></span>

<span data-ttu-id="2094b-110">Þegar hlutirnir eru keyrðir er það ástæða aðgangs að gagnagrunni sem sker úr um hvort nota skuli skrifvarða eftirlíkingu ef hún er í boði eða aðalgagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="2094b-110">When objects run, the database access intent determines whether to use a read-only replica, if one is available, or the primary database.</span></span> <span data-ttu-id="2094b-111">Skýrslur, API-síður og fyrirspurnir eru þróaðar með fyrirframskilgreinda ástæðu fyrir aðgangi (sjá [Eiginleiki DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span><span class="sxs-lookup"><span data-stu-id="2094b-111">Reports, API pages, and queries are developed with a predefined database access intent (see [DatabaseAccessIntent property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span></span>

<span data-ttu-id="2094b-112">Síðan **Listi yfir ástæður fyrir aðgangi að gagnagrunni** gerir þér kleift að hnekkja fyrirframskilgreindri ástæðu fyrir aðgangi að gagnagrunni fyrir hluti þegar þeir eru keyrðir.</span><span class="sxs-lookup"><span data-stu-id="2094b-112">The **Database Access Intent List** page lets you override the predefined database access intent for objects when they're run.</span></span>

<span data-ttu-id="2094b-113">Í gagnagrunni er þessi eiginleiki þekktur sem *lesa útvíkkun*. Frekari upplýsingar um lesa útvíkkun og ástæðu fyrir aðgangi að gagnagrunni í [!INCLUDE[prod_short](includes/prod_short.md)] er að finna í [Nota lesa útvíkkun fyrir aukin afköst](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) í [!INCLUDE[prod_short](includes/prod_short.md)] Developer og IT Pro hjálp.</span><span class="sxs-lookup"><span data-stu-id="2094b-113">In database terms, this feature is commonly known as *read scale-out*. For more information about read-scale out and data access intent in [!INCLUDE[prod_short](includes/prod_short.md)], see [Utilizing Read Scale-Out for Better Performance](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) in the [!INCLUDE[prod_short](includes/prod_short.md)] Developer and Administration help.</span></span>

## <a name="to-change-the-database-access-intent"></a><span data-ttu-id="2094b-114">Breyta ástæðu fyrir aðgangi að gagnagrunni</span><span class="sxs-lookup"><span data-stu-id="2094b-114">To change the database access intent</span></span>

1. <span data-ttu-id="2094b-115">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Listi yfir ástæður fyrir aðgangi að gagnagrunni** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2094b-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Database Access Intent List**, and then choose the related link.</span></span>

    <span data-ttu-id="2094b-116">Á síðunni er listi yfir allar skýrslur, síður og fyrirspurnir.</span><span class="sxs-lookup"><span data-stu-id="2094b-116">The page lists all reports, pages, and queries.</span></span> <span data-ttu-id="2094b-117">Dálkurinn **Ástæða aðgangs** inniheldur eitt af eftirfarandi gildum:</span><span class="sxs-lookup"><span data-stu-id="2094b-117">The **Access Intent** column includes one of the following values:</span></span>

    |<span data-ttu-id="2094b-118">**Stilling**</span><span class="sxs-lookup"><span data-stu-id="2094b-118">**Setting**</span></span>|<span data-ttu-id="2094b-119">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="2094b-119">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="2094b-120">**Sjálfgefið**</span><span class="sxs-lookup"><span data-stu-id="2094b-120">**Default**</span></span>|<span data-ttu-id="2094b-121">Gefur til kynna að hluturinn notar fyrirframskilgreinda ástæðu fyrir aðgangi að gagnagrunni.</span><span class="sxs-lookup"><span data-stu-id="2094b-121">Indicates that the object uses the predefined database access intent.</span></span>|
    |<span data-ttu-id="2094b-122">**Leyfa að skrifa**</span><span class="sxs-lookup"><span data-stu-id="2094b-122">**Allow Write**</span></span>|<span data-ttu-id="2094b-123">Stillir hlutinn þannig að hann noti aðalgagnagrunninn, sem gerir notanda kleift að breyta gögnum.</span><span class="sxs-lookup"><span data-stu-id="2094b-123">Sets the object to use the primary database, allowing the user to modify data.</span></span>|
    |<span data-ttu-id="2094b-124">**Skrifvarið**</span><span class="sxs-lookup"><span data-stu-id="2094b-124">**Read Only**</span></span>|<span data-ttu-id="2094b-125">Stillir hlutinn þannig að hann noti eftirlíkingu gagnagrunns, sem þýðir að notandi getur aðeins skoðað gögn, ekki breytt þeim.</span><span class="sxs-lookup"><span data-stu-id="2094b-125">Sets the object to use the database replica, which means that the user can only view data, not change data.</span></span>|

2. <span data-ttu-id="2094b-126">Veldu aðgerðina **Breyta lista**.</span><span class="sxs-lookup"><span data-stu-id="2094b-126">Choose the **Edit List** action.</span></span>

3. <span data-ttu-id="2094b-127">Á síðunni **Breyta - Listi yfir ástæður fyrir aðgangi að gagnagrunni** skal breyta reitnum **Ástæða aðgangs** fyrir hlutina.</span><span class="sxs-lookup"><span data-stu-id="2094b-127">On the **Edit - Database Access Intent List** page, change the **Access Intent** field for the objects.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2094b-128">Ef hlutur sem er breytanlegur, eins og Viðskiptamannaspjald, er stilltur á **Skrifvarið**, verður aðalgagnagrunnurinn ennþá notaður óháð ástæðu fyrir aðgangi, sem gerir notendum kleift að gera breytingar eins og venjulega.</span><span class="sxs-lookup"><span data-stu-id="2094b-128">If an object that is editable, like the Customer Card, is set to **Read Only**, the primary database will still be used, regardless of the access intent, allowing users to make changes as normal.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="2094b-129">Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="2094b-129">See Related Training at [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="2094b-130">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2094b-130">See Also</span></span>
[<span data-ttu-id="2094b-131">Viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="2094b-131">Business Functionality</span></span>](across-business-functionality.md)  
[<span data-ttu-id="2094b-132">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="2094b-132">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="2094b-133">[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2094b-133">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="2094b-134">Undirbúðu þig fyrir að gera viðskipti</span><span class="sxs-lookup"><span data-stu-id="2094b-134">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]