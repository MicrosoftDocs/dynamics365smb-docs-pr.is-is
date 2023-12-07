---
title: Notaðu rafræn skjöl við sölu og innkaup
description: Lærðu hvernig á að nota rafræn skjöl virkni sem tengist sölu- og innkaupareikningum.
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

# Notaðu rafræn skjöl við sölu og innkaup

Hægt er að nota stillt rafræn skjöl (e-skjöl) með sölu- og innkaupaskjölum.

Þú getur notað eftirfarandi skjöl með rafrænum skjölum:  

- Sala: 
    - Sölureikningar
    - Sölupantanir
    - Sölukreditreikningar
    - Þjónustureikningar
    - Þjónustukreditreikningar
    - Gjaldskrár fjármálafyrirtækja
    - Innheimtubréf
- Innkaup: 
    - Innkaupareikningar
    - Innkaupapantanir (aðeins búið til nýtt skjal)
    - Kaupa kreditnótur
    - Almennar færslubækur

> [!NOTE]
> Eins og er er aðeins hægt að nota innkaupapöntun þegar þú býrð til skjalið úr rafrænu skjalinu frá lánardrottnum þínum. Hins vegar geturðu ekki uppfært núverandi skjal með línum sem þú fékkst frá lánardrottni þínum.  

## Rafræn skjöl í sölu

Til að búa til og senda rafrænan reikning til viðskiptavinar þarf að búa til og bóka sölureikninginn. Til að læra meira um staðlaða ferlið, sjá [Reikningarsala](sales-how-invoice-sales.md).

Eftir að þú hefur birt söluskjalið skaltu opna  **Bókaður sölureikningur** síðuna til að fá aðgang að tengdu **E-skjalinu** síðunni.

### Skoða rafræn skjöl

Fylgdu þessum skrefum til að skoða núverandi rafræn skjöl.

1. Á síðunni **Bókaður sölureikningur**  skaltu velja **E-skjal** \> **Open E-Document**.
2. Á  **E-Document** síðunni, í hausnum, er hægt að skoða grunnupplýsingar um bókaðan reikning.
3. Reiturinn **Skrá**  sýnir skjalanúmer bókaðs sölureiknings. Veldu tengilinn til að opna skjalið.
4. Í reitnum **Staða rafrænna skjala**  er hægt að skoða rauntímastöðu skjalsins og staðsetningu þess í vinnsluferlinu. Ef skjalið er póstað er staðan **Afgreidd**.

### Staða rafrænna skjala og logs

Til að fá upplýsingar um þjónustustöðustig rafrænna skjalsins þíns skaltu skoða **Staða rafrænna skjalaþjónustu** Hraðflipann. Á línunum sýnir kerfið eina eða fleiri þjónustur sem skjalið notaði. Í algengustu atburðarásinni notar hvert skjal aðeins eina þjónustu. Hins vegar getur skjal notað margar þjónustur.

- Athugaðu  **E-skjalaþjónustukóði** reitinn til að ákvarða hvaða þjónusta var notuð.
- Athugaðu  **E-Document Status** reitinn til að ákvarða núverandi þjónustustöðu fyrir þetta skjal.
- Ef þú vilt fá frekari upplýsingar skaltu velja **Logs** reitinn fyrir þjónustuna á  **E-Document Logs** síðunni. Sýnt er tímaröð yfir mismunandi stöður skjalsins.
- Athugaðu  **færslunr.** og **Búið til á** reitunum og aðrar upplýsingar um **E-skjalaskrár** síðu. Í  **E-skjalastaða** reitnum er fyrsta staða **Exported**, sem gefur til kynna að e-skjalaskráin hefur verið búið til. Næsta staða er **Sent**, sem gefur til kynna að skjalið hafi verið sent til þjónustuveitunnar, ef það er stillt.

Til að fá frekari innsýn skaltu velja færsluna sem hefur stöðuna **Exported** og keyra síðan eina af eftirfarandi aðgerðum:

- **Opnaðu kortlagningarskrár** – Fáðu yfirlit yfir alla útfluttu reiti úr töflunum sem þú hefur fengið í reitnum **Upprunalegt gildi** . Ef þú notaðir umbreytingarreglur í útflutningsferlinu geturðu líka fengið lokagildið í reitnum **Nýtt gildi** .
- **Flytja út skrá** – Flytja út XML skrána til handvirkrar skoðunar.

Til að skoða samskipti þín og þjónustunnar sem þú sendir skjalið þitt til skaltu nota reitinn **Communication Logs** . Opnaðu **E-Document Communication Logs** síðuna til að skoða upplýsingar um beiðnina og ástæðuskilaboðin með þeirri þjónustu.

Ef það er vandamál hjá þjónustuveitunni og ekki er hægt að senda skjalið skaltu leita að eftirfarandi vísbendingum á  **E-Document** síðunni:

- Reiturinn **Rafræn skjalastaða** í hausnum sýnir **Villa** stöðuna.
-  **E-skjalastaða** reiturinn á **E-skjalaþjónustustaða** Flýtiflipann sýnir **Sendingarvilla** staða.
-  **Villa og viðvaranir** Flýtiflipi inniheldur eitt eða fleiri skilaboð sem gefa upp orsök vandans.

Eftir að málið hefur verið lagað skaltu keyra handvirkt  **Senda skjal** aðgerðirnar. Ef þú þarft mismunandi aðgerðir, eins og **Endurbúið skjal**, **Hætta við skjal** eða **Fáðu samþykki**, þú getur keyrt þá.

## Rafræn skjöl í innkaupum

Móttaka rafrænna innkaupareikninga í Dynamics 365 Business Central er hægt að gera sem lotuvinnu eða handvirkt.

### Keyra runuvinnuna

> [!NOTE]
> Þetta runuverk er fyrir sjálfvirka innheimtu á reikningum sem koma inn. Það getur aðeins virkað í landi eða svæði þar sem virknin er til staðar.

Í hvert skipti sem vinnuröð er keyrð, ef ytri þjónustan er með reikninga á innleið sem voru sendir frá lánardrottnum þínum, safnar kerfið inn og flytur inn þessa reikninga. Til að ljúka ferlinu skaltu fylgja þessum skrefum.

1. Eftir að runuvinnunni er lokið eru nýinnfluttir reikningar skráðir á **Rafræn skjöl**  síðu, ásamt grunnupplýsingum þeirra.
2. Til að skoða nánari upplýsingar skaltu opna tiltekið e-skjal.
3. Ef engar villur eða vandamál voru í rafrænu skjalinu og það er kortlagning sýnir reiturinn **Record** skjalsnúmer innkaupareikningsins sem kerfið bjó til sjálfkrafa. Veldu tengilinn til að opna skjalið. Þetta kerfisbundna skjal er ekki bókað skjal.
4. Til að fara beint í innkaupaskjalið skaltu velja reitinn **Record** . Eftir að þú hefur opnað síðuna **Innkaupareikningur**  skaltu athuga skjalið. Síðan, ef allt er rétt, póstaðu skjalinu.
5. Þegar þú bókar innkaupaskjalið er **Record** reiturinn á **E-skjalinu** uppfærður frá **Reikning** til **Kaupreikning** og númer bókaðs innkaupaskjals er tiltækt. Þú getur valið númerið til að opna bókaðan innkaupareikning.

Upplýsingar um annála eru þær sömu og þær eru í söluferli rafrænna skjala.

Vegna þess að villur í söluferlinu eru að mestu tengdar framboði þjónustunnar getur innkomið skjal innihaldið margar ástæður. Algengasta ástæðan fyrir villu er sú að kerfið þekkir ekki línurnar á rafrænu skjalinu sem þú fékkst frá söluaðilanum þínum. Þess vegna getur það ekki slegið inn línur í innkaupareikningnum þínum.

Það eru tvær algengar villur:

- Ef þú vilt nota þessa tilteknu línu af reikningi lánardrottins þíns sem var bókaður beint á fjárhagsreikninginn, verður þú að hafa stillt  **kortatexta** gildið rétt. Til að komast framhjá þessari villu ef þú vilt nota G/L reikninga skaltu velja **Map Text to Account** til að búa til ákveðna kortlagningu á **Mapping Text** gildi með **Debet Acc. Nei.** gildi sem þú vilt nota.
- Ef þú vilt fylgjast með birgðum og nota línur af reikningi lánardrottins til að fylla út vörur á skjalalínunum þínum, verður þú að hafa rétt stillt  **vörutilvísunarnr.** gildi. Til að komast framhjá þessari villu skaltu kortleggja ytri hlutinn með vörunúmerum þínum með því að nota vörutilvísunarlistann. Til að fá frekari upplýsingar, sjá [Nota vörutilvísanir](inventory-how-use-item-cross-refs.md).

Eftir að þú hefur lagað villurnar og viðvaranirnar geturðu handvirkt tilgreint hvenær kerfið ætti að búa til innkaupareikning byggt á uppsetningu þinni með því að velja **Búa til skjal**.

### Flytja inn reikninga handvirkt

Til að flytja inn ytri rafræn skjöl handvirkt skaltu fylgja þessum skrefum.

1. Veldu ![peruna sem opnar Segðu mér eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **E-Document Service** og veldu síðan tengda hlekkinn.
2. Á síðunni **E-skjalaþjónusta**  skaltu velja virku þjónustuna. 
3. Veldu **Receive** og hladdu upp e-skjalaskránni sem þú fékkst frá seljanda.
4. Ef villuboð koma upp skaltu opna e-skjalið til að laga vandamálin.
5. Þegar þú hefur lokið við að laga vandamál, í hópnum **Flytja inn handvirkt**, skaltu velja **Create Document**.
6. Eftir að skjalið er búið til í Business Central geturðu skoðað það alveg eins og þú gerir ef þú notar runuvinnu.

## Yfirlit yfir stöðu rafrænna skjala

Til að fá betri yfirsýn yfir öll rafræn skjöl í fyrirtækinu er hægt að velja  **Bókhaldari** hlutverkamiðstöð þar sem stöður rafrænna skjala eru til staðar. Þar geturðu fundið rafræn skjalastarfsemi sem hefur eftirfarandi stöður:

- **Sendandi rafræn skjöl:**

    - Meðhöndlað
    - Í vinnslu
    - Villa

- **Rafræn skjöl sem berast:**

    - Meðhöndlað
    - Í vinnslu
    - Villa

## Sjá einnig .

[Hvernig á að setja upp rafræn skjöl í Business Central](finance-how-setup-edocuments.md)  
[Hvernig á að framlengja rafræn skjöl í Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Fjármálastjórnun](finance.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Skráðu innkaup með innkaupareikningum og pöntunum](purchasing-how-record-purchases.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
