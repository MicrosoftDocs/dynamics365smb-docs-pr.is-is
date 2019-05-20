---
title: Setja upp SEPA kreditfærsla | Microsoft Docs
description: Kynntu þér hvernig á að setja upp SEPA-kreditfærslur í Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sepa, credit, transfer, payment,
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer
ms.openlocfilehash: 56f200d00345bfe18d8fcccbee6493785fe6a034
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238234"
---
# <a name="set-up-sepa-credit-transfer"></a><span data-ttu-id="c26fd-103">Setja upp SEPA-kreditfærslur</span><span class="sxs-lookup"><span data-stu-id="c26fd-103">Set Up SEPA Credit Transfer</span></span>
<span data-ttu-id="c26fd-104">Af síðunni **Greiðslubók** er hægt að flytja út greiðslur í skrá til upphals í netbanka til vinnslu á tengdum peningamillifærslum.</span><span class="sxs-lookup"><span data-stu-id="c26fd-104">From the **Payment Journal** page, you can export payments to a file for upload to your electronic bank for processing of the related money transfers.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="c26fd-105">styður SEPA-kreditfærslusniðið, en í heimalandi þínu / svæði geta önnur snið fyrir rafrænar greiðslur kunna að vera tiltækir.</span><span class="sxs-lookup"><span data-stu-id="c26fd-105">supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>  

<span data-ttu-id="c26fd-106">Til að opna fyrir útflutning af skráasniði bankaskrár sem ekki eru studdar af [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að setja upp gagnaskiptaskilgreiningu með því að nota gagnaskiptaumgjörð.</span><span class="sxs-lookup"><span data-stu-id="c26fd-106">To enable export of a bank file formats that are not supported out of the box in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can set up a data exchange definition by using the data exchange framework.</span></span> <span data-ttu-id="c26fd-107">Frekari upplýsingar er að finna í [Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="c26fd-107">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

<span data-ttu-id="c26fd-108">Áður en þú getur afgreitt greiðslu rafrænt með því að flytja greiðsluskrár í SEPA-kreditfærslusnið, verður þú að framkvæma eftirfarandi uppsetningarskref:</span><span class="sxs-lookup"><span data-stu-id="c26fd-108">Before you can process payment electronically by exporting payment files in the SEPA Credit Transfer format, you must perform the following setup steps:</span></span>  

* <span data-ttu-id="c26fd-109">Setja upp viðkomandi bankareikning til að meðhöndla SEPA-kreditfærslusnið.</span><span class="sxs-lookup"><span data-stu-id="c26fd-109">Set up the bank account in question to handle the SEPA Credit Transfer format</span></span>  
* <span data-ttu-id="c26fd-110">Setja upp lánardrottinn spjöld með því að flytja skrár úr í SEPA-kreditmillifærslur sniði.</span><span class="sxs-lookup"><span data-stu-id="c26fd-110">Set up vendor cards to process payments by exporting files in the SEPA Credit Transfer format</span></span>  
* <span data-ttu-id="c26fd-111">Setja upp viðeigandi bókarkeyrslu til að gera virkan útflutning greiðslu af **Greiðslubók** síðunni</span><span class="sxs-lookup"><span data-stu-id="c26fd-111">Set up the related general journal batch to enable payment export from the **Payment Journal** page</span></span>  
* <span data-ttu-id="c26fd-112">Tengja gagnaskiptaskilgreiningu fyrir eina eða fleiri greiðslugerðir með viðeigandi greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="c26fd-112">Connect the data exchange definition for one or more payment types with the relevant payment method or methods</span></span>  

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a><span data-ttu-id="c26fd-113">Að setja upp bankareikning fyrir SEPA-kreditfærslu</span><span class="sxs-lookup"><span data-stu-id="c26fd-113">To set up a bank account for SEPA Credit Transfer</span></span>  
1. <span data-ttu-id="c26fd-114">Í reitinn **Leita** skal færa inn **Bankareikningar** og velja síðan viðkomandi tengi.</span><span class="sxs-lookup"><span data-stu-id="c26fd-114">In the **Search** box, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c26fd-115">Opnið spjald bankareikningsins sem á að flytja greiðsluskrár úr á SEPA-kreditfærslusniði.</span><span class="sxs-lookup"><span data-stu-id="c26fd-115">Open the card of the bank account from which you will export payment files in the SEPA Credit Transfer format.</span></span>  
3. <span data-ttu-id="c26fd-116">Á flýtiflipanum **Millifærsla**, í reitnum **Útflutningssvið greiðslu** skal velja **SEPADD**.</span><span class="sxs-lookup"><span data-stu-id="c26fd-116">On the **Transfer** FastTab, in the **Payment Export Format** field, choose **SEPADD**.</span></span>  
4. <span data-ttu-id="c26fd-117">Í **SEPA Kreditfærsla skilaboð kenni númeraröð** reitnum skal velja númeraröð sem tölum eru úthlutað úr til SEPA-kreditfærslu.</span><span class="sxs-lookup"><span data-stu-id="c26fd-117">In the **SEPA CT Msg. ID No. Series** field, choose a number series from which numbers are assigned to SEPA credit transfer entries.</span></span>  
5. <span data-ttu-id="c26fd-118">Gangið úr skugga um að reiturinn **IBAN** sé útfylltur.</span><span class="sxs-lookup"><span data-stu-id="c26fd-118">Make sure the **IBAN** field is filled.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="c26fd-119">Reiturinn **Gjaldmiðilskóði** verður að vera stilltur á **EUR**, því SEPA-kreditmillifærslur er aðeins hægt að gera í evrum.</span><span class="sxs-lookup"><span data-stu-id="c26fd-119">The **Currency Code** field must be set to **EUR**, because SEPA credit transfers can only be made in the EURO currency.</span></span>  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a><span data-ttu-id="c26fd-120">Að setja upp lánardrottin fyrir SEPA-kreditfærslu</span><span class="sxs-lookup"><span data-stu-id="c26fd-120">To set up a vendor card for SEPA Credit Transfer</span></span>  
1. <span data-ttu-id="c26fd-121">Í reitnum **Leita** skal færa inn **Lánardrottnar** og velja síðan viðkomandi tengi.</span><span class="sxs-lookup"><span data-stu-id="c26fd-121">In the **Search** box, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c26fd-122">Opnið spjald lánardrottins sem á að greiða til rafrænt útflutningi greiðsluskráa á SEPA-kreditfærslusniði.</span><span class="sxs-lookup"><span data-stu-id="c26fd-122">Open the card of the vendor whom you will pay electronically by export payment files in the SEPA Credit Transfer format.</span></span>  
3. <span data-ttu-id="c26fd-123">Á flýtiflipanum **Greiðsla**, í reitnum **Kóði greiðslumáta** skal velja **BANKI**.</span><span class="sxs-lookup"><span data-stu-id="c26fd-123">On the **Payment** FastTab, in the **Payment Method Code** field, choose **BANK**.</span></span>  
4. <span data-ttu-id="c26fd-124">Í **Valinn bankareikningur** reitnum, veldu banka sem fé verður flutt inn á þegar það er unnið með rafrænum bankann þinn.</span><span class="sxs-lookup"><span data-stu-id="c26fd-124">In the **Preferred Bank Account** field, choose the bank to which the money will be transferred when it is processed by your electronic bank.</span></span>  

     <span data-ttu-id="c26fd-125">Gildið í reitnum **Valinn bankareikningur** er afritað í reitinn **Móttökubankareikningur** á síðunni **Greiðslubók**.</span><span class="sxs-lookup"><span data-stu-id="c26fd-125">The value in the **Preferred Bank Account** field is copied to the **Recipient Bank Account** field on the **Payment Journal** page.</span></span>  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a><span data-ttu-id="c26fd-126">Að stilla greiðslubók upp til að flytja greiðsluskrár</span><span class="sxs-lookup"><span data-stu-id="c26fd-126">To set the payment journal up to export payment files</span></span>  
1. <span data-ttu-id="c26fd-127">Í reitnum **Leit** skal færa inn **Greiðslubækur** og velja síðan viðkomandi tengil.</span><span class="sxs-lookup"><span data-stu-id="c26fd-127">In the **Search** box, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c26fd-128">Opnið greiðslubókina sem á að nota til vinna greiðslur með því að flytja skrár á SEPA-kreditfærslusniði.</span><span class="sxs-lookup"><span data-stu-id="c26fd-128">Open the payment journal that you use to process payments by exporting files in the SEPA Credit Transfer format.</span></span>  
3. <span data-ttu-id="c26fd-129">Í reitnum **Heiti keyrslu** er felli\-lista hnappurinn valinn.</span><span class="sxs-lookup"><span data-stu-id="c26fd-129">In the **Batch Name** field, choose the drop\-down button.</span></span>  
4. <span data-ttu-id="c26fd-130">Á síðunni **Færslubókarkeyrslur** á flipanum **Heim**, í flokknum **Stjórna**, skal velja **Breyta lista**.</span><span class="sxs-lookup"><span data-stu-id="c26fd-130">On the **General Journal Batches** page, on the **Home** tab, in the **Manage** group, choose **Edit List**.</span></span>  
5. <span data-ttu-id="c26fd-131">Á línunni fyrir greiðslubókina sem notuð verður til að flytja út greiðslur skal velja gátreitinn **Leyfa greiðsluútflutning**.</span><span class="sxs-lookup"><span data-stu-id="c26fd-131">On the line for the payment journal that you will use to export payments, select the **Allow Payment Export** check box.</span></span>  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a><span data-ttu-id="c26fd-132">Tengja gagnaskiptaskilgreiningu fyrir eina eða fleiri greiðslugerðir með viðeigandi greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="c26fd-132">To connect the data exchange definition for one or more payment types with the relevant payment method or methods</span></span>  
1. <span data-ttu-id="c26fd-133">Í reitnum **Leit** skal færa inn **Greiðsluhættir** og velja síðan viðkomandi tengil.</span><span class="sxs-lookup"><span data-stu-id="c26fd-133">In the **Search** box, enter **Payment Methods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c26fd-134">Á síðunni **Greiðslumáti** skaltu velja greiðslumáta sem er notað til að flytja út greiðslur frá, og þá velja **Greiðsluútflutningur Línuskilgreining** reitinn.</span><span class="sxs-lookup"><span data-stu-id="c26fd-134">On the **Payment Methods** page, select the payment method that is used to export payments from, and then choose the **Pmt. Export Line Definition** field.</span></span>  
3. <span data-ttu-id="c26fd-135">Á síðunni **Greiðsluútflutningur Línuskilgreining** skal velja kóðann sem var tilgreindur í **Kóði** reitnum á **Línuskilgreiningar** flýtiflipanum í skrefi 4 í „Að lýsa sniði lína og dálka í skránni“ hlutanum í [Setja upp gagnaskiptaskilgreiningar](across-how-to-set-up-data-exchange-definitions.md) aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="c26fd-135">On the **Pmt. Export Line Definitions** page, select the code that you specified in the **Code** field on the **Line Definitions** FastTab in step 4 in the “To describe the formatting of lines and columns in the file” section in the [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) procedure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c26fd-136">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="c26fd-136">See Also</span></span>  
[<span data-ttu-id="c26fd-137">Innheimta greiðslur með SEPA-beingreiðslum</span><span class="sxs-lookup"><span data-stu-id="c26fd-137">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="c26fd-138">Setja upp skilgreiningar gagnaskipta</span><span class="sxs-lookup"><span data-stu-id="c26fd-138">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="c26fd-139">Stofna ítrekaðar sölu- og innkaupalínur</span><span class="sxs-lookup"><span data-stu-id="c26fd-139">Create Recurring Sales and Purchase Lines</span></span>](sales-how-work-standard-lines.md)  
[<span data-ttu-id="c26fd-140">Rafræn gagnaskipti</span><span class="sxs-lookup"><span data-stu-id="c26fd-140">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
