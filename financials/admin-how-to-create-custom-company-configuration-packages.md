---
title: "Hvernig á að búa til sérstillta grunnstillingarpakka fyrirtækja | Microsoft Docs"
description: "Eftir því sem fyrirtækið vex, er líklegt að treyst verði á safn fyrirtækjategunda sem verður notað með flestum af viðskiptamönnum fyrirtækisins. Hægt er að auðvelda innleiðingarferlið með því að breyta þessum tegundum í grunnstillingarpakka fyrir fyrirtæki sem hægt er að nota aftur."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 37fe7a482b88626adff1ef16496a785399d19a8d
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="create-custom-company-configuration-packages"></a>Búa til sérstillta grunnstillingarpakka fyrirtækja
Eftir því sem fyrirtækið vex, er líklegt að treyst verði á safn fyrirtækjategunda sem verður notað með flestum af viðskiptamönnum fyrirtækisins. Hægt er að auðvelda innleiðingarferlið með því að breyta þessum tegundum í grunnstillingarpakka fyrir fyrirtæki sem hægt er að nota aftur.  

Almennt eru grunnstillingarpakkar stofnaðir fyrir hverja virkni, s.s. framleiðslu. Það gerir þér kleift að nota og setja upp ný svæði í fyrirtæki eftir þörfum  

Önnur nálgun væri að stofna sendingu sem inniheldur töflur sem skilgreina uppsetningu, s. s. eftirfarandi:  

-   Eignagrunnur  
-   FjárhagsgrunnurUppsetning fjárhags  
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

Til að sjá heildarlista uppsetningartaflna skal velja táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslutákni"), slá inn **Uppsetning** og velja svo viðeigandi tengil.  

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

