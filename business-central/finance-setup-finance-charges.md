---
title: Setja upp vaxtaskilmála
description: Frekari upplýsingar um uppsetningu Business Central þannig að hægt sé að upplýsa viðskiptavini um viðbótargjöld með því að senda vaxtareikninga.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 08a2443f94efbc9920145109b4b7499a3a4e05b3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783623"
---
# <a name="set-up-finance-charge-terms"></a><span data-ttu-id="2685e-103">Setja upp vaxtaskilmála</span><span class="sxs-lookup"><span data-stu-id="2685e-103">Set Up Finance Charge Terms</span></span>

<span data-ttu-id="2685e-104">Þegar viðskiptamaður greiðir ekki á gjalddaga er hægt að láta reikna út vexti sjálfvirkt og bæta þeim við gjaldföllnu upphæðina á reikningi viðskiptamannsins.</span><span class="sxs-lookup"><span data-stu-id="2685e-104">When a customer does not pay by the due date, you can have finance charges calculated automatically and add them to the overdue amounts on the customer's account.</span></span> <span data-ttu-id="2685e-105">Hægt er að láta viðskiptamenn vita af viðbótargjöldunum með því að senda vaxtareikninga.</span><span class="sxs-lookup"><span data-stu-id="2685e-105">You can inform customers of the added charges by sending finance charge memos.</span></span> <span data-ttu-id="2685e-106">Fyrst verður að setja upp kóða fyrir hvern vaxtaútreikning.</span><span class="sxs-lookup"><span data-stu-id="2685e-106">But first, you must set up a code that represents each finance charge calculation.</span></span> <span data-ttu-id="2685e-107">Síðan er hægt að færa þennan kóða inn í reitinn Kóði skilmála innheimtubréfa á viðskiptavinaspjöldum.</span><span class="sxs-lookup"><span data-stu-id="2685e-107">Then you can enter this code in the Fin. Charge Terms Code field on customer cards.</span></span>  

## <a name="finance-charge-terms"></a><span data-ttu-id="2685e-108">Vaxtaskilmálar</span><span class="sxs-lookup"><span data-stu-id="2685e-108">Finance charge terms</span></span>

<span data-ttu-id="2685e-109">Nauðsynlegt er að setja upp vaxtaskilmála fyrir hvern vaxtaútreikning og úthluta svo skilmálunum til viðskiptamannsins í reitnum **Vaxtaskilmálakóði** á síðunni **Viðskiptavinur**.</span><span class="sxs-lookup"><span data-stu-id="2685e-109">You must set up finance charge terms for each finance charge calculation, and then assign the terms to the customer in the **Fin. Charge Terms Code** field on the **Customer** page.</span></span>

<span data-ttu-id="2685e-110">Hægt er að reikna vexti með því að nota annaðhvort regluna um meðaltal daglegs jafnaðar eða reglur um gjaldfallna stöðu.</span><span class="sxs-lookup"><span data-stu-id="2685e-110">Finance charges can be calculated using either the average daily balance or the balance due methods.</span></span>

* <span data-ttu-id="2685e-111">Dagleg meðaltalsstaða</span><span class="sxs-lookup"><span data-stu-id="2685e-111">Average daily balance</span></span>  
  
  <span data-ttu-id="2685e-112">Fjöldi daga sem greiðslan er komin fram yfir gjalddaga er tekin með í reikninginn:</span><span class="sxs-lookup"><span data-stu-id="2685e-112">The number of days the payment is overdue is taken into account:</span></span>  
  <span data-ttu-id="2685e-113">*Regla um daglega meðaltalsstöðu* - *Vaxtareikningur* = *Gjaldfallin upphæð* x *(Fjöldi daga fram yfir gjalddaga / Vaxtatímabil)* x *(Vextir/100)*</span><span class="sxs-lookup"><span data-stu-id="2685e-113">*Average Daily Balance method* - *Finance Charge* = *Overdue Amount* x *(Days Overdue / Interest Period)* x *(Interest Rate/100)*</span></span>

* <span data-ttu-id="2685e-114">Gjaldfallin staða</span><span class="sxs-lookup"><span data-stu-id="2685e-114">Balance due</span></span>  
  
  <span data-ttu-id="2685e-115">Vaxtareikningurinn er prósentuhluti af gjaldföllnu upphæðinni:</span><span class="sxs-lookup"><span data-stu-id="2685e-115">The finance charge is a percentage of the overdue amount:</span></span>  
  <span data-ttu-id="2685e-116">*Regla fyrir gjaldfallna stöðu* - *Vaxtareikningur* = *Gjaldfallin upphæð* x *(Vextir / 100)*</span><span class="sxs-lookup"><span data-stu-id="2685e-116">*Balance Due method* - *Finance Charge* = *Overdue Amount* x *(Interest Rate / 100)*</span></span>

<span data-ttu-id="2685e-117">Að auki er sérhver skilgreining í töflunni Vaxtaskilmálar tengdur undirtöflunni Vaxtatexti.</span><span class="sxs-lookup"><span data-stu-id="2685e-117">Additionally, each term in the Finance Charge Terms table is linked to a subtable, the Finance Charge Text table.</span></span> <span data-ttu-id="2685e-118">Fyrir hvern vaxtagjalddaga er hægt að skilgreina byrjunar- og/eða lokatexta sem verður á vaxtareikningnum.</span><span class="sxs-lookup"><span data-stu-id="2685e-118">For each set of finance charge terms, you can define a beginning and/or an ending text to include on the finance charge memo.</span></span>

### <a name="to-set-up-finance-charge-terms"></a><span data-ttu-id="2685e-119">Setja upp vaxtaskilmála</span><span class="sxs-lookup"><span data-stu-id="2685e-119">To set up finance charge terms</span></span>

1. <span data-ttu-id="2685e-120">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vaxtaskilmálar** eða Lánardrottinn og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2685e-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2685e-121">Fyllið inn í reitina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="2685e-121">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="2685e-122">Eigi að nota fleiri en eina samsetningu vaxtaskilmálar þarf að setja upp kóta fyrir hverja þeirra.</span><span class="sxs-lookup"><span data-stu-id="2685e-122">To use more than one combination of finance charge terms, set up a code for each one.</span></span>

    <span data-ttu-id="2685e-123">Fyrir hvern vaxtaskilmála er hægt að skilgreina sérstök skilyrði sem í geta falist viðbótargjöld, bæði í SGM og erlendum gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="2685e-123">For each finance charge term, you can specify individual conditions that can include additional fees in both LCY and in foreign currency.</span></span> <span data-ttu-id="2685e-124">Hægt er að skilgreina viðbótargjöld í erlendum gjaldmiðlum fyrir hverja skilmála á síðunni **Vaxtaskilmálar**.</span><span class="sxs-lookup"><span data-stu-id="2685e-124">You can define additional fees in foreign currencies for each term on the **Finance Charge Terms** page.</span></span>
4. <span data-ttu-id="2685e-125">Velja aðgerðina **gjaldmiðlar**.</span><span class="sxs-lookup"><span data-stu-id="2685e-125">Choose the **Currencies** action.</span></span>
5. <span data-ttu-id="2685e-126">Á síðunni **Gjaldmiðlar fyrir vaxtaskilmála**, skal skilgreina gjaldmiðilskóða fyrir hvern skilmála og viðbótargjald.</span><span class="sxs-lookup"><span data-stu-id="2685e-126">On the **Currencies for Fin. Chrg. Terms** page, define for each term a currency code and an additional fee.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="2685e-127">Þegar vextir eru stofnaðir í erlendum gjaldmiðli tekur kerfið mið af þeim skilyrðum sem sett eru um erlendan gjaldmiðil hér til að stofna vaxtareikningur.</span><span class="sxs-lookup"><span data-stu-id="2685e-127">When you create finance charges in a foreign currency, the foreign currency conditions that you set up here will be used to create finance charge memos.</span></span> <span data-ttu-id="2685e-128">Ef engin vaxtaskilyrði fyrir erlenda gjaldmiðla eru sett upp notar kerfið SGM-vaxtaskilyrðin sem eru tilgreind á síðunni **Vaxtaskilmálar** og breytir þeim í viðeigandi gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="2685e-128">If there are no foreign currency finance charge conditions set up, the LCY finance charge conditions specified on the **Finance Charge Terms** page will be used and then converted to the relevant currency.</span></span>

    <span data-ttu-id="2685e-129">Fyrir hvern kóða vaxtaskilmála er hægt að tilgreina texta sem á að prenta á undan (**Byrjunartexti**) eða á eftir (**Endatexti**) færslunum á vaxtareikningnum.</span><span class="sxs-lookup"><span data-stu-id="2685e-129">For each finance charge term, you can specify text that will be printed before (**Beginning Text**) or after (**Ending Text**) on the entries on the finance charge memo.</span></span>  
6. <span data-ttu-id="2685e-130">Veljið **Byrjunartexti** eða **Lokatexti** aðgerðirnar eftir því sem við á, og fyllið út síðuna **Vaxtatexti**.</span><span class="sxs-lookup"><span data-stu-id="2685e-130">Choose the **Beginning Text** or **Ending Text** actions respectively, and fill on the **Finance Charge Text** page.</span></span>
7. <span data-ttu-id="2685e-131">Til að setja viðeigandi gildi sjálfvirkt inn í vaxtatexta, skal fara inn í eftirfarandi staðgengla í reitnum **Texti**.</span><span class="sxs-lookup"><span data-stu-id="2685e-131">To automatically insert related values in the resulting finance charge text, enter the following placeholders in the **Text** field.</span></span>

|<span data-ttu-id="2685e-132">Frátaka</span><span class="sxs-lookup"><span data-stu-id="2685e-132">Placeholder</span></span>|<span data-ttu-id="2685e-133">Gildi:</span><span class="sxs-lookup"><span data-stu-id="2685e-133">Value</span></span>|  
|-----------------|-----------|  
|<span data-ttu-id="2685e-134">%1</span><span class="sxs-lookup"><span data-stu-id="2685e-134">%1</span></span>|<span data-ttu-id="2685e-135">Innihald reitsins **Dagsetning skjals** á bréfshaus vaxtareiknings</span><span class="sxs-lookup"><span data-stu-id="2685e-135">Content of the **Document Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="2685e-136">%2</span><span class="sxs-lookup"><span data-stu-id="2685e-136">%2</span></span>|<span data-ttu-id="2685e-137">Innihald reitsins **gjalddagi** á bréfshaus vaxtareiknings</span><span class="sxs-lookup"><span data-stu-id="2685e-137">Content of the **Due Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="2685e-138">%3</span><span class="sxs-lookup"><span data-stu-id="2685e-138">%3</span></span>|<span data-ttu-id="2685e-139">Innihald reitsins **Vextir** í viðeigandi vaxtaskilmálum</span><span class="sxs-lookup"><span data-stu-id="2685e-139">Content of the **Interest Rate** field on the related finance charge terms</span></span>|  
|<span data-ttu-id="2685e-140">%4</span><span class="sxs-lookup"><span data-stu-id="2685e-140">%4</span></span>|<span data-ttu-id="2685e-141">Innihald reitsins **eftirstöðvar** á bréfshaus vaxtareiknings</span><span class="sxs-lookup"><span data-stu-id="2685e-141">Content of the **Remaining Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="2685e-142">%5</span><span class="sxs-lookup"><span data-stu-id="2685e-142">%5</span></span>|<span data-ttu-id="2685e-143">Innihald reitsins **vextir upphæð** á bréfshaus vaxtareiknings</span><span class="sxs-lookup"><span data-stu-id="2685e-143">Content of the **Interest Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="2685e-144">%6</span><span class="sxs-lookup"><span data-stu-id="2685e-144">%6</span></span>|<span data-ttu-id="2685e-145">Innihald reitsins **Viðbótargjald** á bréfshaus vaxtareiknings</span><span class="sxs-lookup"><span data-stu-id="2685e-145">Content of the **Additional Fee** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="2685e-146">%7</span><span class="sxs-lookup"><span data-stu-id="2685e-146">%7</span></span>|<span data-ttu-id="2685e-147">Heildarupphæð innheimtubréfsins</span><span class="sxs-lookup"><span data-stu-id="2685e-147">The total amount of the reminder</span></span>|  
|<span data-ttu-id="2685e-148">%8</span><span class="sxs-lookup"><span data-stu-id="2685e-148">%8</span></span>|<span data-ttu-id="2685e-149">Innihald reitsins **gjaldmiðilskóði** á bréfshaus vaxtareiknings</span><span class="sxs-lookup"><span data-stu-id="2685e-149">Content of the **Currency Code** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="2685e-150">%9</span><span class="sxs-lookup"><span data-stu-id="2685e-150">%9</span></span>|<span data-ttu-id="2685e-151">Innihald reitsins **bókunardagsetning** á bréfshaus vaxtareiknings</span><span class="sxs-lookup"><span data-stu-id="2685e-151">Content of the **Posting Date** field on the finance charge memo header</span></span>|  

## <a name="see-also"></a><span data-ttu-id="2685e-152">Sjá einnig .</span><span class="sxs-lookup"><span data-stu-id="2685e-152">See also</span></span>

[<span data-ttu-id="2685e-153">Innheimta útistandandi skuldir</span><span class="sxs-lookup"><span data-stu-id="2685e-153">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="2685e-154">Setja upp skilmála og stig innheimtubréfa</span><span class="sxs-lookup"><span data-stu-id="2685e-154">Set Up Reminder Terms and Levels</span></span>](finance-setup-reminders.md)  
[<span data-ttu-id="2685e-155">Uppsetning Fjármála</span><span class="sxs-lookup"><span data-stu-id="2685e-155">Setting Up Finance</span></span>](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]