---
title: Uppsetning bókunarflokks| Microsoft Docs
description: Yfirlit yfir bókunarflokka sparar tíma og hjálpar við að koma í veg fyrir mistök þegar þú bókar færslur.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting setup, initialize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: c36b365b0828a19fa82ef28f8d901915937995c2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746667"
---
# <a name="setting-up-posting-groups"></a>Uppsetning bókunarflokka
Staða hópar korta aðila eins og viðskiptavini, seljendur, atriði, auðlindir og sölu- og kaupskjöl til almennra reikninga. Þeir spara tíma og hjálpar við að koma í veg fyrir mistök þegar þú bókar færslur. Færslugildin fara á lyklana sem tilgreindir eru í bókunarhópnum fyrir þá tilgreindu einingu. Eina krafan er að þú hafir bókhaldslykla. Nánari upplýsingar er að finna í [Uppsetning bókhaldslykilsins](finance-setup-chart-accounts.md).  

Bókunarflokkar falla undir þrjú atriði:  

* Almennt - Tilgreindu hverjum þú selur og kaupir frá og hvað þú selur og hvað þú kaupir. Þú getur líka sameinað hópa til að tilgreina hluti eins og rekstrarreikninga til að birta eða nota hópa til að sía skýrslur.  
* Sérstakur - Notaðu söluskjöl, til dæmis, í stað þess að senda beint í fjárhag. Þegar þú býrð til færslur í viðskiptamannabókinni, eru samsvarandi færslur gerðar í fjárhagnum.  
* Skattur - Tilgreindu skattprósenturnar og útreikningsgerðir sem eiga við um hverjum þú selur og kaupir frá og hvað þú selur og hvað þú kaupir.

Eftirfarandi töflur lýsa bókunarflokkunum undir hverju tilfelli.  

| Almennir bókunarflokkar | Lýsing |
| --- | --- |
| Almennir viðskiptabókunarflokkar |Úthlutaðu þessum hópi á viðskiptavini og lánardrottna til að tilgreina hverjum þú selur og hverjum þú kaupir frá. Settu þetta upp á síðunni fyrir **Alm. viðskiptabókunarflokkar**. Þegar þú gerir það skaltu hugsa um hversu marga hópa þú þarft fyrir niðurbrog á sölu og kaupum. Til dæmis geturðu flokkað viðskiptavini og lánardrottna eftir svæði, eða eftir tegund viðskipta. |
| Almennir vörubókunarflokkar |Úthlutaðu þessum hópi á hluti og tilföng til að tilgreina hvað þú selur og hvað þú kaupir. Setjið þetta upp á síðunni **Alm. vörubókunarflokkar**. Þegar þú gerir það skaltu hugsa um fjölda hópa sem þú þarft til að brjóta niður sölu eftir vöru (atriði og foprði) og kaup eftir vörum. Til dæmis, skaltu skipta þessum hópum eftir hráefnum, smásölu, tilföngum, getu og svo framvegis. |
| Uppsetning almenns bókunargrunns |Sameina viðskipti og vörubókunarflokka, og veldu lyklana til að bóka á. Fyrir hverja samsetningu viðskipta- og vöruskiptahópa er hægt að tengja saman fjölda aðalbókarreikninga. Til dæmis þýðir þetta að hægt er að bóka sölu sömu vöru á marga sölureikninga í fjárhag þegar viðskiptavinir eru tengdir við marga viðskiptabókunarflokka. Settu þetta upp á síðunni **Almennur bókunargrunnur**. |

| Sértækir bókunarflokkar | Description |
| --- | --- |
| Bókunarflokkar viðskm. |Skilgreindu lyklana sem þú vilt nota þegar þú sendir inn færslur viðskiptakrafa. Ef þú notar birgðir með kröfum eru það almenni viðskiptabókunarflokkurinn sem er úthlutaður viðskiptavininum þínum og almenni vörubókunarflokkurinn sem er úthlutaður birgðavöru sem ákvarða lyklana sem sölupöntunarlínur eru bókaðar á. Sjá „Almennir viðskiptabókunarflokkar“ og „Almennir vörubókunarflokkar“ undir **Almennir bókunarflokkar** hér að ofan. Settu þetta upp á síðunni **Bókunarflokkar viðskiptamanna**. |
| Bókunarflokkar lánardrottna |Tilgreindu hvar á að bóka færslur fyrir viðskiptaskuldir, þjónustureikninga og greiðsluafsláttarreikninga. Þetta er svipað og bókunarflokkur viðskiptamanns. Settu þetta upp á síðunni **Bókunarflokkar lánardrottna**. |
| Birgðabókunarflokkar |Skilgreindu birgðabókunarflokka sem þú úthlutar síðan á viðeigandi vörureikninga á síðunni **Uppsetning birgðabókunar**. Síðan þegar bókaðar eru færslur sem tengjast vöru þá bókar kerfið í fjárhagsreikninginn sem settur var upp fyrir þá samsetningu birgðabókunarflokks og birgðageymslu sem tengist vörunni. Birgðabókunarflokkar bjóða einnig upp á góða leið til að skipuleggja birgðir þínar, þannig að þú getur aðskilið hluti eftir bókunarflokkum þegar þú býrð til skýrslur. Settu þetta upp á síðunni **Birgðabókunarflokkar**. |
| Bókunarflokkar bankareikninga |Skilgreina reikninga fyrir bankareikninga. Til dæmis getur þetta einfalt ferlið við að rekja færslr og samræma bankareikninga. Settu þetta upp á síðunni **Bókunarflokkar bankareikninga**. |
| Bókunarflokkur eigna |Skilgreina reikninga fyrir mismunandi gerðir útgjalda og kostnað, svo sem kaupkostnað, uppsafnaðan afskriftir, kaupkostnað við ráðstöfun, uppsafnað afskriftir við förgun, hagnað af sölu, tapi á förgun, viðhaldskostnaði og afskriftargjöldum. Settu þetta upp á síðunni **Eignabókunarflokkar**. |

| Skattbókunarflokkur | Description |
| --- | --- |
| Skattaviðskiptabókunarflokkar |Ákveða hvernig á að reikna og bóka söluskatti fyrir viðskiptavini og lánardrottna. Setjið þetta upp á síðunni **Skattaviðskiptabókunarflokkar**. Þegar þú gerir það skaltu athuga hversu marga hópa þú þarft. Til dæmis getur þetta oltið á þáttum eins og staðbundinni löggjöf og hvort þú stundar viðskipti innanlands og á alþjóðavettvangi. |
| Skattavörubókunarflokkar |Tilgreindu skattaútreikninga sem þarf til að fá þær tegundir af forða sem þú kaupir eða selur. |
| Uppsetning skattbókunar |Sameina viðskiptabókunarflokk skatta og vörubókunarflokk skatta. Þegar þú fyllir inn almenna færslubókarlínu, innkaupalínu, eða sölulínu, munum við líta á samsetninguna til að bera kennsl á lyklana sem nota skal. |

## <a name="example-of-linking-posting-groups"></a>Dæmi um tengingu bókunarflokka
Hér er sviðsmynd.  

Þessar bókunarflokkar eru valdir á viðskiptamannaspjaldinu:  

* Almennur viðskiptabókunarflokkur
* Bókunarflokkur viðskm.  

Þessar bókunarflokkar eru valdir á birgðaspjaldinu:  

* Almennir vörubókunarflokkar  
* Birgðabókunarflokkur  

Þegar þú býrð til söluskjal, notar söluhausinn upplýsingar úr viðskiptamannaspjaldinu og sölulínur nota upplýsingar af birgðaspjaldinu.  

* Tekjubókunin (rekstrarreikningur) er ákvarðaður af samsetningu almennra viðskiptabókunarflokks og almenns vörubókunarflokks.  
* Bókun viðskiptakrafa (efnahagsreikningur) er ákvörðuð af bókunarflokki viðskiptamanni.  
* Birgðabókun (efnahagsreikningur) er ákvörðuð af birgðabókunarlooknum.  
* Kostnaður seldra vara (rekstrarreikningur) er ákvðarðaður af sameiningu almenns viðskiptabókunarflokks og almenns vörubókunarflokk.  

Uppsetningin þín ákvarðar hvenær bókun á sér stað. Til dæmis er tímasetning ákvörðuð af því þegar þú gerir reglubundna starfsemi, svo sem birgðakostnað eða birgðafærslum.

## <a name="copying-posting-setup-lines"></a>Bókunargrunnslínur afritaðar
Því fleiri vörur og viðskiptabókunarflokk sem þú ert með því fleiri línur sérðu á síðunni almennur bókunargrunnur. Vegna þessa gæti þurft að færa inn mikið af gögnum til að setja upp almennan bókunargrunn fyrir fyrirtækið. Þó að samsetningar viðskipta- og vörubókunarflokkanna séu margar er hægt að bóka þær saman í einn fjárhagsreikning. Til að draga úr handvirkum færslum skal afrita fjárhagsreikninga úr línu á síðunni **Alm. bókunargrunnur**.

## <a name="see-also"></a>Sjá einnig .
[Fjárhagur og bókhaldslyklar](finance-general-ledger.md)  
[Uppsetning Fjármála](finance-setup-finance.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
