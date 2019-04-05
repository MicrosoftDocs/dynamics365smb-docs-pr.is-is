---
title: Hvernig á að varpa skattstofunúmerum í bókhaldslykla
description: Fyrirtæki á Íslandi þurfa að senda gagnaskrá á fyrirfram tilgreindu formi til skattyfirvalda. Áður en hægt er að gera þetta þarf að varpa fyrirfram skilgreindum reikningskóða skattstofu (Internal Revenue Service) í fjárhagsreikning.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 20d64022281c9248313710709626ab50c150a003
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "826793"
---
# <a name="map-irs-numbers-to-chart-of-accounts"></a><span data-ttu-id="f6370-104">Varpa skattstofunúmerum í bókhaldslykla</span><span class="sxs-lookup"><span data-stu-id="f6370-104">Map IRS Numbers to Chart of Accounts</span></span>
<span data-ttu-id="f6370-105">Fyrirtæki á Íslandi þurfa að senda gagnaskrá á fyrirfram tilgreindu formi til skattyfirvalda.</span><span class="sxs-lookup"><span data-stu-id="f6370-105">Companies in Iceland are required to send the tax authority a data file in a predefined format.</span></span> <span data-ttu-id="f6370-106">Áður en hægt er að gera þetta þarf að varpa fyrirfram skilgreindum reikningskóða skattstofu (Internal Revenue Service) í fjárhagsreikning.</span><span class="sxs-lookup"><span data-stu-id="f6370-106">Before you can do this, you must map predefined Internal Revenue Service (IRS) account codes to general ledger accounts.</span></span>  

## <a name="to-create-an-internal-revenue-service-number"></a><span data-ttu-id="f6370-107">Til að stofna skattstofunúmer</span><span class="sxs-lookup"><span data-stu-id="f6370-107">To create an Internal Revenue Service number</span></span>  

1.  <span data-ttu-id="f6370-108">Velja skal ![Leit að síðu eða skýrslu](../../media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Skattstofunúmer** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="f6370-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **IRS Number**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f6370-109">Valið er **Nýtt** aðgerð.</span><span class="sxs-lookup"><span data-stu-id="f6370-109">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="f6370-110">Á nýju línunni skaltu slá inn númer í reitinn **Skattstofunúmer** og gefa upp heiti í reitinn **Nafn**.</span><span class="sxs-lookup"><span data-stu-id="f6370-110">On the new line, enter a number in the **IRS number** field, and provide a name in the **Name** field.</span></span>  
4.  <span data-ttu-id="f6370-111">Veldu gátreitinn **Öfugt forskeyti** ef neikvæðu forskeyti á að snúa við á stöðu fjárhagsreiknings sem skattstofunúmerið er varpað á.</span><span class="sxs-lookup"><span data-stu-id="f6370-111">Select the **Reverse Prefix** check box if you want the negative operator to be reversed on the balance of the general ledger account that the IRS number is mapped to.</span></span>  
5.  <span data-ttu-id="f6370-112">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f6370-112">Choose the **OK** button.</span></span>  

## <a name="to-map-an-irs-number-to-a-general-ledger-account"></a><span data-ttu-id="f6370-113">Til að varpa skattstofunúmeri í fjárhagsreikning</span><span class="sxs-lookup"><span data-stu-id="f6370-113">To map an IRS number to a general ledger account</span></span>  

1.  <span data-ttu-id="f6370-114">Velja skal ![Leit að síðu eða skýrslu](../../media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bókhaldslykill** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="f6370-114">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f6370-115">Veldu fjárhagsreikning sem er með **Tegund reiknings** af gerðinni **Bókun**.</span><span class="sxs-lookup"><span data-stu-id="f6370-115">Select a general ledger account that has an **Account Type** of **Posting**.</span></span>  
3.  <span data-ttu-id="f6370-116">Í reitnum **Skattstofunúmer** velurðu skattstofunúmer af listanum.</span><span class="sxs-lookup"><span data-stu-id="f6370-116">In the **IRS Number** field, select an IRS number from the list.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f6370-117">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f6370-117">See Also</span></span>  
 [<span data-ttu-id="f6370-118">Sérstök gögn og skýrslur fyrir skattyfirvöld</span><span class="sxs-lookup"><span data-stu-id="f6370-118">Special Data Output and Reports for the Tax Authority</span></span>](special-data-output-and-reports-for-the-tax-authority.md) 
