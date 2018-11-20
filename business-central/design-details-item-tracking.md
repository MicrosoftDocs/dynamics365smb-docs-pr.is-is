---
title: "Hönnunarupplýsingar - Vörurakning | Microsoft Docs"
description: "Í þessu efnisatriði er að finna yfirlit yfir hönnunarupplýsingar fyrir vörurakningu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/12/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 46a37fb00319647ea1c4b4630e4d9369687dd7cf
ms.openlocfilehash: 1cec78cad8dca74e0a554ea183dae7a75c1b3451
ms.contentlocale: is-is
ms.lasthandoff: 11/12/2018

---
# <a name="design-details-item-tracking"></a><span data-ttu-id="1693c-103">Hönnunarupplýsingar: vörurakning</span><span class="sxs-lookup"><span data-stu-id="1693c-103">Design Details: Item Tracking</span></span>
<span data-ttu-id="1693c-104">Með sífellt flóknara flæði vara í framboðskeðjum nú til dags eykst mikilvægi þess fyrirtæki að geta rakið vörur.</span><span class="sxs-lookup"><span data-stu-id="1693c-104">As the flow of goods in today’s supply chain becomes more and more complex, the ability to keep track of items is increasingly important to the companies involved.</span></span> <span data-ttu-id="1693c-105">Vöktun færsluflæði vöru lagaleg krafa fyrir birgja í heilbrigðis- og íðefnageiranum en í öðrum rekstri kann að vera gott að vakta vörur með ábyrgðir eða lokadag vegna þjónustu  við viðskiptamenn.</span><span class="sxs-lookup"><span data-stu-id="1693c-105">Monitoring an item’s transaction flow is a legal requirement in the business of medical and chemical supply, but other businesses may want to monitor products with warranties or expiration dates for customer service reasons.</span></span>  

<span data-ttu-id="1693c-106">Vörurakningarkerfi á að auðvelda fyrirtæki afgreiðslu á rað- og lotunúmerum, með því að taka tillit til sérhverrar einingar varnings: hvenær og hvar móttekið, hvar geymt, hvenær og hvar selt.</span><span class="sxs-lookup"><span data-stu-id="1693c-106">An item tracking system should provide a company with easy handling of serial and lot numbers, considering each unique piece of merchandise: when and where received, where stored, when and where sold.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="1693c-107">hefur smám saman aukið uppfyllingu þessara skilyrða og býður í dag upp á kerfislæga virkni og stöðugan grunn til að þróa viðbætur.</span><span class="sxs-lookup"><span data-stu-id="1693c-107">has gradually expanded its coverage of this business requirement and today provides application-wide functionality and a solid core on which to develop extensions.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="1693c-108">Í þessum hluta</span><span class="sxs-lookup"><span data-stu-id="1693c-108">In This Section</span></span>  
[<span data-ttu-id="1693c-109">Hönnunarupplýsingarn: vörurakning hönnun</span><span class="sxs-lookup"><span data-stu-id="1693c-109">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)  
[<span data-ttu-id="1693c-110">Hönnunarupplýsingar: bókunarstrúktúr vörurakningar</span><span class="sxs-lookup"><span data-stu-id="1693c-110">Design Details: Item Tracking Posting Structure</span></span>](design-details-item-tracking-posting-structure.md)  
[<span data-ttu-id="1693c-111">Hönnunarupplýsingar: Virk móti sögulegum vörurakningarfærslum</span><span class="sxs-lookup"><span data-stu-id="1693c-111">Design Details: Active versus Historic Item Tracking Entries</span></span>](design-details-active-versus-historic-item-tracking-entries.md)  
[<span data-ttu-id="1693c-112">Hönnunarupplýsingar: vörurakningarlínur gluggi</span><span class="sxs-lookup"><span data-stu-id="1693c-112">Design Details: Item Tracking Lines Window</span></span>](design-details-item-tracking-lines-window.md)  
[<span data-ttu-id="1693c-113">Hönnunarupplýsingar: vörurakning framboð</span><span class="sxs-lookup"><span data-stu-id="1693c-113">Design Details: Item Tracking Availability</span></span>](design-details-item-tracking-availability.md)  
[<span data-ttu-id="1693c-114">Hönnunarupplýsingar: vörurakning og áætlun</span><span class="sxs-lookup"><span data-stu-id="1693c-114">Design Details: Item Tracking and Planning</span></span>](design-details-item-tracking-and-planning.md)  
[<span data-ttu-id="1693c-115">Hönnunarupplýsingar: vörurakning og frátekningar</span><span class="sxs-lookup"><span data-stu-id="1693c-115">Design Details: Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="1693c-116">Hönnunarupplýsingar: vörurakning í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="1693c-116">Design Details: Item Tracking in the Warehouse</span></span>](design-details-item-tracking-in-the-warehouse.md)

