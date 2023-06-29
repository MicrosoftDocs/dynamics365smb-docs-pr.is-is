---
title: Hvernig á að flytja samþykktarverkflæði inn og út
description: 'Til að flytja verkflæði í annan Business Central gagnagrunn, t.d. til að spara tíma þegar stofnað ný verkflæði, er hægt að flytja út og inn verkflæði.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: edupont
---
# <a name="export-and-import-approval-workflows"></a><a name="export-and-import-approval-workflows"></a>Flytja samþykktarverkflæði inn og út

Til að flytja verkflæði í annan [!INCLUDE[prod_short](includes/prod_short.md)] gagnagrunnur, t.d. til að spara tíma þegar stofnað ný verkflæði, er hægt að flytja út og inn verkflæði.  

Önnur leið til að búa til verkflæði á fljótlegan hátt er að nota verkflæðissniðmát. Frekari upplýsingar eru í [Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).  

Á síðunni **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar. Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir. Þú skilgreinir skref í verkflæði með því að fylla út í reiti í verkflæðislínum úr föstum listum yfir gildi tilvika og svara sem standa fyrir verkflæðissviðsmyndir sem kóði forritsins styður. Frekari upplýsingar eru á [Búa til verkflæði](across-how-to-create-workflows.md).  

## <a name="export-a-workflow"></a><a name="export-a-workflow"></a>Flytja út verkflæði

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Verkflæði** og velja síðan viðkomandi tengil.  
2. Veldu verkflæði, veldu síðan aðgerðina **Flytja út í skrá**.  

## <a name="import-a-workflow"></a><a name="import-a-workflow"></a>Glytja inn verkflæði

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, færa inn **Verkflæði** og velja síðan viðkomandi tengil.  
2. Aðgerðin **Flytja inn úr skrá** er valin.  
3. Á síðunni **Flytja inn** skaltu velja **Velja**, velja XML-skrána sem inniheldur verkflæðið, síðan velja **Opna**.  

> [!CAUTION]  
> Ef verkflæðiskóðinn er þegar til í gagnagrunnur verður skrifað yfir verkflæðisskref með skrefum í innfluttu verkflæði.  

## <a name="see-also"></a><a name="see-also"></a>Sjá einnig .

[Stofna verkflæði samþykktar](across-how-to-create-workflows.md)  
[Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md)  
[Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md)  
[Eyða samþykktarverkflæðum](across-how-to-delete-workflows.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Setja upp Verkflæði samþykktar](across-set-up-workflows.md)  
[Nota Samþykktarverkflæði](across-use-workflows.md)  
[Verkflæði](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
