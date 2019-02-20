---
title: "Uppfæra gengi gjaldmiðils| Microsoft Docs"
description: "Til að nota marga gjaldmiðla í rekstri, er hægt að setja upp kóða fyrir hvern gjaldmiðil og nota utanaðkomandi gjaldeyrisgengisþjónustu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 12/19/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa1e7b13cf6cc56df1a6922a9b123e7cc19580c6
ms.openlocfilehash: 7fafae0cba12ba985de2faa795b434d4c670a8ca
ms.contentlocale: is-is
ms.lasthandoff: 12/19/2018

---
# <a name="update-currency-exchange-rates"></a><span data-ttu-id="08afb-103">Uppfæra gengi</span><span class="sxs-lookup"><span data-stu-id="08afb-103">Update Currency Exchange Rates</span></span>
<span data-ttu-id="08afb-104">Þar sem fyrirtæki starfa að auknum mæli í fleiri löndum/svæðum verður æ mikilvægara fyrir þau að geta átt viðskipti og skráð fjárhag sinn í fleiri en einum gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="08afb-104">As companies operate in increasingly more countries/regions, it becomes more important that they be able to trade and report financials in more than one currency.</span></span> <span data-ttu-id="08afb-105">Setja þarf upp kóða fyrir hvern gjaldmiðil sem notaður er ef keypt er eða selt í öðrum gjaldmiðlum en staðbundinn gjaldmiðill, ef eitthvað er útistandandi eða gjaldfallið í öðrum gjaldmiðlum, eða ef fjárhagsfærslur eru skráðar í mismunandi gjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="08afb-105">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>

<span data-ttu-id="08afb-106">Fjárhagurinn þinn er settur upp til að nota staðbundna gjaldmiðilinn (SGM), en þú getur sett hann upp til að einnig nota annan gjaldmiðil með rétt gengi stillt.</span><span class="sxs-lookup"><span data-stu-id="08afb-106">Your general ledger is set up to use your local currency (LCY), but you can set it up to also use another currency with a current exchange rate assigned.</span></span> <span data-ttu-id="08afb-107">Sé öðrum gjaldmiðli gefin svokölluð skilgreining Viðbótarskýrslugjaldmiðill mun [!INCLUDE[d365fin](includes/d365fin_md.md)] skrá upphæðirnar sjálfkrafa bæði í SGM og þessum viðbótarskýrslugjaldmiðli í hverri fjárhagsfærslu og í öðrum færslum á borð við færslur fyrir VSK.</span><span class="sxs-lookup"><span data-stu-id="08afb-107">By designating a second currency as a so-called additional reporting currency, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically record amounts in both LCY and this additional reporting currency on each G/L entry and other entries, such as VAT entries.</span></span> <span data-ttu-id="08afb-108">Nánari upplýsingar er að finna í [Setja upp annan skýrslugjaldmiðil](finance-how-setup-additional-currencies.md).</span><span class="sxs-lookup"><span data-stu-id="08afb-108">For more information, see [Set Up an Additional Reporting Currency](finance-how-setup-additional-currencies.md).</span></span>

## <a name="adjusting-exchange-rates"></a><span data-ttu-id="08afb-109">Gengi leiðrétt</span><span class="sxs-lookup"><span data-stu-id="08afb-109">Adjusting Exchange Rates</span></span>
<span data-ttu-id="08afb-110">Vegna þess hve tíðar gengisbreytingar eru verður reglubundið að leiðrétta aðra jafngildisgjaldmiðla í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="08afb-110">Because exchange rates fluctuate constantly, additional currency equivalents in your system must be adjusted periodically.</span></span> <span data-ttu-id="08afb-111">Sé það ekki gert verða upphæðir misvísandi sem hafa verið umreiknaðar úr erlendum (eða aukalegum) gjaldmiðlum og bókaðar í fjárhag í SGM.</span><span class="sxs-lookup"><span data-stu-id="08afb-111">If these adjustments are not done, amounts that have been converted from foreign (or additional) currencies and posted to the general ledger in LCY may be misleading.</span></span> <span data-ttu-id="08afb-112">Að auki verður að uppfæra daglegar færslur sem eru bókaðar áður en daglegt gengi er fært inn eftir að upplýsingarnar um daglegt gengi hafa verið færðar inn.</span><span class="sxs-lookup"><span data-stu-id="08afb-112">In addition, daily entries posted before a daily exchange rate is entered into the program must be updated after the daily exchange rate information is entered.</span></span> <span data-ttu-id="08afb-113">Keyrslan Stilla gengi er notuð til að lagfæra gengi bókaðs viðskiptamanns, lánardrottins og bankareikningsfærslna.</span><span class="sxs-lookup"><span data-stu-id="08afb-113">The Adjust Exchange Rates batch job is used to adjust the exchange rates of posted customer, vendor and bank account entries.</span></span> <span data-ttu-id="08afb-114">Hún getur einnig uppfært upphæðir annars skýrslugjaldmiðils í fjárhagsfærslum.</span><span class="sxs-lookup"><span data-stu-id="08afb-114">It can also update additional reporting currency amounts on G/L entries.</span></span>

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="08afb-115">Setja upp þjónustu um gengi gjaldmiðils</span><span class="sxs-lookup"><span data-stu-id="08afb-115">To set up a currency exchange rate service</span></span>
<span data-ttu-id="08afb-116">Þú getur notað ytri þjónustu til að halda gjaldeyrisviðskiptum þínum uppfærðum, t.d. FloatRates.</span><span class="sxs-lookup"><span data-stu-id="08afb-116">You can use an external service to keep your currency exchange rates up to date, such as FloatRates.</span></span>

1. <span data-ttu-id="08afb-117">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Þjónusta um gengi gjaldmiðils** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="08afb-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="08afb-118">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="08afb-118">Choose the **New** action.</span></span>
3. <span data-ttu-id="08afb-119">Fylltu í reitina eftir því sem nauðsyn krefur á síðunni **Þjónusta fyrir gengi gjaldmiðils**.</span><span class="sxs-lookup"><span data-stu-id="08afb-119">On the **Currency Exchange Rate Service** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="08afb-120">Veldu reitinn **Virkt** til að virkja þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="08afb-120">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="08afb-121">Til að uppfæra gengi í gegnum þjónustu</span><span class="sxs-lookup"><span data-stu-id="08afb-121">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="08afb-122">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Gjaldmiðlar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="08afb-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="08afb-123">Veldu aðgerðina **Uppfæra gengi**.</span><span class="sxs-lookup"><span data-stu-id="08afb-123">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="08afb-124">Gildið í **Gengi** reitnum á síðunni **Gjaldmiðlar** er uppfært með nýjustu gengi gjaldmiðilsins.</span><span class="sxs-lookup"><span data-stu-id="08afb-124">The value in the **Exchange Rate** field on the **Currencies** page is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="08afb-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="08afb-125">See Also</span></span>
[<span data-ttu-id="08afb-126">Setja upp annan skýrslugjaldmiðil</span><span class="sxs-lookup"><span data-stu-id="08afb-126">Set Up an Additional Reporting Currency</span></span>](finance-how-setup-additional-currencies.md)  
[<span data-ttu-id="08afb-127">Lokaár og Tímabil</span><span class="sxs-lookup"><span data-stu-id="08afb-127">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="08afb-128">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="08afb-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

