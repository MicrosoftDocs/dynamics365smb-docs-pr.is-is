---
title: Greiðslutillögur til lánardr.
description: Notaðu runuvinnuna Stinga upp á greiðslur lánardrottna til að búa til greiðslulínur fyrir lánardrottna þína á grundvelli gjalddaga og greiðsluafsláttar.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256,'
ms.date: 12/04/2023
ms.custom: bap-template
---
# Greiðslutillögur til lánardr.

Á síðunni **Greiðslubók** geturðu notað **Greiðslutillögur til lánardr.** runuvinnsluna til að stinga upp á greiðslulínur. Byggt á stillingum þínum, [!INCLUDE [prod_short](includes/prod_short.md)] leggur til línur fyrir:

- Greiðslur sem eru á gjalddaga fljótlega.
- Greiðslur þar sem greiðsluafsláttur er í boði.

Til að njóta góðs af greiðslutillögum verður þú að forgangsraða söluaðilum þínum. Til að læra meira um að forgangsraða söluaðilum skaltu fara í [Forgangsraða söluaðilum](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Runuvinnan útilokar færslur lánardrottinsbókhalds sem eru **í bið** eða sem eru þegar notaðar og hafa gildi í **Á við auðkenni** reitur.  

> [!IMPORTANT]  
> Ef nýta á greiðsluafslátt og tiltæk upphæð hefur verið færð inn, verður upphæðin notuð fyrir:  
>
> * Forgangsraðar gjaldfallnar lánardrottnafærslur fyrst, í forgangsröð.
> * Tímasettar færslur lánardrottins sem eru ekki settar í forgang.  
> * Opna lánardrottnafærslur sem uppfylla skilyrði fyrir greiðsluafslætti. Færslunum er raðað eftir númeri lánardrottins.  

## Notaðu aðgerðina Stinga upp á greiðslum lánardrottna

1. Veldu ![peruna sem opnar Segðu mér eiginleikann.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, sláðu inn **Greiðsludagbækur** og veldu síðan tengda hlekkinn.  
2. Opnaðu færslubókina og veldu síðan aðgerðina **Stinga upp á greiðslum lánardrottins** .  
3. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Veldu  **OK** hnappinn.  

## Settu gjalddaga inn sem bókunardagsetningu á greiðslubókarlínum

Þegar þú notar lotuvinnuna **Stinga upp á greiðslum lánardrottna**  til að búa til greiðslulínur fyrir lánardrottna þína, geturðu fyllt út tvo sérstaka reiti til að tryggja að útbúnar línur noti gjalddaga til að reikna út færsludagur. Þessir reitir eru **Reikna Bókunardagsetning úr Gjalddaga jöfnunar** og **frávik gjalddaga jöfnunar**.  

> [!IMPORTANT]  
> Þú getur ekki notað reitinn **Reiknið út bókunardagsetningu frá gjalddaga gilda fyrir skjöl** ásamt  **Finndu greiðsluafslátt** reiturinn eða **Samantekt á söluaðila** reitinn. Ef bókunardagsetningin er byggð á gjalddaga gætu sumir greiðsluafsláttir ekki reiknast rétt vegna þess að bókunardagsetningin er eftir greiðsluafsláttinn.  

Einnig, ef útreiknuð bókunardagsetning er í fortíðinni, þá er bókunardagsetningin færð upp á vinnudagsetningu og viðvörun birtist.  

Þú getur líka búið til greiðslulínur handvirkt með því að nota gjalddaga til að reikna út bókunardagsetningu. Þegar lánardrottnafærslur hafa verið jafnaðar er hægt að nota **Reikna út bókunardagsetningu** til að uppfæra bókunardagsetningu á færslubókarlínunni með gjalddaga tengds innkaupareiknings. Til að læra meira um þetta handvirka ferli, farðu í [Beita innkaupafærslum handvirkt](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
> Ef innkaupareikningur er tímabær er bókunardagsetningin stillt á vinnudagsetningu og leturgerð á línunni breytist í rautt.  

## Sjá einnig .

- [Stjórna skuldum](payables-manage-payables.md)  
- [Framkvæma greiðslur](payables-make-payments.md)  
- [Vinna í færslubókum](ui-work-general-journals.md)  
- [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
