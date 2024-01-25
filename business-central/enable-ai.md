---
title: Stilltu Copilot og AI getu
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

# <a name="configure-copilot-and-ai-capabilities"></a>Stilltu Copilot og AI getu

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Þessi grein útskýrir hvernig á að stjórna Copilot og öðrum gervigreindargetum í Business Central. Þetta verkefni er gert af stjórnanda. Copilot er kerfiseiginleiki og óaðskiljanlegur hluti af Business Central. Líkt og flestir kerfiseiginleikar veitir þú ekki einstökum notendum aðgang né geturðu kveikt eða slökkt á Copilot. Hins vegar býður Copilot upp á gagnastjórnunarstýringar og möguleika á að slökkva á einstökum Copilot og AI getu fyrir hvert umhverfi. Það eru mismunandi stig aðgangsstýringar að gervigreindargetu, allt eftir eiginleikum:

- Leyfa gagnaflutning milli landfræðilegra svæða

  Þetta verkefni er aðeins krafist ef Business Central umhverfið þitt er í öðru landafræði en Azure OpenAI þjónustan sem það notar. [Læra meira](#allow-data-movement-across-geographies)

- Virkjaðu eiginleikann á **stýrivélinni & AI Capabilities** síða. [Læra meira](#activate-features)

- Virkjaðu tiltekna eiginleikann, ef hann er enn stjórnað af **eiginleikastjórnun**.

  Í útgáfubylgju 2 fyrir árið 2023 eru bæði tillögurnar um markaðstexta og aðstoðaeiginleika bankareikninga innifalin undir **eiginleikastjórnun**. [Læra meira](#enable-feature-in-feature-management)

Ef eitthvað af þessum kröfum er ekki uppfyllt er eiginleikinn ekki tiltækur til notkunar.

## <a name="prerequisites"></a>Frumskilyrði

- Þú ert að nota Business Central á netinu, útgáfu 23.1 eða nýrri. <!--[preview version](ai-preview-getstarted.md) of Business Central that's enabled for Copilot.-->
- Þú hefur stjórnanda- eða ofurheimildir í Business Central.  <!--For more information, go to [Configure AI-powered item marketing text with Copilot](enable-ai.md).-->

## <a name="allow-data-movement-across-geographies"></a>Leyfa gagnaflutning milli landa

Þetta verkefni á aðeins við ef **Leyfa gagnaflutninga** rofinn birtist nálægt toppi **Copilot & AI Capabilities** síða. Ef hlekkurinn **Hvernig stjórna ég aðstoðarflugmannsgögnunum mínum?** er sýndur í stað **Leyfa gagnaflutninga** rofann, slepptu þetta skref.

![Sýnir skjáskot af rofanum Leyfa gagnahreyfingar á Copilot & AI Capabilities síða.](media/allow-data-movement-v2.png)

 **Leyfa gagnaflutning** rofinn gefur til kynna að staðsetning Business Central umhverfisins þíns&mdash; þ.e. landafræði þar sem gögn eru unnin og geymd&mdash; er ekki það sama og Azure OpenAI þjónustulandafræðin sem Copilot notar. Ef þú vilt virkja Copilot verður þú að leyfa gagnaflutning á milli landa. Til að læra meira um gagnaflutning, farðu í [Copilot gagnaflutningur yfir landsvæði](ai-copilot-data-movement.md). 

Til að leyfa gagnaflutning utan landfræðilegs svæðis þíns skaltu ljúka eftirfarandi skrefum:

1. Í Business Central skaltu leita að og opna **Copilot & AI Capabilities** síðu.
1. Kveiktu á **Leyfa gagnaflutninga** rofa.

Þú getur afþakkað með því að slökkva á  **Leyfa gagnaflutninga** rofanum. Þegar Azure OpenAI þjónusta verður tiltæk í landafræði Business Central umhverfisins þíns er umhverfið þitt sjálfkrafa tengt við það og rofinn er ekki lengur tiltækur. 


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
## <a name="activate-features"></a>Virkjaðu eiginleika

Allar Copilot og gervigreindarhæfileikar eru virkir sjálfgefið þegar þeir eru aðgengilegir í forskoðun eða verða almennt tiltækir. Notkun **Copilot & AI Capabilities** síðu geturðu slökkt eða kveikt á einstökum eiginleikum fyrir alla notendur.

1. Í Business Central skaltu leita að og opna **Copilot & AI Capabilities** síðu.

1. Síðan sýnir alla tiltæka Copilot og AI tengda eiginleika og núverandi stöðu þeirra, sem geta verið annað hvort virkir eða óvirkir. Eiginleikunum er skipt í tvo hluta&mdash; einn hluti fyrir eiginleika í forskoðun og annan fyrir eiginleika sem eru almennt tiltækir. 

   [![Sýnir Business Central hlutverkamiðstöðina og gátlistann fyrir Copilot](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

   - Til að kveikja á eiginleika skaltu velja hann á listanum og velja síðan aðgerðina **Virkja** .
   - Til að slökkva á eiginleika skaltu velja hann og velja síðan **Slökkva á** aðgerð. 


## <a name="enable-feature-in-feature-management"></a>Virkja eiginleika í eiginleikastjórnun

Þegar einstakir Copilot eiginleikar eru gefnir út í Business Central minniháttar uppfærslum eru þessir eiginleikar valfrjálsir fram að næstu meiriháttar uppfærslu. **Eiginleikastjórnun** er notað til að kveikja eða slökkva á eiginleikum sem eru í forskoðun, eins og bankaafstemmingu, og sumum eiginleikum sem eru almennt tiltækir, eins og tillögur um markaðstexta. [Frekari upplýsingar um eiginleikastjórnun](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. Í Business Central skaltu leita að og opna  **Eiginleikastjórnun** síðuna.
2. Til að virkja eiginleika skaltu stilla **Virkt fyrir** dálknum á **Allir notendur**. Til að slökkva á eiginleika skaltu stilla **Virkt fyrir** dálknum á **None**. Notaðu eftirfarandi töflu til að hjálpa þér að ákvarða rofann sem á við um Copilot og AO getu sem þú vilt virkja:

   - **Forskoðun eiginleika: Afstemming bankareiknings við Copilot** viðurkvæmir aðstoðaeiginleika bankareikningsafstemmingar.
   - **Forskoðun eiginleika: Búðu til AI-knúnar vörulýsingar með Copilot** tilheyrir eiginleikanum með markaðstextatillögum.

   Fyrir frekari upplýsingar um eiginleikastjórnun almennt, farðu í [Eiginleikastjórnun](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="granting-user-access"></a>Að veita notanda aðgang

Copilot og gervigreind geta boðið upp á virkni sem ætlað er fyrir alla notendur í fyrirtækinu þínu eða fyrir ákveðin notendahlutverk. Flestar Copilot og gervigreindargetur bjóða upp á aðgangsstýringu með því að nota heimildir og heimildasett í heimildastjórnunarkerfi Business Central. [Lærðu meira um heimildir og heimildasett](ui-define-granular-permissions.md).

Til að veita eða hafna aðgangi að tilteknum Copilot og gervigreindum möguleikum, hafðu samband við skjöl eða útgefanda þess eiginleika til að finna hvaða heimildir eru nauðsynlegar. 

## <a name="next-steps"></a>Næstu skref

Eftir að þú hefur virkjað og samþykkt eiginleikana ertu tilbúinn til að prófa þá. Fara til:

- [Bættu markaðstexta við hluti](item-marketing-text.md) 
- [Samræma með því að nota aðstoð við afstemmingu bankareikninga](bank-reconciliation-with-copilot.md) 

## <a name="see-also"></a>Sjá einnig .

[Villuleita Copilot- og gervigreindarmöguleika](ai-copilot-troubleshooting.md)  
[Yfirlit yfir tillögur um markaðstexta](ai-overview.md)   
[Algengar spurningar um tillögur að markaðstexta](faqs-marketing-text.md)  
