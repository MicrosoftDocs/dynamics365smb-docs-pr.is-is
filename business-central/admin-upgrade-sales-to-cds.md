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
ms.openlocfilehash: 95098397bd9554be6c993b6107963eba9a99c067
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196868"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Uppfærsla samþættingar við Dynamics 365 Sales
[!INCLUDE[d365fin](includes/d365fin_md.md)] er einnig samþætt við [!INCLUDE[d365fin](includes/cds_long_md.md)], sem auðveldar tengingu og samstillingu gagna við önnur Dynamics 365 forrit, t.d. [!INCLUDE[crm_md](includes/crm_md.md)] eða jafnvel forrit sem þú smíðar. Ef samþætting er gerð í fyrsta skipti er mælt með því að gera hana í gegnum [!INCLUDE[d365fin](includes/cds_long_md.md)]. Frekari upplýsingar er að finna í [Samþætting við Common Data Service](admin-common-data-service.md).

Ef þegar er búið að samþætta [!INCLUDE[crm_md](includes/crm_md.md)] við [!INCLUDE[d365fin](includes/d365fin_md.md)] er hægt að halda áfram að samstilla gögn með uppsetningunni. Ef þú hins vegar uppfærir [!INCLUDE[d365fin](includes/d365fin_md.md)] eða slekkur á [!INCLUDE[crm_md](includes/crm_md.md)]-samþættingunni, þarftu að tengjst í gegnum [!INCLUDE[d365fin](includes/cds_long_md.md)] til að kveikja á henni aftur. 

> [!NOTE]
> Endurtenging um [!INCLUDE[d365fin](includes/cds_long_md.md)] mun nota sjálfgefnar samstillingarstillingar og mun skrifa yfir allar grunnstillingar sem eru til staðar. Til dæmis verða sjálfgefnar töfluvarpanir notaðar.

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a>Tenging uppfærð til að nota Common Data Service
1. Opnið síðuna **Uppsetning tengingar Microsoft Dynamics 365**, veljið víxlhnappinn **Virkja** til að slökkva á núverandi tengingu við [!INCLUDE[crm_md](includes/crm_md.md)].
2. Opnið síðuna **Common Data Service Uppsetning tengingar** og veljið víxlhnappinn **Virkja** til að kveikja á tengingunni.
3. Þegar kveikt er á CDS-tengingunni er CDS-grunnsamþættingarlausn Business Central virkjuð í Common Data Service.
4. Á síðunni Uppsetning tengingar Microsoft Dynamics 365, veljið víxlhnappinn Virkja til að kveikja á núverandi tengingu við [!INCLUDE[crm_md](includes/crm_md.md)].
5. Þegar kveikt er á tengingu Sales er samþættingarlausn Business Central virkjuð í Sales. Þetta virkjar samþættingu við einingar sem eru sértækar fyrir [!INCLUDE[crm_md](includes/crm_md.md)], svo sem sölupantanir, tilboð og reikningar.
6. Á síðunni **Uppsetning Sales-tengingar**, veljið **Nota sjálfgefinn samstillingargrunn** til að frumstilla varpanir samþættingartöflu fyrir [!INCLUDE[crm_md](includes/crm_md.md)].
7. Veljið nú **Endurvirkja samþættingarlausn** til að setja upp og grunnstilla uppfærða samþættingarlausn Business Central.

## <a name="see-also"></a>Sjá einnig
[Samþætting við Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Samþætting við Common Data Service](admin-common-data-service.md)