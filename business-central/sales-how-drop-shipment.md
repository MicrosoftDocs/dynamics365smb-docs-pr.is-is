---
title: Gera beina afhendingu (inniheldur myndefni)
description: Lýsir hvernig á að Búa til sölupöntun sem er tengd við innkaupapöntun til að virkja sendingu beint frá lánardrottni til viðskiptamanns.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3fe45eb6403798a7e64b9604321440a2fff38c3f
ms.sourcegitcommit: 865b390b5571b08084bde93b539ec9898e201933
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/02/2022
ms.locfileid: "8372044"
---
# <a name="make-drop-shipments"></a>Beinar sendingar

Bein afhending er afhending frá einum af lánardrottnum fyrirtækisins beint til einhvers af viðskiptamönnum fyrirtækisins.

Þegar sölupöntun er merkt fyrir beina sendingu og stofnuð er innkaupapöntun sem tilgreinir viðskiptamanninn í reitnum **Sendist til**, **Aðsetur viðskiptamanns**, er hægt að tengja skjölin tvö til að segja lánardrottni að senda beint til viðskiptamannsins.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Sölupöntun fyrir beina afhendingu búin til

Til að undirbúa beina sendingu, er stofnuð sölupöntun fyrir vöru og tilgreina í sölulínunni að salan krefst beinnar sendingar.

1. Stofnið sölupöntun fyrir vöru. Frekari upplýsingar eru í [Selja vörur](sales-how-sell-products.md).
2. Á velta pöntunarlínunni fyrir dropatilboðið skaltu velja hnappinn **Senda sendingu**. Notaðu **Dálkaval** ef svæðið er ekki sýnilegt. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Innkaupapöntunin stofnuð fyrir beina sendingu

Til að undirbúa beina sendingu, skal tilgreina í innkaupapöntuninni að senda þarf hana til viðskiptamannsins, ekki til þín.

1. Stofna innkaupapöntun. Ekki fylla inn í neina reiti á línunum. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).
2. Í reitnum **Sendist til** skal velja **Heimilisfang viðskiptavinar**.
3. Í reitnum **Viðskiptavinur** skal velja viðskiptavininn sem þú ert að selja til.
4. Veljið aðgerðina **beinar sendingar** og veljið síðan aðgerðina **sækja sölupöntun**.
5. **Á sölulistasíðunni** er sölupöntunin valin sem var útbúin í [til að stofna sölupöntun fyrir beina afhendingu](#to-create-a-sales-order-for-drop-shipment).
6. Velja hnappinn **Í lagi**.

Línuupplýsingar úr sölupöntun er sett í sölupöntunarlínu(r).

Nú er hægt að segja lánardrottninum aðsenda vörur til viðskiptamanns, til dæmis, með því að póstleggja innkaupapöntun sem er PDF. Ef seljandi lætur í té rakningarnúmer eða svipaðar upplýsingar er hægt að velja um að skrá þær upplýsingar í innkaupapöntunarlínu af gerðinni *Athugasemd*.  

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a>Að stofna margar innkaupapantanir fyrir beinar sendingar

Einnig er hægt að nota innkaupatillögublað til að stofna innkaupapöntunina fyrir lánardrottin. Kosturinn við að nota innkaupatillögublaðið er sá að hægt er að stofna innkaupapantanir fyrir allar útistandandi beinar sendingar þannig að ekki þarf að stofna hverja þeirra fyrir sig.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublöð innkaupatillögu** og velja síðan viðkomandi tengil.
2. Veljið aðgerðina **beinar sendingar** og veljið síðan aðgerðina **sækja sölupöntun**.
3. Velja hnappinn **Í lagi**.
4. Yfirfara innkaupapöntunarlínur, og í reitnum **Lánardrottnanr.** skal velja lánardrottin sem veitir nauðsynlegar vörur. 
5. Veljið aðgerðina **Framkvæma aðgerðaboð** til að færa yfirfarnar línur í innkaupapöntun.

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Til að skoða tengda innkaupapöntunina úr sölupöntuninni

* Veldu Sölupöntunarlínu beinnar sendingar, veldu **Pöntun** aðgerð og veldu **Bein sending** aðgerð og síðan er valið aðgerðin **Innkaupapöntun**.

## <a name="to-post-a-drop-shipment"></a>Til að bóka beina afhendingu

Þegar lánardrottinn hefur sent vörur, er hægt að bóka sölupöntunina sem senda. Einnig er hægt að bóka innkaupapöntun, en aðeins með **Móttöku** valkostinn fyrr en sölupöntunin hefur verið reikningsfært.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Sölupantanir** og velja síðan viðkomandi tengil.
2. Opnaðu sölupöntun sem þú stofnaðir í [Að stofna sölupöntun fyrir beina sendingu](#to-create-a-sales-order-for-drop-shipment).
3. Í reitnum **magn til Afhendingar** er tilgreint hve mikið af pöntunarmagni skal senda, allt eða hluti pöntunarmagns.
4. Veljið aðgerðina **bóka** eða **Bóka og senda**.
5. Síðan er annað hvort valið **senda** valkosturinn til að reikningsfæra síðar eða valkostinn **senda og reikningsfæra** eigi að reikningsfæra strax.

## <a name="see-also"></a>Sjá einnig

[Sérstakar pantanir stofnaðar](sales-how-to-create-special-orders.md)  
[Kaupa vörur fyrir sölu](purchasing-how-purchase-products-sale.md)  
[Selja vörur](sales-how-sell-products.md)  
[Skrá innkaup](purchasing-how-record-purchases.md)  
[Sala](sales-manage-sales.md)  
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]