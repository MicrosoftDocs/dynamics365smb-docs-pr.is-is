---
title: Setja upp pósthópa fyrir tengiliði| Microsoft Docs
description: Pósthópana sem nota má til að auðkenna tengiliðahópa sem eiga að fá sömu upplýsingar, t.d. fyrir markaðsherferð eða kynningu.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: fb9c540819279d042685ad69c790e36e71dcfbed
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238280"
---
# <a name="set-up-mailing-groups-for-contacts"></a><span data-ttu-id="cb1bc-103">Setja upp pósthópaa fyrir tengiliði.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-103">Set Up Mailing Groups for Contacts</span></span>
<span data-ttu-id="cb1bc-104">pósthópana sem nota má til að auðkenna tengiliðahópa sem eiga að fá sömu upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-104">You can use mailing groups to identify groups of contacts that you want to receive the same information.</span></span> <span data-ttu-id="cb1bc-105">Til dæmi er hægt að setja upp pósthóp með þeim tengiliðum sem eiga að fá tilkynningu um að skrifstofan hafi flutt, eða annan hóp til að senda gjafir á hátíðum.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-105">For example, you can set up a mailing group for the contacts that you want to send a notification of an office move, or another group for sending holiday gifts.</span></span>

<span data-ttu-id="cb1bc-106">Notkun pósthópar á tengiliði er tveggja þrepa ferli.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-106">Using mailing groups on contacts is a two-step process.</span></span> <span data-ttu-id="cb1bc-107">Fyrst skilgreina pósthópskóða.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-107">First, you define the mailing group code.</span></span> <span data-ttu-id="cb1bc-108">Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver pósthóp.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-108">You only have to perform this step one time for each mailing group.</span></span> <span data-ttu-id="cb1bc-109">Þegar kominn er pósthópskóði, er hægt að byrja að úthluta kóðanum til tengiliðafyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-109">Once you have a mailing group code, you can start to assign the code to contact companies.</span></span>

## <a name="to-define-mailing-group-codes"></a><span data-ttu-id="cb1bc-110">Skilgreina pósthópskóða</span><span class="sxs-lookup"><span data-stu-id="cb1bc-110">To define mailing group codes</span></span>
<span data-ttu-id="cb1bc-111">Pósthópskóði skilgreinir tegund eða flokk hóps, eins og Move fyrir flutning skrifstofu, GIFT fyrir hátíðsgjöf.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-111">The mailing group code defines the type or category of the group, such as MOVE for office move, or GIFT for holiday gift.</span></span> <span data-ttu-id="cb1bc-112">Hægt er að hafa nokkrar starfsgreinarhópakóða.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-112">You can have several industry group codes.</span></span> <span data-ttu-id="cb1bc-113">Til að skilgreina starfsgreinarhópa skal nota síðuna **Pósthópar**.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-113">To define the industry groups, you use the **Mailing Groups** page.</span></span>

1. <span data-ttu-id="cb1bc-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Pósthópar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Mailing Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="cb1bc-115">Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="cb1bc-116">Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignMailGroupContact"></a> <span data-ttu-id="cb1bc-117">Pósthópum úthlutað á tengiliði</span><span class="sxs-lookup"><span data-stu-id="cb1bc-117">To assign mailing groups to a contact</span></span>
1. <span data-ttu-id="cb1bc-118">Tengiliðurinn er opnaður.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-118">Open the contact.</span></span>
2. <span data-ttu-id="cb1bc-119">Valið er **Pósthópar** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-119">Choose the **Mailing Groups** action.</span></span> <span data-ttu-id="cb1bc-120">Síðan **Pósthópar tengiliða** birtist.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-120">The **Contact Mailing Groups** page opens.</span></span>
3. <span data-ttu-id="cb1bc-121">Í reitnum **Pósthópskóði** veljið pósthópinn sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-121">In the **Mailing Groups Code** field, select the mailing group that you want to assign.</span></span>

<span data-ttu-id="cb1bc-122">Skrefin eru endurtekin til að úthluta eins mörgum pósthópum og óskað er.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-122">Repeat these steps to assign as many mailing groups as you want.</span></span> <span data-ttu-id="cb1bc-123">Einnig má nota sömu aðferð til að úthluta pósthópum úr Tengiliðalisti.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-123">You can also assign mailing groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="cb1bc-124">Fjöldi pósthópa sem þú hefur úthlutað tengiliðnum birtist í **Fjöldi pósthópa** í hlutanum **hlutaaðgerðin** á síðunni **Tengliður**.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-124">The number of mailing groups you have assigned to the contact is displayed in the **No. of Mailing Groups** field in the **Segmentation** section on the **Contact** page.</span></span>

<span data-ttu-id="cb1bc-125">Eftir að tengiliðum hefur verið úthlutað pósthópum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-125">After you have assigned mailing groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="cb1bc-126">Frekari upplýsingar eru í [Bæta tengiliðum við hluta](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="cb1bc-126">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="cb1bc-127">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="cb1bc-127">See Also</span></span>
[<span data-ttu-id="cb1bc-128">Stofna tengiliði</span><span class="sxs-lookup"><span data-stu-id="cb1bc-128">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="cb1bc-129">Unnið með Business Central</span><span class="sxs-lookup"><span data-stu-id="cb1bc-129">Working with Business Central</span></span>](ui-work-product.md)
