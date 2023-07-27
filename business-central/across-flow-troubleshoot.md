---
title: Úrræðaleita sjálfvirk verkflæði
description: Kynntu þér hvernig á að úrræðaleita milli Business Central og Power Automate þegar sjálfvirkt verkflæði er búið til.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions, Power Automate,'
ms.date: 07/03/2023
ms.author: jswymer
ms.reviewer: jswymer
---

# <a name="troubleshoot-your--automated-workflows"></a>Úrræðaleitaðu [!INCLUDE[prod_short](includes/prod_short.md)] sjálfvirku verkflæðin þín

Þegar þú tengir [!INCLUDE [prod_short](includes/prod_short.md)] við Power Automate til að búa til sjálfvirk verkflæði gætu komið upp villuboð. Í þessari grein er að finna tillögur að lausnum á endurteknum vandamálum.

## <a name="flow-doesnt-run-on-all-records-created-or-changed"></a>Flæði keyrir ekki á öllum færslum sem eru stofnaðar eða breytt

### <a name="problem"></a>Vandamál

Ef atburður stofnar eða breytir mörgum færslum er flæðið ekki keyrt á sumum eða öllum færslum.

### <a name="possible-cause"></a>Möguleg orsök

Eins og er eru takmörk fyrir því hversu margar færslur flæði getur unnið úr. Ef fleiri en 1000 færslur eru stofnaðar eða þeim breytt innan 30 sekúndna þá er flæðið ekki ræst.

> [!NOTE]
> Fyrir þróunaraðila er ræsing flæðis gerð í gegnum tilkynningar veftengingar og þessi takmörkun er vegna þess hvernig tengill Business Central meðhöndlar `collection` tilkynningar. Frekari upplýsingar er að finna í [Unnið með veftengingar í Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) í hjálp þróunaraðila og stjórnanda.

## <a name="the-response-from-the-business-central-service-is-too-large-error"></a>"Viðbrögð fyrirtækja við Seðlabankaþjónustu eru of stór" Villa

### <a name="problem-1"></a>Vandamál

Þegar aðgerð er notuð sem virkar með færslum (svo sem  *Stofna færslu (v3)*  og  *Sækja færslu (v3)*), gæti hún birt villu sem er  Power Automate  svipuð þessari:

`The response from the Business Central service is too large`

### <a name="possible-cause-1"></a>Möguleg orsök

Jafnvel þó að Viðskiptamiðlæg hafi engin takmörk á stærð færslna sem skilað er  Dynamics 365 Business Central  af API getur tengitengið  Power Automate  aðeins unnið allt að 8 MB.

Allir Viðskiptamiðað er með Microsoft skilafærslur undir þessum mörkum en það er ekki hægt að veita samstarfsaðilum. Ef þú sérð villu "svarið frá Aðalþjónustunni er of stórt", Hafðu samband við samstarfsaðila sem stofnaði API sem þú ert að nota.

## <a name="entity-set-not-found-error"></a>Villan „Einingasamstæða finnst ekki“

### <a name="problem-2"></a>Vandamál

Þegar nýtt Power Automate flæði er búið til með því að nota [!INCLUDE[prod_short](includes/prod_short.md)] samþykkisræsingu, eins og *Þegar beðið er um samþykki innkaupaskjals* gætu komið upp villuboð svipuð og þessi:

`Entity set not found: \<name\>`

Staðgengillinn, `\<name\>`, er þjónustuheiti vefþjónustunnar sem vantar, t.d. *workflowWebhookSubscriptions* eða *workflowPurchaseDocumentLines*.

### <a name="possible-cause-2"></a>Möguleg orsök

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
