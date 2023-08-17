---
title: Safnvista sölu- og innkaupaskjöl
description: 'Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum og endurheimt upprunalegt ef þörf krefur.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 06/02/2023
ms.custom: bap-template
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
---
# <a name="archive-documents"></a>Safnvista skjöl

Þú getur safnvistað sölu- og innkaupapöntunum, tilboðum, skilapöntunum og standandi pöntunum. Safnvistun skjala gerir þér kleift að endurheimta upprunalegt ef þörf krefur. Þú getur safnvistað sölu- eða innkaupaskjali nokkrum sinnum og vistað aðra safnvistaða útgáfu í hvert skipti.

Fyrir safnvistuð söluskjöl þar sem upprunalega skjalið er enn til og er ekki bókað er hægt að nota aðgerðina **Endurheimta** til að skrifa yfir núverandi skjal með safnvistaðri útgáfu.

Fyrir safnvistuð skjöl þar sem upprunalega skjalinu er eytt geturðu aðeins notað efnið aftur með því að afrita gögnin, til dæmis með aðgerðinni **Afrita úr skjali**.  

## <a name="to-set-up-automatic-document-archiving"></a>Setja upp sjálfvirka safnvistun

Hægt er að setja upp sjálfvirka safnvistun á sölu- og innkaupapöntunum, tilboðum, standandi pöntunum og vöruskilapöntunum. Þegar kveikt er á sjálfvirkri safnvistun er ný útgáfa af safnvistaða skjalinu búin til þegar einhver gerir eftirfarandi:

* Breytir eða eyðir athugasemd.
* Prentar, sækir eða sendir skjal í tölvupósti.
* Umbreytir tilboði í pöntun eða reikning.
* Leggur inn pöntun.

Eftirfarandi ferli sýnir hvernig skal setja upp sjálfvirka safnvistun á söluskjölum. Skrefin eru svipuð fyrir innkaupaskjöl.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning sölu og útistandandi** og velja svo viðeigandi tengil.
2. Í flýtiflipanum **Safnvistun** skal tilgreina hvort kveikja eigi á sjálfvirkri safnvistun fyrir ýmsar tegundir af söluskjölum. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Eftirfarandi tafla lýsir valkostunum fyrir reitinn **Safnvista tilboð**.

|Valkostur|Lýsing|
|------|-----------|
|**Aldrei**| Ekki safnvista sölutilboð þegar þeim er eytt.|
|**Spurning**|Biddu notandann um að velja hvort eigi að safnvista sölutilboðum þegar þeim er eytt.|
|**Alltaf**|Safnvista sölutilboðum sjálfkrafa þegar þeim er eytt.|

## <a name="to-manually-archive-a-sales-order"></a>Til að Skjalfæra sölupöntun handvirkt

Eftirfarandi ferli lýsir því hvernig á að Skjalfæra sölupöntun handvirkt. Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.  
2. Opnuð er sölupöntun sem þú vilt kaupa safnvista.  
3. Valin er aðgerðin **Safnvista skjal**.

Sölupöntunin er safnvistuð. Hægt er að skoða hana á síðunni **Safnvistaðar sölupantanir**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Að endurheimta óbókaða sölupöntun úr skjalasafninu

Eftirfarandi ferli útskýrir hvernig skal endurheimta safnvistaða sölupöntun í upprunalega sölupöntun. Endurheimt skjals er aðeins möguleg þegar upprunalega skjalið hefur ekki verið bókað. Skrefin eru svipuð fyrir allar pantanir, standandi pantanir, vöruskilapantanir og tilboð.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Safnvistaðar sölupantanir** og velja síðan viðkomandi tengil.
2. Valin er safnvistuð sölupöntun, eða útgáfa af henni, sem á að endurheimta og velja síðan aðgerðina **Endurheimta**.  

Efni upprunalegrar sölupöntunar er skipt út fyrir safnvistuðu útgáfuna.

## <a name="to-delete-archived-sales-orders"></a>Eyða safnvistuðum sölupöntunum

Nota varðveislureglu til að hreinsa vistuð skjöl sem ekki er lengur þörf fyrir. Varðveislureglur láta stjórnendur skilgreina hversu lengi þeir vilja geyma gögn. Til dæmis geta þeir sett upp stefnu sem eyðir gögnum eftir lokadagsetningu. Frekari upplýsingar er að finna í [Skilgreina varðveislureglur](admin-data-retention-policies.md).

Ýmislegt ber að hafa í huga varðandi stofnun varðveislureglna fyrir eldri skjöl:

* * Ef upprunalega skjalinu hefur ekki verið eytt, mun Viðskiptamiðinu ekki eyða útgáfum í skjalasafni. Eldri útgáfur renna ekki út svo framarlega sem upprunalega er til.
* Þegar varðveisluregla er sett upp er hægt að tilgreina að óskað sé eftir að stefnunni sé eytt í eldri útgáfum skjals nema nýjustu. Til dæmis gætir þú verið með 10 útgáfur af skjali og vilt halda eintak af því nýjasta. 
* Aðalviðskiptamiðlæg reiknar út gildistíma skjala sem byggð eru á dagsetningu nýjustu útgáfu í skjalasafni.

## <a name="see-also"></a>Sjá einnig

[Rekja skjalalínur](across-how-to-track-document-lines.md)  
[Sala](sales-manage-sales.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
