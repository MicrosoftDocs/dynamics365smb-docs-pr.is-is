---
title: Uppfærsla samþættingar við Dynamics 365 Sales
description: Fáið upplýsingar um hvernig á að færa Dynamics 365 Business Central samþættinginu við Dynamics 365 Sales yfir í nýjustu útgáfuna.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3bb6b26e011afc515fbd4f492f56b3090c56e860
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922368"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Uppfærsla samþættingar við Dynamics 365 Sales
[!INCLUDE[d365fin](includes/d365fin_md.md)] er einnig samþætt við [!INCLUDE[d365fin](includes/cds_long_md.md)], sem auðveldar tengingu og samstillingu gagna við önnur Dynamics 365 forrit, t.d. [!INCLUDE[crm_md](includes/crm_md.md)] eða jafnvel forrit sem þú smíðar. Ef samþætting er gerð í fyrsta skipti er mælt með því að gera hana í gegnum [!INCLUDE[d365fin](includes/cds_long_md.md)]. Frekari upplýsingar er að finna í [Samþætting við Common Data Service](admin-common-data-service.md).

Ef þegar er búið að samþætta [!INCLUDE[crm_md](includes/crm_md.md)] við [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að halda áfram að samstilla gögn með uppsetningunni. Ef þú hins vegar uppfærir [!INCLUDE[d365fin](includes/d365fin_md.md)] eða slekkur á [!INCLUDE[crm_md](includes/crm_md.md)]-samþættingunni, þarftu að tengjst í gegnum [!INCLUDE[d365fin](includes/cds_long_md.md)] til að kveikja á henni aftur. 

> [!NOTE]
> Endurtenging um [!INCLUDE[d365fin](includes/cds_long_md.md)] mun nota sjálfgefnar samstillingarstillingar og mun skrifa yfir allar grunnstillingar sem eru til staðar. Til dæmis verða sjálfgefnar töfluvarpanir notaðar.

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a>Tenging uppfærð til að nota Common Data Service
1. Opnið síðuna **Uppsetning tengingar Microsoft Dynamics 365** , veljið víxlhnappinn **Virkja** til að slökkva á núverandi tengingu við [!INCLUDE[crm_md](includes/crm_md.md)].
2. Opnið síðuna **Common Data Service Uppsetning tengingar** og veljið víxlhnappinn **Virkja** til að kveikja á tengingunni.
  
   Þegar kveikt er á CDS-tengingunni er CDS-grunnsamþættingarlausn Business Central virkjuð í Common Data Service.
3. Fjarlægja þarf Microsoft Dynamics 365 Business Central Samþættingarlausn úr Dynamics 365 Sales. Frekari upplýsingar er að finna í [Fjarlægja eða eyða efnisatriðum lausnar](/powerapps/developer/common-data-service/uninstall-delete-solution). 

4. Á síðunni **Microsoft Dynamics 365 uppsetning tengingar** skal kveikja á **Virkja** til að kveikja á núverandi tengingu við [!INCLUDE[crm_md](includes/crm_md.md)].
  
   Þegar kveikt er á tengingu Sales er samþættingarlausn Business Central virkjuð í Sales. Þetta virkjar samþættingu við einingar sem eru sértækar fyrir [!INCLUDE[crm_md](includes/crm_md.md)], svo sem sölupantanir, tilboð og reikningar.
5. Á síðunni **Uppsetning Sales-tengingar** , veljið **Nota sjálfgefinn samstillingargrunn** til að frumstilla varpanir samþættingartöflu fyrir [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Sjá einnig
[Samþætting við Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Samþætting við Common Data Service](admin-common-data-service.md)
