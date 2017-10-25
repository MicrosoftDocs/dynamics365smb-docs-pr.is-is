---
title: "Setja upp starfsgreinahópar fyrir tengiliðafyrirtæki| Microsoft Docs"
description: "Lýsir því hvernig skal skilgreina starfsgreinahóp og úthluta honum til tengiliðafyrirtækis, til dæmis smásöluaðilar eða bílgreinaiðnaðurinn."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7fef570e7e56e348a25ae660fa9248b529d0bfde
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-industry-groups-for-contact-companies"></a><span data-ttu-id="98713-103">Hvernig skal: setja upp starfsgreinahópar fyrir tengiliðafyrirtæki</span><span class="sxs-lookup"><span data-stu-id="98713-103">How to: Set Up Industry Groups for Contact Companies</span></span>
<span data-ttu-id="98713-104">Starfsgreinahópar eru notaðir til að tilgreina tegund starfsgreinar sem tengiliðirnir tilheyra, til dæmis smásöluaðilar eða bílgreinaiðnaðurinn.</span><span class="sxs-lookup"><span data-stu-id="98713-104">You use industry groups to indicate the type of industry to which your contacts belong, for example, the retail industry or the automobile industry.</span></span>

<span data-ttu-id="98713-105">Notkun starfsgreinahópa á tengiliði er tveggja þrepa ferli.</span><span class="sxs-lookup"><span data-stu-id="98713-105">Using industry groups on contacts is a two-step process.</span></span> <span data-ttu-id="98713-106">Fyrst skilgreina starfsgreinarhópakóðann.</span><span class="sxs-lookup"><span data-stu-id="98713-106">First, you define the industry group code.</span></span> <span data-ttu-id="98713-107">Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver starfsgreinarhóp.</span><span class="sxs-lookup"><span data-stu-id="98713-107">You only have to perform this step one time for each industry group.</span></span> <span data-ttu-id="98713-108">Þegar kominn er starfsgreinarhópakóði, er hægt að byrja að úthluta kóðanum til tengiliðafyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="98713-108">Once you have an industry group code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="98713-109">Ef á að samstilla tengiliði við lánardrottna, viðskiptamenn eða bankareikninga í öðrum hlutum kerfisins er ráðlegt að setja upp viðskiptatengsl fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="98713-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-an-industry-group-code"></a><span data-ttu-id="98713-110">Til að skilgreina kóða starfsgreinarhóps</span><span class="sxs-lookup"><span data-stu-id="98713-110">To define an industry group code</span></span>
<span data-ttu-id="98713-111">Kóði starfsgreinarhópsins skilgreinir tegund eða flokk hópsins, til dæmis ADVERT fyrir auglýsingar eða Press fyrir sjónvarp og útvarp.</span><span class="sxs-lookup"><span data-stu-id="98713-111">The industry group code defines the type or category of the group, such as ADVERT for advertising, or PRESS, for TV and radio.</span></span> <span data-ttu-id="98713-112">Hægt er að hafa nokkrar starfsgreinarhópakóða.</span><span class="sxs-lookup"><span data-stu-id="98713-112">You can have several industry group codes.</span></span> <span data-ttu-id="98713-113">Til að skilgreina starfsgreinarhópar er að nota gluggann **starfsgreinarhópar** .</span><span class="sxs-lookup"><span data-stu-id="98713-113">To define the industry groups, you use the **Industry Groups** window.</span></span>

1. <span data-ttu-id="98713-114">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **starfsgreinahópur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="98713-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Industry Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="98713-115">Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing.</span><span class="sxs-lookup"><span data-stu-id="98713-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="98713-116">Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.</span><span class="sxs-lookup"><span data-stu-id="98713-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <span data-ttu-id="98713-117"><a name="AssignIndustryGroupContact"></a> Starfsgreinahópum úthlutað á tengilið</span><span class="sxs-lookup"><span data-stu-id="98713-117"><a name="AssignIndustryGroupContact"></a> To assign industry groups to a contact</span></span>
<span data-ttu-id="98713-118">Þú getur ekki Úthluta Starfsgreinahópar á tengilið - aðeins fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="98713-118">You cannot assign industry groups to a contact person - only companies.</span></span>

1. <span data-ttu-id="98713-119">Tengiliðurinn er opnaður.</span><span class="sxs-lookup"><span data-stu-id="98713-119">Open the contact.</span></span>
2. <span data-ttu-id="98713-120">Valið er **Fyrirtæki** aðgerð, og síðan **starfsgreinarhópar** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="98713-120">Choose the **Company** action, and then the **Industry Groups** action.</span></span> <span data-ttu-id="98713-121">Glugginn **Starfsgreinahópar tengiliða** birtist.</span><span class="sxs-lookup"><span data-stu-id="98713-121">The **Contact Industry Groups** window opens.</span></span>
3. <span data-ttu-id="98713-122">Í reitnum **starfsgreinarhópakóði** veljið starfsgreinahópinn sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="98713-122">In the **Industry Groups Code** field, select the industry groups you want to assign.</span></span>

<span data-ttu-id="98713-123">Skrefin eru endurtekin til að úthluta eins mörgum starfsgreinahópum og óskað er.</span><span class="sxs-lookup"><span data-stu-id="98713-123">Repeat these steps to assign as many industry groups as you want.</span></span> <span data-ttu-id="98713-124">Einnig má nota sömu aðferð til að úthluta Starfsgreinahópar úr Tengiliðalista.</span><span class="sxs-lookup"><span data-stu-id="98713-124">You can also assign industry groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="98713-125">Fjöldi iðnaðarhópa sem þú hefur úthlutað tengiliðnum birtist á **Fjöldi starfsgreinahópa** reitnum í **Hlutunarviðmið** hlutanum í glugganum **Tengiliður**.</span><span class="sxs-lookup"><span data-stu-id="98713-125">The number of industry groups that you have assigned to the contact is displayed in the **No. of Industry Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="98713-126">Þegar tengiliðum hefur verið úthlutað starfsgreinarhópum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta.</span><span class="sxs-lookup"><span data-stu-id="98713-126">After you have assigned industry groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="98713-127">Sjá frekari upplýsingar hér [Hvernig á að bæta tengiliðum við hluta:](marketing-add-contact-segment.md)</span><span class="sxs-lookup"><span data-stu-id="98713-127">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="98713-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="98713-128">See Also</span></span>
[<span data-ttu-id="98713-129">Fyrirtækjatengiliðir stofnaðir</span><span class="sxs-lookup"><span data-stu-id="98713-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="98713-130">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="98713-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

