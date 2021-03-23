---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 539ee2eb2c9e4a71eacfb78d95320870128fb1d9
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470288"
---
<span data-ttu-id="f8114-101">Þegar allar vörur hafa verið færðar í sölulínurnar er hægt að reikna reikningsafslátt af öllu skjalinu með því að velja aðgerðina **Reikna reikningsafsl**.</span><span class="sxs-lookup"><span data-stu-id="f8114-101">When all the items have been entered on the sales lines, you can calculate the invoice discount for the entire document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="f8114-102">Afslátturinn er reiknaður byggt á öllum línum í söluskjalinu fyrir vörur þar sem **Já** er í reitnum **Reikna reikningsafslátt**.</span><span class="sxs-lookup"><span data-stu-id="f8114-102">The discount is calculated based on all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="f8114-103">Þetta er sjálfgefin stilling fyrir vörur.</span><span class="sxs-lookup"><span data-stu-id="f8114-103">This is the default setting for items.</span></span> <span data-ttu-id="f8114-104">Línur með kostnaðarauka eru til dæmis ekki teknar með í útreikningi reikningsafsláttar.</span><span class="sxs-lookup"><span data-stu-id="f8114-104">Lines with item charges, for example, are not included in the calculation of the invoice discount.</span></span> <span data-ttu-id="f8114-105">Ef nota á afslátt á slíkar línur verður að stilla reitinn **Línuafsláttur %** í línunni sem á við.</span><span class="sxs-lookup"><span data-stu-id="f8114-105">If you want to apply a discount to such lines, you must set the **Line Discount %** field on the relevant lines.</span></span>  

> [!TIP]
> <span data-ttu-id="f8114-106">Ef reiturinn **Reikna reikn.afsl.** er valinn á síðunni **Sölugrunnur** þá er reikningsafslátturinn reiknaður sjálfkrafa þegar þú gerir annað af eftirfarandi á söluskjali:</span><span class="sxs-lookup"><span data-stu-id="f8114-106">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** page, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>
>
> * <span data-ttu-id="f8114-107">Skoða tölfræði</span><span class="sxs-lookup"><span data-stu-id="f8114-107">View statistics</span></span>
> * <span data-ttu-id="f8114-108">Skoða prufuskýrslu</span><span class="sxs-lookup"><span data-stu-id="f8114-108">View a test report</span></span>
> * <span data-ttu-id="f8114-109">Prenta</span><span class="sxs-lookup"><span data-stu-id="f8114-109">Print</span></span>
> * <span data-ttu-id="f8114-110">Færsla</span><span class="sxs-lookup"><span data-stu-id="f8114-110">Post</span></span>

<span data-ttu-id="f8114-111">Reikningsafsláttarskilmálar fyrir viðskiptamann eru skilgreindir á síðunni **Reikningsafsl. viðskm.** fyrir viðskiptamanninn.</span><span class="sxs-lookup"><span data-stu-id="f8114-111">The invoice discount terms for a customer are defined in the **Cust. Invoice Discounts** page for the customer.</span></span> <span data-ttu-id="f8114-112">Kerfið notar gjaldmiðilskóðann í sölureikningnum til að finna skilmála reikningsafsláttar í samsvarandi gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="f8114-112">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="f8114-113">Ef reikningsafsláttur hefur ekki verið skilgreindur í erlendum gjaldeyri þá eru notaðir skilmálar reikningsafsláttarsem skilgreindir eru í töflunni **Reikningsafsl. viðskm** síðunni með upphæðir í staðbundnum gjaldmiðli og gengi á bókunardegi söluskjalsins er notað til að reikna reikningsafsláttinn í erlendum gjaldeyri.</span><span class="sxs-lookup"><span data-stu-id="f8114-113">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
