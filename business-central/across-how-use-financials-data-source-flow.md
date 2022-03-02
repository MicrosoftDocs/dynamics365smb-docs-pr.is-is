---
title: Tengja gögn við Power Automate| Microsoft Docs
description: Notandi getur gert Business Central-gögnin sín aðgengileg sem gagnaveitu og tiltekið OData vefslóð úr vefþjónustunni til að búa til sjálfvirkt verkflæði.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 07/27/2021
ms.author: edupont
author: jswymer
ms.openlocfilehash: 7335092e74c0f681ba14a81a7045f2688fbb1df4
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8133357"
---
# <a name="using-prod_short-in-an-automated-workflow"></a>Nota [!INCLUDE[prod_short](includes/prod_short.md)] í sjálfvirku verkflæði.

Notandi getur notað [!INCLUDE[prod_short](includes/prod_short.md)]-gögnin sín sem hluta af verkflæði í Microsoft Power Automate.

> [!NOTE]
> Til viðbótar við Power Automate er hægt að nota verkflæðisvirknina innan [!INCLUDE[prod_short](includes/prod_short.md)]. Hafa skal í huga að þótt þetta séu tvö aðskilin verkflæðisforrit, þá eru öll flæðissniðmát sem búin eru til með Power Automate bætt við listann yfir verkflæðissniðmát innan [!INCLUDE[prod_short](includes/prod_short.md)]. Frekari upplýsingar eru í [Verkflæði](across-workflow.md).  

> [!NOTE]  
> Notandi verður að vera með gildan reikning hjá [!INCLUDE[prod_short](includes/prod_short.md)] og hjá Power Automate.  

## <a name="add-prod_short-as-a-data-source-in-power-automate"></a>Bæta [!INCLUDE[prod_short](includes/prod_short.md)] við sem gagnaveitu í Power Automate

1. Flettið í [flow.microsoft.com](https://flow.microsoft.com) í vafranum og skráið ykkur svo inn.
2. Veldu **Mitt flæði** af borðanum efst á síðunni.
3. Það eru þrjár leiðir til að búa til flæði; **Byrja á sniðmáti**, **Byrja á auðu** og **Byrja á tengli**. Sniðmát er fyrirframskilgreint flæði sem hefur verið búið til fyrir þig. Til að nota sniðmát skaltu velja það og búa til tengingu fyrir hverja þjónustu sem sniðmátið notar. Með valkostunum **Byrja á auðu** og **Byrja á tengli** er hægt að stofna nýtt flæði frá grunni.
4. Til að búa til úr auðu skal á síðunni **Mitt flæði** velja valkostina **Byrja á auðu** og **Sjálfvirkt flæði**.
5. Leitaðu að **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]** tengi.
6. Skilgreinið heiti og veljið kveikjuna sem á að nota fyrir flæðið.
7. Farðu í lista yfir tiltækar kveikjur og veldu eina af [!INCLUDE[prod_short](includes/prod_short.md)] tiltækum kveikjum í boði:  

    - *Þegar beðið er um samþykki lánardrottins*  
    - *Þegar beðið er um samþykki fyrir almenna færslubókarlínu* 
    - *Þegar færslu er eytt*
    - *Þegar færslu er breytt*
    - *Þegar færsla er stofnuð*
    - *Þegar færsla er löguð*
    - *Þegar beðið er um samþykki fyrir almenna færslubókarkeyrslu* 
    - *Þegar beðið er um samþykki viðskiptavinar*
    - *Þegar beðið er um samþykki fyrir vöru*
    - *Þegar beðið er um samþykki innkaupaskjals*
    - *Þegar beðið er um samþykki söluskjals*

8. Power Automate biður þig um að velja umhverfi og fyrirtæki innan [!INCLUDE[prod_short](includes/prod_short.md)] leigjandans þíns, ásamt öllum þeim skilyrðum sem eru í gögnunum sem þú vilt hlusta á.

    > [!NOTE]
    > [!INCLUDE[prod_short](includes/prod_short.md)] tengillinn fyrir Power Automate styður mörg framleiðslu- og sandkassaumhverfi. Ef ekki hafa verið stofnuð mörg framleiðslu- og sandkassaumhverfi er **Framleiðsla** eini tiltæki valkosturinn sem hægt er að velja.  

    Nú hefur þér tekist að tengjast gögnum þínum í Business Central[!INCLUDE[prod_short](includes/prod_short.md)] og getur byrjað að byggja upp flæðið.

9. Til að búa til úr sniðmáti skal velja valkostinn **Byrja á sniðmáti**.
10. Leitaðu að sniðmáti **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**.
11. Í lista yfir tiltæk sniðmát skal velja eitt af sniðmátunum og síðan **Búa til**.  

    - *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] sölupöntun*
    - *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] sölutilboð*
    - *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] sölureikning*
    - *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] sölukreditreikning*
    - *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] viðskiptavin*
    - *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] innkaupapöntun*
    - *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] innkaupareikning*
    - *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] innkaupakreditreikning*  
    - *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] vöru*
    - *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] lánardrottin*
    - *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] færslubókarkeyrslu*  
    - *Biðja um samþykkt fyrir Microsoft [!INCLUDE[prod_long](includes/prod_long.md)] færslubókarlínur*
12. Power Automate birtir lista yfir þjónustur sem notaðar eru í flæðissniðmátinu og reynir að tengjast sjálfkrafa við þessar þjónustur. Ef notandi hefur ekki áður tengst þjónustu verður notandi beðinn um að skrá sig inn í hverja þá þjónustu sem hann þarf að tengjast. Grænt gátmerki mun birtast við hliðina á hverri þjónustu þegar tenging hefur verið gerð. Veldu **Halda áfram**.
13. Power Automate biður þig um velja umhverfi og fyrirtæki innan leigjandans [!INCLUDE[prod_short](includes/prod_short.md)]. Vegna þess að hvert skref í flæði er óháð því næsta, getur verið að þú þurfir að skilgreina umhverfið og fyrirtækið mörgum sinnum þegar þú notar [!INCLUDE[prod_short](includes/prod_short.md)]Power Automate sniðmát.

Frekari upplýsingar er að finna í [Power Automate skráning](/power-automate/getting-started).

## <a name="troubleshooting"></a>Úrræðaleit

### <a name="entity-set-not-found-error"></a>Villan „Einingasamstæða finnst ekki“

#### <a name="problem"></a>Vandamál

Þegar nýtt Power Automate flæði er búið til með [!INCLUDE[prod_short](includes/prod_short.md)] samþykkisræsingu, eins og *Þegar beðið er um samþykki innkaupaskjals* koma upp villuboð líkt og:

**Einingasamstæða finnst ekki: \<name\>**

þar sem **\<name\>** er þjónustuheiti vefþjónustunnar sem vantar, eins og **workflowWebhookSubscriptions** eða **workflowPurchaseDocumentLines**.

#### <a name="possible-cause"></a>Möguleg orsök

Að nota Power Automate til að samþætta við [!INCLUDE[prod_short](includes/prod_short.md)] samþykki þín krefst þess að ákveðnir síðu- og kóðaeiningahlutir séu birtir sem vefþjónustur. Sjálfgefið er að flestir nauðsynlegir hlutir séu birtir sem vefþjónustur fyrir þig. En í sumum tilvikum kann umhverfi þitt að hafa verið sérsniðið þannig að þessir hlutir eru ekki lengur birtir.

#### <a name="fix"></a>Laga

Farðu á síðuna **Vefþjónustur** og gakktu úr skugga um að eftirfarandi hlutir séu birtir sem vefþjónustur. Það ætti að vera færsla í listanum fyrir hvern hlut með gátreitinn **Birt** valinn. 

|Gerð hlutar|Kenni hlutar|Heiti hlutar|Heiti þjónustu|
|-----------|---------|-----------|------------|
|Codeunit|  1544    |WorkflowWebhookSubscription|WorkflowActionResponse|
|Síða|  6408|   workflowCustomers|  workflowCustomers|
|Síða   |6406   |workflowGenJournalBatches| workflowGenJournalBatches|
|Síða   |6407   |workflowGenJournalLines|workflowGenJournalLines|
|Síða   |6409   |workflowItems| workflowItems|
|Síða   |6405   |Eining innkaupaskjalalínu|workflowPurchaseDocumentLines|
|Síða|  6404    |workflowPurchaseDocuments| workflowPurchaseDocuments|
|Síða|  6403    |Eining söluskjalalínu |workflowSalesDocumentLines|
|Síða|  6402|   workflowSalesDocuments| workflowSalesDocuments|
|Síða|  6410    |workflowVendors|   workflowVendors|
|Síða|  831 |workflowWebhookSubscriptions|  workflowWebhookSubscriptions|

> [!NOTE]
> Gildið fyrir **Heiti þjónustu** verður að vera nákvæmlega eins og sýnt er í töflunni. Ekki breyta eða þýða þjónustuheitið.

Frekari upplýsingar um birtingu vefþjónustu er að finna á [Birta vefþjónustu](across-how-publish-web-service.md).

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