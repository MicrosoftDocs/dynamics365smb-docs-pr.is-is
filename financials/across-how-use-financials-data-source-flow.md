---
title: "Tengja gögn við flæði| Microsoft Docs"
description: "Notandi getur gert Financials-gögnin sín aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til sjálfvirkt verkflæði."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

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
    *Þegar færsla er stofnuð*,  
    *Þegar færslu er eytt*,  
    *Þegar færslu er breytt*,  
    *Þegar beðið er um samþykki viðskiptavinar*,  
    *Þegar beðið er um samþykki fyrir almenna færslubókarkeyrslu*,  
    *Þegar beðið er um samþykki fyrir almenna færslubókarlínu*,  
    *Þegar beðið er um samþykki fyrir vöru*,  
    *Þegar beðið er um samþykki innkaupaskjals*,  
    *Þegar beðið er um samþykki söluskjals*, eða  
    *Þegar beðið er um samþykki lánardrottins*.
5. Flow mun biðja um upplýsingarnar sem gefa þarf upp til að tengja notanda við [!INCLUDE[d365fin](includes/d365fin_md.md)]-gögnin sín. Ef ein af eftirfarandi kveikjum voru valdara: *Þegar færsla er stofnuð*, *Þegar færslu er breytt* eða *Þegar færslu er eytt*, verður að velja heiti fyrirtækis og töflu. Þegar einungis er um eina kveikju að ræða þarf aðeins að tilgreina heiti fyrirtækis til að tengjast.

   Flow birtir þá lista yfir fyrirtæki og töflur sem eru aðgengilegar úr [!INCLUDE[d365fin](includes/d365fin_md.md)]. Þessar töflur eða endapunktar tákna allar vefþjónustur sem notandi hefur birt úr [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Einnig er hægt að stofna nýja vefslóð vefþjónustu í [!INCLUDE[d365fin](includes/d365fin_md.md)] með því að nota aðgerðina **Stofna gagnamengi** á síðunni **Vefþjónustur** með því að nota Uppsetningu með hjálp fyrir **Setja upp skýrslugerð** eða með því að velja aðgerðina **Breyta í Excel** í hvaða lista sem er.

Nú hefur notanda tekist að tengjast gögnum sínum í Finance and Operations, Business Edition og getur byrjað að byggja upp flæðið. Frekari upplýsingar eru í [gögnum um Flow](https://flow.microsoft.com/documentation/getting-started/).

Fyrir úrræðaleit við Microsoft Flow sjá [Úrræðaleit samþættingar við Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Sjá einnig
[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](upload-data.md)  
[Vinna með notendur og heimildir](ui-how-users-permissions.md)    
[Uppsetning [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Fjármál](finance.md)  

