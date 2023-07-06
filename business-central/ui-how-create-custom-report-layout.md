---
title: Stofna og breyta sérsniðið útlit fyrir skýrslur og skjöl
description: 'Kynntu þér hvernig skal stofna sérstillt útlit til að sérsníða útlit skýrslu þegar hún er skoðuð, prentuð eða vistuð.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/06/2022
ms.author: edupont
---
# <a name="legacy-create-and-modify-custom-report-layouts"></a><a name="legacy-create-and-modify-custom-report-layouts"></a><a name="legacy-create-and-modify-custom-report-layouts"></a>(Eldra) Búa til og breyta sérsniðnum skýrsluútlitum

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Skýrslur eru sjálfgefið með innbyggt útlit. Skýrsluútlitið getur verið annaðhvort RDLC-skýrsluútlit, Microsoft Word skýrsluútlit eða bæði. Og þótt ekki sé hægt að breyta innbyggðu útliti er hægt að búa til sérsniðið útlit. Skýrsla getur verið með mörg sérsniðin útlit.

> [!NOTE]  
> Í [!INCLUDE[prod_short](includes/prod_short.md)] táknar hugtakið "skýrsla" einnig utanaðkomandi skjöl, s.s. sölureikninga og pöntunarstaðfestingar sem þú sendir til viðskiptavina sem PDF skjöl.

Til að búa til sérsniðið útlit skal annaðhvort afrita fyrirliggjandi sérsniðið útlit eða bæta við nýju sérsniðnu útliti. Sérsniðin útlit byggja oft á innbyggðu útliti. Þegar þú bætir við nýju sérsniðnu útliti geturðu valið að bæta við RDLC- eða Word-skýrsluútliti, eða bæði. Nýja sérsniðna útlitið verður byggt á innbyggða útlitinu fyrir skýrsluna ef það er til staðar. Ef ekkert innbyggt útlit er til fyrir skýrslugerðina er nýtt autt útlit búið til. Þú verður að breyta og hanna þetta auða útlit frá grunni. Frekari upplýsingar um RDLC- og Word-skýrsluútlit, innbyggð útlit, sérsniðið útlit og fleira eru í [stjórna skýrsluútliti](ui-manage-report-layouts.md).  

> [!TIP]
> Notaðu fjárhagsskýrslur til að fá innsýn í fjárhagsgögn sem eru geymd í bókhaldslyklum. Frekari upplýsingar er að finna í [Útbúa Financial Reporting með fjárhagsgögnum og reikningsflokkum](bi-how-work-account-schedule.md).

Þegar þú hefur skilgreint sérsniðin skýrsluútlit geturðu valið þau á síðum viðskiptamannaspjalds og lánardrottnaspjalds. Útlitin eru síðan notuð þegar þú býrð til skjöl fyrir viðskiptamann eða lánardrottin. Frekari upplýsingar eru í [Skilgreina útlit skjala fyrir viðskiptamenn og lánardrottna](ui-define-customer-vendor-document-layouts.md).

Einnig er hægt að nota sérsniðið skýrsluútlit til að bæta efni við tölvupóst. Skýrsluútlit geta sparað tíma og tryggt samræmi með því að endurnota sama efnið þegar haft er samband við viðskiptamenn. Til að nota sérsniðið skýrsluútlit með tölvupósti verður skráargerðin fyrir útlitið að vera Word, ekki er hægt að nota RDLC-skráargerð. Frekari upplýsingar má finna á [Setja upp endurnýtanlega texta og útlit tölvupósts ](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts).

## <a name="create-a-custom-layout"></a><a name="create-a-custom-layout"></a><a name="create-a-custom-layout"></a>Búa til sérsniðið útlit

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Val á skýrsluútliti** og velja síðan viðkomandi tengil.

    Síðan **Val á útliti skýrslu** sýnir allar skýrslur sem eru í boði fyrir fyrirtæki sem er tiltekið í reitnum **Heiti fyrirtækis** efst á síðunni.
2. Í reitnum **Heiti fyrirtækis** skal velja fyrirtækið sem á að búa til skýrsluútlit fyrir.
3. Veldu röðina fyrir skýrsluna sem þú vilt stofna útlitið fyrir, og veldu svo **Sérsniðið útlit** aðgerðina.  

   Síðan **Sérsniðið skýrsluútlit** birtist og sýnir öll sérsniðin útlit sem eru í boði fyrir völdu skýrsluna.
4. Ef þú vilt búa til afrit af sérsniðnu útliti sem þegar er til velurðu sérsniðið útlitið af listanum og velur svo **Afrita** aðgerðina.  

   Afrit af sérsniðna útlitinu birtist á síðunni **Sérsniðið skýrsluútlit** með orðunum *Afrit af* í **lýsing** reitnum.
5. Ef þú vilt bæta við nýju sérsniðnu útliti sem byggir á innbyggðu útliti skaltu fylgja þessum skrefum:  
   1. Valið er aðgerðin **Nýtt**. Síðan **Setja inn innbyggt útlit fyrir skýrslu** birtist með reitunum **Auðkenni** og **Heiti** sjálfkrafa útfylltum.
   2. Kveiktu á **Setja inn Word-útlit** til að bæta við sérsniðinni gerð Word-skýrsluútlits EÐA kveiktu á **Setja inn RDLC-útlit** til að bæta við sérsniðinni gerð RDLC-skýrsluútlits.
   4. Velja hnappinn **Í lagi**.  

    Nýja sérsniðna útlitið birtist nú á síðunni **Sérsniðið skýrsluútlit**. Ef nýtt útlit byggir á innbyggðu útliti þá birtast orðin **Afrit af innbyggðu útiliti** í reitnum **Lýsing**. Ef ekkert innbyggt útlit var til staðar fyrir skýrsluna þá er nýja útlitið með orðin **Nýtt útlit** í reitnum **Lýsing**, sem merkir að sérsniðna útlitið er autt.
6. Reiturinn **Heiti fyrirtækis** er sjálfgefið auður og sérsniðna útlitið er í boði fyrir skýrslur í öllum fyrirtækjum. Til að gera sérsniðið útlit aðeins aðgengilegt fyrir tiltekið fyrirtæki skal velja **Breyta** og stilla síðan reitinn **Heiti fyrirtækis** á það fyrirtæki sem þú vilt.

Sérsniðna útlitið hefur verið búið til og hægt er að breyta því eftir þörfum.

> [!TIP]
> Hægt er að flytja niðurstöður skýrslunnar út í Microsoft Excel skrá til að skoða allt gagnasafnið, þar með talið alla dálkana, en án útlitsins. Excel-skráin getur hjálpað til við að staðfesta að skýrslan skili væntanlegum gögnum eða beri kennsl á vandamálin. Frekari upplýsingar er að finna í [Greining skýrslugagna með Excel](report-analyze-excel.md).

## <a name="modifying-a-custom-layout"></a><a name="modifying-a-custom-layout"></a><a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Breyta sérsniðnu útliti

Til að breyta sérsniðnu skýrsluútliti þarftu fyrst að flytja út skýrsluútlit sem skrá á staðsetningu í tölvunni þinni eða neti. Opnaðu síðan útflutt skjal og gerðu breytingarnar. Þegar þú hefur lokið við að gera breytingarnar flyturðu inn skýrsluútlitið.

### <a name="modify-a-custom-layout"></a><a name="modify-a-custom-layout"></a><a name="modify-a-custom-layout"></a>Breyta sérsniðnu útliti

1. Flytja út sérsniðið útlit á síðunni **Sérsniðið skýrsluútlit**. Ef sú síða er ekki þegar opin skaltu leita að og opna síðuna **Val á skýrsluútliti**, velja skýrsluna sem þú vilt breyta útliti fyrir og velja svo aðgerðina **Sérsniðið útlit**.  
2. Á síðunni **Sérsniðið skýrsluútlit** skal velja útlitið sem þú vilt breyta, veldu **Flytja út útlit** aðgerðina og svo velja **Vista** eða **Vista sem** til að vista skýrsluútlitsskjalið á staðsetningu í tölvunni eða á netkerfi.  
3. Opnaðu skjal skýrsluútlitsins sem þú vistaðir og gerðu breytingar.

   Ef þú ert að breyta Word-útliti skaltu opna útlitsskjalið í Word. Frekari upplýsingar um breytingar á Word-skýrslum er að finna í [Vinna með Word-útlit](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   Breyting RDLC-skýrsluútlits er flóknara en Word-skýrsluútlits. Frekari upplýsingar um breytingu á RDLC-skýrsluútliti er að finna í [Hönnun RDLC-skýrsluútlits](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Mundu að vista breytingarnar að þessu loknu.

4. Farið aftur á síðuna **Sérsniðið skýrsluútlit**, veljið skýrsluútlit sem var flutt út og breytt og veljið svo **Flytja inn útlit** aðgerðina.  

5. Í svarglugganum **Flytja inn** skal velja **Velja** til að finna og velja breytt skjal skýrsluútlits og svo velja **Opna**.

> [!IMPORTANT]
> Mundu að flytja inn skjal skýrsluútlits sem þú breyttir. Annars verður nýja skýrsluútlitið ekki í boði.

<!--
## <a name="create-and-modify-custom-report-layouts"></a><a name="create-and-modify-custom-report-layouts"></a><a name="create-and-modify-custom-report-layouts"></a><a name="MakeChangesToLayout"></a> Create and modify custom report layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### <a name="embedding-fonts-in-word-layouts-for-consistency"></a><a name="embedding-fonts-in-word-layouts-for-consistency"></a><a name="embedding-fonts-in-word-layouts-for-consistency"></a>Embedding fonts in Word layouts for consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. Learn more about embedding fonts in Word at [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

### <a name="removing-label-and-data-fields-in-word-layouts"></a><a name="removing-label-and-data-fields-in-word-layouts"></a><a name="removing-label-and-data-fields-in-word-layouts"></a><a name="RemoveField"></a> Removing label and data fields in Word layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field"></a><a name="to-remove-a-label-or-data-field"></a><a name="to-remove-a-label-or-data-field"></a>To remove a label or data field

1. Right-click the field you want to delete, then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### <a name="adding-data-fields"></a><a name="adding-data-fields"></a><a name="adding-data-fields"></a>Adding data fields

Adding data fields from a report dataset is more advanced and requires some knowledge of the report dataset. Learn more about adding fields for data, labels, and images at [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft þjálfun](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Breyta núverandi skýrsluútliti](ui-how-change-layout-currently-used-report.md)  
[Flytja inn og út sérsniðið skýrsluútlit eða skjalaútlit](ui-how-import-and-export-report-layout.md)  
[Vinna með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
[Útbúa Financial Reporting með fjárhagsgögnum og reikningsflokkum](bi-how-work-account-schedule.md)  
[Viðskiptaupplýsingar](bi.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
