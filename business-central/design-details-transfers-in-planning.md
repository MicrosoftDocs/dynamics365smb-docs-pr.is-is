---
title: Hönnunarupplýsingar - Flutningur í áætlun | Microsoft Docs
description: Þetta efnisatriði lýsir því hvernig á að nota flutningspantanir sem uppsprettu framboðs þegar verið er að áætla birgðastig.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, transfer, sku, locations, warehouse
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 72755bb2b83a3560c79cd004987003d3d7585f6b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381568"
---
# <a name="design-details-transfers-in-planning"></a>Hönnunarupplýsingar: Flutningur í áætlun
Millifærslupantanir eru einnig uppspretta framboðs þegar unnið er á birgðahaldseiningarstigi. Þegar margar staðsetningar (vöruhús) eru notaðar er hægt að stilla áfyllingarkerfi birgðahaldseininga á Flutning og gefa þannig í skyn að staðsetningin verði áfyllt með því að flytja þangað varning af annarri staðsetningu. Í aðstæðum með fleiri vöruhús, fyrirtæki gætu haft keðju flutnings þar sem framboð til grænar staðsetningar er flutt frá gulum og framboð til gulra er flutt úr rauðum og svo framvegis. Í upphafi af keðjunni er áfyllingarkerfi Framl.pöntun eða innkaup.  

![Dæmi um flutningsflæði](media/nav_app_supply_planning_7_transfers1.png "Dæmi um flutningsflæði")  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Við samanburð á ástandinu þar sem birgðapöntun er beint á móti eftirspurnarpöntun við aðstæður þar sem sölupöntun er veitt í gegnum keðju af birgðahaldseiningum, er augljóst að áætlanagerð getur verið mjög flókin í sennna tilvikinu. Ef eftirspurn breytist gæti það valdið keðjuverkun gegnum keðjuna, vegna þess að vinna verður með allar millifærslupantanir auk innkaupa-/framleiðslupöntunarinnar á hinum enda keðjunnar til að koma aftur á jafnvægi milli eftirspurnar og framboðs.  

![Dæmi um stöðu framboðs- og eftirspurnar í flutningi](media/nav_app_supply_planning_7_transfers2.png "Dæmi um stöðu framboðs- og eftirspurnar í flutningi")  

## <a name="why-is-transfer-a-special-case"></a>Hvers vegna er millifærsla sérstakt tilfelli?  
Millifærslupöntun lítur svipað út eins aðrar pantanir í forritinu. Hins vegar er þetta mjög ólíkt á bak við tjöldin.  

Eitt grundvallaratriði sem greinir millifærslur í áætlun frá innkaupa- og framleiðslupöntununum er að millifærslulína stendur samtímis fyrir eftirspurn og framboð. Sá hluti sem er á útleið, sem er fluttur af fyrri staðsetningunni, er eftirspurnin. Hlutinn á innleið, sem á að taka við á nýju staðsetningunni, er birgðir á þeirri staðsetningu.  

![Innihald flutningspöntunarsíðu](media/nav_app_supply_planning_7_transfers3.png "Innihald flutningspöntunarsíðu")I  

Þetta þýðir að þegar kerfið vinnur á framboðshlið flutningsins, verður það að gera svipaða breytingu á eftirspurnarhlið.  

## <a name="transfers-are-dependent-demand"></a>Millifærslur eru háðar Eftirspurn  
Tengd eftirspurn og birgðir hafa einhver líkindi með íhlutum framleiðslupöntunarlínu en munurinn er sá að íhlutir verða á næsta áætlanastigi og tengjast annarri vöru en millifærsluhlutarnir tveir eru staðsettir á sama stigi og fyrir sömu vöru.  

Mikilvæg líkindi eru að íhlutir eru bæði háðir eftirspurn og flutningseftirspurn. Eftirspurn frá millifærslulínu er ráðist af framboðshlið millifærslu í þeim skilningi að ef framboð er breytt, að eftirspurn er fyrir beinum áhrifum.  

Nema sveigjanleiki áætlunar sé enginn, ætti millifærslulína aldrei að meðhöndla eins og sjálfstæða eftirspurn í áætlanagerð.  

Í áætlanaferli er flutningseftirspurn aðeins að taka tillit til þegar framboðshlið hefur verið unnin af áætlanakerfi. Áður en þetta, er raunveruleg eftirspurn ekki þekkt. Röð breytinga er af þeim sökum mjög mikilvæg hvað varðar flutningspantanir.  

## <a name="planning-sequence"></a>Áætlunarröð  
Eftirfarandi mynd sýnir hvernig millifærslustrengur gæti litið út.  

![Dæmi um einfalt flutningsflæði](media/nav_app_supply_planning_7_transfers4.png "Dæmi um einfaldan flutningsflæði")  

Í þessu dæmi, viðskiptamaður pantar vöru á græna staðsetningu. Birgðageymslan GRÆNT fær tilföng með millifærslu frá miðlæga vöruhúsinu RAUTT. Aðalvöruhús RED fæst með millifærslu frá framleiðslu á staðsetningu blár.  

Í þessu dæmi er áætlanakerfi mun byrja á viðskiptamannseftirspurn og vinna sig aftur í gegnum keðju. Kröfur og birgðir verða meðhöndlaðar á eina staðsetningu í einu.  

![Framboðsáætlun með flutningi](media/nav_app_supply_planning_7_transfers5.png "Framboðsáætlun með flutningi")  

## <a name="transfer-level-code"></a>Flutningsstigskóði  
Röðin sem staðsetningar eru unnar í áætlanakerfinu er ákveðin af flutningsstigskóðanum í birgðahaldseiningunni.  

Flutningsstigskóði er innri reitur sem er reiknaður sjálfkrafa og vistaður í birgðahaldseiningunni þegar hún er stofnuð eða henni breytt. Útreikningur nær yfir allt BHE fyrir tiltekið samsetningu vöru/afbrigðis og notar staðsetningarkóðann og millifærslukóða til að ákvarða leiðina sem áætlun verður að nota í gegnum BHE til að tryggja að allar kröfur eru afgreidd.  

Flutningsstigskóði verður 0 fyrir birgðahaldseiningar með áfyllingarkerfi, Innkaupa- eða Framl.pöntun og verður -1 fyrir fyrsta flutningsstigið, -2 fyrir það næsta o.s.frv. Í flutningskeðju sem lýst er hér að ofan, stigið væri því -1 fyrir rautt og -2 til Green, eins og sést á eftirfarandi mynd.  

![Innihald síðu birgðahaldseiningaspjalds](media/nav_app_supply_planning_7_transfers6.gif "Innihald síðu birgðahaldseiningaspjalds")  

Þegar birgðahaldseining er endurnýjuð greinir áætlanakerfið hvort birgðahaldseiningar með uppsettu áfyllingarkerfi millifærsla eru settar upp með hringlaga tilvísunum.  

## <a name="planning-transfers-without-sku"></a>Áætlun millifærslna án BHE  

Jafnvel þótt birgðahaldseiningareiginleikinn sé ekki notaður er hægt að nota staðsetningar og gera handvirkan flutning milli staðsetninga. Fyriri fyrirtæki með einfaldari vöruhúsauppsetningu styður áætlunargerðarkerfið aðstæður þar sem fyrirliggjandi birgðir eru fluttar handvirkt á annan stað, til dæmis til að sinna sölupöntun á þeim stað. Á sama tíma, ætti áætlanakerfið að bregðast við breytingum í eftirspurn.  

Til að styðja handvirka millifærslur greinir áætlunargerðin núverandi flutningspöntun og svo skipuleggur í hvaða röð á að vinna staðsetningar. Innbyrðis, mun áætlanakerfið stýra bráðabirgða birgðahaldseiningum sem innihalda flutningsstigskóða.  

![Flutningsstigskóði](media/nav_app_supply_planning_7_transfers7.png "Flutningsstigskóði")  

Ef fleiri millifærslur á tiltekinn stað eru til staðar skilgreinir fyrsta millifærslupöntunin áætlunarstefnuna. Millifærslur sem keyra í  í gagnstæða átt verður eytt.  

## <a name="changing-quantity-with-reservations"></a>Breyting magni með frátekningum  
Þegar breyta á  magni af núverandi framboð,tekur  áætlanagerð tillit til frátekninga í þeim skilningi að fráteknið magn táknar neðri mörk fyrir hversu mikið framboð er hægt að minnka.  

Þegar breyta á magn á núverandi flutningspöntunarlína, hafa í huga að neðri mörk verður skilgreint sem hæsta frátekna magn á útleiðar og innleiðar flutningslínu  

Til dæmis ef flutningspöntunarlína 117 hluta er frátekin á sölulínu með 46 og innkaupalínu með 24 er ekki hægt að lækka flutningslínuna undir 46 hluti jafnvel þótt þetta gæti endurspeglað umframframboð á innleiðarhlið.  

![Frátekning í flutningsáætlun](media/nav_app_supply_planning_7_transfers8.png "Frátekning í flutningsáætlun")  

## <a name="changing-quantity-in-a-transfer-chain"></a>Breyting á magni í flutningskeðju  
Í eftirfarandi dæmi er upphafið er jöfnuð  staða með flutningskeðju sem býður sölupöntun með 27 á rauðri staðsetningu með samsvarandi innkaupapöntun á staðsetningunni Blá, flutt á staðsetninguna Bleikt. Því eru tvær flutningspantanir, fyrir utan sölu og kaup: BLÁTT-BLEIKT og BLEIKT-RAUTT.  

![Breyting á magni í flutningsáætlun 1](media/nav_app_supply_planning_7_transfers9.png "Breyting á magni í flutningsáætlun 1")  

Nú velur áætlun í birgðageymslunni BLEIKT frátekt á móti innkaupum.  

![Breyting á magni í flutningsáætlun 2](media/nav_app_supply_planning_7_transfers10.png "Breyting á magni í flutningsáætlun 2")  

Þetta þýðir yfirleitt að áætlanakerfi mun hunsa innkaupapöntun og flytja eftirspurn. Svo lengi sem staða er fyrir hendi er ekkert vandamál. En hvað gerist þegar viðskiptavinur á RAUÐUM stað breytir pöntun sinni í 22?  

![Breyting á magni í flutningsáætlun 3](media/nav_app_supply_planning_7_transfers11.png "Breyting á magni í flutningsáætlun 3")  

Þegar áætlanakerfið er keyrt aftur ætti það að losa sig við umfram framboð. Hins vegar læsir frátekningin kaupunum og yfirfærir svo í magnið 27.  

![Breyting á magni í flutningsáætlun 4](media/nav_app_supply_planning_7_transfers12.png "Breyting á magni í flutningsáætlun 4")  

BLEIKTRAUTT pöntunin hefur verið minnkuð niður í 22. Sá hluti af BLÁTTBLEIKT tilfærslunni sem er á innleið er ekki frátekinn en þar sem hlutinn á útleið er frátekinn er ekki hægt að minnka magnið niður fyrir 27.  

## <a name="lead-time-calculation"></a>Útreikn. afhendingartíma  
Við útreikning á skiladegi flutningspöntunar er tekið mið af mismunandi tegundir af afhendingartíma.  

Afhendingartímar sem eru virkir þegar millifærslupöntun er áætluð eru:  

* Afgreiðslutími á vörum út úr vöruhúsi  
* Afhendingartími  
* Afgreiðslutími á vörum inn í vöruhús  
* Á áætlunarlínunni eru eftirfarandi reitir notaðir til að veita upplýsingar um útreikninginn.  
* Afh.dags. millifærslu  
* Upphafsdagsetning  
* Lokadagsetning  
* Skiladagur  

Afhendingardagur flutningslínunnar verður sýnd í reitnum Dagsetning flutningsafhendingar og móttökudagsetning flutningslínunnar er sýnd í reitnum Skiladagur.  

Upphafs- og lokadagsetningar verða notaðar til að lýsa raunverulegu flutningstímabili.  

Eftirfarandi mynd sýnir túlkun á tíma upphafsdagsetningar og tíma lokadagsetningar á áætlanagerðarlínum sem tengjast millifærslupöntunum.  

![Miðlæg dagsetning-tími í flutningsáætlun](media/nav_app_supply_planning_7_transfers13.png "Miðlæg dagsetning-tími í flutningsáætlun")  

Í þessu dæmi, þýðir það að:  

* Afhendingardagsetning + Afgreiðsla á útleið = Upphafsdagsetning  
* Upphafsdagsetning + Afhendingartími = Lokadagsetning  
* Lokadagsetning + Afgreiðslutími inn í vöruhús = Móttökudagsetning  

## <a name="safety-lead-time"></a>Öryggisforskot  
Reiturinn Sjálfgefið öryggisforskot á síðunni Uppsetning framleiðslu og tengdi reiturinn Öryggisforskot á vöruspjaldinu mun ekki taka tillit til við útreikning á að millifærslupöntun. Hins vegar hefur öryggisafhendingartíminn áfram áhrif á heildaráætlunina eins og hann hefur áhrif á áfyllingarpöntunina (kaup eða framleiðslu) í upphafi flutningskeðjunnar þegar vörurnar eru settar á staðinn þaðan sem þær verða fluttar.  

![Einingar flutningsgjalddaga](media/nav_app_supply_planning_7_transfers14.png "Einingar flutningsgjalddaga")  

Í framleiðslupöntunarlínunni Lokadagsetning + Öryggisforskot + Afgreiðslutími vara á innleið í vöruhús = Gjalddagi.  

Í innkaupapöntunarlínunni Ráðgerð móttökudagsetning + Öryggisforskot + Afgreiðslutími vara á innleið í vöruhús Áætluð móttökudagsetning.  

## <a name="reschedule"></a>Endurtímasetja  
Þegar fyrirliggjandi flutningslína er enduráætluð verður áætlanakerfi að fletta upp hlutanum á útleið og breyta dagsetningu og tíma hans. Mikilvægt er að hafa í huga að ef afhendingartími hefur tilgreindur verður bil á milli afhendignar og móttöku. Eins og fyrr segir getur afhendingartími samanstaðið af fleiri einingum, eins og flutningstíma og meðhöndlunartíma í vöruhúsi. Á tímalínu mun áætlanakerfið fara aftur í tímann á með það jafnar stöðu eininganna.  

![Breyting á gjalddaga í flutningsáætlun](media/nav_app_supply_planning_7_transfers15.png "Breyting á gjalddaga í flutningsáætlun")  

Þegar gjalddaga er því breytt á flutningslínu þarf afhendingartími að vera reiknaður til að hægt sé að uppfæra þann hluta færslunnar sem er á útleið.  

## <a name="seriallot-numbers-in-transfer-chains"></a>Rað-/Lotunúmer í millifærslukeðjum  
Ef eftirspurn er með raðnúmer/lotunúmer og áætlunarvélin er keyrð leiðir það til þess að millifærslupantanir eru stofnaðar beint. Nánari upplýsingar um þetta hugtak eru í Eigindir vöru. Ef hins vegar raðnúmer / lotunúmeri eru fjarlægð úr eftirspurn, skapað flutningspantanir í keðjunni mun enn bera raðnúmer / lotunúmeri og mun því vera hunsuð af áætlanagerð (ekki eytt).  

## <a name="order-to-order-links"></a>Tenglar á milli pantana  
Í þessu dæmi, blá birgðahaldseining er sett upp við röð endurpöntunarstefnu, en bleikur og rauður nota Lotu -fyrir-Lotu. Þegar sölupöntun upp á 27 er búin til á rauðri staðsetningu mun það leiða til flutningskeðju með síðasta sameiginlega lið á blárri staðsetningu með frátekningu með bindingu. Í þessu dæmi, eru frátekningar ekki harðar frátekningar búnar til af skipuleggjandi á bleikum stað, heldur bindingar búnar til af áætlanakerfinu. Veigamesti munurinn er að áætlunarkerfið getur breytt því síðarnefnda.  

![Pöntun-til-pöntunar tenglar í flutningsáætlun](media/nav_app_supply_planning_7_transfers16.png "Pöntun-til-pöntunar tenglar í flutningsáætlun")  

Ef eftirspurn er breytt úr 27 í 22 lækkar kerfið magnið niður í gegnum keðjuna, og bindandi frátekning er einnig minnkuð.  

## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Áætlunarfæribreytur](design-details-planning-parameters.md)   
[Hönnunarupplýsingar: áætlunartafla](design-details-planning-assignment-table.md)   
[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
[Hönnunarupplýsingar: Eftirspurn í birgðageymslunni TÓMT](design-details-demand-at-blank-location.md)   
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)   
[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]