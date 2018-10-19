---
title: "Hönnunarupplýsingar - Vörurakning Hönnun | Microsoft Docs"
description: "Þetta efnisatriði lýsir hönnuninni á bak við vörurakningu í Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, tracing
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 99534c3cf5c683c1e1d1fe3e6b5940a757fbebca
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-item-tracking-design"></a>Hönnunarupplýsingarn: vörurakning hönnun
Í fyrstu útgáfu af vörurakningu í [!INCLUDE[d365fin](includes/d365fin_md.md)] 2.60 eru raðnúmer eða lotunúmer voru skráð beint á birgðabókarfærslur. Þessi hönnun veitir heildarupplýsingar um það hvað er til ráðstöfunar og einfalda rakningu fyrri færslna en vantar sveigjanleika og virkni.  

Frá [!INCLUDE[d365fin](includes/d365fin_md.md)] 3,00 var vörurakningareiginleikinn í aðskilinni hlutaskipan með flóknum tenglum í bókuð skjöl og birgðabókarfærslur. Þessi hönnun bauð upp á sveigjanleika og virkni en rakning færslna fyrir vörur var ekki að fullu til staðar fyrir útreikning til ráðstöfunar.  

Frá [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60 er vörurakningareiginleikinn innbyggður í frátekningarkerfið, sem annast frátekningar, pöntunarrakningu og aðgerðarboð. Nánari upplýsingar eru í „Upplýsingar um hönnun: Frátekning, Vörurakning og aðgerðaboð“ í „Upplýsingar um hönnun, framboðsáætlun“.  

Í nýjustu útgáfunni eru vörurakningarfærslur í útreikninga framboðs alls í gegnum kerfið, þ.m.t. áætlun, framleiðsla og vöruhús. Gamla hugmyndin um að taka rað- og lotunúmer með yfir í birgðahöfuðbókarfærslur er kynnt aftur til sögunnar til að tryggja auðvelt aðgengi að sögulegum gögnum til að nota við vörurakningu. Í tengslum við vörurakningarúrbætur í [!INCLUDE[d365fin](includes/d365fin_md.md)] 3,60, var frátekningarkerfi stækkað yfir í atriði önnur en pantanir, svo sem færslubækur, reikninga og kreditreikninga.  

Með því að bæta við rað- eða lotunúmerum vinnur frátekningarkerfið úr varanlegum eigindum vöru en vinnur einnig úr slitróttum tenglum á milli eftirspurnar og framboðs í formi pantanarakningafærslna og frátekningarfærslna. Aðrir öðruvísi eiginleikar rað- og lotunúmera samanborið við hefðbundin frátekningargögn er sú staðreynd að hægt að bóka þau, bæði að hluta og að fullu. Því mun taflan **Frátekningarfærsla** (T337) nú vinna með tengdri töflu, töflunni **Rakningarlýsing** (T336), sem stjórnar og birtir samantekt yfir virkt og bókað vörurakningarmagn. Frekari upplýsingar, sjá: [Hönnunarupplýsingar: Virk móti sögulegum vörurakningarfærslum](design-details-active-versus-historic-item-tracking-entries.md).  

Eftirfarandi skýringarmynd lýsir hönnun vörurakningar í [!INCLUDE[d365fin](includes/d365fin_md.md)]  

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

