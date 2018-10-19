---
title: "Hvernig á að búa til sérstillta grunnstillingarpakka fyrirtækja | Microsoft Docs"
description: "Eftir því sem fyrirtækið vex, er líklegt að treyst verði á safn fyrirtækjategunda sem verður notað með flestum af viðskiptamönnum fyrirtækisins. Hægt er að auðvelda innleiðingarferlið með því að breyta þessum tegundum í grunnstillingarpakka fyrir fyrirtæki sem hægt er að nota aftur."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e26174fcf723e13ef5a9ed0b386006c0439e1c7a
ms.contentlocale: is-is
ms.lasthandoff: 09/28/2018

---
# <a name="create-custom-company-configuration-packages"></a>Búa til sérstillta grunnstillingarpakka fyrirtækja
Eftir því sem fyrirtækið vex, er líklegt að treyst verði á safn fyrirtækjategunda sem verður notað með flestum af viðskiptamönnum fyrirtækisins. Hægt er að auðvelda innleiðingarferlið með því að breyta þessum tegundum í grunnstillingarpakka fyrir fyrirtæki sem hægt er að nota aftur.  

Almennt eru grunnstillingarpakkar stofnaðir fyrir hverja virkni, s.s. framleiðslu. Það gerir þér kleift að nota og setja upp ný svæði í fyrirtæki eftir þörfum  

Önnur nálgun væri að stofna sendingu sem inniheldur töflur sem skilgreina uppsetningu, s. s. eftirfarandi:  

-   Eignagrunnur  
-   Uppsetning fjárhags  
-   Birgðagrunnur  
-   Framleiðslugrunnur  
-   Innkaupagrunnur  
-   Tengslastjórnunargrunnur  
-   Þjónustukerfisgrunnur  
-   Sölugrunnur  
-   Vöruhúsagrunnur  
-   Alm. bókunargrunnur  
-   VSK-bókunargrunnur  
-   Birgðabókunargrunnur  

Til að sjá heildarlista yfir uppsetningartöflur skaltu velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning** og veldu síðan tengda tengilinn.  

## <a name="to-create-a-custom-company-configuration-package"></a>Til að búa til sérstilltan grunnstillingarpakka fyrirtækis  
1.  Stofna nýjan [!INCLUDE[d365fin](includes/d365fin_md.md)]. ***EKKI MÖGULEGT tengill við hjálp til að „Búa til nýjan leigjanda“***.   
2.  Stofna nýtt fyrirtæki fyrir atvinnugreinina eða lausnarsniðmáti. Nánari upplýsingar eru í [Stofna nýtt fyrirtæki](admin-how-to-create-a-new-company.md).  
3.  Setja upp nýja fyrirtækið á þann hátt sem þörf krefur. Fylla út allar nauðsynlegar töflur.  
4.  Opna skal nýja fyrirtækið.
5. Opna gluggann **Grunnstillingarvinnublað**.  
6.  Bæta töflunum sem óskað er eftir að færa á annað fyrirtæki við vinnublaðið. Úthluta vinnublaðslínunum til pakkans.  
7.  Stofna spurningalista fyrir mest notuðu uppsetningartöflurnar.  
8.  Stofna skilgreiningarsniðmát til að auðvelda stofnun aðalgagna, svo sem viðskiptavini eða vöru.  
9.  Flytja út pakka notanda sem rapidstart-skrá.  

## <a name="see-also"></a>Sjá einnig  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)

