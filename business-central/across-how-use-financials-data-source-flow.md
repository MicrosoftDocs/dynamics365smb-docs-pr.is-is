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
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 23e9ebbb75d23595d568d022526e551bf590a979
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
3. Í glugganum **Mitt flæði** skal velja valkostinn **Stofna úr auðu**.
4. Farðu í lista yfir tiltækar kveikjur og veldu eina af [!INCLUDE[d365fin](includes/d365fin_md.md)] tiltækum kveikjum í boði:  
    *Þegar beðið er um samþykki viðskiptavinar*,  
    *Þegar beðið er um samþykki fyrir almenna færslubókarkeyrslu*,  
    *Þegar beðið er um samþykki fyrir almenna færslubókarlínu*,  
    *Þegar beðið er um samþykki fyrir vöru*,  
    *Þegar beðið er um samþykki innkaupaskjals*,  
    *Þegar beðið er um samþykki söluskjals*, eða  
    *Þegar beðið er um samþykki lánardrottins*.
5. Flæði biður þig um velja fyrirtæki innan leigjandans [!INCLUDE[d365fin](includes/d365fin_md.md)]. Vegna þess að hvert skref í Flæði er óháð því næsta, getur verið að þú þurfir að skilgreina fyrirtækið mörgum sinnum þegar þú notar [!INCLUDE[d365fin](includes/d365fin_md.md)] sniðmát.

Nú hefur notanda tekist að tengjast gögnum sínum í Business Central og getur byrjað að byggja upp flæðið. Frekari upplýsingar eru í [gögnum um Flow](https://flow.microsoft.com/documentation/getting-started/).

Fyrir úrræðaleit við Microsoft Flow sjá [Úrræðaleit samþættingar við Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Sjá einnig
[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](upload-data.md)  
[Vinna með notendur og heimildir](ui-how-users-permissions.md)    
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Fjármál](finance.md)  

