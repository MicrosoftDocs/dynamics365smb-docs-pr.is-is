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
ms.date: 03/06/2022
ms.author: edupont
ms.openlocfilehash: 465954e6549ee7ffd0822438a0ad004686d5b424
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9604778"
---
# <a name="legacy-create-and-modify-custom-report-layouts"></a>Arfur Stofna og breyta skipan sérsniðinnar skýrslu

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Sjálfgefið er að skýrslur séu með innbyggðu útliti. Skýrsluútlit getur verið annað hvort RDLC (skýrslufyrir tungumálabiðlarahlið), Microsoft Word skýrsluútlit eða bæði. Og á meðan ekki er hægt að breyta innbyggðu útliti getur þú búið til sérsniðna skipan. Skýrsla getur haft marga skipan sérsniðinnar skýrslu.

> [!NOTE]  
> Í [!INCLUDE[prod_short](includes/prod_short.md)] er hugtakið "skýrsla" nær einnig utan um skjöl sem snúa að skjölum, svo sem sölureikninga og pöntunarstaðfestingar sem send eru viðskiptamönnum sem PDF-skrár.

Ef búa á til sérsniðið útlit er annað hvort afritað sérsniðið útlit eða bætt við nýju sérsniðnu útliti. Sérsniðnar uppsetningar eru oft byggðar á innbyggðu útliti. Þegar bætt er við nýju sérsniðnu útliti er hægt að bæta annaðhvort RDLC eða Word-skýrslugerð við uppsetningu eða hvort tveggja. Nýtt sérsniðinn skipulag verður Byggt á innbyggðu útliti fyrir skýrsluna, sé þess nokkur völ. Ef ekkert innbyggt skipulag er til fyrir skýrslugerðina er stofnuð ný auð Uppsetning. Þú verður að breyta og hanna þetta auða útlit frá grunni. Frekari upplýsingar um RDLC og Word-skýrsluna skipulag, innbyggð og sérsniðin skipulag og fleira í [Umsjón með skýrsluskipan](ui-manage-report-layouts.md).  

> [!TIP]
> Notið ársskýrslur til að fá innsýn í fjárhagsgögnin sem geymd eru í bókhaldslykli. Frekari upplýsingar um [undirbúning fjárhagsskýrslugerðar með fjárhagslegum gögnum og lykilflokkum](bi-how-work-account-schedule.md).

Þegar Uppsetning sérsniðinnar skýrslu hefur verið skilgreind er hægt að velja þær á kortasíðum viðskiptamannakorta og lánardrottna. Uppsetning er síðan notuð þegar skjöl eru stofnuð fyrir viðskiptavininn eða lánardrottininn. [Frekari upplýsingar um skilgreiningu Skjalauppsetningar fyrir viðskiptavini og lánardrottna](ui-define-customer-vendor-document-layouts.md).

Einnig er hægt að nota sérsniðna skýrsluskipan til að bæta efni í bréfapóstum. Skýrsluútlit getur sparað tíma og hjálpað til við að tryggja samræmi með því að endurnýta sama efni þegar þú átt samskipti við viðskiptavini þína. Ef nota á sérsniðna skýrslu með tölvupósti verður skrárgerðin fyrir útlitinu að vera Word; Ekki er hægt að nota RDLC-skrárgerðina. Frekari upplýsingar í [Setja upp Endurnýtanlegan tölvupóst-texta og skipulag](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts).

## <a name="create-a-custom-layout"></a>Stofna sérsniðið útlit

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Val á skýrsluútliti** og velja síðan viðkomandi tengil.

    Á **valsíðu** skýrsluuppsetningar eru allar skýrslurnar sem tiltækar eru í fyrirtækinu tilgreindar í **reitnum Nafn** fyrirtækis efst á síðunni.
2. **Fyrirtækið sem stofna á skýrsluútlit fyrir fyrir er valið í reitnum Nafn** fyrirtækis.
3. Valin er röðin fyrir skýrsluna sem á að stofna útlit fyrir og síðan er **valin aðgerðin sérsniðin skipan**.  

   **Síðan Uppsetning sérsniðinnar skýrslu** birtist og birtir lista yfir allar sérsniðnar uppsetningar sem eru tiltækar fyrir völdu skýrsluna.
4. Ef búa á til eintak af sérsniðnu útliti skal velja sérsniðið útlit á listanum og velja **síðan afritunaraðgerðina**.  

   Afrit af sérsniðna útlitinu birtist á síðunni **Sérsniðið skýrsluútlit** með orðunum *Afrit af* í **lýsing** reitnum.
5. Ef þú vilt bæta við nýju sérsniðnu útliti á grundvelli innbyggða útlits skaltu fylgja þessum skrefum:  
   1. Valið er aðgerðin **Nýtt**. **Innbyggða Útlitshönnun fyrir skýrslusíðu** birtist með **Kenni** og **Heiti** svæða sem sjálfkrafa hafa verið fyllt inn.
   2. Kveikja skal á **uppsetningu** á skipanagerð skipta til að bæta við gerð útlits SÉRSNIÐINNAR skýrslu eða kveikja á **uppsetningu RDLC-útlits** til að bæta við sérsniðnu RDLC-skýrslu.
   4. Velja hnappinn **Í lagi**.  

    Nýja sérsniðna útlitið birtist nú á síðunni **Sérsniðið skýrsluútlit**. Ef nýtt útlit byggist á innbyggðu útliti þá birtast orðin **afrit af innbyggðu útliti** í **reitnum Lýsing**. Ef ekkert innbyggt skipulag er til fyrir skýrsluna er nýtt útlit **með nýju** útliti í **reitnum Lýsing**, sem þýðir að sérsniðið útlit er autt.
6. Sjálfgefið er að **reiturinn Heiti** fyrirtækis er auður og sérsniðna útlitið er tiltækt fyrir skýrslur hjá öllum fyrirtækjum. Ef velja á sérsniðið skipulag sem aðeins er tiltækt fyrir tiltekið fyrirtæki er valið **Breyta** og síðan er reiturinn Heiti **fyrirtækis settur** á fyrirtækið sem óskað er eftir.

Sérsniðið útlit hefur verið stofnað og hægt er að breyta því að vild.

> [!TIP]
> Hægt er að flytja niðurstöður skýrslunnar út Microsoft Excel í skrá til að skoða heildardataset, þar á meðal alla dálka, en án útlits. Excel-skráin getur auðveldað að skýrslan skili væntanlegum gögnum eða greiningu vandamála. Frekari upplýsingar í að [greina skýrslugögn með Excel](report-analyze-excel.md).

## <a name="modifying-a-custom-layout"></a><a name="ModifyCustomLayout"></a>Breyta sérsniðnu útliti

Til að breyta sérsniðnu skýrslusniði þarf fyrst að flytja skýrsluútlitið út sem skrá á birgðageymslu í tölvunni eða netinu. Opnaðu síðan útflutt skjal og gerðu breytingarnar. Þegar þú hefur lokið við að gera breytingarnar flyturðu inn skýrsluútlitið.

### <a name="modify-a-custom-layout"></a>Breyta sérsniði

1. Flytja sérsniðið útlit út af **sérsniðnu útliti skýrslusíðunnar**. Ef sú síða er ekki þegar opin skal leita að og opna **valsíðu** skýrsluútlits, velja skýrsluna sem hefur útlitið sem á að breyta og velja **síðan aðgerðina sérsniðna**.  
2. **Á síðunni Uppsetning sérsniðna skýrslna** skal velja útlitið sem á að breyta, velja **aðgerðina Flytja út útlit**, síðan **Vista** eða **Vista sem** til að vista skjal skýrsluútlits á staðsetningu í tölvunni eða neti.  
3. Opna skal skýrsluútlitskjalið sem vistað var og gera breytingar.

   Ef þú ert að breyta Word-útliti skaltu opna útlitsskjalið í Word. Frekari upplýsingar um ritgerðarskýrslur í [vinnu með Orðskipulag](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   Breyting RDLC-skýrsluútlits er flóknara en Word-skýrsluútlits. Frekari upplýsingar um breytingar á RDLC-skýrslu við [hönnun RDLC-skýrslu uppsetningar](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Munið að vista breytingarnar þegar þið eruð búin.

4. Fara skal aftur í **síðuna Uppsetning sérsniðinnar skýrslu**, velja skýrsluútlit sem flutt var út og breyta og velja **síðan aðgerðina innflutningsútlit**.  

5. **Í innflutningsglugganum** er **valið** til að finna og velja breytt skjal fyrir uppsetningu skýrslna og síðan valið **Opna**.

> [!IMPORTANT]
> Mundu að flytja inn skjal skýrsluútlits sem þú breyttir. Annars verður nýja skýrsluútlitið ekki í boði.

<!--
##  <a name="MakeChangesToLayout"></a> Create and modify custom report layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### Embedding fonts in Word layouts for consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. Learn more about embedding fonts in Word at [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="RemoveField"></a> Removing label and data fields in Word layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### To remove a label or data field  

1. Right-click the field you want to delete, then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### Adding data fields

Adding data fields from a report dataset is more advanced and requires some knowledge of the report dataset. Learn more about adding fields for data, labels, and images at [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig .

[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Breyta núverandi skýrsluútliti](ui-how-change-layout-currently-used-report.md)  
[Flytja inn og út sérsniðið skýrsluútlit eða skjalaútlit](ui-how-import-and-export-report-layout.md)  
[Vinna með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
[Undirbúa fjárhagsskýrslugerð með fjárhagslegum gögnum og lykilflokkum](bi-how-work-account-schedule.md)  
[Viðskiptaupplýsingar](bi.md)  
[Vinna með[!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
