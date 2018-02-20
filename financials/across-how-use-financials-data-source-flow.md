---
title: "Tengja gögn við flæði| Microsoft Docs"
description: "Notandi getur gert Financials-gögnin sín aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til sjálfvirkt verkflæði."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="86b76-103">Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] í sjálfvirku verkflæði.</span><span class="sxs-lookup"><span data-stu-id="86b76-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="86b76-104">Notandi getur notað [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín sem hluta af verkflæði í Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="86b76-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="86b76-105">Notandi verður að vera með gildan reikning hjá [!INCLUDE[d365fin](includes/d365fin_md.md)] og hjá Flæði.</span><span class="sxs-lookup"><span data-stu-id="86b76-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="86b76-106">Til að bæta [!INCLUDE[d365fin](includes/d365fin_md.md)]við sem gagnaveitu í flæði</span><span class="sxs-lookup"><span data-stu-id="86b76-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="86b76-107">Flettið í [flow.microsoft.com](https://flow.microsoft.com/en-us/) í vafranum og skráið ykkur svo inn.</span><span class="sxs-lookup"><span data-stu-id="86b76-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="86b76-108">Veldu **Mitt flæði** af borðanum efst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="86b76-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="86b76-109">Í glugganum **Mitt flæði** skal velja valkostinn **Stofna úr auðu**.</span><span class="sxs-lookup"><span data-stu-id="86b76-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="86b76-110">Farðu í lista yfir tiltækar kveikjur og veldu eina af [!INCLUDE[d365fin](includes/d365fin_md.md)] tiltækum kveikjum í boði:</span><span class="sxs-lookup"><span data-stu-id="86b76-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="86b76-111">*Þegar færsla er stofnuð*,</span><span class="sxs-lookup"><span data-stu-id="86b76-111">*When a record is created*,</span></span>  
    <span data-ttu-id="86b76-112">*Þegar færslu er eytt*,</span><span class="sxs-lookup"><span data-stu-id="86b76-112">*When a record is deleted*,</span></span>  
    <span data-ttu-id="86b76-113">*Þegar færslu er breytt*,</span><span class="sxs-lookup"><span data-stu-id="86b76-113">*When a record is modified*,</span></span>  
    <span data-ttu-id="86b76-114">*Þegar beðið er um samþykki viðskiptavinar*,</span><span class="sxs-lookup"><span data-stu-id="86b76-114">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="86b76-115">*Þegar beðið er um samþykki fyrir almenna færslubókarkeyrslu*,</span><span class="sxs-lookup"><span data-stu-id="86b76-115">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="86b76-116">*Þegar beðið er um samþykki fyrir almenna færslubókarlínu*,</span><span class="sxs-lookup"><span data-stu-id="86b76-116">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="86b76-117">*Þegar beðið er um samþykki fyrir vöru*,</span><span class="sxs-lookup"><span data-stu-id="86b76-117">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="86b76-118">*Þegar beðið er um samþykki innkaupaskjals*,</span><span class="sxs-lookup"><span data-stu-id="86b76-118">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="86b76-119">*Þegar beðið er um samþykki söluskjals*, eða</span><span class="sxs-lookup"><span data-stu-id="86b76-119">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="86b76-120">*Þegar beðið er um samþykki lánardrottins*.</span><span class="sxs-lookup"><span data-stu-id="86b76-120">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="86b76-121">Flow mun biðja um upplýsingarnar sem gefa þarf upp til að tengja notanda við [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín.</span><span class="sxs-lookup"><span data-stu-id="86b76-121">Flow will prompt you for the information that is required to connect to your [!INCLUDE[d365fin](includes/d365fin_md.md)] data.</span></span> <span data-ttu-id="86b76-122">Ef ein af eftirfarandi kveikjum voru valdara: *Þegar færsla er stofnuð*, *Þegar færslu er breytt* eða *Þegar færslu er eytt*, verður að velja heiti fyrirtækis og töflu.</span><span class="sxs-lookup"><span data-stu-id="86b76-122">If you selected one of the following triggers: *When a record is created*, *When a record is modified*, or *When a record is deleted*, you must select a company name and table name.</span></span> <span data-ttu-id="86b76-123">Þegar einungis er um eina kveikju að ræða þarf aðeins að tilgreina heiti fyrirtækis til að tengjast.</span><span class="sxs-lookup"><span data-stu-id="86b76-123">With any other trigger, only the company name is required to connect.</span></span>

   <span data-ttu-id="86b76-124">Flow birtir þá lista yfir fyrirtæki og töflur sem eru aðgengilegar úr [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="86b76-124">Flow will show a list of companies and tables that are available from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="86b76-125">Þessar töflur eða endapunktar tákna allar vefþjónustur sem notandi hefur birt úr [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="86b76-125">These tables, or end points, represent all the web services that you have published from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

   <span data-ttu-id="86b76-126">Einnig er hægt að stofna nýja vefslóð vefþjónustu í [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að nota aðgerðina **Stofna gagnamengi** á síðunni **Vefþjónustur** með því að nota Uppsetningu með hjálp fyrir **Setja upp skýrslugerð** eða með því að velja aðgerðina **Breyta í Excel** í hvaða lista sem er.</span><span class="sxs-lookup"><span data-stu-id="86b76-126">Alternatively, create a new web service URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] by using the **Create Data Set** action in the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>

<span data-ttu-id="86b76-127">Nú hefur notanda tekist að tengjast gögnum sínum í Finance and Operations, Business Edition og getur byrjað að byggja upp flæðið.</span><span class="sxs-lookup"><span data-stu-id="86b76-127">At this point, you have successfully connected to your Finance and Operations, Business edition data and are ready to begin building your flow.</span></span> <span data-ttu-id="86b76-128">Frekari upplýsingar eru í [gögnum um Flow](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="86b76-128">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="86b76-129">Fyrir úrræðaleit við Microsoft Flow sjá [Úrræðaleit samþættingar við Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="86b76-129">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="86b76-130">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="86b76-130">See Also</span></span>
<span data-ttu-id="86b76-131">[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="86b76-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="86b76-132">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="86b76-132">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="86b76-133">[Vinna með notendur og heimildir](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="86b76-133">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="86b76-134">[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="86b76-134">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="86b76-135">Fjármál</span><span class="sxs-lookup"><span data-stu-id="86b76-135">Finance</span></span>](finance.md)  

