---
title: Notkun Invoicing og Business Central | Microsoft Docs
description: Hjáleið fyrir aðgang að Microsoft Invoicing þegar þú hefur skráð þig fyrir Dynamics 365 Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Office 365
ms.date: 04/30/2020
ms.author: bholtorf
ms.openlocfilehash: 7776cd01218f5959734173226574bb4a0d043153
ms.sourcegitcommit: 866f0e6ed9df3397072b9df838e31c3a1f4b626d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/05/2020
ms.locfileid: "3333861"
---
# <a name="using-the-same-office-365-account-in-d365fin-and-microsoft-invoicing"></a>Nota sama Office 365-reikninginn í [!INCLUDE[d365fin](includes/d365fin_long_md.md)] og Microsoft Invoicing
Þegar þú skráir þig í prufuáskrift fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] geturðu farið í 30 daga matsáfanga, þú getur byrjað áskrift eða hættir að nota [!INCLUDE[d365fin](includes/d365fin_md.md)]. Í öllum tilvikum getur þú á einhverjum tímapunkti hafa séð eitthvað sem kallast **Microsoft Invoicing** og smellt á það. Þetta forrit var hluti af því sem er núna Microsoft 365 Business og var áður þekkt sem Office 365 Business Premium-áskrift, þannig hafa ekki allir séð þennan valkost við notkun Office 365.  

Microsoft Invoicing er ekki lengur í boði, en ef þú þarft að skrá þig inn á Invoicing til að sækja gögnin þín gætirðu séð skilaboð um að þú hafir ekki aðgang að Microsoft Invoicing þar sem reikningurinn þinn er notaður í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Þú sérð svipuð skilaboð ef þú setur upp farsímaforritið fyrir Invoicing.  

## <a name="workaround"></a>Hjáleið
Invoicing og [!INCLUDE[d365fin](includes/d365fin_md.md)] deila verkvangi. Það þýðir að þú ert viðurkennd(ur) sem núverandi notandi [!INCLUDE[d365fin](includes/d365fin_md.md)] þegar þú smellir á Invoicing í stjórnendamiðstöð Microsoft 365. Ástæðan er sú að Invoicing getur ekki notað sama fyrirtæki og [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Þannig verður þú að skrá þig inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] og endurnefna núverandi fyrirtæki þitt og búa síðan til nýtt fyrirtæki sem þú getur síðan notað í Invoicing. Engin gögn eru flutt eða skrifuð yfir í þessa hjáleið.

### <a name="to-rename-your-company"></a>Til að endurnefna fyrirtækið þitt
1. Skráðu þig inn á [!INCLUDE[d365fin](includes/d365fin_md.md)].
2. Í efra hægra horninu skaltu velja **Stillingar** táknið ![Stillingar](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") og velja síðan **Stillingar mínar**.
3. Í reitnum **Fyrirtæki** er annað fyrirtæki valið.
4. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fyrirtæki** og veldu síðan tengda tengilinn.  
5. Á síðunni **Fyrirtæki** skal velja **Breyta lista**.  
6. Breyta nafni færslu í *Fyrirtækið mitt* í eitthvað annað.  

    Bíddu í nokkrar mínútur. Við munum gera ýmsar breytingar á undirliggjandi gagnagrunni og það tekur nokkurn tíma.
7.  Þegar kerfið er tilbúið á ný skal nota hnappinn **Stofna nýtt fyrirtæki**.  
8.  Í svarglugganum sem birtist skaltu tilgreina nafnið sem *Fyrirtækið mitt* og veldu valkostinn **Framleiðsla - Aðeins uppsetningargögn**.  

Þetta tekur líka nokkrar mínútur. Þegar ferlinu lýkur geturðu fengið aðgang að Invoicing með Microsoft 365 Business. en aðeins til að flytja út gögn þar sem forritið Reikningar er úrelt.  

### <a name="what-about-my-data"></a>Hvað með gögnin mín?
Þegar þú endurnefnir upprunalega fyrirtækið mitt, verða gagnagrunnstöflurnar sem geyma núverandi [!INCLUDE[d365fin](includes/d365fin_md.md)] gögn þín endurnefnd, en gögnin sjálft eru ekki snert.  

Ef þú notar bæði Invoicing og [!INCLUDE[d365fin](includes/d365fin_md.md)] eru gögnin geymd í tveimur mismunandi hólfum (tvö fyrirtæki). Ekkert er deilt, þannig að þú verður að stjórna viðskiptamönnum og vörum í báðum fyrirtækjum.  

## <a name="see-also"></a>Sjá einnig
[Algengar spurningar](across-faq.md)  
[Stjórnun](admin-setup-and-administration.md)  
