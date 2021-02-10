---
title: Skýrsluval í Business Central
description: Kynntu þér hvernig á að setja upp skýrslurnar sem þú notar til að prenta ýmsar tegundir skjala í Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.date: 01/18/2021
ms.author: edupont
ms.openlocfilehash: d30baa44894658c03c3deffdf24a7923293b88fd
ms.sourcegitcommit: 32bfc2acaaf3693afc9aeb86feea505fd328caa1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/19/2021
ms.locfileid: "5024638"
---
# <a name="report-selection-in-business-central"></a><span data-ttu-id="c457e-103">Skýrsluval í Business Central</span><span class="sxs-lookup"><span data-stu-id="c457e-103">Report Selection in Business Central</span></span>

<span data-ttu-id="c457e-104">Hægt er að setja upp sjálfgefnar skýrslur sem verða notaðar til að prenta hin ýmsu skjöl fyrir sölu og innkaup, svo sem pantanir, tilboð, reikninga og kreditreikninga.</span><span class="sxs-lookup"><span data-stu-id="c457e-104">You can set up default reports that will be used to print the various documents for sales and purchases, such as orders, quotes, invoices, and credit memos.</span></span> <span data-ttu-id="c457e-105">Ef til dæmis um er að ræða tiltekið útlit fyrir sölureikninga er hægt að tilgreina þá skýrslu á síðunni **Skýrsluval - Sala** þannig að hún verði notuð til að senda eða prenta sölureikninga.</span><span class="sxs-lookup"><span data-stu-id="c457e-105">For example, if you have a specific layout for sales invoices, you can specify that report in the **Report Selections - Sales** page so that it will be used to send or print sales invoices.</span></span>  

<span data-ttu-id="c457e-106">Síðurnar **Skýrsluval** tilgreina hvaða skýrsla verður prentuð við mismunandi aðstæður.</span><span class="sxs-lookup"><span data-stu-id="c457e-106">The **Report Selections** pages specify which report will be printed in different situations.</span></span> <span data-ttu-id="c457e-107">[!INCLUDE [prod_short](includes/prod_short.md)] inniheldur sjálfgefnar skilgreiningar, en hægt er að breyta þeim.</span><span class="sxs-lookup"><span data-stu-id="c457e-107">[!INCLUDE [prod_short](includes/prod_short.md)] includes default configurations, but of course you can change these defaults.</span></span> <span data-ttu-id="c457e-108">Einnig er hægt að bæta skýrslum við síðurnar **Skýrsluval** ef á að prenta fleiri en eina skýrslu fyrir hverja skjalagerð sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="c457e-108">You can also add reports to the **Report Selection** pages if you want to print more than one report per document type, for example.</span></span>  

## <a name="available-report-selections"></a><span data-ttu-id="c457e-109">Skýrsluval í boði</span><span class="sxs-lookup"><span data-stu-id="c457e-109">Available report selections</span></span>

<span data-ttu-id="c457e-110">[!INCLUDE [prod_short](includes/prod_short.md)] inniheldur mismunandi síður **Skýrsluvals** fyrir mismunandi svæði.</span><span class="sxs-lookup"><span data-stu-id="c457e-110">[!INCLUDE [prod_short](includes/prod_short.md)] includes different **Report Selection** pages for different areas.</span></span> <span data-ttu-id="c457e-111">Eftirfarandi töflur útskýra hvar hægt er að finna upplýsingar um mismunandi síður.</span><span class="sxs-lookup"><span data-stu-id="c457e-111">The following tables describes where you can find information about the different pages.</span></span>  

|<span data-ttu-id="c457e-112">Svæði eða verkefni</span><span class="sxs-lookup"><span data-stu-id="c457e-112">Area or task</span></span>  |<span data-ttu-id="c457e-113">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c457e-113">Learn more</span></span>|
|--------------|----------|
|<span data-ttu-id="c457e-114">Dæmi um hvernig skýrsluval virkar (sala)</span><span class="sxs-lookup"><span data-stu-id="c457e-114">Example of how report selection works (Sales)</span></span>|[<span data-ttu-id="c457e-115">Skýrsluval fyrir söluskjöl</span><span class="sxs-lookup"><span data-stu-id="c457e-115">Report selection for sales documents</span></span>](#example-report-selection-for-sales-documents)|
|<span data-ttu-id="c457e-116">Sjálfgefið útlit fyrir tölvupósta með sölu- og innkaupaskjölum</span><span class="sxs-lookup"><span data-stu-id="c457e-116">Default layout for emails with sales and purchase documents</span></span>  |[<span data-ttu-id="c457e-117">Setja upp endurnýtanlega texta og útlit tölvupósts fyrir sölu- og innkaupaskjöl</span><span class="sxs-lookup"><span data-stu-id="c457e-117">Set Up Reusable Email Texts and Layouts for Sales and Purchase Documents</span></span>](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|<span data-ttu-id="c457e-118">Skilgreina útlit ávísana</span><span class="sxs-lookup"><span data-stu-id="c457e-118">Define check layouts</span></span>     |[<span data-ttu-id="c457e-119">Velja útlit ávísunar</span><span class="sxs-lookup"><span data-stu-id="c457e-119">Select a Check Layout</span></span>](finance-how-define-check-layouts.md) |
|<span data-ttu-id="c457e-120">Skilgreina skýrslur fyrir VSK-skýrslugerð (Þýskaland)</span><span class="sxs-lookup"><span data-stu-id="c457e-120">Define reports for VAT reporting (Germany)</span></span>|[<span data-ttu-id="c457e-121">Setja upp skýrslur fyrir VSK og Intrastat</span><span class="sxs-lookup"><span data-stu-id="c457e-121">Set Up Reports for VAT and Intrastat</span></span>](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> <span data-ttu-id="c457e-122">Sem dæmi getur [!INCLUDE [prod_short](includes/prod_short.md)] innihaldið fleiri síður **Skýrsluvals**, en það fer eftir staðsetningu þinni og atvinnugrein.</span><span class="sxs-lookup"><span data-stu-id="c457e-122">Your [!INCLUDE [prod_short](includes/prod_short.md)] can include additional **Report Selection** pages, depending on your location and industry, for example.</span></span> <span data-ttu-id="c457e-123">Það er alltaf hægt að athuga uppsetninguna með því að velja táknið ![Ljósapera sem opnar eiginleika viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera"), slá inn **Skýrsluval** og síðan velja viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="c457e-123">You can always check your setup by choosing the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, entering **Report Selections**, and then choose the relevant link.</span></span>

<span data-ttu-id="c457e-124">Sjálfgefna útgáfan af [!INCLUDE [prod_short](includes/prod_short.md)] inniheldur eftirfarandi síður **Skýrsluhluta**:</span><span class="sxs-lookup"><span data-stu-id="c457e-124">The default version of [!INCLUDE [prod_short](includes/prod_short.md)] includes the following **Report Section** pages:</span></span>

* <span data-ttu-id="c457e-125">**Skýrsluval - Sala**</span><span class="sxs-lookup"><span data-stu-id="c457e-125">**Report Selection - Sales**</span></span>  
* <span data-ttu-id="c457e-126">**Skýrsluval - innkaup**</span><span class="sxs-lookup"><span data-stu-id="c457e-126">**Report Selection - Purchase**</span></span>  
* <span data-ttu-id="c457e-127">**Skýrsluval - Birgðir**</span><span class="sxs-lookup"><span data-stu-id="c457e-127">**Report Selection - Inventory**</span></span>  
* <span data-ttu-id="c457e-128">**Skýrsluval - Sjóðstreymi**</span><span class="sxs-lookup"><span data-stu-id="c457e-128">**Report Selection - Cash Flow**</span></span>  
* <span data-ttu-id="c457e-129">**Skýrsluval – vöruhús**</span><span class="sxs-lookup"><span data-stu-id="c457e-129">**Report Selection - Warehouse**</span></span>  
* <span data-ttu-id="c457e-130">**Skýrsluval - Bankareikningur**</span><span class="sxs-lookup"><span data-stu-id="c457e-130">**Report Selection - Bank Account**</span></span>  
* <span data-ttu-id="c457e-131">**Innheimtubréf/vaxtareikningur skýrsluvals**</span><span class="sxs-lookup"><span data-stu-id="c457e-131">**Report Selections Reminder/Finance Charge**</span></span>  

## <a name="example-report-selection-for-sales-documents"></a><span data-ttu-id="c457e-132">Dæmi: Skýrsluval fyrir söluskjöl</span><span class="sxs-lookup"><span data-stu-id="c457e-132">Example: Report selection for sales documents</span></span>

<span data-ttu-id="c457e-133">Síðan **Skýrsluval - Sala** skilgreinir sjálfgefnar skýrslur til að nota í mismunandi aðstæðum fyrir hverja skjalagerð sem á við.</span><span class="sxs-lookup"><span data-stu-id="c457e-133">The **Report Selection - Sales** page defines the default reports to use in different scenarios for each related document type.</span></span> <span data-ttu-id="c457e-134">Veljið gerð skjals í reitnum **Notkun** og bætið síðan við eða yfirfarið skýrsluvalið.</span><span class="sxs-lookup"><span data-stu-id="c457e-134">Choose a document type in the **Usage** field, and then add or review the report selection.</span></span> <span data-ttu-id="c457e-135">Hægt er að setja upp fleiri en eina skýrslu og röðina sem á að senda eða prenta skýrslurnar eftir.</span><span class="sxs-lookup"><span data-stu-id="c457e-135">You can set up more than one report and the order of sequence that the reports must be sent or printed in.</span></span>  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="c457e-136">Sumar skjalagerðir er hægt að senda sem tölvupóstviðhengi en aðrar ekki.</span><span class="sxs-lookup"><span data-stu-id="c457e-136">Some types of document can be sent as email attachments, and others cannot.</span></span> <span data-ttu-id="c457e-137">Hver síða **Skýrsluvals** sýnir viðbótarreiti ef gerðin styður tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="c457e-137">Each **Report Selection** page shows additional fields if the type support email out of the box.</span></span>  

<span data-ttu-id="c457e-138">Til dæmis á síðunum **Skýrsluval - Sala** og **Skýrsluval - innkaup** hjálpa eftirfarandi reitir þér við að setja upp tölvupóst:</span><span class="sxs-lookup"><span data-stu-id="c457e-138">For example, in the **Report Selection - Sales** and **Report Selection - Purchase** pages, the following fields help you set up emailing:</span></span>

|<span data-ttu-id="c457e-139">Heiti reits</span><span class="sxs-lookup"><span data-stu-id="c457e-139">Field name</span></span> |<span data-ttu-id="c457e-140">Description</span><span class="sxs-lookup"><span data-stu-id="c457e-140">Description</span></span>  |
|-----------|-------------|
|<span data-ttu-id="c457e-141">**Nota fyrir meginmál tölvupósts**</span><span class="sxs-lookup"><span data-stu-id="c457e-141">**Use for Email Body**</span></span>| <span data-ttu-id="c457e-142">Tilgreinir samanteknar upplýsingar, eins og númer reiknings, gjalddaga og tengil greiðsluþjónustu, sem verða settar inn í meginmál tölvupóstsins sem á að senda.</span><span class="sxs-lookup"><span data-stu-id="c457e-142">Specifies that summarized information, such as invoice number, due date, and payment service link, will be inserted in the body of the email that you send.</span></span>        |
|<span data-ttu-id="c457e-143">**Nota fyrir tölvupóstsviðhengi**</span><span class="sxs-lookup"><span data-stu-id="c457e-143">**Use for Email Attachment**</span></span>| <span data-ttu-id="c457e-144">Tilgreinir að tengt fylgiskjal verði hengt við tölvupóstinn.</span><span class="sxs-lookup"><span data-stu-id="c457e-144">Specifies that the related document will be attached to the email.</span></span>|
|<span data-ttu-id="c457e-145">**Lýsing á útliti meginmáls tölvupósts**</span><span class="sxs-lookup"><span data-stu-id="c457e-145">**Email Body Layout Description**</span></span>|<span data-ttu-id="c457e-146">Tilgreinir útlit á meginmáli tölvupósts sem er notað, yfirleitt sérsniðið skýrsluútlit.</span><span class="sxs-lookup"><span data-stu-id="c457e-146">Specifies the email body layout that is used, typically a custom report layout.</span></span> |

## <a name="see-also"></a><span data-ttu-id="c457e-147">Sjá einnig .</span><span class="sxs-lookup"><span data-stu-id="c457e-147">See also</span></span>

[<span data-ttu-id="c457e-148">Setja upp endurnýtanlega texta og útlit tölvupósts fyrir sölu- og innkaupaskjöl</span><span class="sxs-lookup"><span data-stu-id="c457e-148">Set Up Reusable Email Texts and Layouts for Sales and Purchase Documents</span></span>](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[<span data-ttu-id="c457e-149">Velja útlit ávísunar</span><span class="sxs-lookup"><span data-stu-id="c457e-149">Select a Check Layout</span></span>](finance-how-define-check-layouts.md)  
[<span data-ttu-id="c457e-150">Setja upp skýrslur fyrir VSK og Intrastat (Þýskaland)</span><span class="sxs-lookup"><span data-stu-id="c457e-150">Set Up Reports for VAT and Intrastat (Germany)</span></span>](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[<span data-ttu-id="c457e-151">Stjórna útliti skýrslna og skjala</span><span class="sxs-lookup"><span data-stu-id="c457e-151">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
[<span data-ttu-id="c457e-152">Skilgreina útlit skjala fyrir viðskiptamenn og lánardrottna</span><span class="sxs-lookup"><span data-stu-id="c457e-152">Define Document Layouts for Customers and Vendors</span></span>](ui-define-customer-vendor-document-layouts.md)  
[<span data-ttu-id="c457e-153">Setja upp prentara</span><span class="sxs-lookup"><span data-stu-id="c457e-153">Set Up Printers</span></span>](ui-specify-printer-selection-reports.md)  
