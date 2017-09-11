---
title: "Uppfæra gengi gjaldmiðils| Microsoft Docs"
description: "Til að nota mismunandi gjaldmiðla í rekstri, er hægt að setja upp kóða fyrir hvern gjaldmiðil og nota utanaðkomandi gjaldeyrisgengisþjónustu, eins og t.d. Yahoo."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: cc60569091b3aa37d17e981f1fae8f46c4a004df
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-update-currency-exchange-rates"></a><span data-ttu-id="edf3b-103">Hvernig á að: Uppfæra gengi</span><span class="sxs-lookup"><span data-stu-id="edf3b-103">How to: Update Currency Exchange Rates</span></span>
<span data-ttu-id="edf3b-104">Setja þarf upp kóða fyrir hvern gjaldmiðil sem notaður er ef keypt er eða selt í öðrum gjaldmiðlum en staðbundinn gjaldmiðill, ef eitthvað er útistandandi eða gjaldfallið í öðrum gjaldmiðlum, eða ef fjárhagsfærslur eru skráðar í mismunandi gjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="edf3b-104">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="edf3b-105">Þessi virkni krefst þess að upplifun þín sé stillt á **Pakki**.</span><span class="sxs-lookup"><span data-stu-id="edf3b-105">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="edf3b-106">Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="edf3b-106">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

<span data-ttu-id="edf3b-107">Þú getur notað ytri þjónustu til að halda gjaldeyrisviðskiptum þínum upp til dags.</span><span class="sxs-lookup"><span data-stu-id="edf3b-107">You can use an external service to keep your currency exchange rates up to date.</span></span> <span data-ttu-id="edf3b-108">Yahoo gjaldeyrisgengi er fyrirfram og tilbúinn til að virkja.</span><span class="sxs-lookup"><span data-stu-id="edf3b-108">The Yahoo Currency Exchange Rates service is preinstalled and ready to enable.</span></span>

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="edf3b-109">Setja upp þjónustu um gengi gjaldmiðils</span><span class="sxs-lookup"><span data-stu-id="edf3b-109">To set up a currency exchange rate service</span></span>
1. <span data-ttu-id="edf3b-110">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Þjónusta um gengi gjaldmiðla** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="edf3b-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="edf3b-111">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="edf3b-111">Choose the **New** action.</span></span>
3. <span data-ttu-id="edf3b-112">Fylltu inn **Þjónusta um gengi gjaldmiðils** eftir því sem nauðsyn krefur.</span><span class="sxs-lookup"><span data-stu-id="edf3b-112">In the **Currency Exchange Rate Service** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="edf3b-113">Veldu reitinn **Virkt** til að virkja þjónustuna.</span><span class="sxs-lookup"><span data-stu-id="edf3b-113">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="edf3b-114">Til að uppfæra gengi í gegnum þjónustu</span><span class="sxs-lookup"><span data-stu-id="edf3b-114">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="edf3b-115">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Gjaldmiðlar** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="edf3b-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="edf3b-116">Veldu aðgerðina **Uppfæra gengi**.</span><span class="sxs-lookup"><span data-stu-id="edf3b-116">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="edf3b-117">Gildið í **Gengi** reitnum í **Gjaldmiðlar** er uppfærður með nýjustu gengi gjaldmiðilsins.</span><span class="sxs-lookup"><span data-stu-id="edf3b-117">The value in the **Exchange Rate** field in the **Currencies** window is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="edf3b-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="edf3b-118">See Also</span></span>
[<span data-ttu-id="edf3b-119">Lokaár og Tímabil</span><span class="sxs-lookup"><span data-stu-id="edf3b-119">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="edf3b-120">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="edf3b-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

