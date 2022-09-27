---
title: Færa vörur
description: Í birgðum þarf hugsanlega að færa vörur á milli hólfa til þess að styðja við flæði í vöruhúsinu í daglegum aðgerðum.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7315, 7349, 7351, 7382, 7384, 7386, 7387, 7399, 7400, 9314, 9330, 9345
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: c74a14711fc6bd682a4a1675925690b7aabdf8d3
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9530838"
---
# <a name="moving-items"></a>Færa vörur

Vöruhúsaaðgerðin að færa vörur innan vöruhúss er framkvæmd með mismunandi hætti eftir því hvernig aðgerðir vöruhúsakerfis eru grunnstilltar. Flækjustigið getur verið allt frá engum vöruhúsaaðgerðum, gegnum einfaldar grunngerðum vöruhúss með meðhöndlun pöntun fyrir pöntun í einni eða fleiri aðgerðum einvörðungu, til ítarlegra grunnstillinga þar sem allar vöruhúsaaðgerðir eru framkvæmdar í beinu verkflæði. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Á meðan í einni vöruhúsabirgðageymslu þarf hugsanlega að færa vörur á milli hólfa til þess að styðja við vöruflæði í vöruhúsinu í daglegum aðgerðum. Sumar hreyfingar eiga sér stað í beinu sambandi við innri aðgerðir, s.s. framleiðslupöntun sem þarf íhluti afhenta eða gengið frá lokavörum. Aðrar hreyfingar eru aðeins til hagræðingar á plássi í vöruhúsi eða sem tilfallandi hreyfingar til og frá aðgerðum.

Millifærsluverk til viðbótar felast í því að fylla reglulega á tínsluhólf eða búðarhólf og breyta upplýsingum um hólfainnihald.

Ef vara er flutt í aðra birgðageymslu, hefur það áhrif á birgðabókarfærslur og þarf því að gerast með millifærslupöntun. Nánari upplýsingar eru í [Flytja birgðir milli staða](inventory-how-transfer-between-locations.md).  

Birgðatengd verk talningar, leiðréttingar og endurflokkunar á vörum kann að fela í sér verk vöruhúss sem verður að framkvæma í færslum vöruhúss áður en hægt er að samstilla þau við tengdar birgðabókafærslur. Nánari upplýsingar er að finna í [Telja, leiðrétta og endurflokka birgðir](inventory-how-count-adjust-reclassify.md)  

 Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.   

|**Til að**|**Sjá**|  
|------------|-------------|  
|Færa vörur milli hólfa í einfaldri vöruhúsagrunnstillingu hvenær sem er án upprunaskjala.|[Færa vörur í einfaldri grunngerð vöruhúsa](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Nota skal vinnublað vöruhúsahreyfinga til að færa vörur í ítarlegum vöruhúsaskilgreiningum, bæði fyrir upprunaskjöl og tilfallandi.|[Færa vörur með ítarlegum vöruhúsaaðgerðum](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Færa hlutavörur á innri aðgerðir í einfaldri vöruhúsagrunnstillingu eftir beiðni frá upprunaskjölum fyrir þessar aðgerðir.|[Færa íhluti á aðgerðasvæði í grunnskilgreiningu vöruhúss](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)|
|Áætla hvaða hólf á að fylla eða tæma til þess að viðhalda skilvirku flæði, til dæmis með því að tæma magngeymsluhólf fyrir móttöku með miklu magni.|[Áætla vöruhúsahreyfingar á vinnublöðum](warehouse-how-to-plan-warehouse-movements-in-worksheets.md)|
|Uppfæra tíðnina milli áfyllingar hólfa, til dæmis tínsluhólfa, í samræmi við sveiflur í eftirspurn.|[Reikna út áfyllingu hólfs](warehouse-how-to-calculate-bin-replenishment.md)|
|Endurskipuleggja vöruhúsið með nýjum hólfakótum og hólfaeinkennum og hugsanlega færa þau á milli.|[Endurskipulagning vöruhúsa](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/manage-internal-warehouse-processes/)

## <a name="see-also"></a>Sjá einnig .

[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
