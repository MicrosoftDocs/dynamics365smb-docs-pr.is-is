---
title: Fjöldabóka framleiðslufrálag og keyrslutíma
description: Frálagsmagnið sýnir framvindu vinnunnar sem lokið magn og notuð afköst vinnu eða vélastöðvar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 99000773, 99000778, 99000823, 99000827
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7a1c30340efabed66e4ce359fc7680945e0db1de
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522747"
---
# <a name="batch-post-output-and-run-times"></a>Fjöldabóka frálag og keyrslutíma
Frálagsmagnið sýnir framvindu vinnunnar sem lokið magn og notuð afköst vinnu eða vélastöðvar.

Hægt er að nota frálagsbókina til að:

* Leiðréttir birgðir í tengslum við frálag tilbúinnar vörur frá framleiðslu.
* Skrá magn og rýrnun hverrar aðgerðar í framleiðsluleið.
* Skrá uppsetningu og keyrslutíma fyrir vinnu og vélastöðvar.

> [!NOTE]
> Ef framleiðsluleiðir eru notaðar eru birgðir aðeins uppfærðar þegar frálagsmagn er bókað í síðustu aðgerðinni.

Með glugganum **Framleiðslubók** er hægt að vinna sömu verk og í glugganum **Frálagsbók** og um leið framkvæma tengdar notkunarbókanir. Frekari upplýsingar eru í [Skrá notkun og frálag fyrir eina útgefna framleiðslupöntunarlínu](production-how-to-register-consumption-and-output.md).

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a>Að bóka frálagsmagn og/eða skrá keyrslutíma fyrir eina eða fleiri framleiðslupantanalínur

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Úttaksbók** og velja síðan viðkomandi tengil.  
2. Reitirnir eru fylltir út með framleiðslupöntunargögnunum og frálagsgögnunum og/eða keyrslutímanum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    Hægt er að nota aðgerðina **Opna leið** til að mynda færslubókarlínur úr framleiðslupöntunum.
  
3. Ef aðgerðinni er lokið skal velja reitinn **Lokið**.  
4. Veldu aðgerðina **Bóka** til að bóka aðgerðina. 

Fjárhagsfærslur afkasta eru uppfærðar fyrir notaða vinnu eða vélastöðvar með upplýsingum um tíma og magn frálags og rýrnunar.  

Ef síðasta aðgerðin var bókuð verður vörunni bætt við birgðir.  

## <a name="see-also"></a>Sjá einnig

[Bóka rýrnun handvirk](production-how-to-post-scrap.md)
[Bakfæra frálagsbókun](production-how-to-reverse-output-posting.md)
[Framleiðsla](production-manage-manufacturing.md)
[Setja upp framleiðslu](production-configure-production-processes.md)  
[Áætlun](production-planning.md)  
[Birgðir](inventory-manage-inventory.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
