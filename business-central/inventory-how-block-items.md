---
title: Hvernig loka á vörum eða vöruafbrigðum vegna sölu eða innkaupa
description: Hægt er að loka vörum og vöruafbrigðum í línur í sölu- eða innkaupaskjölum og bókast í færslu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, variant, product'
ms.date: 05/16/2024
ms.service: dynamics-365-business-central
---

# Loka vörum eða vöruafbrigðum vegna sölu eða innkaupa

Hægt er að loka vörum og vöruafbrigðum í línur í sölu- eða innkaupaskjölum og hægt er að loka fyrir að þær séu bókaðar í færslum. Til dæmis er þetta gagnlegt þegar vara er með þekktan galla. Ef einhver velur útilokaða vöru eða afbrigði á sölu- eða innkaupaskjali mun boð þess efnis tilkynna þeim að vörunni sé lokað.

Eftirfarandi tafla lýsir því hvað gerist þegar vörum eða afbrigðum er lokað.  

|Valkostur|Heimildasamstæða|  
|--------------------|------------|  
|**Lokað fyrir sölu**|Ekki er hægt að velja vöru eða afbrigði í söluskjali eða birgðabók sölu.|  
|**Lokað fyrir innkaup**|Ekki er hægt að velja vöru eða afbrigði á innkaupaskjali, birgðabók innkaupa eða í vinnslum innkaupaáætlunar.|  
|**Lokað**|Ekki er hægt að taka vöruna eða afbrigðið með þegar færslur eru bókaðar.|  

> [!NOTE]
> Hægt er að skila útilokuðum vörum. Þetta þýðir að engar ofangreindra stillinga gilda fyrir skilapantanir og kreditreikninga.

Þegar aðgerðin **Afrita úr skjali** er notuð til að stofna ný skjöl á grundvelli fyrirliggjandi skjala er tilkynnt hvort vörur eða afbrigði í upprunaskjalslínunum eru lokuð. Útilokaðar fylgiskjalslínur eru ekki í nýja skjalinu og tilkynning sýnir yfirlit yfir allar fylgiskjalalínur sem eru útilokaðar í upprunaskjalinu.

## Lokað á vöru  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
2. Eftir því hvað á að gera er varan valin og síðan valinn einn eða fleiri af eftirfarandi gátreitum:
    * **Lokað**
    * **Lokað fyrir sölu**
    * **Lokað fyrir innkaup**  

## Lokað á vöruafbrigði  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
2. Velja skal vöruna sem er með afbrigði sem á að loka, velja **Afbrigði** og velja síðan einn eða fleiri af eftirfarandi gátreitum:  
    * **Lokað**
    * **Lokað fyrir sölu**
    * **Lokað fyrir innkaup**

## Sjá einnig .  

[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Birgðir](inventory-manage-inventory.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]