---
title: Tengja gögn við Power Automate| Microsoft Docs
description: Notandi getur gert Business Central-gögnin sín aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til sjálfvirkt verkflæði.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, OData, Power App, SOAP
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d179275dd5bd225ace1555bb312b81a9553db0c3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781337"
---
# <a name="using-prod_short-in-an-automated-workflow"></a>Nota [!INCLUDE[prod_short](includes/prod_short.md)] í sjálfvirku verkflæði.

Notandi getur notað [!INCLUDE[prod_short](includes/prod_short.md)]-gögnin sín sem hluta af verkflæði í Microsoft Power Automate.

> [!NOTE]
> Til viðbótar við Power Automate er hægt að nota verkflæðisvirknina innan [!INCLUDE[prod_short](includes/prod_short.md)]. Hafa skal í huga að þótt þetta séu tvö aðskilin verkflæðisforrit, þá eru öll flæðissniðmát sem búin eru til með Power Automate bætt við listann yfir verkflæðissniðmát innan [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar eru í [Verkflæði](across-workflow.md).  

> [!NOTE]  
> Notandi verður að vera með gildan reikning hjá [!INCLUDE[prod_short](includes/prod_short.md)] og hjá Power Automate.  

## <a name="to-add-prod_short-as-a-data-source-in-power-automate"></a>Til að bæta [!INCLUDE[prod_short](includes/prod_short.md)] við sem gagnaveitu í Power Automate

1. Flettið í [flow.microsoft.com](https://flow.microsoft.com) í vafranum og skráið ykkur svo inn.
2. Veldu **Mitt flæði** af borðanum efst á síðunni.
3. Það eru þrjár leiðir til að búa til flæði; **Byrja á sniðmáti**, **Byrja á auðu** og **Byrja á tengli**. Sniðmát er fyrirframskilgreint flæði sem hefur verið búið til fyrir þig. Til að nota sniðmát skaltu einfaldlega velja það og búa til tengingu fyrir hverja þjónustu sem sniðmátið notar. Með valkostunum **Byrja á auðu** og **Byrja á tengli** er hægt að stofna nýtt flæði frá grunni.
4. Til að búa til úr auðu skal á síðunni **Mitt flæði** velja valkostina **Byrja á auðu** og **Sjálfvirkt flæði**.
5. Leitaðu að **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]** tengi.
6. Skilgreinið heiti og veljið kveikjuna sem á að nota fyrir flæðið.
7. Farðu í lista yfir tiltækar kveikjur og veldu eina af [!INCLUDE[prod_short](includes/prod_short.md)] tiltækum kveikjum í boði:  

    *Þegar beðið er um samþykki lánardrottins*,  
    *Þegar beðið er um samþykki fyrir almenna færslubókarlínu*,  
    *Þegar færslu er eytt*,  
    *Þegar færslu er breytt*,  
    *Þegar færsla er stofnuð*,  
    *Þegar færslu er breytt*,  
    *Þegar beðið er um samþykki fyrir almenna færslubókarkeyrslu*,  
    *Þegar beðið er um samþykki viðskiptavinar*,  
    *Þegar beðið er um samþykki fyrir vöru*,  
    *Þegar beðið er um samþykki innkaupaskjals*, eða  
    *Þegar beðið er um samþykki söluskjals*.

8. Power Automate biður þig um að velja umhverfi og fyrirtæki innan [!INCLUDE[prod_short](includes/prod_short.md)] leigjandann þíns, ásamt öllum þeim skilyrðum sem eru í gögnunum sem þú vilt hlusta á.

    > [!NOTE]
    > [!INCLUDE[prod_short](includes/prod_short.md)] tengillinn fyrir Power Automate styður mörg framleiðslu- og sandkassaumhverfi. Ef ekki hafa verið stofnuð mörg framleiðslu- og sandkassaumhverfi er **Framleiðsla** eina tiltæki valkosturinn sem hægt er að velja.  

    Nú hefur notanda tekist að tengjast gögnum sínum í Business Central [!INCLUDE[prod_short](includes/prod_short.md)] og getur byrjað að byggja upp flæðið.

9. Til að búa til úr sniðmáti skal velja valkostinn **Byrja á sniðmáti**.
10. Leitaðu að sniðmáti **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**.
11. Í lista yfir tiltæk sniðmát skal velja eitt af sniðmátunum og síðan **Búa til**.  

    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] sölupöntun*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] sölutilboði*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] sölureikningi*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] sölukreditreikningi*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] viðskiptavini*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] innkaupapöntun*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] innkaupareikningi*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] innkaupakreditreikningi*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] vöru*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] lánardrottni*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] færslubókarkeyrslu*, eða    
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] færslubókarlínum*.  
12. Power Automate birtir lista yfir þjónustur sem notaðar eru í flæðissniðmátinu og reynir að tengjast sjálfkrafa við þessar þjónustur. Ef notandi hefur ekki áður tengst þjónustu verður notandi beðinn um að skrá sig inn í hverja þá þjónustu sem hann þarf að tengjast. Grænt gátmerki mun birtast við hliðina á hverri þjónustu þegar tenging hefur verið gerð. Veldu **Halda áfram**.
13. Power Automate biður þig um velja umhverfi og fyrirtæki innan leigjandans [!INCLUDE[prod_short](includes/prod_short.md)]. Vegna þess að hvert skref í flæði er óháð því næsta, getur verið að þú þurfir að skilgreina umhverfið og fyrirtækið mörgum sinnum þegar þú notar [!INCLUDE[prod_short](includes/prod_short.md)]Power Automate sniðmát.

Frekari upplýsingar er að finna í [Power Automate skráning](/power-automate/getting-started).

## <a name="see-also"></a>Sjá einnig

[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Verkflæði](across-workflow.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Stjórna [!INCLUDE[prod_long](includes/prod_long.md)] vinnuflæði](across-use-workflows.md)  
[Notandauppsetning samþykktar](across-how-to-set-up-approval-users.md)  
[Uppsetning [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Fjármál](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]