---
title: Uppfærsla samþættingar við Dynamics 365 Sales
description: Fáið upplýsingar um hvernig á að færa Dynamics 365 Business Central samþættinginu við Dynamics 365 Sales yfir í nýjustu útgáfuna.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 772052fc88e0b8be7ec5276600b0c237e2d2f8b2
ms.sourcegitcommit: a76475f124e79440a5bba20577b335c4d50a2d83
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025809"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="a61d0-103">Uppfærsla samþættingar við Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="a61d0-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="a61d0-104">er einnig samþætt við [!INCLUDE[prod_short](includes/cds_long_md.md)], sem auðveldar tengingu og samstillingu gagna við önnur Dynamics 365 forrit, t.d. [!INCLUDE[crm_md](includes/crm_md.md)] eða jafnvel forrit sem þú smíðar.</span><span class="sxs-lookup"><span data-stu-id="a61d0-104">integrates with [!INCLUDE[prod_short](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="a61d0-105">Ef samþætting er gerð í fyrsta skipti er mælt með því að gera hana í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a61d0-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> <span data-ttu-id="a61d0-106">Frekari upplýsingar er að finna í [Samþætting við Dataverse](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="a61d0-106">For more information, see [Integration with Dataverse](admin-common-data-service.md).</span></span>

<span data-ttu-id="a61d0-107">Ef þegar er búið að samþætta [!INCLUDE[crm_md](includes/crm_md.md)] við [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að halda áfram að samstilla gögn með uppsetningunni.</span><span class="sxs-lookup"><span data-stu-id="a61d0-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[prod_short](includes/prod_short.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="a61d0-108">Ef þú hins vegar uppfærir [!INCLUDE[prod_short](includes/prod_short.md)] eða slekkur á [!INCLUDE[crm_md](includes/crm_md.md)]-samþættingunni, þarftu að tengjst í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)] til að kveikja á henni aftur.</span><span class="sxs-lookup"><span data-stu-id="a61d0-108">However, if you upgrade [!INCLUDE[prod_short](includes/prod_short.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="a61d0-109">Endurtenging um [!INCLUDE[prod_short](includes/cds_long_md.md)] mun nota sjálfgefnar samstillingarstillingar og mun skrifa yfir allar grunnstillingar sem eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="a61d0-109">Reconnecting through [!INCLUDE[prod_short](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="a61d0-110">Til dæmis verða sjálfgefnar töfluvarpanir notaðar.</span><span class="sxs-lookup"><span data-stu-id="a61d0-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-dataverse"></a><span data-ttu-id="a61d0-111">Tenging uppfærð til að nota Dataverse</span><span class="sxs-lookup"><span data-stu-id="a61d0-111">To upgrade your connection to use Dataverse</span></span>
1. <span data-ttu-id="a61d0-112">Opnaðu síðuna **Microsoft Dynamics 365 uppsetning tengingar** og slökktu á víxlhnappinum **Virkja** til að aftengjast við [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a61d0-112">Open the **Microsoft Dynamics 365 Connection Setup** page, and then turn off the **Enabled** toggle to disconnect from [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="a61d0-113">Opnið síðuna **Dataverse Uppsetning tengingar** og veljið víxlhnappinn **Virkjað** til að kveikja á tengingunni við [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a61d0-113">Open the **Dataverse Connection Setup** page, and choose the **Enabled** toggle to turn on the connection to [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="a61d0-114">Þegar kveikt er á tengingunni er samþættingarlausn Business Central virkjuð í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="a61d0-114">After you enable the connection, the Business Central Integration Solution is deployed to Dataverse.</span></span>
3. <span data-ttu-id="a61d0-115">Veldu **Endurvirkja samþættingarlausn** til að setja aftur upp samþættingarlausn Business Central.</span><span class="sxs-lookup"><span data-stu-id="a61d0-115">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
4. <span data-ttu-id="a61d0-116">Á síðunni **Microsoft Dynamics 365 uppsetning tengingar** skal kveikja á **Virkja** til að tengja aftur við [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a61d0-116">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enabled** toggle to reconnect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="a61d0-117">Þegar kveikt er á tengingunni er samþættingarlausn Business Central virkjuð í [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="a61d0-117">After you enable the connection, the Business Central Integration Solution is deployed to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="a61d0-118">Þetta virkjar samþættingu við töflur sem eru sértækar fyrir [!INCLUDE[crm_md](includes/crm_md.md)], svo sem sölupantanir, tilboð og reikningar.</span><span class="sxs-lookup"><span data-stu-id="a61d0-118">This enables integration with tables that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="a61d0-119">Veldu **Endurvirkja samþættingarlausn** til að setja aftur upp samþættingarlausn Business Central.</span><span class="sxs-lookup"><span data-stu-id="a61d0-119">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
6. <span data-ttu-id="a61d0-120">Á síðunni **Uppsetning Sales-tengingar**, veljið **Nota sjálfgefinn samstillingargrunn** til að frumstilla varpanir samþættingartöflu fyrir [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a61d0-120">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="a61d0-121">Notkun á aðgerðinni **Nota sjálfgefinn samstillingargrunn** mun beita sjálfgefnum vörpunum samþættingartaflna.</span><span class="sxs-lookup"><span data-stu-id="a61d0-121">Using the **Use Default Synchronization Setup** action will apply the default integration table mappings.</span></span> <span data-ttu-id="a61d0-122">Skrifað verður yfir allar sérsniðnar varpanir.</span><span class="sxs-lookup"><span data-stu-id="a61d0-122">All custom mappings will be overwritten.</span></span> <span data-ttu-id="a61d0-123">Ef sérsniðnar varpanir eru til staðar sem þú vilt geyma mælum við með að þú flytjir þær út í Excel eða ræðir við Microsoft samstarfsaðila þinn um aðrar leiðir til að geyma sérsniðnar varpanir.</span><span class="sxs-lookup"><span data-stu-id="a61d0-123">If you have custom mappings that you want to keep, we recommend that you export them to Excel or talk to your Microsoft partner about other ways to keep your custom mappings.</span></span>    

## <a name="see-also"></a><span data-ttu-id="a61d0-124">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a61d0-124">See Also</span></span>
[<span data-ttu-id="a61d0-125">Samþætting við Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="a61d0-125">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="a61d0-126">Samþætting við Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="a61d0-126">Integrating with Microsoft Dataverse</span></span>](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]