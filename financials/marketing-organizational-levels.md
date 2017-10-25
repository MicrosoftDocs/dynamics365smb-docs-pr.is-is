---
title: "Setja upp stjórnunarstig fyrir tengiliði| Microsoft Docs"
description: "Hægt er að skilgreina stjórnunarstig og úthluta því til tengiliðs til að gefa til kynna stöðuna sem hann hefur í fyrirtækinu, til dæmis forstjóri."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d101076c8a51b1c7a79606d207f79a826c89bf29
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-organizational-levels-for-contact-persons"></a><span data-ttu-id="75a50-103">Hvernig skal: Setja upp stjórnunarstig fyrir tengiliði</span><span class="sxs-lookup"><span data-stu-id="75a50-103">How to: Set Up Organizational Levels for Contact Persons</span></span>
<span data-ttu-id="75a50-104">Hægt er að úthluta stjórnunarstigum á tengiliði til að tilgreina hvaða stöðu þeir hafa innan fyrirtækis, til dæmis forstjóri.</span><span class="sxs-lookup"><span data-stu-id="75a50-104">You can use organizational levels on your contacts to specify which position they have in the company, for example, top management.</span></span> <span data-ttu-id="75a50-105">Þessar upplýsingar er hægt að nota þegar færðar eru inn upplýsingar um tengiliði.</span><span class="sxs-lookup"><span data-stu-id="75a50-105">You can use this information when entering information about your contacts.</span></span>

<span data-ttu-id="75a50-106">Notkun viðskiptatengsla á tengiliði er tveggja þrepa ferli.</span><span class="sxs-lookup"><span data-stu-id="75a50-106">Using organizational levels on contacts is a two-step process.</span></span> <span data-ttu-id="75a50-107">Fyrst að skilgreina viðskiptatengslakóðann.</span><span class="sxs-lookup"><span data-stu-id="75a50-107">First, you define the organizational level code.</span></span> <span data-ttu-id="75a50-108">Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver viðskiptatengsl.</span><span class="sxs-lookup"><span data-stu-id="75a50-108">You only have to perform this step one time for each organizational level.</span></span> <span data-ttu-id="75a50-109">Þegar kominn er viðskiptatengslakóði er hægt að byrja að úthluta kóðanum til tengiliða.</span><span class="sxs-lookup"><span data-stu-id="75a50-109">Once you have an organizational level code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-an-organizational-level-code"></a><span data-ttu-id="75a50-110">Skilgreining viðskiptatengslakóða</span><span class="sxs-lookup"><span data-stu-id="75a50-110">To define an organizational level code</span></span>
<span data-ttu-id="75a50-111">Viðskiptatengslakóði skilgreinir tegund eða flokk stjórnunarstigs, eins og framkvæmdastjóri eða fjármálastjóri.</span><span class="sxs-lookup"><span data-stu-id="75a50-111">The organizational level code defines the type or category of the organizational level, such a CEO  or CFO.</span></span> <span data-ttu-id="75a50-112">Hægt er að hafa nokkra viðskiptatengslakóða.</span><span class="sxs-lookup"><span data-stu-id="75a50-112">You can have several organizational level codes.</span></span> <span data-ttu-id="75a50-113">Glugginn **Stjórnunarstig** er notaður til að skilgreina stjórnunarstigið.</span><span class="sxs-lookup"><span data-stu-id="75a50-113">To define the organizational level, you use the **Organizational Levels** window.</span></span>

1. <span data-ttu-id="75a50-114">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Stjórnunarstig** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="75a50-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Organizational Levels**, and then choose the related link.</span></span>
2. <span data-ttu-id="75a50-115">Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing.</span><span class="sxs-lookup"><span data-stu-id="75a50-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="75a50-116">Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.</span><span class="sxs-lookup"><span data-stu-id="75a50-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="to-assign-organizational-levels-to-a-contact-person"></a><span data-ttu-id="75a50-117">Að úthluta skipulagsstigum til tengiliðs</span><span class="sxs-lookup"><span data-stu-id="75a50-117">To assign organizational levels to a contact person</span></span>
<span data-ttu-id="75a50-118">Aðeins er hægt að úthluta stjórnunarstigum á einstaklinga, ekki á fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="75a50-118">You can assign organizational levels to contact persons only, not contact companies.</span></span> <span data-ttu-id="75a50-119">Aðeins er hægt að úthluta einu stjórnunarstigi á hvern tengilið.</span><span class="sxs-lookup"><span data-stu-id="75a50-119">You can only assign one organizational level to each contact.</span></span>

1. <span data-ttu-id="75a50-120">Tengiliðurinn er opnaður.</span><span class="sxs-lookup"><span data-stu-id="75a50-120">Open the contact.</span></span>
2. <span data-ttu-id="75a50-121">Í reitnum **Stjórnunarstig** skal velja kóðann sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="75a50-121">In the **Organizational Levels** field, select the code you want to assign.</span></span>

<span data-ttu-id="75a50-122">Þegar tengiliðum hefur verið úthlutað stjórnunarstigi er hægt að nota þær upplýsingar til að stofna hluta.</span><span class="sxs-lookup"><span data-stu-id="75a50-122">After you have assigned organizational levels to your contacts, you can use this information to create segments.</span></span>

<span data-ttu-id="75a50-123">Eftir að tengiliðum hefur verið úthlutað starfsábyrgðum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta.</span><span class="sxs-lookup"><span data-stu-id="75a50-123">After you have assigned job responsibilities to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="75a50-124">Sjá frekari upplýsingar hér [Hvernig á að bæta tengiliðum við hluta:](marketing-add-contact-segment.md)</span><span class="sxs-lookup"><span data-stu-id="75a50-124">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="75a50-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="75a50-125">See Also</span></span>
[<span data-ttu-id="75a50-126">Fyrirtækjatengiliðir stofnaðir</span><span class="sxs-lookup"><span data-stu-id="75a50-126">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="75a50-127">Einstaklingstengiliðir stofnaðir</span><span class="sxs-lookup"><span data-stu-id="75a50-127">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
<span data-ttu-id="75a50-128">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="75a50-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

