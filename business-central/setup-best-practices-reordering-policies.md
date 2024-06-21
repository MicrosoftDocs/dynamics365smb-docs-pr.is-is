---
title: Setja upp bestu venjur - Endurpöntunarstefnur | Microsoft-skjöl
description: Svæðið Endurpöntunarstefna á birgðaspjöldum býður upp á fjórar mismunandi áætlunaraðferðir sem ákvarða hvernig einstaka áætlunarfæribreytur orka hver á aðra.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# <a name="setup-best-practices-reordering-policies"></a>Uppsetning bestu venja: Endurpöntunarstefna

Reiturinn **Endurpöntunarstefna** á birgðaspjöldum hefur áætlunaraðferðir sem ákvarða hvernig einstakar áætlunarfæribreytur hafa samskipti.  

Einn grundvöllur undir bestu venjur til að velja endurpöntunarstefnu er ABC-flokkun vörunnar. Þegar ABC-flokkun er notuð er vörum stjórnað eftir þremur flokkum. Klasinn sem notaður er ræðst af virði vörunnar og rúmmáli miðað við heildarbirgðir. Eftirfarandi tafla sýnir virðismagnsdreifingu klasanna þriggja.

|Flokkur|Prósenta af heildarbirgðamagni|Prósenta af heildarbirgðavirði|
|-----|-----------------------------|----------------------------|
|A|10-20|50-70|
|B|20|20|
|C|60-70|10-30|

ABC-flokkunin segir að spara megi vinnu og peninga með því að hafa lausari taum á vörum af lágu virði-magni en á vörum af háu virði-magni. Eftirfarandi mynd sýnir hvaða endurpöntunarstefna í [!INCLUDE[prod_short](includes/prod_short.md)] er best við fyrir A, B og C - vörur, í þessari röð.

![ABC-flokkun.](media/abc_classification.png "abc_classification")

Eftirfarandi tafla gefur upp bestu venjur til að velja milli fjögurra stefna.  

|Uppsetning valkostar|Bestu starfsvenjur|Athugasemd|  
|------------------|-------------------|-------------|  
|**Röð**|Notist fyrir A vörur.<br /><br /> Notist fyrir vörur sem búnar eru til eftir pöntun.<br /><br /> Við framleiðslu skal nota þetta fyrir vörur á efsta stigi og fyrir dýra íhluti og millivörur.<br /><br /> Notist fyrir vörur sem eru keyptar sem beinar afhending og sérstakar pantanir.<br /><br /> Ekki nota ef sjálfvirk frátekning er ekki samþykkt.|Vörur, eins og leðursófar í húsgagnaverslun, eru vörur með háu virði og lágan eða óreglulegan pöntunarhraða og birgðir eru óásættanlegar, eða nauðsynlegar eigindir breytilegar. Besta endurpöntunarstefnan er því sú sem áætlar sérstaklega fyrir hverja eftirspurn.|  
|**Lotu-fyrir-lotu**|Notist fyrir B vörur.<br /><br /> Við framleiðslu skal nota íhluti sem koma fyrir í mörgum uppskriftum. Þessi regla tryggir að innkaupapantanir séu sameinaðar fyrir sama lánardrottin, svo hægt sé að semja um betra verð.<br /><br /> Notaðu ef þú ert ekki viss um hvaða endurpöntunarstefnu á að velja.|B vörur, eins og borðstofustólar, hafa reglulega og fremur háa pöntunartíðni, en þeim fylgir einnig mikill kostnaðar. Besta endurpöntunarstefnan fyrir B-vörur er sú sem er hagkvæmust með því að pakka saman eftirspurn í endurpöntunarferlinu.<br /><br /> 80 prósent af vörum geta nota þessa reglu.<br /><br /> Má nota án áætlunarfæribreytna.|  
|**Fast endurpöntunarmagn**|Notist fyrir C vörur.<br /><br /> Sameina með færibreytum endurpöntunarmarks.<br /><br /> Við framleiðslu skal nota þetta fyrir íhluti á lægsta stigi.<br /><br /> Ekki nota ef varan er oft tekin frá.|C vörur, eins og tebollar, eru verðlitlar vörur með mikilli og reglulegri pöntunartíðni. Besta endurpöntunarstefnan fyrir C-vörur er því sú sem tryggir stöðugt framboð með því að vera alltaf yfir endurpöntunarpunkti.<br /><br /> Ef notandinn tekur frá magn fyrir fjarlæga eftirspurn er áætlunargrunnurinn truflaður. Jafnvel þó áætluð birgðastig sé samþykkt vegna endurpöntunarmarks er hugsanlegt að magnið sé ekki tiltækt vegna frátekningarinnar.|  
|**Hámarksmagn**|Notist fyrir C vörur með háan birgðakostnað eða geymslutakmarkanir.<br /><br /> Sameina við eina eða fleiri pöntunarbreytur (lágmarks-/hámarkspöntunarmagn eða fjöldapanta).|C vörur, eins og tebollar, eru verðlitlar vörur með mikilli og reglulegri pöntunartíðni. Besta endurpöntunarstefnan fyrir C-vörur er sú sem tryggir stöðugan fáanleika með því að vera alltaf yfir endurpöntunarpunkti, en undir hámarks birgðamagni.<br /><br /> Til að breyta pöntuninni gæti þurft að minnka pöntunarmagnið í tiltekið hámarksmagn pöntunar, hækka í tiltekið lágmarksmagn pöntunar eða slétta það upp til að uppfylla tiltekið pöntunarmargfeldi. **Athugið:** Ef endurpöntunarmark er notað haldast birgðir á milli þess og hámarksmagns.|  

## <a name="see-also"></a>Sjá einnig .

 [Uppsetning bestu venja: Framboðsáætlun](setup-best-practices-supply-planning.md)  
 [Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefnur](design-details-handling-reordering-policies.md)  
 [Setja upp flókin notkunarsviðum með því að nota bestu venjur](set-up-complex-application-areas-using-best-practices.md)  
 [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
