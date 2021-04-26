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
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: e20208d50eb65f1a92e6661396bf53007ab88eb8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786883"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a><span data-ttu-id="6c4d8-103">Unnið með Business Central Data í Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6c4d8-103">Working with Business Central Data in Microsoft Teams</span></span>

[!INCLUDE [online_only](includes/online_only.md)]

<span data-ttu-id="6c4d8-104">[!INCLUDE [prod_short](includes/prod_short.md)] býður upp á forrit sem tengir Microsoft Teams við viðskiptagögn í [!INCLUDE [prod_short](includes/prod_short.md)] þannig að hægt sé að deila upplýsingum á fjótlegan hátt á meðal teymismeðlima og svara fyrirspurnum með skjótari hætti.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-104">[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="6c4d8-105">Í þessari grein koma fram upplýsingar um hvernig á að nota forritið til að deila [!INCLUDE [prod_short](includes/prod_short.md)]-gögnum með samstarfsfólki í samtali í Teams.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-105">In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] data with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="6c4d8-106">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="6c4d8-106">Overview</span></span>

<span data-ttu-id="6c4d8-107">[!INCLUDE [prod_short](includes/prod_short.md)]-forritið gerir kleift að:</span><span class="sxs-lookup"><span data-stu-id="6c4d8-107">The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:</span></span>

- <span data-ttu-id="6c4d8-108">Afrita tengil í hvaða færslu Business Central sem er og líma hann í spjall á Teams til að deila honum með samstarfsfólki.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="6c4d8-109">Forritið stækkar svo tengilinn í gagnvirkt spjald sem birtir upplýsingar um færsluna.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-109">The app will then expand the link into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="6c4d8-110">Þegar á samtalinu stendur getur þú og samstarfsfólk þitt skoðað frekari upplýsingar um færsluna, breytt gögnum og gripið til aðgerða &mdash; án þess að fara úr Teams.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.</span></span>

<span data-ttu-id="6c4d8-111">[![Samþætting Teams við Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="6c4d8-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6c4d8-112">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="6c4d8-112">Prerequisites</span></span>

- <span data-ttu-id="6c4d8-113">Þú hefur aðgang að Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="6c4d8-114">Þú hefur sett upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið  í Teams.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-114">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="6c4d8-115">Frekari upplýsingar er að finna í [Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="6c4d8-115">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="6c4d8-116">Allir þátttakendur í Teams-spjalli geta skoðað spjöld fyrir færslur Business Central sem þú sendir inn á spjallið.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="6c4d8-117">En til að skoða frekari upplýsingar um færslur með því að nota hnappana **Upplýsingar** eða **Sprettigluggi** á spjaldi, þurfa þeir að fá aðgang að [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c4d8-117">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="6c4d8-118">Nánari upplýsingar er að finna í [Stjórnun Microsoft Teams samþættingar](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="6c4d8-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="6c4d8-119">Hafa með Business Central-spjald í samtali í Teams</span><span class="sxs-lookup"><span data-stu-id="6c4d8-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="6c4d8-120">Skráðu þig inn í [!INCLUDE [prod_short](includes/prod_short.md)] með vafranum.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-120">Sign in to [!INCLUDE [prod_short](includes/prod_short.md)] using your browser.</span></span>
2. <span data-ttu-id="6c4d8-121">Opnið færsluna sem á að deila.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="6c4d8-122">Forritið er hannað til að birta síðu kortagerðar úr [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c4d8-122">The app is designed to display card type pages from [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="6c4d8-123">Opnið því síðu sem sýnir eina færslu, eins og vöru, viðskiptavin eða sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="6c4d8-124">Ekki er hægt að nota hana fyrir hlutverkamiðstöðvar eða síður sem birta nokkrar færslur í lista.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="6c4d8-125">Afritið alla vefslóðina úr veffangastiku vafrans.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Afrita vefslóð Business Central úr vafranum](media/teams-url-v2.png)
4. <span data-ttu-id="6c4d8-127">Farið í Teams og hefjið samtal sem getur verið spjall við einstakling, hóp eða teymisrás.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="6c4d8-128">Límið vefslóðina í skilaboðagluggann þar sem skrifuð eru skilaboð..</span><span class="sxs-lookup"><span data-stu-id="6c4d8-128">Paste the URL in the message box where you compose a message.</span></span>

   ![Líma vefslóð Business Central í Teams](media/teams-paste-url-v2.png)
6. <span data-ttu-id="6c4d8-130">Fyrsta skiptið sem tengill er límdur í samtal, verður beðið um innskráningu í [!INCLUDE [prod_short](includes/prod_short.md)] og að veita samþykki fyrir forritinu til að sækja gögn.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prod_short](includes/prod_short.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="6c4d8-131">Fylgið einfaldlega leiðbeiningunum á skjánum.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6c4d8-132">Aðeins þarf að gera þetta skref einu sinni.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="6c4d8-133">Bíðið augnablik á meðan spjald er búið til í skilaboðaglugganum.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="6c4d8-134">Þegar spjaldið birtist skal leita vel og vandlega í innihald þess eftir viðkvæmum upplýsingum áður en skilaboðin eru send.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="6c4d8-135">Þetta skref er mikilvægt vegna þess að þegar skilaboðin eru send geta allir í samtalinu séð spjaldið.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="6c4d8-136">Ef spjaldið lítur vel út skal velja **Senda** til að senda það í samtalið.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="6c4d8-137">Eftir að kortið birtist og áður en **Senda** er valið er hægt að eyða límdri vefslóð ef þú vilt.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-137">After the card appears, and before you select **Send**, you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="6c4d8-138">Til að fá frekari upplýsingar eða gera breytingar á færslunni sem birtist í spjaldinu skal velja **Upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-138">To view more details or make changes to the record shown in the card, select **Details**.</span></span> <span data-ttu-id="6c4d8-139">Nánari upplýsingar er að finna í næsta hluta.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-139">For more information, see the next section.</span></span>

## <a name="view-card-details"></a><span data-ttu-id="6c4d8-140">Skoða upplýsingar spjalds</span><span class="sxs-lookup"><span data-stu-id="6c4d8-140">View card details</span></span>

<span data-ttu-id="6c4d8-141">Þegar búið er að senda spjald á samtal, geta allir þátttakendur með [viðeigandi heimildir](admin-teams-integration.md#permissions) valið **Upplýsingar** til að opna glugga sem sýnir frekari upplýsingar um færsluna&mdash;og hugsanlega geta gert breytingar á henni.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-141">Once a card's been sent to a conversation, all participants with the [proper permissions](admin-teams-integration.md#permissions) can select **Details** to open a window that displays more information about the record&mdash;and possibly make changes to the record.</span></span> <span data-ttu-id="6c4d8-142">Það skiptir ekki máli hvort það sért þú sem sendir spjaldið eða sá sem fær spjaldið.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-142">It doesn't matter if you're the one sending the card or the one receiving the card.</span></span> <span data-ttu-id="6c4d8-143">Eiginleikinn **Upplýsingar** er sérstaklega gagnlegur viðtakendum af því að hann veitir þeim samanteknar, hnitmiðaðar upplýsingar um færsluna á fljótlegan hátt í stað þess að þurfa að renna yfir alla færsluna.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-143">The **Details** feature is especially useful to recipients, because it quickly provides them with concise, targeted information about the record, as opposed to having to scan the full record.</span></span>

<span data-ttu-id="6c4d8-144">Upplýsingasíðan svipar til þess sem þú sérð í færslunni [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c4d8-144">The details window is similar to what you'd see in [!INCLUDE [prod_short](includes/prod_short.md)] the record.</span></span> <span data-ttu-id="6c4d8-145">En það er örlítið aðlagað að Teams.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-145">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="6c4d8-146">Þegar skoðun er lokið og breytingar hafa verið gerðar skal loka glugganum til að fara aftur í samtalið í Teams.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-146">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

<span data-ttu-id="6c4d8-147">Hér eru nokkur atriði sem vert er að hafa í huga þegar unnið er með upplýsingar spjalds:</span><span class="sxs-lookup"><span data-stu-id="6c4d8-147">Here are a couple things to keep in mind when working with the card details:</span></span>

- <span data-ttu-id="6c4d8-148">Til að opna upplýsingar spjalds verða notendur að vera með heimild á síðunni og gögnum þess í [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c4d8-148">To open the card details, users must have permission on the page and its data in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span>
- <span data-ttu-id="6c4d8-149">Spjöld í Teams-spjalli uppfærast ekki sjálfkrafa þegar gerðar eru breytingar.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-149">Cards in Teams chats aren't automatically updated to changes.</span></span> <span data-ttu-id="6c4d8-150">Allar breytingar sem eru vistaðar í færslu í upplýsingaglugganum eru vistaðar í [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c4d8-150">Any changes you save to a record in the details window are saved in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="6c4d8-151">En spjaldið í Teams sýnir ekki breytingarnar í samtalinu fyrr en tengillinn er límdur inn aftur.</span><span class="sxs-lookup"><span data-stu-id="6c4d8-151">But the card in Teams won't show the changes in the conversion, until you paste the link again.</span></span>

<span data-ttu-id="6c4d8-152">Frekari upplýsingar um hvernig nota á spjöld og upplýsingar spjalds er að finna í [Teams - Algengar spurningar](teams-faq.md).</span><span class="sxs-lookup"><span data-stu-id="6c4d8-152">To learn more about working with cards and card details, see [Teams FAQ](teams-faq.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6c4d8-153">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6c4d8-153">See Also</span></span>

[<span data-ttu-id="6c4d8-154">Business Central og Microsoft Teams samþættingaryfirlit</span><span class="sxs-lookup"><span data-stu-id="6c4d8-154">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="6c4d8-155">[Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="6c4d8-155">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="6c4d8-156">Teams - Algengar spurningar</span><span class="sxs-lookup"><span data-stu-id="6c4d8-156">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="6c4d8-157">Úrræðaleit Teams</span><span class="sxs-lookup"><span data-stu-id="6c4d8-157">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="6c4d8-158">Þróun fyrir samþættingu Teams</span><span class="sxs-lookup"><span data-stu-id="6c4d8-158">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]