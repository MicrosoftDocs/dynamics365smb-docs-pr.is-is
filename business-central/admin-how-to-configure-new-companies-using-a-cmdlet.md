---
title: "Hvernig á að grunnstilla ný fyrirtæki með Cmdlet | Microsoft Docs"
description: "Í mörgum tilfellum getur þú vlijað hlaða og flytja inn stillingapakka án þátttöku notenda eða nota notendaviðmót RapidStart Services. Það er gert með því að nota Windows PowerShell smáskipun."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 9d248f2f8676c392451ae4a6f99932145f354f5b
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a><span data-ttu-id="fa634-104">Grunnstilla ný fyrirtæki með Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fa634-104">Configure New Companies using a Cmdlet</span></span>
<span data-ttu-id="fa634-105">Í mörgum tilfellum getur þú vlijað hlaða og flytja inn stillingapakka án þátttöku notenda eða nota notendaviðmót RapidStart Services.</span><span class="sxs-lookup"><span data-stu-id="fa634-105">In a number of scenarios, you may want to load and import a configuration package without involving your users or using the RapidStart Services user interface.</span></span> <span data-ttu-id="fa634-106">Það er gert með því að nota Windows PowerShell smáskipun.</span><span class="sxs-lookup"><span data-stu-id="fa634-106">You can do so by using a Windows PowerShell cmdlet.</span></span> <span data-ttu-id="fa634-107">Atburðarás þar sem þetta getur verið gagnlegt eru:</span><span class="sxs-lookup"><span data-stu-id="fa634-107">Scenarios where this may be useful include:</span></span>  

- <span data-ttu-id="fa634-108">Gagnainnflutningur þvert yfir margar uppsetningar [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fa634-108">Performing data import across multiple [!INCLUDE[d365fin](includes/d365fin_md.md)] installations.</span></span>
- <span data-ttu-id="fa634-109">Grunnstilli viðbótarnotkunarsvið fyrir marga viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="fa634-109">Configuring additional application areas for multiple customers.</span></span>  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a><span data-ttu-id="fa634-110">Að nota uppsetningarpakka með cmdlet</span><span class="sxs-lookup"><span data-stu-id="fa634-110">To deploy a configuration package using a cmdlet</span></span>  

1. <span data-ttu-id="fa634-111">Undirbúa RapidStart Services pakkann.</span><span class="sxs-lookup"><span data-stu-id="fa634-111">Prepare a RapidStart Services package.</span></span> <span data-ttu-id="fa634-112">Til dæmis er hægt að búa til pakka til að flytja inn tiltekin gildi og heiti töflunnar og reitanna sem á að setja gildin inn í.</span><span class="sxs-lookup"><span data-stu-id="fa634-112">For example, you can create a package to import certain values and the names of the table and the fields to insert these values into.</span></span>  
2. <span data-ttu-id="fa634-113">Setjið pakkann upp í tölvunni þar sem cmdlet verður keyrt.</span><span class="sxs-lookup"><span data-stu-id="fa634-113">Place the package on a computer where you will run the cmdlet.</span></span>  
3. <span data-ttu-id="fa634-114">Opna stjórnunarskelina [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fa634-114">Open the [!INCLUDE[d365fin](includes/d365fin_md.md)] administration shell.</span></span>  
4. <span data-ttu-id="fa634-115">Færið inn **Invoke-NAVCodeUnit** og tilgreinið upplýsingar eins og þær sem sjá má í eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="fa634-115">Enter **Invoke-NAVCodeUnit**, and specify information similar to the following example.</span></span>  
    ```powershell  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
<span data-ttu-id="fa634-116">Cmdlet flytur pakkann inn í hvert fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="fa634-116">The cmdlet imports the package into each company.</span></span> <span data-ttu-id="fa634-117">Notendur geta byrjað að nota nýja virkni strax.</span><span class="sxs-lookup"><span data-stu-id="fa634-117">Users can start to use the new functionality immediately.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fa634-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="fa634-118">See Also</span></span>  
[<span data-ttu-id="fa634-119">Grunnstilla ný fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="fa634-119">Configure New Companies</span></span>](admin-how-to-configure-new-companies.md)  
[<span data-ttu-id="fa634-120">Nota skilgreiningu á ný fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="fa634-120">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="fa634-121">Uppsetning fyrirtækis með RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="fa634-121">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="fa634-122">Stjórnun</span><span class="sxs-lookup"><span data-stu-id="fa634-122">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="fa634-123">Microsoft Dynamics NAV Windows PowerShell Cmdlets</span><span class="sxs-lookup"><span data-stu-id="fa634-123">Microsoft Dynamics NAV Windows PowerShell Cmdlets</span></span>](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

