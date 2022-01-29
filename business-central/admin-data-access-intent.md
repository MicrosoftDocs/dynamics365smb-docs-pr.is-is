---
title: Umsjón með aðgengi að gagnagrunni á Viðskiptamiðmið-
description: Breyta ástæðu aðgangs að gagnagrunni fyrir skýrslur, API-síður og fyrirspurnir.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9880
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: f1f77c4c1506db6d4f90d5d13f7c22ca54f44eac
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/19/2022
ms.locfileid: "8011205"
---
# <a name="managing-database-access-intent"></a>Umsjón með ástæðu aðgangs að gagnagrunni

Sem yfirnotandi eða stjórnandi er hægt að breyta ástæðu aðgangs að gagnagrunni fyrir skýrslur, síður af API-gerð og fyrirspurnir til að auka afköst þjónustunnar.

## <a name="overview"></a>Yfirlit

Hægt er að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að nota skrifvarðar eftirlíkingar af aðalgagnagrunninum (skrifa-lesa). Að nota eftirlíkingu gagnagrunns dregur úr álagi á aðalgagnagrunninum. Í sumum tilfellum eykur það einnig afköst þegar gögn eru skoðuð í biðlaranum. Eftirlíkingar eru gagnlegar fyrir hluti á borð við skýrslur, fyrirspurnir og API-síður, sem eru notaðar til að skoða gögn eingöngu, ekki til að breyta gögnum.

Þegar hlutirnir eru keyrðir er það ástæða aðgangs að gagnagrunni sem sker úr um hvort nota skuli skrifvarða eftirlíkingu ef hún er í boði eða aðalgagnagrunninn. Skýrslur, API-síður og fyrirspurnir eru þróaðar með fyrirframskilgreinda ástæðu fyrir aðgangi (sjá [Eiginleiki DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).

Síðan **Listi yfir ástæður fyrir aðgangi að gagnagrunni** gerir þér kleift að hnekkja fyrirframskilgreindri ástæðu fyrir aðgangi að gagnagrunni fyrir hluti þegar þeir eru keyrðir.

Í gagnagrunni er þessi eiginleiki þekktur sem *lesa útvíkkun*. Frekari upplýsingar um lesa útvíkkun og ástæðu fyrir aðgangi að gagnagrunni í [!INCLUDE[prod_short](includes/prod_short.md)] er að finna í [Nota lesa útvíkkun fyrir aukin afköst](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) í [!INCLUDE[prod_short](includes/prod_short.md)] Developer og IT Pro hjálp.

## <a name="to-change-the-database-access-intent"></a>Breyta ástæðu fyrir aðgangi að gagnagrunni

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Listi yfir ástæður fyrir aðgangi að gagnagrunni** og veldu síðan tengda tengilinn.

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
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]