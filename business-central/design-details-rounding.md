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
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 2d866fda09934aadf9744f152f3a711193ac23f0
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2019
ms.locfileid: "799617"
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
