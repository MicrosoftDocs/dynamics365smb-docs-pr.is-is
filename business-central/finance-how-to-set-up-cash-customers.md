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
ms.date: 08/11/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 93c28879417b12bc142c84c38c054828b380cc53
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-cash-customers"></a><span data-ttu-id="f11be-103">Uppsetning staðgreiðsluviðskiptamanna</span><span class="sxs-lookup"><span data-stu-id="f11be-103">Set Up Cash Customers</span></span>
<span data-ttu-id="f11be-104">Ekki er hægt að gera reikning án viðskiptamannsnúmers.</span><span class="sxs-lookup"><span data-stu-id="f11be-104">You cannot create an invoice without a customer number.</span></span> <span data-ttu-id="f11be-105">Þetta á við þó svo að selt sé gegn staðgreiðslu og ekki sé þörf á að skrá upplýsingar í viðskiptamannareikning.</span><span class="sxs-lookup"><span data-stu-id="f11be-105">This is true, even if you make a cash sale and do not have anything to record in a customer account.</span></span>  

## <a name="to-set-up-a-cash-customer"></a><span data-ttu-id="f11be-106">Uppsetning staðgreiðsluviðskiptamanna</span><span class="sxs-lookup"><span data-stu-id="f11be-106">To set up a cash customer</span></span>  
1.  <span data-ttu-id="f11be-107">Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **viðskiptamaður** og velja svo viðeigandi tengil.</span><span class="sxs-lookup"><span data-stu-id="f11be-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f11be-108">Stofna nýtt spjald **Viðskiptamaður**.</span><span class="sxs-lookup"><span data-stu-id="f11be-108">Create a new **Customer** card.</span></span> <span data-ttu-id="f11be-109">Frekari upplýsingar eru í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="f11be-109">For more information, see [Register New Customers](sales-how-register-new-customers.md).</span></span>
3.  <span data-ttu-id="f11be-110">Í reitnum **númer**</span><span class="sxs-lookup"><span data-stu-id="f11be-110">In the **No.**</span></span> <span data-ttu-id="f11be-111">er ritað **Reiðufé**, til dæmis.</span><span class="sxs-lookup"><span data-stu-id="f11be-111">field, enter **Cash**, for example.</span></span>  
4.  <span data-ttu-id="f11be-112">Í reitinn **Heiti** er til dæmis ritað **Staðgreitt við sölu**.</span><span class="sxs-lookup"><span data-stu-id="f11be-112">In the **Name** field, enter **Cash Sale**, for example.</span></span>  
5.  <span data-ttu-id="f11be-113">Á flýtiflipanum **Reikningsfærsla** þarf að fylla út reitina **Bókunarflokkur viðskiptam.** og **Alm. viðsk.bókunarflokkur**.</span><span class="sxs-lookup"><span data-stu-id="f11be-113">On the **Invoicing** FastTab, fill in the **Customer Posting Group** and the **Gen. Bus. Posting Group** fields.</span></span>  

 <span data-ttu-id="f11be-114">Nú hefur verið stofnaður viðskiptamaður með nægar upplýsingar til reikningsfærslu.</span><span class="sxs-lookup"><span data-stu-id="f11be-114">Now you have set up a customer that contains sufficient information for invoicing.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f11be-115">Hugsanlega hefur verið valinn bókunarflokkur sem er einnig notaður við kreditsölu innanlands.</span><span class="sxs-lookup"><span data-stu-id="f11be-115">You may have chosen a posting group that is also used for domestic credit sales.</span></span> <span data-ttu-id="f11be-116">Eigi að geyma gögn um sölu gegn staðgreiðslu sérstaklega, til dæmis með sérstökum sölu- eða safnreikningi, er hægt að setja upp sérstakan bókunarflokk í því skyni.</span><span class="sxs-lookup"><span data-stu-id="f11be-116">If you want to maintain separate data on cash sales, for example, with a special sales or receivables account, you can set up an extra posting group for this purpose.</span></span>  
>   
>  <span data-ttu-id="f11be-117">Rita þarf safnreikningsnúmer fyrir bókunarflokkinn þó svo að staðan á reikningnum verði alltaf 0 eftir bókun reiknings.</span><span class="sxs-lookup"><span data-stu-id="f11be-117">You must enter a number for a receivables account for the posting group, even though the balance in this account will always be 0 after you post an invoice.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f11be-118">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f11be-118">See Also</span></span>
[<span data-ttu-id="f11be-119">Stjórnun skulda</span><span class="sxs-lookup"><span data-stu-id="f11be-119">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="f11be-120">[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)  </span><span class="sxs-lookup"><span data-stu-id="f11be-120">[Register New Customers](sales-how-register-new-customers.md)  </span></span>  
[<span data-ttu-id="f11be-121">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f11be-121">Finance</span></span>](finance.md)  


