---
title: Bæta við aukalínum til að skilgreina ítarlegar lýsingar
description: Þú getur bætt við auka línum til að lengja staðlaðan texta sem lýsir vöru, fjárhagsreikningi og öðrum gögnum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/08/2020
ms.author: edupont
ms.openlocfilehash: cf0418f4182e9d66da88af9262dd807a34dd3572
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782319"
---
# <a name="add-extended-text"></a><span data-ttu-id="bd6e8-103">Bæta við lengdum texta</span><span class="sxs-lookup"><span data-stu-id="bd6e8-103">Add Extended Text</span></span>

<span data-ttu-id="bd6e8-104">Hægt er að víkka lýsinguna fyrir vörur, lagerbirgðir, fjárhagslykla og tilföng með því að bæta við aukalínum sem lengdum texta.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-104">You can extend the description for items, stock-keeping units, general ledger accounts, and resources by adding extra lines as extended text.</span></span> <span data-ttu-id="bd6e8-105">Einnig er hægt að setja upp skilyrði fyrir notkun á aukalínum.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-105">You can also set up conditions for use of the extra lines.</span></span>  

<span data-ttu-id="bd6e8-106">Í eftirfarandi kafla er því lýst hvernig bæta skal lengdum texta við lýsingu á vöru.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-106">The following section describes how to add extended text to a description of an item.</span></span> <span data-ttu-id="bd6e8-107">En sömu skref eiga við um birgðahaldseiningu, fjárhagsreikninga og tilföng.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-107">But the same steps apply to stock-keeping units, general ledger accounts, and resources.</span></span>  

## <a name="to-define-extended-text-for-an-description"></a><span data-ttu-id="bd6e8-108">Til að skilgreina lengdan texta fyrir lýsingu</span><span class="sxs-lookup"><span data-stu-id="bd6e8-108">To define extended text for an description</span></span>

1. <span data-ttu-id="bd6e8-109">Opnið spjaldið fyrir vöru sem bæta á við texta fyrir og veljið aðgerðina **Lengdur texti**.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-109">Open the card for an item that you want to add extended text to, and then choose the **Extended Text** action.</span></span>
2. <span data-ttu-id="bd6e8-110">Fyllt er í reitina **Kóti** og **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-110">Fill in the **Code** and **Description** fields.</span></span>
3. <span data-ttu-id="bd6e8-111">Veldu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-111">Choose the **New**.</span></span>
4. <span data-ttu-id="bd6e8-112">Fylltu í reitinn **Tungumálakóði** eða veldu gátreitinn **Allir tungumálakóðar** ef notaðir eru tungumálakóðar.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-112">Fill in the **Language Code** field or select the **All Language Codes** check box if you use language codes.</span></span>
5. <span data-ttu-id="bd6e8-113">Reitirnir **Upphafsdagsetning** og **Lokadagsetning** eru fylltir út ef afmarka á tímabil fyrir lengdan texta.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-113">Fill in the **Starting Date** and **Ending Date** fields if you want to limit the dates on which the extended text is used.</span></span>
6. <span data-ttu-id="bd6e8-114">Í reitnum **Texti** skal skrifa lengdan texta.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-114">In the **Text** field, write the extended text.</span></span>
7. <span data-ttu-id="bd6e8-115">Veljið viðeigandi gátreiti fyrir skjalategundir sem á að prenta lengda textann á.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-115">Select relevant check boxes for the document types where you want the extended text printed.</span></span>
8. <span data-ttu-id="bd6e8-116">Lokaðu síðunni.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-116">Close the page.</span></span>

<span data-ttu-id="bd6e8-117">Nú er hægt að bæta þessum lengda texta við skjöl.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-117">You can now add this extended text to documents.</span></span> <span data-ttu-id="bd6e8-118">Eftirfarandi ferli útskýrir hvernig á að bæta lengdum texta við sölupöntun en sömu skref eiga við um önnur skjöl sem voru tilgreind fyrir lengda textann.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-118">The following procedure explains how to add extended text to a sales order, but the same steps apply to any other document that you specified for the extended text.</span></span>  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a><span data-ttu-id="bd6e8-119">Að bæta við lengdum vörutexta í sölupöntunarlínu</span><span class="sxs-lookup"><span data-stu-id="bd6e8-119">To add an extended item text on a sales order line</span></span>

1. <span data-ttu-id="bd6e8-120">Opnið sölupöntun með sölulínu fyrir vöru sem hefur lengdan texta skilgreindan.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-120">Open a sales order with a sales line for an item that has extended text defined.</span></span> <span data-ttu-id="bd6e8-121">Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="bd6e8-121">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="bd6e8-122">Veljið viðkomandi línu og veljið síðan aðgerðina **Bæta við lengdum texta**.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-122">Select the line in question, and then choose the **Insert Ext. Text** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd6e8-123">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="bd6e8-123">See Also</span></span>

[<span data-ttu-id="bd6e8-124">Uppsetning birgða</span><span class="sxs-lookup"><span data-stu-id="bd6e8-124">Setting Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="bd6e8-125">[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bd6e8-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
