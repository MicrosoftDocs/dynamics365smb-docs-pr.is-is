---
title: Uppsetning staðgreiðsluviðskiptamanna
description: Í þessu efnisatriði er lýst þeim skrefum sem þarf til að setja upp reikning með númeri viðskiptavinar fyrir viðskiptavini sem greiða með reiðufé.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 21, 22
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 7b021b957d2984d2b2ea239c1e8f737d90071215
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/14/2022
ms.locfileid: "7973441"
---
# <a name="set-up-cash-customers"></a>Uppsetning staðgreiðsluviðskiptamanna

Ekki er hægt að gera reikning án viðskiptamannsnúmers. Þetta á við þó svo að selt sé gegn staðgreiðslu og ekki sé þörf á að skrá upplýsingar í viðskiptamannareikning.  

## <a name="to-set-up-a-cash-customer"></a>Uppsetning staðgreiðsluviðskiptamanna

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Viðskiptavinur** og velja síðan viðkomandi tengil.  
2. Stofna nýtt spjald **Viðskiptamaður**. Frekari upplýsingar eru í [Skrá nýja viðskiptamenn](sales-how-register-new-customers.md).
3. Í reitnum **númer** er ritað **Reiðufé**, til dæmis.  
4. Í reitinn **Heiti** er til dæmis ritað **Staðgreitt við sölu**.  
5. Á flýtiflipanum **Reikningsfærsla** þarf að fylla út reitina **Bókunarflokkur viðskiptam.** og **Alm. viðsk.bókunarflokkur**.  

 Nú hefur verið stofnaður viðskiptamaður með nægar upplýsingar til reikningsfærslu.  

> [!NOTE]  
> Hugsanlega hefur verið valinn bókunarflokkur sem er einnig notaður við kreditsölu innanlands. Eigi að geyma gögn um sölu gegn staðgreiðslu sérstaklega, til dæmis með sérstökum sölu- eða safnreikningi, er hægt að setja upp sérstakan bókunarflokk í því skyni.  
>
> Rita þarf safnreikningsnúmer fyrir bókunarflokkinn þó svo að staðan á reikningnum verði alltaf 0 eftir bókun reiknings.  

## <a name="see-also"></a>Sjá einnig

[Stjórnun skulda](receivables-manage-receivables.md)  
[Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)
[Fjármál](finance.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]