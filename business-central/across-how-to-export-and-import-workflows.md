---
title: Hvernig á að flytja samþykktarverkflæði inn og inn
description: Til að flytja verkflæði í annan Business Central gagnagrunn, t.d. til að spara tíma þegar stofnað ný verkflæði, er hægt að flytja út og inn verkflæði.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/08/2022
ms.author: edupont
ms.openlocfilehash: 873f168bf8a707519af9a6429658e8383ab1f41e
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585418"
---
# <a name="export-and-import-approval-workflows"></a>Flytja samþykktarverkflæði út og flytja út

Til að flytja verkflæði í annan [!INCLUDE[prod_short](includes/prod_short.md)] gagnagrunnur, t.d. til að spara tíma þegar stofnað ný verkflæði, er hægt að flytja út og inn verkflæði.  

Önnur leið til að stofna verkflæði á fljótlegan hátt er að nota verkflæðissniðmát. Frekari upplýsingar um [Stofna verkflæði úr Verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md).  

Á síðunni **Verkflæði** er hægt að stofna verkflæði með því að skrá viðkomandi skref í línurnar. Hvert skref samanstendur af atburði verkflæðis, breytt eftir atburður skilyrði, og verkflæðissvar, breytt eftir svarvalkostir. Verkflæðisskrefum er skilgreint með því að fylla út reiti í verkflæðislínum með því að nota fasta lista yfir tilvik og svargildi sem tákna áætlanir sem styðja með forritskóta Frekari upplýsingar um [Stofna verkflæði](across-how-to-create-workflows.md).  

## <a name="export-a-workflow"></a>Flytja út verkflæði

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **verkflæði** og velja síðan tengdan tengil.  
2. Velja verkflæði og velja **síðan útflutning til að skrá** aðgerð.  

## <a name="import-a-workflow"></a>Flytja inn verkflæði

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **verkflæði** og velja síðan tengdan tengil.  
2. Aðgerðin **Flytja inn úr skrá** er valin.  
3. **Á innflutningssíðunni**, Veldu **Velja**, Veldu XML-skrána sem inniheldur verkflæðið og veldu **svo Open**.  

> [!CAUTION]  
> Ef verkflæðiskóðinn er þegar til í gagnagrunnur verður skrifað yfir verkflæðisskref með skrefum í innfluttu verkflæði.  

## <a name="see-also"></a>Sjá einnig .

[Stofna samþykktarverkflæði](across-how-to-create-workflows.md)  
[Búa til verkflæði úr verkflæðissniðmátum](across-how-to-create-workflows-from-workflow-templates.md)  
[Skoða verkflæðisskrefstilvik í skráasafni](across-how-to-view-archived-workflow-step-instances.md)  
[Eyða samþykktarverkflæði](across-how-to-delete-workflows.md)  
[Kynning: Uppsetning og notkun á samþykktarverkflæði innkaupa](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Uppsetning Samþykktarverkflæðis](across-set-up-workflows.md)  
[Nota samþykktarverkflæði](across-use-workflows.md)  
[Verkflæði](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
