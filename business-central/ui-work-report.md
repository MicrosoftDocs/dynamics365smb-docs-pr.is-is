---
title: Unnið með skýrslur, runuvinnslur og XMLports
description: Kynntu þér hvernig skal setja skýrslu inn í verkröð og tímasetja hana þannig að hún sé unnin á tilteknum degi og tíma.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.date: 06/21/2021
ms.author: jswymer
ms.openlocfilehash: 9deb7e30e05da74e6ea263a0262680d2e99b8b4b
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6439951"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Unnið með skýrslur, runuvinnslur og XMLports

Skýrsla safnar saman upplýsingum byggðum á sérstöku safni af skilyrðum. Hún flokkar og birtir upplýsingarnar á sniði sem er auðvelt að lesa og sem hægt er að prenta eða vista sem skrá. Til eru margar skýrslur sem má finna víðsvegar í forritinu. Skýrslurnar veita alla jafna upplýsingar sem tengjast samhengi síðunnar sem þú ert á. Til dæmis, síðan **Viðskiptamaður** inniheldur skýrslur fyrir efstu 10 viðskiptamennina, sölutölur og fleira.

Runuvinnslur og XMLports gera meira eða minna það sama og skýrslur, en eru meira notaðar í þeim tilgangi að vinna úr og flytja út gögn. Til dæmis býr runuvinnslan **Stofna innheimtubréf** til áminningarskjöl fyrir viðskiptavini með gjaldfallnar greiðslur.  

> [!NOTE]
> Þetta efnisatriði vísar aðallega í „skýrsla“, en svipaðar upplýsingar gilda um runuvinnslur og XMLport.

## <a name="getting-started"></a>Hafist handa

Þú finnur skýrslur í flipanum **Skýrslur** á völdum síðum eða þú getur leitað með því að nota ![Ljósaperuna sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") til að finna skýrslur eftir nafni.

Þegar þú opnar skýrslu, runuvinnslu eða XMLport birtist þér yfirleitt beiðnisíða þar sem þú tilgreinir ýmsa valmöguleika og síur sem ákvarða hvað skal hafa með í skýrslunni. Eftirfarandi hlutar útskýra hvernig á að nota beiðnisíðuna til að búa til, forskoða og prenta út skýrslur.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Sjálfgefin gildi notuð - fyrirframskilgreindar stillingar 

Flestar beiðnisíður innihalda reitinn **Nota sjálfgildi úr**. Þessi reitur gerir þér kleift að velja fyrirframskilgreindar stillingar fyrir skýrsluna sem sjálfkrafa stilla valkosti og síur fyrir skýrsluna. Veljið færslu úr fellilistanum og þar koma þá í ljós breytingarnar á valkostum og síum beiðnisíðunnar.

Færslan sem kallast **Valkostir og síur síðast notað** er alltaf í boði. Þessi færsla stillir skýrsluna á að nota valkosti og síur sem voru síðast notuð þegar skýrslan var keyrð.

Reiturinn **Nota sjálfgildi úr** veitir fljótlega og áreiðanlega leið til að búa til skýrslur sem innihalda réttar upplýsingar. Þegar færsla er valin, er hægt að breyta öllum valkostum og síum áður skýrslan er forskoðuð eða prentuð. Breytingarnar sem þú gerir verða ekki vistaðar í færslu fyrirframskilgreindrar stillingar sem þú velur, en þær verða vistaðar í færslunni **Síðast notaðir valkostir og afmarkanir**.

>[!NOTE]
> Fyrirframskilgreindar stillingar eru yfirleitt settar upp og stjórnað af stjórnanda. Til að fá nánari upplýsingar er hægt að skoða [Stjórna vistuðum stillingum fyrir skýrslur og runuvinnslur](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-reports"></a>Tilgreina gögnin sem eiga að vera í skýrslunum

Notið reitina undir **Valkostir** og **Síur** til að breyta takmörkunum á upplýsingum sem eiga að koma fram í skýrslunni. Síur eru stilltar í skýrslu nánast á sama hátt og þær eru stilltar í listum. Frekari upplýsingar er að finna í [Síun](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Hlutinn **Sía lista eftir** á beiðnisíðu veitir almennan síumöguleika fyrir skýrslur. Þessar síur eru valfrjálsar.
>
> Einhverjar skýrslur hunsa slíkar síur, sem þýðir að sama hvaða sía er stillt í hlutanum **Sía lista eftir** verður útkoma skýrslunnar sú sama. Ekki er hægt að gefa upp lista yfir hvaða reitir eru hunsaðir í hvaða skýrslum, þannig að þú verður að gera tilraunir með síurnar þegar þú notar þær.
>
> **Dæmi**: Þegar þú notar runuvinnsluna **Sent innheimtubréf** verður sía fyrir reitinn **Færslur í viðskiptamannabók** í **Stig síðasta útgefins innheimtubréfs** hunsuð vegna þess að síurnar eru fastar fyrir þessa runuvinnslu.

## <a name="previewing-a-report"></a>Forskoðun skýrslu

Að forskoða skýrsluna gerir notanda kleift að sjá hvernig skýrslan komi til með að líta út áður en hún er prentuð. Forskoðunin fer ekki eftir prentaranum sem valinn er í reitnum **Prentari** á beiðnisíðunni. Hún fer eftir vafranum. Að forskoðun lokinni er hægt að fara aftur á beiðnisíðuna og gera breytingar á valkostum og síum eftir þörfum.

Til að forskoða skýrslu skal velja hnappinn **Forskoða** eða **Forskoða og loka** á beiðnisíðu skýrslunnar. Hnappurinn sem birtist fer eftir skýrslunni, þannig að sumar skýrslur eru með hnappinn **Forskoða** á meðan aðrar eru með hnappinn **Forskoða og loka**. Báðir hnapparnir opna forskoðun á skýrslunni. Munurinn liggur í því að **Forskoðun** heldur beiðnisíðunni opinni, þannig að hægt er að fara aftur í hana, gera breytingar, forskoða aftur eða prenta. Með **Forskoða og loka** lokast beiðnisíðan, þannig að opna þarf skýrsluna aftur til að gera breytingar eða prenta.

> [!NOTE]
> Ef verið er að nota Business Central 2020 útgáfutímabil 1 eða eldra, er aðeins hnappurinn **Forskoða**, sem lokar beiðnisíðunni við forskoðun eins og lýst er fyrir **Forskoðun og loka**.

### <a name="working-with-the-preview"></a>Vinna með forskoðun

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

## <a name="saving-a-report-to-a-file"></a>Skýrsla vistuð í skrá

Þú getur vistað skýrslu í PDF-skjali, Microsoft Word-skjali eða Microsoft Excel-vinnublaði með því að velja hnappinn **Senda til** og svo framkvæma þitt val.

### <a name="send-to-excel"></a>Senda í Excel

<!-- The following table describes the options for saving the report results as a worksheet in an Excel workbook.

|Option  |Description  |
|---------|---------|
|Microsoft Excel Document (data and layout)|Export the report results with the RDLC layout applied. Use this option if you want to export the data one time, and only want to make minor changes to its appearance, such as font and color scheme. <br><br>**Note**: Some reports might export numbers as text, so it's a good idea to verify the numbers. |
|Microsoft Excel Document (data only)|Export the report results and the criteria that was used to generate them, such as the parameters you specified on the request page, metadata, and the fields that control the layout of the printed report. Use this option when you want to do ad hoc analysis of the data or diagnose data issues in reports. For example, you can filter the data and use Power Pivot to display it.<br><br>This option exports all columns, including columns that hold formatting instructions for other values and filters. In columns that hold binary data like images, instead of actually values, fields will include the text **Binary data ({0} bytes)**, where **{0}** indicates the number of bytes.<br><br>**NOTE** With Business Central on-premises, the Business Central Server includes a configurations setting, called **Max Data Rows Allowed to Send to Excel**. This setting limits the number of rows that can be exported to Excel. If you don't see the expected number of rows, it might be because of this setting. For more information, see [Configuring Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) or contact your administrator.|-->

Tveir valkostir eru í boði til að vista niðurstöður skýrslunnar sem vinnublað í Excel-vinnubók: **Microsoft Excel Skjal (gögn og útlit)** og **Microsoft Excel Skjal (aðeins gögn)**

#### <a name="microsoft-excel-document-data-and-layout"></a>[Microsoft Excel Skjal (gögn og útlit)](#tab/data-and-layout)

Þessi valkostur er aðeins í boði fyrir skýrslur sem nota RDLC-útlit. Hann flytur út niðurstöður skýrslunnar með RDLC-útlitinu sem er notað. Notaðu þennan valkost ef þú vilt flytja skýrsluna út einu sinni og vilt aðeins gera minniháttar breytingar á útliti hennar, t.d. á leturgerð og litaskema.

#### <a name="microsoft-excel-document-data-only"></a><a name="exportdataonly"></a>[Microsoft Excel Skjal (aðeins gögn)](#tab/data-only)

Valkosturinn **Microsoft Excel Skjal (aðeins gögn)** flytur út niðurstöður skýrslunnar og skilyrðið sem var notað til að mynda þær&mdash;en hún inniheldur ekki skýrsluútlitið. Excel-skráin mun innihalda allt gagnasafnið sem hrágögn, raðað í línur og dálka. Allir gagnadálkar í gagnasafni skýrslunnar eru innifaldir, óháð því hvort þeir eru notaðir í skýrsluútlitinu.  Notaðu þennan valkost þegar þú vilt:

- Gera tilfallandi greiningu á gögnum. Til dæmis er hægt að sía gögnin og nota Power Pivot til að sýna þau.

  Í hvert skipti sem þú flytur út niðurstöður er nýtt vinnublað búið til. Með því að nota valkostinn **Microsoft Excel Skjal (aðeins gögn)** er hægt að keyra sömu skýrsluna og endurnota sniðsbreytingar. Til dæmis fyrir Power Pivot geturðu keyrt skýrsluna aftur fyrir annað tímabil, afritað niðurstöðurnar í vinnublaðið og síðan uppfært vinnublaðið. Einnig er hægt að finna skýrslugerðarforrit í [AppSource](https://appsource.microsoft.com/).
- Skoðaðu gagnasafn skýrslunnar þegar þú býrð til eða breytir sérsniðnu útlit skýrslu.

  Upplýsingar um hvernig á að búa til sérsniðið skýrsluútlit er að finna í [Búa til eða breyta sérsniðnum skýrsluútlitum](ui-how-create-custom-report-layout.md)
- Greina gagnavandamál í skýrslum.

##### <a name="for-administrators"></a>Fyrir stjórnendur

- **Microsoft Excel Skjal (aðeins gögn)** var kynnt sem valfrjáls eiginleiki í útgáfutímabili 1, uppfærslu 18.3 fyrir árið 2021. Til að veita notendum aðgang að þessum eiginleika skal virkja eiginleikauppfærsluna **Vista gagnasafn skýrslu í Microsoft Excel skjal** í **Eiginleikastjórnun**. Frekari upplýsingar er að finna [Virkjun væntanlegra eiginleika fyrir tíma](/dynamics365/business-central/dev-itpro/administration/feature-management). Á útgáfutímabili 2 fyrir árið 2021 verður þessi eiginleiki varanlegur og þarf þá ekki að virkja hann.

- Notendareikningar þurfa heimildina **<!--Export Report Dataset To Excel-->Leyfa aðgerð til að flytja út skýrslugagnasafn í Excel** sem hægt er að gefa með því að nota heimildasamstæðuna **Verkfæri úrræðaleitar** eða heimildasamstæðuna **Flytja út skýrslu í Excel**.  

- Ekki er hægt að flytja út skýrslu sem er með fleiri en 1.048.576 línur eða 16.384 dálka.

    > [!NOTE]
    > Með Business Central á staðnum gæti hámarksfjöldi útfluttra lína verið jafnvel minni. Business Central Server inniheldur grunnstillingasafn sem kallast **Hámarksfjöldi gagnaraða sem má senda til Excel** til að minnka mörk hámarksgildisins. Frekari upplýsingar er að finna í [Skilgreining Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) eða hafa samband við stjórnanda.

##### <a name="for-developers-and-advanced-users"></a>Fyrir þróunaraðila og reynslumikla notendur

Valkosturinn **Microsoft Excel Skjal (aðeins gögn)** flytur út alla dálka, þ.m.t. dálka sem geyma leiðbeiningar um síur og snið fyrir önnur gildi. Hér eru nokkur áhugaverð atriði:

- Tvíundargögn í reit, eins og mynd, eru ekki flutt út.

  Í dálkum sem geyma tvíundargögn munu reitir innihalda textann **Tvíundargögn ({0} bæti)** þar sem **{0}** gefur til kynna fjölda bæta.
- Frá og með útgáfutímabil 2 í Business Central 2021 mun Excel-skráin einnig innihalda vinnublaðið **Lýsigögn skýrslu**.

  Þetta vinnublað sýnir síurnar sem notaðar eru í skýrslunni og almenna skýrslueiginleika eins og heiti, auðkenni og upplýsingar um viðbót. Síurnar eru sýndar í dálknum **Sía (DataItem::Table::FilterGroupNo::FieldName)**. Síurnar í þessum dálki innihalda síur sem eru stilltar á beiðnisíðu skýrslunnar. Þar eru einnig síur sem skilgreindar eru til að mynda í AL-kóða af [DataItemLink-eiginleikanum](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) og [DataItemTableView-eiginleikanum](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Frekari upplýsingar um skýrsluhönnun er að finna í [Yfirlit skýrslu](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

---

> [!NOTE]
> Sumar skýrslur flytja út tölur sem texta, sem kemur í veg fyrir að þú getir gert útreikninga eða notað Power Pivot í hólfunum í Excel-vinnublaðinu. Eftir útflutning er góð hugmynd að staðfesta tölurnar í vinnublaðinu. Ef gera á greiningu á tölunum og setja þær upp í graf skal breyta sniðinu á viðkomandi hólfum úr **Texta** í **Tölustafi**. Nánari upplýsingar um hvernig eigi að sníða tölur í hólfum er að finna í þessu myndbandi: [Tölur sniðnar í hólfum í Microsoft Excel](https://www.youtube.com/watch?v=2suE4YmZu_Q).

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Tímasetja keyrslu skýrslu

Hægt er að tímasetja eða runuvinna skýrslu þannig að hún keyri á tilteknum degi og tíma. Tímasettar skýrslur og runuvinnslur eru færðar inn í verkröð og unnar á áætluðum tíma, eins og önnur verk. Veldu valkostinn **Áætlun** eftir að hafa valið **Senda til** og færðu svo inn upplýsingar á borð við prentara, og tíma og dagsetningu. Skýrslunni er síðan bætt við verkröðina og hún verður keyrð á tilgreindum tíma. Þegar skýrslan hefur verið meðhöndluð er varan fjarlægð úr verkröðinni. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).  

Þegar keyrsla skýrslu er áætluð er hægt að tilgreina að keyra þurfi alla fimmtudaga með því að stilla reitinn **Reikniregla næstu keyrsludagsetningar** á t.d. *D4*. Frekari upplýsingar er að finna í [Að nota dagsetningarreiknireglur](ui-enter-date-ranges.md#using-date-formulas).  

Hægt er að velja að vista skýrsluna í skrá (t.d. Excel, Word, eða PDF), prenta hana eða aðeins búa til skýrsluna. Ef þú velur að vista skýrsluna í skrá þá er meðhöndlaða skýrslan send á svæðið **Skýrsluinnhólf** á Mitt hlutverk þar sem þú getur skoðað hana.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Prenta skýrslu

Til að prenta skýrslu skal velja hnappinn **Prenta** á beiðnisíðunni eða valmyndastikunni á síðunni **Forskoða**.

### <a name="printer"></a><a name="Printer"></a>Prentari

Reiturinn **Prentari** á beiðnisíðunni sýnir heiti prentarans sem skýrslan verður send til. Til að breyta prentara skal einfaldlega velja prentarann úr listanum.

> [!NOTE]
> **(Meðhöndlað af vafra)** gefur til kynna að enginn prentari sé valinn fyrir skýrsluna. Í slíku tilfelli sér vafrinn um útprentun og sýnir hefðbundið viðmót þar sem hægt er velja staðbundinn prentara sem tengdur er við tækið þitt. **(Meðhöndlað af vafra)** er ekki í boði í farsímaforriti [!INCLUDE[prod_short](includes/prod_short.md)] eða forrit fyrir Microsoft Teams.

> [!TIP]
> Prentarinn sem er sjálfgefið valinn fyrir þig er settur upp á síðunni **Prentaraval**. Upplýsingar um hvernig á að breyta sjálfgefnum prentara er að finna í [Að velja hvaða prentara prenta hvaða skýrslur](ui-specify-printer-selection-reports.md#default).

### <a name="printing-reports-in-thai"></a>Prenta skýrslur á taílensku

Sérstaklega fyrir taílensku útgáfuna af [!INCLUDE[prod_short](includes/prod_short.md)], getur hnappurinn **Prenta** ekki prentað skýrslur rétt vegna takmarkana á þjónustunni sem býr til prentanlegt PDF-skjal. Í staðinn getur þú opnað skýrsluna í Word og síðan vistað hana sem prentvæna PDF-skrá.  

Eða þú getur beðið stjórnanda þinn um að búa til Word-skýrsluútlit fyrir mest notuðu skýrslurnar. Frekari upplýsingar, sjá [Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Breyting skýrsluútlita

Skýrsluútlit stjórnar því hvað er sýnt í skýrslu, hvernig því er stillt upp og það stílfært. Ef þú vilt skipta yfir í annað útlit skaltu skoða [Breyta núverandi skýrsluútliti](ui-how-change-layout-currently-used-report.md). Eða, ef þú vilt sérsníða þitt eigið skýrsluútlit, sjá [Búa til og breyta sérsniðnu skýrsluútliti](ui-how-create-custom-report-layout.md).

## <a name="advanced-options"></a>Ítarlegir valkostir

Reitirnir undir **Ítarlegt** setja takmarkanir á myndaða skýrslu til að stjórna tilföngum prentarans. Yfirleitt þarf ekki að breyta þessum stillingum nema um stóra skýrslu sé að ræða. Ef skýrsla fer umfram þessar takmarkanir þegar reynt er að forskoða eða prenta, birtast skilaboð sem segja til um hvaða takmörkun var farið yfir. Síðan er hægt að breyta stillingunum svo þær henti skýrslunni betur. Hver reitur er hinsvegar með hámarksgildi sem hafa ætti í huga:

|Svæði|Hámarksgildi|
|-----|-------------|
|Hámarksmyndunartími|12:00:00|
|Hámarksfjöldi lína|1000000|
|Hámarksfjöldi skjala|500|

> [!NOTE]
> Hámarksgildin kunna að vera mismunandi fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum og stjórnandi getur breytt þeim. Frekari upplýsingar er að finna í [Skilgreining Business Central Server - Skýrslur](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Fyrir yfirlit yfir takmarkanir á skýrslum í [!INCLUDE[prod_short](includes/prod_short.md)] á netinu, skal skoða [Rekstrarlegar takmarkanir](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-also"></a>Sjá einnig

[Setja upp prentara](ui-specify-printer-selection-reports.md)  
[Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md)  
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]