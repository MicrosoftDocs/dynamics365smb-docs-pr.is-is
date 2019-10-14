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
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 354babea367b80cdb0eae4078f6111d44583df9e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300762"
---
# <a name="using-the-same-office-365-account-in-included365finincludesd365fin_long_mdmd-and-microsoft-invoicing"></a>Nota sama Office 365-reikninginn í [!INCLUDE[d365fin](includes/d365fin_long_md.md)] og Microsoft Invoicing
Þegar þú skráir þig í prufuáskrift fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] geturðu farið í 30 daga matsáfanga, þú getur byrjað áskrift eða hættir að nota [!INCLUDE[d365fin](includes/d365fin_md.md)]. Í öllum tilvikum, ef þú skráir þig inn á Office Portal, gætirðu séð reit sem heitir **Microsoft Invoicing** og smellt á það. Þetta er hluti af Office 365 Business Premium áskriftinni, svo ekki allir munu sjá þennan reit í Office Portal.  

Ef þú opnar Microsoft Invoicing sérð þú skilaboð að þú getur ekki opnað Microsoft Invoicing vegna þess að reikningurinn þinn er notaður í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Þú sérð svipuð skilaboð ef þú setur upp farsímaforritið fyrir Invoicing.  

## <a name="workaround"></a>Hjáleið
Invoicing og [!INCLUDE[d365fin](includes/d365fin_md.md)] deila verkvangi. Það þýðir að þú ert viðurkennd sem núverandi notandi [!INCLUDE[d365fin](includes/d365fin_md.md)] þegar þú smellir á Invoicing í Office Portal. Ástæðan er sú að Invoicing getur ekki notað sama fyrirtæki og [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Þannig verður þú að skrá þig inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] og endurnefna núverandi fyrirtæki þitt og búa síðan til nýtt fyrirtæki sem þú getur síðan notað í Invoicing. Engin gögn eru flutt eða skrifuð yfir í þessa hjáleið.

### <a name="to-rename-your-company"></a>Til að endurnefna fyrirtækið þitt
1. Skráðu þig inn á [!INCLUDE[d365fin](includes/d365fin_md.md)].
2. Í efra hægra horninu skaltu velja **Stillingar** táknið ![Stillingar](media/ui-experience/settings_icon_small.png "Stillingar tákn fyrir miðstöð") og velja síðan **Stillingar mínar**.
3. Í reitnum **Fyrirtæki** er annað fyrirtæki valið.
4. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fyrirtæki** og veldu síðan tengda tengilinn.  
5. Á síðunni **Fyrirtæki** skal velja **Breyta lista**.  
6. Breyta nafni færslu í *Fyrirtækið mitt* í eitthvað annað.  

    Bíddu í nokkrar mínútur. Við munum gera ýmsar breytingar á undirliggjandi gagnagrunni og það tekur nokkurn tíma.
7.  Þegar kerfið er tilbúið á ný skal nota hnappinn **Stofna nýtt fyrirtæki**.  
8.  Í svarglugganum sem birtist skaltu tilgreina nafnið sem *Fyrirtækið mitt* og veldu valkostinn **Framleiðsla - Aðeins uppsetningargögn**.  

Þetta tekur líka nokkrar mínútur. Þegar ferlið lýkur geturðu fengið aðgang að Invoicing sem hluti af Office 365 Business Premium upplifun.  

### <a name="what-about-my-data"></a>Hvað með gögnin mín?
Þegar þú endurnefnir upprunalega fyrirtækið mitt, verða gagnagrunnstöflurnar sem geyma núverandi [!INCLUDE[d365fin](includes/d365fin_md.md)] gögn þín endurnefnd, en gögnin sjálft eru ekki snert.  

Ef þú notar bæði Invoicing og [!INCLUDE[d365fin](includes/d365fin_md.md)] eru gögnin geymd í tveimur mismunandi hólfum (tvö fyrirtæki). Ekkert er deilt, þannig að þú verður að stjórna viðskiptamönnum og vörum í báðum fyrirtækjum.  

## <a name="see-also"></a>Sjá einnig
[Algengar spurningar](across-faq.md)  
[Stjórnun](admin-setup-and-administration.md)  
