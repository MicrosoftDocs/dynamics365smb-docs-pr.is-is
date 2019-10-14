---
title: Tengja gögn við flæði| Microsoft Docs
description: Notandi getur gert Business Central-gögnin sín aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til sjálfvirkt verkflæði.
documentationcenter: ''
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: bmeier
ms.openlocfilehash: 86178bafa806fb8cba531d5b78157437c242d432
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305030"
---
# <a name="using-included365finincludesd365fin_mdmd-in-an-automated-workflow"></a>Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] í sjálfvirku verkflæði.
Notandi getur notað [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín sem hluta af verkflæði í Microsoft Flow.

> [!NOTE]
> Til viðbótar við Microsoft Flow er hægt að nota verkflæðisvirknina innan [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hafa skal í huga að þótt þetta séu tvö aðskilin verkflæðisforrit, þá eru öll Flow-sniðmát sem búin eru til með Microsoft Flow bætt við listann yfir verkflæðissniðmát innan [!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar eru í [Verkflæði](across-workflow.md).  

> [!NOTE]  
> Notandi verður að vera með gildan reikning hjá [!INCLUDE[d365fin](includes/d365fin_md.md)] og hjá Flæði.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-flow"></a>Til að bæta [!INCLUDE[d365fin](includes/d365fin_md.md)]við sem gagnaveitu í flæði
1. Flettið í [flow.microsoft.com](https://flow.microsoft.com/en-us/) í vafranum og skráið ykkur svo inn.
2. Veldu **Mitt flæði** af borðanum efst á síðunni.
3. Það eru þrjár leiðir til að búa til flæði; **Byrja á sniðmáti**, **Byrja á auðu** og **Byrja á tengli**. Sniðmát er fyrirframskilgreint flæði sem hefur verið búið til fyrir þig. Til að nota sniðmát skaltu einfaldlega velja það og búa til tengingu fyrir hverja þjónustu sem sniðmátið notar. Með valkostunum **Byrja á auðu** og **Byrja á tengli** er hægt að stofna nýtt flæði frá grunni.
4. Til að búa til úr auðu skal á síðunni **Mitt flæði** velja valkostina **Byrja á auðu** og **Sjálfvirkt flæði**.
5. Leitaðu að **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]** tengi.
6. Skilgreinið heiti og veljið kveikjuna sem á að nota fyrir flæðið.
7. Farðu í lista yfir tiltækar kveikjur og veldu eina af [!INCLUDE[d365fin](includes/d365fin_md.md)] tiltækum kveikjum í boði:  
    
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
     
8. Flæði biður þig um að velja umhverfi og fyrirtæki innan [!INCLUDE[d365fin](includes/d365fin_md.md)] leigjandann þíns, ásamt öllum þeim skilyrðum sem eru í gögnunum sem þú vilt hlusta á.

> [!NOTE]  
>   [!INCLUDE[d365fin](includes/d365fin_md.md)] tengillinn fyrir Microsoft Flow styður mörg framleiðslu- og sandkassaumhverfi. Ef ekki hafa verið stofnuð mörg framleiðslu- og sandkassaumhverfi er **Framleiðsla** eina tiltæki valkosturinn sem hægt er að velja. 

Nú hefur notanda tekist að tengjast gögnum sínum í Business Central og getur byrjað að byggja upp flæðið.

9. Til að búa til úr sniðmáti skal velja valkostinn **Byrja á sniðmáti**.
10. Leitaðu að sniðmáti **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
11. Í lista yfir tiltæk sniðmát skal velja eitt af sniðmátunum og síðan **Búa til**.  

    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] sölupöntun*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] sölutilboði*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] sölureikningi*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] sölukreditreikningi*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] viðskiptavini*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] innkaupapöntun*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] innkaupareikningi*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] innkaupakreditreikningi*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] vöru*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] lánardrottni*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] færslubókarkeyrslu*, eða    
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] færslubókarlínum*.  
12. Flæði birtir lista yfir þjónustur sem notaðar eru í Flow-sniðmátinu og reynir að tengjast sjálfkrafa við þessar þjónustur. Ef notandi hefur ekki áður tengst þjónustu verður notandi beðinn um að skrá sig inn í hverja þá þjónustu sem hann þarf að tengjast. Grænt gátmerki mun birtast við hliðina á hverri þjónustu þegar tenging hefur verið gerð. Veldu **Halda áfram**.
13. Flæði biður þig um velja umhverfi og fyrirtæki innan leigjandans [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Vegna þess að hvert skref í flæði er óháð því næsta, getur verið að þú þurfir að skilgreina umhverfið og fyrirtækið mörgum sinnum þegar þú notar [!INCLUDE[d365fin_md](includes/d365fin_md.md)] Flow-sniðmát.

Frekari upplýsingar eru í [Flæðisskjöl](/flow/getting-started).

## <a name="see-also"></a>Sjá einnig
[Hafist handa](product-get-started.md)  
[Verkflæði](across-workflow.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Vinna með notendur og heimildir](ui-how-users-permissions.md)   
[Stjórna [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] vinnuflæði](across-use-workflows.md)  
[Notandauppsetning samþykktar](across-how-to-set-up-approval-users.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Fjármál](finance.md)  
