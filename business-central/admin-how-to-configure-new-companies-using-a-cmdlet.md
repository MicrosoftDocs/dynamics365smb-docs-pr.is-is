---
title: "Hvernig á að grunnstilla ný fyrirtæki með Cmdlet | Microsoft Docs"
description: "Í mörgum tilfellum getur þú vlijað hlaða og flytja inn stillingapakka án þátttöku notenda eða nota notendaviðmót RapidStart Services. Það er gert með því að nota Windows PowerShell smáskipun."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ce8bfdb40d8d428f4b02abcbba4498d58d6481be
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a>Grunnstilla ný fyrirtæki með Cmdlet
Í mörgum tilfellum getur þú vlijað hlaða og flytja inn stillingapakka án þátttöku notenda eða nota notendaviðmót RapidStart Services. Það er gert með því að nota Windows PowerShell smáskipun. Atburðarás þar sem þetta getur verið gagnlegt eru:  

- Gagnainnflutningur þvert yfir margar uppsetningar [!INCLUDE[d365fin](includes/d365fin_md.md)].
- Grunnstilli viðbótarnotkunarsvið fyrir marga viðskiptavini.  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a>Að nota uppsetningarpakka með cmdlet  

1. Undirbúa RapidStart Services pakkann. Til dæmis er hægt að búa til pakka til að flytja inn tiltekin gildi og heiti töflunnar og reitanna sem á að setja gildin inn í.  
2. Setjið pakkann upp í tölvunni þar sem cmdlet verður keyrt.  
3. Opna stjórnunarskelina [!INCLUDE[d365fin](includes/d365fin_md.md)].  
4. Færið inn **Invoke-NAVCodeUnit** og tilgreinið upplýsingar eins og þær sem sjá má í eftirfarandi dæmi.  
    ```powershell  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
Cmdlet flytur pakkann inn í hvert fyrirtæki. Notendur geta byrjað að nota nýja virkni strax.  

## <a name="see-also"></a>Sjá einnig  
[Grunnstilla ný fyrirtæki](admin-how-to-configure-new-companies.md)  
[Nota skilgreiningu á ný fyrirtæki](admin-apply-configuration-to-new-companies.md)  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)  
[Microsoft Dynamics NAV Windows PowerShell Cmdlets](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

