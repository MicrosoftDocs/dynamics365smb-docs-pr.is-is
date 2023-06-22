---
title: FAQ markaðstexta vöru (Forskoðun) með hjálp Copilot
description: Fáðu svör við algengum spurningum um formyndaða textamöguleika með Copilot.
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: faq
ms.date: 04/03/2023
ms.custom: bap-template
author: jswymer
ms.service: dynamics365-business-central
---

# <a name="ai-powered-item-marketing-text-preview-with-copilot-faq" />FAQ markaðstexta vöru (Forskoðun) með hjálp Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Þessi grein notar spurningar og svör til að útskýra mikilvæga þætti um Al tækni bak við Copilot og textann sem hún myndar.

## [Almennt](#tab/general)

### <a name="what-is-copilot" />Hvað er Copilot?

Copilot veitir AI-myndaða texta tillögur um atriði í Viðskiptamiðinu. Hún er ætluð fyrir notendur sem skrifa markaðstexta fyrir vörur til að hjálpa þeim að framleiða þátt og sannfærandi efni. Nokkur lykilávinningur er meðal annars:

- Minnkar tímann sem notaður er við ljósritunarpappír, sem getur flýtt tíma til markaðunar á vörum sem seldar eru í verslunum á netinu.
- Aflæsir sköpun til að veita meiri þátt vörulýsingar.
- Bætir samræmi markaðsefnis fyrir vörulínur.

Notendur skulu hafa í huga þann texta sem þarf að yfirfara og breyta fyrir nákvæmni áður en hann er aðgengilegur opinberlega.

### <a name="why-isnt-copilot-available-for-marketing-text-on-my-items-in-business-central" />Af hverju er Copilot ekki til staðar fyrir markaðstexta á vörum mínum í Viðskiptamiðinu?

Til að Copilot séu tiltæk þarf að uppfylla eftirfarandi kröfur:

- Tungumálið sem þú notar í Viðskiptamiðinu verður að vera Enskt. Eitthvert af tiltækum enskum staðin mun virka, eins og Enska (Bandaríkin), Enska (Bretland), eða Enska (Suður-Afríka).

  Til að breyta tungumálinu, efst í hægra horninu, skaltu velja stillingar fyrir  **stillingar**  teikni ![...](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð"). > **Stillingar** > **tungumáls**. Frekari upplýsingar er að fara í breytingar á  [grunnstillingum](ui-change-basic-settings.md#language).
- Þú verður að vera að nota viðskipti Miðnetaútgáfu 22 eða nýrri (ef þú ert viðskiptavinur) eða réttara.  <!--**22.0.54157.54311 (Preview - Copilot edition)**-->

   Til að athuga útgáfuna velurðu spurningarmerkið efst í hægra horninu, velur  **þá hjálp & stuðning**. Leita að útgáfu hugbúnaðarins undir  **Úrræðaleit**. Til að fá upplýsingar um rétta Forskoðun útgáfu er farið í  [hafist handa með aðalforskoðun á fyrirtæki](ai-preview-getstarted.md).
-  **Create AI-knúin vörulýsingar með Copilot**  verða að vera virkar.

   Frekari upplýsingar er að fara í til að  [gera eða slökkva á "Create AI vörulýsingum með Copilot '](enable-ai.md#enable-or-disable-create-ai-powered-product-descriptions-with-copilot).
- Admin hefur samþykki á skilmálum og skilyrðum.

   Frekari upplýsingar er  [að leita í samþykkis á eða hafna forskráningu og persónuverndarskilmálum og skilyrðum fyrir alla notendur](enable-ai.md#consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users).

### <a name="is-copilot-available-for-preview-in-business-central-on-premises" />Er Copilot fáanleg fyrir forskoðun í Business miðlægt innanhúss?

Nei, það er nú ekki stutt í viðskiptafræði miðsvæðis innanhúss.

### <a name="how-does-copilot-work-where-does-the-suggested-text-come-from" />Hvernig virkar Copilot, Hvaðan kemur leiðbeinandi textinn?

Copilot notar  [Azure OpenAI þjónustuna](/azure/cognitive-services/openai/overview)  til að nálgast öflug tungumálalíkön sem greina og mynda náttúruleg tungumál. Þessi líkön hafa verið þjálfuð á breiðum megintexta af datamengi textana. Þar af leiðandi geta Copilot myndað leiðbeinandi, persónuleg svör á ensku Byggt á lágmarks inntaksgögnum, líkt og eigindum vöru, tegund eða lýsingu. 

### <a name="whats-the-quality-of-the-text-suggested-by-copilot" />Hver er gæði textans sem lagður er til við Copilot?

Þar sem undirliggjandi tækni á bak við Copilot notar AI sem hefur verið þjálfuð á margs konar uppruna, þá er myndað efni ekki alltaf efnismikið eða hentugt. Sumar tillögur geta jafnvel falið í sér vafasamt eða óviðeigandi efni. Það er á þína ábyrgð að endurskoða og breyta myndaðir tillögur til að tryggja það réttmætt og viðeigandi.

Upplýsingar um óviðeigandi uppákomur er farið í  [það sem gert er um móðgandi og skaðlegar textatillögur?](/dynamics365/business-central/ai-faq?&tabs=oversight#whats-done-about-abusive-and-harmful-text-suggestions).

### <a name="how-can-i-improve-the-suggestions-i-get-from-copilot" />Hvernig get ég bætt úr þeim tillögum sem ég fæ frá Copilot?

Það eru nokkur atriði sem þú getur gert til að fá sem mest út úr tillögum frá Copilot:

- Bæta fleiri eigindum við vöru til að stuðla að þeim sértækari eiginleikum og eiginleikum sem þú hefur áhuga á.
- Breyta valkostum fyrir tón rödd og áherslu á gæði til að stemma stigu við persónulegum óskum þínum.
- Bæta lýsingu vörunnar.
- Gakktu úr skugga um að vörunni sé úthlutað heppilegasta flokknum.

Til að fá frekari upplýsingar er farið í að  [bæta og sníða tillögur](item-marketing-text.md#improve-and-tailor-text-suggestions) að texta.

### <a name="what-if-im-not-satisfied-with-the-generated-text" />Hvað ef ég er ekki sáttur við myndaða textann?

Til að hjálpa okkur að bæta textann, valið  **er þetta góð uppákoma?**  **á vefsíðunni Create with Copilot**, sem þú getur svarað með þumalfingurs-upp (mér líst vel á það) eða Þumalputtareglur (þarfnast úrbóta).

![Sýnir birgðaspjald með rúðu Markaðstexta](media/create-with-copilot-window-feedback.png)

### <a name="can-admins-disable-copilot-if-so-how" />Má viðurkenningar gera við copilot? Ef svo er, hvernig?

Miðborg býður viðurkenningar tvær leiðir til að gera Kópavog óvirka í forskoðun:

- Ósammála að Azure opni persónuverndartilkynningu fyrir alla notendur.

  eða

- Slökkva á  **Create-AI vörulýsingum með Copilot**  -aðgerðinni á  **síðunni Feature Management** .

Til að fá frekari upplýsingar er farið í að  [samskipa texta um MARKAÐSSETNINGU AI-vara (Preview) með Copilot sem admin](enable-ai.md).

## [Sanngirni](#tab/fairness)

### <a name="does-copilot-work-with-languages-other-than-english" />Virkar Copilot með tungumálum öðrum en ensku?

Eins og er, styður Copilot aðeins ensku. Rangar svör kunna að skila sér þegar notendur samtengjast kerfinu á tungumálum öðrum en ensku.

## [Mannlegu yfirsjónir](#tab/oversight)

### <a name="whats-done-about-abusive-and-harmful-text-suggestions" />Hvað er gert um móðgandi og skaðlegar texttillögur?

Azure OpenAI þjónustan geymir kvaðningar og margbreytileika úr þjónustunni til að fylgjast með að móðgandi notkun og að þróa og bæta gæði hiure OpenAI efnisstjórnunarkerfa fyrirtækisins. [Lærðu meira um efnistjórnun okkar og síun.](/azure/cognitive-services/openai/concepts/content-filter)

Starfsmenn Microsoft hafa aðgang að kvaðningu og gögnum sem hafa komið upp í sjálfvirku kerfi okkar í þeim tilgangi að rannsaka og sannprófa hugsanlega misnotkun. fyrir viðskiptavini sem hafa virkjað Azure OpenAI þjónustuna í Evrópusambandinu verða starfsmenn Microsoft í notendaþjónustu í Evrópusambandinu. Þessi gögn má nota til að bæta okkar efniskerfi.Ef um staðfest brot á reglu er að ræða biðjum við þig að grípa tafarlaust til aðgerða til úrbætur á málefninu og til að fyrirbyggja frekari misnotkun. Bilun í aðsetri úthreyfinga getur orðið til þess að frestun eða uppsögn á Azure OpenAI tilfangsaðgangi er sinnt.

Nánari upplýsingar er að finna  [í gögnum, persónuvernd og öryggi hjá Azure OpenAI þjónustunni](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

### <a name="can-i-opt-out-of-the-logging-and-human-review-process" />Get ég valið úr skógarhöggi og manna endurskoðunarferli?

Sem hluti af því að veita Azure OpenAI foryfirlitunum, mun Microsoft vinna og geyma gögn viðskiptavinar sem send eru til þjónustunnar, ásamt frálagsefni, til þess að fylgjast með og koma í veg fyrir móðgandi eða skaðlegar not eða fráhald þjónustunnar; og til að þróa, prófa og bæta getu sem ætlað er að koma í veg fyrir móðgandi notkun eða skaðleg áhrif af þjónustunni. 

Með viðurkenndum Microsoft-starfsmönnum er heimilt að fara yfir gögn sem hafa ræst út í kerfum okkar til að rannsaka og sannreyna hugsanlega misnotkun og geta tekið þátt í takmörkuðum sýnum af hugtökum sem ekki eru í sjálfvirkum kerfum okkar til að tryggja að kerfin virki eðlilega. Starfsmenn Microsoft geta einnig fengið aðgang að og notað þessi gögn til að bæta okkar kerfi sem fylgjast með og koma í veg fyrir móðgandi eða skaðleg not eða fráleit þjónustu.Lesa meira um  [forskoðunarskilmála](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

## [Persónuvernd](#tab/privacy)

### <a name="what-data-does-the-capability-collect-how-is-the-data-used" />Hvaða gögnum safnar hæfileiki? Hvernig eru gögnin notuð?

Hæfileiki safnar þínu svari til  **er þetta góð uppákoma?**  Spurning um að búa til  **með Copilot**  síðu, sem getur verið annað hvort þumalfingur-upp (mér líkar það) eða þumalfingurs-niður (þarf framför).

Við notum þessi gögn til að meta og bæta gæði þeirrar getu. Frekari upplýsingar um hvaða gögnum er safnað er að finna í  [forskoðunarskilmálum](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

![Sýnir birgðaspjald með rúðu Markaðstexta](media/create-with-copilot-window-feedback.png)

---

## <a name="see-also" />Sjá einnig .

[Yfirlit um markaðssetningu á AI-knúinn vöru með Copilot](ai-overview.md)  
[Skilgreina markaðstexta með AI-knúinn vöru með Copilot sem admin](enable-ai.md)  
[Stofna markaðstexta fyrir vörur með Copilot](item-marketing-text.md)  

