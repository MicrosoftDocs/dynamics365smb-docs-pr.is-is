---
title: Fjárhagsfærslur fyrir opnar vörur með núll í birgðastöðu
description: Þessi grein fjallar um vandamál þar sem birgðastaðan er núll þótt opnar birgðafærslur séu til staðar.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-known-item-application-issue"></a>Hönnunarupplýsingar: Þekkt vandamál birgðajöfnunar
Þessi grein fjallar um vandamál þar sem birgðastaðan er núll þótt opnar birgðafærslur séu til staðar í [!INCLUDE[prod_short](includes/prod_short.md)].  

Greinin byrjar á því að lýsa dæmigerðum einkennum vandamálsins og síðan fylgja grunnatriði birgðajöfnunar til að styðja við útskýrðar ástæður á þessum vanda. Í lok greinarinnar er hjáleið til að takast á við slíkar opnar birgðafærslur.  

## <a name="symptoms-of-the-issue"></a>Einkenni vandamálsins
 Dæmigerð einkenni vandans við enga birgðastöðu þótt opnar birgðabókafærslur séu til staðar eru eftirfarandi:  

-   Eftirfarandi skilaboð þegar reynt er að loka birgðatímabili: „Ekki er hægt að loka birgðum þar sem neikvæðar birgðir eru til staðar í einni eða fleiri vörum.“  

-   Kringumstæður birgðafærslu þar sem bæði birgðafærsla á útleið og tengd birgðafærsla á innleið eru opnar.  

     Sjá eftirfarandi dæmi um kringumstæður birgðafærslu.  

     |Færslunr.|Bókunardagsetning|Tegund færslu|Gerð skjals|Nr. fylgiskjals|Vörunr.|Staðsetningarkóði|Magn|Kostnaðarupphæð (raunverul.)|Reikningsfært magn|Eftirstöðvar (magn)|Opið|  
     |---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
     |333|01/28/2018|Sala|Söluafhending|102043|PRÓFUN|BLÁTT|-1|-10|-1|-1|Já|  
     |334|01/28/2018|Sala|Söluafhending|102043|PRÓFUN|BLÁTT|1|10|1|1|Já|  

## <a name="basics-of-item-application"></a>Grunnatriði birgðajöfnunar
 Birgðajöfnunarfærsla er búin til fyrir hverja birgðafærslu til að tengja kostnað viðtakanda við kostnaðaruppruna svo hægt sé að áframsenda kostnaðinn samkvæmt aðferð kostnaðarútreiknings. Nánari upplýsingar eru í [Upplýsingar um hönnun: Vörujöfnun](design-details-item-application.md).  

-   Fyrir birgðafærslu á innleið er birgðajöfnunarfærslan búin til þegar birgðafærslan er búin til.  

-   Fyrir birgðafærslu á útleið er birgðajöfnunarfærslan búin til þegar birgðafærslan er bókuð, EF það til opin birgðafærsla á innleið með tiltækt magn sem hægt er að jafna. Ef það er engin opin birgðafærsla sem hægt er jafna, þá helst birgðafærslan á útleið opin þar til birgðafærsla á innleið sem hægt er að jafna er bókuð.  

 Til eru tvær gerðir birgðajöfnunar:  

-   Magnjöfnun  

-   Jöfnun kostnaðar  

### <a name="quantity-application"></a>Magnjöfnun
 Magnjöfnun er gerð fyrir allar birgðafærslur og er búin til sjálfkrafa eða handvirkt í sérstökum ferlum. Þegar gert handvirkt er magnjöfnun kölluð föst jöfnun.  

 Eftirfarandi skýringarmynd sýnir hvernig magnjöfnun er gerð.  

![Flæði kostnaðarleiðréttingar frá kaupum til sölu.](media/helene/TechArticleInventoryZero2.png "Flæði kostnaðarleiðréttingar frá kaupum til sölu")

 Takið eftir fyrir ofan að birgðafærsla 1 (Innkaup) er bæði birgir vörunnar og kostnaðaruppruni fyrir jafnaða birgðafærslu, birgðafærslu 2 (Sala).  

> [!NOTE]  
>  Ef birgðafærslan á útleið er metin á meðalkostnað þá hefur jafnaða birgðafærslan á innleið ekki einkvæman kostnaðaruppruna. Hún tekur varla þátt í útreikningi á meðalkostnaði tímabilsins.  

### <a name="cost-application"></a>Jöfnun kostnaðar
Kostnaðarjöfnun er aðeins búin til fyrir færslur á innleið þar sem reiturinn **Jafna frá birgðafærslu** er fylltur út til að útvega fasta jöfnun. Þetta gerist venjulega í tengslum við sölukreditreikning eða aðstæður ógildrar afhendingar. Kostnaðarjöfnunin tryggir að varan endi aftur inn á birgðum með sama kostnaði og þegar hún var send.  

Eftirfarandi skýringarmynd sýnir hvernig kostnaðarjöfnun er gerð.  

|Færslunr.|Bókunardagsetning|Tegund færslu|Gerð skjals|Nr. fylgiskjals|Vörunr.|Staðsetningarkóði|Magn|Kostnaðarupphæð (raunverul.)|Reikningsfært magn|Eftirstöðvar (magn)|Opið|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
|333|01/28/2018|Sala|Söluafhending|102043|PRÓFUN|BLÁTT|-1|-10|-1|-1|Já|  
|334|01/28/2018|Sala|Söluafhending|102043|PRÓFUN|BLÁTT|1|10|1|1|Já|  

 Takið eftir fyrir ofan að birgðahöfuðbók á innleið 3 (söluvöruskil) er kostnaður viðtakanda á upprunalegu birgðafærslunni á útleið 2 (sala).  

## <a name="illustration-of-a-basic-cost-flow"></a>Skýringarmynd af grunnkostnaðarflæði
 Gerum ráð fyrir að heildarkostnaðarflæði þar sem vara er móttekin, afhend og reikningsfærð sé skilað með nákvæmlega eins\-bakfærðum kostnaði og er send aftur.  

 Eftirfarandi skýringarmynd sýnir kostnaðarflæðið.  

![Flæði kostnaðarleiðréttingar frá sölu til söluvöruskila.](media/helene/TechArticleInventoryZero4.png "Flæði kostnaðarleiðréttingar frá sölu til söluvöruskila")

 Takið eftir fyrir ofan að kostnaðurinn er áframsendur á birgðafærslu 2 (sala), síðan á birgðafærslu 3 (söluvöruskil) og að lokum á birgðafærslu 4 (sala 2).  

## <a name="reasons-for-the-issue"></a>Ástæður fyrir vandamálinu
 Vandinn við engar birgðir þótt til séu opnar birgðarbókafærslur getur verið út af eftirfarandi aðstæðna:  

-   Atburðarás 1: Sending og reikningur er bókaður þótt varan sé ekki tiltæk. Bókunin er þá nákvæmur kostnaður bakfærður með sölukreditreikningi.  

-   Atburðarás 2: Sending er bókuð þótt varan sé ekki tiltæk. Bókunin er þá afturkölluð með aðgerðinni afturkalla sendingu.  

 Eftirfarandi skýringarmynd sýnir hvernig birgðajöfnun er gerð í báðum atburðarásum.  

![Flæði kostnaðarleiðréttingar liggur í báðar áttir.](media/helene/TechArticleInventoryZero6.png "Flæði kostnaðarleiðréttingar liggur í báðar áttir")  

 Takið eftir fyrir ofan að kostnaðarjöfnun er gerð (táknuð með bláum örvum) til að tryggja að birgðafærslu 2 (söluvöruskil) sé úthlutað sama kostnaði og birgðafærslan sem hún bakfærir, birgðafærsla 1 (sala 1). Hins vegar er magnjöfnun (táknuð með rauðum örvum) ekki gerð.  

 Birgðafærsla 2 (söluvöruskil) getur ekki verið bæði kostnaður viðtakanda á upprunalegu birgðafærslunni og á sama tíma verið vörubirgir og kostnaðaruppruni þeirra. Þess vegna helst upprunalega birgðafærslan 1 (sala 1) opin þar til gild uppspretta birtist.  

## <a name="identifying-the-issue"></a>Auðkenna vandann
 Til að komast að því hvort opnar birgðarbókafærslur eru búnar til skal gera eftirfarandi fyrir viðkomandi atburðarás:  

 Fyrir atburðarás 1, auðkenna vandann sem hér segir:  

-   Á síðunum **Bókaður sölukreditreikningur** eða **Bókuð vöruskilamóttaka** skal fletta upp í reitnum **Jöfnun\-frá birgðafærslu** til að sjá hvort reiturinn er útfylltur og í því tilfelli, hvaða vöruskilamóttaka birgðabókafærslu er kostnaðarjöfnuð.  

 Fyrir atburðarás 2, auðkennið vandann á annan hvorn eftirfarandi hátt:  

-   Leitið að opinni birgðafærsla á útleið og birgðafærslu á innleið með sama númeri í reitnum **Skjalanr.** og Já í reitnum **Leiðrétting**. Sjá eftirfarandi dæmi um þannig birgðafærslu.  

|Færslunr.|Bókunardagsetning|Tegund færslu|Gerð skjals|Nr. fylgiskjals|Vörunr.|Staðsetningarkóði|Magn|Kostnaðarupphæð (raunverul.)|Reikningsfært magn|Eftirstöðvar (magn)|Opið|Leiðréttingarfærsla|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|---------|
|333|01/28/2018|Sala|Söluafhending|102043|PRÓFUN|BLÁTT|-1|-10|-1|-1|Já|Nr|  
|334|01/28/2018|Sala|Söluafhending|102043|PRÓFUN|BLÁTT|1|10|1|1|Já|**Já**|  

-   Á síðunni **Bókuð söluafhending** skal fletta upp í reitnum **Jafna frá birgðafærslu** til að sjá hvort reiturinn er útfylltur og í því tilfelli hvaða vöruskilamóttaka birgðafærslu er kostnaðarjöfnuð.  

> [!NOTE]  
>  Ekki er hægt að bera kennsl á kostnaðarjöfnun á síðunni **Jafnaðar birgðafærslur** vegna þess að sú síða sýnir aðeins magnjöfnun.  

 Í báðum atburðarásum, auðkennið viðkomandi kostnaðarjöfnun sem hér segir:  

1.  Opnið töfluna **Birgðajöfnunarfærsla**.  

2.  Afmarkið reitinn **Birgðafærslunr.** með því að nota númer birgðafærslunnar á söluvöruskilum.  

3.  Greinið birgðajöfnunarfærsluna og athugið eftirfarandi:  

     Ef reiturinn **Birgðafærslunr. á útleið** er útfylltur af birgðafærslu á innleið (jákvætt magn), þá þýðir það að birgðafærslan á innleið er kostnaður viðtakanda á birgðafærslu á útleið.  

     Sjá eftirfarandi dæmi um birgðajöfnunarfærslu.  

     |Færslunr.|Birgðafærsla nr.|Birgðafærslunr. vöru á innleið|Jafnað af færslu nr.|Magn|Bókunardagsetning|Jöfnun kostnaðar|  
     |---------|---------------------|----------------------|-----------------------|--------|------------|----------------|  
     |299|334|334|333|1|01/28/2018|Já|  
<!--![Why is inventory zero 8.](media/helene/TechArticleInventoryZero8.png "Whyisinventoryzero\_8")  -->

 Takið eftir hér að ofan að birgðafærsla 334 á innleið kostnaðarjöfnuð við birgðafærslu 333 á útleið.  

## <a name="workaround-for-the-issue"></a>Hjáleið á vandanum
 Á síðunni **Birgðabók** skal bóka eftirfarandi línur fyrir vöruna sem um ræðir:  

-   Jákvæð leiðrétting til að loka opnu birgðafærslunni á útleið.  

-   Neikvæð leiðrétting með sama magni.  

     Þessi leiðrétting kemur jafnvægi á birgðaaukningu sem stafar af jákvæðri leiðréttingu og lokar opnu birgðafærslunni á innleið.  

 Niðurstaðan er sú að birgðir eru engar og allar birgðarbókafærslur eru lokaðar.  

## <a name="see-also"></a>Sjá einnig
[Hönnunarupplýsingar: umsókn vöru](design-details-item-application.md)   
[Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
