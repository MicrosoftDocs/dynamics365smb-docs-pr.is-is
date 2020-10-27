---
title: Tengja og samstilla færslur handvirkt| Microsoft Docs
description: Samstilling samþættingartöflu virkjar gagnasamþættingu í öllum færslum í töflu í Business Central og Dynamics 365 Sales einingu sem eru tengdar.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: d8140f71709208a271eff5c8de415b0e95736072
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911406"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="e43e4-103">Tengja og samstilla færslur handvirkt</span><span class="sxs-lookup"><span data-stu-id="e43e4-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="e43e4-104">Þetta efnisatriði lýsir því hvernig á að tengja eina eða fleiri færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] við færslur í Common Data Service eða [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e43e4-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="e43e4-105">Að tengja færslur gerir þér kleift að skoða Common Data Service upplýsingar úr [!INCLUDE[d365fin](includes/d365fin_md.md)] og öfugt.</span><span class="sxs-lookup"><span data-stu-id="e43e4-105">Coupling records lets you view Common Data Service information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="e43e4-106">Tenging gerir þér einnig að samstilla gögn á milli færslna.</span><span class="sxs-lookup"><span data-stu-id="e43e4-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="e43e4-107">Hægt er að tengja fyrirliggjandi færslur eða stofna og tengja nýjar færslur.</span><span class="sxs-lookup"><span data-stu-id="e43e4-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="e43e4-108">Tenging og samstilling gagna við er aðeins í boði ef kerfisstjórinn hefur búið til tengingu milli [!INCLUDE[d365fin](includes/d365fin_md.md)] og Common Data Service eða [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e43e4-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="e43e4-109">Fljótleg leið til að athuga þetta er að opna spjaldið **Viðskiptamaður** og leita að aðgerðinni **Setja upp tengingu** .</span><span class="sxs-lookup"><span data-stu-id="e43e4-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="e43e4-110">Ef aðgerðin er tiltæk eru forritin tengd.</span><span class="sxs-lookup"><span data-stu-id="e43e4-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="e43e4-111">Myndbandsdæmi</span><span class="sxs-lookup"><span data-stu-id="e43e4-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="e43e4-112">Til að tengja færslu</span><span class="sxs-lookup"><span data-stu-id="e43e4-112">To couple a record</span></span>  
1.  <span data-ttu-id="e43e4-113">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] skal opna spjaldið fyrir færsluna sem á að tengja.</span><span class="sxs-lookup"><span data-stu-id="e43e4-113">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="e43e4-114">Til dæmis viðskiptamanna- eða tengiliðaspjald.</span><span class="sxs-lookup"><span data-stu-id="e43e4-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="e43e4-115">Einnig er hægt að opna listasíðu og velja færsluna sem á að tengja.</span><span class="sxs-lookup"><span data-stu-id="e43e4-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="e43e4-116">Veldu aðgerðina **Setja upp tengingu** .</span><span class="sxs-lookup"><span data-stu-id="e43e4-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="e43e4-117">Fylltu út reitina og smelltu síðan á hnappinn **Í lagi** .</span><span class="sxs-lookup"><span data-stu-id="e43e4-117">Fill in the fields, and then choose **OK** .</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="e43e4-118">Til að samstilla staka færslu</span><span class="sxs-lookup"><span data-stu-id="e43e4-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="e43e4-119">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] skal opna spjaldið fyrir færsluna sem á að tengja.</span><span class="sxs-lookup"><span data-stu-id="e43e4-119">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="e43e4-120">Til dæmis viðskiptamanna- eða tengiliðaspjald.</span><span class="sxs-lookup"><span data-stu-id="e43e4-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="e43e4-121">Veldu aðgerðina **Samstilla núna** .</span><span class="sxs-lookup"><span data-stu-id="e43e4-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="e43e4-122">Ef hægt er að samstilla færslu í aðra áttina, skal velja valkostinn sem tilgreinir átt gagnauppfærslu og velja síðan **Í lagi** .</span><span class="sxs-lookup"><span data-stu-id="e43e4-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK** .</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="e43e4-123">Að samstilla staka færslu úr [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="e43e4-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="e43e4-124">Í [!INCLUDE[crm_md](includes/crm_md.md)] skal opna skjámynd fyrir færsluna sem á að tengja.</span><span class="sxs-lookup"><span data-stu-id="e43e4-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="e43e4-125">Til dæmis skjámynd reiknings- eða tengiliðaspjalds.</span><span class="sxs-lookup"><span data-stu-id="e43e4-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="e43e4-126">Veldu aðgerðina **[!INCLUDE[d365fin](includes/d365fin_md.md)]** í borðanum til að opna og tengja færslu sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="e43e4-126">Choose the **[!INCLUDE[d365fin](includes/d365fin_md.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="e43e4-127">Aðeins er hægt að samstilla staka færslu úr [!INCLUDE[crm_md](includes/crm_md.md)] sjálfkrafa þegar **Aðeins samstilla tengdar færslur** er óvirk og samstillingaráttin er stillt á tvíátta eða „Frá samþættingartöflu“ á síðunni **Vörpun samþættingartöflu** fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="e43e4-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="e43e4-128">Frekari upplýsingar er að finna í [Vörpun á töflum og reitum fyrir samstillingu](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="e43e4-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="e43e4-129">Til að samstilla margar færslur</span><span class="sxs-lookup"><span data-stu-id="e43e4-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="e43e4-130">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er opnuð listasíða fyrir færsluna, t.d. listasíður viðskiptamanna eða tengiliða.</span><span class="sxs-lookup"><span data-stu-id="e43e4-130">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="e43e4-131">Veldu færslurnar sem á að samstilla og veldu svo aðgerðina **Samstilla núna** .</span><span class="sxs-lookup"><span data-stu-id="e43e4-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="e43e4-132">Ef hægt er að samstilla færslur í eina átt skal velja valkostinn sem tilgreinir stefnuna og velja svo **Í lagi** .</span><span class="sxs-lookup"><span data-stu-id="e43e4-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK** .</span></span>  

## <a name="see-also"></a><span data-ttu-id="e43e4-133">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="e43e4-133">See Also</span></span>  
[<span data-ttu-id="e43e4-134">Nota Dynamics 365 Sales úr Business Central</span><span class="sxs-lookup"><span data-stu-id="e43e4-134">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
