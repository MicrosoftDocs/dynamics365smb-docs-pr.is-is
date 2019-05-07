---
title: Nota forstillingar til að flokka tengiliði
description: Setja upp spurningalista forstillingar til að auðvelda flokkun á viðskiptatengiliðum
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 04/01/2019
ms.openlocfilehash: fe02153a89ad5f63855cff5eec5344d601c8663a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2019
ms.locfileid: "934443"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Nota spurningalista forstillingar til að flokka viðskiptatengiliði
Hægt er að setja upp spurningalista sem á að nota þegar upplýsingar um forstillingu tengiliða eru færðar inn. Innan hvers spurningalista er hægt að setja upp þær mismunandi spurningar sem spyrja á tengiliðina.  

Einnig er hægt að keyra spurningalistann til að svara sjálfkrafa nokkrum spurningum samkvæmt gögnum um tengiliði, viðskiptamenn eða lánardrottna.  

## <a name="to-add-a-profile-questionnaire"></a>Til að bæta við spurningalista forstillingar
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning spurningalista** og veldu síðan tengda tengilinn.  
2.  Á flipanum **Heim** í flokknum **Nýtt** skal velja **Nýtt**.  
3.  Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>Til að bæta spurningum við spurningalista forstillingar
1.  Veljið viðeigandi spurningalista forstillingar og síðan í flipanum **Heim**, í flokknum **Vinna úr**, skal velja **Breyta uppsetningu spurningalista**.  
2.  Í fyrstu auðu línunni reitnum **Tegund**, veljið **Spurning** ritið spurninguna í reitinn **Lýsing**. Aðrir reitir í línunni eru fylltir út.  
3.  Í næstu auðu línu er smellt á reitinn **Tegund**, valið **Svar** og svarið ritað í reitinn **Lýsing**.  
4.  Í reitnum **Forgangur** veljið forganginn. Í reitunum **Frá virði** og **Til virðis** skilgreinið bil. Tengiliðir sem fá stig innan skilgreinda bilsins fá svarið.  

Skrefin eru endurtekin til að færa inn allar spurningar og svör í spurningalistanum.

Þegar búið er að stofna spurningalista þarf að stofna tengiliðaflokkanir til að flokka tengiliðina. Einnig er hægt að setja fram spurningar sem eru metnar sjálfkrafa í samræmi við upplýsingar tengiliðarspjaldinu.  

> [!NOTE]
> Ef færð er inn spurning sem er svarað sjálfkrafa skal velja <STRONG>Lína</STRONG> og svo <STRONG>Upplýs. um spurningar</STRONG> til að færa inn skilyrðin sem notuð eru til að svara spurningunni sjálfkrafa.

## <a name="the-automatic-classification-of-contacts"></a>Sjálfvirk flokkun tengiliða
Hægt er að flokka tengiliði sjálfvirkt eftir viðskiptamanna-, lánardrottna-, og tengiliðaupplýsingum með því að setja upp sjálfvirkt svöruðum forstillingarspurningum á síðunni **Uppsetning spurningalisti forstillingar**.  

> [!NOTE]
> Aðeins er hægt að flokka tengiliði sem skráðir eru sem viðskiptamenn á grunni viðskiptamannaupplýsinga og aðeins er flokka tengilið sem skráðir eru sem lánardrottnar á grundvelli lánardrottnaupplýsinga. Sjálfvirk flokkun uppfærist ekki sjálfkrafa. Þar af leiðandi er ráðlegt að uppfæra spurningalista forstillingar þegar viðskiptamanna-, lánardrottna- eða tengiliðaupplýsingum sem þeir byggja á er breytt.  

Þegar sjálfvirkt svaraðar forstillingarspurningar hafa verið settar upp, ef þú úthlutar tengiliði forstillingarspurningar sem innihalda þessar spurningar, mun [!INCLUDE[d365fin](includes/d365fin_md.md)] sjálfkrafa úthluta réttu svörunum fyrir tengiliðinn.  

## <a name="example"></a>Dæmi
Hægt er að flokka tengiliði eftir því hversu mikið þeir hafa keypt:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Svar</strong></th>
<th><strong>Gildir um</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>A</p></td>
<td><p>tengiliði sem keyptu fyrir 500.000 SGM eða meira</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p>tengiliði sem keyptu fyrir 100.000 til 499.999 SGM</p></td>
</tr>
<tr class="odd">
<td><p>U</p></td>
<td><p>tengiliði sem keyptu fyrir 99.999 SGM eða minna</p></td>
</tr>
</tbody>
</table>

Það er gert með því að fylla út síðuna **Uppsetning á spurningalista forstillingar** sem hér segir:


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Tegund</strong></th>
<th><strong>Lýsing</strong></th>
<th><strong>Sjálfvirk flokkun</strong></th>
<th><strong>Frá virði</strong></th>
<th><strong>Til virðis</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Spurning</p></td>
<td><p>ABC-flokkun</p></td>
<td><p>Smellt er til að færa inn gátmerki</p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p>Svar</p></td>
<td><p>A</p></td>
<td><p> </p></td>
<td><p>500,000</p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p>Svar</p></td>
<td><p>Á</p></td>
<td><p> </p></td>
<td><p>100,000</p></td>
<td><p>499,999</p></td>
</tr>
<tr class="even">
<td><p>Svar</p></td>
<td><p>U</p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p>99,999</p></td>
</tr>
</tbody>
</table>

Svo er síðan **Upplýs. forstillingarspurningar** fylltur út sem hér segir:
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Reitur</strong></th>
<th><strong>Gildi</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Flokkunarreitur viðskiptavinar</strong></td>
<td><emphasis>Sala (SGM)</emphasis></td>
</tr>
<tr>
<td><strong>Flokkunaraðferð</strong></td>
<td><emphasis>Skilgreint virði</emphasis></td>
</tr>
</tbody>
</table>

Þegar spurningalista forstillingar sem inniheldur þessa spurningu er úthlutað á tengilið færir kerfið sjálfkrafa viðeigandi svar fyrir tengiliðinn í forstillingarlínurnar á tengiliðaspjaldinu.

## <a name="see-also"></a>Sjá einnig
[Stofna tengiliði](marketing-create-contact-companies.md)  
