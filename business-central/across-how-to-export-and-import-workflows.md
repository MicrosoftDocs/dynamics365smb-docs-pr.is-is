---
title: Hvernig á að flytja verkflæði inn og út | Microsoft Docs
description: Til að flytja verkflæði í annan Business Central gagnagrunn, t.d. til að spara tíma þegar stofnað ný verkflæði, er hægt að flytja út og inn verkflæði.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6f47b137a2915f790b510c0fd66944a4fe7814ca
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384425"
---
# <a name="export-and-import-workflows"></a>Flytja verkflæði inn og út
Til að flytja verkflæði í annan [!INCLUDE[prod_short](includes/prod_short.md)] gagnagrunnur, t.d. til að spara tíma þegar stofnað ný verkflæði, er hægt að flytja út og inn verkflæði.  

 Önnur leið til að búa til verkflæði er að búa til verkflæði úr verkflæðissniðmátum. Nánari upplýsingar eru í [Stofna verkflæði út frá verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).  

 Á síðunni **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar. Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir. Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins. Frekari upplýsingar eru í [Búa til verkflæði](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Til að flytja út verkflæði  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkflæði** og veldu síðan tengda tengilinn.  
2.  Veljið Verkflæði og smellið á hnappinn **Flytja út í skrá**.  
3.  Á síðunni **Flytja út skrá** skal velja hnappinn **Vista**.  
4.  Á síðunni **Flytja út** skal velja staðsetningu skrána og svo hnappinn **Vista**.  

## <a name="to-import-a-workflow"></a>Til að flytja inn verkflæði  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Verkflæði** og veldu síðan tengda tengilinn.  
2.  Aðgerðin **Flytja inn úr skrá** er valin.  
3.  Á síðunni **Flytja inn** skal velja XML-skrá sem inniheldur verkflæðið og velja svo hnappinn **opna**.  

> [!CAUTION]  
>  Ef verkflæðiskóðinn er þegar til í gagnagrunnur verður skrifað yfir verkflæðisskref með skrefum í innfluttu verkflæði.  

## <a name="see-also"></a>Sjá einnig  
 [Búa til verkflæði](across-how-to-create-workflows.md)   
 [Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md)   
 [Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md)   
 [Eyða verkflæðum](across-how-to-delete-workflows.md)   
 [Kynning: Uppsetning og notkun verkflæði innkaupasamþykktar](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Uppsetning verkflæðis](across-set-up-workflows.md)   
 [Nota verkflæði](across-use-workflows.md)   
 [Verkflæði](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]