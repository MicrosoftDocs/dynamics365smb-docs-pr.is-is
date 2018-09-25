---
title: "Leita í gögnum og færa inn afmörkunarviðmið | Microsoft Docs"
description: "Lýsir því hvernig vinna skal með afmarkanir, eins og Flýtiafmörkun, til að sérstilla leitarniðurstöðurnar."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d0ef9148b082b05a46283f89c3cb98bb1cd0c6d0
ms.openlocfilehash: 10aac3906d9da8b9e0791db614142eeb90940a9b
ms.contentlocale: is-is
ms.lasthandoff: 08/06/2018

---
# <a name="searching-filtering-and-sorting-data"></a>Leita í, afmarka og raða gögnum
Það eru nokkrir hlutir sem þú getur gert sem mun hjálpa þér að finna, ákvarða nákvæmlega, og skanna skrár í lista. Þar á meðal er röðun, leit og afmörkun.

Til að leita að gögnum, svo sem heiti viðskiptamanna, aðsetrum eða vöruhópum er hægt að setja inn skilyrði. Í leitarskilyrðum er hægt að nota alla sömu tölustafi og bókstafi sem venjulega eru notaðir í reitnum. Ennfremur er hægt að nota sértákn til að afmarka niðurstöðurnar frekar. Tvær leiðir til að leita: nota flýtiafmörkun eða dálkaafmörkun.

## <a name="sorting"></a>Röðun
Með Röðun er auðvelt og fljótlegt að fá yfirsýn yfir gögnin. Ef þú ert með marga viðskiptamenn til dæmis, er hægt að velja að raða þeim eftir **númeri Viðskiptamanns**, **Bókunarflokkum viðskiptavinar**, **Gjaldmiðilskóði**, **LandsSvæðiskóða**, eða **skráningarnúmer Söluskatts** til að fá það yfirlit sem þú þarft.

Til að raða á lista, getur annað hvort valið fyrirsagnatexta dálka til að skipta á milli hækkandi og lækkandi pöntunar, eða valið litlu örina í dálkafyrirsögninni, og síðan valið **Hækkandi** eða **Lækkandi**.  

> [!NOTE]  
>   Röðun er ekki studd myndir, BLOB-reitir, FlowFilters og reitir sem tilheyra ekki töflu.  

## <a name="searching-by-using-the-quick-filter"></a>Leita með því að nota flýtiafmörkun
Hægt er að bæta afmörkunum við allar síður með því að nota flýtiafmörkun. Flýtiafmörkun er virkjuð með því að velja stækkunarglerstáknið í efra hægra horni síðu. Þessi síugerð er notuð fyrir flýtiinnfærslu viðmiða.

> [!IMPORTANT]  
>   Flýtiafmörkun veitir auðveldan aðgang að afmörkunargögnum með því að færa inn texta án sniðtákna en veitir einnig margs konar valkosti fyrir leitarskilyrði. Það fer eftir því hvort þú slærð texta eða texta með táknum, flýtiafmörkun hagar sér öðruvísi.  

* Ef ósniðinn texti er sleginn inn í leitarskilyrðum eru leitarskilyrðin túlkuð sem leit óháð há- og lágstöfum sem inniheldur ákveðinn texta.  
* Ef texti með táknum er sleginn inn í leitarskilyrðum eru leitarskilyrðin túlkuð nákvæmlega eins og þau voru slegin inn og leitin er háð há- og lágstöfum.

### <a name="quick-filter-criteria"></a>Skilyrði flýtiafmörkunar
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH>Leitarskilyrði</TH>
    <TH>Túlkað sem...</TH>
    <TH>Vöruskil...</TH>
  </TR>
  <TR>
    <TD>man</TD>
    <TD>@&#42;man&#42;</TD>
    <TD>Allar færslur þurfa að innihalda textann <b>man</b> og rétta há- og lágstafi.</TD>
  </TR>
  <TR>
    <TD>se</TD>
    <TD>@&#42;se&#42;</TD>
    <TD>Allar færslur þurfa að innihalda textann <b>se</b> og rétta há- og lágstafi.</TD>
  </TR>
  <TR>
    <TD>Man&#42;</TD>
    <TD>Hefst á <b>Man</b> og greinarmunur á litlum og stórum stöfum.</TD>
    <TD>Allar færslur sem byrja á textanum <b>Man</b></TD>
  </TR>
  <TR>
    <TD>‚man‘</TD>
    <TD>Nákvæmur texti og greinarmunur á litlum og stórum stöfum.</TD>
    <TD>Allar færslur sem samsvara <b>man</b> nákvæmlega.</TD>
  </TR>
  <TR>
    <TD>@man* </TD>
    <TD>Hefst á og enginn greinarmunur á litlum og stórum stöfum.</TD>
    <TD>Allar færslur sem byrja á <b>man</b>.</TD>
  </TR>
    <TR>
    <TD>@&#42;man</TD>
    <TD>Lýkur á og enginn greinarmunur á litlum og stórum stöfum.</TD>
    <TD>Allar færslur sem enda á <b>man</b>.</TD>
  </TR>
</TABLE>

> [!NOTE]  
>   Ekki er hægt að nota algildisstafi þegar afmarkanir eru á tölusettum reitum, til dæmis reiturinn **Staða** á sölupöntunum. Til að færa inn afmörkun fyrir þessa gerð reits, er hægt að færa inn númeragildið sem afmörkunarbreytu. Til dæmis í reitnum **Sala** á sölupöntun sem hafa gildin **Opin**, **Útgefið**, **Samþykkt í bið** og **Fyrirframgreiðsla í bið** skal nota gildin **0**, **1**, **2** og **3** til þess að afmarka þessa valmöguleika.

## <a name="searching-by-using-column-filters"></a>Leita með því að nota dálkaafmörkun
Hægt er að bæta við afmörkunum á einn eða fleiri dálka í lista. Afmörkun dálka er sveigjanlegri og meiri en flýtiafmörkunin

### <a name="to-add-a-filter-on-a-column"></a>Bæta afmörkun á dálk
1.  Áður en þú bætir við afmörkun, skal velja ![Sýna sem lista](media/ui_show_as_list_icon.png "Sýna sem lista ör vinstri") tákn til að breyta yfir í skoðun lista.
2. Velja örina sem vísar niður í fyrirsögn dálksins og velja síðan **Afmörkun**.
3. Gert er eitt af eftirfarandi:
  -  Velja *...* næst boxinu til að velja gildi úr lista.
  -  Færið inn afmörkunarviðmið í boxið. Sjá næsta hluta til að fá upplýsingar.
4. Velja hnappinn **Í lagi**.

## <a name="FilterCriteria"> </a>Afmörkunarviðmið og tákn
Þegar skilyrði eru sett er hægt að nota alla sömu tölustafi og bókstafi sem venjulega eru notaðir í reitnum. Ennfremur er hægt að nota sértákn til að afmarka niðurstöðurnar frekar. Í eftirfarandi töflum eru táknin sem hægt er að nota í afmarkanir.  

> [!IMPORTANT]  
>  Það geta verið tilvik þar sem gildi reita innihalda þessi tákn og þú vilt setja afmörkun á þau. Til að gera það, verðurðu að hafa með afmörkunarsegðina sem inniheldur táknið með gæsalöppum („“). Ef þú vilt t.d. setja afmörkun á færslur sem byrja á textanum *S&R* er afmörkunarsegðin **„S&R*'**.  

### <a name="-interval"></a>(..) Bil  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|1100..2100|Tölur 1100 til 2100.|  
|..2500|Reikningar til og með 2500|  
|..12 31 00|Dagsetningar til og með 31. 12. 00.|  
|P8..|Upplýsingar um reikningstímabil 8 og síðar.|  
|..23|Frá upphafsdegi til 23. þessa mánaðar – þessa árs 23:59:59|  
|23..|Frá 23. þessa mánaðar – þessa árs 00:00:00 til loka tímans|  
|22..23|Frá 22. þessa mánaðar – þessa árs 00:00:00 til 23. þessa mánaðar – þessa árs 23:59:59|  

### <a name="124-eitheror"></a>(&#124;) Annaðhvort/eða  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|1200&#124;1300|Tölur með 1200 eða 1300|  

### <a name="-not-equal-to"></a>(<>) Ekki jafnt og  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|<>0|Allar tölur aðrar en 0<br /><br /> Valkosturinn SQL Server býður upp á að sameina þetta tákn algildistákni. Til dæmis merkir <>A* ekki jafnt og neinn texti sem byrjar á stafnum A.|  

### <a name="-greater-than"></a>(>) Meira en  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|>1200|Tölur hærri en 1200|  

### <a name="-greater-than-or-equal-to"></a>(>=) Hærra en eða jafnt og  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|>=1200|Tölur hærri en eða jafnar 1200|  

### <a name="-less-than"></a>(<) Minna en  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|<1200|Tölur lægri en 1200|  

### <a name="-less-than-or-equal-to"></a>(<=) Lægra en eða jafnt og  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|<=1200|Tölur lægri en eða jafnar 1200|  

### <a name="-and"></a>(&) Og  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|>200&<1200|Tölur hærri en 200 og minni en 1200|  

### <a name="-an-exact-character-match"></a>('') Nákvæm stafasamsvörun  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|‚man‘|Texta sem passar nákvæmlega við Man og er stafréttur.|  

### <a name="-case-insensitive"></a>(@) Stafrétt  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|@man*|Texti sem byrjar á Man og er ekki stafréttur.|  

### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Ótilgreindur fjöldi óþekktra staftákna  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|*Co*|Texta sem inniheldur „Co“  og er stafréttur.|  
|*Ko|Texta sem endar á „Co“  og er stafréttur.|  
|Ko*|Texta sem byrjar á „Co“  og er stafréttur.|  

### <a name="-one-unknown-character"></a>(?) eitt óþekkt stafatákn  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|Hans?n|Texti eins og Hansen eða Hanson|  

### <a name="combined-format-expressions"></a>Sameinað framsetningarsnið  

|Dæmi|Sýndar færslur|  
|-----------------------|-----------------------|  
|5999&#124;8100..8490|Allar færslur með tölunni 5999 eða tölu á bilinu frá 8100 til og með 8490 er teknar með.|  
|.1299&#124;1400..|Telja með færslur með tölu sem er lægri eða jöfn 1299 eða tölu sem er jöfn 1400 eða hærri (allar tölur nema 1300 til 1399).|  
|>50&<100|Telja með færslur með tölum sem eru hærri en 50 og lægri en 100 (tölurnar 51 til 99).|  

## <a name="see-also"></a>Sjá einnig
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

