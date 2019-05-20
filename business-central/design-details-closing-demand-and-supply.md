---
title: Hönnunarupplýsingar - Lokun eftirspurnar og framboðs | Microsoft Docs
description: Þetta efnisatriði býður upp á tillögu um hvað skuli gera eftir að þú framkvæmir ferli jöfnunar framboðs.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, planning, example, closing, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.openlocfilehash: aa2a5e11f8b669a097a472bab1bda8f7fadc565f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242837"
---
# <a name="design-details-closing-demand-and-supply"></a>Hönnunarupplýsingar: Lokun eftirspurnar og framboðs
Þegar jafnvægisstillingarferli hafa verið framkvæmd eru þrjár hugsanlegar lokaaðstæður:  
  
* Nauðsynlegt magn og dagsetning eftirspurnartilvika hafa verið uppfyllt þeim er hægt að loka. Birgðatilvikið er enn opið og gæti uppfyllt næstu eftirspurn, svo hægt er að hefja afstemmingu að nýju með núverandi birgðatilviki og næstu eftirspurn.  
* Ekki er hægt að breyta birgðapöntuninni svo hún nái yfir alla eftirspurn. Eftirspurnartilvik er enn opinn, með nokkru óuppfylltu magni sem hugsanlega er uppfyllt í næsta framboðstilviki. Þannig er núverandi framboðstilvik lokað, þannig að jöfnunaraðgerð getur byrjað aftur með núverandi eftirspurn og næsta framboðstilviki.  
* Öll eftirspurn hefur verið uppfyllt, engin eftirspurn stendur eftir (eða eftirspurn var ekki til staðar). Ef það er eitthvert afgangsframboð er hægt að minnka það (eða hætta við) og loka síðan. Hugsanlega eru fleiri framboðstilvik til staðar innar í keðjunni og einnig ætti að hætta við þau.  
  
Að lokum mun áætlanakerfið stofna pöntunarrakningartengil milli framboðs og eftirspurnar.  
  
## <a name="creating-the-planning-line-suggested-action"></a>Stiofna áætlunarlínu (Tillögu um aðgerð)  
Ef einhver aðgerð – Ný, Breyta magni, Enduráætla, Enduráætla og breyta magni eða Hætta við – er lögð til til að endurskoða birgðapöntunina býr áætlanakerfið til áætlunarlínu í áætlanavinnublaðinu. Vegna pöntunarrakningar, er áætlunarlína ekki aðeins búin til þegar framboðsatburður er lokaður, en einnig ef eftirspurnaratburði er lokað, jafnvel þótt framboðsatburður er enn opinn og getur verið háð frekari breytingum þegar næsta eftirspurnaratburður er afgreiddur. Þetta þýðir að þegar fyrst búið til er hægt að breyta áætlunarlínu aftur.  
  
Til að lágmarka gagnagrunnsaðgang við meðhöndlun framleiðslu pantanir, áætlunarlína getur verið haldið í þrjú stig, en stefnt að framkvæma einfaldasta viðhald stig:  
  
* Stofna aðeins áætlanagerðarlínu með núverandi gjalddagadagsetningu og magni en án vegvísun og íhlutum.  
* Taka með leið: fyrirhuguð leið er sett fram með útreikningur á upphaf og endir dagsetningar og tíma. Þetta fer eftir aðgangi að gagnagrunni. Til að ákvarða endi og skiladag, kann að vera nauðsynlegt að reikna þetta jafnvel ef framboðstilvik hefur ekki verið lokað (ef um er að ræða framvirk tímasetningu).  
* Taka með uppskriftarsprengingu: Þetta getur bíða þangað til rétt áður en framboðstilvik er lokað.  
  
Þetta lýkur lýsingu á því hvernig eftirspurn og framboð er hlaðið, gefið forgang og jafnað í áætlanakerfinu. Í samþættingu við þessa framboðsáætlunarstarfsemi verður kerfið að tryggja að nauðsynlegt birgðastig hverrar áætlunarvöru sé haldið í samræmi við pöntunarstefnu hennar.  
  
## <a name="see-also"></a>Sjá einnig  
[Hönnunarupplýsingar: Jöfnun eftirspurnar og framboðs](design-details-balancing-demand-and-supply.md)   
[Hönnunarupplýsingar: Miðlægar hugmyndir áætlanakerfisins](design-details-central-concepts-of-the-planning-system.md)   
[Hönnunarupplýsingar: framboðsáætlun](design-details-supply-planning.md)