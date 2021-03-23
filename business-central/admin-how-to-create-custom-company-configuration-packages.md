---
title: Hvernig á að búa til sérstillta grunnstillingarpakka fyrirtækja | Microsoft Docs
description: Eftir því sem fyrirtækið vex, er líklegt að treyst verði á safn fyrirtækjategunda sem verður notað með flestum af viðskiptamönnum fyrirtækisins. Hægt er að auðvelda innleiðingarferlið með því að breyta þessum tegundum í grunnstillingarpakka fyrir fyrirtæki sem hægt er að nota aftur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a1b1bfd5dd685eb57e291842d7b6d2e3691482fc
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378299"
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

> [!IMPORTANT]
> Farðu varlega ef þú velur töflur eða reiti sem hafa sama tímabundna heitið en eru aðgreind með sérstöfum, t.d. %, &, <, >, (, og ). Til dæmis getur taflan "XYZ" innihaldið reitina „Svæði 1“ og „Svæði 1%“.
>
> XML-úrvinnslan samþykkir aðeins suma sérstafi og fjarlægir þá sem hún samþykkir ekki. Ef sértákn á borð við %-merkið í „Svæði 1%“ er fjarlægt, verða til tvær eða fleiri töflur eða reitir með sama heitinu og villa kemur upp þegar grunnstillingapakki er fluttur út eða inn.

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


[!INCLUDE[footer-include](includes/footer-banner.md)]