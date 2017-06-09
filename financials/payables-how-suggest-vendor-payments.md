---
title: "Hvernig á að: Leggja til greiðslur til lánardrottna | Microsoft Docs"
description: "Hvernig á að leggja til greiðslutillögur til lánardrottna"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 4b85fc783cdebb7c1d2e048315e48aee02a189fa
ms.contentlocale: is-is
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-suggest-vendor-payments"></a>Hvernig á að leggja til greiðslutillögur til lánardrottna
Í glugganum **Greiðslubók** geturðu notað **Greiðslutillögur til lánardr.** runuvinnsluna til að stinga upp á greiðslulínur. Línur fyrir hluti eins og greiðslur sem eiga sér stað fljótlega, eða greiðslur þar sem greiðsla afsláttur er í boði, er leiðbeinandi miðað við stillingarnar þínar.

Til að njóta fulls af leiðbeinandi línur, verður þú fyrst að forgangsraða söluaðilum þínum. Nánari upplýsingar sjá [Hvernig: forgangsraða lánardrottnum](purchasing-how-prioritize-vendors.md).  

Lánardrottnafærslur sem eru ekki merktar **Í biðstöðu** eru ekki teknar með.  

**Mikilvægt:** Ef þú vilt nýta greiðslukort og hafa slegið inn tiltækan upphæð, þá verður upphæðin notuð fyrir:  

* Forgangsatriði fyrirframgreiddar seljenda færslur fyrst í forgangsröð.  
* Lánardrottnafærslur sem eru fallnar á tíma sem eru ekki forgangsraðar.  
* Opnaðu söluaðili færslur sem eiga rétt á greiðslukortum, raðað eftir seljanda númeri.  

## <a name="to-use-the-suggest-vendor-payments-function"></a>nota aðgerðina Greiðslutillögur til lánardrottna
1. Efst í hægra horni skal velja **Leita að síðu eða skýrslu** táknið ![Leita að síðu eða skýrslu](media/ui-search/search_small.png "Leita að síðu eða skýrslu táknið"), færa **Greiðslubækur**, og velja síðan viðeigandi tengil.  
2. Opna skal viðeigandi færslubók, og síðan velja **Greiðslutillögur til lánardrottna** aðgerðina.  
3. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Velja hnappinn **Í lagi**.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Setja inn skiladag sem bókunardagsetningu á greiðslubókarlínum
Þegar þú notar runuvinnsluna **Greiðslutillögur til lánardrottna** til að stofna greiðslulínur fyrir lánardrottna þína getur þú fyllt út tvo sérstaka reiti til að gæta þess að stofnuðu línurnar noti gjalddaga til að reikna út bókunardagsetningu. Þessir reitir eru **Reikna Bókunardagsetning úr Gjalddaga jöfnunar** og **frávik gjalddaga jöfnunar**.  

**Mikilvægt:** Ekki er hægt að nota **Reikna út bókunardagsetningu úr Jöfnun** reitinn ásamt **Finna greiðsluafslátt** reitinn eða **Leggja saman á lánardr.**. Ef staðsetningardagsetningin er byggð á gjalddaga, geta sumir afsláttarmöguleikar ekki reiknað rétt vegna þess að póstsetningardagur er eftir gjalddaga.  

Ef útreiknuð bókunardagsetning er liðin er bókunardagsetningin færð upp að vinnudagsetningunni og viðvörun birtist.  

Einnig er hægt að myndað sjálfkrafa greiðslulínur með gjalddaga til að reikna bókunardagsetningu Þegar lánardrottnafærslur hafa verið jafnaðar er hægt að nota **Reikna út bókunardagsetningu** til að uppfæra bókunardagsetningu á færslubókarlínunni með gjalddaga tengds innkaupareiknings. Nánari upplýsingar sjá [Hvernig: Jafna innkaupafærslur Handvirkt](payables-how-apply-purchase-transactions-manually.md).  

**Athugaðu:** Ef innheimtuskírteini er tímabært er póstsetningardagur stillt á vinnudag og leturgerð á línunni verður rautt.  

## <a name="see-also"></a>Sjá einnig
[Stjórna skuldum](payables-manage-payables.md)  
[Framkvæma greiðslur](payables-make-payments.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

