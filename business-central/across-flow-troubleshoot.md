---
title: Úrræðaleit vegna sjálfvirkra verkflæða
description: Lærðu hvernig á að leysa tenginguna á milli Viðskiptamiðseðla og Power Automate þegar búið er að byggja sjálfvirkt verkflæði.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585919"
---
# <a name="troubleshoot-your-prod_short-automated-workflows"></a>[!INCLUDE[prod_short](includes/prod_short.md)] Úrræðaleit vegna sjálfvirkra verkflæða

Þegar tengst [!INCLUDE [prod_short](includes/prod_short.md)] er við Power Automate Stofna sjálfvirka verkflæði er hugsanlegt að keyra villuskilaboð. Í greininni eru lagðar til tillögur til lausnar á endurteknum vandamálum.

## <a name="flow-doesnt-run-on-all-records-created-or-changed"></a>Flæði keyrir ekki á öllum færslum sem stofnaðar eru eða breyttar

### <a name="problem"></a>Vandamál

Ef atburður stofnar eða breytir lotu færslna keyrir flæðið ekki á sumar-eða allar færslur.

### <a name="possible-cause"></a>Möguleg orsök

Eins og er, þá eru takmörk á hversu margar skráningar flæði getur unnið. Ef fleiri en 100 færslur eru búnar til eða þeim breytt innan 30 sekúndna þá fer flæðið ekki af stað.

> [!NOTE]
> Fyrir hönnuði er flæðikveikjun gerð í gegnum tilkynningar vefkrókur og þessi takmörkun er til komin vegna þess hvernig Business Central Connector annast `collection` tilkynningar. [Frekari upplýsingar í vinnu með Vefkróka í Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) í Hjálp fyrir hönnuði og stjórnun.

## <a name="entity-set-not-found-error"></a>"Einingarmengi fannst ekki" Villa

### <a name="problem"></a>Vandamál

Þegar nýtt Power Automate flæði er stofnað með [!INCLUDE[prod_short](includes/prod_short.md)] samþykktarkveikju, svo sem *þegar beðið* er um samþykki innkaupaskjals, gætu villuskilaboð orðið svipuð þessari:

`Entity set not found: \<name\>`

Frátakandi, `\<name\>`,, er þjónustuheiti vefþjónustunnar sem vantar, *til dæmis workflowwebhookáskriftir* eða *workflowkaupthing sedocumentlines*.

### <a name="possible-cause"></a>Möguleg orsök

Með því að nota Power Automate fyrir samþykki þurfa tilteknar síðu-og Codeunit-hlutir að vera gefnir út sem vefþjónustur. Sjálfgefið er að flestir hlutir sem eru nauðsynlegir eru gefnir út sem vefþjónustur. En í sumum tilfellum kann umhverfið þitt að hafa verið sérsniðið þannig að þessir hlutir eru ekki lengur gefnir út.

### <a name="fix"></a>Laga

Farðu á **síðuna vefþjónusta** og Gakktu úr skugga um að eftirfarandi hlutir séu gefnir upp sem vefþjónustur. Það ætti að vera færsla í listanum fyrir hvern hlut með gátreitinn **Birt** valinn.  

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

Frekari upplýsingar um útgáfu vefþjónustu á [Útgáfuvef vefþjónustu](across-how-publish-web-service.md).

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun kl [Microsoft Learn](/learn/modules/use-power-automate/).

## <a name="see-also"></a>Sjá einnig .

[Nota Power Automate rennur í[!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)  
[Verkflæði](across-workflow.md)  
[Setja upp sjálfvirk verkflæði](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Rofi á Skyndistreymi](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  
[Stjórna Power Automate streymi](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
