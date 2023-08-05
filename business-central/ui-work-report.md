---
title: Keyra og prenta skýrslur
description: Kynntu þér hvernig skal setja skýrslu inn í verkröð og tímasetja hana þannig að hún sé unnin á tilteknum degi og tíma.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, Word, dataset'
ms.search.form: null
ms.date: 09/09/2022
ms.author: jswymer
---
# Keyra og prenta skýrslur

Skýrsla safnar saman upplýsingum byggðum á sérstöku safni af skilyrðum. Hún flokkar og birtir upplýsingarnar á sniði sem er auðvelt að lesa og sem hægt er að prenta eða vista sem skrá. Hægt er að opna margar skýrslur í gegnum forritið. Skýrslurnar veita alla jafna upplýsingar sem tengjast samhengi síðunnar sem þú ert á. Til dæmis, síðan **Viðskiptamaður** inniheldur skýrslur fyrir efstu 10 viðskiptamennina, sölutölur og fleira.

> [!NOTE]
> Runuvinnslur og XMLports gera meira eða minna það sama og skýrslur, en eru meira notaðar í þeim tilgangi að vinna úr og flytja út gögn. Til dæmis býr runuvinnslan **Stofna innheimtubréf** til innheimtuskjöl til að senda á viðskiptamenn með gjaldfallnar greiðslur. Þessi grein vísar aðallega í „skýrslur“, en svipaðar upplýsingar gilda um runuvinnslur og XMLport.

## Hafist handa

Þú finnur skýrslur í flipanum **Skýrslur** á völdum síðum, listum og spjöldum eða þú getur leitað með ![Ljósaperunni sem opnar eiginleika viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") til að finna skýrslur eftir nafni. Yfirlit yfir innbyggðar skýrslur sem þú getur notað í [!INCLUDE[prod_short](includes/prod_short.md)], raðað eftir flokkum, er að finna í [Tiltækar skýrslur í [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md).

Þegar þú velur skýrslu færðu yfirleitt upp beiðnisíðu&mdash;sem ber heiti skýrslunnar&mdash;þar sem þú velur ýmsa valkosti og síur sem ákvarða hvaða gögn eru innifalin. Eftirfarandi hlutar útskýra hvernig á að nota beiðnisíðuna til að búa til, forskoða og prenta út skýrslur.

## <a name="SavedSettings"></a>Sjálfgefin gildi notuð&mdash;fyrirframskilgreindar stillingar

Flestar síður skýrslubeiðni innihalda reitinn **Nota sjálfgefin gildi úr**. Með þessum reit geturðu valið fyrirframskilgreindar stillingar fyrir skýrsluna, sem velur valkosti og síur sjálfkrafa. Veldu færslu úr fellilistanum til að sjá valkosti og síur á síðu skýrslubeiðni breytast í samræmi.

Færslan sem kallast **Valkostir og síur síðast notað** er alltaf í boði. Þessi færsla stillir skýrsluna á að nota valkosti og síur sem voru síðast notuð þegar skýrslan var keyrð.

Reiturinn **Nota sjálfgildi úr** veitir fljótlega og áreiðanlega leið til að búa til skýrslur sem innihalda réttar upplýsingar. Þegar færsla er valin, er hægt að breyta öllum valkostum og síum áður skýrslan er forskoðuð eða prentuð. Breytingarnar sem þú gerir verða ekki vistaðar í færslu fyrirframskilgreindrar stillinga sem þú valdir, en þær verða vistaðar í færslunni **Síðast notaðir valkostir og afmarkanir**.

> [!NOTE]
> Fyrirframskilgreindar stillingar eru yfirleitt settar upp og stjórnað af stjórnanda. Frekari upplýsingar er að finna í [Stjórna vistuðum stillingum fyrir skýrslur og runuvinnslur](reports-saving-reusing-settings.md).

## Tilgreina gögnin sem eiga að vera í skýrslu

Notaðu reitina undir **Valkostir** og **Síur** til að breyta eða takmarka upplýsingarnar sem eiga að koma fram í skýrslunni. Hægt er að stilla síur í skýrslu nánast á sama hátt og þær eru stilltar í listum. Frekari upplýsingar er að finna í hlutanum [Síun](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Flýtiflipinn **Sía** á síðu skýrslubeiðni býður upp á almenna síunarmöguleika fyrir skýrslur. Þessar síur eru valfrjálsar.
>
> Sumar skýrslur hunsa slíkar síur, sem þýðir að sama hvaða sía er stillt í flýtiflipanum **Sía** verður útkoma skýrslunnar sú sama. Ekki er hægt að gefa upp lista yfir hvaða reitir eru hunsaðir í hvaða skýrslum, þannig að þú verður að gera tilraunir með síurnar þegar þú notar þær.
>
> **Dæmi**: Þegar þú notar runuvinnsluna **Stofna innheimtubréf** er sía fyrir reitinn **Færslur í viðskiptamannabók** í **Stig síðasta útgefins innheimtubréfs** hunsuð vegna þess að síurnar eru fastar fyrir þessa runuvinnslu.

## Forskoða skýrslu

Með því að forskoða skýrslu geturðu séð hvernig skýrslan kemur til með að líta út áður en hún er prentuð. Forskoðunin fer ekki eftir prentaranum sem valinn er í reitnum **Prentari** á beiðnisíðunni. Hún fer eftir vafranum. Að forskoðun lokinni er hægt að fara aftur á beiðnisíðuna og gera breytingar á valkostum og síum eftir þörfum.

Forskoðunarvalið á síðunni **Skýrslubeiðni** fer eftir skýrslunni. Fyrir sumar skýrslur er því hægt að velja **Forskoða** en fyrir aðrar er valið **Forskoða og loka**. Báðir valkostirnir opna forskoðun á skýrslunni. Munurinn liggur í því að **Forskoðun** heldur beiðnisíðunni opinni, þannig að hægt er að fara aftur í hana, gera breytingar, forskoða aftur eða prenta. Aftur á móti lokast beiðnisíðan með **Forskoða og loka** og opna þarf skýrsluna aftur til að gera breytingar eða prenta.

> [!NOTE]
> Ef þú notar Business Central 2020 útgáfutímabil 1 eða eldra er eini kosturinn **Forskoða**, sem lokar beiðnisíðunni við forskoðun, eins og lýst er hér að ofan fyrir **Forskoða og loka**.

### Vinna með forskoðunina

Í forskoðun skal nota valmyndastikuna í forskoðun skýrslunnar til að:

- Fara gegnum síður
- Auka aðdrátt og minnka
- Breyta stærð svo passi á síðu
- Velja texta

    Þú getur afritað texta úr skýrslu og svo límt hann eitthvert annað, eins og á síðu í [!INCLUDE[prod_short](includes/prod_short.md)] eða Microsoft Word. Með því að nota mús er til dæmis valinn vinstri músarhnappur og haldið þar sem byrjað er á að ræsa. Færðu svo músina til til að velja eitt eða fleiri orð, setningar eða málsgreinar. Þá er hægri músarhnapp valinn og valið  **Afrita**. Nú geturðu límt valinn texta þar sem þú vilt hafa hann.
- Fletta skjali

    Hægt er að færa sjáanlega svæði skýrslunnar í hvaða átt sem er til að skoða önnur svæði skýrslunnar. Fletting er gagnleg þegar þú hefur aukið aðdrátt til að sjá smáatriði. Músin er notuð til dæmis með því að velja og halda vinstri músarhnappi hvert sem er í skýrsluforskoðun skýrslunnar og músin færð til að velja hluta skýrslunnar.

- Hlaða niður PDF-skrá á tölvuna eða netið.
- Prenta

## Skýrsla vistuð í skrá

Þú getur vistað skýrslu sem PDF-skjal, Microsoft Word-skjal, Microsoft Excel-vinnubók eða XML-skjal með því að velja **Senda til** og síðan velja. Skrá er sótt í tækið.

Ef fyrirtækið þitt hefur grunnstillt OneDrive fyrir kerfiseiginleika, í stað þess að vera sótt, eru Excel vinnubækur og Word-skjöl opnuð í vafranum þínum með því að nota annaðhvort Excel eða Word fyrir vefinn.

> [!TIP]
> Valkostirnir **Microsoft Excel Skjal (aðeins gögn)** og **XML-skjal** eru mest megnis fyrir flóknari tilgang. Yfirleitt notar þú þessa valkosti til að gera ítarlega greiningu á gögnum. Frekari upplýsingar er að finna í [Greining skýrslugagna með Excel og XML](report-analyze-excel.md).
>
> Einnig er hægt að nota **Microsoft Excel Skjal (aðeins gögn)** til að búa til nýtt Excel-útlit fyrir ákveðna skýrslu. Frekari upplýsingar er að finna í [Vinna með Excel-útlit](ui-excel-report-layouts.md).  

## <a name="ScheduleReport"></a>Skýrsla tímasett á að keyra síðar eða reglubundið

Hægt er að tímasetja eina eða endurtekna skýrslu þannig að hún keyri á tilteknum degi og tíma. Tímasettar skýrslur eru færðar inn í verkröð og unnar á settum tíma, eins og önnur verk. Veldu valkostinn **Áætlun** eftir að þú hefur valið **Senda til** og sláðu síðan inn upplýsingar, eins og prentara og tíma og dagsetningu. Skýrslunni er bætt við verkröðina og verður keyrð á tilgreindum tíma. Þegar unnið hefur verið úr skýrslunni er varan fjarlægð úr verkröðinni. Frekari upplýsingar eru í [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).  

Þegar keyrsla skýrslu er áætluð er til dæmis hægt að tilgreina að keyra þurfi alla fimmtudaga með því að stilla reitinn **Dagsetningarformúla næstu keyrslu** á *D4*. Frekari upplýsingar er að finna í hlutanum [Nota dagsetningarformúlur](ui-enter-date-ranges.md#use-date-formulas).  

Hægt er að velja að vista skýrsluna í skrá (t.d. Excel, Word, eða PDF), prenta hana eða aðeins búa til skýrsluna. Ef þú velur að vista skýrsluna í skrá þá er meðhöndlaða skýrslan send á síðuna **Skýrsluinnhólf** á Mitt hlutverk þar sem þú getur skoðað hana. Frekari upplýsingar er að finna í [Deila og flytja út skýrslur með skýrsluinnhólfinu](ui-work-report-inbox.md)

### Stjórna tímasettum endurteknum skýrslum

Tímasettar skýrslur eru búnar til með runuvinnslum sem stjórnað er á síðunni **Verkraðarfærslur**. Hægt er að sjá stöðuna og aðrar upplýsingar fyrir hverja skýrslu á síðunni, gera hlé á/endurtaka runuvinnslu skýrslunnar og búa til skýrsluna eftir eftirspurn.

Á síðunni **Verkraðarfærslur** er einnig hægt að breyta nokkrum skýrslufæribreytum eins og gerð úttaksskráar, endurtekningu, keyrsludagsetningu og upphafs- og lokatímum. Áður en fyrirliggjandi tímasettri skýrslu er breytt er hins vegar nauðsynlegt að setja verkröð skýrslunnar í bið:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar 1.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verkraðarfærslur**, velja síðan viðkomandi tengil.  
2. Á síðunni **Verkraðarfærslur** skal velja æskilega skýrslu.
3. Veldu aðgerðina **Setja í bið**.
4. Opnaðu og breyttu tímasettu skýrslunni með því að velja stöðu hennar (*Í bið*).

Eftir að valkostum skýrslunnar er breytt skal endurtaka fyrstu tvö skrefin og velja  **síðan Stilla stöðu í tilbúnar**  Aðgerðir til að halda áfram að mynda skýrsluna.

Frekari upplýsingar um stjórnun verkraðar er að finna í [Nota verkraðir til að tímasetja verk](admin-job-queues-schedule-tasks.md).  

## <a name="PrintReport"></a>Prenta skýrslu

Til að prenta skýrslu skal velja hnappinn **Prenta** á síðu skýrslubeiðninnar eða í valmyndastikunni á síðunni **Forskoða**.

Þegar skýrsla notar Excel-útlit sérðu ekki reitinn **Prentari** eða hnappana **Prenta** eða **Forskoða**. Í staðinn er valkosturinn **Hlaða niður**. Til að prenta skal velja **Hlaða niður** og síðan opna sóttu skrána í Excel og prenta þaðan.

### <a name="Printer"></a>Prentari

Reiturinn **Prentari** á beiðnisíðunni sýnir heiti prentarans sem skýrslan er send til. Til að breyta prentara skal einfaldlega velja prentarann úr listanum.

> [!NOTE]
> Valkosturinn **(Meðhöndlað af vafra)** gefur til kynna að enginn prentari sé valinn fyrir skýrsluna. Í slíku tilfelli sér vafrinn um útprentun og sýnir stöðluð skref útprentunar þar sem hægt er velja staðbundinn prentara sem tengdur er við tækið þitt. Valkosturinn **(Meðhöndlað af vafra)** er ekki í boði í [!INCLUDE[prod_short](includes/prod_short.md)]-farsímaforriti eða forriti fyrir Microsoft Teams.

> [!TIP]
> Prentarinn sem er sjálfgefið valinn fyrir þig er settur upp á síðunni **Prentaraval**. Frekari upplýsingar um að breyta sjálfgefnum prentara er að finna í hlutanum [Setja upp sjálfgefna prentara](ui-specify-printer-selection-reports.md#default).

### Býr til skýrslu í Thai

Sérstaklega fyrir taílensku útgáfuna af [!INCLUDE[prod_short](includes/prod_short.md)], getur hnappurinn **Prenta** ekki prentað skýrslur rétt vegna takmarkana á þjónustunni sem býr til prentanlegt PDF-skjal. Í staðinn getur þú opnað skýrsluna í Word og síðan vistað hana sem prentvæna PDF-skrá.  

Eða þú getur beðið stjórnanda þinn um að búa til Word-skýrsluútlit fyrir mest notuðu skýrslurnar. Frekari upplýsingar er að finna í [Stjórna skýrslu- og skjalaútliti](ui-manage-report-layouts.md).  

## Skipt um skýrsluútlit

Skýrsluútlit stjórnar því hvað er sýnt í skýrslu, hvernig því er stillt upp og það stílfært. Nokkrar leiðir eru í boði til að breyta útlitinu:

- Þegar þú setur upp og keyrir skýrslu sérðu núverandi útlit í reitnum **Skýrsluútlit** á beiðnisíðunni. Til að skipta tímabundið yfir á annað útlit skal velja reitinn **Skýrsluútlit**, síðan velja úr listanum yfir tiltækt útlit fyrir skýrsluna.
- Til að breyta sjálfgefnu útliti sem skýrsla notar skal annaðhvort fara á síðuna **Skýrsluútlit** eða **Val á skýrsluútliti**.

Frekari upplýsingar er að finna í [Stilla útlitið sem skýrslan notar](ui-set-report-layout.md). Eða ef þú vilt sérstilla þitt eigið skýrsluútlit skaltu fara í [Hefjast handa við að búa til útlit](ui-get-started-layouts.md).

## Breyta tungumáli og sniði talna, dagsetninga og tíma

Sjálfgefið er að tungumál texta og snið númera, dagsetninga og tíma í skýrslu séu byggð á vinnutungumáli og svæðisstillingum sem skilgreindar eru á  **síðunni mínar stillingar** . Annars vegar er hægt að breyta tungumáli og sníða svæðið á Málsnið máls þegar það er Forskoðun, prenta eða senda skýrslu. Á beiðnisíðunni skal velja  **Ítarlegt**, síðan stilla  **valkosti tungumáls**  og  **sniðsvæðis**  að vild.

Nánari upplýsingar um  **síðuna stillingar**  mínar má fara í  [Breyta grunnstillingum](ui-change-basic-settings.md#region).

## Ítarlegir valkostir

Reitirnir undir flýtiflipanum **Ítarlegt** setja takmarkanir á útbúna skýrslu til að stjórna tilföngum prentarans. Yfirleitt þarf ekki að breyta þessum stillingum nema um stóra skýrslu sé að ræða. Ef skýrsla fer umfram þessar takmarkanir þegar reynt er að forskoða eða prenta birtast skilaboð sem segja til um hvaða takmörkun var farið yfir. Síðan er hægt að breyta stillingunum svo þær henti skýrslunni betur. Hver reitur er hinsvegar með hámarksgildi sem hafa ætti í huga:

|Svæði|Hámarksgildi|
|-----|-------------|
|Hámarksmyndunartími|12:00:00|
|Hámarksfjöldi lína|1000000|
|Hámarksfjöldi skjala|500|

> [!NOTE]
> Hámarksgildin kunna að vera mismunandi fyrir [!INCLUDE[prod_short](includes/prod_short.md)] á staðnum og stjórnandi getur breytt þeim. Frekari upplýsingar er að finna í hlutanum [Grunnstilling Business Central Server - Skýrslur](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports). Fyrir yfirlit yfir skýrslutakmarkanir í [!INCLUDE[prod_short](includes/prod_short.md)] á netinu skal skoða [Rekstrarlegar takmarkanir](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## Sjá tengda [Microsoft þjálfun](/training/paths/setup-reporting-dynamics-365-business-central/).

## Sjá einnig .

[Tiltækar skýrslur í [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Nota skýrslur í daglegu starfi](reports-use-reports.md)  
[Viðskiptagreind og skýrsluyfirlit](reports-bi-reporting.md)  
[Setja upp prentara](ui-specify-printer-selection-reports.md)  
[Keyra runuvinnslur og XMLports](ui-how-run-batch-jobs.md)  
[Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md)  
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Viðskiptagreind fjármála](bi.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
