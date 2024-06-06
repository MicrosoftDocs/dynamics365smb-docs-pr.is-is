---
title: Gera sjóðstreymisspár með fjárhagsskýrslum
description: Í þessari kynningu er lýst hvernig hægt er að nota fjárhagsskýrslur til að búa til sjóðstreymisspár í Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 08/18/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Kynning: Að gera sjóðstreymisspár með fjárhagsskýrslum

Í þessari kynningu er lýst hvernig hægt er að nota fjárhagsskýrslur til að búa til sjóðstreymisspár. Fjárhagsskýrslur framkvæma útreikninga sem ekki er hægt að framkvæma beint í myndriti yfir sjóðstreymisreikninga. Í fjárhagsskýrslum er hægt að setja upp millisamtölur fyrir sjóðstreymismóttökur og heildarútborganir. Þessar millisamtölur er hægt að hafa með í nýjum samtölum sem síðan er hægt að nota til að gera sjóðstreymisspár.  

## Um kynninguna

Þessi kynning fjallar um eftirfarandi verk:  

- Setja upp nýtt heiti fjárhagsskýrslu sjóðstreymis.  
- Setja upp fjárhagsskýrslulínur.  
- Setja upp nýja dálkskilgreiningu.  
- Úthlutun dálkskilgreiningar á fjárhagsskýrslu.  
- Sjóðstreymisspá skoðuð og prentuð.  

### Frumskilyrði

Til að ljúka þessari kynningu þarf:  

- [!INCLUDE[prod_short](includes/prod_short.md)]  
- Vinnublað sjóðstreymis með skráðum línum  

## Hlutverk

Þessi kynning sýnir þau verk sem framkvæmd eru með eftirfarandi hlutverkum notenda:  

- Eftirlitsmaður  

## Ferill

Ken er fjármálastjóri á CRONUS sem gerir mánaðarlega sjóðstreymisspár. Ken inniheldur fjármál, sölu, innkaup og eignir í spánum og birtir CFO Sara fyrir viðskiptainnsýn.  

## Setja upp nýtt heiti fjárhagsskýrslu

Heiti fjárhagsskýrslunnar er nafnið sem þú gefur sjóðstreymisspánni sem inniheldur röð af skilgreindum línum og dálkskilgreiningu.  

### Setja upp nýtt heiti fjárhagsskýrslu  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Fjárhagsskýrslur** og velja síðan viðkomandi tengil.  
2. Á síðunni **Fjárhagsskýrslur** skal velja aðgerðina **Nýtt** til að búa til nýtt heiti fjárhagsskýrslu sjóðstreymis.  
3. Í reitinn **Heiti** skal færa inn **Spá**.  
4. Í reitnum **Lýsing** færið inn **Lýsing fyrir sjóðstremisspá**.  
5. Skildu reitina **Línuskilgreining** og **Dálkskilgreining** eftir auða.

## Setja upp línuskilgreiningar

Eftir að heiti fjárhagsskýrslu er sett upp skilgreinir Ken hverja línu í fjárhagsskýrslu sjóðstreymis. Ken skilgreinir línur sem á að sýna í skýrslum auk lína sem eru eingöngu fyrir útreikninga.  

### Setja upp línuskilgreiningar  

1. Á síðunni **Fjárhagsskýrslur** skaltu velja nýju fjárhagsskýrsluna **Spá** sem þú bjóst til, síðan velja aðgerðina **Breyta línuskilgreiningu**.  
2. Á síðunni **Línuskilgreining** skal færa inn hverja línu eins og sýnt er í eftirfarandi töflu.  

    > [!TIP]  
    > Notaðu aðgerðina **Setja inn CF-reikninga** til að merkja hratt, grafi sjóðstreymireikninga, sjóðstreymireikninga sem þú vilt og afrita þá í línur línuskilgreiningar.  

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
    | R20     | Heildarsjóðstekjur      | Formúla                  | R10      |Nettóbreyting | Nettóupphæð  | Já  |
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
    | R60     | Sjóðstreymissjóðir          | Færslureikningar sjóðstreymis | 2100     |Nettóbreyting | Nettóupphæð  | Já  |
    | R70     | Heildarsjóðstreymi          | Formúla                  | R50+R60  |Nettóbreyting | Nettóupphæð  | Já  |

    > [!NOTE]
    > Línunúmer R10 er notað til að ná yfir niðurstöðutölur fyrir útistandandi reikninga. Línunúmer R20 er notað ef reikna á samtölu allra inngreiðsla. Línunúmer R30 er notað til að ná yfir niðurstöðutölur fyrir gjaldfallnar greiðslur. Línunúmer R40 er notað ef reikna á samtölu allra útborgana. Línunúmer R50 er notað ef ná á samtölu umframmagns reiðufés. Línunúmer R60 er notað til að ná yfir lausafé. Línunúmer R70 er notað til að reikna áætlað sjóðstreymi.

## Setja upp nýja dálkskilgreiningu

Áður en sjóðsstreymisspáin er prentuð þarf Ken að búa til dálkaskilgreiningu fyrir tölulegar upplýsingar. Í dálkunum skilgreinir Ken upplýsingarnar sem þarf til að nota úr línunum.

- Fyrsti dálkurinn hefur númerið *C10* með heitinu **Upphæð** og inniheldur Hreina breytingu.  
- Annar reiturinn hefur númerið *C20* með heitinu **Staða á dagsetningu** og inniheldur færslur tímabilsins.  
- Þriðji dálkurinn hefur númerið *C30* með heitinu **Allt árið** og inniheldur breytingar á innistæðum fyrir allt reikningsárið.  
- Að lokum úthlutar Ken dálkskilgreiningunni sem sjálfgefnum valkosti fyrir fjárhagsskýrsluna **Spá** .  

### Setja upp nýja dálkskilgreiningu

1. Á síðunni **Fjárhagsskýrslur** skaltu velja nýju fjárhagsskýrsluheitið **Spá** sem þú bjóst til. Á flipanum **Heim** í flokknum **Vinna** skal velja **Breyta dálkskilgreiningu**.

2. Búðu til nýja dálkskilgreiningu með heitinu **Sjóðstreymi**.

3. Velja hnappinn **Í lagi**.

4. Færa inn hverja línu nákvæmlega eins og sýnt er í eftirfarandi töflu.

    |Dálknr.|Dálkfyrirsögn|Dálktegund|Færslutegund|Tegund upphæðar|Sýna|  
    |----------|-------------|-----------|-----------------|-----------|----|
    |C10|Upphæð|Nettóbreyting|Færslur|Nettóupphæð|Alltaf|  
    |C20|Upphæð til dags|Staða til dags.|Færslur|Nettóupphæð|Alltaf|  
    |C30|Allt reikningsárið|Allt reikningsárið|Færslur|Nettóupphæð|Alltaf|

## Að úthluta dálkskilgreiningu á fjárhagsskýrsluheiti

Ken er nú tilbúinn til að úthluta dálkskilgreiningu á fjárhagsskýrsluheitið.  

### Úthluta dálkskilgreiningu á fjárhagsskýrsluheiti

1. Á síðunni **Fjárhagsskýrslur** skaltu velja fjárhagsskýrsluna **Spá**, síðan velja aðgerðina **Breyta dálkskilgreiningu**.  
2. Í reitnum **Heiti** skaltu velja dálkskilgreininguna **Sjóðstreymi** til að úthluta sem sjálfgefna dálkskilgreiningu.  

## Skoða og prenta sjóðstreymisspána

1. Á síðunni **Fjárhagsskýrslur** skal velja fjárhagsskýrsluna **Spá** til að skoða sjóðsstreymisspána.  
2. Á síðunni **Fjárhagsskýrsla** er hægt að velja upphæð og síðan skoða sjóðstreymisspáfærslur sem mynda upphæðina. Að auki er hægt að sjá formúluna sem notuð er til að reikna út þá upphæð. Einnig er hægt að afmarka upphæðir eftir dagsetningu og vídd.  
3. Veldu hnappinn **Prenta** til þess að prenta sjóðstreymisspá.  

## Sjá einnig .

[Vinna með fjárhagsskýrslur](bi-how-work-account-schedule.md)  
[Greining á sjóðstreymi í fyrirtækinu þínu](finance-analyze-cash-flow.md)  
[Kynningar á viðskiptaferli](walkthrough-business-process-walkthroughs.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
