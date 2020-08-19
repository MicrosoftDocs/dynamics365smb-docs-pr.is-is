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
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: a558976667050484d444333953657497b376b1ba
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/10/2020
ms.locfileid: "3676804"
---
# <a name="map-irs-numbers-to-chart-of-accounts"></a><span data-ttu-id="e21d1-104">Varpa skattstofunúmerum í bókhaldslykla</span><span class="sxs-lookup"><span data-stu-id="e21d1-104">Map IRS Numbers to Chart of Accounts</span></span>
<span data-ttu-id="e21d1-105">Fyrirtæki á Íslandi þurfa að senda gagnaskrá á fyrirfram tilgreindu formi til skattyfirvalda.</span><span class="sxs-lookup"><span data-stu-id="e21d1-105">Companies in Iceland are required to send the tax authority a data file in a predefined format.</span></span> <span data-ttu-id="e21d1-106">Áður en hægt er að gera þetta þarf að varpa fyrirfram skilgreindum reikningskóða skattstofu (Internal Revenue Service) í fjárhagsreikning.</span><span class="sxs-lookup"><span data-stu-id="e21d1-106">Before you can do this, you must map predefined Internal Revenue Service (IRS) account codes to general ledger accounts.</span></span>  

## <a name="to-create-an-internal-revenue-service-number"></a><span data-ttu-id="e21d1-107">Til að stofna skattstofunúmer</span><span class="sxs-lookup"><span data-stu-id="e21d1-107">To create an Internal Revenue Service number</span></span>  

1.  <span data-ttu-id="e21d1-108">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skattstofunúmer** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="e21d1-108">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **IRS Number**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e21d1-109">Valið er aðgerðin **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e21d1-109">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="e21d1-110">Á nýju línunni skaltu slá inn númer í reitinn **Skattstofunúmer** og gefa upp heiti í reitinn **Nafn**.</span><span class="sxs-lookup"><span data-stu-id="e21d1-110">On the new line, enter a number in the **IRS number** field, and provide a name in the **Name** field.</span></span>  
4.  <span data-ttu-id="e21d1-111">Veldu gátreitinn **Öfugt forskeyti** ef neikvæðu forskeyti á að snúa við á stöðu fjárhagsreiknings sem skattstofunúmerið er varpað á.</span><span class="sxs-lookup"><span data-stu-id="e21d1-111">Select the **Reverse Prefix** check box if you want the negative operator to be reversed on the balance of the general ledger account that the IRS number is mapped to.</span></span>  
5.  <span data-ttu-id="e21d1-112">Velja hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e21d1-112">Choose the **OK** button.</span></span>  

## <a name="to-map-an-irs-number-to-a-general-ledger-account"></a><span data-ttu-id="e21d1-113">Til að varpa skattstofunúmeri í fjárhagsreikning</span><span class="sxs-lookup"><span data-stu-id="e21d1-113">To map an IRS number to a general ledger account</span></span>  

1.  <span data-ttu-id="e21d1-114">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](../../media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Bókhaldslykill** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="e21d1-114">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e21d1-115">Veldu fjárhagsreikning sem er með **Tegund reiknings** af gerðinni **Bókun**.</span><span class="sxs-lookup"><span data-stu-id="e21d1-115">Select a general ledger account that has an **Account Type** of **Posting**.</span></span>  
3.  <span data-ttu-id="e21d1-116">Í reitnum **Skattstofunúmer** velurðu skattstofunúmer af listanum.</span><span class="sxs-lookup"><span data-stu-id="e21d1-116">In the **IRS Number** field, select an IRS number from the list.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e21d1-117">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e21d1-117">See Also</span></span>  
 [<span data-ttu-id="e21d1-118">Sérstök gögn og skýrslur fyrir skattyfirvöld</span><span class="sxs-lookup"><span data-stu-id="e21d1-118">Special Data Output and Reports for the Tax Authority</span></span>](special-data-output-and-reports-for-the-tax-authority.md) 
