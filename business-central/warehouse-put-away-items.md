---
title: Frágangur á vörum
description: Frágangur á vörum eftir að tekið er á móti þeim, eða frálag, er framkvæmdur á mismunandi hátt eftir því hvernig eiginleikar vöruhúsakerfis eru skilgreindir.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5770, 5783, 5784, 5786, 5795, 7334, 7352, 7354, 7356, 7375, 7379, 7390, 7394, 7396, 9312, 9315, 9343
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 4643368181fa2f36c010f50ab6ce444d0a5fdce4
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134510"
---
# <a name="putting-items-away"></a>Vörufrágangur

Vöruhúsaaðgerðin að ganga frá vörum eftir að tekið er á móti þeim, eða frálag, er framkvæmd með mismunandi hætti eftir því hvernig aðgerðir vöruhúsakerfis eru grunnstilltar. Flækjustigið getur verið allt frá engum vöruhúsaaðgerðum, gegnum einfaldar grunngerðum vöruhúss með meðhöndlun pöntun fyrir pöntun í einni eða fleiri aðgerðum einvörðungu, til ítarlegra grunnstillinga þar sem allar vöruhúsaaðgerðir eru framkvæmdar í beinu verkflæði. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Ef ákveðið er að skipuleggja og skrá frágangsupplýsingar með fylgiskjölum í kerfinu er sett gátmerki í reitinn **Krefjast frágangs** á birgðageymsluspjaldinu. Þetta segir kerfinu að þegar um er að ræða vörur sem koma inn í vöruhúsið með upprunaskjali á innleið, að þú vilt að fráganginum af þessum vörum sé stjórnað af kerfinu. Upprunaskjalið á innleið getur verið innkaupapöntun, söluvöruskilapöntun, millifærslupöntun á innleið eða framleiðslupöntun þar sem úttakið er tilbúið til frágangs.  

Þegar birgðageymslan er sett upp þannig að hún noti frágangsvinnslu en ekki móttökuvinnslu skal nota síðuna **Birgðafrágangur** til að skipuleggja frágangsupplýsingar, prenta þær, færa inn niðurstöður af raunverulegum frágangi og bóka frágangsupplýsingar, sem á móti bóka móttökuupplýsingar fyrir upprunaskjalið. Ef um er að ræða framleiðslupöntun, bókar bókunarferlið frálag pöntunarinnar og lýkur henni.

Ef vöruhúsið er sett upp þannig að það krefjist bæði móttökuvinnslu og frágangsvinnslu þannig að merkt hefur verið bæði við **Krefjast móttöku** og **Krefjast frágangs** á birgðageymsluspjaldinu er ferlið við frágang á vörum annað. Í því tilviki er síðan **Vöruhúsafrágangur** notuð til að sjá um frágang. Vöruhúsafrágangur er svipaður birgðafrágangi, nema í stað þess að bóka upplýsingarnar er frágangurinn skráður. Athugið að skráning á frágangi vöruhúsins bókar ekki móttöku varanna. Það uppfærir aðeins innihald hólfsins. Sem stjórnandi vöruhúss, geturðu notað frágangsvinnublað til að flokka frágangsupplýsingar áður en þú stofnar einstakar frágangsleiðbeiningar vöruhússins.

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.  

|**Til að**|**Sjá**|  
|------------|-------------|  
|Bóka móttöku vöru beint frá pantanaskjali á innleið, og um leið skrá fráganginn, því engar vöruhúsaskilgreiningar eru fyrir hendir.|[Móttaka vara](warehouse-how-receive-items.md)|  
|Ganga frá vöru pöntun fyrir pöntun og bóka móttöku í sömu aðgerð, í einfaldri vöruhúsagrunnstillingu.|[Ganga frá vörum með birgðafrágangi](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Ganga frá vörum fyrir margar pantanir í ítarlegri vöruhúsagrunnstillingu.|[Ganga frá vörum með vöruhúsafrágangi](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  
|Ganga frá framleiðslu eða samsetningu vörur í einfaldri eða ítarlegri vöruhúsagrunnstillingu.|[Ganga frá framleiðslu eða samsetningarfrálagi](warehouse-how-to-put-away-production-output.md)|
|Áætla leiðbeiningar um besta frágang fyrir margar bókaðar vöruhúsainnhreyfingar í stað þess að starfsmenn vöruhúss vinni beint með innhreyfingar.|[Áætla frágang á vinnublöðum](warehouse-how-to-plan-put-aways-in-worksheets.md)|  
|Skila aftur vörum sem voru tíndar í innanhússtínslu, til dæmis fyrir framleiðslupöntun sem notaði ekki væntanlegt magn.|[Tína og ganga frá án upprunaskjals](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Skipta frágangslínu til þess að setja hluta af frágangsmagninu í tiltækt hólf því merkta hólfið er orðið fullt.|[Skipta aðgerðalínum vöruhúss](warehouse-how-to-split-warehouse-activity-lines.md)|
|Fá tafarlausan aðgang að frágangi sem notandi hefur fengið úthlutað sem starfsmaður vöruhúss.|[Finna vöruhúsaúthlutanir](warehouse-how-to-find-your-warehouse-assignments.md)|

## <a name="see-also"></a>Sjá einnig

[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md) 
[samsetningarstýring](assembly-assemble-items.md)
[hönnunar upplýsingar: vöruhúsastjórnun](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]