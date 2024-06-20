---
title: Upplýsingar um hönnun - Millifærslur í áætlun
description: Fræðast um notkun millifærslupantana sem framboðsuppruna þegar birgðastig eru áætluð.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.keywords: 'design, transfer, sku, locations, warehouse'
ms.service: dynamics-365-business-central
---
# <a name="design-details-transfers-in-planning"></a>Hönnunarupplýsingar: Flutningur í áætlun

Millifærslupantanir eru einnig uppspretta framboðs þegar unnið er á birgðahaldseiningarstigi. Þegar margar staðsetningar (vöruhús) eru notaðar er hægt að stilla áfyllingarkerfi birgðahaldseininga á Flutning og gefa þannig í skyn að staðsetningin verði áfyllt með því að flytja þangað varning af annarri staðsetningu. Í aðstæðum með fleiri vöruhús gæti verið til flutningakeðja. Framboð til birgðageymslunnar GRÆNT er flutt frá GULU, framboð til GULUR er flutt frá RAUÐU, og svo framvegis. Í upphafi keðjunnar er áfyllingarkerfi **Framl.pöntun eða**  **Innkaup**.  

![Dæmi um flutningsflæði.](media/nav_app_supply_planning_7_transfers1.png "Dæmi um flutningsflæði")  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Ef eftirfarandi aðstæður eru bornar saman er ljóst að áætlanagerðin í seinni tíð getur orðið flókin:

* Framboðspöntun stendur beint frammi fyrir eftirspurnarpöntun
* Sölupöntun fæst með keðju birgðahaldseiningaflutninga

Ef eftirspurnin breytist gæti það valdið gátum í gegnum keðjuna. Allar millifærslupantanir, að viðbættum innkaupa- og framleiðslupöntunum í gagnstæðum enda keðjunnar, þarf að uppfæra til að jafna eftirspurn og framboð aftur.  

![Dæmi um stöðu framboðs- og eftirspurnar í flutningi.](media/nav_app_supply_planning_7_transfers2.png "Dæmi um stöðu framboðs- og eftirspurnar í flutningi")  

## <a name="why-is-a-transfer-a-special-case"></a>Hvers vegna er um að ræða sérstakt tilfelli?

Millifærslupantanir eru svipaðar og aðrar pantanir, t.d. innkaupa- og framleiðslupantanir. Á bak við atriðið eru þeir hins vegar ólíkir.  

Einn munur er sá að millifærslulína táknar bæði eftirspurn og framboð. Sá hluti á útleið sem afhentur er eftirspurn. Sá innleiðarhluti sem móttekinn er á nýja staðnum er framboð á þeim stað.  

![Innihald flutningspöntunarsíðu.](media/nav_app_supply_planning_7_transfers3.png "Innihald flutningspöntunarsíðu")  

Þegar [!INCLUDE [prod_short](includes/prod_short.md)] birgðahlið millifærslu er breytt verður að gera svipaðar breytingar á eftirspurnarhliðinni.  

## <a name="transfers-are-dependent-demand"></a>Flutningar eru háð eftirspurn

Eftirspurn og framboðstengsl líkjast íhlutum í framleiðslupöntunarlínum. Mismunurinn er sá að íhlutir í framleiðslupöntunarlínum eru á næsta áætlunarstigi og hafa aðra vöru. Tveir hlutar millifærslunnar eru á sama stigi fyrir sömu vöru.  

Mikilvægt líkt er að íhlutir og millifærslur séu ósjálfstæð eftirspurn. Eftirspurn úr millifærslulínu ræðst af framboðshlið millifærslunnar. Ef framboðið breytist hefur eftirspurnin bein áhrif á eftirspurnina.

Ekki ætti að meðhöndla millifærslulínu sem sjálfstæða eftirspurn í áætlun nema um sveigjanleika áætlunarinnar sé að ræða.  

Í áætlunarferlinu ætti aðeins að taka tillit til millifærslueftirspurnar þegar áætlunarkerfið hefur unnið framboðshliðina. Áður en sú vinnsla gerist er ekki vitað um raunverulega eftirspurn. Röð breytinga skiptir miklu fyrir millifærslupantanir.  

## <a name="planning-sequence"></a>Áætlunarröð

Eftirfarandi mynd sýnir dæmi um flutningastreng.  

![Dæmi um einfalt flutningsflæði.](media/nav_app_supply_planning_7_transfers4.png "Dæmi um einfaldan flutningsflæði")  

Í þessu dæmi, viðskiptamaður pantar vöru á græna staðsetningu. Birgðageymslan GRÆNT fær tilföng með millifærslu frá miðlæga vöruhúsinu RAUTT. Aðalvöruhús RED fæst með millifærslu frá framleiðslu á staðsetningu blár.  

Í þessu dæmi byrjar áætlunarkerfið á eftirspurn viðskiptamannsins og vinnur leiðina aftur í gegnum keðjuna. Eftirspurn og birgðir eru unnin í einni birgðageymslu í einu.  

![Framboðsáætlun með flutningi.](media/nav_app_supply_planning_7_transfers5.png "Framboðsáætlun með flutningi")  

## <a name="transfer-level-code"></a>Flutningsstigskóði

Flutningsstigskóti birgðahaldseiningarinnar ákvarðar í hvaða röð áætlunarkerfið vinnur birgðageymslur.  

Kóti flutningsstigsins er innri reitur. Reiturinn er reiknaður og geymdur í birgðahaldseiningunni þegar birgðahaldseiningin er stofnuð eða því breytt. Útreikningarnir eru keyrðir í öllum birgðaeiningum fyrir tiltekna samsetningu vöru og vöruafbrigðis. Útreikningurinn notar birgðageymslukótann og sendist-frá kótann til að ákvarða leiðina sem á að nota fyrir birgðaeiningarnar. Útreikningurinn tryggir að allar eftirspurn sé unnin.  

Flutningsstigskótinn verður 0 fyrir birgðahaldseiningar með Innkaupa- eða Framl.pöntunaráfyllingarkerfi, og verður -1 fyrir fyrsta flutningsstigið, -2 fyrir það annað, og svo framvegis. Í dæminu sem lýst er í fyrri hlutanum yrðu stigin -1 fyrir RAUTT og -2 fyrir GRÆNT, eins og sýnt er í eftirfarandi mynd.  

![Innihald síðu birgðahaldseiningaspjalds.](media/nav_app_supply_planning_7_transfers6.gif "Innihald síðu birgðahaldseiningaspjalds")  

Þegar birgðahaldseining er uppfærð finnur áætlunarkerfið hvort áfyllingarkerfi fyrir birgðahaldseiningar eru með hringvirkar tilvísanir.  

## <a name="planning-transfers-without-sku"></a>Áætlunarflutningar án birgðahaldseininga

Fyrir minna ítarlegri vöruhúsauppsetningar er hægt að nota birgðageymslur og færa handvirkar millifærslur milli birgðageymslna, jafnvel þótt ekki séu notaðar birgðahaldseiningar. Til dæmis gæti flutningurinn náð til sölupöntunar í þeirri birgðageymslu. Áætlunarkerfið bregst við breytingum á eftirspurninni.  

Fyrir handvirkar millifærslur greinir áætlunarkerfið millifærslupantanir og áætlar svo í hvaða röð á að vinna birgðageymslurnar. Í innri vinnslu notar áætlunarkerfið bráðabirgða birgðahaldseiningar sem hafa flutningsstigskóta.  

![Flutningsstigskóði.](media/nav_app_supply_planning_7_transfers7.png "Flutningsstigskóði")  

Ef nokkrar millifærslur eru til birgðageymslu skilgreinir fyrsta millifærslupöntunin áætlunarstefnuna. Hætt er við flutning í gagnstæða átt.  

## <a name="changing-quantity-with-reservations"></a>Breyta magni með frátekningum

Þegar magni er breytt í birgðum tekur áætlunarkerfið frátekningar með í reikninginn. Frátekið magn stendur fyrir neðri mörkin fyrir hversu mikið þarf að minnka framboðið.  

Þegar magninu er breytt í millifærslupöntunarlínu skal hafa neðri mörkin í huga. Neðri mörkin er hæsta frátekna magnið í millifærslulínum á útleið og innleið.

Til dæmis er millifærslupöntunarlína með 117 stykkjum tekin frá fyrir eftirfarandi línur:

* Sölulína 46
* Innkaupalína 24

Jafnvel þó að umframbirgðir á innleið sé umframbirgðir er ekki hægt að minnka millifærslulínuna undir 46.  

![Frátekningar í flutningsáætlun.](media/nav_app_supply_planning_7_transfers8.png "Frátekning í flutningsáætlun")  

## <a name="changing-quantity-in-a-transfer-chain"></a>Magni breytt í millifærslukeðju

Hér er dæmi um hvað gerist þegar magni er breytt í millifærslubreytingu.

Upphafspunkturinn er jafnvægisstaða með millifærslukeðju sem útvegar sölupöntun 27 á staðnum RAUTT. Það er samsvarandi innkaupapöntun í birgðageymslunni BLÁTT. Báðar millifærslur fara í gegnum staðsetningu BLEIKT. Um er að ræða tvær millifærslupantanir, BLÁBLEIKT og BLEIKT-RAUTT.  

![Breyting á magni í flutningsáætlun 1.](media/nav_app_supply_planning_7_transfers9.png "Breyting á magni í flutningsáætlun 1")  

Skipuleggjandi í birgðageymslunni BLEIKT kýs að taka frá fyrir innkaupin.  

![Breyting á magni í flutningsáætlun 2.](media/nav_app_supply_planning_7_transfers10.png "Breyting á magni í flutningsáætlun 2")  

Frátekning þýðir yfirleitt að áætlunarkerfið hunsar innkaupapöntunina og millifærslueftirspurnina. Það er ekki vandamál á meðan innistæða er. En hvað gerist þegar staðsetningin RAUTT breytist úr 27 í 22?  

![Breyting á magni í flutningsáætlun 3.](media/nav_app_supply_planning_7_transfers11.png "Breyting á magni í flutningsáætlun 3")  

Þegar áætlanakerfið er keyrt aftur ætti það að losa sig við umfram framboð. Hins vegar læsir frátekningin innkaupunum og millifærslunni í magnið 27.  

![Breyting á magni í flutningsáætlun 4.](media/nav_app_supply_planning_7_transfers12.png "Breyting á magni í flutningsáætlun 4")  

BLEIKTRAUTT pöntunin hefur verið minnkuð niður í 22. Innleiðarhluti millifærslunnar BLÁTT-BLEIKT er ekki frátekinn en útleiðarhlutinn er. Frátekningin merkir að ekki er hægt að minnka magnið undir 27.  

## <a name="lead-time-calculation"></a>Útreikningur afhendingartíma

Þegar skiladagsetning millifærslupöntunar er reiknuð er tekið tillit til ýmiss konar afhendingartíma.  

Eftirfarandi afhendingartímar eru virkir þegar millifærslupöntun er áætluð:  

* Afgreiðslutími á vörum út úr vöruhúsi  
* Afhendingartími  
* Afgreiðslutími á vörum inn í vöruhús  

Í áætlunarlínunni eru eftirfarandi reitir notaðir til að veita upplýsingar um útreikninginn:  

* Flutningsdagsetning afhendingar  
* Upphafsdagsetning  
* Lokadagsetning  
* Eindagi  

Afhendingardagsetning millifærslulínunnar er sýnd í reitnum **Millifærsluafhendingardags** . Móttökudagsetning millifærslulínunnar er sýnd í reitnum **Gjalddagi** .  

Upphafs- og lokadagsetningar lýsa sjálfu flutningstímabilinu.  

Eftirfarandi mynd sýnir túlkun upphafsdagsetningar- og lokadagsetningar-tíma á áætlunarlínum fyrir millifærslupantanir.  

![Miðlæg dagsetning-tími í flutningsáætlun.](media/nav_app_supply_planning_7_transfers13.png "Miðlæg dagsetning-tími í flutningsáætlun")  

Dæmið sýnir eftirfarandi útreikninga:  

* Afhendingardagsetning + Afgreiðsla á útleið = Upphafsdagsetning  
* Upphafsdagsetning + Afhendingartími = Lokadagsetning  
* Lokadagsetning + Afgreiðslutími inn í vöruhús = Móttökudagsetning  

## <a name="safety-lead-time"></a>Öryggisforskot

Reiturinn **Sjálfgefinn öryggisforskot** á síðunni **Uppsetning** framleiðslu og tengdur **öryggisforskot** á síðunni **Birgðaspjald** eru ekki teknir með í útreikningum á millifærslupöntunum. Hins vegar hefur öryggisforskot áhrif á heildaráætlunina. Öryggisforskotið hefur áhrif á áfyllingarpöntun (innkaup eða framleiðslu) í upphafi millifærslukeðjunnar. Þá eru vörurnar settar í birgðageymsluna sem þær verða fluttar frá.  

![Einingar flutningsgjalddaga.](media/nav_app_supply_planning_7_transfers14.png "Einingar flutningsgjalddaga")  

Í framleiðslupöntunarlínunni Lokadagsetning + Öryggisforskot + Afgreiðslutími vara á innleið í vöruhús = Gjalddagi.  

Í innkaupapöntunarlínunni Ráðgerð móttökudagsetning + Öryggisforskot + Afgreiðslutími vara á innleið í vöruhús Áætluð móttökudagsetning.  

## <a name="reschedule"></a>Enduráætla

Þegar millifærslulína er endurtímasett finnur áætlunarkerfið útleiðarhlutann og breytir dagsetningunni-tíminn.

> [!NOTE]
> Ef afhendingartími er skilgreindur verður bil milli afhendingar og móttöku. Í afgreiðslutíma geta verið fleiri einingar, svo sem flutningstími og afgreiðslutími í vöruhúsi. Á tímalínu færist áætlunarkerfið aftur í tímann á meðan það stemmir einingarnar.  

![Breyting á gjalddaga í flutningsáætlun.](media/nav_app_supply_planning_7_transfers15.png "Breyting á gjalddaga í flutningsáætlun")  

Þegar gjalddaga er breytt í millifærslulínu verður að reikna út afhendingartímann til að uppfæra útleiðarhlið millifærslunnar.  

## <a name="serial-and-lot-numbers-in-transfer-chains"></a>Rað- og lotunúmer í millifærslukeðjum

Ef eftirspurnin notar rað- eða lotunúmer og áætlunarvélin er keyrð stofnar hún millifærslupantanir. Nánari upplýsingar um þetta hugtak eru í Eigindir vöru. Ef hins vegar rað- eða lotunúmer eru fjarlægð af eftirspurninni þá nota millifærslupantanirnar samt rað- eða lotunúmerin og áætlunin þá hunsa þau (ekki eytt).  

## <a name="order-to-order-links"></a>Tenglar á milli pantana

Í þessu dæmi er BLÁTT birgðahaldseining sett upp með **pöntunar** endurpöntunarstefnu. BLEIKI og RAUÐU SKUs eru með endurpöntunarstefnuna **Lota fyrir lotu** . Stofnun sölupöntunar fyrir 27 á staðnum RAUTT leiðir til millifærslukeðju. Síðasta flutningurinn er í birgðageymslunni BLÁTT og hann er tekinn frá með bindingu. Í þessu dæmi eru frátekningarnar ekki erfiðar frátekningar sem skipuleggjandi býr til á BLEIKum stað. Áætlunarkerfið stofnar bindingarnar. Veigamesti munurinn er að áætlunarkerfið getur breytt því síðarnefnda.  

![Pöntun-til-pöntunar tenglar í flutningsáætlun.](media/nav_app_supply_planning_7_transfers16.png "Pöntun-til-pöntunar tenglar í flutningsáætlun")  

Ef eftirspurninni er breytt úr 27 í 22 lækkar áætlunarkerfið magnið um keðjuna. Bindandi frátekning er einnig lækkuð.  

## <a name="see-also"></a>Sjá einnig

[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)   
[Hönnunarupplýsingar: áætlunartafla](design-details-planning-assignment-table.md)   
[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
[Hönnunarupplýsingar: Áætlanir með eða án birgðageymslna](production-planning-with-without-locations.md)   
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfis](design-details-central-concepts-of-the-planning-system.md)   
[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
