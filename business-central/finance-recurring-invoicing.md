---
title: Vinna með endurteknar tekjur | Microsoft docs
description: Frekari upplýsingar um tiltæka valmöguleika sem gera þér kleift að senda greiðslureikninga til viðskiptavina þinna og skrá endurteknar tekjur.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: recurring, invoicing, subscription, billing
ms.reviewer: edupont
ms.date: 05/27/2020
ms.author: andreipa
ms.openlocfilehash: a0439557ce69b3c53406bd43b3b76cdf9ae73a10
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410788"
---
# <a name="work-with-recurring-revenue-in-d365fin"></a><span data-ttu-id="91398-103">Vinna með endurteknar tekjur í [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="91398-103">Work with recurring revenue in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>

<span data-ttu-id="91398-104">Mörg fyrirtæki eru að færa sig úr tekjulíkönum þar sem tekjur eru úr einskiptiskaupum viðskiptavinar í viðskiptalíkan þar sem tekjur eru gerðar á endurteknum grunni í skiptum fyrir stöðugt aðgengi að afhendingu góðrar vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="91398-104">Many companies are moving from a business revenue model where revenue is made from a customer's one-time purchase to a subscription model where revenue is made on a recurring basis in return for consistent access to the delivery of a good or service.</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="91398-105">er með eftirfarandi valmöguleika til að gera sendingerferli reikninga í gegnum viðskiptavini og skráningu endurtekinna tekna sjálfvirkt.</span><span class="sxs-lookup"><span data-stu-id="91398-105">has the following options for automating how you send subscription invoices to your customers and register recurring revenue.</span></span> 

## <a name="register-revenue-with-a-recurring-general-journal"></a><span data-ttu-id="91398-106">Skrá tekjur með ítrekunarfærslubók</span><span class="sxs-lookup"><span data-stu-id="91398-106">Register revenue with a recurring general journal</span></span>

<span data-ttu-id="91398-107">Ítrekunarbók er færslubók með sérstökum reitum til að stjórna færslum sem eru bókaðar reglulega með litlum eða engum breytingum, t.d. leigu, áskriftum, rafmagni eða hita.</span><span class="sxs-lookup"><span data-stu-id="91398-107">A recurring journal is a general journal with specific fields for managing transactions that you post frequently with few or no changes, such as rent, subscriptions, electricity, or heat.</span></span> <span data-ttu-id="91398-108">Með því að nota þessa reiti fyrir endurteknar færslur er hægt að bóka bæði fastar og breytilegar upphæðir.</span><span class="sxs-lookup"><span data-stu-id="91398-108">Using these fields for recurring transactions, you can post both fixed and variable amounts.</span></span> <span data-ttu-id="91398-109">Með ítrekunarbók þarf aðeins einu sinni að setja inn færslur sem bókaðar verða reglulega.</span><span class="sxs-lookup"><span data-stu-id="91398-109">With a recurring journal, entries that will be posted regularly need to be typed in only once.</span></span> <span data-ttu-id="91398-110">Það þýðir að reikningar, víddir og víddargildi o.s.frv sem fært er inn verður áfram í færslubókinni að lokinni bókun.</span><span class="sxs-lookup"><span data-stu-id="91398-110">That is, the accounts, dimensions and dimension values and so on that you enter will be remain in the journal after posting.</span></span> <span data-ttu-id="91398-111">Óhjákvæmilegar leiðréttingar má gera við hverja bókun.</span><span class="sxs-lookup"><span data-stu-id="91398-111">If any adjustments are necessary, you can make them with each posting.</span></span>

### <a name="why-use-this-option"></a><span data-ttu-id="91398-112">Af hverju að nota þennan möguleika</span><span class="sxs-lookup"><span data-stu-id="91398-112">Why use this option</span></span>

<span data-ttu-id="91398-113">Með þessum valkosti eru sveigjanleg reikningsfærslutímabil skilgreind með [Dagsetningarformúlum](ui-enter-date-ranges.md#using-date-formulas).</span><span class="sxs-lookup"><span data-stu-id="91398-113">With this option, you define flexible invoicing periods with [Date Formulas](ui-enter-date-ranges.md#using-date-formulas).</span></span>

<span data-ttu-id="91398-114">Með þessum valkosti er hins vegar ekki hægt að prenta og senda reikninga í sjálfgefinni útgáfu af [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="91398-114">However, with this option, you cannot print and send invoices in the default version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="91398-115">Frekari upplýsingar er að finna í [Vinna með Ítrekunarbækur](ui-work-general-journals.md#working-with-recurring-journals).</span><span class="sxs-lookup"><span data-stu-id="91398-115">For more information, see [Working with Recurring Journals](ui-work-general-journals.md#working-with-recurring-journals).</span></span>  

## <a name="create-multiple-invoices-based-on-a-recurring-job-journal"></a><span data-ttu-id="91398-116">Stofna marga reikninga byggða á ítrekunarverkbók verka</span><span class="sxs-lookup"><span data-stu-id="91398-116">Create multiple invoices based on a recurring job journal</span></span>

<span data-ttu-id="91398-117">Ítrekunarbók vinnslunnar er ítarlegri valkostur en almenn færslubók.</span><span class="sxs-lookup"><span data-stu-id="91398-117">The recurring job journal is a more advanced alternative to the general journal.</span></span> <span data-ttu-id="91398-118">Hægt er að skilgreina vörur, tilföng og fjárhagsreikninga sem þarf að endurtaka fyrir hvert verk, og tilgreina tíðni endurtekninga.</span><span class="sxs-lookup"><span data-stu-id="91398-118">You define Items, Resources and G/L Accounts, that must be repeated for each job, and you specify the frequency of recurrence.</span></span>  

<span data-ttu-id="91398-119">Þegar búið er að bóka endurtekna verkbók er hægt að búa til marga reikninga með **Stofna verksölureikning**.</span><span class="sxs-lookup"><span data-stu-id="91398-119">After posting a recurring job journal, you can create multiple invoices with the **Create Job Sales Invoice** task.</span></span> <span data-ttu-id="91398-120">Hægt er að yfirfara og bóka stofnaða reikninga á síðunni **Sölureikningar** .</span><span class="sxs-lookup"><span data-stu-id="91398-120">You can review and post created invoices in the **Sales Invoices** page.</span></span>

### <a name="why-use-this-option"></a><span data-ttu-id="91398-121">Af hverju að nota þennan möguleika</span><span class="sxs-lookup"><span data-stu-id="91398-121">Why use this option</span></span>

<span data-ttu-id="91398-122">Með þessum valkosti fylgir staðlað reikningsfærsluferli með öllum fríðindum þess, þar á meðal stöðluðu og útliti viðskiptavinar fyrir samskipti.</span><span class="sxs-lookup"><span data-stu-id="91398-122">With this option, you follow the standard invoicing procedure with all the benefits of that, including standard and customer layouts for communication preferences.</span></span> <span data-ttu-id="91398-123">Einnig er hægt að skilgreina verð fyrir hvert verk fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="91398-123">You can also define prices for each job individually.</span></span>

<span data-ttu-id="91398-124">Fyrir hvern nýjan viðskiptavin verður hins vegar að stofna nýtt starf og bæta línum við ítrekunarbókina.</span><span class="sxs-lookup"><span data-stu-id="91398-124">However, for each new customer, you must create a new job and add lines to the recurring journal.</span></span> 

<span data-ttu-id="91398-125">Frekari upplýsingar er að finna í [Stofna verkbókarlínur](projects-how-record-job-usage.md#to-create-job-journal-lines-manually) og [Búa til marga sölureikninga verks](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices).</span><span class="sxs-lookup"><span data-stu-id="91398-125">For more information, see [Create job journal lines](projects-how-record-job-usage.md#to-create-job-journal-lines-manually) and [Create multiple job sales invoices](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices).</span></span>

## <a name="create-multiple-invoices-based-on-recurring-sales-lines"></a><span data-ttu-id="91398-126">Stofna marga reikninga byggða á endurteknum sölulínum</span><span class="sxs-lookup"><span data-stu-id="91398-126">Create multiple invoices based on recurring sales lines</span></span>

<span data-ttu-id="91398-127">Ef þú þarft oft að stofna innkaupa- og sölulínur með svipuðum upplýsingum, geturðu sett upp endurtekntar sölulínur, sem þú getur svo fært inn í ítrekuð sölu- og innkaupaskjöl, til dæmis fyrir endurteknar áfyllingapantanir.</span><span class="sxs-lookup"><span data-stu-id="91398-127">If you often need to create sales and purchase lines with similar information, you can set up recurring sales lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span> <span data-ttu-id="91398-128">Notaðu runuvinnsluna **Stofna ítrekaða sölureikninga** til að stofna sölureikninga samkvæmt endurteknum sölulínum sem eru tengdar við viðskiptamenn og með bókunardagsetningum innan gildir-frá og gildir-til dagsetningum sem hafa verið tilgreindar í endurteknum sölulínum.</span><span class="sxs-lookup"><span data-stu-id="91398-128">Use the **Create Recurring Sales Invoices** batch job to create sales invoices according to recurring sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the recurring sales lines.</span></span>  

### <a name="why-use-this-option"></a><span data-ttu-id="91398-129">Af hverju að nota þennan möguleika</span><span class="sxs-lookup"><span data-stu-id="91398-129">Why use this option</span></span>

<span data-ttu-id="91398-130">Með þessum valkosti er hægt að úthluta sömu ítrekunarlínum á marga viðskiptamenn.</span><span class="sxs-lookup"><span data-stu-id="91398-130">With this option, you can assign the same recurring lines to multiple customers.</span></span> <span data-ttu-id="91398-131">Hægt er að skilgreina gildistímabil fyrir endurteknar sölulínur tiltekins viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="91398-131">You can define period of validity for the recurring sales lines for specific customer.</span></span> <span data-ttu-id="91398-132">Hægt er að úthluta mörgum ítrekunarlínum á sama viðskiptavin og allir þeirra verða teknir með í reikningunum.</span><span class="sxs-lookup"><span data-stu-id="91398-132">You can assign multiple recurring lines to the same customer and all of them will be included in the invoice.</span></span>

<span data-ttu-id="91398-133">Hins vegar er engin leið til að setja fast verð fyrir vörur vegna þess að [!INCLUDE[d365fin](includes/d365fin_md.md)] notar raunverulegt verð og afslátt á dagsetningu skjals, og reynir að finna bestu samsetningu sem gefur lægsta verðið.</span><span class="sxs-lookup"><span data-stu-id="91398-133">However, there is no way to set fixed prices for items because [!INCLUDE[d365fin](includes/d365fin_md.md)] will use the actual prices and discount valid on document date, trying to find best combination that gives the lowest price.</span></span>  

<span data-ttu-id="91398-134">Nánari upplýsingar er að finna í [Stofna ítrekaðar sölu og innkaupalínur](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="91398-134">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>

## <a name="recurring-invoices-with-service-contract"></a><span data-ttu-id="91398-135">Endurteknir reikningar með þjónustusamning</span><span class="sxs-lookup"><span data-stu-id="91398-135">Recurring invoices with service contract</span></span>

<span data-ttu-id="91398-136">Þjónustusamningur inniheldur samkomulag viðskiptamanna og fyrirtækisins um þjónustusamning.</span><span class="sxs-lookup"><span data-stu-id="91398-136">A service contract contains the service contract agreements between your customers and your company.</span></span> <span data-ttu-id="91398-137">Í þjónustusamningi er samkomulag um þjónustustig og þjónustuvörurnar sem þjónustaðar eru samkvæmt samningnum.</span><span class="sxs-lookup"><span data-stu-id="91398-137">A service contract includes service level agreements and the service items that you service as a part of the contract.</span></span>  

<span data-ttu-id="91398-138">Hægt er að skilgreina upphafsdagsetningu samningsins, reikningstímabilsins, hvort samningurinn er fyrirframgreiddur og verðuuppfærslum ef þú ætlar að breyta verði þegar samningurinn er virkur.</span><span class="sxs-lookup"><span data-stu-id="91398-138">You can define the starting date of the contract, the invoice period, whether or not the contract is prepaid, price update specifications if you plan to change prices while contract is active.</span></span> <span data-ttu-id="91398-139">Hægt er að nota bæði þjónustuvörur eða vörur í þjónustusamningslínum.</span><span class="sxs-lookup"><span data-stu-id="91398-139">You can use both service items or items in service contract lines.</span></span>
<span data-ttu-id="91398-140">Hægt er að  stofna samningssniðmát til að skilgreina hvernig eigi að stofna ákveðnar tegundir samninga.</span><span class="sxs-lookup"><span data-stu-id="91398-140">You can create contract templates to define how to create certain types of contracts.</span></span>  

### <a name="why-use-this-option"></a><span data-ttu-id="91398-141">Af hverju að nota þennan möguleika</span><span class="sxs-lookup"><span data-stu-id="91398-141">Why use this option</span></span>

<span data-ttu-id="91398-142">Með þessum valkosti er notaður hluti af virkni ítarlegrar þjónustustýringar sem takmarkast ekki við útgáfu af endurteknum reikningum heldur styður viðgerðir og vettvangsaðferðir.</span><span class="sxs-lookup"><span data-stu-id="91398-142">With this option, you use a part of the advanced service management functionality that not limited to issuing of recurring invoices but support repair shop and field service operations.</span></span>

<span data-ttu-id="91398-143">Þessi valkostur krefst hins vegar Premium-leyfis.</span><span class="sxs-lookup"><span data-stu-id="91398-143">However, this option requires the Premium license.</span></span> <span data-ttu-id="91398-144">Uppsetning þjónustustjórnunar og viðhald þess skilar e.t.v. ekki miklum ávinningi í einfaldari áskriftaraðstæðum.</span><span class="sxs-lookup"><span data-stu-id="91398-144">Setting up service management and maintaining it might not give huge advantages in simpler subscription scenarios.</span></span>  

<span data-ttu-id="91398-145">Frekari upplýsingar, sjá [Vinna með þjónustusamninga og þjónustusamningstilboð](service-how-to-create-service-contracts-and-service-contract-quotes.md) og [Rukka nokkra þjónustusamninga](service-how-create-invoices.md#to-invoice-several-service-contracts).</span><span class="sxs-lookup"><span data-stu-id="91398-145">For more information, see [Work with Service Contracts and Service Contract Quotes](service-how-to-create-service-contracts-and-service-contract-quotes.md) and [Invoice several service contracts](service-how-create-invoices.md#to-invoice-several-service-contracts).</span></span>

## <a name="related-features"></a><span data-ttu-id="91398-146">Tengdir eiginleikar</span><span class="sxs-lookup"><span data-stu-id="91398-146">Related features</span></span>
<span data-ttu-id="91398-147">Nokkrir tengdir eiginleikar eru í [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="91398-147">There are several related capabilities in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

### <a name="blanket-sales-orders"></a><span data-ttu-id="91398-148">Standandi sölupantanir</span><span class="sxs-lookup"><span data-stu-id="91398-148">Blanket sales orders</span></span>

<span data-ttu-id="91398-149">Standandi sölupöntun er rammi fyrir langtímasamning milli fyrirtækisins þíns og viðskiptavinarins þíns.</span><span class="sxs-lookup"><span data-stu-id="91398-149">A blanket sales order represents a framework for a long-term agreement between your company and your customer.</span></span>
<span data-ttu-id="91398-150">Standandi pöntun er yfirleitt stofnuð þegar viðskiptamaður hefur skuldbundið sig til kaupa á miklu magni sem afhenda á í nokkrum minni afhendingum á ákveðnu tímabili.</span><span class="sxs-lookup"><span data-stu-id="91398-150">A blanket order is typically made when a customer has committed to purchasing large quantities that are to be delivered in several smaller shipments over a certain period of time.</span></span> <span data-ttu-id="91398-151">Standandi pantanir ná oft eingöngu yfir eina vöru með fyrirframákveðnum afhendingardögum.</span><span class="sxs-lookup"><span data-stu-id="91398-151">Often blanket orders cover only one item with predetermined delivery dates.</span></span> <span data-ttu-id="91398-152">Aðalástæðan fyrir notkun standandi pantana í stað sölupantana er sú að magn sem tilgreint er á standandi pöntun hafa ekki áhrif á framboð vöru, en hægt er að nota það í áætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="91398-152">The main reason for using a blanket order rather than a sales order is that quantities entered on a blanket order do not affect item availability, however it can be used for planning purposes.</span></span>

#### <a name="why-use-this-option"></a><span data-ttu-id="91398-153">Af hverju að nota þennan möguleika</span><span class="sxs-lookup"><span data-stu-id="91398-153">Why use this option</span></span>

<span data-ttu-id="91398-154">Með þessum valkosti er hægt að nota áætlaða eftirspurn þannig að upplýsingarnar standist eðlilegar áætlunarvenjur.</span><span class="sxs-lookup"><span data-stu-id="91398-154">With this option, you use the anticipated demand, so the information is considered during the normal planning routines.</span></span> <span data-ttu-id="91398-155">Frekari upplýsingar er að finna í [Eftirspurnarspá og standandi pantanir](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders).</span><span class="sxs-lookup"><span data-stu-id="91398-155">For more information, see [Demand Forecasts and Blanket Orders](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders).</span></span>  

<span data-ttu-id="91398-156">Sjálfgefin útgáfa býður hins vegar ekki upp á þann möguleika að vinna úr mörgum standandi pöntunum í fjöldahjálparglugga án breytinga.</span><span class="sxs-lookup"><span data-stu-id="91398-156">However, the default version does not offer an out-of-the-box possibility to process multiple blanket orders in bulk.</span></span>

<span data-ttu-id="91398-157">Nánari upplýsingar eru í [Vinna með standandi sölupantanir](sales-how-to-create-blanket-sales-orders.md).</span><span class="sxs-lookup"><span data-stu-id="91398-157">For more information, see [Work with Blanket Sales Orders](sales-how-to-create-blanket-sales-orders.md).</span></span>

### <a name="recurring-orders-norway"></a><span data-ttu-id="91398-158">Endurteknar pantanir (Noregur)</span><span class="sxs-lookup"><span data-stu-id="91398-158">Recurring Orders (Norway)</span></span>

<span data-ttu-id="91398-159">Hægt er að nota endurteknar pantanir til að stofna standandi pöntunarsniðmát þannig að hægt sé að stofna sölupantanir út frá dagsetningabilum sem eru skilgreind.</span><span class="sxs-lookup"><span data-stu-id="91398-159">You can use recurring orders to create blanket order templates so that sales orders can be created based on date intervals that you define.</span></span> <span data-ttu-id="91398-160">Ef sama sölupöntun er t.d. afhent á tveggja vikna fresti er hægt að nota standandi sölupöntun og stofna endurteknar pantanir.</span><span class="sxs-lookup"><span data-stu-id="91398-160">For example, if you deliver the same sales order every two weeks, you can use a blanket sales order and create recurring orders.</span></span>
<span data-ttu-id="91398-161">Hægt er að nota endurtekna flokka til að skilgreina svið færibreytna sem sýna hvernig pantanir eru gerðar.</span><span class="sxs-lookup"><span data-stu-id="91398-161">You can use recurring groups to define a range of parameters that show how you make the orders.</span></span> <span data-ttu-id="91398-162">Þessum flokkum er úthlutað á standandi pantanir sem þarf að stofna reglulega.</span><span class="sxs-lookup"><span data-stu-id="91398-162">These groups are assigned to blanket orders that have to be created regularly.</span></span> <span data-ttu-id="91398-163">Til að búa til endurteknar pantanir þarf reglulega að keyra ferli til að stofna endurteknar pantanir.</span><span class="sxs-lookup"><span data-stu-id="91398-163">To create the recurring orders, you will have to periodically run the create recurring orders process.</span></span> 

#### <a name="why-use-this-option"></a><span data-ttu-id="91398-164">Af hverju að nota þennan möguleika</span><span class="sxs-lookup"><span data-stu-id="91398-164">Why use this option</span></span>

<span data-ttu-id="91398-165">Með þessum valkosti er hægt að velja á milli fastra verða og „bestu“ verða.</span><span class="sxs-lookup"><span data-stu-id="91398-165">With this option, you can choose between fixed and "best" prices.</span></span>

<span data-ttu-id="91398-166">Þetta er hins vegar aðeins í boði í Noregi.</span><span class="sxs-lookup"><span data-stu-id="91398-166">However, this is only available in Norway.</span></span> <span data-ttu-id="91398-167">Hægt er að skilgreina gildistímabil á ítrekunarflokksstigi.</span><span class="sxs-lookup"><span data-stu-id="91398-167">Validity period can be defined on the recurring group level.</span></span>

<span data-ttu-id="91398-168">Nánari upplýsingar eru í [Endurteknar pantanir (Noregur)](/localfunctionality/norway/recurring-orders.md).</span><span class="sxs-lookup"><span data-stu-id="91398-168">For more information, see [Recurring Orders (Norway)](/localfunctionality/norway/recurring-orders.md).</span></span>

### <a name="recurring-revenue-and-subscription-billing-by-other-providers"></a><span data-ttu-id="91398-169">Endurteknar tekjur og áskriftarreikningar frá öðrum veitum</span><span class="sxs-lookup"><span data-stu-id="91398-169">Recurring revenue and subscription billing by other providers</span></span>

<span data-ttu-id="91398-170">Á [AppSource.microsoft.com](https://appsource.microsoft.com/), er hægt að fá viðbætur fyrir Business Central.</span><span class="sxs-lookup"><span data-stu-id="91398-170">At [AppSource.microsoft.com](https://appsource.microsoft.com/), you can get extensions for Business Central.</span></span> <span data-ttu-id="91398-171">Sumar viðbætur eru veittar af Microsoft, og aðrar viðbætur eru veittar af öðrum fyrirtækjum.</span><span class="sxs-lookup"><span data-stu-id="91398-171">Some extensions are provided by Microsoft, and other extensions are provided by other companies.</span></span> <span data-ttu-id="91398-172">Listi yfir viðbætur frá öðrum fyrirtækjum lengist í hverjum mánuði.</span><span class="sxs-lookup"><span data-stu-id="91398-172">The list of the extensions by other companies grows each month.</span></span> <span data-ttu-id="91398-173">Fylgstu því með á [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1) og fáðu forrit sem aðstoða þig í vinnunni í Business Central.</span><span class="sxs-lookup"><span data-stu-id="91398-173">So keep an eye out for [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1) and get apps to help you in your work in Business Central.</span></span>  

## <a name="see-also"></a><span data-ttu-id="91398-174">Sjá einnig .</span><span class="sxs-lookup"><span data-stu-id="91398-174">See also</span></span>

[<span data-ttu-id="91398-175">Dagsetningarreiknireglur</span><span class="sxs-lookup"><span data-stu-id="91398-175">Date Formulas</span></span>](ui-enter-date-ranges.md#using-date-formulas)  
[<span data-ttu-id="91398-176">Vinna með Ítrekunarbækur</span><span class="sxs-lookup"><span data-stu-id="91398-176">Working with Recurring Journals</span></span>](ui-work-general-journals.md#working-with-recurring-journals)  
[<span data-ttu-id="91398-177">Stofna færslubókarlínur verks</span><span class="sxs-lookup"><span data-stu-id="91398-177">Create job journal lines</span></span>](projects-how-record-job-usage.md#to-create-job-journal-lines-manually)  
[<span data-ttu-id="91398-178">Búa til marga sölureikninga verks</span><span class="sxs-lookup"><span data-stu-id="91398-178">Create multiple job sales invoices</span></span>](projects-how-invoice-jobs.md#to-create-multiple-job-sales-invoices)  
[<span data-ttu-id="91398-179">Stofna ítrekaðar sölu- og innkaupalínur</span><span class="sxs-lookup"><span data-stu-id="91398-179">Create Recurring Sales and Purchase Lines</span></span>](sales-how-work-standard-lines.md)  
[<span data-ttu-id="91398-180">Vinna með þjónustusamninga og þjónustusamningstilboð</span><span class="sxs-lookup"><span data-stu-id="91398-180">Work with Service Contracts and Service Contract Quotes</span></span>](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[<span data-ttu-id="91398-181">Reikningsfæra nokkra þjónustusamninga</span><span class="sxs-lookup"><span data-stu-id="91398-181">Invoice several service contracts</span></span>](service-how-create-invoices.md#to-invoice-several-service-contracts)  
[<span data-ttu-id="91398-182">Eftirspurnarspá og standandi pantanir</span><span class="sxs-lookup"><span data-stu-id="91398-182">Demand Forecasts and Blanket Orders</span></span>](design-details-central-concepts-of-the-planning-system.md#demand-forecasts-and-blanket-orders)  
[<span data-ttu-id="91398-183">Vinna með standandi sölupantanir</span><span class="sxs-lookup"><span data-stu-id="91398-183">Work with Blanket Sales Orders</span></span>](sales-how-to-create-blanket-sales-orders.md)  
[<span data-ttu-id="91398-184">Endurteknar pantanir (Noregur)</span><span class="sxs-lookup"><span data-stu-id="91398-184">Recurring Orders (Norway)</span></span>](/localfunctionality/norway/recurring-orders.md)  