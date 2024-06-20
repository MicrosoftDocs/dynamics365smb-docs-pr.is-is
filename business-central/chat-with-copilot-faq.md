---
title: Spjall við eignaspjall (Copilot FaQ)
description: 'Lærðu að spjalla við Copilot, raunverulegur aðstoðarmaður sem hjálpar þér að nota Business Central. Finna svör við algengum spurningum um spjallaðgerðir, stillingar og takmarkanir.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 06/13/2024
ms.custom: bap-template jswymer
---
# Spjall við eignaspjall (Copilot FaQ)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Þessi grein svarar nokkrum algengum spurningum um að spjalla við Copilot í [!INCLUDE[prod_short](includes/prod_short.md)]. Fyrir spurningar sem tengjast AI og spjalli skal leita ráða [hjá Ábyrgum algengum spurningum um spjall við Copilot](faqs-chat-with-copilot.md).

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Geta stjórnendur veitt eða neitað heimildum einstakra notenda til að fá aðgang að spjalli?

Nei, það er engin heimild til að spjalla. Ef spjall er virkjað á síðunni [Copilot og ÓNægir](enable-ai.md) hafa allir notendur í umhverfi aðgang að spjalli.
 
## Er spjall í boði á spjaldtölvu, síma eða öðrum þáttum eyðublaða?

Nei, spjallsvæðið er aðeins tiltækt á vefbiðlaranum [!INCLUDE[web_client](includes/web_client.md)] .

## Ég nota ekki Business Central á ensku. Hver eru mínir valkostir?

Eins og er er spjall aðeins í boði á ensku. Hægt er að breyta tungumáli notanda í ensku í [Mínar stillingar](ui-change-basic-settings.md#language).

## Hvaða útgáfu af Business Central þarf ég að spjalla?

Spjall er fáanlegt í opinberu forskoðun frá útgáfu 24.0 (2024 útgáfubylgju 1).

## Vinnur spjall við sérstillingarnar mínar?

Það fer eftir tegund spurningarinnar sem þú spyrð Copilot. Dæmi:

- Ef spurt er hvort leita eigi að færslum er hægt að finna færslur í sérsniðnum töflum sem nota sérsniðna reiti.
- Ef þú biður Copilot um útskýringar eða leiðbeiningar hefur það ekki aðgang að neinum upplýsingum um sérstillingarnar þínar eða fylgiskjöl með viðbótunum þínum.

## Hvernig opna ég færslu eða síðu með spjalli?

Þegar copilot er beðið um að finna færslur [!INCLUDE[prod_short](includes/prod_short.md)] birtast allar færslur sem það finnur sem valkostlegar flísar eða tengla á spjallsvæðinu. Með forskoðun færir Copilot ekki sjálfkrafa á neinar síður.

## Hvers vegna fæ ég mismunandi svör frá Copilot fyrir sömu spurningu?

Copilot gæti stundum svarað á mismunandi hátt. Svörin eru ekki alltaf eins.

## Hvernig nota ég afritunaraðgerðina í spjallskilaboðum?

Hægt er að nota hnappinn Afrita til að afrita skilaboð frá fyrra samtali við Copilot, líma það í ílagsreitinn til að reyna aftur eða reyna afbrigði af skeytinu til Copilot.

## Get ég sérstillt eða lengt spjall?

Í forskoðun er ekki hægt að breyta spjallsvæðinu og svörum Copilot á nokkurn hátt með sérstillingu, innbótum eða sérstillingum.

## Leitar Copilot að gögnum í öðrum fyrirtækjum eða umhverfi?

Copilot leitar aðeins að færslum hjá fyrirtækinu sem þú ert skráður inn á. Hún leitar ekki að gögnum í mörgum umhverfi eða fyrirtækjum.

## Hvað get ég gert ef spjallsvæðið sýnir ekki?

Athuga hvort notandatungumálið í **Mínar** stillingar er stillt á ensku og að umhverfi notanda sé útgáfu 24.0 eða síðar. Á síðunni Copilot og AI Geta er gengið úr skugga um að stjórnandinn hafi kveikt á samþykki fyrir gögnum þvert á landafræði og hafi spjall. Einnig skal ganga úr skugga um að staðfæring umhverfisins sé ekki Kanada.

Ef þú sérð samt ekki spjallið við Copilot eiginleikann er mögulegt að Microsoft velti eiginleikunum áfram út á svæðið þitt. Copilot valtaði til viðskiptavina Bandaríkjanna fyrst í apríl 2024 og síðan yfir vikurnar fer þaðan til annarra landa/svæða staðfæringa.

## Af hverju sýnir Copilot aðeins þrjár færslur á spjallsvæðinu?

Þegar þú biður Copilot að finna færslur ákvarðar það hvernig Copilot auðkennir og notar afmarkanir á síðum til að finna það sem leitað er að. Til að halda svörum nákvæmum birtir Spjallsvæðið mest þrjár færsluflísar, jafnvel þegar Copilot finnur viðeigandi færslur.

## Af hverju gefur Copilot röng svör við útreikningum?

Spjall við Copilot getur hjálpað þér að finna færslur, útskýra hugtök og leiðbeina þér um hvernig á að ljúka verkum í Business Central. Önnur notkunarmál eru ekki studd, svo sem að bæta upp reit þvert á færslur eða reikna út meðaltal mánaðarlegrar upphæðar. Við vonumst til að bæta grunnstærðfræðigetu við Copilot í framtíðinni.

## Get ég notað ræðu í stað þess að slá inn kvaðningar?

Þú getur spjallað við Copilot með því að nota raddritun til að tala í stað þess að rita orðin þín á spjallsvæðið. Röddritun notar talgreiningu á netinu og er fáanlegt með Windows. Til að nota rödd skal virkja spjallskilaboðareitinn, nota <kbd>síðan Windows</kbd>+<kbd>H</kbd> flýtivísunina og byrja að tala. Nánari upplýsingar eru [í Nota raddritun til að tala í stað tegundar á tölvunni](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## Næstu skref

- [Spjalla við Copilot (forskoðun)](chat-with-copilot.md)
