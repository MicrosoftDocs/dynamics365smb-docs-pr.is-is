---
title: "Meðhöndla, eyða eða þjappa skjöl | Microsoft Docs"
description: "Geyma söguleg gögn eða eyða þeim."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 292231a907970de2821daeba87003eca7bf54cdc
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="manage-documents"></a><span data-ttu-id="8b5d2-103">Umsjón með skjölum</span><span class="sxs-lookup"><span data-stu-id="8b5d2-103">Manage Documents</span></span>
<span data-ttu-id="8b5d2-104">Meginhlutverk, t.d. kerfisstjóri, þarf reglulega að sjá um þau gögn sem safnast upp, eyða þeim eða þjappa þau.</span><span class="sxs-lookup"><span data-stu-id="8b5d2-104">A central role, such as the application administrator, must regularly deal with accumulating historic documents by deleting or compressing them.</span></span>  

## <a name="delete-documents"></a><span data-ttu-id="8b5d2-105">Eyða skjölum</span><span class="sxs-lookup"><span data-stu-id="8b5d2-105">Delete Documents</span></span>
<span data-ttu-id="8b5d2-106">Í vissum tilvikum kann að þurfa að eyða reikningsfærðum innkaupapöntunum sem ekki hefur verið eytt.</span><span class="sxs-lookup"><span data-stu-id="8b5d2-106">In certain situations, you may need to delete invoiced purchase orders that have not been deleted.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="8b5d2-107"> kannar hvort eyddu innkaupapantanirnar hafa verið reikningsfærðar að fullu.</span><span class="sxs-lookup"><span data-stu-id="8b5d2-107"> checks that you have fully invoiced the deleted purchase orders.</span></span> <span data-ttu-id="8b5d2-108">Ekki er hægt að eyða pöntunum sem hafa ekki verið fullkomlega reikningsfærðar og mótteknar.</span><span class="sxs-lookup"><span data-stu-id="8b5d2-108">You cannot delete orders that you have not fully invoiced and received.</span></span>  

<span data-ttu-id="8b5d2-109">Vöruskilapöntunum er yfirleitt eytt þegar þær hafa verið reikningsfærðar.</span><span class="sxs-lookup"><span data-stu-id="8b5d2-109">Return orders are usually deleted after they are invoiced.</span></span> <span data-ttu-id="8b5d2-110">Þegar reikningur er bókaður er hann fluttur í gluggann **Bókaður innkaupakreditreikningur**.</span><span class="sxs-lookup"><span data-stu-id="8b5d2-110">When you post an invoice, it is transferred to the **Posted Purchase Credit Memo** window.</span></span> <span data-ttu-id="8b5d2-111">Ef gátreiturinn **Vöruskilaafhending á kreditreikningi** hefur verið valinn í glugganum **Innkaupagrunnur** er reikningurinn fluttur í gluggann **Bókuð skilaafhending**.</span><span class="sxs-lookup"><span data-stu-id="8b5d2-111">If you selected the **Return Shipment on Credit Memo** check box in the **Purchases & Payable Setup** window, then the invoice is transferred to the **Posted Return Shipment** window.</span></span> <span data-ttu-id="8b5d2-112">Hægt er að eyða skjölunum með því að nota keyrsluna **Eyða reiknf. innk.vöruskilapönt.**.</span><span class="sxs-lookup"><span data-stu-id="8b5d2-112">You can delete the documents using the **Delete Invd Purch. Ret. Orders** batch job.</span></span> <span data-ttu-id="8b5d2-113">Áður en eytt er, athugar runuvinnslan hvort innkaupaskilapantanirnar séu að fullu afhentar og reikningsfærðar.</span><span class="sxs-lookup"><span data-stu-id="8b5d2-113">Before deleting, the batch job checks if the purchase return orders are fully shipped and invoiced.</span></span>  

<span data-ttu-id="8b5d2-114">Standandi pöntunum er ekki eytt eftir að allar tengdar innkaupapantanir hafa verið unnar og reikningsfærðar.</span><span class="sxs-lookup"><span data-stu-id="8b5d2-114">Blanket purchase orders are not deleted after you have processed and invoiced all the related purchase orders.</span></span> <span data-ttu-id="8b5d2-115">Hægt er að eyða standandi pöntunum með keyrslunni **Reikningsfærðum standandi innkaupapöntunum eytt**.</span><span class="sxs-lookup"><span data-stu-id="8b5d2-115">You can delete blanket orders with the **Delete Invoiced Blanket Purchase Orders** batch job.</span></span>  

<span data-ttu-id="8b5d2-116">Þjónustupöntunum er yfirleitt eytt sjálfkrafa þegar þær hafa verið reikningsfærðar til fulls.</span><span class="sxs-lookup"><span data-stu-id="8b5d2-116">Invoiced service orders are usually deleted automatically after having been fully invoiced.</span></span> <span data-ttu-id="8b5d2-117">Þegar reikningur er bókaður er samsvarandi færsla stofnuð í glugganum  **Bókaðir þjónustureikningar** .</span><span class="sxs-lookup"><span data-stu-id="8b5d2-117">When an invoice is posted, a corresponding entry is created in the **Posted Service Invoices** window.</span></span> <span data-ttu-id="8b5d2-118">Hægt er að skoða bókaða fylgiskjalið í glugganum **Bókaður þjónustureikningur**.</span><span class="sxs-lookup"><span data-stu-id="8b5d2-118">The posted document can be viewed in the **Posted Service Invoice** window.</span></span>  

<span data-ttu-id="8b5d2-119">Forritið eyðir þjónustupöntun ekki sjálfkrafa ef heildarmagn pöntunarinnar hefur verið bókað í glugganum **Þjónustureikningur** en ekki í þjónustupöntuninni sjálfri.</span><span class="sxs-lookup"><span data-stu-id="8b5d2-119">Service orders are not deleted automatically, however, if the total quantity on the order has been posted not from the service order itself, but from the **Service Invoice** window.</span></span> <span data-ttu-id="8b5d2-120">Þá þarf að eyða bókuðum pöntunum sem ekki var búið að eyða.</span><span class="sxs-lookup"><span data-stu-id="8b5d2-120">Then you may need to delete invoiced orders that were not deleted.</span></span> <span data-ttu-id="8b5d2-121">Hægt er að gera það með því að nota keyrsluna **Eyða reikningsfærðum þjónustupöntunum**.</span><span class="sxs-lookup"><span data-stu-id="8b5d2-121">You can do this by running the **Delete Invoiced Service Orders** batch job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8b5d2-122">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="8b5d2-122">See Also</span></span>  
[<span data-ttu-id="8b5d2-123">Uppsetning og stjórnun í Business Central</span><span class="sxs-lookup"><span data-stu-id="8b5d2-123">Setup and Administration in Business Central</span></span>](admin-setup-and-administration.md)  

