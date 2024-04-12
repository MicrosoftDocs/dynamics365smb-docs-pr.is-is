---
title: Nota tölvupóstskjöl í sölu
description: Læra að nota tölvupóstskjöl sem tengjast sölu.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice, sales, deliver'
ms.search.form: '42, 43, 132, 6103, 6133, 6121, 9301, 9305'
ms.date: 03/29/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---

# Nota tölvupóstskjöl í söluferlinu

Hægt er að nota grunnstillt rafræn skjöl (e-documents) með söluskjölunum.

Hægt er að nota eftirfarandi söluskjöl með virkni tölvupóstskjala:  

- Sölureikningar
- Sölupantanir
- Sölukreditreikningar
- Þjónustureikningar
- Þjónustukreditreikningar
- Vaxtareikningar
- Áminningar

## E-skjöl í sölu  

Til að stofna og senda tölvupóstreikning til viðskiptamanns þarf að stofna og bóka sölureikninginn. Nánari upplýsingar um stöðluðu ferlið eru [í Reikningssala](sales-how-invoice-sales.md).

Þegar söluskjalið hefur verið bókað er síðan Bókaður sölureikningur opnaður **til að opna síðuna Tengdur** E-fylgiskjal **.** 

### Skoða tölvupóstskjöl   

Til að skoða fyrirliggjandi e-skjöl skal fylgja þessum skrefum.

1. Á síðunni **Bókaður sölureikningur** skal velja **E-skjal** \> **opna e-fylgiskjal**.
2. Á síðunni **E-fylgiskjal** á hausnum er hægt að skoða grunnupplýsingar um bókaða reikninginn.
3. Reiturinn **Færsla** sýnir fylgiskjalsnúmer bókaða sölureikningsins. Velja skal tengilinn til að opna skjalið.
4. Í reitnum **Staða** rafræns skjals er hægt að skoða rauntímastöðu skjalsins og staðsetningu þess í vinnsluleiðslunni. Ef skjalið er bókað er **staðan Í vinnslu**.

### Staða og skráningar í tölvupósti 

Nánari upplýsingar um þjónustustöðustig tölvupóstskjalsins eru í flýtiflipanum Staða **þjónustu í tölvupósti** . Í línunum sýnir kerfið eina eða fleiri þjónustu sem skjalið notaði. Í algengustu dæminu notar hvert fylgiskjal aðeins eina þjónustu. Hins vegar getur skjal notað margar þjónustur.

- Haka í reitinn **Þjónustukóti** tölvupóstskjals til að ákvarða hvaða þjónusta var notuð.
- Reiturinn **Staða tölvupóstskjals** er athugaður til að ákvarða núverandi þjónustustöðu fyrir þetta fylgiskjal.
- Ef óskað er eftir nánari upplýsingum skal velja reitinn **Skráir** fyrir þjónustuna á síðunni **Skráningar í e-skjölum** . Yfirlit yfir mismunandi stöður skjalsins er birt.
- Reiturinn Færslunr **.** og **Stofnað í** reitum og aðrar upplýsingar á síðunni **E-Document Logs** . Í reitnum **Staða** tölvupóstskjals er **fyrsta staðan Flutt út** sem gefur til kynna að skráin hafi verið stofnuð í tölvupóstskjalinu. Næsta staða er Sent **, sem gefur til kynna að skjalið hafi verið sent til þjónustuveitu, ef það er** grunnstillt.

Nánari innsýn er valin færslan sem hefur **stöðuna Útflutt** og keyrt eina af eftirfarandi aðgerðum:

- **Opna vörpunarskrár**  – Fá yfirlit yfir alla útflutta reiti úr upprunalegu töflunum í reitnum **Upphaflegt virði** . Ef notaðar eru umbreytingarreglur í útflutningsferlinu er einnig hægt að fá lokagildið í reitnum **Nýtt virði** .
- **Flytja út skrá** – Flytja XML-skrána út til handvirkar endurskoðunar.

Til að skoða samskipti milli þíns og þjónustunnar sem þú sendir skjalið til er reiturinn **Samskiptaskráningar notaður** . Opna síðuna **Samskiptaskrár tölvupóstskjala** til að skoða upplýsingar um beiðnina og ástæðuskilaboðin með þeirri þjónustu.

Ef eitthvað er til hjá þjónustuveitanda og ekki er hægt að senda skjalið skal leita að eftirfarandi vísum á síðunni **E-fylgiskjal** :

- Reiturinn **Staða** rafræns skjals í hausnum sýnir stöðuna **Villa** .
- Reiturinn **Staða tölvupóstskjals** á flýtiflipanum **Þjónustustaða** sendingar **sýnir stöðuna Villa** við sendingu.
- Á **flýtiflipanum Villur og Viðvaranir** er að finna eitt eða fleiri boð sem gefa út ástæðu þess.

Þegar úthreyfingin hefur verið föst er aðgerðin **Senda fylgiskjal** keyrð handvirkt. Ef þörf er á mismunandi aðgerðum, svo sem **Endurgerð skjals**, **Hætta við skjal** eða **Sækja samþykki**, er hægt að keyra þær.

## Yfirlit yfir stöður tölvupóstskjala

Til að fá betra yfirlit yfir öll tölvupóstskjöl í fyrirtækinu er hægt að velja mitt hlutverk í endurskoðendahlutverkinu **þar** sem staða e-skjala er til. Þar er hægt að finna aðgerðir í tölvupósti sem hafa eftirfarandi stöðu:

- **Tölvupóstskjöl á útleið:**

    - Meðhöndlað
    - Í vinnslu
    - Villa


## Sjá einnig .

[Hvernig á að setja upp tölvupóstskjöl í Business Central](finance-how-setup-edocuments.md)  
[Hvernig á að framlengja tölvupóstskjöl í Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Fjármálastjórnun](finance.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Skrá innkaup með innkaupareikningum og pöntunum](purchasing-how-record-purchases.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
