---
title: "Afturkalla bókun færslubókar með bókun bakfærslu| Microsoft Docs"
description: "Ef þú hefur framkvæmt ranga bókun í færslubók, geturðu notað bakfærsluaðgerðina til að afturkalla bókunina með réttri endurskoðunarslóð."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8126a53d59e72276eb1558fd65fe3c0cd53600cc
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-reverse-journal-posting"></a>Hvernig skal: Bakfæra bókun færslubókar
Til að afturkalla ranga bókun færslubókar skal velja færsluna og búa til bakfærslu (færsla sem er alveg eins og upphaflega færslan en með andstæðu tákni í reitnum fyrir upphæð) með sama skjalanúmeri og bókunardagsetningu og upphaflega færslan. Þegar færsla hefur verið bakfærð þarf að búa til rétta færslu.

Aðeins er hægt að bakfæra færslu sem er bókuð frá færslubókarlínu. Færslu er einungis hægt að bakfæra einu sinni.

Frekari upplýsingar um bókun frá færslubók, sjá [Hvernig skal: Bóka færslur beint í fjárhag](finance-how-post-transactions-directly.md)

Hægt er að bakfæra færslur úr öllum **Fjárhagsfærslur** gluggum. Eftirfarandi ferli byggist á **Fjárhagsfærslur** glugganum.

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Að bakfæra færslubókarbókun fjárhagsfærslu
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Fjárhagsfærslur** og velja svo viðeigandi tengil.
2. Veljið færsluna sem á að bakfæra og veljið síðna aðgerðina **Bakfæra færslu**. Athugið að þetta verður að koma úr bókun færslubókar.
3. Í glugganum **Bakfærðar viðskiptafærslur** skal velja viðeigandi línu og svo aðgerðina **Bakfæra**.
4. Velja hnappinn **Já** á staðfestingarskilaboðunum.

## <a name="see-also"></a>Sjá einnig
[Hvernig skal: Bóka færslu beint í Fjárhag](finance-how-post-transactions-directly.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Fjármál](finance.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

