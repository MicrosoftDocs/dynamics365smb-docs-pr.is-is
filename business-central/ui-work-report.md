---
title: Tímasetja skýrslu þannig að hún keyri á tilteknum degi og tíma | Microsoft Docs
description: Kynntu þér hvernig skal setja skýrslu inn í verkröð og tímasetja hana þannig að hún sé unnin á tilteknum degi og tíma.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: 98d51b10d3ca415a463b58405cb3c4f2449b75ad
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/19/2019
ms.locfileid: "852425"
---
# <a name="working-with-reports-and-batch-jobs"></a>Unnið með skýrslur og runuvinnslur
Skýrsla safnar saman upplýsingum byggðum á sérstöku viðmiðssafni, og flokkar og birtir upplýsingarnar á sniði sem hægt er að prenta og er auðvelt að lesa. Til eru margar skýrslur sem má finna víðsvegar í forritinu. Skýrslurnar veita alla jafna upplýsingar sem tengjast samhengi síðunnar sem þú ert á. Til dæmis, síðan **Viðskiptamaður** inniheldur skýrslur fyrir efstu 10 viðskiptamennina og söluupplýsingar og fleira.

Runuvinnslur gera meira og minna það sama og skýrslur en í þeim tilgangi að setja af stað ferli. Til dæmis býr runuvinnslan **Stofna innheimtubréf** til áminningarskjöl fyrir viðskiptavini með gjaldfallnar greiðslur.  

> [!NOTE]
> Þetta efnisatriði á að mestu leyti við um „skýrslu“, en svipaðar upplýsingar eiga við um runuvinnslur.

Þú getur fundið skýrslurnar á flipanum **Skýrslur** á völdum síðum, eða þú getur notað ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") til að finna skýrslur eftir heiti.


## <a name="specifying-the-data-to-include-in-the-report"></a>Tilgreina gögnin sem eiga að vera í skýrslunni
Þegar þú opnar skýrslu, birtist þér yfirleitt síða þar sem þú tilgreinir ýmsa valmöguleikar og afmarkanir sem ákvarða hvað skal hafa með í skýrslunni. Þessi síða er kölluð beiðnisíða skýrslu. Til dæmis, beiðnisíða skýrslu leyfir þér að búa til skýrslu fyrir sérstakan viðskiptamann tiltekið dagabil eða flokka röð upplýsinga í skýrslunni. Eftirfarandi er dæmi um beiðnisíðu skýrslu:

![Valkostir fyrir skýrslu](media/report_options.png "Valkostir fyrir skýrslu")

> [!Caution]
> Hlutinn **Sýna niðurstöður** á beiðnisíðu býður upp á almenna síunarmöguleika fyrir skýrslur. Þessar síur eru valfrjálsar.<br /><br /> Sumar skýrslur munu hunsa allar slíkar síur, sem þýðir að sama hvaða sía er stillt í hlutanum **Sýna niðurstöður**, verður útkoman skýrslunnar sú sama. Ekki er hægt að gefa upp lista yfir hvaða reitir eru hunsaðir í hvaða skýrslum, þannig að þú verður að gera tilraunir með síurnar þegar þú notar þær.<br /><br />
**Dæmi**: Þegar þú notar runuvinnsluna **Sent innheimtubréf** verður sía fyrir reitinn **Færslur í viðskiptamannabók** í **Stig síðasta útgefins innheimtubréfs** hunsuð vegna þess að síurnar eru fastar fyrir þessa runuvinnslu.

### <a name="SavedSettings"></a>Nota vistaðar stillingar
Með sumum skýrslum, allt eftir því hvernig þær eru hannaðar, kann skýrslusíðan að fela í sér **Vistaðar stillingar** hluta sem inniheldur eina eða fleiri færslur í **Nota sjálfgefið gildi frá** reitnum. Færslurnar í þessum reit eru kölluð *vistaðar stillingar*. Vistaðar stillingar eru í raun fyrirframskilgreindur flokkur valmöguleika og afmarkanna sem þú getur notað í skýrslunni áður en þú forskoðar og sendir hana til skráar. Vistaða stillingafærslan sem kallast **Síðast notaðir valkostir og afmarkanir** er alltaf tiltæk. Þessi færsla stillir skýrsluna til að nota valmöguleika og afmarkanir sem voru notaðar síðast þegar þú kíktir á skýrsluna.

Notkun vistaðra stillinga er fljótleg og áreiðanleg leið til að búa til skýrslur sem innihalda rétt gögn. Eftir að þú velur **Nota sjálfgefið gildi frá** reitinn við færslu fyrir vistaðar stillingar geturðu breytt öllum valkostum og afmörkunum áður en skýrslan er forskoðuð eða vistuð. Breytingarnar sem þú gerir verða ekki vistaðar í færslu fyrir vistaðar stillingar sem þú velur en þær verða vistaðar í **Síðast notaðir valkostir og afmarkanir**.

>[!NOTE]
>Ef þú ert stjórnandi geturðu stofna og breyta vistuðum stillingum fyrir skýrslur fyrir alla notendur. Frekari upplýsingar, sjá [Stjórna vistaðar stillingar á skýrslum](reports-saving-reusing-settings.md).

### <a name="setting-options-and-filters"></a>Valkostir og afmarkanir stillt
Til að takmarka frekar hvaða gögn eru tekin með í skýrsluna má setja fleiri afmarkanir og valkosti.

Afmarkanir gefa þér sjágögn sem byggjast á tilgreint skilyrði. Afmarkanir eru hópaðar saman með einingunni sem þeir tilheyra, t.d. **Viðskiptamaður** í teikningunni að ofan. Þú skilgreinir afmörkun með því að stilla **Hvar** reitinn á svæði sem þú vilt nota afmörkun og bæta síðan skilyrði í **er:** reitinn. Til dæmis, á teikningunni að ofan er ein afmörkun sem býr til skýrslu fyrir viðskiptamann sem **Nr.** jafngildir **01121212**.

Þú getur bætt við fleiri afmörkunum með því að stilla **Bæta við** reitinn. Þegar þú ert með meira en eina afmörkun eru aðeins niðurstöður sem uppfylla skilyrði fyrir allar afmarkanir teknar með í skýrslunni.

Eftir því hvaða gerð reits er að afmarka getur þú tilgreint síuskilyrði til að leita að nákvæmri samsvörun, hluta samsvörun, gildissvið og fleira. Aðstoð um hvernig síur eru settir upp eru í:
-   [Afmörkun](ui-enter-criteria-filters.md#FilterCriteria)
-   [Unnið með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md)

## <a name="previewing-a-report"></a>Forskoðun skýrslu
Velja **Forskoðun** til að skoða skýrsluna í netvafranum. Benda á svæði í skýrslunni til að sýna valmyndin.  

![Forskoðunarstika skýrslu](media/report_viewer.png "Forskoðunarstika skýrslu")

Nota valmyndarslá til að:

-   Fara gegnum síður
-   Auka aðdrátt og minnka
-   Breyta stærð svo passi á síðu
-   Velja texta

    Þú getur afritað texta úr skýrslu og svo límt hann eitthvert annað, eins og á síðu í [!INCLUDE[d365fin](includes/d365fin_md.md)] eða Microsoft Word.  Ef þú notar mús, til dæmis, þá þrýstirðu niður og heldur þar sem þú vilt byrja, og færir svo músina til að velja eitt eða fleiri orð, setningar eða málsgreinar. Þú getur síðan hægrismellt og valið **Afrita**. Hægt er að líma valinn textann hvar sem er.
-   Fletta skjali

    Hægt er að færa sjáanlega svæðið af skýrslunni í allar átti svo þú getir skoðað önnur svæði skýrslunnar. Þetta er nytsamlegt þegar þú eykur aðdrátt til að sjá upplýsingar.  Ef þú notar músina, til dæmis, þrýstirðu niður og heldur inni hnappinum hvar sem er á forskoðun skýrslunnar og svo hreyfirðu músina.

-   Hlaða niður PDF-skrá á tölvuna eða netið.
-   Prenta


## <a name="saving-a-report"></a>Vistar skýrslu
Þú getur vistað skýrsluna sem PDF-skjal, Microsoft Word-skjal eða Microsoft Excel-skjal með því að velja **Senda til** og síðan velja.

## <a name="ScheduleReport"></a> Tímasetja keyrslu skýrslu
Hægt er að tímasetja skýrslu þannig að hún keyri á tilteknum degi og tíma. Tímasettar skýrslur eru færðar inn í verkröð og unnar á settum tíma, eins og önnur verk. Hægt er að velja að vista meðhöndlaða skýrslu í skrá, t.d. Excel, Word, eða PDF, prenta hana á völdum prentara, eða meðhöndla aðeins skýrsluna. Ef þú velur að vista skýrsluna í skrá þá er meðhöndlaða skýrslan send á svæðið **Skýrsluinnhólf** á Mitt hlutverk þar sem þú getur skoðað hana.

Hægt er að tímasetja skýrslu þegar skýrsla er opnuð. Valkosturinn **Áætlun** er valinn og síðan eru upplýsingar á borð við prentara, og tíma og dagsetningu færðar inn. Skýrslunni er síðan bætt við verkröðina og hún verður keyrð á tilgreindum tíma. Þegar skýrslan hefur verið meðhöndluð er varan fjarlægð úr verkröðinni. Ef þú vistaðir meðhöndlaða skýrsluna í skrá er hún aðgengileg á svæðinu **Skýrsluinnhólf**.

## <a name="PrintReport"></a>Prenta skýrslu
Hægt er að prenta skýrslu með hnappnum **Prenta** á valsíðunni sem birtist þegar skýrslan er opnuð eða úr valmyndastikunni í Forskoðun.

## <a name="changing-the-layout-and-look-of-a-report"></a>Breyta útliti og ásýnd skýrslu
Útlit skýrslu stjórnar því hvað er birt í skýrslu, hvernig því er stillt upp og það stílfært. Ef þú vilt skipta yfir í annað útlit, sjá [Breyta hvaða útlit er nú notað í skýrslu](ui-how-change-layout-currently-used-report.md). Eða, ef þú vilt sérsníða þitt eigið skýrsluútlit, sjá [Búa til og breyta sérsniðnu skýrsluútliti](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Sjá einnig
[Tilgreina prentaraval fyrir skýrslur](ui-specify-printer-selection-reports.md)  
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
