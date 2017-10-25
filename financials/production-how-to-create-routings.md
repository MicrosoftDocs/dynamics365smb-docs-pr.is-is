---
title: "Hvernig skal búa til leiðir | Microsoft Docs"
description: "Leið hefur að geyma aðalgögn sem skráir ferlisþarfir vara. Þegar framleiðslupöntun er búin til fyrir vöru stjórnar leið hennar áætlanagerð yfir aðgerðir eins og sýnt er í glugganum **Leið framl.pöntunar** í framleiðslupöntuninni."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 166d85bbcf7d97cb513ba668e41fc4a179d8fcc3
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-routings"></a>Hvernig á að stofna Nýjar leiðir
Framleiðslufyrirtæki nota leiðir til að stýra framleiðsluferlinu og gera sýnilegt.

Leiðin er grunnurinn að vinnsluáætlun, áætlun um afköst og áætlaðri úthlutun á efnisþörf og framleiðsluskjölum.  

Varðandi framleiðsluuppskriftir, er leiðunum úthlutað til endanlegrar framleiddrar vöru. Leið hefur að geyma aðalgögn sem skráir ferlisþarfir vara. Þegar framleiðslupöntun er búin til fyrir vöru stjórnar leið hennar áætlanagerð yfir aðgerðir eins og sýnt er í glugganum **Leið framl.pöntunar** í framleiðslupöntuninni.  

Áður en þú getur sett upp leið verður eftirfarandi að vera á réttum stað:  

- Birgðaspjöld er búin til fyrir yfirvörur sem taka þátt í framleiðslu. Nánari upplýsingar eru í [Hvernig á að: Skrá nýjar vörur](inventory-how-register-new-items.md).
- Framleiðsluforði eru uppsettur. Nánari upplýsingar er að finna í [Hvernig á að setja upp vinnustöðvar og vélastöðvar](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-routing"></a>Stofna leið  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **leiðir** og velja svo viðeigandi tengil.  
2.  Valið er **Nýtt** aðgerð.  
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Í reitnum **Tegund**, veljið **Í röð** til að reikna framl. leiðina samkvæmt gildinu í reitnum **Aðgerðarnr.**. .   
    Veljið **Samhliða** til að reikna aðgerðir samkvæmt gildinu í reitnum **Næsta aðgerðarnr.** .  
5.  Reiturinn **Staða** verður að vera stilltur á **Ný** eða **Í þróun** svo hægt sé að breyta leið. Til að ræsa hana þarf að stilla **Staða** á **Vottað**.  

    Halda áfram til að fylla út í leiðarlínur.
6.  Í **Aðgerð Nr.**. reitinn er fært inn númer fyrstu aðgerðarinnar, t.d. **10**.  
7.  Í reitnum **Tegund** er valið hvers konar forði er notaður, t.d. **Vinnustöð**.  
8.  Í reitnum **númer** er forðinn sem á að nota valinn eða hann sleginn inn í reitinn.  
9.  Í reitnum **Leiðartengilskóti** er hægt að slá inn kóta til að tengja íhlut við ákveðna aðgerð. Frekari upplýsingar, sjá hlutann „Stofna leiðartengla“.
10.  Í reitunum **Keyrslutími** og **Uppsetn.tími** er færðir inn þeir vinnslutímar þarf til að framkvæma aðgerð.  

    > [!NOTE]  
    >  Uppsetningartími er reiknaður fyrir hverja framleiðslupöntun en keyrslutími fyrir hverja framleidda vöru.  

11.  Í reitnum **Samþætt afkastageta** er tilgreint hversu margar einingar valda forðans eru notaðar til að framkvæma aðgerð. Til dæmis helminga tveir einstaklingar úthlutaðir á eina pökkunaraðgerð keyrslutímann.  
12.  Haldið er áfram að fylla út línur fyrir allar aðgerðir sem koma við sögu í framleiðslu viðkomandi vöru.  
13.  Línur úr fyrirliggjandi leið eru afritaðar með því að smella á **Afrita leiðir** aðgerðina til að velja línur sem eru til.  
14. Leiðin vottuð.  
15. Nú er hægt að hengja nýju leiðina við spjald viðkomandi framleiðsluvöru, með því að fylla upp í reitinn **Leið nr.**. Nánari upplýsingar eru í [Hvernig á að: Skrá nýjar vörur](inventory-how-register-new-items.md).  

> [!NOTE]  
>  Mundu líka að endurreikna staðlað kostnaðarverð vörunnar úr **birgða** spjaldinu: velja **Framleiða** aðgerðina, og síðan smellt á **Reikna staðlað kostn.verð** aðgerðina og veljið síðan **Öll stig** aðgerðina.  

## <a name="to-create-routing-links"></a>Leiðartenglar stofnaðir
Hægt að búa til leiðartengla til að tengja íhluti við ákveðnar aðgerðir til að viðhalda sambandi þeirra jafnvel þótt framleiðsluuppskrift eða leið sé breytt. Þeir auðvelda einnig bráða birgðaskráningu íhluta þegar ákveðin tengd aðgerð hefst, ekki þegar öll framleiðslupöntunin er gefin út. Nánari upplýsingar eru í [Hvernig á að birgðaskrá íhluti samkvæmt frálagi aðgerða](production-how-to-flush-components-according-to-operation-output.md).  

Annar mikilvægur kostur er sá að tenging íhluta og aðgerða er birt í rökrænni uppbyggingu framvindu þegar **framleiðslubókin** er notuð í bókanir frálags og notkunar.  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **leiðir** og velja svo viðeigandi tengil.  
2.  Opna skal leiðina með aðgerðunum sem á að tengja.  

    Tryggja þarf að staða leiðar sé **Í þróun**.  

3.  Á viðkomandi leiðarlínu í reitnum **Leiðartengilskóti** skal velja kóta.  
4.  Því næst er bætt við öðruvísi leiðartengilskótum á aðrar aðgerðir í leiðinni, ef það á við.  

    > [!NOTE]  
    >  Ekki skal nota sama leiðartengilskótann í mismunandi aðgerðir í leið þar sem hætta er á að tengja íhlut fyrir mistök við tvær mismunandi aðgerðir og þar með nota hann tvisvar.  
    >   
    >  Góð regla er að nefna leiðartengilskótann eftir aðgerðinni til að tryggja sértæka leiðartengla í aðgerðir.

5.  Staða leiðar er stillt á **Vottað**.  

    Leiðartenglakótar eru nú tengdir við aðgerðir. Næst skal stofna sjálfan tengilinn með því að úthluta sömu kótum á tiltekna íhluti í viðeigandi framleiðsluuppskrift.  

6.  Opna skal **framleiðsluuppskriftina** sem inniheldur íhlutina sem á að tengja við ofantaldar aðgerðir. Frekari upplýsingar, sjá [Hvernig skal: Stofna framleiðsluuppskriftir](production-how-to-create-production-boms.md).
7.  Tryggja þarf að uppskriftin sé stillt á **Í þróun**.  
8.  Á viðkomandi framleiðsluuppskriftarlínu í reitnum **Leiðartengilskóti** skal velja kótann sem úthlutað hefur verið á viðeigandi aðgerð.  
9. Því næst er leiðartengilskótum bætt við aðra íhluti eftir því í hvaða aðgerðum þeir kótar eru notaðir.  
10. Staða framleiðsluuppskriftar er stillt á **Vottað**.  

    > [!NOTE]  
    >  Til að virkja leiðartengla í framleiðslupöntun sem þegar er til þarf fyrst að endurnýja hana. Frekari upplýsingar, sjá [Hvernig skal: Stofna framleiðslupantanir](production-how-to-create-production-orders.md).  

Valdir íhlutir verða nú tengdir við valdar aðgerðir þegar framleiðslupöntun er búin til eða endurnýjuð með umræddri framleiðsluuppskrift og leið. Hægt er að skoða þetta í glugganum **Íhlutir framleiðslupöntunar** undir framleiðslupöntuninni og í honum er einnig hægt að fjarlægja og bæta við tilgreindum leiðartengilskótum hvenær sem er.

## <a name="to-assign-personnel-tools-and-quality-measures-to-routing-operations"></a>Úthluta starfsmönnum, verkfærum og gæðaráðstöfunum til leiðaraðgerðir.
Ef krafist er starfsmanna með sérþekkingu eða sérstaka heimild fyrir aðgerðinni má úthluta viðkomandi starfsmönnum á aðgerðina. Að auki geturðu úthlutað verkfærum og gæðaráðstöfunum til aðgerðarinnar. Þetta ferli lýsir því hvernig skal úthluta starfsmönnum. Skrefin eru svipuð fyrir aðrar gerðir aðgerðaupplýsinga.

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **leiðir** og velja svo viðeigandi tengil.  
2.  Viðeigandi leið er opnuð.  
3.  Á flýtiflipanum **Línur** skal velja línuna sem á að vinna úr og svo velja aðgerðina **Starfsmenn**.  
4.  Reitirnir í glugganum **Starfsmenn leiðar** eru fylltir út.  
5.  Velja hnappinn **Í lagi** til að hætta í glugganum. Innfærð gildi eru afrituð og úthlutuð aðgerðinni.    

## <a name="to-create-a-new-versions-of-a-routing"></a>Gerð nýrra útgáfa af leiðum:  
Með útgáfureglunni er hægt að fást við margar útgáfur. Skipulag leiðaútgáfunnar samsvarar skipulagi leiðarinnar sem felur í sér leiðaútgáfuhaus og leiðaútgáfulínur. Aðalmunurinn ræðst af upphafsdagsetningunni.  

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **leiðir** og velja svo viðeigandi tengil.  
2.  Leið sem á að afrita er valin og svo er aðgerðin **Útgáfur** valin.  
3. Í glugganum **Leiðarútgáfur** skal velja aðgerðina **Nýtt**.
4. Fyllið inn í reitina eftir þörfum.
5.  Einstakt auðkenni útgáfunnar er fært inn í reitinn **Útgáfukóti**. Hvaða samsetning af tölum og bókstöfum er leyfileg.  

    Nýja útgáfan sem búin var til fær sjálfkrafa stöðuna **Ný.**  
6.  Til að búa til aðgerðarlínur, skal velja fyrstu auðu línuna og svo fylla inn í **Aðgerð nr.** reitinn eftir aðgerðaröðinni.

    Aðgerðalínunum er raðað í hækkandi röð eftir aðgerðanúmerum. Til að hægt sé að gera breytingar síðar er mælt með því að nægilegt bil sé haft milli stiga. **Næsta aðgerðarnr.** reiturinn vísar í eftirfarandi aðgerð. Hægt er að færa aðgerðarnúmerið inn beint.

7. Þegar leiðarútgáfunni er lokið, setja **Staða** reitinn á **Vottað**.

Gildistími útgáfunnar er tilgreindur í reitnum **Upphafsdagsetning**.  

## <a name="see-also"></a>Sjá einnig  
[Hvernig á að stofna nýjar framl.uppskriftir](production-how-to-create-production-boms.md)  
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Framleiðsla](production-manage-manufacturing.md)    
[Áætlun](production-planning.md)   
[Birgðir](inventory-manage-inventory.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

