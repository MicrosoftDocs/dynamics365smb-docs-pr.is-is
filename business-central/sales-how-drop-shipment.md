---
title: Gera beinar afhendingar
description: Lýsir hvernig á að Búa til sölupöntun sem er tengd við innkaupapöntun til að virkja sendingu beint frá lánardrottni til viðskiptamanns.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: direct shipment
ms.date: 05/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="make-drop-shipments"></a>Gera beinar afhendingar

Bein afhending er afhending frá einum af lánardrottnum fyrirtækisins beint til einhvers af viðskiptamönnum fyrirtækisins.

Þegar sölupöntun er merkt fyrir beina sendingu og stofnuð er innkaupapöntun sem tilgreinir viðskiptamanninn í reitnum **Sendist til**, **Aðsetur viðskiptamanns**, er hægt að tengja skjölin tvö til að segja lánardrottni að senda beint til viðskiptamannsins.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Sölupöntun fyrir beina afhendingu búin til

Til að undirbúa beina sendingu, er stofnuð sölupöntun fyrir vöru og tilgreina í sölulínunni að salan krefst beinnar sendingar.

1. Stofnið sölupöntun fyrir vöru. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).
2. Í sölupöntunarlínunni fyrir beina afhendingu er gátreiturinn Bein **afhending** valin. Einnig er hægt að velja innkaupakóta sem hefur reitinn Bein afhending **valið í** reitnum **Innkaupakóti** .

> [!TIP]
> Sjálfgefið er að reitirnir Bein afhending og Innkaupakóti séu ekki tiltækir í línunum. Ef svo er ekki er hægt að bæta þeim við með því að sérsníða hluta síðunnar sem inniheldur línurnar. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Innkaupapöntunin stofnuð fyrir beina sendingu

Til að undirbúa beina sendingu, skal tilgreina í innkaupapöntuninni að senda þarf hana til viðskiptamannsins, ekki til þín.

1. Stofna innkaupapöntun. Ekki fylla inn í neina reiti á línunum. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).
2. Í reitnum **Sendist til** skal velja **Heimilisfang viðskiptavinar**.
3. Í reitnum **Viðskiptamaður** skal velja viðskiptamanninn sem þú ert að selja til.
4. Veljið aðgerðina **beinar sendingar** og veljið síðan aðgerðina **sækja sölupöntun**.
5. Á síðunni **Sölulisti** er valin sölupöntun sem var útbúin í [Að stofna sölupöntun fyrir beina sendingu](#to-create-a-sales-order-for-drop-shipment).
6. Velja hnappinn **Í lagi**.

Línuupplýsingar úr sölupöntun er sett í sölupöntunarlínu(r).

Nú getur þú sagt lánardrottinum þínum að senda vörurnar beint til viðskiptamanns. Til dæmis væri hægt að senda viðkomandi pöntunina með tölvupósti.

Ef birgir veitir viðbótarupplýsingar, t.d. rakningarnúmer, er hægt að bæta þeim upplýsingum við sem athugasemd í innkaupapöntunarlínu. Til að bæta athugasemd við línu er valið Athugasemd í reitnum **Tegund** og upplýsingar færðar inn í reitinn **Lýsing**. **·**   

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a>Að stofna margar innkaupapantanir fyrir beinar sendingar

Einnig er hægt að nota innkaupatillögublaðið til að stofna innkaupapantanir. Kosturinn við að nota innkaupatillögublaðið er sá að hægt er að stofna innkaupapantanir fyrir allar útistandandi beinar sendingar. Það þýðir að ekki þarf að stofna hverja pöntun fyrir sig.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublöð beiðni** og velja síðan viðkomandi tengil.
2. Veljið aðgerðina **beinar sendingar** og veljið síðan aðgerðina **sækja sölupöntun**.
3. Ef þörf krefur skal færa inn afmörkunarskilyrði fyrir pantanirnar sem á að ná í og velja svo hnappinn **Í lagi** .
4. Farið er yfir innkaupapantanalínurnar og í reitnum Nr. lánardrottins **.** er valinn lánardrottinn sem sér um vörurnar.
5. Veljið aðgerðina **Framkvæma aðgerðarboð** til að breyta línunum í innkaupapöntun.

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Til að skoða tengda innkaupapöntunina úr sölupöntuninni

Veldu Sölupöntunarlínu beinnar sendingar, veldu **Pöntun** aðgerð og veldu **Bein sending** aðgerð og síðan er valið aðgerðin **Innkaupapöntun**.

## <a name="to-post-a-drop-shipment"></a>Til að bóka beina afhendingu

Þegar lánardrottinn hefur sent vörur, er hægt að bóka sölupöntunina sem senda. Einnig er hægt að bóka innkaupapöntun, en aðeins með **Móttöku** valkostinn fyrr en sölupöntunin hefur verið reikningsfært.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.
2. Opnaðu sölupöntun sem þú stofnaðir í [Að stofna sölupöntun fyrir beina sendingu](#to-create-a-sales-order-for-drop-shipment).
3. Í reitnum **magn til Afhendingar** er tilgreint hve mikið af pöntunarmagni skal senda, allt eða hluti pöntunarmagns.
4. Veljið aðgerðina **bóka** eða **Bóka og senda**.
5. Síðan er annað hvort valið **senda** valkosturinn til að reikningsfæra síðar eða valkostinn **senda og reikningsfæra** eigi að reikningsfæra strax.

> [!TIP]
> Ekki gleyma að bóka þarf reikning innkaupapöntunarinnar.

## <a name="see-also"></a>Sjá einnig .

[Sérstakar pantanir stofnaðar](sales-how-to-create-special-orders.md)  
[Kaupa vörur fyrir sölu](purchasing-how-purchase-products-sale.md)  
[Selja vörur](sales-how-sell-products.md)  
[Skrá innkaup](purchasing-how-record-purchases.md)  
[Sala](sales-manage-sales.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
