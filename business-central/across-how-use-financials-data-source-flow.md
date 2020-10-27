---
title: Tengja gögn við Power Automate| Microsoft Docs
description: Notandi getur gert Business Central-gögnin sín aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til sjálfvirkt verkflæði.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, OData, Power App, SOAP
ms.date: 10/01/2020
ms.author: bmeier
ms.openlocfilehash: 8f4da5b51b4e0df5cdf6f41f7a78c0a51cf0f083
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924854"
---
# <a name="using-prodshort-in-an-automated-workflow"></a>Nota [!INCLUDE[prodshort](includes/prodshort.md)] í sjálfvirku verkflæði.

Notandi getur notað [!INCLUDE[prodshort](includes/prodshort.md)]-gögnin sín sem hluta af verkflæði í Microsoft Power Automate.

> [!NOTE]
> Til viðbótar við Power Automate er hægt að nota verkflæðisvirknina innan [!INCLUDE[prodshort](includes/prodshort.md)]. Hafa skal í huga að þótt þetta séu tvö aðskilin verkflæðisforrit, þá eru öll flæðissniðmát sem búin eru til með Power Automate bætt við listann yfir verkflæðissniðmát innan [!INCLUDE[prodshort](includes/prodshort.md)]. Frekari upplýsingar eru í [Verkflæði](across-workflow.md).  

> [!NOTE]  
> Notandi verður að vera með gildan reikning hjá [!INCLUDE[prodshort](includes/prodshort.md)] og hjá Power Automate.  

## <a name="to-add-prodshort-as-a-data-source-in-power-automate"></a>Til að bæta [!INCLUDE[prodshort](includes/prodshort.md)] við sem gagnaveitu í Power Automate

1. Flettið í [flow.microsoft.com](https://flow.microsoft.com) í vafranum og skráið ykkur svo inn.
2. Veldu **Mitt flæði** af borðanum efst á síðunni.
3. Það eru þrjár leiðir til að búa til flæði; **Byrja á sniðmáti** , **Byrja á auðu** og **Byrja á tengli** . Sniðmát er fyrirframskilgreint flæði sem hefur verið búið til fyrir þig. Til að nota sniðmát skaltu einfaldlega velja það og búa til tengingu fyrir hverja þjónustu sem sniðmátið notar. Með valkostunum **Byrja á auðu** og **Byrja á tengli** er hægt að stofna nýtt flæði frá grunni.
4. Til að búa til úr auðu skal á síðunni **Mitt flæði** velja valkostina **Byrja á auðu** og **Sjálfvirkt flæði** .
5. Leitaðu að **Microsoft [!INCLUDE[prodlong](includes/prodlong.md)]** tengi.
6. Skilgreinið heiti og veljið kveikjuna sem á að nota fyrir flæðið.
7. Farðu í lista yfir tiltækar kveikjur og veldu eina af [!INCLUDE[prodshort](includes/prodshort.md)] tiltækum kveikjum í boði:  

    *Þegar beðið er um samþykki lánardrottins* ,  
    *Þegar beðið er um samþykki fyrir almenna færslubókarlínu* ,  
    *Þegar færslu er eytt* ,  
    *Þegar færslu er breytt* ,  
    *Þegar færsla er stofnuð* ,  
    *Þegar færslu er breytt* ,  
    *Þegar beðið er um samþykki fyrir almenna færslubókarkeyrslu* ,  
    *Þegar beðið er um samþykki viðskiptavinar* ,  
    *Þegar beðið er um samþykki fyrir vöru* ,  
    *Þegar beðið er um samþykki innkaupaskjals* , eða  
    *Þegar beðið er um samþykki söluskjals* .

8. Power Automate biður þig um að velja umhverfi og fyrirtæki innan [!INCLUDE[prodshort](includes/prodshort.md)] leigjandann þíns, ásamt öllum þeim skilyrðum sem eru í gögnunum sem þú vilt hlusta á.

    > [!NOTE]
    > [!INCLUDE[prodshort](includes/prodshort.md)] tengillinn fyrir Power Automate styður mörg framleiðslu- og sandkassaumhverfi. Ef ekki hafa verið stofnuð mörg framleiðslu- og sandkassaumhverfi er **Framleiðsla** eina tiltæki valkosturinn sem hægt er að velja.  

    Nú hefur notanda tekist að tengjast gögnum sínum í Business Central [!INCLUDE[prodshort](includes/prodshort.md)] og getur byrjað að byggja upp flæðið.

9. Til að búa til úr sniðmáti skal velja valkostinn **Byrja á sniðmáti** .
10. Leitaðu að sniðmáti **Microsoft [!INCLUDE[prodlong](includes/prodlong.md)]** .
11. Í lista yfir tiltæk sniðmát skal velja eitt af sniðmátunum og síðan **Búa til** .  

    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] sölupöntun* ,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] sölutilboði* ,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] sölureikningi* ,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] sölukreditreikningi* ,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] viðskiptavini* ,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] innkaupapöntun* ,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] innkaupareikningi* ,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] innkaupakreditreikningi* ,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] vöru* ,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] lánardrottni* ,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] færslubókarkeyrslu* , eða    
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] færslubókarlínum* .  
12. Power Automate birtir lista yfir þjónustur sem notaðar eru í flæðissniðmátinu og reynir að tengjast sjálfkrafa við þessar þjónustur. Ef notandi hefur ekki áður tengst þjónustu verður notandi beðinn um að skrá sig inn í hverja þá þjónustu sem hann þarf að tengjast. Grænt gátmerki mun birtast við hliðina á hverri þjónustu þegar tenging hefur verið gerð. Veldu **Halda áfram** .
13. Power Automate biður þig um velja umhverfi og fyrirtæki innan leigjandans [!INCLUDE[prodshort](includes/prodshort.md)]. Vegna þess að hvert skref í flæði er óháð því næsta, getur verið að þú þurfir að skilgreina umhverfið og fyrirtækið mörgum sinnum þegar þú notar [!INCLUDE[prodshort](includes/prodshort.md)]Power Automate sniðmát.

Frekari upplýsingar er að finna í [Power Automate skráning](/power-automate/getting-started).

## <a name="see-also"></a>Sjá einnig

[Hafist handa](product-get-started.md)  
[Verkflæði](across-workflow.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Úthluta leyfi til notenda og hópa](ui-define-granular-permissions.md)  
[Stjórna [!INCLUDE[prodlong](includes/prodlong.md)] vinnuflæði](across-use-workflows.md)  
[Notandauppsetning samþykktar](across-how-to-set-up-approval-users.md)  
[Uppsetning [!INCLUDE[prodshort](includes/prodshort.md)]](setup.md)  
[Fjármál](finance.md)  
