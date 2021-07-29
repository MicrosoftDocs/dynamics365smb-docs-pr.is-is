---
title: Uppsetning vátrygginga eigna| Microsoft Docs
description: Sett er upp vátryggingarspjald og almennar vátryggingaupplýsingar til að stjórna vátryggingasviði eigna.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0e9eab4b00e0729f13adb4cd38b7b4992a160539
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6440650"
---
# <a name="set-up-fixed-asset-insurance"></a>Uppsetning vátryggingar eignar.
Til að stjórna vátryggingasviði eigna, þarf fyrst að setja upp nokkrar almennar vátryggingaupplýsingar og vátryggingarspjald á hvert tryggingaskírteini.

## <a name="to-set-up-general-insurance-information"></a>Uppsetning almennra vátryggingaupplýsinga
Til að nota tryggingaraðgerðirnar í [!INCLUDE[prod_short](includes/prod_short.md)] verður þú að setja upp almennar tryggingarupplýsingar.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning eigna** og velja síðan viðkomandi tengil.  
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Uppsetning vátryggingategunda
Hægt er að flokka vátryggingar, til dæmis í tryggingar vegna þjófnaðar eða brunatryggingu. Vátryggingategundirnar eru notaðar á vátryggingaspjaldinu.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Tryggingargerðir** og velja síðan viðkomandi tengil.  
2. Fyllið inn í svæðin eftir þörfum.

## <a name="to-set-up-insurance-cards"></a>Uppsetning vátryggingaspjalda
Hægt er að safna saman upplýsingum um hverja vátryggingu á vátryggingaspjaldinu.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Trygging** og velja síðan viðkomandi tengil.  
2. Á síðunni **Vátrygging** skal velja aðgerðina **Nýtt** til að stofna nýtt vátryggingarspjald.  
3. Fyllið inn reitina eftir þörfum.

## <a name="to-set-up-insurance-journal-templates"></a>Uppsetning vátryggingabókasniðmáta
[!INCLUDE[prod_short](includes/prod_short.md)] skapar sjálfkrafa vátryggingarsniðmát í fyrsta skipti sem þú opnar síðuna **Vátryggingabók**, en þú getur sett upp viðbótarsniðmát færslubókar. Frekari upplýsingar, sjá [Vinna með almennar færslubækur](ui-work-general-journals.md).  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sniðmát vátryggingabóka** og velja síðan viðkomandi tengil.  
2. Fyllið inn í svæðin eftir þörfum.

## <a name="to-set-up-insurance-journal-batches"></a>Uppsetning vátryggingabókakeyrslna
Hægt er að setja upp keyrslur í sniðmáti vátryggingabókar. Gildin í keyrslunni eru notuð sem sjálfgildi ef reitirnir í færslubókarlínunum hafa ekki verið fylltir út. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sniðmát vátryggingabóka** og velja síðan viðkomandi tengil.  
2. Valin er sniðmát vátryggingabókar og veldu svo **keyrslur** aðgerðina.
3. Á síðunni **vátryggingarbókarkeyrslur** þarf að fylla reitina út eftir þörfum.

> [!NOTE]  
>   Tölur hafa sérstaka þýðingu í færslubókarheitum. Ef tala er í heiti færslubókarsniðmáts, hækkar hún sjálfkrafa um einn í hvert sinn sem færslubókin er bókuð. Ef til dæmis HH1 er fært inn í reitinn **Heiti**, mun færslubókarheitið breytast í HH2 eftir bókun.

## <a name="see-also"></a>Sjá einnig
[Uppsetning eigna](fa-setup.md)  
[Eignir](fa-manage.md)  
[Fjármál](finance.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]