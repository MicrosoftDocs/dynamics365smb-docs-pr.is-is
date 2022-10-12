---
title: Keyra og prenta skýrslur
description: Lærðu að færa inn skýrslu í vinnslubiðröð og áætla að hún sé unnin á tilteknum degi og tíma.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.search.form: ''
ms.date: 09/09/2022
ms.author: jswymer
ms.openlocfilehash: be4817ceac67674b82452b972c38dc316e274e8c
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607176"
---
# <a name="run-and-print-reports"></a>Keyra og prenta skýrslur

Skýrsla safnar saman upplýsingum byggðum á sérstöku safni af skilyrðum. Hún skipuleggur og birtir upplýsingar í auðveldu lestrarformi sem hægt er að prenta út eða vista sem skrá. Það eru margar skýrslur sem þú getur nálgast í gegnum forritið. Skýrslurnar veita alla jafna upplýsingar sem tengjast samhengi síðunnar sem þú ert á. Til dæmis, síðan **Viðskiptamaður** inniheldur skýrslur fyrir efstu 10 viðskiptamennina, sölutölur og fleira.

> [!NOTE]
> Runuvinnslur og XMLports gera meira eða minna það sama og skýrslur, en eru meira notaðar í þeim tilgangi að vinna úr og flytja út gögn. Þannig að keyrslan Stofna innheimtubréf **stofnar t.d.** innheimtuskjöl til að senda til viðskiptamanna með gjaldfallnar greiðslur. Þessi grein vísar aðallega til "skýrslna", en svipaðar upplýsingar eiga við runuvinnslur og XMLports.

## <a name="get-started"></a>Hafist handa

Þú finnur skýrslur í **valmyndinni skýrslur** á völdum síðum, listum og kortum eða notar leitarljósinn ![sem opnar aðgerðina segja mér upp.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") til að finna skýrslur eftir nafni. Fyrir yfirlit yfir innbyggðar skýrslur sem hægt er að nota í [!INCLUDE[prod_short](includes/prod_short.md)], flokkað eftir tegundum, sjá [tiltækar skýrslur í [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md).

Þegar skýrsla er valin er vanalega sett fram heiti tilboðsbeiðni &mdash; á eftir nafni &mdash; skýrslunnar þar sem hægt er að setja upp ýmsa valkosti og afmarkanir sem ákvarða hvaða gögn eru innifalin. Eftirfarandi hlutar útskýra hvernig á að nota beiðnisíðuna til að búa til, forskoða og prenta út skýrslur.

## <a name="using-default-valuesmdashpredefined-settings"></a><a name="SavedSettings"></a> Notkun sjálfgefinna gilda &mdash; fyrirfram stillta stillingu

Á **síðum flestra skýrslubeiðna eru sjálfgefin gildi frá** svæðinu nota. Með þessum reit er hægt að velja fyrirframskilgreindar stillingar fyrir skýrsluna sem stillir sjálfkrafa valkosti og afmarkanir. Veljið færslu úr fellilista til að sjá valkosti og afmarkanir á síðunni breytingar á skýrslubeiðni til samræmis.

Færslan sem kallast **Valkostir og síur síðast notað** er alltaf í boði. Þessi færsla stillir skýrsluna til að nota valkostina og afmarkanirnar sem voru notaðar síðast þegar skýrslan var notuð.

Reiturinn **Nota sjálfgildi úr** veitir fljótlega og áreiðanlega leið til að búa til skýrslur sem innihalda réttar upplýsingar. Þegar færsla er valin, er hægt að breyta öllum valkostum og síum áður skýrslan er forskoðuð eða prentuð. Breytingunum verður ekki bjargað í fyrirfram skilgreinda stillingarfærsluna sem valin var, en þær verða vistaðar **í síðustu valkostunum fyrir notaða valkosti og afmarkanir**.

> [!NOTE]
> Fyrirframskilgreindar stillingar eru yfirleitt settar upp og stjórnað af stjórnanda. [Frekari upplýsingar fást með því að stjórna vistuðum stillingum fyrir skýrslur og runuvinnslur](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-a-report"></a>Tilgreind gögn sem eiga að koma fram í skýrslu

Notið svæðin undir **Valkostir** og **afmarkanir** til að breyta eða takmarka þær upplýsingar sem óskað er eftir í skýrslunni. Hægt er að setja afmarkanir í skýrslu á meira eða minna sama hátt og afmarkanir eru settar á lista. Frekari upplýsingar er [að fá í síuhlutanum](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> **Flipinn sía** í skýrslubeiðssíðu gefur almenna síugetu til skýrslna. Þessar síur eru valfrjálsar.
>
> Sumar skýrslur hunsa allar slíkar síur, sem þýðir að sama hvaða Afmörkun er sett á **fastflipa afmörkunar** er framleiðsla skýrslunnar sú sama. Það er ekki hægt að gefa upp lista yfir hvaða reitir eru hunsaðir í hvaða skýrslur, svo að þú munt þurfa að gera tilraunir með síur þegar þær eru notaðar.
>
> **Dæmi** : þegar keyrslan Stofna innheimtubréf **er notuð**, er afmörkun í **reitnum** viðskiptamannafærslur **Síðasta útgefna innheimtubréfs** hunsuð þar sem afmarkanir eru fastar í þeirri keyrslu.

## <a name="previewing-a-report"></a>Forskoða skýrslu

Með því að forskoða skýrslu er hægt að sjá hvað skýrslan mun líta út áður en hún er prentuð. Forskoðunin er ekki byggð á prentaranum sem er valinn í **reitnum prentari** á beiððsíðunni. Hún fer eftir vafranum. Að forskoðun lokinni er hægt að fara aftur á beiðnisíðuna og gera breytingar á valkostum og síum eftir þörfum.

Forskoðunarvalkostirnir á **síðunni Skýrslubeiðni** fara eftir skýrslunni. Þannig að í sumum skýrslum er hægt að velja **Forskoðun, á** meðan aðrir velja Forskoðun & Loka **·**. Báðir Valkostir opna Forskoðun skýrslunnar. Munurinn liggur í því að **Forskoðun** heldur beiðnisíðunni opinni, þannig að hægt er að fara aftur í hana, gera breytingar, forskoða aftur eða prenta. Á móti, með **forskoðun & loka Beiðnssíðu** lokast og þú verður að opna skýrsluna aftur til að gera breytingar eða prenta.

> [!NOTE]
> Ef notað er **2020 út bylgju 1 eða eldri er eini kosturinn Forskoðun**, sem lokar beiðnsíðunni á Forskoðun, eins og lýst er hér að framan fyrir **Forskoðun & Loka**.

### <a name="work-with-the-preview"></a>Vinna með forskoðunina

Í forskoðun skal nota valmyndastikuna í forskoðun skýrslunnar til að:

- Fara gegnum síður
- Auka aðdrátt og minnka
- Breyta stærð svo passi á síðu
- Velja texta

    Hægt er að afrita texta úr skýrslu, líma hann annars staðar, svo sem síðu í [!INCLUDE[prod_short](includes/prod_short.md)] eða Microsoft Word. Með því að nota mús, til dæmis, ýtir þú á vinstri músarhnapp og heldur þar sem þú vilt byrja. Renndu músinni til að velja eitt eða fleiri orð, setningar eða málsgreinar. Ýttu svo á hægri músarhnapp og veldu **Copy**. Nú er hægt að líma inn valinn texta þar sem hann á við.
- Fletta skjali

    Hægt er að færa sýnilegt svæði skýrslunnar í hvaða átt sem er til að skoða önnur svæði skýrslunnar. Fletting er gagnleg þegar þú hefur aukið aðdrátt til að sjá smáatriði. Músin er notuð til dæmis með því að styðja á vinstri músarhnapp hvar sem er í skýrsluforskoðuninni og músin færð til að velja hluta skýrslunnar.

- Hlaða niður PDF-skrá á tölvuna eða netið.
- Prenta

## <a name="saving-a-report-to-a-file"></a>Vista skýrslu í skrá

Hægt er að vista skýrslu í PDF skjali, Microsoft Word skjali, Microsoft Excel VINNUBÓK eða XML skjali með því að velja **senda til**, þá er valið. Skrá er sótt í tækið þitt.

Ef fyrirtækið hefur skilgreint OneDrive fyrir kerfiseiginleika í stað þess að það sé hlaðið niður, opnast Excel-vinnubók og Word-skjöl í vafranum með því að nota annaðhvort Excel eða Word fyrir vefinn.

> [!TIP]
> **Microsoft Excel Skjalið (gagnaaðeins)** og **Valkostir XML-skjals** eru að mestu til Ítarlegir. Gjarnan eru notaðir þessir valkostir til að gera nákvæma greiningu á gögnum. Frekari upplýsingar í að [greina skýrslugögn með Excel og XML](report-analyze-excel.md).
>
> Einnig er hægt að nota **Microsoft Excel Fylgiskjal (aðeins gögn)** til að stofna nýtt Excel-skipulag fyrir gefna skýrslu. Frekari upplýsingar í [vinnu við Excel-skipulag](ui-excel-report-layouts.md).  

## <a name="scheduling-a-report-to-run-later-or-periodically"></a><a name="ScheduleReport"></a> Raða skýrslu sem á að keyra síðar eða reglulega

Hægt er að áætla eina eða endurtekna skýrslu sem á að keyra á tilteknum degi og tíma. Tímasettar skýrslur eru færðar inn í verkröð og unnar á settum tíma, eins og önnur verk. **Velja skal valkostinn áætlun** eftir **að** senda er valið og færa inn upplýsingar, eins og prentara, og tíma og dagsetningu. Skýrslunni er bætt við vinnsluröðina og keyrð á tilgreindum tíma. Þegar skýrslan er unnin er varan fjarlægð úr vinnslubiðröð. [Frekari upplýsingar um notkun Vinnubiðraða á að áætla verk](admin-job-queues-schedule-tasks.md).  

Þegar skýrsla er tímasett er hægt að tilgreina, til dæmis, að hún verði keyrð á hverjum fimmtudegi með því að stilla **dagsetningarsvæði næsta Keyrsludags** í *D4*. Frekari upplýsingar í [reikniformúlum](ui-enter-date-ranges.md#use-date-formulas) notkunardags.  

Hægt er að velja að vista skýrsluna í skrá (eins og Excel, Word, eða PDF), prenta hana eða búa aðeins til skýrsluna. Ef valið er að vista skýrsluna í skrá er sú sem er unnin skýrsla send **á síðuna Skýrsluinnhólfið** í hlutverkamiðstöðinni fyrir þig til að skoða hana. Frekari upplýsingar í [Share og Útflutningsskýrslum með Skýrsluinnhólfinu](ui-work-report-inbox.md)

### <a name="manage-scheduled-recurring-reports"></a>Stjórna áætluðum endurteknum skýrslum

Áætlaðar skýrslur eru myndaðar með runuvinnslum sem **meðhöndlaðar eru á síðunni Vinnslubiðfærslur**. Hægt er að sjá stöðu og aðrar upplýsingar fyrir hverja skýrslu á síðunni, gera hlé/halda áfram í skýrslukeyrslunnar og búa skýrsluna til eftirspurnar.

Einnig er hægt að breyta nokkrum skýrslufæribreytum, svo sem úttaksskrárgerð, endurtekningu, keyrsludagsetningu og upphafs-og lokatíma í færslum **á** síðunni. Áður en fyrirliggjandi tímasettri skýrslu er breytt er þó nauðsynlegt að setja skýrsluna vinnslubiðröð í bið:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **Verkraðarafærslur**, velja síðan tengda tengilinn.  
2. **Á síðunni Vinnsluraðarfærslur** er viðkomandi skýrsla valin.
3. Velja skal **aðgerðina setja á bið**.
4. Opna og breyta áætlaðri skýrslu með því að velja stöðu hennar (*í bið*).

Eftir að valkostum skýrslunnar er breytt skal endurtaka fyrstu tvö skrefin og velja **síðan Stilla stöðu í tilbúnar** Aðgerðir til að halda áfram að mynda skýrsluna.

Frekari upplýsingar um stjórnun vinnslu í [Vinnslubiðröðum eru notaðar til að áætla verk](admin-job-queues-schedule-tasks.md).  

## <a name="printing-a-report"></a><a name="PrintReport"></a> Skýrsla prentuð

Til að prenta skýrslu er valið **Prenta** á síðunni skýrslubeiðni eða á valreininni **á forskoðunarsíðunni**.

Þegar skýrsla er notuð í Excel sjást **ekki svæði prentarans** eða **PRINT** eða **Preview** -hnappar. Þess í stað er **niðurhalsvalkostur**. Til að prenta, Veldu **Download**, Opnaðu þá skrána sem var sótt í Excel og Prentaðu þaðan út.

### <a name="printer"></a><a name="Printer"></a>Prentari

Í **reitnum prentari** á beiðssíðu kemur fram heiti prentarans sem skýrslan er send til. Til að breyta prentara skal einfaldlega velja prentarann úr listanum.

> [!NOTE]
> **Valkosturinn (meðhöndlaði vafrinn)** gefur til kynna að enginn merktur prentari sé til skýrslunnar. Í þeim tilfellum sér vafrinn um útprentunina og birtir staðlaða prentskrefa þar sem hægt er að velja staðbundinn prentara sem tengdur er við tækið. Sá **(afgreiddur með vafra)** valkostur er ekki tiltækur í [!INCLUDE[prod_short](includes/prod_short.md)] Mobile App eða App fyrir Microsoft Teams.

> [!TIP]
> Prentarinn sem er sjálfgefið valinn fyrir þig er settur upp á síðunni **Prentaraval**. Frekari upplýsingar um breytingar á sjálfgefnum prentara í [hlutanum Uppsetning sjálfgefinna prentara](ui-specify-printer-selection-reports.md#default).

### <a name="printing-reports-in-thai"></a>Býr til skýrslu í Thai

Sérstaklega fyrir taílensku útgáfuna af [!INCLUDE[prod_short](includes/prod_short.md)], getur hnappurinn **Prenta** ekki prentað skýrslur rétt vegna takmarkana á þjónustunni sem býr til prentanlegt PDF-skjal. Í staðinn getur þú opnað skýrsluna í Word og síðan vistað hana sem prentvæna PDF-skrá.  

Eða þú getur beðið stjórnanda þinn um að búa til Word-skýrsluútlit fyrir mest notuðu skýrslurnar. Frekari upplýsingar í [Umsjón með skýrslu og Skjalaskipan](ui-manage-report-layouts.md).  

## <a name="switching-the-report-layout"></a>Skipta um útlit skýrslunnar

Skýrsluútlit stjórnar því hvað er sýnt í skýrslu, hvernig því er stillt upp og það stílfært. Það eru nokkrar leiðir til að breyta útlitinu:

- Þegar verið er að setja upp til að keyra skýrslu sést núverandi útlit í **reitnum útlit** skýrslu á beiðssíðu. Ef skipta á tímabundið um annað útlit skal velja **svæðið skýrslusnið** og velja síðan úr lista yfir tiltæk útlit skýrslunnar.
- Til að breyta sjálfgefnu útlitinu sem notuð er í skýrslu er farið í annað hvort **skýrsluskipulag** eða **síður skýrsluuppsetningar**.

Frekari upplýsingar eru í [set-uppsetningunni sem notuð er í skýrslu](ui-set-report-layout.md). Ef sérsníða á skýrsluuppsetningu er farið í hafist handa til að [Stofna skipulag](ui-get-started-layouts.md).

## <a name="advanced-options"></a>Ítarlegir valkostir

Reitirnir undir **Advanced** festivaltab setja takmarkanir á tilbúnar skýrslur til að stjórna prentaratengingum. Yfirleitt þarf ekki að breyta þessum stillingum nema um stóra skýrslu sé að ræða. Ef skýrsla er yfir þessum takmörkunum þegar reynt er að forskoða eða prenta gefur skilaboð til kynna hvaða takmörkun notandi hefur farið fram á. Síðan er hægt að breyta stillingunum svo þær henti skýrslunni betur. Hvert svæði hefur hins vegar hámarks gildi sem þú ættir að gera grein fyrir:

|Svæði|Hámarksgildi|
|-----|-------------|
|Hámarksmyndunartími|12:00:00|
|Hámarksfjöldi lína|1000000|
|Hámarksfjöldi skjala|500|

> [!NOTE]
> Hámarksgildin kunna að vera mismunandi fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum og stjórnandi getur breytt þeim. Frekari upplýsingar er að [skilgreina í hlutanum Skilgreining miðlægra þjón Business-](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports) miðlara. Fyrir yfirlit yfir takmarkanir skýrslunnar á [!INCLUDE[prod_short](includes/prod_short.md)] netinu, sjá [rekstrarmörk](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/paths/setup-reporting-dynamics-365-business-central/).

## <a name="see-also"></a>Sjá einnig .

[Tiltækar skýrslur í[!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Nota skýrslur í daglegu starfi](reports-use-reports.md)  
[Yfirlit yfir viðskiptagreind og skýrslugerð](reports-bi-reporting.md)  
[Setja upp prentara](ui-specify-printer-selection-reports.md)  
[Keyra runuvinnslur og XMLports](ui-how-run-batch-jobs.md)  
[Vinna með dagsetningar og tímasetningar dagatals](ui-enter-date-ranges.md)  
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Upplýsingarit um Fjármál fyrirtækja](bi.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
