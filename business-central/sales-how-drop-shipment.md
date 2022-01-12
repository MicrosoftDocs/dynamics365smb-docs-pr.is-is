---
title: Tengja sölupöntun við innkaupapöntun fyrir beina afhendingu (inniheldur myndefni) | Microsoft docs
description: Lýsir hvernig á að Búa til sölupöntun sem er tengd við innkaupapöntun til að virkja sendingu beint frá lánardrottni til viðskiptamanns.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1e4ce5185ba1a672784f2a1c893de82c3da69ee5
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2021
ms.locfileid: "7939956"
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
5. Á síðunni **Sölulisti** er valin sölupöntun sem var útbúin í [Að stofna sölupöntun fyrir beina sendingu](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).
6. Velja hnappinn **Í lagi**.

Línuupplýsingar úr sölupöntun er sett í sölupöntunarlínu(r).

Nú er hægt að segja lánardrottninum aðsenda vörur til viðskiptamanns, til dæmis, með því að póstleggja innkaupapöntun sem er PDF.     

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