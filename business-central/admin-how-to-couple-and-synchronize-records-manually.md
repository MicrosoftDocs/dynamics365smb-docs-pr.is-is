---
title: Tengja og samstilla færslur handvirkt| Microsoft Docs
description: Samstilling samþættingartöflu virkjar gagnasamþættingu í öllum færslum í töflu í Business Central og Dynamics 365 Sales einingu sem eru tengdar.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: d8140f71709208a271eff5c8de415b0e95736072
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911406"
---
# <a name="couple-and-synchronize-records-manually"></a>Tengja og samstilla færslur handvirkt
Þetta efnisatriði lýsir því hvernig á að tengja eina eða fleiri færslur í [!INCLUDE[d365fin](includes/d365fin_md.md)] við færslur í Common Data Service eða [!INCLUDE[crm_md](includes/crm_md.md)]. Að tengja færslur gerir þér kleift að skoða Common Data Service upplýsingar úr [!INCLUDE[d365fin](includes/d365fin_md.md)] og öfugt. Tenging gerir þér einnig að samstilla gögn á milli færslna. Hægt er að tengja fyrirliggjandi færslur eða stofna og tengja nýjar færslur.

> [!Note]
> Tenging og samstilling gagna við er aðeins í boði ef kerfisstjórinn hefur búið til tengingu milli [!INCLUDE[d365fin](includes/d365fin_md.md)] og Common Data Service eða [!INCLUDE[crm_md](includes/crm_md.md)]. Fljótleg leið til að athuga þetta er að opna spjaldið **Viðskiptamaður** og leita að aðgerðinni **Setja upp tengingu** . Ef aðgerðin er tiltæk eru forritin tengd.   

## <a name="video-example"></a>Myndbandsdæmi

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Til að tengja færslu  
1.  Í [!INCLUDE[d365fin](includes/d365fin_md.md)] skal opna spjaldið fyrir færsluna sem á að tengja. Til dæmis viðskiptamanna- eða tengiliðaspjald.  

    Einnig er hægt að opna listasíðu og velja færsluna sem á að tengja.  

2.  Veldu aðgerðina **Setja upp tengingu** .  
3.  Fylltu út reitina og smelltu síðan á hnappinn **Í lagi** .  

## <a name="to-synchronize-a-single-record"></a>Til að samstilla staka færslu  
1.  Í [!INCLUDE[d365fin](includes/d365fin_md.md)] skal opna spjaldið fyrir færsluna sem á að tengja. Til dæmis viðskiptamanna- eða tengiliðaspjald.  
2.  Veldu aðgerðina **Samstilla núna** .  
3.  Ef hægt er að samstilla færslu í aðra áttina, skal velja valkostinn sem tilgreinir átt gagnauppfærslu og velja síðan **Í lagi** .  

## <a name="to-synchronize-a-single-record-from-crm_md"></a>Að samstilla staka færslu úr [!INCLUDE[crm_md](includes/crm_md.md)]  
1.  Í [!INCLUDE[crm_md](includes/crm_md.md)] skal opna skjámynd fyrir færsluna sem á að tengja. Til dæmis skjámynd reiknings- eða tengiliðaspjalds.  
2.  Veldu aðgerðina **[!INCLUDE[d365fin](includes/d365fin_md.md)]** í borðanum til að opna og tengja færslu sjálfkrafa.

> [!Note]
> Aðeins er hægt að samstilla staka færslu úr [!INCLUDE[crm_md](includes/crm_md.md)] sjálfkrafa þegar **Aðeins samstilla tengdar færslur** er óvirk og samstillingaráttin er stillt á tvíátta eða „Frá samþættingartöflu“ á síðunni **Vörpun samþættingartöflu** fyrir færsluna. Frekari upplýsingar er að finna í [Vörpun á töflum og reitum fyrir samstillingu](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).     

## <a name="to-synchronize-multiple-records"></a>Til að samstilla margar færslur  
1.  Í [!INCLUDE[d365fin](includes/d365fin_md.md)] er opnuð listasíða fyrir færsluna, t.d. listasíður viðskiptamanna eða tengiliða.  
2.  Veldu færslurnar sem á að samstilla og veldu svo aðgerðina **Samstilla núna** .  
3.  Ef hægt er að samstilla færslur í eina átt skal velja valkostinn sem tilgreinir stefnuna og velja svo **Í lagi** .  

## <a name="see-also"></a>Sjá einnig  
[Nota Dynamics 365 Sales úr Business Central](marketing-integrate-dynamicscrm.md)
