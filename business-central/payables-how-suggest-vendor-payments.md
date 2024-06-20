---
title: Greiðslutillögur til lánardr.
description: 'Keyrslan Greiðslutillögur til lánardr. er notuð til að stofna greiðslulínur fyrir lánardrottna, byggt á gjalddögum og greiðsluafslætti.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256,'
ms.date: 12/04/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Greiðslutillögur til lánardr.

Á síðunni **Greiðslubók** geturðu notað **Greiðslutillögur til lánardr.** runuvinnsluna til að stinga upp á greiðslulínur. Á grundvelli stillinganna eru [!INCLUDE [prod_short](includes/prod_short.md)]  tillögur um línur fyrir:

- Greiðslur sem eru í gjalddaga fljótlega.
- Greiðslur þar sem greiðsluafsláttur er tiltækur.

Til að njóta góðs af greiðslutillögum þarf að forgangsraða lánardrottnum. Frekari upplýsingar um forgangsröðun lánardrottna er farið í [Forgangsraða lánardrottnum](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Keyrslan undanskilur lánardrottnafærslur sem eru **í bið** eða sem þegar hafa verið jafnaðar og hafa gildi í reitnum **Kenni** jöfnunar.  

> [!IMPORTANT]  
> Ef nýta á greiðsluafslátt og tiltæk upphæð hefur verið færð inn, verður upphæðin notuð fyrir:  
>
> * Forgangsraðað gjaldfallnar lánardrottnafærslur fyrst í forgangsröð.
> * Gjaldfallnar lánardrottnafærslur sem ekki hefur verið forgangsraðað.  
> * Opna lánardrottnafærslur sem eru gjaldföllnar fyrir greiðsluafslátt. Færslunum er raðað eftir númeri lánardrottins.  

## Nota aðgerðina Greiðslutillögur til lánardr.

1.  ![Veldu Lightbulb sem opnar Tell Me eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknmynd, slá inn **greiðslubækur** og velja síðan viðeigandi tengil.  
2. Færslubókin er opnuð og aðgerðin **Greiðslutillögur til lánardr** . valinn.  
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Hnappurinn Í lagi **er** valinn.  

## Gjalddaginn er settur inn sem bókunardagsetning í greiðslubókarlínum

Þegar keyrslan Greiðslutillögur **til lánardr. er notuð** til að stofna greiðslulínur fyrir lánardrottna er hægt að fylla út tvo sérstaka reiti til að tryggja að myndaðar línur noti gjalddagann til að reikna bókunardagsetninguna. Þessir reitir eru **Reikna Bókunardagsetning úr Gjalddaga jöfnunar** og **frávik gjalddaga jöfnunar**.  

> [!IMPORTANT]  
> Ekki er hægt að nota reitinn **Reikna bókunardagsetningu úr Jöfnunargjalddagi** ásamt reitunum **Finna greiðsluafslætti** eða í reitnum **Leggja saman eftir lánardrottni** . Ef bókunardagsetningin er byggð á gjalddaga er hugsanlegt að einhver greiðsluafsláttur reikni ekki rétt þar sem bókunardagsetningin er eftir dagsetningu greiðsluafsláttarins.  

Ef reiknað bókunardagsetning er einnig liðin er bókunardagsetningin færð upp á vinnudagsetninguna og viðvörun birtist.  

Einnig er hægt að stofna greiðslulínur handvirkt með því að nota gjalddagann til að reikna bókunardagsetninguna. Þegar lánardrottnafærslur hafa verið jafnaðar er hægt að nota **Reikna út bókunardagsetningu** til að uppfæra bókunardagsetningu á færslubókarlínunni með gjalddaga tengds innkaupareiknings. Nánari upplýsingar um þetta handvirka ferli eru notaðar handvirkt [til að](payables-how-apply-purchase-transactions-manually.md) sækja innkaup.  

> [!NOTE]  
> Ef innkaupareikningurinn er gjaldfallinn er bókunardagsetningin stillt á vinnudagsetninguna og leturgerð línunnar breytist í rautt.  

## Sjá einnig .

- [Stjórna skuldum](payables-manage-payables.md)  
- [Framkvæma greiðslur](payables-make-payments.md)  
- [Vinna í færslubókum](ui-work-general-journals.md)  
- [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
