---
title: Hvernig vörutegundir virka
description: 'Þú getur leiðrétt birgðaverðmat vöru með því að nota FIFO eða Meðalkostnaðaraðferð þegar vöruverð breytist ekki vegna viðskiptalegra ástæðna, heldur einhvers annars.'
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="about-item-types"></a><a name="about-item-types"></a>Um vörutegundir
Í reitnum **Tegund** á síðunni **Birgðaspjald** er hægt að velja í hvað varan er notuð í fyrirtækinu, sem hefur áhrif á hvernig þú getur stjórnað vörunni í birgðum. Eftirfarandi tafla sýnir og lýsir þeim þremur tegundum vara sem eru tiltækar.

|Valkostur|Dæmigerður tilgangur|
|------|-----------|
|Birgðir|Efnislegir hlutir eins og reiðhjól, símar og skrifborð þar sem þú vilt geta notað alla birgðaferla. Þetta getur einnig átt við óefnislega hluti eins og hugbúnaðarleyfi og áskriftir ef vörurnar eru með auðkennisnúmerum, t.d. raðnúmerum. Þú getur fylgst að fullu með virði og framboði vöru í birgðum.|
|Ekki í birgðum|Yfirleitt eru hlutir sem ekki eru í birgðum efnislegir hlutir, t.d. boltar eða pennar, sem fyrirtæki notar en vill ekki rekja birgðir að fullu. Til dæmis vegna þess að þetta eru kostnaðarlitlar vörur og eru aðeins notaðar innanhúss.|
|Þjónusta|Vinnutímaeining, svo sem ráðgjöf í klukkustund, fyrir takmarkaðan stuðning fyrirtækis.|

> [!NOTE]
> Gerðirnar **Þjónusta** og **Ekki í birgðum** styðja ekki rakningu á birgðamagni eða virði. Aðeins valdar færslugerðir og eiginleikar eru studd.

Í eftirfarandi töflu er listi yfir eiginleikana sem gerðirnar þrjár styðja.

|Vörutegund|Sölur|Innkaup|Vinnunotkun|Þjónustunotkun|Samsetningarnotkun|Framleiðsla Notkun|Samsetningarfrálag|Framleiðslufrálag|Staðsetningarflutningur|Birgðatalning|Endurmat á birgðum|Birgðakostnaður|Vörurakning|Frátekning|Vörugeymsla|Áætlanagerð|Áætlun pöntunar|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Birgðir|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|Já|
|Ekki í birgðum|Já|Já|Já|Já|Já|Já|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Já|
|Þjónusta|Já|Já|Já|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Já|

## <a name="costing-methods-for-types-of-items"></a><a name="costing-methods-for-types-of-items"></a>Kostnaðaraðferðir fyrir vörutegundir
Þegar birgðafærslur eru bókaðar eru magnið og gildisbreytingarnar í birgðunum skráð í birgðafærslunum og virðisfærslurnar, hvort í sínu lagi. 

Fyrir birgðavörur er kostnaðurinn skráður í reitinn **Kostnaðarupphæð (raunveruleg)** á **Virðisfærslur**, og við afstemmingu við fjárhag er kostnaðurinn sýndur í reitnum **Kostnaður bókaður í fjárhag**. Nánari upplýsingar, sjá [Upplýsingar um hönnun: Birgðakostnaður](design-details-inventory-costing.md)

Fyrir vörur sem eru ekki birgðir og þjónusta er kostnaðurinn skráður í **Kostnaðarupphæð (óbirgðafæranl.)** svæði á síðunni **Virðisfærslur**. Fyrir vörur sem eru ekki birgðir og þjónusta er kostnaðurinn tilgreindur í sölu, samsetningu og framleiðsluskjölum og færslubókum. Hægt er að tilgreina sjálfgefinn kostnað í reitnum **Einingarkostnaður** á síðunum **Birgðaspjald** og **Birgðahaldseining**. Kostnaður fyrir þessar vörutegundir er ekki stemmdur við fjárhag. 

## <a name="catalog-and-service-items"></a><a name="catalog-and-service-items"></a>Vörulistar og þjónustuvörur
Vörur sem þú býður viðskiptamönnum þínum en þú vilt ekki stjórna í kerfinu þínu fyrr en þú byrjar að selja þær er hægt að setja upp sem vörulistaatriði. Vörulistaatriðum skal ekki rugla saman við venjulegar vörur af gerðinni „Engar birgðir“. Nánari upplýsingar er að finna í [Vinna með vörulistaatriði](inventory-how-work-nonstock-items.md).

Hlutir viðskiptamanna sem þú framkvæmir þjónustu á, svo sem prentarar, kallast þjónustuvörur. Þjónustuvörur hafa ekkert að gera með venjulegar vörur eða vörulistaatriði. Hins vegar geta íhlutir þjónustuvara verið venjulegar vörur. Nánari upplýsingar er að finna í [Setja upp þjónustuvörur og íhluti þjónustuvara](service-how-setup-service-items.md).

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig
[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Uppsetning birgða](inventory-setup-inventory.md)  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
