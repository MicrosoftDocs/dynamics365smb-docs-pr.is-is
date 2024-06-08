---
title: Uppsetning vafrans
description: Lýsir því hvernig á að setja upp vafra til að vinna með Business Central og sasmþættum vörum.
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'Teams, web client, troubleshooting, errors'
ms.date: 12/04/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a>Uppsetning og úrræðaleit með vafra til að vinna með Business Central Web Client

Þessi grein útskýrir hvernig á að setja upp vafrann þannig að [!INCLUDE[web_client](includes/web_client.md)] og allir eiginleikar þess virki rétt. Lestu þessa grein ef þú átt í vandræðum með að [!INCLUDE[web_client](includes/web_client.md)] opna, stillingar vafrans geta verið orsök einhverra vandamála.

Í greininni er að finna upplýsingar fyrir uppsetningu Microsoft Edge, en kröfur um JavaScript, fótspor og sprettiglugga eru þær sömu fyrir alla studda vafra. Fyrir aðra vafra skal skoða leiðbeiningarnar sem framleiðandinn gefur upp.  

## <a name="use-a-supported-browser"></a>Notaðu studdan vafra

Gættu þess að nota einn af studdu vöfrunum. Sjá [Lágmarkskröfur fyrir notkun Business Central](product-requirements.md#browsers).

Mælt er með því að þú notir stöðugan rásarútgáfu af vafra þar sem það er áreiðanlegasta og stöðugasta útgáfan sem hefur gengist undir víðtæka prófun og galla festingu. Þetta tryggir að þú hafir bestu reynslu og eru minni líkur á að þú lendir í öllum vandamálum á meðan þú notar vefbiðlarann.  

## <a name="allow-javascript-from-business-central"></a>Leyfa JavaScript úr Business Central

*Vandamál:*

Ef vafrinn leyfir ekki JavaScript sést **NotSupported/DisabledJavaScript** á slóðarstikunni og **HTTP-villa 404.0 - Ekki fundin** skilaboð þegar reynt er að opna [!INCLUDE[prod_short](includes/prod_short.md)] og 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

*Laga:*

1. Í Microsoft Edge, ferðu í **Stillingar** > **Fótspor og heimildir svæðis** > **JavaScript**.
2. Framkvæmdu eitt af eftirfarandi skrefum. Velja skal skrefið sem fyrirtækið mælir með:

    - Færa **Leyft** til vinstri (slökkt). Síðan skal velja **Bæta við** og slá inn vistfang (URL) fyrir [!INCLUDE[prod_short](includes/prod_short.md)] í reitnum **Svæði**. Velja **Bæta við** að þessu loknu.
    - Færa **Leyft** til hægri (kveikt).

## <a name="allow-cookies-from-business-central"></a>Leyfa kökur úr Business Central

*Vandamál:*

Ef vafrinn leyfir ekki kökur birtist eftirfarandi villa:

**Því miður fannst síðan ekki. Athugaðu netfangið og reyndu aftur.** 

*Laga:*

1. Í Microsoft Edge, ferðu í **Stillingar** > **Fótspor og heimildir svæðis** > **Fótspor og gögn svæðis**.
2. Færið **Leyfa vefsvæðum að vista og lesa kökugögn** til hægri (kveikt).  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a>Leyfa sprettiglugga úr Business Central

[!INCLUDE[prod_short](includes/prod_short.md)] samþættist við nokkrar vörur. Í sumum tilfellum, eins og með,opnast Microsoft Teams [!INCLUDE[prod_short](includes/prod_short.md)]  eða "sprettigluggar" innan vörunnar. Þessi eiginleiki krefst þess að vafrinn þinn leyfi sprettiglugga í [!INCLUDE[prod_short](includes/prod_short.md)].

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

## <a name="see-also"></a>Sjá einnig .

[Úrræðaleit Teams](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
