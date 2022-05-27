---
title: Úrræðaleit vegna sjálfvirkra verkflæða
description: Lærðu hvernig á að leysa tenginguna á milli Viðskiptamiðseðla og Power Automate þegar búið er að byggja sjálfvirkt verkflæði.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: b8fff95ced93e7ee2a3112969f45525532b19445
ms.sourcegitcommit: e86f0bd15604c2fb327e3182929c44a4172790c7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/20/2022
ms.locfileid: "8786197"
---
# <a name="troubleshoot-your-prod_short-automated-workflows"></a>[!INCLUDE[prod_short](includes/prod_short.md)] Úrræðaleit vegna sjálfvirkra verkflæða

Þegar tengst [!INCLUDE [prod_short](includes/prod_short.md)] er við Power Automate Stofna sjálfvirka verkflæði er hugsanlegt að keyra villuskilaboð. Í þessari grein eru lagðar til lausnir sem tengjast oft endurteknum vandamálum.

## <a name="flow-doesnt-run-on-all-records-created-or-changed"></a>Flæði keyrir ekki á öllum færslum sem stofnaðar eru eða breyttar

### <a name="problem"></a>Vandamál

Ef atburður stofnar eða breytir mörgum færslum er flæðið ekki keyrt á sumum eða öllum færslum.

### <a name="possible-cause"></a>Möguleg orsök

Eins og er, þá eru takmörk fyrir því hversu margar plötur sem læðan getur unnið. Ef fleiri en 100 færslur eru búnar til eða þeim breytt innan 30 sekúndna þá fer flæðið ekki af stað.

> [!NOTE]
> Fyrir hönnuði er flæðikveikjun gerð í gegnum tilkynningar vefkrókur og þessi takmörkun er til komin vegna þess hvernig Business Central Connector annast `collection` tilkynningar. Nánari upplýsingar [fást með því að vinna með Webkrókur í Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) í Hjálp fyrir hönnuði og stjórnun.

## <a name="entity-set-not-found-error"></a>Villan „Einingasamstæða finnst ekki“

### <a name="problem"></a>Vandamál

Þegar nýtt Power Automate flæði er stofnað með [!INCLUDE[prod_short](includes/prod_short.md)] samþykktarkveikju, svo sem *þegar beðið* er um samþykki innkaupaskjals, gætu villuskilaboð orðið svipuð þessari:

`Entity set not found: \<name\>`

Frátakandi, `\<name\>`,, er þjónustuheiti vefþjónustunnar sem vantar, *til dæmis workflowwebhookáskriftir* eða *workflowkaupthing sedocumentlines*.

### <a name="possible-cause"></a>Möguleg orsök

Notkun Power Automate fyrir samþykktir þínar krefst þess að tilteknir síðu-og Codeunit hlutir séu gefnir upp sem vefþjónustur. Sjálfgefið er að flestir nauðsynlegir hlutir séu birtir sem vefþjónustur fyrir þig. En í sumum tilvikum kann umhverfi þitt að hafa verið sérsniðið þannig að þessir hlutir eru ekki lengur birtir.

### <a name="fix"></a>Laga

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

[Nota [!INCLUDE[prod_short](includes/prod_short.md)] í sjálfvirku verkflæði](across-how-use-financials-data-source-flow.md)  
[Verkflæði](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]