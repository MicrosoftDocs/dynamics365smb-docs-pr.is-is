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
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: dde99e50c6984a7ec162b4047e8640e6affb3f25
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="48dcf-103">Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] í sjálfvirku verkflæði.</span><span class="sxs-lookup"><span data-stu-id="48dcf-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="48dcf-104">Notandi getur notað [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín sem hluta af verkflæði í Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="48dcf-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="48dcf-105">Notandi verður að vera með gildan reikning hjá [!INCLUDE[d365fin](includes/d365fin_md.md)] og hjá Flæði.</span><span class="sxs-lookup"><span data-stu-id="48dcf-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="48dcf-106">Til að bæta [!INCLUDE[d365fin](includes/d365fin_md.md)]við sem gagnaveitu í flæði</span><span class="sxs-lookup"><span data-stu-id="48dcf-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="48dcf-107">Flettið í [flow.microsoft.com](https://flow.microsoft.com/en-us/) í vafranum og skráið ykkur svo inn.</span><span class="sxs-lookup"><span data-stu-id="48dcf-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="48dcf-108">Veldu **Mitt flæði** af borðanum efst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="48dcf-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="48dcf-109">Í glugganum **Mitt flæði** skal velja valkostinn **Stofna úr auðu**.</span><span class="sxs-lookup"><span data-stu-id="48dcf-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="48dcf-110">Farðu í lista yfir tiltækar kveikjur og veldu eina af [!INCLUDE[d365fin](includes/d365fin_md.md)] tiltækum kveikjum í boði:</span><span class="sxs-lookup"><span data-stu-id="48dcf-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="48dcf-111">*Þegar beðið er um samþykki viðskiptavinar*,</span><span class="sxs-lookup"><span data-stu-id="48dcf-111">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="48dcf-112">*Þegar beðið er um samþykki fyrir almenna færslubókarkeyrslu*,</span><span class="sxs-lookup"><span data-stu-id="48dcf-112">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="48dcf-113">*Þegar beðið er um samþykki fyrir almenna færslubókarlínu*,</span><span class="sxs-lookup"><span data-stu-id="48dcf-113">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="48dcf-114">*Þegar beðið er um samþykki fyrir vöru*,</span><span class="sxs-lookup"><span data-stu-id="48dcf-114">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="48dcf-115">*Þegar beðið er um samþykki innkaupaskjals*,</span><span class="sxs-lookup"><span data-stu-id="48dcf-115">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="48dcf-116">*Þegar beðið er um samþykki söluskjals*, eða</span><span class="sxs-lookup"><span data-stu-id="48dcf-116">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="48dcf-117">*Þegar beðið er um samþykki lánardrottins*.</span><span class="sxs-lookup"><span data-stu-id="48dcf-117">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="48dcf-118">Flæði biður þig um velja fyrirtæki innan leigjandans [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="48dcf-118">Flow will prompt you to select a company within your [!INCLUDE[d365fin](includes/d365fin_md.md)] tenant.</span></span> <span data-ttu-id="48dcf-119">Vegna þess að hvert skref í Flæði er óháð því næsta, getur verið að þú þurfir að skilgreina fyrirtækið mörgum sinnum þegar þú notar [!INCLUDE[d365fin](includes/d365fin_md.md)] sniðmát.</span><span class="sxs-lookup"><span data-stu-id="48dcf-119">Because each step in the Flow is independent of the next, you may be required to define the company multiple times when using a [!INCLUDE[d365fin](includes/d365fin_md.md)] template.</span></span>

<span data-ttu-id="48dcf-120">Nú hefur notanda tekist að tengjast gögnum sínum í Finance and Operations, Business Edition og getur byrjað að byggja upp flæðið.</span><span class="sxs-lookup"><span data-stu-id="48dcf-120">At this point, you have successfully connected to your Finance and Operations, Business edition data and are ready to begin building your flow.</span></span> <span data-ttu-id="48dcf-121">Frekari upplýsingar eru í [gögnum um Flow](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="48dcf-121">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="48dcf-122">Fyrir úrræðaleit við Microsoft Flow sjá [Úrræðaleit samþættingar við Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="48dcf-122">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="48dcf-123">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="48dcf-123">See Also</span></span>
<span data-ttu-id="48dcf-124">[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="48dcf-124">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="48dcf-125">Innflutningur viðskiptagagna úr öðrum fjárhagskerfum</span><span class="sxs-lookup"><span data-stu-id="48dcf-125">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="48dcf-126">[Vinna með notendur og heimildir](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="48dcf-126">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="48dcf-127">[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="48dcf-127">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="48dcf-128">Fjármál</span><span class="sxs-lookup"><span data-stu-id="48dcf-128">Finance</span></span>](finance.md)  

