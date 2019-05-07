---
title: Skoðun á Síðum í Business Central
description: Notið eiginleika fyrir eftirlit með síðu til að skoða sérstaklega upplýsingar um síðuhönnun og gagnaveitu. Síðuskoðun hentar vel við úrræðaleit á vandamálum varðandi gögnin þín.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
author: jswymer
ms.date: 04/01/2019
ms.openlocfilehash: eb9d4ec76c0dbbd59763f7622ca51137c9563a91
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2019
ms.locfileid: "969879"
---
# <a name="inspecting-pages-in-business-central"></a><span data-ttu-id="eabde-104">Skoðun á Síðum í Business Central</span><span class="sxs-lookup"><span data-stu-id="eabde-104">Inspecting Pages in Business Central</span></span>

<span data-ttu-id="eabde-105">Eiginleiki fyrir eftirlit með síðu gerir þér kleift að ná í upplýsingar um síðu, veitir innsýn inn í síðuhönnun, mismunandi þætti sem síðan samanstendur af og uppruna gagnanna sem eru sýnd.</span><span class="sxs-lookup"><span data-stu-id="eabde-105">The page inspection feature enables you to get details about a page, providing insight into the page design, the different elements that comprise the page, and the source behind the data it displays.</span></span> <span data-ttu-id="eabde-106">Eftirlit með síðu er sérstaklega hönnuð fyrir stjórnendur, kraftnotendur, starfsfólk notendaþjónustu og þróunaraðila.</span><span class="sxs-lookup"><span data-stu-id="eabde-106">Page inspection is especially designed for administrators, power users, support personnel, and developers.</span></span> <span data-ttu-id="eabde-107">Hún er tilvalin í að fræðast um gagnalíkanið á bak við síðu og úrræðaleit.</span><span class="sxs-lookup"><span data-stu-id="eabde-107">It is ideal for learning the data model behind a page and troubleshooting.</span></span> <span data-ttu-id="eabde-108">Ef þú átt til að mynda í vandræðum með síðu er hægt að nota eftirlit með síðu til að fá upplýsingar sem eru sendar áfram til kerfisstjórans eða starfsfólk notendaþjónustu.</span><span class="sxs-lookup"><span data-stu-id="eabde-108">For example, if you are experiencing a problem with a page, you could use page inspection to get information to pass on to your system administrator or support personnel.</span></span>

## <a name="working-with-page-inspection"></a><span data-ttu-id="eabde-109">Vinna með síðueftirlit</span><span class="sxs-lookup"><span data-stu-id="eabde-109">Working with Page Inspection</span></span>

<span data-ttu-id="eabde-110">Til að skoða síðu skal velja ![Stillingartákn](media/ui-experience/settings_icon_small.png) efst í hægra horninu, síðan velja **Skoða**.</span><span class="sxs-lookup"><span data-stu-id="eabde-110">To inspect a page, in the top right corner, choose ![Settings icon](media/ui-experience/settings_icon_small.png), then choose **Inspect**.</span></span> <span data-ttu-id="eabde-111">Eða hægt er að nota flýtileiðina **Ctrl+Alt+F1**.</span><span class="sxs-lookup"><span data-stu-id="eabde-111">Or, you can use the keyboard shortcut **Ctrl+Alt+F1**.</span></span>

<span data-ttu-id="eabde-112">Rúðan **Eftirlit með síðu** opnast á hliðinni.</span><span class="sxs-lookup"><span data-stu-id="eabde-112">The **Page inspection** pane opens on the side.</span></span> <span data-ttu-id="eabde-113">Eftirfarandi skýringarmynd sýnir rúðuna **Eftirlit með síðu** á síðunni **Sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="eabde-113">The following figure illustrates the **Page Inspection** pane on the **Sales Order** page.</span></span>

![Eftirlit með síðu](media/page-inspection-example.png)

<span data-ttu-id="eabde-115">Þegar rúðan **Eftirlit með síðu** opnast fyrst, sýnir hún upplýsingar sem á við um hlut aðalsíðunnar.</span><span class="sxs-lookup"><span data-stu-id="eabde-115">When the **Page Inspection** pane first opens, it shows information that pertains to the main page object.</span></span>

<span data-ttu-id="eabde-116">Notaðu lyklaborðið eða benditækið til að færa fókusinn á aðrar einingar á síðunni.</span><span class="sxs-lookup"><span data-stu-id="eabde-116">Use the keyboard or pointing device to move focus to different elements on the page.</span></span> <span data-ttu-id="eabde-117">Þegar Upplýsingakassi er valinn eða hluti á aðalsíðunni verður afmarkaða svæðið auðkennt með ramma og rúðan **Eftirlit með síðu** birtir upplýsingar um valda einingu.</span><span class="sxs-lookup"><span data-stu-id="eabde-117">When you select a FactBox or a part on the main page, the bounding area is highlighted by a border, and the **Page Inspection** pane shows information about the selected element.</span></span> <span data-ttu-id="eabde-118">Til dæmis sýnir skýringarmyndin hér á undan upplýsingar um listahlutann á síðunni **Sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="eabde-118">For example, the previous figure shows information about the list part in the **Sales Order** page.</span></span> <span data-ttu-id="eabde-119">Þar sem þú ferð yfir á aðrar síður í forritinu mun rúðan **Eftirlit með síðu** uppfærast sjálfkrafa með síðuupplýsingum um leið og þú ferð á milli.</span><span class="sxs-lookup"><span data-stu-id="eabde-119">As you navigate to other pages in the application, the **Page Inspection** pane will automatically update with page information as you move along.</span></span>

<span data-ttu-id="eabde-120">Frekari upplýsingar um hvað er sýnt í síðueftirliti er að finna í [Síður eftirlits og úrræðaleitar](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) í hjálpinni fyrir Business Central Developer og IT Pro.</span><span class="sxs-lookup"><span data-stu-id="eabde-120">For more information about what is shown in page inspection, see [Inspecting and Troubleshooting Pages](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) in the Business Central Developer and IT Pro help.</span></span>

<span data-ttu-id="eabde-121">Ef upplýsingarnar sjást ekki sem þú býst við að sjá í rúðunni **Eftirlit með síðu** ertu líklega ekki með nauðsynlegar heimildir eins og er lýst í næsta hluta.</span><span class="sxs-lookup"><span data-stu-id="eabde-121">If you do not see the details that you expect to see in the **Page Inspection** pane, you probably do not have the required permissions, as described in th next section.</span></span>

## <a name="controlling-access-to-page-inspection-details"></a><span data-ttu-id="eabde-122">Upplýsingar um stjórnun á aðgangi að síðueftirliti</span><span class="sxs-lookup"><span data-stu-id="eabde-122">Controlling Access to Page Inspection Details</span></span>

<span data-ttu-id="eabde-123">Sem stjórnandi er hægt að stýra aðgangi að ítarlegum upplýsingum sem eru sýndar í rúðunni **Eftirlit með síðu** með því að stilla heimildir sem notendur eru með.</span><span class="sxs-lookup"><span data-stu-id="eabde-123">As an administrator, you can control access to the full details that are shown in the **Page Inspection** pane by configuring the permissions that users have.</span></span> <span data-ttu-id="eabde-124">Til að veita aðgangsheimild notanda að ítarlegum upplýsingum skal gefa notendum heimildina **Keyra** í **Kerfis** hlutanum **5330**.</span><span class="sxs-lookup"><span data-stu-id="eabde-124">To grant a user permission to the full details, give users **Execute** permission on the **System** object **5330**.</span></span> <span data-ttu-id="eabde-125">Hægt er að veita þessa heimild með því að nota heimildasamstæðu (t.d. **D365 úrræðaleit**) eða notendaflokk (t.d. **D365 úrræðaleit**).</span><span class="sxs-lookup"><span data-stu-id="eabde-125">You can grant this permission by using a permission set (such as **D365 Troubleshoot**) or a user group (such as **D365 Troubleshoot**).</span></span> <span data-ttu-id="eabde-126">Frekari upplýsingar um heimildir er að finna í [Stjórnun notenda og heimilda](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="eabde-126">For more information about permissions, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>

<span data-ttu-id="eabde-127">Notendur sem fá heimildir í **Kerfishlutur 5330** geta enn opnað rúðuna **Eftirlit með síðu**, en þeir munu aðeins sjá reitina **Síða** og **Tafla** sem birta grunnupplýsingar sem hægt er að senda áfram til þjónustudeildar.</span><span class="sxs-lookup"><span data-stu-id="eabde-127">Users who are not granted permissions on **System object 5330** can still access the **Page Inspection** pane, but they will only see the **Page** and **Table** fields, which display basic details that they can pass on to their support team.</span></span>

## <a name="see-also"></a><span data-ttu-id="eabde-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="eabde-128">See Also</span></span>

<span data-ttu-id="eabde-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eabde-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
