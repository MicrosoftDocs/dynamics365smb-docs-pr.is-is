---
title: "Hvernig á að færa inn gögn í reiti | Microsoft Docs"
description: "Það eru margar grunnaðgerðir sem auðvelda og flýta fyrir gagnainnfærslu. Öllum grunnaðgerðum við gagnainnslátt er lýst í þessu efnisatriði."
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 5f95efb5cad24db9848752035172bc7bb76db716
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="entering-data"></a>Gagnainnfærsla
Það eru margar grunnaðgerðir sem auðvelda og flýta fyrir gagnainnfærslu. Öllum grunnaðgerðum við gagnainnslátt er lýst í þessu efnisatriði.  

Í dæmunum í þessu efnisatriði er notast við sýnigögn.

## <a name="mandatory-fields"></a>Áskildir reitir
Þegar þú slærð inn gögn á síðum, eru tilteknir reitir merktir með rauðri stjörnu. Rauða stjarnan merkir að fylla verður reitinn út til að ljúka tilteknu ferli sem notar reitinn, eins og að bóka færslu sem notar gildið í reitnum.  

Jafnvel þótt reiturinn innihaldi rauða stjörnu er ekki nauðsynlegt að fylla út í reitinn áður en haldið er áfram í aðra reiti eða síðunni lokað. Rauða stjarnan er eingöngu áminning um að þú verðir útilokaður frá tilteknu ferli.  


## <a name="finding-data-as-you-type"></a>Finna gögn um leið og ritað er  
 Þegar byrjað er að slá inn stafi í reit birtist fellilisti með mögulegum gildum. Listinn breytist eftir því sem fleiri stafir eru slegnir inn og hægt er að velja rétt gildi þegar það birtist.  

 Margir af reitunum eru með örvahnapp niður sem hægt er að velja. Örin er valin til að fá lista yfir gögn sem tiltæk eru til að færa inn í reitinn. Hnappurinn hefur tvær aðgerðir, eftir því hver tegund reitsins er:  

-   Uppfletting - Birtir upplýsingar úr annarri töflu sem færa má inn í reitinn. Hægt er að velja eina gagnaeiningu í einu.  

-   Fellival - Birtir safn valkosta sem í boði eru fyrir reitinn. Aðeins er hægt að velja einn kost.  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards in the **Items** window, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a>Magn slegið inn eftir útreikningum  
 Þegar tölur eru færðar inn í magnreiti, svo sem reitinn **Magn** í birgðabókarlínu, er hægt að færa inn reikniregluna í stað heiltölumagns.  

## <a name="examples"></a>Dæmi  

-   Ef tölurnar 19+19 eru slegnar inn er niðurstaðan í reitnum 38.  

-   Ef tölurnar 41-9 eru slegnar inn er niðurstaðan í reitnum 32.  

-   Ef tölurnar 12*4 eru slegnar inn er niðurstaðan í reitnum 48.  

-   Ef tölurnar 12/4 eru slegnar inn er niðurstaðan í reitnum 3.  

# <a name="entering-negative-numbers"></a>Neikvæðar tölur er færðar inn
Hægt er að færa inn neikvæðar tölur eftir tveimur leiðum. Númerið -20.5 má færa inn sem:  

- -20.5  

  Eða
- 20.5-  

  Í báðum tilfellum verður upphæðin skráð í  sem -20.5.  

  Ef síðasti stafur segðarinnar er **+** eða **-**, mun öll segðin verða skráð með því formerki. Dæmi: **10-20+** mun gefa niðurstöðuna 10 en ekki -10.  

## <a name="entering-dates-and-times"></a>Dagsetning og tími færð inn
Færa má inn dagsetningar og tíma í alla þá reiti sem ætlaðir eru fyrir dagsetningar (dagsetningarreitir). Hægt er að færa inn dagsetningar með eða án skiltákna.

> [!NOTE]  
> Hvernig skal Færa inn dagsetningu og tíma fer eftir **Svæði** stillingunum þínum. Frekari upplýsingar, sjá [Breyta grunnstillingum](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Dagsetningar færðar inn  
 Í dagsetningarreit má færa inn tvær, fjórar, sex eða átta tölur:  

- Ef aðeins tvær tölur eru færðar inn þá túlkar kerfið þær sem daginn og bætir við mánuði og ári vinnudagsetningar.  

- Ef færðar eru inn fjórar tölur þá túlkar kerfið þær sem daginn og mánuðinn og bætir við ári vinnudagsetningar.  

- Ef sú dagsetning sem færa á inn er á bilinu 01/01/1930 til 31/12/2029 má færa árið inn í tveimur tölum; annars skal færa árið inn með fjórum tölum.  

  Einnig er hægt að færa inn dagsetningu sem vikudag ásamt vikunúmeri og hugsanlega ári (til dæmis Mán25 eða mán25 þýðir mánudagur í 25. viku).  

  Hægt er að færa inn einn af tveimur kóðum í stað sérstakrar dagsetningar.  

|Kóði|Niðurstaða|  
|--------------|----------------|  
|t|Þetta er dagurinn í dag (kerfisdagsetning tölvunnar).|  
|v|Þetta er vinnudagurinn sem er settur upp í forritinu. Vinnudagsetningunni breytt úr valmyndinni [Breyta grunnstillingum](ui-change-basic-settings.md) Handhægt gæti verið að nota vinnudagsetningar ef verið er að nota margar færslur með aðra dagsetningu en dagsins í dag.|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

## <a name="entering-times"></a>Tími færður inn  
 Þegar tímasetningar eru ritaðar er hægt að setja inn hvaða skiltákn sem er milli eininga en það er ekki nauðsynlegt. Ekki þarf að tilgreina mínútur, sekúndur eða FH/EH.  

 Í eftirfarandi töflu birtast mismunandi leiðir til að færa inn tímasetningar og hvernig þær eru túlkaðar:  

|Færsla|Túlkun|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30|05:30:00|  
|0530|05:30:00|  
|5:30:5|05:30:05|  
|053005|05:30:05|  
|5:30:5,50|05:30:05,5|  
|053005050|05:30:05.05|  

 Rita þarf tvær tölur fyrir hverja tímaeiningu ef skiltákn er ekki notað.  

## <a name="entering-datetimes"></a>Dagsetning og tímasetning færð inn  
 Þegar dagsetning og tími eru færð inn verður að vera bil milli dags og tímasetningar.  

 Í eftirfarandi töflu birtast mismunandi leiðir til að færa inn dagsetningar og tímasetningar og hvernig þær eru túlkaðar:  

|Færsla|Túlkun|  
|---------------|------------------------|  
|131202 132455|13-12-02 13:24:55|  
|1-12-02 10|01-12-02 10:00:00|  
|1.12.02 5|01-12-02 05:00:00|  
|1.12.02|01-12-02 00:00:00|  
|11 12|11-gildandi mánuður-gildandi ár 12:00:00|  
|1112 12|11-12-gildandi ár 12:00:00|  
|d eða dagurinn í dag|dagurinn í dag 00:00:00|  
|t tími|gildandi tími dagsins í dag|  
|d 10:30|dagurinn í dag 10:30:00|  
|d 03:03:03|dagurinn í dag 03:03:03|  
|v eða vinnudagsetningin|vinnudagsetningin 00:00:00|  
|m eða mánudagur|Mánudagur yfirstandandi viku 00:00:00|  
|þr eða þriðjudagur|Þriðjudagur yfirstandandi viku 00:00:00|  
|mi eða miðvikudagur|Miðvikudagur yfirstandandi viku 00:00:00|  
|fi eða fimmtudagur|Fimmtudagur yfirstandandi viku 00:00:00|  
|f eða föstudagur|Föstudagur yfirstandandi viku 00:00:00|  
|l eða laugardagur|Laugardagur yfirstandandi viku 00:00:00|  
|s eða sunnudagur|Sunnudagur yfirstandandi viku 00:00:00|  
|þr 10:30:00|Þriðjudagur yfirstandandi viku 10:30:00|  
|þr 03:03:03|Þriðjudagur yfirstandandi viku 03:03:03|  

## <a name="entering-duration"></a>Færið inn tímalengd  
 Hægt er að færa inn tímalengd sem tölu og mælieiningu.  

 Hér eru nokkur dæmi.  

|Lengd|Mælieining**|  
|------------------|-------------------------|  
|2t|2 klst|  
|6t 30 m|6 klst 30 mín|  
|6,5t|6 klst 30 mín|  
|90m|1 klst 30 mín|  
|2d 6t 30m|2 dagar 6 klst 30 mín|  
|2d 6t 30m 56s 600ms|2 dagar 6 klst 30 mín 56 sek 600 millis|  

 Einnig er hægt að færa inn tölu og þá er henni sjálfkrafa breytt í tímalengd. Tölunni sem færð er inn er breytt samkvæmt sjálfgefnu mælieiningunni sem hefur verið tilgreind fyrir reitinn tímalengd.  

 Hægt er að sjá hvaða mælieining er notuð í reitnum tímalengd með því að færa inn tölu og sjá í hvaða mælieiningu kerfið færir hana í.  

 Tölunni 5 er breytt í 5 klst. ef mælieiningin er klukkustundir.  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a>Notkun dagsetningarreiknireglna  
 Dagsetningarregla er stutt, skammstöfuð samsetning stafa og tölustafa sem tilgreinir hvernig skal reikna út dagsetningar. Hægt er að færa dagsetningarreiknireglur í ólíka dagsetningarreiknireiti og í ítrekunartíðnireiti í ítrekunarbókum.  

> [!NOTE]  
>  Dagurinn í dag, fyrir upphaf tímabilsins, er með í öllum reitum fyrir reiknireglur dagsetninga. Í samræmi við það, ef fært er inn 1V, til dæmis, er tímabilið í raun átta dagar þar sem dagurinn í dag er tekinn með. Til að tilgreina sjö daga tímabil (ein raunvika) að meðtalinni upphafsdagsetningu tímabilsins þarf að færa inn 6D eða 1W-1D.  

 Hér eru nokkur dæmi um hvernig nota má dagsetningarreiknireglur:  

- Dagsetningarreikniregla í ítrekunartíðnireitnum í ítrekunarbókum ákvarðar hversu oft færsla í færslubókarlínu er bókuð.  

- Dagsetningarreikniregla í reitnum Biðtími fyrir tiltekið innheimtustig ákvarðar það tímabil sem þarf að líða frá gjalddaga (eða frá dagsetningu fyrri innheimtubréfs) áður en innheimtubréf er búið til.  

- Dagsetningarreikniregla í reitnum Gjalddagaútreikningur ákvarðar hvernig kerfið reiknar gjalddaga á innheimtubréfinu.  

  Dagsetningarreikniregla getur mest haft 20 stafi, bæði tölu- og bókstafi. Hægt er að nota eftirfarandi stafi sem skammstafanir fyrir tiltekinn tíma.  

|||  
|-|-|  
|C|Gildandi|  
|D|Dagar|  
|W|Vikur|  
|M|Mánuðir|  
|F|Fjórðungar|  
|Á|Ár|  

 Hægt er að rita dagsetningarreiknireglu á þrjá vegu.  

 Eftirfarandi dæmi sýnir hvernig núverandi og tímaeining.  

|||  
|-|-|  
|LV|Líðandi vika|  
|LM|Líðandi mánuður|  

 Eftirfarandi dæmi sýnir hvernig tala og tímaeining. Talan getur ekki verið hærri en 9999.  

|||  
|-|-|  
|10D|10 dögum eftir daginn í dag|  
|2V|2 vikum eftir daginn í dag|  

 Eftirfarandi dæmi sýnir hvernig tímaeining og tala.  

|||  
|-|-|  
|D10|Næsti 10. dagur mánaðar|  
|VD4|Næsti 4. dagur viku (fimmtudagur)|  

 Eftirfarandi dæmi sýnir hvernig eigi að samræma þessi þrjú eyðublöð eins og þörf er á.  

|||  
|-|-|  
|LM+10D|Líðandi mánuður + 10 dagar|  

 Eftirfarandi dæmi sýnir hvernig hægt er að nota mínustákn til að sýna gamla dagsetningu.  

|||  
|-|-|  
|-1Á|1 ári fyrir daginn í dag|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a>Sjá einnig  
 [Leita í, afmarka og raða gögnum](ui-enter-criteria-filters.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

