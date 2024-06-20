---
title: Setja upp kóða fyrir endurskoðunarslóðir
description: Kynntu þér verkin til að setja upp upprunakóða og ástæðukóða sem þú getur notað til að fylgjast með eftirlitsferðum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.search.form: '257, 259, 279'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a>Uppsetning upprunakóða og ástæðukóða fyrir endurskoðunarslóðir

Öllum bókuðum færslum er sjálfvirkt úthlutað upprunakóða þannig að hægt er að rekja færslur til uppruna þeirra. Ef gefa á færslum upprunakóta til viðbótar má nota ástæðukóta. Ástæðukótar gefa til kynna hvar færsla var stofnuð. Þegar ástæðukóðar eru settir upp má úthluta þeim til heilla bókarsniðmáta og bókarkeyrslna, og hægt er að úthluta þeim til einstakra bókarlína og skjala.  

Nota skal kóða sem auðvelt er að muna og eru lýsandi. Hægt er að setja upp ótakmarkaðan fjölda kóða.

## <a name="define-source-codes"></a>Skilgreina upprunakóða

Stundum þarf að skoða hvernig ákveðin færsla varð til, t.d. hvort hún varð til við bókun færslubókar eða innkaupareiknings. Upprunakóði gefur til kynna hvar færsla var stofnuð. Færslur eru stofnaðar þegar færslubækur og reikningar eru bókuð og við tilteknar keyrslur. Hver bókunargerð er með tiltekinn upprunakóða sem er úthlutað þegar einstakar færslur eru stofnaðar.  

Við bókun færslubóka, pantana, reikninga og kreditreikninga og notkun ýmissa keyrslna eru stofnaðar færslur á ársreikningum. Nokkrir flýtiflipar eru í glugganum **Uppsetn. upprunakóða**, einn fyrir hvern kerfishluta. Hver flýtiflipi hefur upprunakóðana sem eiga við þann kerfishluta.

Við bókun eða keyrslu er réttur upprunakóði sjálfkrafa hengdur við færsluna. Til dæmis, við bókun úr færslubók er færslan kóðuð sem *FÆRSLUBK*. Síðan er hægt að sía síðuna **fjárhagsfærslur** til að sýna hvaða færslur voru bókaðar úr almennu færslubókinni eða úr söluskjölum, til dæmis

### <a name="to-define-source-codes"></a>Upprunakóðar skilgreindir:

1. Veldu ![Leita að síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") táknið, fara í **Uppsetning upprunakóða** og velja síðan viðkomandi tengil.  

2. Í glugganum **Uppsetning upprunakóða** skal tilgreina viðeigandi upprunakóða fyrir hverja bókunargerð og runuvinnslu.  

Hægt er að breyta innihaldi reits síðar og breytingin mun hafa áhrif á væntanlegar bókanir í framtíðinni.

## <a name="change-source-codes"></a>Breyta upprunakóðum

Hugsanlega þarf að breyta upprunakóða. Til dæmis ef notandi vill breyta upprunakóða *FHFBOK* í *FBK*.

### <a name="to-change-source-codes"></a>Upprunakóðum breytt:

1. Veldu ![Leita að síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") táknið, fara í **Upprunakóðar** og velja síðan viðkomandi tengil.

2. Kóðinn í reitnum **Kóði** er valinn í línunni með kóðanum sem á að breyta.

3. Færa inn nýja kóðann velja síðann hnappinn **Já**. Einnig er hægt að breyta efni reitsins **Lýsing**.

Allar færslur sem á eftir koma og bókaðar eru í færslubók verða með nýja upprunakóðann.

## <a name="define-reason-codes"></a>Skilgreina ástæðukóða

Ástæðukóðar gefa til kynna hvar færsla var stofnuð. Þú getur úthlutað ástæðukóðum í stökum færslum og þú getur úthlutað endanlegum kóðum í tiltekin færslubókarsniðmát og -bókarkeyrslur. Þegar kóðar eru tengdir við færslubókarlínu eða sölu- eða innkaupahaus merkir kerfið allar færslur með ástæðukóðanum þegar það bókar þær.  

### <a name="to-set-up-reason-codes"></a>Uppsetning ástæðukóða

1. Veldu ![Leita að síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn")  táknið, fara í **Ástæðukóðar** og velja síðan viðkomandi tengil.

2. Í glugganum **Ástæðukóðar** er skal færa fyrsta kóðann inn í reitinn **Kóði**. Texti til útskýringar er færður í reitinn **Lýsing**.

Þetta er endurtekið fyrir alla kóða sem á að nota. Hægt er að setja upp kóða að vild.

Eftirfarandi ferli sýnir hvernig á að bæta ástæðukóða við færslubókarsniðmát en svipuð skref eiga við um að bæta ástæðukóða við færslubókarlínu eða bókarkeyrslu.  

### <a name="to-assign-reason-codes-to-journal-templates"></a>Ástæðukóðum úthlutað á færslubókarkeyrslur:

1. Veldu ![Leita að síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn")  táknið, fara í **Sniðmát færslubóka** og velja síðan viðkomandi tengil.

2. Í línunni með valda færslubókarsniðmátinu, í reitnum **Ástæðukóði**, skal tilgreina viðeigandi kóða.

3. Færslubókarsniðmátinu er lokað.

Ástæðukóðinn sem var valinn verður afritaður í nýju færslubókarkeyrsluna sem búin var til með viðkomandi sniðmáti. Ástæðukóðum er úthlutað á færslubókarsniðmát í öðrum kerfishlutum á sama hátt.

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a>Nota ástæðukóða á sölu- og innkaupaskjöl

1. Viðeigandi sölu- eða innkaupaskjal er opnað.

2. Kóðinn er færður í reitinn **Ástæðukóði** í sölu- eða innkaupahaus.

Þegar reikningurinn er bókaður afritast ástæðukóðinn í allar fjarhags-, viðskiptamanna- og lánardrottnafærslur. Ekki er hægt að úthluta mismunandi ástæðukótum í einstakar innkaupa- og sölulínur vegna þess að allar línur bókast sem ein færsla.

## <a name="see-also"></a>Sjá einnig

[Fjármál](finance.md)  
[Afstemming bankareikninga](bank-manage-bank-accounts.md)  
[Vinna með víddir](finance-dimensions.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Greining á sjóðstreymi í fyrirtækinu þínu](finance-analyze-cash-flow.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
