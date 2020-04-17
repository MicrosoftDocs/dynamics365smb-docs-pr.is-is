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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: f6b771b0107214702785d2b124983eb369741a84
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187917"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="d245f-103">Tengjast við Business Central gögnin til að búa til viðskiptaforrit með því að nota Power Apps</span><span class="sxs-lookup"><span data-stu-id="d245f-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="d245f-104">Notandi getur gert [!INCLUDE[prodshort](includes/prodshort.md)]-gögnin sín aðgengileg sem gagnaveitu í Power Apps.</span><span class="sxs-lookup"><span data-stu-id="d245f-104">You can make your [!INCLUDE[prodshort](includes/prodshort.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="d245f-105">Notandi verður að vera með gildan reikning hjá [!INCLUDE[prodshort](includes/prodshort.md)] og hjá Power Apps.</span><span class="sxs-lookup"><span data-stu-id="d245f-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power Apps.</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-apps"></a><span data-ttu-id="d245f-106">Til að bæta [!INCLUDE[prodshort](includes/prodshort.md)] við sem gagnaveitu í Power Apps</span><span class="sxs-lookup"><span data-stu-id="d245f-106">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="d245f-107">Flettið í [powerapps.microsoft.com](https://powerapps.microsoft.com/) í vafranum og skráið ykkur svo inn.</span><span class="sxs-lookup"><span data-stu-id="d245f-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="d245f-108">Á heimasíðunni skal velja **Forrit**, **Búa til forrit** og **Vinnusvæði** til að búa til nýtt vinnusvæðisforrit.</span><span class="sxs-lookup"><span data-stu-id="d245f-108">On the Home page, choose the **Apps**, **Create an app** and **Canvas** to create a new canvas app.</span></span> <span data-ttu-id="d245f-109">Þetta forrit verður hannað til notkunar í farsíma, en þú getur einnig valið að nota annað sniðmát.</span><span class="sxs-lookup"><span data-stu-id="d245f-109">This app will be designed for use on a mobile device, but you can also choose to use another template.</span></span>

    <span data-ttu-id="d245f-110">Næsta skrefið til að búa til Power App er að velja gögn.</span><span class="sxs-lookup"><span data-stu-id="d245f-110">The next step to create a Power App is to select your data.</span></span> <span data-ttu-id="d245f-111">Veldu örtáknið og veldu svo valkostinn **Ný tenging** á efri hluta síðunnar, vinstra megin.</span><span class="sxs-lookup"><span data-stu-id="d245f-111">Choose the Arrow icon then choose the **New connection** option in the upper left side of the page.</span></span>
3. <span data-ttu-id="d245f-112">Úr lista yfir tiltækar tengingar skal velja **Business Central** og svo hnappinn **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="d245f-112">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="d245f-113">Power Apps mun tengjast [!INCLUDE [prodshort](includes/prodshort.md)] með því að nota skilríkin sem notandi er skráður inn í með.</span><span class="sxs-lookup"><span data-stu-id="d245f-113">Power Apps will connect to your [!INCLUDE [prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="d245f-114">Ef þú ert ekki stjórnandi á [!INCLUDE [prodshort](includes/prodshort.md)] þínu þarftu hugsanlega að skrá þig inn með öðrum reikningi.</span><span class="sxs-lookup"><span data-stu-id="d245f-114">If you are not an administrator of your [!INCLUDE [prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="d245f-115">Power Apps mun birta lista yfir *umhverfi og fyrirtæki* sem eru tiltæk í [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="d245f-115">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="d245f-116">Velja skal umhverfi og fyrirtækið sem inniheldur gögnin sem á að tengjast við.</span><span class="sxs-lookup"><span data-stu-id="d245f-116">Choose the environment and company that contains the data you want to connect to.</span></span> <span data-ttu-id="d245f-117">Næst færðu að sjá lista yfir API.</span><span class="sxs-lookup"><span data-stu-id="d245f-117">Next, you will be presented with a list of APIs.</span></span> <span data-ttu-id="d245f-118">Veldu **API** sem þú vilt tengjast við.</span><span class="sxs-lookup"><span data-stu-id="d245f-118">Select the **API** you want to connect to.</span></span>

<span data-ttu-id="d245f-119">Þessar svokölluðu töflur eru hluti af [!INCLUDE [prodshort](includes/prodshort.md)] API.</span><span class="sxs-lookup"><span data-stu-id="d245f-119">These so-called tables are part of the [!INCLUDE [prodshort](includes/prodshort.md)] API.</span></span> <span data-ttu-id="d245f-120">Þú þarft ekki að grunnstilla endapunktana sjálf(ur) - [!INCLUDE [prodshort](includes/prodshort.md)] tengillinn fyrir Power Apps gerir það fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="d245f-120">You do not have to configure the end points yourself - the [!INCLUDE [prodshort](includes/prodshort.md)] connector for Power Apps does it for you.</span></span>  

> [!NOTE]
> <span data-ttu-id="d245f-121">Ef þú vilt hafa með gögn úr öðrum töflum í [!INCLUDE [prodshort](includes/prodshort.md)] í forritinu þínu verður þú að vinna með þróunaraðila til að skilgreina sérsniðið API í [!INCLUDE [prodshort](includes/prodshort.md)] og síðan nota þetta sérsniðna API í gegnum sérsniðinn tengil í Power Apps.</span><span class="sxs-lookup"><span data-stu-id="d245f-121">If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="d245f-122">Nánari upplýsingar má finna í [Stofna sérsniðin tengi frá grunni](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="d245f-122">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="d245f-123">Nú hefur þér tekist að tengjast gögnum þínum í [!INCLUDE [prodshort](includes/prodshort.md)] og getur byrjað að byggja upp PowerApp.</span><span class="sxs-lookup"><span data-stu-id="d245f-123">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="d245f-124">Hægt er að bæta við fleiri skjáum og tengjast við fleiri gögn úr [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="d245f-124">You can add additional screens and connect to additional data from your [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="d245f-125">Frekari upplýsingar er að finna á [Búa til vinnusvæðisforrit úr sniðmáti í Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).</span><span class="sxs-lookup"><span data-stu-id="d245f-125">For more information, see [Create a canvas app from a template in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).</span></span>  

<span data-ttu-id="d245f-126">Þegar þú hefur hannað og smíðað forritið þitt getur þú deilt því með samstarfsmönnum þínum.</span><span class="sxs-lookup"><span data-stu-id="d245f-126">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="d245f-127">Frekari upplýsingar er að finna á [Vista og birta vinnusvæðisforrit í Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="d245f-127">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="d245f-128">Ef þú vilt tengjast við [!INCLUDE [prodshort](includes/prodshort.md)] á staðnum verður þú að velja tengilinn **Business Central (á staðnum)** í skrefi 3.</span><span class="sxs-lookup"><span data-stu-id="d245f-128">If you want to connect to [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d245f-129">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d245f-129">See Also</span></span>

[<span data-ttu-id="d245f-130">Búa til vinnusvæðisforrit úr sniðmáti í Power Apps</span><span class="sxs-lookup"><span data-stu-id="d245f-130">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="d245f-131">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="d245f-131">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="d245f-132">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="d245f-132">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="d245f-133">[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="d245f-133">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="d245f-134">Fjármál</span><span class="sxs-lookup"><span data-stu-id="d245f-134">Finance</span></span>](finance.md)  
[<span data-ttu-id="d245f-135">Hafist handa við þróun á tengiforritum fyrir Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="d245f-135">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
