---
title: "Færa vörur | Microsoft Docs"
description: "Í birgðum þarf hugsanlega að færa vörur á milli hólfa til þess að styðja við flæði í vöruhúsinu í daglegum aðgerðum. Sumar hreyfingar eiga sér stað í beinu sambandi við innri aðgerðir, s.s. framleiðslupöntun sem þarf íhluti afhenta eða gengið frá lokavörum. Aðrar hreyfingar eru aðeins til hagræðingar á plássi í vöruhúsi eða sem tilfallandi hreyfingar til og frá aðgerðum."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f52353ec74b10983b0acfd04169d6b146c70eb84
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="moving-items"></a>Færa vörur
Vöruhúsaaðgerðin að færa vörur innan vöruhúss er framkvæmd með mismunandi hætti eftir því hvernig aðgerðir vöruhúsakerfis eru grunnstilltar. Flækjustigið getur verið allt frá engum vöruhúsaaðgerðum, gegnum einfaldar grunngerðum vöruhúss með meðhöndlun pöntun fyrir pöntun í einni eða fleiri aðgerðum einvörðungu, til ítarlegra grunnstillinga þar sem allar vöruhúsaaðgerðir eru framkvæmdar í beinu verkflæði. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Á meðan í einni vöruhúsabirgðageymslu þarf hugsanlega að færa vörur á milli hólfa til þess að styðja við vöruflæði í vöruhúsinu í daglegum aðgerðum. Sumar hreyfingar eiga sér stað í beinu sambandi við innri aðgerðir, s.s. framleiðslupöntun sem þarf íhluti afhenta eða gengið frá lokavörum. Aðrar hreyfingar eru aðeins til hagræðingar á plássi í vöruhúsi eða sem tilfallandi hreyfingar til og frá aðgerðum.

Ef vara er flutt í aðra birgðageymslu, hefur það áhrif á birgðabókarfærslur og þarf því að gerast með millifærslupöntun. Nánari upplýsingar eru í [Hvernig á að: Flytja birgðir milli staða](inventory-how-transfer-between-locations.md).  

Millifærsluverk til viðbótar felast í því að fylla reglulega á tínsluhólf eða búðarhólf og breyta upplýsingum um hólfainnihald.  

 Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.   

|**Til að**|**Sjá**|  
|------------|-------------|  
|Færa vörur milli hólfa í einfaldri vöruhúsagrunnstillingu hvenær sem er án upprunaskjala.|[Hvernig á að: færa vörur í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Nota skal vinnublað vöruhúsahreyfinga til að færa vörur í ítarlegum vöruhúsaskilgreiningum, bæði fyrir upprunaskjöl og tilfallandi.|[Hvernig á að: færa vörur í ítarlegri grunngerð vöruhúsa](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Færa hlutavörur á innri aðgerðir í einfaldri vöruhúsagrunnstillingu eftir beiðni frá upprunaskjölum fyrir þessar aðgerðir.|[Hvernig á að: færa íhluti á aðgerðasvæði í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)|
|Áætla hvaða hólf á að fylla eða tæma til þess að viðhalda skilvirku flæði, til dæmis með því að tæma magngeymsluhólf fyrir móttöku með miklu magni.|[Hvernig á að áætla vöruhúsahreyfingar á vinnublöðum](warehouse-how-to-plan-warehouse-movements-in-worksheets.md)|
|Uppfæra tíðnina milli áfyllingar hólfa, til dæmis tínsluhólfa, í samræmi við sveiflur í eftirspurn.|[Hvernig á að Reikna út áfyllingu hólfs](warehouse-how-to-calculate-bin-replenishment.md)|
|Endurskipuleggja vöruhúsið með nýjum hólfakótum og hólfaeinkennum og hugsanlega færa þau á milli.|[Hvernig á að: Endurskipuleggja vöruhús](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

