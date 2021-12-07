---
title: Tenging og samstilling
description: Samstilling samþættingartöflu virkjar gagnasamþættingu í öllum færslum í töflu í Business Central og Dynamics 365 Sales töflu sem eru tengdar.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2021
ms.author: bholtorf
ms.openlocfilehash: c21d06eaaa9200bb11839d1b2db1666c816638b3
ms.sourcegitcommit: a6000804ad9a176de5750372d3951547ddb71006
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2021
ms.locfileid: "7865391"
---
# <a name="coupling-and-synchronizing-records-between-dataverse-and-business-central"></a>Coupling og samstilla færslur milli Dataverse og Business Central

Í þessu efnisatriði er lýst því hvernig á að ein-eða fleiri færslur séu [!INCLUDE[prod_short](includes/prod_short.md)] með færslur í Dataverse eða [!INCLUDE[crm_md](includes/crm_md.md)]. Coupling-færslur gerir þér kleift að skoða Dataverse upplýsingar frá [!INCLUDE[prod_short](includes/prod_short.md)] og öfugt. Tenging gerir þér einnig að samstilla gögn á milli færslna. Hægt er að tengja fyrirliggjandi færslur eða stofna og tengja nýjar færslur.

> [!Note]
> Coupling og samstilling gagna er aðeins tiltæk ef Kerfisstjórinn hefur stofnað tengingu milli [!INCLUDE[prod_short](includes/prod_short.md)] og Dataverse eða [!INCLUDE[crm_md](includes/crm_md.md)]. Fljótleg leið til að athuga þetta er að opna spjaldið **Viðskiptamaður** og leita að aðgerðinni **Setja upp tengingu**. Ef aðgerðin er tiltæk eru forritin tengd.   

## <a name="video-example"></a>Myndbandsdæmi
Þetta myndefni sýnir festingu og samstillingu gagna í samhengi við samþættingu [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Til að tengja færslu  
1.  Í [!INCLUDE[prod_short](includes/prod_short.md)] skal opna spjaldið fyrir færsluna sem á að tengja. Til dæmis viðskiptamanna- eða tengiliðaspjald.  

    Einnig er hægt að opna listasíðu og velja færsluna sem á að tengja.  

2.  Veldu aðgerðina **Setja upp tengingu**.  
3.  Fylltu út reitina og smelltu síðan á hnappinn **Í lagi**.  

## <a name="to-synchronize-a-single-record"></a>Til að samstilla staka færslu  
1.  Í [!INCLUDE[prod_short](includes/prod_short.md)] skal opna spjaldið fyrir færsluna sem á að tengja. Til dæmis viðskiptamanna- eða tengiliðaspjald.  
2.  Veldu aðgerðina **Samstilla núna**.  
3.  Ef hægt er að samstilla færslu í aðra áttina, skal velja valkostinn sem tilgreinir átt gagnauppfærslu og velja síðan **Í lagi**.  

## <a name="to-synchronize-a-single-record-from-crm_md"></a>Að samstilla staka færslu úr [!INCLUDE[crm_md](includes/crm_md.md)]  
1.  Í [!INCLUDE[crm_md](includes/crm_md.md)] skal opna skjámynd fyrir færsluna sem á að tengja. Til dæmis skjámynd reiknings- eða tengiliðaspjalds.  
2.  Veldu aðgerðina **[!INCLUDE[prod_short](includes/prod_short.md)]** í borðanum til að opna og tengja færslu sjálfkrafa.

> [!Note]
> Aðeins er hægt að samstilla staka færslu úr [!INCLUDE[crm_md](includes/crm_md.md)] sjálfkrafa þegar **Aðeins samstilla tengdar færslur** er óvirk og samstillingaráttin er stillt á tvíátta eða „Frá samþættingartöflu“ á síðunni **Vörpun samþættingartöflu** fyrir færsluna. Frekari upplýsingar er að finna í [Vörpun á töflum og reitum fyrir samstillingu](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).     

## <a name="to-couple-multiple-records-using-match-based-coupling"></a>Að tengja margar færslur með því að nota tengi sem byggir á samsvörun

Hægt er að tilgreina gögnin sem á að samstilla fyrir einingu, t.d. viðskiptavin eða tengilið, með því að tengja skrár sem byggir á samsvörun. Hægt er að fínstilla samsvörunina með því að gera leitina næma og úthluta forgangi fyrir hverja samsvörun. Ef engin samsvörun finnst er einnig hægt að tilgreina að stofna eigi eininguna í Dataverse. Frekari upplýsingar er að finna í [Sérstilla tengingu sem byggir á samsvörun](admin-how-to-set-up-a-dynamics-crm-connection.md#customize-the-match-based-coupling).  

1. Í [!INCLUDE[prod_short](includes/prod_short.md)] er opnuð listasíða fyrir færsluna, t.d. listasíður viðskiptamanna eða tengiliða.
2. Veldu aðgerðina **Tenging byggð á samsvörun**.
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-synchronize-multiple-records"></a>Til að samstilla margar færslur  
1.  Í [!INCLUDE[prod_short](includes/prod_short.md)] er opnuð listasíða fyrir færsluna, t.d. listasíður viðskiptamanna eða tengiliða.  
2.  Veldu færslurnar sem á að samstilla og veldu svo aðgerðina **Samstilla núna**.  
3.  Ef hægt er að samstilla færslur í eina átt skal velja valkostinn sem tilgreinir stefnuna og velja svo **Í lagi**.  

## <a name="uncoupling-records"></a>Aftengja færslur
Hægt er að aftengja eina eða fleiri færslur af listasíðum eða síðunni **Samstillingarvillur í tengdum gögnum** með því að velja eina eða fleiri línu og velja **Eyða tengingu**. Einnig er hægt að fjarlægja allar tengingar fyrir eina eða fleiri töfluvörpun á síðunni **Vörpun samþættingartöflu**.

## <a name="see-also"></a>Sjá einnig  
[Nota Dynamics 365 Sales úr Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]