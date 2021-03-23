---
title: Senda rafræn skjöl
description: lærðu hvernig á að senda reikninga rafrænt
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d547f031d9d33c0d7cd5f8b20398fd7b6dbe0393
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383001"
---
# <a name="send-electronic-documents"></a><span data-ttu-id="6c662-103">Senda rafræn skjöl</span><span class="sxs-lookup"><span data-stu-id="6c662-103">Send Electronic Documents</span></span>

<span data-ttu-id="6c662-104">Almenn útgáfa [!INCLUDE[prod_short](includes/prod_short.md)] styður sendingu rafrænna reikninga og kreditreikninga á PEPPOL-sniði, sem er snið sem er stutt af stærstu skjalaskiptaþjónustuaðilunum.</span><span class="sxs-lookup"><span data-stu-id="6c662-104">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] supports sending electronic invoices and credit memos in the PEPPOL format, a format that the largest document exchange service providers support.</span></span> <span data-ttu-id="6c662-105">Þjónustuaðili í skjalaskiptaþjónustu sendir rafræn skjöl á milli viðskiptaaðila.</span><span class="sxs-lookup"><span data-stu-id="6c662-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="6c662-106">Til að veita stuðning á öðrum rafrænu formi er notaður gagnaskiptarammi.</span><span class="sxs-lookup"><span data-stu-id="6c662-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="6c662-107">Í almennri útgáfu af [!INCLUDE[prod_short](includes/prod_short.md)] er skjalaskiptaþjónusta forstillt og tilbúinn til uppsetningar fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="6c662-107">In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="6c662-108">Frekari upplýsingar, sjá [Setja upp skjalaskiptaþjónustu](across-how-to-set-up-a-document-exchange-service.md).</span><span class="sxs-lookup"><span data-stu-id="6c662-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span> <span data-ttu-id="6c662-109">Hins vegar verður í sumum tilvikum að setja upp forrit.</span><span class="sxs-lookup"><span data-stu-id="6c662-109">However, in some cases, you must install an app.</span></span> <span data-ttu-id="6c662-110">Frekari upplýsingar eru í [Algengar spurningar um rafrænar reikningsfærslur](faq-electronic-invoicing.yml).</span><span class="sxs-lookup"><span data-stu-id="6c662-110">For more information, see [Electronic Invoicing FAQ](faq-electronic-invoicing.yml).</span></span>  

 <span data-ttu-id="6c662-111">Til að senda sölureikning sem rafrænt PEPPOL-skjal skal velja sem **Rafrænt skjal** valkostinn í á **Bóka og senda** svargluggi.</span><span class="sxs-lookup"><span data-stu-id="6c662-111">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box.</span></span> <span data-ttu-id="6c662-112">Einnig er hægt setja upp sjálfgefna forstillingu skjalasendingar viðskiptamanns úr þeim svarglugga.</span><span class="sxs-lookup"><span data-stu-id="6c662-112">You can also set up the customer's default document sending profile from that dialog box.</span></span> <span data-ttu-id="6c662-113">Fyrst þarf að setja upp mismunandi aðalgögn, t.d. upplýsingar um fyrirtækið, viðskiptavini, atriði, og mælieiningar.</span><span class="sxs-lookup"><span data-stu-id="6c662-113">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="6c662-114">Þau eru notuð til að bera kennsl á viðskiptafélaga og vörur þegar gögnum er umbreytt í reiti í [Setja upp rafræn skjöl sending og móttaka](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="6c662-114">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="6c662-115">Til að senda rafrænan sölureikning</span><span class="sxs-lookup"><span data-stu-id="6c662-115">To send an electronic sales invoice</span></span>

1. <span data-ttu-id="6c662-116">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sölureikningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="6c662-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2. <span data-ttu-id="6c662-117">Nýr sölureikningur er búinn til.</span><span class="sxs-lookup"><span data-stu-id="6c662-117">Create a new sales invoice.</span></span>  

3. <span data-ttu-id="6c662-118">Þegar sölureikningurinn er tilbúinn til innheimtu skaltu velja aðgerðina **Bóka og senda**.</span><span class="sxs-lookup"><span data-stu-id="6c662-118">When the sales invoice is ready to be invoiced, choose the **Post and Send** action.</span></span>  

     <span data-ttu-id="6c662-119">Ef sjálfgefið sendisnið viðskiptamannsins er **Rafrænt skjal**, mun það sjást í **Bóka og senda staðfestingu** svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="6c662-119">If the customer's default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box.</span></span> <span data-ttu-id="6c662-120">Þannig þarf aðeins að velja **Já** hnappinn til að bóka og senda reikninginn rafrænt á völdu sniði.</span><span class="sxs-lookup"><span data-stu-id="6c662-120">This way, you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4. <span data-ttu-id="6c662-121">Í **Bóka og senda staðfestingu** svarglugganum er hnappurinn AssistEdit til hægri við **Senda skjal til** reitinn valinn.</span><span class="sxs-lookup"><span data-stu-id="6c662-121">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5. <span data-ttu-id="6c662-122">Í **Senda skjal til** svarglugganum í á **Rafrænt skjal** reitnum er valið **Gegnum skjalaskiptaþjónustu**.</span><span class="sxs-lookup"><span data-stu-id="6c662-122">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6. <span data-ttu-id="6c662-123">Í **Snið** reitnum er valið **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="6c662-123">In the **Format** field, choose **PEPPOL**.</span></span>  

7. <span data-ttu-id="6c662-124">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6c662-124">Choose the **OK** button.</span></span> <span data-ttu-id="6c662-125">Svarglugginn **Bóka og senda staðfestingu** birtist.</span><span class="sxs-lookup"><span data-stu-id="6c662-125">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="6c662-126">**Rafrænt skjal (PEPPOL)** er bætt við **Senda skjal til** reitinn.</span><span class="sxs-lookup"><span data-stu-id="6c662-126">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8. <span data-ttu-id="6c662-127">Velja hnappinn **Já**.</span><span class="sxs-lookup"><span data-stu-id="6c662-127">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="6c662-128">Sölureikningur er bókaður og sendur til viðskiptamannsins á PEPPOL-sniði.</span><span class="sxs-lookup"><span data-stu-id="6c662-128">The sales invoice is posted and sent to the customer in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="6c662-129">Einnig er hægt að senda bókaða sölureikninga sem rafrænt skjal.</span><span class="sxs-lookup"><span data-stu-id="6c662-129">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="6c662-130">Ferlið er það sama og lýst er í þessu efnisatriði fyrir óbókuð söluskjöl.</span><span class="sxs-lookup"><span data-stu-id="6c662-130">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="6c662-131">Á síðunni **Bókaður sölureikningur** skal velja aðgerðina **Aðgerðakladdi** til að skoða stöðu rafræna skjalsins.</span><span class="sxs-lookup"><span data-stu-id="6c662-131">On the **Posted Sales Invoice** page, choose the **Activity Log** action to view the status of the electronic document.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="6c662-132">Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="6c662-132">See Related Training at [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="6c662-133">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6c662-133">See Also</span></span>

[<span data-ttu-id="6c662-134">Reikningsfæra sölur</span><span class="sxs-lookup"><span data-stu-id="6c662-134">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="6c662-135">Setja upp sendisnið skjala</span><span class="sxs-lookup"><span data-stu-id="6c662-135">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="6c662-136">Setja upp sendingu og móttöku rafrænna skjala</span><span class="sxs-lookup"><span data-stu-id="6c662-136">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="6c662-137">Setja upp skjalaskiptaþjónustu</span><span class="sxs-lookup"><span data-stu-id="6c662-137">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="6c662-138">Setja upp skilgreiningar gagnaskipta</span><span class="sxs-lookup"><span data-stu-id="6c662-138">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="6c662-139">Rafræn gagnaskipti</span><span class="sxs-lookup"><span data-stu-id="6c662-139">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="6c662-140">Algengar spurningar um rafrænar reikningsfærslur</span><span class="sxs-lookup"><span data-stu-id="6c662-140">Electronic Invoicing FAQ</span></span>](faq-electronic-invoicing.yml)  
[<span data-ttu-id="6c662-141">Almenn viðskiptavirkni</span><span class="sxs-lookup"><span data-stu-id="6c662-141">General Business Functionality</span></span>](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]