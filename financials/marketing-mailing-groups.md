---
title: "Setja upp pósthópa fyrir tengiliði| Microsoft Docs"
description: "Pósthópana sem nota má til að auðkenna tengiliðahópa sem eiga að fá sömu upplýsingar, t.d. fyrir markaðsherferð eða kynningu."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: bc1c89b87426b72ce4f9522cb7f0dc31c77acad1
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-mailing-groups-for-contacts"></a><span data-ttu-id="7d0d7-103">Hvernig skal: setja upp pósthópa fyrir tengiliði</span><span class="sxs-lookup"><span data-stu-id="7d0d7-103">How to: Set Up Mailing Groups for Contacts</span></span>
<span data-ttu-id="7d0d7-104">pósthópana sem nota má til að auðkenna tengiliðahópa sem eiga að fá sömu upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-104">You can use mailing groups to identify groups of contacts that you want to receive the same information.</span></span> <span data-ttu-id="7d0d7-105">Til dæmi er hægt að setja upp pósthóp með þeim tengiliðum sem eiga að fá tilkynningu um að skrifstofan hafi flutt, eða annan hóp til að senda gjafir á hátíðum.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-105">For example, you can set up a mailing group for the contacts that you want to send a notification of an office move, or another group for sending holiday gifts.</span></span>

<span data-ttu-id="7d0d7-106">Notkun pósthópar á tengiliði er tveggja þrepa ferli.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-106">Using mailing groups on contacts is a two-step process.</span></span> <span data-ttu-id="7d0d7-107">Fyrst skilgreina pósthópskóða.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-107">First, you define the mailing group code.</span></span> <span data-ttu-id="7d0d7-108">Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver pósthóp.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-108">You only have to perform this step one time for each mailing group.</span></span> <span data-ttu-id="7d0d7-109">Þegar kominn er pósthópskóði, er hægt að byrja að úthluta kóðanum til tengiliðafyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-109">Once you have a mailing group code, you can start to assign the code to contact companies.</span></span>

## <a name="to-define-mailing-group-codes"></a><span data-ttu-id="7d0d7-110">Skilgreina pósthópskóða</span><span class="sxs-lookup"><span data-stu-id="7d0d7-110">To define mailing group codes</span></span>
<span data-ttu-id="7d0d7-111">Pósthópskóði skilgreinir tegund eða flokk hóps, eins og Move fyrir flutning skrifstofu, GIFT fyrir hátíðsgjöf.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-111">The mailing group code defines the type or category of the group, such as MOVE for office move, or GIFT for holiday gift.</span></span> <span data-ttu-id="7d0d7-112">Hægt er að hafa nokkrar starfsgreinarhópakóða.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-112">You can have several industry group codes.</span></span> <span data-ttu-id="7d0d7-113">Til að skilgreina starfsgreinarhópar er að nota gluggann **pósthópar** .</span><span class="sxs-lookup"><span data-stu-id="7d0d7-113">To define the industry groups, you use the **Mailing Groups** window.</span></span>

1. <span data-ttu-id="7d0d7-114">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **pósthópar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Mailing Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="7d0d7-115">Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="7d0d7-116">Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <span data-ttu-id="7d0d7-117"><a name="AssignMailGroupContact"></a> Pósthópum úthlutað á tengiliði</span><span class="sxs-lookup"><span data-stu-id="7d0d7-117"><a name="AssignMailGroupContact"></a> To assign mailing groups to a contact</span></span>
1. <span data-ttu-id="7d0d7-118">Tengiliðurinn er opnaður.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-118">Open the contact.</span></span>
2. <span data-ttu-id="7d0d7-119">Valið er **Pósthópar** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-119">Choose the **Mailing Groups** action.</span></span> <span data-ttu-id="7d0d7-120">Glugginn **Pósthópar tengiliða** birtist.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-120">The **Contact Mailing Groups** window opens.</span></span>
3. <span data-ttu-id="7d0d7-121">Í reitnum **Pósthópskóði** veljið pósthópinn sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-121">In the **Mailing Groups Code** field, select the mailing group that you want to assign.</span></span>

<span data-ttu-id="7d0d7-122">Skrefin eru endurtekin til að úthluta eins mörgum pósthópum og óskað er.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-122">Repeat these steps to assign as many mailing groups as you want.</span></span> <span data-ttu-id="7d0d7-123">Einnig má nota sömu aðferð til að úthluta pósthópum úr Tengiliðalisti.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-123">You can also assign mailing groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="7d0d7-124">Fjöldi pósthópa sem þú hefur úthlutað tengiliðnum birtist í **Fjöldi pósthópa** í hlutanum **hlutaaðgerðin** á glugganum **Tengliður**.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-124">The number of mailing groups you have assigned to the contact is displayed in the **No. of Mailing Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="7d0d7-125">Eftir að tengiliðum hefur verið úthlutað pósthópum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta.</span><span class="sxs-lookup"><span data-stu-id="7d0d7-125">After you have assigned mailing groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="7d0d7-126">Sjá frekari upplýsingar hér [Hvernig á að bæta tengiliðum við hluta:](marketing-add-contact-segment.md)</span><span class="sxs-lookup"><span data-stu-id="7d0d7-126">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7d0d7-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="7d0d7-127">See Also</span></span>
[<span data-ttu-id="7d0d7-128">Fyrirtækjatengiliðir stofnaðir</span><span class="sxs-lookup"><span data-stu-id="7d0d7-128">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="7d0d7-129">Einstaklingstengiliðir stofnaðir</span><span class="sxs-lookup"><span data-stu-id="7d0d7-129">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="7d0d7-130">Unnið með Financials</span><span class="sxs-lookup"><span data-stu-id="7d0d7-130">Working with Financials</span></span>](ui-work-product.md)

