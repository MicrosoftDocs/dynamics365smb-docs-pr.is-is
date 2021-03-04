---
title: 'Kynning: Gera sjóðstreymisspár með því að nota fjárhagsskemu | Microsoft Docs'
description: Í þessari kynningu er lýst hvernig hægt er að nota reikningsáætlanir til að búa til sjóðstreymisspár. Fjárhagsskemu framkvæma útreikninga sem ekki er hægt að framkvæma beint í myndriti yfir sjóðstreymisreikninga. í fjárhagsskemum er hægt að setja upp millisummur fyrir sjóðstreymismóttökur og heildarútborganir. Þessar undirsamtölur er hægt að hafa með í nýjum samtölum sem hægt er að nota til að gera sjóðstreymisspár.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a210792a187bde0217917659f118c58a6a135df2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756540"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a>Kynning: Gera sjóðstreymisspár með því að nota fjárhagsskemu
Í þessari kynningu er lýst hvernig hægt er að nota reikningsáætlanir til að búa til sjóðstreymisspár. Fjárhagsskemu framkvæma útreikninga sem ekki er hægt að framkvæma beint í myndriti yfir sjóðstreymisreikninga. í fjárhagsskemum er hægt að setja upp millisummur fyrir sjóðstreymismóttökur og heildarútborganir. Þessar undirsamtölur er hægt að hafa með í nýjum samtölum sem hægt er að nota til að gera sjóðstreymisspár.  

## <a name="about-this-walkthrough"></a>Um kynninguna  
Þessi kynning fjallar um eftirfarandi verk:  

- Setja upp nýtt heiti fyrir fjárhagsskema  
- Uppsetning fjárhagsskemalína.  
- Setja upp nýtt dálkaútlit.  
- Úthluta dálkauppsetningu til fjárhagsskema.  
- Sjóðstreymisspá skoðuð og prentuð.  

### <a name="prerequisites"></a>Frumskilyrði  
Til að ljúka þessari kynningu þarf:  

- [!INCLUDE[prod_short](includes/prod_short.md)] uppsett.  
- Vinnublaðslínur sjóðstreymis eru skráðar.  

## <a name="roles"></a>Hlutverk  
Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:  

- Eftirlitsmaður  

## <a name="story"></a>Ferill  
Ken er fjármálastjóri á CRONUS sem gerir mánaðarlega sjóðstreymisspár. Hann hefur fjármál, sölu, innkaup og eignir með í spánni og sýnir síðan fjármálastjóranum Söru til að fá greiningu hennar.  

## <a name="setting-up-a-new-account-schedule-name"></a>Setja upp Nýtt heiti fyrir fjárhagsskema  
Fjárhagsskema hefur að geyma heiti fjárhagsskema sjóðstreymis með röð af línum og dálkauppsetningu.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Setja upp Nýtt heiti fyrir fjárhagsskema  

1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fjárhagsskema** eða Lánardrottinn og veldu síðan tengda tengilinn.  
2.  Á síðunni **Heiti fjárhagsskema** skal velja aðgerðina **Nýtt** til að búa til nýtt sjóðstreymi á fjárhagsskema.  
3.  Í reitinn **Heiti** skal færa inn **Spá**.  
4.  Í reitnum **Lýsing** færið inn **Lýsing fyrir sjóðstremisspá**.  
5.  Reitirnir **Sjálfgefin dálkauppsetning** og **Heiti greiningaryfirlits** eru fylltir út eftir því sem við á.  

## <a name="setting-up-account-schedule-lines"></a>Setja upp fjárhagsskemalínur  
Eftir að heiti fjárhagsskema er sett upp, skilgreinir Ken hverja línu sem birtist í fjárhagsskema sjóðsstreymis. Ken skilgreinir línur sem hægt er að birta í skýrslum auk lína sem aðeins eru til útreikninga.  

### <a name="to-set-up-account-schedule-lines"></a>Til að setja upp fjárhagsskemalínur  

1.  Á síðunni **Heiti fjárhagsskema** skal velja nýja heiti fjárhagsskemans fyrir **Spá** sem búið var til og svo velja aðgerðina **Breyta fjárhagsskema**.  
2.  Á síðunni **Fjárhagsskema** skal færa inn hverja línu nákvæmlega eins og sýnt er í eftirfarandi töflu.  

    > [!NOTE]  
    >  Með aðgerðinni **Setja inn CF reikninga** er hægt að merkja sjóðstreymisreikninga á fljótlegan hátt úr línuriti sjóðstreymisreikninga og afrita þá í reikningsáætlunarlínur.  

    |Línunúmer|Description|Tegund samantektar|Samantekt|Tegund línu|Tegund upphæðar|Sýna|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |C10|Upphæð|Hreyfing|Færslur|Nettóupphæð|Alltaf|  
    |C20|Upphæð til dags|Staða til dags.|Færslur|Nettóupphæð|Alltaf|  
    |C30|Allt reikningsárið|Allt reikningsárið|Færslur|Nettóupphæð|Alltaf|  

4.  Velja hnappinn **Í lagi**.  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Dálkaútlitinu úthlutað til reikningsáætlunarheitis.  
Ken er nú tilbúinn að úthluta dálkaútlitinu á reikningsáætlunarheitið.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Til að úthluta dálkaútlitinu á reikningsáætlunarheiti  

1.  Á síðunni **Heiti fjárhagsskema** skal velja **Spá** í reitnum **heiti**.  
2.  Í reitnum **Sjálfgefin dálkauppsetning** er valið dálkauppsetninguna **Sjóðstreymi** sem á að tilnefna sem sjálfgefin dálkauppsetning.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Til að skoða og prenta sjóðstreymisspána  
1.  Á síðunni **Heiti fjárhagsskema** skal velja **Yfirlit** aðgerðina til að skoða sjóðstreymisspá.  
2.  Á síðunni **Yfirlit fjárhagsskema** er hægt að velja upphæð og síðan skoða sjóðstreymisspáfærslur sem mynda upphæðina. Auk þess er hægt að skoða reikniregluna sem er notuð til að reikna upphæðina. Einnig er hægt að afmarka upphæðir eftir dagsetningu og vídd.  
3.  Veldu hnappinn **Prenta** til þess að prenta sjóðstreymisspá.  

## <a name="see-also"></a>Sjá einnig  
 [Vinna með fjárhagsskemu](bi-how-work-account-schedule.md)   
 [Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  
 [Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]