---
title: Úrræðaleita sjálfvirk verkflæði
description: Kynntu þér hvernig á að úrræðaleita milli Business Central og Power Automate þegar sjálfvirkt verkflæði er búið til.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions, Power Automate,
ms.date: 08/04/2022
ms.author: edupont
ms.openlocfilehash: 42b9a61f40afda0a50d6c6ec86d9984e53ae9ffb
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585919"
---
# <a name="troubleshoot-your-prod_short-automated-workflows"></a>Úrræðaleitaðu [!INCLUDE[prod_short](includes/prod_short.md)] sjálfvirku verkflæðin þín

Þegar þú tengir [!INCLUDE [prod_short](includes/prod_short.md)] við Power Automate til að búa til sjálfvirk verkflæði gætu komið upp villuboð. Í þessari grein er að finna tillögur að lausnum á endurteknum vandamálum.

## <a name="flow-doesnt-run-on-all-records-created-or-changed"></a>Flæði keyrir ekki á öllum færslum sem eru stofnaðar eða breytt

### <a name="problem"></a>Vandamál

Ef tilvik stofnar eða breytir fullt af færslum keyrir flæðið ekki á sumum eða öllum færslum.

### <a name="possible-cause"></a>Möguleg orsök

Eins og er eru takmörk fyrir því hversu margar færslur flæði getur unnið úr. Ef fleiri en 100 færslur eru stofnaðar eða breytt á innan við 30 sekúndum verður flæðið ekki ræst.

> [!NOTE]
> Fyrir þróunaraðila er ræsing flæðis gerð í gegnum tilkynningar veftengingar og þessi takmörkun er vegna þess hvernig tengill Business Central meðhöndlar `collection` tilkynningar. Frekari upplýsingar er að finna í [Unnið með veftengingar í Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) í hjálp þróunaraðila og stjórnanda.

## <a name="entity-set-not-found-error"></a>Villan „Einingasamstæða finnst ekki“

### <a name="problem"></a>Vandamál

Þegar nýtt Power Automate flæði er búið til með því að nota [!INCLUDE[prod_short](includes/prod_short.md)] samþykkisræsingu, eins og *Þegar beðið er um samþykki innkaupaskjals* gætu komið upp villuboð svipuð og þessi:

`Entity set not found: \<name\>`

Staðgengillinn, `\<name\>`, er þjónustuheiti vefþjónustunnar sem vantar, t.d. *workflowWebhookSubscriptions* eða *workflowPurchaseDocumentLines*.

### <a name="possible-cause"></a>Möguleg orsök

Notkun Power Automate fyrir samþykki krefst þess að ákveðnir síðu- og kóðaeiningarhlutir séu birtir sem vefþjónustur. Sjálfgefið er að flestir nauðsynlegir hlutir séu birtir sem vefþjónustur. En í sumum tilvikum kann umhverfi þitt að hafa verið sérsniðið þannig að þessir hlutir eru ekki lengur birtir.

### <a name="fix"></a>Laga

Farðu á síðuna **Vefþjónustur** og gakktu úr skugga um að eftirfarandi hlutir séu birtir sem vefþjónustur. Það ætti að vera færsla í listanum fyrir hvern hlut með gátreitinn **Birt** valinn.  

| Gerð hlutar | Kenni hlutar | Heiti hlutar | Heiti þjónustu |
|--|--|--|--|
| Codeunit | 1544 | WorkflowWebhookSubscription | WorkflowActionResponse |
| Síða | 6408 | workflowCustomers | workflowCustomers |
| Síða | 6406 | workflowGenJournalBatches | workflowGenJournalBatches |
| Síða | 6407 | workflowGenJournalLines | workflowGenJournalLines |
| Síða | 6409 | workflowItems | workflowItems |
| Síða | 6405 | Eining innkaupaskjalalínu | workflowPurchaseDocumentLines |
| Síða | 6404 | workflowPurchaseDocuments | workflowPurchaseDocuments |
| Síða | 6403 | Eining söluskjalalínu | workflowSalesDocumentLines |
| Síða | 6402 | workflowSalesDocuments | workflowSalesDocuments |
| Síða | 6410 | workflowVendors | workflowVendors |
| Síða | 831 | workflowWebhookSubscriptions | workflowWebhookSubscriptions |

> [!NOTE]
> Gildið fyrir **Heiti þjónustu** verður að vera nákvæmlega eins og sýnt er í töflunni. Ekki breyta eða þýða þjónustuheitið.

Frekari upplýsingar um vefþjónustur er að finna í [Gefa út vefþjónustu](across-how-publish-web-service.md).

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/use-power-automate/).

## <a name="see-also"></a>Sjá einnig .

[Nota Power Automate flæði í [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)  
[Verkflæði](across-workflow.md)  
[Setja upp sjálfvirk verkfllæði](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Kveikja á skyndiflæði](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  
[Stjórna Power Automate flæði](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
