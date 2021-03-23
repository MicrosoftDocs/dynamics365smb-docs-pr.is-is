---
title: Hönnunarupplýsingar - Vörurakning | Microsoft Docs
description: Í þessu efnisatriði er að finna yfirlit yfir hönnunarupplýsingar fyrir vörurakningu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c5a72fd3026f0dd78a547809e0ad6afe9de2d420
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390875"
---
# <a name="design-details-item-tracking"></a><span data-ttu-id="19b58-103">Hönnunarupplýsingar: vörurakning</span><span class="sxs-lookup"><span data-stu-id="19b58-103">Design Details: Item Tracking</span></span>
<span data-ttu-id="19b58-104">Með sífellt flóknara flæði vara í framboðskeðjum nú til dags eykst mikilvægi þess fyrirtæki að geta rakið vörur.</span><span class="sxs-lookup"><span data-stu-id="19b58-104">As the flow of goods in today’s supply chain becomes more and more complex, the ability to keep track of items is increasingly important to the companies involved.</span></span> <span data-ttu-id="19b58-105">Vöktun færsluflæði vöru lagaleg krafa fyrir birgja í heilbrigðis- og íðefnageiranum en í öðrum rekstri kann að vera gott að vakta vörur með ábyrgðir eða lokadag vegna þjónustu  við viðskiptamenn.</span><span class="sxs-lookup"><span data-stu-id="19b58-105">Monitoring an item’s transaction flow is a legal requirement in the business of medical and chemical supply, but other businesses may want to monitor products with warranties or expiration dates for customer service reasons.</span></span>  

<span data-ttu-id="19b58-106">Vörurakningarkerfi á að auðvelda fyrirtæki afgreiðslu á rað- og lotunúmerum, með því að taka tillit til sérhverrar einingar varnings: hvenær og hvar móttekið, hvar geymt, hvenær og hvar selt.</span><span class="sxs-lookup"><span data-stu-id="19b58-106">An item tracking system should provide a company with easy handling of serial and lot numbers, considering each unique piece of merchandise: when and where received, where stored, when and where sold.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="19b58-107">hefur smám saman aukið uppfyllingu þessara skilyrða og býður í dag upp á kerfislæga virkni og stöðugan grunn til að þróa viðbætur.</span><span class="sxs-lookup"><span data-stu-id="19b58-107">has gradually expanded its coverage of this business requirement and today provides application-wide functionality and a solid core on which to develop extensions.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="19b58-108">Í þessum hluta</span><span class="sxs-lookup"><span data-stu-id="19b58-108">In This Section</span></span>  
[<span data-ttu-id="19b58-109">Hönnunarupplýsingarn: vörurakning hönnun</span><span class="sxs-lookup"><span data-stu-id="19b58-109">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)  
[<span data-ttu-id="19b58-110">Hönnunarupplýsingar: bókunarstrúktúr vörurakningar</span><span class="sxs-lookup"><span data-stu-id="19b58-110">Design Details: Item Tracking Posting Structure</span></span>](design-details-item-tracking-posting-structure.md)  
[<span data-ttu-id="19b58-111">Hönnunarupplýsingar: Virk móti sögulegum vörurakningarfærslum</span><span class="sxs-lookup"><span data-stu-id="19b58-111">Design Details: Active versus Historic Item Tracking Entries</span></span>](design-details-active-versus-historic-item-tracking-entries.md)  
[<span data-ttu-id="19b58-112">Hönnunarupplýsingar: síða vörurakningarlína</span><span class="sxs-lookup"><span data-stu-id="19b58-112">Design Details: Item Tracking Lines Page</span></span>](design-details-item-tracking-lines-window.md)  
[<span data-ttu-id="19b58-113">Hönnunarupplýsingar: vörurakning framboð</span><span class="sxs-lookup"><span data-stu-id="19b58-113">Design Details: Item Tracking Availability</span></span>](design-details-item-tracking-availability.md)  
[<span data-ttu-id="19b58-114">Hönnunarupplýsingar: vörurakning og áætlun</span><span class="sxs-lookup"><span data-stu-id="19b58-114">Design Details: Item Tracking and Planning</span></span>](design-details-item-tracking-and-planning.md)  
[<span data-ttu-id="19b58-115">Hönnunarupplýsingar: vörurakning og frátekningar</span><span class="sxs-lookup"><span data-stu-id="19b58-115">Design Details: Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="19b58-116">Hönnunarupplýsingar: vörurakning í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="19b58-116">Design Details: Item Tracking in the Warehouse</span></span>](design-details-item-tracking-in-the-warehouse.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]