---
title: Staðlaðar ítrekunarinnkaupalínur
description: Settu upp innkaupalínur sem eru oft notaðar til að færa þær inn í innkaupaskjöl og fylla þannig á fljótlegan hátt út í línurnar með stöðluðum upplýsingum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'trade, purchase, replenishment'
ms.search.form: 177
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Stofna ítrekunarinnkaupalínur

Ef þú þarft oft að stofna innkaupalínur með svipuðum upplýsingum geturðu sett upp staðlaðar línur sem þú getur svo fært inn í endurtekin innkaupaskjöl, til dæmis fyrir endurteknar áfyllingapantanir.

## Setja upp endurteknar innkaupalínur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Endurteknar innkaupalínur** og velja síðan viðkomandi tengil.
2. Á síðunni **Endurteknar innkaupalínur** skal velja aðgerðina **Nýtt**.
3. Fyllt er út í reiti eftir því sem er nauðsynlegt í flýtiflipanum **Almennt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Í flýtiflipanum **Línur** skal færa inn upplýsingar í reitina sem endurspegla staðlaðar línur sem þú býst við að nota sem endurteknar línur í innkaupaskjölum.

> [!NOTE]
> Þú getur ekki skilgreint verð í endurteknum innkaupalínum vegna þess að verð, afslættir o.s.frv. er reiknað út á raunverulegu söluskjölunum eftir að þú setur inn endurteknar innkaupalínur.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## Úthluta endurteknum innkaupalínum á lánardrottin

Úthluta lánardrottni einni eða fleiri ítrekunarinnkaupalínum svo hægt sé að setja þær inn í innkaupaskjöl frá viðkomandi lánardrottni.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Lánardrottnar** og síðan velja viðkomandi tengil.
2. Opnaðu spjaldið fyrir viðeigandi lánardrottin.
3. Veldu aðgerðina **Endurteknar innkaupalínur**.
4. Á síðunni **Endurteknar innkaupalínur** skal velja kóða fyrir endurteknar innkaupalínur sem þú vilt geta sett inn á söluskjöl fyrir lánardrottin.
5. Fylltu út viðbótarreitina til að skilgreina hvenær, hvernig og hvar eigi að nota endurteknar innkaupalínur.
6. Í þeim fjórum reitum þar sem þú velur hvernig línurnar eru settar inn á skjalategundum skaltu velja einn af eftirfarandi valkostum:

|Valkostur|Lýsing|
|------|-----------|
|**Handvirkt**|Þú verður að leita handvirkt og setja inn endurtekna innkaupalínu sem er til fyrir lánardrottin.|
|**Sjálfvirkt**|Ef margar ítrekunarinnkaupalínur eru til fyrir lánardrottininn fæst tilkynning þar sem hægt er að tína hvora á að setja inn. Ef aðeins ein endurtekin innkaupalína er til staðar verður hún sett inn sjálfkrafa.<br /><br />Þetta virkar aðeins ef nýja skjalið var búið til úr skjalalista, til dæmis með því að velja aðgerðina **Nýtt** á síðunni **Innkaupapantanir**. Það virkar til dæmis ekki ef skjalið var stofnað á lánardrottnaspjaldi.|
|**Spyrja alltaf**|Tilkynning birtist og allar núverandi endurteknar innkaupalínur eru sýndar þannig að hægt er að velja eina.

## Setja endurteknar innkaupalínur inn á innkaupareikning

Ef endurteknar innkaupalínur eru til fyrir lánardrottin getur þú sett þær inn eða látið bæta þeim við sjálfkrafa á allar tegundir innkaupaskjala, t.d. innkaupareikning. Hafi valkostirnir Alltaf spurt **verið virkjaðir** þegar lánardrottnum er úthlutað ítrekuðum innkaupalínum verður þér tilkynnt hvort ítrekaðar innkaupalínur séu til.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningar** og velja síðan viðkomandi tengil.
2. Opnaðu innkaupareikninginn þar sem á að setja inn eina eða fleiri staðlaðar innkaupalínur.
3. Veldu aðgerðina **Sækja endurteknar innkaupalínur**.
4. Á síðunni **Endurteknar innkaupalínur** skal velja uppflettihnappinn í reitnum **Kóði** og síðan velja safn staðlaðra innkaupalína.
5. Veldu hnappinn **Í lagi** til að setja staðlaðar innkaupalínur á reikninginn þar sem þú getur endurnýtt þær eins og þær eru eða breyttu upplýsingunum.

## Sjá einnig .

[Innkaup](purchasing-manage-purchasing.md)  
[Setja upp innkaup](purchasing-setup-purchasing.md)  
[Stofna endurteknar sölur](sales-how-work-standard-lines.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]