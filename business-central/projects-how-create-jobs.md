---
title: Stofna vinnsluspjald fyrir vinnu og tilgreina verkefni
description: Í nýju verkefni skal stofna verkspjald sem inniheldur verkhluta starfsins og áætlunarlínur, til að auðvelda þér að stjórna framvindu og fjárhagsáætlunum.
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: project management, task
ms.search.form: 88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020
ms.date: 08/03/2022
ms.author: edupont
ms.openlocfilehash: 8d70c11aa3d467ada4f7aae3a1cf3efa1603bbe4
ms.sourcegitcommit: bb9b2b4e693fa326a13d94e5e83f60e6c7ac5b68
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227473"
---
# <a name="create-jobs"></a>Stofna verk

Þegar nýtt verk er stofnað verður að stofna verkspjald með samþættum verkhlutum og áætlunarlínum, sem skipt er upp í tvö lög.  

Fyrsta lagið samanstendur af verkhlutum. Það verður að stofna að minnsta kosti einn verkhluta fyrir hvert verk vegna þess að allar bókanir vísa til verkhluta. Ef a.m.k. einn verkhluti er í verkinu er hægt að setja upp áætlunarlínur og bóka notkun fyrir verkið.

Hitt lagið samanstendur af áætlunarlínum sem tilgreina ítarlega notkun forða, vara og ýmis fjárhagsleg útgjöld.

Lagskiptingin gerir kleift að skipta verkinu í smærri verk og notast við ítarlegri upplýsingar við fjárhagsáætlun, tilboð og skráningu. Auk þess veitir það innsýn í framvindu verksins. Þú getur til dæmis fylgst með hvort þú sért að hitta tilnefnda áfanga eða ef þú ert á miða til að uppfylla væntingar fjárhagsáætlunar.

> [!TIP]
> Veldu aðgerðina **Nýtt Verk** í hlutverkamiðstöðinni **Verkefnastjóri** til að setja af stað uppsetningarleiðsögn sem leiðir notandann í gegnum skrefin við að stofna verk með samþættum verkhlutum og áætlunarlínum. Eftirfarandi ferli sýnir hvernig á að framkvæma skrefin handvirkt. Til að sjá dæmi um hvernig á að búa til starf handvirkt skal fara í [Myndband: Hvernig á að stofna verk Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).

Stundum er sá aðili sem tekur á móti þjónustu annar en sá aðili sem er að greiða reikninginn. **Á síðunni vinnslur** er hægt að tilgreina viðskiptamanninn sem mun njóta góðs af verkinu í **reitunum Selt-til** og aðila sem á að reikningsfæra í **reitunum Reikn**. Einnig má veita eftirfarandi upplýsingar: 

* Þar sem vinnan mun gerast með því að velja úr lista yfir Aðsetur sendist á viðskiptamanninn.
* Bæta við upplýsingum um ytri tilvísanir til að einfalda samskipti um verkefnið.
* Skrifa yfir staðlaða fjárhagslega skilmála verksins.

## <a name="to-create-a-job-card"></a>Til að stofna verkspjald

Stofnað er verkspjald og svo eru stofnaðar verkhlutalínur og áætlunarlínur fyrir það.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk** og velja síðan viðkomandi tengil.  
2. Veljið aðgerðina **Nýtt** og fyllið svo út reitina eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Til að tilgreina verkið með upplýsingum um önnur verk skal velja aðgerðina **Afrita verk** og fylla svo út reitina eins og þörf krefur og velja hnappinn **Í lagi**.

> [!NOTE]  
> Ef vinnuskýrslur eru notaðar í verkinu þarf einnig að tilnefna ábyrgan aðila. Einstaklingurinn getur samþykkt vinnuskýrslur fyrir starfsmannaverkefni sem tengjast verkinu. Frekari upplýsingar eru í [Setja upp vinnuskýrslur](projects-how-setup-time-sheets.md).

Einnig er augljóst að merkja skal aðgerðir í verki sem lokað er með því að **nota lokað** svæði. í eftirfarandi töflu er lýst hvaða áhrif Valkostirnir hafa fyrir þennan reit.

|Valkostur  |Lýsing  |
|---------|---------|
|Autt |Allar aðgerðir eru leyfðar.|
|Bóka    |Hægt er að vinna með áætlunarlínur, en bókun vegna verksins er lokuð. Sé þessi kostur valinn hefur það í för með sér að hvorki er hægt að bóka notkun né sölu verksins.|
|Allt  |Allar aðgerðir eru lokaðar.|

## <a name="to-create-tasks-for-a-job"></a>Til að búa til verkhluta fyrir verk

Lykilatriði í stofnun verka er að tilgreina þá verkhluta sem verkið felur í sér. Verkefnum er tilgreint með því að stofna eina línu fyrir hvert verk á **fastflipanum** verk á **síðunni vinnsluspjald**. Hvert verk verður að hafa að minnsta kosti einn verkhluta.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk** og velja síðan viðkomandi tengil.
2. Opnið verkspjaldið fyrir viðeigandi verk.
3. Á flýtiflipanum **Verkhlutar** skal fylla út reitina eins og þörf krefur í nýrri línu.
4. Til að draga inn verkhluta og búa til stigveldi skal velja aðgerðina **Verkhlutar** og svo aðgerðina **Draga inn verkhluta**.
5. Endurtakið skref 3 og 4 fyrir alla verkhluta sem þarf fyrir verkið.
6. Til að tilgreina verkhluta með upplýsingum um aðra verkhluta skal velja aðgerðina **Afrita verkhluta frá** og fylla svo út reitina eins og þörf krefur og velja hnappinn **Í lagi**.

## <a name="to-create-planning-lines-for-a-job"></a>Til að stofna verkáætlunarlínu fyrir verk

Hægt er að fínstilla nýja verkhluta á áætlunarlínum verksins. Í áætlunarlínu er hægt að fanga upplýsingarnar sem á að rekja fyrir vinnslu. Til dæmis er hægt að rekja tilföng sem vinnslan krefst, eða þær vörur sem þörf er á. Til dæmis er verkefni að fá viðskiptavin til að samþykkja vinnu. Verkið er tengt við áætlunarlínur fyrir vörur eins og að hitta viðskiptavininn og úthluta forða.  

Áætlunarlína getur verið ein af eftirfarandi tegundum.  

| Gerð | Lýsing |
| --- | --- |
| **Fjárhagsáætlun** |Sýnir áætlaða notkun og kostnað við verkið, yfirleitt í verkefni af tíma- og efnisgerð. Ekki er hægt að reikningsfæra áætlunarlínur af þessari gerð. |
| **Reikningshæft** |Sýnir áætlaða reikningsfærslu til viðskiptamanns, yfirleitt í verkefni með fast verð. |
| **Bæði fjárhagsáætlun og reikningshæft** |Sýnir áætlaða notkun sem jafngildir því sem á að reikningsfæra. |

> [!NOTE]
> Þegar upplýsingar um verkáætlunarlínur eru færðar inn eru kostnaðarupplýsingar sjálfkrafa fylltar inn. Til dæmis er kostnaður, verð og afsláttur fyrir aðföng og vörur samkvæmt upplýsingum úr forðagæsinni og vöru. 

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Verk** og velja síðan viðkomandi tengil.
2. Opnið viðeigandi verkspjald.
3. Valinn er verkhluti þar sem reiturinn **Verkhlutagerð** inniheldur **Bókuð** og svo er aðgerðin **Verkhlutalínur** valin.  
4. Á síðunni **Verkáætlunarlínur** skal fylla út reitina eins og þörf krefur í nýrri línu.
5. Endurtakið skref 3 og 4 fyrir allar verkhlutalínur sem þarf fyrir verkhlutann.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/modules/create-new-job/)

## <a name="see-also"></a>Sjá einnig .

[Verkefnastjórnun](projects-manage-projects.md)  
[Myndband: Hvernig á að stofna verk í Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)  
[Sala](sales-manage-sales.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
