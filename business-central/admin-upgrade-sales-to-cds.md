---
title: Uppfærsla samþættingar við Dynamics 365 Sales| Microsoft Docs
description: Kynntu þér hvernig þú sækir Dynamics 365 Business Central tilbúið til að samþætta við Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 84e335bacbfec965968d6a6839fe1eb407ab089d
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324127"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="5207b-103">Uppfærsla samþættingar við Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="5207b-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="5207b-104">er einnig samþætt við [!INCLUDE[d365fin](includes/cds_long_md.md)], sem auðveldar tengingu og samstillingu gagna við önnur Dynamics 365 forrit, t.d. [!INCLUDE[crm_md](includes/crm_md.md)] eða jafnvel forrit sem þú smíðar.</span><span class="sxs-lookup"><span data-stu-id="5207b-104">integrates with [!INCLUDE[d365fin](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="5207b-105">Ef samþætting er gerð í fyrsta skipti er mælt með því að gera hana í gegnum [!INCLUDE[d365fin](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5207b-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> <span data-ttu-id="5207b-106">Frekari upplýsingar er að finna í [Samþætting við Common Data Service](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="5207b-106">For more information, see [Integration with Common Data Service](admin-common-data-service.md).</span></span>

<span data-ttu-id="5207b-107">Ef þegar er búið að samþætta [!INCLUDE[crm_md](includes/crm_md.md)] við [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að halda áfram að samstilla gögn með uppsetningunni.</span><span class="sxs-lookup"><span data-stu-id="5207b-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="5207b-108">Ef þú hins vegar uppfærir [!INCLUDE[d365fin](includes/d365fin_md.md)] eða slekkur á [!INCLUDE[crm_md](includes/crm_md.md)]-samþættingunni, þarftu að tengjst í gegnum [!INCLUDE[d365fin](includes/cds_long_md.md)] til að kveikja á henni aftur.</span><span class="sxs-lookup"><span data-stu-id="5207b-108">However, if you upgrade [!INCLUDE[d365fin](includes/d365fin_md.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="5207b-109">Endurtenging um [!INCLUDE[d365fin](includes/cds_long_md.md)] mun nota sjálfgefnar samstillingarstillingar og mun skrifa yfir allar grunnstillingar sem eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="5207b-109">Reconnecting through [!INCLUDE[d365fin](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="5207b-110">Til dæmis verða sjálfgefnar töfluvarpanir notaðar.</span><span class="sxs-lookup"><span data-stu-id="5207b-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a><span data-ttu-id="5207b-111">Tenging uppfærð til að nota Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5207b-111">To upgrade your connection to use Common Data Service</span></span>
1. <span data-ttu-id="5207b-112">Opnið síðuna **Uppsetning tengingar Microsoft Dynamics 365**, veljið víxlhnappinn **Virkja** til að slökkva á núverandi tengingu við [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5207b-112">Open the **Microsoft Dynamics 365 Connection Setup** page, choose the **Enable** toggle to turn off your existing connection to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="5207b-113">Opnið síðuna **Common Data Service Uppsetning tengingar** og veljið víxlhnappinn **Virkja** til að kveikja á tengingunni.</span><span class="sxs-lookup"><span data-stu-id="5207b-113">Open the **Common Data Service Connection Setup** page, and choose the **Enable** toggle to turn on the connection.</span></span>
  
   <span data-ttu-id="5207b-114">Þegar kveikt er á CDS-tengingunni er CDS-grunnsamþættingarlausn Business Central virkjuð í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="5207b-114">After you enable the CDS connection, the Business Central CDS Base Integration Solution is deployed to Common Data Service.</span></span>
3. <span data-ttu-id="5207b-115">Á síðunni Uppsetning tengingar Microsoft Dynamics 365, veljið víxlhnappinn Virkja til að kveikja á núverandi tengingu við [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5207b-115">On the Microsoft Dynamics 365 Connection Setup page, choose the Enable toggle to turn on the connection to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   <span data-ttu-id="5207b-116">Þegar kveikt er á tengingu Sales er samþættingarlausn Business Central virkjuð í Sales.</span><span class="sxs-lookup"><span data-stu-id="5207b-116">After you enable the Sales connection, the Business Central Integration Solution is deployed to Sales.</span></span> <span data-ttu-id="5207b-117">Þetta virkjar samþættingu við einingar sem eru sértækar fyrir [!INCLUDE[crm_md](includes/crm_md.md)], svo sem sölupantanir, tilboð og reikningar.</span><span class="sxs-lookup"><span data-stu-id="5207b-117">This enables integration with entities that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
4. <span data-ttu-id="5207b-118">Veljið nú **Endurvirkja samþættingarlausn** til að setja upp og grunnstilla uppfærða samþættingarlausn Business Central.</span><span class="sxs-lookup"><span data-stu-id="5207b-118">Choose **Redeploy Integration Solution** to install and configure the upgraded Business Central Integration Solution.</span></span>
5. <span data-ttu-id="5207b-119">Á síðunni **Uppsetning Sales-tengingar**, veljið **Nota sjálfgefinn samstillingargrunn** til að frumstilla varpanir samþættingartöflu fyrir [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5207b-119">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="5207b-120">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5207b-120">See Also</span></span>
[<span data-ttu-id="5207b-121">Samþætting við Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="5207b-121">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="5207b-122">Samþætting við Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5207b-122">Integrating with Common Data Service</span></span>](admin-common-data-service.md)