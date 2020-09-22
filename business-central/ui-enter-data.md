---
title: Hvernig á að færa inn gögn í Business Central| Microsoft Docs
description: Kynntu þér almenna eiginleika sem auðvelda þér að færa gögn inn í reiti.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/03/2020
ms.author: edupont
ms.openlocfilehash: 1ad2eb6d2e9a423aa1891eb52f71e815f4b89eff
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785447"
---
# <a name="entering-data"></a>Gagnainnfærsla

Margir almennir eiginleikar auðvelda þér að færa inn gögn með fljótlegri hætti og af meiri nákvæmni. Helstu meginreglum og ítarlegum eiginleikum fyrir innslátt gagna er lýst í þessari grein.  

Í dæmunum í þessu efnisatriði er notast við sýnigögn.

## <a name="working-with-editable-fields"></a>Unnið með breytanlegum reitum
Reitirnir í [!INCLUDE[d365fin](includes/d365fin_md.md)] gætu innihaldið mismunandi breytanleg gögn, eins og texta eða gjaldmiðilsupphæðir. Breytanlegir reitir sýna yfirleitt innsláttarreit þar sem hægt er að slá inn gildi eða velja það. Óbreytanlegir reitir birtast yfirleitt með gráum bakgrunni.   

Sumir breytanlegir reitir bjóða upp á val til að auðvelda þér að tilgreina gildi.  

<!-- TODO: Add illustrations or images of each picker -->
|**Tínslumaður**        |**Hvernig það hjálpar að tilgreina gildi.**|
|------------------|------------------------------------|
|Dagsetningarval       |Þetta val birtir dagatal sem byggir á virkum svæðisstillingum. Það hjálpar þér að velja staka dagsetningu.|
|Fellilisti          |Fellilistar gefa þér kost á föstum gildum eða tilvísunarfærslum úr annarri töflu|
|Rofi eða gátreitur|Sumir reitir bjóða upp á einfalt val, *Já* eða *Nei*. Rofinn er notaður til að tilgreina þetta gildi og birtist alltaf sem gátreitur í listum|
|Breytingahjálp       |Sumir reitir bjóða upp á sérsniðna glugga sem henta til að fletta upp og velja besta gildið fyrir viðkomandi reit, eins og sprettigluggi|


### <a name="modifying-a-field-value"></a>Reitargildi breytt

Til að breyta gildi reits verður fyrst að velja þann reit. Þú stillir fókus með því að framkvæma eftirfarandi aðgerðir:

- Notaðu **dálkalykilinn**. Aðgerðin velur allt gildið.
- Vinstrismelltu á músinni eða svipuðu inntakstæki. Þessi aðgerð mun aðeins velja gildi reitsins í heild sinni ef reiturinn er í listanum.  

Þegar þú átt í samskiptum við reiti í notandaviðmótinu velur [!INCLUDE[d365fin](includes/d365fin_md.md)] yfirleitt allt reitargildið til að auðvelda þér að skipta út því gildi.

Þegar gildi svæðisins í heild sinni er valið:
- Skiptu um gildi með því að slá inn nýtt gildi. Ef reiturinn býður upp á val geturðu virkjað það með því að nota flýtilykilinn **Alt+ör niður**.
- Notaðu lykilinn **Delete** eða **bakklykilinn** til að hreinsa gildið.

Ýttu á **F2** til að skipta á milli þess að velja gildi reitsins í heild sinni eða setja bendilinn á eftir gildi reitsins. Ef bendillinn er settur í lok gildisins er auðveldara að bæta við gildið sem fyrir er.

Þegar bendillinn er sýndur við lok reitargildis:
- Bæta við gildið með því að slá einfaldlega inn.
- Notaðu lyklana **Home**, **End**, **vinstriör** og **hægriör** til að færa bendilinn innan gildis. Ef þú ert að breyta reit í lista skaltu ýta á **vinstriör** aftur þegar bendillinn er við upphaf gildis til að stilla áherslu á fyrri reit. Á sama hátt er fókusinn færður á næsta reit þegar ýtt er á **hægriör** aftur þegar bendillinn er við endann á gildinu.

> [!NOTE]
> Eftir að þú hefur tilgreint gildi mun Business Central aðeins athuga að það sé gilt eftir að þú smellir utan reitsins eða stillir áhersluna á aðra einingu, eins og á næsta reit.  


## <a name="keyboard-shortcuts"></a>Flýtivísanir

Nokkrir flýtilyklar gera þér kleift að vinna án músar og flýta fyrir skráningu gagna. Þessir flýtilyklar eru sérstaklega gagnlegir fyrir margar færslur og endurtekin innsláttarverk.

Frekari upplýsingar er að finna í [Flýtilyklar á lyklaborði](keyboard-shortcuts.md). Í þessari grein er fjallað um nokkra af flýtilyklunum.

## <a name="accelerating-data-entry-using-quick-entry"></a><a name="QuickEntry"></a>Hraða gagnaskráningu með flýtifærslu

Flýtifærsla er eiginleiki sem er hannaður fyrir gagnaskráningu þegar lyklaborð er notað. Flýtifærsla virkar á reiti (t.d. í spjaldsíðum) og í listum (röðum og dálkum). Það er gagnlegt þegar verið er að framkvæma endurtekin innsláttarverk sem krefjast þess að stofnaðar séu margar færslur í röðinni. Dæmi eru sölupantanakeyrsla eða skráning nýrra vara.

Hægt er að nota dálkalykilinn til að fletta úr einum reit á síðu yfir í næsta breytanlega reit. Ókostur við að nota Tab er að hann fer alltaf yfir á næsta reit. <!-- even if the field is non-editable or seldom filled it in.-->Flýtifærsla gerir þér kleift að breyta þessari leið. Með flýtifærslu geturðu notað færslulykilinn til að fara í gegnum aðeins þá reiti sem þú hefur áhuga á. Flýtifærsla sleppir skrifvörðum reitum og reitum sem þú fyllir yfirleitt ekki út. Þú gætir hafa tekið eftir þessari hegðun á sumum síðum. Þessi hegðun er vegna þess að reitirnir sem eiga að fylgja með þegar ýtt er á færslulykilinn og þeir sem á að sleppa hafa verið forskilgreindir. Hægt er að sérstilla flýtifærslu með því að sérstilla vinnusvæðið þitt og fínstilla hvernig þú færir inn gögn á hverri síðu.

### <a name="how-quick-entry-works"></a>Hvernig flýtifærsla virkar

Hægt er að merkja sérhvern reit sem annaðhvort *hafa með í flýtifærslu* eða *ekki hafa með í flýtifærslu*. Reitir sem eru með flýtifærslu verða hafðir í slóðinni þegar ýtt er á færslulykilinn. Reitir sem eru undanskildir flýtifærslu verða það ekki.

Þegar þú hefur lokið við að færa gögn inn í reit ýtirðu einfaldlega á Enter til að staðfesta breytingarnar og ferð í næsta reit. Ef þú vilt snúa áttinni við og fara í fyrri reit skaltu ýta á Shift+Enter. Frekari upplýsingar um flýtileiðir er að finna í [Flýtileiðir flýtifærslu fyrir reiti](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Ábendingar og góð ráð

Eftirfarandi listi veitir gagnlegar upplýsingar um notkun á flýtifærslu.

- Hann er í boði fyrir alla breytanlega reiti.
- Hún virkar einnig fyrir bæði dálka og línur.
- Hann kemur ekki í veg fyrir aðgang annarra að öðrum einingum á síðu, svo sem aðgerðum. Þessar einingar eru enn aðgengilegar með því að nota dálkalykil og Shift+dálkalykil.  
- Ekki þarf að víkka flýtiflipa til að Snögg færsla virki. Ef næsti reitur flýtifærslu er staðsettur í samandregnum flýtiflipa mun sá flýtiflipi sjálfkrafa stækka og setja fókus á tiltekinn reit. [!INCLUDE[d365fin](includes/d365fin_md.md)] man að flýtiflipinn ætti að víkka næst þegar þú opnar síðuna.  
- Flýtifærsla virkar hvort sem reitir eru áskildir eða ekki. Því er góð hugmynd að tryggja að áskilin svæði séu höfð með í flýtiskráningu.
- Sjálfgefið er að flestir reitir eru sjálfkrafa með í flýtifærslu. Í upphafi verður það líklega þitt verk að útiloka reiti úr flýtifærslu.

### <a name="to-change-quick-entry-fields"></a>Til að breyta reitum flýtifærslu

Til að setja upp flýtifærslu á reitum skaltu nota sérstillingu.

1. Byrjaðu sérstillingu með því að velja táknið ![Stillingar](media/ui-experience/settings_icon_small.png "Stillingatákn fyrir hlutverkamiðstöð") og síðan aðgerðina **Sérstilla**.
2. Veldu reit sem þú vilt breyta. Í listum skaltu velja samsvarandi dálkahaus. Veldu síðan annaðhvort **Hafa með í flýtifærslu** eða **Útiloka frá flýtifærslu**.

Frekari upplýsingar um sérstillingu er að finna í [Sérstilling verksvæðis](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Áskildir reitir

Þegar þú slærð inn gögn á síðum, eru tilteknir reitir merktir með rauðri stjörnu. Rauða stjarnan merkir að fylla verður reitinn út til að ljúka tilteknu ferli sem notar reitinn. Dæmi um þetta er bókun færslu sem notar gildið í reitnum.  

Þótt reitur sé áskilinn er ekki nauðsynlegt að fylla hann út áður en farið er áfram í aðra reiti eða síðunni er lokað. Rauða stjarnan er eingöngu áminning um að þú verðir útilokuð/útilokaður frá tilteknu ferli.  

## <a name="finding-data-as-you-type"></a>Finna gögn um leið og ritað er

 Þegar byrjað er að slá inn stafi í reit birtist fellilisti með mögulegum gildum. Listinn breytist eftir því sem fleiri stafir eru slegnir inn og hægt er að velja rétt gildi þegar það birtist.  

 Margir af reitunum eru með örvahnapp niður sem hægt er að velja. Örin er valin til að fá lista yfir gögn sem tiltæk eru til að færa inn í reitinn. Hnappurinn hefur tvær aðgerðir, eftir því hver tegund reitsins er:  

-   Uppfletting - Birtir upplýsingar úr annarri töflu sem færa má inn í reitinn. Hægt er að velja eina gagnaeiningu í einu.  

-   Fellival - Birtir safn valkosta sem í boði eru fyrir reitinn. Aðeins er hægt að velja einn kost.  

## <a name="copying-and-pasting-faq-fields-and-lines"></a>Afrita og líma reiti og línur

Hægt er að afrita eina eða fleiri línur af listanum eða staka reiti á síðu. Límdu svo það sem þú afritaðir á sömu síðu, aðra síðu eða ytra skjal. Þú gætir til dæmis límt í Microsoft Excel eða Outlook-tölvupóst. Í stuttu máli, til að afrita er ýtt á CTRL+C (cmd+C í macOS) á lyklaborðinu þínu. Ýttu á CTRL + V eða cmd + V í macOS til að líma.

Í lista, til að afrita reitinn í sama dálki og í röðinni fyrir ofan, og líma hann í núverandi röð, skal ýta á F8.

Frekari upplýsingar er að finna í [Afrita og líma algengar spurningar](ui-copy-paste.md).

## <a name="filtering-line-items"></a>Síun á línuatriðum

Til að byrja síun skal velja ![Tákn fyrir afmörkunarsvæði](media/open-filter-pane-icon.png "Afmörkunarsvæðistákn") efst á listanum eða ýta á Shift+F3 til að opna afmörkunarsvæðið. Þú vinnur með afmörkunarsvæðið eins og þú gerir í öllum öðrum listum. Frekari upplýsingar er að finna í [Síun](ui-enter-criteria-filters.md#filtering).

Síun er sérstaklega hjálpleg þegar lengri skjöl eru skoðuð og greind. Ímyndaðu þér að þú opnir bókaðan sölureikning. Síðan eru línuatriði síuð til að birta öll línuatriði sem eru með einstakan afslátt yfir 5%. Einnig er hægt að sía til að sýna eingöngu fylgihluti reiðhjóls með „pro“ í heitinu.

## <a name="focusing-on-line-items"></a><a name="Focus"></a>Fókus settur á línuatriði

Þegar unnið er á skjölum sem innihalda vörulínuhluta reikningssíðu, er hægt að skipta yfirlitinu til að einbeita sér eingöngu að vörulínunum. Dæmaskjöl eru sölupöntun eða reikningssíða. Línuatriðahlutinn stækkar þannig að hann nær yfir nánast allt vinnusvæðið. Það felur aðra hluta síðunnar fyrir utan aðgerðasvæðið efst. Þetta veitir þér betri yfirsýn yfir línuatriðin og gefur meira rými til að vinna í þeim.

Þú hefur gagn af því sérstaklega þegar þú vinnur með stórum línuatriðinu og þú vilt færa gögnin hratt inn. Þessi eiginleiki býður einnig upp á ítarlega síugetu. Eins og á öðrum listum verður vefskoðun og leit í gegnum línuatriði enn auðveldari.

### <a name="switching-the-focus-on-and-off"></a>Kveikja eða slökkva á fókus

Til að setja fókus á línuatriði skal velja hvar sem er í hluta línuatriða og síðan velja ![Tákn fyrir fókusstillingu](media/focus-mode.png "Fókusstillingartákn") efst í hægra horninu eða ýta á Ctrl+Shift+F12.

Til að skipta yfir í venjulegt yfirlit skal velja ![Tákn fyrir fókusstillingu](media/focus-mode.png "Fókusstillingartákn") eða ýta aftur á Ctrl+Shift+F12.

## <a name="multitasking-across-multiple-pages"></a>Fjölvinnsla þvert á margar síður

Þú getur opnað spjald eða síðu skjals í nýjum glugga. Með því að opna nýjan glugga geturðu:

- Unnið að mörgum verkum á sama tíma
- Stjórnað rofi á yfirstandandi verki, eins og að svara símtali.
- Haltu glugga opnum í yfirstandandi verki á meðan þú ræsir eða lýkur öðru verki í gluggum.

Til að opna núverandi spjald eða skjal í nýjum glugga skal velja táknið ![Opna nýjan glugga](media/open-new-window-icon.png "Táknið „Opna nýjan glugga“") efst í hægra horninu eða ýta á Alt+Shift+W.

<!--
When working on multiple tasks at a time or when managing interruptions to the current task, such as taking an incoming call, you can open a card or document page in a new window. This allows you to keep a window open for an ongoing task while you start or complete another task in one or more other windows.
-->
Til að opna núverandi spjald eða skjal í nýjum glugga skal velja táknið ![Opna nýjan glugga](media/open-new-window-icon.png "Táknið „Opna nýjan glugga“") efst í hægra horninu eða ýta á Alt+Shift+W.

> [!NOTE]
> Þegar opnaðar eru aðrar síður úr spjaldi eða skjali sem opnað er í nýjum glugga opnast þessar síður í nýjum glugga, þó að ekki sé valið ![Opna nýjan glugga](media/open-new-window-icon.png "Táknið „Opna nýjan glugga“").

> [!NOTE]
> Ef unnið er í Safari-vafranum gæti sprettigluggavörn valdið því að nýi glugginn opnist ekki. Ef þetta er tilfellið skal tilgreina vefslóð afurðarinnar sem heimilaða vefsvæði. Frekari upplýsingar er að finna í [Breyta sérstillingum í Safari](https://go.microsoft.com/fwlink/?LinkId=2102965).<br /><br />
> Sama kann að gerast í öðrum vöfrum, svo sem Firefox. Frekari upplýsingar er að finna í [Stillingar sprettigluggavarnar í Firefox](https://go.microsoft.com/fwlink/?LinkId=2116400).  

Önnur leið til að gera margt í einu er að opna [!INCLUDE[d365fin](includes/d365fin_md.md)] í tveimur eða fleiri vafragluggum. Þegar þetta er gert ætti að búa til nýjan flipa og síðan afrita/líma vefslóð upprunalega flipans í nýja flipann. Þetta býr til nýja lotu.   

> [!NOTE]
> Ekki skal nota aðgerðina **Tvítekning** í vafranum til að búa til nýjan flipa því að það getur leitt til þess að aðgerðir í einum flipa útiloki aðgerðir í öðrum flipa vegna þess að þeir tilheyra sömu lotunni.

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
> Hvernig skal Færa inn dagsetningu og tíma fer eftir **Svæði** stillingunum þínum. Frekari upplýsingar eru í [Breyta grundvallarstillingum](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Dagsetningar færðar inn

Þú getur annaðhvort notað gagnaval til að velja dagsetningu úr dagbók eða fært inn dagsetningar handvirkt. Þessi hluti veitir stutt yfirlit yfir hvernig skuli slá inn dagsetningar. Frekari upplýsingar er að finna í [Vinna með dagsetningar og tíma í dagatali](ui-enter-date-ranges.md).

Fyrir handvirka færslu á dagsetningu er hægt að færa inn tvær, fjórar, sex eða átta tölur:  

-   Tveir tölustafir eru túlkaðir sem dagur. Það mun bæta við mánuði og ári vinnudagsetningar.  

-   Fjórir tölustafir eru túlkaðir sem dagur og mánuður. Það mun bæta við ári vinnudagsetningarinnar.  

-   Ef sú dagsetning sem færa á inn er á bilinu 01/01/1930 til 31/12/2029 skaltu slá inn árið með tveimur tölustöfum. Annars skaltu slá inn ártal með fjórum tölustöfum.  

Einnig er hægt að færa inn dagsetningu sem vikudag með vikunúmeri. Einnig er hægt að færa inn ártal. Til dæmis þýðir Mán25 eða mán25 mánudagur í viku 25.  

Hægt er að færa inn einn af þessum kóðum í stað sérstakrar dagsetningar.  

|Kóti|Niðurstaða|  
|--------------|----------------|  
|d|Þetta er dagurinn í dag (kerfisdagsetning tölvunnar).|  
|t|Þetta tilgreinir reikningstímabil þar sem t þýðir fyrsta reikningstímabilið, t2 þýðir annað reikningstímabilið og svo framvegis. |
|v|Tilgreinir vinnudagsetninguna sem er sett upp í forritinu. Vinnudagsetningunni breytt úr valmyndinni [Breyta grunnstillingum](ui-change-basic-settings.md) Handhægt gæti verið að nota vinnudagsetningar ef verið er að nota margar færslur með aðra dagsetningu en dagsins í dag.|
|n|Þetta tilgreinir að dagsetningin l eftir er lokunardagsetning, t.d. N123101.|  

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
|`131202` 132455|13-12-02 13:24:55|  
|1-12-02 10|01/12/02 10:00:00|  
|1.12.02 5|01/12/02 05:00:00|  
|1.12.02|01/12/02 00:00:00|  
|11 12|11/gildandi mánuður/gildandi ár 12:00:00|  
|1112 12|11/12/gildandi ár 12:00:00|  
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

## <a name="see-also"></a>Sjá einnig  
 [Röðun, leit og síun í listum](ui-enter-criteria-filters.md)  
 [Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
