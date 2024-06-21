---
title: Leiðir stofnaðar
description: 'Þessi grein gefur yfirlit yfir mismunandi leiðir til að búa til leiðir, þ.m.t. skilyrði sem þarf og hvernig á að búa til leiðartengla.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '99000764, 99000765, 99000766, 99000767, 99000794, 99000796, 99000798, 99000806, 99000808, 99000810, 99000817, 99000834, 99000835, 99000836, 99000837, 99000840, 99000841, 99000844, 99000845'
ms.date: 06/06/2024
ms.service: dynamics-365-business-central
---
# Leiðir stofnaðar

Framleiðslufyrirtæki nota leiðir til að stýra framleiðsluferlinu og gera sýnilegt.

Leiðin er grunnurinn að vinnsluáætlun, áætlun um afköst og áætlaðri úthlutun á efnisþörf og framleiðsluskjölum.  

Leiðunum er úthlutað á framleiðsluvöruna eins og fyrir framleiðsluuppskriftirnar. Leið hefur að geyma aðalgögn sem skráir ferlisþarfir vara. Þegar framleiðslupöntun hefur verið stofnuð fyrir vöru stjórnar hún tímasetningu aðgerða eins og fram kemur á **síðunni Leið** framl.pöntunar undir framleiðslupöntuninni.  

Áður en hægt er að setja upp leið verða eftirfarandi uppsetningar að vera á staðnum:  

- Birgðaspjöld er búin til fyrir yfirvörur sem taka þátt í framleiðslu. Nánari upplýsingar eru skráðar í [Nýjar vörur](inventory-how-register-new-items.md).
- Framleiðsluforði eru uppsettur. Nánari upplýsingar eru settar [upp vinnustöðvar og vélastöðvar](production-how-to-set-up-work-and-machine-centers.md).

## Stofna leið

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Leiðir** og velja síðan viðkomandi tengil.  
2. Valið er aðgerðin **Nýtt**.  
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Í reitnum **Tegund** er valinn einn af eftirfarandi kostum:
   - **Raðað** til að reikna framleiðsluleiðina samkvæmt gildinu í reitnum Aðgerðarnr **.** .  
   - Veljið **Samhliða** til að reikna aðgerðir samkvæmt gildinu í reitnum **Næsta aðgerðarnr.** .  
5. Reiturinn **Staða** verður að vera stilltur á **Ný** eða **Í þróun** svo hægt sé að breyta leið.  

    Halda áfram til að fylla út í leiðarlínur.
6. Í **Aðgerð Nr.**. reitinn er fært inn númer fyrstu aðgerðarinnar, t.d. **10**.  
7. Í reitnum **Tegund** er valið hvers konar forði er notaður, t.d. **Vinnustöð**.  
8. Í reitnum **númer** er forðinn sem á að nota valinn eða hann sleginn inn í reitinn.  
9. Í reitnum **Leiðartengilskóti** er hægt að slá inn kóta til að tengja íhlut við ákveðna aðgerð. Frekari upplýsingar er að finna í [Að stofna leiðartengla](production-how-to-create-routings.md#to-create-routing-links).
10. Í reitunum **Keyrslutími** og **Uppsetn.tími** er færðir inn þeir vinnslutímar þarf til að framkvæma aðgerð.

     > [!NOTE]
     > Uppsetningartími er reiknaður fyrir hverja framleiðslupöntun en keyrslutími fyrir hverja framleidda vöru.  

11. Í reitnum **Samþætt afkastageta** er tilgreint hversu margar einingar valda forðans eru notaðar til að framkvæma aðgerð. Ef t.d. tvær manns er úthlutað á eina pökkunaraðgerð helmar keyrslutíminn.  
12. Haldið er áfram að fylla út línur fyrir allar aðgerðir sem koma við sögu í framleiðslu viðkomandi vöru.  
13. Línur úr fyrirliggjandi leið eru afritaðar með því að smella á **Afrita leiðir** aðgerðina til að velja línur sem eru til.  
14. Til að virkja leiðina skal velja **Vottað**  í reitnum **Staða**.  
15. Nú er hægt að hengja nýju leiðina við spjald viðkomandi framleiðsluvöru, með því að fylla upp í reitinn **Leið nr.**. Nánari upplýsingar eru skráðar í [Nýjar vörur](inventory-how-register-new-items.md).  

> [!NOTE]  
> Muna þarf að endurreikna staðlað kostnaðarverð vörunnar af **birgðaspjaldinu** . Veljið aðgerðina **Framleiðsla**, aðgerðina **Reikna staðlað kostnaðarverð** og veljið svo aðgerðina **Öll stig** .  

## Leiðartenglar stofnaðir

Hægt er að búa til leiðartengla til að tengja íhluti við ákveðnar aðgerðir til að viðhalda sambandi þeirra jafnvel þótt framleiðsluuppskriftinni eða leiðinni sé breytt. Leiðartenglar auðvelda einnig tímanlega birgðaskráningu íhluta, þ.e. þegar tiltekin tengd aðgerð hefst, ekki þegar heildarframleiðslupöntunin er gefin út. Nánari upplýsingar eru notaðar með því að fara í [Birgðaskráning íhluta eftir frálagi aðgerðar](production-how-to-flush-components-according-to-operation-output.md).  

Annar mikilvægur ávinningur er sá að tengdir íhlutir og aðgerðir sýna í rökrænni uppbyggingu framvindu þegar síðan Framleiðslubók **er notuð** til að bóka frálag og notkun.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Leiðir** og velja síðan viðkomandi tengil.  
2. Opna skal leiðina með aðgerðunum sem á að tengja.  

    Tryggja þarf að staða leiðar sé **Í þróun**.  

3. Á viðkomandi leiðarlínu í reitnum **Leiðartengilskóti** skal velja kóta.  
4. Mismunandi leiðartengilskótum er bætt við aðrar aðgerðir í leiðinni, ef við á.  

    > [!NOTE]  
    > Ekki ætti að nota sama leiðartengilskótann í mismunandi aðgerðum á leið því ranglega er hægt að tengja íhlut við tvær mismunandi aðgerðir svo að hann sé notaður tvisvar sinnum.  
    >
    > Mælt er með því að nefna leiðartengilskótann eftir aðgerðinni til að tryggja sértæka leiðartengla fyrir aðgerðir.

5. Staða leiðar er stillt á **Vottað**.  

    Leiðartenglakótar eru nú tengdir við aðgerðir. Næst skal stofna sjálfan tengilinn með því að úthluta sömu kótum á tiltekna íhluti í viðeigandi framleiðsluuppskrift.  

6. Opna skal **framleiðsluuppskriftina** sem inniheldur íhlutina sem á að tengja við ofantaldar aðgerðir. Nánari upplýsingar eru notaðar með því að fara í Búa til [framl.uppskriftir](production-how-to-create-production-boms.md).
7. Tryggja þarf að uppskriftin sé stillt á **Í þróun**.  
8. Í viðkomandi framleiðsluuppskriftarlínu í reitnum **Leiðartengilskóti** er valinn kótinn sem aðgerðinni var úthlutað.  
9. Þvínæst er leiðartengilskótum bætt við aðra íhluti í samræmi við einstakar aðgerðir þar sem þeir eru notaðir.  
10. Staða framleiðsluuppskriftar er stillt á **Vottað**.  

    > [!NOTE]  
    > Til að virkja leiðartengla í framleiðslupöntun sem þegar er til þarf fyrst að endurnýja hana. Nánari upplýsingar eru notaðar með því að fara á Búa til [framleiðslupantanir](production-how-to-create-production-orders.md).  

Valdir íhlutir eru nú tengdir við valdar aðgerðir þegar framleiðslupöntun er stofnuð eða endurnýjuð með framleiðsluuppskrift og leið. Þessi tengill sést á síðunni **Íhlutir** framl.pöntunar undir framleiðslupöntuninni. Hægt er að fjarlægja og bæta við leiðartengilskótum hvenær sem er.

## Úthluta starfsmönnum, verkfærum og gæðaráðstöfunum til leiðaraðgerðir

Ef krafist er starfsmanna með sérþekkingu eða sérstaka heimild fyrir aðgerðinni má úthluta viðkomandi starfsmönnum á aðgerðina. Að auki geturðu úthlutað verkfærum og gæðaráðstöfunum til aðgerðarinnar. Þetta ferli lýsir því hvernig skal úthluta starfsmönnum. Skrefin eru svipuð fyrir aðrar gerðir aðgerðaupplýsinga.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Leiðir** og velja síðan viðkomandi tengil.  
2. Viðeigandi leið er opnuð.  
3. Á flýtiflipanum **Línur** skal velja línuna sem á að vinna úr og svo velja aðgerðina **Virkni** og svo aðgerðina **Starfsmenn**.  
4. Reitirnir á síðunni **Starfsmenn leiðar** eru fylltir út.  
5. Velja hnappinn **Í lagi** til að hætta á síðunni. Innfærð gildi eru afrituð og úthlutuð aðgerðinni.  

## Ný útgáfa af leið búin til

Með útgáfureglunni er hægt að fást við margar útgáfur. Skipulag leiðaútgáfunnar samsvarar skipulagi leiðarinnar sem felur í sér leiðaútgáfuhaus og leiðaútgáfulínur. Upphafsdagsetningin skilgreinir grundvallarmuninn.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Leiðir** og velja síðan viðkomandi tengil.  
2. Valin er leiðin til að afrita og svo aðgerðin **Útgáfur** valin.  
3. Á síðunni **Leiðarútgáfur** skal velja aðgerðina **Nýtt**.
4. Einstakt auðkenni útgáfunnar er fært inn í reitinn **Útgáfukóti**. Hægt er að nota hvaða samsetningu sem er af tölustöfum og bókstöfum.  

    Nýja útgáfan sem búin var til fær sjálfkrafa stöðuna **Ný.**  
5. Fyllið inn reitina eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]
6. Til að búa til aðgerðarlínur, skal velja fyrstu auðu línuna og svo fylla inn í **Aðgerð nr.** reitinn eftir aðgerðaröðinni.

    Aðgerðarlínurnar eru í hækkandi röð eftir aðgerðarnúmerum. Til að hægt sé að gera breytingar síðar er mælt með því að nægileg breidd skrefa sé valin. **Næsta aðgerðarnr.** í reitnum er vísað til næstu aðgerðar í leiðinni.

7. Þegar leiðarútgáfan er sett upp er valið **Vottað**  í reitnum **Staða**.

## Sjá einnig .

[Búa til framleiðsluuppskriftir](production-how-to-create-production-boms.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)  
[Áætlun](production-planning.md)  
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]