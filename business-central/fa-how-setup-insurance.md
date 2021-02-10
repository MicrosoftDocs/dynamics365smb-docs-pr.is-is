---
title: Uppsetning vátrygginga eigna| Microsoft Docs
description: Sett er upp vátryggingarspjald og almennar vátryggingaupplýsingar til að stjórna vátryggingasviði eigna.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c5c9af3a076647380e2f6bed8ef7d0a55c3d8efe
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749294"
---
# <a name="set-up-fixed-asset-insurance"></a>Uppsetning vátryggingar eignar.
Til að stjórna vátryggingasviði eigna, þarf fyrst að setja upp nokkrar almennar vátryggingaupplýsingar og vátryggingarspjald á hvert tryggingaskírteini.

## <a name="to-set-up-general-insurance-information"></a>Uppsetning almennra vátryggingaupplýsinga
Til að nota tryggingaraðgerðirnar í [!INCLUDE[prod_short](includes/prod_short.md)] verður þú að setja upp almennar tryggingarupplýsingar.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetningar eigna** og veldu síðan tengda tengilinn.  
2. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Uppsetning vátryggingategunda
Hægt er að flokka vátryggingar, til dæmis í tryggingar vegna þjófnaðar eða brunatryggingu. Vátryggingategundirnar eru notaðar á vátryggingaspjaldinu.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Vátryggingategundir** og veldu síðan tengda tengilinn.  
2. Fyllið inn í svæðin eftir þörfum.

## <a name="to-set-up-insurance-cards"></a>Uppsetning vátryggingaspjalda
Hægt er að safna saman upplýsingum um hverja vátryggingu á vátryggingaspjaldinu.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Trygging** og veldu síðan tengda tengilinn.  
2. Á síðunni **Vátrygging** skal velja aðgerðina **Nýtt** til að stofna nýtt vátryggingarspjald.  
3. Fyllið inn reitina eftir þörfum.

## <a name="to-set-up-insurance-journal-templates"></a>Uppsetning vátryggingabókasniðmáta
[!INCLUDE[prod_short](includes/prod_short.md)] skapar sjálfkrafa vátryggingarsniðmát í fyrsta skipti sem þú opnar síðuna **Vátryggingabók**, en þú getur sett upp viðbótarsniðmát færslubókar. Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sniðmát vátryggingabóka** og veldu síðan tengda tengilinn.  
2. Fyllið inn í svæðin eftir þörfum.

## <a name="to-set-up-insurance-journal-batches"></a>Uppsetning vátryggingabókakeyrslna
Hægt er að setja upp keyrslur í sniðmáti vátryggingabókar. Gildin í keyrslunni eru notuð sem sjálfgildi ef reitirnir í færslubókarlínunum hafa ekki verið fylltir út. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Sniðmát vátryggingabóka** og veldu síðan tengda tengilinn.  
2. Valin er sniðmát vátryggingabókar og veldu svo **keyrslur** aðgerðina.
3. Á síðunni **vátryggingarbókarkeyrslur** þarf að fylla reitina út eftir þörfum.

> [!NOTE]  
>   Tölur hafa sérstaka þýðingu í færslubókarheitum. Ef tala er í heiti færslubókarsniðmáts, hækkar hún sjálfkrafa um einn í hvert sinn sem færslubókin er bókuð. Ef til dæmis HH1 er fært inn í reitinn **Heiti**, mun færslubókarheitið breytast í HH2 eftir bókun.

## <a name="see-also"></a>Sjá einnig
[Uppsetning eigna](fa-setup.md)  
[Eignir](fa-manage.md)  
[Fjármál](finance.md)  
[Hafist handa](product-get-started.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
