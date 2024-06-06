---
title: Úrræðaleit vegna sjálfvirkra verkflæða
description: Kynntu þér hvernig á að úrræðaleita milli Business Central og Power Automate þegar sjálfvirkt verkflæði er búið til.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions, Power Automate,'
ms.date: 12/13/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
---

# Úrræðaleit vegna [!INCLUDE[prod_short](includes/prod_short.md)] sjálfvirkra verkflæða

Þegar þú tengir [!INCLUDE [prod_short](includes/prod_short.md)] við Power Automate til að búa til sjálfvirk verkflæði gætu komið upp villuboð. Í þessari grein er að finna tillögur að lausnum á endurteknum vandamálum.

## Flæði keyrir ekki á öllum færslum sem eru stofnaðar eða breytt

### Vandamál

Ef tilvik stofnar eða breytir mörgum færslum keyrir flæðið ekki í sumum eða öllum færslum.

### Möguleg orsök

Eins og er eru takmörk fyrir því hversu margar færslur flæði getur unnið úr. Ef fleiri en 1000 færslur eru stofnaðar eða breyttar innan 30 sekúndna er flæðið ekki sett af stađ.

> [!NOTE]
> Fyrir þróunaraðila er ræsing flæðis gerð í gegnum tilkynningar veftengingar og þessi takmörkun er vegna þess hvernig tengill Business Central meðhöndlar `collection` tilkynningar. Frekari upplýsingar er að finna í [Unnið með veftengingar í Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) í hjálp þróunaraðila og stjórnanda.

## "Svarið frá Þjónustumiðstöð Business Central er of stór" villa

### Vandamál

Þegar aðgerð sem hefur samskipti við færslur (t.d *. Stofna færslu (V3)*  og *Sækja færslu (V3))* Power Automate  gæti komið upp villa svipuð þessari:

`The response from the Business Central service is too large`

### Möguleg orsök

Jafnvel þó að Business Central hafi engin sett takmörk á stærð færslna sem API skilar, Dynamics 365 Business Central getur tengið fyrir Power Automate tengið aðeins unnið með færslur allt að 8 MB.

Öll Business Central API sem fylgir vöruskilafærslum Microsoft undir þessum takmörkum, en API sem samstarfsaðilar veita ekki. Ef villa birtist "Svarið frá Business Central þjónustunni er of stórt" skal hafa samband við félagann sem stofnaði API sem þú notar.

## Villan „Einingasamstæða finnst ekki“

### Vandamál

Þegar nýtt Power Automate flæði er búið til með því að nota [!INCLUDE[prod_short](includes/prod_short.md)] samþykkisræsingu, eins og *Þegar beðið er um samþykki innkaupaskjals* gætu komið upp villuboð svipuð og þessi:

`Entity set not found: \<name\>`

Staðgengillinn, `\<name\>`, er þjónustuheiti vefþjónustunnar sem vantar, t.d. *workflowWebhookSubscriptions* eða *workflowPurchaseDocumentLines*.

### Möguleg orsök

Notkun Power Automate fyrir samþykki krefst þess að ákveðnir síðu- og kóðaeiningarhlutir séu birtir sem vefþjónustur. Sjálfgefið er að flestir nauðsynlegir hlutir séu birtir sem vefþjónustur. En í sumum tilfellum gæti umhverfið hafa verið sérsniðið þannig að þessir hlutir séu ekki lengur birtir.

### Laga

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

## Sjá einnig .

[Nota Power Automate flæði í [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)  
[Verkflæði](across-workflow.md)  
[Setja upp sjálfvirk verkfllæði](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Kveikja á skyndiflæði](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  
[Stjórna Power Automate flæði](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
