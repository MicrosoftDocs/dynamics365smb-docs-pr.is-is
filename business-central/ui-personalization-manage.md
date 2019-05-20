---
title: Stjórnun sérstillinga sem stjórnandi í Business Central | Microsoft Docs
description: Lærðu hvernig á að aðlaga notendaviðmótið til að henta því hvernig þú vinnur.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 37cdf2d7dcc46b1286cbb7a5ad620547e364309e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250596"
---
# <a name="managing-personalization-as-an-administrator"></a>Stjórnun sérstillinga sem stjórnandi

 Notendur geta sérsniðið vinnusvæði sitt að vild. Sem stjórnandi stjórnar þú og hefur umsjón með sérstillingum með því að:

-   Kveikja eða slökkva á eiginleika sérstillingar fyrir allt forritið (einungis fyrir uppsetningar á staðnum).
-   Kveikja eða slökkva á eiginleika sérstillingar fyrir notendur af tilteknum prófíl.
-   Hreinsa allar sérstillingar á síðu sem notendur hafa gert.

## <a name="EnablePersonalization"></a>Kveikja eða slökkva á sérstillingum (aðeins á staðnum)

Sjálfgefið er að slökkt sé á sérstillingu í biðlaranum. Þú kveikir eða slekkur á sérstillingum með því að breyta skilgreiningarskránni (navsettings.json) í tilviki fyrir vefþjón Business Central sem þjónar biðlaranum.

1. Til að kveikja á sérstillingum skaltu bæta eftirfarandi línu við navsettings.json skrána:

    ```
    "PersonalizationEnabled": "true"
    ```

    Til að slökkva á sérstillingum skaltu fjarlægja þessa línu eða breyta henni í:

    ```
    "PersonalizationEnabled": "false"
    ```

    Nánari upplýsingar um hvernig skuli breyta navsettings.json skránni er að finna í [Breyta navsettings.json skránni beint](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).

2. Búðu til og sæktu táknin fyrir forritið.

    Þetta skref er valfrjálst og er ekki nauðsynlegt til að kveikja á sérstillingu. Hins vegar tryggir það að þróunaraðilar geti sérstillt nýjar síður sem eru stofnaðar.

    1. Fyrst eru táknin búin til með því að keyra finsql.exe með `generatesymbolreference` skipuninni. Skráin finsql.exe er staðsett í uppsetningarmöppunni fyrir [!INCLUDE[server](includes/server.md)] og Dynamics NAV þróunarumhverfi (CSIDE). Til að búa til táknin skaltu opna skipanakvaðningu, breyta yfir í skráasafnið þar sem skráin er geymd og síðan keyra eftirfarandi skipun:

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    Dæmi:

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    Frekari upplýsingar er að finna í [Keyra C/SIDE og AL samhliða](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).

    2. Skilgreindu [!INCLUDE[nav_server_md](includes/nav_server_md.md)] tilvik í **Virkja hleðslu á tilvísunum forritatákna við ræsingu þjóns** (EnableSymbolLoadingAtServerStartup). Frekari upplýsingar er að finna í [Skilgreining Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).

## <a name="to-disable-personalization-for-a-profile"></a>Að slökkva á sérstillingu fyrir prófíl

Hægt er að koma í veg fyrir að allir notendur sem tilheyra tiltekinni forstillingu geti sérstillt síður sínar.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notandastillingar** og veldu síðan tengda tengilinn.
2. Veljið forstillinguna sem á að breyta í listanum.
3. Veljið gátreitinn **Afvirkja sérstillingar notanda** og smellið síðan á hnappinn **Í lagi**.

## <a name="to-clear-user-personalizations"></a>Að hreinsa sérstillingar notanda

Þegar sérstillingar síðu er eytt fer síðan aftur í upprunalegt útlit áður en sérstillingin var gerð. Það eru tvær leiðir til að hreinsa sérstillingar sem notendur hafa gert á síðum: með **Eyða sérstillingum notanda** síðunni og **Sérstillingaspjald notanda**.

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Að hreinsa sérstillingar notenda með því að nota síðuna Eyða sérstillingum notanda

Síðan **Eyða sérstillingum notanda** gerir þér kleift að hreinsa sérstillingar á einstaka síðum, eftir einstaka notendum.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eyða sérstillingum notanda** og veldu síðan tengda tengilinn.

    Á síðunni er listi yfir allar síður sem hafa verið sérstilltar og sem notandinn tilheyrir.

    >[!NOTE]
    > Gátmerki í **Eldri sérstilling** dálknum gefur til kynna að sérstillingin hafi verið gerð í eldri útgáfu af [!INCLUDE[d365fin](includes/d365fin_md.md)], sem meðhöndlaði sérstillingu öðruvísi en er núna gert. Notendur sem reyna að sérstilla þessar síður eru útilokaðir frá því að gera það nema þeir velji að opna síðuna. Frekari upplýsingar eru í [Af hverju er síða læst og því ekki hægt að sérsníða hana](ui-personalization-locked.md).

2. Veljið færsluna sem á að eyða og veljið síðna aðgerðina **Eyða**.

    Notandinn mun sjá breytingarnar næst þegar hann skráir sig inn.

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Að hreinsa sérstillingar notenda með því að nota síðuna Sérstillingaspjald notanda

Síðan **Sérstillingaspjald notanda** gerir þér kleift að hreinsa sérstillingar á öllum síðum fyrir tiltekinn notanda. Þetta krefst skrifleyfis fyrir töflu 2000000072 **Forstilling**.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sérstillingar notanda** og veldu síðan tengda tengilinn.

    Síðan **Sérstillingar notanda** sýnir alla notendur sem hugsanlega hafa sérstillt síður. Ef þú finnur ekki notanda á listanum þýðir það að hann hefur engar sérstilltar síður.

2. Veljið notanda af listanum og veljið svo aðgerðina **Breyta**.

3. Í flipanum **Aðgerðir** veljið **Hreinsa sérstilltar síður**.

    Notandinn mun sjá breytingarnar næst þegar hann skráir sig inn.

## <a name="see-also"></a>Sjá einnig
[Sérstillingar verksvæðis](ui-personalization-user.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Breyta grundvallarstillingum](ui-change-basic-settings.md)  
[Breyting á hvaða eiginleikar eru sýndir](ui-experiences.md)  
