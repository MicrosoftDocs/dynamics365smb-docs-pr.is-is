---
title: Skilja vörutegundir
description: Fræðast um tegundir vara sem hægt er að stjórna í birgðum og hvernig tegundirnar hafa áhrif Á Aðlaga birgðamat vöru með því að nota FIFO eða Meðalkostnaðarútreikning þegar vörukostnaður breytist af öðrum ástæðum en færslum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Um vörutegundir

Í reitnum **Tegund** á síðunni **Birgðaspjald** er hægt að velja í hvað varan er notuð í fyrirtækinu, sem hefur áhrif á hvernig þú getur stjórnað vörunni í birgðum. Eftirfarandi tafla sýnir og lýsir þeim þremur tegundum vara sem eru tiltækar.

|Valkostur|Dæmigerður tilgangur|
|------|-----------|
|Birgðir|Efnislegir hlutir eins og reiðhjól, símar og skrifborð þar sem þú vilt geta notað alla birgðaferla. Í birgðum geta einnig verið ólíkar vörur, svo sem hugbúnaðarleyfi og áskriftir, ef vörurnar eru með kenninúmer, t.d. raðnúmer. Þú getur fylgst að fullu með virði og framboði vöru í birgðum.|
|Ekki í birgðum|Yfirleitt eru utanbirgðavörur efnislegir hlutir, eins og bolir eða pennar, sem fyrirtækið notar en rekur ekki að fullu í birgðum. Til dæmis vegna þess að þær eru lágkostnaðarvörur og aðeins notaðar við innri vinnslu.|
|Þjónusta|Vinnutímaeining, svo sem ráðgjöf í klukkustund, fyrir takmarkaðan stuðning fyrirtækis.|

> [!NOTE]
> Tegundirnar **Þjónusta** og **Ekki birgðir** gera notanda kleift að rekja birgðamagn og virði. Aðeins valdar færslugerðir og eiginleikar eru studd. Í eftirfarandi töflu er listi yfir eiginleikana sem gerðirnar þrjár styðja.

|Vörutegund|Sölur|Innkaup|Vinnunotkun|Þjónustunotkun|Samsetningarnotkun|Framleiðsla Notkun|Samsetningarfrálag|Framleiðslufrálag|Staðsetningarflutningur|Birgðatalning|Endurmat á birgðum|Birgðakostnaður|Vörurakning|Frátekning|Vörugeymsla|Áætlanagerð|Áætlun pöntunar|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Birgðir|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|
|Ekki í birgðum|Já|Já|Já|Já|Já|Já|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Já|
|Þjónusta|Já|Já|Já|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Já|

## Aðferðir kostnaðarútreiknings fyrir gerðir vara

Þegar birgðafærslur eru bókaðar eru magnið og gildisbreytingarnar í birgðunum skráð í birgðafærslunum og virðisfærslurnar, hvort í sínu lagi.

Kostnaður birgðavara er skráður í reitinn **Kostnaðarupphæð (raunverul.)** á síðunni **Virðisfærslur** . Þegar færslan er stemmd af við fjárhag sýnir kostnaðurinn í reitnum **Kostnaður bókaður í fjárhag** . Nánari upplýsingar um birgðakostnað eru notaðar með því að [fara í Upplýsingar um hönnun: Birgðakostnaður](design-details-inventory-costing.md).

Kostnaður er skráður í kostnaðarupphæð fyrir utanbirgðavörur og þjónustuvörur og er kostnaður skráður í **kostnaðarupphæðina (Óbirgðab.)** á síðunni **Virðisfærslur** . Fyrir utanbirgðavörur og þjónustuvörur skal tilgreina kostnað við sölu, samsetningu og framleiðsluskjöl og færslubækur. Tilgreina sjálfgefinn kostnað í reitnum Kostnaðarverð **á** birgðaspjaldinu **og** Birgðahaldseiningarsíðunum **·** . Kostnaður vegna þessara vara er ekki stemmdur af við fjárhag.

## Vörulisti og þjónustuvörur

Hægt er að setja upp vörur sem boðnar eru viðskiptamönnum en ekki er stjórnað fyrr en þær eru selt sem vörulistavörur. Þó svo að vörulistavörum líkist venjulegum vörum af tegundinni **Ekki birgðir** í þessu tilviki, ekki rugla saman tveimur vegna þess að munur er á vörum. Til að fá nánari upplýsingar er farið í [Vinna við vörulistaatriði](inventory-how-work-nonstock-items.md).

Viðskiptamannavörur sem þjónusta, t.d. prentari, eru kallaðar þjónustuvörur. Þjónustuvörur hafa ekkert að gera með venjulegar vörur eða vörulistaatriði. Hins vegar geta íhlutir þjónustuvara verið venjulegar vörur. Nánari upplýsingar eru notaðar til að [setja upp þjónustuvörur og þjónustuvöruíhluti](service-how-setup-service-items.md).

## Sjá einnig .

[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Uppsetning birgða](inventory-setup-inventory.md)  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
