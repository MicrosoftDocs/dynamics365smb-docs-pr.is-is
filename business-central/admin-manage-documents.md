---
title: Stjórna geymslu með því að eyða skjölum eða þjappa gögnum
description: Kynntu þér hvernig hægt er að vinna úr uppsöfnun á gömlum skjölum (og draga úr gagnamagninu sem geymt er í gagnagrunni) með því að eyða eða þjappa gögnum.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '107, 9035, 9040'
ms.date: 04/16/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Stjórna geymslu með því að eyða skjölum eða þjappa gögnum

Meginhlutverk, t.d. kerfisstjóri, þarf reglulega að sjá um þau gögn sem safnast upp, eyða þeim eða þjappa þau.  

> [!TIP]
> Frekari upplýsingar um aðrar leiðir til að draga úr magni gagna sem vistuð eru í gagnagrunni með því að lesa [Draga úr gögnum sem eru geymd í gagnagrunnum Business Central](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) í fylgiskjölum Developer og IT Pro.

## Eyða skjölum.

Við vissar kringumstæður gæti þurft að eyða reikningsfærðum innkaupapöntunum. Hins vegar er ekki hægt að eyða þeim nema vörurnar hafi verið reikningsfærðar og mótteknar að fullu. [!INCLUDE[prod_short](includes/prod_short.md)] hjálpar þér með því að athuga með það.

Fyrirtæki eyða yfirleitt vöruskilapöntunum þegar þær hafa verið reikningsfærðar. Þegar reikningur er bókaður færir [!INCLUDE [prod_short](includes/prod_short.md)]  hann á síðuna **Bókaður innkaupakreditreikningur** . Ef gátreiturinn **Vöruskilaafhending á kreditreikningi** hefur verið valinn á síðunni **Innkaupagrunnur** er reikningurinn fluttur á síðuna **Bókuð skilaafhending**. Hægt er að eyða skjölunum með því að nota keyrsluna **Eyða reiknf. innk.vöruskilapönt.**. Áður en hún eyðir skjölum athugar keyrslan hvort innkaupaskilapantanirnar séu afhentar að fullu og reikningsfærðar.  

Standandi innkaupapöntunum er ekki sjálfkrafa eytt eftir vinnslu og allar tengdar innkaupapantanir eru reikningsfærðar. Í staðinn er hægt að eyða þeim í runuvinnslunni **Eyða reikningsfærðum standandi innkaupapöntunum**.  

Fyrirtæki eyða yfirleitt reikningsfærðum þjónustupöntunum sjálfkrafa eftir að þær hafa verið reikningsfærðar að fullu. Þegar reikningur er bókaður er samsvarandi færsla stofnuð á síðunni **Bókaðir þjónustureikningar** þar sem hægt er síðan að skoða hann.  

Þjónustupöntunum er hins vegar ekki eytt sjálfvirkt ef heildarmagn pöntunarinnar var bókað af síðunni **Þjónustureikningur** í staðinn fyrir þjónustupöntunina sjálfa. Hugsanlega þarf að eyða slíkum reikningsfærðu pöntunum handvirkt með því að keyra keyrsluna **Eyða reikningsf. þjónustupöntunum** .  

## Þjappa gögnum með dagsetningarþjöppun

Hægt er að þjappa gögnum í [!INCLUDE [prod_short](includes/prod_short.md)] til að spara pláss í gagnagrunninum, sem í [!INCLUDE [prod_short](includes/prod_short.md)] á netinu getur jafnvel sparað þér peninga. Þjöppunin, sem byggir á dagsetningum og aðgerðum, sameinar nokkrar eldri færslur í eina nýja færslu.

Hægt er að þjappa færslum sem uppfylla öll eftirfarandi skilyrði:

* Þær eru frá lokuðum fjárhagsárum.
* Reiturinn **Opið** er stilltur á **Nei**.
* Þær eru að minnsta kosti fimm ára gamlar. Ef þjappa á gögnum sem eru yngri en fimm ára skaltu hafa samband við samstarfsaðila þinn hjá Microsoft.

Þannig má til að mynda þjappa lánardrottnafærslum síðustu fjárhagsára þannig að á hverjum reikningi sé einungis ein kreditfærsla og ein debetfærsla fyrir hvern mánuð. Upphæðin í nýju færslunni er samtala allra þjöppuðu færslnanna. Dagsetningin sem er úthlutað er upphafsdagsetning þjappaðs tímabils, eins og fyrsti dagur mánaðarins (ef færslum er þjappað eftir mánuðum). Að þjöppun lokinni er eftir sem áður hægt að skoða nettóbreytingar fyrir hvern reikning á fyrra fjárhagsári.

Fjöldi færslna frá dagsetningarþjappa ræðst af því hve mikið var afmarkað, hvaða reitir voru tengdir saman og hvaða tímabilslengd var valin. Það er alltaf minnst ein færsla. Þegar runuvinnslu er lokið má sjá útkomuna á síðunni **Skráningar dags.þjöppunar**.

Hægt er að þjappa eftirfarandi gerðum gagna með runuvinnslum.

* Fjármálafærslur - fjárhagsfærslur, VSK-færslur, bankareikningsfærslur, fjárhagsáætlunarfærslur, viðskiptamannafærslur og lánardrottnafærslur.
* Vöruhúsafærslur
* Tilfangafærslur
* Birgðaáætlunarfærslur
* Fjárhagsfærslur eigna, viðhaldsbókarfærslur eigna og vátryggingafærslur eigna.

Þegar verið er að skilgreina skilyrði fyrir þjöppunina er hægt að halda efni tiltekinna reita með valkostunum undir **Varðveita reitainnihald**. Tiltækir reitir fara eftir gögnunum sem eru þjöppuð.

> [!NOTE]
> Áður en þú getur keyrt dagsetningarþjöppun þarf greiningaryfirlitið að vera uppfært. Frekari upplýsingar er að finna í hlutanum [Uppfæra greiningaryfirlit](bi-how-analyze-data-dimension.md#update-an-analysis-view).

Eftir þjöppunina er efni eftirfarandi reita alltaf varðveitt: **Bókunardagsetning**, **Númer lánardrottins**, **Tegund fylgiskjals**, **Gjaldmiðilskóði**, **Bókunarflokkur**, **Upphæð**, **Eftirstöðvar**, **Upphafleg upph. (SGM)**, **Eftirstöðvar (SGM)**, **Upphæð (SGM)**, **Innkaup (SGM)**, **Reikningsafsl. (SGM)**, **Veittur greiðsluafsláttur (SGM)** og **Mögul. að jafna greiðsluafsl.**.

## Bókun þjappaðra færslna

Þjöppaðar færslur eru bókaðar aðeins öðruvísi en stöðluð bókun. Þessi mismunur er að fækka nýjum fjárhagsfærslum sem stofnaðar eru eftir dagsetningarþjöppun og skiptir sérstaklega miklu máli þegar upplýsingum á borð við víddir og númer fylgiskjala eru geymdar. Dagsetningarþjöppun stofnar nýjar færslur á eftirfarandi hátt:

* Á síðunni **Fjárhagsfærslur** eru nýjar færslur stofnaðar fyrir þjöppunarfærslurnar. Reiturinn **Lýsing** inniheldur **Dags. þjöppuð** þannig að auðvelt sé að bera kennsl á þjöppuðu færslurnar. 
* Á síðum fjárhags, eins og á síðunni **Fjárhagsfærslur**, eru ein eða fleiri færslur stofnaðar. 

Bókunarferlið stofnar eyður í númeraröðinni fyrir færslur síðunni **Fjárhagsfærslur**. Þessum númerum er aðeins úthlutað á færslurnar á fjárhagssíðum. Númerabilið sem var úthlutað á færslurnar er í boði á síðunni **Fjárhagsdagbók** í reitinum **Frá færslunr.** og **Til færslunr.**. 

> [!NOTE]
> Þegar dagsetningarþjöppun hefur verið keyrð er ekki hægt að bakfæra lánardrottna- eða bankafærslur fyrir færslur sem verða fyrir áhrifum af þjöppuninni.

Fjöldi færslna frá dagsetningarþjöppun ræðst af því hve margar síur voru valdar, hvaða reitir eru sameinaðir og lengd tímabilsins sem þú velur. Það er alltaf minnst ein færsla.

> [!WARNING]
> Dagsetningaþjöppun eyðir færslum svo að tryggara er að taka alltaf afrit af gagnasafni áður en keyrslan er sett í gang.

### Að keyra gagnaþjöppun

1. Velja skal táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn"), slá inn **Gagnaumsjón** og velja svo viðeigandi tengil.
2. Eitt af eftirfarandi er gert eftir þörfum:
    * Til að nota leiðbeiningar um uppsetningu með aðstoð til að setja upp gagnaþjöppun fyrir eina eða fleiri tegundir gagna skaltu velja **Leiðbeiningar um gagnaumsjón**.
    * Til að setja upp þjöppun fyrir eina gagnagerð skal velja **Gagnaþjöppun**, **Þjöppunarfærslur**, síðan velja gögnin sem á að þjappa.

   > [!NOTE]
   > Aðeins er hægt að þjappa gögnum sem eru eldri en fimm ára. Ef þjappa á gögnum sem eru yngri en fimm ára skaltu hafa samband við samstarfsaðila þinn hjá Microsoft. Þeir þurfa að nota atburðinn `OnSetMinimumNumberOfYearsToKeep` í "Dagsetningaþjöppun" codeunit til að stilla þröskuldinn.


## Sjá einnig .

[Stjórnun](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
