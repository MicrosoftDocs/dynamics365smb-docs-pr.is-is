---
title: "Hvernig á að setja upp staðgreiðsluviðskiptamenn | Microsoft Docs"
description: "Þetta efnisatriði lýsir skrefum í uppsetningu viðskiptamanns sem staðgreiðir."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b904daec68261af855e789829791505e69f3f07a
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-cash-customers"></a><span data-ttu-id="2ab64-103">Uppsetning staðgreiðsluviðskiptamanna</span><span class="sxs-lookup"><span data-stu-id="2ab64-103">Set Up Cash Customers</span></span>
<span data-ttu-id="2ab64-104">Ekki er hægt að gera reikning án viðskiptamannsnúmers.</span><span class="sxs-lookup"><span data-stu-id="2ab64-104">You cannot create an invoice without a customer number.</span></span> <span data-ttu-id="2ab64-105">Þetta á við þó svo að selt sé gegn staðgreiðslu og ekki sé þörf á að skrá upplýsingar í viðskiptamannareikning.</span><span class="sxs-lookup"><span data-stu-id="2ab64-105">This is true, even if you make a cash sale and do not have anything to record in a customer account.</span></span>  

## <a name="to-set-up-a-cash-customer"></a><span data-ttu-id="2ab64-106">Uppsetning staðgreiðsluviðskiptamanna</span><span class="sxs-lookup"><span data-stu-id="2ab64-106">To set up a cash customer</span></span>  
1.  <span data-ttu-id="2ab64-107">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **viðskiptamaður** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2ab64-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2ab64-108">Stofna nýtt spjald **Viðskiptamaður**.</span><span class="sxs-lookup"><span data-stu-id="2ab64-108">Create a new **Customer** card.</span></span> <span data-ttu-id="2ab64-109">Frekari upplýsingar eru í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="2ab64-109">For more information, see [Register New Customers](sales-how-register-new-customers.md).</span></span>
3.  <span data-ttu-id="2ab64-110">Í reitnum **númer**</span><span class="sxs-lookup"><span data-stu-id="2ab64-110">In the **No.**</span></span> <span data-ttu-id="2ab64-111">er ritað **Reiðufé**, til dæmis.</span><span class="sxs-lookup"><span data-stu-id="2ab64-111">field, enter **Cash**, for example.</span></span>  
4.  <span data-ttu-id="2ab64-112">Í reitinn **Heiti** er til dæmis ritað **Staðgreitt við sölu**.</span><span class="sxs-lookup"><span data-stu-id="2ab64-112">In the **Name** field, enter **Cash Sale**, for example.</span></span>  
5.  <span data-ttu-id="2ab64-113">Á flýtiflipanum **Reikningsfærsla** þarf að fylla út reitina **Bókunarflokkur viðskiptam.** og **Alm. viðsk.bókunarflokkur**.</span><span class="sxs-lookup"><span data-stu-id="2ab64-113">On the **Invoicing** FastTab, fill in the **Customer Posting Group** and the **Gen. Bus. Posting Group** fields.</span></span>  

 <span data-ttu-id="2ab64-114">Nú hefur verið stofnaður viðskiptamaður með nægar upplýsingar til reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="2ab64-114">Now you have set up a customer that contains sufficient information for invoicing.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2ab64-115">Hugsanlega hefur verið valinn bókunarflokkur sem er einnig notaður við kreditsölu innanlands.</span><span class="sxs-lookup"><span data-stu-id="2ab64-115">You may have chosen a posting group that is also used for domestic credit sales.</span></span> <span data-ttu-id="2ab64-116">Eigi að geyma gögn um sölu gegn staðgreiðslu sérstaklega, til dæmis með sérstökum sölu- eða safnreikningi, er hægt að setja upp sérstakan bókunarflokk í því skyni.</span><span class="sxs-lookup"><span data-stu-id="2ab64-116">If you want to maintain separate data on cash sales, for example, with a special sales or receivables account, you can set up an extra posting group for this purpose.</span></span>  
>   
>  <span data-ttu-id="2ab64-117">Rita þarf safnreikningsnúmer fyrir bókunarflokkinn þó svo að staðan á reikningnum verði alltaf 0 eftir bókun reiknings.</span><span class="sxs-lookup"><span data-stu-id="2ab64-117">You must enter a number for a receivables account for the posting group, even though the balance in this account will always be 0 after you post an invoice.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2ab64-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2ab64-118">See Also</span></span>
[<span data-ttu-id="2ab64-119">Stjórnun skulda</span><span class="sxs-lookup"><span data-stu-id="2ab64-119">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="2ab64-120">[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)  </span><span class="sxs-lookup"><span data-stu-id="2ab64-120">[Register New Customers](sales-how-register-new-customers.md)  </span></span>  
[<span data-ttu-id="2ab64-121">Fjármál</span><span class="sxs-lookup"><span data-stu-id="2ab64-121">Finance</span></span>](finance.md)  


