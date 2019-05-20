---
title: Nota runuvinnsluna Greiðslutillögur til lánardrottna| Microsoft Docs
description: Hægt er að tilgreina stillingar fyrir greiðslur til lánardrottna og fá þannig greiðslutillögur sem taka mið af gjalddögum og afsláttum.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 9936a77c7afdc89d6d8c8485d01b4970e85fcb19
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2019
ms.locfileid: "1254000"
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
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **greiðslubók** og veldu síðan tengda tengilinn.  
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
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
