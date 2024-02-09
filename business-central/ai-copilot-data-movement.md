---
title: Yfirmannsgagnahreyfing í landsvæðum
description: Fræðast um hvernig gögn sem notuð eru í afritunareiginleikum færist Dynamics 365 Business Central yfir landfræðileg atriði þar sem Azure OpenAI þjónusta er ekki sjálfgefin.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.date: 11/30/2023
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---

# <a name="copilot-data-movement-across-geographies"></a>Yfirmannsgagnahreyfing í landsvæðum

Copilot er fáanlegt í öllum studdum [Business Central löndum/svæðum](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). Hins vegar notar Microsoft Azure OpenAI Copilot þjónustu sem er eingöngu tiltæk fyrir Business Central á sumum landsvæðum. Þetta þýðir að ef umhverfið þitt er staðsett annars staðar verður að senda gögn úr eiginleikanum Copilot og generative AI utan landsvæðisins og hægt er að vinna gögnin utan samræmismarka þíns. Gögn fela í sér kvaðningar og viðskiptagögn sem copilot notar eða mynda þau. Í þessu tilfelli verður að velja að leyfa hreyfingu gagna til Azure-þjónustu OpenAI í annarri landafræði. <!--For a list of geographies, refer to the [Azure OpenAI Service geographies](#azure-openai-service-geographies) section that follows.-->

> [!IMPORTANT]
> Ef umhverfi þitt er staðsett á sama Azure svæðinu og Azure OpenAI þjónusta, það tengist sjálfkrafa við Azure OpenAI Þjónustu, það er ekki valkostur og engin einu sinni grunnstilling er krafist.

> [!NOTE]
> Einstakar copilot- og myndandi AI-eiginleikar gætu verið ekki í boði í öllum Business Central umhverfislöndum/svæðum. Hafa skal samráð við útgefanda hvers getu til að skilja ráðstöfunarmagn.
> 
> Copilot- og myndandi AI-eiginleikar frá útgefendum sem ekki koma frá Microsoft, svo sem þeim sem koma úr sérstillingum eða AppSource forritum sem þú setur upp, skilgreina hvert þeirra sérstök Azure-þjónustusvæði OpenAI . Ráðfærðu þig við útgefanda viðbótarinnar til að skilja hvaða svæðisbundna Azure-þjónustur notast við viðbótina. 

### <a name="azure-openai-service-geographies"></a>Azure OpenAI þjónusta landfræði

Eftirfarandi tafla sýnir landafræði Azure-þjónustunnar OpenAI sem Copilot notar, byggt á Azure-svæðinu í Business Central umhverfi. Þessar upplýsingar skipta miklu máli þegar ákveðið er hvort eigi að skrá gagnahreyfingar yfir landfræðilegar upplýsingar. Þú getur fundið Azure-svæðið fyrir umhverfið í stjórnunarmiðstöð Business Central (sjá [Stjórnun umhverfis í stjórnunarmiðstöðinni](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)).

| Umhverfis azure-svæði| Azure OpenAI þjónusta landfræði|Stjórna aðgerð sem þarf til að aflæsa Stjórnunaraðgerð| 
| - | - | - |
|Asía (Austur, Suður-Austur) |Bandaríkin|Já|
|Ástralía (Suður-Austur)| Bandaríkin |Já |
|Brasilía (Suður) |Bandaríkin|Já|
|Kanada (Mið, Austur)|Bandaríkin|Já|
|Evrópa (Vestur, Norður)| Svíþjóð eða Sviss |Já|
|Frakkland (Mið, Suður)| Svíþjóð eða Sviss |Já|
|Þýskaland (Norður, Vestur-Miðborg)| Svíþjóð eða Sviss |Já|
|Indland (Mið, Suður)|Bandaríkin|Já|
|Japan (Austur, Vestur)|Bandaríkin|Já|
|Kórea (Mið, Suður)|Bandaríkin|Já|
|Noregur (Austur, Vestur)|Svíþjóð eða Sviss |Já|
|Suður-Afríka (Norður, Vestur)|Bandaríkin|Já|
|Sviss (Norður, Vesturland) |Svíþjóð eða Sviss |Já|
|Sameinuðu Arabísku Furstadæmin (Norður, Vestur)|Bandaríkin|Já|
|Bretland (Suður, Vestur)|Bretland|Já|
|Bandaríkin (Mið, Austur, Norður miðsvæðis, Suður miðsvæðis, Vestur) |Bandaríkin|Nr.|

> [!NOTE]
> Þegar Azure OpenAI þjónusta verður í boði í Business Central landafræði þinni mun umhverfi þitt sjálfkrafa umskipti til að nota Azure OpenAI þjónustuna og kíkir í er ekki krafist eða jafnvel mögulegt.  
<!--

BC geos base on https://dynamics.microsoft.com/en-us/availability-reports/georeport/
case "AUSTRALIAEAST":
            case "AUSTRALIASOUTHEAST":
                return new CapiRegion("au", 2);
            case "BRAZILSOUTH":
                return new CapiRegion("br", 2);
            case "CANADACENTRAL":
            case "CANADAEAST":
                return new CapiRegion("ca", 2);
            case "CENTRALINDIA":
            case "SOUTHINDIA":
                return new CapiRegion("in", 1);
            case "EASTASIA":
                return new CapiRegion("as", 2);
            case "EASTUS":
            case "EASTUS2":
            case "SOUTHCENTRALUS":
            case "CENTRALUS":
            case "NORTHCENTRALUS":
            case "WESTUS":
            case "US":
                return new CapiRegion("us", 9, HasGpt4InGeo: true, HasTurboInGeo: true);
            case "FRANCECENTRAL":
            case "FRANCESOUTH":
                return new CapiRegion("fr", 1);
            case "GERMANYNORTH":
            case "GERMANYWESTCENTRAL":
                return new CapiRegion("de", 1);
            case "JAPANEAST":
            case "JAPANWEST":
                return new CapiRegion("jp", 1);
            case "KOREACENTRAL":
            case "KOREASOUTH":
                return new CapiRegion("kr", 1);
            case "NORWAYEAST":
            case "NORWAYWEST":
                return new CapiRegion("no", 1);
            case "SOUTHAFRICANORTH":
            case "SOUTHWESTAFRICA":
                return new CapiRegion("za", 1);
            case "SOUTHEASTASIA":
                return new CapiRegion("sg", 1);
            case "SWITZERLANDNORTH":
            case "SWITZERLANDWEST":
                return new CapiRegion("ch", 1, HasTurboInGeo: true);
            case "UKSOUTH":
            case "UKWEST":
                return new CapiRegion("uk", 2);
            case "NORTHEUROPE":
            case "WESTEUROPE":
                return new CapiRegion("eu", 10);
            case "UAENORTH":
            case "UAECENTRAL":
                return new CapiRegion("ae", 1);

-->

## <a name="next-steps"></a>Næstu skref

Þú kýst að leyfa hreyfingu gagna yfir landfræðilegar gerðir af síðunni [Copilot & AI.](https://businesscentral.dynamics.com/?page=7775)  Nánari upplýsingar eru notaðar til að [leyfa hreyfingu gagna í landfræði.](enable-ai.md#allow-data-movement-across-geographies)
