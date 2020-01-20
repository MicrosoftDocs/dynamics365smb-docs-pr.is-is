---
title: Stofna sandkassaumhverfi| Microsoft Docs
description: Stofna umhverfi þar sem hægt er að kanna, læra, búa til sýni, þróa og prófa.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 12/10/2019
ms.author: solsen
ms.openlocfilehash: 7d189ab6fa5aff518b643c797b7600570fcad43e
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910637"
---
# <a name="creating-a-sandbox-environment-in-include-prodshortincludesprodshortmd"></a><span data-ttu-id="aaf91-103">Búa til sandkassaumhverfi í [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="aaf91-103">Creating a Sandbox Environment in [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

<span data-ttu-id="aaf91-104">Með [!INCLUDE [prodshort](includes/prodshort.md)] geturðu auðveldlega búið til öruggt hverfi þar sem hægt er að prófa, þjálfa eða leysa úr málum án þess að það trufli verkferla eða viðskiptagögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="aaf91-104">With [!INCLUDE [prodshort](includes/prodshort.md)], you can easily create a safe environment where you can test, train, or troubleshoot without disturbing your company's work processes or business data.</span></span> <span data-ttu-id="aaf91-105">Slíkt umhverfi sem ekki er hægt að framleiða í er kallað *sandkassi*.</span><span class="sxs-lookup"><span data-stu-id="aaf91-105">Such a non-production environment is called a *sandbox*.</span></span> <span data-ttu-id="aaf91-106">Sandkassaumhverfi er staðurinn, ótengdur framleiðslu, þar sem hægt er að kanna, læra, búa til sýni, þróa og prófa þjónustuna í öruggu umhverfi án þess að eiga á hættu að hafa áhrif á gögnin eða stillingarnar í framleiðsluumhverfi þínu.</span><span class="sxs-lookup"><span data-stu-id="aaf91-106">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>  

<span data-ttu-id="aaf91-107">Kerfisstjórinn þinn getur búið til sandkassaumhverfi í [Stjórnandamiðstöð](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), en ef þú vilt prófa eitthvað á fljótlegan hátt geturðu búið til sandkassaumhverfi úr [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="aaf91-107">Your administrator can create sandbox environments in the [administration center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), but if you want to quickly test something, you can create a sandbox environment from inside [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>  

> [!NOTE]
> <span data-ttu-id="aaf91-108">Tæknilega séð eru sandkassaumhverfi mjög frábrugðin framleiðsluumhverfi, jafnvel þótt stjórnandi búi til sandkassa sem inniheldur framleiðslugögn.</span><span class="sxs-lookup"><span data-stu-id="aaf91-108">Technically, sandbox environments are very different from production environments, even if your administrator creates a sandbox that includes production data.</span></span> <span data-ttu-id="aaf91-109">Til dæmis er ekki hægt að nota sandkassa fyrir viðmið og ekki er hægt að biðja um útflutning á gagnagrunni.</span><span class="sxs-lookup"><span data-stu-id="aaf91-109">You cannot use a sandbox for benchmarking, and you cannot request a database export, for example.</span></span> <span data-ttu-id="aaf91-110">Ef þú vilt búa til sandkassa sem viðmið getur stjórnandi þinn búið til sérhæft framleiðsluumhverfi í stjórnunarmiðstöðinni.</span><span class="sxs-lookup"><span data-stu-id="aaf91-110">If you want to create a sandbox for benchmarking, your administrator can create a dedicated production environment in the administration center.</span></span> <span data-ttu-id="aaf91-111">Frekari upplýsingar er að finna á [Gerðir umhverfis](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span><span class="sxs-lookup"><span data-stu-id="aaf91-111">For more information, see [Types of environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span></span>

## <a name="to-create-a-sandbox-environment-in-your-include-prodshortincludesprodshortmd"></a><span data-ttu-id="aaf91-112">Til að búa til sandkassaumhverfi í [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="aaf91-112">To create a sandbox environment in your [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

1. <span data-ttu-id="aaf91-113">Skráðu þig inn í þitt framleiðslutilvik af [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="aaf91-113">Sign in to your production instance of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

2. <span data-ttu-id="aaf91-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sandkassaumhverfi** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="aaf91-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="aaf91-115">Veldu hnappinn **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="aaf91-115">Choose the **Create** button.</span></span>  

    <span data-ttu-id="aaf91-116">Annar flipi með [!INCLUDE[d365fin](includes/d365fin_md.md)] opnast svo hægt sé að ljúka uppsetningu á sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="aaf91-116">Another tab with [!INCLUDE[d365fin](includes/d365fin_md.md)] opens where you can finish the setup of your sandbox environment.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="aaf91-117">Ef þú ert með sprettigluggavörn virka í vafranum, skaltu breyta henni þannig að vefslóðir frá \*.businesscentral.dynamics.com aðsetrinu verði leyfðar.</span><span class="sxs-lookup"><span data-stu-id="aaf91-117">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>

<span data-ttu-id="aaf91-118">Þegar sandkassaumhverfið er tilbúið, verður þér beint inn á leiðsagnarforrit sandkassaumhverfisins.</span><span class="sxs-lookup"><span data-stu-id="aaf91-118">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

<span data-ttu-id="aaf91-119">Þú getur valið hnappinn **Frekari upplýsingar** til að lesa um þróunardæmi sem hægt er að prófa í sandkassaumhverfinu eða veldu hnappinn **Loka** til að halda áfram í Mínu hlutverki í [!INCLUDE[d365fin](includes/d365fin_md.md)] sandkassatilvikinu þínu.</span><span class="sxs-lookup"><span data-stu-id="aaf91-119">You can choose the **Learn more** button to read about developer scenarios that you can try in a sandbox environment or choose the **Close** button to continue to the Role Center of your [!INCLUDE[d365fin](includes/d365fin_md.md)] sandbox instance.</span></span>

<span data-ttu-id="aaf91-120">Efst í Hlutverkamiðstöðinni birtist tilkynning til að upplýsa þig um að þetta sé sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="aaf91-120">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="aaf91-121">Einnig er hægt að sjá um hvaða gerð af umhverfi er að ræða í titilstiku biðlarans.</span><span class="sxs-lookup"><span data-stu-id="aaf91-121">You can also see the type of the environment in the title bar of the client.</span></span>
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> <span data-ttu-id="aaf91-122">Sandkassaumhverfi sem er búið til á þennan hátt inniheldur aðeins sjálfgefin sýnigögn fyrir fyrirtækið CRONUS.</span><span class="sxs-lookup"><span data-stu-id="aaf91-122">A sandbox environment created in this way only contains the default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="aaf91-123">Engin gögn eru afrituð eða yfirhöfuð flutt frá framleiðsluumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="aaf91-123">No data is copied or otherwise transferred from the production environment.</span></span><br /><br />
> <span data-ttu-id="aaf91-124">Einnig er hægt að búa til sandkassaumhverfi sem inniheldur framleiðslugögnin.</span><span class="sxs-lookup"><span data-stu-id="aaf91-124">You can also create a sandbox environment containing the production data.</span></span> <span data-ttu-id="aaf91-125">Þetta þarf að gera í gegnum stjórnendamiðstöðina.</span><span class="sxs-lookup"><span data-stu-id="aaf91-125">You must do this through the administration center.</span></span> <span data-ttu-id="aaf91-126">Frekari upplýsingar eru í [Stjórnun umhverfa](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) í þróunar- og IT-pro hjálpinni.</span><span class="sxs-lookup"><span data-stu-id="aaf91-126">For more information, see [Managing Environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in the Developer and IT-Pro help.</span></span>

<span data-ttu-id="aaf91-127">Alltaf er hægt að fara til baka á **Sandkassaumhverfi** síðuna og endurstilla sandkassaumhverfið.</span><span class="sxs-lookup"><span data-stu-id="aaf91-127">At any time, you can return to the **Sandbox Environment** page, and reset the sandbox environment.</span></span>

> [!NOTE]  
> <span data-ttu-id="aaf91-128">Endurstilling sandkassaumhverfisins mun eyða því algerlega og síðan stofna það á ný með sjálfgefnum sýnigögnum.</span><span class="sxs-lookup"><span data-stu-id="aaf91-128">Resetting the sandbox environment will remove it completely, and then create it again with the default demonstration data.</span></span>  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

<span data-ttu-id="aaf91-129">Stjórnandi eða annar notandi getur að takmarkað eða jafnvel hindrað aðganga sumra notenda að sandkassaumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="aaf91-129">An administrator can limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="aaf91-130">Þetta er hægt að gera með því að nota staðlaða öryggiseiginleika vörunnar, eins og t.d. Notandakort, Notendaflokkar og Heimildasamstæður.</span><span class="sxs-lookup"><span data-stu-id="aaf91-130">This can be done by using the standard security features of the product, such as the User card, user groups, and permission sets.</span></span> <span data-ttu-id="aaf91-131">Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="aaf91-131">For more information, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="aaf91-132">Ítarleg virkni í sandkassaumhverfinu</span><span class="sxs-lookup"><span data-stu-id="aaf91-132">Advanced Functionality in the Sandbox Environment</span></span>

<span data-ttu-id="aaf91-133">Sandkassaumhverfið er ekki síst gagnlegt vegna þess að það felur í sér nokkra handhægan eiginleika.</span><span class="sxs-lookup"><span data-stu-id="aaf91-133">The sandbox environment is not least useful because it includes a couple of handy features.</span></span>

### <a name="designer"></a><span data-ttu-id="aaf91-134">Hönnuður</span><span class="sxs-lookup"><span data-stu-id="aaf91-134">Designer</span></span>

<span data-ttu-id="aaf91-135">Í sandkassaumhverfi er kveikt á **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="aaf91-135">In a sandbox environment, you will find the **Designer** enabled.</span></span> <span data-ttu-id="aaf91-136">Hægt er að virkja Hönnuð með því að velja hönnunartáknið ![Hönnuður](./media/across-sandbox/sandbox-inclient-design-icon.png) á síðu eða með því að velja **Hanna** valmyndaratriðið í stillingavalmyndinni ![Stillingar](media/ui-experience/settings_icon_small.png).</span><span class="sxs-lookup"><span data-stu-id="aaf91-136">You can activate Designer by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page, or by choosing the **Design** menu item in the ![Settings](media/ui-experience/settings_icon_small.png) Settings menu.</span></span>

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a><span data-ttu-id="aaf91-137">Gera ítarlega notandaupplifun virka</span><span class="sxs-lookup"><span data-stu-id="aaf91-137">To enable the advanced user experience</span></span>
<span data-ttu-id="aaf91-138">Mögulegt er að opna fyrir og prófa fulla virkni af staðalútgáfu [!INCLUDE[d365fin](includes/d365fin_md.md)] í sandkassa leigjanda með því að stilla **Upplifun** reitinn á **Upplýsingar um fyrirtæki** síðunni.</span><span class="sxs-lookup"><span data-stu-id="aaf91-138">It is possible to enable and try the full functionality of the standard version of [!INCLUDE[d365fin](includes/d365fin_md.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page.</span></span>

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

<span data-ttu-id="aaf91-139">Eftir að þú hefur opnað fyrir notendaupplifunina *Premium*, færðu aðgang að öllum stöðluðu forstillingunum (hlutverkum) og Mitt hlutverk í stöðluðu útgáfunni.</span><span class="sxs-lookup"><span data-stu-id="aaf91-139">After you have enabled the *Premium* user experience, you get access to all the standard profiles (roles) and Role Centers in the standard version.</span></span> <span data-ttu-id="aaf91-140">Einnig er hægt að stofna matsfyrirtæki sem er að fullu uppsett, með sýnigögnum og aðgangi að ítarlegri svæðum vörunnar.</span><span class="sxs-lookup"><span data-stu-id="aaf91-140">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span> <span data-ttu-id="aaf91-141">Að öðrum kosti er hægt að hafa samskipti við endursöluaðila til að fá sýniútgáfu af þeim eiginleikum.</span><span class="sxs-lookup"><span data-stu-id="aaf91-141">Alternatively, contact a reselling partner for a demonstration of the capabilities.</span></span> <span data-ttu-id="aaf91-142">Nánari upplýsingar er að finna í [Hvernig finn ég endursöluaðila?](across-faq.md#findpartner).</span><span class="sxs-lookup"><span data-stu-id="aaf91-142">For more information, see [How do I find a reselling partner?](across-faq.md#findpartner).</span></span>  

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->

## <a name="see-also"></a><span data-ttu-id="aaf91-143">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="aaf91-143">See Also</span></span>

<span data-ttu-id="aaf91-144">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="aaf91-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="aaf91-145">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Prufuútgáfa og áskrift](across-preview.md)</span><span class="sxs-lookup"><span data-stu-id="aaf91-145">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Trials and Subscriptions](across-preview.md)</span></span>  
[<span data-ttu-id="aaf91-146">Stjórnun umhverfis í stjórnunarmiðstöð Business Central</span><span class="sxs-lookup"><span data-stu-id="aaf91-146">Managing Environments in the Business Central administration center</span></span>](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
