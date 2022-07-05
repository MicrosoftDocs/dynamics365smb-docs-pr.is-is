---
title: Unnið með Excel-skipulag
description: Lærðu að búa til og breyta útliti skýrslu sem eru byggð á með Excel.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/14/2022
ms.author: jswymer
ms.openlocfilehash: c0800642804b8e8c9e1dc629224bfac77b174500
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9075734"
---
# <a name="working-with-excel-layouts"></a>Unnið með Excel-skipulag

Excel skýrsluskipanir eru byggðar á Microsoft Excel vinnubókum (. xlsx files). Þeir gera kleift að stofna skýrslur með því að nota kunnuglegar Excel-aðgerðir til að draga saman, greina og kynna gögn, líkt og formúlur, PivotTables og Pivotgrösum.

![Sýnir dæmi um Excel útlit.](media/excel-layout-2.png)

Í þessari grein er útskýrt eitthvað af því mikilvægasta sem þú þarft að vita til að byrja með Excel skipulag.

## <a name="why-use-excel-layouts"></a>Hvers vegna að nota Excel-skipulag?

Hér eru nokkur meiri ávinningur af notkun Excel-uppsetningar:

- Búa til gagnvirkar skýrslur með sjóningum eins og sneiðingum
- Skoða hrágögn úr skýrslunni DataSet til að hjálpa til við að skilja hvernig skýrslan virkar og hvaðan gögnin á sjónarbilinu koma frá
- Nota aðgerðir sem eru byggðar á Office til að gera eftir vinnslu skýrslna, eins og:
  - [Vinnublöð vernduð](https://support.microsoft.com/en-us/office/protect-a-worksheet-3179efdb-1285-4d49-a9c3-f4ca36276de6)
  - [Beitt næmi Límmiðar](https://support.microsoft.com/en-us/office/apply-sensitivity-labels-to-your-files-and-email-in-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
  - [Athugasemdum bætt við og athugasemdir](https://support.microsoft.com/en-us/office/insert-comments-and-notes-in-excel-65f504d8-160b-4a05-ac30-46fbd5227a52)
  - [Spár og greining](https://support.microsoft.com/en-us/office/introduction-to-what-if-analysis-22bffa5f-e891-4acc-bf7a-e4645c446fb4) 
- Nota uppsetta samþættingu viðbætur og forrita eins Power Automate og flæðisl OneDrive.

## <a name="get-started"></a>Hafist handa

Það eru í rauninni tvö verkefni sem taka þátt í uppsetningu Excel-útlits á skýrslu:

1. Stofnið nýja Útlitshönnun fyrir Excel.
2. Bæta nýju útliti við skýrsluna.

## <a name="task-1-create-the-excel-layout-file"></a>Verkefni 1: Búa til skrána fyrir Excel-skipulag

Þrjár leiðir eru til að búa til Excel-Útlitshönnun fyrir skýrslu eins og útskýrt er í þessum kafla

### <a name="from-any-report"></a>[Úr hvaða skýrslu](#tab/any-report)

Hægt er að nota eftirfarandi skref til að búa til Excel-skipulag í hvaða skýrslu sem er, óháð gildandi útlitsgerð. Í Excel-útlitinu verða til nauðsynleg **gagnaskjöl** og Tafla, **lýsigagnablað** skýrslu og ekkert annað.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. **Í listanum Uppsetning skýrslu** er hægt að velja hvaða útlit fyrir skýrsluna og velja **síðan aðgerðina keyra skýrslu**.
3. Á skýrslubeiðssíðu skal velja **Senda í** > **Microsoft Excel skjal (aðeins gögn)** > **í lagi**.

   Í þessu skrefi er niðurhal Excel vinnubók með skýrslunni DataSet.
4. Opna skrána sem sótt er í Excel, gera breytingar og vista síðan skrána.

### <a name="from-another-excel-layout-on-a-report"></a>[Úr öðru Excel útliti í skýrslu](#tab/other-layout)

Ef Excel-útlit er þegar í skýrslu er fyrirliggjandi skipulag notað sem upphafsstaður. Tvær nálganir eru til þess að fá afrit af útlitinu. Hægt er að flytja fyrirliggjandi útlit út af **síðu skýrsluuppsetningar** eða sækja útlitið út frá beiðssíðu skýrslunnar. Báðar leiðir sækja Excel layout-Útlitshönnun sem nær yfir öll þau blöð sem í skránni eru. Munurinn er sá að úr beiðssíðu kemur útlitið með raunverulegum gögnum. Gögnin eru ekki nauðsynleg, en það hjálpar til þegar útlitið er hannað.

#### <a name="approach-1-export-the-layout-from-the-report-layouts-page"></a>Nálgun 1: flytja útlitið út frá **síðu skýrsluuppsetningar**

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Velja Excel-útlit af listanum og velja **síðan aðgerðina Flytja út útlit** efst á síðunni.
3. Opnaðu skrána í Excel, gerðu breytingarnar og geymdu síðan skrána.

#### <a name="approach-2-download-the-layout-from-the-reports-request-page"></a>Nálgunarbanni 2: Sækja skal um skipulag frá beiðssíðu skýrslunnar

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. **Í listanum Uppsetning skýrslu** er hægt að velja hvaða útlit fyrir skýrsluna og velja **síðan aðgerðina keyra skýrslu**.
3. Á skýrslubeiðssíðu er valið **Sækja**.
4. Opnaðu skrána í Excel, gerðu breytingarnar og geymdu síðan skrána.

### <a name="from-al-code"></a>[Frá AL-kóða](#tab/from-code)

Þessi leið er sú Þrítugasta. Það krefst þekkingar á AL-kóðanum, þannig að það markforritarar. Excel-skipanir í þessu tilfelli eru hluti af framlengingarpakka sem þú setur upp. Frekari upplýsingar er að finna [í stofnun Excel-útlits](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout) í Developer og Hjálp við það.

---

## <a name="task-2-add-the-excel-layout-to-the-report"></a>Verkefni 2: Bættu Excel-útlitinu við skýrsluna

Þegar Excel-útlitskráin er komin af er næsta verkefni að bæta henni við sem nýtt útlit fyrir skýrsluna.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Velja **nýtt útlit**.
3. KENNI **skýrslunnar er** stillt á.
4. Færið inn nafn í **Heiti** útlits.
5. Stilla **Sniðkosti** í **Excel**.
6. Veldu **OK** > **Veldu** til að opna skrárexplorer í tækinu. 
7. Finna og velja Excel-skrána og velja **síðan opna**.

   Völdu skránni er hlaðið upp í útlitið og síðan er snúið aftur á **síðuna útlit** skýrslu.
8. Ef þú vilt sjá hvernig skýrslan lítur út með nýja útlitinu skaltu velja útlitið á listanum og velja **síðan Keyra skýrslu**.


<!--

**Data** sheet
  - An Excel layout must contain a sheet named **Data**.
  - The **Data** sheet can only include one table named **Data**.

**Data** table
  - The **Data** sheet must include a table that has the name **Data**.
  - The table must have at least one column and can only include columns that are also in report dataset.
  - The table must start in the first cell A1 of the **Data** sheet.

3. Report Metadata 
-->

## <a name="understanding-excel-layouts"></a>Skilningur á Excel-skipan

Það eru fáir hlutir sem þú ættir að vita eða íhuga þegar þú byrjar að stofna eða gera breytingar á Excel útliti. Hvert Excel-útlit þarf að innihalda tvo þætti: **gagnatöflu** og **Gagnaöflun**. Þessum þáttum út frá grunni útlits með því að skilgreina viðskipagögn frá Viðskiptamiðinu sem hægt er að vinna með. Hægt er að hugsa **sér gagnablað** sem nokkurs konar samning milli útlits í viðskipagögnum. Þessi gögn eru notuð sem Uppruni útreikninganna og birtinga sem óskað er að séu á öðrum blöðum.

Nokkrar sértækar kröfur eru gerðar við uppbyggingu Excel-vinnubókar. Ef kröfurnar eru ekki uppfylltar er erfitt að nota útlitið. Eftirfarandi skýringarmynd og tafla lýsir einingum Excel-útlits og-þarfa.

[![Sýnir mismunandi einingar Excel-útlits.](media/excel-layout-callouts-2.png)](media/excel-layout-callouts-2.png#lightbox)

|Nr.|Atriði|Lýsing|Áskilið|
|---|-------|----|---|
|1|**Gagnablað**|<ul><li>Verður að hafa **nafngögn**</li><li>Getur aðeins innihaldið eina töflu og töfluna verður að nefna **gögn**</li></ul>|![Er skylda](media/check.png) | 
|2|**Gagnatöflu**|<ul><li>Verður að hafa **nafngögn**</li><li>Verður að vera a.m.k. einn dálkur.</li><li>Getur aðeins innihaldið dálka sem eru í skýrslunni DataSet.</li><li>Verður að byrja í fyrstu frumu **a1** á **gagnablaðinu**</li></ul>|![Er skylda](media/check.png)|
|3|Kynningarblöð|<ul><li>Notað til að kynna gögn.</li><li>Gögn koma frá **gagnablaðinu**. </li></ul>||
|4|**Blað skýrslulýsigagna**|<ul><li>Sjálfkrafa innifalin ef útlitið var búið til með því að flytja aðra skýrslu út sem Excel</li><li>Inniheldur almennar upplýsingar um skýrsluna</li><li>Má eyða</li></ul>|

Til að draga saman það sem hægt er og má ekki gera á **gagnablaðinu**:

- Ekki breyta heiti **gagnablaðunar**, **gagnaöflunar** eða dálka.
- Hægt er að eyða eða fela dálka.
- Ekki bæta við neinum dálkum nema það sé tekið með í skýrsluna DataSet.
- Hægt er að setja blöðin í hvaða röð sem er. Til dæmis **getur gagnablað** verið fyrst eða síðast.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig

[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Breyta núverandi skýrsluútliti](ui-how-change-layout-currently-used-report.md)  
[Flytja inn og út sérsniðið skýrsluútlit eða skjalaútlit](ui-how-import-and-export-report-layout.md)  
[Unnið með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
[Undirbúa Financial Reporting með fjárhagsskemu og lyklategundum](bi-how-work-account-schedule.md)  
[Viðskiptaupplýsingar](bi.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Greining á skýrslugögnum með Excel](report-analyze-excel.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]