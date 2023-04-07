---
title: Unnið með Excel-útlit
description: Kynntu þér hvernig á að búa til og breyta skýrsluútliti sem er hannað með Excel.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 11/10/2022
ms.author: jswymer
---
# Unnið með Microsoft Excel útlit

Microsoft Excel skýrsluútlit byggja á Excel-vinnubókum (.xlsx-skrár). Með þeim geturðu búið til skýrslur sem innihalda kunnuglega Excel-eiginleika til að draga saman, greina og kynna gögn eins og formúlur, PivotTable og PivotChart.

![Sýnir dæmi um Excel-útlit.](media/excel-layout-2.png)

Þessi grein útskýrir nokkur mikilvæg atriði sem þú þarft að vita til að hefjast handa með Excel-útlit.

## Af hverju að nota Excel-útlit?

Ávinningur þess að nota Excel-útlit:

- Búðu til gagnvirkar skýrslur með myndrænni framsetningu eins og sneiðsíum.
- Skoðaðu hrá gögn úr gagnasafni skýrslunnar sem hjálpar þér að skilja hvernig skýrslan virkar og hvaðan gögnin í myndefninu koma.
- Notaðu innbyggða Microsoft Office eiginleika til að gera eftirvinnslu á myndþýddum skýrslum, þ.m.t.:
  - [Vinnublöð varin](https://support.microsoft.com/office/protect-a-worksheet-3179efdb-1285-4d49-a9c3-f4ca36276de6)
  - [Trúnaðarmerki notuð](https://support.microsoft.com/office/apply-sensitivity-labels-to-your-files-and-email-in-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
  - [Ummælum og athugasemdum bætt við](https://support.microsoft.com/office/insert-comments-and-notes-in-excel-65f504d8-160b-4a05-ac30-46fbd5227a52)
  - [Spá og greining](https://support.microsoft.com/office/introduction-to-what-if-analysis-22bffa5f-e891-4acc-bf7a-e4645c446fb4)
- Notaðu uppsettar innbætur og samþættingar forrits eins og Power Automate flæði eða OneDrive.

## Hafist handa

Í grundvallaratriðum eru tvö verk sem koma að uppsetningu Excel-útlits í skýrslu:

1. Búðu til nýja Excel-útlitsskrá.
2. Bættu nýja útlitinu við skýrsluna.

## Verk 1: Búa til Excel-útlitsskrá

Þetta eru leiðirnar þrjár til að búa til Excel-útlitsskrá fyrir skýrslu.

### [Úr öllum skýrslum](#tab/any-report)

Fylgdu þessum skrefum til að búa til Excel-útlit úr hvaða skýrslu sem er, óháð núverandi útlitsgerð. Excel-útlitið mun innihalda nauðsynlegt **Gagnabla** og töflu, vinnublaðið **Lýsigögn skýrslu** og ekkert annað.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Á síðunni **Skýrsluútlit** skal velja hvaða útlit sem er fyrir skýrsluna, síðan velja aðgerðina **Keyra skýrslu**.
3. Á beiðnisíðu skýrslunnar skal velja **Senda til** > **Microsoft Excel skjal (aðeins gögn)** > **Í lagi**.

   Þetta skref hleður niður Excel-vinnubók sem inniheldur gagnasafn skýrslunnar.
4. Opnaðu skrána sem var hlaðið niður í Excel, gerðu breytingar og vistaðu síðan skrána.

### [Úr öðru Excel-skýrsluútliti](#tab/other-layout)

Ef þegar er til Excel-útlit fyrir skýrslu er hægt að nota fyrirliggjandi útlit sem útgangspunkt. Það eru tvær aðferðir til að fá afrit af útlitinu. Hægt er að flytja út núverandi útlit af síðunni **Skýrsluútlit** eða sækja útlitið af beiðnisíðu skýrslunnar. Báðar leiðir sækja Excel-útlitsskrána sem inniheldur öll vinnublöð fyrirliggjandi skráar. Munurinn er sá að þegar þú sækir hana af beiðnisíðunni inniheldur útlitið raunveruleg gögn. (Gögnin eru ekki nauðsynleg en þau hjálpa þegar útlitið er hannað.)

#### Aðferð 1: Flytja út útlitið af síðunni **Skýrsluútlit**.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Veldu Excel-útlitið af listanum og veldu svo aðgerðina **Flytja út útlit** efst á síðunni.
3. Opnaðu skrána í Excel, gerðu breytingarnar og vistaðu síðan skrána.

#### Aðferð 2: Sækja útlitið af beiðnisíðu skýrslunnar

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Á síðunni **Skýrsluútlit** skal velja hvaða útlit sem er fyrir skýrsluna, síðan velja aðgerðina **Keyra skýrslu**.
3. Á beiðnisíðu skýrslunnar skal velja **Sækja**.
4. Opnaðu skrána í Excel, gerðu breytingarnar og vistaðu síðan skrána.

### [Frá AL-kóða](#tab/from-code)

Þetta er ítarlegasta aðferðin við að búa til Excel-skýrsluútlit. Hún er ætluð forriturum þar sem hún krefst þekkingar á AL-kóða. Í þessari aðferð eru Excel-útlitin hluti af viðbótarpakka sem þú setur upp. Frekari upplýsingar er að finna í [Excel-skýrsluútlit búið til](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout) í hjálparefni þróunaraðila og upplýsingatækni.

---

## Verk 2: Bæta Excel-útlitinu við skýrsluna

Þegar þú ert með Excel-útlitsskrána er næsta verk að bæta henni við sem nýtt útlit fyrir skýrsluna.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Veldu **Nýtt útlit**.
3. Stilltu **Skýrslukenni** á *Skýrslu*.
4. Færðu inn heiti í **Útlitsheiti**.
5. Stilltu **Sniðsvalkosti** á **Excel**.
6. Valið  **er í lagi** og skal þá gera einn af eftirtöldum skrefum til að senda útlitsskrána inn fyrir skýrsluna:

   [!INCLUDE[file-upload](includes/file-upload.md)]

   Valdri skrá er hlaðið upp í útlitið og síðan **Skýrsluútlit** opnast.
8. Til að sjá hvernig skýrslan lítur út í nýja útlitinu skal velja útlitið af listanum og velja síðan **Keyra skýrslu**.

<!--

**Data** sheet
  - An Excel layout must contain a sheet named **Data**.
  - The **Data** sheet must include a table named **Data**.

**Data** table
  - The **Data** sheet must include a table named **Data**.
  - The table must have at least one column and can only include columns that are also in the report dataset.
  - The table must start in the first cell **A1** of the **Data** sheet.

3. Report metadata 
-->

## Skilningur á Excel-útlitum

Hafa þarf nokkur atriði í huga til að vita eða velta fyrir sér hvenær á að búa til eða gera breytingar á Excel-útliti. Excel-útlit verður að innihalda tvær einingar: **Gagnablað** og **Gagnatöflu**. Þessar einingar mynda grunn skýrslunnar með því að skilgreina viðskiptagögnin úr Business Central sem hægt er að vinna með. Hægt er að líta á **Gagnablaðið** sem eins konar samning milli útlits og viðskiptagagna. Þessi gögn verða notuð sem heimild útreikninga og myndrænna framsetninga sem á að kynna á öðrum vinnublöðum.

Gerðar eru ákveðnar kröfur um skipulag Excel-vinnubókar. Ef kröfurnar eru ekki uppfylltar lendirðu í vandræðum með að nota útlitið. Í eftirfarandi skýringarmynd og töflu er gert grein fyrir einingum Excel-útlits og kröfunum.

[![Sýnir mismunandi einingar Excel-útlits.](media/excel-layout-callouts-2.png)](media/excel-layout-callouts-2.png#lightbox)

|Nr.|Atriði|Lýsing|Áskilið|
|---|-------|----|---|
|1|**Gagna**-blað|<ul><li>Verður að hafa heitið **Gögn**.</li><li>Má aðeins innihalda eina töflu, sem verður að heita **Gögn**.</li></ul>|![Er áskilið](media/check.png) | 
|2|**Gagna**-tafla|<ul><li>Verður að hafa heitið **Gögn**.</li><li>Verður að hafa minnst einn dálk.</li><li>Má aðeins innihalda dálka sem eru í gagnasafni skýrslunnar.</li><li>Verður að byrja í fyrsta hólfi **A1** í **Gagnablaðinu**.</li></ul>|![Er áskilið](media/check.png)|
|3|Vinnublöð kynningar|<ul><li>Notað til að kynna gögn.</li><li>Gögn koma úr **Gagnablaðinu**. </li></ul>||
|4|Vinnublaðið **Lýsigögn skýrslu**|<ul><li>Sjálfkrafa með ef útlitið var búið til með því að flytja út aðra Excel-skýrslu.</li><li>Inniheldur almennar upplýsingar um skýrsluna.</li><li>Hægt að eyða.</li></ul>|

Í stuttu máli er það þetta sem þú ættir og ættir ekki að gera í **Gagnablaðinu**:

- Ekki breyta heitinu á **Gagnablaðinu**, **Gagnatöflunni** eða dálkum.
- Þú getur eytt eða falið dálka.
- Ekki bæta við dálkum nema þeir séu í gagnasafni skýrslunnar.
- Þú getur sett vinnublöðin í hvaða röð sem er, með **Gagnablaðinu** fyrst eða síðast.

## Sjá einnig .

[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Breyta núverandi skýrsluútliti](ui-how-change-layout-currently-used-report.md)  
[Flytja inn og út sérsniðið skýrsluútlit eða skjalaútlit](ui-how-import-and-export-report-layout.md)  
[Unnið með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
[Útbúa Financial Reporting með fjárhagsgögnum og reikningsflokkum](bi-how-work-account-schedule.md)  
[Viðskiptaupplýsingar](bi.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Greina skýrslugögn með Excel](report-analyze-excel.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
