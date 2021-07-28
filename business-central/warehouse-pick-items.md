---
title: Tína til vörur
description: Aðgerðin að tína vörur áður en þær eru afhentar eða notaðar er framkvæmd með mismunandi hætti, eftir því hvernig eiginleikar vöruhúsakerfis eru skilgreindir.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 973e9b43e69205b80361ee38c0cfc0f1cf946959
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/30/2021
ms.locfileid: "6324765"
---
# <a name="pick-items"></a>Tína til vörur

Vöruhúsaaðgerðin að tína vörur áður en þær eru afhentar eða notaðar er framkvæmd með mismunandi hætti, eftir því hvernig vöruhúsakerfisaðgerðir eru grunnstilltar. Flækjustigið getur verið allt frá engum vöruhúsaaðgerðum, gegnum einfaldar grunngerðum vöruhúss með meðhöndlun pöntun fyrir pöntun í einni eða fleiri aðgerðum einvörðungu, til ítarlegra grunnstillinga þar sem allar vöruhúsaaðgerðir eru framkvæmdar í beinu verkflæði. Nánari upplýsingar er að finna í [Uppsetning vöruhúsastjórnunar](warehouse-setup-warehouse.md).

Ef ákveðið er að skipuleggja og skrá tínsluvirkni með vöruhúsafylgiskjölum, er sett gátmerki í reitinn **Krefjast tínslu** á birgðageymsluspjaldinu. Þetta segir kerfinu að þegar um er að ræða vörur sem þarf að tína fyrir upprunaskjal viltu að tínslunni fyrir þessar vörur sé stjórnað af kerfinu. Upprunaskjalið getur verið sölupöntun, innkaupaskilapöntun, millifærslupöntun á útleið, þjónustupöntun eða framleiðslupöntun þar sem á að tína íhluti.

> [!NOTE]
> Jafnvel þótt stillingarnar séu kallaðar **Krefjast tínslu** geturðu samt sem áður bókað afhendingu beint frá uppruna viðskiptaskjala í birgðageymslum þar sem þú velur þessa gátreiti.

Ef birgðageymsla er sett upp þannig að krafist sé tínsluvinnslu en ekki afhendingarvinnslu skal nota síðuna **birgðatínslu** til að flokka tínsluupplýsingarnar, prenta tínsluupplýsingarnar, færa inn útkomu tínslunnar, bóka tínsluupplýsingarnar, sem í staðinn bókar afhendingu varanna. Hægt er að sjá upplýsingar um bókaðar tínslur í glugganum Bókuð tínsla.

Ef birgðageymslan hefur verið sett upp fyrir bæði tínslu- og afhendingarvinnslu og því verið sett gátmerki bæði í reitinn **Krefjast tínslu** og **Krefjast afhendingar** á birgðageymsluspjaldinu er síðan **Vöruhúsatínsla** notuð til að meðhöndla tínsluna. Vöruhúsatínsla er svipuð birgðatínslu, nema í stað þess að bóka tínsluupplýsingar er tínslan skráð. Þetta skráningarferli bókar ekki afhendinguna en gerir aðeins vörurnar tiltækar til afhendingar. Sem stjórnandi vöruhúss, geturðu notað tínsluvinnublað til að flokka tínsluupplýsingar áður en þú stofnar einstakar tínsluleiðbeiningar vöruhússins.

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.   

|**Til að**|**Sjá**|
|------------|-------------|  
|Bóka afhendingu vöru beint í pöntun á útleið því engar vöruhúsaaðgerðir eru fyrir hendi. (Kemur eins út fyrir sölupantanir, millifærslupantanir á útleið, og skilaafhendingar.)|[Senda vörur](warehouse-how-ship-items.md)|  
|Tína vörur pöntun fyrir pöntun og bóka afhendingu í sömu aðgerð, í einfaldri vöruhúsagrunnstillingu.|[Vörur tíndar með birgðatínslu](warehouse-how-to-pick-items-with-inventory-picks.md)|
|Tína vörur fyrir margar pantanir í ítarlegri vöruhúsagrunnstillingu.|[Vörur tíndar með vöruhúsatínslu](warehouse-how-to-pick-items-for-warehouse-shipment.md)|  
|Tína íhluti fyrir framleiðslu eða samsetningu í einfaldri vöruhúsagrunnstillingu.|[Taka til fyrir framleiðslu eða samsetningu í Grunngerðir vöruhúss](warehouse-how-to-pick-for-production.md)|
|Tína íhluti fyrir framleiðslu eða samsetningu í ítarlegri vöruhúsagrunnstillingu.|[Taka til fyrir framleiðslu eða samsetningu í Grunngerðir vöruhúss](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)|  
|Áætla bestu tínslufyrirmæli fyrir nokkrar afhendingar í stað þess að láta starfsmenn vöruhúss framkvæma beint fyrir bókaðar afhendingar.|[Skipuleggja tínslur á vinnublaðinu](warehouse-how-to-plan-picks-in-worksheets.md)|  
|Tína vörur sem tæknilega eru ætlaðar sérstökum tilgangi, eins og til dæmis framleiðslueiningu sem vantar aukaíhluti, þannig að vörurnar fari ekki tæknilega séð ekki úr vöruhúsinu.|[Tína og ganga frá án upprunaskjals](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Skilja hvernig skal tína vörur sjálfvirkt samkvæmt lokadagsetningu þeirra, til dæmis vörum sem hætt er við skemmdum.|[Tínsla eftir FEFO](warehouse-picking-by-fefo.md)|
|Skipta tínslulínu upp í fleiri línur, til dæmis vegna þess að það eru ekki nógu margar vörur til að taka frá í úthlutaða hólfinu.|[Skipta aðgerðalínum vöruhúss](warehouse-how-to-split-warehouse-activity-lines.md)|
|Fá tafarlausan aðgang að tínslu sem notandi hefur fengið úthlutað sem starfsmaður vöruhúss.|[Finna vöruhúsaúthlutanir](warehouse-how-to-find-your-warehouse-assignments.md)|  

## <a name="see-also"></a>Sjá einnig  
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]