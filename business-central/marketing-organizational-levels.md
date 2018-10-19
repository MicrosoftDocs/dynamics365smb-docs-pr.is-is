---
title: "Setja upp stjórnunarstig fyrir tengiliði| Microsoft Docs"
description: "Hægt er að skilgreina stjórnunarstig og úthluta því til tengiliðs til að gefa til kynna stöðuna sem hann hefur í fyrirtækinu, til dæmis forstjóri."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6680a5dedcbedc3ed7e430c4290871d5fbaaf9ad
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-organizational-levels-for-contact-persons"></a><span data-ttu-id="fc08b-103">Setja upp stjórnunarstig fyrir tengiliði.</span><span class="sxs-lookup"><span data-stu-id="fc08b-103">Set Up Organizational Levels for Contact Persons</span></span>
<span data-ttu-id="fc08b-104">Hægt er að úthluta stjórnunarstigum á tengiliði til að tilgreina hvaða stöðu þeir hafa innan fyrirtækis, til dæmis forstjóri.</span><span class="sxs-lookup"><span data-stu-id="fc08b-104">You can use organizational levels on your contacts to specify which position they have in the company, for example, top management.</span></span> <span data-ttu-id="fc08b-105">Þessar upplýsingar er hægt að nota þegar færðar eru inn upplýsingar um tengiliði.</span><span class="sxs-lookup"><span data-stu-id="fc08b-105">You can use this information when entering information about your contacts.</span></span>

<span data-ttu-id="fc08b-106">Notkun viðskiptatengsla á tengiliði er tveggja þrepa ferli.</span><span class="sxs-lookup"><span data-stu-id="fc08b-106">Using organizational levels on contacts is a two-step process.</span></span> <span data-ttu-id="fc08b-107">Fyrst að skilgreina viðskiptatengslakóðann.</span><span class="sxs-lookup"><span data-stu-id="fc08b-107">First, you define the organizational level code.</span></span> <span data-ttu-id="fc08b-108">Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver viðskiptatengsl.</span><span class="sxs-lookup"><span data-stu-id="fc08b-108">You only have to perform this step one time for each organizational level.</span></span> <span data-ttu-id="fc08b-109">Þegar kominn er viðskiptatengslakóði er hægt að byrja að úthluta kóðanum til tengiliða.</span><span class="sxs-lookup"><span data-stu-id="fc08b-109">Once you have an organizational level code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-an-organizational-level-code"></a><span data-ttu-id="fc08b-110">Skilgreining viðskiptatengslakóða</span><span class="sxs-lookup"><span data-stu-id="fc08b-110">To define an organizational level code</span></span>
<span data-ttu-id="fc08b-111">Viðskiptatengslakóði skilgreinir tegund eða flokk stjórnunarstigs, eins og framkvæmdastjóri eða fjármálastjóri.</span><span class="sxs-lookup"><span data-stu-id="fc08b-111">The organizational level code defines the type or category of the organizational level, such a CEO  or CFO.</span></span> <span data-ttu-id="fc08b-112">Hægt er að hafa nokkra viðskiptatengslakóða.</span><span class="sxs-lookup"><span data-stu-id="fc08b-112">You can have several organizational level codes.</span></span> <span data-ttu-id="fc08b-113">Glugginn **Stjórnunarstig** er notaður til að skilgreina stjórnunarstigið.</span><span class="sxs-lookup"><span data-stu-id="fc08b-113">To define the organizational level, you use the **Organizational Levels** window.</span></span>

1. <span data-ttu-id="fc08b-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Stjórnunarstig** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="fc08b-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Organizational Levels**, and then choose the related link.</span></span>
2. <span data-ttu-id="fc08b-115">Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing.</span><span class="sxs-lookup"><span data-stu-id="fc08b-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="fc08b-116">Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.</span><span class="sxs-lookup"><span data-stu-id="fc08b-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="to-assign-organizational-levels-to-a-contact-person"></a><span data-ttu-id="fc08b-117">Að úthluta skipulagsstigum til tengiliðs</span><span class="sxs-lookup"><span data-stu-id="fc08b-117">To assign organizational levels to a contact person</span></span>
<span data-ttu-id="fc08b-118">Aðeins er hægt að úthluta stjórnunarstigum á einstaklinga, ekki á fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="fc08b-118">You can assign organizational levels to contact persons only, not contact companies.</span></span> <span data-ttu-id="fc08b-119">Aðeins er hægt að úthluta einu stjórnunarstigi á hvern tengilið.</span><span class="sxs-lookup"><span data-stu-id="fc08b-119">You can only assign one organizational level to each contact.</span></span>

1. <span data-ttu-id="fc08b-120">Tengiliðurinn er opnaður.</span><span class="sxs-lookup"><span data-stu-id="fc08b-120">Open the contact.</span></span>
2. <span data-ttu-id="fc08b-121">Í reitnum **Stjórnunarstig** skal velja kóðann sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="fc08b-121">In the **Organizational Levels** field, select the code you want to assign.</span></span>

<span data-ttu-id="fc08b-122">Þegar tengiliðum hefur verið úthlutað stjórnunarstigi er hægt að nota þær upplýsingar til að stofna hluta.</span><span class="sxs-lookup"><span data-stu-id="fc08b-122">After you have assigned organizational levels to your contacts, you can use this information to create segments.</span></span>

<span data-ttu-id="fc08b-123">Eftir að tengiliðum hefur verið úthlutað starfsábyrgðum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta.</span><span class="sxs-lookup"><span data-stu-id="fc08b-123">After you have assigned job responsibilities to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="fc08b-124">Frekari upplýsingar eru í [Bæta tengiliðum við hluta](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="fc08b-124">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="fc08b-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="fc08b-125">See Also</span></span>
[<span data-ttu-id="fc08b-126">Fyrirtækjatengiliðir stofnaðir</span><span class="sxs-lookup"><span data-stu-id="fc08b-126">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="fc08b-127">Einstaklingstengiliðir stofnaðir</span><span class="sxs-lookup"><span data-stu-id="fc08b-127">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
<span data-ttu-id="fc08b-128">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fc08b-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

