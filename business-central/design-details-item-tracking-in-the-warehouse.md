---
title: Hönnunarupplýsingar - vörurakning í vöruhúsi | Microsoft Docs
description: Meðhöndlun á raðnúmeri eða lotunúmeri er aðallega vöruhúsaverkefni, og því eru öll vöruhúsaskjöl á innleið og útleið með staðlaða virkni fyrir úthlutun og val á vörurakningarnúmerum. Hins vegar, vegna þess að frátekningarkerfið er byggt á færslum í birgðahöfuðbók, eru skjöl um færslur í vöruhúsi sem skrá aðeins vöruhúsafærslur ekki studd að fullu.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e369517d05cd4a9e9c0586f6d7407f0351966def
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917402"
---
# <a name="design-details-item-tracking-in-the-warehouse"></a><span data-ttu-id="0e505-104">Hönnunarupplýsingar: vörurakning í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="0e505-104">Design Details: Item Tracking in the Warehouse</span></span>
<span data-ttu-id="0e505-105">Meðhöndlun á raðnúmeri eða lotunúmeri er aðallega vöruhúsaverkefni, og því eru öll vöruhúsaskjöl á innleið og útleið með staðlaða virkni fyrir úthlutun og val á vörurakningarnúmerum.</span><span class="sxs-lookup"><span data-stu-id="0e505-105">Serial number and lot number handling is primarily a warehouse task and therefore all inbound and outbound warehouse documents have standard functionality for assigning and selecting item tracking numbers.</span></span>  

<span data-ttu-id="0e505-106">Hins vegar, vegna þess að frátekningarkerfið er byggt á færslum í birgðahöfuðbók, eru skjöl um færslur í vöruhúsi sem skrá aðeins vöruhúsafærslur ekki studd að fullu.</span><span class="sxs-lookup"><span data-stu-id="0e505-106">However, because the reservation system is based on item ledger entries, warehouse activity documents that register only warehouse entries are not fully supported.</span></span> <span data-ttu-id="0e505-107">Vegna þess að frátekningar og vörurakningarnúmer geta aðeins verið meðhöndluð á staðsetningastigi, ekki á hólfa- og svæðisstigi er ekki hægt að opna síðuna **Vörurakningarlínur** úr virkniskjölum vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="0e505-107">Because reservations and item tracking numbers can be handled only at the location level, not at the bin and zone level, the **Item Tracking Lines** page cannot be opened from warehouse activity documents.</span></span> <span data-ttu-id="0e505-108">Sama á við um síðuna **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="0e505-108">The same applies to the **Reservation** page.</span></span>  

<span data-ttu-id="0e505-109">Eftir að rað- eða lotunúmer hefur verið bætt við vöru í vöruhúsastaðsetningu er hægt að færa hana og endurflokka að vild í vöruhúsinu með því að nota sjálfstæða vörurakningaruppbyggingu sem er ótengd frátekningarkerfinu.</span><span class="sxs-lookup"><span data-stu-id="0e505-109">After a serial or lot number has been added to an item at a warehouse location, it can be moved and reclassified freely within the warehouse by using an independent item tracking structure that is unrelated to the reservation system.</span></span> <span data-ttu-id="0e505-110">**Raðnúmer** og **Lotunúmer** er farið inn í beint úr vöruhúsaskjalalínunum.</span><span class="sxs-lookup"><span data-stu-id="0e505-110">**Serial No.** and **Lot No.** fields are accessed directly on warehouse document lines.</span></span> <span data-ttu-id="0e505-111">Þegar rað- eða lotunúmer verður seinna hluti af bókun á útleið er það samstill við frátekningarkerfið sem hluti af venjulegri leiðréttingu hólfa.</span><span class="sxs-lookup"><span data-stu-id="0e505-111">When the serial or lot number later partakes in outbound posting, it is synchronized with the reservation system as a part of ordinary bin adjustment.</span></span> <span data-ttu-id="0e505-112">Nánari upplýsingar eru í [Upplýsingar um hönnun: Samþætting við birgðir](design-details-integration-with-inventory.md).</span><span class="sxs-lookup"><span data-stu-id="0e505-112">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="0e505-113">Hins vegar tekur frátekningarkerfið tillit til vöruhúsaaðgerða þegar það reiknar út framboð.</span><span class="sxs-lookup"><span data-stu-id="0e505-113">However, the reservation system does take warehouse activities into consideration when it calculates availability.</span></span> <span data-ttu-id="0e505-114">Til dæmis vörur sem úthlutað er til tínslu eða skráðar sem tíndar er ekki hægt að taka frá.</span><span class="sxs-lookup"><span data-stu-id="0e505-114">For example, items that are allocated to picks, or registered as picked, cannot be reserved.</span></span> <span data-ttu-id="0e505-115">Nánari upplýsingar eru í [Hönnunarupplýsingar: staða vöruhúss](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="0e505-115">For more information, see [Design Details: Warehouse Availability](design-details-availability-in-the-warehouse.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0e505-116">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0e505-116">See Also</span></span>  
[<span data-ttu-id="0e505-117">Hönnunarupplýsingar: vörurakning</span><span class="sxs-lookup"><span data-stu-id="0e505-117">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)  
[<span data-ttu-id="0e505-118">Hönnunarupplýsingar: Sameining með birgðum</span><span class="sxs-lookup"><span data-stu-id="0e505-118">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)  
[<span data-ttu-id="0e505-119">Hönnunarupplýsingar: staða vöruhúss</span><span class="sxs-lookup"><span data-stu-id="0e505-119">Design Details: Warehouse Availability</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="0e505-120">Hönnunarupplýsingarn: vörurakning hönnun</span><span class="sxs-lookup"><span data-stu-id="0e505-120">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)
