---
title: "Hvernig á að tengja úr skrám í ytri upplýsingar eða forrit | Microsoft Docs"
description: "Setja tengil í skjal eða vefsíðu á tiltekna skrá, s.s. viðskiptavin eða fylgiskjal."
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 8eee2a93a56c33fd5cefb70c475e237166017606
ms.contentlocale: is-is
ms.lasthandoff: 11/10/2017

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a><span data-ttu-id="bf4e0-103">Bæta við tengli á vefsíður, skjöl, eða forrit á skrám.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-103">Adding Links to Websites, Documents, or Programs on Records</span></span>
<span data-ttu-id="bf4e0-104">Á tilgreindri skrá, eins og t.d. viðskiptamanni, skjali eða sölupöntun, er hægt að bæta við tengli í ytra skjal, vefsíðu eða forrit.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-104">On a specific record, such as a customer, document, or sales order, you can add a link to an external document, website, or program.</span></span> <span data-ttu-id="bf4e0-105">Einnig gæti verið þörf á tengli sem opnar nýjan auðan tölvupóst á tiltekinn viðtakanda þegar hann er valinn.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-105">Or, you may want a link that opens a new empty email to a specific recipient when you select it.</span></span> <span data-ttu-id="bf4e0-106">Spjaldasíðan fyrir sumar skrár, s.s. viðskiptamanna- eða lánardrottnaspjöld, innihalda reitinn **Heimasíða** þar sem hægt er að færa inn vefslóð (URL).</span><span class="sxs-lookup"><span data-stu-id="bf4e0-106">The card page for some records, such as customer and vendor cards, include a **Home Page** field where you can enter an Internet address (URL).</span></span> <span data-ttu-id="bf4e0-107">Til að hafa aðra tengla með er hægt að nota aðferðina sem lýst er í þessari grein.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-107">To include other links, you can use the method described in this article.</span></span>

<span data-ttu-id="bf4e0-108">Annað dæmi gæti verið þegar þú tekur á móti prentuðum reikningum frá lánardrottnum.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-108">Another example could be when you receive printed invoices from vendors.</span></span> <span data-ttu-id="bf4e0-109">Hægt að skanna þá inn og geyma sem pdf-skrár á SharePoint-setri.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-109">You can scan them and store them as .pdf files on a SharePoint site.</span></span> <span data-ttu-id="bf4e0-110">Síðan hægt er að búa til tengil úr innkaupareikningi í [!INCLUDE[d365fin_md](includes/d365fin_md.md)] við viðkomandi reikning í SharePoint.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-110">Then you can make a link from a purchase invoice in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] to the corresponding invoice on  SharePoint.</span></span> <span data-ttu-id="bf4e0-111">Einnig er hægt að tengja af vöruspjaldi yfir á samsvarandi síðu í netvörulista lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-111">Or, you can make a link from an item card to the corresponding page in your vendor's online catalog.</span></span>

## <a name="to-add-a-link-on-a-record"></a><span data-ttu-id="bf4e0-112">Bæta tengli við skrá</span><span class="sxs-lookup"><span data-stu-id="bf4e0-112">To add a link on a record</span></span>   

1.  <span data-ttu-id="bf4e0-113">Færslan sem á að tengja við er opnuð, t.d. viðskiptamannaspjald eða sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-113">Open the record that you want to attach the link to, such as a customer card or sales order.</span></span> <span data-ttu-id="bf4e0-114">Ef tengja á við sérstaka línu, t.d. færslubókarlínu, er hún valin.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-114">If you want to attach the link to a specific line, such as a journal line, select the line.</span></span>  

2.  <span data-ttu-id="bf4e0-115">Velja aðgerðin **Tenglar** til að opna gluggana **Tenglar** sem sýna alla núgildandi tengla sem hefur verið bætt við skrána.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-115">Choose the **Links** action to open the **Links** windows that shows all the current links that are added to the record.</span></span>

3. <span data-ttu-id="bf4e0-116">Til að bæta við nýjum tengli, skal velja **+nýr**.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-116">To add a new link, choose **+new**.</span></span>

4.  <span data-ttu-id="bf4e0-117">Í reitnum **Tengill aðsetur** færið inn</span><span class="sxs-lookup"><span data-stu-id="bf4e0-117">In the **Link Address** field, enter</span></span>

    -   <span data-ttu-id="bf4e0-118">Til að tengja skrá á þinni tölvu eða neti, færa inn fulla slóð og skráarheiti, eins og t.d. **C:My Documentsinvoice1.doc**.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-118">To link to a file on your computer or network, enter the full path and file name, such as  **C:My Documentsinvoice1.doc**.</span></span>
    -   <span data-ttu-id="bf4e0-119">Til að tengja á vefsíðu, færa inn vefslóðina (URL) eins og t.d. **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-119">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="bf4e0-120">Til að tengja á vefsíðu, færa inn vefslóðina (URL) eins og t.d. **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-120">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="bf4e0-121">Til að tengja forrit, færa inn tilgreindan streng til að opna forritið.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-121">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="bf4e0-122">Til dæmis, til að opna OneNote með tilgreindri síðu, færa inn **onenote:///C:My Documentstest.one**.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-122">For example, to open OneNote with a specific page, enter **onenote:///C:My Documentstest.one**.</span></span> <span data-ttu-id="bf4e0-123">Eða, til að opna Outlook með nýjum tómum tölvupósti til tiltekins viðtakanda skal færa inn **mailto:testalias**.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-123">Or, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5.  <span data-ttu-id="bf4e0-124">Reiturinn **Lýsing** er fylltur út með upplýsingum um tengilinn.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-124">Fill in the **Description** field with information about the link.</span></span>  

6.  <span data-ttu-id="bf4e0-125">Veldu hnappinn **Vista**.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-125">Choose the **Save** button.</span></span>  

## <a name="to-delete-a-link-from-a-record"></a><span data-ttu-id="bf4e0-126">Til að eyða tengli úr færslu:</span><span class="sxs-lookup"><span data-stu-id="bf4e0-126">To delete a link from a record</span></span>  

<span data-ttu-id="bf4e0-127">Til að eyða tengli, í **Tenglar** í glugganum geturðu valið **...** og svo **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-127">To delete a link, in the **Links** window, you can select **...** and then **Delete**.</span></span>

<span data-ttu-id="bf4e0-128">Ef notandi eyðir einni færslu, t.d. sölupöntunarlínu, sölupöntun eða viðskiptamanni, er öllum tenglum þeirrar færslu líka eytt.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-128">If you delete a single record, such as a sales order line, a sales order, or a customer, then all the links attached to the record are deleted.</span></span> <span data-ttu-id="bf4e0-129">Ef færslum er hins vegar eytt með runuvinnslu, t.d. runuvinnslunni **Eyða reikningsfærðum sölupöntunum**, eru tenglarnir geymdir áfram í töflunni .</span><span class="sxs-lookup"><span data-stu-id="bf4e0-129">However, if you delete records using a batch job, such as the **Delete Invoiced Sales Orders** batch job, then the links are still stored in the database.</span></span> <span data-ttu-id="bf4e0-130">Til að eyða tenglunum úr gagnagrunninum þarf að keyra kótaeininguna **Eyða færslutenglum án tilvísana**.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-130">To delete the links from the database, run the **Delete Orphaned Record Links** codeunit.</span></span> <span data-ttu-id="bf4e0-131">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Eyða færslutenglum án tilvísana** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="bf4e0-131">To do this, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Orphaned Record Links**, and then choose the related link.</span></span>   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a><span data-ttu-id="bf4e0-132">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="bf4e0-132">See Also</span></span>  
<span data-ttu-id="bf4e0-133">[Unnið með [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bf4e0-133">[Working with [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  

