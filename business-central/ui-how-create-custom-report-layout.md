---
title: Stofna og breyta sérsniðnum útlitsstillingum fyrir skýrslur og skjöl
description: Kynntu þér hvernig skal stofna sérstillt útlit til að sérsníða útlit skýrslu þegar hún er skoðuð, prentuð eða vistuð.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d629b2639325b95ab90db8aaf8ac9a3e5d51fc33
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511442"
---
# <a name="legacy-create-and-modify-custom-report-layouts"></a>Arfur Stofna og breyta skipan sérsniðinnar skýrslu

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Sjálfgefið er að skýrsla hafa innbyggt skýrsluútlit, sem getur verið RDLC-skýrsluútlit, Word-skýrsluútlit eða bæði. Ekki er hægt að breyta innbyggðum útlitum. En þú getur búið til þín eigin sérsniðin útlit sem gerir þér kleift að breyta útliti skýrslu þegar hún er skoðuð, prentuð eða vistuð. Hægt er að búa til mörg sérsniðin skýrsluútlit fyrir sömu skýrsluna, og skipta svo á milli útlita fyrir skýrsluna eftir þörfum.

> [!NOTE]  
> Í [!INCLUDE[prod_short](includes/prod_short.md)] táknar hugtakið "skýrsla" einnig utanaðkomandi skjöl, s.s. sölureikninga og pöntunarstaðfestingar sem þú sendir til viðskiptavina sem PDF skjöl.

Til að búa til sérsniðið útlit geturðu búið til afrit af öðru sérsniðið útliti eða bætt við nýju sérsniðnu útliti, sem í flestum tilfellum er byggt á innbyggða útlitinu. Þegar þú bætir við nýju sérsniðnu útliti geturðu valið að bæta við RDLC-skýrsluútliti, Word-skýrsluútliti eða bæði. Nýja sérsniðna útlitið verður sjálfkrafa byggt á innbyggða útlitinu fyrir skýrsluna ef það er til staðar. Ef ekkert innbyggt útlit er til fyrir gerðina er nýtt autt útlit stofnað. Þú verður að breyta og hanna þetta auða útlit frá grunni. Frekari upplýsingar um RDLC- og Word-skýrsluútlit, innbyggð útlit, sérsniðið útlit og fleira eru í [stjórna skýrsluútliti](ui-manage-report-layouts.md).  

> [!TIP]
> Notaðu reikningsáætlanir til að fá innsýn í fjárhagsupplýsingar sem eru geymdar í bókhaldslyklum. Frekari upplýsingar er að finna í [Undirbúa Financial Reporting með fjárhagsskemu og lyklategundum](bi-how-work-account-schedule.md).

Þegar sérsniðið skýrsluútlit er skilgreint er hægt að velja það úr spjöldum viðskiptamanna og lánardrottna til að tilgreina að valið útlit á að nota fyrir skjöl sem þú býrð til fyrir viðskiptamanninn eða lánardrottin. Frekari upplýsingar eru í [Skilgreina útlit skjala fyrir viðskiptamenn og lánardrottna](ui-define-customer-vendor-document-layouts.md).

## <a name="to-create-a-custom-layout"></a>Til að búa til sérsniðið útlit

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Val á skýrsluútliti** og velja síðan viðkomandi tengil.

    Síðan **Val á útliti skýrslu** sýnir allar skýrslur sem eru í boði fyrir fyrirtæki sem er tiltekið í reitnum **Heiti fyrirtækis** efst á síðunni.
2. Stilltu reitinn **Fyrirtæki** á fyrirtækið sem búa á til skýrsluútliti fyrir.
3. Veldu röðina fyrir skýrsluna sem þú vilt stofna útlitið fyrir, og veldu svo **Sérsniðið útlit** aðgerðina.  

   Síðan **Sérsniðið skýrsluútlit** birtist og sýnir öll sérsniðin útlit sem eru í boði fyrir völdu skýrsluna.
4. Ef þú vilt búa til afrit af sérsniðnu útliti sem þegar er til velurðu sérsniðið útlitið af listanum og velur svo **Afrita** aðgerðina.  

   Afrit af sérsniðna útlitinu birtist á síðunni **Sérsniðið skýrsluútlit** með orðunum *Afrit af* í **lýsing** reitnum.
5. Ef þú vilt bæta við nýju sérsniðnu útliti sem byggir á innbyggðu útliti skaltu fara í gegnum eftirfarandi skref:  
   1. Valið er aðgerðin **Nýtt**. Síðan **Setja inn innbyggt útlit fyrir skýrslu** birtist. Reitirnir **Auðkenni** og **Heiti** eru fylltir inn sjálfkrafa.
   2. Til að bæta við sérsniðnu Word-skýrsluútliti skaltu velja **Setja inn Word-útlit** gátreitinn.
   3. Til að bæta við sérsniðnu RDLC-skýrsluútliti skaltu velja **Setja inn RDLC-útlit** gátreitinn.
   4. Velja hnappinn **Í lagi**.  

    Nýja sérsniðna útlitið birtist nú á síðunni **Sérsniðið skýrsluútlit**. Ef nýtt útlit byggir á innbyggðu útliti er það með orðin **Afrit af innbyggðu útiliti** í reitnum **Lýsing**. Ef ekkert innbyggt útlit var til staðar fyrir skýrsluna þá er nýja útlitið með orðin **Nýtt útlit** í reitnum **Lýsing**, sem táknar að sérsniðna útlitið er autt.
6. Reiturinn **Heiti fyrirtækis** er sjálfgefið auður, sem táknar að sérsniðið útlit er í boði fyrir skýrsluna í öllum fyrirtækjum. Til að gera sérsniðið útlit aðeins aðgengilegt fyrir tiltekið fyrirtæki, skal velja **Breyta** og stilla síðan reitinn **Heiti fyrirtækis** á það fyrirtæki sem þú vilt.

Sérsniðna útlitið hefur verið búið til. Þá er hægt að breyta sérsniðna útlitinu eftir þörfum.

> [!TIP]
> Hægt er að flytja niðurstöður skýrslunnar út í Excel-skrá til að skoða allt gagnasafnið, þar með talið alla dálkana, en án útlitsins. Excel-skráin getur hjálpað til við að staðfesta að skýrslan skili væntanlegum gögnum eða beri kennsl á vandamálin. Nánari upplýsingar er að finna [í greina skýrslugögn með Excel](report-analyze-excel.md).

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Breyta sérsniðnu útliti

Til að breyta skýrsluútliti þarftu fyrst að flytja út skýrsluútlit sem skrá á staðsetningu í tölvunni þinni eða neti. Opnaðu síðan útflutt skjal og gerðu breytingarnar. Þegar þú hefur lokið við að gera breytingarnar flyturðu inn skýrsluútlitið.

### <a name="to-modify-a-custom-layout"></a>Skýrsluútliti sérsniðnu breytt

1. Þú flytur út sérsniðið útlit á síðunni **sérsniðið skýrsluútlit**. Ef þessi síða er ekki þegar opin skaltu leita að og opna síðuna **Val á skýrsluútliti**, velja skýrsluna sem þú vilt breyta útlitið fyrir og velja svo aðgerðina **Sérsniðið útlit**.  
2. Á síðunni **Sérsniðið skýrsluútlit** skal velja útlitið sem þú vilt breyta, veldu **Flytja út útlit** aðgerðina og svo velja **Vista** eða **Vista sem** til að vista skýrsluútlitsskjalið á staðsetningu í tölvunni eða á netkerfi.  
3. Opnaðu skýrsluútlitsskjalið sem þú vistaðir og gerðu breytingar.

   Ef þú ert að breyta Word-útliti skaltu opna útlitsskjalið í Word. Til að breyta upplýsingum má sjá [vinnu með Word skipulag](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   Breyting RDLC-skýrsluútlits er flóknara en Word-skýrsluútlits. Frekari upplýsingar um það hvernig RDLC-skýrsluútliti er breytt eru í [Hanna RDLC-skýrsluútlit](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Mundu að vista breytingar þegar lokið.

4. Farið aftur á síðuna **Sérsniðið skýrsluútlit**, veljið skýrsluútlit sem var flutt út og breytt og veljið svo **Flytja inn útlit** aðgerðina.  

5. Í svarglugganum **Flytja inn** skal velja **Velja** til að finna og velja brreytt skjal skýrsluútlits og svo velja **Opna**.

> [!IMPORTANT]
> Mundu að flytja inn skjal skýrsluútlits sem þú breyttir. Annars verður nýja skýrsluútlitið ekki í boði.

<!--
##  <a name="MakeChangesToLayout"></a> Create and Modify Custom Report Layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word, like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### Embedding Fonts in Word Layouts for Consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. For more information about embedding fonts in Word, see [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="RemoveField"></a> Removing Label and Data Fields in Word Layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### To remove a label or data field  

1. Right-click the field that you want to delete, and then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### Adding data fields

Adding data fields from a report dataset is a more advanced and requires some knowledge of the report dataset. For information about adding fields for data, labels, data, and images, see [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Breyta núverandi skýrsluútliti](ui-how-change-layout-currently-used-report.md)  
[Flytja inn og út sérsniðið skýrsluútlit eða skjalaútlit](ui-how-import-and-export-report-layout.md)  
[Vinna með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
[Undirbúa Financial Reporting með fjárhagsskemu og lyklategundum](bi-how-work-account-schedule.md) 
[Business Intelligence](bi.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]