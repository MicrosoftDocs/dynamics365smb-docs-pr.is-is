---
title: "Notkun greiðslna og afstemmingar (DK) viðbótarinnar | Microsoft Docs"
description: "Þessi viðbót gerir það auðvelt að flytja út skrár sem eru forstilltar til að uppfylla kröfur banka um rafræna skráningu."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 09/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b345100f2ec89685855bfd8e630e3ef44506e86d
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---

# <a name="the-payments-and-reconciliations-dk-extension-for-microsoft-dynamics-for-business-central"></a><span data-ttu-id="68890-103">Greiðslur og afstemmingar (DK) viðbótin fyrir Microsoft Dynamics for Business Central</span><span class="sxs-lookup"><span data-stu-id="68890-103">The Payments and Reconciliations (DK) Extension for Microsoft Dynamics for Business Central</span></span>
<span data-ttu-id="68890-104">Greiddu hratt og án mistaka með því að flytja út skrár sem eru sérstaklega sniðnar fyrir millifærslur með lánardrottni eða banka.</span><span class="sxs-lookup"><span data-stu-id="68890-104">Make fast, error-free payments by exporting files that are formatted specifically for exchanges with your vendor or bank.</span></span> <span data-ttu-id="68890-105">Þessar skrár flýta fyrir greiðslu- og afstemmingum og útrýma villum sem geta komið upp þegar upplýsingar eru slegnar inn á bankasíðu.</span><span class="sxs-lookup"><span data-stu-id="68890-105">These files speed up the payment and reconciliation processes, and eliminate errors that can happen when you manually enter the information on a bank website.</span></span>  
  
<span data-ttu-id="68890-106">Þessi viðbót styður skráarsnið fyrir nokkra danska banka.</span><span class="sxs-lookup"><span data-stu-id="68890-106">This extension supports file formats for several Danish banks.</span></span> <span data-ttu-id="68890-107">Þegar þú flytur út greiðsluupplýsingar í skrá pakkar viðbótin gögnunum inn í sniðið sem bankinn fer fram á.</span><span class="sxs-lookup"><span data-stu-id="68890-107">When you export payment information to a file, the extension packages the data into the format that your bank requires.</span></span> <span data-ttu-id="68890-108">Dæmi um þetta eru sniðin Bankdata-V3, BEC, SDC og FIK, sem margir mismunandi bankar nota, og sum sem eru sérhæfðari fyrir tiltekna banka á borð við Danske Bank og Nordea.</span><span class="sxs-lookup"><span data-stu-id="68890-108">For example, the formats include Bankdata-V3, BEC, SDC, and FIK, which many different banks use, and some that are more specialized for certain banks, for example, Danske Bank and Nordea.</span></span> <span data-ttu-id="68890-109">Viðbótin inniheldur einnig nokkur snið til að flytja inn og afstemma bankareikninga.</span><span class="sxs-lookup"><span data-stu-id="68890-109">The extension also includes some formats for importing and reconciling bank statements.</span></span>  
  
> [!Note]
> <span data-ttu-id="68890-110">Til að nota viðbótina er nauðsynlegt að vita hvaða snið bankinn eða lánardrottinn krefst.</span><span class="sxs-lookup"><span data-stu-id="68890-110">To use the extension, you must know the format that your bank or vendor requires.</span></span> <span data-ttu-id="68890-111">Sumir bankar eða lánardrottnar veita þessar upplýsingar á vefsvæðum sínum: Hins vegar gætirðu þurft að hafa samband við þjónustudeild þeirra til að fá upplýsingarnar.</span><span class="sxs-lookup"><span data-stu-id="68890-111">Some banks or vendors provide this information on their websites; however, you might need to contact their customer service to get the information.</span></span>  
  
## <a name="supported-bank-formats"></a><span data-ttu-id="68890-112">Studd bankasnið</span><span class="sxs-lookup"><span data-stu-id="68890-112">Supported Bank Formats</span></span>
<span data-ttu-id="68890-113">Þessi viðbót getur notað eftirfarandi skráarsnið fyrir greiðsluskrár:</span><span class="sxs-lookup"><span data-stu-id="68890-113">This extension can apply the following file formats for payment files:</span></span>  
  
* <span data-ttu-id="68890-114">BANKDATA-V3</span><span class="sxs-lookup"><span data-stu-id="68890-114">BANKDATA-V3</span></span>  
* <span data-ttu-id="68890-115">BEC-INDLAND</span><span class="sxs-lookup"><span data-stu-id="68890-115">BEC-INDLAND</span></span>  
* <span data-ttu-id="68890-116">BEC-CSV</span><span class="sxs-lookup"><span data-stu-id="68890-116">BEC-CSV</span></span>  
* <span data-ttu-id="68890-117">DANSKEBANK-CMKV</span><span class="sxs-lookup"><span data-stu-id="68890-117">DANSKEBANK-CMKV</span></span>  
* <span data-ttu-id="68890-118">DANSKEBANK-CMKXKSX</span><span class="sxs-lookup"><span data-stu-id="68890-118">DANSKEBANK-CMKXKSX</span></span>  
* <span data-ttu-id="68890-119">DANSKEBANK</span><span class="sxs-lookup"><span data-stu-id="68890-119">DANSKEBANK</span></span>  
* <span data-ttu-id="68890-120">FIK71</span><span class="sxs-lookup"><span data-stu-id="68890-120">FIK71</span></span>  
* <span data-ttu-id="68890-121">NORDEA-ERHVERV-CSV</span><span class="sxs-lookup"><span data-stu-id="68890-121">NORDEA-ERHVERV-CSV</span></span>  
* <span data-ttu-id="68890-122">NORDEA</span><span class="sxs-lookup"><span data-stu-id="68890-122">NORDEA</span></span>  
* <span data-ttu-id="68890-123">NORDEA-UNITEL-V3</span><span class="sxs-lookup"><span data-stu-id="68890-123">NORDEA-UNITEL-V3</span></span>  
* <span data-ttu-id="68890-124">SDC</span><span class="sxs-lookup"><span data-stu-id="68890-124">SDC</span></span>  
* <span data-ttu-id="68890-125">SDC-CSV</span><span class="sxs-lookup"><span data-stu-id="68890-125">SDC-CSV</span></span>  

## <a name="to-set-up-the-extension"></a><span data-ttu-id="68890-126">Til að setja upp viðbótina</span><span class="sxs-lookup"><span data-stu-id="68890-126">To set up the extension</span></span>
<span data-ttu-id="68890-127">Nokkur skref eru nauðsynleg í upphafi.</span><span class="sxs-lookup"><span data-stu-id="68890-127">There are a few steps to get started.</span></span>  
  
* <span data-ttu-id="68890-128">Leyfa útflutning greiðslugagna.</span><span class="sxs-lookup"><span data-stu-id="68890-128">Allow payment data exports.</span></span> <span data-ttu-id="68890-129">Til að vernda gögnin þín er þetta ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="68890-129">To help protect your data, this is not readily available.</span></span>  
* <span data-ttu-id="68890-130">Setja upp innkaup og viðskiptaskuldir þannig að þú þurfir ekki utanaðkomandi skjalanúmer á reikningum.</span><span class="sxs-lookup"><span data-stu-id="68890-130">Set up purchase and payables so that you do not require external document numbers on invoices.</span></span> <span data-ttu-id="68890-131">Ef þess er þörf geturðu notað tilvísunarnúmerið til að vísa til tiltekins reiknings.</span><span class="sxs-lookup"><span data-stu-id="68890-131">If needed, you can use the reference number to refer to a specific invoice.</span></span>  
* <span data-ttu-id="68890-132">Tilgreina greiðslumáta fyrir hvern lánardrottininn.</span><span class="sxs-lookup"><span data-stu-id="68890-132">Specify the payment method for each vendor.</span></span> <span data-ttu-id="68890-133">Greiðslumátar skilgreina hvernig þú borgar reikninga frá lánardrottninum.</span><span class="sxs-lookup"><span data-stu-id="68890-133">Payment methods define how you pay invoices from the vendor.</span></span> <span data-ttu-id="68890-134">Til dæmis Banki, Staðgreiðsla, Ávísun eða Reikningur.</span><span class="sxs-lookup"><span data-stu-id="68890-134">For example, Bank, Cash, Check, or Account.</span></span>  
* <span data-ttu-id="68890-135">Tilgreina gerð sniðsins sem á að nota fyrir hvern bankareikning.</span><span class="sxs-lookup"><span data-stu-id="68890-135">Specify the type of format to use for each of your bank accounts.</span></span> <span data-ttu-id="68890-136">Til dæmis NORDEA, DANSKEBANK, SDC og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="68890-136">For example, NORDEA, DANSKEBANK, SDC, and so on.</span></span>  
  
<span data-ttu-id="68890-137">Að auki þarftu að úthluta lánardrottnum á staðbundinn **Alm. viðsk.bókunarflokkur** og **Bókunarflokk lánardrottins**.</span><span class="sxs-lookup"><span data-stu-id="68890-137">Additionally, you must assign vendors to a domestic **Gen. Bus. Posting Group** and a **Vendor Posting Group**.</span></span> <span data-ttu-id="68890-138">Stilling fyrir land/svæði fyrir lánardrottinn verður að vera Danmörk (DK).</span><span class="sxs-lookup"><span data-stu-id="68890-138">The Country/Region setting for the vendor must be Denmark (DK).</span></span> <span data-ttu-id="68890-139">Nánari upplýsingar er að finna í [Uppsetning Bókunarflokka](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="68890-139">For more information, see [Setting Up Posting Groups](finance-posting-groups.md).</span></span>  
  
### <a name="to-allow-included365finincludesd365finmdmd-to-export-payment-data"></a><span data-ttu-id="68890-140">Til að leyfa [!INCLUDE[d365fin](includes/d365fin_md.md)] að flytja út greiðslugögn</span><span class="sxs-lookup"><span data-stu-id="68890-140">To allow [!INCLUDE[d365fin](includes/d365fin_md.md)] to export payment data</span></span>
1. <span data-ttu-id="68890-141">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **greiðslubók** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="68890-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="68890-142">Í glugganum **Breyta greiðslubók** er valið **Banki**.</span><span class="sxs-lookup"><span data-stu-id="68890-142">In the **Edit Payment Journal** window, choose the **Bank** batch.</span></span>  
3. <span data-ttu-id="68890-143">Veljið gátreitinn **Leyfa greiðsluútflutning**.</span><span class="sxs-lookup"><span data-stu-id="68890-143">Choose the **Allow Payment Export** check box.</span></span>  

### <a name="to-specify-a-payment-method-for-a-vendor"></a><span data-ttu-id="68890-144">Til að tilgreina greiðslumáta lánardrottins</span><span class="sxs-lookup"><span data-stu-id="68890-144">To specify a payment method for a vendor</span></span>
<span data-ttu-id="68890-145">Eftirfarandi tafla sýnir sambland FIK og GIRO greiðslumáta sem [!INCLUDE[d365fin](includes/d365fin_md.md)] styður.</span><span class="sxs-lookup"><span data-stu-id="68890-145">The following table shows the combinations of FIK and GIRO payment methods that [!INCLUDE[d365fin](includes/d365fin_md.md)] supports.</span></span>

||<span data-ttu-id="68890-146">Gerð 01</span><span class="sxs-lookup"><span data-stu-id="68890-146">Type 01</span></span> | <span data-ttu-id="68890-147">Gerð 04</span><span class="sxs-lookup"><span data-stu-id="68890-147">Type 04</span></span> | <span data-ttu-id="68890-148">Gerð 71</span><span class="sxs-lookup"><span data-stu-id="68890-148">Type 71</span></span> | <span data-ttu-id="68890-149">Gerð 73</span><span class="sxs-lookup"><span data-stu-id="68890-149">Type 73</span></span> |
|----|---|---|---|---|
|<span data-ttu-id="68890-150">Númer gíróreiknings eða FIK-lánardrottins?</span><span class="sxs-lookup"><span data-stu-id="68890-150">Giro Account No. or FIK Creditor No.?</span></span> | <span data-ttu-id="68890-151">Númer gíróreiknings</span><span class="sxs-lookup"><span data-stu-id="68890-151">Giro Account No.</span></span> | <span data-ttu-id="68890-152">Númer gíróreiknings</span><span class="sxs-lookup"><span data-stu-id="68890-152">Giro Account No.</span></span> | <span data-ttu-id="68890-153">Númer FIK-lánardrottins</span><span class="sxs-lookup"><span data-stu-id="68890-153">FIK Creditor No.</span></span> | <span data-ttu-id="68890-154">Númer FIK-lánardrottins</span><span class="sxs-lookup"><span data-stu-id="68890-154">FIK Creditor No.</span></span>|
|<span data-ttu-id="68890-155">Leyfja skilaboð til viðtakanda?</span><span class="sxs-lookup"><span data-stu-id="68890-155">Allows Message to Recipient?</span></span> | <span data-ttu-id="68890-156">Já</span><span class="sxs-lookup"><span data-stu-id="68890-156">Yes</span></span> |<span data-ttu-id="68890-157">Nei</span><span class="sxs-lookup"><span data-stu-id="68890-157">No</span></span> |<span data-ttu-id="68890-158">Nei</span><span class="sxs-lookup"><span data-stu-id="68890-158">No</span></span> | <span data-ttu-id="68890-159">Já</span><span class="sxs-lookup"><span data-stu-id="68890-159">Yes</span></span> |
|<span data-ttu-id="68890-160">Inniheldur greiðslutilvísunarnúmer?</span><span class="sxs-lookup"><span data-stu-id="68890-160">Contains Payment Reference number?</span></span> | <span data-ttu-id="68890-161">Nei</span><span class="sxs-lookup"><span data-stu-id="68890-161">No</span></span> | <span data-ttu-id="68890-162">Já, 16 stafir.</span><span class="sxs-lookup"><span data-stu-id="68890-162">Yes, 16 digits.</span></span> | <span data-ttu-id="68890-163">Já, 15 stafir.</span><span class="sxs-lookup"><span data-stu-id="68890-163">Yes, 15 digits.</span></span> | <span data-ttu-id="68890-164">Nei</span><span class="sxs-lookup"><span data-stu-id="68890-164">No</span></span>|

1. <span data-ttu-id="68890-165">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **lánardrottnar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="68890-165">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="68890-166">Opnaðu kortið, víkkaðu **Greiðslur** flipann, í **Greiðslumáti** veldu greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="68890-166">Open the card, expand the **Payments** tab, in the **Payment Method** field choose the payment method.</span></span>  
3. <span data-ttu-id="68890-167">Nauðsynlegt er að ljúka öðrum reitum, allt eftir valinu.</span><span class="sxs-lookup"><span data-stu-id="68890-167">Depending on your selection, you must complete other fields.</span></span> <span data-ttu-id="68890-168">Lýsing samsetninga er að finna í töflunni hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="68890-168">See the table above for a description of the combinations.</span></span>  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a><span data-ttu-id="68890-169">Til að tilgreina sniðið sem á að nota fyrir bankareikning</span><span class="sxs-lookup"><span data-stu-id="68890-169">To specify the format to use for a bank account</span></span>
1. <span data-ttu-id="68890-170">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Bankareikningar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="68890-170">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="68890-171">Opna spjaldið fyrir bankareikninginn.</span><span class="sxs-lookup"><span data-stu-id="68890-171">Open the card for the bank account.</span></span>  
3. <span data-ttu-id="68890-172">Á **Útflutningssnið greiðslu** skal velja sniðið fyrir útflutningsskrána.</span><span class="sxs-lookup"><span data-stu-id="68890-172">In the **Payment Export Format** field, choose the format for your export file.</span></span>  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a><span data-ttu-id="68890-173">Velja FIK eða Gírógreiðsluupplýsingar fyrir reikninga lánardrottins</span><span class="sxs-lookup"><span data-stu-id="68890-173">Choosing the FIK or Giro payment information for vendor invoices</span></span>
1. <span data-ttu-id="68890-174">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Innkaupareikningar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="68890-174">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="68890-175">Veljið lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="68890-175">Choose the vendor.</span></span> <span data-ttu-id="68890-176">Munið að þetta verður að vera danskur lánardrottinn með heimilisfang í Danmörku.</span><span class="sxs-lookup"><span data-stu-id="68890-176">Remember, this must be a Danish vendor with an address in Denmark.</span></span>
3. <span data-ttu-id="68890-177">Búa til reikning.</span><span class="sxs-lookup"><span data-stu-id="68890-177">Create an invoice.</span></span> <span data-ttu-id="68890-178">Reitirnir **Greiðslumáti** og **Númer lánardrottins** eru fylltir út samkvæmt stillingum á lánardrottnaspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="68890-178">The **Payment Method** and **Vendor Number** fields are filled in based on settings on the Vendor card.</span></span> <span data-ttu-id="68890-179">Hægt er að breyta þeim ef óskað er.</span><span class="sxs-lookup"><span data-stu-id="68890-179">You can change them if you want.</span></span>
4. <span data-ttu-id="68890-180">Í **Greiðslutilvísun** skal slá inn 15 stafa númerið á reikningi lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="68890-180">In the **Payment Reference** field, enter the 15-digit number from the vendor invoice.</span></span>  
  
    > [!Tip]
    > <span data-ttu-id="68890-181">Þú verður aðeins að bæta við síðustu 11 tölustöfum í númerinu.</span><span class="sxs-lookup"><span data-stu-id="68890-181">You only have to add the last 11 digits of the number.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="68890-182"> mun bæta fjórum núllum við upphaf númersins.</span><span class="sxs-lookup"><span data-stu-id="68890-182"> will add four zeros to the beginning of the number.</span></span>  
  
5. <span data-ttu-id="68890-183">Bóka skal reikninginn.</span><span class="sxs-lookup"><span data-stu-id="68890-183">Post the invoice.</span></span>

## <a name="to-use-the-extension-to-export-payment-data"></a><span data-ttu-id="68890-184">Til að nota viðbótina til að flytja út greiðslugögn</span><span class="sxs-lookup"><span data-stu-id="68890-184">To use the extension to export payment data</span></span>
1. <span data-ttu-id="68890-185">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **greiðslubækur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="68890-185">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="68890-186">Velja **Stinga upp á greiðslubókum lánardrottins** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="68890-186">Choose the **Suggest Vendor Payment Journals** action.</span></span>  
  
    > [!Tip]
    > <span data-ttu-id="68890-187">Ef þú vilt aðeins flytja út tilteknar greiðslur skaltu nota afmörkunarvalkosti gagna.</span><span class="sxs-lookup"><span data-stu-id="68890-187">If you want to export only specific payments, use the options for filtering the data.</span></span>  
  
3. <span data-ttu-id="68890-188">Ef það er nauðsynlegt er hægt að bæta við afmörkunum til að flytja aðeins tilteknar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="68890-188">If needed, you can add filters to export only specific payments.</span></span>  
4. <span data-ttu-id="68890-189">Í reitnum **Tegund bankagreiðslu** skal velja **Rafræn greiðsla**.</span><span class="sxs-lookup"><span data-stu-id="68890-189">In the **Bank Payment Type** field, choose **Electronic Payment**.</span></span>  
5. <span data-ttu-id="68890-190">Veldu **Export** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="68890-190">Choose the **Export** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="68890-191">Sjá einnig .</span><span class="sxs-lookup"><span data-stu-id="68890-191">See also</span></span>
<span data-ttu-id="68890-192">[Sérstilla Business Central fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="68890-192">[Customizing Business Central for [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="68890-193">Stofna SEPA-innheimtufærslur fyrir beingreiðslur og flytja út í bankaskrá</span><span class="sxs-lookup"><span data-stu-id="68890-193">Create SEPA Direct Debit Collection Entries and Export to a Bank File</span></span>](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
[<span data-ttu-id="68890-194">Setja upp SEPA-beingreiðslur</span><span class="sxs-lookup"><span data-stu-id="68890-194">Set Up SEPA Direct Debit</span></span>](finance-how-to-set-up-sepa-direct-debit.md)  
[<span data-ttu-id="68890-195">Bóka SEPA-greiðslukvittanir beingreiðslna</span><span class="sxs-lookup"><span data-stu-id="68890-195">Post SEPA Direct Debit Payment Receipts</span></span>](finance-how-to-post-sepa-direct-debit-payment-receipts.md)  
[<span data-ttu-id="68890-196">Innheimta greiðslur með SEPA-beingreiðslum</span><span class="sxs-lookup"><span data-stu-id="68890-196">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="68890-197">Vinna í færslubókum</span><span class="sxs-lookup"><span data-stu-id="68890-197">Working with General Journals</span></span>](ui-work-general-journals.md)  





