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
ms.openlocfilehash: 4e3b79d6245a0f1b8277c94faa58c24edc66662e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777017"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Uppfærsla samþættingar við Dynamics 365 Sales
[!INCLUDE[prod_short](includes/prod_short.md)] er einnig samþætt við [!INCLUDE[prod_short](includes/cds_long_md.md)], sem auðveldar tengingu og samstillingu gagna við önnur Dynamics 365 forrit, t.d. [!INCLUDE[crm_md](includes/crm_md.md)] eða jafnvel forrit sem þú smíðar. Ef samþætting er gerð í fyrsta skipti er mælt með því að gera hana í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)]. Frekari upplýsingar er að finna í [Samþætting við Dataverse](admin-common-data-service.md).

Ef þegar er búið að samþætta [!INCLUDE[crm_md](includes/crm_md.md)] við [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að halda áfram að samstilla gögn með uppsetningunni. Ef þú hins vegar uppfærir [!INCLUDE[prod_short](includes/prod_short.md)] eða slekkur á [!INCLUDE[crm_md](includes/crm_md.md)]-samþættingunni, þarftu að tengjst í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)] til að kveikja á henni aftur. 

> [!NOTE]
> Endurtenging um [!INCLUDE[prod_short](includes/cds_long_md.md)] mun nota sjálfgefnar samstillingarstillingar og mun skrifa yfir allar grunnstillingar sem eru til staðar. Til dæmis verða sjálfgefnar töfluvarpanir notaðar.

## <a name="to-upgrade-your-connection-to-use-dataverse"></a>Tenging uppfærð til að nota Dataverse
1. Opnaðu síðuna **Microsoft Dynamics 365 uppsetning tengingar** og slökktu á víxlhnappinum **Virkja** til að aftengjast við [!INCLUDE[crm_md](includes/crm_md.md)].
2. Opnið síðuna **Dataverse Uppsetning tengingar** og veljið víxlhnappinn **Virkjað** til að kveikja á tengingunni við [!INCLUDE[prod_short](includes/cds_long_md.md)].
  
   > [!NOTE]
   > Þegar kveikt er á tengingunni er samþættingarlausn Business Central virkjuð í Dataverse.
3. Veldu **Endurvirkja samþættingarlausn** til að setja aftur upp samþættingarlausn Business Central.
4. Á síðunni **Microsoft Dynamics 365 uppsetning tengingar** skal kveikja á **Virkja** til að tengja aftur við [!INCLUDE[crm_md](includes/crm_md.md)].
  
   > [!NOTE]
   > Þegar kveikt er á tengingunni er samþættingarlausn Business Central virkjuð í [!INCLUDE[prod_short](includes/prod_short.md)]. Þetta virkjar samþættingu við töflur sem eru sértækar fyrir [!INCLUDE[crm_md](includes/crm_md.md)], svo sem sölupantanir, tilboð og reikningar.
5. Veldu **Endurvirkja samþættingarlausn** til að setja aftur upp samþættingarlausn Business Central.
6. Á síðunni **Uppsetning Sales-tengingar**, veljið **Nota sjálfgefinn samstillingargrunn** til að frumstilla varpanir samþættingartöflu fyrir [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Sjá einnig
[Samþætting við Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Samþætting við Microsoft Dataverse](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]