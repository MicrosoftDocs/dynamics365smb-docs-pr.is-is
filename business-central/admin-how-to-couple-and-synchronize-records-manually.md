---
title: Tenging og samstilling | Microsoft docs
description: Samstilling samþættingartöflu virkjar gagnasamþættingu í öllum færslum í töflu í Business Central og Dynamics 365 Sales töflu sem eru tengdar.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 53b12b6ab7e53a20bb1b8fcc659b2f1454e85321
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779933"
---
# <a name="coupling-and-synchronizing"></a><span data-ttu-id="8b687-103">Tenging og samstilling</span><span class="sxs-lookup"><span data-stu-id="8b687-103">Coupling and Synchronizing</span></span>
<span data-ttu-id="8b687-104">Þetta efnisatriði lýsir því hvernig á að tengja eina eða fleiri færslur í [!INCLUDE[prod_short](includes/prod_short.md)] við færslur í Dataverse eða [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8b687-104">This topic describes how to couple one or more records in [!INCLUDE[prod_short](includes/prod_short.md)] with records in Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="8b687-105">Að tengja færslur gerir þér kleift að skoða Dataverse upplýsingar úr [!INCLUDE[prod_short](includes/prod_short.md)] og öfugt.</span><span class="sxs-lookup"><span data-stu-id="8b687-105">Coupling records lets you view Dataverse information from [!INCLUDE[prod_short](includes/prod_short.md)], and vice versa.</span></span> <span data-ttu-id="8b687-106">Tenging gerir þér einnig að samstilla gögn á milli færslna.</span><span class="sxs-lookup"><span data-stu-id="8b687-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="8b687-107">Hægt er að tengja fyrirliggjandi færslur eða stofna og tengja nýjar færslur.</span><span class="sxs-lookup"><span data-stu-id="8b687-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="8b687-108">Tenging og samstilling gagna við er aðeins í boði ef kerfisstjórinn hefur búið til tengingu milli [!INCLUDE[prod_short](includes/prod_short.md)] og Dataverse eða [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8b687-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[prod_short](includes/prod_short.md)] and Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="8b687-109">Fljótleg leið til að athuga þetta er að opna spjaldið **Viðskiptamaður** og leita að aðgerðinni **Setja upp tengingu**.</span><span class="sxs-lookup"><span data-stu-id="8b687-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="8b687-110">Ef aðgerðin er tiltæk eru forritin tengd.</span><span class="sxs-lookup"><span data-stu-id="8b687-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="8b687-111">Myndbandsdæmi</span><span class="sxs-lookup"><span data-stu-id="8b687-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="8b687-112">Til að tengja færslu</span><span class="sxs-lookup"><span data-stu-id="8b687-112">To couple a record</span></span>  
1.  <span data-ttu-id="8b687-113">Í [!INCLUDE[prod_short](includes/prod_short.md)] skal opna spjaldið fyrir færsluna sem á að tengja.</span><span class="sxs-lookup"><span data-stu-id="8b687-113">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="8b687-114">Til dæmis viðskiptamanna- eða tengiliðaspjald.</span><span class="sxs-lookup"><span data-stu-id="8b687-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="8b687-115">Einnig er hægt að opna listasíðu og velja færsluna sem á að tengja.</span><span class="sxs-lookup"><span data-stu-id="8b687-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="8b687-116">Veldu aðgerðina **Setja upp tengingu**.</span><span class="sxs-lookup"><span data-stu-id="8b687-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="8b687-117">Fylltu út reitina og smelltu síðan á hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="8b687-117">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="8b687-118">Til að samstilla staka færslu</span><span class="sxs-lookup"><span data-stu-id="8b687-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="8b687-119">Í [!INCLUDE[prod_short](includes/prod_short.md)] skal opna spjaldið fyrir færsluna sem á að tengja.</span><span class="sxs-lookup"><span data-stu-id="8b687-119">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="8b687-120">Til dæmis viðskiptamanna- eða tengiliðaspjald.</span><span class="sxs-lookup"><span data-stu-id="8b687-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="8b687-121">Veldu aðgerðina **Samstilla núna**.</span><span class="sxs-lookup"><span data-stu-id="8b687-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="8b687-122">Ef hægt er að samstilla færslu í aðra áttina, skal velja valkostinn sem tilgreinir átt gagnauppfærslu og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="8b687-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="8b687-123">Að samstilla staka færslu úr [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="8b687-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="8b687-124">Í [!INCLUDE[crm_md](includes/crm_md.md)] skal opna skjámynd fyrir færsluna sem á að tengja.</span><span class="sxs-lookup"><span data-stu-id="8b687-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="8b687-125">Til dæmis skjámynd reiknings- eða tengiliðaspjalds.</span><span class="sxs-lookup"><span data-stu-id="8b687-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="8b687-126">Veldu aðgerðina **[!INCLUDE[prod_short](includes/prod_short.md)]** í borðanum til að opna og tengja færslu sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="8b687-126">Choose the **[!INCLUDE[prod_short](includes/prod_short.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="8b687-127">Aðeins er hægt að samstilla staka færslu úr [!INCLUDE[crm_md](includes/crm_md.md)] sjálfkrafa þegar **Aðeins samstilla tengdar færslur** er óvirk og samstillingaráttin er stillt á tvíátta eða „Frá samþættingartöflu“ á síðunni **Vörpun samþættingartöflu** fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="8b687-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="8b687-128">Frekari upplýsingar er að finna í [Vörpun á töflum og reitum fyrir samstillingu](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="8b687-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="8b687-129">Til að samstilla margar færslur</span><span class="sxs-lookup"><span data-stu-id="8b687-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="8b687-130">Í [!INCLUDE[prod_short](includes/prod_short.md)] er opnuð listasíða fyrir færsluna, t.d. listasíður viðskiptamanna eða tengiliða.</span><span class="sxs-lookup"><span data-stu-id="8b687-130">In [!INCLUDE[prod_short](includes/prod_short.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="8b687-131">Veldu færslurnar sem á að samstilla og veldu svo aðgerðina **Samstilla núna**.</span><span class="sxs-lookup"><span data-stu-id="8b687-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="8b687-132">Ef hægt er að samstilla færslur í eina átt skal velja valkostinn sem tilgreinir stefnuna og velja svo **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="8b687-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK**.</span></span>  

## <a name="uncoupling-records"></a><span data-ttu-id="8b687-133">Aftengja færslur</span><span class="sxs-lookup"><span data-stu-id="8b687-133">Uncoupling Records</span></span>
<span data-ttu-id="8b687-134">Hægt er að aftengja eina eða fleiri færslur af listasíðum eða síðunni **Samstillingarvillur í tengdum gögnum** með því að velja eina eða fleiri línu og velja **Eyða tengingu**.</span><span class="sxs-lookup"><span data-stu-id="8b687-134">You can uncouple one or more records from list pages or the **Coupled Data Synchronization Errors** page by choosing one or more lines and choosing **Delete Coupling**.</span></span> <span data-ttu-id="8b687-135">Einnig er hægt að fjarlægja allar tengingar fyrir eina eða fleiri töfluvörpun á síðunni **Vörpun samþættingartöflu**.</span><span class="sxs-lookup"><span data-stu-id="8b687-135">You can also remove all couplings for one or more table mappings on the **Integration Table Mappings** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="8b687-136">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="8b687-136">See Also</span></span>  
[<span data-ttu-id="8b687-137">Nota Dynamics 365 Sales úr Business Central</span><span class="sxs-lookup"><span data-stu-id="8b687-137">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]