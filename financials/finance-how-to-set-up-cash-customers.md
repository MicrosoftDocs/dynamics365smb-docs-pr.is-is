---
title: "Hvernig á að setja upp staðgreiðsluviðskiptamenn | Microsoft Docs"
description: "Þetta efnisatriði lýsir skrefum í uppsetningu viðskiptamanns sem staðgreiðir."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/11/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6826c574bf63de70d76a29b45968c68c0b2e2d1f
ms.contentlocale: is-is
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-cash-customers"></a>Hvernig á að setja upp staðgreiðsluviðskiptamenn
Ekki er hægt að gera reikning án viðskiptamannsnúmers. Þetta á við þó svo að selt sé gegn staðgreiðslu og ekki sé þörf á að skrá upplýsingar í viðskiptamannareikning.  

## <a name="to-set-up-a-cash-customer"></a>Uppsetning staðgreiðsluviðskiptamanna  
1.  Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **viðskiptamaður** og velja svo viðeigandi tengil.  
2.  Stofna nýtt spjald **Viðskiptamaður**. Nánari upplýsingar eru í [Hvernig á að skrá nýjan viðskiptamaður](sales-how-register-new-customers.md).
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
[Hvernig á að Skrá nýja viðskiptamenn](sales-how-register-new-customers.md)    
[Fjármál](finance.md)  


