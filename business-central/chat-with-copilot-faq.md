---
title: Spjall við eignaspjall (Copilot FaQ)
description: Þessi grein svarar nokkrum algengum spurningum um spjall við Copilot í Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 05/17/2024
ms.custom: bap-template jswymer
---
# Spjall við eignaspjall (Copilot FaQ)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Þessi grein svarar nokkrum algengum spurningum um að spjalla við Copilot í [!INCLUDE[prod_short](includes/prod_short.md)]. Fyrir spurningar sem tengjast AI og spjalli skal leita ráða [hjá Ábyrgum algengum spurningum um spjall við Copilot](faqs-chat-with-copilot.md).

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Geta stjórnendur veitt eða neitað heimildum einstakra notenda til að fá aðgang að spjalli?

Nei, það er engin heimild til að spjalla. Ef spjall er virkjað á síðunni [Copilot og ÓNægir](enable-ai.md) hafa allir notendur í umhverfi aðgang að spjalli.
 
## Er spjall í boði á spjaldtölvu, síma eða öðrum þáttum eyðublaða?

Nei, spjallsvæðið er aðeins tiltækt á vefbiðlaranum [!INCLUDE[web_client](includes/web_client.md)] .

## Ég nota ekki Business Central á ensku. Hver eru mínir valkostir?

Spjall er aðeins í boði á ensku. Hægt er að breyta tungumáli notanda í ensku í [Mínar stillingar](ui-change-basic-settings.md#language).

## Hvaða Business Central útgáfu þarf ég að upplifa spjall?

Spjall er fáanlegt í opinberu forskoðun frá útgáfu 24.0 (2024 útgáfubylgju 1).

## Vinnur spjall við sérstillingarnar mínar?

Það fer eftir tegund spurningarinnar sem þú spyrð Copilot. Dæmi:

- Þegar spurt er um spurningar um að finna færslur finnur Copilot færslur í sérsniðnum töflum sem eru auðkenndar með sérsniðnum reitum.
- Þegar þú biður um útskýringar eða leiðbeiningar hefur Copilot ekki aðgang að neinum upplýsingum um sérstillingarnar þínar eða fylgiskjöl með viðbótunum þínum.

## Copilot virðist aldrei opna færsluna eða síðuna sem ég bað um. Hvað er ég að gera rangt?

Þegar copilot er beðið um að finna færslur [!INCLUDE[prod_short](includes/prod_short.md)] birtast allar færslur sem það finnur sem valkostlegar flísar eða tengla á spjallsvæðinu. Með forskoðun færir Copilot ekki sjálfkrafa á neinar síður.

## Svörin sem ég fæ frá Copilot eru mismunandi þótt ég spyrji sömu spurningarinnar. Er þetta galli?

Copilot gæti stundum svarað á mismunandi hátt. Svörin eru ekki endilega eins.

## Hvenær á ég að nota afritið í spjallskilaboðum?

Hægt er að nota hnappinn Afrita til að afrita skilaboð frá fyrra samtali við Copilot, líma það í ílagsreitinn til að reyna aftur eða reyna afbrigði af skeytinu til Copilot.

## Hvernig sérstilli ég eða lengi spjall?

Í forskoðun er ekki hægt að breyta spjallsvæðinu og svörum Copilot á nokkurn hátt með sérstillingu, innbótum eða sérstillingum.

## Finnur Copilot gögn í öðrum fyrirtækjum eða umhverfi?

Copilot leitar aðeins að færslum í fyrirtækinu sem þú ert skráð(ur) inn í&mdash; jafnvel þótt fyrirtækið noti mörg umhverfi eða fyrirtæki til að aðskilja gögn.

## Spjallsvæði Copilot birtist ekki. Hvað get ég gert?

Athuga hvort notandatungumálið í Mínar stillingar er stillt á ensku og að umhverfi notanda sé útgáfu 24.0 eða síðar. Á síðunni Copilot og AI Geta ganga úr skugga um að stjórnendur hafi kveikt á samþykki fyrir gögnum í landafræði og hafi spjall virkt. Gættu þess að staðfæring umhverfisins sé ekki Kanada.

Ef þú sérð samt ekki spjallið við Copilot eiginleikann er mögulegt að Microsoft velti eiginleikunum áfram út á svæðið þitt. Copilot veltir sér fyrst til viðskiptavina Bandaríkjanna í apríl 2024 og síðan yfir vikurnar fer þaðan að öðrum staðfæringum á löndum/svæðum.

## Af hverju sýnir Copilot aðeins þrjár færslur á spjallsvæðinu?

Þegar copilot er beðið að sækja færslur ákvarðar það hvernig Copilot auðkennir og notar afmarkanir á síðum til að finna það sem leitað er að. Til að halda svörum þjöppuðum og nákvæmum birtir Spjallsvæðið mest þrjár færsluflísar, jafnvel þegar Copilot finnur stærri fjölda viðeigandi færslna.

## Copilot skilar röngum svörum við samtölum og öðrum útreikningum

Spjall við Copilot getur fundið færslur, útskýrt hugtök og leiðbeiningar um hvernig á að ljúka verkum í Business Central. Önnur notkunarmál eru ekki studd, svo sem að bæta upp reit þvert á færslur eða reikna út meðaltal mánaðarlegrar upphæðar. Við vonumst til að bæta grunnstærðfræðigetu við Copilot í framtíðinni.

## Get ég notað ræðu í stað þess að slá inn kvaðningar?

Þú getur spjallað við Copilot með því að nota raddritun til að tala í stað þess að rita orðin þín á spjallsvæðið. Röddritun notar talgreiningu á netinu og er fáanlegt með Windows. Til að nota rödd skal virkja spjallskilaboðareitinn og nota <kbd>síðan Windows</kbd>+<kbd>H</kbd> flýtivísunina og byrja að tala. Nánari upplýsingar eru [í Nota raddritun til að tala í stað tegundar á tölvunni](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## Næstu skref

[Spjalla við Copilot (forskoðun)](chat-with-copilot.md)
