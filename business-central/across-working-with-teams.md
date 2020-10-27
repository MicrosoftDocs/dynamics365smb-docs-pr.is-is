---
title: Unnið með Business Central Data í Microsoft Teams| Microsoft docs
description: Fá upplýsingar um notkun Business Central fyrir Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989423"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a><span data-ttu-id="63e6f-103">Unnið með Business Central Data í Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="63e6f-103">Working with Business Central Data in Microsoft Teams</span></span>

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

<span data-ttu-id="63e6f-104">[!INCLUDE [prodshort](includes/prodshort.md)] býður upp á forrit sem tengir Microsoft Teams við viðskiptagögn í [!INCLUDE [prodshort](includes/prodshort.md)] þannig að hægt sé að deila upplýsingum á fjótlegan hátt á meðal teymismeðlima og svara fyrirspurnum með skjótari hætti.</span><span class="sxs-lookup"><span data-stu-id="63e6f-104">[!INCLUDE [prodshort](includes/prodshort.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prodshort](includes/prodshort.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="63e6f-105">Í þessari grein koma fram upplýsingar um hvernig á að nota forritið til að deila [!INCLUDE [prodshort](includes/prodshort.md)]-gögnum með samstarfsfólki í samtali í Teams.</span><span class="sxs-lookup"><span data-stu-id="63e6f-105">In this article, you'll learn how to use the app to share [!INCLUDE [prodshort](includes/prodshort.md)] data with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="63e6f-106">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="63e6f-106">Overview</span></span>

<span data-ttu-id="63e6f-107">[!INCLUDE [prodshort](includes/prodshort.md)]-forritið gerir kleift að:</span><span class="sxs-lookup"><span data-stu-id="63e6f-107">The [!INCLUDE [prodshort](includes/prodshort.md)] app lets you:</span></span>

- <span data-ttu-id="63e6f-108">Afrita tengil í hvaða færslu Business Central sem er og líma hann í spjall á Teams til að deila honum með samstarfsfólki.</span><span class="sxs-lookup"><span data-stu-id="63e6f-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="63e6f-109">Tengillinn stækkar og verður að þéttu, gagnvirku spjaldi sem birtir upplýsingar um færsluna.</span><span class="sxs-lookup"><span data-stu-id="63e6f-109">The link will expand that into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="63e6f-110">Þegar á samtalinu stendur getur þú og samstarfsfólk þitt skoðað frekari upplýsingar um færsluna, breytt gögnum og gripið til aðgerða - án þess að fara úr Teams.</span><span class="sxs-lookup"><span data-stu-id="63e6f-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action - without leaving Teams.</span></span>

<span data-ttu-id="63e6f-111">[![Samþætting Teams við Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="63e6f-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="63e6f-112">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="63e6f-112">Prerequisites</span></span>

- <span data-ttu-id="63e6f-113">Þú hefur aðgang að Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="63e6f-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="63e6f-114">Þú hefur sett upp [!INCLUDE [prodshort](includes/prodshort.md)]-forritið  í Teams.</span><span class="sxs-lookup"><span data-stu-id="63e6f-114">You've installed the [!INCLUDE [prodshort](includes/prodshort.md)] app in Teams.</span></span> <span data-ttu-id="63e6f-115">Frekari upplýsingar er að finna í [Setja upp [!INCLUDE [prodshort](includes/prodshort.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="63e6f-115">For more information, see [Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="63e6f-116">Allir þátttakendur í Teams-spjalli geta skoðað spjöld fyrir færslur Business Central sem þú sendir inn á spjallið.</span><span class="sxs-lookup"><span data-stu-id="63e6f-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="63e6f-117">En til að skoða frekari upplýsingar um færslur með því að nota hnappana **Upplýsingar** eða **Sprettigluggi** á spjaldi, þurfa þeir að fá aðgang að [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="63e6f-117">But to view more details about records, by using the **Details** or **Pop-out** buttons on a card, they'll need access to [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="63e6f-118">Nánari upplýsingar er að finna í [Stjórnun Microsoft Teams samþættingar](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="63e6f-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="63e6f-119">Hafa með Business Central-spjald í samtali í Teams</span><span class="sxs-lookup"><span data-stu-id="63e6f-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="63e6f-120">Skráðu þig inn í [!INCLUDE [prodshort](includes/prodshort.md)] með vafranum.</span><span class="sxs-lookup"><span data-stu-id="63e6f-120">Sign in to [!INCLUDE [prodshort](includes/prodshort.md)] using your browser.</span></span>
2. <span data-ttu-id="63e6f-121">Opnið færsluna sem á að deila.</span><span class="sxs-lookup"><span data-stu-id="63e6f-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="63e6f-122">Forritið er hannað til að birta síðu kortagerðar úr [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="63e6f-122">The app is designed to display card type pages from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="63e6f-123">Opnið því síðu sem sýnir eina færslu, eins og vöru, viðskiptavin eða sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="63e6f-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="63e6f-124">Ekki er hægt að nota hana fyrir hlutverkamiðstöðvar eða síður sem birta nokkrar færslur í lista.</span><span class="sxs-lookup"><span data-stu-id="63e6f-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="63e6f-125">Afritið alla vefslóðina úr veffangastiku vafrans.</span><span class="sxs-lookup"><span data-stu-id="63e6f-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Afrita vefslóð Business Central úr vafranum](media/teams-url.png)
4. <span data-ttu-id="63e6f-127">Farið í Teams og hefjið samtal sem getur verið spjall við einstakling, hóp eða teymisrás.</span><span class="sxs-lookup"><span data-stu-id="63e6f-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="63e6f-128">Límið vefslóðina í reitinn þar sem þú bætir við skilaboðum.</span><span class="sxs-lookup"><span data-stu-id="63e6f-128">Paste the URL into the box where you add a message.</span></span>

   ![Líma vefslóð Business Central í Teams](media/teams-paste-url.png)
6. <span data-ttu-id="63e6f-130">Fyrsta skiptið sem tengill er límdur í samtal, verður beðið um innskráningu í [!INCLUDE [prodshort](includes/prodshort.md)] og að veita samþykki fyrir forritinu til að sækja gögn.</span><span class="sxs-lookup"><span data-stu-id="63e6f-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prodshort](includes/prodshort.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="63e6f-131">Fylgið einfaldlega leiðbeiningunum á skjánum.</span><span class="sxs-lookup"><span data-stu-id="63e6f-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="63e6f-132">Aðeins þarf að gera þetta skref einu sinni.</span><span class="sxs-lookup"><span data-stu-id="63e6f-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="63e6f-133">Bíðið augnablik á meðan spjald er búið til í skilaboðaglugganum.</span><span class="sxs-lookup"><span data-stu-id="63e6f-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="63e6f-134">Þegar spjaldið birtist skal leita vel og vandlega í innihald þess eftir viðkvæmum upplýsingum áður en skilaboðin eru send.</span><span class="sxs-lookup"><span data-stu-id="63e6f-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="63e6f-135">Þetta skref er mikilvægt vegna þess að þegar skilaboðin eru send geta allir í samtalinu séð spjaldið.</span><span class="sxs-lookup"><span data-stu-id="63e6f-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="63e6f-136">Ef spjaldið lítur vel út skal velja **Senda** til að senda það í samtalið.</span><span class="sxs-lookup"><span data-stu-id="63e6f-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="63e6f-137">Eftir að kortið birtist og áður en **Senda** er valið er hægt að eyða límdri vefslóð ef þú vilt.</span><span class="sxs-lookup"><span data-stu-id="63e6f-137">After the card appears, and before you select **Send** , you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="63e6f-138">Til að skoða frekari upplýsingar eða gera breytingar á færslunni skal velja **Upplýsingar** .</span><span class="sxs-lookup"><span data-stu-id="63e6f-138">To view more details or make changes to the record, select **Details** .</span></span>

    <span data-ttu-id="63e6f-139">Upplýsingasíðan svipar til þess sem þú sérð í [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="63e6f-139">The details page is similar to what you'd see in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="63e6f-140">En það er örlítið aðlagað að Teams.</span><span class="sxs-lookup"><span data-stu-id="63e6f-140">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="63e6f-141">Þegar skoðun er lokið og breytingar hafa verið gerðar skal loka glugganum til að fara aftur í samtalið í Teams.</span><span class="sxs-lookup"><span data-stu-id="63e6f-141">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="63e6f-142">Allar breytingar sem eru gerðar endurspeglast ekki í spjaldinu fyrr en næst þegar tengill þess er límdur í samtal.</span><span class="sxs-lookup"><span data-stu-id="63e6f-142">Any changes you make won't be reflected in the card until the next time you paste its link in a conversation.</span></span>

## <a name="see-also"></a><span data-ttu-id="63e6f-143">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="63e6f-143">See Also</span></span>

[<span data-ttu-id="63e6f-144">Business Central og Microsoft Teams samþættingaryfirlit</span><span class="sxs-lookup"><span data-stu-id="63e6f-144">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="63e6f-145">[Setja upp [!INCLUDE [prodshort](includes/prodshort.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="63e6f-145">[Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="63e6f-146">Þróun fyrir samþættingu Teams</span><span class="sxs-lookup"><span data-stu-id="63e6f-146">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[<span data-ttu-id="63e6f-147">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="63e6f-147">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
