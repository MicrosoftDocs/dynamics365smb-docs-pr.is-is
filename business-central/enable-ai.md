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
ms.collection:
  - bap-ai-copilot
---

# Grunnstilling copilot og AI-möguleika 

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Þessi grein útskýrir hvernig á að stjórna Copilot og öðrum afkastagetu AI í Business Central. Þetta er gert af stjórnanda. Copilot er kerfisaðgerð og óaðgreindur hluti Af Business Central. Svipað og með flesta kerfisaðgerði veitir notandi hvorki aðgang að einstökum notendum né vísbendingum um eða slökkt á copilot. Hins vegar býður Copilot upp á eftirlit með gögnum og getur slökkva á einstökum möguleikum Copilot og AI fyrir hvert umhverfi. Mismunandi aðgangsstýringarstig eru til staðar fyrir Óháð getu, eftir því hver eiginleikinn er:

- Leyfa hreyfingu gagna á landsvæðum

  Þetta verk er aðeins krafist ef Business Central umhverfið þitt er í annarri landfræði en Azure OpenAI þjónustan sem hún notar. [Læra meira](#allow-data-movement-across-geographies)

- Virkja eiginleikann á síðunni **Copilot & AI Getu** . [Læra meira](#activate-features)

- Virkja tiltekna eiginleika ef hún er enn stjórnað af **eiginleikastjórnun**.

  Í 2023 gefa út bylgju 2 eru bæði tillögur um markaðssetningartexta og aðstoð við afstemmingu bankareikninga undir **Eiginleikastjórnun**. [Læra meira](#enable-feature-in-feature-management)

Ef einhver þessara þarfa er ekki uppfyllt er aðgerðin ekki tiltæk til notkunar.

## Frumskilyrði

- Þú notar Business Central á netinu, útgáfa 23.1 eða síðar. <!--[preview version](ai-preview-getstarted.md) of Business Central that's enabled for Copilot.-->
- Þú ert með admin eða yfirheimildir í Business Central.  <!--For more information, go to [Configure AI-powered item marketing text with Copilot](enable-ai.md).-->

## Leyfa hreyfingu gagna á landsvæðum

Þetta verk á aðeins við ef **rofi gagnahreyfingar** birtist efst á síðunni **Copilot & AI.**  Ef tengillinn **Hvernig stjórna ég gögnum um afritun mína?** er sýnt í staðinn fyrir rofann **Leyfa gagnahreyfingar** er þessu skrefi sleppt.

![Sýnir skjáskot af rofa gagnahreyfingar á síðunni Copilot & AI Getu.](media/allow-data-movement-v2.png)

Rofinn **Leyfa gagnahreyfingar** gefur til kynna að staðsetning&mdash; Business Central umhverfisins sem er, landafræðin þar sem gögn eru unnin og geymd&mdash; er ekki sú sama og Azure OpenAI Service landafræðin sem Copilot notar. Ef þú vilt virkja Copilot verður að leyfa hreyfingu gagna milli landa. Til að fræðast meira um hreyfingu gagna er farið í [Copilot-gagnahreyfingu yfir landfræðilegar](ai-copilot-data-movement.md) upplýsingar. 

Til að leyfa gagnahreyfingar utan landsvæðisins skal ljúka eftirfarandi skrefum:

1. Í Business Central er leitað að og opna síðuna **Copilot & AI Getu** .
1. Kveikja á rofanum **Leyfa gagnahreyfingar** .

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

Allir stjórnunarmöguleikar og AI-eiginleikar eru sjálfgefið virkir þegar þeir eru tiltækir í forskoðun eða verða almennt tiltækir. Með því að nota síðuna **Copilot & AI Getu** er hægt að slökkva á einstökum eiginleikum eða aftur fyrir alla notendur.

1. Í Business Central er leitað að og opna síðuna **Copilot & AI Getu** .

1. Síðan birtir lista yfir allar tiltækar copilot- og AI-tengdar aðgerðir og núverandi stöðu þeirra, sem geta verið virkar eða óvirkar. Eiginleikunum er skipt í tvo hluta eins hluta&mdash; fyrir aðgerðir í forskoðun og aðra fyrir aðgerðir sem eru almennt tiltækar. 

   [![Sýnir mitt hlutverk Business Central og gátlistann fyrir Copilot](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

   - Til að kveikja á aðgerð skal velja hana á listanum og velja svo aðgerðina **Virkja** .
   - Til að slökkva á aðgerð skal velja hana og velja **svo Óvirkja** aðgerð. 


## Gera eiginleika virka í eiginleikastjórnun

Þegar einstakar copilot-uppfærslur eru gefnar út í minniháttar uppfærslum Business Central er þessi möguleiki valfrjáls fram að næstu stóru uppfærslu. **Aðgerðastjórnun** er notuð til að kveikja eða slökkva á eiginleikum sem eru í forskoðun, eins og bankaafstemmingu og nokkrar aðgerðir sem eru almennt tiltækar, eins og tillögur um markaðssetningartexta. [Fræðast meira um aðgerðastjórnun](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. Í Business Central skal leita að og opna síðuna **Eiginleikastjórnun** .
2. Til að virkja eiginleika er dálkurinn **Virkt fyrir** alla notendur stilltur á **Alla notendur**. Til að gera aðgerð óvirka er virkt fyrir **dálkinn Ekkert stillt** á **Ekkert**. Eftirfarandi tafla er notuð til að hjálpa til við að ákvarða rofa sem gildir um Copilot og AO möguleikann sem á að virkja:

   - **Forskoðun aðgerðar: Afstemming bankareikninga og stjórntæki** tengist aðgerðinni afstemming bankareikninga.
   - **Forskoðun eiginleika: Búa til Ónýtar vörulýsingar með Copilot** fyrir eiginleikann textatillögur markaðssetningar.

   Nánari upplýsingar um eiginleikastjórnun eru almennt notaðar [í Eiginleikastjórnun](/dynamics365/business-central/dev-itpro/administration/feature-management).

## Aðgangur að notanda veittur 

Copilot og AI geta boðið virkni sem ætluð er öllum notendum innan fyrirtækisins eða fyrir tiltekin notendahlutverk. Flestir copilot og AI geta bjóða aðgangsstýringu með því að nota heimildir og heimildasafn í heimildastjórnunarkerfi Business Central. [Fá nánari upplýsingar um heimildir og heimildasafn](ui-define-granular-permissions.md).

Ef veita á eða neita aðgangi að tilteknum afkastagetu Copilot og AI er leitað ráða hjá heimildum eða útgefanda þeirrar aðgerðar til að bera kennsl á hvaða heimilda er þörf. 

## Næstu skref

Þegar þú hefur virkjað og veitt samþykki fyrir aðgerðunum er þú tilbúinn að prófa þær. Farðu til:

- [Bæta markaðssetningartexta við vörur](item-marketing-text.md) 
- [Stemma af með aðstoð afstemmingar bankareiknings](bank-reconciliation-with-copilot.md) 

## Sjá einnig .

[Villuleita Copilot- og gervigreindarmöguleika](ai-copilot-troubleshooting.md)  
[Yfirlit yfir markaðssetningartextatillögur](ai-overview.md)   
[Algengar spurningar um tillögur að markaðstexta](faqs-marketing-text.md)  
