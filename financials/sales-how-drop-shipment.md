---
title: "Stofna sölupöntun sem er tengd við innkaupapöntun fyrir beina afhendingu | Microsoft Docs"
description: "Lýsir hvernig á að Búa til sölupöntun sem er tengd við innkaupapöntun til að virkja sendingu beint frá lánardrottni til viðskiptamanns."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 977debf7386ad1113ef54147b20fd24c7c285a78
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-make-drop-shipments"></a>Hvernig á að: Gera beinar afhendingar
Bein afhending er afhending frá einum af lánardrottnum fyrirtækisins beint til einhvers af viðskiptamönnum fyrirtækisins.

Þegar sölupöntun er merkt fyrir bein sending og þú býrð til innkaupapöntun sem tilgreinir viðskiptamaður í reitnum **Selt-til-Viðskm.nr.** Sviði, getur þú tengt tvö skjöl og þar með leiðbeint seljanda um að senda beint til viðskiptavinarins.

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Sölupöntun fyrir beina afhendingu búin til
Til að Undirbúa bein afhending, er stofnuð sölupöntun fyrir vöru sem venjulega, nema þarf tilgreina í sölulínunni að salan krefst beinnar sendingar.

1. Stofnið sölupöntun fyrir vöru. Nánari upplýsingar eru í [Hvernig á að: selja vörur.](sales-how-sell-products.md)
2. Á velta pöntunarlínunni fyrir dropatilboðið skaltu velja hnappinn **Senda sendingu**. Notaðu **Dálkaval** ef svæðið er ekki sýnilegt. Nánari upplýsingar er að finna í [Sérstillingar notanda](ui-user-personalization.md).

> [!NOTE]  
>   Þessi virkni krefst þess að upplifun þín sé stillt á **Pakki**. Nánari upplýsingar, sjá [Sérstilla þína [!INCLUDE[d365fin](includes/d365fin_md.md)] upplifun](ui-experiences.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>Innkaupapöntunin stofnuð fyrir beina sendingu
Til að undirbúa beina sendingu fyrir vöru sem á að selja, stofnarðu innkaupapöntun sem venjulega, nema taka þarf fram í innkaupapöntun að senda verði til viðskiptamannsins, ekki til þíns sjálfs.

1. Stofna innkaupapöntun. Ekki fylla inn í neina reiti á línunum. Nánari upplýsingar eru í [Hvernig á að: Skrá innkaup](purchasing-how-record-purchases.md).
2. Í reitnum **Selt til Viðskm.nr.**. er valinn viðskiptamaður sem selt er til.
3. Veljið aðgerðina **beinar sendingar** og veljið síðan aðgerðina **sækja sölupöntun**.
4. Í **Sölulisti** glugganum er valin sölupöntun sem var útbúin í "stofna sölupöntun fyrir beina sendingu" hlutanum.
5. Velja hnappinn **Í lagi**.

Línuupplýsingar úr sölupöntun er sett í sölupöntunarlínu(r).

Nú er hægt að segja lánardrottninum aðsenda vörur til viðskiptamanns, til dæmis, með því að póstleggja innkaupapöntun sem er PDF.     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>Til að skoða tengda innkaupapöntunina úr sölupöntuninni
* Veldu Sölupöntunarlínu beinnar sendingar, veldu **Pöntun** aðgerð og veldu **Bein sending** aðgerð og síðan er valið aðgerðin **Innkaupapöntun**.

## <a name="to-post-a-drop-shipment"></a>Til að bóka beina afhendingu
Þegar lánardrottinn hefur sent vörur, er hægt að bóka sölupöntunina sem senda. Einnig er hægt að bóka innkaupapöntun, en aðeins með **Móttöku** valkostinn fyrr en sölupöntunin hefur verið reikningsfært.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Sölupantanir** og velja svo viðeigandi tengil.
2. Opnaðu sölupöntun sem þú stofnaðir í "stofna sölupöntun fyrir beina sendingu" hlutanum.
3. Í reitnum **magn til Afhendingar** er tilgreint hve mikið af pöntunarmagni skal senda, allt eða hluti pöntunarmagns.
4. Veljið aðgerðina **bóka** eða **Bóka og senda**.
5. Síðan er annað hvort valið **senda** valkosturinn til að reikningsfæra síðar eða valkostinn **senda og reikningsfæra** eigi að reikningsfæra strax.

## <a name="see-also"></a>Sjá einnig
[Hvernig á að: Selja vörur](sales-how-sell-products.md)  
[Hvernig á að skrá kaup](purchasing-how-record-purchases.md)  
[Sala](sales-manage-sales.md)  
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

