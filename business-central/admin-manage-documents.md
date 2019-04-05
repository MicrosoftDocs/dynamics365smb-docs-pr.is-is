---
title: Meðhöndla, eyða eða þjappa skjöl | Microsoft Docs
description: Geyma söguleg gögn eða eyða þeim.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: 5cc49d8b17a56c8f19926cf33e63467005d4788c
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "800768"
---
# <a name="manage-documents"></a><span data-ttu-id="b9afa-103">Umsjón með skjölum</span><span class="sxs-lookup"><span data-stu-id="b9afa-103">Manage Documents</span></span>
<span data-ttu-id="b9afa-104">Meginhlutverk, t.d. kerfisstjóri, þarf reglulega að sjá um þau gögn sem safnast upp, eyða þeim eða þjappa þau.</span><span class="sxs-lookup"><span data-stu-id="b9afa-104">A central role, such as the application administrator, must regularly deal with accumulating historic documents by deleting or compressing them.</span></span>  

## <a name="delete-documents"></a><span data-ttu-id="b9afa-105">Eyða skjölum</span><span class="sxs-lookup"><span data-stu-id="b9afa-105">Delete Documents</span></span>
<span data-ttu-id="b9afa-106">Í vissum tilvikum kann að þurfa að eyða reikningsfærðum innkaupapöntunum sem ekki hefur verið eytt.</span><span class="sxs-lookup"><span data-stu-id="b9afa-106">In certain situations, you may need to delete invoiced purchase orders that have not been deleted.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="b9afa-107">kannar hvort eyddu innkaupapantanirnar hafa verið reikningsfærðar að fullu.</span><span class="sxs-lookup"><span data-stu-id="b9afa-107">checks that you have fully invoiced the deleted purchase orders.</span></span> <span data-ttu-id="b9afa-108">Ekki er hægt að eyða pöntunum sem hafa ekki verið fullkomlega reikningsfærðar og mótteknar.</span><span class="sxs-lookup"><span data-stu-id="b9afa-108">You cannot delete orders that you have not fully invoiced and received.</span></span>  

<span data-ttu-id="b9afa-109">Vöruskilapöntunum er yfirleitt eytt þegar þær hafa verið reikningsfærðar.</span><span class="sxs-lookup"><span data-stu-id="b9afa-109">Return orders are usually deleted after they are invoiced.</span></span> <span data-ttu-id="b9afa-110">Þegar reikningur er bókaður er hann fluttur á síðuna **Bókaður innkaupakreditreikningur**.</span><span class="sxs-lookup"><span data-stu-id="b9afa-110">When you post an invoice, it is transferred to the **Posted Purchase Credit Memo** page.</span></span> <span data-ttu-id="b9afa-111">Ef gátreiturinn **Vöruskilaafhending á kreditreikningi** hefur verið valinn á síðunni **Innkaupagrunnur** er reikningurinn fluttur á síðuna **Bókuð skilaafhending**.</span><span class="sxs-lookup"><span data-stu-id="b9afa-111">If you selected the **Return Shipment on Credit Memo** check box on the **Purchases & Payable Setup** page, then the invoice is transferred to the **Posted Return Shipment** page.</span></span> <span data-ttu-id="b9afa-112">Hægt er að eyða skjölunum með því að nota keyrsluna **Eyða reiknf. innk.vöruskilapönt.**.</span><span class="sxs-lookup"><span data-stu-id="b9afa-112">You can delete the documents using the **Delete Invd Purch. Ret. Orders** batch job.</span></span> <span data-ttu-id="b9afa-113">Áður en eytt er, athugar runuvinnslan hvort innkaupaskilapantanirnar séu að fullu afhentar og reikningsfærðar.</span><span class="sxs-lookup"><span data-stu-id="b9afa-113">Before deleting, the batch job checks if the purchase return orders are fully shipped and invoiced.</span></span>  

<span data-ttu-id="b9afa-114">Standandi pöntunum er ekki eytt eftir að allar tengdar innkaupapantanir hafa verið unnar og reikningsfærðar.</span><span class="sxs-lookup"><span data-stu-id="b9afa-114">Blanket purchase orders are not deleted after you have processed and invoiced all the related purchase orders.</span></span> <span data-ttu-id="b9afa-115">Hægt er að eyða standandi pöntunum með keyrslunni **Reikningsfærðum standandi innkaupapöntunum eytt**.</span><span class="sxs-lookup"><span data-stu-id="b9afa-115">You can delete blanket orders with the **Delete Invoiced Blanket Purchase Orders** batch job.</span></span>  

<span data-ttu-id="b9afa-116">Þjónustupöntunum er yfirleitt eytt sjálfkrafa þegar þær hafa verið reikningsfærðar til fulls.</span><span class="sxs-lookup"><span data-stu-id="b9afa-116">Invoiced service orders are usually deleted automatically after having been fully invoiced.</span></span> <span data-ttu-id="b9afa-117">Þegar reikningur er bókaður er samsvarandi færsla stofnuð á síðunni **Bókaðir þjónustureikningar** .</span><span class="sxs-lookup"><span data-stu-id="b9afa-117">When an invoice is posted, a corresponding entry is created on the **Posted Service Invoices** page.</span></span> <span data-ttu-id="b9afa-118">Hægt er að skoða bókaða fylgiskjalið á síðunni **Bókaður þjónustureikningur**.</span><span class="sxs-lookup"><span data-stu-id="b9afa-118">The posted document can be viewed on the **Posted Service Invoice** page.</span></span>  

<span data-ttu-id="b9afa-119">Forritið eyðir þjónustupöntun ekki sjálfkrafa ef heildarmagn pöntunarinnar hefur verið bókað af síðunni **Þjónustureikningur** en ekki í þjónustupöntuninni sjálfri.</span><span class="sxs-lookup"><span data-stu-id="b9afa-119">Service orders are not deleted automatically, however, if the total quantity on the order has been posted not from the service order itself, but from the **Service Invoice** page.</span></span> <span data-ttu-id="b9afa-120">Þá þarf að eyða bókuðum pöntunum sem ekki var búið að eyða.</span><span class="sxs-lookup"><span data-stu-id="b9afa-120">Then you may need to delete invoiced orders that were not deleted.</span></span> <span data-ttu-id="b9afa-121">Hægt er að gera það með því að nota keyrsluna **Eyða reikningsfærðum þjónustupöntunum**.</span><span class="sxs-lookup"><span data-stu-id="b9afa-121">You can do this by running the **Delete Invoiced Service Orders** batch job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b9afa-122">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="b9afa-122">See Also</span></span>  
[<span data-ttu-id="b9afa-123">Stjórnun</span><span class="sxs-lookup"><span data-stu-id="b9afa-123">Administration</span></span>](admin-setup-and-administration.md)  
