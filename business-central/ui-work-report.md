---
title: Tímasetja skýrslu þannig að hún keyri á tilteknum degi og tíma | Microsoft Docs
description: Kynntu þér hvernig skal setja skýrslu inn í verkröð og tímasetja hana þannig að hún sé unnin á tilteknum degi og tíma.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 7fe5d0870cfc18ab103dc57044fd0ba84b151662
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392445"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Unnið með skýrslur, runuvinnslur og XMLports

Skýrsla safnar saman upplýsingum byggðum á sérstöku viðmiðssafni, og flokkar og birtir upplýsingarnar á sniði sem er auðvelt að lesa og sem hægt er að prenta eða vista sem skrá. Til eru margar skýrslur sem má finna víðsvegar í forritinu. Skýrslurnar veita alla jafna upplýsingar sem tengjast samhengi síðunnar sem þú ert á. Til dæmis, síðan **Viðskiptamaður** inniheldur skýrslur fyrir efstu 10 viðskiptamennina, sölutölur og fleira.

Runuvinnslur og XMLports gera meira eða minna það sama og skýrslur, en í þeim tilgangi að framkvæma ferli eða flytja út gögn. Til dæmis býr runuvinnslan **Stofna innheimtubréf** til áminningarskjöl fyrir viðskiptavini með gjaldfallnar greiðslur.  

> [!NOTE]
> Þetta efnisatriði vísar aðallega í „skýrsla“, en svipaðar upplýsingar gilda um runuvinnslur og XMLport.

## <a name="getting-started"></a>Hafist handa

Þú finnur skýrslurnar á flipanum **Skýrslur** á völdum síðum, eða þú getur notað ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") til að finna skýrslur eftir heiti.

Þegar þú opnar skýrslu, runuvinnslu eða XMLport birtist þér yfirleitt beiðnisíða þar sem þú tilgreinir ýmsa valmöguleika og síur sem ákvarða hvað skal hafa með í skýrslunni. Eftirfarandi hlutar útskýra hvernig á að nota beiðnisíðuna til að búa til, forskoða og prenta út skýrslur.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Sjálfgefin gildi notuð - fyrirframskilgreindar stillingar 

Flestar beiðnisíður innihalda reitinn **Nota sjálfgildi úr**. Þessi reitur gerir þér kleift að velja fyrirframskilgreindar stillingar fyrir skýrsluna sem sjálfkrafa stilla valkosti og síur fyrir skýrsluna. Veljið færslu úr fellilistanum og þar koma þá í ljós breytingarnar á valkostum og síum beiðnisíðunnar.

Færslan sem kallast **Valkostir og síur síðast notað** er alltaf í boði. Þessi færsla stillir skýrsluna á að nota valkosti og síur sem voru síðast notuð þegar skýrslan var keyrð.

Reiturinn **Nota sjálfgildi úr** veitir fljótlega og áreiðanlega leið til að búa til skýrslur sem innihalda réttar upplýsingar. Þegar færsla er valin, er hægt að breyta öllum valkostum og síum áður skýrslan er forskoðuð eða prentuð. Breytingarnar sem þú gerir verða ekki forskilgreindar í færslu fyrir vistaðar stillingar sem þú velur en þær verða vistaðar í færslunni **Síðast notaðir valkostir og afmarkanir**.

>[!NOTE]
> Fyrirframskilgreindar stillingar eru yfirleitt settar upp og stjórnað af stjórnanda. Til að fá nánari upplýsingar er hægt að skoða [Stjórna vistuðum stillingum fyrir skýrslur og runuvinnslur](reports-saving-reusing-settings.md).
<!--
Depending on the report, the request page might include the **Use default values from** field. This field lets you select a predefined set of can include the **Saved Settings** section that contains one or more entries in the **Use default value from** box. A saved setting is basically a predefined group of options and filters that you can apply to the report before previewing or sending the report to a file. The saved settings entry called **Last used options and filters** is always available. This entry sets the report to use options and filters that were used the last time you used the report.

Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data. After you set the **Use default value from** box to a saved settings entry, you can change any of the options and filters before previewing or saving the report. The changes that you make will not be saved to the saved settings entry you selected, but they will be saved to the **Last used options and filters** entry.

>[!NOTE]
>If you are an administrator, you can create and manage the saved settings for reports for all users. For more information, see [Manage Saved Settings for Reports and Batch Jobs](reports-saving-reusing-settings.md).
-->
## <a name="specifying-the-data-to-include-in-reports"></a>Tilgreina gögnin sem eiga að vera í skýrslunum

Notið reitina undir **Valkostir** og **Síur** til að breyta takmörkunum á upplýsingum sem eiga að koma fram í skýrslunni. Síur eru stilltar í skýrslu nánast á sama hátt og þær eru stilltar í listum. Frekari upplýsingar er að finna í [Síun](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Hlutinn **Sía lista eftir** á beiðnisíðu veitir almennan síumöguleika fyrir skýrslur. Þessar síur eru valfrjálsar.
>
> Einhverjar skýrslur hunsa slíkar síur, sem þýðir að sama hvaða sía er stillt í hlutanum **Sía lista eftir** verður útkoma skýrslunnar sú sama. Ekki er hægt að gefa upp lista yfir hvaða reitir eru hunsaðir í hvaða skýrslum, þannig að þú verður að gera tilraunir með síurnar þegar þú notar þær.
>
> **Dæmi**: Þegar þú notar runuvinnsluna **Sent innheimtubréf** verður sía fyrir reitinn **Færslur í viðskiptamannabók** í **Stig síðasta útgefins innheimtubréfs** hunsuð vegna þess að síurnar eru fastar fyrir þessa runuvinnslu.

## <a name="previewing-a-report"></a>Forskoðun skýrslu

Að forskoða skýrsluna gerir notanda kleift að sjá hvernig skýrslan komi til með að líta út áður en hún er prentuð. Forskoðunin sýnir skýrsluna samkvæmt [prentaranum](#Printer) sem sést í reitnum **Prentari** á beiðnisíðunni. Að forskoðun lokinni er hægt að fara aftur á beiðnisíðuna og gera breytingar á valkostum og síum eftir þörfum.

Til að forskoða skýrslu skal velja hnappinn **Forskoða** eða **Forskoða og loka** á beiðnisíðu skýrslunnar. Hnappurinn sem birtist fer eftir skýrslunni, þannig að sumar skýrslur eru með hnappinn **Forskoða** á meðan aðrar eru með hnappinn **Forskoða og loka**. Báðir hnapparnir opna forskoðun á skýrslunni. Munurinn liggur í því að **Forskoðun** heldur beiðnisíðunni opinni, þannig að hægt er að fara aftur í hana, gera breytingar, forskoða aftur eða prenta. Með **Forskoða og loka** lokast beiðnisíðan, þannig að opna þarf skýrsluna aftur til að gera breytingar eða prenta.

> [!NOTE]
> Ef verið er að nota Business Central 2020 útgáfutímabil 1 eða eldra, er aðeins hnappurinn **Forskoða**, sem lokar beiðnisíðunni við forskoðun eins og lýst er fyrir **Forskoðun og loka**.

### <a name="working-with-the-preview"></a>Vinna með forskoðun

Í forskoðun skal nota valmyndastikuna í forskoðun skýrslunnar til að:

- Fara gegnum síður
- Auka aðdrátt og minnka
- Breyta stærð svo passi á síðu
- Velja texta

    Þú getur afritað texta úr skýrslu og svo límt hann eitthvert annað, eins og á síðu í [!INCLUDE[prod_short](includes/prod_short.md)] eða Microsoft Word.  Ef þú notar mús, til dæmis, þá þrýstirðu niður og heldur þar sem þú vilt byrja, og færir svo músina til að velja eitt eða fleiri orð, setningar eða málsgreinar. Smellið á hægri músarhnappinn og veljið **Afrita**. Límið síðan valinn texta þar sem hann á að vera.
- Fletta skjali

    Hægt er að færa sjáanlega svæðið af skýrslunni í allar átti svo þú getir skoðað önnur svæði skýrslunnar. Fletting er gagnleg þegar eitthvað hefur verið stækkað til að sjá smáatriði.  Ef þú notar músina, til dæmis, þrýstirðu niður og heldur inni hnappinum hvar sem er á forskoðun skýrslunnar og svo hreyfirðu músina.

- Hlaða niður PDF-skrá á tölvuna eða netið.
- Prenta

## <a name="saving-a-report"></a>Vistar skýrslu

Þú getur vistað skýrsluna á PDF-sniði, Microsoft Word-skjali eða Microsoft Excel-skjali með því að velja hnappinn **Senda til** og svo framkvæma þitt val.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Tímasetja keyrslu skýrslu

Hægt er að tímasetja eða runuvinna skýrslu þannig að hún keyri á tilteknum degi og tíma. Tímasettar skýrslur og runuvinnslur eru færðar inn í verkröð og unnar á áætluðum tíma, eins og önnur verk. Veldu valkostinn **Áætlun** eftir að hafa valið **Senda til** og færðu svo inn upplýsingar á borð við prentara, og tíma og dagsetningu. Skýrslunni er síðan bætt við verkröðina og hún verður keyrð á tilgreindum tíma. Þegar skýrslan hefur verið meðhöndluð er varan fjarlægð úr verkröðinni. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).  

Þegar keyrsla skýrslu er áætluð er hægt að tilgreina að keyra þurfi alla fimmtudaga með því að stilla reitinn **Reikniregla næstu keyrsludagsetningar** á t.d. *D4*. Frekari upplýsingar er að finna í [Að nota dagsetningarreiknireglur](ui-enter-date-ranges.md#using-date-formulas).  

Hægt er að velja að vista skýrsluna í skrá, t.d. Excel, Word, eða PDF, prenta hana á völdum prentara, eða aðeins búa til skýrsluna. Ef þú velur að vista skýrsluna í skrá þá er meðhöndlaða skýrslan send á svæðið **Skýrsluinnhólf** á Mitt hlutverk þar sem þú getur skoðað hana.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Prenta skýrslu

Til að prenta skýrslu skal velja hnappinn **Prenta** á beiðnisíðunni eða valmyndastikunni á síðunni **Forskoða**.

<!--
### Printer selection

The report prints to the printer shown in the **Selected printer** field on the report request page. You can't change the printer from this page.

The selected printer is either set on the **Printer Selections** page or it's the default printer set up on the **Printer Management** page. If you want to use another printer, see  [Set Up Printers](ui-specify-printer-selection-reports.md).

If no printer is specified on the **Printer Selections** page or set as default on the **Printer Management** page, the browser printing feature is used. In this case, **Browser** appears in the **Selected printer** field on the report request page.
-->
### <a name="printer"></a><a name="Printer"></a>Prentari

Reiturinn **Prentari** á beiðnisíðunni sýnir heiti prentarans sem skýrslan verður send til. **(Meðhöndlað af vafra)** gefur til kynna að enginn prentari er valinn fyrir skýrsluna. Í slíku tilfelli sér vafrinn um útprentun og sýnir hefðbundið viðmót þar sem hægt er velja staðbundinn prentara sem tengdur er við tækið þitt.

Ekki er hægt að breyta prentaranum með reitnum **Prentari**. Til að breyta prentaranum þarf að fara á síðurnar **Prentaraval** eða **Prentarastjórnun**. Að stilla prentarann er yfirleitt verk sem stjórnandi sér um. Frekari upplýsingar má finna í [Setja upp prentara](ui-specify-printer-selection-reports.md).

<!--
### Browser printing

Because [!INCLUDE[prod_short](includes/prod_short.md)] is a cloud service, it can't reach local printers connected to your computer. However, it can connect to cloud-enabled printers. In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a cloud printer named **Email Printer** is installed as an extension and is ready to use after initial setup.

If a cloud printer is not installed and set up, or if an installed printer fails, then printing will default to the printing options for the browser.

> [!NOTE]
> The browser printing options work independently of [!INCLUDE[prod_short](includes/prod_short.md)]. So any printer settings that might have been set up from printers in [!INCLUDE[prod_short](includes/prod_short.md)] aren't carried over to the browser print options.

<!-- 
On the **Printer Management** page, you can see the printers that are set up. For more information, see [Set Up Printers](ui-specify-printer-selection-reports.md).

> [!NOTE]
> You can't change the **Printer** field on the report request page. To use another printer, you must select it from the **Printer Management** page.
-->
### <a name="printing-reports-in-thai"></a>Prenta skýrslur á taílensku

Sérstaklega fyrir taílensku útgáfuna af [!INCLUDE[prod_short](includes/prod_short.md)], getur hnappurinn **Prenta** ekki prentað skýrslur rétt vegna takmarkana á þjónustunni sem býr til prentanlegt PDF-skjal. Í staðinn getur þú opnað skýrsluna í Word og síðan vistað hana sem prentvæna PDF-skrá.  

Að öðrum kosti geturðu beðið stjórnanda þinn um að búa til Word-skýrsluútlit fyrir mest notuðu skýrslurnar. Frekari upplýsingar, sjá [Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Breyting skýrsluútlita

Útlit skýrslu stjórnar því hvað er birt í skýrslu, hvernig því er stillt upp og það stílfært. Ef þú vilt skipta yfir í annað útlit skaltu skoða [Breyta núverandi skýrsluútliti](ui-how-change-layout-currently-used-report.md). Eða, ef þú vilt sérsníða þitt eigið skýrsluútlit, sjá [Búa til og breyta sérsniðnu skýrsluútliti](ui-how-create-custom-report-layout.md).

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