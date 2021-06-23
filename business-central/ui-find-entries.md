---
title: Leita að færslum | Microsoft Docs
description: Þessi grein lýsir því hvernig á að finna skjöl og færslur sem tengjast
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a29cea15cba15da1bc68816e07f76de59f43958b
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216129"
---
# <a name="finding-related-entries-for-posted-documents"></a><span data-ttu-id="4d5f0-103">Leita að tengdum færslum fyrir bókuð skjöl</span><span class="sxs-lookup"><span data-stu-id="4d5f0-103">Finding Related Entries for Posted Documents</span></span> 

<span data-ttu-id="4d5f0-104">Í þessari grein er að finna upplýsingar um skjöl og færslur sem tengjast innbyrðis samkvæmt sameiginlegum upplýsingum á borð við:</span><span class="sxs-lookup"><span data-stu-id="4d5f0-104">In this article, you learn how to find documents and entries that are related to each other based on a common information, like:</span></span>

- <span data-ttu-id="4d5f0-105">Skjalanúmer eða bókunardagsetning</span><span class="sxs-lookup"><span data-stu-id="4d5f0-105">Document number or posting date</span></span>
- <span data-ttu-id="4d5f0-106">Gerð viðskiptatengsla, númer eða ytra skjalanúmer</span><span class="sxs-lookup"><span data-stu-id="4d5f0-106">Business contact type, number, or external document number</span></span>
- <span data-ttu-id="4d5f0-107">Raðnúmer eða lotunúmer vöru</span><span class="sxs-lookup"><span data-stu-id="4d5f0-107">Item serial number or lot number</span></span>

<span data-ttu-id="4d5f0-108">Þessi eiginleiki er gagnlegur til að hafa upp á fjárhagsfærslum sem urðu til vegna ákveðinna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-108">This feature is useful for finding the ledger entries that resulted from certain transactions.</span></span> <span data-ttu-id="4d5f0-109">Þegar leitað er eftir skjalanúmeri, er hægt að prenta samantektina úr skýrslu skjalafærslna.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-109">When you search by document number, you can print the summary from the Document Entries report.</span></span>

## <a name="get-started"></a><span data-ttu-id="4d5f0-110">Hefjast handa</span><span class="sxs-lookup"><span data-stu-id="4d5f0-110">Get started</span></span>

<span data-ttu-id="4d5f0-111">Eiginleiki færsluleitar er aðgengilegur á flestum síðum sem sýna bókuð skjöl eða bókaðar skjalafærslur - fyrir bæði lista og spjöld.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-111">The find entries feature is readily available on most pages that display posted documents or posted documents entries - for both lists and cards.</span></span> <span data-ttu-id="4d5f0-112">Þannig að fyrsta skrefið er að opna eina af þessum síðum.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-112">So the first step is open one of these pages.</span></span> <span data-ttu-id="4d5f0-113">Síðan skal annaðhvort velja aðgerðina **Leita að færslum** eða ýta á Alt+G.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-113">Then, either choose the **Find Entries** action or press the Alt+G keys.</span></span>

<span data-ttu-id="4d5f0-114">Síðan **Leita að færslum** inniheldur öll tengd skjöl og færslur samkvæmt skjalanúmerinu og bókunardagsetningunni.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-114">The **Find Entries** page  includes all related documents and entries based on the document no. and posting date.</span></span> <span data-ttu-id="4d5f0-115">Síðan skiptist í þrjá hluta:</span><span class="sxs-lookup"><span data-stu-id="4d5f0-115">The page is divided into three sections:</span></span>

- <span data-ttu-id="4d5f0-116">Efsti hlutinn sýnir reiti og aðgerðir sem eru notuð til að sía leitina.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-116">The top section displays fields and actions that you use for filtering your search.</span></span>
- <span data-ttu-id="4d5f0-117">Miðhlutinn sýnir tengd skjöl samkvæmt leitinni.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-117">The middle section displays related documents based on the search.</span></span>
- <span data-ttu-id="4d5f0-118">Neðsti hlutinn sýnir upplýsingar um upprunaskjalið sem fannst með leit.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-118">The bottom section displays information about the source document that was found by searching.</span></span>


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a><span data-ttu-id="4d5f0-119">Leita að færslum</span><span class="sxs-lookup"><span data-stu-id="4d5f0-119">Search for entries</span></span>

<span data-ttu-id="4d5f0-120">Hægt er að leita að færslum út frá upplýsingum um annaðhvort skjalið, viðskiptatengilið eða vörutilvísun.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-120">You can search for entries based on information about either the document, business contact, or item reference.</span></span> <span data-ttu-id="4d5f0-121">Til að breyta leitinni skal velja **Aðgerðir**, **Leita eftir** og síðan eina af eftirfarandi aðgerðum:</span><span class="sxs-lookup"><span data-stu-id="4d5f0-121">To change the search, select **Actions**, **Find By**, then one of the following actions:</span></span>

|<span data-ttu-id="4d5f0-122">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="4d5f0-122">Action</span></span>|<span data-ttu-id="4d5f0-123">Description</span><span class="sxs-lookup"><span data-stu-id="4d5f0-123">Description</span></span>|
|------|-----------|
|<span data-ttu-id="4d5f0-124">Leita eftir fylgiskjali</span><span class="sxs-lookup"><span data-stu-id="4d5f0-124">Find by Document</span></span>|<span data-ttu-id="4d5f0-125">Skoðið færslur út frá tilteknu skjalanúmeri eða bókunardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-125">View entries based on a specific document number or posting date.</span></span>|
|<span data-ttu-id="4d5f0-126">Viðskiptatengiliður</span><span class="sxs-lookup"><span data-stu-id="4d5f0-126">Business Contact</span></span> |<span data-ttu-id="4d5f0-127">Skoðið færslur út frá tiltekinni gerð tengiliðar, númeri tengiliðar og/eða ytra skjalanúmeri.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-127">View entries based on a specific contact type, contact number, anr/or external document number.</span></span> <span data-ttu-id="4d5f0-128">Hægt er að færa inn upplýsingar um skjal sem lánardrottin eða viðskiptamaður úthlutaði.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-128">You can enter document information that was assigned by a vendor or a customer.</span></span> <span data-ttu-id="4d5f0-129">Notið tiltæka reiti til að leita að skjölum lánardrottins með því að nota númerin sem lánardrottinn hefur úthlutað skjölunum.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-129">Use the available fields to search for vendor documents by using the numbers that the vendor has assigned the documents.</span></span>|
|<span data-ttu-id="4d5f0-130">Vörutilvísun</span><span class="sxs-lookup"><span data-stu-id="4d5f0-130">Item reference</span></span>|<span data-ttu-id="4d5f0-131">Skoðið færslur út frá raðnúmeri eða lotunúmeri.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-131">View entires based on a serial number or lot number.</span></span> <span data-ttu-id="4d5f0-132">Hægt er að færa inn lotunúmer eða raðnúmer, eða sía fyrir lotunúmerinu eða raðnúmerinu sem leita á að.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-132">You can enter the lot number or serial number, or filter on the lot number or serial number that you want to search for.</span></span> <span data-ttu-id="4d5f0-133">Þessi aðgerð er gagnleg til að sjá hvar tiltekið vörurakningarnúmer var notað, frá hvaða lánardrottni það kom eða hvaða viðskiptamanni það var selt.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-133">This action is useful to see where a specific item tracking number was used, what vendor it came from, or what customer it was sold to.</span></span>|

<span data-ttu-id="4d5f0-134">Þegar búið er að velja skal færa inn viðeigandi leitarupplýsingar í reitina efst uppi.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-134">After you make a selection, enter the relevant search information in the fields at the top.</span></span> <span data-ttu-id="4d5f0-135">Notið ábendingarnar í reitunum til að fá hjálp.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-135">Use the tooltips on the fields to help.</span></span> <span data-ttu-id="4d5f0-136">Þegar þessu er lokið skal velja **Leita** til að hefja leitina.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-136">When you're finished, choose **Find** to start the search.</span></span> <span data-ttu-id="4d5f0-137">Ef einhverjum síunum er breytt þarf að velja **Leita** aftur.</span><span class="sxs-lookup"><span data-stu-id="4d5f0-137">If you change any of the filters, you have to choose **Find** again.</span></span>

> [!TIP]
> <span data-ttu-id="4d5f0-138">Til að fá nokkur dæmi um notkun á **Leita að færslum** skal skoða [Rekja vöruraktar vörur](inventory-how-to-trace-item-tracked-items.md)</span><span class="sxs-lookup"><span data-stu-id="4d5f0-138">For a couple examples about using **Find Entries**, see [Trace Item-Tracked Items](inventory-how-to-trace-item-tracked-items.md)</span></span> <!--and [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md). -->

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="4d5f0-139">Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="4d5f0-139">See Related Training at [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="4d5f0-140">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4d5f0-140">See Also</span></span>

[<span data-ttu-id="4d5f0-141">Unnið með Business Central</span><span class="sxs-lookup"><span data-stu-id="4d5f0-141">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="4d5f0-142">Bæta Síðuaðgerð við hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="4d5f0-142">Add a Page Action to Your Role Center</span></span>](ui-bookmarks.md)  
[<span data-ttu-id="4d5f0-143">Rekja vöruraktar vörur</span><span class="sxs-lookup"><span data-stu-id="4d5f0-143">Trace Item-Tracked Items</span></span>](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
