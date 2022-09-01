---
title: Viðbótin QuickBooks-gagnaflutningur
description: Lýsir því hvernig skal nota viðbótina til að flytja inn viðskiptamenn, lánardrottna, vörur og reikninga frá QuickBooks Desktop til Business Central.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, import, implement
ms.search.form: 1911, 1912, 1913, 1914, 1915, 1916, 1918, 1919
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 99a7e12543751fef0297051a64f19c2fb5700022
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361637"
---
# <a name="the-quickbooks-data-migration-extension"></a>Viðbótina QuickBooks gagnaflutningur

Þessi viðbót auðveldar flutning viðskiptamanna, lánardrottna og vara úr QuickBooks í [!INCLUDE[prod_short](includes/prod_short.md)]. Ef fyrirtækið notar QuickBooks er hægt að flytja út viðeigandi upplýsingar og opna síðan leiðarvísi fyrir uppsetningu með hjálp til að hlaða gögnunum upp í [!INCLUDE[prod_short](includes/prod_short.md)].  
Nánari upplýsingar eru í [Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md).

## <a name="data-from-quickbooks-desktop"></a>Gögn úr skjáborði Fljótbókar

Þú getur flutt inn eftirfarandi gögn úr QuickBooks Online til Business Central:

- Viðskiptavinum  
- Lánardrottnar  
- Birgðir  
- Bókhaldslykill  
- Upphafsstöðufærslur í fjárhagnum  
- Magn á lager fyrir birgðavörur  
- Opna skjöl fyrir viðskiptamenn og lánardrottna, eins og t.d. reikningar, kreditreikningar og greiðslur  

Við flytjum aðeins fullar upphæðir í sölu- og innkaupaskjöl. Við uppfærum ekki upphæðir greiddar að hluta. Ef viðskiptamaður hefur t.d. borgað 300 af 500 dollurum á sölureikningi, flytjum við fulla upphæð eða 500. Ef þú hefur fengið greiddan hluta af greiðslum, þarf að uppfæra þær handvirkt, annað hvort áður eða eftir að þú flytur gögn. Við mælum með því að þú jafnir útistandandi færslur áður en þú flytur gögn, bara til þess að gera eftirleikinn auðveldari.

> [!NOTE]
> Við flytjum ekki innkaupapantanir eða sölupantanir.

## <a name="before-you-start"></a>Verður að byrja fyrir

Mikilvægur hluti flutningsferlisins er að tilgreina reikningana sem flytja á færslur til. Það er tilvalið að skipuleggja vörpunina áður en þú flytur gögn. Til dæmis, reikningana sem þú bókar færslurnar fyrir:

- Sala vöru eða þjónustu til viðskiptamanna  
- Innkaup vöru eða þjónustu frá lánardrottnum  
- Leiðréttingar í fjárhagnum  

Business Central krefst þess að fjárhagsreikningum hafi verið úthlutað reikningsnúmerum. Vertu viss um að reikningsnúmerum hafi verið úthlutað til reikninganna í QuickBooks.
Ef færslur í QuickBooks hafa skattaupphæðir, þarf að setja upp skattareikning fyrir þína skattalögsögu í Business Central áður en þú getur bókað færslur.

Til þess að fá gögnin þín úr QuickBooks Desktop þarftu að hlaða niður Microsoft Data Exporter tólinu.  Leiðbeiningar fyrir tólið eru í leiðsagnarforriti fyrir gagnaflutning í [!INCLUDE[prod_short](includes/prod_short.md)]. Tólið mun tengjast QuickBooks-forritinu og flytja út viðeigandi gögn í .zip-skrá.  

> [!NOTE]
> Að svo stöddu er gagnaútflutningstólið aðeins með QuickBooks 2017 og 2018.

## <a name="finding-the-quickbooks-data-migration-extension"></a>Leit að gagnaflutendagögnum Fljótsbóka

Viðbótin QuickBooks gagnaflutningar er sett upp og tilbúin til keyrslu sem samþættur hluti af Gagnaflutningar uppsetningarleiðbeiningar með aðstoð. Ef þú ert tilbúinn til að byrja núna og hefur flutt út gögnin þín úr QuickBooks skaltu velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning með hjálp** og velja síðan viðkomandi tengil. Veljið **Flytja viðskiptagögn** og fara síðan eftir skrefunum í leiðbeiningunum.  

## <a name="what-do-i-do-after-i-migrate-data"></a>Hvað geri ég eftir gagnaflutninginn?

Þegar gagnaflutningi er lokið, hafa færslur stöðuna Óbókaðar, svo þú getur endurskoðað þær og gert leiðréttingar. Til að endurskoða færslurnar, skal farið á síðuna þar þú myndir venjulega finna þær. Til dæmis, til að endurskoða óbókaða sölureikninga, skal farið á síðuna Sölureikningar. Til að endurskoða greiðslubækur, skal fara á síðuna Greiðslubækur.
Það eru einkum nokkrir hlutir sem þú þarft að gera: Ef færslurnar í QuickBooks Online höfðu breytingarmerkingar eða afsláttarupphæð, verður að bæta upphæðunum handvirkt við tengdar færslur í Business Central áður en þú bókar þær.
Ef þú ert að nota VSK, þarftu kannski að bæta viðskiptabókunarflokki og vörubókunarflokki við uppsetningu bókana svo þú getir bókað VSK upphæðir.
Staðfesta upphafsstöðu reikninga í fjárhagnum. QuickBooks geymir ekki núgildandi stöðu fyrir alla reikninga, og því gætirðu þurft að leiðrétta upphafstöður.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/modules/migrate-data-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig .

[Innflutningur viðskiptagagna úr öðrum fjárhagskerfum](across-import-data-configuration-packages.md)  
[Sérstilling [!INCLUDE[prod_short](includes/prod_short.md)] með viðbótum ](ui-extensions.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
