---
title: Nota e-skjöl í sölu og innkaupum
description: Lærðu að nota eiginvirkni e-skjala sem tengjast sölu-og innkaupareikningum.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, purchase'
ms.search.form: '42, 43, 51, 6103, 6133, 6121, 9301, 9305, 9308'
ms.date: 10/03/2023
ms.author: altotovi
---

# Nota e-skjöl í sölu og innkaupum

Hægt er að nota skilgreind rafræn skjöl (e-skjöl) með sölu-og innkaupaskjölum.

Eins er hægt að nota eftirfarandi skjöl fyrir e-skjöl:

- Sölureikninga
- Sölupantanir
- Sölukreditreikninga
- Innkaupareikninga
- Innkaupapantanir
- Innkaupakreditreikninga
- Almennar færslubækur

Eins og er er aðeins hægt að nota innkaupapöntun þegar skjalið er stofnað úr skjali frá lánardrottni. Hins vegar er ekki hægt að uppfæra fyrirliggjandi skjal með línum sem þú fékkst frá lánardrottninum.

## E-skjöl í sölu

Til að stofna og senda e-reikning til viðskiptamanns þarf að stofna og bóka sölureikninginn. Nánari upplýsingar um staðlaða ferlið er að finna  [í Reikningsölu](sales-how-invoice-sales.md).

Eftir að söluskjal hefur verið bókað skal opna  **síðuna bókuð sölureikningur**  til að fá aðgang að tengdri  **E-skjali**  síðu.

### Skoða e-skjöl

Fylgdu þessum skrefum til að skoða tiltæk skjöl.

1.  **Á síðunni bókuð sölureikningur**  er valið  **e-** \> **Fylgiskjal með opnu fylgiskjali**.
2.  **Á síðu E-skjals**  er á hausnum hægt að skoða grunnupplýsingar um bókaða reikninginn.
3. Í  **reitnum færsla**  kemur fram fylgiskjalsnúmer bókaða sölureikningsins. Velja skal tengilinn til að opna skjalið.
4.  **Í svæðinu rafræn staða**  skjals er hægt að skoða stöðu skjalsins og staðsetningar þess í ferli ferlis. Ef skjalið er bókað er staðan  **unnin**.

### E-skjalastöður og annmarkar

Nánari upplýsingar um stöðu þjónustustaða í e-skjali er að leita í  **fastflipa fyrir e-skjalaþjónustu** . Í línunum sýnir kerfið eina eða fleiri þjónustur sem skjalið notar. Í algengustu aðstæðunum notar hvert skjal aðeins eina þjónustu. Skjal getur þó notað margar þjónustur.

- Athuga skal  **reitinn E-Skjalakóti**  til að ákvarða hvaða þjónusta var notuð.
-  **Hakið í reitinn E-Document staða**  til að ákvarða núverandi stöðu þjónustu fyrir þetta skjal.
- Ef óskað er eftir frekari upplýsingum skal velja  **svæðið annmarkar**  fyrir þjónustuna á  **síðunni E-skjalaskanningar** . Sýnt verður frá tímareimayfirliti yfir mismunandi stöður fyrir skjalið.
-  **Athuga Færslunr.** og  **búið til hjá**  reitum, og aðrar upplýsingar á  **síðu E-skjalaannálanna** .  **Í reitnum E-staða**  er  **fyrsta staða flutt út** þar sem fram kemur að E-skjalaskráin hafi verið stofnuð. Næsta staða er send  **, sem gefur til kynna að skjalið hafi verið sent til þjónustuveitanda, ef það er** samskipað.

Nánari innsýn er valin færslan sem hefur  **stöðuna útflutt**  og síðan er keyrð ein af eftirfarandi aðgerðum:

- **Opna vörpunarkladda**  – fá yfirlit yfir öll útflutt svæði úr suðr töflunum í  **reitnum upphaflegt gildi** . Ef reglur um umbreytingu voru notaðar í útflutningsferlinu er einnig hægt að fá lokagildi í  **nýja**  reitnum.
- **Útflutningsskrá**  – Flytja út XML-skrána fyrir handvirka yfirferð.

Til að skoða samskiptin milli þín og þeirrar þjónustu sem þú ert að senda skjalið til skaltu nota  **reitinn Samskiptaskráir** .  **Opnið síðuna samskipti-Skjalaskráir**  til að skoða upplýsingar um beiðnina og ástæður skilaboða við þá þjónustu.

Ef mál er höfðað hjá þjónustuveitanda og ekki er unnt að senda skjalið skal leita að eftirfarandi vísum á  **síðu E-skjals** :

- Í  **reitnum Staða**  rafrænna skjala á hausnum kemur fram  **villustaða** .
-  **Reiturinn Staða**  e-skjals á fastflipanum fyrir  **e-skjalaþjónustu**  sýnir  **villustöðu**  sendingar.
-  **Flipinn Villa og viðvaranir**  inniheldur eitt eða fleiri skilaboð sem gefa upp orsök málefunnar.

Þegar úthreyfing hefur verið föst skal keyra  **Sendingarskjalaaðgerðirnar**  handvirkt. Ef þörf er á mismunandi aðgerðum, svo sem  **endurgerðum,** aflýsa  **skjali**, eða  **fá samþykki** er hægt að keyra þær.

## E-skjöl í innkaupum

Móttöku innkaupa á rafrænum reikningum í  Dynamics 365 Business Central  má gera sem runuvinnslu eða handvirkt.

### Keyrslan er keyrð

> [!NOTE]
> Þessi keyrsla er fyrir sjálfvirka innheimtu reikninga sem berast. Það getur aðeins unnið á landi eða svæði þar sem virknin er til staðar.

Í hvert sinn sem vinnsluröð er keyrð ef utanaðkomandi þjónusta er með innsendum reikningum sem sendir hafa verið frá lánardrottni safnar kerfið og flytur inn reikningana. Fylgdu þessum skrefum til að ljúka ferlinu.

1. Þegar keyrslunni hefur verið lokið er nýinnfluttur reikningur skráður á  **síðuna E-skjöl**  ásamt grunnupplýsingum þeirra.
2. Til að skoða nánar er opnað sérstakt skjal.
3. Ef engar villur eða úthreyfingar voru í e-skjalinu og það er kortlagt,  **·**  sýnir reiturinn númer fylgiskjalsnúmerið á innkaupareikningi sem kerfið stofnaði sjálfkrafa. Velja skal tengilinn til að opna skjalið. Þetta kerfisstofnaða skjal er ekki bókaða skjalið.
4. Veljið  **færslusvæðið**  til að fara beint á innkaupaskjalið. Þegar búið er að  **Opna innkaupareikning**  síðu er leitað í skjalinu. Síðan, ef allt er rétt, bókið skjalið.
5. Þegar innkaupaskjal  **er bókað er reiturinn**  færsla  **í E-skjalinu**  uppfærður frá  **reikningi**  yfir í  **innkaupareikning** og númer bókaða innkaupaskjalsins er tiltækt. Hægt er að velja númerið til að opna bókaða innkaupareikning.

Upplýsingar um lóða eru þær sömu og eru í söluferlinu fyrir e-skjöl.

Þar sem villur í söluferlinu eru að mestu tengdar framboði á þjónustu getur viðtökuskjalið haft að geyma margar ástæður. Algengasta ástæða villu er að kerfið getur ekki þekkt línurnar á e-skjalinu sem þú fékkst frá söluaðila. Því er ekki hægt að færa línur inn í innkaupareikning notanda.

Tvær algengar villur eru:

- Ef óskað er eftir að nota þessa tilteknu línu á reikningi lánardrottins sem bókuð var beint í fjárhag (Fjárhagsreikningur) er rétt að skilgreina gildið fyrir  **vörpun texta** . Ef sneiða á frá þessari villu ef nota á fjárhagsreikninga, skal velja  **varpa texta sem**  á að stofna tiltekna vörpun úr  **gildi fyrir vörpun texta**  með  **debetreikn.** gildi sem ætlunin er að nota.
- Ef rekja á birgðir og notkunarlínur frá reikningi lánardrottins til að fylla út vörur í fylgiskjalslínum verður að skilgreina  **rétt Vörutilvísunarnr.** gildi. Ef sneiða á frá þessari villu skal varpa ytri vörunni með vörunúmerunum með því að nota tilvísunarlistann vara. Til að fá frekari upplýsingar, sjá  [nota vörutilvísanir](inventory-how-use-item-cross-refs.md).

Þegar búið er að lagfæra villur og viðvaranir er hægt að tilgreina handvirkt hvenær kerfið á að stofna innkaupareikning á grundvelli uppsetningar með því að velja  **Stofna skjal**.

### Flytja inn reikninga handvirkt

Ef flytja á inn ytri e-skjöl handvirkt er þessum skrefum fylgt.

1. Veldu þá  ![ljósaperu sem opnast Segðu mér aðgerðina.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn  **E-skjalaþjónustu** og velja síðan tengda tengilinn.
2.  **Á þjónustusíðunni**  E-Document er valin virk þjónusta. 
3. Veldu  **taka á móti** og senda inn skjalaskrána sem þú fékkst hjá lánardrottninum.
4. Ef villuskilaboð koma, opnið þá e-skjalið til að leysa málin.
5. Þegar notandi hefur lokið við að lagfæra úthreyfingar, skal velja  **Stofna skjal**  handvirkt  **í** flokknum innflutningur.
6. Þegar búið er að stofna skjalið í Business Central er hægt að skoða það rétt eins og ef runuvinnsla er notuð.

## Yfirlit yfir e-Document stöður

Til að fá betri yfirsýn yfir öll skjöl í fyrirtækinu er hægt að velja  **hlutverkamiðstöð endurskoðanda**  þar sem staða e-skjals er til staðar. Þar má finna starfsemi e-skjala sem hafa á eftirfarandi stöðum að:

- **Send e-skjöl:**

    - Meðhöndlað
    - Í vinnslu
    - Villa

- **Komandi e-skjöl:**

    - Meðhöndlað
    - Í vinnslu
    - Villa

## Sjá einnig .

[Hvernig á að setja upp e-skjöl í Viðskiptamiðl-](finance-how-setup-edocuments.md)  
[Hvernig á að framlengja e-skjöl í Viðskiptamiðl-](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Fjármálastjórnun](finance.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Skrá innkaup með innkaupareikningum og pöntunum](purchasing-how-record-purchases.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
