---
title: "Hvernig skal búa til innihald hólfs | Microsoft Docs"
description: "Þegar búið er að setja upp hólfin er hægt að setja upp innihald þeirra. Þ.e.a.s., hægt er að setja upp vörurnar sem á að geyma í hverju hólfi og setja reglurnar stjórna því hvaða tiltekin vara er sett í hólfið."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 1f3a90b9bc9cce2e138e490d3064f6d505a088b9
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-bin-contents"></a>Hvernig á að: stofna Innihald hólfs
Þegar búið er að setja upp hólfin er hægt að setja upp innihald þeirra. Þ.e.a.s., hægt er að setja upp vörurnar sem á að geyma í hverju hólfi og setja reglurnar stjórna því hvaða tiltekin vara er sett í hólfið. Þú getur gert þetta handvirkt í glugganum **Hólfainnihald** eða sjálfvirkt með glugganum **Stofna Hólfainnihald vinnublað**.

## <a name="to-create-bin-content-manually"></a>Stofna Innihald hólfs handvirkt  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn  **Staðsetningar** og velja svo viðeigandi tengil.  
2.  Veljið birgðageymsluna þar sem á að setja upp hólfainnihald og veljið svo aðgerðina **Hólf**.  
3.  Veljið hólfið þar sem á að setja upp innihald og veljið svo aðgerðina **Innihald**.  
4.  Fyrir hverja vöru sem geyma á í hólfinu skal fylla út línu í glugganum **Innihald hólfs** með viðeigandi upplýsingum. Nokkrir reitir eru þegar útfylltir með upplýsingum um hólfið.  
5.  Fyrst er reiturinn **Vörunr.** fylltur út og, ef notaður er beinn frágangur og tínsla, eru aðrir reitir fylltir út, svo sem **Mælieiningarkóti**, **Hám.magn** og **Lágm.magn**.  

Veljið **Fast** ef þess þarf. Ef hólfið á að vera sjálfgefið fyrir vöruna veljið reitinn **Sjálfgefið hólf**.  

Ef notaður er beinn frágangur og tínsla og réttar víddarupplýsingar hafa verið færðar inn á birgðaspjaldinu um mælieiningu hverrar vöru er hámarksmagnið sem fært er inn í gluggann **Innihald hólfs** borið samanvið raungetu hólfsins. Hámarks- og lágmarksmagn er síðan notað þegar áfylling hólfa er reiknuð og tillögur gerðar um frágang.  

Ef gátmerki er sett inn í reitinn **Fast** er varan fest við hólfið sem þýðir að  [!INCLUDE[d365fin](includes/d365fin_md.md)] reynir að setja þessa vöru í hólfið ef það er pláss fyrir hana og geyma færsluna sem festir vöruna við hólfið jafnvel þó magnið í hólfinu sé 0. Kerfið getur sett aðrar vörur í hólfið þó að tiltekin vara hafi verið fest við hólfið.  

> [!NOTE]  
>  Hægt er að setja upp fleiri en eitt innihald hólfs samtímis í glugganum **Vinnublað f. stofnun hólfainnihalds**.  

## <a name="to-create-bin-content-with-a-worksheet"></a>Stofna Innihald hólfs með vinnublaði  
Þegar lokið er við að stofna hólfin er hægt að stofna það innihald sem á að vera í hverju hólfi á stofnunarvinnublaði hólfainnihalds.

1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Hólfainnihald stofnun vinnublað** og velja svo viðeigandi tengil.  
2.  Á vinnublaðshausnum er smellt í reitinn **Heiti** og valið vinnublað birgðageymslunnar þar sem stofna á hólfainnihald.  
3.  Í reitnum **Hólfakóti** er valinn kóti hólfsins þar sem á að tilgreina innihaldið.   

    Ef notaður er beinn frágangur og tínsla í birgðageymslunni er fyllt sjálfkrafa út reitina sem tilheyra hólfinu, svo sem **Tegund hólfs**, **Kóti vöruhúsaflokks** og **Hólfaflokkun**. Þetta eru upplýsingar sem þarf að hafa í huga þegar innihald hólfsins er skilgreint.  
4.  Varan sem úthluta á hólfinu er valin og reitir sem tengjast hólfainnihaldi fylltir út. Ef notaður er beinn frágangur og tínsla og nota á aðgerðina **Reikna út áfyllingu hólfa** þarf að fylla út reitina **Hám.magn.** og **Lágm.magn**.  

    Til að stilla þetta hólf sem æskilegt hólf fyrir vöruna jafnvel þó hólfamagnið sé **0** og öll önnur frágangsskilyrði séu jöfn skal velja reitinn **Fast**.  
5.  Skref 3 til 4 eru endurtekin fyrir hverja vöru sem á að úthluta hólfi.  
6.  Velja aðgerðina **Prenta** til að forskoða og prenta hólfainnihaldið sem hefur verið fært inn á vinnublaðið. Haldið er áfram að yfirfara innihald hólfa þar til notandinn er ánægður.  
7.  Þegar þú ert tilbúin(n) er valið **Stofna innihald hólfa** aðgerð.  

Á þessu vinnublaði er hægt að vinna með nokkrar hólfainnihaldslínur fyrir nokkur hólf og fá þannig gott yfirlit yfir hvað er sett í hin ýmsu hólf á tilteknu svæði, gangi eða rekka.  

## <a name="see-also"></a>Sjá einnig
[Hvernig á að Reikna út áfyllingu hólfs](warehouse-how-to-calculate-bin-replenishment.md)    
[Vöruhúsastjórnun](warehouse-manage-warehouse.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)     
[Samsetningardeild](assembly-assemble-items.md)    
[Hönnunarupplýsingar vöruhúsakerfi](design-details-warehouse-management.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

