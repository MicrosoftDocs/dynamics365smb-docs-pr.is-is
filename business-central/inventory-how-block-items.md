---
title: Hvernig á að útiloka vörur eða vöruafbrigði frá sölu eða innkaupum
description: 'Hægt er að útiloka að vörur og vöruafbrigði séu færð inn í línur í sölu-eða innkaupaskjölum, sem og bókuð í færslu.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, variant, product'
ms.date: 08/22/2023
ms.service: dynamics-365-business-central
---
# <a name="block-items-or-item-variants-from-sales-or-purchasing"></a>Útiloka vörur eða vöruafbrigði frá sölu eða innkaupum

Hægt er að útiloka að vörur og vöruafbrigði séu færð inn í línur í sölu-eða innkaupaskjölum og hægt er að útiloka að þau séu bókuð í færslum. Til dæmis er þetta gagnlegt þegar vara er með þekktan galla. Ef lokuð vara eða afbrigði er læst í sölu-eða innkaupaskjali verða skilaboð um að varan sé læst.

Eftirfarandi tafla lýsir því hvað gerist þegar vörur eða afbrigði eru læst.  

|Valkostur|Heimildasamstæða|  
|--------------------|------------|  
|**Lokað fyrir sölu**|Ekki er hægt að velja vöruna eða afbrigðið á söluskjali eða sölubirgðabókarbók.|  
|**Lokað fyrir innkaup**|Ekki er hægt að velja vöruna eða afbrigðið á innkaupaskjali, færslubók innkaupavöru eða í innkaupaáætlunarferlum.|  
|**Lokað**|Ekki er hægt að taka vöruna eða afbrigðið þegar færslur eru bókaðar.|  

> [!NOTE]
> Hægt er að skila útilokuðum vörum. Þetta þýðir að engar ofangreindra stillinga gilda fyrir skilapantanir og kreditreikninga.

Þegar notað er  **afritið frá aðgerð skjals**  til að stofna ný skjöl byggð á fyrirliggjandi skjölum er tilkynnt um það ef vörur eða afbrigði á upprunaskjalslínunum eru læst. Útilokaðar fylgiskjalslínur eru ekki í nýja skjalinu og tilkynning sýnir yfirlit yfir allar fylgiskjalalínur sem eru útilokaðar í upprunaskjalinu.

## <a name="to-block-an-item"></a>Til að loka fyrir vöru

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
2. Eftir því hvað á að gera er varan valin og síðan er valinn einn eða fleiri af eftirtöldum gátreitum:
    * **Lokað**
    * **Lokað fyrir sölu**
    * **Lokað fyrir innkaup**  

## <a name="to-block-an-item-variant"></a>Til að loka vöruafbrigði

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
2. Veldu vöruna sem hefur afbrigði sem þú vilt útiloka, Veldu  **afbrigði** og veldu svo einn eða fleiri eftirfarandi gátreita:  
    * **Lokað**
    * **Lokað fyrir sölu**
    * **Lokað fyrir innkaup**

## <a name="see-also"></a>Sjá einnig

[Skrá nýjar vörur](inventory-how-register-new-items.md)  
[Birgðir](inventory-manage-inventory.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
