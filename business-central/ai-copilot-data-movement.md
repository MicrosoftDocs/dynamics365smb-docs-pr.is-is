---
title: Yfirmannsgagnahreyfing í landsvæðum
description: Fræðast um hvernig gögn sem notuð eru í afritunareiginleikum færist Dynamics 365 Business Central yfir landfræðileg atriði þar sem Azure OpenAI þjónusta er ekki sjálfgefin.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection: get-started
ms.date: 11/09/2023
ms.custom: bap-template
---

# Yfirmannsgagnahreyfing í landsvæðum 

Copilot er fáanlegt á öllum studdum [Business Central landsvæðum](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). Hins vegar notar Microsoft Azure OpenAI Copilot Þjónustu, sem er eingöngu í boði fyrir Business Central á sumum landsvæðum, sem stendur Bandaríkjunum og Sviss. Þetta þýðir að ef umhverfið þitt er staðsett annars staðar verður að senda gögn úr eiginleikanum Copilot og generative AI utan landsvæðisins og hægt er að vinna gögnin utan samræmismarka þíns. Gögn fela í sér kvaðningar og viðskiptagögn sem copilot notar eða mynda þau. Í þessu tilfelli verður að velja að leyfa hreyfingu gagna til Azure-þjónustu OpenAI í annarri landafræði. <!--For a list of geographies, refer to the [Azure OpenAI Service geographies](#azure-openai-service-geographies) section that follows.-->

> [!IMPORTANT]
> Ef umhverfið þitt er staðsett í sömu landafræði og Azure OpenAI þjónusta, það tengir það sjálfkrafa við Azure OpenAI Service, það er enginn valkostur. Í Evrópu velur Business Central sjálfkrafa við hreyfingu gagna, en stjórnendur geta valið að afþakka hvenær sem er.

> [!NOTE]
> Einstakar copilot- og myndandi AI-eiginleikar gætu verið ekki tiltækir á öllum Business Central landsvæðum. Hafa skal samráð við útgefanda hvers getu til að skilja ráðstöfunarmagn.
> 
> Copilot- og myndandi AI-eiginleikar frá útgefendum sem ekki koma frá Microsoft, svo sem þeim sem koma úr sérstillingum eða AppSource forritum sem þú setur upp, skilgreina hvert þeirra sérstök Azure-þjónustusvæði OpenAI . Ráðfærðu þig við útgefanda viðbótarinnar til að skilja hvaða svæðisbundna Azure-þjónustur notast við viðbótina. 

### Azure OpenAI þjónusta landfræði

Eftirfarandi tafla sýnir landafræði Azure-þjónustunnar OpenAI sem Copilot notar, byggt á landafræði Business Central umhverfis. Þessar upplýsingar skipta miklu máli þegar ákveðið er hvort eigi að skrá gagnahreyfingar yfir landfræðilegar upplýsingar. Hægt er að *auðkenna landafræði umhverfisins í stjórnunarmiðstöð Business Central þar sem það er kallað Azure-svæði*  (sjá [Stjórnun umhverfis í stjórnunarmiðstöðinni](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)).

| Landafræði Business Central (Azure-svæði)| Azure OpenAI þjónusta landfræði|
| - | - |
|Asía (Austur, Suður-Austur) |Bandaríkin|
|Ástralía (Suður-Austur)| Bandaríkin |
|Brasilía (Suður) |Bandaríkin|
|Kanada (Mið, Austur)|Bandaríkin|
|Evrópa (Vestur, Norður)| Sviss |
|Frakkland (Mið, Suður)|Sviss |
|Þýskaland (Norður, Vestur-Miðborg)|Sviss |
|Indland (Mið, Suður)|Bandaríkin|
|Japan (Austur, Vestur)|Bandaríkin|
|Kórea (Mið, Suður)|Bandaríkin|
|Noregur (Austur, Vestur)|Sviss |
|Suður-Afríka (Norður, Vestur)|Bandaríkin|
|Sviss (Norður, Vesturland) |Sviss|
|Sameinuðu Arabísku Furstadæmin (Norður, Vestur)|Bandaríkin|
|Bretland (Suður, Vestur)|Bandaríkin|
|Bandaríkin (Mið, Austur, Norður miðsvæðis, Suður miðsvæðis, Vestur) |Bandaríkin|
<!--
| Business Central environment geography | Azure OpenAI Service geography|
| - | - |
|Asia Pacific|United States|
|Australia| United States |
|Brazil |United States|
|Canada|United States|
|Europe| Switzerland |
|France|Switzerland |
|Germany|Switzerland |
|France|Switzerland |
|India|United States|
|Japan|United States|
|Korea|United States|
|Norway|Switzerland |
|Singapore|United States|
|South Africa|United States|
|Switzerland |Switzerland|
|United Arab Emirates|United States|
|United Kingdom|United States|
|United States|United States|-->

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

## Næstu skref

Þú kýst að leyfa hreyfingu gagna yfir landfræðilegar gerðir af síðunni [Copilot & AI.](https://businesscentral.dynamics.com/?page=7775)  Nánari upplýsingar eru notaðar til að [leyfa hreyfingu gagna í landfræði.](enable-ai.md#allow-data-movement-across-geographies)
