---
title: Setja upp stöður fyrir þjónustupantanir og viðgerðir | Microsoft Docs
description: Þú verður að setja upp níu viðgerðarstöðuvalkosti sem sýna framvindu viðgerða og viðhalds á þjónustuvöru í þjónustupöntunum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: 4c28fcfbc2cbc7493ba183812383225754fd3dfa
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389650"
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="2e122-103">Setja upp stöður fyrir þjónustupantanir og viðgerðir</span><span class="sxs-lookup"><span data-stu-id="2e122-103">Set Up Statuses for Service Orders and Repairs</span></span>

<span data-ttu-id="2e122-104">Þú verður að setja upp viðgerðarstöðuvalkosti sem sýna framvindu viðgerða og viðhalds á þjónustuvöru í þjónustupöntunum.</span><span class="sxs-lookup"><span data-stu-id="2e122-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="2e122-105">Gert er ráð fyrir níu mismunandi valkostum viðgerðarstöðu miðað við aðstæður eða aðgerðir sem gripið er til þegar þjónustuvörur eru teknar til þjónustu.</span><span class="sxs-lookup"><span data-stu-id="2e122-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="2e122-106">Þú getur stillt forgang stöðuvalkosti þjónustupöntunar.</span><span class="sxs-lookup"><span data-stu-id="2e122-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="2e122-107">Fernt kemur til greina: **Mikill**, **Í meðallagi mikill**, **Í meðallagi lítill** og **Lítill**.</span><span class="sxs-lookup"><span data-stu-id="2e122-107">The four priorities are **High**, **Medium High**, **Medium Low**, and **Low**.</span></span>  

<span data-ttu-id="2e122-108">Þegar viðgerðarstöðu þjónustuvöru í þjónustupöntun er breytt uppfærir kerfi þjónustupöntunarstöðuna.</span><span class="sxs-lookup"><span data-stu-id="2e122-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="2e122-109">Viðgerðarstaða hverrar þjónustuvöru tengist stöðu þjónustupöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="2e122-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="2e122-110">Ef þjónustuvaran tengist tveimur eða fleiri þjónustupöntunarstöðuvalkostum er þjónustupöntunarstöðuvalkosturinn valinn sem gefur mesta forgangsröð.</span><span class="sxs-lookup"><span data-stu-id="2e122-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

<span data-ttu-id="2e122-111">Áður en hægt er að setja upp viðgerðarstöðu verður að setja upp forgang þjónustustöðu.</span><span class="sxs-lookup"><span data-stu-id="2e122-111">Before you can set up a repair status, you must set up service status priorities.</span></span>

## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="2e122-112">Uppsetning viðgerðarstöðuforgangs</span><span class="sxs-lookup"><span data-stu-id="2e122-112">To set up service status priorities</span></span>

1. <span data-ttu-id="2e122-113">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Staða þjónustupöntunar** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2e122-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2e122-114">Velja skal þjónustupöntunarstöðuna sem á að forgangsraða.</span><span class="sxs-lookup"><span data-stu-id="2e122-114">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="2e122-115">Í reitnum **Forgangur** er valin forgangsröð sem veita á þjónustupöntunarstöðunni.</span><span class="sxs-lookup"><span data-stu-id="2e122-115">In the **Priority** field, choose the priority you want for this service order status.</span></span>  

<span data-ttu-id="2e122-116">Þrep 2 og 3 eru endurtekin þar til búið er að forgangsraða stöðuvalkostunum fjórum. **Í undirbúningi** , **Í vinnslu** , **Lokið** og **Í bið**.</span><span class="sxs-lookup"><span data-stu-id="2e122-116">Repeat steps 2 and 3 until you have set the priority for each of the four status options: **Pending**, **In Process**, **Finished**, and **On Hold**.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="2e122-117">Uppsetning viðgerðarstöðu</span><span class="sxs-lookup"><span data-stu-id="2e122-117">To set up a repair status</span></span>

1. <span data-ttu-id="2e122-118">Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðgerðarstaða** og veldu síðan tengda tengilinn.</span><span class="sxs-lookup"><span data-stu-id="2e122-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Repair Status**, and then choose the related link.</span></span>
2. <span data-ttu-id="2e122-119">Stofnið nýja viðgerðarstöðu.</span><span class="sxs-lookup"><span data-stu-id="2e122-119">Create a new repair status.</span></span>  
3. <span data-ttu-id="2e122-120">Fyllt er í reitina **Kóti** og **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="2e122-120">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="2e122-121">Í reitnum **Staða þjónustupöntunar** er valin staða pöntunar sem á að tengja viðgerðarstöðuna við.</span><span class="sxs-lookup"><span data-stu-id="2e122-121">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="2e122-122">Reiturinn **Forgangur** sýnir forgangi stöðunnar á þjónustupöntun sem valin var.</span><span class="sxs-lookup"><span data-stu-id="2e122-122">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="2e122-123">Veldu viðgerðarstaða</span><span class="sxs-lookup"><span data-stu-id="2e122-123">Choose a repair status.</span></span> <span data-ttu-id="2e122-124">Hægt er að velja aðeins eina</span><span class="sxs-lookup"><span data-stu-id="2e122-124">You can choose only one.</span></span> <span data-ttu-id="2e122-125">Viðgerðarstöðu er ekki hægt að tengja við fleiri en einn valkost fyrir viðgerðarstöðu.</span><span class="sxs-lookup"><span data-stu-id="2e122-125">A repair status cannot be linked more than one repair status option.</span></span>  
6. <span data-ttu-id="2e122-126">Til að hægt sé að bóka þjónustupantanir, þar með taldar þjónustuvörur, með þessa viðgerðarstöðu, skal velja **Bókun leyfð** reitinn.</span><span class="sxs-lookup"><span data-stu-id="2e122-126">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="2e122-127">Til að unnt sé að breyta handvirkt stöðukosti þjónustupöntunar í **Í undirbúningi** í þjónustupöntunum með þjónustuvöru sem hefur þessa viðgerðarstöðu, skal velja **Í undirbúningi staða leyfð** gátreitinn.</span><span class="sxs-lookup"><span data-stu-id="2e122-127">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="2e122-128">Veljið gátreitina **Staðan Í vinnslu leyfð**, **Staðan Lokið leyfð** og **Staðan Í bið leyfð** á sama hátt.</span><span class="sxs-lookup"><span data-stu-id="2e122-128">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>

<span data-ttu-id="2e122-129">Skrefin eru endurtekin fyrir hvern valkost viðgerðarstöðu sem á að stofna.</span><span class="sxs-lookup"><span data-stu-id="2e122-129">Repeat these steps for each of the repair status options you want to create.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e122-130">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2e122-130">See Also</span></span>

[<span data-ttu-id="2e122-131">Þjónustupöntunarstaða og viðgerðarstaða</span><span class="sxs-lookup"><span data-stu-id="2e122-131">Service Order Status and Repair Status</span></span>](service-service-order-status-and-repair-status.md)  
[<span data-ttu-id="2e122-132">Þjónustustýring sett upp</span><span class="sxs-lookup"><span data-stu-id="2e122-132">Setting Up Service Management</span></span>](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]