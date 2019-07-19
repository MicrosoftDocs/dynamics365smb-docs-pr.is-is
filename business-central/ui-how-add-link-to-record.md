---
title: Hvernig á að tengja úr skrám í ytri upplýsingar eða forrit | Microsoft Docs
description: Setja tengil í skjal eða vefsíðu á tiltekna skrá, s.s. viðskiptavin eða fylgiskjal.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/12/2019
ms.author: jswymer
ms.openlocfilehash: 781f43daf6482c7e29696dc7a03aa021550cde7d
ms.sourcegitcommit: f2e3b571eab6e01d9f5aa8ef47056b6bd313dcbd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/13/2019
ms.locfileid: "1629758"
---
# <a name="add-links-to-websites-documents-or-programs-on-records"></a><span data-ttu-id="0c324-103">Bæta við tenglum á vefsíður, skjöl, eða forrit á skrám.</span><span class="sxs-lookup"><span data-stu-id="0c324-103">Add Links to Websites, Documents, or Programs on Records</span></span>
<span data-ttu-id="0c324-104">Á tilgreindri skrá, eins og t.d. viðskiptamanni, skjali eða sölupöntun, er hægt að bæta við tengli í ytra skjal, vefsíðu eða forrit.</span><span class="sxs-lookup"><span data-stu-id="0c324-104">On a specific record, such as a customer, document, or sales order, you can add a link to an external document, website, or program.</span></span> <span data-ttu-id="0c324-105">Einnig gæti verið þörf á tengli sem opnar nýjan auðan tölvupóst á tiltekinn viðtakanda þegar hann er valinn.</span><span class="sxs-lookup"><span data-stu-id="0c324-105">Or, you may want a link that opens a new empty email to a specific recipient when you select it.</span></span> <span data-ttu-id="0c324-106">Spjaldasíðan fyrir sumar skrár, s.s. viðskiptamanna- eða lánardrottnaspjöld, innihalda reitinn **Heimasíða** þar sem hægt er að færa inn vefslóð (URL).</span><span class="sxs-lookup"><span data-stu-id="0c324-106">The card page for some records, such as customer and vendor cards, include a **Home Page** field where you can enter an Internet address (URL).</span></span> <span data-ttu-id="0c324-107">Til að hafa aðra tengla með er hægt að nota aðferðina sem lýst er í þessari grein.</span><span class="sxs-lookup"><span data-stu-id="0c324-107">To include other links, you can use the method described in this article.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="0c324-108">Eins og er þá er þessi eiginleiki aðeins í boði í [!INCLUDE [prodshort](includes/prodshort.md)] fyrir virkjun á staðnum með eldri Dynamics NAV Windows biðlara.</span><span class="sxs-lookup"><span data-stu-id="0c324-108">Currently, this capability is available only in [!INCLUDE [prodshort](includes/prodshort.md)] on-premises deployments with the legacy Dynamics NAV Windows client.</span></span>  

<span data-ttu-id="0c324-109">Annað dæmi gæti verið þegar þú tekur á móti prentuðum reikningum frá lánardrottnum.</span><span class="sxs-lookup"><span data-stu-id="0c324-109">Another example could be when you receive printed invoices from vendors.</span></span> <span data-ttu-id="0c324-110">Hægt að skanna þá inn og geyma sem pdf-skrár á SharePoint svæði.</span><span class="sxs-lookup"><span data-stu-id="0c324-110">You can scan them and store them as .pdf files on a SharePoint site.</span></span> <span data-ttu-id="0c324-111">Síðan hægt er að búa til tengil úr innkaupareikningi í [!INCLUDE[d365fin_md](includes/d365fin_md.md)] við viðkomandi reikning í SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0c324-111">Then you can make a link from a purchase invoice in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] to the corresponding invoice on  SharePoint.</span></span> <span data-ttu-id="0c324-112">Einnig er hægt að tengja af vöruspjaldi yfir á samsvarandi síðu í netvörulista lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="0c324-112">Or, you can make a link from an item card to the corresponding page in your vendor's online catalog.</span></span>

## <a name="to-add-a-link-on-a-record"></a><span data-ttu-id="0c324-113">Bæta tengli við skrá</span><span class="sxs-lookup"><span data-stu-id="0c324-113">To add a link on a record</span></span>   

1.  <span data-ttu-id="0c324-114">Færslan sem á að tengja við er opnuð, t.d. viðskiptamannaspjald eða sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="0c324-114">Open the record that you want to attach the link to, such as a customer card or sales order.</span></span> <span data-ttu-id="0c324-115">Ef tengja á við sérstaka línu, t.d. færslubókarlínu, er hún valin.</span><span class="sxs-lookup"><span data-stu-id="0c324-115">If you want to attach the link to a specific line, such as a journal line, select the line.</span></span>  

2.  <span data-ttu-id="0c324-116">Velja aðgerðina **Tenglar** til að opna síðurnar **Tenglar** sem sýna alla núgildandi tengla sem hefur verið bætt við skrána.</span><span class="sxs-lookup"><span data-stu-id="0c324-116">Choose the **Links** action to open the **Links** pages that shows all the current links that are added to the record.</span></span>

3. <span data-ttu-id="0c324-117">Til að bæta við nýjum tengli, skal velja **+nýr**.</span><span class="sxs-lookup"><span data-stu-id="0c324-117">To add a new link, choose **+new**.</span></span>

4.  <span data-ttu-id="0c324-118">Í reitnum **Tengill aðsetur** færið inn</span><span class="sxs-lookup"><span data-stu-id="0c324-118">In the **Link Address** field, enter</span></span>

    -   <span data-ttu-id="0c324-119">Til að tengja skrá á þinni tölvu eða neti, skaltu færa inn fulla slóð og skráarheiti, eins og t.d. **C:\My Documents\invoice1.doc**.</span><span class="sxs-lookup"><span data-stu-id="0c324-119">To link to a file on your computer or network, enter the full path and file name, such as  **C:\My Documents\invoice1.doc**.</span></span>
    -   <span data-ttu-id="0c324-120">Til að tengja á vefsíðu, færa inn vefslóðina (URL) eins og t.d. **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="0c324-120">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="0c324-121">Til að tengja forrit, færa inn tilgreindan streng til að opna forritið.</span><span class="sxs-lookup"><span data-stu-id="0c324-121">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="0c324-122">Til dæmis til að opna OneNote með tiltekinni síðu skal slá inn **onenote:///C:\My Documents/test.one**.</span><span class="sxs-lookup"><span data-stu-id="0c324-122">For example, to open OneNote with a specific page, enter **onenote:///C:\My Documents/test.one**.</span></span> <span data-ttu-id="0c324-123">Eða, til að opna Outlook með nýjum tómum tölvupósti til tiltekins viðtakanda skal færa inn **mailto:testalias**.</span><span class="sxs-lookup"><span data-stu-id="0c324-123">Or, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5.  <span data-ttu-id="0c324-124">Reiturinn **Lýsing** er fylltur út með upplýsingum um tengilinn.</span><span class="sxs-lookup"><span data-stu-id="0c324-124">Fill in the **Description** field with information about the link.</span></span>  

6.  <span data-ttu-id="0c324-125">Veldu hnappinn **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0c324-125">Choose the **Save** button.</span></span>  

## <a name="to-delete-a-link-from-a-record"></a><span data-ttu-id="0c324-126">Til að eyða tengli úr færslu:</span><span class="sxs-lookup"><span data-stu-id="0c324-126">To delete a link from a record</span></span>  

<span data-ttu-id="0c324-127">Til að eyða tengli, í **Tenglar** á síðunni geturðu valið **...** og svo **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="0c324-127">To delete a link, on the **Links** page, you can select **...** and then **Delete**.</span></span>

<span data-ttu-id="0c324-128">Ef notandi eyðir einni færslu, t.d. sölupöntunarlínu, sölupöntun eða viðskiptamanni, er öllum tenglum þeirrar færslu líka eytt.</span><span class="sxs-lookup"><span data-stu-id="0c324-128">If you delete a single record, such as a sales order line, a sales order, or a customer, then all the links attached to the record are deleted.</span></span> <span data-ttu-id="0c324-129">Ef færslum er hins vegar eytt með runuvinnslu, t.d. runuvinnslunni **Eyða reikningsfærðum sölupöntunum**, eru tenglarnir geymdir áfram í töflunni .</span><span class="sxs-lookup"><span data-stu-id="0c324-129">However, if you delete records using a batch job, such as the **Delete Invoiced Sales Orders** batch job, then the links are still stored in the database.</span></span> <span data-ttu-id="0c324-130">Til að eyða tenglunum úr gagnagrunninum þarf að keyra kótaeininguna **Eyða færslutenglum án tilvísana**.</span><span class="sxs-lookup"><span data-stu-id="0c324-130">To delete the links from the database, run the **Delete Orphaned Record Links** codeunit.</span></span> <span data-ttu-id="0c324-131">Til að gera þetta skaltu velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða færslutenglum án tilvísana** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="0c324-131">To do this, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Orphaned Record Links**, and then choose the related link.</span></span>   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a><span data-ttu-id="0c324-132">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0c324-132">See Also</span></span>  
<span data-ttu-id="0c324-133">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0c324-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
