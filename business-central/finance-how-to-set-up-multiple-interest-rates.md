---
title: Hvernig á að setja upp marga vexti
description: Hægt er að reikna út vaxtareikninga með mörgum vöxtum fyrir tiltekið tímabil. Vaxtaútreikningar er svipaðir fyrir öll fjárhagsgjöld, með aðeins breytingum á vöxtum fyrir tiltekið tímabil.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1a38e286dab02dcb23acaba39a0d61b0b939bb20
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775426"
---
# <a name="set-up-multiple-interest-rates"></a>Setja upp marga vexti
Margir vextir eru notaðir fyrir mismunandi tímabil vegna seinkunar á greiðslum fyrir viðskiptafærslur. Til dæmis tilgreinir ríkisstjórn hámarksvexti sem má leggja á neytendur. Vöxtum er hægt að breyta tvisvar á ári, 1. janúar og 1. júlí. Vextir á milli fyrirtækja eru samþykktir af báðum aðilum og engin takmörk eru fyrir þennan viðskiptavinaflokk. Tilkynntir vextir eru vanalega fjórum prósentum hærri en vextir venjulegra banka.

Þegar vaxtaskilmálar og skilmálar innheimtubréfs er búið til, fyrir sekt vegna seinkunar á greiðslu, er hægt að tilgreina marga vexti þannig að sektargreiðsla er reiknuð út frá mismunandi vöxtum á mismunandi tímabilum. Nánari upplýsingar er að finna í [Innheimta útistandandi skuldir](receivables-collect-outstanding-balances.md).

## <a name="to-set-up-multiple-interest-rates"></a>Uppsetning á mörgum vöxtum  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vaxtaskilmálar** eða Lánardrottinn og veldu síðan tengda tengilinn.  
2.  Á síðunni **Vaxtaskilmálar** skal velja nauðsynlega skilmála og síðan velja aðgerðina **Vextir**.  
3.  Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Velja hnappinn **Í lagi**.  
5.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Skilmálar innheimtubréfa** og veldu síðan tengda tengilinn.  
6.  Á síðunni **Skilmálar innheimtubréfa** skal velja nauðsynlega skilmála innheimtubréfs og síðan velja aðgerðina **Stig**.  
7.  Á síðunni **Stig innheimtubréfa** skal velja reitinn **Reikna út vexti**.  

Þegar gefið er út minnisblað vaxtareiknings, sýnir það vaxtagjöldin með mörgum vöxtum fyrir tiltekið tímabil. Minnisblaðið inniheldur einnig samskiptaupplýsingar viðskiptavinar, fyrirtækið sem gefur út minnisblaðið og viðbótar- og heildarfjárhæðina. Upphafsfærsla minnisblaðsins birtist í feitletruðu. Vaxtagjöldin eru reiknuð með mörgum vöxtum á tilteknu tímabili og eru prentuð eftir upphafsfærslu minnisblaðsins.  

## <a name="see-also"></a>Sjá einnig  
[Innheimta útistandandi skuldir](receivables-collect-outstanding-balances.md)  
[Uppsetning Fjármála](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]