---
title: Skoða stöðu á samstillingarverkum | Microsoft Docs
description: Kynntu þér hvernig á að skoða stöðuna eftir samstillingu tengdra færslna.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 2371c61c36a17df93ccc1a24c588b12613f5c380
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196616"
---
# <a name="view-the-status-of-synchronization-jobs"></a>Skoða stöðu samstillingarverka
Notaðu síðuna **Samstillingarvillur í tengdum gögnum** til að skoða stöðu samstillingarverka sem hafa verið keyrðar fyrir tengdar færslur í Common Data Service eða [!INCLUDE[crm_md](includes/crm_md.md)] samþættingum. Þetta felur í sér verk sem voru í gangi frá verkröð og handvirk samstillingarverk sem voru í gangi í færslum frá [!INCLUDE[d365fin](includes/d365fin_md.md)]. Til dæmis er gagnlegt að skoða stöðu þeirra við úrræðaleit vegna þess að þú færð aðgang að upplýsingum um villur sem tengjast tengdum færslum. Venjulega koma þessar tegundir af villum upp vegna aðgerða notanda, t.d. þegar:  

* Tveir einstaklingar gerðu breytingu á sömu færslunni í báðum viðskiptaforritunum.
* Einhver eyddi færslu í öðru hvoru forritinu, en ekki í báðum.

> [!Note]
> Á síðunni **Samstillingarvillur í tengdum gögnum** er að finna upplýsingar um verk sem tengjast tengdum færslum. Ef leyst er úr öllum villunum en færslurnar eru enn ekki samstilltar gæti það haft eitthvað að gera með stillingu samþættingarinnar. Venjulega þarf stjórnandi þinn að leysa úr þess konar villum.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Skoða og leysa úr samstillingarvillum fyrir tengdar færslur
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Samstillingarvillur í tengdum gögnum** og veldu síðan tengda tengilinn.
2. Síðan **Samstillingarvillur í tengdum gögnum** sýnir vandamál sem komu upp þegar tengdar færslur voru samstilltar. Eftirfarandi tafla inniheldur aðgerðir sem hægt er að nota til að leysa vandamál eitt í einu:

|Aðgerð|Description|
|----|----|
|**Fjarlægja tengingu**|Aftengir færslurnar og þær samstillast ekki lengur. Til að samstilla færslurnar á ný þarf að tengja þær aftur.|
|**Reyna aftur**|Fyrir hverja færslu þar sem villa finnst er samstillingu sleppt nema vandamálið sé leyst handvirkt. Þegar reynt er aftur verður færslan höfð með í næstu samstillingu.|
|**Samstilla**|Forritið reynir að leysa úr árekstri þar sem færslu var breytt í báðum viðskiptaforritunum. Hægt er að velja útgáfu færslunnar sem á að nota í báðum forritunum.|
|**Endurheimta færslur** og **Eyða færslum**|Þetta er gagnlegt þegar færslu var eytt í einu viðskiptaforritanna. Eyða færslum eyðir færslunni í forritinu þar sem hún er enn til staðar. Endurheimt býr færsluna til aftur í viðskiptaforritinu sem henni var eytt úr.|

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Að skoða samstillingarkladdann fyrir tiltekna (handvirkt samstillta) færslu
1. Opnaðu til dæmis viðskiptamann, vöru eða einhverja aðra færslu sem samstillir gögn milli [!INCLUDE[d365fin](includes/d365fin_md.md)] og Common Data Service eða [!INCLUDE[crm_md](includes/crm_md.md)].
2. Veldu aðgerðina **Samstillingarkladdi** til að skoða samstillingarkladda fyrir valda færslu. Til dæmis tiltekinn viðskiptavin sem var samstilltur handvirkt.

## <a name="see-also"></a>Sjá einnig  
[Uppsetning á notendareikningum fyrir samþættingu við Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Nota Dynamics 365 Sales úr Business Central](marketing-integrate-dynamicscrm.md)
