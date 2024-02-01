---
title: Að setja upp vafrann þinn
description: Lýsir því hvernig á að setja upp vafra til að vinna með Business Central og sasmþættum vörum.
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'Teams, web client, troubleshooting, errors'
ms.date: 12/04/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Uppsetning og úrræðaleit vafrann þinn til að vinna með Business Central Web Client

Þessi grein útskýrir hvernig á að setja upp vafrann þannig að [!INCLUDE[web_client](includes/web_client.md)] og allir eiginleikar þess virki rétt. Lestu þessa grein ef þú átt í vandræðum með að opna [!INCLUDE[web_client](includes/web_client.md)], stillingar vafrans geta verið orsök sumra vandamála.

Í greininni er að finna upplýsingar fyrir uppsetningu Microsoft Edge, en kröfur um JavaScript, fótspor og sprettiglugga eru þær sömu fyrir alla studda vafra. Fyrir aðra vafra skal skoða leiðbeiningarnar sem framleiðandinn gefur upp.  

## Notaðu studdan vafra

Gættu þess að nota einn af studdu vöfrunum. Sjá [Lágmarkskröfur fyrir notkun Business Central](product-requirements.md#browsers).

Við mælum með því að þú notir stöðuga rásarútgáfu af vafra þar sem það er áreiðanlegasta og stöðugasta útgáfan sem hefur gengið í gegnum miklar prófanir og villuleiðréttingu. Þetta tryggir að þú hafir bestu upplifunina og ert ólíklegri til að lenda í vandræðum meðan þú notar vefþjóninn.  

## Leyfa JavaScript úr Business Central

*Vandamál:*

Ef vafrinn leyfir ekki JavaScript sérðu **NotSupported/DisabledJavaScript** í veffangastikunni og **HTTP Villa 404.0 - Fannst ekki** skilaboð þegar þú reynir að opna [!INCLUDE[prod_short](includes/prod_short.md)] og 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

*Laga:*

1. Í Microsoft Edge, ferðu í **Stillingar** > **Fótspor og heimildir svæðis** > **JavaScript**.
2. Framkvæmdu eitt af eftirfarandi skrefum. Veldu skrefið sem fyrirtækið þitt mælir með:

    - Færa **Leyft** til vinstri (slökkt). Síðan skal velja **Bæta við** og slá inn vistfang (URL) fyrir [!INCLUDE[prod_short](includes/prod_short.md)] í reitnum **Svæði**. Velja **Bæta við** að þessu loknu.
    - Færa **Leyft** til hægri (kveikt).

## Leyfa kökur úr Business Central

*Vandamál:*

Ef vafrinn leyfir ekki vafrakökur færðu eftirfarandi villu:

**Því miður fannst síðan ekki. Athugaðu netfangið og reyndu aftur.** 

*Laga:*

1. Í Microsoft Edge, ferðu í **Stillingar** > **Fótspor og heimildir svæðis** > **Fótspor og gögn svæðis**.
2. Færið **Leyfa vefsvæðum að vista og lesa kökugögn** til hægri (kveikt).  

## <a name="popup"></a>Leyfa sprettiglugga úr Business Central

[!INCLUDE[prod_short](includes/prod_short.md)] samþættist við nokkrar vörur. Í sumum tilfellum, eins og með Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] opnast eða „sprettiglugga“ í vörunni. Þessi eiginleiki krefst þess að vafrinn þinn leyfi sprettiglugga í [!INCLUDE[prod_short](includes/prod_short.md)].

*Vandamál:*

Ef verið er að læsa sprettiglugga fyrir [!INCLUDE[prod_short](includes/prod_short.md)] birtast skilaboð sem svipar til eftirfarandi skilaboða:

**Eitthvað fór úrskeiðis. Vafrinn kann að hindra sprettiglugga sem Business Central þarf á að halda.**

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
*Laga:*

1. Í Microsoft Edge, er farið í **Stillingar** > **Fótspor og heimildir svæðis** > **Sprettigluggar og áframsendingar**.
2. Færa **Lokað fyrir** til hægri (kveikt).
3. Veljið **Bæta við**. Í reitinn **Svæði** skal slá inn `https://businesscentral.dynamics.com` og síðan velja **Bæta við**.

## Sjá einnig .

[Úrræðaleit Teams](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
