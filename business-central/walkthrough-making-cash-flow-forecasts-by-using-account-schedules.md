---
title: Sjóðstreymisspár með því að nota fjárhagsskemu
description: Í þessari kynningu er lýst hvernig hægt er að nota reikningsáætlanir til að búa til sjóðstreymisspár í Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 7238b4de3b4a48c61560bc9a96a6923afe82eb93
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533482"
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

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Vinnublaðslínur sjóðstreymis eru skráðar  

## <a name="roles"></a>Hlutverk

Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:  

- Eftirlitsmaður  

## <a name="story"></a>Ferill

Ken er fjármálastjóri á CRONUS sem gerir mánaðarlega sjóðstreymisspár. Hann hefur fjármál, sölu, innkaup og eignir með í spánni og sýnir síðan fjármálastjóranum Söru til að fá greiningu hennar.  

## <a name="setting-up-a-new-account-schedule-name"></a>Setja upp Nýtt heiti fyrir fjárhagsskema

Fjárhagsskema hefur að geyma heiti fjárhagsskema sjóðstreymis með röð af línum og dálkauppsetningu.  

### <a name="to-set-up-a-new-account-schedule-name"></a>Setja upp Nýtt heiti fyrir fjárhagsskema  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagsskema** og svo velja viðeigandi tengil.  
2. Á síðunni **Heiti fjárhagsskema** skal velja aðgerðina **Nýtt** til að búa til nýtt sjóðstreymi á fjárhagsskema.  
3. Í reitinn **Heiti** skal færa inn **Spá**.  
4. Í reitnum **Lýsing** færið inn **Lýsing fyrir sjóðstremisspá**.  
5. Reitirnir **Sjálfgefin dálkauppsetning** og **Heiti greiningaryfirlits** eru fylltir út eftir því sem við á.  

## <a name="setting-up-account-schedule-lines"></a>Setja upp fjárhagsskemalínur

Eftir að heiti fjárhagsskema er sett upp, skilgreinir Ken hverja línu sem birtist í fjárhagsskema sjóðsstreymis. Ken skilgreinir línur sem hægt er að birta í skýrslum auk lína sem aðeins eru til útreikninga.  

### <a name="to-set-up-account-schedule-lines"></a>Til að setja upp fjárhagsskemalínur  

1. Á síðunni **Heiti fjárhagsskema** skal velja nýja heiti fjárhagsskemans fyrir **Spá** sem búið var til og svo velja aðgerðina **Breyta fjárhagsskema**.  
2. Á síðunni **Fjárhagsskema** skal færa inn hverja línu eins og sýnt er í eftirfarandi töflu.  

    > [!TIP]  
    >  Með aðgerðinni **Setja inn CF reikninga** er hægt að merkja sjóðstreymisreikninga á fljótlegan hátt úr línuriti sjóðstreymisreikninga og afrita þá í reikningsáætlunarlínur.  

    | Línunúmer | Description              | Tegund samantektar            | Samantekt | Tegund línu   | Tegund upphæðar | Sýna |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | H10     | Opna sölupantanir        | Færslureikningar sjóðstreymis | 20       |Hreyfing | Nettóupphæð  | Já  |
    | H10     | Leiga                  | Færslureikningar sjóðstreymis | 30       |Hreyfing | Nettóupphæð  | Já  |
    | H10     | Fjáreignir         | Færslureikningar sjóðstreymis | 40       |Hreyfing | Nettóupphæð  | Já  |
    | H10     | Eignaafskráning    | Færslureikningar sjóðstreymis | 50       |Hreyfing | Nettóupphæð  | Já  |
    | H10     | Fjárfestingar      | Færslureikningar sjóðstreymis | 60       |Hreyfing | Nettóupphæð  | Já  |
    | H10     | Ýmsar innhreyfingar   | Færslureikningar sjóðstreymis | 70       |Hreyfing | Nettóupphæð  | Já  |
    | H10     | Opnar þjónustupantanir      | Færslureikningar sjóðstreymis | 80       |Hreyfing | Nettóupphæð  | Já  |
    | R20     | Heildarsjóðstekjur      | Reikniregla                  | H10      |Hreyfing | Nettóupphæð  | Já  |
    | R20     | Heildarsjóðstekjur      | Reikniregla                  | H10      |Hreyfing | Nettóupphæð  | Já  |
    | R30     | Viðskiptaskuldir                 | Færslureikningar sjóðstreymis | 1010     |Hreyfing | Nettóupphæð  | Já  |
    | R30     | Opnar innkaupapantanir     | Færslureikningar sjóðstreymis | 1020     |Hreyfing | Nettóupphæð  | Já  |
    | R30     | Starfsmannakostnaður          | Færslureikningar sjóðstreymis | 1030     |Hreyfing | Nettóupphæð  | Já  |
    | R30     | Rekstrarkostnaður            | Færslureikningar sjóðstreymis | 1040     |Hreyfing | Nettóupphæð  | Já  |
    | R30     | Fjármagnskostnaður            | Færslureikningar sjóðstreymis | 1050     |Hreyfing | Nettóupphæð  | Já  |
    | R30     | Fjárfestingar              | Færslureikningar sjóðstreymis | 1070     |Hreyfing | Nettóupphæð  | Já  |
    | R30     | Einkaneysla     | Færslureikningar sjóðstreymis | 1090     |Hreyfing | Nettóupphæð  | Já  |
    | R30     | VSK til greiðslu                  | Færslureikningar sjóðstreymis | 1100     |Hreyfing | Nettóupphæð  | Já  |
    | R30     | Annar rekstrarkostnaður           | Færslureikningar sjóðstreymis | 1110     |Hreyfing | Nettóupphæð  | Já  |
    | R40     | Heildarútborgun | Reikniregla                  | R30      |Hreyfing | Nettóupphæð  | Já  |
    | R50     | Tekjuafgangur                  | Reikniregla                  | R20+R40  |Hreyfing | Nettóupphæð  | Já  |
    | R60     | Sjóðstreymissjóðir          | Færslureikningar sjóðstreymis | 2100     |Hreyfing | Nettóupphæð  | Já  |
    | R70     | Heildarsjóðstreymi          | Reikniregla                  | R50+R60  |Hreyfing | Nettóupphæð  | Já  |

    > [!NOTE]
    > Línunúmer R10 er notað til að ná yfir niðurstöðutölur fyrir útistandandi reikninga. Línunúmer R20 er notað ef reikna á samtölu allra inngreiðsla. Línunúmer R30 er notað til að ná yfir niðurstöðutölur fyrir gjaldfallnar greiðslur. Línunúmer R40 er notað ef reikna á samtölu allra útborgana. Línunúmer R50 er notað ef ná á samtölu umframmagns reiðufés. Línunúmer R60 er notað til að ná yfir lausafé. Línunúmer R70 er notað til að reikna áætlað sjóðstreymi.

## <a name="setting-up-a-new-column-layout"></a>Setja upp nýtt dálkaútlit

Áður en Ken getur að prentað sjóðsstreymisspána, þarf hann að stofna dálkauppsetningu fyrir tölulegu upplýsingarnar. Í dálkunum skilgreinir hann upplýsingar sem hann vill nota úr línunum.

- Fyrsti dálkurinn hefur númerið *C10* með heitinu **Upphæð** og inniheldur Hreina breytingu.  
- Annar reiturinn hefur númerið *C20* með heitinu **Staða á dagsetningu** og inniheldur færslur tímabilsins.  
- Þriðji dálkurinn hefur númerið *C30* með heitinu **Allt árið** og inniheldur breytingar á innistæðum fyrir allt reikningsárið.  
- Að lokum úthlutar hann dálkauppsetningunni sem sjálfgefinni dálkauppsetningu fyrir fjárhagsskemað **Spá**.  

## <a name="to-set-up-a-new-column-layout"></a>Til að setja upp nýtt dálkaútlit

1. Í glugganum **Heiti fjárhagsskema** skal velja nýja heiti fjárhagsskemans fyrir **Spá** sem búið var til. Á flipanum **Heim** í flokknum **Vinna** skal velja **Breyta uppsetningu dálkaútlits**.

    > [!TIP]
    > Hægt er að finna sömu aðgerðina á síðunni **Fjárhagsskema** ef enn er verið að breyta fjárhagsskemanu **Spá** á henni.

2. Stofna nýja dálkuppsetningu með heitinu **Sjóðstreymi**.

3. Velja hnappinn Í lagi.

4. Færa inn hverja línu nákvæmlega eins og sýnt er í eftirfarandi töflu.

    |Dálknr.|Dálkfyrirsögn|Dálktegund|Færslutegund|Tegund upphæðar|Sýna|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |C10|Upphæð|Hreyfing|Færslur|Nettóupphæð|Alltaf|  
    |C20|Upphæð til dags|Staða til dags.|Færslur|Nettóupphæð|Alltaf|  
    |C30|Allt reikningsárið|Allt reikningsárið|Færslur|Nettóupphæð|Alltaf|

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a>Dálkaútlitinu úthlutað til reikningsáætlunarheitis.

Ken er nú tilbúinn að úthluta dálkaútlitinu á reikningsáætlunarheitið.  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a>Til að úthluta dálkaútlitinu á reikningsáætlunarheiti  

1. Á síðunni **Fjárhagsskema** þar sem unnið er með fjárhagsskemað **Spá** skal velja aðgerðina **Breyta uppsetningu dálkaútlits**.  
2. Í reitnum **Heiti dálkauppsetningar** skal velja dálkauppsetninguna **Sjóðstreymi** sem á að tilnefna sem sjálfgefin dálkauppsetning.  

### <a name="to-view-and-print-the-cash-flow-forecast"></a>Til að skoða og prenta sjóðstreymisspána

1. Á síðunni **Heiti fjárhagsskema** skal velja **Yfirlit** aðgerðina til að skoða sjóðstreymisspá.  
2. Á síðunni **Yfirlit fjárhagsskema** er hægt að velja upphæð og síðan skoða sjóðstreymisspáfærslur sem mynda upphæðina. Auk þess er hægt að skoða reikniregluna sem er notuð til að reikna upphæðina. Einnig er hægt að afmarka upphæðir eftir dagsetningu og vídd.  
3. Veldu hnappinn **Prenta** til þess að prenta sjóðstreymisspá.  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/forecast-cash-flow-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Vinna með fjárhagsskemu](bi-how-work-account-schedule.md)  
[Greining á sjóðstreymi í fyrirtækinu þínu](finance-analyze-cash-flow.md)  
[Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
