---
title: Yfirmannsgagnahreyfing í landsvæðum
description: Fræðast um hvernig gögn sem notuð eru í gervigreindaraðstoðari eiginleikum færist Dynamics 365 Business Central yfir landfræðileg atriði þar sem Azure OpenAI þjónusta er ekki sjálfgefin.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.date: 04/16/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
ms.search.form: 7775
---

# Yfirmannsgagnahreyfing í landsvæðum 

Copilot er fáanlegt í öllum studdum [Business Central löndum/svæðum](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). Hins vegar notar Microsoft Azure OpenAI Copilot þjónustu sem er eingöngu tiltæk fyrir Business Central á sumum landsvæðum. Þetta þýðir að ef umhverfið þitt er staðsett annars staðar verður að senda gögn úr eiginleikanum Copilot og generative AI utan landsvæðisins og hægt er að vinna gögnin utan samræmismarka þíns. Gögn fela í sér kvaðningar og viðskiptagögn sem copilot notar eða mynda þau. Í þessu tilfelli verður að velja að leyfa hreyfingu gagna til Azure-þjónustu OpenAI í annarri landafræði. <!--For a list of geographies, refer to the [Azure OpenAI Service geographies](#azure-openai-service-geographies) section that follows.-->

> [!IMPORTANT]
> Ef umhverfi þitt er staðsett á sama Azure svæðinu og Azure OpenAI þjónusta, það tengist sjálfkrafa við Azure OpenAI Þjónustu, það er ekki valkostur og engin einu sinni grunnstilling er krafist.

> [!NOTE]
> Einstakar copilot- og myndandi AI-eiginleikar gætu verið ekki í boði í öllum Business Central umhverfislöndum/svæðum. Hafa skal samráð við útgefanda hvers getu til að skilja ráðstöfunarmagn.
> 
> Copilot- og myndandi AI-eiginleikar frá útgefendum sem ekki koma frá Microsoft, svo sem þeim sem koma úr sérstillingum eða AppSource forritum sem þú setur upp, skilgreina hvert þeirra sérstök Azure-þjónustusvæði OpenAI . Ráðfærðu þig við útgefanda viðbótarinnar til að skilja hvaða svæðisbundna Azure-þjónustur notast við viðbótina. 

### Azure OpenAI þjónusta landfræði

Eftirfarandi tafla sýnir landafræði Azure-þjónustunnar OpenAI sem Copilot notar, byggt á Azure-svæðinu í Business Central umhverfi. Þessar upplýsingar skipta miklu máli þegar ákveðið er hvort eigi að skrá gagnahreyfingar yfir landfræðilegar upplýsingar. Þú getur fundið Azure-svæðið fyrir umhverfið í stjórnunarmiðstöð Business Central (sjá [Stjórnun umhverfis í stjórnunarmiðstöðinni](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)).

| Umhverfis azure-svæði| Azure OpenAI þjónusta landfræði|Stjórna aðgerð sem þarf til að aflæsa Stjórnunaraðgerð| 
| - | - | - |
|Asía (Austur, Suður-Austur) |Bandaríkin|Já|
|Ástralía (Suður-Austur)| Ástralía |Nr. |
|Brasilía (Suður) |Bandaríkin|Já|
|Kanada (Mið, Austur)|Bandaríkin|Já|
|Evrópa (Vestur, Norður)| Svíþjóð eða Sviss |Nei\*|
|Frakkland (Mið, Suður)| Svíþjóð eða Sviss |Já|
|Þýskaland (Norður, Vestur-Miðborg)| Svíþjóð eða Sviss |Já|
|Indland (Mið, Suður)|Indland|Nr.|
|Japan (Austur, Vestur)|Bandaríkin|Já|
|Kórea (Mið, Suður)|Bandaríkin|Já|
|Noregur (Austur, Vestur)|Svíþjóð eða Sviss |Já|
|Suður-Afríka (Norður, Vestur)|Bandaríkin|Já|
|Sviss (Norður, Vesturland) |Svíþjóð eða Sviss |Já|
|Sameinuðu Arabísku Furstadæmin (Norður, Vestur)|Bandaríkin|Já|
|Bretland (Suður, Vestur)|Bretland|Nr.|
|Bandaríkin (Mið, Austur, Norður miðsvæðis, Suður miðsvæðis, Vestur) |Bandaríkin|Nr.|

\* Í umhverfi á Vestur-Evrópu og Norður-Evrópu Azure svæðum velur Business Central sjálfkrafa að gagnahreyfingu yfir landfræðilegu svæði, en stjórnendur geta valið að afþakka hvenær sem er.

> [!NOTE]
> Þegar Azure OpenAI þjónusta verður í boði í Business Central landafræði þinni mun umhverfi þitt sjálfkrafa umskipti til að nota Azure OpenAI þjónustuna og kíkir í er ekki krafist eða jafnvel mögulegt.


## Næstu skref

Þú velur (eða út úr) gagnahreyfingu yfir landfræðilegar gerðir af síðunni [Copilot & AI.](https://businesscentral.dynamics.com/?page=7775)  Nánari upplýsingar eru notaðar til að [leyfa hreyfingu gagna í landfræði.](enable-ai.md#allow-data-movement-across-geographies)
