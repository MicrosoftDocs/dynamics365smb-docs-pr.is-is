---
title: Senda rafræn skjöl | Microsoft Docs
description: lærðu hvernig á að senda reikninga rafrænt
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8cb28db63e977cf02b81daa7043b64838406161f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251606"
---
# <a name="send-electronic-documents"></a><span data-ttu-id="1d9fd-103">Senda rafræn skjöl</span><span class="sxs-lookup"><span data-stu-id="1d9fd-103">Send Electronic Documents</span></span>
<span data-ttu-id="1d9fd-104">Almenn útgáfa [!INCLUDE[d365fin](includes/d365fin_md.md)] styður sendingu rafrænna reikninga og kreditreikninga á PEPPOL-sniði, sem er stutt af stærstu skjalaskiptaþjónustuaðilunum.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-104">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] supports sending electronic invoices and credit memos in the PEPPOL format, which is supported by the largest document exchange service providers.</span></span> <span data-ttu-id="1d9fd-105">Þjónustuaðili í skjalaskiptaþjónustu sendir rafræn skjöl á milli viðskiptaaðila.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="1d9fd-106">Til að veita stuðning á öðrum rafrænu formi er notaður gagnaskiptarammi.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="1d9fd-107">Í almennri útgáfu af [!INCLUDE[d365fin](includes/d365fin_md.md)] er skjalaskiptaþjónusta forstillt og tilbúinn til uppsetningar fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-107">In the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="1d9fd-108">Frekari upplýsingar, sjá [Setja upp skjalaskiptaþjónustu](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="1d9fd-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span>  

 <span data-ttu-id="1d9fd-109">Til að senda sölureikningi sem rafrænt PEPPOL-skjal er valinn valkosturinn **Rafrænt skjal** í **Bóka og senda** svarglugganum þar sem einnig er hægt að setja það upp sem sjálfgefið sendisnið skjals viðskiptamannsins.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-109">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box from where you can also set up the customer’s default document sending profile.</span></span> <span data-ttu-id="1d9fd-110">Fyrst þarf að setja upp mismunandi aðalgögn, t.d. upplýsingar um fyrirtækið, viðskiptavini, atriði, og mælieiningar.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-110">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="1d9fd-111">Þau eru notuð til að bera kennsl á viðskiptafélaga og vörur þegar gögnum er umbreytt í reiti í [Setja upp rafræn skjöl sending og móttaka](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="1d9fd-111">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="1d9fd-112">Til að senda rafrænan sölureikning</span><span class="sxs-lookup"><span data-stu-id="1d9fd-112">To send an electronic sales invoice</span></span>  

1.  <span data-ttu-id="1d9fd-113">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölureikningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="1d9fd-114">Nýr sölureikningur er búinn til.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-114">Create a new sales invoice.</span></span>  

3.  <span data-ttu-id="1d9fd-115">Þegar hægt er að reikningsfæra sölureikninginn, á **Aðgerðir** flipanum í flokknum **Bókun** er valið **Bóka og senda**.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-115">When the sales invoice is ready to be invoiced, on the **Actions** tab, in the **Posting** group, choose **Post and Send**.</span></span>  

     <span data-ttu-id="1d9fd-116">Ef sjálfgefið sendisnið viðskiptamannsins er **Rafrænt skjal**, mun það sjást í **Bóka og senda staðfestingu** svarglugganum og aðeins þarf að velja **Já** hnappinn til að bóka og senda reikninginn rafrænt á völdu sniði.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-116">If the customer’s default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box and you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4.  <span data-ttu-id="1d9fd-117">Í **Bóka og senda staðfestingu** svarglugganum er hnappurinn AssistEdit til hægri við **Senda skjal til** reitinn valinn.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-117">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5.  <span data-ttu-id="1d9fd-118">Í **Senda skjal til** svarglugganum í á **Rafrænt skjal** reitnum er valið **Gegnum skjalaskiptaþjónustu**.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-118">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6.  <span data-ttu-id="1d9fd-119">Í **Snið** reitnum er valið **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-119">In the **Format** field, choose **PEPPOL**.</span></span>  

7.  <span data-ttu-id="1d9fd-120">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-120">Choose the **OK** button.</span></span> <span data-ttu-id="1d9fd-121">Svarglugginn **Bóka og senda staðfestingu** birtist.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-121">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="1d9fd-122">**Rafrænt skjal (PEPPOL)** er bætt við **Senda skjal til** reitinn.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-122">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8.  <span data-ttu-id="1d9fd-123">Velja hnappinn **Já**.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-123">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="1d9fd-124">Sölureikningur er bókaður og sendur til viðskiptamannsins sem rafrænt skjal á PEPPOL-sniði.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-124">The sales invoice is posted and sent to the customer as an electronic document in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="1d9fd-125">Einnig er hægt að senda bókaða sölureikninga sem rafrænt skjal.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-125">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="1d9fd-126">Ferlið er það sama og lýst er í þessu efnisatriði fyrir óbókuð söluskjöl.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-126">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="1d9fd-127">Á síðunni **Bókaðir sölureikningar**, á flipanum **Aðgerðir**, í flokknum **Almennt**, veljið **Aðgerðakladdi** til að skoða stöðu rafræna skjalsins.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-127">On the **Posted Sales Invoice** page, on the **Actions** tab, in the **General** group, choose **Activity Log** to view the status of the electronic document.</span></span> <span data-ttu-id="1d9fd-128">Frekari upplýsingar, sjá **Aðgerðakladdi**.</span><span class="sxs-lookup"><span data-stu-id="1d9fd-128">For more information, see **Activity Log**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1d9fd-129">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1d9fd-129">See Also</span></span>  
[<span data-ttu-id="1d9fd-130">Reikningsfæra sölur</span><span class="sxs-lookup"><span data-stu-id="1d9fd-130">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="1d9fd-131">Setja upp sendisnið skjala</span><span class="sxs-lookup"><span data-stu-id="1d9fd-131">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="1d9fd-132">Setja upp sendingu og móttöku rafrænna skjala</span><span class="sxs-lookup"><span data-stu-id="1d9fd-132">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="1d9fd-133">Setja upp skjalaskiptaþjónustu</span><span class="sxs-lookup"><span data-stu-id="1d9fd-133">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="1d9fd-134">Setja upp skilgreiningar gagnaskipta</span><span class="sxs-lookup"><span data-stu-id="1d9fd-134">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="1d9fd-135">Rafræn gagnaskipti</span><span class="sxs-lookup"><span data-stu-id="1d9fd-135">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="1d9fd-136">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="1d9fd-136">General Business Functionality</span></span>](ui-across-business-areas.md)  
