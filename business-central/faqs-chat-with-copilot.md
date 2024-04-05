---
title: Ábyrg algengar spurningar fyrir spjall við copilot (forskoðun)
description: 'Þessi algenga spurning veitir upplýsingar um AI-tæknina sem notuð er til að spjalla við Copilot í Business Central. Í honum eru lykilatriði og upplýsingar um notkun ÓM, hvernig það var prófað og metið og allar sérstakar takmarkanir.'
ms.date: 03/18/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI, chat'
---
# Ábyrg algengar spurningar fyrir spjall við copilot (forskoðun)

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

Þessar algengu spurningar (FAQ) lýsa algengum áhrifum spjalls við Copilot í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef þú hefur áhuga á almennum spurningum um notkun eiginleikans skaltu fara [í algengar spurningar í spjalli við Copilot](chat-with-copilot-faq.md).

## Hvað er Spjall við copilot?

Microsoft Copilot er AI-powered aðstoðarmaður sem hjálpar neista sköpunarkrafti, uppörva framleiðni og útrýma leiðinlegum verkefnum. Þú getur spjallað við Copilot í Business Central til að svara spurningum og fundið viðskiptagögn með því að tjá það sem þú ert að leita að á náttúrulegu tungumáli.

Spjall við Copilot, einnig kallað spjall, er gagnvirkur eiginleiki sem svarar spurningum og finnur viðskiptagögn tengd [!INCLUDE[prod_short](includes/prod_short.md)], án þess að notendur þurfi að fletta upp á notandaviðmótinu eða vörufylgigögnunum. Copilot-svæðið er tiltækt hvar sem er í biðlaranum [!INCLUDE[prod_short](includes/prod_short.md)] .

Notendur spyrja spurninga á náttúrulegu tungumáli, eins og "Hvernig skila ég vörum til viðskiptavina minna beint frá lánardrottnum mínum?" Eða "Erum við með skrifstofustóla á lager fyrir $600?" Til að svara gefur Copilot svör á náttúrulegu tungumáli. Svörin geta innihaldið venjulegan texta, tengla á færslur eða síður í [!INCLUDE[prod_short](includes/prod_short.md)] og tengla til að [!INCLUDE[prod_short](includes/prod_short.md)] hjálpa greinum með Microsoft Learn.

## Hvað er hægt að spjalla við Copilot?

Hægt er að spjalla við Copilot til að fá svör við eftirfarandi spurningaflokkum:

### Útskýra og fylgja

Notendur geta beðið Copilot að útskýra sérstakt hugtak sem tengist [!INCLUDE[prod_short](includes/prod_short.md)], eins og hvað eru víddir, eða veitt leiðbeiningar um hvernig eigi að ljúka verki, eins og hvernig á að bóka sölupöntun. Copilot leitar í opinberum [!INCLUDE[prod_short](includes/prod_short.md)] fylgiskjölum sem Microsoft hefur gefið út og gefur út svar sem byggir á heimildum.

- Copilot notar þekkinguna á Microsoft Learn  (ekki breiða vefleit) til að leita aðeins í dynamics 365 fylgiskjölum með [!INCLUDE[prod_short](includes/prod_short.md)]  Dynamics 365 Microsoft Learn.

- Copilot grípur ekki til aðgerða, býr til ný gögn eða breytir stillingum. Það tekur einfaldlega saman allar málsgreinar sem finnast um Microsoft Learn spurninguna eða spjallið í spjallinu.

### Finna viðskiptagögn og tengdar síður

Notendur geta beðið Copilot að finna síður með nafni eða beðið um færslur sem byggðar eru á reitum og hömlum. Ef Copilot finnur samsvörun svarar það með tengli á viðeigandi færslu eða síðu, sem notandinn getur valið að opna.

- Copilot breytir inntaki náttúrulegs tungumáls í fyrirspurn sem samanstendur af töfluleit, röðun og afmörkunarskilyrðum.

  Getan nýtir [!INCLUDE[prod_short](includes/prod_short.md)] leitarmöguleika móðurgagna til að finna samsvarandi gögn úr töflum í gagnagrunni fyrirtækja. Leitin liggur undir eigin kenni notandans fyrir öryggi og samræmi. Hún leitar ekki utan gagnagrunnsins [!INCLUDE[prod_short](includes/prod_short.md)] .

- Copilot grípur ekki til aðgerða, býr til ný gögn eða breytir stillingum. Hún tekur aðeins saman þær færslur sem bárust frá gagnaleitinni. [!INCLUDE[prod_short](includes/prod_short.md)]  

## Hver er tilætluð notkun Spjalls við Copilot?

Spjall er hannað til að nota fyrirtækjanotkun og svara spurningum sem tengjast [!INCLUDE[prod_short](includes/prod_short.md)] og þeim viðskiptagögnum sem hann inniheldur. Eiginleikinn styrkir fólk til að leysa algeng verk eins og að finna færslur eða fá leiðbeiningar með því að tjá sig með eigin orðum, auðvelda og aðgengilegra að vinna með [!INCLUDE[prod_short](includes/prod_short.md)].

## Hvernig var Spjall við Copilot metið? Hvaða mælieiningar eru notaðar til að mæla afköst?

- Aðgerðin gekkst undir umfangsmikla prófun þar sem fjölmargir enskir textar sem ná yfir margs konar efnisatriði og tjáningarstíla voru gefnir Copilot. Niðurstaðan var metin gegn nákvæmni, vægi og öryggi.
- Eiginleikinn er byggður upp samkvæmt staðlinum Ábyrgur AI-staðall Microsoft. [Fræðast meira um ábyrgt ÓM frá Microsoft](https://aka.ms/RAI).

## Hvernig fylgist Microsoft með gæðum myndaðs efnis?

Microsoft hefur mismunandi kerfi til að tryggja að efni sem Copilot myndar sé í hæsta gæðaráði, finni fyrir misnotkun og tryggi öryggi fyrir viðskiptavini okkar og gögn þeirra.

Notendur geta veitt endurgjöf við öllum svörum copilot og gefið skýrslu um ónákvæmt eða óviðeigandi efni til að gera Microsoft kleift að endurbæta þessa aðgerð. 

- Notandi veitir svörun með því að nota táknið like (þumlur upp) eða mislíkar (þumlur niður) á **Copilot** svæðinu á [!INCLUDE[prod_short](includes/prod_short.md)].
- Við greinum og nýtum endurgjöf notenda á þeim eiginleika til að hjálpa okkur að bæta svörun.
- Ef óviðeigandi myndað efni kemur upp skal tilkynna það til Microsoft með því að nota þetta svarglugga: [Tilkynna misnotkun](https://go.microsoft.com/fwlink/?linkid=2249810).
- Microsoft gæti slökkva á copilot-knúnum aðgerðum fyrir tilgreinda viðskiptamenn ef misnotkun á virkninni finnst.

## Hvaða takmarkanir eru á spjall við Copilot? Hvernig geta notendur minnkað áhrif spjallsins með takmörkunum copilot þegar kerfið er notað?

- Almennar takmarkanir AI

  Al-kerfi eru verðmæt verkfæri, en þau eru óákægð. Efnið sem þær mynda má ekki vera alveg nákvæmt. Svo er mikilvægt að nota dómgreind þína til að fara yfir og staðfesta viðbrögð Copilot áður en ákvarðanir sem gætu haft áhrif á hagsmunaaðila eins og viðskiptamenn og samstarfsaðila. Til flestra svara inniheldur Copilot einnig vitnanir eða tilvísunartengla sem hægt er að nota til að sannreyna fljótt hvort Copilot sé komið að réttu svari. Þegar hann er til dæmis spurður hvernig eigi að framkvæma einhver verk inniheldur Copilot tengla á upprunagreinina. Þegar hann er beðinn að finna færslu sem byggir á tilteknum skilyrðum inniheldur Copilot tengla sem lýsa listasíðunni sem hún er skilgreind sem efnisatriði samræðu, sem og allar afmarkanir eða röðun sem var beitt til að fá svar.

- Takmarkanir á tungumáli

  - Spjall er aðeins stutt á ensku fyrir eftirfarandi heimamenn: en-AU, en-CA, en-GB, en-IE, en-Í-NZ, en-PH, en-SG, en-US, en-ZA.

    Ef tungumálið [!INCLUDE[prod_short](includes/prod_short.md)] á skjánum er ekki eitt af þessum heimamönnum er spjallið ekki tiltækt.

  - Gæði svara geta verið lægri við eftirfarandi skilyrði:
    - Tungumálastaðurinn er eitthvað annað en en en í Bandaríkjunum.
    - Þegar tungumálastilling notanda er [!INCLUDE[prod_short](includes/prod_short.md)] frábrugðin aðaltungumáli gagna í gagnagrunninum [!INCLUDE[prod_short](includes/prod_short.md)] .

- Sértækar takmarkanir á iðnaði, vöru og efnisatriði

   Spjallið felur í sér innbyggðar öryggisbúnaðar sem koma í veg fyrir óæskilega myndun skaðlegs efnis, svo sem kynferðislega skýrt efni eða ofbeldis. Stundum starfa viðskiptavinir í atvinnugreinum, selja vörur og þjónustu eða vinna við ferli sem skarast náttúrulega við það sem gæti talist óviðeigandi í öðru samhengi, eða unnið með gögn sem gætu kallað á þessa öryggisverði. Spjall gæti ekki framkvæmt eins vel í þessum tilvikum.

<!--## What operational factors and settings allow for effective and responsible use of the feature?-->

## Hvaða gögnum spjall við Copilot safnar og hvernig það er notað

Microsoft notar ekki gögn fyrirtækisins, þ.m.t. textann sem sendur er til Copilot, til að þjálfa grunngerðir notenda til hagsbóta fyrir aðra. Stjórnendur fyrirtækisins hafa fulla stjórn á því að stjórna þessum gögnum sem eru hluti af Azure-áskrift þeirra. Þar sem stjórnendur eða aðrir innan fyrirtækisins gætu haft aðgang að þessum gögnum samkvæmt ákvörðun vinnuveitanda er mælt með því að notendur færi ekki inn viðkvæm gögn, svo sem aðgangsorð eða önnur leyndarmál.

## Hvað býður Spjall við Copilot um öryggi

Spjall er hannað til að vera öruggt og keyrt undir auðkenni notandans, erfa allar öryggisheimildir og aðrar takmarkanir og starfa aldrei utan [!INCLUDE[prod_short](includes/prod_short.md)] öryggis á vettvangi. Það þýðir að Copilot hefur aðeins aðgang að gögnum sem notandinn hefur aðgang að.

Fyrir notendur með SUPER heimild getur spjall auðveldara að finna ótryggð gögn sem yfirleitt er erfiðara að komast til fyrir aðra notendur. Fyrirtæki sem ekki nota öryggislíkan beita [!INCLUDE[prod_short](includes/prod_short.md)] til að takmarka hvaða töflur og hlutir sem hver notandi eða hlutverk notanda hefur aðgang að, gætu verið í aukinni hættu þegar spjall er notað. Þess vegna er mælt með því að fyrirtækið innleiði [!INCLUDE[prod_short](includes/prod_short.md)] öryggislíkanið eða slökkvi á spjalli.

## Sjá einnig .

[Spjalla við Copilot (forskoðun)](chat-with-copilot.md)

