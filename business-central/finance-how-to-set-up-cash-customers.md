---
title: Hvernig á að setja upp staðgreiðsluviðskiptamenn | Microsoft Docs
description: Þetta efnisatriði lýsir skrefum í uppsetningu viðskiptamanns sem staðgreiðir.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: d122eaf5e7f898f2497b3cc0848309fb36fa62c1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238830"
---
# <a name="set-up-cash-customers"></a>Uppsetning staðgreiðsluviðskiptamanna
Ekki er hægt að gera reikning án viðskiptamannsnúmers. Þetta á við þó svo að selt sé gegn staðgreiðslu og ekki sé þörf á að skrá upplýsingar í viðskiptamannareikning.  

## <a name="to-set-up-a-cash-customer"></a>Uppsetning staðgreiðsluviðskiptamanna  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **viðskiptamaður** og veldu síðan tengda tengilinn.  
2.  Stofna nýtt spjald **Viðskiptamaður**. Frekari upplýsingar eru í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md).
3.  Í reitnum **númer** er ritað **Reiðufé**, til dæmis.  
4.  Í reitinn **Heiti** er til dæmis ritað **Staðgreitt við sölu**.  
5.  Á flýtiflipanum **Reikningsfærsla** þarf að fylla út reitina **Bókunarflokkur viðskiptam.** og **Alm. viðsk.bókunarflokkur**.  

 Nú hefur verið stofnaður viðskiptamaður með nægar upplýsingar til reikningsfærslu.  

> [!NOTE]  
>  Hugsanlega hefur verið valinn bókunarflokkur sem er einnig notaður við kreditsölu innanlands. Eigi að geyma gögn um sölu gegn staðgreiðslu sérstaklega, til dæmis með sérstökum sölu- eða safnreikningi, er hægt að setja upp sérstakan bókunarflokk í því skyni.  
>   
>  Rita þarf safnreikningsnúmer fyrir bókunarflokkinn þó svo að staðan á reikningnum verði alltaf 0 eftir bókun reiknings.  

## <a name="see-also"></a>Sjá einnig
[Stjórnun skulda](receivables-manage-receivables.md)  
[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)    
[Fjármál](finance.md)  

