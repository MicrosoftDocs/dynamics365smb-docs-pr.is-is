---
title: Leggja til keyrslu á greiðslum lánardrottins
description: Hægt er að tilgreina stillingar fyrir greiðslur til lánardrottna og fá þannig greiðslutillögur sem taka mið af gjalddögum og afsláttum.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.search.form: 256
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 962a1fde49db09b3d739ac33eba43fa7316cc25d
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953159"
---
# <a name="suggest-vendor-payments"></a>Greiðslutillögur til lánardr.

Á síðunni **Greiðslubók** geturðu notað **Greiðslutillögur til lánardr.** runuvinnsluna til að stinga upp á greiðslulínur. Línur fyrir greiðslur sem falla brátt á gjalddaga, eða greiðslur þar sem greiðsluafsláttur er í boði, eru ráðlagðar á grunni stillinganna þinna.

Til að njóta greiðsluábendinga til fulls verður þú fyrst að forgangsraða lánardrottnum þínum. Frekari upplýsingar eru í [Lánardrottnum forgangsraðað](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Lánardrottnafærslur sem eru **Í bið** eru ekki teknar með í runukeyrslunni.  

> [!IMPORTANT]  
>   Ef nýta á greiðsluafslátt og tiltæk upphæð hefur verið færð inn, verður upphæðin notuð fyrir:  
    * Forgangsatriði fyrirframgreiddar seljenda færslur fyrst í forgangsröð.   
    * Lánardrottnafærslur sem eru fallnar á tíma sem eru ekki forgangsraðar.  
    * Opnaðu söluaðili færslur sem eiga rétt á greiðslukortum, raðað eftir seljanda númeri.  

## <a name="to-use-the-suggest-vendor-payments-function"></a>nota aðgerðina Greiðslutillögur til lánardrottna
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðslubækur** og velja síðan viðkomandi tengil.  
2. Opna skal viðeigandi færslubók, og síðan velja **Greiðslutillögur til lánardrottna** aðgerðina.  
3. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Velja hnappinn **Í lagi**.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Setja inn skiladag sem bókunardagsetningu á greiðslubókarlínum
Þegar þú notar runuvinnsluna **Greiðslutillögur til lánardrottna** til að stofna greiðslulínur fyrir lánardrottna þína getur þú fyllt út tvo sérstaka reiti til að gæta þess að stofnuðu línurnar noti gjalddaga til að reikna út bókunardagsetningu. Þessir reitir eru **Reikna Bókunardagsetning úr Gjalddaga jöfnunar** og **frávik gjalddaga jöfnunar**.  

> [!IMPORTANT]  
>   Ekki er hægt að nota reitinn **Reikna út bókunardagsetningu úr gildisdegi** samhliða reitunum **Finna greiðsluafslátt** eða **Samantekt fyrir lánardrottinn**. Ef staðsetningardagsetningin er byggð á gjalddaga, geta sumir afsláttarmöguleikar ekki reiknað rétt vegna þess að póstsetningardagur er eftir gjalddaga.  

Ef útreiknuð bókunardagsetning er liðin er bókunardagsetningin færð upp að vinnudagsetningunni og viðvörun birtist.  

Einnig er hægt að myndað sjálfkrafa greiðslulínur með gjalddaga til að reikna bókunardagsetningu Þegar lánardrottnafærslur hafa verið jafnaðar er hægt að nota **Reikna út bókunardagsetningu** til að uppfæra bókunardagsetningu á færslubókarlínunni með gjalddaga tengds innkaupareiknings. Frekari upplýsingar eru í [Jafna innkaupafærslur handvirkt](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
>   Ef innkaupareikningur er gjaldfallinn, er bókunardagsetningin stillt á vinnudag og leturgerð á línunni verður rautt.  

## <a name="see-also"></a>Sjá einnig
[Stjórna skuldum](payables-manage-payables.md)  
[Framkvæma greiðslur](payables-make-payments.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]