---
title: Leggja til runuvinnsluna Greiðslutillögur til lánardrottna
description: Hægt er að tilgreina greiðslustillingar lánardrottins til að fá tillögur um greiðslur.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256,'
ms.date: 09/07/2023
ms.custom: bap-template
---
# <a name="suggest-vendor-payments"></a>Greiðslutillögur til lánardr.

Á síðunni **Greiðslubók** geturðu notað **Greiðslutillögur til lánardr.** runuvinnsluna til að stinga upp á greiðslulínur. Byggt á stillingum,  [!INCLUDE [prod_short](includes/prod_short.md)]  leggur til línur fyrir greiðslur:

* Greiðslur sem koma brátt til vegna
* Greiðslur þar sem staðgreiðsluafsláttur er í boði

Til að njóta greiðsluábendinga til fulls verður þú fyrst að forgangsraða lánardrottnum þínum. Til að fræðast meira um forgangsröðun lánardrottna er farið í  [forgangsröðun lánardrottna](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Keyrslan útilokar þær lánardrottnafærslur sem  **á að halda**  eða þegar eru notaðar og hafa gildi í  **reitnum Kenni**  jöfnunar.  

> [!IMPORTANT]  
> Ef nýta á greiðsluafslátt og tiltæk upphæð hefur verið færð inn, verður upphæðin notuð fyrir:  
>
> * Forgangsraða gjaldföllnum lánardrottnafærslum fyrst, í forgangsröð.
> * Lánardrottnafærslur sem eru fallnar á tíma sem eru ekki forgangsraðar.  
> * Opna lánardrottnafærslur sem standast greiðsluafslátt. Færslunum er raðað eftir númeri lánardrottins.  

## <a name="to-use-the-suggest-vendor-payments-function"></a>nota aðgerðina Greiðslutillögur til lánardrottna

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðslubækur** og velja síðan viðkomandi tengil.  
2. Opnið færslubókina og veljið síðan aðgerðir fyrir  **Greiðslutillögur**  lánardrottins.  
3. Fyllið inn í svæðin eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Velja hnappinn **Í lagi**.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Setja inn skiladag sem bókunardagsetningu á greiðslubókarlínum

Þegar þú notar runuvinnsluna **Greiðslutillögur til lánardrottna** til að stofna greiðslulínur fyrir lánardrottna þína getur þú fyllt út tvo sérstaka reiti til að gæta þess að stofnuðu línurnar noti gjalddaga til að reikna út bókunardagsetningu. Þessir reitir eru **Reikna Bókunardagsetning úr Gjalddaga jöfnunar** og **frávik gjalddaga jöfnunar**.  

> [!IMPORTANT]  
> Ekki er hægt að  **nota bókunardagsetninguna reikna frá jöfnunar-á-lokadagsetningu**  **í reitnum finna staðgreiðsluafslátt**  eða  **reitinn draga saman hvern lánardrottinn** . Ef bókunardagsetningin er byggð á gjalddagann, gæti einhver staðgreiðsluafsláttur ekki reiknast rétt þar sem bókunardagsetningin er á eftir staðgreiðsluafsláttardagsetningunni.  

Einnig, ef reiknuð bókunardagsetning er í fortíðinni, þá er bókunardagsetning færð upp í vinnudagsetninguna og viðvörunarmerki birt.  

Einnig er hægt að stofna greiðslulínur handvirkt með því að nota gjalddagann til að reikna út bókunardagsetninguna. Þegar lánardrottnafærslur hafa verið jafnaðar er hægt að nota **Reikna út bókunardagsetningu** til að uppfæra bókunardagsetningu á færslubókarlínunni með gjalddaga tengds innkaupareiknings. Til að fá frekari upplýsingar um þetta handvirka ferli er farið í að  [Sækja um innkaupafærslur handvirkt](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
> Ef innkaupareikningur er í vanskilum er bókunardagsetningin stillt á vinnudagsetninguna og Leturgerðin í línunni verður rauð.  

## <a name="see-also"></a>Sjá einnig .

[Stjórna skuldum](payables-manage-payables.md)  
[Framkvæma greiðslur](payables-make-payments.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
