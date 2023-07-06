---
title: Notkun Invoicing og Business Central
description: Hjáleið fyrir aðgang að Microsoft Invoicing þegar þú hefur skráð þig fyrir Dynamics 365 Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Invoicing, Microsoft 365'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="use-the-same-microsoft-365-account-in--and-microsoft-invoicing"></a><a name="use-the-same-microsoft-365-account-in--and-microsoft-invoicing"></a><a name="use-the-same-microsoft-365-account-in--and-microsoft-invoicing"></a>Nota sama Microsoft 365-reikninginn í [!INCLUDE[prod_short](includes/prod_long.md)] og Microsoft Invoicing
Þegar þú skráir þig í prufuáskrift fyrir [!INCLUDE[prod_short](includes/prod_short.md)] geturðu farið í 30 daga matsáfanga, þú getur byrjað áskrift eða hættir að nota [!INCLUDE[prod_short](includes/prod_short.md)]. Í öllum tilvikum getur þú á einhverjum tímapunkti hafa séð eitthvað sem kallast **Microsoft Invoicing** og smellt á það. Þetta forrit var hluti af því sem er núna Microsoft 365 Business Standard og var áður þekkt sem Microsoft 365 Business Premium-áskrift, þannig hafa ekki allir séð þennan valkost við notkun Microsoft 365.  

Microsoft Invoicing er ekki lengur í boði, en ef þú þarft að skrá þig inn á Invoicing til að sækja gögnin þín gætirðu séð skilaboð um að þú hafir ekki aðgang að Microsoft Invoicing þar sem reikningurinn þinn er notaður í [!INCLUDE[prod_short](includes/prod_short.md)].  

Þú sérð svipuð skilaboð ef þú setur upp farsímaforritið fyrir Invoicing.  

## <a name="workaround"></a><a name="workaround"></a><a name="workaround"></a>Hjáleið
Invoicing og [!INCLUDE[prod_short](includes/prod_short.md)] deila verkvangi. Það þýðir að þú þekkist sem núverandi notandi á [!INCLUDE[prod_short](includes/prod_short.md)] þegar þú smellir á reikningsfærslu í Microsoft 365 stjórnendamiðstöðinni. Ástæðan er sú að Invoicing getur ekki notað sama fyrirtæki og [!INCLUDE[prod_short](includes/prod_short.md)].  

Þannig verður þú að skrá þig inn í [!INCLUDE[prod_short](includes/prod_short.md)] og endurnefna núverandi fyrirtæki þitt og búa síðan til nýtt fyrirtæki sem þú getur síðan notað í Invoicing. Engin gögn eru flutt eða skrifuð yfir í þessa hjáleið.

### <a name="to-rename-your-company"></a><a name="to-rename-your-company"></a><a name="to-rename-your-company"></a>Til að endurnefna fyrirtækið þitt
1. Skráðu þig inn á [!INCLUDE[prod_short](includes/prod_short.md)].
2. Í efra hægra horninu skaltu velja **Stillingar** táknið ![Stillingar](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") og velja síðan **Stillingar mínar**.
3. Í reitnum **Fyrirtæki** er annað fyrirtæki valið.
4. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fyrirtæki** og veldu síðan tengda tengilinn.  
5. Á síðunni **Fyrirtæki** skal velja **Breyta lista**.  
6. Breyta nafni færslu í *Fyrirtækið mitt* í eitthvað annað.  

    Bíddu í nokkrar mínútur. Við munum gera ýmsar breytingar á undirliggjandi gagnagrunni og það tekur nokkurn tíma.
7.  Þegar kerfið er tilbúið á ný skal nota hnappinn **Stofna nýtt fyrirtæki**.  
8.  Í svarglugganum sem birtist skaltu tilgreina nafnið sem *Fyrirtækið mitt* og veldu valkostinn **Framleiðsla - Aðeins uppsetningargögn**.  

Þetta tekur líka nokkrar mínútur. Þegar ferlið lýkur geturðu fengið aðgang að Invoicing sem hluti af Microsoft 365 Business Standard upplifun. en aðeins til að flytja út gögn þar sem forritið Reikningar er úrelt.  

### <a name="what-about-my-data"></a><a name="what-about-my-data"></a><a name="what-about-my-data"></a>Hvað með gögnin mín?
Þegar þú endurnefnir upprunalega fyrirtækið mitt, verða gagnagrunnstöflurnar sem geyma núverandi [!INCLUDE[prod_short](includes/prod_short.md)] gögn þín endurnefnd, en gögnin sjálft eru ekki snert.  

Ef þú notar bæði Invoicing og [!INCLUDE[prod_short](includes/prod_short.md)] eru gögnin geymd í tveimur mismunandi hólfum (tvö fyrirtæki). Ekkert er deilt, þannig að þú verður að stjórna viðskiptamönnum og vörum í báðum fyrirtækjum.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig
[Algengar spurningar](across-faq.yml)  
[Stjórnun](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
