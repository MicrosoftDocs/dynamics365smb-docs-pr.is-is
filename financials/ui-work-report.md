---
title: "Tímasetja skýrslu þannig að hún keyri á tilteknum degi og tíma | Microsoft Docs"
description: "Kynntu þér hvernig skal setja skýrslu inn í verkröð og tímasetja hana þannig að hún sé unnin á tilteknum degi og tíma."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 07/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: badcdee3dfa5bec3c2462149989cf9d4fb5af2a0
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="working-with-reports"></a>Unnið með Skýrslur
Skýrsla safnar saman upplýsingum byggðum á sérstöku viðmiðssafni, og flokkar og birtir upplýsingarnar á sniði sem hægt er að prenta og er auðvelt að lesa. Til eru margar skýrslur sem má finna víðsvegar í forritinu. Skýrslurnar veita alla jafna upplýsingar sem tengjast samhengi síðunnar sem þú ert á. Til dæmis, síðan **Viðskiptamaður** inniheldur skýrslur fyrir efstu 10 viðskiptamennina og söluupplýsingar og fleira.

Þú getur fundið skýrslurnar á flipanum **Skýrslur** á völdum síðum, eða þú getur leitað að skýrslum eftir nafni. Þegar þú opnar skýrslu, birtist þér síða sem leyfir þér að tilgreina upplýsingar (valmöguleikar og afmarkanir) sem ákvarða hvað skal hafa með í skýrslunni. Til dæmis, háð skýrslunni, geturðu tilgreint tímabil út frá dagsetningum, sérstaka skrá eins og t.d. viðskiptamaður, eða raða pöntunum.

## <a name="previewing-a-report"></a>Forskoða skýrslu
Velja **Forskoðun** til að skoða skýrsluna í netvafranum. Benda á svæði í skýrslunni til að sýna valmyndin.  

![Valmynd forskoðun skýrsla](media/report_viewer.png "Report preview toolbar")

Nota valmyndarslá til að:

-   Fara gegnum síður
-   Auka aðdrátt og minnka
-   Breyta stærð svo passi í glugga
-   Velja texta

    Þú getur afritað texta úr skýrslu og svo límt hann eitthvert annað, eins og á síðu í [!INCLUDE[d365fin](includes/d365fin_md.md)] eða Microsoft Word.  Ef þú notar mús, til dæmis, þá þrýstirðu niður og heldur þar sem þú vilt byrja, og færir svo músina til að velja eitt eða fleiri orð, setningar eða málsgreinar. Þú getur síðan hægrismellt og valið **Afrita**. Hægt er að líma valinn textann hvar sem er.
-   Fletta skjali

    Hægt er að færa sjáanlega svæðið af skýrslunni í allar átti svo þú getir skoðað önnur svæði skýrslunnar. Þetta er nytsamlegt þegar þú eykur aðdrátt til að sjá upplýsingar.  Ef þú notar músina, til dæmis, þrýstirðu niður og heldur inni hnappinum hvar sem er á forskoðun skýrslunnar og svo hreyfirðu músina.

-   Hlaða niður PDF-skrá á tölvuna eða netið.


## <a name="saving-a-report"></a>Vistar skýrslu
Þú getur vistað skýrsluna á PDF-sniði, Microsoft Word skjali eða Microsoft Excel skjali með því að velja **Senda til**, og svo framkvæma þitt val. 

## <a name="ScheduleReport"></a> Tímasetja keyrslu skýrslu
Hægt er að tímasetja skýrslu þannig að hún keyri á tilteknum degi og tíma. Tímasettar skýrslur eru færðar inn í verkröð og unnar á settum tíma, eins og önnur verk. Hægt er að velja að vista meðhöndlaða skýrslu í skrá, t.d. Excel, Word, eða PDF, prenta hana á völdum prentara, eða meðhöndla aðeins skýrsluna. Ef þú velur að vista skýrsluna í skrá þá er meðhöndlaða skýrslan send á svæðið **Skýrsluinnhólf** á heimasíðu þinni þar sem þú getur skoðað hana.

Hægt er að tímasetja skýrslu þegar skýrsla er opnuð. Valkosturinn **Áætlun** er valinn og síðan eru upplýsingar á borð við prentara, og tíma og dagsetningu færðar inn. Skýrslunni er síðan bætt við verkröðina og hún verður keyrð á tilgreindum tíma. Þegar skýrslan hefur verið meðhöndluð er varan fjarlægð úr verkröðinni. Ef þú vistaðir meðhöndlaða skýrsluna í skrá er hún aðgengileg á svæðinu **Skýrsluinnhólf**.

## <a name="PrintReport"></a>Prenta skýrslu
Þegar þú vilt prenta skýrslu þarf að hlaða niður skýrslunni sem PDF, Word eða Excel skjali fyrst með því að velja **Senda til**. Nú er hægt að opna PDF-skjalið strax og prenta það, eða vista það og prentað það síðar.

## <a name="using-saved-settings"></a>Nota vistaðar stillingar
Skýrsla getur innihaldið eitt eða fleiri færslur í **vistaðar stillingar** boxinu. *Vistaðar stillingar* eru í raun fyrirframskilgreindur flokkur valmöguleika og afmarkanna sem þú getur notað í skýrslunni áður en þú forskoðar og sendir hana til skráar. Með því að nota vistaðar stillingar er er fljótleg og reliable leið til að haldbærar búa til skýrslur sem eru rétt gögn.

Vistaða stillingafærslan sem kallast **Síðast notaðir valkostir og afmarkanir** er alltaf tiltæk. Þessi færsla stillir skýrsluna til að nota valmöguleika og afmarkanir sem voru notaðar síðast þegar þú kíktir á skýrsluna.

>[!NOTE]
>Sem stjórnandi geturðu stofna og breyta vistuðum stillingum fyrir skýrslur fyrir alla notendur. Frekari upplýsingar, sjá [Stjórna vistaðar stillingar á skýrslum](reports-saving-reusing-settings.md).

## <a name="changing-the-layout-and-look-of-a-report"></a>Breyta útliti og ásýnd skýrslu
Útlit skýrslu stjórnar því hvað er birt í skýrslu, hvernig því er stillt upp og það stílfært. Ef þú vilt skipta yfir í annað útlit, sjá [Hvernig á að: Breyta hvaða útlit er nú notað í skýrslu](ui-how-change-layout-currently-used-report.md) Eða, ef þú vilt sérsníða þitt eigið skýrsluútlit, sjá [Hvernig á að: Búa til og breyta sérsniðið skýrsluútlit](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Sjá einnig
[Tilgreina prentaraval fyrir skýrslur](ui-specify-printer-selection-reports.md)  
[Stjórna útliti skýrslna og skjala](ui-manage-report-layouts.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

