---
title: Hönnunarupplýsingar - vörurakningarhönnun
description: Þetta efnisatriði lýsir hönnuninni á bak við vörurakningu í Business Central eftir því sem hún þróast í gegnum vöruútgáfur.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, tracing
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 626d22b4a45035698862c727547b332c898508af
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141334"
---
# <a name="design-details-item-tracking-design"></a>Hönnunarupplýsingarn: vörurakning hönnun

Vörurakning í [!INCLUDE[prod_short](includes/prod_short.md)] hófst á [!INCLUDE [navnow_md](includes/navnow_md.md)]. Vörurakningarvirknin er í aðskildri hlutaskipan með flóknum tenglum á bókuð skjöl og birgðafærslur og hún er samþætt við frátekningarkerfið sem sér um frátekningu, pöntunarrakningu og aðgerðarboð. Frekari upplýsingar er að finna í [Hönnunarupplýsingar: Pöntun, pöntunarrakning og aðgerðarboð](design-details-reservation-order-tracking-and-action-messaging.md) í hönnunarlýsingu framboðsáætlunar.  

Í þessari útgáfu eru vörurakningarfærslur í útreikninga framboðs alls í gegnum kerfið, þ.m.t. áætlun, framleiðsla og vöruhús. Rað- og lotunúmer eru notuð í birgðafærslum til að tryggja einfaldan aðgang að sögulegum gögnum fyrir vörurakninguna. Með útgáfutímabili 1 fyrir árið 2021 mun vörurakning í [!INCLUDE [prod_short](includes/prod_short.md)] innihalda pakkanúmer.  

Með því að bæta við rað-, lotu- og pakkanúmerum vinnur frátekningarkerfið úr varanlegum eigindum vöru en vinnur einnig úr slitróttum tenglum á milli eftirspurnar og framboðs í formi pantanarakningafærslna og frátekningarfærslna. Aðrir öðruvísi eiginleikar rað- og lotunúmera samanborið við hefðbundin frátekningargögn er sú staðreynd að hægt að bóka þau, bæði að hluta og að fullu. Því mun taflan **Frátekningarfærsla** (T337) nú vinna með tengdri töflu, töflunni **Rakningarlýsing** (T336), sem stjórnar og birtir samantekt yfir virkt og bókað vörurakningarmagn. Frekari upplýsingar, sjá: [Hönnunarupplýsingar: Virk móti sögulegum vörurakningarfærslum](design-details-active-versus-historic-item-tracking-entries.md).  

Eftirfarandi skýringarmynd lýsir hönnun vörurakningar í [!INCLUDE[prod_short](includes/prod_short.md)]  

![Dæmi um vörurakningarflæði.](media/design_details_item_tracking_design.png "Dæmi um vörurakningarflæði")  

Meginbókunarhluturinn er endurhannaður til að takast á við einstaka undirflokkun skjalslínu í formi raðnúmers eða lotunúmers og sérstökum tengslatöflum er bætt við til að búa til einn-í-marga tengsl milli bókaðra skjala og skiptra fjárhagsfærsla þeirra og gildisfærsla.  

Kóðaeining 22, **Birgðabók - Bókunarlína**, skiptir nú bókuninni samkvæmt vörurakningarnúmerunum sem eru tilgreind á skráarlínunni. Hvert einstakt vörurakningarnúmer á línunni býr til eigin birgðahöfuðbókarfærslu fyrir vöruna. Þetta þýðir að á tengilinn frá bókaðri skjalalínu í tengda birgðahöfuðbókarfærslur er nú í einn-til -marga tengslum. Þetta samband er stjórnað af eftirfarandi vörurakningar tengslatöflum.  

|Svæði|Lýsing|  
|---------------|---------------------------------------|  
|**Birgðafærslutengsl** (T6507)|TTengir flutt eða fengið línur við birgðabókarfærslur|  
|**Virðisfærslutengsl** (T6508)|Tengir reikningsfærðar línur við virðisfærslur|  

Nánari upplýsingar eru í [Upplýsingar um hönnun: Vörurakning bókunarskipulag](design-details-item-tracking-posting-structure.md)  

## <a name="see-also"></a>Sjá einnig

[Hönnunarupplýsingar: Vörurakning](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
