---
title: Hönnunarupplýsingar - kostnaðarleiðrétting | Microsoft Docs
description: Megintilgangurinn með kostnaðarleiðréttingu er að framsenda breytingar á kostnaði frá uppruna kostnaðar að viðtakendum kostnaðar í samræmi við aðferð kostnaðarútreiknings fyrir hverja vöru, til að fyrir liggi rétt verðmat birgða.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 545a3d1ae7e95623edc373404d5d39c92516e6a8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777899"
---
# <a name="design-details-cost-adjustment"></a>Hönnunarupplýsingar: kostnaðarleiðrétting

Megintilgangurinn með kostnaðarleiðréttingu er að framsenda breytingar á kostnaði frá uppruna kostnaðar að viðtakendum kostnaðar í samræmi við aðferð kostnaðarútreiknings fyrir hverja vöru, til að fyrir liggi rétt verðmat birgða.  

Vara getur verið sölureikningsfærð áður en hún er innkaupareikningsfærð þannig að skráð birgðavirði sölunnar passar ekki við raunverulegan innkaupakostnað. Kostnaðarleiðréttingar uppfærir kostnaðarverð seldra vara (cogs) fyrir sögulegar færslur til að tryggja að þær samsvari kostnaði færslna á innleið sem þeim er beitt á. Nánari upplýsingar eru í [Upplýsingar um hönnun: Vörujöfnun](design-details-item-application.md).  

Eftirfarandi eru aukatilgangur eða -aðgerðir, kostnaðarleiðréttingar:  

* Reikningsfæra afgreiddar framleiðslupantanir:  

  * Breyta stöðu virðisfærslu úr **Væntanlegur** til **Raunveruleg**  
  * Hreinsa VÍV-reikninga. Frekari upplýsingar eru í [Hönnunarupplýsingar: staða framleiðslupöntunar](design-details-production-order-posting.md).  
  * Bóka frávik. Nánari upplýsingar eru í [Upplýsingar um hönnun: Frávik](design-details-variance.md).  
  * Uppfærið kostnaðarverðið á birgðaspjaldinu.  

Birgðakostnað verður að jafna áður en tengdar virðisfærslur er hægt að afstemma við fjárhagsbók. Frekari upplýsingar, sjá [Hönnunarupplýsingar: afstemming við fjárhaginn](design-details-reconciliation-with-the-general-ledger.md)  

## <a name="detecting-the-adjustment"></a>Borin kennsl á leiðréttingu

Það að bera kennsl á það hvort kostnaðarleiðrétting ætti að fara fram fer aðallega fram í Birgðabók - bókunarlína, meðan reikningur og myndun kostnaðarleiðréttingarfærslna fer fram í runuvinnslunni **Leiðr. kostnað – Birgðafærslur**.  

Til að vera fær um að senda kostnaði ákvarðar greiningarkerfið hvaða uppruni hefur breyst í kostnaði og á hvaða áfangastað þessi kostnaður ætti að vera fluttur. Eftirfarandi þrjár greiningaraðgerðir eru í [!INCLUDE[prod_short](includes/prod_short.md)]:  

* Birgðajöfnunarfærsla  
* Færslustig meðalkostnaðarleiðréttingar  
* Pöntunarstig  

### <a name="item-application-entry"></a>Birgðajöfnunarfærsla

Þessi auðkenningarvirkni er notuð fyrir vörur sem nota FIFO, LIFO, Staðlaða og Sértæka aðferð við kostnaðarútreikning og fyrir fasta umsókn. Aðgerðin virkar á eftirfarandi hátt:  

* Kostnaðarleiðrétting er greind með því að merkja upprunabirgðafærslur sem *Jöfnuð færsla til leiðréttingar* í hvert sinn sem birgðabók eða virðisfærsla er bókuð.  
* Kostnaðarframsending á sér stað í samræmi við kostnaðarkeðjur sem eru skráðar í töflunni **Birgðajöfnunarfærsla**.  

### <a name="average-cost-adjustment-entry-point"></a>Færslustig meðalkostnaðarleiðréttingar

Þessi auðkenningarvirkni er notuð fyrir vörur sem nota Aðferð meðalkostnaðarútreiknings. Aðgerðin virkar á eftirfarandi hátt:  

* Kostnaðarleiðréttingu verður vart með því að merkja færslu í töflunni **Upphafsstaður meðalkostnaðarleiðréttingar** þegar virðisfærsla er bókuð.  
* Kostnaðarframsending sér stað með því að beita kostnaðinum á virðisfærslur með síðari matsdegi.  

### <a name="order-level"></a>Pöntunarstig

Þessi auðkenningarvirkni er notuð í umbreytingaraðstæðum, framleiðslu og samsetningu. Aðgerðin virkar á eftirfarandi hátt:  

* Kostnaðarleiðrétting er merkt með því að merkja pöntunina þegar efni/tilfang er bókaður sem neytt/notað.  
* Kostnaðarframsending á sér stað með því að beita kostnaðinum úr efninu/forða á frálagsfærslur sem tengjast pöntuninni.  

Greiningaraðgerðin á pantanastigi er notuð til að greina leiðréttingar á bókun samsetninga. Eftirfarandi mynd sýnir uppbyggingu leiðréttingarfærslu:  

![Flæði færslna í kostnaðarleiðréttingu](media/design_details_assembly_posting_3.png "Flæði færslna í kostnaðarleiðréttingu")  

Frekari upplýsingar, sjá [Hönnunarupplýsingar: bókun samsetningarpöntunar](design-details-assembly-order-posting.md).  

## <a name="manual-versus-automatic-cost-adjustment"></a>Handvirk samanborið við sjálfvirka kostnaðarleiðréttingu

Kostnaðarleiðréttingu er hægt að framkvæma á tvo vegu:  

* Keyra runuvinnsluna **Kostnaðarleiðrétting - Birgðafærslur** handvirkt. Hægt er að keyra þessa runuvinnslu fyrir allar vörur eða aðeins fyrir tilteknar vörur eða flokka. Runuvinnslan keyrir kostnaðarleiðréttingu fyrir vörurnar í birgðum sem færsla á innleið hefur verið stofnuð fyrir, líkt og innkaup. Fyrir vörur sem nota aðferðina Meðaltal til kostnaðarútreiknings gerir runuvinnslan einnig leiðréttingu ef einhverjar færslur á útleið eru stofnaðar.  
* Sjálfkrafa með því að stilla kostnaði í hvert skipti sem þú bókar birgðafærslu og þegar þú hefur lokið við framleiðslupöntun. Kostnaðarleiðrétting er aðeins keyrt fyrir tiltekna vöru eða vörur sem verða fyrir áhrifum af bókun. Þetta er sett upp þegar gátreiturinn **Sjálfvirk kostnaðarleiðrétting** er valinn á síðunni **Uppsetning birgða**.  

Það er gott að keyra kostnaðarleiðréttingu sjálfkrafa við bókun þar sem kostnaðarverð er oftar uppfært og því réttara. Ókosturinn er að afköst af gagnagrunninum getur haft áhrif með því að keyra kostnaðarleiðréttingu svo oft.  

Því það er mikilvægt að halda einingarkostnaður á vöru uppfærðri, það er mæla með því að þú keyrir **Kostnaðarleiðrétting - Birgðafærslur** runuvinnsluna eins oft og mögulegt er, utan vinnutíma. Einnig er hægt að nota sjálfvirka kostnaðarleiðréttingu. Þetta tryggir að einingarkostnaður vara uppfærist daglega.  

Hvort sem þú keyrir kostnaðarjöfnun handvirkt eða sjálfvirkt, jöfnunarferlið og afleiðingar þess eru þau sömu. [!INCLUDE[prod_short](includes/prod_short.md)] reiknar virði færslna á innleið og áframsendir kostnaðinn á allar færslur á útleið, svo sem sölu eða notkun, sem hefur verið beitt á færslu á innleið Kostnaðarleiðrétting stofnar gildisfærslur sem innihalda leiðréttingarfjárhæðir og upphæðir sem bæta fyrir sléttun.  

Nýja leiðréttingin og jöfnunargildafærslurnar eru með bókunardagsetningu tengda reikningsins. Undantekningar eru ef virðisfærslurnar lenda á lokuðu reikningstímabil eða bókhaldstímabili eða ef bókunardagsetningin er á undan dagsetningunni í reitnum **Bókun leyfð frá** á síðunni **Fjárhagsgrunnur**. Ef þetta gerist úthlutar runuvinnslan bókunardagsetningu sem fyrstu dagsetningu næsta opna tímabils.  

## <a name="adjust-cost---item-entries-batch-job"></a>Leiðrétta kostnað - Birgðafærslur

Þegar runuvinnslan **Kostnaðarleiðrétting - Birgðafærslur** er keyrð hefurðu þann valkost að keyra runuvinnsluna fyrir allar vörur eða aðeins fyrir tilteknar vörur eða flokka.  

> [!NOTE]  
> Við mælum með að þú keyrir alltaf runuvinnslu fyrir allar vörur og aðeins nota afmörkunarvalkostur til að draga keyrslutíma af runuvinnslunni, eða til að leiðrétta kostnað tiltekinnar vöru.  

### <a name="example"></a>Dæmi

Eftirfarandi dæmi sýnir ef keypt vara er bókuð sem móttekin og reikningsfærð 01-01-20. Seinna eru seldu vörurnar bókaðar sem sendar og reikningsfærðar 01-15-20. Svo keyrðirðu runuvinnslurnar **Leiðrétta kostnað - Birgðafærslur** og **Bóka birgðakostnað í Fjárhag**. Eftirfarandi færslur eru stofnaðar.  

#### <a name="value-entries-1"></a>Virðisfærslur (1) 

|Bókunardagsetning|Birgðafærslutegund|Kostnaðarupphæð (raunverul.)|Kostnaður bókaður í fjárhag|Reikningsfært magn|Færslunr.|  
|------------|----------------------|--------------------|------------------|-----------------|---------|  
|01-01-20|Innkaup|10,00|10,00|1|1|  
|01-15-20|Sala|-10,00|-10,00|-1|2|  

#### <a name="relation-entries-in-the-gl--item-ledger-relation-table-1"></a>Tengslafærslur í fjárhag - tengslatafla fjárhagsbirgðabókar (1)

|Fjárhagsfærslunr.|Virðisfærslunr.|Fjárhagsdagbók nr.|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  

#### <a name="general-ledger-entries-1"></a>Fjárhagsfærslur (1)

|Bókunardagsetning|Fjárhagur|Reikningur nr. (En-US sýnishorn)|Upphæð|Færslunr.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|[Reikningur birgða]|2130|10,00|1|  
|01-01-20|[Jöfnunareikn. beins kostnaðar]|7291|-10,00|2|  
|01-15-20|[Reikningur birgða]|2130|-10,00|3|  
|01-15-20|[Kostnaður seldra vara]|7290|10,00|4|  

Seinna er tengdur kostnaðarauki innaupa upp á SGM 2,00 reikningsfærður 02-10-20. Keyrðu runuvinnslurnar **Leiðrétta kostnað - Birgðafærslur** og **Bóka birgðakostnað í Fjárhag**. Kostnaðarleiðréttingarrunuvinnsla leiðréttir kostnaði við sölu um SGM -2,00 í samræmi við það, og **Bóka birgðakostnað í Fjárhag** runuvinnslan bókar nýja gildisfærslur í fjárhag. Niðurstaðan er eftirfarandi.  

#### <a name="value-entries-2"></a>Virðisfærslur (2)  

|Bókunardagsetning|Birgðafærslutegund|Kostnaðarupphæð (raunverul.)|Kostnaður bókaður í fjárhag|Reikningsfært magn|LEIÐRÉTT|Færslunr.|  
|------------|----------------------|--------------------|------------------|-----------------|----------|---------|  
|02-10-20|Innkaup|2,00|2,00|0|Nei|3|  
|01-15-20|Sala|-2,00|-2,00|0|Já|4|  

#### <a name="relation-entries-in-the-gl--item-ledger-relation-table-2"></a>Tengslafærslur í fjárhag - tengslatafla fjárhagsbirgðabókar (2)

|Fjárhagsfærslunr.|Virðisfærslunr.|Fjárhagsdagbók nr.|  
|-------------|---------------|----------------|  
|5|3|2|  
|6|3|2|  
|7|4|2|  
|8|4|2|  

#### <a name="general-ledger-entries-2"></a>Fjárhagsfærslur (2)

|Bókunardagsetning|Fjárhagur|Reikningur nr. (En-US sýnishorn)|Upphæð|Færslunr.|  
|------------|-----------|------------------------|------|---------|  
|02-10-20|[Reikningur birgða]|2130|2,00|5|  
|02-10-20|[Jöfnunareikn. beins kostnaðar]|7291|-2,00|6|  
|01-15-20|[Reikningur birgða]|2130|-2,00|7|  
|01-15-20|[Kostnaður seldra vara]|7290|2,00|8|  

## <a name="automatic-cost-adjustment"></a>Sjálfvirk kostnaðarleiðrétting

Til að setja upp kostnaðarleiðréttingu til að keyra sjálfkrafa þegar þú bókar birgðafærslu, skal nota reitinn **Sjálfvirk kostnaðarleiðrétting** á síðunni **Uppsetning birgða**. Með þessum reit er hægt að velja hversu langt aftur í tímann frá núverandi vinnudegi sjálfvirk kostnaðarleiðrétting á að eiga sér stað. Eftirfarandi möguleikar eru til staðar.  

|Valkostur|Description|
|------|-----------|
|Aldrei|Kostnaður er ekki leiðréttur við bókun|  
|Dagur|Kostnaður er leiðréttur ef bókun á sér stað innan eins dags frá vinnudagsetningunni.|  
|Vika|Vika - Kostnaður er leiðréttur ef bókun á sér stað innan einnar viku frá vinnudagsetningunni.|  
|Mánuður|Mánuður - Kostnaður er leiðréttur ef bókun á sér stað innan eins mánaðar frá vinnudagsetningunni.|  
|Fjórðungur|Kostnaður er leiðréttur ef bókun á sér stað innan eins ársfjórðungs frá vinnudagsetningunni.|  
|Ár|Kostnaður er leiðréttur ef bókun á sér stað innan eins árs frá vinnudagsetningunni.|  
|Alltaf|Kostnaður er alltaf leiðréttur við bókun óháð bókunardagsetningunni.|  

Valið í reitnum **Sjálfvirk kostnaðarleiðrétting** er mikilvægt fyrir afköst og nákvæmni kostnaðar. Styttri tímabil, td **Dagur** eða **vika**, hefur minni áhrif á kerfið, vegna þess að þeir veita strangari krafa um að einungis kostnaður bókaður á síðasta degi eða viku má jafna sjálfkrafa. Þetta þýðir að sjálfvirk kostnaðarleiðrétting er ekki keyrð eins oft og því eru minni áhrif á afköst kerfisins. Hins vegar þýðir það einnig að einingarkostnaður gæti orðið ónákvæmari.  

### <a name="example"></a>Dæmi

Eftirfarandi dæmi sýnir sjálfvirka leiðréttingu kostnaðar:  

* 10. janúar er keypt vara bókuð sem móttekin og reikningsfærð.  
* 15. janúar er sölupöntun fyrir vöruna bókuð sem afhent og reikningsfærð.
* 5. febrúar verður móttekinn reikningur fyrir flutningsgjald upprunalegra innkaupa. Þetta farmgjald er bókað og jafnað við upprunalega innkaupareikninginn sem eykur kostnað við upprunalegu innkaupin.  

Ef sjálfvirk kostnaðarleiðrétting hefur verið sett upp til að eiga við bókanir sem eiga sér stað innan mánaðar eða ársfjórðungs frá núverandi vinnudagsetningu keyrir sjálfvirka kostnaðarleiðréttingin og kostnaðurinn við innkaupin er framsendur í söluna.  

Ef sjálfvirk kostnaðarleiðrétting hefur verið sett upp til að eiga við bókanir sem eiga sér stað innan dags eða viku frá núverandi vinnudagsetningu keyrir sjálfvirka kostnaðarleiðréttingin ekki og kostnaðurinn við innkaupin er ekki framsendur í söluna fyrr en runuvinnslan **Kostnaðarleiðrétting - Birgðafærslur** er keyrð.  

## <a name="see-also"></a>Sjá einnig

[Leiðr. kostnað vara](inventory-how-adjust-item-costs.md)  
[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  
[Hönnunarupplýsingar: afstemming í fjárhagur](design-details-reconciliation-with-the-general-ledger.md)  
[Hönnunarupplýsingar: birgðabókun](design-details-inventory-posting.md)  
[Hönnunarupplýsingar Frávik](design-details-variance.md)  
[Hönnunarupplýsingar: Bókun samsetningarpöntunar](design-details-assembly-order-posting.md)  
[Hönnunarupplýsingar: staða framleiðslupöntunar](design-details-production-order-posting.md)  
[Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]