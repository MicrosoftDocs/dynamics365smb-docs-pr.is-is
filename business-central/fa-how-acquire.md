---
title: Komast yfir eignir
description: Hægt er að setja upp eign, úthluta afskriftabók, og skrá kaupverð eignarinnar.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.search.form: 5605, 5551, 5600, 5628, 5629
ms.date: 12/03/2021
ms.author: edupont
ms.openlocfilehash: e0a60cbb82c99e3497a6f8d1907c261b6199e7ec
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141211"
---
# <a name="acquire-fixed-assets"></a>Komast yfir eignir
Setja verður upp spjald fyrir hverja eign með upplýsingum um eignina. Hægt er að setja byggingar eða framleiðslubúnað sem aðaleign með íhlutalista upp og hægt er að flokka þær á ýmsa vegu, eins og eftir flokki, deild eða staðsetningu. Afskriftabók þarf að setja upp og tengja hverri eign áður en hægt er að komast yfir hana.

Þegar eign er sett upp og Afskriftabók tengd henni, verðurðu að komast yfir eignina. Til að komast yfir eign, skráirðu kaupferð hennar í viðeigandi Fjárhagsreikning, bankareikning, eða lánardrottin með því að bóka kaupfærslu af síðunni **Fjárhagsbók eigna** . Þú getur notað síðuna **Aðstoð við eignakaup** til að stofna og bóka nauðsynlegar færslubókarlínur sjálfvirkt.

Hrakvirði er afgangsvirði eignar þegar ekki er lengur hægt að nota hana. Hægt er að bóka hrakvirðið um leið og stofnkostnaður er bókaður. Nánari upplýsingar sjá [Afskrifa eða greiða af eignum](fa-how-depreciate-amortize.md).

Endurmat er notað til að laga virði að almennum verðbreytingum. Hægt er að nota keyrsluna **Endurmat eigna** til að reikna kaupferð á endurnýjunarverði.

## <a name="to-create-a-fixed-asset-and-acquire-it-automatically"></a>Stofna eign og komast yfir hana sjálfkrafa
Eftirfarandi ferli sýnir hvernig á að stofna eign og komast svo yfir hana með því að nota **aðstoð við eignakaup** síðuna til að stofna og bóka nauðsynlegar eignafjárhagslínur. Hægt er að einnig að stofna og bóka færslubókarlínurnar handvirkt. Nánari upplýsingar eru í [Bókun eignakaupa handvirkt með fjárhagsbók eigna](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignir** og velja síðan viðkomandi tengil.  
2. Velja sem **Nýtt** aðgerð og síðan fyllt út í reitina á **Almenna** Flýtiflipanum eins og þörf krefur. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Fyllt er út í reiti eftir því sem við á í flýtiflipanum **afskriftabók**. Þetta skref úthlutar afskriftabók á eigninni.  
4. Ef það þarf að úthluta fleiri en einni afskriftabók á eign skal velja **bæta Við Fleiri Afskriftabækur** aðgerð. Frekari upplýsingar er að finna í [Úthluta afskriftarbók á eign](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

    Þegar allir reitir sem þarf til að komast yfir eign eru fylltir út, birtist **hægt er að komast yfir eignina. Komast yfir** tilkynning efst á síðunni.
5. Valið er **Komast yfir** aðgerð í tilkynningunni.
6. Fylgja leiðbeiningunum á síðunni **aðstoð við eignakaup** til að ljúka sjálfvirka kaup eignarinnar.

> [!NOTE]  
>   Einnig má bóka kaupverð sem lánsfé. Í því tilfelli skal muna að gildið í reitnum **kaupverð með VSK** á að vera með mínusmerki til að tilgreina lánið.

Þegar valið er **Ljúka**, er fyllt í reitinn **Bókfært virði** á síðunni **Eignaspjald** sem gefur til kynna að eignin var keypt á tilgreindu kaupverði.  

## <a name="to-set-up-a-component-list-for-a-main-asset"></a>Uppsetning íhlutalista fyrir aðaleignir:
Hægt er að flokka eignir í aðaleignir og íhluti þeirra. Í framleiðslutæki gætu til dæmis verið margir hlutir sem þarf að flokka á þennan hátt.  

Setja verður bæði aðaleignina og íhluti hennar upp sem einstök eignaspjöld. Þegar íhlutalistinn hefur verið settur upp fyllir [!INCLUDE[prod_short](includes/prod_short.md)] sjálfkrafa í reitina **Aðaleign/íhlutur** og **Íhlutir aðaleignar** á eignarspjöldunum.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignir** og velja síðan viðkomandi tengil.
2. Valin er eignin sem er aðaleignin er valin síðan **íhlutir aðaleignar** aðgerð.
3. Á síðunni **Íhlutir aðaleignar** skal velja reitinn **Eignanr.** og síðan valið eignin sem á að bæta við sem íhlut aðaleignar.
4. Lokaðu síðunni.
5. Endurtaktu þrep 3 og 4 fyrir hverja íhlut eignar sem ætlunin er að bæta við.
6. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning eignar** og velja síðan viðkomandi tengil.
7. Valinn er **Leyfa Bókun á Aðaleignir** gátreitinn.

## <a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal"></a>Bókun eignakaupa handvirkt með fjárhagsbók eigna.
Eftirfarandi ferli sýnir hvernig á að komast yfir eign handvirkt með því að stofna og bóka línur á síðunni **Fjárhagsbók eigna**. Einnig má komast yfir eign sjálfkrafa með því að nota síðuna **aðstoð við eignakaup**. Frekari upplýsingar er að finna í skrefi 5 í [Stofna eign og komast yfir hana sjálfkrafa](fa-how-acquire.md#to-create-a-fixed-asset-and-acquire-it-automatically).

> [!NOTE]  
>   Einnig má bóka kaupverð sem lánsfé. Í því tilfelli muna sem gildið í reitnum **upphæð** að vera með mínusmerki til að tilgreina kredit.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eignafjárhagsbók** og velja síðan viðkomandi tengil.
2. Á síðunni **Fjárhagsbók eigna** í reitnum **Eignabókunartegund** er valið **Kaupverð**.
3. Fyllið inn í eftirstandandi reiti eftir þörfum.
4. Valið er **Bóka** aðgerðin.  

> [!TIP]  
>   Ef þú fyllir upp í reitinn **Tryggingarnúmer** í fjárhagsbók eigna þegar kaupverð er bókað, mun [!INCLUDE[prod_short](includes/prod_short.md)] líka bóka kaupverð eignarinnar í vátryggingasviðsbókina. Nánari upplýsingar sjá [Tryggja eignir](fa-how-insure.md).

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>Ógilding bókunar kaupverðs fyrir eina eign
Ef villa á sér stað við bókun stofnkostnaðar er hægt að fjarlægja færsluna með keyrslunni **Afturkalla eignafærslur** og bóka síðan rétta stofnkostnaðarfærslu. Röngu færslurnar eru fluttar á síðuna **Rangar eignafærslur.**

Ef kaup eru til dæmis bókuð með rangri dagsetningu þarf að leiðrétta hana eins fljótt og unnt er þar sem bókunardagsetning eigna er notuð fyrir marga mikilvæga útreikninga.

> [!IMPORTANT]  
> Ekki er hægt að nota aðgerðina **Bakfæra viðskipti** fyrir eignarfærslur.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") Táknið, færa inn **eignafærslur** og velja síðan tengda tengilinn.  
2. **Á síðunni eignafærslur** er færslan eða færslurnar sem á að hætta við valdar.  
3. **Veldu valmyndina aðgerðir** og veldu **síðan aðgerðina Hætta við færslur**.
4. Fyllið inn reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Veldu hnappinn **Í lagi** til að ræsa keyrsluna.
6. Þegar röng færsla eða færslur eru ógiltir, skal halda áfram og bóka rétt kaupverð.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>Bóka hrakvirði með kaupverði.
Hægt er að bóka hrakvirði með stofnkostnaði af færslubók eigna.

> [!NOTE]
> Þetta ferli gæti krafist þess að þú færslubókasíðu eigna með því að bæta við reitnum Hrakvirði. Reiturinn er ekki sjálfgefið sýndur á síðunni. Frekari upplýsingar eru í [Sérstilling verksvæðis](ui-personalization-user.md).

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Færslubækur eigna** og velja síðan viðkomandi tengil.
2. Á síðunni **Eignabækur** skaltu búa til kauplínuna. Nánari upplýsingar eru í [Bókun eignakaupa handvirkt með fjárhagsbók eigna](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).
3. Í reitinn **Hrakvirði** í færslubókarlínunni skal færa inn upphæð hrakvirðis sem kreditfærslu (settu mínusmerki að framan, t.d. **-** 100).
4. Valið er **Bóka** aðgerðin.

> [!NOTE]
> Ef hrakvirði er til staðar fyrir eign verður það gildi notað í afskriftabókun í stað gildis í reitnum **Bókfært lokavirði** á síðunni **Eignaafskriftarbækur** . Frekari upplýsingar eru í [Til að stjórna bókfærðu lokavirði](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## <a name="see-also"></a>Sjá einnig
[Eignir](fa-manage.md)  
[Uppsetning eigna](fa-setup.md)  
[Fjármál](finance.md)  
[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Unnið með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]