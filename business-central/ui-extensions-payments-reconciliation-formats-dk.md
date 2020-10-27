---
title: Notkun greiðslna og afstemmingar (DK) viðbótarinnar | Microsoft Docs
description: Þessi viðbót gerir það auðvelt að flytja út skrár sem eru forstilltar til að uppfylla kröfur banka um rafræna skráningu.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 1afd60dc4c9c86b476c3c2c80974ce805b19a4ca
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912322"
---
# <a name="the-payments-and-reconciliations-dk-extension"></a><span data-ttu-id="91a9e-103">Greiðslur og afstemmingar (DK) viðbótin</span><span class="sxs-lookup"><span data-stu-id="91a9e-103">The Payments and Reconciliations (DK) Extension</span></span>

<span data-ttu-id="91a9e-104">Greiddu hratt og án mistaka með því að flytja út skrár sem eru sérstaklega sniðnar fyrir millifærslur með lánardrottni eða banka.</span><span class="sxs-lookup"><span data-stu-id="91a9e-104">Make fast, error-free payments by exporting files that are formatted specifically for exchanges with your vendor or bank.</span></span> <span data-ttu-id="91a9e-105">Þessar skrár flýta fyrir greiðslu- og afstemmingum og útrýma villum sem geta komið upp þegar upplýsingar eru slegnar inn á bankasíðu.</span><span class="sxs-lookup"><span data-stu-id="91a9e-105">These files speed up the payment and reconciliation processes, and eliminate errors that can happen when you manually enter the information on a bank website.</span></span>  

<span data-ttu-id="91a9e-106">Þessi viðbót styður skráarsnið fyrir nokkra danska banka.</span><span class="sxs-lookup"><span data-stu-id="91a9e-106">This extension supports file formats for several Danish banks.</span></span> <span data-ttu-id="91a9e-107">Þegar þú flytur út greiðsluupplýsingar í skrá pakkar viðbótin gögnunum inn í sniðið sem bankinn fer fram á.</span><span class="sxs-lookup"><span data-stu-id="91a9e-107">When you export payment information to a file, the extension packages the data into the format that your bank requires.</span></span> <span data-ttu-id="91a9e-108">Dæmi um þetta eru sniðin Bankdata-V3, BEC, SDC og FIK, sem margir mismunandi bankar nota, og sum sem eru sérhæfðari fyrir tiltekna banka á borð við Danske Bank og Nordea.</span><span class="sxs-lookup"><span data-stu-id="91a9e-108">For example, the formats include Bankdata-V3, BEC, SDC, and FIK, which many different banks use, and some that are more specialized for certain banks, for example, Danske Bank and Nordea.</span></span> <span data-ttu-id="91a9e-109">Viðbótin inniheldur einnig nokkur snið til að flytja inn og afstemma bankareikninga.</span><span class="sxs-lookup"><span data-stu-id="91a9e-109">The extension also includes some formats for importing and reconciling bank statements.</span></span>  

> [!Note]
> <span data-ttu-id="91a9e-110">Til að nota viðbótina er nauðsynlegt að vita hvaða snið bankinn eða lánardrottinn krefst.</span><span class="sxs-lookup"><span data-stu-id="91a9e-110">To use the extension, you must know the format that your bank or vendor requires.</span></span> <span data-ttu-id="91a9e-111">Sumir bankar eða lánardrottnar veita þessar upplýsingar á vefsvæðum sínum: Hins vegar gætirðu þurft að hafa samband við þjónustudeild þeirra til að fá upplýsingarnar.</span><span class="sxs-lookup"><span data-stu-id="91a9e-111">Some banks or vendors provide this information on their websites; however, you might need to contact their customer service to get the information.</span></span>  

## <a name="supported-bank-formats"></a><span data-ttu-id="91a9e-112">Studd bankasnið</span><span class="sxs-lookup"><span data-stu-id="91a9e-112">Supported Bank Formats</span></span>
<span data-ttu-id="91a9e-113">Þessi viðbót getur notað eftirfarandi skráarsnið fyrir greiðsluskrár:</span><span class="sxs-lookup"><span data-stu-id="91a9e-113">This extension can apply the following file formats for payment files:</span></span>  

* <span data-ttu-id="91a9e-114">BANKDATA-V3</span><span class="sxs-lookup"><span data-stu-id="91a9e-114">BANKDATA-V3</span></span>  
* <span data-ttu-id="91a9e-115">BEC-INDLAND</span><span class="sxs-lookup"><span data-stu-id="91a9e-115">BEC-INDLAND</span></span>  
* <span data-ttu-id="91a9e-116">BEC-CSV</span><span class="sxs-lookup"><span data-stu-id="91a9e-116">BEC-CSV</span></span>  
* <span data-ttu-id="91a9e-117">DANSKEBANK-CMKV</span><span class="sxs-lookup"><span data-stu-id="91a9e-117">DANSKEBANK-CMKV</span></span>  
* <span data-ttu-id="91a9e-118">DANSKEBANK-CMKXKSX</span><span class="sxs-lookup"><span data-stu-id="91a9e-118">DANSKEBANK-CMKXKSX</span></span>  
* <span data-ttu-id="91a9e-119">DANSKEBANK</span><span class="sxs-lookup"><span data-stu-id="91a9e-119">DANSKEBANK</span></span>  
* <span data-ttu-id="91a9e-120">FIK71</span><span class="sxs-lookup"><span data-stu-id="91a9e-120">FIK71</span></span>  
* <span data-ttu-id="91a9e-121">NORDEA-ERHVERV-CSV</span><span class="sxs-lookup"><span data-stu-id="91a9e-121">NORDEA-ERHVERV-CSV</span></span>  
* <span data-ttu-id="91a9e-122">NORDEA</span><span class="sxs-lookup"><span data-stu-id="91a9e-122">NORDEA</span></span>  
* <span data-ttu-id="91a9e-123">NORDEA-UNITEL-V3</span><span class="sxs-lookup"><span data-stu-id="91a9e-123">NORDEA-UNITEL-V3</span></span>  
* <span data-ttu-id="91a9e-124">SDC</span><span class="sxs-lookup"><span data-stu-id="91a9e-124">SDC</span></span>  
* <span data-ttu-id="91a9e-125">SDC-CSV</span><span class="sxs-lookup"><span data-stu-id="91a9e-125">SDC-CSV</span></span>  

## <a name="to-set-up-the-extension"></a><span data-ttu-id="91a9e-126">Til að setja upp viðbótina</span><span class="sxs-lookup"><span data-stu-id="91a9e-126">To set up the extension</span></span>

<span data-ttu-id="91a9e-127">Nokkur skref eru nauðsynleg í upphafi.</span><span class="sxs-lookup"><span data-stu-id="91a9e-127">There are a few steps to get started.</span></span>  

* <span data-ttu-id="91a9e-128">Leyfa útflutning greiðslugagna.</span><span class="sxs-lookup"><span data-stu-id="91a9e-128">Allow payment data exports.</span></span> <span data-ttu-id="91a9e-129">Til að vernda gögnin þín er þetta ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="91a9e-129">To help protect your data, this is not readily available.</span></span>  
* <span data-ttu-id="91a9e-130">Setja upp innkaup og viðskiptaskuldir þannig að þú þurfir ekki utanaðkomandi skjalanúmer á reikningum.</span><span class="sxs-lookup"><span data-stu-id="91a9e-130">Set up purchase and payables so that you do not require external document numbers on invoices.</span></span> <span data-ttu-id="91a9e-131">Ef þess er þörf geturðu notað tilvísunarnúmerið til að vísa til tiltekins reiknings.</span><span class="sxs-lookup"><span data-stu-id="91a9e-131">If needed, you can use the reference number to refer to a specific invoice.</span></span>  
* <span data-ttu-id="91a9e-132">Tilgreina greiðslumáta fyrir hvern lánardrottininn.</span><span class="sxs-lookup"><span data-stu-id="91a9e-132">Specify the payment method for each vendor.</span></span> <span data-ttu-id="91a9e-133">Greiðslumátar skilgreina hvernig þú borgar reikninga frá lánardrottninum.</span><span class="sxs-lookup"><span data-stu-id="91a9e-133">Payment methods define how you pay invoices from the vendor.</span></span> <span data-ttu-id="91a9e-134">Til dæmis Banki, Staðgreiðsla, Ávísun eða Reikningur.</span><span class="sxs-lookup"><span data-stu-id="91a9e-134">For example, Bank, Cash, Check, or Account.</span></span>  
* <span data-ttu-id="91a9e-135">Tilgreina gerð sniðsins sem á að nota fyrir hvern bankareikning.</span><span class="sxs-lookup"><span data-stu-id="91a9e-135">Specify the type of format to use for each of your bank accounts.</span></span> <span data-ttu-id="91a9e-136">Til dæmis NORDEA, DANSKEBANK, SDC og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="91a9e-136">For example, NORDEA, DANSKEBANK, SDC, and so on.</span></span>  

<span data-ttu-id="91a9e-137">Að auki þarftu að úthluta lánardrottnum á staðbundinn **Alm. viðsk.bókunarflokkur** og **Bókunarflokk lánardrottins** .</span><span class="sxs-lookup"><span data-stu-id="91a9e-137">Additionally, you must assign vendors to a domestic **Gen. Bus. Posting Group** and a **Vendor Posting Group** .</span></span> <span data-ttu-id="91a9e-138">Stilling fyrir land/svæði fyrir lánardrottinn verður að vera Danmörk (DK).</span><span class="sxs-lookup"><span data-stu-id="91a9e-138">The Country/Region setting for the vendor must be Denmark (DK).</span></span> <span data-ttu-id="91a9e-139">Nánari upplýsingar er að finna í [Uppsetning Bókunarflokka](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="91a9e-139">For more information, see [Setting Up Posting Groups](finance-posting-groups.md).</span></span>  

### <a name="to-allow-d365fin-to-export-payment-data"></a><span data-ttu-id="91a9e-140">Til að leyfa [!INCLUDE[d365fin](includes/d365fin_md.md)] að flytja út greiðslugögn</span><span class="sxs-lookup"><span data-stu-id="91a9e-140">To allow [!INCLUDE[d365fin](includes/d365fin_md.md)] to export payment data</span></span>

1. <span data-ttu-id="91a9e-141">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiðslubók** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="91a9e-141">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journal** , and then choose the related link.</span></span>  
2. <span data-ttu-id="91a9e-142">Á síðunni **Breyta greiðslubók** er valið **Banki** .</span><span class="sxs-lookup"><span data-stu-id="91a9e-142">On the **Edit Payment Journal** page, choose the **Bank** batch.</span></span>  
3. <span data-ttu-id="91a9e-143">Veljið gátreitinn **Leyfa greiðsluútflutning** .</span><span class="sxs-lookup"><span data-stu-id="91a9e-143">Choose the **Allow Payment Export** check box.</span></span>  

### <a name="to-specify-a-payment-method-for-a-vendor"></a><span data-ttu-id="91a9e-144">Til að tilgreina greiðslumáta lánardrottins</span><span class="sxs-lookup"><span data-stu-id="91a9e-144">To specify a payment method for a vendor</span></span>

<span data-ttu-id="91a9e-145">Eftirfarandi tafla sýnir sambland FIK og GIRO greiðslumáta sem [!INCLUDE[d365fin](includes/d365fin_md.md)] styður.</span><span class="sxs-lookup"><span data-stu-id="91a9e-145">The following table shows the combinations of FIK and GIRO payment methods that [!INCLUDE[d365fin](includes/d365fin_md.md)] supports.</span></span>

|<span data-ttu-id="91a9e-146">Samsetning</span><span class="sxs-lookup"><span data-stu-id="91a9e-146">Combination</span></span>|<span data-ttu-id="91a9e-147">Gerð 01</span><span class="sxs-lookup"><span data-stu-id="91a9e-147">Type 01</span></span> | <span data-ttu-id="91a9e-148">Gerð 04</span><span class="sxs-lookup"><span data-stu-id="91a9e-148">Type 04</span></span> | <span data-ttu-id="91a9e-149">Gerð 71</span><span class="sxs-lookup"><span data-stu-id="91a9e-149">Type 71</span></span> | <span data-ttu-id="91a9e-150">Gerð 73</span><span class="sxs-lookup"><span data-stu-id="91a9e-150">Type 73</span></span> |
|----|--------|---------|---------|---------|
|<span data-ttu-id="91a9e-151">Númer gíróreiknings eða FIK-lánardrottins?</span><span class="sxs-lookup"><span data-stu-id="91a9e-151">Giro Account No. or FIK Creditor No.?</span></span> | <span data-ttu-id="91a9e-152">Númer gíróreiknings</span><span class="sxs-lookup"><span data-stu-id="91a9e-152">Giro Account No.</span></span> | <span data-ttu-id="91a9e-153">Númer gíróreiknings</span><span class="sxs-lookup"><span data-stu-id="91a9e-153">Giro Account No.</span></span> | <span data-ttu-id="91a9e-154">Númer FIK-lánardrottins</span><span class="sxs-lookup"><span data-stu-id="91a9e-154">FIK Creditor No.</span></span> | <span data-ttu-id="91a9e-155">Númer FIK-lánardrottins</span><span class="sxs-lookup"><span data-stu-id="91a9e-155">FIK Creditor No.</span></span>|
|<span data-ttu-id="91a9e-156">Leyfja skilaboð til viðtakanda?</span><span class="sxs-lookup"><span data-stu-id="91a9e-156">Allows Message to Recipient?</span></span> | <span data-ttu-id="91a9e-157">Já</span><span class="sxs-lookup"><span data-stu-id="91a9e-157">Yes</span></span> |<span data-ttu-id="91a9e-158">Nei</span><span class="sxs-lookup"><span data-stu-id="91a9e-158">No</span></span> |<span data-ttu-id="91a9e-159">Nei</span><span class="sxs-lookup"><span data-stu-id="91a9e-159">No</span></span> | <span data-ttu-id="91a9e-160">Já</span><span class="sxs-lookup"><span data-stu-id="91a9e-160">Yes</span></span> |
|<span data-ttu-id="91a9e-161">Inniheldur greiðslutilvísunarnúmer?</span><span class="sxs-lookup"><span data-stu-id="91a9e-161">Contains Payment Reference number?</span></span> | <span data-ttu-id="91a9e-162">Nr</span><span class="sxs-lookup"><span data-stu-id="91a9e-162">No</span></span> | <span data-ttu-id="91a9e-163">Já, 16 stafir.</span><span class="sxs-lookup"><span data-stu-id="91a9e-163">Yes, 16 digits.</span></span> | <span data-ttu-id="91a9e-164">Já, 15 stafir.</span><span class="sxs-lookup"><span data-stu-id="91a9e-164">Yes, 15 digits.</span></span> | <span data-ttu-id="91a9e-165">Nr</span><span class="sxs-lookup"><span data-stu-id="91a9e-165">No</span></span>|

1. <span data-ttu-id="91a9e-166">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Lánardrottnar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="91a9e-166">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors** , and then choose the related link.</span></span>  
2. <span data-ttu-id="91a9e-167">Opnaðu kortið, víkkaðu **Greiðslur** flipann, í **Greiðslumáti** veldu greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="91a9e-167">Open the card, expand the **Payments** tab, in the **Payment Method** field choose the payment method.</span></span>  
3. <span data-ttu-id="91a9e-168">Nauðsynlegt er að ljúka öðrum reitum, allt eftir valinu.</span><span class="sxs-lookup"><span data-stu-id="91a9e-168">Depending on your selection, you must complete other fields.</span></span> <span data-ttu-id="91a9e-169">Lýsing samsetninga er að finna í töflunni hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="91a9e-169">See the table above for a description of the combinations.</span></span>  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a><span data-ttu-id="91a9e-170">Til að tilgreina sniðið sem á að nota fyrir bankareikning</span><span class="sxs-lookup"><span data-stu-id="91a9e-170">To specify the format to use for a bank account</span></span>

1. <span data-ttu-id="91a9e-171">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bankareikningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="91a9e-171">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts** , and then choose the related link.</span></span>  
2. <span data-ttu-id="91a9e-172">Opna spjaldið fyrir bankareikninginn.</span><span class="sxs-lookup"><span data-stu-id="91a9e-172">Open the card for the bank account.</span></span>  
3. <span data-ttu-id="91a9e-173">Á **Útflutningssnið greiðslu** skal velja sniðið fyrir útflutningsskrána.</span><span class="sxs-lookup"><span data-stu-id="91a9e-173">In the **Payment Export Format** field, choose the format for your export file.</span></span>  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a><span data-ttu-id="91a9e-174">Velja FIK eða Gírógreiðsluupplýsingar fyrir reikninga lánardrottins</span><span class="sxs-lookup"><span data-stu-id="91a9e-174">Choosing the FIK or Giro payment information for vendor invoices</span></span>

1. <span data-ttu-id="91a9e-175">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Innkaupareikningar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="91a9e-175">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices** , and then choose the related link.</span></span>
2. <span data-ttu-id="91a9e-176">Veljið lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="91a9e-176">Choose the vendor.</span></span> <span data-ttu-id="91a9e-177">Munið að þetta verður að vera danskur lánardrottinn með heimilisfang í Danmörku.</span><span class="sxs-lookup"><span data-stu-id="91a9e-177">Remember, this must be a Danish vendor with an address in Denmark.</span></span>
3. <span data-ttu-id="91a9e-178">Búa til reikning.</span><span class="sxs-lookup"><span data-stu-id="91a9e-178">Create an invoice.</span></span> <span data-ttu-id="91a9e-179">Reitirnir **Greiðslumáti** og **Númer lánardrottins** eru fylltir út samkvæmt stillingum á lánardrottnaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="91a9e-179">The **Payment Method** and **Vendor Number** fields are filled in based on settings on the Vendor card.</span></span> <span data-ttu-id="91a9e-180">Hægt er að breyta þeim ef óskað er.</span><span class="sxs-lookup"><span data-stu-id="91a9e-180">You can change them if you want.</span></span>
4. <span data-ttu-id="91a9e-181">Í **Greiðslutilvísun** skal slá inn 15 stafa númerið á reikningi lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="91a9e-181">In the **Payment Reference** field, enter the 15-digit number from the vendor invoice.</span></span>  

    > [!Tip]
    > <span data-ttu-id="91a9e-182">Þú verður aðeins að bæta við síðustu 11 tölustöfum í númerinu.</span><span class="sxs-lookup"><span data-stu-id="91a9e-182">You only have to add the last 11 digits of the number.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="91a9e-183">mun bæta fjórum núllum við upphaf númersins.</span><span class="sxs-lookup"><span data-stu-id="91a9e-183">will add four zeros to the beginning of the number.</span></span>  

5. <span data-ttu-id="91a9e-184">Bóka skal reikninginn.</span><span class="sxs-lookup"><span data-stu-id="91a9e-184">Post the invoice.</span></span>

## <a name="to-use-the-extension-to-export-payment-data"></a><span data-ttu-id="91a9e-185">Til að nota viðbótina til að flytja út greiðslugögn</span><span class="sxs-lookup"><span data-stu-id="91a9e-185">To use the extension to export payment data</span></span>

1. <span data-ttu-id="91a9e-186">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiðslubækur** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="91a9e-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals** , and then choose the related link.</span></span>  
2. <span data-ttu-id="91a9e-187">Velja **Stinga upp á greiðslubókum lánardrottins** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="91a9e-187">Choose the **Suggest Vendor Payment Journals** action.</span></span>  

    > [!Tip]
    > <span data-ttu-id="91a9e-188">Ef þú vilt aðeins flytja út tilteknar greiðslur skaltu nota afmörkunarvalkosti gagna.</span><span class="sxs-lookup"><span data-stu-id="91a9e-188">If you want to export only specific payments, use the options for filtering the data.</span></span>  

3. <span data-ttu-id="91a9e-189">Ef það er nauðsynlegt er hægt að bæta við afmörkunum til að flytja aðeins tilteknar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="91a9e-189">If needed, you can add filters to export only specific payments.</span></span>  
4. <span data-ttu-id="91a9e-190">Í reitnum **Tegund bankagreiðslu** skal velja **Rafræn greiðsla** .</span><span class="sxs-lookup"><span data-stu-id="91a9e-190">In the **Bank Payment Type** field, choose **Electronic Payment** .</span></span>  
5. <span data-ttu-id="91a9e-191">Veldu **Export** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="91a9e-191">Choose the **Export** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="91a9e-192">Sjá einnig .</span><span class="sxs-lookup"><span data-stu-id="91a9e-192">See also</span></span>

<span data-ttu-id="91a9e-193">[Sérstilla Business Central fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="91a9e-193">[Customizing Business Central for [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="91a9e-194">Innheimta greiðslur með SEPA-beingreiðslum</span><span class="sxs-lookup"><span data-stu-id="91a9e-194">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="91a9e-195">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="91a9e-195">Working with General Journals</span></span>](ui-work-general-journals.md)  
