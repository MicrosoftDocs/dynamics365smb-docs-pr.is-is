---
title: "Úthluta forgangsstigi til lánardrottins | Microsoft Docs"
description: "Þú getur úthlutað númerum til lánardrottins eða birgja til að forgangsraða þeim og auðvelda greiðslutillögur í Dynamics 365."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: d19d0bce7290ce42b37dd1dfbea5213c6580e2da
ms.contentlocale: is-is
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-prioritize-vendors"></a><span data-ttu-id="2df2c-103">Hvernig á að forgangsraða Lánardrottnum</span><span class="sxs-lookup"><span data-stu-id="2df2c-103">How to: Prioritize Vendors</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="2df2c-104"> getur lagt til ýmsar greiðslur til lánardrottna t.d. greiðslur sem eru bráðum á gjalddaga eða greiðslur sem hægt er að fá afslátt af.</span><span class="sxs-lookup"><span data-stu-id="2df2c-104"> can suggest various payments to vendors, for example, payments that will be due soon or payments where a discount is available.</span></span> <span data-ttu-id="2df2c-105">Nánari upplýsingar má sjá í [Hvernig á að: Leggja til greiðslutillögur til lánardrottna](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="2df2c-105">For more information, see [How to: Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

<span data-ttu-id="2df2c-106">Fyrst verður að forgangsraða lánardrottnum með því að úthluta númerum á þá.</span><span class="sxs-lookup"><span data-stu-id="2df2c-106">First, you must prioritize your vendors by assigning numbers to them.</span></span>

## <a name="to-prioritize-vendors"></a><span data-ttu-id="2df2c-107">Lánardrottnum forgangsraðað</span><span class="sxs-lookup"><span data-stu-id="2df2c-107">To prioritize vendors</span></span>
1. <span data-ttu-id="2df2c-108">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **lánardrottnar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="2df2c-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="2df2c-109">Veljið viðeigandi lánardrottin og veljið því næst **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="2df2c-109">Select the relevant vendor, and then choose **Edit**.</span></span>
3. <span data-ttu-id="2df2c-110">Í reitinn **Forgangur** skal færa inn númer.</span><span class="sxs-lookup"><span data-stu-id="2df2c-110">In the **Priority** field, enter a number.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="2df2c-111"> setur lægsta númerið, fyrir utan 0, efst í forgangsröðina.</span><span class="sxs-lookup"><span data-stu-id="2df2c-111"> considers the lowest number, except 0, to have the highest priority.</span></span> <span data-ttu-id="2df2c-112">Þannig að t.d. ef notaðar eru tölurnar 1, 2 og 3 þá er 1 fyrst í forgangsröðinni.</span><span class="sxs-lookup"><span data-stu-id="2df2c-112">So, for example, if you use 1, 2, and 3, then 1 will have the highest priority.</span></span>

<span data-ttu-id="2df2c-113">Ef ekki á að forgangsraða lánardrottni er reiturinn **Forgangur** skilinn eftir auður.</span><span class="sxs-lookup"><span data-stu-id="2df2c-113">If you do not want to prioritize a vendor, leave the **Priority** field blank.</span></span> <span data-ttu-id="2df2c-114">Síðan ef notuð er aðgerðin greiðslutillaga er lánardrottininn settur á lista á eftir öllum lánardrottnunum sem hafa forgangsnúmer.</span><span class="sxs-lookup"><span data-stu-id="2df2c-114">Then, if you use the payment suggestion feature, the vendor will be listed after all the vendors that have a priority number.</span></span> <span data-ttu-id="2df2c-115">Hægt er að færa inn eins mörg forgangsstig og nauðsynlegt er.</span><span class="sxs-lookup"><span data-stu-id="2df2c-115">You can enter as many priority levels as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="2df2c-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2df2c-116">See Also</span></span>
[<span data-ttu-id="2df2c-117">Uppsetning innkaupa</span><span class="sxs-lookup"><span data-stu-id="2df2c-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="2df2c-118">Stjórna skuldum</span><span class="sxs-lookup"><span data-stu-id="2df2c-118">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="2df2c-119">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2df2c-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

