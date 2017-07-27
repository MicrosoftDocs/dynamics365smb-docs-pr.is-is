---
title: Uppsetning eignaafskrifta| Microsoft Docs
description: "Tiltekið er í afskriftabók hvernig þú vilt að eignir verði afskrifaðar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: fbdfc4431056c4851208aa063daf8761b4e70bf1
ms.contentlocale: is-is
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-fixed-asset-depreciation"></a>Hvernig á að: Uppsetning afskriftir eigna
 Hægt er að nota ýmsar afskriftaaðferðir vegna reikningsskila og skattframtals. Mörg stórfyrirtæki nota beinlínuafskriftir í reikningsskilum vegna þess að með þeim er yfirleitt hægt að tilgreina hærri tekjur. Vegna tekjuskatts nota þó mörg fyrirtæki hraðafskriftaaðferð. Frekari upplýsingar eru í [afskriftaaðferðir](fa-depreciation-methods.md)

 Þegar stofnaðar hafa verið viðeigandi afskriftabækur verður að tengja eina eða fleiri afskriftabækur við hverja eign. Afskriftabók sem úthlutað er á eign er vísað til sem afskriftabók eigna. Í samræmi við það heitir glugginn fyrir úthlutaðar afskriftabækur **Eignaafskriftabækur**.

## <a name="to-create-a-depreciation-book"></a>Stofna afskriftabók
Í eignaafskriftabók er tilgreint hvernig eignir eru afskrifaðar. Ef gera á ráð fyrir margvíslegum afskriftaaðferðum má setja upp margar afskriftabækur.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Afskriftabækur** og velja svo viðeigandi tengil.
2. Í glugganum **afskriftabókalisti** skal velja aðgerðina **Nýtt**.
3. Í glugganum **afskriftabókarspjald** þarf að fylla reitina út eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   Hægt er að skrá eignafærslur í **Fjárhagsbók eigna** gluggann eða í **færslubók eigna** gluggann, allt eftir því hvort færslurnar eru fyrir fjárhagsskýrslugerð eða fyrir innri stjórnun. Fylgja á næsta skref til að skilgreina hvaða tegund færslubókar er notuð sjálfgefið fyrir hinum ýmsu aðgerðum eigna.
4. Í **Samþætting** Flýtiflipanum skal velja gátreit fyrir hverja aðgerð eignar sem bóka á færslur fyrir með því að nota **Fjárhagsbók eigna** gluggann.
5. Endurtaka skal skref 2 til 4 fyrir hverja afskriftaaðferð eða bókunaraðferð sem úthluta á á eignir sem afskriftabók.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset"></a>Úthluta afskriftabók á eign.
1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **eignir** og velja svo viðeigandi tengil.
2. Valin er eignin sem setja á upp eignaafskriftabók fyrir.
3. Fyllt er út í reiti eftir því sem við á í flýtiflipanum **afskriftabók**.
4. Ef það þarf að úthluta fleiri en einni afskriftabók á eign skal velja **bæta Við Fleiri Afskriftabækur** aðgerð.
5. Einnig má velja aðgerðina **Afskriftabækur** til að tilgreina eina eða fleiri eigna-/afskriftabók.

    > [!NOTE]  
>   Þegar handvirk afskriftaaðferð er notuð verður að færa afskriftirnar handvirkt í fjárhagsfærslubók eigna. Aðgerðin **Reikna afskriftir** sleppir eignum sem handvirk afskriftaaðferð er notuð á. Hægt er að nota þessa aðferð á eignir sem ekki eru afskrifanlegar, til dæmis land.

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job"></a>Til að tengja afskriftabók við margar eignir með keyrslu
Ef tengja á afskriftabók við nokkrar eignir er hægt að keyra **Stofna eignaafskriftabækur** runuvinnsluna til að stofna eignaafskriftabækur.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **eignir** og velja svo viðeigandi tengil.
2. Valin er eignin fyrir hverja setja á upp afskriftabók fyrir, og velja síðan sem **Breyta** aðgerð.
3. Í glugganum **Afskriftabókarspjald** er valið **Stofna Eignaafskriftabækur** aðgerð.
4. Í glugganum **stofna eignaafskriftabækur** er fyllt inn í reitinn **afskriftarbók** .
5. Veldu **Afrita frá eignarnr.** reitinn, og veljið síðan eignanúmerið sem á að nota sem grunn að stofnun nýrra eignaafskriftabóka.

    Ef þessi reitur er fylltur út verða sömu upplýsingar í afskriftareitunum í nýju eignaafskriftabókinni og eru í samsvarandi reitum í eignaafskriftabókinni sem er afritað úr. Reiturinn er hafður auður ef búa á til nýja eignaafskriftabók með auðum afskriftareitum.  
6. Á flýtiflipanum **Eign** er hægt að setja afmörkun til að velja eignirnar sem á að stofna eignaafskriftabók fyrir.
7. Velja hnappinn **Í lagi**.

## <a name="to-set-up-depreciation-posting-types"></a>Uppsetning bókunartegundir afskrifta:
Fyrir hverja afskriftabók þarf að stilla hvernig [!INCLUDE[d365fin](includes/d365fin_md.md)] á að meðhöndla ýmsar bókunartegundir. Til dæmis hvort bókun eigi að vera í debet eða kredit og hvort taka eigi bókunartegund með í afskriftargrunni.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Afskriftabækur** og velja svo viðeigandi tengil.  
2. Valin er afskriftabók sem á að setja upp og velja síðan **eignarbókunarflokkur** aðgerð.
3. Í glugganum **uppstning eignarbókunarflokks** þarf að fylla reitina út eftir þörfum.

    > [!NOTE]  
>   Ekki er hægt að skjóta inn eða eyða línum í glugganum **Eignabókunartegund uppsetning**. Aðeins er hægt að breyta þeim línum sem fyrir eru.

    Sterklega er mælt með því að uppsetningunni fyrir afskriftarbækur sem búið er að bóka í sé ekki breytt. Breytingarnar hafa ekki áhrif á færslur sem þegar er búið að bóka og sem myndu gera tölfræðigögn afskriftarbókarinnar óáreiðanleg.

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation"></a>Uppsetning Sjálfgefinna sniðmáta og -keyrslna fyrir afskriftir eigna.
Skilgreina þarf sjálfgefna uppsetningu fyrir sniðmát og keyrslur fyrir hverja afskriftabók. Þú notar þessi sjálfgildi til að afrita línur úr einni bók í aðra, búa til færslubókarlínur með því að keyra **Reikna afskrift** eða **Vísitala eigna** runuvinnslurnar, afrita kaupverð í vátryggingabókina.  

1. Velja skal ![Leit að síðu eða skýrslu](media/ui-search/search_small.png "Leit að síðu eða skýrslu táknið") tákn, slá inn **Afskriftabækur** og velja svo viðeigandi tengil.  
2. Valin er afskriftabók sem á að skilgreina sjálfgefnar bækur fyrir, og veldu svo aðgerðina **uppsetning eignabókar**.  
3. Ef sjálfgefin uppsetning á að vera fyrir hvern notanda skal velja reiturinn **Kenni notanda** til að velja úr glugganum **Notendur**.  
4. Í öðrum reitum er valið er sniðmát færslubókar eða bókarkeyrslu sem nota verður sjálfgefið.  

## <a name="see-also"></a>Sjá einnig
[Uppsetning eigna](fa-setup.md)  
[Eignir](fa-manage.md)  
[Fjármál](finance.md)  
[Velkomin(n) í [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Unnið með [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

