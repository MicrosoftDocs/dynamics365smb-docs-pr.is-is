---
title: Notkun AMC Banking 365 Fundamentals viðbótarinnar | Microsoft skjöl
description: Skiptast á gögnum við bankann á greiðlegan hátt með því að umbreyta gögnum í það snið sem krafist er.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: bank, format, data
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 493abf6f7309d6eb0274f4f416e6e5aea782b031
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194356"
---
# <a name="using-the-amc-banking-365-fundamentals-extension"></a><span data-ttu-id="2735c-103">Notkun AMC Banking 365 Fundamentals viðbótarinnar</span><span class="sxs-lookup"><span data-stu-id="2735c-103">Using the AMC Banking 365 Fundamentals Extension</span></span>
<span data-ttu-id="2735c-104">AMC Banking 365 Fundamentals viðbótin gerir það auðveldar sendingu gagna til bankans þíns og eykur áreiðanlega þeirra.</span><span class="sxs-lookup"><span data-stu-id="2735c-104">The AMC Banking 365 Fundamentals extension makes it easier, and more accurate, to send data to your banks.</span></span> <span data-ttu-id="2735c-105">Viðbótin tengir [!INCLUDE[d365fin](includes/d365fin_md.md)] við AMC Banking 365 Fundamentals fyrir Microsoft Dynamics 365 Business Central þjónustu sem getur breytt bankagögnum úr [!INCLUDE[d365fin](includes/d365fin_md.md)] í snið sem yfir 600 bankar í heiminum krefjast.</span><span class="sxs-lookup"><span data-stu-id="2735c-105">The extension connects [!INCLUDE[d365fin](includes/d365fin_md.md)] with the AMC Banking 365 Fundamentals for Microsoft Dynamics 365 Business Central service, which can convert bank data from [!INCLUDE[d365fin](includes/d365fin_md.md)] into formats that are required by over 600 banks around the world.</span></span> <span data-ttu-id="2735c-106">Þannig er til dæmis auðveldara að millifæra greiðslur og kreditfærslur til lánardrottna með því að slá greiðslurnar inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] og hlaða þeim svo upp í bankann þinn.</span><span class="sxs-lookup"><span data-stu-id="2735c-106">For example, this makes it easier to transfer payments and credits to vendors by entering the payments in [!INCLUDE[d365fin](includes/d365fin_md.md)], and then uploading them to your bank.</span></span> <span data-ttu-id="2735c-107">Sniðin geta einnig jafnað út bankaafstemmingarferli.</span><span class="sxs-lookup"><span data-stu-id="2735c-107">The formats can also smooth out bank reconciliation processes.</span></span> <span data-ttu-id="2735c-108">Frekari upplýsingar er að finna í [AMC Banking fyrir Microsoft Dynamics 365 Business Central](https://amcbanking.com/landing365bc/help).</span><span class="sxs-lookup"><span data-stu-id="2735c-108">For more information, see [AMC Banking for Microsoft Dynamics 365 Business Central](https://amcbanking.com/landing365bc/help).</span></span>

> [!Note]
> <span data-ttu-id="2735c-109">AMC Banking hefur byggt aukalegar viðbætur sem virka með [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2735c-109">AMC Banking has built additional extensions that work with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="2735c-110">Þetta efnisatriði lýsir aðeins Fundamental-viðbótinni.</span><span class="sxs-lookup"><span data-stu-id="2735c-110">This topic describes only the Fundamental extension.</span></span>

## <a name="using-our-demonstration-account"></a><span data-ttu-id="2735c-111">Notkun á sýnireikningi okkar</span><span class="sxs-lookup"><span data-stu-id="2735c-111">Using Our Demonstration Account</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="2735c-112">fylgir með sýnireikningi sem gerir þér kleift að prófa AMC Banking 365 Fundamentals-viðbótina.</span><span class="sxs-lookup"><span data-stu-id="2735c-112">comes with a demonstration account that lets you try out the AMC Banking 365 Fundamentals extension.</span></span> <span data-ttu-id="2735c-113">Við bjóðum upp á sjálfgefnar stillingar fyrir tengingu við AMC Banking, þar sem bankareikningar eru tilgreindir til að sækja gögn frá [!INCLUDE[d365fin](includes/d365fin_md.md)], auk nokkurra gagnaskiptaskilgreininga.</span><span class="sxs-lookup"><span data-stu-id="2735c-113">We provide default settings for connecting to AMC Banking, specifying the bank accounts to get data from in [!INCLUDE[d365fin](includes/d365fin_md.md)], plus a few data exchange definitions.</span></span> <span data-ttu-id="2735c-114">Þú getur skoðað tengingarstillingarnar á síðunni **AMC Banking Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="2735c-114">You can view the connection settings on the **AMC Banking Setup** page.</span></span> <span data-ttu-id="2735c-115">Fyrir bankareikninga bætir viðbótin gildum í reitina **Heiti banka**, **Nr. á skilaboðum kreditfærslu**, **Innflutningssnið bankayfirlits** og **Greiðsluútflutningssnið** á bankareikningspjöldum.</span><span class="sxs-lookup"><span data-stu-id="2735c-115">For bank accounts, the extension applies values in the **Bank Name**, **Credit Transfer Msg. Nos.**, **Bank Statement Import Format**, and **Payment Export Format** fields on bank account cards.</span></span>

<span data-ttu-id="2735c-116">Við veitum stillingarnar en til að prófa viðbótina verður þú að keyra leiðbeiningar um uppsetningu með hjálp til að nota þær.</span><span class="sxs-lookup"><span data-stu-id="2735c-116">We provide the settings, but to try out the extension you must run the assisted setup guide to apply them.</span></span> <span data-ttu-id="2735c-117">Til að keyra leiðarvísinn, á síðunni **AMC Banking Uppsetning**, skaltu velja aðgerðina **Uppsetning með hjálp**.</span><span class="sxs-lookup"><span data-stu-id="2735c-117">To run the guide, on the **AMC Banking Setup** page, choose the **Assisted Setup** action.</span></span>

> [!Note]
> <span data-ttu-id="2735c-118">Einhverjar takmarkanir eru á sýnireikningnum.</span><span class="sxs-lookup"><span data-stu-id="2735c-118">There are some limitations on the demo account.</span></span> <span data-ttu-id="2735c-119">Til dæmis þegar greiðslum er umbreytt mun upphæðin í umbreyttu skránni ekki passa við raunverulegu upphæðina.</span><span class="sxs-lookup"><span data-stu-id="2735c-119">For example, when you convert payments, the amount in the converted file will not match the actual amount.</span></span> <span data-ttu-id="2735c-120">Í staðin verður upphæðin alltaf fimm einingar af gjaldmiðlinum sem þú notar fyrir greiðslur.</span><span class="sxs-lookup"><span data-stu-id="2735c-120">Instead, the amount will always be five units of the currency that you use for payments.</span></span>  

## <a name="setting-up-the-extension"></a><span data-ttu-id="2735c-121">Uppsetning viðbótarinnar</span><span class="sxs-lookup"><span data-stu-id="2735c-121">Setting Up the Extension</span></span>
<span data-ttu-id="2735c-122">Að hefjast handa felur aðeins í sér nokkur einföld skref og leiðbeiningar um uppsetningu með hjálp munu koma á tengingunni og kveikja á viðbótinni.</span><span class="sxs-lookup"><span data-stu-id="2735c-122">Getting started with the extension involves just a few easy steps, and an assisted setup guide will make the connection and turn on the extension.</span></span> <span data-ttu-id="2735c-123">Leiðbeiningin mun gera hluti eins og að setja upp gagnaskiptaskilgreiningar fyrir uppsetningar á útflutningi/innflutningi bankayfirlits og byrja á númeraröðum sem eru notaðar fyrir skilaboð kreditfærslna.</span><span class="sxs-lookup"><span data-stu-id="2735c-123">The guide will do things like install the data exchange definitions for bank statement export/import setups and initiate the number series used for credit transfer messages.</span></span>  

### <a name="to-set-up-the-required-permission-sets"></a><span data-ttu-id="2735c-124">Til að setja upp áskildar heimildasamstæður</span><span class="sxs-lookup"><span data-stu-id="2735c-124">To set up the required permission sets</span></span>
<span data-ttu-id="2735c-125">Áður en hægt er að nota þessa viðbót verður stjórnandi að afrita eftirfarandi heimildasamstæður, breyta þeim og síðan úthluta nýjum heimildasamstæðum til notenda í staðinn fyrir þær upprunalegu:</span><span class="sxs-lookup"><span data-stu-id="2735c-125">Before people can use this extension, your administrator must copy the following permission sets, edit them, and then assign the new permission sets to users instead of original:</span></span>

* <span data-ttu-id="2735c-126">**D365 Grunnútgáfa**</span><span class="sxs-lookup"><span data-stu-id="2735c-126">**D365 Basic**</span></span>
* <span data-ttu-id="2735c-127">**D365-teymismeðlimur**</span><span class="sxs-lookup"><span data-stu-id="2735c-127">**D365 Team Member**</span></span>
* <span data-ttu-id="2735c-128">**D365-upplýsingar**</span><span class="sxs-lookup"><span data-stu-id="2735c-128">**D365 Read**</span></span>
* <span data-ttu-id="2735c-129">**IntelligentCloudBC**</span><span class="sxs-lookup"><span data-stu-id="2735c-129">**IntelligentCloudBC**</span></span>

<span data-ttu-id="2735c-130">Nánari upplýsingar er að finna í [Til að afrita heimildasamstæðu](ui-define-granular-permissions.md#to-copy-a-permission-set).</span><span class="sxs-lookup"><span data-stu-id="2735c-130">For more information, see [To copy a permission set](ui-define-granular-permissions.md#to-copy-a-permission-set).</span></span>

<span data-ttu-id="2735c-131">Fyrir hverja nýja heimildasamstæðu skal aðeins veita heimildina **Lesa** fyrir **AMC Banking Uppsetningartafla (20101)**.</span><span class="sxs-lookup"><span data-stu-id="2735c-131">For each new permission set, grant only the **Read** permission for the **AMC Banking Setup table (20101)**.</span></span> <span data-ttu-id="2735c-132">Nánari upplýsingar er að finna í [Að búa til eða breyta heimildum handvirkt](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).</span><span class="sxs-lookup"><span data-stu-id="2735c-132">For more information, see [To create or modify permissions manually](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).</span></span>

### <a name="to-connect-the-extension-to-amc-banking"></a><span data-ttu-id="2735c-133">Til að tengja viðbótina við AMC Banking</span><span class="sxs-lookup"><span data-stu-id="2735c-133">To connect the extension to AMC Banking</span></span>
1. <span data-ttu-id="2735c-134">Fá einingu og þjónustuáætlun fyrir AMC Banking.</span><span class="sxs-lookup"><span data-stu-id="2735c-134">Get a module and a service plan for AMC Banking.</span></span> <span data-ttu-id="2735c-135">Til að gera það skaltu fara á [AMC leyfissíðuna](https://license.amcbanking.com/register).</span><span class="sxs-lookup"><span data-stu-id="2735c-135">To do that, visit the [AMC License](https://license.amcbanking.com/register) page.</span></span>
2. <span data-ttu-id="2735c-136">Í [!INCLUDE[d365fin](includes/d365fin_md.md)], veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **AMC Banking uppsetning**, og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2735c-136">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **AMC Banking Setup**, and then choose the related link.</span></span>  
3. <span data-ttu-id="2735c-137">Á síðunni **AMC Banking Uppsetning**, skaltu velja aðgerðina **Uppsetning með hjálp**.</span><span class="sxs-lookup"><span data-stu-id="2735c-137">On the **AMC Banking Setup** page, choose the **Assisted Setup** action.</span></span>
4. <span data-ttu-id="2735c-138">Ljúka skal skrefunum í leiðbeiningum um uppsetningu með hjálp.</span><span class="sxs-lookup"><span data-stu-id="2735c-138">Complete the steps in the assisted setup guide.</span></span>

### <a name="to-connect-bank-accounts-to-the-extension"></a><span data-ttu-id="2735c-139">Til að tengja bankareikninga við viðbótina</span><span class="sxs-lookup"><span data-stu-id="2735c-139">To connect bank accounts to the extension</span></span>
1. <span data-ttu-id="2735c-140">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bankareikningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2735c-140">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="2735c-141">Opnaðu spjaldið fyrir bankareikninginn sem þú vilt tengja við þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="2735c-141">Open the card for the bank account that you want to connect to the service.</span></span>
3. <span data-ttu-id="2735c-142">Í reitnum **Heiti banka** skaltu velja sniðið sem bankinn krefst.</span><span class="sxs-lookup"><span data-stu-id="2735c-142">In the **Bank Name** field, choose the format that your bank requires.</span></span>  

   <span data-ttu-id="2735c-143">Sniðin eru síuð til að sýna aðeins þau sem skipta máli fyrir landið/svæðið sem er tilgreint fyrir bankareikninginn.</span><span class="sxs-lookup"><span data-stu-id="2735c-143">The formats are filtered to show only those that are relevant for the country/region that is specified for the bank account.</span></span>
4. <span data-ttu-id="2735c-144">Í reitnum **Númer fyrir skilaboð kreditfærslu** skaltu velja númeraröðina sem nota á fyrir skilaboð sem fylgja greiðslum.</span><span class="sxs-lookup"><span data-stu-id="2735c-144">In the **Credit Transfer Msg. Nos.** field, choose the number series to use for messages that accompany payments.</span></span>
5. <span data-ttu-id="2735c-145">Í reitunum **Innflutningssnið bankayfirlits** og **Greiðsluútflutningssnið** skal velja þær gagnaskiptaskilgreiningar sem bankinn krefst.</span><span class="sxs-lookup"><span data-stu-id="2735c-145">In the **Bank Statement Import Format** and **Payment Export Format** fields, choose the data exchange definitions that your bank requires.</span></span>

## <a name="using-the-extension"></a><span data-ttu-id="2735c-146">Notkun viðbótarinnar</span><span class="sxs-lookup"><span data-stu-id="2735c-146">Using the Extension</span></span>
<span data-ttu-id="2735c-147">Ef þú notar þessa viðbót þarf aðeins að flytja út gögn á síðunni **Greiðslubækur** og síðan hlaða þeim upp á vefþjónustu bankans.</span><span class="sxs-lookup"><span data-stu-id="2735c-147">Using this extension is just a matter of exporting data on the **Payment Journals** page, and then uploading it to your bank's web service.</span></span> <span data-ttu-id="2735c-148">Nánari upplýsingar er að finna í [Greiða með umreikningsþjónustu bankagagna eða SEPA kreditfærslu](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).</span><span class="sxs-lookup"><span data-stu-id="2735c-148">For more information, see [Making Payments with Bank Data Conversion or SEPA Credit Transfer](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).</span></span>

> [!Note]
> <span data-ttu-id="2735c-149">Þú verður að fylla út reitina **SWIFT kóði** og **IBAN** fyrir hvern bankareikning.</span><span class="sxs-lookup"><span data-stu-id="2735c-149">You must fill in the **SWIFT Code** and **IBAN** fields for each bank account.</span></span>

### <a name="to-export-data-and-submit-it-to-your-bank"></a><span data-ttu-id="2735c-150">Til að flytja út gögn og senda þau í bankann þinn</span><span class="sxs-lookup"><span data-stu-id="2735c-150">To export data and submit it to your bank</span></span>
> [!CAUTION]  
>  <span data-ttu-id="2735c-151">Þegar þú flytur út gögn með AMC Banking 365 Fundamentals viðbótinni, mun sá sem veitir þjónustuna geta séð eitthvað af gögnunum.</span><span class="sxs-lookup"><span data-stu-id="2735c-151">When you export data by using the AMC Banking 365 Fundamentals extension, some of your business data will be exposed to the provider of the service.</span></span> <span data-ttu-id="2735c-152">Þjónustuveita, AMC Consult A/S, er ábyrg fyrir persónuvernd gagnanna.</span><span class="sxs-lookup"><span data-stu-id="2735c-152">The service provider, AMC Consult A/S, is responsible for the privacy of this data.</span></span> <span data-ttu-id="2735c-153">Nánari upplýsingar er að finna í [AMC-persónuverndarstefnu](https://go.microsoft.com/fwlink/?LinkId=510158).</span><span class="sxs-lookup"><span data-stu-id="2735c-153">For more information, see [AMC Privacy Policy](https://go.microsoft.com/fwlink/?LinkId=510158).</span></span>

1. <span data-ttu-id="2735c-154">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiðslubækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2735c-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="2735c-155">Stofna skal færslubókarlínurnar sem á að flytja út.</span><span class="sxs-lookup"><span data-stu-id="2735c-155">Create the journal lines that you want to export.</span></span>  

   > [!Note]
   > <span data-ttu-id="2735c-156">Fyrir hverja línu skaltu muna að velja **Rafræn greiðsla** í reitnum **Tegund bankagreiðslu**.</span><span class="sxs-lookup"><span data-stu-id="2735c-156">For each line, remember to choose **Electronic Payment** in the **Bank Payment Type** field.</span></span>
3. <span data-ttu-id="2735c-157">Veldu **Export** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="2735c-157">Choose the **Export** action.</span></span>

### <a name="to-import-and-apply-the-converted-file"></a><span data-ttu-id="2735c-158">Til að flytja inn og nota umbreyttu skrána</span><span class="sxs-lookup"><span data-stu-id="2735c-158">To import and apply the converted file</span></span>
1. <span data-ttu-id="2735c-159">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiðsluafstemmingarbók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2735c-159">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Reconciliation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="2735c-160">Veldu aðgerðina **Flytja inn bankafærslur** og svo umbreyttu skrána.</span><span class="sxs-lookup"><span data-stu-id="2735c-160">Choose the **Import Bank Transaction** action, and then choose the converted file.</span></span>  

   [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="2735c-161">stofnar nýja greiðsluafstemmingarbók sem inniheldur gögnin í skránni.</span><span class="sxs-lookup"><span data-stu-id="2735c-161">will create a new payment reconciliation journal that contains the data in the file.</span></span> <span data-ttu-id="2735c-162">Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="2735c-162">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="2735c-163">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2735c-163">See Also</span></span>
<span data-ttu-id="2735c-164">[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="2735c-164">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="2735c-165">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="2735c-165">Getting Started</span></span>](product-get-started.md)