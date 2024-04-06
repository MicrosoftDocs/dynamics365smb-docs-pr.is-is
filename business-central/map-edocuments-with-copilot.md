---
title: Varpa e-skjölum í innkaupapöntunarlínur með afrita
description: Fræðast um notkun Copilot til að varpa e-skjölum í innkaupapöntunarlínur.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: altotovi
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 02/23/2024
ms.custom: bap-template
---

# <a name="map-e-documents-to-purchase-order-lines-with-copilot-preview"></a>Varpa e-skjölum í innkaupapöntunarlínur með Copilot (forskoðun)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Þegar innkaupaferli verða stafrænni gegnir e-skjöl aðgerðin Business Central lykilhlutverki í því að gera móttöku og vinnslu lánardrottins sjálfvirka. Copilot getur aðstoðað við þetta ferli með því að bæta vörpun og samsvörun reikninga lánardrottna á innkaupapantanir. Þetta styttir tímafrek verk sem myndu venjulega fela í sér umfangsmikla leit, uppflettingu og gagnafærslu. Kosturinn er samsettur af þeirri staðreynd að reikningar lánardrottna tengjast oft ekki nákvæmlega innkaupapöntunum, í hvaða tilviki Copilot er betur staðsett til að auðkenna samsvarandi innkaupapantanir. Aukin samsvörunargeta gagnast sérstaklega litlum og miðstýrðum fyrirtækjum sem þurfa skilvirka rakningu skjala fyrir innkaupapantanalínur. Copilot er aðstoðarmaður sem eykur sköpunarkraft og bætir framleiðni Hjá Business Central notendum.

> [!IMPORTANT]
> - Þetta er aðgerðin Production Ready Preview fyrir framleiðslu- og sandkassaumhverfi í hvaða landi sem er, að undanskildum Kanada.
> - Forskoðun framleiðslu tilbúnar er háð viðbótarnotkunarskilmálum. Nánari upplýsingar: [Viðbótarnotkunarskilmálar fyrir Dynamics 365 forskoðun](https://go.microsoft.com/fwlink/?linkid=2105274)
> - Ónýtt efni getur verið rangt.

Í upphaflegri útgáfu forritsins **e-skjals** kynntum við grundvallaratvik fyrir tölvupóstskjöl fyrir allt söluferlið. Hins vegar er þörf á viðbótum og sjálfvirkni við að meðhöndla móttekin skjöl, sérstaklega í samhengi við innkaupaferli. Copilot skilgreinir hvernig stjórnað er tölvupóstskjölum í innkaupaferlinu, sérstaklega hvað varðar innkaupapantanir. Með ramma tölvupóstskjala er hægt að tilgreina tegund innkaupaskjals sem stofna skal fyrir hvern lánardrottinn þegar tölvupóstur berst frá þeim. Áður var eini valkosturinn að stofna innkaupareikning, annaðhvort sem fylgiskjal eða fjárhagsbók.

Nú er hægt að uppfæra fyrirliggjandi innkaupapöntun í Business Central með þeim upplýsingum sem berast í tölvupósti.

<!--
> [!NOTE]
> - This feature is available as a production-ready preview for production and sandbox environments in any country localization, with the exception of Canada. Production-ready previews are subject to supplemental terms of use. For more information, see [Supplemental terms of use for Dynamics 365 preview](https://go.microsoft.com/fwlink/?linkid=2105274).
> - AI-generated content may be incorrect.-->


## <a name="identify-purchase-orders"></a>Auðkenna innkaupapantanir

Fyrst er hægt að auðkenna innkaupapantanirnar sem hægt er að jafna sjálfkrafa.

## <a name="map-lines"></a>Varpa línum

Copilot auðveldar samsvörun e-reikningslína sjálfvirkt við innkaupapantanalínur og býður upp á auka samsvörunarupplýsingar til að bæta samsvörunina.

Eftir að þær hafa verið jafnaðar og varpaðar uppfærir Business Central samsvarandi innkaupapöntun með viðeigandi móttökuupplýsingum til að tryggja að rétt magn berist í pöntunarlínurnar.

## <a name="see-also"></a>Sjá einnig .

[Yfirlit yfir rafræn skjöl](finance-edocuments-overview.md)  
[Nota rafræn skjöl við sölu og innkaup](finance-how-use-edocuments.md)  
[Villuleita Copilot- og gervigreindarmöguleika](ai-copilot-troubleshooting.md)  
[Algengar spurningar um bankaafstemmingu](faqs-bank-reconciliation.md)  
