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
ms.author: sgroespe
ms.openlocfilehash: 19811dadb284ee9e629c9dc518df5cb989175fdb
ms.sourcegitcommit: 0b5f8f68b1c9526288bfcce1a3bdc988d2910040
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454330"
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

Veljið hnappinn **Forskoða** til að skoða skýrslugerðina í. Notaðu valmyndastikuna í skýrsluforskoðun til að:

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
Hægt er að prenta skýrslu með því að velja hnappinn **Prenta** á síðu skýrslubeiðni eða í valmyndastiku á síðunni **Forskoðun**.

Vegna þess að [!INCLUDE[prodshort](includes/prodshort.md)] er skýjaþjónusta nær hún ekki til staðbundinna prentara sem eru tengdir vélum notanda. Hins vegar er hægt að tengjast skýjavirkum prenturum. Í almennri útgáfu af [!INCLUDE[prodshort](includes/prodshort.md)] er skýjaprentari með heitið **Tölvupóstsprentari** uppsettur sem viðbót og er tilbúinn til notkunar eftir upphaflega uppsetningu.

Ef skýjaprentari er ekki uppsettur, eða ef uppsettur prentari mistekst, er prentun valin sjálfkrafa fyrir prentvalkosti vafrans. Þetta er gefið í skyn með þessu gildi í reitnum **Prentari** á síðu skýrslubeiðna: *(ekkert, vafrinn sér um þetta)*.

Á síðunni **Prentarastjórnun** er hægt að skoða uppsetta prentara. Frekari upplýsingar eru í [Setja upp prentara](ui-specify-printer-selection-reports.md).

> [!NOTE]
> Ekki er hægt að breyta reitnum **Prentari** á síðu skýrslubeiðni. Til að nota annan prentara verður að velja hann af síðunni **Prentarastjórnun**.

### <a name="printing-reports-in-thai"></a>Prenta skýrslur á taílensku
Sérstaklega fyrir taílensku útgáfuna af [!INCLUDE[prodshort](includes/prodshort.md)], hnappurinn **Prenta** getur ekki prentað skýrslur rétt vegna takmarkana á þjónustu sem býr til prentvænu PDF-skrána. Í staðinn getur þú opnað skýrsluna í Word og síðan vistað hana sem prentvæna PDF-skrá.  

Að öðrum kosti geturðu beðið stjórnanda þinn um að búa til Word-skýrsluútlit fyrir mest notuðu skýrslurnar. Frekari upplýsingar, sjá [Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Breyting skýrsluútlita
Útlit skýrslu stjórnar því hvað er birt í skýrslu, hvernig því er stillt upp og það stílfært. Ef þú vilt skipta yfir í annað útlit skaltu skoða [Breyta núverandi skýrsluútliti](ui-how-change-layout-currently-used-report.md). Eða, ef þú vilt sérsníða þitt eigið skýrsluútlit, sjá [Búa til og breyta sérsniðnu skýrsluútliti](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Sjá einnig

[Setja upp prentara](ui-specify-printer-selection-reports.md)  
[Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md)  
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
