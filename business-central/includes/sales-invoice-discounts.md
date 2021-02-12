---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035787"
---
<span data-ttu-id="d8a02-101">Þegar allar vörur hafa verið færðar í sölupöntunarlínurnar er hægt að reikna reikningsafslátt af öllu söluskjalinu með því að velja aðgerðina **Reikna reikningsafsl**.</span><span class="sxs-lookup"><span data-stu-id="d8a02-101">When all the items have been entered on the sales order lines, you can calculate the invoice discount for the entire sales document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="d8a02-102">Ef reiturinn **Reikna reikn.afsl.** er valinn í glugganum **Sölugrunnur** þá er reikningsafslátturinn reiknaður sjálfkrafa þegar þú gerir annað af eftirfarandi á söluskjali:</span><span class="sxs-lookup"><span data-stu-id="d8a02-102">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** window, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>

* <span data-ttu-id="d8a02-103">Skoða tölfræði</span><span class="sxs-lookup"><span data-stu-id="d8a02-103">View statistics</span></span>
* <span data-ttu-id="d8a02-104">Skoða prufuskýrslu</span><span class="sxs-lookup"><span data-stu-id="d8a02-104">View a test report</span></span>
* <span data-ttu-id="d8a02-105">Prenta</span><span class="sxs-lookup"><span data-stu-id="d8a02-105">Print</span></span>
* <span data-ttu-id="d8a02-106">Færsla</span><span class="sxs-lookup"><span data-stu-id="d8a02-106">Post</span></span>

<span data-ttu-id="d8a02-107">Afslættinum er jafnað niður á allar línur í söluskjalinu fyrir vörur þar sem **Já** er í reitnum **Reikna reikningsafsl.**</span><span class="sxs-lookup"><span data-stu-id="d8a02-107">The discount is apportioned over all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="d8a02-108">Þetta er sjálfgefin stilling fyrir vörur.</span><span class="sxs-lookup"><span data-stu-id="d8a02-108">This is the default setting for items.</span></span>

<span data-ttu-id="d8a02-109">Reikningsafsláttarskilmálar eru skilgreindir á síðunni **Reikningsafsl. viðskm.** til að reikna út reikningsafsláttinn.</span><span class="sxs-lookup"><span data-stu-id="d8a02-109">The invoice discount terms are defined in the **Cust. Invoice Discounts** page to calculate the invoice discount.</span></span> <span data-ttu-id="d8a02-110">Kerfið notar gjaldmiðilskóðann í sölureikningnum til að finna skilmála reikningsafsláttar í samsvarandi gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="d8a02-110">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="d8a02-111">Ef reikningsafsláttur hefur ekki verið skilgreindur í erlendum gjaldeyri þá eru notaðir skilmálar reikningsafsláttarsem skilgreindir eru í töflunni **Reikningsafsl. viðskm** síðunni með upphæðir í staðbundnum gjaldmiðli og gengi á bókunardegi söluskjalsins er notað til að reikna reikningsafsláttinn í erlendum gjaldeyri.</span><span class="sxs-lookup"><span data-stu-id="d8a02-111">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
