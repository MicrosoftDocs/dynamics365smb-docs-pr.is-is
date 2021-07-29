---
title: Skoða stöðu samstillingarverka
description: Notaðu síðuna Samstillingarvillur í tengdum gögnum til að skoða stöðu samstillingarverka sem hafa verið keyrðar fyrir tengdar færslur í samþættingum.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: 0a33631908d0f3943486f96bbf6b5e2f801c440b
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441319"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Skoða stöðu samstillingarverka
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Notaðu síðuna **Samstillingarvillur í tengdum gögnum** til að skoða stöðu samstillingarverka sem hafa verið keyrðar fyrir tengdar færslur í Dataverse eða [!INCLUDE[crm_md](includes/crm_md.md)] samþættingum. Þetta felur í sér verk sem voru í gangi frá verkröð og handvirk samstillingarverk sem voru í gangi í færslum frá [!INCLUDE[prod_short](includes/prod_short.md)]. Til dæmis er gagnlegt að skoða stöðu þeirra við úrræðaleit vegna þess að þú færð aðgang að upplýsingum um villur sem tengjast tengdum færslum. Venjulega koma þessar tegundir af villum upp vegna aðgerða notanda, t.d. þegar:  

* Tveir einstaklingar gerðu breytingu á sömu gögnunum í báðum viðskiptaforritunum.
* Einhver eyddi gögnum í öðru hvoru forritinu, en ekki í báðum.

> [!Note]
> Á síðunni **Samstillingarvillur í tengdum gögnum** er að finna upplýsingar um verk sem tengjast tengdum færslum. Ef leyst er úr öllum villunum en færslurnar eru enn ekki samstilltar gæti það haft eitthvað að gera með stillingu samþættingarinnar. Venjulega þarf stjórnandi þinn að leysa úr þess konar villum.   

<!--

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

-->

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Skoða og leysa úr samstillingarvillum fyrir tengdar færslur
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, farðu í **Samstillingarvillur í tengdum gögnum** og veldu síðan tengda tengilinn.
2. Síðan **Samstillingarvillur í tengdum gögnum** sýnir vandamál sem komu upp þegar tengdar færslur voru samstilltar. Eftirfarandi tafla inniheldur aðgerðir sem hægt er að nota til að leysa vandamál eitt í einu:

|Aðgerð|Description|
|----|----|
|**Fjarlægja tengingu**|Aftengir færslurnar og þær samstillast ekki lengur. Til að endurræsa samstillinguna þarf að tengja þær aftur. |
|**Reyna aftur** og **Reyna allt**|Fyrir hverja færslu þar sem villa finnst er samstillingu sleppt nema vandamálið sé leyst. Þegar reynt er aftur verður valin færsla höfð með í næstu samstillingu og **Reyna allt aftur** inniheldur allar færslurnar.|
|**Samstilla**|Forritið reynir að leysa úr árekstri þar sem gögnum var breytt í báðum viðskiptaforritunum. Hægt er að velja gögnin sem á að nota.|
|**Endurheimta færslur** og **Eyða færslum**|Þetta er gagnlegt þegar færslu var eytt í einu viðskiptaforritanna. Eyða færslum eyðir færslunni eða línunni í forritinu þar sem hún er enn til staðar. Endurheimt færsla býr færsluna eða línuna til aftur í viðskiptaforritinu sem henni var eytt úr.|

> [!NOTE]
> Til að draga úr þeim fjölda árekstra sem þarf að leysa er hægt að setja upp varpanir samþættingartöflu til að nota þessar aðgerðir sjálfkrafa. Frekari upplýsingar er að finna í [Vörpun samþættingartaflna](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Að skoða samstillingarkladdann fyrir tiltekna (handvirkt samstillta) færslu
1. Opnaðu til dæmis viðskiptamann, vöru eða einhverja aðra færslu sem samstillir gögn milli [!INCLUDE[prod_short](includes/prod_short.md)] og Dataverse eða [!INCLUDE[crm_md](includes/crm_md.md)].
2. Veldu aðgerðina **Samstillingarkladdi** til að skoða samstillingarkladda fyrir valda færslu. Til dæmis tiltekinn viðskiptavin sem var samstilltur handvirkt.

## <a name="see-also"></a>Sjá einnig  
[Uppsetning á notendareikningum fyrir samþættingu við Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Nota Dynamics 365 Sales úr Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]