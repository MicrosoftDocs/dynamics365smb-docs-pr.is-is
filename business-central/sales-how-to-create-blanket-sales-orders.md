---
title: Vinna með standandi sölupantanir eða innkaupapantanir
description: Standandi pantanir eru notaðar þegar viðskiptamaður hefur samþykkt að kaupa í miklu magni sem afhenda á í nokkrum minni afhendingum á ákveðnu tímabili. Það sama á við um innkaup.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '507, 509, 6620, 6622, 6623, 9303, 9310'
ms.date: 03/20/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="work-with-blanket-sales-orders-or-blanket-purchase-orders"></a>Vinna með standandi sölupantanir eða standandi innkaupapantanir

Standandi sölupöntun er rammi fyrir langtíma samning milli viðkomandi og viðskiptamanns. Á svipaðan hátt eru standandi innkaupapantanir notaðar til að stjórna langtímasamningum milli þín og lánardrottins.

Standandi pöntun er yfirleitt stofnuð þegar viðskiptamaður hefur skuldbundið sig til kaupa á miklu magni sem afhenda á í nokkrum minni afhendingum á ákveðnu tímabili. Standandi pantanir ná oft eingöngu yfir eina vöru með fyrirframákveðnum afhendingardögum. Helsta ástæðan fyrir notkun standandi pöntunar í stað sölupöntunar er sú að magn sem fært er inn á standandi pöntun hefur ekki áhrif á vöru til ráðstöfunar og því er hægt að nota það sem vinnublað til eftirlits, spár og áætlanagerðar.

Í standandi pöntun er hægt að setja hverja afhendingu upp sem pantanalínu sem hægt er að breyta í sölupöntun við afhendingu.

Dæmi um hvenær standandi sölupöntun er hægt að nota er ef viðskiptamaður hefur samband og leggur inn pöntun upp á 1000 einingar af vörur og vill fá afhentar 250 einingar á viku næsta mánuðinn.

> [!NOTE]
> Standandi innkaupapöntun virka á svipaðan hátt og standandi sölupantanir. Þetta fylgiskjal nær eingöngu yfir standandi sölupantanir.

## <a name="to-create-a-blanket-sales-order"></a>Til að búa til standandi sölupöntun.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Standandi sölupantanir** og velja síðan viðkomandi tengil.  
2. Valið er **Nýtt** aðgerð.  
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Reiturinn **Pöntunardags.** er hafður auður. Þegar nokkrar sölupantanir eru stofnaðar úr standandi pöntun notar kerfið eiginlegu vinnudagsetninguna fyrir pöntunardagsetningu sölupöntunarinnar.
5. Á flýtiflipanum **Línur** skal stofna sérstaka línu fyrir hverja afhendingu. Til dæmis ef viðskiptamaðurinn vill skipta 1000 einingum niður á fjórar vikur þarf að færa inn fjórar línur, hver upp á 250.  

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a>Stofnun sölupöntunar úr standandi sölupöntun

1. Til að stofna pöntun fyrir einhverja af línunum í standandi sölupöntuninni skal fjarlægja magnið í reitnum **Magn til afhendingar** í öllum línunum sem ekki á að afhenda að þessu sinni.  
2. Þegar notandi er tilbúinn að stofna pantanir skal velja aðgerðina **Búa til pöntun** og velja **svo Já**. Skilaboð birtast um að standandi pöntunin hafi fengið pöntunarnúmer. Bent er á að standandi pöntuninni hefur ekki verið eytt.  
3. Velja hnappinn **Í lagi**.  
4. Til að birta niðurstöður fyrri skrefa skal velja aðgerðina **, Lína**, velja **Óbókaðar línur**, og velja síðan aðgerðina **Pantanir**.  
5. Á síðunni **Sölulínur** er viðeigandi sölupöntun valin, velja aðgerðina **Lína** og velja svo **Sýna fylgiskjal** aðgerðina.  

Eftirfarandi á við sölupantanir eftir að þær hafa verið stofnaðar úr standandi sölupöntunum:  

- Þegar búið er að breyta standandi pöntun í sölupöntun inniheldur sölupöntunin allar línur standandi pöntunarinnar. Línurnar þar sem magninu í reitnum **Magn til afhendingar** var eytt birtast með reitina **Magn** auða. Hægt er velja hvort línurnar haldi sér, þeim sé breytt eða þeim eytt.  
- Mikilvægt er að muna að magn sölupöntunarlínunnar má ekki vera hærra en magnið í tengdri standandi pöntunarlínu. Annars er ekki hægt að bóka sölupöntunina.  
- Þegar sölupöntun er bókuð eða hún afhent og/eða reikningsfærð uppfærir kerfið reitina **Afhent magn** og **Reikningsfært magn** í tengdri standandi pöntun.  
- Skráð er númer standandi pöntunarinnar og línunúmer sem eiginleika sölulínunnar þegar hún er stofnuð úr standandi pöntun.  
- Þegar sölupantanir eru ekki stofnaðar beint úr standandi pöntun en tengjast henni samt er hægt að koma á tengingu milli sölupöntunar og standandi pöntunar með því að færa inn númer standandi pöntunarinnar í reitinn **Standandi pöntunarnr.** reitinn í sölupöntunarlínunni.  
- Eftir að sölupöntunin hefur verið stofnuð fyrir heildarmagn standandi pöntunarlínu, verður ekki hægt að stofna neina aðra sölupöntun fyrir sömu línu. Notendur eru hindraðir frá því að færa magn inn í reitinn **Magn til afhendingar**. Ef hins vegar þarf að bæta viðbótarmagni við standandi pöntun er hægt að hækka gildið í reitnum **Magn** og svo stofna viðbótarpantanir.  
- Reikningsfærða standandi sölupöntunin helst í kerfinu þar til henni er eytt, annaðhvort með því að eyða einstökum standandi pöntunum eða með keyrslunni **Eyða reikningsfærðum standandi sölupöntunum** .  
- Ef viðskiptamaður er einnig skráður sem tengiliður í kerfishlutanum Tengslagrunnur og ef kóti samskiptasniðmáts fyrir standandi söluvörupöntun hefur verið skilgreindur á síðunni **Tengslagrunnur** eru samskipti skráð sjálfkrafa í töfluna Skráningarfærsla samskipta þegar smellt er á **Prenta** til að prenta standandi söluvörupöntunina.

## <a name="to-view-the-status-of-a-blanket-sales-order"></a>Til að skoða stöðu standandi sölupöntunar:

Hægt er að sjá stöðu standandi sölupöntunar á síðunni **Upplýsingar um** standandi sölupantanir. Þetta getur átt við þegar hafist er handa við að reikningsfæra pöntunina sem er stofnuð úr standandi sölupöntuninni.  

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Standandi sölupantanir** og velja síðan viðkomandi tengil.  
2.  Veldu standandi sölupöntun og síðan aðgerðina **Upplýsingar**.  
3.  Á síðunni **Upplýsingar um** standandi sölupantanir á flýtiflipanum **Almennt** er hægt að skoða samantekt á allri pöntuninni á grundvelli heildarmagnsins í hinum ýmsu magnreitum **í** línum standandi sölupöntunarinnar.  

- Á flýtiflipanum **Reikningsfærsla** er hægt að sjá samantekt byggða á heildarmagni í reitunum **Magn til reikningsfærslu** í línum standandi sölupöntunarinnar.  
- Á flýtiflipanum **Afhending** er hægt að sjá samantekt byggða á heildarmagni í reitunum **Magn til móttöku** í línum standandi sölupöntunarinnar.  
- Á flýtiflipanum **Fyrirframgreiðsla** er hægt að sjá samantekt um allar fyrirframgreiddar upphæðir.  
- Á flýtiflipanum **Lánardrottinn** er hægt að skoða ákveðnar grunnupplýsingar um lánardrottininn.

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a>Hvernig á að skoða óbókaðar og bókaðar línur standandi sölupöntunar

Tengingin milli standandi sölupöntunar og upphaflegrar sölupöntunar, og allra annarra söluskjala, er varðveitt eftir bókun sem listi yfir bókaðar og óbókaðar reikningslínur sölupantana.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Standandi sölupantanir** og velja síðan viðkomandi tengil.
2. Opna standandi sölupöntun sem á að skoða.
3. Til að skoða óbókaðar færslur skal smella á viðkomandi línu, velja aðgerðina **Lína**, og velja síðan aðgerðina **óbókaðar línur**. Einn af eftirfarandi kostum er valinn:  

|Valkostur|Description|
|--|--|
|**Pantanir**|Tilgreinir opnar pantanir tengdar völdu línunni.|
|**Reikningar**|Tilgreinir opna reikninga sem tengdir hafa verið við völdu línuna. Opnir reikningar eru handvirkt tengdir við standandi pöntun með því færa inn standandi pöntunarnúmer í sölureikningslínuna.|
|**Vöruskilapantanir**|Tilgreinir opnar vöruskilapantanir sem hafa verið tengdar við völdu línuna eru opnaðar.|
|**Kreditreikningar**|Tilgreinir kreditreikninga sem tengdir hafa verið við völdu línuna.|

4. Til að skoða bókaðar færslur skal smella á viðkomandi línu, velja aðgerðina **Lína**, og velja síðan aðgerðina **bókaðar línur**. Einn af eftirfarandi kostum er valinn:  

|Valkostur|Description|
|---|----|
|**Afhendingar**|Bókaðar afhendingar tengdar við völdu línuna..|
|**Reikningar**|Bókaðir reikningar tengdir við völdu línuna..|
|**Vöruskilamóttökur**|Bókaðar vöruskilamóttökur tengdar við völdu línuna.|
|**Kreditreikningar**|Bókaðir kreditreikningar sem tengdir hafa verið við völdu línuna.|

5. Á síðunni **Sölulínur** skal velja aðgerðina **Sýna fylgiskjal** til að skoða færsluna.

## <a name="see-also"></a>Sjá einnig .

[Sala](sales-manage-sales.md)  
[Búa til standandi samsetningarpantanir](assembly-how-to-create-blanket-assembly-orders.md)  
[Uppsetning sölu](sales-setup-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
