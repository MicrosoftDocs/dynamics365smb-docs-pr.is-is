---
title: Tímasetja skýrslu þannig að hún keyri á tilteknum degi og tíma | Microsoft Docs
description: Kynntu þér hvernig skal setja skýrslu inn í verkröð og tímasetja hana þannig að hún sé unnin á tilteknum degi og tíma.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 06/10/2020
ms.author: edupont
ms.openlocfilehash: f209088459f29ba5618b065c3a340b0e3bd250e5
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788397"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Unnið með skýrslur, runuvinnslur og XMLports

Skýrsla safnar saman upplýsingum byggðum á sérstöku viðmiðssafni, og flokkar og birtir upplýsingarnar á sniði sem er auðvelt að lesa og sem hægt er að prenta eða vista sem skrá. Til eru margar skýrslur sem má finna víðsvegar í forritinu. Skýrslurnar veita alla jafna upplýsingar sem tengjast samhengi síðunnar sem þú ert á. Til dæmis, síðan **Viðskiptamaður** inniheldur skýrslur fyrir efstu 10 viðskiptamennina, sölutölur og fleira.

Runuvinnslur og XMLports gera meira eða minna það sama og skýrslur, en í þeim tilgangi að framkvæma ferli eða flytja út gögn. Til dæmis býr runuvinnslan **Stofna innheimtubréf** til áminningarskjöl fyrir viðskiptavini með gjaldfallnar greiðslur.  

> [!NOTE]
> Þetta efnisatriði vísar aðallega í „skýrsla“, en svipaðar upplýsingar gilda um runuvinnslur og XMLport.

Þú getur fundið skýrslurnar á flipanum **Skýrslur** á völdum síðum, eða þú getur notað ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") til að finna skýrslur eftir heiti.

## <a name="specifying-the-data-to-include-in-reports"></a>Tilgreina gögnin sem eiga að vera í skýrslunum
Þegar þú opnar skýrslu, runuvinnslu eða XMLport birtist þér yfirleitt beiðnisíða þar sem þú tilgreinir ýmsa valmöguleika og síur sem ákvarða hvað skal hafa með í skýrslunni.

Síur eru stilltar í skýrslu nánast á sama hátt og þær eru stilltar í listum. Frekari upplýsingar er að finna í [Síun](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Hlutinn **Sía lista eftir** á beiðnisíðu veitir almennan síumöguleika fyrir skýrslur. Þessar síur eru valfrjálsar.
>
> Einhverjar skýrslur hunsa slíkar síur, sem þýðir að sama hvaða sía er stillt í hlutanum **Sía lista eftir** verður útkoma skýrslunnar sú sama. Ekki er hægt að gefa upp lista yfir hvaða reitir eru hunsaðir í hvaða skýrslum, þannig að þú verður að gera tilraunir með síurnar þegar þú notar þær.
>
> **Dæmi**: Þegar þú notar runuvinnsluna **Sent innheimtubréf** verður sía fyrir reitinn **Færslur í viðskiptamannabók** í **Stig síðasta útgefins innheimtubréfs** hunsuð vegna þess að síurnar eru fastar fyrir þessa runuvinnslu.

## <a name="using-saved-settings"></a><a name="SavedSettings"></a>Nota vistaðar stillingar
Beiðnisíða getur innihaldið hlutann **Vistaðar stillingar** sem inniheldur eina eða fleiri færslur í kassanum **Nota sjálfgefið gildi frá**. Vistaðar stillingar eru í raun fyrirframskilgreindur flokkur valmöguleika og afmarkanna sem þú getur notað í skýrslunni áður en þú forskoðar og sendir hana til skráar. Vistaða stillingafærslan sem kallast **Síðast notaðir valkostir og afmarkanir** er alltaf tiltæk. Þessi færsla stillir skýrsluna til að nota valmöguleika og síur sem voru notuð síðast þegar þú notaðir skýrsluna.

Notkun vistaðra stillinga er fljótleg og áreiðanleg leið til að búa til skýrslur sem innihalda rétt gögn. Eftir að þú velur **Nota sjálfgefið gildi frá** reitinn við færslu fyrir vistaðar stillingar geturðu breytt öllum valkostum og afmörkunum áður en skýrslan er forskoðuð eða vistuð. Breytingarnar sem þú gerir verða ekki vistaðar í færslu fyrir vistaðar stillingar sem þú velur en þær verða vistaðar í færslunni **Síðast notaðir valkostir og afmarkanir**.

>[!NOTE]
>Ef þú ert stjórnandi geturðu stofna og breyta vistuðum stillingum fyrir skýrslur fyrir alla notendur. Frekari upplýsingar er að finna í [Stjórna vistuðum stillingum fyrir skýrslur og runuvinnslur](reports-saving-reusing-settings.md).

## <a name="previewing-a-report"></a>Forskoðun skýrslu

Veljið hnappinn **Forskoða** til að skoða skýrsluna á síðu skýrslubeiðni. Notaðu valmyndastikuna í skýrsluforskoðun til að:

- Fara gegnum síður
- Auka aðdrátt og minnka
- Breyta stærð svo passi á síðu
- Velja texta

    Þú getur afritað texta úr skýrslu og svo límt hann eitthvert annað, eins og á síðu í [!INCLUDE[d365fin](includes/d365fin_md.md)] eða Microsoft Word.  Ef þú notar mús, til dæmis, þá þrýstirðu niður og heldur þar sem þú vilt byrja, og færir svo músina til að velja eitt eða fleiri orð, setningar eða málsgreinar. Þú getur síðan hægrismellt með músarhnappinum og valið **Afrita**. Síðan geturðu límt valinn texta þar sem þú vilt hafa hann.
- Fletta skjali

    Hægt er að færa sjáanlega svæðið af skýrslunni í allar átti svo þú getir skoðað önnur svæði skýrslunnar. Þetta er nytsamlegt þegar þú eykur aðdrátt til að sjá upplýsingar.  Ef þú notar músina, til dæmis, þrýstirðu niður og heldur inni hnappinum hvar sem er á forskoðun skýrslunnar og svo hreyfirðu músina.

- Hlaða niður PDF-skrá á tölvuna eða netið.
- Prenta

## <a name="saving-a-report"></a>Vistar skýrslu
Þú getur vistað skýrsluna á PDF-sniði, Microsoft Word-skjali eða Microsoft Excel-skjali með því að velja hnappinn **Senda til** og svo framkvæma þitt val.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a> Tímasetja keyrslu skýrslu

Hægt er að tímasetja eða runuvinna skýrslu þannig að hún keyri á tilteknum degi og tíma. Tímasettar skýrslur og runuvinnslur eru færðar inn í verkröð og unnar á áætluðum tíma, eins og önnur verk. Veldu valkostinn **Áætlun** eftir að hafa valið **Senda til** og færðu svo inn upplýsingar á borð við prentara, og tíma og dagsetningu. Skýrslunni er síðan bætt við verkröðina og hún verður keyrð á tilgreindum tíma. Þegar skýrslan hefur verið meðhöndluð er varan fjarlægð úr verkröðinni. Frekari upplýsingar, sjá [Nota verkraðir til að tímaraða verkhlutum](admin-job-queues-schedule-tasks.md).  

Þegar keyrsla skýrslu er áætluð er hægt að tilgreina að keyra þurfi alla fimmtudaga með því að stilla reitinn **Reikniregla næstu keyrsludagsetningar** á t.d. *D4*. Frekari upplýsingar er að finna í [Að nota dagsetningarreiknireglur](ui-enter-date-ranges.md#using-date-formulas).  

Hægt er að velja að vista meðhöndlaða skýrslu í skrá, t.d. Excel, Word, eða PDF, prenta hana á völdum prentara, eða meðhöndla aðeins skýrsluna. Ef þú velur að vista skýrsluna í skrá þá er meðhöndlaða skýrslan send á svæðið **Skýrsluinnhólf** á Mitt hlutverk þar sem þú getur skoðað hana.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Prenta skýrslu

Prentuð er skýrsla með því að velja hnappinn **Prenta** á síðu skýrslubeiðni eða í valmyndastiku á síðunni **Forskoðun**.

### <a name="printer-selection"></a>Val á prentara

Skýrslan prentast á prentaranum sem sýndur er í reitnum **Valinn prentari** á síðu skýrslubeiðni. Ekki er hægt að breyta prentaranum á þessari síðu.

Valinn prentari er annaðhvort stilltur á síðunni **Prentaraval** eða sjálfgefni prentarinn sem settur er upp á síðunni **Prentarastjórnun**. Ef ætlunin er að nota annan prentara skal skoða [Setja upp prentara](ui-specify-printer-selection-reports.md).

Ef enginn prentari er tilgreindur á síðunni **Prentaraval** eða stilltur sem sjálfgefinn á síðunni **Prentarastjórnun** er prenteiginleiki vafrans notaður. Í slíku tilfelli birtist **Vafrinn** í reitnum **Valinn prentari** á síðu skýrslubeiðni. 

### <a name="browser-printing"></a>Prentun í vafra

Vegna þess að [!INCLUDE[prodshort](includes/prodshort.md)] er skýjaþjónusta nær hún ekki til staðbundinna prentara sem eru tengdir tölvum notanda. Hins vegar er hægt að tengjast skýjavirkum prenturum. Í almennri útgáfu af [!INCLUDE[prodshort](includes/prodshort.md)] er skýjaprentari með heitið **Tölvupóstsprentari** uppsettur sem viðbót og er tilbúinn til notkunar eftir upphaflega uppsetningu.

Ef skýjaprentari er ekki uppsettur, eða ef uppsettur prentari mistekst, er prentun valin sjálfkrafa fyrir prentvalkosti vafrans.

> [!NOTE]
> Prentmöguleikar vafrans vinna óháð [!INCLUDE[prodshort](includes/prodshort.md)]. Allar prentarastillingar sem kunna að hafa verið settar upp úr prenturum í [!INCLUDE[prodshort](includes/prodshort.md)] flytjast ekki yfir í prentmöguleika vafrans.

<!-- 
On the **Printer Management** page, you can see the printers that are set up. For more information, see [Set Up Printers](ui-specify-printer-selection-reports.md).

> [!NOTE]
> You can't change the **Printer** field on the report request page. To use another printer, you must select it from the **Printer Management** page.
-->
### <a name="printing-reports-in-thai"></a>Prenta skýrslur á taílensku
Sérstaklega fyrir taílensku útgáfuna af [!INCLUDE[prodshort](includes/prodshort.md)], getur hnappurinn **Prenta** ekki prentað skýrslur rétt vegna takmarkana á þjónustunni sem býr til prentanlegt PDF-skjal. Í staðinn getur þú opnað skýrsluna í Word og síðan vistað hana sem prentvæna PDF-skrá.  

Að öðrum kosti geturðu beðið stjórnanda þinn um að búa til Word-skýrsluútlit fyrir mest notuðu skýrslurnar. Frekari upplýsingar, sjá [Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Breyting skýrsluútlita
Útlit skýrslu stjórnar því hvað er birt í skýrslu, hvernig því er stillt upp og það stílfært. Ef þú vilt skipta yfir í annað útlit skaltu skoða [Breyta núverandi skýrsluútliti](ui-how-change-layout-currently-used-report.md). Eða, ef þú vilt sérsníða þitt eigið skýrsluútlit, sjá [Búa til og breyta sérsniðnu skýrsluútliti](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Sjá einnig

[Setja upp prentara](ui-specify-printer-selection-reports.md)  
[Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md)  
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
