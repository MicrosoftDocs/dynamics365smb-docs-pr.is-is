---
title: Stuttur leiðarvísir um sölu
description: Kynntu þér hvernig á að fylla út fyrstu mikilvægu reitina um vörur og viðskiptamenn í Business Central svo þú getir hafið söluferli.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: quickstart
ms.date: 09/29/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Stuttur leiðarvísir um sölu

Til að geta selt vörur og þjónustu þarf fyrst að setja upp vörur og viðskiptamenn. Þegar því er lokið er hægt að byrja að skrá sölupantanir og senda út reikninga.

## Setja upp vörur til að selja

Þetta myndband sýnir hvernig á að setja upp vöru til að selja í [!INCLUDE[prod_short](includes/prod_short.md)].

<br>

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE47eLx?rel=0]

### Setja upp nýtt atriði

[!INCLUDE[create_new_item](includes/create_new_item.md)]

Frekari upplýsingar og annað sem þú getur gert þegar þú vörur eru settar upp er að finna í [Skrá nýjar vörur](inventory-how-register-new-items.md).  

## Viðskiptamenn settir upp

Þetta myndband sýnir hvernig á að setja upp nýjan viðskiptamann í [!INCLUDE[prod_short](includes/prod_short.md)].  

<br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

### Setja upp nýjan viðskiptamann

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Frekari upplýsingar og annað sem þú getur gert þegar viðskiptamenn eru settir upp er að finna í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)

## Stofna sölupöntun  

Þegar maður selur viðskiptamanni eitthvað eru tveir kostir í boði. Sá fyrri er einfaldari, en hann er snýst bara um að stofna sölureikning. Ef söluferlið þitt er hinsvegar flóknara, t.d. ef þú ert með aðstæður þar sem þú sendir aðeins hluta af pöntunarmagni, notar þú sölupöntun.

### Sölupöntun stofnuð  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 10.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.
2. Veljið **Nýtt** til að stofna nýja færslu.
3. Í reitnum **Viðskiptamaður** er fært inn nafn núverandi viðskiptamanns.

    Aðrir reitir á síðunni **Sölupöntun** eru nú fylltir út með stöðluðum upplýsingum um viðskiptamanninn sem valinn hefur verið.  

4. Fylltu í eftirstandandi reiti á síðunni **sölupöntun** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. Á **Línur** Flýtiflipanum í **Tegund** reitnum, veldu hvaða tegund framleiðsluflokks, kostnaðarauka eða færslu þú munt bókað fyrir viðskiptamanninn með sölulínunni.

6. Í reitnum **númer** sleginn inn fjöldi birgðavöru eða þjónustu.

7. Í reitinn **Magn** er fært magn vara sem á að selja.

8. Í reitnum **Línuafsláttur %**, færið inn prósentutölu ef veita á viðskiptamanninum afslátt af vörunni.

9. Til að bæta við athugasemd um pöntunarlínu sem viðskiptavinurinn getur séð á prentuðu sölupöntuninni, skrifaðu athugasemd í **Lýsingarsvæði** sviði í auða línu.

10. Endurtakið skref 5 til 9 fyrir hverja birgðavöru sem selja á viðskiptamanninum.

11. Til að afhenda Aðeins hluta pöntunarmagns, skal færa magn í reitinn **magn til Afhendingar** reit. Gildið er afritað í reitinn **magn til Reikningsfærslu**.

12. Til að reikningsfæra Aðeins hluta sends magns, skal færa magn í reitinn **magn til að reikningsfæra** . Magnið verður að vera minna en gildið í reitnum **Magn til að senda**.

13. Þegar sölupöntunarlínunum er lokið, skal velja **bóka og senda** aðgerðina.

Frekari upplýsingar og annað sem þú getur gert þegar þú stofnar sölupantanir viðskiptamanns er að finna í [Selja vörur með sölupöntun viðskiptamanns](sales-how-sell-products.md).  

## Búa til sölureikning

Þegar þú stofnar og bókar sölureikning stofnarðu ekki bara reikningsskjalið sem þú sendir viðskiptamanninum, heldur stofnarðu einnig viðkomandi magn- og virðisfærslur í [!INCLUDE[prod_short](includes/prod_short.md)].

### Að stofna og bóka sölureikning  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 20.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölureikningar** og velja síðan viðkomandi tengil.  

2. Veljið **Nýtt** til að stofna nýja færslu.

3. Í reitnum **Viðskiptamaður** er fært inn nafn núverandi viðskiptamanns.

4. Fylltu í eftirstandandi reikningana á síðunni **sölureikningur** eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. Á **Línur** Flýtiflipanum í **Tegund** reitnum, veldu hvaða tegund framleiðsluflokks, kostnaðarauka eða færslu þú munt bókað fyrir viðskiptamanninn með sölulínunni.

6. Í reitnum **númer** Reitnum er valin færsla til að bóka samkvæmt gildinu í reitnum **Tegund** reit.

7. Í reitnum **Magn** er fært inn hversu margar einingar vöru, kostnaðarauka eða færslu sem línan skráir fyrir viðskiptamanninn.  

8. Í reitnum **Línuafsláttur %**, færið inn prósentutölu ef veita á afslátt af vörunni. Gildið í reitnum **Línuupphæð** er uppfært til samræmis.  

9. Endurtakið skref 5 til 8 fyrir hverja vöru eða gjald sem á reikningsfæra viðskiptavininn fyrir.  

10. Í reitnum **afsláttarupphæð reiknings** færið inn upphæð sem draga á frá gildinu sem sýnt er í reitnum **Heildarupphæð með skatti**.

11. Þegar sölureikningslínunum er lokið, skal velja **bóka og senda** aðgerðina.  

Frekari upplýsingar og annað sem þú getur gert þegar þú stofnar sölureikninga viðskiptamanns er að finna í [Reikningsfæra sölu](sales-how-invoice-sales.md)

## Sjá einnig

[Stuttir leiðarvísar Business Central](quick-start-business-central.md)  
[Söluyfirlit](sales-manage-sales.md)  
[Selja vörur með sölupöntun viðskiptavinar](sales-how-sell-products.md)  
[Reikningsfæra sölur](sales-how-invoice-sales.md)  
