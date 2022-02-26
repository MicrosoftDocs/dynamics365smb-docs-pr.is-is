---
title: Setja upp forðakostnað verks, verð og afkastagetu
description: Til að nota forða og auðvelda verkefnastjórnun, tilgreinirðu kostnað og verð fyrir einstaka forða eða forðaflokka, og stillir afkastaveitu forða.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.search.form: 72, 76, 77, 203, 204
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a91bf2cbd82f2b4c8374a1773a6603f52c47c581
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/14/2022
ms.locfileid: "7972253"
---
# <a name="set-up-resources-for-projects"></a>Setja upp tilföng fyrir verk

Til að geta unnið með forðaaðgerðir á réttan hátt verður að setja upp forðann og tengt verð og kostnað. Verktengt verð, afslættir og reglur um verðstuðul eru sett upp á verkspjaldinu. Hægt er að tilgreina kostnað og verð einstaks forða, forðaflokka eða alls tiltæks forða hjá fyrirtækinu.

Þegar forði er notaður eða seldur í verki eru upplýsingar um verð og kostnað þar að lútandi fengnar úr upplýsingunum sem notandi hefur sett upp.

Sjálfgefna upphæð á klukkustund þarf að tilgreina þegar forðinn er stofnaður. Ef í verki er til dæmis notast við ákveðna vél í fimm klukkustundir er verkið reiknað út frá upphæð á klukkustund.

> [!NOTE]
> Hægt að kaupa ytri tilföng, t.d. til að senda reikning á lánardrottin fyrir afhenta vinnu. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).<br /><br />
> Í slíku tilfelli er mælt með því að nefna eða flokka slík ytri tilföng til að gefa til kynna tilgang þeirra svo að þeim sé ekki ruglað við innri tilföng notanda.

## <a name="to-set-up-a-resource"></a>að setja upp forða
Stofna skal spjald fyrir hvern forða sem á að nota í verkefnum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tilföng** og velja síðan viðkomandi tengil.
2. Valið er aðgerðin **Nýtt**.
3. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-a-resource-group"></a>Að setja upp forðaflokk
Hægt er að flokka forða saman í einn forðaflokk. Geta og áætlanir forðaflokka eru samsafn einstakra forða. Einnig er hægt að tilgreina getu forðaflokka, annaðhvort óháð samanlögðu verðmæti eða til viðbótar við það.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tilfangaflokkar** og velja síðan viðkomandi tengil.
2. Valið er **Nýtt** aðgerð.
3. Fyllið inn í svæðin eftir þörfum.

## <a name="to-set-capacity-for-a-resource"></a>Að setja upp afkastagetu fyrir forða
Til að reikna út hve lengi forði getur tengst verki verður fyrst að setja afkastagetuna upp sem tiltækan tíma á tímabilinu á verkdagatalinu. Þessi uppsetning er notuð þegar verkáætlunarlínur sem innihalda forðann eru fylltar út. Frekari upplýsingar eru í [Stofna verk](projects-how-create-jobs.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tilföng** og velja síðan viðkomandi tengil.
2. Opna skal viðeigandi forðaspjald og velja svo aðgerðina **Forðageta**.
3. Á síðunni **Forðageta**, á svæðinu **Skoða eftir** skal skilgreina lengd tímabilsins, svo sem **Dagur**, sem sýnt er í dálkum á flýtiflipanum **Fylki forðagetu**.
4. Fyrir hvern forða á línu skal tilgreina fyrir hvert tímabil á dálkunum fjölda vinnustunda sem forðinn er tiltækur.
5. Að öðrum kosti, til að skrá vikulega afkastagetu forðans milli upphafs- og lokadagsetningar, skal velja aðgerðina **Stilla afkastagetu**.
6. Á síðunni **Stillingar forðagetu** skal fylla út reitina eins og þörf krefur.
7. Veljið aðgerðina **Uppfæra afkastagetu**. Síðan **Uppfæra afkastagetu** er uppfærður með þeirri afkastagetu sem færð var inn.
8. Lokaðu síðunni.

## <a name="to-set-up-alternate-resource-costs"></a>Til að setja upp annan forðakostnað
Auk kostnaðarins sem tilgreindur er á forðaspjaldinu er hægt að setja upp annan kostnað fyrir hvern forða. Ef til dæmis er greitt hærra tímakaup vegna yfirvinnu starfsmanna er hægt að setja upp forðakostnað fyrir yfirvinnu. Þessi annar kostnaður sem settur er upp fyrir forða kemur í stað kostnaðarins á forðaspjaldinu þegar forðinn er notaður í forðabókinni.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tilföng** og velja síðan viðkomandi tengil.  
2. Velja skal forðann sem setja á upp einn eða fleiri annan kostnað fyrir og svo skal velja aðgerðina **Kostnaður**.  
3. Á síðunni **Forðakostnaður** skal fylla út reitina í línu eins og þörf krefur.  
4. Endurtaka skal skref 3 fyrir hvern annan kostnað sem setja skal upp.

**Athugasemd** Til að setja upp forðakostnað fyrir allan forðann og alla forðaflokka er síðan **Forðakostnaður** opnuð og reitirnir síðan fylltir út.

## <a name="to-set-up-alternate-resource-prices"></a>Til að setja upp annað forðaverð
Auk verðsins sem tilgreint er á forðaspjaldinu er hægt að setja upp annað verð fyrir hvern forða. Þetta annað verð getur verið háð skilyrðum. Það getur verið háð því hvort forðinn sé notaður í tilteknu verki eða verktegund.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tilföng** og velja síðan viðkomandi tengil.
2. Velja skal forðann sem setja á upp eitt eða fleiri annað verð fyrir og svo skal velja aðgerðina **Verð**.
3. Á síðunni **Forðaverð** skal fylla út reitina í línu eins og þörf krefur.
4. Endurtaka skal skref 3 fyrir hvert annað verð sem setja skal upp.

## <a name="see-also"></a>Sjá einnig
[Setja upp verkefnastjórnun](projects-setup-projects.md)  
[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)      
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]