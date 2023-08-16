---
title: Hönnunarupplýsingar - vöruhúsaflæði inn
description: Vöruhúsaflæði á innleið hefst þegar vörur berast til vöruhúss fyrirtækisins og eru skráðar og samsvara upprunaskjölum á innleið.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/14/2022
ms.author: bholtorf
---
# Hönnunarupplýsingar: vöruhúsaflæði inn

Flæðiá innleið í vöruhús byrjar þegar vörurnar koma í vöruhús á staðsetningu fyrirtækis, annað hvort frá utanaðkomandi aðila eða frá annarri staðsetningu fyrirtækis. Í meginatriðum er ferlið við móttöku á innsendum pöntunum samsett úr tveimur verkþáttum:

* Taka á móti vörum á viðtökustað vöruhúss, þar sem vörurnar eru auðgreinaðar, samsvara þeim í upprunaskjal og skrá móttekið magn. 
* Setjið vörur í gang á lager og Skráið staðinn sem þið Setjið þá.

Upprunaskjöl fyrir vöruflæði á innleið eru:

* Innkaupapantanir  
* Flutningspantanir á innleið  
* Vöruskilapantanir sölu  

> [!NOTE]
> Framleiðsla og samsetningarframleiðsla standa einnig fyrir upprunaskjöl á innleið. Frekari upplýsingar um meðhöndlun framleiðslu og samsetningu samsetningar fyrir innri vinnslur í  [Hönnunarupplýsingum: innra vöruhús flæðir](design-details-internal-warehouse-flows.md).  

Í  [!INCLUDE[prod_short](includes/prod_short.md)] eru vörur afhentar og þær síðan notaðar með einni af fjórum aðferðum, eins og lýst er í eftirfarandi töflu.

|Aðferð|Ferli á innleið|Krefjast kvittana|Krefjandi frágangur|Flókið stig (frekari upplýsingar um  [Vöruhúsakerfi-Yfirlit](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bóka móttöku og frágang frá pöntunarlínunni|||Engin sérstök vöruhúsaaðgerð.|  
|B|Bóka móttöku og frágang frá birgðafrágangsskjali||Kveikt|Grunnur: pöntun-eftir pöntun.|  
|N|Bóka móttöku og frágang frá vöruhúsamóttökuskjali|Kveikt||Grunnur: Samstæða móttöku/skipa bóka fyrir margar pantanir.|  
|D|Bóka móttöku frá vöruhúsamóttökuskjali og bóka frágang frá vöruhúsafrágangsskjali|Kveikt|Kveikt|Ítarlegt|  

Val á nálgun fer eftir venjum og stigi fyrirtækisins. Eftirfarandi eru nokkur dæmi sem gætu hjálpað við að ákveða.

* Í pöntunar-og vöruhúsaumhverfi, þar sem flestir starfsmenn vöruhúss vinna beint með pöntunarskjöl, gæti verið að nota aðferð A. 
* Vöruhús pöntunarvöruhúss sem hefur flóknari frágangsferli, eða þar sem starfsmenn vöruhúss skili frágangsaðgerðum sínum frá pöntunarskjalinu, gæti notað aðferðina B.
* Fyrirtæki sem þurfa að áætla afgreiðslu margra pantana kunna að finna það gagnlegt að nota innhreyfingarskjöl vöruhúss, aðferðir C og D.  

Í aðferðum A, B og C, Móttaka og frágangur eru sameinaðir í eitt þrep þegar skjöl eru bókuð sem móttekin. Í aðferð D er móttakan bókuð fyrst til að taka upp aukningu birgða og að vörur séu til sölu. Starfsmaður í vöruhúsi skráir síðan fráganginn til að gera vörurnar tiltækar til að taka til út pantanir. 

> [!NOTE]
> Á meðan frágangur vöruhúss og frágangs á birgðum er svipaður eru þau ólík skjölum og eru notuð í mismunandi ferlum.
> * Birgðafrágangurinn sem er notaður í aðferð B ásamt frágangi upplýsinga um frágang bókar einnig móttöku upprunaskjalsins.
> * Vöruhúsafrágangurinn sem er notaður í aðferðard er ekki hægt að bóka og hann skráir aðeins fráganginn. Skráningin gerir þær vörur aðgengilegar til frekari vinnslu en bókar ekki kvittunina. Vöruhúsafrágangur krefst vöruhúsamóttöku í innstreymissinninu.

## Engin sérhæfð vöruhúsastarfsemi

Eftirfarandi greinar veita upplýsingar um hvernig á að vinna innhreyfingar fyrir upprunaskjöl ef ekki er búið að tileinka sér vöruhúsaaðgerðir.

* [Skrá innkaup](purchasing-how-record-purchases.md)
* [Flutningspöntunum](inventory-how-transfer-between-locations.md)
* [Vinna söluvöruskilapantanir](sales-how-process-sales-returns-orders.md)

## Afbrigði grunnvöruhúsa  

Í grunnvöruvöruhúsi afbrigði  **er kveikt á frágangsnunni**  en  **ekki er slökkt á Viðtökuskiptiverði kvittunar**  á síðunni Birgðageymsluspjald fyrir birgðageymsluna.

Eftirfarandi skýringarmynd sýnir innflæði í vöruhús eftir skjalagerð grunngerðar vöruhúss. Númerin í skýringarmyndinni samsvara skrefunum í hlutunum sem koma á eftir skýringarmyndinni.  

:::image type="content" source="media/design_details_warehouse_management_inbound_basic_flow.png" alt-text="Grunngerð innstreymis í vöruhúsi.":::

### 1: gefa út upprunaskjal til að stofna beiðni um birgðafrágang  

Þegar vörur eru afhentar, sleppið upprunaskjalinu, svo sem innkaupapöntun eða millisendingarpöntun á innleið. Ef skjalinu er sleppt er hægt að ganga frá vörunum. Einnig er hægt að stofna birgðafrágangskjör fyrir einstakar pöntunarlínur, á grundvelli tilgreindra hólfa og magn til afgreiðslu.  

### 2: stofna birgðafrágang  

 **Á síðunni birgðafrágangssíða**  er hægt að fá upplýsingar um upprunaskjal í undirbúningi sem byggðar eru á vöruhúsabeiðnum á innleið. Á þrýstihátt er einnig hægt að stofna birgðafrágangslínur þegar upprunaskjalið er stofnað.  

### 3: frágangur bóka frágangs  

Í  **hverri línu fyrir vörur sem gengið hefur verið frá, að hluta til eða fullu, er reiturinn Magn**  fylltur út og síðan bókaður Birgðafrágangur. Upprunaskjöl sem tengjast birgðafrágangi eru bókuð sem móttekin.  

* Jákvæðar birgðabókafærslur eru stofnaðar
* Vöruhúsafærslur eru stofnaðar fyrir staðsetningar sem krefjast hólfakóta í öllum vörufærslum.
* Frágangsbeiðninni er eytt, ef hún er að fullu afgreidd. Til dæmis reiturinn **Móttekið magn** á upprunaskjallínu á innleið er uppfærður.
* Bókað móttökuskjal er stofnað til að til dæmis endurspegla innkaupapöntunina og mótteknar vörur.  

## Grunngerðir í ítarlegu vöruhúsi  

Í ítarlegri samskipan vöruhúss er krafist að  **skipta kvittun**  á Birgðageymsluspjald á síðunni fyrir birgðageymsluna. Skiptibreyta til að  **krefjast**  frágangs er valfrjáls.

Eftirfarandi skýringarmynd sýnir flæði á innleið í vöruhúsi eftir tegund fylgiskjals. Númerin í skýringarmyndinni samsvara skrefunum í hlutunum sem koma á eftir skýringarmyndinni.  

:::image type="content" source="media/design_details_warehouse_management_inbound_advanced_flow.png" alt-text="Ítarlegt innflæði í vöruhús.":::

### 1: gefa út upprunaskjal  

Við móttöku vara er losað um upprunaskjalið, til dæmis innkaupapöntun eða millifærslapöntun á innleið. Ef skjalinu er sleppt er hægt að ganga frá vörunum. Gengið mun innihalda tilvísanir í tegund upprunaskjals og númer.

### 2: stofna vöruhúsamóttöku  

 **Á móttökusíðu**  vöruhúss, fá upprunaskjalslínur á innleið. Hægt er að sameina margar upprunaskjalslínur í einu vöruhúsamóttöku skjali.  **Reiturinn Magn til afgreiðslu**  er fylltur út og valið viðtökusvæði og hólf ef með þarf.  

### 3: bóka vöruhúsamóttöku  

Bóka vöruhúsamóttöku til að stofna jákvæðar birgðabókafærslur.  **Reiturinn móttekið**  Magn í upprunaskjalslínu á innleið er uppfærður.  

 **Ef ekki er kveikt á frágangsvíxlun**  þarf ekki að vera á birgðageymsluspjaldinu þar sem ferlið stöðvast. Að öðrum kosti gerir bókun um upprunaskjal vörurnar það sem hægt er að ganga frá. Frágangurinn inniheldur tilvísanir í gerð upprunaskjals og númer.  

### 4: (valfrjálst) mynda vinnublaðslínur frágangs

Sækja vöruhúsafrágangslínur í  **vinnublaði**  frágangs á grundvelli bókaðra vöruhúsamóttöku eða aðgerða sem framleiða úttak. Velja línurnar til að ganga frá og tilgreina eftirfarandi upplýsingar:

* Hólfin til að taka vörur úr.
* Hólfin til að setja vörur í.
* Hversu margar einingar á að afgreiða.

Hólfin geta verið forskilgreind í uppsetningu vöruhúsastaðarins eða forðarinnar sem framkvæmdi aðgerðina.  

Þegar allur frágangur er áætlaður og úthlutað á vöruhúsastarfsmenn skal mynda vöruhúsafrágangsskjölin. Frágangsbókarlínum hefur verið úthlutað fullfrágengnum  **vinnublaði**.  

> [!NOTE]  
>  **Ef skiptiborð vinnublaðs**  er ekki kveikt á birgðageymsluspjaldinu eru frágangsskjöl vöruhúss stofnuð beint á grundvelli bókaðra vöruhúsamóttöku. Í því tilfelli er þetta skref ekki þörf.  

### 5: frágangur skjals vöruhúsafrágangs stofnaður

Vöruhúsafrágangur skjals er stofnaður í togtísku á grundvelli bókuðu vöruhúsamóttöku. Einnig er hægt að stofna vöruhúsafrágangsskjalið og úthluta því á vöruhúsastarfsmann á þrýstihátt.  

### 6: frágangur vöruhúsa skal skrá

Í hverri línu fyrir vörur sem gengið hefur verið frá, að hluta til eða fullu, er fyllt út í  **reitinn Magn**  á  **frágangssíðu vöruhúsafrágangs**  og síðan er frágangur vöruhússins skráður.  

* Vöruhúsafærslur eru stofnaðar fyrir staðsetningar sem krefjast hólfakóta í öllum vörufærslum.
* Vöruhúsafrágangslínur eru eyddar, ef þær eru að fullu meðhöndlaðar.
* Frágangsskjal vöruhúss er opið þar til allt magn tengdrar móttöku vöruhúss er skráð.
*  **Reiturinn Magn frágangs**  á bókaða vöruhúsamóttökupöntunarlínum vöruhúss er uppfærður.

## Tengd verkefni

Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.

|**Til að**|**Sjá**|  
|------------|-------------|  
|Skrá innhreyfingar vara á vöruhúsastöðum með vöruhúsamóttöku, ef um er að ræða hálf-eða sjálfvirka vöruhúsavinnslu á staðnum.|[Móttaka vara](warehouse-how-receive-items.md)|
|Setja vörur í burtu á grundvelli pöntunar og Bóka móttöku í einni aðgerð í grunnvöruhúsafbrigðum.|[Ganga frá vörum með birgðafrágangi](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Frágangur móttekinna vara úr mörgum innkaupum, söluskilum, millifært er í pantanir í ítarlegri samskipan vöruhúss.|[Ganga frá vörum með vöruhúsafrágangi](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  


## Sjá einnig

[!INCLUDE[footer-include](includes/footer-banner.md)]
