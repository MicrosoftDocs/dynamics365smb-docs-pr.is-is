---
title: "Notkun reikningsfærslna í Finance and Operations, Business Edition | Microsoft Docs"
description: "Hjáleið fyrir aðgang að Microsoft Invoicing þegar þú hefur skráð þig fyrir Dynamics 365 for Finance and Operations, Business Edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/22/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: abceec5b1bc588e2842d0f512240c30eccbf6f8e
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a>Nota sama Office 365-reikninginn í [!INCLUDE[d365fin](includes/d365fin_long_md.md)] og Microsoft Invoicing
Þegar þú skráir þig í prufuáskrift fyrir [!INCLUDE[d365fin](includes/d365fin_md.md)] geturðu farið í 30 daga matsáfanga, þú getur byrjað áskrift eða hættir að nota [!INCLUDE[d365fin](includes/d365fin_md.md)]. Í öllum tilvikum, ef þú skráir þig inn á Office Portal, gætirðu séð reit sem heitir **Viðskiptamiðstöð** og smellt á það. Þetta er hluti af Office 365 Business Premium áskriftinni, svo ekki allir munu sjá þennan reit í Office Portal.  

Ef þú opnar viðskiptamiðstöðinni munt þú sjá hluta sem kallast **Invoicing**. Ef þú opnar þessum hluta sérð þú skilaboð að þú getur ekki opnað Microsoft Invoicing vegna þess að reikningurinn þinn er notaður í [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Þú sérð svipuð skilaboð ef þú setur upp farsímaforritið fyrir Invoicing.  

## <a name="workaround"></a>Hjáleið
Invoicing og [!INCLUDE[d365fin](includes/d365fin_md.md)] deila verkvangi. Það þýðir að þú ert viðurkennd sem núverandi notandi [!INCLUDE[d365fin](includes/d365fin_md.md)] þegar þú smellir á Invoicing í viðskiptamiðstöðinni. Ástæðan er sú að Invoicing getur ekki notað sama fyrirtæki og [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Þannig verður þú að skrá þig inn í [!INCLUDE[d365fin](includes/d365fin_md.md)] og endurnefna núverandi fyrirtæki þitt og búa síðan til nýtt fyrirtæki sem þú getur síðan notað í Invoicing. Engin gögn eru flutt eða skrifuð yfir í þessa hjáleið.

### <a name="to-rename-your-company"></a>Til að endurnefna fyrirtækið þitt
1.  Skráðu þig inn á þinn [!INCLUDE[d365fin](includes/d365fin_md.md)].  
2.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fyrirtæki** og velja svo viðeigandi tengil.  
3.  Í glugganum **Fyrirtæki** skal velja hnappinn **Breyta lista**.  
4.  Breyta nafni færslu í *Fyrirtækið mitt* í eitthvað annað.  

    Bíddu í nokkrar mínútur. Við munum gera ýmsar breytingar á undirliggjandi gagnagrunni og það tekur nokkurn tíma.
5.  Þegar kerfið er tilbúið á ný skal nota hnappinn **Stofna nýtt fyrirtæki**.  
6.  Í svarglugganum sem birtist skaltu tilgreina nafnið sem *Fyrirtækið mitt*, og veldu valkostinn **Suite Framleiðsla - aðeins uppsetningargögn**.  

Þetta tekur líka nokkrar mínútur. Þegar ferlið lýkur geturðu fengið aðgang að Invoicing sem hluti af Office 365 Business Premium upplifun.  

### <a name="what-about-my-data"></a>Hvað með gögnin mín?
Þegar þú endurnefnir upprunalega fyrirtækið mitt, verða gagnagrunnstöflurnar sem geyma núverandi [!INCLUDE[d365fin](includes/d365fin_md.md)] gögn þín endurnefnd, en gögnin sjálft eru ekki snert.  

Ef þú notar bæði Invoicing og [!INCLUDE[d365fin](includes/d365fin_md.md)] eru gögnin geymd í tveimur mismunandi hólfum (tvö fyrirtæki). Ekkert er deilt, þannig að þú verður að stjórna viðskiptamönnum og vörum í báðum fyrirtækjum.  

## <a name="see-also"></a>Sjá einnig
[Algengar spurningar](across-faq.md)  
[Uppsetning og stjórnun](admin-setup-and-administration.md)  

