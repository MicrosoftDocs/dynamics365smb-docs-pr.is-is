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
ms.openlocfilehash: 2a46c6eab31e89da0956a7d847a64792b18a2fcd
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606938"
---
# <a name="working-with-microsoft-excel-layouts"></a>Vinna við Microsoft Excel skipulag

Microsoft Excel skýrsluskipulag miðast við Excel vinnubækur (. xlsx files). Með þeim er hægt að búa til skýrslur sem innihalda kunnuglegar Excel-aðgerðir til að taka saman, greina og kynna gögn eins og formúlur, PivotTables og Pivotgröra.

![Sýnir dæmi um Excel útlit.](media/excel-layout-2.png)

Í þessari grein er útskýrt nokkur mikilvæg atriði sem þú þarft að vita til að byrja með Excel skipulag.

## <a name="why-use-excel-layouts"></a>Hvers vegna að nota Excel-skipulag?

Kostir við notkun Excel-uppsetningar:

- Búa til gagnvirkar skýrslur með sjónarspilum eins og sneam.
- Skoðið hrágögn úr skýrslunni DataSet sem hjálpar til við að skilja hvernig skýrslan virkar og hvaðan gögnin í sjónarsafni koma.
- Nota innbyggðan eiginleika til að gera Post-vinnslu á skýrslum sem eru í Microsoft Office fráhendi, þar á meðal:
  - [Hlítt vinnublöð](https://support.microsoft.com/office/protect-a-worksheet-3179efdb-1285-4d49-a9c3-f4ca36276de6)
  - [Beitt næmi Límmiðar](https://support.microsoft.com/office/apply-sensitivity-labels-to-your-files-and-email-in-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
  - [Athugasemdum bætt við og athugasemdir](https://support.microsoft.com/office/insert-comments-and-notes-in-excel-65f504d8-160b-4a05-ac30-46fbd5227a52)
  - [Spár og greining](https://support.microsoft.com/office/introduction-to-what-if-analysis-22bffa5f-e891-4acc-bf7a-e4645c446fb4)
- Notið uppsettar samþættingar og forritauppsetningar fyrir viðbætur og forrit eins og Power Automate flæði eða OneDrive.

## <a name="get-started"></a>Hafist handa

Það eru í rauninni tvö verkefni sem taka þátt í að setja upp Excel-útlit af skýrslu:

1. Stofnið nýja Útlitshönnun fyrir Excel.
2. Bæta nýju útliti við skýrsluna.

## <a name="task-1-create-the-excel-layout-file"></a>Verkefni 1: Búa til skrána fyrir Excel-skipulag

Þetta eru þrjár leiðir til að búa til Excel-Útlitshönnun fyrir skýrslu.

### <a name="from-any-report"></a>[Úr hvaða skýrslu](#tab/any-report)

Fylgdu þessum skrefum til að búa til Excel-útlit úr einhverri skýrslu, óháð gildandi útlitsgerð. Í Excel-útlitinu verða til nauðsynleg **gagnaskjöl** og Tafla, **lýsigagnablað** skýrslu og ekkert annað.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. **Á síðunni skipulag uppsetningar** er hægt að velja hvaða uppsetningu fyrir skýrsluna og velja **síðan aðgerðina keyra skýrslu**.
3. Í beiðssíðu skýrslunnar er valið **Senda í** > **Microsoft Excel fylgiskjali (aðeins gögn)** > **í lagi**.

   Í þessu skrefi er niðurhal Excel vinnubók með skýrslunni DataSet.
4. Opna skrána sem sótt er í Excel, gera breytingar og vista síðan skrána.

### <a name="from-another-excel-report-layout"></a>[Frá útliti annarrar Excel-skýrslu](#tab/other-layout)

Ef Excel-útlit er þegar fyrir skýrslu er hægt að nota núverandi uppsetningu sem byrjunarreit. Tvær nálganir eru til þess að fá afrit af útlitinu. Hægt er að flytja fyrirliggjandi útlit út af **síðu skýrsluuppsetningar** eða sækja útlitið út frá beiðssíðu skýrslunnar. Báðar leiðir sækja Excel layout-Útlitshönnun sem nær yfir öll þau blöð sem í skránni eru. Mismunurinn er þegar hann er sóttur úr beiðssíðunni, útlitið inniheldur raunveruleg gögn. (Gögnin eru ekki nauðsynleg en það hjálpar til þegar útlitið er hannað.)

#### <a name="approach-1-export-the-layout-from-the-report-layouts-page"></a>Nálgun 1: flytja útlitið út frá **síðu skýrsluuppsetningar**

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Velja Excel-útlit af listanum og velja **síðan aðgerðina Flytja út útlit** efst á síðunni.
3. Opnaðu skrána í Excel, gerðu breytingarnar og geymdu síðan skrána.

#### <a name="approach-2-download-the-layout-from-the-reports-request-page"></a>Nálgunarbanni 2: Sækja skal um skipulag frá beiðssíðu skýrslunnar

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. **Á síðunni skipulag uppsetningar** er hægt að velja hvaða uppsetningu fyrir skýrsluna og velja **síðan aðgerðina keyra skýrslu**.
3. Á beiðsíðu skýrslunnar er valið **niðurhal**.
4. Opnaðu skrána í Excel, gerðu breytingarnar og geymdu síðan skrána.

### <a name="from-al-code"></a>[Frá AL-kóða](#tab/from-code)

Þetta er ítarlegasta aðferðin til að búa til skýrsluútlit í Excel. Þar sem hún krefst þekkingar á AL-kóða er hún miðuð hjá forritarar. Í þessari nálgun er Excel-útlit hluti af framlengingarpakkanum sem þú setur upp. Eisini meira at [Búa til skýrslu](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout) um Excel-útlit í Hönnuðinum og það Pro Help.

---

## <a name="task-2-add-the-excel-layout-to-the-report"></a>Verkefni 2: Bættu Excel-útlitinu við skýrsluna

Þegar Excel-útlitskráin er komin af er næsta verkefni að bæta henni við sem nýtt útlit fyrir skýrsluna.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Velja **nýtt útlit**.
3. Setja **Kenni** skýrslu yfir í *skýrslu*.
4. Færið inn nafn í **Heiti** útlits.
5. Stilla **Sniðkosti** í **Excel**.
6. Veldu **OK** > **Veldu** til að opna skrárexplorer í tækinu.
7. Finna og velja Excel-skrána og velja **síðan opna**.

   Skráin sem var valin er hlaðið upp í útliti og síðan er Uppsetning á **Skýrsluskipan** opnuð.
8. Til að sjá hvernig skýrslan lítur út í nýja útlitinu skal velja útlitið af listanum og velja **síðan Keyra skýrslu**.

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

## <a name="understanding-excel-layouts"></a>Skilningur á Excel-skipan

Það eru nokkrir hlutir sem þú þarft að vita eða íhuga þegar verið er að stofna eða gera breytingar á Excel útliti. Hvert Excel-útlit verður að fela í sér tvo þætti: **gagnatöflu** og **Gagnaöflun**. Þessum þáttum út frá grunni útlits með því að skilgreina viðskipagögn frá Viðskiptamiðinu sem hægt er að vinna með. Hægt er að hugsa **sér gagnablað** sem nokkurs konar samning milli útlits og viðskipagagna. Þessi gögn eru notuð sem Uppruni útreikninganna og birtinga sem óskað er að séu á öðrum blöðum.

Nokkrar sértækar kröfur eru gerðar við uppbyggingu Excel-vinnubókar. Ef kröfurnar eru ekki uppfylltar er erfitt að nota útlitið. Eftirfarandi skýringarmynd og tafla lýsir einingum Excel-útlits og-þarfa.

[![Sýnir mismunandi einingar Excel-útlits.](media/excel-layout-callouts-2.png)](media/excel-layout-callouts-2.png#lightbox)

|Nr.|Atriði|Lýsing|Áskilið|
|---|-------|----|---|
|1|**Gagnablað**|<ul><li>Verður að hafa **nafngögn**.</li><li>Getur aðeins innihaldið eina töflu sem þarf að nefna **gögn**.</li></ul>|![Er skylda](media/check.png) | 
|2|**Gagnatöflu**|<ul><li>Verður að hafa **nafngögn**.</li><li>Verður að vera a.m.k. einn dálkur.</li><li>Getur aðeins innihaldið dálka sem eru í skýrslunni DataSet.</li><li>Verður að byrja í fyrsta frumreit **a1** á **gagnablaðinu**.</li></ul>|![Er skylda](media/check.png)|
|3|Kynningarblöð|<ul><li>Notað til að kynna gögn.</li><li>Gögn koma frá **gagnablaðinu**. </li></ul>||
|4|**Blað skýrslulýsigagna**|<ul><li>Sjálfkrafa innifalin ef útlitið var búið til með því að flytja aðra Excel-skýrslu út.</li><li>Inniheldur almennar upplýsingar um skýrsluna.</li><li>Má eyða.</li></ul>|

Í samantekt er þetta það sem þú ættir og ættir ekki að gera á **gagnablaðinu**:

- Ekki breyta heiti **gagnablaðunar**, **gagnaöflunar** eða dálka.
- Hægt er að eyða eða fela dálka.
- Ekki bæta við neinum dálkum nema það sé tekið með í skýrsluna DataSet.
- Hægt er að setja blöð í hvaða röð sem er, með **gagnablaðinu** fyrst eða síðast.

## <a name="see-related-microsoft-training"></a>Sjá tengda [Microsoft-þjálfun](/training/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Sjá einnig .

[Stjórnun skýrsluútlita](ui-manage-report-layouts.md)  
[Breyta núverandi skýrsluútliti](ui-how-change-layout-currently-used-report.md)  
[Flytja inn og út sérsniðið skýrsluútlit eða skjalaútlit](ui-how-import-and-export-report-layout.md)  
[Unnið með skýrslur, runuvinnslur og XMLports](ui-work-report.md)  
[Undirbúa fjárhagsskýrslugerð með fjárhagslegum gögnum og lykilflokkum](bi-how-work-account-schedule.md)  
[Viðskiptaupplýsingar](bi.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Greining á skýrslugögnum með Excel](report-analyze-excel.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
