---
title: "Tengja gögn við flæði| Microsoft Docs"
description: "Notandi getur gert Financials-gögnin sín aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til sjálfvirkt verkflæði."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 03/21/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 5d7fa359ee99cd177a445e025ddf8d156c6e2421
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Nota [!INCLUDE[d365fin](includes/d365fin_md.md)] í sjálfvirku verkflæði.
Notandi getur notað [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín sem hluta af verkflæði í Microsoft Flow.  

> [!NOTE]  
>   Notandi verður að vera með gildan reikning hjá [!INCLUDE[d365fin](includes/d365fin_md.md)] og hjá Flæði.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Til að bæta [!INCLUDE[d365fin](includes/d365fin_md.md)]við sem gagnaveitu í flæði
1. Flettið í [flow.microsoft.com](https://flow.microsoft.com/en-us/) í vafranum og skráið ykkur svo inn.
2. Veldu **Mitt flæði** af borðanum efst á síðunni.
3. Það eru 2 leiðir til að búa til flæði; **Stofna skjámyndarsniðmát** og **Stofna úr auðu**. Sniðmát er fyrirframskilgreint flæði sem hefur verið búið til fyrir þig.  Til að nota sniðmát skaltu einfaldlega velja það og búa til tengingu fyrir hverja þjónustu sem sniðmátið notar. Autt sniðmát gerir þér kleift að búa til nýtt flæði alveg frá grunni. 
4. Til að búa til úr auðu skal í glugganum **Mitt flæði** velja valkostinn **Stofna úr auðu**.
5. Leitaðu að **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]** tengi.
6. Farðu í lista yfir tiltækar kveikjur og veldu eina af [!INCLUDE[d365fin](includes/d365fin_md.md)] tiltækum kveikjum í boði:  
    *Þegar beðið er um samþykki viðskiptavinar*,  
    *Þegar beðið er um samþykki fyrir almenna færslubókarkeyrslu*,  
    *Þegar beðið er um samþykki fyrir almenna færslubókarlínu*,  
    *Þegar beðið er um samþykki fyrir vöru*,  
    *Þegar beðið er um samþykki innkaupaskjals*,  
    *Þegar beðið er um samþykki söluskjals*, eða  
    *Þegar beðið er um samþykki lánardrottins*.
7. Flæði biður þig um að velja fyrirtæki innan [!INCLUDE[d365fin](includes/d365fin_md.md)] leigjandann þíns, ásamt öllum þeim skilyrðum sem eru í gögnunum sem þú vilt hlusta á. 

Nú hefur notanda tekist að tengjast gögnum sínum í Business Central og getur byrjað að byggja upp flæðið. 

8. Til að stofna úr sniðmáti skal velja valkostinn **Stofna úr sniðmáti**.
9. Leitaðu að sniðmáti **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**. 
10. Veldu eitt sniðmát af listanum yfir tiltæk sniðmát.  
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
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] færslubókarkeyrslu*,  
    *Biðja um samþykkt fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] færslubókarlínum*.  
11. Flæði biður þig um velja fyrirtæki innan leigjandans [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Vegna þess að hvert skref í Flæði er óháð því næsta, getur verið að þú þurfir að skilgreina fyrirtækið mörgum sinnum þegar þú notar [!INCLUDE[d365fin_md](includes/d365fin_md.md)] sniðmát.
12. Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] sniðmátið samþættir við kerfi grunnverkflæðis í Microsoft[!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Sem þýðir að í hvert skipti sem þú notar eitt af þessum sniðmátum til að búa til flæði, er samsvarandi verkflæði búið til innan Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].  Skoðaðu verkflæðisskjöl fyrir Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].

Frekari upplýsingar eru í [Flæðisskjöl](https://docs.microsoft.com/en-us/flow/getting-started).

Fyrir úrræðaleit við Microsoft Flow sjá [Úrræðaleit samþættingar við Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Sjá einnig
[Hafist handa](product-get-started.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](upload-data.md)  
[Vinna með notendur og heimildir](ui-how-users-permissions.md)   
[Stjórna [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] vinnuflæði](across-use-workflows.md)  
[Notandauppsetning samþykktar](across-how-to-set-up-approval-users.md)  
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Fjármál](finance.md)  

