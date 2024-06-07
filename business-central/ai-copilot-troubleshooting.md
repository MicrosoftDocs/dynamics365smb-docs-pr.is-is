---
title: Úrræðaleit vegna stjórnunargetu og ÓM
description: Kynntu þér hvernig laga má algeng vandamál sem þú gætir fundið með Copilot og AI getu í Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.collection:
  - bap-ai-copilot
ms.date: 02/01/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="troubleshoot-copilot-and-ai-capabilities"></a>Úrræðaleit vegna stjórnunargetu og ÓM

Copilot er Ónýt virkni í Business Central sem aðstoðar við ýmis verk eins og að draga markaðssetningartexta og stemma af bankareikninga. Ef þú átt í vandræðum með Copilot eða aðra afkastagetu getur þessi grein hjálpað þér að finna og laga sameiginleg vandamál.

## <a name="copilot-doesnt-appear-on-pages"></a>Copilot birtist ekki á síðum

Ef Copilot-aðgerðir, svo sem **Drög að aðgerðinni Copilot, fyrir markaðssetningartextatillögur** eða **Stemma af aðgerðina Copilot** fyrir afstemmingu bankareikninga, birtist ekki á síðu eins og væntanlegt er athugað eftirfarandi:

- Ef aðgerðinni er stýrt undir Eiginleikastjórnun þarf að ganga úr skugga um að hún sé virk. [Fræðast meira um aðgerðastjórnun](admin-feature-management.md).

- Ganga þarf úr skugga um að eiginleikinn sé ekki falinn með sérstillingu. [Fræðast meira um sérstillingu](ui-personalization-user.md).

## <a name="copilot-appears-on-pages-but-you-get-an-error-that-its-not-activated"></a>Copilot birtist á síðum en villa kemur upp að hún sé ekki virkjuð

Þegar reynt er að nota Copilot og villa svipuð **því miður er Copilot ekki virkt fyrir \[eiginleika\]**, þá eru nokkur atriði til að athuga:

- Fyrst skal ganga úr skugga um að eiginleikinn sé virkjaður á síðunni **Copilot & AI** . [Fá nánari upplýsingar um virkjun copilot og ÓM](enable-ai.md#activate-features). 
- Næst skal ganga úr skugga um að yfirlýsing um persónuvernd fyrir Azure OpenAI samþættingu sé ekki stillt á **Ósamræmt fyrir alla**. Ef svo er, breyttu því í **Sammála fyrir alla**. [Fá nánari upplýsingar um persónuvernd](privacy-notices-status.md).

## <a name="copilot-capabilities-from-microsoft-not-listed-on-copilot--ai-capabilities-page"></a>Copilot getu frá Microsoft sem ekki er tilgreind á síðunni Copilot & AI Getu

Ef enginn af eiginleikum **Microsoft er sýndur á síðunni** Copilot &AI er líklegt að eitt eða fleiri forrit séu uppsett í umhverfi þínu. Innfelld forrit geta boðið upp á eigin Copilot-möguleika en geta sem Gefin er út af Microsoft samhæfir ekki umhverfi með innfelldum forritum.

## <a name="see-also"></a>Sjá einnig .

[Grunnstilla Copilot- og gervigreindarmöguleika](enable-ai.md)  
[Markaðssetningatextatillögur með Copilot](ai-overview.md)  
[Afstemma bankareikninga með Copilot](bank-reconciliation-with-copilot.md)  
