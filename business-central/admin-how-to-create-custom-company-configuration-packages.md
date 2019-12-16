---
title: Hvernig á að búa til sérstillta grunnstillingarpakka fyrirtækja | Microsoft Docs
description: Eftir því sem fyrirtækið vex, er líklegt að treyst verði á safn fyrirtækjategunda sem verður notað með flestum af viðskiptamönnum fyrirtækisins. Hægt er að auðvelda innleiðingarferlið með því að breyta þessum tegundum í grunnstillingarpakka fyrir fyrirtæki sem hægt er að nota aftur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 99fad48961dc201a25af061cf982a1c65d9446bd
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878866"
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

Til að sjá heildarlista yfir uppsetningartöflur skaltu velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Handvirk uppsetning** og veldu síðan tengda tengilinn.  

## <a name="to-create-a-custom-company-configuration-package"></a>Til að búa til sérstilltan grunnstillingarpakka fyrirtækis  
1.  Búa til nýtt fyrirtæki. Frekari upplýsingar eru í [Stofna ný fyrirtæki í Business Central](about-new-company.md).  
3.  Setjið upp nýja fyrirtækið á þann hátt sem þörf krefur. Fylla út allar nauðsynlegar töflur.  
4.  Opna skal nýja fyrirtækið.
5. Opna skal síðun **Skilgreiningarvinnublað**.  
6.  Bæta töflunum sem óskað er eftir að færa á annað fyrirtæki við vinnublaðið. Úthluta vinnublaðslínunum til pakkans.  
7.  Stofna spurningalista fyrir mest notuðu uppsetningartöflurnar.  
8.  Stofna skilgreiningarsniðmát til að auðvelda stofnun aðalgagna, svo sem viðskiptavini eða vöru.  
9.  Flytja út pakka notanda sem rapidstart-skrá.  

## <a name="see-also"></a>Sjá einnig  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)
