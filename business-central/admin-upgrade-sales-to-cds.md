---
title: Uppfærsla samþættingar við Dynamics 365 Sales
description: Í þessu efnisatriði er talað um hvernig á að færa Dynamics 365 Business Central samþættinginu við Dynamics 365 Sales yfir í nýjustu útgáfuna.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: c6405326890b8f33b399f880e54d0fcf14db1650
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543021"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Uppfærsla samþættingar við Dynamics 365 Sales
[!INCLUDE[prod_short](includes/prod_short.md)] er einnig samþætt við [!INCLUDE[prod_short](includes/cds_long_md.md)], sem auðveldar tengingu og samstillingu gagna við önnur Dynamics 365 forrit, t.d. [!INCLUDE[crm_md](includes/crm_md.md)] eða jafnvel forrit sem þú smíðar. Ef samþætting er gerð í fyrsta skipti er mælt með því að gera hana í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)]. Frekari upplýsingar er að finna í [Samþætting við Dataverse](admin-common-data-service.md).

Ef þegar er búið að samþætta [!INCLUDE[crm_md](includes/crm_md.md)] við [!INCLUDE[prod_short](includes/prod_short.md)] er hægt að halda áfram að samstilla gögn með uppsetningunni. Ef þú hins vegar uppfærir [!INCLUDE[prod_short](includes/prod_short.md)] eða slekkur á [!INCLUDE[crm_md](includes/crm_md.md)]-samþættingunni, þarftu að tengjst í gegnum [!INCLUDE[prod_short](includes/cds_long_md.md)] til að kveikja á henni aftur. 

> [!NOTE]
> Endurtenging um [!INCLUDE[prod_short](includes/cds_long_md.md)] mun nota sjálfgefnar samstillingarstillingar og mun skrifa yfir allar grunnstillingar sem eru til staðar. Til dæmis verða sjálfgefnar töfluvarpanir notaðar.

## <a name="to-upgrade-your-connection-to-use-dataverse"></a>Tenging uppfærð til að nota Dataverse
1. Opnaðu síðuna **Microsoft Dynamics uppsetning 365-tengingar** og slökktu á víxlhnappinum **Virkja**. Lokaðu síðan síðunni til að aftengjast [!INCLUDE[crm_md](includes/crm_md.md)].
2. Opnaðu síðuna **Dataverse uppsetning tengingar** og í reitnum **Eignarhaldslíkan** skal velja **Einstaklingur**. Síðan skal velja víxlhnappinn **Virkja** til að kveikja á tengingunni við [!INCLUDE[prod_short](includes/cds_long_md.md)].
  
   > [!NOTE]
   > Þegar kveikt er á tengingunni er samþættingarlausn Business Central virkjuð í Dataverse.
4. Á síðunni **Microsoft Dynamics Uppsetning 365-tengingar** skal velja **Endurvirkja samþættingarlausn** til að setja aftur upp samþættingarlausn Business Central.
5. Kveiktu á **Virkja** til að tengjast aftur við [!INCLUDE[crm_md](includes/crm_md.md)].
  
   > [!NOTE]
   > Þegar kveikt er á tengingunni er samþættingarlausn Business Central virkjuð í [!INCLUDE[prod_short](includes/prod_short.md)]. Þetta virkjar samþættingu við töflur sem eru sértækar fyrir [!INCLUDE[crm_md](includes/crm_md.md)], svo sem sölupantanir, tilboð og reikningar.
6. Á síðunni **Uppsetning Sales-tengingar**, veljið **Nota sjálfgefinn samstillingargrunn** til að frumstilla varpanir samþættingartöflu fyrir [!INCLUDE[crm_md](includes/crm_md.md)].

   > [!IMPORTANT]
   > Notkun á aðgerðinni **Nota sjálfgefinn samstillingargrunn** mun beita sjálfgefnum vörpunum samþættingartaflna. Skrifað verður yfir allar sérsniðnar varpanir. Ef sérsniðnar varpanir eru til staðar sem þú vilt geyma mælum við með að þú flytjir þær út í Excel eða ræðir við Microsoft samstarfsaðila þinn um aðrar leiðir til að geyma sérsniðnar varpanir.    

## <a name="see-also"></a>Sjá einnig
[Samþætting við Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Samþætting við Microsoft Dataverse](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]