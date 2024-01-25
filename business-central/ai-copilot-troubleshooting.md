---
title: Úrræðaleit af Copilot og AI getu
description: Lærðu hvernig á að laga algeng vandamál sem þú gætir lent í þegar þú vinnur með Copilot og gervigreindargetu í Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.collection:
  - bap-ai-copilot
ms.date: 11/15/2023
ms.custom: bap-template
---
# <a name="troubleshoot-copilot-and-ai-capabilities"></a>Úrræðaleit af Copilot og AI getu

Copilot er gervigreindarvirkni í Business Central sem aðstoðar við ýmis verkefni eins og að semja markaðstexta og samræma bankareikninga. Ef þú lendir í vandræðum með Copilot eða aðra gervigreindargetu getur þessi grein hjálpað þér að bera kennsl á og laga algeng vandamál.

## <a name="copilot-doesnt-appear-on-pages"></a>Copilot birtist ekki á síðum

Ef Copilot virkni, svo sem **Drög með Copilot** aðgerð fyrir markaðstextatillögur eða **Samræma við Copilot** aðgerð fyrir aðstoð við afstemmingu bankareiknings, birtist ekki á síðu eins og búist var við, athugaðu eftirfarandi:

- Ef eiginleikanum er stjórnað undir Eiginleikastjórnun, vertu viss um að hann sé virkur. [Lærðu meira um eiginleikastjórnun](admin-feature-management.md).

- Gakktu úr skugga um að virknin sé ekki falin með sérstillingu. [Lærðu meira um sérstillingar](ui-personalization-user.md).

## <a name="copilot-appears-on-pages-but-you-get-an-error-that-its-not-activated"></a>Copilot birtist á síðum, en þú færð villu um að það sé ekki virkt

Þegar þú reynir að nota Copilot og þú færð villu svipað og **Því miður er Copilot ekki virkjaður fyrir \[eiginleika\]**, þá eru nokkur atriði sem þarf að athuga :

- Fyrst skaltu ganga úr skugga um að eiginleikinn sé virkur á **Copilot & AI getu** síða. [Lærðu meira um að virkja Copilot og gervigreindargetu](enable-ai.md#activate-features). 
- Næst skaltu ganga úr skugga um að yfirlýsing um persónuvernd fyrir Azure OpenAI samþættingu sé ekki stillt á **Ósammála fyrir alla**. Ef svo er, breyttu því í **Sammála fyrir alla**. [Frekari upplýsingar um persónuverndartilkynningar](privacy-notices-status.md).

## <a name="see-also"></a>Sjá einnig .

[Grunnstilla Copilot- og gervigreindarmöguleika](enable-ai.md)  
[Tillögur um markaðstexta með Copilot](ai-overview.md)  
[Samræma bankareikninga við Copilot](bank-reconciliation-with-copilot.md)  
