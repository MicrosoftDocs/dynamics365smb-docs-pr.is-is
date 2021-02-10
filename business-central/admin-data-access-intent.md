---
title: Umsjón með ástæðu aðgangs að gagnagrunni í Business Central | Microsoft Docs
description: Breyta ástæðu aðgangs að gagnagrunni fyrir skýrslur, API-síður og fyrirspurnir.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6d79f5b2851df85ea9f19faeeb941eccfd1b397b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752826"
---
# <a name="managing-database-access-intent"></a>Umsjón með ástæðu aðgangs að gagnagrunni 

Sem yfirnotandi eða stjórnandi er hægt að breyta ástæðu aðgangs að gagnagrunni fyrir skýrslur, síður af API-gerð og fyrirspurnir til að auka afköst þjónustunnar.

## <a name="overview"></a>Yfirlit

Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að nota skrifvarðar eftirlíkingar af aðalgagnagrunninum (skrifa-lesa). Að nota eftirlíkingu gagnagrunns dregur úr álagi á aðalgagnagrunninum. Í sumum tilfellum eykur það einnig afköst þegar gögn eru skoðuð í biðlaranum. Eftirlíkingar eru gagnlegar fyrir hluti á borð við skýrslur, fyrirspurnir og API-síður, sem eru notaðar til að skoða gögn eingöngu, ekki til að breyta gögnum.

Þegar hlutirnir eru keyrðir er það ástæða aðgangs að gagnagrunni sem sker úr um hvort nota skuli skrifvarða eftirlíkingu ef hún er í boði eða aðalgagnagrunninn. Skýrslur, API-síður og fyrirspurnir eru þróaðar með fyrirframskilgreinda ástæðu fyrir aðgangi (sjá [Eiginleiki DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).

Síðan **Listi yfir ástæður fyrir aðgangi að gagnagrunni** gerir þér kleift að hnekkja fyrirframskilgreindri ástæðu fyrir aðgangi að gagnagrunni fyrir hluti þegar þeir eru keyrðir.

Í gagnagrunni er þessi eiginleiki þekktur sem *lesa útvíkkun*. Frekari upplýsingar um lesa útvíkkun og ástæðu fyrir aðgangi að gagnagrunni í [!INCLUDE[prod_short](includes/prod_short.md)] er að finna í [Nota lesa útvíkkun fyrir aukin afköst](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) í [!INCLUDE[prod_short](includes/prod_short.md)] Developer og IT Pro hjálp.

## <a name="to-change-the-database-access-intent"></a>Breyta ástæðu fyrir aðgangi að gagnagrunni

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Listi yfir ástæður fyrir aðgangi að gagnagrunni** og veldu síðan tengda tengilinn.

    Á síðunni er listi yfir allar skýrslur, síður og fyrirspurnir. Dálkurinn **Ástæða aðgangs** inniheldur eitt af eftirfarandi gildum:

    |**Stilling**|**Lýsing**|  
    |------------|-------------|  
    |**Sjálfgefið**|Gefur til kynna að hluturinn notar fyrirframskilgreinda ástæðu fyrir aðgangi að gagnagrunni.|
    |**Leyfa að skrifa**|Stillir hlutinn þannig að hann noti aðalgagnagrunninn, sem gerir notanda kleift að breyta gögnum.|
    |**Skrifvarið**|Stillir hlutinn þannig að hann noti eftirlíkingu gagnagrunns, sem þýðir að notandi getur aðeins skoðað gögn, ekki breytt þeim.|

2. Veldu aðgerðina **Breyta lista**.

3. Á síðunni **Breyta - Listi yfir ástæður fyrir aðgangi að gagnagrunni** skal breyta reitnum **Ástæða aðgangs** fyrir hlutina.

    > [!NOTE]
    > Ef hlutur sem er breytanlegur, eins og Viðskiptamannaspjald, er stilltur á **Skrifvarið**, verður aðalgagnagrunnurinn ennþá notaður óháð ástæðu fyrir aðgangi, sem gerir notendum kleift að gera breytingar eins og venjulega.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengda þjálfun á [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig
[Viðskiptavirkni](across-business-functionality.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Hafist handa](product-get-started.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
