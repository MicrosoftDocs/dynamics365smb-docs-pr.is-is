---
title: Stjórna geymslu með því að eyða skjölum eða þjappa gögnum
description: Kynntu þér hvernig hægt er að vinna úr uppsöfnun á gömlum skjölum (og draga úr gagnamagninu sem geymt er í gagnagrunni) með því að eyða eða þjappa gögnum.
author: brentholtorf
ms.topic: conceptual
ms.search.form: '107, 9035, 9040'
ms.date: 09/14/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Stjórna geymslu með því að eyða skjölum eða þjappa gögnum

Meginhlutverk, t.d. kerfisstjóri, þarf reglulega að sjá um þau gögn sem safnast upp, eyða þeim eða þjappa þau.  

> [!TIP]
> Frekari upplýsingar um aðrar leiðir til að draga úr magni gagna sem vistuð eru í gagnagrunni með því að lesa [Draga úr gögnum sem eru geymd í gagnagrunnum Business Central](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) í fylgiskjölum Developer og IT Pro.

## <a name="delete-documents"></a>Eyða skjölum.

Í vissum tilvikum kann að þurfa að eyða reikningsfærðum innkaupapöntunum. Þú getur hins vegar ekki eytt þeim nema þú hafir að fullu reikningsfært og móttekið vörurnar í innkaupapöntunum. [!INCLUDE[prod_short](includes/prod_short.md)] hjálpar þér með því að athuga þetta.

Vöruskilapöntunum er yfirleitt eytt þegar þær hafa verið reikningsfærðar. Þegar reikningur er bókaður er hann fluttur á síðuna **Bókaður innkaupakreditreikningur**. Ef gátreiturinn **Vöruskilaafhending á kreditreikningi** hefur verið valinn á síðunni **Innkaupagrunnur** er reikningurinn fluttur á síðuna **Bókuð skilaafhending**. Hægt er að eyða skjölunum með því að nota keyrsluna **Eyða reiknf. innk.vöruskilapönt.**. Áður en eytt er, athugar runuvinnslan hvort innkaupaskilapantanirnar séu að fullu afhentar og reikningsfærðar.  

Standandi innkaupapöntunum er ekki sjálfkrafa eytt eftir að allar tengdar innkaupapantanir hafa verið afgreiddar og reikningsfærðar. Í staðinn er hægt að eyða þeim í runuvinnslunni **Eyða reikningsfærðum standandi innkaupapöntunum**.  

Reikningsfærðum þjónustupöntunum er yfirleitt eytt sjálfkrafa eftir að þær hafa verið reikningsfærðar að fullu. Þegar reikningur er bókaður er samsvarandi færsla stofnuð á síðunni **Bókaðir þjónustureikningar** þar sem hægt er síðan að skoða hann.  

Hins vegar er þjónustupöntunum ekki sjálfkrafa eytt ef heildarmagn pöntunarinnar hefur verið bókað á síðunni **Þjónustureikningur** frekar en úr sjálfri þjónustupöntuninni. Þú gætir þurft að eyða slíkum reikningsfærðum pöntunum handvirkt með því að keyra runuvinnsluna **Eyða reikningsfærðum þjónustupöntunum**.  

## <a name="compress-data-with-date-compression"></a>Þjappa gögnum með dagsetningarþjöppun

Hægt er að þjappa gögnum í [!INCLUDE [prod_short](includes/prod_short.md)] til að spara pláss í gagnagrunninum, sem í [!INCLUDE [prod_short](includes/prod_short.md)] á netinu getur jafnvel sparað þér peninga. Þjöppunin, sem byggir á dagsetningum og aðgerðum, sameinar nokkrar eldri færslur í eina nýja færslu.

Hægt er að þjappa færslum sem uppfylla öll eftirfarandi skilyrði:

* Þær eru frá lokuðum fjárhagsárum.
* Reiturinn **Opið** er stilltur á **Nei**.
* Þær eru að minnsta kosti fimm ára gamlar. Ef þjappa á gögnum sem eru yngri en fimm ára skaltu hafa samband við samstarfsaðila þinn hjá Microsoft.

Þannig má til að mynda þjappa lánardrottnafærslum síðustu fjárhagsára þannig að á hverjum reikningi sé einungis ein kreditfærsla og ein debetfærsla fyrir hvern mánuð. Upphæðin í nýju færslunni er samtala allra þjöppuðu færslnanna. Úthlutuð dagsetning er upphafsdagurinn fyrir þjöppunartímabilið, t.d. fyrsti dagur mánaðarins (ef færslunum er þjappað eftir mánuði). Að þjöppun lokinni er eftir sem áður hægt að skoða nettóbreytingar fyrir hvern reikning á fyrra fjárhagsári.

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

## <a name="posting-compressed-entries"></a>Bókun þjappaðra færslna

Þjappaðar færslur eru bókaðar á örlítið öðruvísi hátt en venjulegar bókanir. Þetta er til að draga úr fjölda nýrra fjárhagsfærslna sem búnar eru til með dagsetningarþjöppun og eru sérstaklega mikilvægar þegar haldið er eftir upplýsingum á borð við víddir og skjalanúmer. Dagsetningarþjöppun stofnar nýjar færslur á eftirfarandi hátt:

* Á síðunni **Fjárhagsfærslur** eru nýjar færslur stofnaðar fyrir þjöppunarfærslurnar. Reiturinn **Lýsing** inniheldur **Dags. þjöppuð** þannig að auðvelt sé að bera kennsl á þjöppuðu færslurnar. 
* Á síðum fjárhags, eins og á síðunni **Fjárhagsfærslur**, eru ein eða fleiri færslur stofnaðar. 

Bókunarferlið stofnar eyður í númeraröðinni fyrir færslur síðunni **Fjárhagsfærslur**. Þessum númerum er aðeins úthlutað á færslurnar á fjárhagssíðum. Númerabilið sem var úthlutað á færslurnar er í boði á síðunni **Fjárhagsdagbók** í reitinum **Frá færslunr.** og **Til færslunr.**. 

> [!NOTE]
> Eftir að dagsetningarþjöppun er keyrð eru allir lyklar í fjárhagnum læstir. Þetta þýðir að þú getur til dæmis ekki bakfært fjárhagsfærslum lánardrottins eða banka fyrir neina reikninga sem eru hluti af þjöppuninni.

Fjöldi færslna frá dagsetningarþjöppun ræðst af því hve margar síur voru valdar, hvaða reitir eru sameinaðir og lengd tímabilsins sem þú velur. Það verður alltaf minnst ein færsla.

> [!WARNING]
> Dagsetningaþjöppun eyðir færslum svo að tryggara er að taka alltaf afrit af gagnasafni áður en keyrslan er sett í gang.

### <a name="to-run-a-date-compression"></a>Að keyra gagnaþjöppun

1. Velja skal táknið ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn"), slá inn **Gagnaumsjón** og velja svo viðeigandi tengil.
2. Gert er eitt af eftirfarandi:
    * Til að nota leiðbeiningar um uppsetningu með aðstoð til að setja upp gagnaþjöppun fyrir eina eða fleiri tegundir gagna skaltu velja **Leiðbeiningar um gagnaumsjón**.
    * Til að setja upp þjöppun fyrir eina gagnagerð skal velja **Gagnaþjöppun**, **Þjöppunarfærslur**, síðan velja gögnin sem á að þjappa.

   > [!NOTE]
   > Aðeins er hægt að þjappa gögnum sem eru eldri en fimm ára. Ef þjappa á gögnum sem eru yngri en fimm ára skaltu hafa samband við samstarfsaðila þinn hjá Microsoft. Þeir þurfa að nota `OnSetMinimumNumberOfYearsToKeep` atburðinn í "Date Compression" kóðaeiningunni til að stilla þröskuldinn.


## <a name="see-also"></a>Sjá einnig .

[Stjórnun](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
