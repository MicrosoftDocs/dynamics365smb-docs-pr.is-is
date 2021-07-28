---
title: Hönnunarupplýsingar - yfirlit vöruhúss
description: Til að styðja við raunmeðhöndlun vara á svæði og hólfastigi, verða allar upplýsingar að rekja fyrir hverja færslu eða flutning í vöruhús.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: 586fdc74b174ae24dea6354953899370f076a2da
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6439536"
---
# <a name="design-details-warehouse-overview"></a>Hönnunarupplýsingar yfirlit vöruhúss
Til að styðja við raunmeðhöndlun vara á svæði og hólfastigi, verða allar upplýsingar að rekja fyrir hverja færslu eða flutning í vöruhús. Þessu er stjórnað í töflunni **Vöruhúsafærsla**. Hver færsla er vistuð í birgðageymsluskrá.  

Warehouse skjöl og vörugeymsla dagbók eru notuð til að skrá atriði hreyfingar á lager. Í hvert sinn sem vara í vöruhúsinu er færð, móttekin, gengið frá, tekin til, send eða leiðrétt eru vöruhúsafærslur skráðar til að vista raunupplýsingar um svæði, hólf og magn.

Taflan **Innihald hólfs** er notuð til að meðhöndla allar mismunandi víddir innihalds í hólfi fyrir hverja vöru, svo sem mælieiningu, hámarksmagn og lágmarksmagn. Taflan **Innihald hólfs** inniheldur einnig flæðireiti vöruhúsafærslur, vöruhúsaleiðbeiningar og vöruhúsbókarlínur sem tryggja framboð á vöru eftir hólfi og að fljótt sé að reikna hólf fyrir vöru. Nánari upplýsingar eru í [Upplýsingar um hönnun: Til ráðstöfunar í vöruhúsi](design-details-availability-in-the-warehouse.md).  

Þegar vörubókun verður utan vöruhúsaeiningarinnar ern otuð sjálfgefin jöfnunarhólf á hverja staðsetningu til að samstilla vöruhúsafærslur við birgðafærslur. Við birgðir á lager í vöruhúsi, er munur milli reiknaðrar og talins magns skráð í leiðréttingarhólf og síðan færður sem leiðréttar færslur birgðahöfuðbókar. Nánari upplýsingar eru í [Upplýsingar um hönnun: Samþætting við birgðir](design-details-integration-with-inventory.md).  

Eftirfarandi mynd lýsir dæmigerðu vöruhúsaflæði.  

![Yfirlit fyrir vöruhúsaferli.](media/design_details_warehouse_management_overview.png "Yfirlit fyrir vöruhúsaferli")  

## <a name="basic-or-advanced-warehousing"></a>Grunn- eða ítarleg vörugeymsla  
Vöruhúsavirkni í [!INCLUDE[prod_short](includes/prod_short.md)] má framkvæma í mismunandi flækjustigum, allt eftir ferlum fyrirtækisins og pöntunarmagni. Aðalmunurinn er sá aðgerðir eru framkvæmdar pöntun fyrir pöntun í grunnvörugeymslu þegar þeim er steypt saman fyrir margfaldar pantanir í ítarlegu vöruhúsi.  

 Til að greina á milli mismunandi flækjustiga, þessi gögn átt við tvö almenna hluti, grunn og ítarlegt vöruhús. Þessi einfalda aðgreining nær yfir mörg mismunandi flækjustig samkvæmt skilgreiningu vörueinda og staðsetningaruppsetniingu, hvert og eitt stutta f mismunandi notandaviðmótsskjölum. Nánari upplýsingar eru í [Upplýsingar um hönnun: Uppsetning vöruhúss](design-details-warehouse-setup.md).  

> [!NOTE]  
>  Ítarlegasta stig vöruhúss er kallað uppsetningar vöruhúsakerfa í þessu skjali þar sem það stig krefst ítarlegast kornsins, vöruhúsakerfis.  

 Eftirfarandi mismunandi notandaviðmótsskjöl eru notuð í grunngerð og ítarlegu vöruhúsi.  

## <a name="basic-ui-documents"></a>Grunnviðmótsskjöl  

-   **Birgðafrágangur**  
-   **Birgðatínsla**  
-   **Birgðahreyfing**  
-   **Birgðabók**  
-   **Endurflokkunarbók vöru**  
-   (Ýmsar skýrslur)  

## <a name="advanced-ui-documents"></a>Ítarleg notendaviðmótsskjöl  

-   **Vöruhús -**  
-   **Vinnublað frágangs**  
-   **Frágangur vöruhúss**  
-   **Vinnublað tínslu**  
-   **Vöruhúsatínsla**  
-   **Hreyfingavinnublað**  
-   **Vöruhúsatínsla**  
-   **Vöruhús - innanhústínsla**  
-   **Vöruhús - innanhúsfrágangur**  
-   **Vinnublað hólfastofnunar**  
-   **Vinnublað f. stofnun hólfainnihalds**  
-   **Birgðabók vöruhúss**  
-   **Birgðaendurfl.bók vöruhúss**  
-   (Ýmsar skýrslur)  

Nánari upplýsingar um hvert skjal eru á síðum hvers kafla fyrir sig.  

### <a name="terminology"></a>Orðalisti  
Til að jafna við fjárhagshugtökin innkaup og sölu notast [!INCLUDE[prod_short](includes/prod_short.md)] vöruhúsaskjöl við eftirfarandi hugtök fyrir vöruflæði í vöruhúsinu.  

|Hugtak|Description|  
|----------|---------------------------------------|  
|Flæði á innleið|Vörur á ferð innan vöruhúss, svo sem innkaup og millifærslur á innleið.|  
|Tiltekt innanhúss|Vörur á ferð innan vöruhúss, svo sem framleiðsluíhlutir og frálag.|  
|Flæði á útleið|Vörur á leið út úr vöruhúsi, svo sem sala eða millifærslur á útleið.|  

## <a name="see-also"></a>Sjá einnig  
 [Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]