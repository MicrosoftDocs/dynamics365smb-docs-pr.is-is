---
title: Keyra og prenta skýrslur í Business Central
description: Kynntu þér hvernig skal setja skýrslu inn í verkröð og tímasetja hana þannig að hún sé unnin á tilteknum degi og tíma.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, Word, dataset'
ms.search.form: null
ms.date: 06/13/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="run-and-print-reports-in-business-central"></a>Keyra og prenta skýrslur í Business Central

Skýrslur hjálpa til við söfnun og birtingu gagna út frá tilteknum skilyrðum. Hún flokkar og birtir upplýsingarnar á sniði sem er auðvelt að lesa og sem hægt er að prenta eða vista sem skrá. Hægt er að opna margar skýrslur í gegnum forritið. Skýrslurnar veita alla jafna upplýsingar sem tengjast samhengi síðunnar sem þú ert á. Til dæmis, síðan **Viðskiptamaður** inniheldur skýrslur fyrir efstu 10 viðskiptamennina, sölutölur og fleira.

> [!NOTE]
> Keyrslur og XMLports gera meira eða minna það sama og í skýrslum, en eru notaðar meira til að vinna úr eða flytja út gögn. Keyrslan **Stofna innheimtubréf stofnar til dæmis** áminningarskjöl til að senda viðskiptamönnum með gjaldfallnar greiðslur. Þessi grein vísar aðallega í „skýrslur“, en svipaðar upplýsingar gilda um runuvinnslur og XMLport.

## <a name="get-started"></a>Hefjast handa

Finna má skýrslur í valmyndinni **Skýrslur** á völdum síðum, listum og spjöldum. Einnig er hægt að nota leitarljósin ![sem opna eiginleikann Tell Me.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") til að finna skýrslur eftir nafni. Yfirlit yfir innbyggðar skýrslur er hægt að nota í [!INCLUDE[prod_short](includes/prod_short.md)], raðað eftir flokkum, sjá [Tiltækar skýrslur í [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md).

Þegar skýrsla er valin sést beiðnisíða sem nefnd er eftir heiti skýrslunnar þar sem settir eru ýmsir valkostir og afmarkanir sem ákvarða hvaða gögn eru innifalin. Eftirfarandi hlutar útskýra hvernig á að nota beiðnisíðuna til að búa til, forskoða og prenta út skýrslur.

## <a name="use-default-valuesmdashpredefined-settings"></a><a name="SavedSettings"></a>Nota fyrirfram skilgreindar&mdash; stillingar sjálfgefinna gilda

Flestar síður skýrslubeiðni innihalda reitinn **Nota sjálfgefin gildi úr**. Með þessum reit er hægt að velja fyrirfram skilgreindar stillingar fyrir skýrsluna sem stilla sjálfkrafa valkosti og afmarkanir. Veldu færslu úr fellilistanum til að sjá valkosti og síur á síðu skýrslubeiðni breytast í samræmi.

Færslan sem kallast **Valkostir og síur síðast notað** er alltaf í boði. Þessi færsla stillir skýrsluna á að nota valkosti og síur sem voru síðast notuð þegar skýrslan var keyrð.

Reiturinn **Nota sjálfgildi úr** veitir fljótlega og áreiðanlega leið til að búa til skýrslur sem innihalda réttar upplýsingar. Þegar færsla hefur verið valin er hægt að breyta valkostum og afmörkunum áður en skýrslan er forskoðuð eða prentuð. Breytingarnar sem þú gerir verða ekki vistaðar í færslu fyrirframskilgreindrar stillinga sem þú valdir, en þær verða vistaðar í færslunni **Síðast notaðir valkostir og afmarkanir**.

> [!NOTE]
> Fyrirframskilgreindar stillingar eru yfirleitt settar upp og stjórnað af stjórnanda. Frekari upplýsingar er að finna í [Stjórna vistuðum stillingum fyrir skýrslur og runuvinnslur](reports-saving-reusing-settings.md).

## <a name="specify-the-data-to-include-in-a-report"></a>Tilgreina gögnin sem eiga að vera í skýrslu

Notaðu reitina undir **Valkostir** og **Síur** til að breyta eða takmarka upplýsingarnar sem eiga að koma fram í skýrslunni. Hægt er að stilla síur í skýrslu nánast á sama hátt og þær eru stilltar í listum. Frekari upplýsingar er að finna í hlutanum [Síun](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Flýtiflipinn **Sía** á síðu skýrslubeiðni býður upp á almenna síunarmöguleika fyrir skýrslur. Þessar síur eru valfrjálsar.
>
> Sumar skýrslur hunsa allar slíkar afmarkanir sem þýðir að sama hvaða afmörkun er stillt á flýtiflipanum **Afmörkun** er frálag skýrslunnar það sama. Ekki er hægt að gefa upp lista yfir hvaða reitir eru hunsaðir í hvaða skýrslum, þannig að þú verður að gera tilraunir með síurnar þegar þú notar þær.
>
> **Dæmi**: Þegar þú notar runuvinnsluna **Stofna innheimtubréf** er sía fyrir reitinn **Færslur í viðskiptamannabók** í **Stig síðasta útgefins innheimtubréfs** hunsuð vegna þess að síurnar eru fastar fyrir þessa runuvinnslu.

## <a name="preview-a-report"></a>Forskoða skýrslu

Með því að forskoða skýrslu geturðu séð hvernig skýrslan kemur til með að líta út áður en hún er prentuð. Forskoðunin fer ekki eftir prentaranum sem valinn er í reitnum **Prentari** á beiðnisíðunni. Hún fer eftir vafranum. Eftir forskoðun er hægt að fara aftur á beiðnisíðuna og gera breytingar á valkostum og afmörkunum eftir þörfum.

Forskoðunarvalið á síðunni **Skýrslubeiðni** fer eftir skýrslunni. Svo, fyrir sumar skýrslur, getur þú valið **Forskoðun**, en fyrir aðrar er **valið Forskoðun > Loka**. Báðir valkostirnir opna forskoðun á skýrslunni. Munurinn liggur í því að **Forskoðun** heldur beiðnisíðunni opinni, þannig að hægt er að fara aftur í hana, gera breytingar, forskoða aftur eða prenta. Aftur á móti lokast beiðnisíðan með **Forskoða og loka** og opna þarf skýrsluna aftur til að gera breytingar eða prenta.

> [!NOTE]
> Ef þú notar Business Central 2020 útgáfutímabil 1 eða eldra er eini kosturinn **Forskoða**, sem lokar beiðnisíðunni við forskoðun, eins og lýst er hér að ofan fyrir **Forskoða og loka**.

### <a name="work-with-the-preview"></a>Vinna með forskoðunina

Í forskoðun skal nota valmyndastikuna í forskoðun skýrslunnar til að:

- Fara gegnum síður
- Auka aðdrátt og minnka
- Breyta stærð svo passi á síðu
- Velja texta
  
  Þú getur afritað texta úr skýrslu og svo límt hann eitthvert annað, eins og á síðu í [!INCLUDE[prod_short](includes/prod_short.md)] eða Microsoft Word. Mús er til dæmis notuð til að velja vinstri músarhnappinn og halda þar sem ætlunin er að byrja. Færðu svo músina til til að velja eitt eða fleiri orð, setningar eða málsgreinar. Síðan er hægri músarhnappurinn valinn og Afrita **valið**. Nú geturðu límt valinn texta þar sem þú vilt hafa hann.

- Fletta skjali
  
  Hægt er að færa sjáanlega svæði skýrslunnar í hvaða átt sem er til að skoða önnur svæði skýrslunnar. Fletting er gagnleg þegar þú hefur aukið aðdrátt til að sjá smáatriði. Músin er til dæmis notuð til að velja og halda vinstri músarhnappnum hvar sem er í forskoðun skýrslunnar og færa síðan músina til að velja hluta skýrslunnar.

- Hlaða niður PDF-skrá á tölvuna eða netið.
- Prenta

## <a name="save-a-report-to-a-file"></a>Vista skýrslu í skrá

Þú getur vistað skýrslu sem PDF-skjal, Microsoft Word-skjal, Microsoft Excel-vinnubók eða XML-skjal með því að velja **Senda til** og síðan velja. Skrá er sótt á tölvuna.

Ef fyrirtækið þitt hefur grunnstillt OneDrive fyrir kerfiseiginleika, í stað þess að vera sótt, eru Excel vinnubækur og Word-skjöl opnuð í vafranum þínum með því að nota annaðhvort Excel eða Word fyrir vefinn.

> [!TIP]
> Valkostirnir **Microsoft Excel Skjal (aðeins gögn)** og **XML-skjal** eru mest megnis fyrir flóknari tilgang. Yfirleitt notar þú þessa valkosti til að gera ítarlega greiningu á gögnum. Frekari upplýsingar er að finna í [Greining skýrslugagna með Excel og XML](report-analyze-excel.md).
>
> Einnig er hægt að nota **Microsoft Excel Skjal (aðeins gögn)** til að búa til nýtt Excel-útlit fyrir ákveðna skýrslu. Frekari upplýsingar er að finna í [Vinna með Excel-útlit](ui-excel-report-layouts.md).  

## <a name="schedule-a-report-to-run-later-or-periodically"></a><a name="ScheduleReport"></a>Tímasetja skýrslu sem á að keyra síðar eða reglulega

Hægt er að tímasetja eina eða endurtekna skýrslu þannig að hún keyri á tilteknum degi og tíma. Tímasettar skýrslur eru færðar inn í verkröð og unnar á settum tíma, eins og önnur verk. Valkosturinn **Tímasetning** er valinn eftir að **senda er** valið, síðan eru færðar inn upplýsingar eins og prentarinn og tími og dagsetning. Skýrslunni er bætt við verkröðina og verður keyrð á tilgreindum tíma. Þegar unnið hefur verið úr skýrslunni er varan fjarlægð úr verkröðinni. Frekari upplýsingar eru í [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).  

Þegar keyrsla skýrslu er áætluð er til dæmis hægt að tilgreina að keyra þurfi alla fimmtudaga með því að stilla reitinn **Dagsetningarformúla næstu keyrslu** á *D4*. Frekari upplýsingar er að finna í hlutanum [Nota dagsetningarformúlur](ui-enter-date-ranges.md#use-date-formulas).  

Hægt er að vista skýrsluna í skrá (t.d. Excel, Word eða PDF), prenta hana eða búa hana aðeins til. Ef skýrslan er vistuð í skrá er unnin skýrsla send **á síðuna Skýrsluinnhólf** í Mínu hlutverki til að skoða hana. Frekari upplýsingar er að finna í [Deila og flytja út skýrslur með skýrsluinnhólfinu](ui-work-report-inbox.md)

### <a name="manage-scheduled-recurring-reports"></a>Stjórna tímasettum endurteknum skýrslum

Keyrslur mynda tímasettar skýrslur sem stjórnað er á síðunni **Verkraðarfærslur** . Hægt er að sjá stöðu hverrar skýrslu og aðrar upplýsingar á síðunni, gera hlé á skýrslukeyrslunni og búa til skýrslu um eftirspurn.

Á síðunni **Verkraðarfærslur** er einnig hægt að breyta nokkrum skýrslufæribreytum eins og gerð úttaksskráar, endurtekningu, keyrsludagsetningu og upphafs- og lokatímum. Áður en tímasettri skýrslu er breytt er hins vegar nauðsynlegt að setja skýrsluverkröðina í bið:

1.  ![Veldu Lightbulb sem opnar Tell Me aðgerð 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **verkraðarfærslur** og velja síðan viðeigandi tengil.  
2. Á síðunni **Verkraðarfærslur** skal velja skýrsluna sem óskað er eftir.
3. Veljið aðgerðina Setja í **bið** .
4. Opnaðu og breyttu tímasettu skýrslunni með því að velja stöðu hennar (*Í bið*).

Þegar skýrsluvalkostum hefur verið breytt skal endurtaka fyrstu tvö þrepin og velja svo aðgerðina **Setja stöðu á tilbúið** til að hefja skýrsluna aftur.

Frekari upplýsingar um stjórnun verkraðar er að finna í [Nota verkraðir til að tímasetja verk](admin-job-queues-schedule-tasks.md).  

## <a name="print-a-report"></a><a name="PrintReport"></a>Prenta skýrslu

Til að prenta skýrslu er Valið **Prenta** á skýrslubeiðnisíðunni eða á valmyndarstikunni **á forskoðunarsíðunni** .

Þegar skýrslan notar Excel-uppsetningu birtist ekki hnapparnir **Prentari** eða **Prenta** eða **Forskoðun** . Í staðinn er valkosturinn **Hlaða niður**. Til að prenta skal velja **Hlaða niður** og síðan opna sóttu skrána í Excel og prenta þaðan.

### <a name="printer"></a><a name="Printer"></a>Prentari

Reiturinn **Prentari** á beiðnisíðunni sýnir heiti prentarans sem skýrslan er send til. Til að breyta prentara skal einfaldlega velja prentarann úr listanum.

> [!NOTE]
> Valkosturinn **(Meðhöndlað af vafra)** gefur til kynna að enginn prentari sé valinn fyrir skýrsluna. Þá sér vafrinn um útprentunina og birtir stöðluðu prentskrefin þar sem hægt er að velja staðbundinn prentara sem tengdur er við tölvuna. Valkosturinn **(Meðhöndlað af vafra)** er ekki í boði í [!INCLUDE[prod_short](includes/prod_short.md)]-farsímaforriti eða forriti fyrir Microsoft Teams.

> [!TIP]
> Prentarinn sem er sjálfgefið valinn fyrir þig er settur upp á síðunni **Prentaraval**. Fræðast meira um hvernig hægt er að breyta sjálfgefnum prentara í hlutanum [Setja upp sjálfgefna prentara](ui-specify-printer-selection-reports.md#default) .

### <a name="print-reports-in-thai"></a>Prenta skýrslur í tælenskum

Sérstaklega fyrir taílensku útgáfuna af [!INCLUDE[prod_short](includes/prod_short.md)], getur hnappurinn **Prenta** ekki prentað skýrslur rétt vegna takmarkana á þjónustunni sem býr til prentanlegt PDF-skjal. Í staðinn getur þú opnað skýrsluna í Word og síðan vistað hana sem prentvæna PDF-skrá.  

Eða þú getur beðið stjórnanda þinn um að búa til Word-skýrsluútlit fyrir mest notuðu skýrslurnar. Frekari upplýsingar er að finna í [Stjórna skýrslu- og skjalaútliti](ui-manage-report-layouts.md).  

## <a name="switch-the-report-layout"></a>Skipta um skýrsluútlit

Skýrsluútlit stjórnar því hvað er sýnt í skýrslu, hvernig því er stillt upp og það stílfært. Nokkrar leiðir eru í boði til að breyta útlitinu:

- Þegar þú setur upp og keyrir skýrslu sérðu núverandi útlit í reitnum **Skýrsluútlit** á beiðnisíðunni. Til að skipta tímabundið yfir í annað útlit er reiturinn **Skýrsluútlit** valinn og síðan valinn af lista yfir tiltækar útlitsskýrslur fyrir skýrsluna.
- Til að breyta sjálfgefnu útliti sem skýrsla notar skal annaðhvort fara á síðuna **Skýrsluútlit** eða **Val á skýrsluútliti**.

Frekari upplýsingar er að finna í [Stilla útlitið sem skýrslan notar](ui-set-report-layout.md). Einnig má sjá Hafist handa við að stofna útlit [ef sérsníða á eigin skýrsluútlit](ui-get-started-layouts.md).

## <a name="change-language-and-format-of-numbers-dates-and-times"></a>Breyta tungumáli og sniði talna, dagsetninga og tíma

Sjálfgefið er að tungumál texta og sniðs talna, dagsetninga og tímasetninga í skýrslu séu byggðar á vinnutungumáli þínu og svæðisstillingum, sem eru skilgreindar á síðunni **Mínar** stillingar. Hins vegar er hægt að breyta svæðum tungumáls og sniðs þegar skýrsla er forskoðuð, prentað eða sent skýrslu. Á beiðnisíðunni eru valkostirnir Tungumála- **og** sniðsvæði **stilltir** á kjörstillingar notanda. Einnig er hægt að tilgreina tungumála- og svæðissnið sem á að nota sjálfgefið fyrir viðskiptamenn og lánardrottna á spjaldsíðum þeirra.

Eftir því hvar tilgreindar hafa verið stillingar [!INCLUDE [prod_short](includes/prod_short.md)]  tungumáls og sniðs ákvarðar stillingarnar sem á að nota í eftirfarandi röð:

1. Stillingarnar sem eru tilgreindar þegar skýrsla er búin til.
2. Stillingarnar sem tilgreindar eru á skjalinu, sem koma úr stillingum viðskiptamanns eða lánardrottins.
3. Stillingarnar sem tilgreindar eru í skýrslunni AL-hlutur.
4. Stillingarnar sem skilgreindar eru í Mínar stillingar.

Nánari upplýsingar um síðuna Mínar **stillingar eru í** Breyta grunnstillingum [.](ui-change-basic-settings.md#region)

## <a name="advanced-options"></a>Ítarlegir valkostir

Reitirnir undir flýtiflipanum **Ítarlegt** setja takmarkanir á útbúna skýrslu til að stjórna tilföngum prentarans. Yfirleitt þarf ekki að breyta þessum stillingum nema um stóra skýrslu sé að ræða. Ef skýrsla fer yfir þessar takmarkanir þegar reynt er að forskoða eða prenta birtast skilaboð um hvaða takmörkun hefur farið fram úr. Síðan er hægt að breyta stillingunum svo þær henti skýrslunni betur. Hver reitur er hinsvegar með hámarksgildi sem hafa ætti í huga:

|Svæði|Hámarksgildi|
|-----|-------------|
|Hámarksmyndunartími|12:00:00|
|Hámarksfjöldi lína|1000000|
|Hámarksfjöldi skjala|500|

> [!NOTE]
> Hámarksgildin kunna að vera mismunandi fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum og stjórnandi getur breytt þeim. Frekari upplýsingar er að finna í hlutanum [Grunnstilling Business Central Server - Skýrslur](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Fyrir yfirlit yfir skýrslutakmarkanir í [!INCLUDE[prod_short](includes/prod_short.md)] á netinu skal skoða [Rekstrarlegar takmarkanir](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-also"></a>Sjá einnig .

- [Tiltækar skýrslur í [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
- [Nota skýrslur í daglegu starfi](reports-use-reports.md)  
- [Viðskiptagreind og skýrsluyfirlit](reports-bi-reporting.md)  
- [Setja upp prentara](ui-specify-printer-selection-reports.md)  
- [Keyra runuvinnslur og XMLports](ui-how-run-batch-jobs.md)  
- [Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md)  
- [Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
- [Viðskiptagreind fjármála](bi.md)  
- [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
