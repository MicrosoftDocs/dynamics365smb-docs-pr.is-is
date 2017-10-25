---
title: "Hvernig á að búa til verkflæði úr verkflæðissniðmátum | Microsoft Docs"
description: "Hægt er að búa til verkflæði með verkflæðissniðmátum til að spara tíma þegar ný verkflæði eru stofnuð."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: dcf6f5f5b0364ebcaefdcbc43fdbd7471cb6079e
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-workflows-from-workflow-templates"></a>Hvernig á að: Búa til verkflæði úr verkflæðissniðmátum
Hægt er að búa til verkflæði með verkflæðissniðmátum til að spara tíma þegar ný verkflæði eru stofnuð.  

 Verkflæðissniðmát eru óbreytanleg verkflæði sem eru til staðar í almennu útgáfunni af [!INCLUDE[d365fin](includes/d365fin_md.md)]. Kóðar fyrir verkflæðissniðmát sem bætt er við af Microsoft hafa forskeytið „MS-“.  

 Önnur fljótleg leið til að búa til verkflæði er að flytja inn fyrirliggjandi verkflæði sem til er ótengt[!INCLUDE[d365fin](includes/d365fin_md.md)]. Nánari upplýsingar er að finna í [Hvernig að á flytja verkflæði inn og út](across-how-to-export-and-import-workflows.md)  

Í glugganum **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar. Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir. Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins. Nánari upplýsingar eru í [Hvernig á að: Stofna verkflæði](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-workflow-template"></a>Hvernig á að búa til verkflæði úr verkflæðissniðmátum  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkflæði** og velja svo viðeigandi tengil.  
2.  Velja skal aðgerðina **Stofna verkflæði úr sniðmáti**. Glugginn **sniðmát verkflæðis** opnast.  
3.  Veljið verkflæðissniðmát og smellið á hnappinn **Í lagi**.  

     Glugginn **Verkflæði** opnast fyrir nýtt verkflæði sem inniheldur allar upplýsingarnar úr völdu sniðmáti. Við gildið í reitnum **Kóði** er bætt við t.d. „-01“ til að gefa til kynna að þetta sé fyrsta verkflæðið sem er stofnað úr verkflæðissniðmátinu.  
4.  Haldið áfram til að stofna verkflæði með því að breyta verkflæðisskrefum eða bæta við nýjum skrefum. Nánari upplýsingar eru í [Hvernig á að: Stofna verkflæði](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Sjá einnig  
 [Hvernig á að: Búa til verkflæði](across-how-to-create-workflows.md)   
 [Hvernig á að: Flytja verkflæði inn og út](across-how-to-export-and-import-workflows.md)   
 [Hvernig á að: Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md)   
 [Hvernig á að: Eyða verkflæðum](across-how-to-delete-workflows.md)   
 [Kynning: Uppsetning og notkun innkaupasamþykktar](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Uppsetning verkflæðis](across-set-up-workflows.md)   
 [Nota verkflæði](across-use-workflows.md)   
 [Verkflæði](across-workflow.md)   

