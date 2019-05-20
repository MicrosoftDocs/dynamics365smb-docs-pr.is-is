---
title: Hvernig á að færa inn gögn í reiti | Microsoft Docs
description: Kynntu þér almenna eiginleika sem auðvelda þér að færa gögn inn í reiti.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 00143454cf0b0da9b111f92bcdb7879c7e6743d2
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252459"
---
# <a name="entering-data"></a>Gagnainnfærsla

Margir almennir eiginleikar auðvelda þér að færa inn gögn með fljótlegri hætti og af meiri nákvæmni. Almennum eiginleikum við innslátt á gögnum er lýst í þessu efnisatriði.  

<!-- The examples in this article use the demonstration data.-->

## <a name="keyboard-shortcuts"></a>Flýtivísanir

Nokkrir flýtilyklar gera þér kleift að vinna án músar og hraða gagnaskráningu þinni, sérstaklega mikið magn af færslum og endurteknum innsláttarverkum.

Frekari upplýsingar er að finna í [Flýtilyklar á lyklaborði](keyboard-shortcuts.md). Fjallað er um nokkrar af þessum flýtileiðum í þessu efnisatriði.

## <a name="QuickEntry"></a>Hraða gagnaskráningu með flýtifærslu

Flýtifærsla er eiginleiki sem er hannaður fyrir gagnaskráningu þegar lyklaborð er notað. Flýtifærsla virkar á reiti (t.d. í spjaldsíðum) og í listum (röðum og dálkum). Það er gagnlegt þegar framkvæmd eru endurtekin innsláttarverk sem krefjast þess að búnar séu til margar færslur í röð, t.d. runa af sölupöntunum eða skráning á nýjum vörum.

Hugsanlega kannastu við að nota Tab-lykilinn til að fara frá einum reit á síðu yfir á næsta breytanlega reit. Ókostur við að nota Tab er að hann fer alltaf yfir á næsta reit. <!-- even if the field is non-editable or seldom filled it in.-->Flýtifærsla gerir þér kleift að breyta þessari leið. Með flýtifærslu notarðu Enter til að fara aðeins á milli þeirra reita sem þú hefur áhuga á, sleppir óbreytanlegum reitum og reitum sem þú fyllir vanalega ekki út. Þú gætir hafa tekið eftir þessari hegðun á sumum síðum. Þetta er vegna þess að forritið ákveður nú þegar hvaða reiti skuli hafa með þegar ýtt er á Enter og hvaða reitum skuli sleppt. Hægt er að sérstilla flýtifærslu með því að sérstilla vinnusvæðið þitt og fínstilla hvernig þú færir inn gögn á hverri síðu.

### <a name="how-quick-entry-works"></a>Hvernig flýtifærsla virkar

Hægt er að merkja sérhvern reit sem annaðhvort *hafa með í flýtifærslu* eða *ekki hafa með í flýtifærslu*. Reitir sem eru hafðir með í flýtifærslu verða hluti af slóðinni þegar ýtt er á Enter; reitir sem ekki eru hafðir með í flýtifærslum verða ekki hluti af henni.

Þegar þú hefur lokið við að færa gögn inn í reit ýtirðu einfaldlega á Enter til að staðfesta breytingarnar og ferð í næsta reit. Ef þú vilt snúa áttinni við og fara í fyrri reit skaltu ýta á Shift+Enter. Frekari upplýsingar um flýtileiðir er að finna í [Flýtivísanir flýtifærslu](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Ábendingar og góð ráð
Eftirfarandi veitir nokkrar gagnlegar upplýsingar um notkun á flýtifærslu.

- Hún er í boði fyrir alla breytanlega reiti.
- Hún virkar einnig fyrir bæði dálka og línur.
- Hún kemur ekki í veg fyrir aðgang að öðrum einingum á síðu, t.d. aðgerðum. Þær eru enn aðgengilegar með því að nota Tab og Shift+Tab.  
- Ekki þarf að útvíkka flýtiflipa til að flýtifærsla virki. Ef næsti reitur flýtifærslu er staðsettur í samandregnum flýtiflipa mun sá flýtiflipi sjálfkrafa stækka og setja fókus á tiltekinn reit.
- Flýtifærsla virkar óháð því hvort reitir séu áskildir. Því er góð hugmynd að ganga úr skugga um að áskildir reitir séu hluti af flýtifærslu.
- Sjálfgefið er að flestir reitir eru sjálfkrafa með í flýtifærslu. Í upphafi verður það líklega þitt verk að útiloka reiti úr flýtifærslu.

### <a name="how-to-change-quick-entry-fields"></a>Hvernig á að breyta reitum flýtifærslu

Til að breyta því hvaða reitir eru hafðir með eða ekki hafðir með í flýtifærslum á síðu, notarðu sérstillingu.

1. Byrjaðu sérstillingu með því að velja táknið ![Stillingar](media/ui-experience/settings_icon_small.png "Stillingar") og síðan **Sérstilla**.
2. Veldu reit sem þú vilt breyta, eða í listum, veldu samsvarandi dálkahaus, og veldu því næst annaðhvort **Hafa með í flýtifærslu** eða **Ekki hafa með í flýtifærslu**.

Frekari upplýsingar um sérstillingu er að finna í [Sérstillingar vinnusvæðis](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Áskildir reitir

Þegar þú slærð inn gögn á síðum, eru tilteknir reitir merktir með rauðri stjörnu. Rauða stjarnan merkir að fylla verður reitinn út til að ljúka tilteknu ferli sem notar reitinn, eins og að bóka færslu sem notar gildið í reitnum.  

Jafnvel þótt reiturinn innihaldi rauða stjörnu er ekki nauðsynlegt að fylla út í reitinn áður en haldið er áfram í aðra reiti eða síðunni lokað. Rauða stjarnan er eingöngu áminning um að þú verðir útilokaður frá tilteknu ferli.  

## <a name="finding-data-as-you-type"></a>Finna gögn um leið og ritað er

 Þegar byrjað er að slá inn stafi í reit birtist fellilisti með mögulegum gildum. Listinn breytist eftir því sem fleiri stafir eru slegnir inn og hægt er að velja rétt gildi þegar það birtist.  

 Margir af reitunum eru með örvahnapp niður sem hægt er að velja. Örin er valin til að fá lista yfir gögn sem tiltæk eru til að færa inn í reitinn. Hnappurinn hefur tvær aðgerðir, eftir því hver tegund reitsins er:  

-   Uppfletting - Birtir upplýsingar úr annarri töflu sem færa má inn í reitinn. Hægt er að velja eina gagnaeiningu í einu.  

-   Fellival - Birtir safn valkosta sem í boði eru fyrir reitinn. Aðeins er hægt að velja einn kost.  

## <a name="copying-and-pasting-fields-and-lines"></a>Afrita og líma reiti og línur

Þú getur afritað eina eða fleiri raðir úr lista eða einum reit á síðu og síðan líma það sem þú afritaðir á sömu síðu, aðra síðu eða ytri skjal (eins og Microsoft Excel og Outlook tölvupóst). Í stuttu máli, til að afrita, ýtirðu á CTRL+C (cmd+C í macOS) á lyklaborðinu þínu. Til að líma er stutt á CTRL+V (cmd+V í macOS).

Í lista, til að afrita reitinn í sama dálki og í röðinni fyrir ofan, og líma hann í núverandi röð, skal ýta á F8.

Frekari upplýsingar er að finna í [Afrita og líma í Business Central](ui-copy-paste.md).

## <a name="Focus"></a>Fókus settur á línuatriði

Þegar unnið er með skjöl sem innihalda hluta línuatriðis, t.d. síða sölupöntunar eða reiknings, geturðu skipt yfirlitinu til að setja fókus á aðeins línuatriði, svo hluti línuatriða stækkar svo hann tekur yfir næstum allt vinnusvæðið - felur aðra hluta síðunnar nema aðgerðarsvæðið efst uppi. Þetta veitir þér betri yfirsýn yfir línuatriðin og gefur meira rými til að vinna í þeim. Þetta kemur sér sérstaklega vel þegar unnið er með langan lista af línuatriðum og hröð gagnaskráning er æskileg.

Annar kostur er að það býður einnig upp á ítarlega síunarmöguleika, líkt og í hinum listunum, þannig að flettingar og leit í gegnum línuatriði verður enn auðveldari.

### <a name="switch-the-focus-on-and-off"></a>Kveikja eða slökkva á fókus

Til að setja fókus á línuatriði skal velja hvar sem er í hluta línuatriða og síðan velja ![Tákn fyrir fókusstillingu](media/focus-mode.png "Tákn fyrir fókusstillingu") efst í hægra horninu eða ýta á Ctrl+Shift+F12.

Til að skipta yfir í venjulegt yfirlit skal velja ![Tákn fyrir fókusstillingu](media/focus-mode.png "Tákn fyrir fókusstillingu") eða ýta aftur á Ctrl+Shift+F12.

### <a name="filtering-the-line-items"></a>Síun á línuatriðum

Til að byrja síun skal velja ![Tákn fyrir afmörkunarsvæði](media/open-filter-pane-icon.png "Tákn fyrir afmörkunarsvæði") efst í listanum eða ýta á **Shift+F3** til að opna afmörkunarsvæðið. Þú vinnur með afmörkunarsvæðið eins og þú gerir í öllum öðrum listum. Frekari upplýsingar er að finna í [Síun](ui-enter-criteria-filters.md#Filtering).

Síun er sérstaklega hjálpleg þegar lengri skjöl eru skoðuð og greind. Ímyndaðu þér til dæmis að þú opnaðir bókaðan sölureikning og síar línuatriðin til að birta öll línuatriði sem eru með afslætti yfir 5% eða síar til að birta aðeins reiðhjólabúnað með „pro“ í heitinu.

## <a name="entering-quantities-by-calculation"></a>Magn slegið inn eftir útreikningum

Þegar tölur eru færðar inn í magnreiti, svo sem reitinn **Magn** í birgðabókarlínu, er hægt að færa inn reikniregluna í stað heiltölumagns.  

### <a name="examples"></a>Dæmi  

-   Ef tölurnar 19+19 eru slegnar inn er niðurstaðan í reitnum 38.  

-   Ef tölurnar 41-9 eru slegnar inn er niðurstaðan í reitnum 32.  

-   Ef tölurnar 12*4 eru slegnar inn er niðurstaðan í reitnum 48.  

-   Ef tölurnar 12/4 eru slegnar inn er niðurstaðan í reitnum 3.  

## <a name="entering-negative-numbers"></a>Neikvæðar tölur er færðar inn

Hægt er að færa inn neikvæðar tölur eftir tveimur leiðum. Númerið -20.5 má færa inn sem:  

-   -20.5  

    Eða
-   20.5-  

 Í báðum tilfellum verður upphæðin skráð í sem -20.5.  

 Ef síðasti stafur segðarinnar er **+** eða **-**, mun öll segðin verða skráð með því formerki. Dæmi: **10-20+** mun gefa niðurstöðuna 10 en ekki -10.  

## <a name="entering-dates-and-times"></a>Dagsetning og tími færð inn

Færa má inn dagsetningar og tíma í alla þá reiti sem ætlaðir eru fyrir dagsetningar (dagsetningarreitir). Hægt er að færa inn dagsetningar með eða án skiltákna.

> [!NOTE]  
> Hvernig skal Færa inn dagsetningu og tíma fer eftir **Svæði** stillingunum þínum. Frekari upplýsingar, sjá [Breyta grunnstillingum](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Dagsetningar færðar inn

Fyrir dagsetningareiti er annaðhvort hægt að nota dagsetningaval, sem gerir þér kleift að velja dagsetningu úr dagatali, eða hægt er að færa inn dagsetningar handvirkt. Þessi hluti veitir stutt yfirlit yfir hvernig skuli slá inn dagsetningar. Frekari upplýsingar er að finna í [Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md).

Fyrir handvirka færslu á dagsetningu er hægt að færa inn tvær, fjórar, sex eða átta tölur:  

-   Ef aðeins tvær tölur eru færðar inn þá túlkar kerfið þær sem daginn og bætir við mánuði og ári vinnudagsetningar.  

-   Ef færðar eru inn fjórar tölur þá túlkar kerfið þær sem daginn og mánuðinn og bætir við ári vinnudagsetningar.  

-   Ef sú dagsetning sem færa á inn er á bilinu 01/01/1930 til 31/12/2029 má færa árið inn í tveimur tölum; annars skal færa árið inn með fjórum tölum.  

Einnig er hægt að færa inn dagsetningu sem vikudag ásamt vikunúmeri og hugsanlega ári (til dæmis Mán25 eða mán25 þýðir mánudagur í 25. viku).  

Hægt er að færa inn einn af þessum kóðum í stað sérstakrar dagsetningar.  

|Kóti|Niðurstaða|  
|--------------|----------------|  
|d|Þetta tilgreinir daginn í dag (kerfisdagsetning tölvunnar).|  
|e|Þetta tilgreinir reikningstímabil þar sem `p`þýðir fyrsta reikningstímabilið, `p2` þýðir annað reikningstímabilið og svo framvegis. |
|v|Þetta tilgreinir vinnudagsetninguna sem er uppsett í forritinu. Vinnudagsetningunni breytt úr valmyndinni [Breyta grunnstillingum](ui-change-basic-settings.md) Handhægt gæti verið að nota vinnudagsetningar ef verið er að nota margar færslur með aðra dagsetningu en dagsins í dag.|
|c|Þetta tilgreinir að dagsetningin eftir `c`er lokunardagsetning, t.d. `C123101`.|  

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
|5:30:5,50|05:30:05.5|  
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
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|

## Using Date Formulas

 A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.  

> [!NOTE]  
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.  

 Here are some examples of how date formulas can be used:  

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.  

-   The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.  

-   The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.  

 The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.  

|||  
|-|-|  
|C|Current|  
|D|Day(s)|  
|W|Week(s)|  
|M|Month(s)|  
|Q|Quarter(s)|  
|Y|Year(s)|  

 You can construct a date formula in three ways.  

 The following example shows how current plus a time unit.  

|||  
|-|-|  
|CW|Current week|  
|CM|Current month|  

 The following example shows how a number and a time unit. A number cannot be larger than 9999.  

|||  
|-|-|  
|10D|10 days from today|  
|2W|2 weeks from today|  

 The following example shows how a time unit and a number.  

|||  
|-|-|  
|D10|The next 10th day of a month|  
|WD4|The next 4th day of a week (Thursday)|  

 The following example shows how you can combine these three forms as needed.  

|||  
|-|-|  
|CM+10D|Current month + 10 days|  

 The following example shows how you can use a minus sign to indicate a date in the past.  

|||  
|-|-|  
|-1Y|1 year ago from today|

[!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->

## <a name="see-also"></a>Sjá einnig  
 [Röðun, leit og síun í listum](ui-enter-criteria-filters.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
