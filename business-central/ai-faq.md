---
title: AI-knúinn markaðssetningartexti vöru (forskoðun) með eignaútgáfu copilot
description: Fá svör við algengum spurningum um textamöguleika sem myndaður er með Copilot.
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: faq
ms.date: 04/03/2023
ms.custom: bap-template
author: jswymer
ms.service: dynamics365-business-central
---

# AI-knúinn markaðssetningartexti vöru (forskoðun) með eignaútgáfu copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Þessi grein notar spurningar og svör til að útskýra mikilvæga þætti varðandi AI-tæknina á bak við Copilot og textann sem hún býr til.

## [Almennt](#tab/general)

### Hvað er Copilot?

Copilot leggur fram textatillögur með mynduðum texta fyrir vörur í Business Central. Það er ætlað notendum sem skrifa markaðssetningartexta fyrir vörur til að hjálpa þeim að framleiða þátttöku og sannfærandi efni. Sumir helstu kostir eru:

- Minnkar tímann sem notaður er við afritunarskrif, sem getur hraðað tímanlega á markaði fyrir vörur sem eru seldar í netverslunum.
- Aflæsir sköpunarkrafti til að veita fleiri vörulýsingar.
- Bætir samkvæmni markaðsefnis fyrir vörulínur.

Notendur ættu að líta á texta sem Þorvald sem tillögu sem þarf að endurskoða og breyta til nákvæmni áður en hann er tiltækur opinberlega.

### Af hverju er Copilot ekki tiltækt fyrir markaðssetningartexta á vörunum mínum í Business Central?

Til að Copilot sé tiltækt þarf að uppfylla eftirfarandi kröfur:

- Tungumálið sem þú notar á Business Central verður að vera enska. Allir tiltækir enskir heimamenn munu vinna, líkt og enska (bandaríska), enska (bretland), eða enska (Suður-Afríka).

  Til að breyta tungumálinu skal velja Stillingar í hægra horninu **Stillingar**  ![.](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") > **Mínar** > **stillingar**. Nánari upplýsingar eru í [Breyta grunnstillingum](ui-change-basic-settings.md#language).
- Þú verður að nota Business Central á netinu útgáfu 22 eða nýrri (ef þú ert núverandi viðskiptavinur) eða prufuútgáfu.  <!--**22.0.54157.54311 (Preview - Copilot edition)**-->

   Ef athuga á útgáfuna skal velja spurningarmerkið uppi í hægra horninu og velja **síðan Hjálp & stuðningur**. Undir **Úrræðaleit** skal leita að forritsútgáfunni. Til að fá upplýsingar um hvernig á að fá rétta forskoðunarútgáfu er farið í [Hafist handa með Business Central forskoðunarútgáfu](ai-preview-getstarted.md).
-  **Virkja verður eiginleikann Create AI-knúnar vörulýsingar með Copilot** .

   Frekari upplýsingar má fá með því að [fara í Gera virkar eða óvirkar "Búa til Óvirkar vörulýsingar með Copilot" eiginleikanum](enable-ai.md#enable-or-disable-create-ai-powered-product-descriptions-with-copilot).
- Stjórnandi hefur samþykkt skilmálana.

   Frekari upplýsingar má fá [í Samþykki til eða hafna forskoðunar- og persónuverndarskilmálum og skilyrðum allra notenda](enable-ai.md#consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users).

### Er Copilot tiltækt til forskoðunar í Business Central á staðnum?

Nei, það er sem stendur ekki stutt í Business Central á staðnum.

### Hvernig virkar Copilot, hvaðan kemur textinn sem lagður er til?

Copilot notar [Azure-þjónustu OpenAI](/azure/cognitive-services/openai/overview) Microsoft til að komast í öflug tungumálalíkön sem greina og búa til náttúrulegt tungumál. Þessi líkön hafa verið þjálfuð í meginmáli textagagnasafna. Því getur Copilot búið til tillögur, sérsniðin svör á ensku út frá lágmarksmagni af ílagsgögnum, eins og eigindum vöru, tegund eða lýsingu. 

### Hver eru gæði textans sem Copilot stingur upp á?

Þar sem undirliggjandi tækni á bak við Copilot notar AI sem hefur verið þjálfað á margs konar heimildum er myndað efnið ekki alltaf staðreynd eða hentugt. Sumar tillögur geta jafnvel falið í sér vafasamt eða óviðeigandi efni. Það er á ábyrgð þín að endurskoða og breyta tillögum sem gerðar eru til að tryggja að það sé rétt og viðeigandi.

Til að fá upplýsingar um óviðeigandi tillögur er farið [í Hvað er gert varðandi svívirðilegar og skaðlegar textatillögur?](/dynamics365/business-central/ai-faq?&tabs=oversight#whats-done-about-abusive-and-harmful-text-suggestions).

### Hvernig get ég bætt tillögurnar sem ég fæ frá Copilot?

Það er ýmislegt hægt að gera til að fá sem mest út úr tillögum frá Copilot:

- Bæta við fleiri eigindum við vöru til að kynna sértæka eiginleika og eiginleika sem þú hefur áhuga á.
- Breyta valkostum fyrir tón röddarinnar og áherslu á gæði til að uppfylla persónulegar óskir þínar.
- Bæta lýsingu vörunnar.
- Ganga þarf úr skugga um að vörunni sé úthlutað flokknum sem hentar best.

Til að fá nánari upplýsingar er farið í [Endurbætur og sniðið textatillögur](item-marketing-text.md#improve-and-tailor-text-suggestions).

### Hvað ef ég er ekki ánægður með myndaða textann?

Til að hjálpa okkur að bæta textann er **þetta góð tillaga?** á síðunni **Búa til með Copilot, sem hægt er að svara með þumalputtaskrá (mér líkar við hana) eða smámyndatöku (Þarfnast endurbóta**).

![Sýnir birgðaspjald með markaðssetningartextasvæði](media/create-with-copilot-window-feedback.png)

### Geta stjórnendur gert copilot óvirkan? Hvernig þá?

Business Central býður upp á tvær leiðir til að slökkva á Copilot í forskoðun:

- Vera ósammála Azure OpenAI persónuverndartilkynningu fyrir alla notendur.

  eða

- Slökkva á **vörulýsingum með Copilot með Copilot** á síðunni **Eiginleikastjórnun** .

Til að fræðast meira er farið í [Grunnstilla AI-knúinn markaðssetningartexta (forskoðun) með Copilot sem stjórnanda](enable-ai.md).

## [Sanngirni](#tab/fairness)

### Vinnur Copilot með önnur tungumál en ensku?

Eins og er styður Copilot aðeins ensku. Hægt er að skila ónákvæmum svörum þegar notendur tala við kerfið á öðrum tungumálum en ensku.

## [Yfirsjón manna](#tab/oversight)

### Hvað er gert varðandi sóðalegar og skaðlegar textatillögur?

Azure OpenAI þjónustan geymir kvaðningar og lokanir frá þjónustunni um að fylgjast með til svívirðilegrar notkunar og til að þróa og bæta gæði innihaldsstjórnunarkerfa Azure OpenAI. [Fræðast meira um innihaldsstjórnun okkar og afmörkun.](/azure/cognitive-services/openai/concepts/content-filter)

Viðurkenndir starfsmenn Microsoft fá aðgang að kvaðningu þinni og lokagögnum sem hafa sett sjálfvirk kerfi af stað í þeim tilgangi að rannsaka og sannreyna hugsanlega misnotkun; fyrir viðskiptamenn sem hafa virkjað Azure-þjónustu OpenAI innan Evrópusambandsins verður viðurkenndur starfsmaður Microsoft staðsettur í Evrópusambandinu. Gögnin geta verið notuð til að bæta innihaldsstjórnunarkerfin okkar.Ef um staðfest brot á stefnu er að ræða, gætum við beðið þig að grípa til tafarlausra aðgerða til að laga málið að málinu og koma í veg fyrir frekari misnotkun. Ef fjallað er um málið getur það leitt til frestunar eða þegar Azure-aðgangi OpenAI er hætt.

Nánari upplýsingar eru í [Gögn, persónuvernd og öryggi Azure-þjónustunnar OpenAI](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

### Get ég valið um skráningar- og mannaskoðunarferlið?  

Þegar Microsoft sér um forskoðun á Azure OpenAI mun Microsoft vinna og geyma gögn viðskiptavina sem send eru til þjónustunnar, sem og frálagsefnis, til þess að fylgjast með og koma í veg fyrir móðgandi eða skaðleg notkun eða úttak þjónustunnar; til að þróa, prófa og bæta möguleika sem hannaðir eru til að koma í veg fyrir svívirðilega notkun eða skaðleg frálag þjónustunnar. 

Viðurkenndir starfsmenn Microsoft geta skoðað gögn sem hafa sett sjálfvirk kerfi okkar af stað til að rannsaka og sannreyna hugsanlega misnotkun, og kann að taka þátt í takmörkuðum tilviljunarkenndum sýnatökum á hugtökum sem eru ekki merkt sjálfvirku kerfunum okkar til að tryggja að kerfin virki rétt. Viðurkenndir starfsmenn Microsoft geta einnig opnað og notað þessi gögn til að bæta kerfi okkar sem fylgjast með og koma í veg fyrir móðgandi eða skaðlega notkun eða úttak þjónustunnar.Lesa meira um [forskoðunarskilmála](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

## [Næði](#tab/privacy)

### Hvaða gögnum safnar möguleikinn? Hvernig eru gögn notuð?

Möguleikinn safnar svari **þínu við Er þetta góð tillaga?** spurninga á síðunni **Búa til með Copilot, sem getur verið annaðhvort þumalputta upp (mér líkar við hana) eða þumalputta (Þarfnast endurbóta**).

Við notum þessi gögn til að meta og bæta gæði getunnar. Nánari upplýsingar um það hvaða gögnum er safnað er að finna í [forskoðunarskilmálunum](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

![Sýnir birgðaspjald með markaðssetningartextasvæði](media/create-with-copilot-window-feedback.png)

---

## Sjá einnig .

[Yfirlit yfir AI-powered markaðssetningartexta vöru með Copilot](ai-overview.md)  
[Grunnstilla AI-knúinn markaðssetningartexta vöru með Copilot sem admin](enable-ai.md)  
[Búa til markaðssetningartexta fyrir vörur með Copilot](item-marketing-text.md)  

