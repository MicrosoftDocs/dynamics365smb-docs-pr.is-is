---
title: Hönnunarupplýsingar - Sléttun | Microsoft Docs
description: Sléttunar leifar geta átt sér stað þegar þú metur kostnað af birgðaminnkun sem mælt er í öðru magni en samsvarandi birgðaaukning. Sléttunarleifar eru reiknaðar fyrir allar kostnaðarútreikninga þegar **Kostnaðarleiðrétting - Birgðafærsla** runuvinnsla er keyrð.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: d4a4893ade7d89ad7874fd489cd7a74e4ae914e2
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "921915"
---
# <a name="design-details-rounding"></a>Hönnunarupplýsingar: sléttun
Sléttunar leifar geta átt sér stað þegar þú metur kostnað af birgðaminnkun sem mælt er í öðru magni en samsvarandi birgðaaukning. Sléttunarleifar eru reiknaðar fyrir allar kostnaðarútreikninga þegar **Kostnaðarleiðrétting - Birgðafærsla** runuvinnsla er keyrð.  

 Þegar þú notar meðaltal sem aðferð kostnaðarútreiknings er sléttunarafgangurinn reiknaður út og skráður stighækkandi, færslu fyrir færslu.  

 Þegar þú notar aðferð kostnaðarútreiknings annan en Meðaltal er sléttunarafgangur reiknaður út þegar birgðaaukningunni hefur verið jafnað að fullu, það er þegar eftirstandandi magn fyrir birgðaaukningu er jafnt og núll. Sérstök færsla er því næst stofnuð fyrir sléttunarafganginn og bókunardagsetning sléttunarfærslunnar er bókunardagsetning síðustu reikningsfærðu virðisfærslu birgðaaukningarinnar.  

## <a name="example"></a>Dæmi  
 Eftirfarandi dæmi sýnir hvernig mismunandi sléttunarafgangar eru meðhöndlaðir fyrir meðaltalkostnaðaraðferð og aðrar aðferðir. Í báðum tilvikum er **Kostnaðarleiðrétting - Birgðafærsla** runuvinnsla verið keyrð.  

 Eftirfarandi tafla sýnir birgðahöfuðbókarfærslur sem dæmin eru byggð á.  

|Bókunardags.|Magn|Færslunr.|  
|------------------|--------------|---------------|  
|01-01-20|3|1|  
|02-01-20|-1|2|  
|03-01-20|-1|3|  
|04-01-20|-1|4|  

 Fyrir vöru sem notar kostnaðarútreikninginn Meðaltal er sléttunarafgangurinn (1/300) reiknaður með fyrstu minnkun (færsla nr. 2) og er fluttur áfram í færslu nr. 3. Þannig er færsla nr. 3 með gildið - 3.34.  

 Eftirfarandi tafla sýnir afleiddar virðisfærslur.  

|Bókunardags.|Magn|Kostnaðarupphæð (raunverul.)|Birgðafærslunr.|Færslunr.|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|02-01-20|-1|-3,33|2|2|  
|03-01-20|-1|-3,34|3|3|  
|04-01-20|-1|-3,33|4|4|  

 Fyrir vöru sem notar kostnaðarútreikning annan en Meðaltal er sléttunarafgangurinn (0.01) reiknaður þegar eftirstandandi magn fyrir birgðaaukninguna er núll. Sléttunarafgangur er með aðra færslu (númer 5).  

 Eftirfarandi tafla sýnir afleiddar virðisfærslur.  

|Bókunardags.|Magn|Kostnaðarupphæð (raunverul.)|Birgðafærslunr.|Færslunr.|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|02-01-20|-1|-3,33|2|2|  
|03-01-20|-1|-3,33|3|3|  
|04-01-20|-1|-3,33|4|4|  
|01-01-20|0|-0,01|1|5|  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)   
 [Hönnunarupplýsingar: Kostnaðarleiðrétting](design-details-cost-adjustment.md)   
 [Hönnunarupplýsingar: Aðferð kostn.útreiknings](design-details-costing-methods.md) [Stjórna birgðakostnaði](finance-manage-inventory-costs.md)  
 [Fjármál](finance.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
