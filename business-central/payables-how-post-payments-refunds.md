---
title: Skrá greiðslur og endurgreiðslur í greiðslubækur
description: Lestu um hvernig á að skrá greiðslur sem þú greiðir lánardrottnum og endurgreiðslur sem þú greiðir viðskiptavinum á greiðslubókarsíðunni.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment journal, print check, vendor payment, customer refund, refund check, creditor, debt, balance due, AP'
ms.search.form: '256, 233, 624, 1228'
ms.date: 07/17/2024
ms.service: dynamics-365-business-central
---
# Skrá greiðslur og endurgreiðslur í greiðslubókina

Á síðunni **Útgreiðslubækur** eru skráðar greiðslur sem gerðar eru lánardrottnum og endurgreiðslum sem notandi gerir viðskiptamönnum. Þegar útgreiðslubókarlína er bókuð er greidd upphæð skráð á tilgreindan bankareikning. Þú verður þá að gera ráðstafanir til að framkvæma raunverulegu peningamillifærslu af tengdum bankareikningi.  

Greiðslubækur eru almennar færslubækur sem eru bjartsýni til að framkvæma greiðslur. Þú getur bætt við línum með skjótum hætti handvirkt, þú getur látið [!INCLUDE[prod_short](includes/prod_short.md)] stinga upp á lánardrottnagreiðslur, og þú getur jafnað greiðsluna á bókuð skjöl. Þótt greiðslur séu framkvæmdar er jákvæð upphæð færð í reitinn **Upphæð** fylgiskjals. Það fer eftir gerð skjala fyrir færslubókarlínuna, þá er þetta upphæð breytt í neikvæð upphæð í undirliggjandi færslum. Þannig ertu fljótari að bæta við færslubókarlínum handvirkt. Ef þú vilt heldur færa inn neikvæðum upphæðum, getur þú sérsniðið greiðslubókina til að sýna **Upphæð** reitinn í staðinn. Nánari upplýsingar um sérstillingu síðna fást með því að fara í Sérstilling sérstillingar með því að [nota sérstillingarstillinguna](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).  

- Jafna greiðslur á reikninga eða kreditreikninga

    Ef fært er í reitinn Jöfnunarnúmer er reiturinn **Jöfnunarnúmer fylltur út.** með reikningnum eða kreditreikningnum til að greiða eða endurgreiða er fylgiskjalið stillt á **Greitt** þegar færslubókin er bókuð. Stillingin kallast "notað". Í stað þess að jafna þegar greiðsla er bókuð er hægt að nota **síðurnar Jafna lánardrottnafærslur** og **Jafna viðskm.færslur** eftir bókun greiðslunnar. Til að fræðast meira er farið í til [dæmis að stemma lánardrottnagreiðslur af við útgreiðslubókina eða lánardr.færslur](payables-how-apply-purchase-transactions-manually.md).  

- Fáðu tillögur um greiðslur til lánardrottna eða starfsmanna

    Aðgerðirnar **Leggja til lánardrottnagreiðslur** og **Greiðslutillögur starfsmanna** geta hjálpað til við að fylla út greiðslubókarlínur sjálfkrafa samkvæmt forgangsröðun lánardrottins og gjalddögum. Nánari upplýsingar eru notaðar með því að fara á Greiðslutillögur til [lánardrottins](payables-how-suggest-vendor-payments.md). Með þessari aðgerð er reiturinn **Jöfnunarskjalsnúmer** alltaf fylltur út.  

- Prenta ávísanir og senda greiðslur rafrænt til bankans

    Til viðbótar við að skrá þig að greiðslan er hafi verið gerð, geturðu einnig notað síðuna **Greiðslubók** til að gera greiðsluna móttækilega fyrir frekari vinnslu hjá bankanum þínum. Til að fræðast meira er farið í Greiðslur [vegna tékka](payables-how-work-checks.md) og [útbúa rafrænar greiðslur](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## Til að greiða í greiðslubók

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Greiðslubækur** og velja síðan viðkomandi tengil.
2. Færslubókarkeyrslan sem notuð er fyrir greiðslur er opnuð.
3. Ef þú veist hverjum á að greiða skaltu fylla í reitina handvirkt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Til að jafna greiðsluna einnig við tengdan reikning eða kreditreikning er reiturinn **Jöfnunarnúmer valinn.** á síðunni **Jafna lánardrottnafærslur** skal velja viðeigandi reikning eða kreditreikning og velja svo hnappinn **Í lagi** .

    Margir reitir, svo sem **Upphæð** fylgiskjals og **Gjalddagi**, innihalda nú upplýsingar úr völdu skjali.
5. Einnig er hægt að nota aðgerðina **Leggja til lánardrottnagreiðslur** . Allar upplýsingar um jöfnun og upphæðir eru einnig færðar inn í færslubókarlínurnar. Nánari upplýsingar eru notaðar með því að fara á Greiðslutillögur til [lánardrottins](payables-how-suggest-vendor-payments.md).
6. Þegar lokið hefur verið við allar útgreiðslubókarlínur skal velja aðgerðina **Bóka** .

## Gefa út endurgreiðsluávísun

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Greiðslubækur** og veldu síðan tengda tengilinn.
2. Í reitnum **Skjalagerð** skal velja **Endurgreiða**.  
3. Í reitnum **Númer utanaðk.**  skjalser færð inn tilvísun fyrir tékka endurgreiðslu (til dæmis vöruskilapöntunarnúmer).  
4. Í reitnum **Tegund reiknings** er valið **Viðskiptamaður**.  
5. Í reitnum **Reikningsnúmer** skal velja reikningsnúmer viðskiptavinar sem stíla á endurgreiðsluávísunina á.  
6. Í reitinn **Upphæð** skal færa inn upphæð endurgreiðslunnar.  
7. Í reitnum **Tegund mótreiknings** er **Bankareikningur** valinn.  
8. Í reitnum **Mótreikningur nr.** er valinn bankareikningurinn sem tékkinn kemur út úr.  
9. Í **Jöfnunarskjalsnúmer** Skjölin sem þarfnast endurgreiðslu eru valin.  
10. Þegar öllum útgreiðslubókarlínum hefur verið lokið skal velja aðgerðina **Bóka/Prenta**, velja aðgerðina **Bóka og prenta** og velja **svo Já**.  
  
## Sjá einnig .

[Framkvæma ávísanagreiðslur](payables-how-work-checks.md)  
[Framkvæma rafrænar greiðslur](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Stjórna skuldum](payables-manage-payables.md)  
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Flytja út jákvæða greiðsluskrá](finance-how-positive-pay.md)  
[Vinna í færslubókum](ui-work-general-journals.md)  
[Sérstilling verksvæðis](ui-personalization-user.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
