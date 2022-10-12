---
title: Stjórna geymslu með því að eyða skjölum eða þjappa gögnum
description: Kynntu þér hvernig hægt er að vinna úr uppsöfnun á gömlum skjölum (og draga úr gagnamagninu sem geymt er í gagnagrunni) með því að eyða eða þjappa gögnum.
author: edupont04
ms.topic: conceptual
ms.search.form: 107, 9035, 9040
ms.date: 09/14/2022
ms.author: edupont
ms.openlocfilehash: d6a98decb0b518629e29673d21147acc079b1b9e
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607364"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Stjórna geymslu með því að eyða skjölum eða þjappa gögnum

Meginhlutverk, t.d. kerfisstjóri, þarf reglulega að sjá um þau gögn sem safnast upp, eyða þeim eða þjappa þau.  

> [!TIP]
> Lærðu meira um aðrar leiðir til að draga úr gagnamagni sem geymt er í gagnagrunni með því að lesa [úr gögnum sem geymd eru í miðlægum gagnagrunnum](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) hjá HÖNNUÐINUM og það Pro fylgiskjöl.

## <a name="delete-documents"></a>Eyða skjölum.

Við vissar aðstæður getur þurft að eyða reikningsfærðum innkaupapöntunum. Hins vegar er ekki hægt að eyða þeim nema þegar búið er að reikningsfæra að fullu og mótteknar vörur í innkaupapöntunum. [!INCLUDE[prod_short](includes/prod_short.md)] hjálpa þér með því að athuga það.

Skilapöntunum er yfirleitt eytt eftir að þær eru reikningsfærðar. Þegar reikningur er bókaður er hann færður á **síðuna Bókaður innkaupakreditreikningur**. Ef gátreiturinn endursenda afhendingu á kreditreikningi er valinn **á** uppsetningarsíðu **innkaupa & lánardrottna er reikningurinn fluttur á** síðuna bókuð Vöruskilaafhending **.** Hægt er að eyða skjölunum með því að nota keyrsluna **Eyða reiknf. innk.vöruskilapönt.**. Áður en eytt er, athugar runuvinnslan hvort innkaupaskilapantanirnar séu að fullu afhentar og reikningsfærðar.  

Standandi innkaupapöntunum er ekki sjálfkrafa eytt þegar búið er að vinna úr og reikningsfæra allar tengdar innkaupapantanir. Í staðinn er hægt að eyða þeim með **keyrslunni Eyða Reikningsfærðum standandi innkaupapöntunum**.  

Reikningsfærðum þjónustupöntunum er yfirleitt eytt sjálfkrafa eftir að þær eru reikningsfærðar að fullu. Þegar reikningur er bókaður er samsvarandi færsla stofnuð og síðan er hægt að skoða hana á **síðunni bókaðir þjónustureikningar**.  

Þjónustupöntunum er ekki eytt sjálfkrafa, þó ef heildarmagn í pöntuninni hefur verið bókað **á Þjónustureikningssíðu** heldur en í þjónustupöntuninni sjálfri. Hugsanlega þarf að eyða slíkum reikningsfærðum pöntunum handvirkt með því að **keyra keyrsluna eyða reikningsfærðum þjónustupöntunum**.  

## <a name="compress-data-with-date-compression"></a>Þjappa gögnum með dagsetningaþjöppun

Hægt er að þjappa gögnum í [!INCLUDE [prod_short](includes/prod_short.md)] til að spara pláss í gagnagrunninum &mdash; sem á [!INCLUDE [prod_short](includes/prod_short.md)] netinu getur jafnvel sparað þér peninga. Þjöppunin, byggð á dagsetningum og aðgerðum, sameinar nokkrar gamlar færslur í eina nýja færslu.

Hægt er að þjappa færslum sem uppfylla öll eftirtalin skilyrði:

* Þær eru frá lokuðum reikningsárum.
* **Opna** svæðið er stillt á **Nr**.
* Þær eru að minnsta kosti fimm ára gamlar. Ef þjappa á gögnum yngri en fimm ára er hægt að hafa samband við samstarfsaðila Microsoft.

Til dæmis er hægt að þjappa lánardrottnafærslum frá fyrra reikningsári svo það sé aðeins ein kredit-og ein debetfærsla á hvern lykil á mánuði. Upphæðin í nýju færslunni er samtala allra þjöppuðu færslnanna. Dagsetningin sem er úthlutuð er upphafsdagsetning þjöppuðu tímabilsins, eins og Fyrsti dagur mánaðarins (ef færslurnar eru þjappaðar eftir mánuði). Að þjöppun lokinni er enn fremur hægt að sjá nettó breytingu hvers reiknings á fyrra reikningsári.

Fjöldi færslna frá dagsetningarþjappa ræðst af því hve mikið var afmarkað, hvaða reitir voru tengdir saman og hvaða tímabilslengd var valin. Það er alltaf minnst ein færsla. Þegar keyrslunni er lokið er hægt að sjá niðurstöðuna á **dagsetningarþjöppun dags. -Skráir** bls.

Hægt er að þjappa eftirfarandi gagnagerðum með því að nota runuvinnslur.

* Fjárfærslur-færslur fjárhags (fjárhagsfærslur), Virðisauki (VAT), færslur bankareiknings, fjárhagsfærslur, fjárhagsfærslur, viðskiptamannafærslur og lánardrottnafærslur.
* Vöruhúsafærslur
* Tilfangafærslur
* Birgðaáætlunarfærslur
* Fjárhagsfærslur eigna (eignir, EIGNAFÆRSLUR og EIGNATEIGSLUR).

Þegar skilyrði fyrir þjöppunina eru skilgreind er hægt að geyma efni tiltekinna reita með valkostunum undir **efni** reitsins varðveita. Tiltæk svæði fara eftir gögnunum sem þú ert að þjappa.

> [!NOTE]
> Áður en hægt er að keyra dagsetningarþjöppun verða greiningarúrin að vera gildandi. Frekari upplýsingar eru [í hlutanum uppfæra greiningaryfirlit](bi-how-analyze-data-dimension.md#update-an-analysis-view).

Eftir þjöppunina er efni eftirfarandi reita alltaf varðveitt: **Bókunardagsetning**, **Númer lánardrottins**, **Tegund fylgiskjals**, **Gjaldmiðilskóði**, **Bókunarflokkur**, **Upphæð**, **Eftirstöðvar**, **Upphafleg upph. (SGM)**, **Eftirstöðvar (SGM)**, **Upphæð (SGM)**, **Innkaup (SGM)**, **Reikningsafsl. (SGM)**, **Veittur greiðsluafsláttur (SGM)** og **Mögul. að jafna greiðsluafsl.**.

## <a name="posting-compressed-entries"></a>Bókunarþjappaðar færslur

Þjappaðar færslur eru bókaðar á örlítið öðruvísi hátt en venjulegar bókanir. Þetta er til að draga úr fjölda nýrra fjárhagsfærslna sem búnar eru til með dagsetningarþjöppun og eru sérstaklega mikilvægar þegar haldið er eftir upplýsingum á borð við víddir og skjalanúmer. Dagsetningarþjöppun stofnar nýjar færslur á eftirfarandi hátt:

* **Nýjar** færslur eru stofnaðar á síðunni fjárhagsfærslur fyrir þjappaðar færslur. Í **reitnum** Lýsing **er þjöppuð** Dagsetning svo að auðvelt sé að finna þjappaðar færslur. 
* Á fjárhagssíðum, eins og á **síðunni viðskiptamannafærslur**, eru ein eða fleiri nýjar færslur stofnaðar. 

Bókunarferlið stofnar eyður í númeraröðinni fyrir færslur síðunni **Fjárhagsfærslur**. Þessum númerum er aðeins úthlutað á færslurnar á fjárhagssíðum. Númerbilið sem úthlutað er á færslurnar er tiltækt á **síðunni Fjárhagsdagskráfærsla** í reitnum **frá Færslunr.** og **í Færslunr**. 

> [!NOTE]
> Eftir að dagsetningarþjöppun er keyrð eru allir lyklar í fjárhagnum læstir. Það þýðir að til dæmis er hægt að bakfæra lánardrottna-eða bankareikningsfærslur fyrir lykla sem hafa áhrif á þjöppunina.

Fjöldi færslna sem fara fram úr dagsetningarþjöppun veltur á því hversu margar afmarkanir eru settar, hvaða reitir eru sameinaðir og lengd þess tímabils sem valið er. Það verður alltaf minnst ein færsla.

> [!WARNING]
> Dagsetningaþjöppun eyðir færslum svo að tryggara er að taka alltaf afrit af gagnasafni áður en keyrslan er sett í gang.

### <a name="to-run-a-date-compression"></a>Að keyra gagnaþjöppun

1. ![Velja skal leitina á síðu eða skýrslutákni](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn"), færa inn **gögn stjórnunar** og velja síðan tengda tengilinn.
2. Gert er eitt af eftirfarandi:
    * Til að nota aðstoðarleiðsögn til að setja upp dagsetningarþjöppun fyrir eina eða fleiri gerðir gagna skal velja **leiðbeiningar** um stjórnun gagna.
    * Til að setja upp þjöppun fyrir einstaka gerð af gögnum skal velja **Gagnatþjöppun**, **þjappa færslur** og velja síðan gögnin sem á að þjappa.

   > [!NOTE]
   > Einungis má þjappa gögnum meira en fimm ára gömul. Ef þjappa á gögnum yngri en fimm ára er hægt að hafa samband við samstarfsaðila Microsoft.

## <a name="see-also"></a>Sjá einnig .

[Stjórnun](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
