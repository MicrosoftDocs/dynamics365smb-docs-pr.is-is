---
title: "Vinna með fjárhagsskemu| Microsoft Docs"
description: "Lýsir því hvernig skal nota fjárhagsskemu til að búa til ýmis konar yfirlit og skýrslur fyrir greiningar á afkastagögnum fjárhags."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ce7ec04b72fd6a5c4c00eeff277e74a9d834959a
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="work-with-account-schedules"></a>Vinna með fjárhagsskemu
Notaðu reikningsáætlanir til að fá innsýn í fjárhagsupplýsingar sem eru geymdar í bókhaldslyklum. Fjárhagsskemu eru notuð til að greina upphæðir í fjárhagsreikningi og bera saman fjárhagsfærslur og færslur í fjárhagsáætlunarskýrslu. Niðurstöðurnar birtast í töflum á heimasíðunni þinni, svo sem sjóðstreymi.  

[!INCLUDE[d365fin](includes/d365fin_md.md)]  veitir nokkrar sýnishornareikninga sem hægt er að nota strax eða þú getur sett upp eigin línur og dálka til að tilgreina tölurnar sem þú vilt bera saman. Notendur getur þú búið til fjárhagskema til að reikna út framlegð fyrir víddir eins og deildir eða hópa viðskiptamanna. Hægt er að búa til eins margar sérsniðnar fjárhagsskýrslur og óskað er.  

Uppsetning fjárhagsskema krefst skilnings á fjárhagsgögnum í bókhaldslyklinum. Hægt er til dæmis að skoða fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum. Þetta krefst þess að fjárhagsáætlanir séu búnar til. Frekari upplýsingar eru í [Stofna fjárhagsáætlun](finance-how-create-budgets.md).

## <a name="account-categories-and-account-schedules"></a>Lykiltegundir og fjárhagsskemu
Hægt er að nota lykiltegundir til að breyta sniði fjárhagsskýrslna. Þegar lykiltegundir hafa verið settar upp í glugganum **Flokkar fjárhagsreikninga** og aðgerðin **Mynda fjárhagsskemu** er valin, eru undirliggjandi fjárhagsskemu fyrir kjarnaviðskiptaskýrslur uppfærð. Næst þegar einhver af þessum skýrslum er keyrð, eins og stöðuyfirlit, er nýjum samtölum og undirfærslum bætt við, samkvæmt þeim breytingum sem gerðar voru. Frekari upplýsingar er að finna í [Fjárhagur og bókhaldslyklar](finance-general-ledger.md).  

## <a name="to-create-new-account-schedules"></a>Nýtt fjárhagsskema búið til:  
 Fjárhagsskemu eru notuð til að greina upphæðir í fjárhagsreikningi eða bera saman fjárhagsfærslur og fjárhagsáætlunarfærslur. Hægt er til dæmis að skoða fjárhagsfærslur sem prósentuhlutfall af áætlunarfærslum.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsskemu** og velja svo viðeigandi tengil.  
2. Í glugganum **Heiti fjárhagsskema** skal velja aðgerðina **Nýtt** til að búa til nýtt heiti á fjárhagsskema.
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Veljið aðgerðina **Breyta fjárhagsskema**.
5. Í glugganum **Fjárhagsskema** skal fylla reitina út eftir þörfum.  

    Þegar nýtt fjárhagsskema hefur verið stofnað og línurnar hafa verið settar upp, þarf að setja upp dálka. Annaðhvort er hægt að setja þær upp handvirkt eða úthluta forskilgreindri dálkauppsetningu á viðkomandi fjárhagsskema.
6. Veljið aðgerðina **Breyta uppsetningu dálkaútlits**.
7. Í glugganum **Dálkaútlit** skal fylla reitina út eftir þörfum.

> [!NOTE]  
>   Ef ekki var tilgreint sjálfgefið dálkaútlit fyrir fjárhagsskemað verður að setja dálkana upp handvirkt.   

### <a name="to-create-a-column-that-calculates-percentages"></a>Stofnun dálks sem reiknar prósentur:  
Stundum getur verið þörf á dálkum í fjárhagsskema til að reikna prósentur heilda. Til dæmis, ef nokkrar línur skipta sölu eftir vídd kann að vera þörf á dálki sem birtir prósentu heildarsölu sem hver lína stendur fyrir.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsskemu** og velja svo viðeigandi tengil.
2. Í glugganum **Heiti fjárhagsskema** veljið fjárhagsskema.  
3. Veljið aðgerðina **Breyta fjárhagsskema** til að setja upp fjárhagsskemalínu til að reikna heildina sem prósenturnar munu byggjast á.  
4. Setjið inn línu beint fyrir ofan fyrstu línuna sem birta á prósentur fyrir.  
5. Fyllið inn í reitina í línunni sem hér segir: Í **Tegund samantektar** reitnum er færður inn **Valinn stofn fyrir prósentur**. Í reitnum **Samantekt** er færð inn reikniregla fyrir heildina sem prósentan verður byggð á. T. d. ef lína 11 inniheldur heildarsölu, skal færa inn **11**.  
6. Veljið aðgerðina **Breyta uppsetningu dálkaútlits** til að setja upp dálk.  
7. Fyllið inn í reitina í línunni sem hér segir: Í **Tegund dálks** reitnum er færður inn **Formúla**. Í reitnum **Reikniregla** er færð inn reikniregla fyrir upphæðina sem reikna á prósentur fyrir, með % fyrir aftan. Til dæmis ef dálkur N inniheldur hreyfingu, er fært inn **N%**.  
8. Skref 4 til 7 eru endurtekin fyrir hvern flokk línu sem skipta á niður eftir prósentum.

## <a name="to-set-up-account-schedules-with-overviews"></a>Uppsetning fjárhagsskema með yfirlitum  
Hægt er að nota fjárhagsskema til að búa til reikning sem ber saman upphæðir fjárhagsreiknings og fjárhagsáætlunar.

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsskemu** og velja svo viðeigandi tengil.
2. Í glugganum **Heiti fjárhagsskema** veljið fjárhagsskema.  
3. Veljið aðgerðina **Breyta fjárhagsskema**.  
4. Í glugganum **Fjárhagsskema** skal velja heiti sjálfgefins fjárhagsskema í reitnum **Heiti**.
5. Veljið aðgerðina **Setja inn reikning**.  
6. Reikningarnir sem eiga að vera í yfirlitinu eru valdir og smellt á **Í lagi**.

    Reikningarnir eru ekki settir inn í fjárhagsskemað. Einnig er hægt að breyta dálkauppsetningunni.  
7. Veljið aðgerðina **Yfirlit**.  
8. Í flýtiflipanum **Víddarafmarkanir** skal stilla afmörkunarheitið sem á að nota á áætlunarafmörkun.  
9. Velja hnappinn **Í lagi**.  

Nú er hægt að afrita áætlunaryfirlitið og líma það inn í töflureikni.

## <a name="see-also"></a>Sjá einnig
[Viðskiptaupplýsingar](bi.md)  
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

