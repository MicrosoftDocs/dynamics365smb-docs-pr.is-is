---
title: Hvernig á að setja upp staðgreiðsluviðskiptamenn
description: Í þessu efnisatriði er lýst þeim skrefum sem þarf til að setja upp reikning með númeri viðskiptavinar fyrir viðskiptavini sem greiða með reiðufé.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 9462b7bb887b5c4d2dcc0f602d5cd0fe57ccc1fb
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/08/2021
ms.locfileid: "6442086"
---
# <a name="set-up-cash-customers"></a>Uppsetning staðgreiðsluviðskiptamanna
Ekki er hægt að gera reikning án viðskiptamannsnúmers. Þetta á við þó svo að selt sé gegn staðgreiðslu og ekki sé þörf á að skrá upplýsingar í viðskiptamannareikning.  

## <a name="to-set-up-a-cash-customer"></a>Uppsetning staðgreiðsluviðskiptamanna  
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinur** og velja síðan viðkomandi tengil.  
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