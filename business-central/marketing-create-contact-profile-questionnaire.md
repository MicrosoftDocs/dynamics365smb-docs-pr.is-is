---
title: Nota forstillingar til að flokka tengiliði
description: Lestu um hvernig á að setja upp spurningalista forstillingar til að auðvelda flokkun á notandasíðum viðskiptatengiliða.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 06/22/2021
ms.openlocfilehash: 6ce13672651a5b6b65712928b764ad11b3db514d
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588527"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a>Nota spurningalista forstillingar til að flokka viðskiptatengiliði
Hægt er að setja upp spurningalista sem á að nota þegar upplýsingar um forstillingu tengiliða eru færðar inn. Innan hvers spurningalista er hægt að setja upp þær mismunandi spurningar sem spyrja á tengiliðina.  

Einnig er hægt að keyra spurningalistann til að svara sjálfkrafa nokkrum spurningum samkvæmt gögnum um tengiliði, viðskiptamenn eða lánardrottna.  

## <a name="to-add-a-profile-questionnaire"></a>Til að bæta við spurningalista forstillingar
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning spurningalista** og velja síðan viðkomandi tengil.  
2.  Veldu aðgerðina **Nýtt**.  
3.  Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a>Til að bæta spurningum við spurningalista forstillingar
1.  Veldu viðeigandi spurningalista og veldu síðan aðgerðina **Breyta Breyta uppsetningu spurningalista**.  
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

Þegar sjálfvirkt svaraðar forstillingarspurningar hafa verið settar upp, ef þú úthlutar tengiliði forstillingarspurningar sem innihalda þessar spurningar, mun [!INCLUDE[prod_short](includes/prod_short.md)] sjálfkrafa úthluta réttu svörunum fyrir tengiliðinn.  

## <a name="example"></a>Dæmi

Hægt er að flokka tengiliði eftir því hversu mikið þeir hafa keypt:

|Svar|Gildir um|
|--- |--- |
|A|tengiliði sem keyptu fyrir 500.000 SGM eða meira|
|B|tengiliði sem keyptu fyrir 100.000 til 499.999 SGM|
|U|tengiliði sem keyptu fyrir 99.999 SGM eða minna|

Það er gert með því að fylla út síðuna **Uppsetning á spurningalista forstillingar** sem hér segir:

| Tegund     | Description        | Sjálfvirk flokkun     | Frá virði | Til virðis |
|----------|--------------------|------------------------------|------------|----------|
| Spurning | ABC-flokkun | Smellt er til að færa inn gátmerki |            |          |
| Svar   | A                  |                              | 500,000    |          |
| Svar   | Á                  |                              | 100,000    | 499,999  |
| Svar   | U                  |                              |            | 99,999   |

Svo er síðan **Upplýs. forstillingarspurningar** fylltur út sem hér segir:

| Svæði                         | Gildi:         |
|-------------------------------|---------------|
| Flokkunarreitur viðskiptavinar | Sala (SGM)   |
| Flokkunaraðferð         | Skilgreint virði |

Þegar spurningalista forstillingar sem inniheldur þessa spurningu er úthlutað á tengilið færir forritið sjálfkrafa viðeigandi svar fyrir tengiliðinn í forstillingarlínurnar á tengiliðaspjaldinu.

## <a name="see-also"></a>Sjá einnig

[Stofna tengiliði](marketing-create-contact-companies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]