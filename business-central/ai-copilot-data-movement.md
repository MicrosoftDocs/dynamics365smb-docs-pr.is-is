---
title: Flutningur á gagnaflutningum milli landa
description: Kynntu þér hvernig gögn sem eru notuð í aukaflugmannseiginleikum í Dynamics 365 Business Central hreyfast yfir landsvæði þar sem Azure OpenAI þjónusta er sjálfgefið ekki tiltæk.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection: null
ms.date: 11/30/2023
ms.custom: bap-template
---

# <a name="copilot-data-movement-across-geographies"></a>Flutningur á gagnaflutningum milli landa

Copilot er fáanlegt í öllum studdum [Business Central löndum/svæðum](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). Hins vegar notar Copilot Microsoft Azure OpenAI þjónustu, sem er nú aðeins í boði fyrir Business Central á sumum landfræðilegum svæðum. Þetta þýðir að ef umhverfið þitt er staðsett annars staðar verða gögn frá Copilot og generative AI eiginleikanum að vera send utan landfræðilegs svæðis þíns og gætu verið unnin og geymd utan samræmismarka þinna. Gögn innihalda gervigreindartilkynningar og viðskiptagögn þín sem eru notuð af eða mynda af Copilot. Í þessu tilviki verður þú að velja inn til að leyfa gagnaflutning til Azure OpenAI þjónustu í öðru landsvæði. <!--For a list of geographies, refer to the [Azure OpenAI Service geographies](#azure-openai-service-geographies) section that follows.-->

> [!IMPORTANT]
> Ef umhverfið þitt er staðsett á sama Azure svæði og Azure OpenAI þjónustan tengist hún sjálfkrafa við Azure OpenAI þjónustuna, það er enginn valkostur og engin einskiptisstilling er nauðsynleg.

> [!NOTE]
> Einstakir Copilot og generative AI eiginleikar gætu ekki verið tiltækir í öllum löndum/svæðum í Business Central umhverfi. Hafðu samband við útgefanda hvers getu til að skilja framboð.
> 
> Copilot og skapandi gervigreind eiginleikar frá útgefendum sem ekki eru frá Microsoft, eins og þeir sem koma frá sérstillingum eða AppSource öppum sem þú setur upp, skilgreina hver sín sérstöku Azure OpenAI þjónustusvæði. Ráðfærðu þig við útgefanda viðbótarinnar til að skilja hvaða svæðisbundna Azure þjónusta er notuð af viðbótinni. 

### <a name="azure-openai-service-geographies"></a>Azure OpenAI Þjónustusvæði

Eftirfarandi tafla sýnir landafræði Azure OpenAI þjónustunnar sem Copilot notar, byggt á Azure svæðinu í Business Central umhverfi. Þessar upplýsingar eru mikilvægar þegar tekin er ákvörðun um hvort velja eigi gagnaflutning milli landa. Þú getur auðkennt Azure svæðið fyrir umhverfið þitt í Business Central stjórnunarmiðstöðinni (sjá [Umhverfisstjórnun í stjórnunarmiðstöðinni](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)).

| Umhverfi Azure svæði| Azure OpenAI Landafræði þjónustu|Aðgerð stjórnanda nauðsynleg til að opna Copilot| 
| - | - | - |
|Asía (Austur, Suðaustur) |Bandaríkin|Já|
|Ástralía (Suðausturland)| Bandaríkin |Já |
|Brasilía (Suður) |Bandaríkin|Já|
|Kanada (mið, austur)|Bandaríkin|Já|
|Evrópa (Vestur, Norður)| Svíþjóð eða Sviss |Já|
|Frakkland (Mið, Suður)| Svíþjóð eða Sviss |Já|
|Þýskaland (Norður, Vestur Mið)| Svíþjóð eða Sviss |Já|
|Indland (mið, suður)|Bandaríkin|Já|
|Japan (austur, vestur)|Bandaríkin|Já|
|Kórea (Mið, Suður)|Bandaríkin|Já|
|Noregur (Austur, Vestur)|Svíþjóð eða Sviss |Já|
|Suður-Afríka (Norður, Vestur)|Bandaríkin|Já|
|Sviss (Norður, Vestur) |Svíþjóð eða Sviss |Já|
|Sameinuðu arabísku furstadæmin (Norður, Vestur)|Bandaríkin|Já|
|Bretland (Suður, Vestur)|Bretland|Já|
|Bandaríkin (Mið, Austur, Norður Mið, Suður Mið, Vestur) |Bandaríkin|Nr.|

> [!NOTE]
> Þegar Azure OpenAI þjónusta verður tiltæk í Business Central landafræðinni þinni mun umhverfið þitt sjálfkrafa breytast í að nota Azure OpenAI þjónustuna og að skrá sig inn er ekki krafist eða jafnvel möguleg.  
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

Þú velur að leyfa gagnaflutning milli landa frá [Copilot & AI Capabilities](https://businesscentral.dynamics.com/?page=7775) síða. Til að fá frekari upplýsingar skaltu fara á [Leyfa gagnaflutning á milli landa](enable-ai.md#allow-data-movement-across-geographies).
