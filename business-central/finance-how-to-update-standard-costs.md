---
title: Uppfæra staðlaðan kostnað
description: Reglulega verður að uppfæra staðlað kostnaðarverð íhluta og leggja nýja kostnaðinn saman við yfirvöruna.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 5841
ms.date: 10/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="update-standard-costs"></a>Uppfæra staðlaðan kostnað
Reglulega verður að uppfæra staðlað kostnaðarverð íhluta og leggja nýja kostnaðinn saman við yfirvöruna. Ferlið samanstendur yfirleitt af fjórum eftirtöldum skrefum:  

1.  Uppfærslu kostnaðar á íhluta- og afkastagetustigunum. Frekari upplýsingar, sjá **Leggja til staðlaðan vörukostnað** runuvinnslu.  
2.  Samstilling og samantekt íhluta- og afkastakostnaðarins til að reikna út heildarframleiðslu- eða samsetningarkostnað varanna.  
3.  Innleiða staðlaðan kostnað sem færður var inn þegar fyrri keyrsla var keyrð. Staðlaður kostnaður tekur ekki gildi fyrr en hann er innleiddur. Notaðu runuvinnsluna **Innleiða breytingu á stöðluðu kostnaðarverði**, sem uppfærir breytingar á staðalkostnaði á vörum með þeim sem er í töflunni vinnublað staðlaðs kostnaðarverðs.  
4.  Innleiða breytingar til að uppfæra reitinn **Kostn.verð** á birgðaspjaldinu og framkvæma endurmat á birgðum. Nánari upplýsingar eru í [Endurmat birgða](inventory-how-revalue-inventory.md).  

Í [Um útreikning staðlaðs kostnaðar](finance-about-calculating-standard-cost.md) er fjallað nánar um þetta efni.
  
## <a name="to-update-standard-costs"></a>að uppfæra staðlað kostnaðarverð

1.  Keyrslan **Leiðr. kostnað - Birgðafærslur** er keyrð Til að ræsa keyrsluna skaltu velja þá  ![ljósaperu sem opnar aðgerðina segja mér.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Leiðrétta kostnað - Birgðafærslur** og velja síðan viðkomandi tengil. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Fara yfir niðurstöðurnar og gera breytingar eftir þörfum.  
2.  Keyrslan **Bóka birgðakostnað á fjárhag** er keyrð Til að ræsa keyrsluna skaltu velja þá  ![ljósaperu sem opnar aðgerðina segja mér.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Bóka birgðakostnað í fjárhag** og veldu síðan tengda tengilinn. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Fara yfir niðurstöðurnar og gera breytingar eftir þörfum.  
3.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Teiknið, Vinnublað  **staðlaðs kostnaðarverðs, skal færa inn** eina eða fleiri af eftirfarandi aðgerðum:

    1.  Keyrslan **Leggja til staðlaðan vörukostnað** er keyrð.  
    2.  Niðurstöðurnar eru skoðaðar og breytingar eru gerðar eftir þörfum.  
    3.  Keyrslan **Leggja til staðlaðan afkastakostnað** er keyrð.  
    4.  Niðurstöðurnar eru skoðaðar og breytingar eru gerðar eftir þörfum.
    5. Keyrslan **Leggja saman staðlað kostnaðarverð** er keyrð.
    6.  Niðurstöðurnar eru skoðaðar og breytingar eru gerðar eftir þörfum.
    7.  Keyrslan **Innleiða breytingu á stöðluðu kostnaðarverði** er keyrð.  
4.  Skoða og birta skal síðuna **Endurmatsbók** sem hefur verið fyllt með færslum úr fyrri skrefum í þessu ferli.  

## <a name="see-also"></a>Sjá einnig

 [Um umreikning staðalkostnaðar](finance-about-calculating-standard-cost.md)   
 [Birgðakostnaði stjórnað](finance-manage-inventory-costs.md)   
 [Hönnunarupplýsingar: Aðferð kostnaðarútreiknings](design-details-costing-methods.md)   
 [Fjármál](finance.md)  
 [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
