---
title: Uppsetning eignaafskrifta| Microsoft Docs
description: Tiltekið er í afskriftabók hvernig þú vilt að eignir verði afskrifaðar.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c9eea613db52d327caa1c3d5449864900fc867d1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749270"
---
# <a name="set-up-fixed-asset-depreciation"></a>Setja upp eignaafskriftir
 Hægt er að nota ýmsar afskriftaaðferðir vegna reikningsskila og skattframtals. Mörg stórfyrirtæki nota beinlínuafskriftir í reikningsskilum vegna þess að með þeim er yfirleitt hægt að tilgreina hærri tekjur. Vegna tekjuskatts nota þó mörg fyrirtæki hraðari afskriftaaðferð á borð við hlutfallslega afskrift. Afskriftaraðferð eignar er tilgreind með svæðinu **Afskriftaraðferð** á síðunni **Eignaspjald**. Frekari upplýsingar um hvað mismunandi aðferðir gera eru í [Afskriftaaðferðir](fa-depreciation-methods.md).

 Í afskriftabækur eru skilgreindar mismunandi leiðir til að reikna út afskriftir fyrir mismunandi eignir. Fyrir hverja bók er hægt að skilgreina sérstakar afskriftareglur. Til dæmis má tilgreina að eign skuli vera afskrifuð á þriggja ára tímabili í einni bók og á fimm ára tímabili í annarri bók.

 Þegar stofnaðar hafa verið viðeigandi afskriftabækur verður að tengja eina eða fleiri afskriftabækur við hverja eign. Afskriftabók sem úthlutað er á eign er vísað til sem afskriftabók eigna. Setja má upp ótakmarkaðan fjölda afskriftabóka fyrir eign. 

## <a name="to-create-a-depreciation-book"></a>Stofna afskriftabók
Í eignaafskriftabók er tilgreint hvernig eignir eru afskrifaðar. Ef gera á ráð fyrir margvíslegum afskriftaaðferðum má setja upp margar afskriftabækur.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Afskriftabækur** og veldu síðan tengda tengilinn.
2. Á síðunni **afskriftabókalisti** skal velja aðgerðina **Nýtt**.
3. Fyllt er út í reiti eftir því sem á við á síðunni **Afskriftabókarspjald**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Hægt er að skrá eignafærslur á síðunni **Fjárhagsbók eigna** eða á síðunni **Færslubók eigna**, allt eftir því hvort færslurnar eru fyrir fjárhagsskýrslugerð eða fyrir innri stjórnun. Fylgja á næsta skref til að skilgreina hvaða tegund færslubókar er notuð sjálfgefið fyrir hinum ýmsu aðgerðum eigna.
4. Í **Samþætting** Flýtiflipanum skal velja gátreit fyrir hverja aðgerð eignar sem bóka á færslur fyrir með því að nota **Fjárhagsbók eigna** síðuna.
5. Endurtaka skal skref 2 til 4 fyrir hverja afskriftaaðferð eða bókunaraðferð sem úthluta á á eignir sem afskriftabók.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset"></a>Úthluta afskriftabók á eign.
1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignir** og veldu síðan tengda tengilinn.
2. Valin er eignin sem setja á upp eignaafskriftabók fyrir.
3. Fyllt er út í reiti eftir því sem við á í flýtiflipanum **afskriftabók**.
4. Ef það þarf að úthluta fleiri en einni afskriftabók á eign skal velja **bæta Við Fleiri Afskriftabækur** aðgerð.
5. Einnig má velja aðgerðina **Afskriftabækur** til að tilgreina eina eða fleiri eigna-/afskriftabók.

    > [!NOTE]  
    >   Þegar handvirk afskriftaaðferð er notuð verður að færa afskriftirnar handvirkt í fjárhagsfærslubók eigna. Aðgerðin **Reikna afskriftir** sleppir eignum sem handvirk afskriftaaðferð er notuð á. Hægt er að nota þessa aðferð á eignir sem ekki eru afskrifanlegar, til dæmis land.

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job"></a>Til að tengja afskriftabók við margar eignir með keyrslu
Ef tengja á afskriftabók við nokkrar eignir er hægt að keyra **Stofna eignaafskriftabækur** runuvinnsluna til að stofna eignaafskriftabækur.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Eignir** og veldu síðan tengda tengilinn.
2. Valin er eignin fyrir hverja setja á upp afskriftabók fyrir, og velja síðan sem **Breyta** aðgerð.
3. Á síðunni **Afskriftabókarspjald** er valið **Stofna Eignaafskriftabækur** aðgerð.
4. Á síðunni **stofna eignaafskriftabækur** er fyllt inn í reitinn **afskriftarbók** .
5. Veljið **Afrita frá eignanr.** reitinn, og veljið síðan eignanúmerið sem á að nota sem grunn að stofnun nýrra eignaafskriftabóka.

    Ef þessi reitur er fylltur út verða sömu upplýsingar í afskriftareitunum í nýju eignaafskriftabókinni og eru í samsvarandi reitum í eignaafskriftabókinni sem er afritað úr. Reiturinn er hafður auður ef búa á til nýja eignaafskriftabók með auðum afskriftareitum.  
6. Á flýtiflipanum **Eign** er hægt að setja afmörkun til að velja eignirnar sem á að stofna eignaafskriftabók fyrir.
7. Velja hnappinn **Í lagi**.

## <a name="to-set-up-depreciation-posting-types"></a>Uppsetning bókunartegundir afskrifta:
Fyrir hverja afskriftabók þarf að stilla hvernig [!INCLUDE[prod_short](includes/prod_short.md)] á að meðhöndla ýmsar bókunartegundir. Til dæmis hvort bókun eigi að vera í debet eða kredit og hvort taka eigi bókunartegund með í afskriftargrunni.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Afskriftabækur** og veldu síðan tengda tengilinn.  
2. Valin er afskriftabók sem á að setja upp og velja síðan **eignarbókunarflokkur** aðgerð.
3. Á síðunni **uppstning eignarbókunarflokks** þarf að fylla reitina út eftir þörfum.

    > [!NOTE]  
    >   Ekki er hægt að skjóta inn eða eyða línum á síðunni **Eignabókunartegund uppsetning**. Aðeins er hægt að breyta þeim línum sem fyrir eru.

Sterklega er mælt með því að uppsetningunni fyrir afskriftarbækur sem búið er að bóka í sé ekki breytt. Breytingarnar hafa ekki áhrif á færslur sem þegar er búið að bóka og sem myndu gera tölfræðigögn afskriftarbókarinnar óáreiðanleg.

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation"></a>Uppsetning Sjálfgefinna sniðmáta og -keyrslna fyrir afskriftir eigna.
Skilgreina þarf sjálfgefna uppsetningu fyrir sniðmát og keyrslur fyrir hverja afskriftabók. Þú notar þessi sjálfgildi til að afrita línur úr einni bók í aðra, búa til færslubókarlínur með því að keyra **Reikna afskrift** eða **Vísitala eigna** runuvinnslurnar, afrita kaupverð í vátryggingabókina.  

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Afskriftabækur** og veldu síðan tengda tengilinn.  
2. Valin er afskriftabók sem á að skilgreina sjálfgefnar bækur fyrir, og veldu svo aðgerðina **uppsetning eignabókar**.  
3. Ef sjálfgefin uppsetning á að vera fyrir hvern notanda skal velja reitinn **Kenni notanda** til að velja af síðunni **Notendur**.  
4. Í öðrum reitum er valið er sniðmát færslubókar eða bókarkeyrslu sem nota verður sjálfgefið.  

## <a name="see-also"></a>Sjá einnig
[Uppsetning eigna](fa-setup.md)  
[Eignir](fa-manage.md)  
[Fjármál](finance.md)  
[Hafist handa](product-get-started.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]