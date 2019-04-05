---
title: Skilgreina kóða viðskiptatengsla á tengiliði| Microsoft Docs
description: Notaðu viðskiptatengsl í Business Central til að hjálpa til við markaðssetningu og tilgreina þau viðskiptatengsl sem þú hefur við viðföng, biðlara og viðskiptavini, t.d. banka eða þjónustuaðila.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 10/01/2018
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: cb600ea688a856f481d84604d6966231fe7f536d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800204"
---
# <a name="setting-up-business-relations-on-contacts"></a><span data-ttu-id="1b708-103">Uppsetning viðskiptatengsla í tengiliði</span><span class="sxs-lookup"><span data-stu-id="1b708-103">Setting Up Business Relations on Contacts</span></span>
<span data-ttu-id="1b708-104">Þú getur notað Viðskiptatengsl til að tilgreina þau viðskiptatengsl sem eru við tengiliðina, til dæmis viðföng, banka, ráðgjafa eða þjónustuaðila, og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="1b708-104">You can use business relations to indicate the business relationship you have with your contacts, for example, a prospect, bank, consultant, service supplier, and so on.</span></span>

<span data-ttu-id="1b708-105">Notkun viðskiptatengsla á tengiliði er tveggja þrepa ferli.</span><span class="sxs-lookup"><span data-stu-id="1b708-105">Using business relations on contacts is a two-step process.</span></span> <span data-ttu-id="1b708-106">Fyrst skilgreinirðu kóða viðskiptatengsla.</span><span class="sxs-lookup"><span data-stu-id="1b708-106">First, you define the business relation code.</span></span> <span data-ttu-id="1b708-107">Aðeins þarf að framkvæma þetta skref í eitt skipti fyrir hver viðskiptatengsl.</span><span class="sxs-lookup"><span data-stu-id="1b708-107">You only have to perform this step one time for each business relation.</span></span> <span data-ttu-id="1b708-108">Þegar kominn er viðskiptatengslakóði, er hægt að byrja að úthluta kóðanum til tengiliðafyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="1b708-108">Once you have a business relation code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="1b708-109">Ef á að samstilla tengiliði við lánardrottna, viðskiptamenn eða bankareikninga í öðrum hlutum kerfisins er ráðlegt að setja upp viðskiptatengsl fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="1b708-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-a-business-relation-code"></a><span data-ttu-id="1b708-110">Til að skilgreina viðskiptatengslakóða</span><span class="sxs-lookup"><span data-stu-id="1b708-110">To define a business relation code</span></span>
<span data-ttu-id="1b708-111">Viðskiptatengslarkóðinn skilgreinir flokk eða tegund viðskiptasambandsins, svo sem banka eða lög.</span><span class="sxs-lookup"><span data-stu-id="1b708-111">The business relation code defines a category or type of the business relationship, such as BANK or Law.</span></span> <span data-ttu-id="1b708-112">Hægt er að hafa nokkrar viðskiptatengslakóða.</span><span class="sxs-lookup"><span data-stu-id="1b708-112">You can have several business relation codes.</span></span> <span data-ttu-id="1b708-113">Til að skilgreina viðskiptatengslin skal nota síðuna **Viðskiptatengsl**.</span><span class="sxs-lookup"><span data-stu-id="1b708-113">To define the business relation, you use the **Business Relations** page.</span></span>

1. <span data-ttu-id="1b708-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **viðskiptatengsl** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="1b708-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Business Relations**, and then choose the related link.</span></span>
2. <span data-ttu-id="1b708-115">Valið er **Nýtt** aðgerð og fyllt er inn kóði og lýsing.</span><span class="sxs-lookup"><span data-stu-id="1b708-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="1b708-116">Kóðinn má vera mest 11 stafir, og getur verið hvaða samasetning sem er af tölustafir og bókstafir.</span><span class="sxs-lookup"><span data-stu-id="1b708-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignBusRelContact"></a> <span data-ttu-id="1b708-117">Til að úthluta viðskiptatengslum á tengilið</span><span class="sxs-lookup"><span data-stu-id="1b708-117">To assign business relations to a contact</span></span>
<span data-ttu-id="1b708-118">Þú getur ekki Úthluta viðskiptatengslum á tengilið - aðeins fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="1b708-118">You cannot assign business relations to a contact person - only companies.</span></span>

1. <span data-ttu-id="1b708-119">Tengiliðurinn er opnaður.</span><span class="sxs-lookup"><span data-stu-id="1b708-119">Open the contact.</span></span>
2. <span data-ttu-id="1b708-120">Valið er **Fyrirtæki** aðgerð, og síðan **Viðskiptatengsl** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="1b708-120">Choose the **Company** action, and then the **Business Relations** action.</span></span>

    <span data-ttu-id="1b708-121">Síðan **Viðskiptatengsl tengiliðar** birtist.</span><span class="sxs-lookup"><span data-stu-id="1b708-121">The **Contact Business Relations** page opens.</span></span>
3. <span data-ttu-id="1b708-122">Í reitnum **Viðskiptatengslakóti** eru valin þau viðskiptatengsl sem á að úthluta.</span><span class="sxs-lookup"><span data-stu-id="1b708-122">In the **Business Relation Code** field, select the business relation you want to assign.</span></span>

<span data-ttu-id="1b708-123">Skrefin eru endurtekin til að úthluta eins mörgum viðskiptatengslum og óskað er.</span><span class="sxs-lookup"><span data-stu-id="1b708-123">Repeat these steps to assign as many business relations as you want.</span></span> <span data-ttu-id="1b708-124">Einnig má nota sömu aðferð til að úthluta viðskiptatengslum í Tengiliðalisti.</span><span class="sxs-lookup"><span data-stu-id="1b708-124">You can also assign business relations from the contact list by following the same procedure.</span></span>

<span data-ttu-id="1b708-125">Fjöldi viðskiptatengsla sem tengiliðnum hefur verið úthlutað er birtur í reitnum **Fjöldi viðskiptatengsla** á hlutanum **Hlutun** á síðunni **tengiliður**.</span><span class="sxs-lookup"><span data-stu-id="1b708-125">The number of business relations you have assigned to the contact is displayed in the **No. of Business Relations** field in the **Segmentation** section on the **Contact** page.</span></span>

<span data-ttu-id="1b708-126">Þegar tengiliðum hefur verið úthlutað viðskiptatengslum er hægt að nota þessar upplýsingar til að velja tengiliði í hluta.</span><span class="sxs-lookup"><span data-stu-id="1b708-126">After you have assigned business relations to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="1b708-127">Frekari upplýsingar eru í [Bæta tengiliðum við hluta](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="1b708-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1b708-128">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1b708-128">See Also</span></span>
<span data-ttu-id="1b708-129">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1b708-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
