---
title: Kaupa vörur fyrir sölu
description: 'Úr sölureikningi, til að kaupa vörur, geturðu stofnað innkaupareikning fyrir lánardrottinn eða birgja.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'supply planning, sales demand, replenish'
ms.search.form: '50, 51, 56, 9308'
ms.date: 03/14/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Innkaupavörur til sölu með því að búa til innkaupareikninga

Frá sölupöntunum og sölureikningum geturðu notað aðgerð til stofna á skjótan hátt innkaupaskjöl fyrir vörumagn sem vantar en er krafist við söluna. Hægt er að nota tvær mismunandi aðgerðir, eftir gerð skjalsins.

> [!Note]
> Þessi virkni er til þess að endurnýja söluvöru í eigin birgðum. Til að kaupa vörur fyrir beina afhendingu frá lánardrottni þínum til viðskiptamanna þarftu að búa til beina sendingu. Frekari upplýsingar eru í [Beinar sendingar](sales-how-drop-shipment.md).   

|Virkni|Description|
|--------|-----------|
|**Stofna innkaupapantanir**|Frá sölupöntun, stofnar þessi aðgerð innkaupapöntun fyrir hvern lánardrottinn vöru á sölupöntuninni. Þú getur breytt innkaupamagninu áður en þú stofnar innkaupapantanirnar. Aðeins er ótiltækt sölumagn lagt til.
|**Stofna innkaupareikning**|Úr sölupöntun og úr sölureikningi getur þessi aðgerð stofnað innkaupareikning fyrir valinn lánardrottinn fyrir allar línur eða valdar línur í söluskjalinu. Lagt er til fullt sölumagn.|

## Stofna eina eða fleiri innkaupapöntun úr sölupöntun
Til að stofna innkaupapöntun fyrir hvert ótiltækt vörumagn í sölupöntuninni, notarðu **Stofna innkaupapantanir** aðgerðina.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.
2. Opnuð er sölupöntun sem þú vilt kaupa vörur fyrir.
3. Velja **stofna innkaupapantanir** aðgerð.

    Síðan **stofna innkaupapantanir** opnast og birtir eina línu fyrir hverja vöru í sölupöntuninni. Línur fyrir bæði fullkomlega tiltækt sölumagn og ótiltækt sölumagn (grámaðar) eru sýndar að sjálfgefnu. Þú getur valið **sýna ótiltækt** aðgerðina til að sjá aðeins línur fyrir ótiltækt sölumagn.

    Reiturinn **Magn til innkaupa** inniheldur ótiltækt sölumagn að sjálfgefnu.
4. Til að kaupa annað magn en ótiltækt sölumagn, skal breyta gildinu í **Magn til innkaupa** reitnum.

    > [!NOTE]  
    >   Þú getur líka breytt **Magn til innkaupa** reitnum á grámuðum línum jafnvel þótt þær sýni fullkomlega tiltækt sölumagn.
5. Velja hnappinn **Í lagi**.

    Innkaupapöntun er stofnuð fyrir hvern lánardrottinn vöru á sölupöntuninni, og í henni eru allar magnbreytingar sem þú kannt að hafa gert á síðunni **Stofna innkaupapöntun**.
7. Halda áfram að vinna innkaupapöntun eða pantanir, til dæmis með því að breyta eða bæta við innkaupareikningslínum. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).


## Stofna innkaupareikning úr sölupöntun eða sölureikningi
Til að stofna stakan innkaupareikning fyrir eina eða fleiri línur í söluskjali með því að velja fyrst hvaða lánardrottni skal kaupa af, notarðu **Stofna innkaupareikning** aðgerðina.

> [!NOTE]  
>   Þessi aðgerð stofnar innkaupareikning fyrir nákvæmlega það vörumagn sem er á valda söluskjalinu. Til að breyta innkaupamagninu, þarftu að breyta innkaupareikningnum eftir að þú stofnar hann.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.
2. Opnuð er sölureikningur sem þú vilt kaupa vörur fyrir.
3. Veldu eitt eða fleiri sölureikningslínur sem þú vilt nota á innkaupareikningur. Til að nota allar sölureikningslínur er annaðhvort þær allar valdar eða engar línur valdar.
4. Velja **stofna innkaupareikning** aðgerð.
5. Veldu annað hvort **Allar línur** eða  **valdar línur** og velja svo **Í lagi** hnappinn.  
6. Í listanum yfir lánardrottna sem birtist skaltu velja lánardrottin sem þú vilt kaupa allar vörurnar af, og þá velja **Í lagi** hnappinn.

    Innkaupareikningur er stofnaður sem inniheldur eina, fleiri en eina eða allar línur sölureikningsins.
7. Halda áfram að vinna innkaupareikning, til dæmis með því að breyta eða bæta við innkaupareikningslínum. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).

## Sjá einnig .
[Innkaup](purchasing-manage-purchasing.md)  
[Skrá innkaup](purchasing-how-record-purchases.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
[Skrá nýja lánardrottna](purchasing-how-register-new-vendors.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]