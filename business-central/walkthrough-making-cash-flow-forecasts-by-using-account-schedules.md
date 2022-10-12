---
title: Gera Sjóðstreymisspá með fjárhagsskýrslum
description: Þessi Walkthrough lýsir því hvernig hægt er að nota fjárhagsskýrslur til að gera sjóðstreymisspár í Viðskiptamiðinu.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/18/2022
ms.author: edupont
ms.openlocfilehash: 4f3b406435b52d632d20553181aa5f106dc6a387
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606857"
---
# <a name="walkthrough-making-cash-flow-forecasts-using-financial-reports"></a>Walkthrough: gerð sjóðstreymisspáa með fjárhagsskýrslum

Þessi gönguleið lýsir því hvernig hægt er að nota aðgerðina fjársjóðsskýrslur til að gera sjóðstreymisspár. Ársskýrslur haga útreikningum sem ekki er hægt að gera beint í bókhaldslyklum sjóðstreymis. Í fjárskýrslunum er hægt að setja upp millisamtölu fyrir innhreyfingar og afgreiðsluflæði. Þessar millisamtölur er hægt að taka með í nýjar samtölur sem síðan er hægt að nota til að gera sjóðsstreymisspá.  

## <a name="about-this-walkthrough"></a>Um þetta Walk

Þessi kynning fjallar um eftirfarandi verk:  

- Uppsetning á nýju sjóðstreymissskýrsluheiti.  
- Uppsetning lína í fjárhagsskýrslu.  
- Uppsetning á nýrri dálkaskilgreiningu.  
- Með því að úthluta dálkskilgreiningu á fjárhagsskýrslu.  
- Sjóðstreymisspá skoðuð og prentuð.  

### <a name="prerequisites"></a>Frumskilyrði

Til að ljúka þessari kynningu þarf:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Sjóðstreymissvinnublað með skráðum línum  

## <a name="roles"></a>Hlutverk

Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:  

- Eftirlitsmaður  

## <a name="story"></a>Ferill

Ken er fjármálastjóri á CRONUS sem gerir mánaðarlega sjóðstreymisspár. Hann nær til fjármála, sölu, innkaupa og eigna í þeim spám, sem hann síðan kynnir til FRAMKVÆMDASTJÓRA um að Sara sé viðskiptainnsýn.  

## <a name="setting-up-a-new-financial-report-name"></a>Uppsetning á nýju fjárhagsskýrsluheiti

Heiti fjárhagsskýrslunnar er það heiti sem gefið er upp sjóðsstreymisspá sem inniheldur röð af skilgreindum línum og dálkskilgreiningu.  

### <a name="set-up-a-new-financial-report-name"></a>Setja upp nýtt heiti fjárhagsskýrslu  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **ársskýrslur** og velja síðan tengda tengilinn.  
2. **Á síðunni ársskýrslur** skal velja **nýtt** til að stofna nýtt sjóðstreymissheiti fjárhagsskýrslu.  
3. Í reitinn **Heiti** skal færa inn **Spá**.  
4. Í reitnum **Lýsing** færið inn **Lýsing fyrir sjóðstremisspá**.  
5. **Skiljið línuskilgreininguna** og **dálkskilgreiningarsvæðin** eftir auð.

## <a name="setting-up-row-definition-lines"></a>Setja upp línuskilgreiningarlínur

Eftir að nafn á fjárhagsskýrslu hefur verið sett upp skilgreinir Ken hverja línu í fjárhagsskýrslu sjóðstreymis. Ken skilgreinir línur sem á að birta í skýrslum auk lína sem eru aðeins til útreikninga.  

### <a name="set-up-row-definition-lines"></a>Setja upp línuskilgreiningarlínur  

1. **Á síðunni ársskýrslur** skal velja nýju **spárfjárskýrsluna** sem var stofnuð og velja **síðan aðgerðina Breyta línuskilgreiningu**.  
2. **Á Línuskilgreiningsíðunni** skal færa inn hverja línu eins og sýnt er í eftirfarandi töflu.  

    > [!TIP]  
    > **Nota skal aðgerðina Setja inn CF-lykla** sem á að merkja í sjóðstreymissreiknunum, sjóðstreymissreikningarnir sem á að afrita og setja þá í línuskilgreiningarlínur.  

    | Línunúmer | Lýsing              | Tegund samantektar            | Samantekt | Tegund línu   | Gerð upphæðar | Sýna |
    |---------|--------------------------|--------------------------|----------|------------|-------------|------|
    | R10     | Viðskiptakröfur              | Færslureikningar sjóðstreymis | 10       |Nettóbreyting | Nettóupphæð  | Já  |
    | R10     | Opna sölupantanir        | Færslureikningar sjóðstreymis | 20       |Nettóbreyting | Nettóupphæð  | Já  |
    | H10     | Leiga                  | Færslureikningar sjóðstreymis | 30       |Hreyfing | Nettóupphæð  | Já  |
    | H10     | Fjáreignir         | Færslureikningar sjóðstreymis | 40       |Hreyfing | Nettóupphæð  | Já  |
    | H10     | Eignaafskráning    | Færslureikningar sjóðstreymis | 50       |Hreyfing | Nettóupphæð  | Já  |
    | H10     | Fjárfestingar      | Færslureikningar sjóðstreymis | 60       |Hreyfing | Nettóupphæð  | Já  |
    | H10     | Ýmsar innhreyfingar   | Færslureikningar sjóðstreymis | 70       |Hreyfing | Nettóupphæð  | Já  |
    | H10     | Opnar þjónustupantanir      | Færslureikningar sjóðstreymis | 80       |Nettóbreyting | Nettóupphæð  | Já  |
    | R20     | Heildarinnhreyfinga      | Formúla                  | R10      |Nettóbreyting | Nettóupphæð  | Já  |
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
    | R50     | Umframbirgðir                  | Formúla                  | R20+R40  |Nettóbreyting | Nettóupphæð  | Já  |
    | R60     | Sjóðstreymis sjóður          | Færslureikningar sjóðstreymis | 2100     |Nettóbreyting | Nettóupphæð  | Já  |
    | R70     | Samanlagt sjóðstreymi          | Formúla                  | R50+R60  |Nettóbreyting | Nettóupphæð  | Já  |

    > [!NOTE]
    > Línunúmer R10 er notað til að ná yfir niðurstöðutölur fyrir útistandandi reikninga. Línunúmer R20 er notað ef reikna á samtölu allra inngreiðsla. Línunúmer R30 er notað til að ná yfir niðurstöðutölur fyrir gjaldfallnar greiðslur. Línunúmer R40 er notað ef reikna á samtölu allra útborgana. Línunúmer R50 er notað ef ná á samtölu umframmagns reiðufés. Línunúmer R60 er notað til að ná yfir lausafé. Línunúmer R70 er notað til að reikna áætlað sjóðstreymi.

## <a name="setting-up-a-new-column-definition"></a>Uppsetning á nýrri dálkaskilgreiningu

Áður en Ken getur prentað út Sjóðstreymisspá þarf hann að stofna dálkskilgreininguna fyrir tölulegar upplýsingar. Í dálkunum skilgreinir hann upplýsingarnar sem hann vill nota úr línunum.

- Fyrsti dálkurinn hefur númerið *C10* með heitinu **Upphæð** og inniheldur Hreina breytingu.  
- Annar reiturinn hefur númerið *C20* með heitinu **Staða á dagsetningu** og inniheldur færslur tímabilsins.  
- Þriðji dálkurinn hefur númerið *C30* með heitinu **Allt árið** og inniheldur breytingar á innistæðum fyrir allt reikningsárið.  
- Að lokum úthlutar hann dálkskilgreiningunni sem sjálfgefna valkosti fyrir **fjárhagsskýrsluna spá**.  

### <a name="set-up-a-new-column-definition"></a>Setja upp nýja dálkaskilgreiningu

1. **Í síðunni fjármálaskýrslur** er valið nýja **fjárhagsskýrsluheitið** sem þú stofnaðir. **Á flipanum Forsíða**, í **ferliflokknum**, skal velja **Breyta dálkskilgreiningu**.

2. Stofnið nýja dálkskilgreiningu með heiti **sjóðstreymis**.

3. Velja hnappinn **Í lagi**.

4. Færa inn hverja línu nákvæmlega eins og sýnt er í eftirfarandi töflu.

    |Dálknr.|Dálkfyrirsögn|Dálktegund|Færslutegund|Tegund upphæðar|Sýna|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |C10|Upphæð|Nettóbreyting|Færslur|Nettóupphæð|Alltaf|  
    |C20|Upphæð fram að dagsetningu|Staða til dags.|Færslur|Nettóupphæð|Alltaf|  
    |C30|Allt reikningsárið|Allt reikningsárið|Færslur|Nettóupphæð|Alltaf|

## <a name="assigning-the-column-definition-to-the-financial-report-name"></a>Úthlutun dálkskilgreiningarinnar á heiti fjárhagsskýrslunnar

Ken er nú tilbúið að úthluta dálkskilgreiningu á fjárhagsskýrsluheiti.  

### <a name="assign-the-column-definition-to-the-financial-report-name"></a>Úthluta dálkskilgreiningu á heiti fjárhagsskýrslunnar

1. **Í síðunni ársskýrslur** skal velja **spárfjárhagsskýrsluna** og velja **síðan aðgerðina Breyta dálkskilgreiningu**.  
2. **Í reitnum Heiti** skal velja sjóðstreymissskilgreiningu **sem** á að úthluta sem sjálfgefna dálkskilgreiningu.  

## <a name="view-and-print-the-cash-flow-forecast"></a>Skoða og prenta sjóðsstreymisspá

1. **Í** síðunni ársskýrslur er hægt að velja **spárfjárhagsskýrslu** til að skoða Sjóðstreymisspá.  
2. **Á Fjárhagsskýrslusíðu** er hægt að velja upphæð og skoða síðan sjóðsstreymisspáfærslur sem mynda upphæðina. Að auki er hægt að skoða formúluna sem er notuð til að reikna út þá upphæð. Einnig er hægt að afmarka upphæðir eftir dagsetningu og vídd.  
3. Veldu hnappinn **Prenta** til þess að prenta sjóðstreymisspá.  

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/forecast-cash-flow-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Vinna með ársskýrslur](bi-how-work-account-schedule.md)  
[Greining á sjóðstreymi í fyrirtækinu þínu](finance-analyze-cash-flow.md)  
[Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
