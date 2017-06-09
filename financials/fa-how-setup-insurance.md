---
title: "Hvernig á að setja upp vátryggingar eigna | Microsoft Docs"
description: "Lýsir hvernig á að setja upp kerfið fyrir tryggingu eigna."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6473b74823f787e6b1eac599bb95b6d100a02c1e
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-fixed-asset-insurance"></a>Hvernig á að setja upp vátryggingar eigna
Til að stjórna vátryggingasviði eigna, þarf fyrst að setja upp nokkrar almennar vátryggingaupplýsingar og vátryggingarspjald á hvert tryggingaskírteini.

## <a name="to-set-up-general-insurance-information"></a>Uppsetning almennra vátryggingaupplýsinga
Til að nota tryggingaraðgerðirnar í [!INCLUDE[d365fin](includes/d365fin_md.md)] verður þú að setja upp almennar tryggingarupplýsingar.  

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Uppsetning eigna**, og velja síðan viðeigandi tengil.  
2. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Uppsetning vátryggingategunda
Hægt er að flokka vátryggingar, til dæmis í tryggingar vegna þjófnaðar eða brunatryggingu. Vátryggingategundirnar eru notaðar á vátryggingaspjaldinu.

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Vátryggingargerðir**, og velja síðan viðeigandi tengil.  
2. Fyllið inn í svæðin eftir þörfum.

## <a name="to-set-up-insurance-cards"></a>Uppsetning vátryggingaspjalda
Hægt er að safna saman upplýsingum um hverja vátryggingu á vátryggingaspjaldinu.  

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Vátrygging**, og velja síðan viðeigandi tengil.  
2. Í glugganum **Vátrygging** skal velja aðgerðina **Nýtt** til að stofna nýtt vátryggingarspjald.  
3. Fyllið inn í svæðin eftir þörfum.

## <a name="to-set-up-insurance-journal-templates"></a>Uppsetning vátryggingabókasniðmáta
[!INCLUDE[d365fin](includes/d365fin_md.md)] skapar sjálfkrafa vátryggingarsniðmát í fyrsta skipti sem þú opnar gluggann **Vátryggingabók**, en þú getur sett upp viðbótarsniðmát færslubókar. Frekari upplýsingar eru í [Unnið með almennar færslubækur](ui-work-general-journals.md).  

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Sniðmát vátryggingabóka**, og velja síðan viðeigandi tengil.  
2. Fyllið inn í svæðin eftir þörfum.

## <a name="to-set-up-insurance-journal-batches"></a>Uppsetning vátryggingabókakeyrslna
Hægt er að setja upp keyrslur í sniðmáti vátryggingabókar. Gildin í keyrslunni eru notuð sem sjálfgildi ef reitirnir í færslubókarlínunum hafa ekki verið fylltir út. Frekari upplýsingar eru í [vinna með almenn færslubók](ui-work-general-journals.md).  

1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Sniðmát vátryggingabóka**, og velja síðan viðeigandi tengil.  
2. Valin er sniðmát vátryggingabókar og veldu svo **keyrslur** aðgerðina.
3. Í glugganum **vátryggingarbókarkeyrslur** þarf að fylla reitina út eftir þörfum.

**Athugasemd**: Tölur hafa sérstaka þýðingu í færslubókarheitum. Ef tala er í heiti færslubókarsniðmáts, hækkar hún sjálfkrafa um einn í hvert sinn sem færslubókin er bókuð. Ef til dæmis HH1 er fært inn í reitinn **Heiti**, mun færslubókarheitið breytast í HH2 eftir bókun.

## <a name="see-also"></a>Sjá einnig
[Uppsetning eigna](fa-setup.md)  
[Eignir](fa-manage.md)  
[Fjármál](finance.md)  
[Velkomin í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]] (index.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

