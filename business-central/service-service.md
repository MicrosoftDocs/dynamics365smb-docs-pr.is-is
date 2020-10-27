---
title: þjónustukerfi | Microsoft Docs
description: Læra að nota eiginleika sem eru hannaðir til að styðja viðgerðaverkstæði og þjónustuaðgerðir á staðnum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3bf97a81c41823b9b4d839af4d53045f0bdaa74e
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913047"
---
# <a name="service-management"></a><span data-ttu-id="58b5b-103">Þjónustukerfi</span><span class="sxs-lookup"><span data-stu-id="58b5b-103">Service Management</span></span>
> [!NOTE]
> <span data-ttu-id="58b5b-104">Virkni sem lýst er í þessu efni og undirviðfangsefni er aðeins sýnilegt í notendaviðmótinu ef þú hefur **Úrvals** upplifun.</span><span class="sxs-lookup"><span data-stu-id="58b5b-104">Functionality described in this topic and sub topics is only visible in the user interface if you have the **Premium** experience.</span></span> <span data-ttu-id="58b5b-105">Frekari upplýsingar er að finna í [Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="58b5b-105">For more information, see [Change Which Features are Displayed](ui-experiences.md).</span></span>

<span data-ttu-id="58b5b-106">Að veita viðskiptamönnum þjónustu er mikilvægur hluti fyrirtækjareksturs, og getur hún verið uppspretta ánægju og tryggðar þeirra, auk þess að skapa fyrirtækinu tekjur.</span><span class="sxs-lookup"><span data-stu-id="58b5b-106">Providing ongoing service to customers is an important part of any business and one that can be a source of customer satisfaction and loyalty, in addition to revenue.</span></span> <span data-ttu-id="58b5b-107">Hins vegar er stjórnun og rakning þjónustu ekki alltaf auðveld, og í [!INCLUDE[d365fin](includes/d365fin_md.md)] eru verkfæri til að auðveldar slíkt.</span><span class="sxs-lookup"><span data-stu-id="58b5b-107">However, managing and tracking service is not always easy, and [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a set of tools to help.</span></span> <span data-ttu-id="58b5b-108">Þessi verkfæri eru hönnuð til að styðja aðgerðir á vettvangi og verkstæðum, og nýtast í viðskiptaaðstæðum á borð við flókin þjónustudreifingarkerfi viðskiptamanna, iðnaðarþjónustuumhverfi með uppskriftir, og afgreiðslu þjónustutæknimanna með varahlutastjórnunarþarfir í stórum stíl.</span><span class="sxs-lookup"><span data-stu-id="58b5b-108">These tools are designed to support repair shop and field service operations, and can be used in business scenarios such as complex customer service distribution systems, industrial service environments with bills of materials, and high volume dispatching of service technicians with requirements for spare parts management.</span></span>  

 <span data-ttu-id="58b5b-109">Með þessum verkfærum er hægt að ná fram eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="58b5b-109">With these tools you can accomplish the following:</span></span>  

* <span data-ttu-id="58b5b-110">Tímasetja þjónustusímtöl og setja upp þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="58b5b-110">Schedule service calls and set up service orders.</span></span>  
* <span data-ttu-id="58b5b-111">Rekja varahluti og forða</span><span class="sxs-lookup"><span data-stu-id="58b5b-111">Track repair parts and supplies.</span></span>  
* <span data-ttu-id="58b5b-112">Úthluta þjónustustarfsfólki eftir hæfni og ráðstöfunargetu.</span><span class="sxs-lookup"><span data-stu-id="58b5b-112">Assign service personnel based on skill and availability.</span></span>  
* <span data-ttu-id="58b5b-113">Gera skal þjónustumat og þjónustureikninga.</span><span class="sxs-lookup"><span data-stu-id="58b5b-113">Provide service estimates and service invoices.</span></span>  

<span data-ttu-id="58b5b-114">Auk þess er hægt að staðla kótun, setja upp samninga, nota afsláttarstefnu og jafnvel stofna leiðarkort fyrir þjónustustarfsfólk.</span><span class="sxs-lookup"><span data-stu-id="58b5b-114">In addition, you can standardize coding, set up contracts, implement a discounting policy, and create route maps for service employees.</span></span>  

<span data-ttu-id="58b5b-115">Almennt séð skiptist þjónustukerfi í tvo hluta: Stillingu og uppsetningu kerfisins, og notkun þess fyrir verðlagning, samningar, pantanir, afgreiðsla þjónustustarfsfólks og tímasetning verks.</span><span class="sxs-lookup"><span data-stu-id="58b5b-115">In general, there are two aspects to service management: configuring and setting up your system, and using it for pricing, contracts, orders, service personnel dispatch, and job scheduler.</span></span>  

<span data-ttu-id="58b5b-116">Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.</span><span class="sxs-lookup"><span data-stu-id="58b5b-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="58b5b-117">**Til að**</span><span class="sxs-lookup"><span data-stu-id="58b5b-117">**To**</span></span>|<span data-ttu-id="58b5b-118">**Sjá**</span><span class="sxs-lookup"><span data-stu-id="58b5b-118">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="58b5b-119">Setja upp þjónustustjórnun, þ.m.t. bilunarkóta, stefnur, sjálfgefin skjöl og sniðmát.</span><span class="sxs-lookup"><span data-stu-id="58b5b-119">Set up Service Management, including fault codes, policies, default documents and templates.</span></span>|[<span data-ttu-id="58b5b-120">Þjónustustýring sett upp</span><span class="sxs-lookup"><span data-stu-id="58b5b-120">Setting Up Service Management</span></span>](service-setup-service.md)|  
|<span data-ttu-id="58b5b-121">Stjórna þjónustuverðlagi, stofna þjónustuvörur og skilja hvernig skal fylgjast með ferlinu.</span><span class="sxs-lookup"><span data-stu-id="58b5b-121">Manage service pricing, create service items, and understand how to monitor progress.</span></span>|[<span data-ttu-id="58b5b-122">Áætla þjónustu</span><span class="sxs-lookup"><span data-stu-id="58b5b-122">Planning Service</span></span>](service-plan-service.md)|  
|<span data-ttu-id="58b5b-123">Stofna og stjórna samningssamkomulagi á milli þín og þinna viðskiptamanna.</span><span class="sxs-lookup"><span data-stu-id="58b5b-123">Create and manage contractual agreements between you and your customers.</span></span>|[<span data-ttu-id="58b5b-124">Uppfylla þjónustusamninga</span><span class="sxs-lookup"><span data-stu-id="58b5b-124">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)|  
|<span data-ttu-id="58b5b-125">Bjóða upp á þjónustu til handa viðskiptamönnum og reikningsfæra þjónustupantanir.</span><span class="sxs-lookup"><span data-stu-id="58b5b-125">Provide service to customers, and invoice service orders.</span></span>|[<span data-ttu-id="58b5b-126">Þjónustuafhending</span><span class="sxs-lookup"><span data-stu-id="58b5b-126">Delivering Service</span></span>](service-deliver-service.md)|  

## <a name="see-also"></a><span data-ttu-id="58b5b-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="58b5b-127">See Also</span></span>  
<span data-ttu-id="58b5b-128">[Stjórnun útistandandi reikninga](receivables-manage-receivables.md) </span><span class="sxs-lookup"><span data-stu-id="58b5b-128">[Managing Receivables](receivables-manage-receivables.md) </span></span>  
<span data-ttu-id="58b5b-129">[Verk](projects-how-create-jobs.md) </span><span class="sxs-lookup"><span data-stu-id="58b5b-129">[Jobs](projects-how-create-jobs.md) </span></span>  
<span data-ttu-id="58b5b-130">[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] ](index.md)</span><span class="sxs-lookup"><span data-stu-id="58b5b-130">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] ](index.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
