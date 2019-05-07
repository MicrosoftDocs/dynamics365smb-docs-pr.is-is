---
title: Tengja og samstilla færslur handvirkt| Microsoft Docs
description: Samstilling samþættingartöflu virkjar gagnasamþættingu í öllum færslum í töflu í Business Central og Dynamics 365 for Sales-einingu sem eru tengdar.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 36f1a0fe8c50744d9ce13d1e6c3c899f4ceaf5e4
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "940217"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="6520a-103">Tengja og samstilla færslur handvirkt</span><span class="sxs-lookup"><span data-stu-id="6520a-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="6520a-104">Þetta efnisatriði lýsir því hvernig á að tengja eina eða fleiri færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] við færslur í [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6520a-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="6520a-105">Að tengja færslur gerir þér kleift að skoða [!INCLUDE[crm_md](includes/crm_md.md)] upplýsingar úr [!INCLUDE[d365fin](includes/d365fin_md.md)] og öfugt.</span><span class="sxs-lookup"><span data-stu-id="6520a-105">Coupling records lets you view [!INCLUDE[crm_md](includes/crm_md.md)] information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="6520a-106">Tenging gerir þér einnig að samstilla gögn á milli færslna.</span><span class="sxs-lookup"><span data-stu-id="6520a-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="6520a-107">Hægt er að tengja fyrirliggjandi færslur eða stofna og tengja nýjar færslur.</span><span class="sxs-lookup"><span data-stu-id="6520a-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="6520a-108">Tenging og samstilling gagna við [!INCLUDE[crm_md](includes/crm_md.md)] er aðeins hægt ef kerfisstjórinn hefur búið til tengingu milli [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6520a-108">Coupling and synchronizing data with [!INCLUDE[crm_md](includes/crm_md.md)] is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="6520a-109">Fljótleg leið til að athuga þetta er að opna spjaldið **Viðskiptamaður** og leita að aðgerðinni **Setja upp tengingu**.</span><span class="sxs-lookup"><span data-stu-id="6520a-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="6520a-110">Ef aðgerðin er tiltæk eru forritin tengd.</span><span class="sxs-lookup"><span data-stu-id="6520a-110">If the action is available, the apps are connected.</span></span>   

## <a name="to-couple-a-record"></a><span data-ttu-id="6520a-111">Til að tengja færslu</span><span class="sxs-lookup"><span data-stu-id="6520a-111">To couple a record</span></span>  
1.  <span data-ttu-id="6520a-112">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] skal opna spjaldið fyrir færsluna sem á að tengja.</span><span class="sxs-lookup"><span data-stu-id="6520a-112">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="6520a-113">Til dæmis viðskiptamanna- eða tengiliðaspjald.</span><span class="sxs-lookup"><span data-stu-id="6520a-113">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="6520a-114">Einnig er hægt að opna listasíðu og velja færsluna sem á að tengja.</span><span class="sxs-lookup"><span data-stu-id="6520a-114">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="6520a-115">Veldu aðgerðina **Setja upp tengingu**.</span><span class="sxs-lookup"><span data-stu-id="6520a-115">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="6520a-116">Fylltu út reitina og smelltu síðan á hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6520a-116">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="6520a-117">Til að samstilla staka færslu</span><span class="sxs-lookup"><span data-stu-id="6520a-117">To synchronize a single record</span></span>  
1.  <span data-ttu-id="6520a-118">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] skal opna spjaldið fyrir færsluna sem á að tengja.</span><span class="sxs-lookup"><span data-stu-id="6520a-118">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="6520a-119">Til dæmis viðskiptamanna- eða tengiliðaspjald.</span><span class="sxs-lookup"><span data-stu-id="6520a-119">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="6520a-120">Veldu aðgerðina **Samstilla núna**.</span><span class="sxs-lookup"><span data-stu-id="6520a-120">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="6520a-121">Ef hægt er að samstilla færslu ýmist úr [!INCLUDE[d365fin](includes/d365fin_md.md)] í [!INCLUDE[crm_md](includes/crm_md.md)] eða úr [!INCLUDE[crm_md](includes/crm_md.md)] í [!INCLUDE[d365fin](includes/d365fin_md.md)], skal velja valkostinn sem tilgreinir stefnu gagnauppfærslunnar og velja svo **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6520a-121">If a record can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="6520a-122">Til að samstilla margar færslur</span><span class="sxs-lookup"><span data-stu-id="6520a-122">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="6520a-123">Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er opnuð listasíða fyrir færsluna, t.d. listasíður viðskiptamanna eða tengiliða.</span><span class="sxs-lookup"><span data-stu-id="6520a-123">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="6520a-124">Veldu færslurnar sem á að samstilla og veldu svo aðgerðina **Samstilla núna**.</span><span class="sxs-lookup"><span data-stu-id="6520a-124">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="6520a-125">Ef hægt er að samstilla færslur ýmist úr [!INCLUDE[d365fin](includes/d365fin_md.md)] í [!INCLUDE[crm_md](includes/crm_md.md)] eða úr [!INCLUDE[crm_md](includes/crm_md.md)] í [!INCLUDE[d365fin](includes/d365fin_md.md)], skal velja valkostinn sem tilgreinir stefnu gagnauppfærslunnar og velja svo **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6520a-125">If records can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6520a-126">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="6520a-126">See Also</span></span>  
[<span data-ttu-id="6520a-127">Að nota Dynamics 365 for Sales úr Business Central</span><span class="sxs-lookup"><span data-stu-id="6520a-127">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
