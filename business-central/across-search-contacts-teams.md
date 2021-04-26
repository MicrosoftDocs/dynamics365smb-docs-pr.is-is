---
title: Leitar að tengiliðum með úr Microsoft Teams
description: Kynntu þér hvernig á að fletta upp Business Central viðskiptavinum, lánardrottnum og öðrum tengiliðum úr Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, contacts, search, messaging extensions
ms.date: 04/12/2021
ms.author: jswymer
ms.openlocfilehash: 77108cab69a05165616ad5e1a44f1a3ddc9d4cd9
ms.sourcegitcommit: e13b80d4e5141f414109e660e0918eae561acb36
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882493"
---
# <a name="searching-for-customers-vendors-and-other-contacts-from-microsoft-teams"></a><span data-ttu-id="08124-103">Leitar að viðskiptavinum, lánardrottnum og öðrum tengiliðum úr Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="08124-103">Searching for Customers, Vendors, and Other Contacts from Microsoft Teams</span></span>

<span data-ttu-id="08124-104">[!INCLUDE [online_only](includes/online_only.md)].</span><span class="sxs-lookup"><span data-stu-id="08124-104">[!INCLUDE [online_only](includes/online_only.md)].</span></span> <span data-ttu-id="08124-105">Kynnt í útgáfutímabili 1 fyrir 2021.</span><span class="sxs-lookup"><span data-stu-id="08124-105">Introduced in 2021 release wave 1.</span></span>

<span data-ttu-id="08124-106">[!INCLUDE [prod_short](includes/prod_short.md)] er með alhliða stjórnkerfi viðskiptatengiliða sem er nauðsynlegt fyrir notendur í hlutverki sölu eða aðgerða eða öðru hlutverki innan deildar.</span><span class="sxs-lookup"><span data-stu-id="08124-106">[!INCLUDE [prod_short](includes/prod_short.md)] has a comprehensive business contact management system that is essential for users in sales, operations, or other departmental roles.</span></span> <span data-ttu-id="08124-107">Ef þú ert notandi í einhverju þessara hlutverka þarftu oft að fletta upp, hittast eða hefja samtal við lánardrottna, viðskiptavini og aðra tengiliði.</span><span class="sxs-lookup"><span data-stu-id="08124-107">If you're a user in one of these roles, you'll often need to look up, meet, or start a conversation with your vendors, customers, and other contacts.</span></span> <span data-ttu-id="08124-108">Með [!INCLUDE [prod_short](includes/prod_short.md)]-forritinu fyrir Teams er hægt að vinna þessi verk beint úr Teams án þess að skipta yfir í [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="08124-108">With the [!INCLUDE [prod_short](includes/prod_short.md)] app for Teams, you can do these tasks directly from Teams, without having to switch to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="08124-109">Innan Teams er hægt að:</span><span class="sxs-lookup"><span data-stu-id="08124-109">From within Teams, you can:</span></span>

- <span data-ttu-id="08124-110">Fletta upp á [!INCLUDE [prod_short](includes/prod_short.md)]-tengiliðum í skipanareit Teams eða skrifgluggasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="08124-110">Look up [!INCLUDE [prod_short](includes/prod_short.md)] contacts from the Teams command box or from the message compose area.</span></span> <span data-ttu-id="08124-111">Tengiliðir geta verið hugsanlegir kaupendur, lánardrottnar, viðskiptavinir eða annars konar viðskiptatengsl.</span><span class="sxs-lookup"><span data-stu-id="08124-111">Contacts can include prospects, vendors, customers, or other business relationships.</span></span>
- <span data-ttu-id="08124-112">Deila tengilið sem spjaldi í spjalli á Teams.</span><span class="sxs-lookup"><span data-stu-id="08124-112">Share a contact as a card in a Teams conversation.</span></span>
- <span data-ttu-id="08124-113">Skoða tengiliðaupplýsingar nánar, samskiptasögu og annars konar innsýn eins og útistandandi greiðslur eða opin skjöl.</span><span class="sxs-lookup"><span data-stu-id="08124-113">View details about contact information, interaction history, and other insights like outstanding payments or open documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="08124-114">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="08124-114">Prerequisites</span></span>

- <span data-ttu-id="08124-115">Þú hefur aðgang að Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="08124-115">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="08124-116">Þú hefur sett upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið  í Teams.</span><span class="sxs-lookup"><span data-stu-id="08124-116">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="08124-117">Frekari upplýsingar er að finna í [Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="08124-117">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>
- <span data-ttu-id="08124-118">Þú ert [!INCLUDE [prod_short](includes/prod_short.md)] með reikning með aðgangi að tengiliðum í a.m.k. einu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="08124-118">You've got a [!INCLUDE [prod_short](includes/prod_short.md)] account with access to contacts in at least one company.</span></span>

> [!NOTE]
> <span data-ttu-id="08124-119">Hvort sem leitað er í skipanareitnum eða skrifglugganum, gæti verið beðið um innskráningu eða setja upp forritið í fyrsta skiptið.</span><span class="sxs-lookup"><span data-stu-id="08124-119">Whether you searching from the command box or message compose box, you may be asked to sign in or set up the app the first time.</span></span> <span data-ttu-id="08124-120">Þetta skref er nauðsynlegt til að leita að tengiliðum í Business Central fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="08124-120">This step is necessary to search for contacts in the right Business Central company.</span></span> <span data-ttu-id="08124-121">Frekari upplýsingar um uppsetningu forritsins til að velja fyrirtækið er að finna í [Breyta fyrirtæki og öðrum stillingum í Teams](across-teams-settings.md).</span><span class="sxs-lookup"><span data-stu-id="08124-121">For information about setting up the app to choose your company, see [Changing Company and Other Settings in Teams](across-teams-settings.md).</span></span>

## <a name="look-up-contacts-from-the-command-box"></a><span data-ttu-id="08124-122">Fletta upp tengiliðum úr skipanareitnum</span><span class="sxs-lookup"><span data-stu-id="08124-122">Look up contacts from the command box</span></span>

<span data-ttu-id="08124-123">Skipanareiturinn er efst á hverjum skjá í Teams.</span><span class="sxs-lookup"><span data-stu-id="08124-123">The command box is at the top of every screen in Teams.</span></span> <span data-ttu-id="08124-124">Hann gerir notendum kleift að leita, nota flýtiaðgerðir eða ræsa forrit eins og [!INCLUDE [prod_short](includes/prod_short.md)] forritið.</span><span class="sxs-lookup"><span data-stu-id="08124-124">It lets you search, take quick actions, or launch apps, like the [!INCLUDE [prod_short](includes/prod_short.md)] app.</span></span> <span data-ttu-id="08124-125">Að leita úr skipanareitnum er frábær leið til að fletta upp tengiliðum og gögnum tengdum þeim á fljótlegan hátt til eigin nota.</span><span class="sxs-lookup"><span data-stu-id="08124-125">Searching from the command box is great for quickly looking up contacts and their related data for your own use.</span></span> <span data-ttu-id="08124-126">Til dæmis ef ætlunin er að fletta upp netfangi lánardrottins til að setja upp fund í dagatali.</span><span class="sxs-lookup"><span data-stu-id="08124-126">For example, suppose you want to look up an email address of a vendor to set up a calendar meeting.</span></span> <span data-ttu-id="08124-127">Eða kannski er ætlunin að fletta upp samskiptasögu á miðjum fundi við viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="08124-127">Or maybe you want to look up interaction history during a meeting with a customer.</span></span>

1. <span data-ttu-id="08124-128">Í skipanareitnum skal slá inn **@Business Central**, síðan velja Business Central-forritið úr niðurstöðunum.</span><span class="sxs-lookup"><span data-stu-id="08124-128">In the command box, type **@Business Central**, then select the Business Central app from the results.</span></span>

    ![Opna Business Central forrit til að leita að tengiliðum úr skipanareit](media/teams-contacts-command-1.png)

2. <span data-ttu-id="08124-130">Í reitinn **Business Central** skal slá inn leitartexta eins og heiti, aðsetur eða símanúmer.</span><span class="sxs-lookup"><span data-stu-id="08124-130">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="08124-131">Samsvarandi niðurstöður birtast við innslátt.</span><span class="sxs-lookup"><span data-stu-id="08124-131">As you type, matching results will appear.</span></span>

    ![Leita að tengiliðum Business Central úr skipanareit Teams](media/teams-contacts-command-2.png)
3. <span data-ttu-id="08124-133">Velja skal tengilið úr niðurstöðunum.</span><span class="sxs-lookup"><span data-stu-id="08124-133">Select a contact from the results.</span></span>

    <span data-ttu-id="08124-134">Tengiliðaspjaldið birtist fyrir neðan skipanareitinn.</span><span class="sxs-lookup"><span data-stu-id="08124-134">The contact card appears beneath the command box.</span></span>

4. <span data-ttu-id="08124-135">Ef á að bæta tengiliðaspjaldinu við samtal skal fara efst í hægra horn spjaldsins, velja **... (Fleiri valkostir)** > **Afrita**.</span><span class="sxs-lookup"><span data-stu-id="08124-135">If you want to add the contact card into a conversation, go to the upper right corner of the card, select **... (More options)** > **Copy**.</span></span> <span data-ttu-id="08124-136">Því næst skal líma afritið í skrifglogga skilaboða í samtali.</span><span class="sxs-lookup"><span data-stu-id="08124-136">Then, paste the copy in the message compose box of a conversation.</span></span>  

<span data-ttu-id="08124-137">Almennari upplýsingar um skipanareit Teams er að finna í [Teams - Notaðu skipanareitinn](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span><span class="sxs-lookup"><span data-stu-id="08124-137">For more general information about the command box in Teams, see [Teams - Use the command box](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span></span>

## <a name="look-up-contacts-from-the-message-compose-box"></a><span data-ttu-id="08124-138">Fletta upp tengiliðum úr skrifglugga skilaboða</span><span class="sxs-lookup"><span data-stu-id="08124-138">Look up contacts from the message compose box</span></span>

<span data-ttu-id="08124-139">Kosturinn við að nota skrifglugga skilaboða er sá að hægt er að bæta tengiliðaspjaldi við samtal með beinum hætti þannig að aðrir geti séð það.</span><span class="sxs-lookup"><span data-stu-id="08124-139">The advantage of using the message compose box is that you can add a contact card directly to a conversation, for others to see.</span></span>

1. <span data-ttu-id="08124-140">Fyrir neðan skrifglugga skilaboða skal velja **Business Central** táknið til að ræsa forritið.</span><span class="sxs-lookup"><span data-stu-id="08124-140">Beneath to message compose box, select the **Business Central** icon to launch the app.</span></span>

    <span data-ttu-id="08124-141">Ef tákn **Business Central** sést ekki skal velja **... (Viðbætur fyrir skilaboð)**.</span><span class="sxs-lookup"><span data-stu-id="08124-141">If you don't see the **Business Central** icon, select **... (Messaging extensions)**.</span></span>

    ![Opna forrit Business Central til að leita að tengiliðum úr skilaboðaglugga](media/teams-contacts-message-box.png)

2. <span data-ttu-id="08124-143">Í reitinn **Business Central** skal slá inn leitartexta eins og heiti, aðsetur eða símanúmer.</span><span class="sxs-lookup"><span data-stu-id="08124-143">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="08124-144">Samsvarandi niðurstöður birtast við innslátt.</span><span class="sxs-lookup"><span data-stu-id="08124-144">As you type, matching results will appear.</span></span>

    ![Leita að tengiliðum Business Central úr skilaboðaglugga](media/teams-contacts-5.png)
3. <span data-ttu-id="08124-146">Velja skal tengilið úr niðurstöðunum.</span><span class="sxs-lookup"><span data-stu-id="08124-146">Select a contact from the results.</span></span>

    <span data-ttu-id="08124-147">Tengiliðaspjaldið birtist í skrifglugga skilaboða.</span><span class="sxs-lookup"><span data-stu-id="08124-147">The contact card appears in the message compose box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="08124-148">Tengiliðaspjaldið er ekki sent strax í spjallið þannig að aðrir geti séð það.</span><span class="sxs-lookup"><span data-stu-id="08124-148">The contact card isn't sent to the conversation right away for others to see.</span></span> <span data-ttu-id="08124-149">Tækifæri gefst til að yfirfara innihald spjaldsins og bæta við texta fyrir eða eftir það að eigin vild.</span><span class="sxs-lookup"><span data-stu-id="08124-149">You have the opportunity to review the contents of the card, and add text before or after it as you like.</span></span> <span data-ttu-id="08124-150">Því næst skal senda skilaboðin á spjallið þegar þau eru tilbúin.</span><span class="sxs-lookup"><span data-stu-id="08124-150">Then, send your message to the chat when ready.</span></span>

### <a name="heres-another-way"></a><span data-ttu-id="08124-151">Hér er önnur leið</span><span class="sxs-lookup"><span data-stu-id="08124-151">Here's another way</span></span>

1. <span data-ttu-id="08124-152">Í stað þess að nota tákn **Business Central** skal slá **@Business Central** beint inn í skrifglugga skilaboða.</span><span class="sxs-lookup"><span data-stu-id="08124-152">Instead of using the **Business Central** icon, type **@Business Central** directly in the message compose box.</span></span>
2. <span data-ttu-id="08124-153">Sláið inn leitarorð í reitinn.</span><span class="sxs-lookup"><span data-stu-id="08124-153">Enter your search terms in the box.</span></span>
3. <span data-ttu-id="08124-154">Notaðu upp og niður örvalyklana á lyklaborðinu til að velja tengilið, ýtið því næst á Enter til að velja hann.</span><span class="sxs-lookup"><span data-stu-id="08124-154">Use the up and down arrow keys on the keyboard to choose a contact, then press Enter to select it.</span></span>

## <a name="viewing-contact-card-details"></a><span data-ttu-id="08124-155">Upplýsingar tengiliðaspjalds skoðaðar</span><span class="sxs-lookup"><span data-stu-id="08124-155">Viewing contact card details</span></span>

<span data-ttu-id="08124-156">Tengiliðaspjaldið í Teams býður upp á flýtiyfirlit yfir viðskiptavin, lánardrottin eða tengilið.</span><span class="sxs-lookup"><span data-stu-id="08124-156">The contact card in Teams gives you a quick overview of the customer, vendor, or contact.</span></span> <span data-ttu-id="08124-157">Spjaldið er gagnvirkt&mdash;sem þýðir að hægt er að skoða frekari upplýsingar eða jafnvel breyta tengilið með því að nota hnappana **Upplýsingar** eða **Aðskilinn gluggi**.</span><span class="sxs-lookup"><span data-stu-id="08124-157">The card is interactive&mdash;meaning you can view more information or even modify a contact by using the **Details** or **Pop-out** buttons.</span></span>

<span data-ttu-id="08124-158">Hnappurinn **Upplýsingar** opnar glugga innan Teams sem sýnir frekari upplýsingar um tengiliðinn, en ekki eins miklar og hægt er að sjá í [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="08124-158">The **Details** button opens a window within Teams that displays more information about the contact, but not as much as you'd see in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="08124-159">Til að sjá allar upplýsingar um tengilið í [!INCLUDE [prod_short](includes/prod_short.md)] skal velja **Aðskilinn gluggi**.</span><span class="sxs-lookup"><span data-stu-id="08124-159">To see all the information about a contact in [!INCLUDE [prod_short](includes/prod_short.md)], select **Pop-out**.</span></span>

<span data-ttu-id="08124-160">Tengiliðaspjaldið virkar alveg eins og spjöld fyrir færslur eins og vörur, viðskiptavini eða sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="08124-160">The contact card works just like cards for records, like items, customers, or sales orders.</span></span> <span data-ttu-id="08124-161">Frekari upplýsingar um kort er að finna í [Skoða upplýsingar spjalds](across-working-with-teams.md#view-card-details).</span><span class="sxs-lookup"><span data-stu-id="08124-161">For more information about cards, see [View card details](across-working-with-teams.md#view-card-details).</span></span>

> [!NOTE]
> <span data-ttu-id="08124-162">Allir þátttakendur í Teams-spjalli geta skoðað spjöld fyrir Business Central tengilið sem er sendur á spjallið.</span><span class="sxs-lookup"><span data-stu-id="08124-162">All participants in a Teams conversation will be able to view cards for Business Central contact that you submit to a conversation.</span></span> <span data-ttu-id="08124-163">En til að skoða frekari upplýsingar um færslur með því að nota hnappana **Upplýsingar** eða **Sprettigluggi** á spjaldi, þurfa þeir að fá aðgang að [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="08124-163">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="08124-164">Nánari upplýsingar er að finna í [Stjórnun Microsoft Teams samþættingar](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="08124-164">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="see-also"></a><span data-ttu-id="08124-165">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="08124-165">See Also</span></span>

[<span data-ttu-id="08124-166">Business Central og Microsoft Teams samþættingaryfirlit</span><span class="sxs-lookup"><span data-stu-id="08124-166">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="08124-167">[Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="08124-167">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="08124-168">Teams - Algengar spurningar</span><span class="sxs-lookup"><span data-stu-id="08124-168">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="08124-169">Úrræðaleit Teams</span><span class="sxs-lookup"><span data-stu-id="08124-169">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="08124-170">Þróun fyrir samþættingu Teams</span><span class="sxs-lookup"><span data-stu-id="08124-170">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]