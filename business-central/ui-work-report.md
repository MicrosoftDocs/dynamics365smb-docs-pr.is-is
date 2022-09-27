---
title: Keyra og prenta skýrslur
description: Kynntu þér hvernig skal setja skýrslu inn í verkröð og tímasetja hana þannig að hún sé unnin á tilteknum degi og tíma.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.search.form: ''
ms.date: 03/24/2022
ms.author: jswymer
ms.openlocfilehash: b4184f5538ea15c1a5be5ed1d7a6e8fd7ef3e1cb
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531270"
---
# <a name="run-and-print-reports"></a>Keyra og prenta skýrslur

Skýrsla safnar saman upplýsingum byggðum á sérstöku safni af skilyrðum. Hún flokkar og birtir upplýsingarnar á sniði sem er auðvelt að lesa og sem hægt er að prenta eða vista sem skrá. Til eru margar skýrslur sem má finna víðsvegar í forritinu. Skýrslurnar veita alla jafna upplýsingar sem tengjast samhengi síðunnar sem þú ert á. Til dæmis, síðan **Viðskiptamaður** inniheldur skýrslur fyrir efstu 10 viðskiptamennina, sölutölur og fleira.

Runuvinnslur og XMLports gera meira eða minna það sama og skýrslur, en eru meira notaðar í þeim tilgangi að vinna úr og flytja út gögn. Til dæmis býr runuvinnslan **Stofna innheimtubréf** til áminningarskjöl fyrir viðskiptavini með gjaldfallnar greiðslur.  

> [!NOTE]
> Þetta efnisatriði vísar aðallega í „skýrsla“, en svipaðar upplýsingar gilda um runuvinnslur og XMLport.

## <a name="get-started"></a>Hafist handa

Þú finnur skýrslur í flipanum **Skýrslur** á völdum síðum eða þú getur leitað með því að nota ![Ljósaperuna sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") til að finna skýrslur eftir nafni.

Þegar þú opnar skýrslu, runuvinnslu eða XMLport birtist þér yfirleitt beiðnisíða þar sem þú tilgreinir ýmsa valmöguleika og síur sem ákvarða hvað skal hafa með í skýrslunni. Eftirfarandi hlutar útskýra hvernig á að nota beiðnisíðuna til að búa til, forskoða og prenta út skýrslur.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Sjálfgefin gildi notuð - fyrirframskilgreindar stillingar

Flestar beiðnisíður innihalda reitinn **Nota sjálfgildi úr**. Þessi reitur gerir þér kleift að velja fyrirframskilgreindar stillingar fyrir skýrsluna sem sjálfkrafa stilla valkosti og síur fyrir skýrsluna. Veljið færslu úr fellilistanum og þar koma þá í ljós breytingarnar á valkostum og síum beiðnisíðunnar.

Færslan sem kallast **Valkostir og síur síðast notað** er alltaf í boði. Þessi færsla stillir skýrsluna á að nota valkosti og síur sem voru síðast notuð þegar skýrslan var keyrð.

Reiturinn **Nota sjálfgildi úr** veitir fljótlega og áreiðanlega leið til að búa til skýrslur sem innihalda réttar upplýsingar. Þegar færsla er valin, er hægt að breyta öllum valkostum og síum áður skýrslan er forskoðuð eða prentuð. Breytingarnar sem þú gerir verða ekki vistaðar í færslu fyrirframskilgreindrar stillingar sem þú velur, en þær verða vistaðar í færslunni **Síðast notaðir valkostir og afmarkanir**.

>[!NOTE]
> Fyrirframskilgreindar stillingar eru yfirleitt settar upp og stjórnað af stjórnanda. Til að fá nánari upplýsingar er hægt að skoða [Stjórna vistuðum stillingum fyrir skýrslur og runuvinnslur](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-a-report"></a>Tilgreind gögn sem eiga að koma fram í skýrslu

Notið reitina undir **Valkostir** og **Síur** til að breyta takmörkunum á upplýsingum sem eiga að koma fram í skýrslunni. Síur eru stilltar í skýrslu nánast á sama hátt og þær eru stilltar í listum. Frekari upplýsingar er að finna í [Síun](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Hlutinn **Sía lista eftir** á beiðnisíðu veitir almennan síumöguleika fyrir skýrslur. Þessar síur eru valfrjálsar.
>
> Einhverjar skýrslur hunsa slíkar síur, sem þýðir að sama hvaða sía er stillt í hlutanum **Sía lista eftir** verður útkoma skýrslunnar sú sama. Ekki er hægt að gefa upp lista yfir hvaða reitir eru hunsaðir í hvaða skýrslum, þannig að þú verður að gera tilraunir með síurnar þegar þú notar þær.
>
> **Dæmi**: Þegar þú notar runuvinnsluna **Sent innheimtubréf** verður sía fyrir reitinn **Færslur í viðskiptamannabók** í **Stig síðasta útgefins innheimtubréfs** hunsuð vegna þess að síurnar eru fastar fyrir þessa runuvinnslu.

## <a name="previewing-a-report"></a>Forskoða skýrslu

Að forskoða skýrsluna gerir notanda kleift að sjá hvernig skýrslan komi til með að líta út áður en hún er prentuð. Forskoðunin er ekki byggð á prentaranum sem er valinn í **reitnum prentari** á beiððsíðunni. Hún fer eftir vafranum. Að forskoðun lokinni er hægt að fara aftur á beiðnisíðuna og gera breytingar á valkostum og síum eftir þörfum.

Til að forskoða skýrslu skal velja hnappinn **Forskoða** eða **Forskoða og loka** á beiðnisíðu skýrslunnar. Hnappurinn sem birtist fer eftir skýrslunni, þannig að sumar skýrslur eru með hnappinn **Forskoða** á meðan aðrar eru með hnappinn **Forskoða og loka**. Báðir hnapparnir opna forskoðun á skýrslunni. Munurinn liggur í því að **Forskoðun** heldur beiðnisíðunni opinni, þannig að hægt er að fara aftur í hana, gera breytingar, forskoða aftur eða prenta. Með **Forskoða og loka** lokast beiðnisíðan, þannig að opna þarf skýrsluna aftur til að gera breytingar eða prenta.

> [!NOTE]
> Ef verið er að nota Business Central 2020 útgáfutímabil 1 eða eldra, er aðeins hnappurinn **Forskoða**, sem lokar beiðnisíðunni við forskoðun eins og lýst er fyrir **Forskoðun og loka**.

### <a name="work-with-the-preview"></a>Vinna með Forskoðunina

Í forskoðun skal nota valmyndastikuna í forskoðun skýrslunnar til að:

- Fara gegnum síður
- Auka aðdrátt og minnka
- Breyta stærð svo passi á síðu
- Velja texta

    Þú getur afritað texta úr skýrslu og svo límt hann eitthvert annað, eins og á síðu í [!INCLUDE[prod_short](includes/prod_short.md)] eða Microsoft Word.  Ef þú notar mús, til dæmis, þá ýtirðu og heldur niðri þar sem þú vilt byrja. Færðu svo músina til að velja eitt eða fleiri orð, setningar eða málsgreinar. Smellið á hægri músarhnappinn og veljið **Afrita**. Límið síðan valinn texta þar sem hann á að vera.
- Fletta skjali

    Hægt er að færa sjáanlega svæðið af skýrslunni í allar átti svo þú getir skoðað önnur svæði skýrslunnar. Fletting er gagnleg þegar þú hefur aukið aðdrátt til að sjá smáatriði.  Ef þú notar músina, til dæmis, þrýstirðu niður og heldur inni hnappinum hvar sem er á forskoðun skýrslunnar og svo hreyfirðu músina.

- Hlaða niður PDF-skrá á tölvuna eða netið.
- Prenta

## <a name="saving-a-report-to-a-file"></a>Vista skýrslu í skrá

Hægt er að vista skýrslu í PDF-skjali, Microsoft Word skjali, Microsoft Excel vinnublaði eða XML skjali með því að velja **hnappinn senda til** og gera svo valið.

> [!TIP]
> **Microsoft Excel Skjalið (gagnaaðeins)** og **Valkostir XML-skjals** eru að mestu til Ítarlegir. Gjarnan eru notaðir þessir valkostir við að gera ítarlegar gagnagreiningar. Frekari upplýsingar er að finna [í greina skýrslugögn með Excel og XML](report-analyze-excel.md).
>
> Einnig er hægt að nota **Microsoft Excel skjalið (aðeins gögn)** til að stofna nýtt Excel-skipulag fyrir gefna skýrslu. Sjá [vinnu með Excel-skipan](ui-excel-report-layouts.md) fyrir frekari upplýsingar.  
  
<!--
### About sending to Word

Use the **Microsoft Word Document** option to generate a report as a Word document.  

> [!NOTE]
> You can specify the layout to use for each report on the **Report Selection** page in the **Selected Layout** field. The default setting for reports is **RDLC (built-in)**, which produces reports in the same, or similar, layout as the **Microsoft Word Document** layout. However, the key difference is whether you want to generate a single or multiple report documents. For single documents, you can use the RDLC (built-in) option. For multiple documents, set the **Microsoft Word Document** as the default layout for the report. For more information, see [Managing Report and Document Layouts](ui-manage-report-layouts.md).

-->

## <a name="scheduling-a-report-to-run-later"></a><a name="ScheduleReport"></a> Raða skýrslu sem á að keyra síðar

Hægt er að tímasetja eða runuvinna skýrslu þannig að hún keyri á tilteknum degi og tíma. Tímasettar skýrslur og runuvinnslur eru færðar inn í verkröð og unnar á áætluðum tíma, eins og önnur verk. Veldu valkostinn **Áætlun** eftir að hafa valið **Senda til** og færðu svo inn upplýsingar á borð við prentara, og tíma og dagsetningu. Skýrslunni er síðan bætt við verkröðina og hún verður keyrð á tilgreindum tíma. Þegar skýrslan hefur verið meðhöndluð er varan fjarlægð úr verkröðinni. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).  

Þegar keyrsla skýrslu er áætluð er hægt að tilgreina að keyra þurfi alla fimmtudaga með því að stilla reitinn **Reikniregla næstu keyrsludagsetningar** á t.d. *D4*. Sjá [Use Dagsetningarformúlur fyrir frekari upplýsingar](ui-enter-date-ranges.md#use-date-formulas).  

Hægt er að velja að vista skýrsluna í skrá (t.d. Excel, Word, eða PDF), prenta hana eða aðeins búa til skýrsluna. Ef þú velur að vista skýrsluna í skrá þá er meðhöndlaða skýrslan send á svæðið **Skýrsluinnhólf** á Mitt hlutverk þar sem þú getur skoðað hana.  

## <a name="printing-a-report"></a><a name="PrintReport"></a> Skýrsla prentuð

Til að prenta skýrslu skal velja hnappinn **Prenta** á beiðnisíðunni eða valmyndastikunni á síðunni **Forskoða**.

Þegar skýrsla er notuð í Excel sjást **ekki svæði prentarans**, **prenthnappur** eða **forskoðunarhnappur**. Þess í stað er **niðurhalshnappur**. Til að prenta, Veldu **Download**, Opnaðu þá skrána sem var sótt í Excel og Prentaðu þaðan út.

### <a name="printer"></a><a name="Printer"></a>Prentari

Reiturinn **Prentari** á beiðnisíðunni sýnir heiti prentarans sem skýrslan verður send til. Til að breyta prentara skal einfaldlega velja prentarann úr listanum.

> [!NOTE]
> **(Meðhöndlað af vafra)** gefur til kynna að enginn prentari sé valinn fyrir skýrsluna. Í slíku tilfelli sér vafrinn um útprentun og sýnir hefðbundið viðmót þar sem hægt er velja staðbundinn prentara sem tengdur er við tækið þitt. **(Meðhöndlað af vafra)** er ekki í boði í farsímaforriti [!INCLUDE[prod_short](includes/prod_short.md)] eða forrit fyrir Microsoft Teams.

> [!TIP]
> Prentarinn sem er sjálfgefið valinn fyrir þig er settur upp á síðunni **Prentaraval**. Upplýsingar um hvernig á að breyta sjálfgefnum prentara er að finna í [Að velja hvaða prentara prenta hvaða skýrslur](ui-specify-printer-selection-reports.md#default).

### <a name="printing-reports-in-thai"></a>Býr til skýrslu í Thai

Sérstaklega fyrir taílensku útgáfuna af [!INCLUDE[prod_short](includes/prod_short.md)], getur hnappurinn **Prenta** ekki prentað skýrslur rétt vegna takmarkana á þjónustunni sem býr til prentanlegt PDF-skjal. Í staðinn getur þú opnað skýrsluna í Word og síðan vistað hana sem prentvæna PDF-skrá.  

Eða þú getur beðið stjórnanda þinn um að búa til Word-skýrsluútlit fyrir mest notuðu skýrslurnar. Frekari upplýsingar, sjá [Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md).  

## <a name="switching-the-report-layout"></a>Skipta um útlit skýrslunnar

Skýrsluútlit stjórnar því hvað er sýnt í skýrslu, hvernig því er stillt upp og það stílfært. Ef skipta á um annað útlit er að finna [í stilla útlit sem skýrsla](ui-set-report-layout.md) notar. Eða ef sérsníða á skýrsluuppsetningu notanda er hægt að sjá [byrja á stofnun uppsetningar](ui-get-started-layouts.md).

## <a name="advanced-options"></a>Ítarlegir valkostir

Reitirnir undir **Ítarlegt** setja takmarkanir á myndaða skýrslu til að stjórna tilföngum prentarans. Yfirleitt þarf ekki að breyta þessum stillingum nema um stóra skýrslu sé að ræða. Ef skýrsla fer umfram þessar takmarkanir þegar reynt er að forskoða eða prenta, birtast skilaboð sem segja til um hvaða takmörkun var farið yfir. Síðan er hægt að breyta stillingunum svo þær henti skýrslunni betur. Hver reitur er hinsvegar með hámarksgildi sem hafa ætti í huga:

|Svæði|Hámarksgildi|
|-----|-------------|
|Hámarksmyndunartími|12:00:00|
|Hámarksfjöldi lína|1000000|
|Hámarksfjöldi skjala|500|

> [!NOTE]
> Hámarksgildin kunna að vera mismunandi fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum og stjórnandi getur breytt þeim. Frekari upplýsingar er að finna í [Skilgreining Business Central Server - Skýrslur](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Fyrir yfirlit yfir takmarkanir á skýrslum í [!INCLUDE[prod_short](includes/prod_short.md)] á netinu, skal skoða [Rekstrarlegar takmarkanir](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/paths/setup-reporting-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Setja upp prentara](ui-specify-printer-selection-reports.md)  
[Vinna með dagsetningar og tímasetningar dagatals](ui-enter-date-ranges.md)  
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
