---
title: Skrá greiðslur og endurgreiðslur í greiðslubók
description: Lestu um hvernig á að skrá greiðslur sem þú greiðir lánardrottnum og endurgreiðslur sem þú greiðir viðskiptavinum á greiðslubókarsíðunni.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment journal, print check, vendor payment, customer refund, refund check, creditor, debt, balance due, AP'
ms.search.form: '256, 233, 624, 1228'
ms.date: 07/09/2021
ms.author: bholtorf
---
# Skrá greiðslur og endurgreiðslur í greiðslubókina

Á síðunni **Greiðslubók** skráir þú greiðslur sem þú greiðir lánardrottnum og endurgreiðslur sem þú greiðir viðskiptavinum. Þegar þú bókar greiðslubókarlínu er greidda upphæðin skráð í tilgreindan bankareikning kerfisins. Þú verður þá að gera ráðstafanir til að framkvæma raunverulegu peningamillifærslu af tengdum bankareikningi.  

Greiðslubókin er færslubók sem er fínstillt til að framkvæma greiðlsur. Þú getur bætt við línum með skjótum hætti handvirkt, þú getur látið [!INCLUDE[prod_short](includes/prod_short.md)] stinga upp á lánardrottnagreiðslur, og þú getur jafnað greiðsluna á bókuð skjöl. Jafnvel þótt þú greiðir greiðslur, þá færirðu inn jákvæð upphæð í **Skjalaupphæð** reitinn. Það fer eftir gerð skjala fyrir færslubókarlínuna, þá er þetta upphæð breytt í neikvæð upphæð í undirliggjandi færslum. Þannig ertu fljótari að bæta við færslubókarlínum handvirkt. Ef þú vilt heldur færa inn neikvæðum upphæðum, getur þú sérsniðið greiðslubókina til að sýna **Upphæð** reitinn í staðinn.  

- Jafna greiðslur á reikninga eða kreditreikninga

    Ef þú fyllir út reitinn **Jöfnunarskjalsnúmer** með reikningnum eða kreditreikningnum sem þarf að greiða eða endurgreiða, þá er skjalið sem um ræðir sett til greiðslu þegar þú bókar færslubókina. Þetta kallast að vera „jafnað“. Í stað þess að framkvæma jöfnun við bókun á greiðslu geturðu notað síðuna **Jafna lánardr.færslur** og **Jafna viðskm.færslur** eftir að þú hefur framkvæmt bókun á greiðslu. Nánari upplýsingar má til dæmis finna í [Afstemma greiðslur lánardrottins við greiðslubók eða úr færslum í lánardrottnabók](payables-how-apply-purchase-transactions-manually.md).  

- Fáðu tillögur um greiðslur til lánardrottna eða starfsmanna

    The **Greiðslutillögur til lánardrottna** og **Greiðslutillögur til starfsmanna** aðgerðir geta hjálpað þér að fylla greiðslubókarlínur sjálfkrafa í samræmi við forgangsröðun lánardrottna og gjalddaga. Frekari upplýsingar er að finna í [Greiðslutillögur til lánardrottna](payables-how-suggest-vendor-payments.md). Með þessari aðgerð er reiturinn **Jöfnunarskjalsnúmer** alltaf fylltur út.  

- Prenta ávísanir og senda greiðslur rafrænt til bankans

    Til viðbótar við að skrá þig að greiðslan er hafi verið gerð, geturðu einnig notað síðuna **Greiðslubók** til að gera greiðsluna móttækilega fyrir frekari vinnslu hjá bankanum þínum. Frekari upplýsingar eru að finna í [Greiða greiðslu með ávísun](payables-how-work-checks.md) og [Greiða rafrænar greiðslur](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## Til að greiða í greiðslubók

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðslubækur** og velja síðan viðkomandi tengil.
2. Opnaðu bókarkeyrsluna sem er notuð fyrir greiðslur.
3. Ef þú veist hverjum á að greiða skaltu fylla í reitina handvirkt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Til að einnig jafna greiðsluna við tengdan reikning eða kreditreikning skaltu velja **Jöfnunarskjalsnúmer**. reitinn á síðunni **Jafna lánardr.færslur**, velja viðeigandi reikning eða kreditreikning og síðan velja hnappinn **Í lagi**.

    Mörg reiti, svo sem **Skjalaupphæð** og **Gjalddagi** reitir, eru nú fylltir inn með upplýsingum úr völdu skjalinu.
5. Annar valkostur er að nota aðgerðina **Greiðslutillögur til lánardrottna**. Allar jöfnunarupplýsingar og upphæðir eru síðan einnig færðar inn í færslubókarlínur. Frekari upplýsingar er að finna í [Greiðslutillögur til lánardrottna](payables-how-suggest-vendor-payments.md).

    Skilaboð munu leiðbeina þér í að fylla út nauðsynlega reiti á réttan hátt.
6. Þegar öllum greiðslubókarlínum er lokið skal velja aðgerðina **Bóka**.


## Gefa út endurgreiðsluávísun

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiðslubækur** og veldu síðan tengda tengilinn.
2. Í reitnum **Skjalagerð** skal velja **Endurgreiða**.  
3. Í reitnum **Númer ytra skjals** skal nota þessa tilvísun fyrir endurgreiðsluávísunina (til dæmis númer skilapöntunar).  
4. Í reitnum **Tegund reiknings** er valið **Viðskiptamaður**.  
5. Í reitnum **Reikningsnúmer** skal velja reikningsnúmer viðskiptavinar sem stíla á endurgreiðsluávísunina á.  
6. Í reitinn **Upphæð** skal færa inn upphæð endurgreiðslunnar.  
7. Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.  
8. Í reitnum **Mótreikningur nr.** er sá bankareikningur valinn sem ávísunin kemur frá.  
9. Í **Jöfnunarskjalsnúmer** reitnum skal velja skjölin sem krefjast endurgreiðslu.  
10. Þegar öllum greiðslubókarlínum er lokið skal velja aðgerðina **Bóka/prenta** og síðan velja aðgerðina **Bóka og prenta** og velja **Já**.  
  

## Sjá einnig
[Framkvæma ávísanagreiðslur](payables-how-work-checks.md)  
[Framkvæma rafrænar greiðslur](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Stjórna skuldum](payables-manage-payables.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Flytja út jákvæða greiðsluskrá](finance-how-positive-pay.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Sérstilling verksvæðis](ui-personalization-user.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
