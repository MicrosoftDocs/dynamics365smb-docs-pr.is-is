---
title: Stjórna geymslu með því að eyða skjölum eða þjappa gögnum
description: Fáið upplýsingar um hvernig hægt er að geyma söguleg gögn með því að þjappa fjárhagsfærslum, eða eyða þeim.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f0d713f57345c312ddbfe6b5462f2623b1088dfc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753868"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Stjórna geymslu með því að eyða skjölum eða þjappa gögnum

Meginhlutverk, t.d. kerfisstjóri, þarf reglulega að sjá um þau gögn sem safnast upp, eyða þeim eða þjappa þau.  

> [!TIP]
> Frekari upplýsingar um aðrar leiðir til að draga úr magni gagna sem vistuð eru í gagnagrunni er að finna í [Draga úr gögnum sem eru geymd í gagnagrunnum Business Central](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) í Developer og IT Pro Help.

## <a name="delete-documents"></a>Eyða skjölum

Í vissum tilvikum kann að þurfa að eyða reikningsfærðum innkaupapöntunum sem ekki hefur verið eytt. [!INCLUDE[prod_short](includes/prod_short.md)] kannar hvort eyddu innkaupapantanirnar hafa verið reikningsfærðar að fullu. Ekki er hægt að eyða pöntunum sem hafa ekki verið fullkomlega reikningsfærðar og mótteknar.  

Vöruskilapöntunum er yfirleitt eytt þegar þær hafa verið reikningsfærðar. Þegar reikningur er bókaður er hann fluttur á síðuna **Bókaður innkaupakreditreikningur**. Ef gátreiturinn **Vöruskilaafhending á kreditreikningi** hefur verið valinn á síðunni **Innkaupagrunnur** er reikningurinn fluttur á síðuna **Bókuð skilaafhending**. Hægt er að eyða skjölunum með því að nota keyrsluna **Eyða reiknf. innk.vöruskilapönt.**. Áður en eytt er, athugar runuvinnslan hvort innkaupaskilapantanirnar séu að fullu afhentar og reikningsfærðar.  

Standandi pöntunum er ekki eytt eftir að allar tengdar innkaupapantanir hafa verið unnar og reikningsfærðar. Hægt er að eyða standandi pöntunum með keyrslunni **Reikningsfærðum standandi innkaupapöntunum eytt**.  

Þjónustupöntunum er yfirleitt eytt sjálfkrafa þegar þær hafa verið reikningsfærðar til fulls. Þegar reikningur er bókaður er samsvarandi færsla stofnuð á síðunni **Bókaðir þjónustureikningar** . Hægt er að skoða bókaða fylgiskjalið á síðunni **Bókaður þjónustureikningur**.  

Forritið eyðir þjónustupöntun ekki sjálfkrafa ef heildarmagn pöntunarinnar hefur verið bókað af síðunni **Þjónustureikningur** en ekki í þjónustupöntuninni sjálfri. Þá þarf að eyða bókuðum pöntunum sem ekki var búið að eyða. Hægt er að gera það með því að nota keyrsluna **Eyða reikningsfærðum þjónustupöntunum**.  

## <a name="compress-data-with-date-compression"></a>Þjappa gögnum með dagsetningarþjöppun

Hægt er að þjappa gögnum í [!INCLUDE [prod_short](includes/prod_short.md)] til að spara pláss í gagnagrunninum, sem í [!INCLUDE [prod_short](includes/prod_short.md)] á netinu getur jafnvel sparað þér peninga. Þjöppunin byggir á dagsetningum og vinnu með því að sameina margar gamlar færslur í eina nýja færslu. Einungis er hægt að þjappa færslum reikningsára sem búið er að loka, og aðeins lánardrottnafærslum þar sem reiturinn **Opið** er stilltur á *Nei*.  

Þannig má til að mynda þjappa lánardrottnafærslum umliðinna reikningsára þannig að á hverjum reikningi sé einungis um að ræða eina kreditfærslu og eina debetfærslu fyrir hvern mánuð. Upphæðin í nýju færslunni er samtala allra þjöppuðu færslnanna. Dagsetningin sem færslan hlýtur er upphafsdagsetning tímabilsins sem er þjappað, til dæmis fyrsti dagur mánaðarins (ef færslunum er þjappað eftir mánuðum). Eftir þjöppunina er enn hægt að sjá hreyfingar fyrir hvern reikning reikningsársins á undan.

Fjöldi færslna frá dagsetningarþjappa ræðst af því hve mikið var afmarkað, hvaða reitir voru tengdir saman og hvaða tímabilslengd var valin. Það verður alltaf til minnst ein færsla. Þegar keyrslu er lokið má sjá útkomuna á síðunni **Dags.þjöppun dagbóka**.

Hægt er að þjappa eftirfarandi gagnagerðum í [!INCLUDE [prod_short](includes/prod_short.md)] með runuvinnslum:

* Bankareikningsfærslur

  Eftir þjöppunina, með aðgerðinni **Varðveita reitaefni** má varðveita efni reitanna **Númer fylgiskjalsTengiliður okkar**, **Deildarkóði 1** og **Verkefniskóði 2**.
* Lánardr.færslur

  Eftir þjöppunina er efni eftirfarandi reita alltaf varðveitt: **Bókunardagsetning**, **Númer lánardrottins**, **Tegund fylgiskjals**, **Gjaldmiðilskóði**, **Bókunarflokkur**, **Upphæð**, **Eftirstöðvar**, **Upphafleg upph. (SGM)**, **Eftirstöðvar (SGM)**, **Upphæð (SGM)**, **Innkaup (SGM)**, **Reikningsafsl. (SGM)**, **Veittur greiðsluafsláttur (SGM)** og **Mögul. að jafna greiðsluafsl.**.

  Með aðgerðinni **Varðveita innihald reita** er líka hægt að varðveita efni þessara viðbótarreita: **Númer fylgiskjals**, **Númer afh.aðila**, **Kóði innkaupaaðila**, **Alvíddarkóði 1** og **Alvíddarkóði 2**.

> [!NOTE]
> Eftir að dagsetningarþjöppun er keyrð eru allir lyklar í fjárhagnum læstir. Til dæmis er ekki hægt að aftengja fjárhagsfærslur lánardrottna eða banka fyrir neina reikninga á tímabilinu þar sem dagsetningar eru þjappaðar.

<!--* General ledger entries
* Customer ledger entries-->
<!--* Fixed asset ledger entries
* G/L budget entries
* VAT entries

  After the compression the contents of the following fields are always retained: **Posting Date**, **Type**, **Closed**, **Gen. Bus. Posting Group**, **Gen. Prod. Posting Group**, **VAT Calculation Type**, **Base**, and **Amount**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Bill-to/Pay-to No.**, **EU 3-Party Trade**, **Country/Region Code**, and **Internal Ref. No.**.
* Insurance ledger entries
* Maintenance ledger entries
* Resource ledger entries

  After the compression, the contents of the following fields are retained: **Posting Date**, **Resource No.**, **Resource Group No.**, **Entry Type**, **Quantity**, **Total Cost**, **Total Price**, and **Chargeable**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Work Type Code**, **Job No.**, **Unit of Measure Code**, **Source Type**, **Source No.**. **Chargeable**, **
* Warehouse entries

  After the compression the contents of the following fields are always retained: **Registering Date**, **Location Code**, **Zone Code**, **Bin Code**, **Item No.**, **Quantity**, **Qty. (Base)**, **Bin Type Code**, **Entry Type**, **Variant Code**, **Qty. per Unit of Measure**, **Unit of Measure Code**, **Warranty Date**, **Expiration Date**, **Cubage**, and **Weight**.

  With the **Retain Field Contents** facility, you can also retain the contents of the **Serial No.** and **Lot No.** fields. -->

Fjöldi færslna sem keyrsla dagsetningaþjöppunar skilar veltur á fjölda afmarkana, reitum sem eru sameinaðir og þeirri lengd tímabils sem valin er. Það verður alltaf til minnst ein færsla. 

> [!WARNING]
> Dagsetningaþjöppun eyðir færslum svo að tryggara er að taka alltaf afrit af gagnasafni áður en keyrslan er sett í gang.

Eftirfarandi tafla sýnir reitina í flýtiflipanum **Valkostir** sem eru í boði í öllum runuvinnslum. Hlutinn **Varðveita reitainnihald** inniheldur viðbótarreiti sem lýst er hér að ofan.

|Svæði  |Description  |
|-------|-------------|
|Upphafsdagur     |Hér er færð inn upphafsdagsetning þjöppunarinnar. Þjöppunin mun hafa áhrif á allar færslur frá þessari dagsetningu til lokadagsetningarinnar.|
|Lokadagsetning     |Hér er skráð lokadagsetning þjöppunarinnar. Þjöppunin mun hafa áhrif á allar færslur frá upphafsdagsetningu til þessarar dagsetningar.|
|Lengd tímabils |Lengd þess tímabils sem sameina á færslur í er valið. Til að sjá valkostina skal velja reitinn. Ef valin var tímabilslengdin *Fjórðungur*, *Mánuður* eða *Vika* eru eingöngu færslur með sama reikningstímabil þjappaðar.|
|Varðveita reitainnihald     |Gátmerki eru sett í reitina ef á að varðveita efni tiltekinna reita jafnvel þótt færslunum sé þjappað. Því fleiri reitir sem eru valdir, þeim mun ítarlegri verða þjöppuðu færslurnar. Ef enginn þessara reita er valinn býr keyrslan til eina færslu fyrir hvern dag, viku eða annað tímabil, í samræmi við það tímabil sem valið er í reitnum **Lengd tímabils**. |

## <a name="see-also"></a>Sjá einnig

[Stjórnun](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]