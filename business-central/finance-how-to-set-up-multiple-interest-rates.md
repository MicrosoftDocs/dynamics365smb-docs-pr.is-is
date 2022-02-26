---
title: Setja upp marga vexti til að seinka greiðslu
description: Í þessu efnisatriði er sagt hvernig á að reikna út gjöld með mörgum vöxtum fyrir tiltekið tímabil.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 6, 431, 432, 572
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 6d90f8e042899495bfc8e171d7e69f7e5b4fdb36
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971604"
---
# <a name="set-up-multiple-interest-rates-for-delayed-payment"></a>Setja upp marga vexti til að seinka greiðslu

Hægt er að nota mismunandi vexti fyrir mismunandi tímabil fyrir seinkaðar greiðslur í verslunarviðskiptum. [!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)]

Til dæmis tilgreinir ríkisstjórn hámarksvexti sem má leggja á neytendur. Vöxtum er hægt að breyta tvisvar á ári, 1. janúar og 1. júlí. Vextir á milli fyrirtækja eru samþykktir af báðum aðilum og engin takmörk eru fyrir þennan viðskiptavinaflokk. Tilkynntir vextir eru vanalega fjórum prósentum hærri en vextir venjulegra banka.

Þegar vaxtaskilmálar og skilmálar innheimtubréfs er búið til, fyrir sekt vegna seinkunar á greiðslu, er hægt að tilgreina marga vexti þannig að sektargreiðsla er reiknuð út frá mismunandi vöxtum á mismunandi tímabilum.  

## <a name="to-set-up-multiple-interest-rates"></a>Uppsetning á mörgum vöxtum

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vaxtaskilmálar** og velja síðan viðkomandi tengil.  
2. Á síðunni **Vaxtaskilmálar** skal velja nauðsynlega skilmála og síðan velja aðgerðina **Vextir**.  
3. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Velja hnappinn **Í lagi**.  
5. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Skilmálar innheimtubréfa** og velja síðan viðkomandi tengil.  
6. Á síðunni **Skilmálar innheimtubréfa** skal velja nauðsynlega skilmála innheimtubréfs og síðan velja aðgerðina **Stig**.  
7. Á **síðunni stig innheimtubréfa**, fyrir viðeigandi stig innheimtubréfs, er **reiturinn Reikna vexti valinn**.  

Þegar gefið er út minnisblað vaxtareiknings, sýnir það vaxtagjöldin með mörgum vöxtum fyrir tiltekið tímabil. Minnisblaðið inniheldur einnig samskiptaupplýsingar viðskiptavinar, fyrirtækið sem gefur út minnisblaðið og viðbótar- og heildarfjárhæðina. Upphafsfærsla minnisblaðsins birtist í feitletruðu. Vaxtagjöldin eru reiknuð með mörgum vöxtum á tilteknu tímabili og eru prentuð eftir upphafsfærslu minnisblaðsins.  

## <a name="see-also"></a>Sjá einnig

[Innheimta útistandandi skuldir](receivables-collect-outstanding-balances.md)  
[Uppsetning Fjármála](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]