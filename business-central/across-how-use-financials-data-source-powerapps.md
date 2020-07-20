---
title: Nota gögn til að stofna forrit| Microsoft Docs
description: Notandi getur gert Business Central gögnin aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til viðskiptaforrit með því að nota Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 06/22/2020
ms.author: edupont
ms.openlocfilehash: 8f0eb7a1562a8300bd7181ef6470c70f60934470
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528639"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="3a3bc-103">Tengjast við Business Central gögnin til að búa til viðskiptaforrit með því að nota Power Apps</span><span class="sxs-lookup"><span data-stu-id="3a3bc-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="3a3bc-104">Notandi getur gert [!INCLUDE[prodshort](includes/prodshort.md)]-gögnin sín aðgengileg sem gagnaveitu í Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-104">You can make your [!INCLUDE[prodshort](includes/prodshort.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="3a3bc-105">Notandi verður að vera með gildan reikning hjá [!INCLUDE[prodshort](includes/prodshort.md)] og hjá Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power Apps.</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-apps"></a><span data-ttu-id="3a3bc-106">Til að bæta [!INCLUDE[prodshort](includes/prodshort.md)] við sem gagnaveitu í Power Apps</span><span class="sxs-lookup"><span data-stu-id="3a3bc-106">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="3a3bc-107">Flettið í [powerapps.microsoft.com](https://powerapps.microsoft.com/) í vafranum og skráið ykkur svo inn.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="3a3bc-108">Á heimasíðunni, í hlutanum **Byrja frá gögnum** skal velja **Aðrir gagnagjafar**.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-108">On the Home page, in the **Start from data** section, choose the **Other data sources** tile.</span></span>  

    <span data-ttu-id="3a3bc-109">Þetta opnar Power Apps Studio.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-109">This opens Power Apps Studio.</span></span> <span data-ttu-id="3a3bc-110">Í fyrstu innskráningu þarf að tilgreina land/svæði.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-110">On first login, you must specify the country/region.</span></span>  
3. <span data-ttu-id="3a3bc-111">Úr lista yfir tiltækar tengingar skal velja **Business Central** og svo hnappinn **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-111">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="3a3bc-112">Power Apps mun tengjast [!INCLUDE[prodshort](includes/prodshort.md)] með því að nota skilríkin sem notandi er skráður inn í með.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-112">Power Apps will connect to your [!INCLUDE[prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="3a3bc-113">Ef þú ert ekki stjórnandi á [!INCLUDE[prodshort](includes/prodshort.md)] þínu þarftu hugsanlega að skrá þig inn með öðrum reikningi.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-113">If you are not an administrator of your [!INCLUDE[prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="3a3bc-114">Power Apps mun birta lista yfir *umhverfi og fyrirtæki* sem eru tiltæk í [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="3a3bc-114">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="3a3bc-115">Velja skal umhverfi og fyrirtækið sem inniheldur gögnin sem á að tengjast við, svo sem *FRAMLEIÐSLA - Fyrirtækið mitt*.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-115">Choose the environment and company that contains the data you want to connect to, such as *PRODUCTION - My Company*.</span></span>  

5. <span data-ttu-id="3a3bc-116">Næst verður settur fram listi yfir töflur sem verða fyrir áhrifum sem hluti af API fyrir umhverfið þitt.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-116">Next, you will be presented with a list of tables that are exposed as part of the API for your environment.</span></span> <span data-ttu-id="3a3bc-117">Velja töfluna sem á að tengjast við og síðan **Tengjast**.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-117">Select the table that you want to connect to, and then choose **Connect**.</span></span>

<span data-ttu-id="3a3bc-118">Þessar svokölluðu töflur verða skráðar sem endastöðvar með [!INCLUDE[prodshort](includes/prodshort.md)] tengli fyrir Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-118">These so-called tables are exposed as endpoints by the [!INCLUDE[prodshort](includes/prodshort.md)] connector for Power Apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="3a3bc-119">Ef þú vilt hafa með gögn úr öðrum töflum í [!INCLUDE[prodshort](includes/prodshort.md)] í forritinu þínu verður þú að vinna með þróunaraðila til að skilgreina sérsniðið API í [!INCLUDE[prodshort](includes/prodshort.md)] og síðan nota þetta sérsniðna API í gegnum sérsniðinn tengil í Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-119">If you want to include data from other tables in [!INCLUDE[prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE[prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="3a3bc-120">Nánari upplýsingar má finna í [Stofna sérsniðin tengi frá grunni](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="3a3bc-120">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="3a3bc-121">Nú hefur þér tekist að tengjast gögnum þínum í [!INCLUDE[prodshort](includes/prodshort.md)] og getur byrjað að byggja upp PowerApp.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-121">At this point, you have successfully connected to your [!INCLUDE[prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="3a3bc-122">Hægt er að bæta við fleiri skjáum og tengjast við fleiri gögn úr [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="3a3bc-122">You can add additional screens and connect to additional data from your [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="3a3bc-123">Frekari upplýsingar er að finna á [Búa til vinnusvæðisforrit úr sniðmáti í Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span><span class="sxs-lookup"><span data-stu-id="3a3bc-123">For more information, see [Create a canvas app from a sample in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span></span>  

<span data-ttu-id="3a3bc-124">Þegar þú hefur hannað og smíðað forritið þitt getur þú deilt því með samstarfsmönnum þínum.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="3a3bc-125">Frekari upplýsingar er að finna á [Vista og birta vinnusvæðisforrit í Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="3a3bc-125">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="3a3bc-126">Ef þú vilt tengjast við [!INCLUDE[prodshort](includes/prodshort.md)] á staðnum verður þú að velja tengilinn **Business Central (á staðnum)** í skrefi 3.</span><span class="sxs-lookup"><span data-stu-id="3a3bc-126">If you want to connect to [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3a3bc-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="3a3bc-127">See Also</span></span>

[<span data-ttu-id="3a3bc-128">Búa til vinnusvæðisforrit úr sniðmáti í Power Apps</span><span class="sxs-lookup"><span data-stu-id="3a3bc-128">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="3a3bc-129">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="3a3bc-129">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="3a3bc-130">[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="3a3bc-130">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="3a3bc-131">Hafist handa við þróun á tengiforritum fyrir Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="3a3bc-131">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
