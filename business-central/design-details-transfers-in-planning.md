---
title: Upplýsingar um hönnun-fært í áætlanagerð
description: Lærðu að nota flutningspantanir sem upprunaframboð þegar birgðastig eru áætlanað.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.keywords: 'design, transfer, sku, locations, warehouse'
---
# <a name="design-details-transfers-in-planning"></a>Hönnunarupplýsingar: Flutningur í áætlun

Millifærslupantanir eru einnig uppspretta framboðs þegar unnið er á birgðahaldseiningarstigi. Þegar margar staðsetningar (vöruhús) eru notaðar er hægt að stilla áfyllingarkerfi birgðahaldseininga á Flutning og gefa þannig í skyn að staðsetningin verði áfyllt með því að flytja þangað varning af annarri staðsetningu. Ef um er að ræða aðstæður með fleiri vöruhúsum gæti verið að um flutninga sé að ræða. Framboð til GRÆNNAR staðsetningar flyst úr GULU, framboð til GULU er flutt úr rauðu o. sfrv. Í upphafi keðjunnar eru Áfyllingarkerfi  **framl. pöntunar**  eða  **innkaupa**.  

![Dæmi um flutningsflæði.](media/nav_app_supply_planning_7_transfers1.png "Dæmi um flutningsflæði")  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Ef borið er saman við eftirfarandi aðstæður er ljóst að skipulagsverkefnin í seinni tíð geta orðið flókin:

* Framboðstilskipun beint frammi fyrir kröfupöntun
* Sölupöntun er gefin í gegnum keðju af be-flutningum

Ef þörf er á breytingum gæti það valdið rifa áhrifum í gegnum keðjuna. Allar flutningspantanir, auk innkaupa-og framleiðslupöntunarinnar í öfugum enda keðjunnar, verða að vera uppfærðar til endurstöðu eftirspurnar og framboðs.  

![Dæmi um stöðu framboðs- og eftirspurnar í flutningi.](media/nav_app_supply_planning_7_transfers2.png "Dæmi um stöðu framboðs- og eftirspurnar í flutningi")  

## <a name="why-is-a-transfer-a-special-case"></a>Af hverju er verið að flytja sérstakt mál?

Flutningspantanir eru svipaðar og í öðrum pöntunum, til dæmis innkaupa-og framleiðslupantanir. Þó á bak við atriðið að þeir séu ólíkir.  

Einn munur er á því að Millifærslulína táknar bæði eftirspurn og framboð. Eftirspurnarhlutinn sem afhentur er er eftirspurn. Innsendinn hluti sem berast á nýja staðnum er framboð á þeim stað.  

![Innihald flutningspöntunarsíðu.](media/nav_app_supply_planning_7_transfers3.png "Innihald flutningspöntunarsíðu")  

Þegar  [!INCLUDE [prod_short](includes/prod_short.md)]  breytist framboðhlið flutnings þarf að gera sams konar breytingu á eftirspurnarhlið.  

## <a name="transfers-are-dependent-demand"></a>Flutningar eru háðar eftirspurn

Tengsl eftirspurnar og framboðs eru svipuð íhlutum í framleiðslupöntunarlínum. Munurinn er sá að íhlutir á framleiðslupöntunarlínunum eru á næsta stigi áætlunar og hafa aðra vöru með. Tveir hlutar flutnings eru á sama stigi vegna sömu vöru.  

Mikilvæg líking er að íhlutir og flutningar séu háðar eftirspurn. Krafa úr flutningslínu er lýsingarlega útleikin eftir framboðshlið flutnings. Ef framboð breytist þá hefur eftirspurnin bein áhrif.

Ef Sveigjanleiki áætlunar er enginn þarf að meðhöndla flutningslínu sem sjálfstæða eftirspurn í áætlanagerð.  

Í skipulagsferlinu skal einungis taka tillit til flutningskröfunnar eftir að áætlanakerfi hefur unnið á framboðshliðinni. Áður en sú vinnsla gerist er raunveruleg eftirspurn ekki þekkt. Röð breytinganna er mikilvæg fyrir flutningspantanir.  

## <a name="planning-sequence"></a>Áætlunarraðar

Eftirfarandi mynd sýnir dæmi um flutning á streng.  

![Dæmi um einfalt flutningsflæði.](media/nav_app_supply_planning_7_transfers4.png "Dæmi um einfaldan flutningsflæði")  

Í þessu dæmi, viðskiptamaður pantar vöru á græna staðsetningu. Birgðageymslan GRÆNT fær tilföng með millifærslu frá miðlæga vöruhúsinu RAUTT. Aðalvöruhús RED fæst með millifærslu frá framleiðslu á staðsetningu blár.  

Í þessu dæmi byrjar áætlanakerfið á eftirspurn viðskiptavina og vinnur þannig aftur í gegnum keðjuna. Kröfur og vistir eru unnar fyrir eina staðsetningu í einu.  

![Framboðsáætlun með flutningi.](media/nav_app_supply_planning_7_transfers5.png "Framboðsáætlun með flutningi")  

## <a name="transfer-level-code"></a>Flutningsstigskóði

Flutningstigskóti be ákvarðar röðina sem áætlunarkerfið vinnur birgðageymslur fyrir.  

Kóti flutningsstigs er innri reitur. Reiturinn er reiknaður út og geymdur á BIRGÐASPJALDINU þegar BIRGÐAHALDSEINING er stofnuð eða henni breytt. Útreikningurinn keyrir yfir alla SKUs fyrir gefna samsetningu vöru og vöruafbrigða. Útreikningarnir nota birgðageymslukótann og sendist-frá-kótanum til að ákvarða leiðina til að nota fyrir SKUs. Útreikningur tryggir að allar kröfur séu unnar.  

Flutningsstigskótinn verður 0 fyrir SKUs með innkaupa-eða framl. Pöntunaráfyllingarkerfi pöntunar og verður-1 fyrir fyrsta flutningastig,-2 fyrir seinni o. s. frv. Í dæminu sem lýst er í fyrri hlutanum myndi stigin vera-1 fyrir RAUÐU og-2 fyrir grænt, eins og sést á eftirfarandi mynd.  

![Innihald síðu birgðahaldseiningaspjalds.](media/nav_app_supply_planning_7_transfers6.gif "Innihald síðu birgðahaldseiningaspjalds")  

Við uppfærslu á BIRGÐAHALDSKERFI skynjar áætlanakerfið hvort Áfyllingarkerfi fyrir SKUs eru með hringlaga tilvísunum.  

## <a name="planning-transfers-without-sku"></a>Áætlunarflutningar án SKÚTU

Fyrir minni ítarlegar vöruhúsauppsetningar er hægt að nota staðsetningar og gera handvirka flutninga milli birgðageymslna þó að ekki sé hægt að nota SKUs. Til dæmis gæti flutningurinn forað sölupöntun á þeirri birgðageymslu. Áætlanakerfið bregst við breytingum á eftirspurninni.  

Fyrir handvirka flutninga greinir áætlanakerfið flutningspantanir og áætlar síðan pöntunina sem á að vinna birgðageymslur fyrir. Fyrir innan er áætlanakerfið notað tímabundið SKUs sem er með flutningstigskóta.  

![Flutningsstigskóði.](media/nav_app_supply_planning_7_transfers7.png "Flutningsstigskóði")  

Ef nokkrir flutningar eru á stað skilgreinir fyrsta flutningspöntunin áætlunarstefnuna. Hætt er við flutningum í gagnstæða átt.  

## <a name="changing-quantity-with-reservations"></a>Breyta magni með frátekningum

Þegar magni er breytt í framboði tekur áætlanakerfið frátekningu mið af því. Frátekið magn táknar því neðri mörk fyrir hversu mikið á að draga framboðið.  

Þegar magninu í flutningspöntunarlínu er breytt þarf að hafa neðri mörkin í huga. Neðri mörkin eru hæsta frátekna magn á út-og millifærslulínum á útleið.

Til dæmis eru flutningspöntunarlínur úr 117 stykkjum teknar frá fyrir eftirtaldar línur:

* Til sölu vörulína af 46
* Í innkaupalínu 24

Jafnvel þó að innkomin hlið hafi hugsanlega umframframboð þá er ekki hægt að stytta flutningslínuna um 46.  

![Frátekningar í flutningsáætlun.](media/nav_app_supply_planning_7_transfers8.png "Frátekning í flutningsáætlun")  

## <a name="changing-quantity-in-a-transfer-chain"></a>Breyta magni í flutningskeðju

Hér er dæmi um það sem gerist þegar magni er breytt í flutningabreytingu.

Byrjunarpunktinum er jafnað með flutningskeðju með því að útvega sölupöntun 27 á staðnum RED. Tað er samsvarandi innkaupapöntun á staðnum bls. Báðir flutningar fara í gegnum staðsetningarbleikjuna. Í honum eru tvær flutningspantanir, BLÁBLEIK og BLEIK með RAUÐU.  

![Breyting á magni í flutningsáætlun 1.](media/nav_app_supply_planning_7_transfers9.png "Breyting á magni í flutningsáætlun 1")  

Nú kýs skipuleggjandi BLEIKU staðsetningarinnar að taka frá fyrir kaupin.  

![Breyting á magni í flutningsáætlun 2.](media/nav_app_supply_planning_7_transfers10.png "Breyting á magni í flutningsáætlun 2")  

Úttektin þýðir yfirleitt að áætlanakerfið hunsar innkaupapöntun og flutningseftirspurn. Það er ekkert vandamál lengi í jafnvægi. En hvað gerist þegar RAUÐ staðsetning breytist röðin úr 27 í 22?  

![Breyting á magni í flutningsáætlun 3.](media/nav_app_supply_planning_7_transfers11.png "Breyting á magni í flutningsáætlun 3")  

Þegar áætlanakerfið er keyrt aftur ætti það að losa sig við umfram framboð. Hins vegar lásu kaupin og flutningurinn í magninu 27.  

![Breyting á magni í flutningsáætlun 4.](media/nav_app_supply_planning_7_transfers12.png "Breyting á magni í flutningsáætlun 4")  

BLEIKTRAUTT pöntunin hefur verið minnkuð niður í 22. Innsendinn hluti BLÁBLEIKU flutningins er ekki frátekinn en útleiðarhlutinn er. Úttektin þýðir að ekki er hægt að minnka magnið niður 27.  

## <a name="lead-time-calculation"></a>Útreikningur afgreiðslutíma

Við útreikning á gjalddögum millifærslapönta er tekið mið af mismunandi tegundum afgreiðslutíma.  

Eftirtaldir afhendingartímar eru virkir við skipulagningu flutningspöntunarinnar:  

* Afgreiðslutími á útleið í vöruhúsi  
* Endingartími  
* Afgreiðslutími á innleið í vöruhúsi  

Eftirfarandi reitir eru notaðir í áætlunarlínunni til að veita upplýsingar um útreikninginn:  

* Sendingardagsetning afhendingar  
* Upphafsdagsetningunni  
* Lokadagsetning  
* Gjalddagi  

Afhendingardagsetning flutningslínu er sýnd í  **reitnum flutningsdagsetning**  afhendingar. Móttökudagsetning flutningslínu er sýnd í  **reitnum Gjalddagi** .  

Upphafs-og lokadagsetningar lýsa raunverulegu flutningstímabili.  

Eftirfarandi mynd sýnir túlkun Upphafsdags-tíma-og lokadagsetningar á áætlunarlínum fyrir flutningspantanir.  

![Miðlæg dagsetning-tími í flutningsáætlun.](media/nav_app_supply_planning_7_transfers13.png "Miðlæg dagsetning-tími í flutningsáætlun")  

Dæmið sýnir eftirfarandi útreikninga:  

* Afhendingardagsetning + Afgreiðsla á útleið = Upphafsdagsetning  
* Upphafsdagsetning + Afhendingartími = Lokadagsetning  
* Lokadagsetning + Afgreiðslutími inn í vöruhús = Móttökudagsetning  

## <a name="safety-lead-time"></a>Öryggisforskot

 **Reiturinn sjálfgefið öryggisforskot**  á  **síðunni Uppsetning**  framleiðslu og tengd  **tímasvæði**  öryggisleiða á  **birgðaspjaldinu**  eru ekki teknir með í útreikningum millisendingarpöntunar. Öryggisafhendingartími hefur hins vegar áhrif á heildaráætlunina. Öryggisafhendingartími hefur áhrif á áfyllingarpöntunina (innkaup eða framleiðslu) við upphaf flutningskeðjunnar. Það er punkturinn þar sem vörurnar voru settar á þann stað þaðan sem þær verða fluttar.  

![Einingar flutningsgjalddaga.](media/nav_app_supply_planning_7_transfers14.png "Einingar flutningsgjalddaga")  

Í framleiðslupöntunarlínunni Lokadagsetning + Öryggisforskot + Afgreiðslutími vara á innleið í vöruhús = Gjalddagi.  

Í innkaupapöntunarlínunni Ráðgerð móttökudagsetning + Öryggisforskot + Afgreiðslutími vara á innleið í vöruhús Áætluð móttökudagsetning.  

## <a name="reschedule"></a>Endurtímasetja

Þegar Flutningslína er endurtímasett finnur kerfið útleiðarhlutann og breytir dagsetningu-tíma.

> [!NOTE]
> Ef afhendingartími er skilgreindur þá skal vera bil á milli afhendingarinnar og kvittunar. Afhendingartími getur samanstaðið af fleiri einingum eins og flutningstíma og afgreiðslutíma vöruhúss. Í tímalínu færist áætlanakerfið aftur í tímann á meðan það stemmir einingarnar.  

![Breyting á gjalddaga í flutningsáætlun.](media/nav_app_supply_planning_7_transfers15.png "Breyting á gjalddaga í flutningsáætlun")  

Þegar gjalddögum er breytt í millisendingarlínu verður afhendingartími að vera reiknaður út til að uppfæra hlið flutnings.  

## <a name="serial-and-lot-numbers-in-transfer-chains"></a>Rað-og lotunúmer í flutningskeðjum

Ef eftirspurnin notar rað-eða lotunúmer og keyrð er áætlunarvélin, mun hún búa til flutningspantanir. Nánari upplýsingar um þetta hugtak eru í Eigindir vöru. Hins vegar, ef rað-eða lotunúmer eru fjarlægð úr eftirspurninni, eru flutningspantanir enn notaðar rað-eða lotunúmerunum og áætlun hunsar þær (ekki eytt).  

## <a name="order-to-order-links"></a>Tenglar á milli pantana

Í þessu dæmi er bláa skvísan  **sett upp með endurpöntunarstefnu pöntunar** . Hinir BLEIKU og RAUÐU SKUs hafa loið  **-fyrir-Lot**  endurpöntunarstefnuna. Sölupöntun er stofnuð fyrir 27 á staðnum RAUÐAR leiðir í keðju flutninga. Síðasti flutningurinn er á staðnum BLÁR og hann er tekinn frá með bindingum. Í þessu dæmi eru frátekningar ekki harðar frátekningar stofnaðar af skipuleggjanda á BLEIKA stað. Áætlanakerfið stofnar bindingar. Veigamesti munurinn er að áætlunarkerfið getur breytt því síðarnefnda.  

![Pöntun-til-pöntunar tenglar í flutningsáætlun.](media/nav_app_supply_planning_7_transfers16.png "Pöntun-til-pöntunar tenglar í flutningsáætlun")  

Ef eftirspurninni er breytt úr 27 í 22 þá mun áætlanakerfið lækka magnið í gegnum keðjuna. Bindingartekning er einnig minni.  

## <a name="see-also"></a>Sjá einnig

[Hönnunarupplýsingar: áætlunarfæribreyta](design-details-planning-parameters.md)   
[Hönnunarupplýsingar: áætlunartafla](design-details-planning-assignment-table.md)   
[Hönnunarupplýsingar: Meðhöndlun endurpöntunarstefna](design-details-handling-reordering-policies.md)   
[Hönnunarupplýsingar: áætlun með eða án staðsetningar](production-planning-with-without-locations.md)   
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)   
[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
