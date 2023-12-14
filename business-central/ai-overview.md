---
title: Markaðssetningartextatillögur með yfirliti Copilot
description: Fá yfirlit yfir innihald myndaðs efnis í Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: overview
ms.date: 10/29/2023
ms.custom: bap-template
---
# Markaðssetningartextatillögur með yfirliti Copilot

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

Þessi grein veitir yfirsýn yfir Ónýta getu sem er veitt af Copilot í Business Central.

## Hvað er AI-powered vöru markaðssetning texti með Copilot?

Copilot veitir AI-öfluga aðstoð fyrir Business Central notendur sem eru ábyrgir fyrir markaðssetningartexta (vörulýsingar) á vörum sem seldar eru í netverslunum, eins og Shopify. Með því að smella á hnapp, býr Copilot til texta sem er að taka þátt og skapandi, og það auðkenna lykileigindir tiltekinnar vöru. Með smá yfirferð og ritfærslu er það tilbúið að birta.

Copilot notar [Microsoft Azure OpenAI Þjónustu](/azure/cognitive-services/openai/overview) til að fá aðgang að tungumálalíkönum sem þekkja, spá fyrir og búa til texta sem byggir á þjálfuðum gagnasöfnum.

<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RWZdAr]

*Myndbandið sýnir ekki nákvæmlega hvernig eiginleikinn virkar eða lítur út í vörunni. Þessi eiginleiki hefur breyst síðan myndbandið var framleitt. En það gefur þér almenna hugmynd um eiginleikann og til hvers þú getur notað hana.*
  
## Þar sem það er notað

Copilot er fáanlegt á birgðaspjöldum í Business Central. Í Business Central eru vörur eins og vörur í öðrum forritum og verslunum. Hægt er að stjórna hverri vöru á spjaldi þar sem færðar eru inn upplýsingar um vöruna, eins og víddir hennar, kostnað eða mynd. Á þessu spjaldi er einnig reitur til að færa inn markaðssetningartexta. Þennan markaðstexta er hægt að birta á netverslun þinni til að kynna vöruna. Hér kemur copilot. Með því að **velja uppkast með Copilot** aðgerð á birgðaspjaldinu býr Copilot til greindan uppkaststexta fyrir þig. Þegar þú hefur fengið fyrstu uppköstin geturðu keyrt Copilot aftur og aftur þangað til þú færð uppkast sem þú vilt. Þegar notandi hefur tillögu um það vistar þú hana og breytir henni svo til nákvæmni.

Ef Business Central er sett upp til að tengjast netversluninni þinni á Shopify getur þú tekið þennan texta enn frekar með því að birta hann með vörunni beint í verslunina með því að **velja Shopify** Bæta við.

## Hvers vegna og hvernig á að nota það

AI-myndaður texti getur hjálpað þér að flýta tímanlega á markaði vöru í netverslanir með því að takmarka tíma sem notaður er við afrit ritun. Sumir helstu kostir eru:

- Hjálpar notendum að sigrast á rithöfundarblokk með því að koma þeim í gang með greindum drögum.
- Aflæsir sköpunarkrafti til að veita fleiri vörulýsingar.
- Bætir samkvæmni markaðsefnis fyrir framleiðslulínur.

Aðeins ætti að líta á texta sem tillaga af *eiginleikum*. Tillögur geta í sumum tilvikum innihaldið mistök og jafnvel óviðeigandi texta, svo yfirsýn og endurskoðun manna sé nauðsynleg. Áður en textinn er tiltækur opinberlega þarf að fara yfir hann til nákvæmni og gera viðeigandi breytingar.

## Núgildandi takmarkanir

Þessi hluti útskýrir gildandi takmarkanir á textagetu sem Copilot veitir.

- [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]
- Lélegar tillögur geta leitt til þess að óljós eða almenn vöruheiti séu notuð og tiltekin atriði vantar, eins og lykileigindir eða tegund.
- Copilot er aðeins stutt á Business Central á netinu, ekki einka skýjaumhverfi eða Business Central umhverfi innanhúss.
- Copilot er ekki stutt í gegnum tengingar við eigin Azure-þjónustuforða OpenAI í Azure áskriftinni.

<!-- Partner extensibility of the AI capability by using AL code isn't supported.-->

## Næstu skref

Til að byrja þarftu Business Central (v23.1 og síðar) umhverfi sem er virkt með Copilot.

- Ef þú ert núverandi Business Central viðskiptavinur verður Business Central admin að setja upp umhverfi sem er virkt fyrir markaðssetningartextatillögur. Nánari upplýsingar eru í [Grunnstilling copilot og AI](enable-ai.md).

- Ef þú ert ekki Business Central viðskiptavinur en vilt prófa það getur þú skráð þig fyrir ókeypis prufuútgáfu. Frekari upplýsingar [fást í Skráðu þig fyrir ókeypis Dynamics 365 Business Central prufuútgáfu](trial-signup.md).

Þegar þú hefur umhverfi eða slóð sem er tilbúinn skaltu fara í [Bæta við markaðstexta við vörur með Copilot](item-marketing-text.md).  

## Sjá einnig .

[Grunnstilling copilot og AI-möguleika](enable-ai.md)  
[Bæta markaðssetningartexta við vörur með Afrita](item-marketing-text.md)  
[FAQ fyrir markaðssetningartextatillögur](faqs-marketing-text.md)  
[Hefjast handa með Shopify tengli](shopify/get-started.md)  
