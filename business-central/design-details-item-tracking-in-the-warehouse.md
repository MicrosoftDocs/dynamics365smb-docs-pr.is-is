---
title: "Hönnunarupplýsingar - Vörurakning Framboð | Microsoft Docs"
description: "Þetta efnisatriði fjallar um hvernig skal ganga úr skugga um að fólkið sem vinnur pantanir geti stólað á tiltækileika rað- eða lotunúmera."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: fcdfc219f94462048474acdef259f671e1c8a402
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="design-details-item-tracking-availability"></a><span data-ttu-id="2edc1-103">Hönnunarupplýsingar: vörurakning framboð</span><span class="sxs-lookup"><span data-stu-id="2edc1-103">Design Details: Item Tracking Availability</span></span>
<span data-ttu-id="2edc1-104">Síðurnar **Vörurakningarlínur** og **Samantekt vörurakningar** veita gagnvirkar framboðsupplýsingar fyrir raðnúmer eða lotunúmer.</span><span class="sxs-lookup"><span data-stu-id="2edc1-104">The **Item Tracking Lines** and **Item Tracking Summary** pages provide dynamic availability information for serial or lot numbers.</span></span> <span data-ttu-id="2edc1-105">Tilgangurinn með þessu er að auka gagnsæi fyrir notendur á fylgiskjölum á útleið, svo sem sölupöntunum, með því að sýna þeim hvaða raðnúmerum eða hve mörgum einingum lotunúmers er sem stendur úthlutað á önnur opin fylgiskjöl.</span><span class="sxs-lookup"><span data-stu-id="2edc1-105">The purpose of this is to increase transparency for users on outbound documents, such as sales orders, by showing them which serial numbers or how many units of a lot number are currently assigned on other open documents.</span></span> <span data-ttu-id="2edc1-106">Þetta minnkar óvissu sem stafar af tvöfaldri úthlutun og framkallar traust í pantanavinnslum að vörurakningarnúmerin og dagsetningar sem þeir eru að lofa á óbókuðum sölupöntunum sé hægt að uppfylla.</span><span class="sxs-lookup"><span data-stu-id="2edc1-106">This reduces uncertainty that is caused by double allocation and instills confidence in order processors that the item tracking numbers and dates that they are promising on unposted sales orders can be fulfilled.</span></span> <span data-ttu-id="2edc1-107">Nánari upplýsingar eru á síðunni [Upplýsingar um hönnun: Vörurakningarlínur](design-details-item-tracking-lines-window.md).</span><span class="sxs-lookup"><span data-stu-id="2edc1-107">For more information, see [Design Details: Item Tracking Lines Page](design-details-item-tracking-lines-window.md).</span></span>  

<span data-ttu-id="2edc1-108">Þegar þú opnar síðuna **Vörurakningarlínu** eru aðgengisgögn sótt úr töflunni **birgðafærsla** og töflunni **Frátekningarfærsla** án nokkurrar gagnaafmörkunar.</span><span class="sxs-lookup"><span data-stu-id="2edc1-108">When you open the **Item Tracking Lines** page, availability data is retrieved from the **Item Ledger Entry** table and the **Reservation Entry** table, with no date filter.</span></span> <span data-ttu-id="2edc1-109">Þegar þú velur reitinn **Raðnr.** eða **Lotunr.** opnast síðan **Samantekt vörurakningar** og birtir samantekt á vörurakningarupplýsingum í töflunni **Frátekningarfærsla**.</span><span class="sxs-lookup"><span data-stu-id="2edc1-109">When you choose the **Serial No.** field or the **Lot No.** field, the **Item Tracking Summary** page opens and shows a summary of the item tracking information in the **Reservation Entry** table.</span></span> <span data-ttu-id="2edc1-110">Þessi samantekt inniheldur eftirfarandi upplýsingar um hvert rað- eða lotunúmer í vörurakningarlínunni:</span><span class="sxs-lookup"><span data-stu-id="2edc1-110">The summary contains the following information about each serial or lot number on the item tracking line:</span></span>  

|<span data-ttu-id="2edc1-111">Svæði</span><span class="sxs-lookup"><span data-stu-id="2edc1-111">Field</span></span>|<span data-ttu-id="2edc1-112">Lýsing</span><span class="sxs-lookup"><span data-stu-id="2edc1-112">Description</span></span>|  
|---------------------------------|---------------------------------------|  
|<span data-ttu-id="2edc1-113">**Heildarmagn**</span><span class="sxs-lookup"><span data-stu-id="2edc1-113">**Total Quantity**</span></span>|<span data-ttu-id="2edc1-114">Heildarmagn rað- eða lotunúmers sem er í birgðum.</span><span class="sxs-lookup"><span data-stu-id="2edc1-114">The total quantity of the serial or lot number that is currently in inventory.</span></span>|  
|<span data-ttu-id="2edc1-115">**Umbeðið magn samtals**</span><span class="sxs-lookup"><span data-stu-id="2edc1-115">**Total Requested Quantity**</span></span>|<span data-ttu-id="2edc1-116">Heildarmagn lotu- eða raðnúmers sem þegar er í beiðni í öllum skjölum.</span><span class="sxs-lookup"><span data-stu-id="2edc1-116">The total quantity of the serial or lot number that is currently requested in all documents.</span></span>|  
|<span data-ttu-id="2edc1-117">**Magn í undirbúningi**</span><span class="sxs-lookup"><span data-stu-id="2edc1-117">**Current Pending Quantity**</span></span>|<span data-ttu-id="2edc1-118">Magnið sem er fært inn í núverandi tilvik á síðunni **Vörurakningarlínur** en hefur enn ekki verið skuldbundið í gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="2edc1-118">The quantity that is entered in the current instance of the **Item Tracking Lines** page but is not yet committed to the database.</span></span>|  
|<span data-ttu-id="2edc1-119">**Heildarmagn tiltækt**</span><span class="sxs-lookup"><span data-stu-id="2edc1-119">**Total Available Quantity**</span></span>|<span data-ttu-id="2edc1-120">Tilgreinir tiltækt magn sem notandinn getur tekið frá í þeim gerðum af færslum sem eru í línunni.</span><span class="sxs-lookup"><span data-stu-id="2edc1-120">The quantity of the serial or lot number that is available for the user to request.</span></span><br /><br /> <span data-ttu-id="2edc1-121">Þetta magn er reiknað út frá öðrum reitum á síðuna sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="2edc1-121">This quantity is calculated from other fields on the page as follows:</span></span><br /><br /> <span data-ttu-id="2edc1-122">heildarmagn – (umbeðið heildarmagn + núgildandi magn í bið).</span><span class="sxs-lookup"><span data-stu-id="2edc1-122">total quantity – (total requested quantity + current pending quantity).</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="2edc1-123">Einnig er hægt að sjá upplýsingar í töflunni á undan með því að nota aðgerðina **Velja færslur** á síðunni **Vörurakningarlínur**.</span><span class="sxs-lookup"><span data-stu-id="2edc1-123">You can also see the information in the preceding table by using the **Select Entries** function on the **Item Tracking Lines** page.</span></span>  

<span data-ttu-id="2edc1-124">Til að varðveita gagnasafn frammistöðu, gögn um magn til ráðstöfunar er aðeins sótt einu sinni úr gagnagrunninum þegar þú opnar **Vörurakningarlínur** glugga og nota **Endurnýja Til ráðstöfunar** eiginleikann á síðunni.</span><span class="sxs-lookup"><span data-stu-id="2edc1-124">To preserve database performance, availability data is only retrieved once from the database when you open the **Item Tracking Lines** page and use the **Refresh Availability** function on the page.</span></span>  

## <a name="calculation-formula"></a><span data-ttu-id="2edc1-125">Tegund útreiknings</span><span class="sxs-lookup"><span data-stu-id="2edc1-125">Calculation Formula</span></span>  
<span data-ttu-id="2edc1-126">Eins og lýst er í undanfarandi töflu er framboð á tilteknu raðnúmeri eða lotunúmeri reiknað á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="2edc1-126">As described in the preceding table, the availability of a given serial or lot number is calculated as follows:</span></span>  

* <span data-ttu-id="2edc1-127">Allt Laust Magn = magn birgða - (öll eftirspurn + magn ekki enn úthlutað á gagnagrunninum)</span><span class="sxs-lookup"><span data-stu-id="2edc1-127">total available quantity = quantity in inventory – (all demands + quantity not yet committed to the database)</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="2edc1-128">Þessi formúla gefur til kynna að rað- eða lotunúmer framboðsútreiknings taki aðeins til birgða og hundsi áætlaðar innhreyfingar.</span><span class="sxs-lookup"><span data-stu-id="2edc1-128">This formula implies that the serial or lot number availability calculation considers only inventory and ignores projected receipts.</span></span> <span data-ttu-id="2edc1-129">Í samræmi hefur framboð sem ekki hefur verið bókað í birgðir ekki áhrif á framboð vörurakningar öfugt við eðlilegt vöruframboð þar sem áætlaðar móttökur eru teknar með.</span><span class="sxs-lookup"><span data-stu-id="2edc1-129">Accordingly, supply that is not yet posted to inventory does not affect item tracking availability, as opposed to regular item availability where projected receipts are included.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2edc1-130">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2edc1-130">See Also</span></span>  
[<span data-ttu-id="2edc1-131">Hönnunarupplýsingar: vörurakning</span><span class="sxs-lookup"><span data-stu-id="2edc1-131">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)

