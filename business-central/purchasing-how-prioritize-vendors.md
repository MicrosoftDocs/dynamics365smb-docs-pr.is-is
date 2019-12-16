---
title: Úthluta forgangsstigi til lánardrottins | Microsoft Docs
description: Þú getur úthlutað númerum til lánardrottins eða birgja til að forgangsraða þeim og auðvelda greiðslutillögur í Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 538a6f4b1ead61afde223391441bf097f3c26f77
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877592"
---
# <a name="prioritize-vendors"></a><span data-ttu-id="f9f62-103">Forgangsraða lánardrottnum</span><span class="sxs-lookup"><span data-stu-id="f9f62-103">Prioritize Vendors</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="f9f62-104">getur lagt til ýmsar greiðslur til lánardrottna t.d. greiðslur sem eru bráðum á gjalddaga eða greiðslur sem hægt er að fá afslátt af.</span><span class="sxs-lookup"><span data-stu-id="f9f62-104">can suggest various payments to vendors, for example, payments that will be due soon or payments where a discount is available.</span></span> <span data-ttu-id="f9f62-105">Frekari upplýsingar er að finna í [Greiðslutillögur til lánardrottna](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="f9f62-105">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

<span data-ttu-id="f9f62-106">Fyrst verður að forgangsraða lánardrottnum með því að úthluta númerum á þá.</span><span class="sxs-lookup"><span data-stu-id="f9f62-106">First, you must prioritize your vendors by assigning numbers to them.</span></span>
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa]

## <a name="to-prioritize-vendors"></a><span data-ttu-id="f9f62-107">Lánardrottnum forgangsraðað</span><span class="sxs-lookup"><span data-stu-id="f9f62-107">To prioritize vendors</span></span>
1. <span data-ttu-id="f9f62-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Lánardrottnar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="f9f62-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="f9f62-109">Veljið viðeigandi lánardrottin og veljið því næst **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="f9f62-109">Select the relevant vendor, and then choose **Edit**.</span></span>
3. <span data-ttu-id="f9f62-110">Í reitinn **Forgangur** skal færa inn númer.</span><span class="sxs-lookup"><span data-stu-id="f9f62-110">In the **Priority** field, enter a number.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="f9f62-111">setur lægsta númerið, fyrir utan 0, efst í forgangsröðina.</span><span class="sxs-lookup"><span data-stu-id="f9f62-111">considers the lowest number, except 0, to have the highest priority.</span></span> <span data-ttu-id="f9f62-112">Þannig að t.d. ef notaðar eru tölurnar 1, 2 og 3 þá er 1 fyrst í forgangsröðinni.</span><span class="sxs-lookup"><span data-stu-id="f9f62-112">So, for example, if you use 1, 2, and 3, then 1 will have the highest priority.</span></span>

<span data-ttu-id="f9f62-113">Ef ekki á að forgangsraða lánardrottni er reiturinn **Forgangur** skilinn eftir auður.</span><span class="sxs-lookup"><span data-stu-id="f9f62-113">If you do not want to prioritize a vendor, leave the **Priority** field blank.</span></span> <span data-ttu-id="f9f62-114">Síðan ef notuð er aðgerðin greiðslutillaga er lánardrottininn settur á lista á eftir öllum lánardrottnunum sem hafa forgangsnúmer.</span><span class="sxs-lookup"><span data-stu-id="f9f62-114">Then, if you use the payment suggestion feature, the vendor will be listed after all the vendors that have a priority number.</span></span> <span data-ttu-id="f9f62-115">Hægt er að færa inn eins mörg forgangsstig og nauðsynlegt er.</span><span class="sxs-lookup"><span data-stu-id="f9f62-115">You can enter as many priority levels as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9f62-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f9f62-116">See Also</span></span>
[<span data-ttu-id="f9f62-117">Uppsetning innkaupa</span><span class="sxs-lookup"><span data-stu-id="f9f62-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="f9f62-118">Stjórna skuldum</span><span class="sxs-lookup"><span data-stu-id="f9f62-118">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="f9f62-119">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f9f62-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
