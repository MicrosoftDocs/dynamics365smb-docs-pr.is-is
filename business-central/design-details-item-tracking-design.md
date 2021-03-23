---
title: Hönnunarupplýsingar - Vörurakning Hönnun | Microsoft Docs
description: Þetta efnisatriði lýsir hönnuninni á bak við vörurakningu í Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, tracing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a0c60381634543f367e85a465c4ee74c3396d5ad
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390997"
---
# <a name="design-details-item-tracking-design"></a>Hönnunarupplýsingarn: vörurakning hönnun
Í fyrstu útgáfu af vörurakningu í [!INCLUDE[prod_short](includes/prod_short.md)] 2.60 eru raðnúmer eða lotunúmer voru skráð beint á birgðabókarfærslur. Þessi hönnun veitir heildarupplýsingar um það hvað er til ráðstöfunar og einfalda rakningu fyrri færslna en vantar sveigjanleika og virkni.  

Frá [!INCLUDE[prod_short](includes/prod_short.md)] 3,00 var vörurakningareiginleikinn í aðskilinni hlutaskipan með flóknum tenglum í bókuð skjöl og birgðabókarfærslur. Þessi hönnun bauð upp á sveigjanleika og virkni en rakning færslna fyrir vörur var ekki að fullu til staðar fyrir útreikning til ráðstöfunar.  

Frá [!INCLUDE[prod_short](includes/prod_short.md)] 3.60 er vörurakningareiginleikinn innbyggður í frátekningarkerfið, sem annast frátekningar, pöntunarrakningu og aðgerðarboð. Nánari upplýsingar eru í „Upplýsingar um hönnun: Frátekning, Vörurakning og aðgerðaboð“ í „Upplýsingar um hönnun, framboðsáætlun“.  

Í nýjustu útgáfunni eru vörurakningarfærslur í útreikninga framboðs alls í gegnum kerfið, þ.m.t. áætlun, framleiðsla og vöruhús. Gamla hugmyndin um að taka rað- og lotunúmer með yfir í birgðahöfuðbókarfærslur er kynnt aftur til sögunnar til að tryggja auðvelt aðgengi að sögulegum gögnum til að nota við vörurakningu. Í tengslum við vörurakningarúrbætur í [!INCLUDE[prod_short](includes/prod_short.md)] 3,60, var frátekningarkerfi stækkað yfir í atriði önnur en pantanir, svo sem færslubækur, reikninga og kreditreikninga.  

Með því að bæta við rað- eða lotunúmerum vinnur frátekningarkerfið úr varanlegum eigindum vöru en vinnur einnig úr slitróttum tenglum á milli eftirspurnar og framboðs í formi pantanarakningafærslna og frátekningarfærslna. Aðrir öðruvísi eiginleikar rað- og lotunúmera samanborið við hefðbundin frátekningargögn er sú staðreynd að hægt að bóka þau, bæði að hluta og að fullu. Því mun taflan **Frátekningarfærsla** (T337) nú vinna með tengdri töflu, töflunni **Rakningarlýsing** (T336), sem stjórnar og birtir samantekt yfir virkt og bókað vörurakningarmagn. Frekari upplýsingar, sjá: [Hönnunarupplýsingar: Virk móti sögulegum vörurakningarfærslum](design-details-active-versus-historic-item-tracking-entries.md).  

Eftirfarandi skýringarmynd lýsir hönnun vörurakningar í [!INCLUDE[prod_short](includes/prod_short.md)]  

![Dæmi um vörurakningarflæði](media/design_details_item_tracking_design.png "Dæmi um vörurakningarflæði")  

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