---
title: Safnvista sölu- og innkaupaskjöl
description: 'Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/26/2024
ms.custom: bap-template
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
ms.service: dynamics-365-business-central
---
# Geyma skjöl

Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum. Ef notaðar eru aðgerðir verkefnastjórnunar er einnig hægt að geyma verkefnin. Hægt er að geyma skjöl og verkefni nokkrum sinnum, sem vistar aðra geymda útgáfu í hvert skipti.

Ef frumritið er enn til fyrir söluskjöl og er ekki bókað er hægt að nota aðgerðina **Endurheimta** til að skrifa yfir það með geymdri útgáfu. 

> [!NOTE]
> Aðeins er hægt að endurheimta söluskjöl og verkefni. Aðgerðin er ekki tiltæk fyrir skráð innkaupaskjöl.

Fyrir geymd skjöl þar sem frumritinu er eytt er hægt að endurnota efnið með því að afrita gögnin, til dæmis með því að nota aðgerðina Afrita úr **skjali** .  

## Setja upp sjálfvirka safnvistun

Hægt er að gera skjalavistun sjálfvirka til að búa til nýja útgáfu af geymda skjalinu þegar einhver gerir eftirfarandi hluti:

* Breytir eða eyðir skjali eða verki.
* Prentar, sækir eða sendir skjal í tölvupósti.
* Umbreytir tilboði í pöntun eða reikning.
* Leggur inn pöntun.

Eftirfarandi skref lýsa því hvernig á að setja upp sjálfvirka geymslu söluskjala á síðunni **Sölugrunnur** . Skrefin eru svipuð fyrir innkaupaskjöl og verkefni. Fyrir innkaupaskjöl er síðan Innkaup **notuð** . Fyrir verkefni skal nota síðuna **Verkuppsetning** .

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sölu og útistandandi** og velja svo viðeigandi tengil.
2. Í flýtiflipanum **Safnvistun** skal tilgreina hvort kveikja eigi á sjálfvirkri safnvistun fyrir ýmsar tegundir af söluskjölum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Eftirfarandi tafla lýsir valkostunum fyrir reitinn **Safnvista tilboð**.

|Valkostur|Lýsing|
|------|-----------|
|**Aldrei**| Ekki safnvista sölutilboð þegar þeim er eytt.|
|**Spurning**|Biddu notandann um að velja hvort eigi að safnvista sölutilboðum þegar þeim er eytt.|
|**Alltaf**|Safnvista sölutilboðum sjálfkrafa þegar þeim er eytt.|

## Til að geyma sölupöntun handvirkt

Eftirfarandi ferli lýsir því hvernig á að geyma sölupöntun handvirkt. Skrefin eru svipuð fyrir öll skjöl og verkefni sem hægt er að geyma.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Opnuð er sölupöntun sem þú vilt kaupa safnvista.  
3. Valin er aðgerðin **Safnvista skjal**.

Sölupöntunin er safnvistuð. Hægt er að skoða hana á síðunni **Safnvistaðar sölupantanir**.

## Endurheimta söluskjal sem ekki er bókað eða verkefni úr safninu

Eftirfarandi ferli útskýrir hvernig skal endurheimta safnvistaða sölupöntun í upprunalega sölupöntun. Endurheimt skjals er aðeins mögulegt þegar upprunalega skjalið er ekki bókað. Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð og einnig fyrir verkefni.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Safnvistaðar sölupantanir** og velja síðan viðkomandi tengil.
2. Valin er safnvistuð sölupöntun, eða útgáfa af henni, sem á að endurheimta og velja síðan aðgerðina **Endurheimta**.  

Innihaldi upphaflegu sölupöntunarinnar eða verksins er skipt út fyrir geymdu útgáfuna.

## Til að eyða geymdar útgáfur

Notaðu varðveislustefnu til að hreinsa geymdar útgáfur sem þú þarft ekki lengur. Varðveitingarreglur gera stjórnendum kleift að skilgreina hversu lengi þeir vilja geyma gögn. Til dæmis er hægt að setja upp stefnu sem eyðir gögnum eftir fyrningardagsetningu. Nánari upplýsingar eru notaðar til að [skilgreina varðveitingarstefnur](admin-data-retention-policies.md).

Ýmislegt er hægt að hafa í huga við að búa til varðveitingarstefnu fyrir geymd skjöl og verkefni:

* Ef upprunalega skjalinu er ekki eytt [!INCLUDE [prod_short](includes/prod_short.md)]  eyðir það ekki geymdar útgáfur. Geymdar útgáfur renna ekki út svo lengi sem frumritið er til.
* Þegar varðveitingarstefnan er sett upp er hægt að tilgreina að stefnan eigi að eyða öllum geymdar útgáfur nema þær nýjustu. Til dæmis gæti notandi haft 10 útgáfur og ætlunin er að halda afrit af því nýjasta. 
* [!INCLUDE [prod_short](includes/prod_short.md)] reiknar út fyrningardagsetningu skjala samkvæmt dagsetningu síðustu útgáfu skjalasafnsins.

## Sjá einnig

[Rekja skjalalínur](across-how-to-track-document-lines.md)  
[Sala](sales-manage-sales.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
