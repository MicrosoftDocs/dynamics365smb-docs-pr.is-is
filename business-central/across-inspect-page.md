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
ms.date: 04/01/2020
ms.openlocfilehash: 7790548828595838e6c2f626194d59260ef4e8ab
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187773"
---
# <a name="inspecting-pages-in-business-central"></a><span data-ttu-id="0d662-104">Skoðun á Síðum í Business Central</span><span class="sxs-lookup"><span data-stu-id="0d662-104">Inspecting Pages in Business Central</span></span>

<span data-ttu-id="0d662-105">Eiginleiki fyrir eftirlit með síðu gerir þér kleift að ná í upplýsingar um síðu, veitir innsýn inn í síðuhönnun, mismunandi þætti sem síðan samanstendur af og uppruna gagnanna sem eru sýnd.</span><span class="sxs-lookup"><span data-stu-id="0d662-105">The page inspection feature enables you to get details about a page, providing insight into the page design, the different elements that comprise the page, and the source behind the data it displays.</span></span> <span data-ttu-id="0d662-106">Eftirlit með síðu er sérstaklega hönnuð fyrir stjórnendur, kraftnotendur, starfsfólk notendaþjónustu og þróunaraðila.</span><span class="sxs-lookup"><span data-stu-id="0d662-106">Page inspection is especially designed for administrators, power users, support personnel, and developers.</span></span> <span data-ttu-id="0d662-107">Hún er tilvalin í að fræðast um gagnalíkanið á bak við síðu og úrræðaleit.</span><span class="sxs-lookup"><span data-stu-id="0d662-107">It is ideal for learning the data model behind a page and troubleshooting.</span></span> <span data-ttu-id="0d662-108">Ef þú átt til að mynda í vandræðum með síðu er hægt að nota eftirlit með síðu til að fá upplýsingar sem eru sendar áfram til kerfisstjórans eða starfsfólk notendaþjónustu.</span><span class="sxs-lookup"><span data-stu-id="0d662-108">For example, if you are experiencing a problem with a page, you could use page inspection to get information to pass on to your system administrator or support personnel.</span></span>

## <a name="working-with-page-inspection"></a><span data-ttu-id="0d662-109">Vinna með síðueftirlit</span><span class="sxs-lookup"><span data-stu-id="0d662-109">Working with Page Inspection</span></span>

<span data-ttu-id="0d662-110">Þú byrjar síðueftirlit á **Hjálp og notendaþjónusta**.</span><span class="sxs-lookup"><span data-stu-id="0d662-110">You start page inspection from the **Help & Support** page.</span></span> <span data-ttu-id="0d662-111">Veldu spurningamerkið efst í hægra horninu, svo **Hjálp og notendaþjónusta** og svo **Kanna síður og gögn**.</span><span class="sxs-lookup"><span data-stu-id="0d662-111">Choose the question mark in the top right corner, choose **Help & Support**, and then choose **Inspect pages and data**.</span></span> <span data-ttu-id="0d662-112">Einnig er hægt að nota flýtilykilinn **Ctrl+Alt+F1**.</span><span class="sxs-lookup"><span data-stu-id="0d662-112">Or, you can just use the keyboard shortcut **Ctrl+Alt+F1**.</span></span>

<span data-ttu-id="0d662-113">Rúðan **Eftirlit með síðu** opnast á hliðinni.</span><span class="sxs-lookup"><span data-stu-id="0d662-113">The **Page inspection** pane opens on the side.</span></span> <span data-ttu-id="0d662-114">Eftirfarandi skýringarmynd sýnir rúðuna **Eftirlit með síðu** á síðunni **Sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="0d662-114">The following figure illustrates the **Page Inspection** pane on the **Sales Order** page.</span></span>

![Eftirlit með síðu](media/page-inspection-example.png)

<span data-ttu-id="0d662-116">Þegar rúðan **Eftirlit með síðu** opnast fyrst, sýnir hún upplýsingar sem á við um hlut aðalsíðunnar.</span><span class="sxs-lookup"><span data-stu-id="0d662-116">When the **Page Inspection** pane first opens, it shows information that pertains to the main page object.</span></span>

<span data-ttu-id="0d662-117">Notaðu lyklaborðið eða benditækið til að færa fókusinn á aðrar einingar á síðunni.</span><span class="sxs-lookup"><span data-stu-id="0d662-117">Use the keyboard or pointing device to move focus to different elements on the page.</span></span> <span data-ttu-id="0d662-118">Þegar Upplýsingakassi er valinn eða hluti á aðalsíðunni verður afmarkaða svæðið auðkennt með ramma og rúðan **Eftirlit með síðu** birtir upplýsingar um valda einingu.</span><span class="sxs-lookup"><span data-stu-id="0d662-118">When you select a FactBox or a part on the main page, the bounding area is highlighted by a border, and the **Page Inspection** pane shows information about the selected element.</span></span> <span data-ttu-id="0d662-119">Til dæmis sýnir skýringarmyndin hér á undan upplýsingar um listahlutann á síðunni **Sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="0d662-119">For example, the previous figure shows information about the list part in the **Sales Order** page.</span></span> <span data-ttu-id="0d662-120">Þar sem þú ferð yfir á aðrar síður í forritinu mun rúðan **Eftirlit með síðu** uppfærast sjálfkrafa með síðuupplýsingum um leið og þú ferð á milli.</span><span class="sxs-lookup"><span data-stu-id="0d662-120">As you navigate to other pages in the application, the **Page Inspection** pane will automatically update with page information as you move along.</span></span>

<span data-ttu-id="0d662-121">Frekari upplýsingar um hvað er sýnt í síðueftirliti er að finna í [Síður eftirlits og úrræðaleitar](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) í hjálpinni fyrir Business Central Developer og IT Pro.</span><span class="sxs-lookup"><span data-stu-id="0d662-121">For more information about what is shown in page inspection, see [Inspecting and Troubleshooting Pages](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) in the Business Central Developer and IT Pro help.</span></span>

<span data-ttu-id="0d662-122">Ef upplýsingarnar sjást ekki sem þú býst við að sjá í rúðunni **Eftirlit með síðu** ertu líklega ekki með nauðsynlegar heimildir eins og er lýst í næsta hluta.</span><span class="sxs-lookup"><span data-stu-id="0d662-122">If you do not see the details that you expect to see in the **Page Inspection** pane, you probably do not have the required permissions, as described in the next section.</span></span>

## <a name="controlling-access-to-page-inspection-details"></a><span data-ttu-id="0d662-123">Upplýsingar um stjórnun á aðgangi að síðueftirliti</span><span class="sxs-lookup"><span data-stu-id="0d662-123">Controlling Access to Page Inspection Details</span></span>

<span data-ttu-id="0d662-124">Sem stjórnandi er hægt að stýra aðgangi að ítarlegum upplýsingum sem eru sýndar í rúðunni **Eftirlit með síðu** með því að stilla heimildir sem notendur eru með.</span><span class="sxs-lookup"><span data-stu-id="0d662-124">As an administrator, you can control access to the full details that are shown in the **Page Inspection** pane by configuring the permissions that users have.</span></span> <span data-ttu-id="0d662-125">Til að veita aðgangsheimild notanda að ítarlegum upplýsingum skal gefa notendum heimildina **Keyra** í **Kerfis** hlutanum **5330**.</span><span class="sxs-lookup"><span data-stu-id="0d662-125">To grant a user permission to the full details, give users **Execute** permission on the **System** object **5330**.</span></span> <span data-ttu-id="0d662-126">Hægt er að veita þessa heimild með því að nota heimildasamstæðu (t.d. **D365 úrræðaleit**) eða notendaflokk (t.d. **D365 úrræðaleit**).</span><span class="sxs-lookup"><span data-stu-id="0d662-126">You can grant this permission by using a permission set (such as **D365 Troubleshoot**) or a user group (such as **D365 Troubleshoot**).</span></span> <span data-ttu-id="0d662-127">Nánari upplýsingar um heimildir má finna í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="0d662-127">For more information about permissions, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>

<span data-ttu-id="0d662-128">Notendur sem fá heimildir í **Kerfishlutur 5330** geta enn opnað rúðuna **Eftirlit með síðu**, en þeir munu aðeins sjá reitina **Síða** og **Tafla** sem birta grunnupplýsingar sem hægt er að senda áfram til þjónustudeildar.</span><span class="sxs-lookup"><span data-stu-id="0d662-128">Users who are not granted permissions on **System object 5330** can still access the **Page Inspection** pane, but they will only see the **Page** and **Table** fields, which display basic details that they can pass on to their support team.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d662-129">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0d662-129">See Also</span></span>

<span data-ttu-id="0d662-130">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0d662-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
