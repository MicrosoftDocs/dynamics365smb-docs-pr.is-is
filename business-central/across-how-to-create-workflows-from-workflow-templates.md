---
title: "Hvernig á að búa til verkflæði úr verkflæðissniðmátum | Microsoft Docs"
description: "Hægt er að búa til verkflæði með verkflæðissniðmátum til að spara tíma þegar ný verkflæði eru stofnuð."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 0ae5a7a308568dd8ede10c485564824685963bf4
ms.contentlocale: is-is
ms.lasthandoff: 11/26/2018

---
# <a name="create-workflows-from-workflow-templates"></a>Búa til verkflæði úr verkflæðissniðmátum
Hægt er að búa til verkflæði með verkflæðissniðmátum til að spara tíma þegar ný verkflæði eru stofnuð.  

 Verkflæðissniðmát eru óbreytanleg verkflæði sem eru til staðar í almennu útgáfunni af [!INCLUDE[d365fin](includes/d365fin_md.md)]. Kóðar fyrir verkflæðissniðmát sem bætt er við af Microsoft hafa forskeytið „MS-“.  

 Önnur fljótleg leið til að búa til verkflæði er að flytja inn fyrirliggjandi verkflæði sem til er ótengt[!INCLUDE[d365fin](includes/d365fin_md.md)]. Frekari upplýsingar eru í [Flytja verkflæði inn og út](across-how-to-export-and-import-workflows.md).  

Á síðunni **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar. Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir. Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins. Frekari upplýsingar eru í [Búa til verkflæði](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-workflow-template"></a>Hvernig á að búa til verkflæði úr verkflæðissniðmátum  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **verkflæði** og veldu síðan tengda tengilinn.  
2.  Velja skal aðgerðina **Stofna verkflæði úr sniðmáti**. Síðan **Sniðmát verkflæðis** opnast.  
3.  Veljið verkflæðissniðmát og smellið á hnappinn **Í lagi**.  

     Síðan **Verkflæði** opnast fyrir nýtt verkflæði sem inniheldur allar upplýsingarnar úr völdu sniðmáti. Við gildið í reitnum **Kóði** er bætt við t.d. „-01“ til að gefa til kynna að þetta sé fyrsta verkflæðið sem er stofnað úr verkflæðissniðmátinu.  
4.  Haldið áfram til að stofna verkflæði með því að breyta verkflæðisskrefum eða bæta við nýjum skrefum. Frekari upplýsingar eru í [Búa til verkflæði](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Sjá einnig  
 [Búa til verkflæði](across-how-to-create-workflows.md)   
 [Flytja verkflæði inn og út](across-how-to-export-and-import-workflows.md)   
 [Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md)   
 [Eyða verkflæðum](across-how-to-delete-workflows.md)   
 [Kynning: Uppsetning og notkun verkflæði innkaupasamþykktar](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Uppsetning verkflæðis](across-set-up-workflows.md)   
 [Nota verkflæði](across-use-workflows.md)   
 [Verkflæði](across-workflow.md)   

