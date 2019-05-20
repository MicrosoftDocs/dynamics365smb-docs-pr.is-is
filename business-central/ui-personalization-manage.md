---
title: Stjórnun sérstillinga sem stjórnandi í Business Central | Microsoft Docs
description: Lærðu hvernig á að aðlaga notendaviðmótið til að henta því hvernig þú vinnur.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 37cdf2d7dcc46b1286cbb7a5ad620547e364309e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250596"
---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="379fb-103">Stjórnun sérstillinga sem stjórnandi</span><span class="sxs-lookup"><span data-stu-id="379fb-103">Managing Personalization as an Administrator</span></span>

<span data-ttu-id="379fb-104"> Notendur geta sérsniðið vinnusvæði sitt að vild.</span><span class="sxs-lookup"><span data-stu-id="379fb-104">Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="379fb-105">Sem stjórnandi stjórnar þú og hefur umsjón með sérstillingum með því að:</span><span class="sxs-lookup"><span data-stu-id="379fb-105">As an administrator, you control and manage personalization by:</span></span>

-   <span data-ttu-id="379fb-106">Kveikja eða slökkva á eiginleika sérstillingar fyrir allt forritið (einungis fyrir uppsetningar á staðnum).</span><span class="sxs-lookup"><span data-stu-id="379fb-106">Enabling or disabling the personalization feature for the entire the application (on-premises installation only).</span></span>
-   <span data-ttu-id="379fb-107">Kveikja eða slökkva á eiginleika sérstillingar fyrir notendur af tilteknum prófíl.</span><span class="sxs-lookup"><span data-stu-id="379fb-107">Enabling or disabling the personalization feature for users of a specific profile.</span></span>
-   <span data-ttu-id="379fb-108">Hreinsa allar sérstillingar á síðu sem notendur hafa gert.</span><span class="sxs-lookup"><span data-stu-id="379fb-108">Clearing any page personalizations that users have made.</span></span>

## <a name="EnablePersonalization"></a><span data-ttu-id="379fb-109">Kveikja eða slökkva á sérstillingum (aðeins á staðnum)</span><span class="sxs-lookup"><span data-stu-id="379fb-109">To enable or disable personalization (On-Premises Only)</span></span>

<span data-ttu-id="379fb-110">Sjálfgefið er að slökkt sé á sérstillingu í biðlaranum.</span><span class="sxs-lookup"><span data-stu-id="379fb-110">By default, personalization is not enabled in the client.</span></span> <span data-ttu-id="379fb-111">Þú kveikir eða slekkur á sérstillingum með því að breyta skilgreiningarskránni (navsettings.json) í tilviki fyrir vefþjón Business Central sem þjónar biðlaranum.</span><span class="sxs-lookup"><span data-stu-id="379fb-111">You enable or disable personalization by modifying the configuration file (navsettings.json) of the Business Central Web Server instance that serves the clients.</span></span>

1. <span data-ttu-id="379fb-112">Til að kveikja á sérstillingum skaltu bæta eftirfarandi línu við navsettings.json skrána:</span><span class="sxs-lookup"><span data-stu-id="379fb-112">To enable personalization, add the following line in the navsettings.json file:</span></span>

    ```
    "PersonalizationEnabled": "true"
    ```

    <span data-ttu-id="379fb-113">Til að slökkva á sérstillingum skaltu fjarlægja þessa línu eða breyta henni í:</span><span class="sxs-lookup"><span data-stu-id="379fb-113">To disable personalization, remove this line or change it to:</span></span>

    ```
    "PersonalizationEnabled": "false"
    ```

    <span data-ttu-id="379fb-114">Nánari upplýsingar um hvernig skuli breyta navsettings.json skránni er að finna í [Breyta navsettings.json skránni beint](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span><span class="sxs-lookup"><span data-stu-id="379fb-114">For more information about how to modify the navsettings.json file, see [Modify the navsettings.json file directly](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span></span>

2. <span data-ttu-id="379fb-115">Búðu til og sæktu táknin fyrir forritið.</span><span class="sxs-lookup"><span data-stu-id="379fb-115">Generate and download the application symbols.</span></span>

    <span data-ttu-id="379fb-116">Þetta skref er valfrjálst og er ekki nauðsynlegt til að kveikja á sérstillingu.</span><span class="sxs-lookup"><span data-stu-id="379fb-116">This step is optional, and not required to enable personalization.</span></span> <span data-ttu-id="379fb-117">Hins vegar tryggir það að þróunaraðilar geti sérstillt nýjar síður sem eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="379fb-117">However, it ensures that new pages that are created by developers can be personalized.</span></span>

    1. <span data-ttu-id="379fb-118">Fyrst eru táknin búin til með því að keyra finsql.exe með `generatesymbolreference` skipuninni.</span><span class="sxs-lookup"><span data-stu-id="379fb-118">First, you generate the symbols by running finsql.exe with `generatesymbolreference` command.</span></span> <span data-ttu-id="379fb-119">Skráin finsql.exe er staðsett í uppsetningarmöppunni fyrir [!INCLUDE[server](includes/server.md)] og Dynamics NAV þróunarumhverfi (CSIDE).</span><span class="sxs-lookup"><span data-stu-id="379fb-119">The finsql.exe file is located in the installation folder for the [!INCLUDE[server](includes/server.md)] and Dynamics NAV Development Environment (CSIDE).</span></span> <span data-ttu-id="379fb-120">Til að búa til táknin skaltu opna skipanakvaðningu, breyta yfir í skráasafnið þar sem skráin er geymd og síðan keyra eftirfarandi skipun:</span><span class="sxs-lookup"><span data-stu-id="379fb-120">To generate the symbols, open a command prompt, change to the directory where the file is store, and the run the following command:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    <span data-ttu-id="379fb-121">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="379fb-121">For example:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    <span data-ttu-id="379fb-122">Frekari upplýsingar er að finna í [Keyra C/SIDE og AL samhliða](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span><span class="sxs-lookup"><span data-stu-id="379fb-122">For more information, see [Running C/SIDE and AL Side-by-Side](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span></span>

    2. <span data-ttu-id="379fb-123">Skilgreindu [!INCLUDE[nav_server_md](includes/nav_server_md.md)] tilvik í **Virkja hleðslu á tilvísunum forritatákna við ræsingu þjóns** (EnableSymbolLoadingAtServerStartup).</span><span class="sxs-lookup"><span data-stu-id="379fb-123">Configure [!INCLUDE[nav_server_md](includes/nav_server_md.md)] instance to **Enable loading application symbol references at server startup** (EnableSymbolLoadingAtServerStartup).</span></span> <span data-ttu-id="379fb-124">Frekari upplýsingar er að finna í [Skilgreining Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span><span class="sxs-lookup"><span data-stu-id="379fb-124">For more information, see [Configuring Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span></span>

## <a name="to-disable-personalization-for-a-profile"></a><span data-ttu-id="379fb-125">Að slökkva á sérstillingu fyrir prófíl</span><span class="sxs-lookup"><span data-stu-id="379fb-125">To disable personalization for a profile</span></span>

<span data-ttu-id="379fb-126">Hægt er að koma í veg fyrir að allir notendur sem tilheyra tiltekinni forstillingu geti sérstillt síður sínar.</span><span class="sxs-lookup"><span data-stu-id="379fb-126">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>

1. <span data-ttu-id="379fb-127">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notandastillingar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="379fb-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="379fb-128">Veljið forstillinguna sem á að breyta í listanum.</span><span class="sxs-lookup"><span data-stu-id="379fb-128">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="379fb-129">Veljið gátreitinn **Afvirkja sérstillingar notanda** og smellið síðan á hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="379fb-129">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="to-clear-user-personalizations"></a><span data-ttu-id="379fb-130">Að hreinsa sérstillingar notanda</span><span class="sxs-lookup"><span data-stu-id="379fb-130">To clear user personalizations</span></span>

<span data-ttu-id="379fb-131">Þegar sérstillingar síðu er eytt fer síðan aftur í upprunalegt útlit áður en sérstillingin var gerð.</span><span class="sxs-lookup"><span data-stu-id="379fb-131">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="379fb-132">Það eru tvær leiðir til að hreinsa sérstillingar sem notendur hafa gert á síðum: með **Eyða sérstillingum notanda** síðunni og **Sérstillingaspjald notanda**.</span><span class="sxs-lookup"><span data-stu-id="379fb-132">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="379fb-133">Að hreinsa sérstillingar notenda með því að nota síðuna Eyða sérstillingum notanda</span><span class="sxs-lookup"><span data-stu-id="379fb-133">To clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="379fb-134">Síðan **Eyða sérstillingum notanda** gerir þér kleift að hreinsa sérstillingar á einstaka síðum, eftir einstaka notendum.</span><span class="sxs-lookup"><span data-stu-id="379fb-134">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1. <span data-ttu-id="379fb-135">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða sérstillingum notanda** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="379fb-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="379fb-136">Á síðunni er listi yfir allar síður sem hafa verið sérstilltar og sem notandinn tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="379fb-136">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="379fb-137">Gátmerki í **Eldri sérstilling** dálknum gefur til kynna að sérstillingin hafi verið gerð í eldri útgáfu af [!INCLUDE[d365fin](includes/d365fin_md.md)], sem meðhöndlaði sérstillingu öðruvísi en er núna gert.</span><span class="sxs-lookup"><span data-stu-id="379fb-137">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="379fb-138">Notendur sem reyna að sérstilla þessar síður eru útilokaðir frá því að gera það nema þeir velji að opna síðuna.</span><span class="sxs-lookup"><span data-stu-id="379fb-138">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="379fb-139">Frekari upplýsingar eru í [Af hverju er síða læst og því ekki hægt að sérsníða hana](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="379fb-139">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="379fb-140">Veljið færsluna sem á að eyða og veljið síðna aðgerðina **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="379fb-140">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="379fb-141">Notandinn mun sjá breytingarnar næst þegar hann skráir sig inn.</span><span class="sxs-lookup"><span data-stu-id="379fb-141">The user will see the changes the next time they sign-in.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="379fb-142">Að hreinsa sérstillingar notenda með því að nota síðuna Sérstillingaspjald notanda</span><span class="sxs-lookup"><span data-stu-id="379fb-142">To clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="379fb-143">Síðan **Sérstillingaspjald notanda** gerir þér kleift að hreinsa sérstillingar á öllum síðum fyrir tiltekinn notanda.</span><span class="sxs-lookup"><span data-stu-id="379fb-143">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="379fb-144">Þetta krefst skrifleyfis fyrir töflu 2000000072 **Forstilling**.</span><span class="sxs-lookup"><span data-stu-id="379fb-144">This requires write permission to Table 2000000072 **Profile**.</span></span>

1. <span data-ttu-id="379fb-145">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sérstillingar notanda** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="379fb-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="379fb-146">Síðan **Sérstillingar notanda** sýnir alla notendur sem hugsanlega hafa sérstillt síður.</span><span class="sxs-lookup"><span data-stu-id="379fb-146">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="379fb-147">Ef þú finnur ekki notanda á listanum þýðir það að hann hefur engar sérstilltar síður.</span><span class="sxs-lookup"><span data-stu-id="379fb-147">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="379fb-148">Veljið notanda af listanum og veljið svo aðgerðina **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="379fb-148">Select the user from the list, and then choose the **Edit** action.</span></span>

3. <span data-ttu-id="379fb-149">Í flipanum **Aðgerðir** veljið **Hreinsa sérstilltar síður**.</span><span class="sxs-lookup"><span data-stu-id="379fb-149">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="379fb-150">Notandinn mun sjá breytingarnar næst þegar hann skráir sig inn.</span><span class="sxs-lookup"><span data-stu-id="379fb-150">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="379fb-151">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="379fb-151">See Also</span></span>
[<span data-ttu-id="379fb-152">Sérstillingar verksvæðis</span><span class="sxs-lookup"><span data-stu-id="379fb-152">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="379fb-153">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="379fb-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="379fb-154">Breyta grundvallarstillingum</span><span class="sxs-lookup"><span data-stu-id="379fb-154">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="379fb-155">Breyting á hvaða eiginleikar eru sýndir</span><span class="sxs-lookup"><span data-stu-id="379fb-155">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
