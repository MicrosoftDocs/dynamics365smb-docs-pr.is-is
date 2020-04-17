---
title: Algengar spurningar um Viðmótsleit | Microsoft Docs
description: Þessi grein veitir svör við spurningum sem samstarfsaðilar og viðskiptamenn spyrja oft um Viðmótsleit.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: a23851dfbca688c5935d967a66ad6ebc8a0abe5e
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195340"
---
# <a name="tell-me-faq"></a><span data-ttu-id="80817-103">Algengar spurningar um Viðmótsleit</span><span class="sxs-lookup"><span data-stu-id="80817-103">Tell Me FAQ</span></span>
<span data-ttu-id="80817-104">Þetta efnisatriði svarar spurningum sem reyndir notendur spyrja oft um eiginleika viðmótsleitar.</span><span class="sxs-lookup"><span data-stu-id="80817-104">This topic answers questions that our advanced users often ask about the Tell Me feature.</span></span>

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a><span data-ttu-id="80817-105">Eru allar aðgerðir úr núverandi síðunni minni sýnilegar í Viðmótsleit?</span><span class="sxs-lookup"><span data-stu-id="80817-105">Are all actions from my current page discoverable in Tell Me?</span></span>
<span data-ttu-id="80817-106">Nei.</span><span class="sxs-lookup"><span data-stu-id="80817-106">No.</span></span> <span data-ttu-id="80817-107">Aðgerðir í hlutum, svo sem sölulínur eða upplýsingakassar, birtast ekki í Viðmótsleit.</span><span class="sxs-lookup"><span data-stu-id="80817-107">Actions in parts, such as the Sales Lines part or FactBoxes, are not displayed in Tell Me.</span></span>

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a><span data-ttu-id="80817-108">Eru niðurstöðurnar í Viðmótsleit síaðar eftir heimildum?</span><span class="sxs-lookup"><span data-stu-id="80817-108">Are the results in Tell Me filtered by permissions?</span></span>
<span data-ttu-id="80817-109">Ef notandinn hefur ekki AccessByPermissions þá eru aðgerðir ekki sýndar.</span><span class="sxs-lookup"><span data-stu-id="80817-109">If the user does not have AccessByPermissions then actions are not displayed.</span></span> <span data-ttu-id="80817-110">Hins vegar birtast síður og skýrslur í niðurstöðum en krefjast þess að notandinn hafi heimild til að fá aðgang að þeim.</span><span class="sxs-lookup"><span data-stu-id="80817-110">However, pages and reports appear in the results but require that the user has permission to access them.</span></span> <span data-ttu-id="80817-111">Skilaboð birtast ef notandinn hefur ekki leyfi til að skoða hlutinn.</span><span class="sxs-lookup"><span data-stu-id="80817-111">A message will display if the user does not have permission to view the object.</span></span>

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a><span data-ttu-id="80817-112">Sýnir Viðmótsleit efni úr sérstillingum mínum eða uppsettum viðbótum þriðja aðila?</span><span class="sxs-lookup"><span data-stu-id="80817-112">Does Tell Me display content from my customizations or installed third-party extensions?</span></span>
<span data-ttu-id="80817-113">Aðgerðir, síður og skýrslur sem koma frá viðbótum eru sóttar með Viðmótsleit, en sérsniðin hjálpargögn eru það ekki.</span><span class="sxs-lookup"><span data-stu-id="80817-113">Actions, pages, and reports that originate from extensions are picked up by Tell Me, but custom help documentation is not.</span></span> <span data-ttu-id="80817-114">Fyrir tæknilegar upplýsingar um hvernig á að búa til sérsniðnar síður og skýrslur sýnileg, sjá [Bæta síðum og skýrslum við leit](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span><span class="sxs-lookup"><span data-stu-id="80817-114">For technical information about how to make custom pages and reports discoverable, see [Adding Pages and Reports to Search](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span></span>

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a><span data-ttu-id="80817-115">Hvað gerir þetta frábrugðið því sem áður var þekkt sem Síðuleit?</span><span class="sxs-lookup"><span data-stu-id="80817-115">What makes this different from what was previously known as Page Search?</span></span>
<span data-ttu-id="80817-116">Síðuleit hefur þróast í Viðmótsleit til að hjálpa þér að koma hlutum í verk fljótt.</span><span class="sxs-lookup"><span data-stu-id="80817-116">Page Search has evolved into Tell Me to help you get work done quickly.</span></span> <span data-ttu-id="80817-117">Síðuleit gæti aðeins hjálpað þér að vafra á síður eða skýrslur.</span><span class="sxs-lookup"><span data-stu-id="80817-117">Page Search could only help you navigate to pages or reports.</span></span> <span data-ttu-id="80817-118">Á tæknilegu stigi er Viðmótsleit ekki lengur byggt á eldra hugtakinu MenuSuite.</span><span class="sxs-lookup"><span data-stu-id="80817-118">At a technical level, Tell Me is no longer based on the legacy MenuSuite concept.</span></span>

### <a name="i-use-on-premises-d365fin-does-that-include-tell-me"></a><span data-ttu-id="80817-119">Ég nota á staðnum [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="80817-119">I use on-premises [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="80817-120">Felur það í sér Viðmótsleit?</span><span class="sxs-lookup"><span data-stu-id="80817-120">Does that include Tell Me?</span></span>
<span data-ttu-id="80817-121">Þú getur notað Viðmótsleit í vefbiðlaranum á staðnum til að finna aðgerðir, síður og skýrslur en ekki skjöl, eða forrit og ráðgjafarþjónustu á AppSource.</span><span class="sxs-lookup"><span data-stu-id="80817-121">You can use Tell Me in the on-premises Web Client to find actions, pages, and reports, but not documentation, or apps and consulting services on AppSource.</span></span>

### <a name="is-tell-me-available-for-all-form-factors"></a><span data-ttu-id="80817-122">Er Viðmótsleit aðgengileg fyrir alla myndaþætti?</span><span class="sxs-lookup"><span data-stu-id="80817-122">Is Tell Me available for all form factors?</span></span>
<span data-ttu-id="80817-123">Viðmótsleit er aðeins í boði í vefbiðlaranum eða Windows skjáborðsforritinu.</span><span class="sxs-lookup"><span data-stu-id="80817-123">Tell Me is only available in the Web Client or Windows desktop app.</span></span>

### <a name="are-the-documentation-results-available-in-any-language"></a><span data-ttu-id="80817-124">Eru niðurstöður fyrir fylgiskjöl tiltæk á hvaða tungumáli sem er?</span><span class="sxs-lookup"><span data-stu-id="80817-124">Are the documentation results available in any language?</span></span>
<span data-ttu-id="80817-125">Hjálparefnin birtast á því tungumáli sem þú hefur tilgreint í **Stillingarnar mínar**, ef hjálp er til staðar á því tungumáli.</span><span class="sxs-lookup"><span data-stu-id="80817-125">The help articles display in the language you have specified in **My Settings**, if help is available in that language.</span></span>

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a><span data-ttu-id="80817-126">Hvers vegna sé ég ekki bókamerkistákn fyrir leitarniðurstöðurnar mínar?</span><span class="sxs-lookup"><span data-stu-id="80817-126">Why don't I see a bookmark icon for my search results?</span></span>
<span data-ttu-id="80817-127">Bókamerkjatákn er ekki birt í glugganum „Viðmótsleit“ þegar sérstillingar eru óvirkar fyrir notandahlutverk.</span><span class="sxs-lookup"><span data-stu-id="80817-127">The bookmark icon is not displayed in the Tell Me window when personalization is disabled for a user role.</span></span>


## <a name="see-also"></a><span data-ttu-id="80817-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="80817-128">See Also</span></span>  
[<span data-ttu-id="80817-129">Vista og sérsníða listayfirlit</span><span class="sxs-lookup"><span data-stu-id="80817-129">Save and Personalize List Views</span></span>](ui-views.md)  
[<span data-ttu-id="80817-130">Finndu síður og upplýsingar með Viðmótsleit</span><span class="sxs-lookup"><span data-stu-id="80817-130">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
[<span data-ttu-id="80817-131">Að finna síður með hlutverkaleit</span><span class="sxs-lookup"><span data-stu-id="80817-131">Finding Pages with the Role Explorer</span></span>](ui-role-explorer.md)  
[<span data-ttu-id="80817-132">Síða eða skýrsla bókamerkt í Mitt hlutverk</span><span class="sxs-lookup"><span data-stu-id="80817-132">Bookmark a Page or Report on Your Role Center</span></span>](ui-bookmarks.md)
