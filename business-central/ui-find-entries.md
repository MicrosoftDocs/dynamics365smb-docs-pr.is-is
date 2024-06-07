---
title: Leit að tengdum færslum fyrir fylgiskjöl
description: 'Fræðast um hvernig finna má skjöl, viðskiptatengiliði og birgðafærslur sem tengjast hvert öðru.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: find
ms.search.form: 344
ms.date: 05/23/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="finding-related-entries-for-documents"></a>Leit að tengdum færslum fyrir fylgiskjöl

Fræðast um hvernig finna má skjöl og færslur sem tengjast hvert öðru út frá sameiginlegum upplýsingum, eins og:

- Númer fylgiskjals eða bókunardagsetning.
- Tegund viðskiptatengiliðs, númer eða númer utanaðkomandi skjals.
- Raðnúmer vöru eða lotunúmer.

Þessi eiginleiki er gagnlegur til að hafa upp á fjárhagsfærslum sem urðu til vegna ákveðinna viðskipta. Þegar leitað er eftir númeri fylgiskjals er hægt að prenta samantektina úr skýrslunni **Fylgiskjalafærslur** .

## <a name="get-started"></a>Hafist handa

Eiginleikinn Finna færslur er auðkennandi fyrir næstum hvaða síðu sem er með því að styðja á <kbd>lyklana Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Q</kbd> . Á síðum þar sem sérstaklega birtast bókuð skjöl eða bókaðar fylgiskjalafærslur&mdash; fyrir bæði lista og spjöld&mdash; er hægt að opna eiginleikann með því að velja aðgerðina **Finna færslur** .

Síðan **Finna færslur** nær til allra tengdra skjala og færslna sem byggð eru á númeri fylgiskjalsins og bókunardagsetningunni. Síðan skiptist í þrjá hluta:

- Efsti hlutinn sýnir reiti og aðgerðir sem eru notuð til að sía leitina.
- Miðhlutinn sýnir tengd skjöl samkvæmt leitinni.
- Neðsti hlutinn sýnir upplýsingar um upprunaskjalið sem fannst með leit.

## <a name="search-for-entries"></a>Leita að færslum

Hægt er að leita að færslum út frá upplýsingum um annaðhvort skjalið, viðskiptatengilið eða vörutilvísun. Efst er valinn einn af eftirfarandi valkostum á grundvelli upplýsingategundarinnar sem um er að ræða:

|Aðgerð|Heimildasamstæða|
|------|-----------|
| **Leita að skjölum** | Skoðið færslur út frá tilteknu skjalanúmeri eða bókunardagsetningu. |
| **Leita að viðskiptatengslum** | Skoða færslur sem byggðar eru á tiltekinni tegund tengiliðar, númeri tengiliðar og/eða númeri utanaðkomandi skjals. Síðasti valkosturinn gerir kleift að leita að lánardrottna- eða viðskiptamannaskjölum með því að nota númerið sem tengiliðurinn úthlutar. |
| **Leita að vörutilvísunum** | Skoða færslur byggðar á raðnúmeri eða lotunúmeri. Hægt er að færa inn lotunúmer eða raðnúmer, eða sía fyrir lotunúmerinu eða raðnúmerinu sem leita á að. Þessi aðgerð er gagnleg til að sjá hvar tiltekið vörurakningarnúmer var notað, frá hvaða lánardrottni það kom eða hvaða viðskiptamanni það var selt. |

Þegar búið er að velja eru viðeigandi leitarupplýsingar færðar inn efst á síðunni. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Að lokinni leit skal velja **Finna** til að hefja leitina. Ef einhverjum síunum er breytt þarf að velja **Leita** aftur.

> [!TIP]
> Til að fá nokkur dæmi um notkun **Leitarfærslna** er að finna [í Rekja vöruraktar vörur](inventory-how-to-trace-item-tracked-items.md) og [kynning: Rakning rað-lotunúmera](walkthrough-tracing-serial-lot-numbers.md).

## <a name="see-also"></a>Sjá einnig .

[Rekja vöruraktar vörur](inventory-how-to-trace-item-tracked-items.md)  
[Finna bókuð fylgiskjöl án færslu skjals á innleið](across-how-find-posted-documents-without-income-document-records.md)  
[Aðgengi og Flýtivísanir](ui-accessibility.md)  
[Vinna með Business Central](ui-work-product.md)  
[Bæta Síðuaðgerð við hlutverkamiðstöð](ui-bookmarks.md)  
[Finna síður og upplýsingar með Viðmótsleit](ui-search.md)  
[Finna síður með hlutverkaleit](ui-role-explorer.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
