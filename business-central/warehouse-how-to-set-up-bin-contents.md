---
title: Stofna innihald hólfs
description: Þegar búið er að setja upp hólfin er hægt að tilgreina vörurnar sem á að geyma í þeim og setja upp reglur sem stýra því hversu oft er fyllt á hólfin.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 7374
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="create-bin-contents"></a>Stofna innihald hólfs

Þegar búið er að setja upp hólfin er hægt að setja upp innihald þeirra. Þ.e.a.s., hægt er að setja upp vörurnar sem á að geyma í hverju hólfi og setja reglurnar stjórna því hvaða tiltekin vara er sett í hólfið. Þú getur gert þetta handvirkt á síðunni **Hólfainnihald** eða sjálfvirkt með glugganum **Stofna Hólfainnihald vinnublað**.

## <a name="to-create-bin-content-manually"></a>Stofna Innihald hólfs handvirkt

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningar** og velja síðan viðkomandi tengil.  
2. Veljið birgðageymsluna þar sem á að setja upp hólfainnihald og veljið svo aðgerðina **Hólf**.  
3. Veljið hólfið þar sem á að setja upp innihald og veljið svo aðgerðina **Innihald**.  
4. Fyrir hverja vöru sem geyma á í hólfinu skal fylla út línu á síðunni **Innihald hólfs** með viðeigandi upplýsingum. Nokkrir reitir eru þegar útfylltir með upplýsingum um hólfið.  
5. Fyrst er reiturinn **Vörunr.** fylltur út og, ef notaður er beinn frágangur og tínsla, eru aðrir reitir fylltir út, svo sem **Mælieiningarkóti**, **Hám.magn** og **Lágm.magn**.  

Veljið **Fast** ef þess þarf. Ef hólfið á að vera sjálfgefið fyrir vöruna veljið reitinn **Sjálfgefið hólf**.  

Ef notaður er beinn frágangur og tínsla og réttar víddarupplýsingar hafa verið færðar inn á birgðaspjaldinu um mælieiningu hverrar vöru er hámarksmagnið sem fært er inn á síðuna **Innihald hólfs** borið samanvið raungetu hólfsins. Hámarks- og lágmarksmagn er síðan notað þegar áfylling hólfa er reiknuð og tillögur gerðar um frágang.  

Ef gátmerki er sett inn í reitinn **Fast** er varan fest við hólfið sem þýðir að  [!INCLUDE[prod_short](includes/prod_short.md)] reynir að setja þessa vöru í hólfið ef það er pláss fyrir hana og geyma færsluna sem festir vöruna við hólfið jafnvel þó magnið í hólfinu sé 0. Kerfið getur sett aðrar vörur í hólfið þó að tiltekin vara hafi verið fest við hólfið.  

> [!NOTE]  
> Hægt er að setja upp fleiri en eitt innihald hólfs samtímis á síðunni **Vinnublað f. stofnun hólfainnihalds**.  

## <a name="to-create-bin-content-with-a-worksheet"></a>Stofna Innihald hólfs með vinnublaði

Þegar lokið er við að stofna hólfin er hægt að stofna það innihald sem á að vera í hverju hólfi á stofnunarvinnublaði hólfainnihalds.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vinnublað fyrir stofnun hólfainnihalds** og velja viðkomandi tengil.  
2. Á vinnublaðshausnum er smellt í reitinn **Heiti** og valið vinnublað birgðageymslunnar þar sem stofna á hólfainnihald.  
3. Í reitnum **Hólfakóti** er valinn kóti hólfsins þar sem á að tilgreina innihaldið.  

    Ef notaður er beinn frágangur og tínsla í birgðageymslunni er fyllt sjálfkrafa út reitina sem tilheyra hólfinu, svo sem **Tegund hólfs**, **Kóti vöruhúsaflokks** og **Hólfaflokkun**. Þetta eru upplýsingar sem þarf að hafa í huga þegar innihald hólfsins er skilgreint.  
4. Varan sem úthluta á hólfinu er valin og reitir sem tengjast hólfainnihaldi fylltir út. Ef notaður er beinn frágangur og tínsla og nota á aðgerðina **Reikna út áfyllingu hólfa** þarf að fylla út reitina **Hám.magn.** og **Lágm.magn**.  

    Til að stilla þetta hólf sem æskilegt hólf fyrir vöruna jafnvel þó hólfamagnið sé **0** og öll önnur frágangsskilyrði séu jöfn skal velja reitinn **Fast**.  
5. Skref 3 til 4 eru endurtekin fyrir hverja vöru sem á að úthluta hólfi.  
6. Velja aðgerðina **Prenta** til að forskoða og prenta hólfainnihaldið sem hefur verið fært inn á vinnublaðið. Haldið er áfram að yfirfara innihald hólfa þar til notandinn er ánægður.  
7. Þegar þú ert tilbúin(n) er valið **Stofna innihald hólfa** aðgerð.  

Á þessu vinnublaði er hægt að vinna með nokkrar hólfainnihaldslínur fyrir nokkur hólf og fá þannig gott yfirlit yfir hvað er sett í hin ýmsu hólf á tilteknu svæði, gangi eða rekka.  

## <a name="see-also"></a>Sjá einnig .

[Yfirlit yfir vöruhúsakerfi](design-details-warehouse-management.md)
[Birgðir](inventory-manage-inventory.md)  
[Vöruhúsastjórnun sett upp](warehouse-setup-warehouse.md)  
[Samsetningardeild](assembly-assemble-items.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
