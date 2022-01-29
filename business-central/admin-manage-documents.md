---
title: Stjórna geymslu með því að eyða skjölum eða þjappa gögnum
description: Kynntu þér hvernig hægt er að vinna úr uppsöfnun á gömlum skjölum (og draga úr gagnamagninu sem geymt er í gagnagrunni) með því að eyða eða þjappa gögnum.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.form: 107, 9040
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: edd23c8dcb7e129446a8f3d0180fcd107d08fa02
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/19/2022
ms.locfileid: "8011466"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Stjórna geymslu með því að eyða skjölum eða þjappa gögnum

Meginhlutverk, t.d. kerfisstjóri, þarf reglulega að sjá um þau gögn sem safnast upp, eyða þeim eða þjappa þau.  

> [!TIP]
> Frekari upplýsingar um aðrar leiðir til að draga úr magni gagna sem vistuð eru í gagnagrunni er að finna í [Draga úr gögnum sem eru geymd í gagnagrunnum Business Central](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) í fylgiskjölum Developer og IT Pro.

## <a name="delete-documents"></a>Eyða skjölum

Í vissum tilvikum kann að þurfa að eyða reikningsfærðum innkaupapöntunum sem ekki hefur verið eytt. [!INCLUDE[prod_short](includes/prod_short.md)] kannar hvort eyddu innkaupapantanirnar hafa verið reikningsfærðar að fullu. Ekki er hægt að eyða pöntunum sem hafa ekki verið fullkomlega reikningsfærðar og mótteknar.  

Vöruskilapöntunum er yfirleitt eytt þegar þær hafa verið reikningsfærðar. Þegar reikningur er bókaður er hann fluttur á síðuna **Bókaður innkaupakreditreikningur**. Ef gátreiturinn **Vöruskilaafhending á kreditreikningi** hefur verið valinn á síðunni **Innkaupagrunnur** er reikningurinn fluttur á síðuna **Bókuð skilaafhending**. Hægt er að eyða skjölunum með því að nota keyrsluna **Eyða reiknf. innk.vöruskilapönt.**. Áður en eytt er, athugar runuvinnslan hvort innkaupaskilapantanirnar séu að fullu afhentar og reikningsfærðar.  

Standandi pöntunum er ekki eytt eftir að allar tengdar innkaupapantanir hafa verið unnar og reikningsfærðar. Hægt er að eyða standandi pöntunum með keyrslunni **Reikningsfærðum standandi innkaupapöntunum eytt**.  

Þjónustupöntunum er yfirleitt eytt sjálfkrafa þegar þær hafa verið reikningsfærðar til fulls. Þegar reikningur er bókaður er samsvarandi færsla stofnuð á síðunni **Bókaðir þjónustureikningar** . Hægt er að skoða bókaða fylgiskjalið á síðunni **Bókaður þjónustureikningur**.  

Forritið eyðir þjónustupöntun ekki sjálfkrafa ef heildarmagn pöntunarinnar hefur verið bókað af síðunni **Þjónustureikningur** en ekki í þjónustupöntuninni sjálfri. Þá þarf að eyða bókuðum pöntunum sem ekki var búið að eyða. Hægt er að gera það með því að nota keyrsluna **Eyða reikningsfærðum þjónustupöntunum**.  

## <a name="compress-data-with-date-compression"></a>Þjappa gögnum með dagsetningarþjöppun

Hægt er að þjappa gögnum í [!INCLUDE [prod_short](includes/prod_short.md)] til að spara pláss í gagnagrunninum, sem í [!INCLUDE [prod_short](includes/prod_short.md)] á netinu getur jafnvel sparað þér peninga. Þjöppunin byggir á dagsetningum og vinnu með því að sameina margar gamlar færslur í eina nýja færslu. 

Hægt er að þjappa færslur við eftirfarandi aðstæður:

* Þær eru frá lokuðum fjárhagsárum
* Reiturinn **Opið** er stilltur á **Nei** 
* Þær eru að minnsta kosti fimm ára gamlar. Ef þjappa á gögnum sem eru yngri en fimm ára skaltu hafa samband við Microsoft-samstarfsaðilann.

Þannig má til að mynda þjappa lánardrottnafærslum umliðinna reikningsára þannig að á hverjum reikningi sé einungis um að ræða eina kreditfærslu og eina debetfærslu fyrir hvern mánuð. Upphæðin í nýju færslunni er samtala allra þjöppuðu færslnanna. Dagsetningin sem færslan hlýtur er upphafsdagsetning tímabilsins sem er þjappað, til dæmis fyrsti dagur mánaðarins (ef færslunum er þjappað eftir mánuðum). Eftir þjöppunina er enn hægt að sjá hreyfingar fyrir hvern reikning reikningsársins á undan.

Fjöldi færslna frá dagsetningarþjappa ræðst af því hve mikið var afmarkað, hvaða reitir voru tengdir saman og hvaða tímabilslengd var valin. Það verður alltaf til minnst ein færsla. Þegar keyrslu er lokið má sjá útkomuna á síðunni **Dags.þjöppun dagbóka**.

Hægt er að þjappa eftirfarandi gagnagerðum í með runuvinnslum. Það er runuvinnsla fyrir hverja gerð gagna.

* Fjármálafærslur - fjármálafærslur, VSK-færslur, bankareikningsfærslur, fjárhagsáætlunarfærslur, viðskiptavinafærslur, lánardrottnafærslur.
* Vöruhúsafærslur 
* Tilfangafærslur
* Birgðaáætlunarfærslur
* Eign - Fjárhagsfærslur eigna, fjárhagsfærslur eignaviðhalds, fjárhagsfærslur eignatryggingar.

Þegar verið er að skilgreina skilyrði fyrir þjöppunina er hægt að nota valkostina undir **Varðveita innihald reita** til að halda innihalda ákveðinna reita. Reitirnir sem eru tiltækir fara eftir gögnunum sem verið er að þjappa saman.

> [!NOTE]
> Áður en þú getur keyrt gagnaþjöppun þarf greiningaryfirlitið að vera uppfært. Frekari upplýsingar er að finna í [Að uppfæra greiningaryfirlit](bi-how-analyze-data-dimension.md#to-update-an-analysis-view).

Eftir þjöppunina er efni eftirfarandi reita alltaf varðveitt: **Bókunardagsetning**, **Númer lánardrottins**, **Tegund fylgiskjals**, **Gjaldmiðilskóði**, **Bókunarflokkur**, **Upphæð**, **Eftirstöðvar**, **Upphafleg upph. (SGM)**, **Eftirstöðvar (SGM)**, **Upphæð (SGM)**, **Innkaup (SGM)**, **Reikningsafsl. (SGM)**, **Veittur greiðsluafsláttur (SGM)** og **Mögul. að jafna greiðsluafsl.**.

## <a name="posting-compressed-entries"></a>Bókun þjappaðra færslna
Þjappaðar færslur eru bókaðar á örlítið öðruvísi hátt en venjulegar bókanir. Þetta er til að draga úr fjölda nýrra fjárhagsfærslna sem búnar eru til með dagsetningarþjöppun og eru sérstaklega mikilvægar þegar haldið er eftir upplýsingum á borð við víddir og skjalanúmer. Dagsetningarþjöppun stofnar nýjar færslur á eftirfarandi hátt:
* Á síðunni **Fjárhagsfærslur** eru nýjar færslur stofnaðar með nýjum færslunúmerum fyrir þjöppuðu færslurnar. Reiturinn **Lýsing** inniheldur **Dagsetningarþjöppun** þannig að auðvelt sé að bera kennsl á þjöppuðu færslurnar. 
* Á síðum fjárhags, eins og á síðunni **Fjárhagsfærslur**, eru ein eða fleiri færslur stofnaðar með nýjum færslunúmerum. 

Bókunarferlið stofnar eyður í númeraröðinni fyrir færslur síðunni **Fjárhagsfærslur**. Þessum númerum er aðeins úthlutað á færslurnar á fjárhagssíðum. Númerabilið sem var úthlutað á færslurnar er í boði á **Fjárhagsdagbókarsíðunni** í reitunum **Frá færslu nr.** og **Til færslu nr.**. 

> [!NOTE]
> Eftir að dagsetningarþjöppun er keyrð eru allir lyklar í fjárhagnum læstir. Til dæmis er ekki hægt að aftengja fjárhagsfærslur lánardrottna eða banka fyrir neina reikninga á tímabilinu þar sem dagsetningar eru þjappaðar.

Fjöldi færslna frá dagsetningarþjappa ræðst af því hve mikið var afmarkað, hvaða reitir voru tengdir saman og hvaða tímabilslengd var valin. Það verður alltaf til minnst ein færsla. 

> [!WARNING]
> Dagsetningaþjöppun eyðir færslum svo að tryggara er að taka alltaf afrit af gagnasafni áður en keyrslan er sett í gang.

### <a name="to-run-a-date-compression"></a>Að keyra gagnaþjöppun
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") táknið, slá inn **Gagnaumsjón** og velja svo viðeigandi tengil.
2. Gert er eitt af eftirfarandi:
    * Til að nota leiðbeiningar um uppsetningu með aðstoð til að setja upp gagnaþjöppun fyrir eina eða fleiri tegundir gagna skaltu velja **Leiðbeiningar um gagnaumsýslu**.
    * Til að setja upp þjöppun fyrir eina gagnagerð skal velja **Dagsetning þjöppunar**, **Þjöppunarfærslur** og síðan velja þau gögn sem á að þjappa.

   > [!NOTE]
   > Aðeins er hægt að þjappa gögnum sem eru eldri en fimm ára. Ef þjappa á gögnum sem eru yngri en fimm ára skaltu hafa samband við Microsoft-samstarfsaðilann.

## <a name="see-also"></a>Sjá einnig

[Stjórnun](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]