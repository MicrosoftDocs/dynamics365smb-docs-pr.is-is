---
title: Hvernig á að setja upp staðgreiðsluviðskiptamenn | Microsoft Docs
description: Þetta efnisatriði lýsir skrefum í uppsetningu viðskiptamanns sem staðgreiðir.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f047876678d26e7e53bf304433f38a410ba7d7fa
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5770392"
---
# <a name="set-up-cash-customers"></a>Uppsetning staðgreiðsluviðskiptamanna
Ekki er hægt að gera reikning án viðskiptamannsnúmers. Þetta á við þó svo að selt sé gegn staðgreiðslu og ekki sé þörf á að skrá upplýsingar í viðskiptamannareikning.  

## <a name="to-set-up-a-cash-customer"></a>Uppsetning staðgreiðsluviðskiptamanna  
1.  Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Viðskiptamaður** og veldu síðan tengda tengilinn.  
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



[!INCLUDE[footer-include](includes/footer-banner.md)]