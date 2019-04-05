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
ms.date: 10/01/2018
ms.author: bholtorf
ms.openlocfilehash: 70ab7fb07cda5ce9d86b3f39dd14321829e85a52
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800440"
---
# <a name="tell-me-faq"></a><span data-ttu-id="ac193-103">Algengar spurningar um Viðmótsleit</span><span class="sxs-lookup"><span data-stu-id="ac193-103">Tell Me FAQ</span></span>
<span data-ttu-id="ac193-104">Þetta efni svarar spurningum sem háþróaðir notendur okkar spyrja oft um nýja eiginleikann Viðmótsleit, sem hefur komið í stað fyrri leitareiginleika sem kallast **Finna síður og skýrslur**.</span><span class="sxs-lookup"><span data-stu-id="ac193-104">This topic answers questions that our advanced users often ask about the new Tell Me feature, which has replaced the previous Page Search feature known as **Find Pages and Reports**.</span></span>

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a><span data-ttu-id="ac193-105">Eru allar aðgerðir úr núverandi síðunni minni sýnilegar í Viðmótsleit?</span><span class="sxs-lookup"><span data-stu-id="ac193-105">Are all actions from my current page discoverable in Tell Me?</span></span>
<span data-ttu-id="ac193-106">Nei.</span><span class="sxs-lookup"><span data-stu-id="ac193-106">No.</span></span> <span data-ttu-id="ac193-107">Aðgerðir í hlutum, svo sem sölulínur eða upplýsingakassar, birtast ekki í Viðmótsleit.</span><span class="sxs-lookup"><span data-stu-id="ac193-107">Actions in parts, such as the Sales Lines part or FactBoxes, are not displayed in Tell Me.</span></span>

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a><span data-ttu-id="ac193-108">Eru niðurstöðurnar í Viðmótsleit síaðar eftir heimildum?</span><span class="sxs-lookup"><span data-stu-id="ac193-108">Are the results in Tell Me filtered by permissions?</span></span>
<span data-ttu-id="ac193-109">Ef notandinn hefur ekki AccessByPermissions þá eru aðgerðir ekki sýndar.</span><span class="sxs-lookup"><span data-stu-id="ac193-109">If the user does not have AccessByPermissions then actions are not displayed.</span></span> <span data-ttu-id="ac193-110">Hins vegar birtast síður og skýrslur í niðurstöðum en krefjast þess að notandinn hafi heimild til að fá aðgang að þeim.</span><span class="sxs-lookup"><span data-stu-id="ac193-110">However, pages and reports appear in the results but require that the user has permission to access them.</span></span> <span data-ttu-id="ac193-111">Skilaboð birtast ef notandinn hefur ekki leyfi til að skoða hlutinn.</span><span class="sxs-lookup"><span data-stu-id="ac193-111">A message will display if the user does not have permission to view the object.</span></span>

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a><span data-ttu-id="ac193-112">Sýnir Viðmótsleit efni úr sérstillingum mínum eða uppsettum viðbótum þriðja aðila?</span><span class="sxs-lookup"><span data-stu-id="ac193-112">Does Tell Me display content from my customizations or installed third-party extensions?</span></span>
<span data-ttu-id="ac193-113">Aðgerðir, síður og skýrslur sem koma frá viðbótum eru sóttar með Viðmótsleit, en sérsniðin hjálpargögn eru það ekki.</span><span class="sxs-lookup"><span data-stu-id="ac193-113">Actions, pages, and reports that originate from extensions are picked up by Tell Me, but custom help documentation is not.</span></span> <span data-ttu-id="ac193-114">Fyrir tæknilegar upplýsingar um hvernig á að búa til sérsniðnar síður og skýrslur sýnileg, sjá [Bæta síðum og skýrslum við leit](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span><span class="sxs-lookup"><span data-stu-id="ac193-114">For technical information about how to make custom pages and reports discoverable, see [Adding Pages and Reports to Search](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).</span></span>

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a><span data-ttu-id="ac193-115">Hvað gerir þetta frábrugðið því sem áður var þekkt sem Síðuleit?</span><span class="sxs-lookup"><span data-stu-id="ac193-115">What makes this different from what was previously known as Page Search?</span></span>
<span data-ttu-id="ac193-116">Síðuleit hefur þróast í Viðmótsleit til að hjálpa þér að koma hlutum í verk fljótt.</span><span class="sxs-lookup"><span data-stu-id="ac193-116">Page Search has evolved into Tell Me to help you get work done quickly.</span></span> <span data-ttu-id="ac193-117">Síðuleit gæti aðeins hjálpað þér að vafra á síður eða skýrslur.</span><span class="sxs-lookup"><span data-stu-id="ac193-117">Page Search could only help you navigate to pages or reports.</span></span> <span data-ttu-id="ac193-118">Á tæknilegu stigi er Viðmótsleit ekki lengur byggt á eldra hugtakinu MenuSuite.</span><span class="sxs-lookup"><span data-stu-id="ac193-118">At a technical level, Tell Me is no longer based on the legacy MenuSuite concept.</span></span>

### <a name="i-use-on-premises-included365finincludesd365finmdmd-does-that-include-tell-me"></a><span data-ttu-id="ac193-119">Ég nota á staðnum [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ac193-119">I use on-premises [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ac193-120">Felur það í sér Viðmótsleit?</span><span class="sxs-lookup"><span data-stu-id="ac193-120">Does that include Tell Me?</span></span>
<span data-ttu-id="ac193-121">Þú getur notað Viðmótsleit í vefbiðlaranum á staðnum til að finna aðgerðir, síður og skýrslur en ekki skjöl.</span><span class="sxs-lookup"><span data-stu-id="ac193-121">You can use Tell Me in the on-premises Web Client to find actions, pages, and reports, but not documentation.</span></span> <span data-ttu-id="ac193-122">Notendur sem tengjast [!INCLUDE[d365fin](includes/d365fin_md.md)] frá Dynamics NAV biðlaranum halda áfram að nota Síðuleit.</span><span class="sxs-lookup"><span data-stu-id="ac193-122">Users connecting to [!INCLUDE[d365fin](includes/d365fin_md.md)] from the Dynamics NAV client continue to use Page Search.</span></span>

### <a name="is-tell-me-available-for-all-form-factors"></a><span data-ttu-id="ac193-123">Er Viðmótsleit aðgengileg fyrir alla myndaþætti?</span><span class="sxs-lookup"><span data-stu-id="ac193-123">Is Tell Me available for all form factors?</span></span>
<span data-ttu-id="ac193-124">Viðmótsleit er aðeins í boði í vefbiðlaranum eða Windows skjáborðsforritinu.</span><span class="sxs-lookup"><span data-stu-id="ac193-124">Tell Me is only available in the Web Client or Windows desktop app.</span></span>

### <a name="are-the-documentation-results-available-in-any-language"></a><span data-ttu-id="ac193-125">Eru niðurstöður fyrir fylgiskjöl tiltæk á hvaða tungumáli sem er?</span><span class="sxs-lookup"><span data-stu-id="ac193-125">Are the documentation results available in any language?</span></span>
<span data-ttu-id="ac193-126">Hjálparefnin birtast á því tungumáli sem þú hefur tilgreint í **Stillingarnar mínar**, ef hjálp er til staðar á því tungumáli.</span><span class="sxs-lookup"><span data-stu-id="ac193-126">The help articles display in the language you have specified in **My Settings**, if help is available in that language.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac193-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ac193-127">See Also</span></span>  
[<span data-ttu-id="ac193-128">Að finna eiginleika og upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ac193-128">Finding Features and Information</span></span>](ui-search.md)
