---
title: Setja upp vinnuskýrslur og samþykktarferli þeirra| Microsoft Docs
description: Þú setur upp vinnuskýrslu til að mæla tíma sem er notaður í verk og notkun forða, til að auðvelda þér verkefnastjórnun, mönnun og afkastaveitu.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 1a5bb6f15f568c09aa2e897a7f986bfbcd63de56
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781811"
---
# <a name="set-up-time-sheets"></a>Setja upp vinnuskýrslur
Vinnuskjöl í [!INCLUDE[d365fin](includes/d365fin_md.md)] meðhöndla tímaskráningu í vikulegum stigum sjö daga. Þær eru notaðar til að fylgjast með þeim tíma sem varið er í verk og hægt er að nota þær fyrir einfalda tímaskráningu forða. Áður en hægt er að nota vinnuskýrslur, verður að skilgreina hvernig þær eiga að vera settar upp og grunnstilltar.

Þegar búið er að setja upp hvernig fyrirtækið á að nota vinnuskýrslur er hægt að tilgreina hvort og hvernig tímaskýrslur eru samþykktar. Allt eftir þörfum fyrirtækisins er hægt að tilgreina:

* Einn eða fleiri notendur sem vinnuskýrslustjóra og sem samþykkja allar vinnuskýrslur.
* Vinnuskýrslusamþykkjandi fyrir hvern forða.

Þegar búið er að setja upp vinnuskýrslur er hægt að búa til vinnuskýrslur fyrir forða, úthluta þeim á verkáætlunarlínur og bóka vinnuskýrslulínur. Frekari upplýsingar eru í [Nota vinnuskýrslur](projects-how-use-time-sheets.md).

## <a name="to-set-up-general-information-for-time-sheets"></a>Til að setja upp almennar upplýsingar um vinnuskýrslur
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning forða** og veldu síðan tengda tengilinn.  
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Í reitnum **Vinnuskýrslur eftir samþykkt verks** skal velja einn af eftirfarandi valkostum.

| Valkostur | Lýsing |
| --- | --- |
| **Aldrei** |Notandinn í reitnum **Notandakenni samþykktaraðila vinnuskýrslu** á forðaspjaldinu samþykkir vinnuskýrsluna. |
| **Alltaf** |Notandinn í reitnum **Ábyrgðaraðili** á verkspjaldinu samþykkir vinnuskýrsluna. |
| **Aðeins véla** |Ef vinnuskýrsla vélar er tengd við verk er það notandinn í reitnum **Ábyrgðaraðili** á verkspjaldinu sem samþykkir vinnuskýrsluna. Ef vinnuskýrsla vélar er tengd við forða er það notandinn í reitnum **Notandakenni samþykktaraðila vinnuskýrslu** á forðaspjaldinu sem samþykkir vinnuskýrsluna. |

## <a name="to-assign-a-time-sheet-administrator"></a>Til að tilnefna vinnuskýrslustjóra
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Notandauppsetning** og veldu síðan tengda tengilinn.  
2. Bæta við nýjum notanda ef notandalistinn inniheldur ekki einstaklinginn sem notandinn vill að sé vinnuskýrslustjórnandi. Frekari upplýsingar eru í [Úthluta leyfum til notenda og hópa](ui-define-granular-permissions.md).
3. Velja skal notanda sem á að vera vinnuskýrslustjóri og svo skal velja gátreitinn **Stjórnandi vinnuskýrslu**  

> [!TIP]  
>   Mælt er með að aðeins einn notandi sé tilgreindur sem vinnuskýrslustjóri fyrir fyrirtæki. Í eftirfarandi ferli eru eigandi og samþykkjandi vinnuskýrslu settir upp þar sem samþykkjandi er tilgreindur fyrir hvern forða.  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a>Til að tilgreina eiganda og samþykkjanda vinnuskýrslu
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Forði** og veldu síðan tengda tengilinn.
2. Veljið forðann sem á að geta notað vinnuskýrslur og veljið svo gátreitinn **Nota vinnuskýrslu**.  
3. Í reitinn **Notandakenni eiganda vinnuskýrslu** skal slá inn notandakenni eiganda vinnuskýrslunnar. Eigandinn getur fært inn tímanotkun á vinnuskýrslu og sent hana til samþykktar. Þegar forði er einstaklingur er einstaklingurinn yfirleitt einnig eigandi.  
4. Í reitinn **Notandakenni samþykkjanda vinnuskýrslu** skal slá inn notandakenni samþykkjanda vinnuskýrslunnar. Samþykkjandi getur samþykkt, hafnað eða enduropnað vinnuskýrslu.  

> [!NOTE]  
>   Ekki er hægt að auðkenni samþykkjanda vinnuskýrslu ef tíma fyrir eru tímaskýrslur sem ekki hefur verið unnið með og sem hafa stöðuna **Sent** eða **Opið**.

## <a name="see-also"></a>Sjá einnig
[Setja upp verkefnastjórnun](projects-setup-projects.md)  
[Verkefnastjórnun](projects-manage-projects.md)  
[Fjármál](finance.md)  
[Innkaup](purchasing-manage-purchasing.md)         
[Sala](sales-manage-sales.md)      
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
