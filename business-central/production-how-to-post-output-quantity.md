---
title: Fjöldabóka framleiðslufrálag og keyrslutíma
description: Frálagsmagnið sýnir framvindu vinnunnar sem lokið magn og notuð afköst vinnu eða vélastöðvar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 923f68b13619013dd54062438c66192a682868bc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787878"
---
# <a name="batch-post-output-and-run-times"></a>Fjöldabóka frálag og keyrslutíma
Frálagsmagnið sýnir framvindu vinnunnar sem lokið magn og notuð afköst vinnu eða vélastöðvar.

Hægt er að nota frálagsbókina til að:
*  Leiðréttir birgðir í tengslum við frálag tilbúinnar vörur frá framleiðslu.
*  Skrá magn og rýrnun hverrar aðgerðar í framleiðsluleið.
*  Skrá uppsetningu og keyrslutíma fyrir vinnu og vélastöðvar.

> [!NOTE]
> Ef framleiðsluleiðir eru notaðar eru birgðir aðeins uppfærðar þegar frálagsmagn er bókað í síðustu aðgerðinni.

Með glugganum **Framleiðslubók** er hægt að vinna sömu verk og í glugganum **Frálagsbók** og um leið framkvæma tengdar notkunarbókanir. Frekari upplýsingar eru í [Skrá notkun og frálag fyrir eina útgefna framleiðslupöntunarlínu](production-how-to-register-consumption-and-output.md).

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a>Að bóka frálagsmagn og/eða skrá keyrslutíma fyrir eina eða fleiri framleiðslupantanalínur
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Frálagsbók** og veldu síðan tengda tengilinn.  
2. Reitirnir eru fylltir út með framleiðslupöntunargögnunum og frálagsgögnunum og/eða keyrslutímanum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    Hægt er að nota aðgerðina **Opna leið** til að mynda færslubókarlínur úr framleiðslupöntunum.
  
4. Ef aðgerðinni er lokið skal velja reitinn **Lokið**.  
5. Veldu aðgerðina **Bóka** til að bóka aðgerðina. 
 
Fjárhagsfærslur afkasta eru uppfærðar fyrir notaða vinnu eða vélastöðvar með upplýsingum um tíma og magn frálags og rýrnunar. Ef síðasta aðgerðin var bókuð verður vörunni bætt við birgðir. 

## <a name="see-also"></a>Sjá einnig  
[Bóka rýrnun handvirk](production-how-to-post-scrap.md)
[Bakfæra frálagsbókun](production-how-to-reverse-output-posting.md)
[Framleiðsla](production-manage-manufacturing.md)    
[Uppsetning framleiðslu](production-configure-production-processes.md)  
[Áætlun](production-planning.md)      
[Birgðir](inventory-manage-inventory.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
