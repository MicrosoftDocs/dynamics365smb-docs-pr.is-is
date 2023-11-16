---
title: Grunnstilling copilot og AI-möguleika
description: Þessi grein útskýrir hvernig á að virkja Copilot í umhverfi.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 10/29/2023
ms.custom: bap-template
ms.search.form: 7775
---

# Grunnstilling copilot og AI-möguleika 

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Þessi grein útskýrir hvernig stjórna skal aðgangi notenda að Copilot og öðrum afkastagetu notenda í Business Central. Þetta er gert af stjórnanda. Það eru þrjú stig aðgangsstýringar fyrir Copolit og ÓM, eftir því hver eiginleikinn er:

- Samþykki til Azure OpenAI [forskoðunar](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) og [persónuverndarskilmála](https://go.microsoft.com/fwlink/?LinkId=521839) og skilyrða.

   Þetta samþykki er nauðsynlegt fyrir alla stjórnborða eða afkastagetu til að vinna fyrir notendur. Samþykkið er altækt fyrir alla notendur og á við um alla eiginleika Copilot og AI. [Læra meira](#consent-to-preview-and-privacy-terms)

- Leyfa hreyfingu gagna á landsvæðum

  Þetta verk er aðeins krafist ef Business Central umhverfið þitt er í annarri landfræði en Azure OpenAI þjónustan sem hún notar. [Læra meira](#allow-data-movement-across-geographies)

- Virkja tiltekna eiginleika ef hún er enn stjórnað af **eiginleikastjórnun**.

  Í 2023 gefa út bylgju 2 eru bæði tillögur um markaðssetningartexta og aðstoð við afstemmingu bankareikninga undir **Eiginleikastjórnun**. Hins vegar er tillögur um markaðssetningartexta sjálfgefið virkar. [Læra meira](#enable-feature-in-feature-management)

- Virkja eiginleikann á síðunni **Copilot & AI Getu** . [Læra meira](#activate-features)

Ef einhver þessara þarfa er ekki uppfyllt er aðgerðin ekki tiltæk til notkunar.

## Frumskilyrði

- Þú notar Business Central á netinu, útgáfa 23.1 eða síðar. <!--[preview version](ai-preview-getstarted.md) of Business Central that's enabled for Copilot.-->
- Þú ert með admin eða yfirheimildir í Business Central.  <!--For more information, go to [Configure AI-powered item marketing text with Copilot](enable-ai.md).-->

## Samþykki fyrir forskoðun og skilmálum um persónuvernd

Samþykki samkvæmt forskoðunarskilmálum [og](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) [yfirlýsingu](https://go.microsoft.com/fwlink/?LinkId=521839) Microsoft um persónuvernd fyrir hönd fyrirtækisins. Ólíkt persónuverndartilkynningum fyrir aðra eiginleika og þjónustu geta aðeins admins samþykkt notkun Azure OpenAI, sem þeir gera fyrir hönd fyrirtækisins. Notendur geta ekki sjálfir ákveðið sig.   

1. Í Business Central er leitað að og opna síðuna **Staða** persónuverndartilkynninga.
2. Í dálknum **Heiti** samþættingar skal velja **Azure OpenAI** og lesa síðan skilmálana sem birtast notandanum.
3.  **Í Azure OpenAI** línunni skal velja **Samkomulag um að allir** gátreiti til samþykkis eða **Afplánun fyrir alla** gátreiti til að hafna.

## Gera eiginleika virka í eiginleikastjórnun

**Aðgerðastjórnun** er notuð til að kveikja eða slökkva á eiginleikum sem eru í forskoðun, eins og bankaafstemmingu og nokkrar aðgerðir sem eru yfirleitt tiltækar, eins og markaðssetningartillaga vöru. [Fræðast meira um aðgerðastjórnun](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. Í Business Central skal leita að og opna síðuna **Eiginleikastjórnun** .
2. Til að virkja eiginleika er dálkurinn **Virkt fyrir** alla notendur stilltur á **Alla notendur**. Til að gera aðgerð óvirka er virkt fyrir **dálkinn Ekkert stillt** á **Ekkert**. Eftirfarandi tafla er notuð til að hjálpa til við að ákvarða rofa sem gildir um Copilot og AO möguleikann sem á að virkja:

   - **Forskoðun aðgerðar: Afstemming bankareikninga og stjórntæki** tengist aðgerðinni afstemming bankareikninga.
   - **Forskoðun eiginleika: Búa til Ónýtar vörulýsingar með Copilot** fyrir eiginleikann textatillögur markaðssetningar.

   Nánari upplýsingar um eiginleikastjórnun eru almennt notaðar [í Eiginleikastjórnun](/dynamics365/business-central/dev-itpro/administration/feature-management).

## Leyfa hreyfingu gagna á landsvæðum

Þetta verk á aðeins við ef **rofi gagnahreyfingar** birtist efst á síðunni **Copilot & AI.**  Rofinn  **Leyfa gagnahreyfingar** gefur til kynna að staðsetning&mdash; Business Central umhverfisins sem er, landafræðin þar sem gögn eru unnin og geymd&mdash; er ekki sú sama og Azure OpenAI Service landafræðin sem Copilot notar. Ef þú vilt virkja Copilot verður að leyfa hreyfingu gagna milli landa. Til að fræðast meira um hreyfingu gagna er farið í [Copilot-gagnahreyfingu yfir landfræðilegar](ai-copilot-data-movement.md) upplýsingar. 

Til að leyfa gagnahreyfingar utan landsvæðisins skal ljúka eftirfarandi skrefum:

1. Í Business Central er leitað að og opna síðuna **Copilot & AI Getu** .
1. Kveikja á rofanum **Leyfa gagnahreyfingar** .

   ![![Alt texti](allow-data-movement.png)](allow-data-movement.png)

Hægt er að velja með því að slökkva á rofanum  **Leyfa gagnahreyfingar** . Þegar Azure OpenAI þjónusta verður tiltæk í landafræði Business Central er umhverfið þitt sjálfkrafa tengt við það og rofinn er ekki lengur tiltækur. 


<!--
| Australia, United Kingdom, United States | Within the respective geographical region |
| Europe, France, Germany, Norway, Switzerland  | Sweden or Switzerland |
| Asia Pacific, Brazil, Canada, India, Japan, Singapore, South Africa, South Korea, United Arab Emirates  | United States |-->



<!--Note

If your environment is hosted in North America, Copilot will use an Azure OpenAI endpoint in North America to process your data.
If your environment is hosted in Europe, Copilot will use an Azure OpenAI endpoint in Europe to process your data.
If your environment is hosted anywhere else, Copilot will use an Azure OpenAI endpoint outside of the region in which the environment is hosted.
To opt in 

Copilot and other AI capabilities use Azure OpenAI Service.  and are provided by default to only those customers with environments that have United States as their geography for data processing and storage. While the Azure OpenAI Service is available in multiple geographies including Australia, Canada, United States, France, Japan and UK, Copilot does not follow the same regional rollout schedule.

Meanwhile, customers with environments outside the United States can use Copilot AI features by opting in to share relevant data with the Azure OpenAI Service in United States or Switzerland.

The information in the following table outlines the Azure OpenAI service that's used by the Copilot services based on the geography of their Dynamics 365 environment when they opt-in to share data.-->
## Virkja eiginleika

Með því að nota síðuna **Copilot & AI Getu** er hægt að kveikja eða slökkva á einstökum eiginleikum fyrir alla notendur.

1. Í Business Central er leitað að og opna síðuna **Copilot & AI Getu** .

1. Síðan birtir lista yfir allar tiltækar copilot- og AI-tengdar aðgerðir og núverandi stöðu þeirra, sem geta verið virkar eða óvirkar. Eiginleikunum er skipt í tvo hluta eins hluta&mdash; fyrir aðgerðir í forskoðun og aðra fyrir aðgerðir sem eru almennt tiltækar. 

   [![Sýnir mitt hlutverk Business Central og gátlistann fyrir Copilot](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

   - Til að kveikja á eiginleika skal velja hana á listanum og velja **svo Virkja** í borðanum.
   - Til að slökkva á aðgerð skal velja hann og velja **svo Óvirkja** í borðanum. 


## Næstu skref

Þegar þú hefur virkjað og veitt samþykki fyrir aðgerðunum er þú tilbúinn að prófa þær. Farðu til:

- [Bæta markaðssetningartexta við vörur](item-marketing-text.md) 
- [Stemma af með aðstoð afstemmingar bankareiknings](bank-reconciliation-with-copilot.md) 

## Sjá einnig .

[Yfirlit yfir markaðssetningartextatillögur](ai-overview.md)   
[FAQ fyrir markaðssetningartextatillögur](faqs-marketing-text.md)  
