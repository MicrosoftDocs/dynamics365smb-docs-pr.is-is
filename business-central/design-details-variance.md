---
title: "Hönnunarupplýsinga - Frávik | Microsoft Docs"
description: "Frávik er skilgreint sem mismunurinn á raunverulegum kostnaði og staðalkostnað, eins og lýst er í eftirfarandi formúlu."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 36062fc6fa40c3fc2b928ffad7e3b242634149fc
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-variance"></a>Hönnunarupplýsingar Frávik
Frávik er skilgreint sem mismunurinn á raunverulegum kostnaði og staðalkostnað, eins og lýst er í eftirfarandi formúlu.  

 raunkostnaður – staðlaður kostnaður = frávik  

 Ef raunkostnaður breytist, til dæmis vegna þess að kostnaðarauki er bókaður á síðari dagsetningu, er frávikið uppfært samkvæmt því.  

> [!NOTE]  
>  Endurmat hefur ekki áhrif á dreifni útreikning, því endurmat einungis breytir birgðavirði.  

## <a name="example"></a>Dæmi  
 Eftirfarandi dæmi sýnir hvernig frávik er reiknað út fyrir keyptar vörur. Þetta er byggt á eftirfarandi atburðarás:  

1.  Notandinn kaupir vöru á SGM 90.00 en staðalkostnaður er SGM 100.00. Í samræmi er innkaupafrávikið SGM -10,00.  
2.  SGM 10,00 er kreditfært fráviksreikning innkaupa.  
3.  Notandinn bókar kostnaðarauka SGM 20.00. Í samræmi er raunverulegur kostnaður aukinn í SGM 110,00 og virði innkaupafráviks verður SGM 10,00.  
4.  SGM 20,00 er debetfært á fráviksreikning innkaupa. Í samræmi verður nettóinnkaupafrávikið SGM 10,00.  
5.  Notandinn endurmetur vöruna úr SGM 100.00 í SGM 70.00. Þetta hefur ekki áhrif á fráviksútreikninginn, aðeins birgðavirðið.  

 Eftirfarandi tafla sýnir afleiddar virðisfærslur.  

 ![Innkaupafráviksútreikningur](media/design_details_inventory_costing_11_purchase_variance.png "Innkaupafráviksútreikningur")  

## <a name="determining-the-standard-cost"></a>Ákvarða staðalkostnað  
 Staðlaður kostnaður er notaður við útreikning fráviks og upphæð sem á að eignfæra. Þar sem staðalkostnaður er hægt að breyta með tímanum vegna útreikninga með handvirkri uppfærslu, þú þarft að hafa tímapunkt þegar staðalkostnaður er fastur fyrir fráviksútreikning. Þetta mark er þegar birgðaaukning er reikningsfærð. Fyrir framleiddar eða samsettar vörur er punkturinn þegra staðalkostnaður er ákvarðaður þegar kostnaður er jafnaður.  

 Eftirfarandi tafla sýnir hvernig mismunandi kostnaðarhlutdeild er reiknuð fyrir framleiddar og samsettar vörur þegar aðgerðin Reikna staðlað kostnaðarverð er notaður.  

|Kostn.hlutdeild|Keypt vara|Framleidd/samsett vara|  
|----------------|--------------------|------------------------------|  
|**Staðlað kostn.verð**||Eins stigs efniskostnaður + Eins stigs  afkastakostnaður + Eins stigs undirverktakakostnaður + Eins stigs óbeinn afkastakostnaður + Eins stigs óbeinn framleiðslukostnaður|  
|**Efniskostnaður á einu stigi**|Kostnaðarverð|![Jafna 1](media/design_details_inventory_costing_11_equation_1.png "Jafna 1")|  
|**Getukostnaður á einu stigi**|Á ekki við|![Jafna 2](media/design_details_inventory_costing_11_equation_2.png "Jafna 2")|  
|**Undirverkt.kostn. á einu stigi**|Á ekki við|![Jafna 3](media/design_details_inventory_costing_11_equation_3.png "Jafna 3")|  
|**Sam.ób. afk.kostn á einu stigi**|Á ekki við|![Jafna 4](media/design_details_inventory_costing_11_equation_4.png "Jafna 4")|  
|**Sam.ób. frlkostn á einu stigi**|Á ekki við|(Eniskostnaður á einu stigi + Kostnaður afkastaveitu á einu stigi + Kostnaður undirverktaka á einu stigi) * Óbeinn kostnaður % / 100 + Sameiginlegur kostnaður|  
|**Samantekinn efniskostnaður**|Kostnaðarverð|![Jafna 5](media/design_details_inventory_costing_11_equation_5.png "Jafna 5")|  
|**Samantekinn getukostnaður**|Á ekki við|![Jafna 6](media/design_details_inventory_costing_11_equation_6.png "Jafna 6")|  
|**Samantekinn undirverktakakostn.**|Á ekki við|![Jafna 7](media/design_details_inventory_costing_11_equation_7.png "Jafna 7")|  
|**Samantekinn sameiginlegur kostnaðar afkastagetu**|Á ekki við|![Jafna 8](media/design_details_inventory_costing_11_equation_8.png "Jafna 8")|  
|**Samant. ób. sam. framl.kostn.**|Á ekki við|![Jafna 9](media/design_details_inventory_costing_11_equation_9.png "Jafna 9")|  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)   
 [Hönnunarupplýsingar: Aðferð kostn.útreiknings](design-details-costing-methods.md) [Stjórna birgðakostnaði](finance-manage-inventory-costs.md)  
 [Fjármál](finance.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

