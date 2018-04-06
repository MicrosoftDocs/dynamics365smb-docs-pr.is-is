---
title: Setja upp Yodlee bankastreymi| Microsoft Docs
description: "Hægt er að umreikna greiðsluupplýsingar í hvaða gagnasnið sem bankinn krefst og opna fyrir inn- og útflutning á bankaskrám."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, payment process
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fa5c0c39dbbce40b59d639f810522c66da1a09ab
ms.contentlocale: is-is
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-the-envestnet-yodlee-bank-feeds-service"></a>Setja upp Envestnet Yodlee bankastreymisþjónustu
Hægt er að flytja inn rafræn bankayfirlit frá bankanum til að fylla fljótlega út gluggann **Greiðsluafstemmingarbók** þannig að hægt sé að jafna greiðslur og stemma af bankareikninginn. Nánari upplýsingar er að finna í [Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Envestnet Yodlee bankastreymisþjónusta er uppsett sem viðbót við [!INCLUDE[d365fin](includes/d365fin_md.md)] og tilbúin til að láta virkja sig. Frekari upplýsingar skoða [Sérstilla [!INCLUDE[d365fin](includes/d365fin_md.md)] Nota viðbætur](ui-extensions.md).

> [!NOTE]
> Envestnet Yodlee bankastreymisþjónusta er aðeins studd í BNA, Kanada og Bretlandi.

Þegar búið að virkja bankastreymisþjónustu, verður að tengja bankareikning við netbankareikning sem streymið kemur úr. Þú býrð til tengla frá bankareikningum í netbankareikninga í mismunandi eftirfarandi aðstæður:

* Bankareikning er ekki til í [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrir netbankareikning þinn. Því er stofnarðu bankareikning með því að búa til tengil úr netbankareikningi.
* Bankareikningur er til staðar í [!INCLUDE[d365fin](includes/d365fin_md.md)], sem þú vilt tengja við netbankareikning.
* Tengdar bankareikning þarf að aftengja af því þú vilt hætta að nota bankastreymisþjónustuna fyrir reikninginn..
* Netbankareikningar hafa breyst og þú vilt uppfæra upplýsingarnar um bankareikninga í [!INCLUDE[d365fin](includes/d365fin_md.md)].

Þegar bankastreymisþjónustan er virkjuð, geturðu sett upp bankareikning til að flytja sjálfvirkt inn nýja bankayfirlitin í **Greiðsluafstemmingarbók** gluggann á tveggja tíma fresti. Færslur fyrir greiðslur sem þegar hafa verið bókaðar sem jöfnuð og/eða stemmt af í **Greiðsluafstemmingarbók** glugganum verða ekki fluttar inn. Sjá frekari upplýsingar í “Til að virkja sjálfvirkan innflutning bankayfirlits” hlutann.

> [!NOTE]  
>   Ef þú notar uppsetningaraðstoðina í Setja upp fyrirtæki, þá geta sum skrefin í ferlunum sem fylgja þar á eftir gerst sjálfvirkt þegar þú ert kominn í uppsetninguna fyrir bankareikning fyrirtækis. Nánari upplýsingar, sjá [Velkomin í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md).

## <a name="to-enable-the-bank-feed-service"></a>Til að virkja bankastreymisþjónustu
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bankareikningar** og velja svo viðeigandi tengil.
2. Opnið bankareikning sem á að nota fyrir bankastreymisþjónustuna.
3. Í á **Bankareiknings** glugganum í á **infflutningssnið BankaYfirlits** er valinn YODLEEBANKFEED .  

Bankastreymisþjónusta verður virkjuð þegar þú tengir bankareikning við tendan netbankareikning. Sjá næsta ferli..  

## <a name="to-create-a-new-linked-bank-account"></a>Stofna nýjan tengdan bankareikning
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bankareikningar** og velja svo viðeigandi tengil.
2. Valinn er viðeigandi bankareikningur og síðan valið **stofna nýjan tengdan bankareikning**. **Stofnun tengla fyrir Bankareiknings** opnast eftir smá stund.

    > [!NOTE]  
>   Þessi gluggi sýnir raunverulega vefsíðu fyrir Bankastreymisþjónustu Envestnet Yodlee. Hugtök og virkni í glugganum mega ekki vera þau sömu og í þessu efnisatriði.  
3. Í á **Stofnun tengla fyrir netbankareikninga** glugga í á **Tengja Reikning** flipanum, skal nota leitaraðgerðina til að finna banka þar sem þú ert með einn eða fleiri netbankareikninga.
4. Veljið nafn banka. **Skrá inn** svæðinu opnast.
5. Sláðu inn notandanafn og aðgangsorð sem er notuð til að skrá inn í netbanka og velja síðan **Næst** hnapp.  
6. Bankastreymisþjónusta undirbýr að tengja fyrsta netbankareikning á tilgreindum banka í nýja bankareikninginn í [!INCLUDE[d365fin](includes/d365fin_md.md)].

    > [!NOTE]  
>   Ef þú ert með fleiri en einn netbankareikning í bankanum, verður að stofna fleiri bankareikninga í [!INCLUDE[d365fin](includes/d365fin_md.md)] fyrir þá. Sjá skref 8 til 10.  

    Þegar vinnslunni er lokið, birtist bankaheitið í **Mínir reikningar** svæðinu á **Tengt** flipanum. Númerið í svigunum gefur til kynna hversu margir netbankareikningar voru tengdir.  
7. Velja hnappinn **Í lagi**.

    Ef aðeins er verið að tengja einn netbankareikning, mun **Bankareikningsspjald** glugginn opnast og birta heiti netbankareikningsins. Í þessu tilfelli er tenging bankareiknings lokið. Allt sem er eftir er að setja upp bankareikninginn. Nánari upplýsingar um það eru í [Setja upp bankareikninga](bank-how-setup-bank-accounts.md).

    Ef fleiri en einn netbankareikningur eru tengdir, mun **Tenglar fyrir bankareikning** glugginn opnast og sýna skrár yfir netbankareikninga sem eru enn ekki tengdir við bankareikninga í [!INCLUDE[d365fin](includes/d365fin_md.md)]. Í því tilviki, fylgið næsta skrefi.  
8. Í á **Stofnun tengla fyrir bankareikning** glugganum, velja línuna fyrir netbankareikning, og velja síðan **tengja í Nýr Bankareikningur** aðgerð.  

    **Bankareikningsspjald** glugginn fyrir nýr bankareikningur opnast og sýnir nafn netbankareikningsins.

    Ef bankareikningur er til í [!INCLUDE[d365fin](includes/d365fin_md.md)] sem á að tengja annan netbankareikning við, skal fylgja næsta skrefi.  
9. Í á **Stofnun tengla fyrir bankareikning** glugganum, velja línuna fyrir netbankareikning, og velja síðan **tengja í fyrirliggjandi Bankareikningur** aðgerð.
10. Í glugganum **Listi yfir bankareikninga** er valið bankareikningur sem á að tengja í og smellt á **Í lagi**.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>Til að tengja bankareikning í netbankareikning
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bankareikningar** og velja svo viðeigandi tengil.
2. velja línuna fyrir bankareikning sem er ekki tengdur við netbankareikningur, og velja síðan **tengja í netbankareikning** aðgerð. **Stofnun tengla fyrir netbankareikning** glugginn opnast með heiti bankans sem var forútfylltur í svæðinu **Tengja reikning**
3. Veljið nafn banka. **Skrá inn** svæðinu opnast.
4. Sláðu inn notandanafn og aðgangsorð sem er notuð til að skrá inn í netbanka og velja síðan **Næst** hnapp.  

    Bankastreymisþjónusta undirbýr að tengja bankareikning í [!INCLUDE[d365fin](includes/d365fin_md.md)] við viðkomandi netbankareikning.  

    Þegar vinnslunni er lokið á árangursríkan hátt, birtist bankaheiti á **Mínar Reikninga** svæðinu í á **Tengt** flipanum. Ef bankinn er með fleiri en einn bankareikning, er aðeins bankareikningurinn sem þú valdir í skrefi 2 tengdur.  
5. Velja hnappinn **Í lagi**.

Í glugganum **Bankareikningayfirlit** er valinn  **tengt** gátreiturinn .

## <a name="to-unlink-a-bank-account"></a>Að Aftengja bankareikningi
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bankareikningar** og velja svo viðeigandi tengil.  
2. Velja línuna fyrir tengdar bankareikning sem á að aftengja frá sínum tengda netbankareikningi, og velja síðan **aftengja frá netbankareikning** aðgerð.

> [!NOTE]  
>   Ef þú velur **Já** í staðfestingarglugganum, er tengillinn í netbankareikninginn fjarlægður, og innskráningarupplýsingar eru þurrkaðar út. Til að tengja bankareikning við netbankareikning aftur verðurðu að skrá þig inn í bankann aftur. Nánari upplýsingar er að finna í “Til að tengja bankareikning í netbankareikning“ hlutanum.

## <a name="to-update-bank-account-linking"></a>Uppfæra tengla bankareikninga
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bankareikningar** og velja svo viðeigandi tengil.
2. Valinn er viðeigandi bankareikningur og síðan valið **uppfæra tengla bankareiknings** aðgerðina.

Ef vandamál eru til staðar fyrir tengdu bankareikninga í glugganum **Bankareikningayfirlit** opnast **Stofnun tengla fyrir bankareikninga** og tilgreinir hvaða bankareikningar hafa verið vandamál. Vandamál má besta leyst með því að aftengja netbankareikninginn og síðan endurstofna tengilinn. Nánari upplýsingar er að finna í “Til að tengja bankareikning í netbankareikning“ hlutanum.

## <a name="to-enable-automatic-import-of-bank-statements"></a>Til að virkja sjálfvirkan innflutning bankayfirlits
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **bankareikningar** og velja svo viðeigandi tengil.
2. Veldu línuna fyrir tengdu bankareikningur og síðan valið **uppsetning sjálfvirks innflutnings bankayfirlits** aðgerð.
3. Í glugganum **uppsetning sjálfvirks innflutnings bankayfirlits** glugga í á **Fjöldi daga innifalið** reitnum, er tilgreint hversu langt aftur í tíma á að fá nýjar bankafærslur fyrir.

    > [!NOTE]  
>   Mælt er með því að setja þetta gildi á 7 daga eða fleiri.  
4. Veldu **virkjað** gátreitinn.  

Á hverri klukkustund mun **Greiðsluafstemmingarbók** glugginn sýna nýjar greiðslur sem eru framkvæmdar á netbankareikningi.

> [!NOTE]  
>   Færslur fyrir greiðslur sem þegar hafa verið bókaðar sem jöfnuð og/eða stemmt af í **Greiðsluafstemmingarbók** glugganum verða ekki fluttar inn.

## <a name="see-also"></a>Sjá einnig
[Uppsetning bankaþjónustu](bank-setup-banking.md)  
[Stjórna bankareikningum](bank-manage-bank-accounts.md)  
[Jafna greiðslur sjálfkrafa og afstemma bankareikninga](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Sérstilling [!INCLUDE[d365fin](includes/d365fin_md.md)] með viðbótum ](ui-extensions.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

