---
title: Grunnstilling copilot og AI-möguleika
description: Þessi grein útskýrir hvernig á að virkja Copilot í umhverfi.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 04/16/2024
ms.custom: bap-template
ms.search.form: 7775
ms.collection:
  - bap-ai-copilot
---

# Grunnstilling copilot og AI-möguleika 

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Þessi grein útskýrir hvernig á að stjórna Copilot og öðrum afkastagetu AI í Business Central. Þetta er gert af stjórnanda. Copilot er kerfisaðgerð og óaðgreindur hluti Af Business Central. Svipað og með flesta kerfisaðgerði veitir notandi hvorki aðgang að einstökum notendum né vísbendingum um eða slökkt á copilot. Hins vegar býður Copilot upp á eftirlit með gögnum og getur slökkva á einstökum möguleikum Copilot og AI fyrir hvert umhverfi. Mismunandi aðgangsstýringarstig eru til staðar fyrir Óháð getu, eftir því hver eiginleikinn er:

- Leyfa hreyfingu gagna á landsvæðum.

  Þetta verk er aðeins krafist ef Business Central umhverfið þitt er í annarri landfræði en Azure OpenAI þjónustan sem hún notar. [Læra meira](#allow-data-movement-across-geographies)

- Virkja eiginleikann á síðunni **Copilot & AI Getu** . [Læra meira](#activate-features)

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
- Enable the specific feature if it's governed by **Feature Management**.

  Check whether  of 2024 release wave 1, chat with Copilot, marketing text suggestions, and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)
<!-- 
- Enable the specific feature, if it's still governed by **Feature Management**.

  In 2023 release wave 2, both the marketing text suggestions and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)-->

Ef einhver þessara þarfa er ekki uppfyllt er aðgerðin ekki tiltæk til notkunar.

## Frumskilyrði

- Þú notar Business Central á netinu.
- Ūú ert stjķrnandi [í](#requirements-for-being-an-administrator) Business Central.

## Leyfa hreyfingu gagna á landsvæðum

Þetta verk á aðeins við ef **rofi gagnahreyfingar** birtist efst á síðunni **Copilot & AI.**  Ef tengillinn **Hvernig stjórna ég gögnum um afritun mína?** er sýnt í staðinn fyrir rofann **Leyfa gagnahreyfingar** er þessu skrefi sleppt.

![Sýnir skjáskot af rofa gagnahreyfingar á síðunni Copilot & AI Getu.](media/allow-data-movement-v2.png)

Rofinn **Leyfa gagnahreyfingar** gefur til kynna að staðsetning&mdash; Business Central umhverfisins sem er, landafræðin þar sem gögn eru unnin og geymd&mdash; er ekki sú sama og Azure OpenAI Service landafræðin sem Copilot notar. Ef þú vilt virkja Copilot verður að leyfa hreyfingu gagna milli landa. Til að fræðast meira um hreyfingu gagna er farið í [Copilot-gagnahreyfingu yfir landfræðilegar](ai-copilot-data-movement.md) upplýsingar. 

Til að leyfa gagnahreyfingar utan landsvæðisins skal ljúka eftirfarandi skrefum:

1. Í Business Central er leitað að og opna síðuna **Copilot & AI Getu** .
1. Kveikja á rofanum **Leyfa gagnahreyfingar** .

   Rofi **Leyfa gagnahreyfingar** er sjálfgefið virkur fyrir umhverfi í Vestur-Evrópu og Norður-Evrópu Azure-svæðum.

Hægt er að afþakka gagnahreyfingar með því að slökkva á rofanum **Leyfa gagnahreyfingar** . Þegar Azure OpenAI þjónusta verður tiltæk í landafræði Business Central er umhverfið þitt sjálfkrafa tengt við það og rofinn er ekki lengur tiltækur.

<!-- Don't review
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

Allir afkastagetu copilot og AI eru sjálfgefið virkir þegar þeir eru tiltækir í forskoðun eða verða almennt tiltækir. Með því að nota síðuna **Copilot & AI Getu** er hægt að slökkva á einstökum eiginleikum eða aftur fyrir alla notendur.

1. Í Business Central er leitað að og opna síðuna **Copilot & AI Getu** .

1. Síðan birtir lista yfir allar tiltækar copilot- og AI-tengdar aðgerðir og núverandi stöðu þeirra, sem geta verið virkar eða óvirkar. Eiginleikunum er skipt í tvo hluta eins hluta&mdash; fyrir aðgerðir í forskoðun og aðra fyrir aðgerðir sem eru almennt tiltækar. 

   [![Sýnir mitt hlutverk Business Central og gátlistann fyrir Copilot](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

   - Til að kveikja á aðgerð skal velja hana á listanum og velja svo aðgerðina **Virkja** .
   - Til að slökkva á aðgerð skal velja hana og velja **svo Óvirkja** aðgerð. 

<!-- don't review 

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
## Enable feature in Feature Management

When individual Copilot capabilities are released in Business Central minor updates, these capabilities are optional until the next major update. **Feature Management** is used to turn on or off features that are in preview, like bank reconciliation, and some features that are generally available, like marketing text suggestions. [Learn more about feature management](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. In Business Central, search for and open the **Feature Management** page.
2. To enable a feature, set the **Enabled for** column to **All users**. To disable a feature, set the **Enabled for** column to **None**. Use the following table to help you determine the switch that applies to the Copilot and AI capability you want to enable:

   - **Feature Preview: Bank account reconciliation with Copilot** enables the bank account reconciliation assist feature.
   - **Feature Preview: Chat with Copilot** enables the chat with Copilot feature.
   - **Feature preview: Create AI-powered product descriptions with Copilot** enables the marketing text suggestions feature.

   For more information about feature management in general, go to [Feature Management](/dynamics365/business-central/dev-itpro/administration/feature-management).-->

## Aðgangur að notanda veittur

Copilot og AI geta boðið virkni sem ætluð er öllum notendum innan fyrirtækisins eða fyrir tiltekin notendahlutverk. Flestir copilot og AI geta bjóða aðgangsstýringu með því að nota heimildir og heimildasafn í heimildastjórnunarkerfi Business Central. [Fá nánari upplýsingar um heimildir og heimildasafn](ui-define-granular-permissions.md).

Eftirfarandi tafla birtir nauðsynlegar heimildir til að nota Copilot-eiginleika sem Veitt er af Business Central.

|Eiginleikar stjórnklefa|Nauðsynlegar heimildir|
|-|-|
|Greiningaraðstoð|**GAGNAGREINING - EXEC** heimild stillt eða keyrð heimild fyrir kerfishlut 9640 **Leyfa gagnagreiningarstillingu**. Þessar heimildir eru sömu heimildir sem þarf til að komast í greiningarhaminn.|
|Aðstoð við bankaafstemmingu|Heimild á bls. 7250 **Bankareikn.uppg. AI-tillaga og bls** . 7252 **Trans. Tillaga til fjárhagss**. AI.|
|Spjalla |Engar heimildir eða heimildamengi hafa aðgang að til að spjalla eftir notanda. Ef spjall er virkjað er það tiltækt öllum notendum.|
|Varpa e-skjölum |Heimild á bls. 6166 **E-Doc. Stjórnklefavinnslna innkaupapöntunar**|
|Tillögur að markaðstexta |Heimild á síðu 5836 **Copilot markaðssetningartexti**|
|Sölulínutillögur |Heimild á bls. 7275 **Sölulína AI tillögur og bls** . 7276 **Sölulína AI-tillögur undir**|

Ef veita á eða neita aðgangi að tilteknum stjórnunarmöguleikum Microsoft og afkastagetu er leitað ráða hjá heimildum eða útgefanda aðgerðarinnar til að bera kennsl á tilskildar heimildir.

## Kröfur um að vera stjórnandi

Þú verður að hafa annaðhvort SUPER heimildir í Business Central notandareikningi eða eitt af eftirfarandi Business Central leyfi:

- Úthlutaður stjórnandi
- Úthlutuð hjálp
- Altækur stjórnandi
- BC stjórnandi
- D365-stjórnandi

Business Central býður ekki enn eindar heimildir til að aðeins tilteknir stjórnendur geti stillt Copilot.

## Næstu skref

Þegar þú hefur virkjað og veitt samþykki fyrir aðgerðunum er þú tilbúinn að prófa þær. Farðu til:

- [Bæta markaðssetningartexta við vörur með Afrita](item-marketing-text.md)
- [Greina listagögn með hjálp Copilot](analysis-assist.md)  
- [Spjall við Copilot](chat-with-copilot.md)
- [Tengja rafræn við innkaupapöntunarlínur með Copilot](map-edocuments-with-copilot.md)
- [Afstemma bankareikninga með Copilot](bank-reconciliation-with-copilot.md)
- [Leggja til línur á sölupöntunum með Copilot](sales-suggest-sales-lines-with-copilot.md)  

## Sjá einnig .

[Úrræðaleit fyrir Copilot- og AI-eiginleika](ai-copilot-troubleshooting.md)  
[Algengar spurningar um greiningaraðstoð](faqs-analysis-assist.md)  
[Algengar spurningar um aðstoð vegna bankaafstemmingar](faqs-bank-reconciliation.md)  
[Algengar spurningar fyrir spjall við Copilot](faqs-chat-with-copilot.md)  
[Algengar spurningar um vörpun e-skjala með innkaupapöntunum](faqs-map-edocuments.md)  
[Algengar spurningar um tillögur að markaðstexta](faqs-marketing-text.md)  
[Algengar spurningar fyrir sölulínutillögur](faq-sales-suggest-sales-lines-with-copilot.md)  

[Yfirlit yfir tillögur að markaðstexta](ai-overview.md)  