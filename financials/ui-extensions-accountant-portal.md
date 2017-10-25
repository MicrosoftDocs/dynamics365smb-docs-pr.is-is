---
title: "Notkun á endurskoðandagátt | Microsoft Docs"
description: "Veitir upplýsingar um viðbótina fyrir Endurskoðandagátt"
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, accountant
ms.date: 09/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 84b2331f14b8c7e8d73921189e2df33fa709626e
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="accountant-portal-for-dynamics-365-for-financials"></a><span data-ttu-id="9e350-103">Endurskoðandagátt fyrir Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="9e350-103">Accountant Portal for Dynamics 365 for Financials</span></span>
<span data-ttu-id="9e350-104">Þetta forrit býður upp á yfirlit með samanteknum gögnum fyrir hvern skjólstæðing endurskoðanda.</span><span class="sxs-lookup"><span data-stu-id="9e350-104">This application provides a dashboard with summary data for each client of an accountant.</span></span> <span data-ttu-id="9e350-105">Í gáttinni er að finna afkastavísi fjárhags ásamt beinni tengingu við fjármálaforrit skjólstæðingsins.</span><span class="sxs-lookup"><span data-stu-id="9e350-105">The portal displays financial KPIs as well as a direct link to the client’s financial application.</span></span>  

<span data-ttu-id="9e350-106">Í yfirlitinu er líka sérútbúin Hlutverkamiðstöð sem býður upp á betra yfirlit yfir viðskiptavinina.</span><span class="sxs-lookup"><span data-stu-id="9e350-106">The dashboard is a highly specialized Role Center for a better overview of your clients.</span></span>  
<span data-ttu-id="9e350-107">[![Endurskoðandagátt](./media/ui-extensions-accportal/accountant-portal.png)](https://go.microsoft.com/fwlink/?linkid=851257)</span><span class="sxs-lookup"><span data-stu-id="9e350-107">[![Accountant Portal](./media/ui-extensions-accportal/accountant-portal.png)](https://go.microsoft.com/fwlink/?linkid=851257)</span></span>

<span data-ttu-id="9e350-108">Þegar þú setur upp viðbótina í fyrsta sinn, mun sýnifyrirtæki hjálpa þér af stað.</span><span class="sxs-lookup"><span data-stu-id="9e350-108">When you first install the extension, a sample company helps you get started.</span></span> <span data-ttu-id="9e350-109">Þú getur eytt sýnifyrirtækinu hvenær sem er.</span><span class="sxs-lookup"><span data-stu-id="9e350-109">You can delete the sample company at any time.</span></span>  

## <a name="installing-the-extension"></a><span data-ttu-id="9e350-110">Uppsetning viðbótar</span><span class="sxs-lookup"><span data-stu-id="9e350-110">Installing the Extension</span></span>
<span data-ttu-id="9e350-111">Þegar þú setur upp viðbótina í [!INCLUDE[d365fin](includes/d365fin_md.md)], verðurðu spurð(ur) hvort þú viljir nota hana núna.</span><span class="sxs-lookup"><span data-stu-id="9e350-111">When you install the extension in your [!INCLUDE[d365fin](includes/d365fin_md.md)], you will be asked if you want to use it now.</span></span> <span data-ttu-id="9e350-112">Ef þú gerir það, þarftu að skrá þig út og svo inn aftur, því viðbótin skiptir hlutverkamiðstöðinni sem fyrir er út og bætir heimildum við notandaaðganginn þinn.</span><span class="sxs-lookup"><span data-stu-id="9e350-112">If you do, then you must sign out and sign in again, because the extension replaces your current Role Center and adds permissions to your user profile.</span></span>  

<span data-ttu-id="9e350-113">Frekari upplýsingar, sjá [Upplifun Endurskoðandi í Dynamics 365 for Financials](finance-accounting.md)</span><span class="sxs-lookup"><span data-stu-id="9e350-113">For more information, see [Accountant Experiences in Dynamics 365 for Financials](finance-accounting.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9e350-114">Núverandi útgáfa af viðbótinni krefst þess að viðskiptavinir þínir noti [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9e350-114">The current version of the extension requires that your clients use [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="using-the-extension"></a><span data-ttu-id="9e350-115">Nota viðbótina</span><span class="sxs-lookup"><span data-stu-id="9e350-115">Using the extension</span></span>
<span data-ttu-id="9e350-116">Þessi viðbót er notuð þegar þú skráir þig í [Financials for Accountants á Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants). Ef þú setur upp viðbótina í þínu [!INCLUDE[d365fin](includes/d365fin_md.md)], mun hún skipta út núverandi Hlutverkamiðstöð.</span><span class="sxs-lookup"><span data-stu-id="9e350-116">This extension is used when you sign up at [Financials for Accountants on Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants). If you install the extension in your [!INCLUDE[d365fin](includes/d365fin_md.md)], it will replace your current Role Center.</span></span> <span data-ttu-id="9e350-117">Ef þú vilt síðan fara aftur yfir í hina Hlutverkamiðstöð, geturðu gert það í Mínar stilllingar.</span><span class="sxs-lookup"><span data-stu-id="9e350-117">If you then want to return to the other Role Center, then you can do that in My Settings.</span></span> <span data-ttu-id="9e350-118">Nánari upplýsingar sjá [Hvernig: Breyta Hlutverkamiðstöð](change-role.md).</span><span class="sxs-lookup"><span data-stu-id="9e350-118">For more information, see [How to: Change the Role Center](change-role.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="9e350-119">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9e350-119">See Also</span></span>
[<span data-ttu-id="9e350-120">Upplifun Endurskoðandi í Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="9e350-120">Accountant Experiences in Dynamics 365 for Financials</span></span>](finance-accounting.md)  
[<span data-ttu-id="9e350-121">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9e350-121">Finance</span></span>](finance.md)  

