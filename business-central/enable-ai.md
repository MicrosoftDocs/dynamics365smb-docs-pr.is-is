---
title: Skilgreina markaðstexta með AI-tilbúinni vöru (Forskoðun) með Copilot
description: Í þessari grein er útskýrt hvernig á að fá Copilot Trial Version af Business Central og virkja Copilot á umhverfi.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# Skilgreina markaðstexta með AI-tilbúinni vöru (Forskoðun) með Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Í greininni er útskýrt hvernig hægt er að stýra möguleikum til að búa til markaðseftirlit með AI-vara með Copilot fyrir fyrirtækið. Þetta verk er unnið af admin. Það eru tvær kröfur sem þarf að uppfylla til að gera aðgerðina tiltæka fyrir notendur:

- Gera kleift að  **Stofna vörulýsingar með Copilot** .
- Samþykkis á skilmálum og skilyrðum  [forskoðunar](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/)  og  [yfirlýsingar](https://go.microsoft.com/fwlink/?LinkId=521839)  Microsoft um persónuvernd fyrir hönd samtakanna.

Ef annarri hvorri þessara þarfa er ekki fullnægt verður aðgerðin ekki tiltæk.

## Frumskilyrði

Þú notar  [forskoðunarútgáfu](ai-preview-getstarted.md)  af Business Central sem er virkjaður fyrir Copilot. Virkjun Copilot er unnin af admin. Frekari upplýsingar er að fara í til að  [samskipa texta fyrir MARKAÐSSETNINGU AI-vara með Copilot](enable-ai.md).

## Gera stofnaðar vörulýsingar fyrir virka eða óvirka með Copilot

1. Í Viðskiptamiðnum er að leita að og opna  **síðuna Feature Management** .
2.  **Stilla aðgerðina fyrir**  **Forskoðun eiginleikann aðgerðir: stofna skal forknúinna vörulýsingar með copilot**  til  **allra notenda**  til að virkja eiginleikann eða  **ekkert**  til að gera hann óvirkan.

   Nánari upplýsingar um aðgangsstýringu Almennt er að fara í  [aðgangsstjórnun](/dynamics365/business-central/dev-itpro/administration/feature-management).

## Samþykki til eða hafnar forskráningu og friðlýsingarskilmálum og skilyrðum fyrir því að allir notendur

1. Í Viðskiptamiðstöðer að leita að og opna  **stöðusíðu**  persónuverndartilkynninga.
2.  **Í dálkinum Samþætting heiti**  velurðu  **Azure openai** og Les svo skilmálana sem kynntir eru þér.
3.  **Í Azure OpenAI**  röðinni er verið að  **Velja Samþykkja fyrir alla**  gátreit til samþykkis eða  **ósammála fyrir alla**  gátreit til að hafna.

## Næstu skref

Eftir að aðgerðin er gerð virk og samþykkt er hægt að prófa Copilot á vörum í Viðskiptamiðinu. Fara í að  [Bæta markaðstexta við vörur](item-marketing-text.md).  

## Sjá einnig .

[Yfirlit um markaðssetningu á AI-knúinn vöru með Copilot](ai-overview.md)  
[Stofna markaðstexta fyrir vörur með Copilot](item-marketing-text.md)  
[Textahöfundur Markaðsupplýsingar með Copilot-FAQ vöru](ai-faq.md)  
