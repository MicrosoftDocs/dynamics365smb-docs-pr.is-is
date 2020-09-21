---
title: Setja upp viðbætur til að sérstilla Business Central | Microsoft Docs
description: Kynntu þér hvernig skal bæta virkni og sérstilla Business Central með því að setja upp viðbætur.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765922"
---
# <a name="customizing-business-central-using-extensions"></a><span data-ttu-id="d0f67-103">Sérstilling Business Central með viðbótum</span><span class="sxs-lookup"><span data-stu-id="d0f67-103">Customizing Business Central Using Extensions</span></span>

<span data-ttu-id="d0f67-104">Þú getur breytt [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að setja viðbætur sem bæta við virkni, breyta hegðun eða gefa þér aðgang að nýjum netþjónustu, til dæmis.</span><span class="sxs-lookup"><span data-stu-id="d0f67-104">You can change [!INCLUDE[d365fin](includes/d365fin_md.md)] by installing extensions that add functionality, changes behavior, or gives you access to new online services, for example.</span></span>

> [!NOTE]
> <span data-ttu-id="d0f67-105">Til að setja upp viðbætur frá AppSource eða bæta við viðbótum fyrir hvern leigjanda fyrir sig eru réttar heimildir nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="d0f67-105">To install extensions from AppSource or add per-tenant extensions, you must have the right permissions.</span></span> <span data-ttu-id="d0f67-106">Annaðhvort verður þú að vera aðili að notendaflokknum D365 EXTENSION MGMT eða vera með heimildasamstæðu D365 EXTENSION MGMT.</span><span class="sxs-lookup"><span data-stu-id="d0f67-106">You must either be a member of the D365 EXTENSION MGMT user group or you must have the D365 EXTENSION MGMT permission set.</span></span> <span data-ttu-id="d0f67-107">Ef þú ert stjórnandi geturðu úthlutað notendaflokkum og heimildum til annarra notenda fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="d0f67-107">If you are an administrator, you can assign user groups and permissions to other users in your company.</span></span><br /><br />
<span data-ttu-id="d0f67-108">Til að nota virkni sem viðbót býður upp á, t.d. opna síður, keyra skýrslur, velja aðgerðir o.s.frv., verður þú að hafa fengið heimildasamstæðunum úthlutað sem settar eru upp sem hluti viðbótarinnar.</span><span class="sxs-lookup"><span data-stu-id="d0f67-108">To use the functionality that is provided by an extension, such as opening pages, running reports, selecting actions, and so on, you must be assigned the permission sets that are installed as part of the extension.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="d0f67-109">Uppfærsla viðbóta á leigjanda og uppsetning AppSource viðbóta er ekki studd í gegnum **Viðbótastjórnun** síðu fyrir uppsetningar á forútgáfu.</span><span class="sxs-lookup"><span data-stu-id="d0f67-109">The upload of per-tenant extensions and the installation of AppSource extensions is not supported through the **Extension Management** page for on-premise installations.</span></span>

<span data-ttu-id="d0f67-110">Þegar þú fyrst ræsir [!INCLUDE[d365fin](includes/d365fin_md.md)], eru nokkrar viðbætur þegar settar upp fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="d0f67-110">When you first launch [!INCLUDE[d365fin](includes/d365fin_md.md)], some extensions are already installed for you.</span></span> <span data-ttu-id="d0f67-111">Með tímanum verða fleiri viðbætur tiltækar fyrir þig, og þú getur síðan valið hvort þú viljir nota viðbótina eða ekki.</span><span class="sxs-lookup"><span data-stu-id="d0f67-111">Over time, more extensions will be made available to you, and you can then choose if you want to use the extension or not.</span></span>

<span data-ttu-id="d0f67-112">Til dæmis veitir Microsoft viðbót sem veitir samþættingu við PayPal Payments Standard.</span><span class="sxs-lookup"><span data-stu-id="d0f67-112">For example, Microsoft provides an extension that provides integration with PayPal Payments Standard.</span></span> <span data-ttu-id="d0f67-113">Þessi viðbót er uppsett sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="d0f67-113">This extension is installed by default.</span></span>
<span data-ttu-id="d0f67-114">En ef önnur viðbót er gerð sem veitir samþættingu við aðra greiðsluþjónusta, geturðu sett inn nýja viðbót og síðan valið hvaða af þessum tveimur þjónustum þú notar.</span><span class="sxs-lookup"><span data-stu-id="d0f67-114">But if another extension is made available that offers integration with another payment service, you can install the new extension and then choose which of the two services to use.</span></span>  

<span data-ttu-id="d0f67-115">Þú stjórnar viðbótum á síðunni **viðbótastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="d0f67-115">You manage the extensions on the **Extension Management** page.</span></span> <span data-ttu-id="d0f67-116">Hægt er að opna þessa síðu úr heimasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="d0f67-116">You can access this page from Home.</span></span> <span data-ttu-id="d0f67-117">Einnig er hægt að velja **Leita að síðu eða skýrslu** táknið ![Ljósaperu sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") efst í hægra horninu, slá inn **Viðbætur** og velja svo tengda hlekkinn.</span><span class="sxs-lookup"><span data-stu-id="d0f67-117">Alternatively, choose the **Search for Page or Report** icon ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") in the top right corner, enter **Extension**, and then choose the related link.</span></span> <span data-ttu-id="d0f67-118">Nánari upplýsingar eru í [Uppsetning og fjarlæging viðbóta](ui-extensions-install-uninstall.md).</span><span class="sxs-lookup"><span data-stu-id="d0f67-118">For more information, see [Installing and Uninstalling Extensions](ui-extensions-install-uninstall.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="d0f67-119">Ef þú telur að þú ættir að hafa aðgang að viðbót en finnur ekki virknina sem í henni felst, skaltu athuga síðuna **Viðbótarstjórnun** - ef viðbótin er ekki skráð þar getur þú sett hana upp eins og lýst er í eftirfarandi kafla.</span><span class="sxs-lookup"><span data-stu-id="d0f67-119">If you think you should have access to an extension but you cannot find its functionality, check the **Extension Management** page - if the extension is not listed there, you can install it as described in the following section.</span></span>  

> [!NOTE]  
> <span data-ttu-id="d0f67-120">Nýjar viðbætur eru ekki tiltækar í AppSource strax eftir að við tilkynnum um uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="d0f67-120">New extensions are not available in AppSource immediately after we announce an update.</span></span> <span data-ttu-id="d0f67-121">Þú getur fylgst með viðbótum á [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span><span class="sxs-lookup"><span data-stu-id="d0f67-121">You can keep an eye out for the extensions at  [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span></span>

## <a name="see-also"></a><span data-ttu-id="d0f67-122">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d0f67-122">See Also</span></span>

[<span data-ttu-id="d0f67-123">Stækka Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="d0f67-123">Extending Dynamics 365 Business Central</span></span>](about-develop-extensions.md)  
[<span data-ttu-id="d0f67-124">Microsoft Business Central viðbætur frá öðrum veitum</span><span class="sxs-lookup"><span data-stu-id="d0f67-124">Business Central Extensions by Other Providers</span></span>](ui-extensions-other.md)  
[<span data-ttu-id="d0f67-125">Setja upp Envestnet Yodlee Bank Feeds þjónustuna</span><span class="sxs-lookup"><span data-stu-id="d0f67-125">Set Up the Envestnet Yodlee Bank Feeds Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="d0f67-126">Virkja greiðslur viðskiptamanna gegnum PayPal</span><span class="sxs-lookup"><span data-stu-id="d0f67-126">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md)  
[<span data-ttu-id="d0f67-127">Yfirfæra viðskiptagögn úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="d0f67-127">Migrating Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="d0f67-128">Setja upp GetAddress.io UK Postal Code viðbótina</span><span class="sxs-lookup"><span data-stu-id="d0f67-128">Setting Up the GetAddress.io UK Postal Code extension</span></span>](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
<span data-ttu-id="d0f67-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] Viðbætur frá öðrum veitum](ui-extensions-other.md)</span><span class="sxs-lookup"><span data-stu-id="d0f67-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] Extensions by Other Providers](ui-extensions-other.md)</span></span>  
[<span data-ttu-id="d0f67-130">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="d0f67-130">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
