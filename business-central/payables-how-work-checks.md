---
title: "Gefa út, prenta, hætta við og ógilda ávísanir| Microsoft Docs"
description: "Lýsir því hvernig skal gefa út ávísanir með því að nota greiðslubók, prenta ávísanir og ógilda eða skoða ávísanafjárhagsfærslur í Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: db28ad9a4adb45514b1d1287d269d8daefe64865
ms.openlocfilehash: 39b48fbd34b29db56b39712fbd2cbf5dc91fefc6
ms.contentlocale: is-is
ms.lasthandoff: 04/26/2018

---
# <a name="make-check-payments"></a><span data-ttu-id="019a2-103">Framkvæma ávísanagreiðslur</span><span class="sxs-lookup"><span data-stu-id="019a2-103">Make Check Payments</span></span>
<span data-ttu-id="019a2-104">Þú getur gefið út rafrænar og handvirkar ávísanir [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="019a2-104">You can issue electronic and manual checks in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="019a2-105">Í báðum aðferðum er útgreiðslubók notuð til að gefa út tékka til lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="019a2-105">Both methods use the payment journal to issue checks to vendors.</span></span> <span data-ttu-id="019a2-106">Einnig er hægt að ógilda tékka og skoða fjárhagsfærslur.</span><span class="sxs-lookup"><span data-stu-id="019a2-106">You can also void checks and view check ledger entries.</span></span>

<span data-ttu-id="019a2-107">Eftirfarandi ferli sýnir hvernig á að greiða lánardrottni með tölvuávísunum með því að jafna greiðsluna við viðeigandi reikning lánardrottins, prenta út ávísunina og síðan bóka greiðsluna sem greidda.</span><span class="sxs-lookup"><span data-stu-id="019a2-107">The following procedure shows how to pay a vendor with a computer checks by applying the payment to the relevant vendor invoice, printing the check, and then posting the payment as paid.</span></span> <span data-ttu-id="019a2-108">Þetta leiðir til jákvæðra lánardrottnafærslna, jafnaðar við neikvæðar bankafjárhagsfærslur og raunverulegar ávísanir fyrir úrvinnslu í bankanum.</span><span class="sxs-lookup"><span data-stu-id="019a2-108">This results in positive vendor ledger entries, applied to negative bank ledger entries, and physical checks for processing in the bank.</span></span>

<span data-ttu-id="019a2-109">Hægt er að greiða með tveimur gerðum af ávísunum.</span><span class="sxs-lookup"><span data-stu-id="019a2-109">You can pay with two types of checks.</span></span> <span data-ttu-id="019a2-110">Fyrir báðar gerðir verður reiturinn **Mótreikningur nr.** eða **Tegund reiknings** að innihalda **Bankareikning**.</span><span class="sxs-lookup"><span data-stu-id="019a2-110">For both types, the **Bal. Account Type** or the **Account Type** field must contain **Bank Account**.</span></span>

- <span data-ttu-id="019a2-111">**Vélfærður tékki**: veldu þennan valkost ef  á að prenta tékka með upphæðinni í færslubókarlínunni.</span><span class="sxs-lookup"><span data-stu-id="019a2-111">**Computer Check**: Select this option if you want to print a check for the amount on the payment journal line.</span></span> <span data-ttu-id="019a2-112">Þú þarft að prenta tékkana áður en þú bókar færslubókarlínurnar.</span><span class="sxs-lookup"><span data-stu-id="019a2-112">You must print the checks before you can post the journal lines.</span></span> <span data-ttu-id="019a2-113">Þú getur eingöngu valið **Vélfærður tékki** ef</span><span class="sxs-lookup"><span data-stu-id="019a2-113">You can only select **Computer Check** if</span></span>
- <span data-ttu-id="019a2-114">**Handfærður tékki**  Þessi kostur er valinn ef handfærður tékki hefur verið búinn til og  á að búa til tékkafærslu sem samsvarar upphæðinni.</span><span class="sxs-lookup"><span data-stu-id="019a2-114">**Manual Check**: Select this option if you have created a check manually and want to create a corresponding check ledger entry for this amount.</span></span> <span data-ttu-id="019a2-115">Með því að nota þennan valkost er ekki hægt að prenta út ávísun.</span><span class="sxs-lookup"><span data-stu-id="019a2-115">By using this option, you cannot print the check.</span></span>

> [!NOTE]  
> <span data-ttu-id="019a2-116">Til að ganga úr skugga um að bankinn þinn eingöngu taki við fullgildum ávísunum og upphæðum, geturðu sent þeim skrá sem inniheldur seljanda, ávísun og greiðsluupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="019a2-116">To make sure that your bank only clears validated checks and amounts, you can send them a file that contains vendor, check, and payment information.</span></span> <span data-ttu-id="019a2-117">Nánari upplýsingar er að finna í [Flytja út jákvæða greiðsluskrá](finance-how-positive-pay.md).</span><span class="sxs-lookup"><span data-stu-id="019a2-117">For more information, see [Export a Positive Pay file](finance-how-positive-pay.md).</span></span>

<span data-ttu-id="019a2-118">Prentarinn verður að vera rétt stilltur með tékkaeyðublöðum, og þú verður að skilgreina hvaða útlit tékka á að nota.</span><span class="sxs-lookup"><span data-stu-id="019a2-118">Your printer must be correctly set up with the check forms, and you must define which check layout to use.</span></span> <span data-ttu-id="019a2-119">Nánari upplýsingar sjá [Skilgreina útlit ávísana](finance-how-define-check-layouts.md)</span><span class="sxs-lookup"><span data-stu-id="019a2-119">For more information, see [Define Check Layouts](finance-how-define-check-layouts.md)</span></span>

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a><span data-ttu-id="019a2-120">Til að greiða reikning lánardrottins með vélfærðum tékka</span><span class="sxs-lookup"><span data-stu-id="019a2-120">To pay a vendor invoice with a computer check</span></span>
<span data-ttu-id="019a2-121">Eftirfarandi dæmi sýnir hvernig á að greiða lánardrottni með ávísun.</span><span class="sxs-lookup"><span data-stu-id="019a2-121">The following describes how to pay a vendor by check.</span></span> <span data-ttu-id="019a2-122">Skrefin eru svipuð og endurgreiðsla til viðskiptavinar með ávísun.</span><span class="sxs-lookup"><span data-stu-id="019a2-122">The steps are similar to refund a customer by check.</span></span>

1. <span data-ttu-id="019a2-123">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **greiðslubækur** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="019a2-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="019a2-124">Fyllið út greiðslubókarlínurnar.</span><span class="sxs-lookup"><span data-stu-id="019a2-124">Fill in the payment journal lines.</span></span> <span data-ttu-id="019a2-125">Nánari upplýsingar eru í [Skrá greiðslur og endurgreiðslur](payables-how-post-payments-refunds.md).</span><span class="sxs-lookup"><span data-stu-id="019a2-125">For more information, see [Record Payments and Refunds](payables-how-post-payments-refunds.md).</span></span>
3. <span data-ttu-id="019a2-126">Í reitnum **Kóði greiðslumáta** skal velja **Ávísun**.</span><span class="sxs-lookup"><span data-stu-id="019a2-126">In the **Payment Method Code** field, select **Check**.</span></span>
4. <span data-ttu-id="019a2-127">Í reitnum **Tegund bankagreiðslu** skal velja **Vélfærður tékki**.</span><span class="sxs-lookup"><span data-stu-id="019a2-127">In the **Bank Payment Type** field, select **Computer Check**.</span></span>
5. <span data-ttu-id="019a2-128">Veldu aðgerðina **Prenta ávísun**.</span><span class="sxs-lookup"><span data-stu-id="019a2-128">Choose the **Print Check** action.</span></span>
6. <span data-ttu-id="019a2-129">Í glugganum **ávísun** þarf að fylla reitina út eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="019a2-129">In the **Check** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. <span data-ttu-id="019a2-130">Veldu hnappinn **Senda til**, veldu valkostinn **PDF-skjal** og veldu síðan hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="019a2-130">Choose the **Send to** button, select the **PDF Document** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="019a2-131">Raunverulegu ávísanirnar er nú hægt að fara með í bankann til vinnslu.</span><span class="sxs-lookup"><span data-stu-id="019a2-131">The physical checks can now be brought to the bank for processing.</span></span> <span data-ttu-id="019a2-132">Haltu áfram að bóka greiðsluna eins og hún er jöfnuð við lánardrottin og þar af leiðandi greidd í kerfinum.</span><span class="sxs-lookup"><span data-stu-id="019a2-132">Proceed to post the payment as applied to the vendor and thereby paid in the system.</span></span>
8. <span data-ttu-id="019a2-133">Valið er **Bóka** aðgerðin.</span><span class="sxs-lookup"><span data-stu-id="019a2-133">Choose the **Post** action.</span></span>

<span data-ttu-id="019a2-134">Lánardrottnafærslur og fjárhagsfærslur sem eru jafnaðar að fullu eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="019a2-134">Fully applied vendor ledger entries and bank ledger entries are created.</span></span>

> [!NOTE]  
> <span data-ttu-id="019a2-135">Ef þarf að prenta og greiða tékka í fleiri en einum gjaldmiðli frá mismunandi bankareikningum verður að keyra keyrsluna **Prenta tékka** sérstaklega fyrir hvern gjaldmiðil og tilgreina réttan bankareikning.</span><span class="sxs-lookup"><span data-stu-id="019a2-135">If you want to print and pay checks in more than one currency from different bank accounts, you must run the **Print Check** batch job separately for each currency and specify the appropriate bank account.</span></span>

## <a name="to-cancel-printed-checks-that-are-not-posted"></a><span data-ttu-id="019a2-136">Til að ógilda prentaðan tékka sem ekki eru bókaðar</span><span class="sxs-lookup"><span data-stu-id="019a2-136">To cancel printed checks that are not posted</span></span>
<span data-ttu-id="019a2-137">Hægt er að ógilda tékka sem eftir á að bóka þegar þær hafa verið prentuð með því að nota **Ógilda Tékka** aðgerð í á **greiðslubók** glugga.</span><span class="sxs-lookup"><span data-stu-id="019a2-137">You can cancel non-posted checks after they have been printed by using the **Void Check** action in the **Payment Journal** window.</span></span>

1. <span data-ttu-id="019a2-138">Í á **greiðslubókarglugga** er valið á **Ógilda Tékka**, og síðan valið hvaða tékka á að ógilda.</span><span class="sxs-lookup"><span data-stu-id="019a2-138">In the **Payment Journal** window, choose the **Void Check**, and then choose which checks to cancel.</span></span>

## <a name="to-void-checks"></a><span data-ttu-id="019a2-139">Tékkar ógiltir:</span><span class="sxs-lookup"><span data-stu-id="019a2-139">To void checks</span></span>
<span data-ttu-id="019a2-140">Þegar tékkagreiðslur hafa verið bókaðar, geturðu aðeins afturkallað (ógilt) tékka úr bankafærslum sem fengust út úr þessu.</span><span class="sxs-lookup"><span data-stu-id="019a2-140">When check payment have been posted, you can only cancel (void) checks from the resulting bank ledger entries.</span></span>

1. <span data-ttu-id="019a2-141">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bankareikningar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="019a2-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="019a2-142">Veldu viðeigandi bankareikning, veldu **breyta** aðgerðina og veldu síðan **tékkafærslur** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="019a2-142">Select the relevant bank account, choose the **Edit** action, and then choose the **Check Ledger Entries** action.</span></span>
3. <span data-ttu-id="019a2-143">Í **tékkafærslur** glugganum, veldu **ógilda tékka** aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="019a2-143">In the **Check Ledger Entries** window, choose the **Void Check** action.</span></span>
4. <span data-ttu-id="019a2-144">Veldu gátreitinn **eingöngu ógilda tékka**.</span><span class="sxs-lookup"><span data-stu-id="019a2-144">Select the **Void Check Only** check box.</span></span>
5. <span data-ttu-id="019a2-145">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="019a2-145">Choose the **OK** button.</span></span>

## <a name="to-view-a-summary-of-posted-checks"></a><span data-ttu-id="019a2-146">Til að skoða samantekt bókaðra tékka</span><span class="sxs-lookup"><span data-stu-id="019a2-146">To view a summary of posted checks</span></span>
<span data-ttu-id="019a2-147">Ef þú vilt endurskoða bókaða tékka, til dæmis til að staðfesta marga greidda tékka til eins lánardrottins, getur þú notað skýrsluna **Bankareikningur - Upplýsingar um tékka**.</span><span class="sxs-lookup"><span data-stu-id="019a2-147">If you want to review posted checks, for example to verify multiple checks paid to one vendor, you can use the **Bank Account - Check Details** report.</span></span>
1. <span data-ttu-id="019a2-148">Velja skal táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið"), slá inn **Bankareikningur - Upplýsingar um tékka** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="019a2-148">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Account - Check Details**, and then choose the related link.</span></span>
2. <span data-ttu-id="019a2-149">Stilla afmarkanir sem viðeigandi og velja svo hnappinn **Forskoða**.</span><span class="sxs-lookup"><span data-stu-id="019a2-149">Set filters as relevant, and then choose the **Preview** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="019a2-150">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="019a2-150">See Also</span></span>
[<span data-ttu-id="019a2-151">Framkvæma greiðslur</span><span class="sxs-lookup"><span data-stu-id="019a2-151">Making Payments</span></span>](payables-make-payments.md)  
[<span data-ttu-id="019a2-152">Stjórna skuldum</span><span class="sxs-lookup"><span data-stu-id="019a2-152">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="019a2-153">Uppsetning bankaþjónustu</span><span class="sxs-lookup"><span data-stu-id="019a2-153">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="019a2-154">Flytja út jákvæða greiðsluskrá</span><span class="sxs-lookup"><span data-stu-id="019a2-154">Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="019a2-155">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="019a2-155">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

