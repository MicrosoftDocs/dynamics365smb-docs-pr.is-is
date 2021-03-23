---
title: Yfirlit bókunarlínu færslubókar | Microsoft Docs
description: Þetta efnisatriði fjallar um breytingar á Kóðaeining 12, **Bókunarlína fjárhags**, sem er helsti forritahluti bókana í fjárhag og er eini staðurinn þar sem færslur í fjárhag, VSK, viðskiptamenn og lánardrottna eru settar inn.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7ed6c60ddf1be51bbbc14eb8384cdc4ac05337ac
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390225"
---
# <a name="general-journal-post-line-overview"></a>Yfirlit bókunarlínu færslubókar
Kóðaeining 12, **Bókunarlína fjárhags**, er helsti forritahluti bókana í fjárhag og er eini staðurinn þar sem færslur í fjárhag, VSK, viðskiptamenn og lánardrottna eru settar inn. Kóðaeiningin er einnig notuð fyrir allar aðgerðir Jafna, Ógilda og Reverse.  
  
Þrátt fyrir að kóðaeiningin hafi verið endurbætt í hverri útgáfu síðustu tíu ár var arkitektúr hennar nákvæmlega sá sami. Kóðaeiningin varð mjög stór, með u.þ.b. 7.600 kóðalínum. Í þessari útgáfu af [!INCLUDE[prod_short](includes/prod_short.md)] er arkitektúrnum breytt og kóðaeiningin hefur verið gerð einfaldari og auðveldara er að viðhalda henni. Í þessu eru breytingar tilteknar og upplýsingar fyrir skilyrði uppfærslu gefnar.  
  
## <a name="old-architecture"></a>Eldri arkitektúr  
Eldri arkitektúr var með eftirfarandi eiginleika:  
  
* Mikið var um notkun alþjóðlegra breyta, sem jók möguleikann á földum villum vegna notkun breyta með röngu umfangi.  
* Það voru mörg löng ferli (með yfir 100 kóðalínum) sem voru einnig með flóknum mælingum (þ.e. mörgum CASE, REPEAT, IF földum segðum) sem gerðu það erfitt að lesa og viðhalda kóða.  
* Nokkur ferli sem voru aðeins notuð staðbundið og var aðeins ætla að vera notað staðbundið voru ekki merkt sem staðbundin.  
* Flest ferli höfðu engar færibreytur og notuðu altækar breytur. Sumir notuðu færibreytur og yfirskrifuð altækar breytur með staðbundnum.  
* Kóðamynstur fyrir leit í fjárhagsreikningi og stofnun fjárhags og VSK færslna var ekki staðlað og breytilegt frá stað til staðs. Að auki var mikið um endurtekinn kóða og ósamhverfu milli kóða viðskiptamanna og lánardrottna.  
* Stór hluti kóðans í kóðaeiningu 12, um 30 prósent, tengdur greiðsluafslætti og útreikningi á vikmörkum, þó svo þessir eiginleikar séu ekki nauðsynlegar í mörgum löndum eða svæðum.  
* Bókun, jöfnun, ógilda, Reverse, greiðsluafsláttur og vikmörk og gengisleiðréttingar voru sameinaðar í kóðaeiningu 12 með löngum lista altækra breyta.  
  
### <a name="new-architecture"></a>Nýr arkitektúr  
Í [!INCLUDE[prod_short](includes/prod_short.md)], hafa eftirfarandi bætur verið gerðar á kóðaeiningu 12:  
  
* Kóðaeining 12 hefur verið endurbætt í smærri ferli (allir innan við 100 kóðalínur).  
* Staðlað mynstur fyrir leit fjárhagsreiknings sem hefur verið sett inn með hjálparaðgerð úr bókunarflokkstöflum.  
* Bókunarvélarrammi hefur verið settur inn til að stjórna upphafi og lokum færslna og einangra stofnun í fjárhag og VSK-færslur, söfnun VSK-leiðréttingum og útreikningi viðbótarupphæðum gjaldmiðla.  
* Kóðatvíverknaður hefur verið útilokaður.  
* Margir hjálparvalkostir hafa verið fluttir í viðkomandi töflur viðskiptamanna- og lánardrottnafærsla.  
* Notkun alþjóðlegra breyta hefur verið lágmörkuð þannig að hvert ferli noti breytur og eigin rökbreytum.  
  
## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Uppbygging bókunarviðmóts](design-details-posting-interface-structure.md)   
[Hönnunarupplýsingar: Uppbygging bókunarvélar](design-details-posting-engine-structure.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]