---
title: "Hvernig á að flytja verkflæði inn og út | Microsoft Docs"
description: "Til að flytja verkflæði í annan Finance and Operations, Business Edition-gagnagrunnur, t.d. til að spara tíma þegar stofnað ný verkflæði, er hægt að flytja út og inn verkflæði."
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6da772f9eefab9aa0ef8b9f47f6ea7656ebef1b4
ms.contentlocale: is-is
ms.lasthandoff: 01/30/2018

---
# <a name="export-and-import-workflows"></a>Flytja verkflæði inn og út
Til að flytja verkflæði í annan [!INCLUDE[d365fin](includes/d365fin_md.md)] gagnagrunnur, t.d. til að spara tíma þegar stofnað ný verkflæði, er hægt að flytja út og inn verkflæði.  

 Önnur leið til að búa til verkflæði er að búa til verkflæði úr verkflæðissniðmátum. Nánari upplýsingar eru í [Stofna verkflæði út frá verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).  

 Í glugganum **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar. Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir. Þú skilgreinir skref í verkflæði með því að fylla út í reiti á verkflæðislínum úr föstum listum yfir tilvik og svör gildi sem standa fyrir verkflæðissviðsmyndir sem eru studd af kóða forritsins. Frekari upplýsingar eru í [Búa til verkflæði](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Til að flytja út verkflæði  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkflæði** og velja svo viðeigandi tengil.  
2.  Veljið Verkflæði og smellið á hnappinn **Flytja út í skrá**.  
3.  Í gluggi **Flytja út skrá** veljið hnappinn **Vista**.  
4.  Í glugganum **Flytja út** skal velja staðsetningu skrána og svo hnappinn **Vista**.  

## <a name="to-import-a-workflow"></a>Til að flytja inn verkflæði  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Verkflæði** og velja svo viðeigandi tengil.  
2.  Aðgerðin **Flytja inn úr skrá** er valin.  
3.  Í glugganum **flytja inn** skal velja XML-skrá sem inniheldur verkflæðið og velja svo hnappinn **opna**.  

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

