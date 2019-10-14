---
title: Hvernig á að grunnstilla fyrirtæki með RapidStart-leiðsagnarforriti | Microsoft Docs
description: Fljótlegt er að skilgreina nýja fyrirtækið sem var stofnað með því að nota RapidStart Services leiðsagnarforritið.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: a6bc660112edb7a316fcbb2f0bdfddd0f5e90634
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308141"
---
# <a name="configure-a-company-with-the-rapidstart-wizard"></a>Grunnstilla fyrirtæki með RapidStart-leiðsagnarforriti
Fljótlegt er að skilgreina nýja fyrirtækið sem var stofnað með því að nota RapidStart Services leiðsagnarforritið.

Í eftirfarandi aðgerð hefur viðskiptamanninum verið veitt grunnstillingarpakki, sem er síðan uppsettur á tölvu. Viðskiptavinurinn opnar nýja fyrirtækið, sem inniheldur engin viðskiptamannagögn. Notandi eða viðskiptamaður fylgir síðan skrefunum í leiðsagnarforriti RapidStart Services sem lýst er í þessu ferli, til að veita grunnupplýsingar um fyrirtækið. Leiðsagnarforritið flytur inn skilgreiningarpakkann og notar svo pakkann á fyrirtækið.  

## <a name="to-configure-a-new-company"></a>Til að grunnstilla nýtt fyrirtæki  
1. Í Mitt hlutverk RapidStart Services innleiðara skal velja aðgerðina **RapidStart leiðsagnarforrit**.  
2. Útvíkka flýtiflipann **Skref 1** sem inniheldur almennar upplýsingar um nýja fyrirtækið. Færa inn viðeigandi upplýsingar um nýja fyrirtækið í reitina. Til er einn reitur sem verður að fylla út, **Heiti**. Aðrir reitir eru valfrjálsir.  
3. Útvíkka flýtiflipann **Skref 2** sem inniheldur samskipta- og tengiliðaupplýsingar um nýja fyrirtækið. Færa inn viðeigandi upplýsingar um nýja fyrirtækið í reitina.
4. Útvíkka flýtiflipann **Skref 3** sem inniheldur bankareiknings- og greiðsluupplýsingar um nýja fyrirtækið. Færa inn viðeigandi upplýsingar um nýja fyrirtækið í reitina.  
5. Flýtiflipinn **Skref 4** er stækkaður. Velja hnappinn **AssistEdit** til að velja afbrigði pakka sem á að nota. Heiti grunnstillingarpakkans er birt. Hægt er að framkvæma eftirfarandi aðgerðir í þeirri röð sem gefin er upp:  

    1. Nota skilgreininguna með því að velja aðgerðina **Nota pakka**. Þetta flytur inn grunnstillingarpakkann og notar gagnagrunnsgögn pakkans á sama tíma.  

    2. Fara skal yfir grunnstillinguna eftir virkjun hennar. Þessi valkostur gerir kleift að fara yfir upplýsingar um skilgreiningar og spurningalista frá félaga og flytja inn nauðsynleg aðalgögn fyrir fyrirtækið. Velja skal aðgerðina **Grunnstillingarvinnublað**. Frekari upplýsingar er að finna í [Að ljúka við spurningalista grunnstillingar](admin-gather-customer-setup-values.md#to-complete-the-configuration-questionnaire).  

6. Flýtiflipinn **Skref 5** er stækkaður. Tilgreinið Mitt hlutverk sem á að vera sjálfgefin fyrir nýja fyrirtækið.  

    > [!IMPORTANT]  
    >  Aðeins breyta Mínu hlutverki notanda eftir hann hefur lokið við grunnstillingu fyrirtækisins. Ef breyta þarf fleiri uppsetningaratriðum skal fyrst notast við grunnstillingarvinnublaðið. Síðan er farið aftur í leiðsagnarforritið til að uppfæra forstillingar Mitt hlutverk eða valin aðgerðin **Klára uppsetningu**.

7. Velja hnappinn **Í lagi**.  
8. Til að ganga úr skugga um að grunnstillingarupplýsingarnar hafi verið notaðar á nýja fyrirtækið skaltu velja ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Fyrirtækjaupplýsingar** og veldu síðan tengda tengilinn.

Síðan **Stofngögn** inniheldur upplýsingar sem hafa verið tilgreindar.   

Á þessum tímapunkti hefur fyrirtækið verið skilgreint og gögn notuð í það.  

## <a name="see-also"></a>Sjá einnig  
[Nota skilgreiningu á ný fyrirtæki](admin-apply-configuration-to-new-companies.md)  
[Uppsetning fyrirtækis með RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Stjórnun](admin-setup-and-administration.md)
