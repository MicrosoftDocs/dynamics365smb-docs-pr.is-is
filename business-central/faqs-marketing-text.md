---
title: FAQ fyrir markaðssetningartextatillögur
description: 'Þessi faQ veitir upplýsingar um AI-tæknina sem notuð er í markaðstextatillögum í Business Central, ásamt lykilatriðum og upplýsingum um notkun AI, hvernig það var prófað og metið og allar sérstakar takmarkanir.'
ms.date: 10/07/2023
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.collection:
  - bap-ai-copilot
---

# <a name="faq-for-marketing-text-suggestions-with-copilot"></a>FAQ fyrir markaðssetningartextatillögur með Copilot

Algengar spurningar (FAQ) lýsa algengum áhrifum eiginleikans [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] í [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="what-is-item-marketing-text-suggestions"></a>Hvað er markaðssetningartexti vöru?

Copilot veitir notendum aðstoð sem ber ábyrgð á markaðssetningartexta (einnig þekkt sem afrit) á vörum í [!INCLUDE[prod_short](includes/prod_short.md)]. Þessi aðgerð er þekkt sem [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]. Eiginleikinn [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] veitir notendum aðstoð sem ber ábyrgð á markaðssetningartexta (einnig þekkt sem *afrit*) á vörum í [!INCLUDE[prod_short](includes/prod_short.md)].

Aðgerðin er tiltæk á hvaða birgðaspjaldi sem er á [!INCLUDE[prod_short](includes/prod_short.md)]. Til að nota hana er vara opnuð og síðan valin **markaðssetning textadrög** > **með Copilot**. Þessi aðgerð býr sjálfkrafa til textatillögu sem er að taka þátt, skapandi og sértæk fyrir vöruna sem er birt. Tillögur eru byggðar á ýmsum ílögum, þar á meðal:

- Eigindir vörunnar, tegund og heiti.
- Eigin kjörstillingar ritstíls, eins og tónn rödd, áhersla gæði, snið og lengd.

Hægt er að breyta gildi þessara ílagsvalkosta til að hafa áhrif á niðurstöðu textans AI-mynda. Áður en tillaga er vistuð er auðvelt að fara yfir hana og breyta henni til nákvæmni eða reyna aðra tillögu.

Sumir helstu kostir þessa eiginleika eru:

- Minnkar tímann sem notaður er við afritunarskrif, sem getur hraðað tímanlega á markaði fyrir vörur sem eru seldar í netverslunum.
- Aflæsir sköpunarkrafti til að veita fleiri vörulýsingar.
- Bætir samkvæmni markaðsefnis fyrir vörulínur.

## <a name="what-are-the-systems-capabilities"></a>Hver er hæfileiki kerfisins?

Eiginleikinn [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] notar [Azure-þjónustu OpenAI](/azure/cognitive-services/openai/overview) Microsoft til að fá aðgang að öflugum tungumálalíkönum sem greina og búa til náttúrulegt tungumál. Þessi líkön hafa verið þjálfuð í meginmáli textagagnasafna. Því getur Copilot búið til tillögur, sérsniðin svör á ensku út frá lágmarksmagni af ílagsgögnum, eins og eigindum vöru, tegund eða lýsingu. 

## <a name="what-is-the-systems-intended-use"></a>Hver er tilætluð notkun kerfisins?

Þessi aðgerð er ætluð til að aðstoða notendur við stofnun markaðssetningartexta fyrir vörur í [!INCLUDE[prod_short](includes/prod_short.md)]. Rithöfundar nota eiginleikann til að fá fljótt sannfærandi og taka þátt í textatillögum, sem síðan eru skoðaðar og breytt fyrir nákvæmni. 

## <a name="how-was-item-marketing-text-evaluated-what-metrics-are-used-to-measure-performance"></a>Hvernig var texti markaðssetningar metinn? Hvaða mælieiningar eru notaðar til að mæla afköst?

- Eiginleikinn gekkst undir umfangsmikla prófun þar sem margir textar á mismunandi tungumálum voru metnir af tungumálasérfræðingum gegn ýmsum skilyrðum. Prófunin var byggð á [!INCLUDE[prod_short](includes/prod_short.md)] gögnum um sýni og öðrum ímynduðum vörulistum.
- Þessi eiginleiki er byggður upp samkvæmt staðlinum Ábyrgur AI-staðall Microsoft. [Fræðast meira um ábyrgt ÓM frá Microsoft](https://aka.ms/RAI).

## <a name="how-does-microsoft-monitor-the-quality-of-generated-content"></a>Hvernig fylgist Microsoft með gæðum myndaðs efnis?

Microsoft hefur mismunandi kerfi til að tryggja að Copilot getu haldist rekstrarhæf og mynda efni í hæsta gæðamálum.

- Notendur hafa tækifæri til að gefa ábendingar um að gefa skýrslu um óviðeigandi efni og bæta virknina.

  - Ef óviðeigandi myndað efni kemur upp skal tilkynna það til Microsoft með því að nota þetta svarglugga: [Tilkynna misnotkun](https://go.microsoft.com/fwlink/?linkid=2249810). 

    Microsoft gæti slökkva á copilot-knúnum aðgerðum fyrir tilgreinda viðskiptamenn ef misnotkun á virkninni finnst. 

  - Við rekja endurgjöf [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] til að hjálpa okkur að bæta tillögur. 

    Þú veitir svörun með því að nota eins (þumlur upp) eða mislíkar (þumlur niður) á **Copilot** síðunni í [!INCLUDE[prod_short](includes/prod_short.md)]. Við söfnum saman fjarmælingum þessara bendinga fyrir hvert frálag sem notandi sendir inn ábendingar fyrir.

    ![Sýnir birgðaspjald með markaðssetningartextasvæði](media/create-with-copilot-window-feedback.svg)

- Azure OpenAI þjónustan geymir kvaðningar og lokanir frá þjónustunni um að fylgjast með til svívirðilegrar notkunar og til að þróa og bæta gæði innihaldsstjórnunarkerfa Azure OpenAI. [Fræðast meira um efnisstjórnun okkar og afmörkun.](/azure/cognitive-services/openai/concepts/content-filter). Fyrirtækisgögnin þín eru ekki notuð til að þjálfa AI-gerðir í Azure-þjónustunni OpenAI .

   Viðurkenndir starfsmenn Microsoft fá aðgang að kvaðningu og lokum gagna sem hafa sett sjálfvirkt kerfi af stað í þeim tilgangi að rannsaka og sannreyna hugsanlega misnotkun; fyrir viðskiptamenn sem nota [!INCLUDE[prod_short](includes/prod_short.md)] innan Evrópusambandsins eru viðurkenndir starfsmenn Microsoft staðsettir í Evrópusambandinu. Gögnin geta verið notuð til að bæta innihaldsstjórnunarkerfin okkar. Ef um staðfest brot á stefnu er að ræða, gætum við beðið þig að grípa til tafarlausra aðgerða til að laga málið að málinu og koma í veg fyrir frekari misnotkun. Ef fjallað er um málið getur það leitt til frestunar eða þegar Azure-aðgangi OpenAI er hætt.

   Nánari upplýsingar má fá með því að leita ráða [hjá Gögnum, persónuvernd og öryggi Azure-þjónustunnar OpenAI](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

## <a name="is-there-a-logging-and-human-review-process-as-part-of-azure-openai-service-and-if-so-can-i-opt-out"></a>Er til skráningar- og mannaskoðunarferli sem hluti af Azure OpenAI Service, og ef svo er, get ég valið það?

Þegar Microsoft veitir Azure OpenAI þjónustuna mun Microsoft vinna og geyma gögn viðskiptavina sem send eru til þjónustunnar, sem og frálagsefnis, til þess að fylgjast með og koma í veg fyrir móðgandi eða skaðlega notkun eða úttak þjónustunnar; til að þróa, prófa og bæta möguleika sem hannaðir eru til að koma í veg fyrir svívirðilegt notkun eða skaðleg frálag þjónustunnar. 

Viðurkenndir starfsmenn Microsoft geta skoðað gögn sem hafa sett sjálfvirk kerfi okkar af stað til að rannsaka og sannreyna hugsanlega misnotkun, og kann að taka þátt í takmörkuðum tilviljunarkenndum sýnatökum á hugtökum sem eru ekki merkt sjálfvirku kerfunum okkar til að tryggja að kerfin virki rétt. Viðurkenndir starfsmenn Microsoft geta einnig opnað og notað þessi gögn til að bæta kerfi okkar sem fylgjast með og koma í veg fyrir móðgandi eða skaðlega notkun eða úttak þjónustunnar.Lesa meira um [forskoðunarskilmála](https://go.microsoft.com/fwlink/?linkid=2189520).

Til að Microsoft gæti þjónustunnar og viðskiptavina hennar er ekki hægt að kjósa út úr skráningar- og mannaskoðunarferlum.

## <a name="what-data-does-the-capability-collect-how-is-the-data-used"></a>Hvaða gögnum safnar möguleikinn? Hvernig eru gögn notuð?

Tillögur um markaðssetningartexta safnar lágmarksgögnum sem Business Central krefst til að bjóða þjónustuna. Nánari upplýsingar eru í [Dynamics 365 terms for Azure-powered OpenAI eiginleikar](https://go.microsoft.com/fwlink/?linkid=2236010).

Möguleikinn safnar einnig gögnum frá svörunarnotandanum með því að nota eins og (þumla upp) eða ólík (þumlur niður) tákn efst **á Copilot** síðunni. Gögnin eru nafnlaus og felur í sér val á eins og ot mislíkindi, mislíkindaástæðunni ef það er kveðið á um og copilot aðgerðin sem svörunin gildir fyrir. Við notum þessi gögn til að meta og bæta gæði getunnar.

## <a name="what-are-the-limitations-of--how-can-users-minimize-the-impact-of-the-includefeature-marketing-text-suggestions-limitations-when-using-the-system"></a>Til hvers eru takmarkanir á [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]? Hvernig geta notendur minnkað áhrif takmarkananna [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] þegar kerfið er notað?

- Þar sem undirliggjandi tækni á bak við eiginleikann notar ÓM sem hefur verið þjálfað á margs konar heimildum, er myndað efnið ekki alltaf staðreynd eða hentugt. Sumar tillögur geta jafnvel falið í sér vafasamt eða óviðeigandi efni. Það er á ábyrgð þín að endurskoða og breyta tillögum sem gerðar eru til að tryggja að það sé rétt og viðeigandi.

- Tiltæk tungumál
  
   [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-system"></a>Hvaða rekstrarþættir og stillingar leyfa skilvirka og ábyrga notkun kerfisins?

Það eru nokkur atriði sem hægt er að gera til að ná sem mest út úr eiginleikanum:

- Bæta við fleiri eigindum við vöru til að kynna sértæka eiginleika og eiginleika sem þú hefur áhuga á.
- Breyta valkostum fyrir tón röddarinnar og áherslu á gæði til að uppfylla persónulegar óskir þínar.
- Bæta lýsingu vörunnar.
- Ganga þarf úr skugga um að vörunni sé úthlutað flokknum sem hentar best.

Til að fá nánari upplýsingar er farið í [Endurbætur og sniðið textatillögur](item-marketing-text.md#improve-and-tailor-text-suggestions).

> [!TIP]
> Skoða alltaf tillögur um nákvæmni áður en þær eru vistaðar og þær birtar til opinberrar notkunar.


## <a name="see-also"></a>Sjá einnig .

- [Tillögur um markaðssetningu texta](ai-overview.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
