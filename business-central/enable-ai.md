---
title: Grunnstilla Copilot- og gervigreindarmöguleika
description: Þessi grein útskýrir hvernig á að virkja Copilot í umhverfi.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/28/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
ms.search.form: '7771,7772_Primary,7775_Primary'
---

# Grunnstilla Copilot- og gervigreindarmöguleika

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Þessi grein útskýrir hvernig stjórna Microsoft Copilot á og aðra möguleika ÓM Dynamics 365 Business Central. Stjórnandi verður að ljúka þessum verkum.

Copilot er kerfisaðgerð og óaðgreindur hluti Af Business Central. Eins og við á um flesta kerfisaðgerðir veitir notandi ekki aðgang að einstökum notendum og ekki er hægt að kveikja eða slökkva á Copilot. Hins vegar býður Copilot upp á eftirlit með gögnum og getur slökkva á einstökum möguleikum Copilot og AI fyrir hvert umhverfi. Mismunandi aðgangsstýringarstig eru tiltæk fyrir ÓHÍ, eftir því hver eiginleikinn er:

- Leyfa hreyfingu gagna á landsvæðum.

    Aðeins er krafist þessa verks ef Business Central umhverfið þitt er í annarri landfræði en Azure-þjónustan OpenAI sem hún notar. [Fræðast meira um þetta verk](#allow-data-movement-across-geographies).

- Virkja eiginleikann á síðunni **Copilot & AI** . [Fræðast meira um þetta verk](#activate-features).

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
- Enable the specific feature if it's governed by **Feature Management**.

  Check whether  of 2024 release wave 1, chat with Copilot, marketing text suggestions, and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)
<!-- 
- Enable the specific feature, if it's still governed by **Feature Management**.

  In 2023 release wave 2, both the marketing text suggestions and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)-->

Ef einhver þessara þarfa er ekki uppfyllt er eiginleikinn ekki tiltækur til notkunar.

## Frumskilyrði

- Þú notar Business Central á netinu.
- Ūú ert stjķrnandi [í](#requirements-for-being-an-administrator) Business Central.

## Leyfa hreyfingu gagna á landsvæðum

Þetta verk á aðeins við ef kosturinn **Leyfa hreyfingu** gagna birtist efst á síðunni **Copilot & AI** . Ef hvernig **stjórna ég gervigreindaraðstoðari gögnum mínum?** tengja birtist í stað **Leyfa gagnahreyfingarvalkosti**, sleppa þessu verki.

![Skjámynd sem sýnir valkostinn Leyfa hreyfingu gagna á síðunni Copilot & AI.](media/allow-data-movement-v2.png)

Nærvera valkostsins **Leyfa gagnahreyfingar** gefur til kynna að staðsetning Business Central umhverfisins (þ.e. landafræði þar sem gögn eru unnin og geymd) er frábrugðin landafræði Azure OpenAI Service sem Copilot notar. Til að virkja Copilot verður að leyfa hreyfingu gagna milli landa. [Fá nánari upplýsingar um hreyfingu](ai-copilot-data-movement.md) gagna.

Til að leyfa gagnahreyfingar utan landsvæðisins skal fylgja eftirfarandi skrefum:

1. Í Business Central er leitað að og opna síðuna **Copilot & AI** .
1. Kveikja á valkostinum **Leyfa gagnahreyfingu** .

    > [!NOTE]
    > Í umhverfi á Vestur-Evrópu og Norður-Evrópu Azure-svæðunum er sjálfgefið **að valkosturinn Leyfa gagnahreyfingu** sé virkur.

Til að hætta við hreyfingu gagna er valkosturinn **Leyfa gagnahreyfingu** gerður óvirkur.

Þegar Azure OpenAI þjónusta verður tiltæk í landafræði Business Central umhverfisins er umhverfið þitt sjálfkrafa tengt við það. Þá birtist valkosturinn **Leyfa gagnahreyfingu** ekki lengur á síðunni **Afrita & AI** .

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

Allir afkastageta copilot og AI eru sjálfgefið virk þegar þeir eru tiltækir í forútgáfa eða verða almennt tiltækir. Á síðunni **Copilot & AI** er hægt að slökkva á einstökum eiginleikum eða aftur fyrir alla notendur.

1. Í Business Central er leitað að og opna síðuna **Copilot & AI** .
1. Síðan birtir lista yfir allar tiltækar aðgerðir tengdar stjórnborði og núverandi stöðu þeirra. (Staðan getur verið annaðhvort *Virkt* eða *Óvirkt*.) Eiginleikunum er skipt í tvo hluta: annan fyrir aðgerðir sem eru í forútgáfa og eina fyrir aðgerðir sem eru almennt tiltækar.

    - Til að kveikja á aðgerð skal velja hana á listanum og velja **svo Virkja**.
    - Til að slökkva á aðgerð skal velja hann á listanum og velja **svo Óvirkja**.

    [![Skjámynd sem sýnir hnappana Virkja og Gera hnappa óvirka fyrir eiginleikalistana á síðunni Copilot & AI.](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

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

Copilot og AI geta boðið virkni sem er ætluð öllum notendum innan fyrirtækisins eða fyrir tiltekin notendahlutverk. Flestir copilot og AI geta bjóða upp á aðgangsstýringu í gegnum heimildir og heimildasafn í heimildastjórnunarkerfi Business Central. [Fá nánari upplýsingar um heimildir og heimildasafn](ui-define-granular-permissions.md).

Í eftirfarandi töflu eru taldar upp þær heimildir sem eru nauðsynlegar til að nota Copilot-eiginleikana sem Business Central veitir.

| Stjórnborðsaðgerð | Nauðsynlegar heimildir |
|---|---|
| Greiningaraðstoð |  **Gagnagreiningin - EXEC**  heimildasamstæða eða keyra heimild fyrir kerfishlut 9640,Leyfa **gagnagreiningarstillingu**. Þessar heimildir eru sömu heimildir og nauðsynlegar eru til að komast í greiningarhaminn. |
| Aðstoð við bankaafstemmingu | Heimild á bls. 7250,Bankareikn.upph **. AI-tillaga og bls**. 7252,Millifærslu **. Til að fjárhagur tillögu um** reikn.AI. |
| Spjalla | Engar heimildir eða heimildasafn eru sem stýra aðgangi að spjalli hvers notanda. Ef spjall er virkjað er það tiltækt öllum notendum. |
| Varpa e-skjölum | Heimild á bls. 6166,E-Skjal **. Stjórnk.afk.pönt. innkaupapöntunar** |
| Tillögur að markaðstexta | Heimild á síðu 5836,Copilot **markaðssetningartexti**. |
| Sölulínutillögur | Heimild á síðu 7275,Sölulínu **AI tillögur og bls**. 7276,Sölulína **AI tillögur undir**. |

Ef veita á eða neita aðgangi að tilteknum gervigreindaraðstoðari Microsoft og afkastagetu er leitað ráða hjá heimildum eða útgefanda aðgerðarinnar til að auðkenna tilskildar heimildir.

## Kröfur um að vera stjórnandi

Þú verður að hafa annaðhvort SUPER heimildir á Business Central notandareikningnum þínum eða eitt af eftirfarandi Business Central leyfi:

- Framseljandi stjórnanda - félagi
- Framseldur helpdesk umboðsmaður - félagi
- Innri stjórnandi
- Innri BC-kerfisstjóri
- Dynamics 365-stjórnandi

Business Central býður ekki enn eindar heimildir til að aðeins tilteknir stjórnendur geti stillt Copilot.

## Næstu skref

Þegar þú hefur virkjað og veitt samþykki fyrir aðgerðunum er þú tilbúinn að prófa þær. Fara í eftirfarandi greinar:

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
[Algengar spurningar fyrir vörpun e-skjöl með innkaupapöntunum](faqs-map-edocuments.md)  
[Algengar spurningar um tillögur að markaðstexta](faqs-marketing-text.md)  
[Algengar spurningar fyrir sölulínutillögur](faq-sales-suggest-sales-lines-with-copilot.md)  
[Yfirlit yfir tillögur að markaðstexta](ai-overview.md)
