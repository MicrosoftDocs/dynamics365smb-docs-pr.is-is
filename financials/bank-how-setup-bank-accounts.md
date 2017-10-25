---
title: Uppsetning bankareikninga| Microsoft Docs
description: "Hægt er að afstemma bankareikninga í Financials við yfirlit frá bankanum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: f46e95e24ef39a93bc93cfda1b9c575b07273566
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-bank-accounts"></a><span data-ttu-id="da68b-103">Hvernig á að setja upp Bankareikninga lánardrottna</span><span class="sxs-lookup"><span data-stu-id="da68b-103">How to: Set Up Bank Accounts</span></span>
<span data-ttu-id="da68b-104">Þú notar bankareikninga í [!INCLUDE[d365fin](includes/d365fin_md.md)] til að fylgjast með bankafærslunum þínum.</span><span class="sxs-lookup"><span data-stu-id="da68b-104">You use bank accounts in the [!INCLUDE[d365fin](includes/d365fin_md.md)] to keep track of your banking transactions.</span></span> <span data-ttu-id="da68b-105">Hægt er að hafa reikninga í SGM eða erlendum gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="da68b-105">Accounts can be denominated in your local currency or in a foreign currency.</span></span> <span data-ttu-id="da68b-106">Þegar bankareikningar hafa verið settir upp er einnig hægt að nota valkostinn prentskoðun.</span><span class="sxs-lookup"><span data-stu-id="da68b-106">After you have set up bank accounts, you can also use the check printing option.</span></span>

## <a name="to-set-up-bank-accounts"></a><span data-ttu-id="da68b-107">Bankareikningar settir upp</span><span class="sxs-lookup"><span data-stu-id="da68b-107">To set up bank accounts</span></span>
1. <span data-ttu-id="da68b-108">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bankareikningar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="da68b-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="da68b-109">Í glugganum **bankareikningar** skal velja aðgerðina **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="da68b-109">In the **Bank Accounts** window, choose the **New** action.</span></span>
3. <span data-ttu-id="da68b-110">Fyllið inn í svæðin eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="da68b-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a><span data-ttu-id="da68b-111">Til að setja upp bankareikning þinn til að flytja inn eða flytja út bankaskrár</span><span class="sxs-lookup"><span data-stu-id="da68b-111">To set up your bank account for import or export of bank files</span></span>
<span data-ttu-id="da68b-112">Reitir á **Flutningur** flýtiflipanum í **Bankareikningsspjald** glugganum eru tengdir innflutningi og útflutningi á banka straumum og skrám.</span><span class="sxs-lookup"><span data-stu-id="da68b-112">Fields on the **Transfer** FastTab in the **Bank Account Card** window are related to import and export of bank feeds and files.</span></span> <span data-ttu-id="da68b-113">Nánari upplýsingar er að finna í [Hvernig á að: Setja upp umskráningarþjónusta fyrir bankagögn](bank-how-setup-bank-data-conversion-service.md) og [hvernig á að: Setja upp Envestnet Yodlee Bank Feeds þjónustu](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="da68b-113">For more information, see [How to: Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md) and [How to: Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

1. <span data-ttu-id="da68b-114">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bankareikningar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="da68b-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="da68b-115">Opnaðu kortið fyrir bankareikning sem þú vilt flytja út eða flytja inn bankaskrár fyrir.</span><span class="sxs-lookup"><span data-stu-id="da68b-115">Open the card for a bank account that you will export or import bank files for.</span></span>
3. <span data-ttu-id="da68b-116">Fyllt er út í reiti eftir því sem við á í flýtiflipanum **Flytja**.</span><span class="sxs-lookup"><span data-stu-id="da68b-116">On the **Transfer** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="da68b-117">Mismunandi útflutningsþjónusta skráa og snið þeirra þurfa mismunandi uppsetningargildi í glugganum **Bankareikningsspjald**.</span><span class="sxs-lookup"><span data-stu-id="da68b-117">Different file export services and their formats require different setup values in the **Bank Account Card** window.</span></span> <span data-ttu-id="da68b-118">Þú færð að vita um uppsetningargildi sem eru röng eða sem vantar þegar þú reynir að flytja út skrána.</span><span class="sxs-lookup"><span data-stu-id="da68b-118">You will be informed about wrong or missing setup values as you try to export the file.</span></span> <span data-ttu-id="da68b-119">Svo lestu stuttar lýsingar á reitunum vandlega eða vísaðu til viðkomandi efnisferlis.</span><span class="sxs-lookup"><span data-stu-id="da68b-119">So read the short descriptions of the fields carefully or refer to the related procedure topics.</span></span> <span data-ttu-id="da68b-120">Til dæmis, við útflutning greiðsluskráar fyrir kortamillifærslu NA (EFT) þarf að fylla út reitina **Síðasta greiðslutilkynningarnúmer** og **Kenninúmer**.</span><span class="sxs-lookup"><span data-stu-id="da68b-120">For example, exporting a payment file for North American electronic funds transfer (EFT) requires that both the **Last Remittance Advice No.** field and the **Transit No.** field are filled in.</span></span> <span data-ttu-id="da68b-121">Nánari upplýsingar sjá [Hvernig: Flytja Greiðslur í bankaskrá](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="da68b-121">For more information, see [How to: Export Payments to a Bank File](payables-how-export-payments-bank-file.md).</span></span>

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a><span data-ttu-id="da68b-122">Til að setja upp bankareikninga lánardrottna fyrir útflutning bankaskráa</span><span class="sxs-lookup"><span data-stu-id="da68b-122">To set up vendor bank accounts for export of bank files</span></span>
<span data-ttu-id="da68b-123">Reitir á **Flutningur** flýtiflipanum í **Bankareikningsspjald lánardrottins** glugganum eru tengdir innflutningi og útflutningi á banka straumum og skrám.</span><span class="sxs-lookup"><span data-stu-id="da68b-123">Fields on the **Transfer** FastTab in the **Vendor Bank Account Card** window are related to export of bank feeds and files.</span></span> <span data-ttu-id="da68b-124">Nánari upplýsingar er að finna í [Hvernig á að: Setja upp umreikningsþjónustu fyrir bankagögn](bank-how-setup-bank-data-conversion-service.md) og [Hvernig á að: Flytja út greiðslur í bankaskrá](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="da68b-124">For more information, see [How to: Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md) and [How to: Export Payments to a Bank File](payables-how-export-payments-bank-file.md).</span></span>

1. <span data-ttu-id="da68b-125">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **lánardrottnar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="da68b-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="da68b-126">Opnaðu kortið fyrir lánardrottinn með bankareikning sem þú sendir út greiðslubankaskrár til.</span><span class="sxs-lookup"><span data-stu-id="da68b-126">Open the card for a vendor whose bank account you will export payment bank files to.</span></span>
3. <span data-ttu-id="da68b-127">Veldu aðgerðina **Bankareikningar**.</span><span class="sxs-lookup"><span data-stu-id="da68b-127">Choose the **Bank Accounts** action.</span></span>
3. <span data-ttu-id="da68b-128">Í glugganum **Bankareikn.spjald lánardr** á flipanum **Flutningur** fylltu inn reitina eftir því sem þörf er á.</span><span class="sxs-lookup"><span data-stu-id="da68b-128">In the **Vendor Bank Account Card** window, on the **Transfer** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="da68b-129">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="da68b-129">See Also</span></span>
[<span data-ttu-id="da68b-130">Uppsetning bankaþjónustu</span><span class="sxs-lookup"><span data-stu-id="da68b-130">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="da68b-131">Stjórna bankareikningum</span><span class="sxs-lookup"><span data-stu-id="da68b-131">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
<span data-ttu-id="da68b-132">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="da68b-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

