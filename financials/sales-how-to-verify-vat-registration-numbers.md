---
title: "Hvernig á að staðfesta VSK-númer | Microsoft Docs"
description: "Hægt er að nota EB vefþjónustu til að staðfesta að VSK-númer sem þú slærð inn í viðskiptamann, lánardrottinn eða tengiliðaspjöld séu gild."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7180c7823055dba52a398584ed2f4c2952d08492
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-verify-vat-registration-numbers"></a><span data-ttu-id="f8f82-103">Hvernig á að staðfesta VSK-númer</span><span class="sxs-lookup"><span data-stu-id="f8f82-103">How to: Verify VAT Registration Numbers</span></span>
<span data-ttu-id="f8f82-104">Hægt er að nota EB vefþjónustu til að staðfesta að VSK-númer sem þú slærð inn í viðskiptamann, lánardrottinn eða tengiliðaspjöld séu gild.</span><span class="sxs-lookup"><span data-stu-id="f8f82-104">You can use an EU web service to verify that VAT registration numbers that you enter on customer, vendor, or contact cards are valid.</span></span>  

 <span data-ttu-id="f8f82-105">Þegar þú breytir **VSK númer** reitnum á korti þar sem gildið í **land/svæði kóði** reitnum er innan Land/svæði Evrópusambandsins, eru nýja VSK-númerið þitt og notandakenni skráð í **VSK Skráningarkladdi** gluggann.</span><span class="sxs-lookup"><span data-stu-id="f8f82-105">When you modify the **VAT Registration No.** field on a card where the value in the **Country/Region Code** field is an EU country/region, then the new VAT registration number and your user ID are logged in the **VAT Registration Log** window.</span></span> <span data-ttu-id="f8f82-106">Þú sannprófar VSK-númer með því að velja **Staðfesta skráningarnúmer** hnappinn í **VSK Skráningarkladdi** gluggann.</span><span class="sxs-lookup"><span data-stu-id="f8f82-106">You verify a VAT registration number by choosing the **Verify Registration No.** button in the **VAT Registration Log** window.</span></span> <span data-ttu-id="f8f82-107">Ný lína er stofnuð í hvert skipti sem staðfestingaraðgerðin er notuð.</span><span class="sxs-lookup"><span data-stu-id="f8f82-107">A new line is created every time you use the verification function.</span></span> <span data-ttu-id="f8f82-108">Ef hægt var að sannprófa tölurnar inniheldur **Staða** reiturinn **Gilt**.</span><span class="sxs-lookup"><span data-stu-id="f8f82-108">If the number could be verified, the **Status** field contains **Valid**.</span></span> <span data-ttu-id="f8f82-109">Ef ekki er hægt að sannprófa töluna inniheldur **Staða** reiturinn **Ógilt** og þú verður að breyta tölunni í **VSK Númer** reitnum á kortinu og hefja sannprófunina aftur.</span><span class="sxs-lookup"><span data-stu-id="f8f82-109">If the number could not be verified, the **Status** field contains **Invalid**, and you must then change the number in the **VAT Registration No.** field on the card and start the verification function again.</span></span>  

 <span data-ttu-id="f8f82-110">Vefslóð sjálfgefinnar vefþjónustu er sett upp í **VSK skráningarnúmer sannprófun vefslóð** reitnum í **Uppsetning fjárhags** glugganum.</span><span class="sxs-lookup"><span data-stu-id="f8f82-110">The URL of the default web service is set up in the **VAT Reg. No. Validation URL** field in the **General Ledger Setup** window.</span></span>  

 <span data-ttu-id="f8f82-111">Í **VSK Skráningarnúmerasnið** töflunni er hægt að breyta fyrir hvert landsvæði mismunandi snið VSK-skráningarnúmera sem notendur hafa leyfi til að slá inn í **VSK skráningarnúmer** reitinn</span><span class="sxs-lookup"><span data-stu-id="f8f82-111">In the **VAT Registration No. Format** table, you can change for each country/region the different formats of VAT registration number that users are allowed to enter in the **VAT Registration No.** field.</span></span>  

> [!WARNING]  
>  <span data-ttu-id="f8f82-112">Þessi vefþjónusta notar http-reglur, sem táknar að gagnaflutningur um þjónustuna er ekki dulritaður.</span><span class="sxs-lookup"><span data-stu-id="f8f82-112">This web service uses the http protocol, which means that data transferred through the service is not encrypted.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f8f82-113">Þú getur upplifað niðurtíma fyrir þessa þjónustu sem Microsoft er ekki ábyrgt fyrir, þar sem þjónustan er hluti af breiðu EB neti landsbundinna VSK-skráa.</span><span class="sxs-lookup"><span data-stu-id="f8f82-113">You may experience downtime for this service for which Microsoft is not responsible, as the service is part of a broad EU network of national VAT registers.</span></span>  

## <a name="to-verify-a-vat-registration-number-from-a-customer-card"></a><span data-ttu-id="f8f82-114">Til að staðfesta VSK-númer af viðskiptamannaspjaldi</span><span class="sxs-lookup"><span data-stu-id="f8f82-114">To verify a VAT registration number from a customer card</span></span>  
<span data-ttu-id="f8f82-115">Eftirfarandi lýsir því hvernig skal sannprófa VSK númer fyrir viðskiptamann.</span><span class="sxs-lookup"><span data-stu-id="f8f82-115">The following describes how to verify a VAT registration number for a customer.</span></span> <span data-ttu-id="f8f82-116">Skrefin eru svipuð fyrir lánardrottinn og tengilið.</span><span class="sxs-lookup"><span data-stu-id="f8f82-116">The steps are similar for a vendor and a contact.</span></span>   
1.  <span data-ttu-id="f8f82-117">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **viðskiptamenn** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="f8f82-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="f8f82-118">Opnaðu spjald viðskiptamannsins þar sem þú vilt staðfesta NVS-númerið.</span><span class="sxs-lookup"><span data-stu-id="f8f82-118">Open the card of a customer where you want to verify the VAT registration number.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f8f82-119">**Land/svæði kóði** Reiturinn á viðskiptamannaspjaldinu þarf að innhalda land/svæði innan Evrópusambandsins.</span><span class="sxs-lookup"><span data-stu-id="f8f82-119">The **Country/Region Code** field on the customer card must contain an EU country/region.</span></span>  
3.  <span data-ttu-id="f8f82-120">Á flýtiflipanum **Reikningsfæra** velurðu hnappinn KafaNiður við hlið **VSK skráningarnúmer** reitarins.</span><span class="sxs-lookup"><span data-stu-id="f8f82-120">On the **Invoicing** FastTab, choose the DrillDown button next to the **VAT Registration No.** field.</span></span>  

    <span data-ttu-id="f8f82-121">**VSK skráningarkladdi** glugginn opnast með einni línu þar sem **Staða** reiturinn inniheldur **Ekki sannvottað**.</span><span class="sxs-lookup"><span data-stu-id="f8f82-121">The **VAT Registration Log** window opens showing one line where the **Status** field contains **Not Verified**.</span></span>  
4.  <span data-ttu-id="f8f82-122">Velja **Staðfestið skráningarnúmer** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="f8f82-122">Choose the **Verify Registration No.** action.</span></span>  

     <span data-ttu-id="f8f82-123">Ný lína er stofnuð þar sem **Staða** reiturinn inniheldur annað hvort **Gilt** eða **Ógilt**.</span><span class="sxs-lookup"><span data-stu-id="f8f82-123">A new line is created where the **Status** field contains either **Valid** or **Invalid**.</span></span>  
5.  <span data-ttu-id="f8f82-124">Ef **Staða** reiturinn inniheldur **Ógilt** skaltu breyta númerinu í **VSK númer** reitnum á spjaldinu og endurtaka svo skref 3 og 4.</span><span class="sxs-lookup"><span data-stu-id="f8f82-124">If the **Status** field contains **Invalid**, change the number in the **VAT Registration No.** field on the card, and then repeat steps 3 through 4.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f8f82-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f8f82-125">See Also</span></span>  
[<span data-ttu-id="f8f82-126">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f8f82-126">Finance</span></span>](finance.md)  
[<span data-ttu-id="f8f82-127">Hvernig á að: Skrá nýja viðskiptamenn</span><span class="sxs-lookup"><span data-stu-id="f8f82-127">How to: Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="f8f82-128">Hvernig á að Skrá nýja lánardrottna</span><span class="sxs-lookup"><span data-stu-id="f8f82-128">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="f8f82-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f8f82-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

