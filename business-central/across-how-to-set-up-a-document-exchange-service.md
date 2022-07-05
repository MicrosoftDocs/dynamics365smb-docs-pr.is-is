---
title: Hvernig á að setja upp skjalaskiptaþjónustu | Microsoft Docs
description: Notaður er ytri þjónustuveitandi til að skiptast á rafrænum skjölum við viðskiptafélögum.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 4a502dc56f45673c0a052b0081518ae0ec888a14
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9076020"
---
# <a name="set-up-a-document-exchange-service"></a>Setja upp skjalaskiptaþjónustu

Sem hluti af gagnaskiptarammanum er hægt að skiptast á sölu- og innkaupaskjölum við viðskiptafélaga án aukaskrefa á borð við að hengja skjölin við tölvupóstskeyti sem PDF-skrár. Til dæmis þegar þú ætlar að reikningsfæra viðskipavin getur þú bókað reikninginn og sent hann til greiðslu sem skrá sem viðskiptavinur þinn getur móttekið í viðskiptastjórnunarforritinu sínu. Frekari upplýsingar eru í [Rafræn gagnaskipti](across-data-exchange.md).

> [!NOTE]
> Uppsetning skjalaskiptaþjónustu fyrir Business Central á staðnum krefst nokkurra skrefa til viðbótar vegna heimilda. Frekari upplýsingar eru í [Stillingar fyrir Business Central á staðnum](#settings-for-business-central-on-premises).

## <a name="connecting-with-trading-partners"></a>Tenging við viðskiptafélaga

Til að skiptast á rafrænum skjölum þarf tengingu við viðskiptafélaga. Til að auðvelda þér að stofna örugga tengingu er [!INCLUDE[prod_short](includes/prod_short.md)] á netinu stillt til að nota forritið Business Central Integration. Forritið er í boði í Tradeshift App Store og allt sem þú og viðskiptaaðilar þínir þurfa að gera er að stofna Tradeshift-reikning og síðan virkja forritið. Forrit Business Central Integration kemur í vinnslu- og sandkassaútgáfum. Til dæmis er gott að nota sandkassaútgáfuna til að prófa skjalaskiptin. Þú getur skipt á milli vinnsluútgáfu og sandkassaútgáfu með því að kveikja eða slökkva á víxlhnappnum **Sandkassi** á síðunni **Uppsetning Doc. Exch. þjónustu**. Þegar þú gerir það eru upplýsingarnar í flýtiflipanum **Þjónusta** uppfærðar fyrir þig.

Ef þú vilt hinsvegar nota aðra þjónustu þarftu að gefa upp upplýsingarnar til að setja á tengingu. Frekari upplýsingar er að finna í [Að tengjast við skjalaskiptaþjónustu](across-how-to-set-up-a-document-exchange-service.md#to-connect-to-a-document-exchange-service).

## <a name="to-connect-to-the-business-central-integration-app-on-tradeshift"></a>Að tengjast við forrit Business Central Integration í Tradeshift

Þú getur stofnað Tradeshift-reikning á fljótlegan hátt og hafist handa með forrit Business Central Integration á síðunni **Uppsetning Doc. Exch. þjónustu**. Veldu annaðhvort tengilinn **Virkja forrit** í tilkynningunni eða reitinn **Vefslóð forrits** til að fara í forritið í Tradeshift App Store. Á innskráningarsíðunni fyrir Tradeshift getur þú annaðhvort skráð þig inn eða nýskráð þig.

> [!NOTE]
> Eftir að þú skráir þig inn á Tradeshift-reikninginn þinn gæti verið að vefsvæðið fari ekki með þig á síðuna þar sem þú virkjar forritið. Til að gera það er hægt að smella aftur á tengilinn á síðunni **Uppsetning Doc. Exch. þjónustu** í Business Central til að fara beint í forritið.

Ef þú ákveður að hætta að nota Business Central Integration ættir þú að gera það óvirkt í Tradeshift App Store. 

## <a name="to-connect-to-a-document-exchange-service"></a>Að tengjast við skjalaskiptaþjónustu

Ef þú kýst að nota aðra skjalaskiptaþjónustu verður þú að veita upplýsingar til að tengjast þjónustunni.

1. Veldu ![Ljósaperuna sem opnar eiginleika Viðmótsleitar](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, sláðu inn **Uppsetning skjalaskiptaþjónustu** og veldu síðan tengda tengilinn.  
2. Fylla inn í reitina eins og lýst er í eftirfarandi töflu.  

    |Svæði|Description|  
    |---------------------------------|---------------------------------------|  
    |**Notandagerandi**|Færa inn texta sem hægt er að nota til að auðkenna fyrirtækið í skjalaskiptaferlinu.|  
    |**Virk**|Tilgreindu hvort tengingin við þjónustuna sé virk.<br><br> **Athugið:** Þegar þjónustan er virkjuð eru a.m.k. tvær verkraðarfærslur stofnaðar til að senda og taka á móti rafrænum skjölum. Þegar þú slekkur á þjónustu er verkraðarfærslum eytt.|  
    |**Sandbox**|Tilgreindu hvort þú ert að tengjast við sandkassaútgáfu skjalaskiptaþjónustunnar.|
    |**Vefslóð skráningar**|Tilgreina vefsíðuna þar sem nýskráning fyrir skjalskiptiþjónustuna fer fram.|  
    |**Vefslóð forrits**|Veldu tengilinn til að opna forritsverslunina og kveiktu eða slökktu á Business Central Integration.|
    |**Vefslóð þjónustu**|Tilgreina veffang skjalaskiptiþjónustunna sem verður kölluð þegar rafræn skjöl eru send og tekið við þeim.|  
    |**Innskráningarvefslóð**|Tilgreindu vefslóð fyrir síðuna sem þú notar til að skrá þig inn á skjalaskiptaþjónustuna. Þetta er síðan þar sem notandanafn og aðgangsorð fyrirtækisins er slegið inn.|  
    
    > [!NOTE]  
    > Innskráningarupplýsingar þínar eru sjálfkrafa dulritaðar. Ekki er hægt að slökkva á dulritun.

    > [!NOTE]
    > Ef þú getur ekki tengst skjalaskiptaþjónustunni vegna vandamála með heimild gæti það verið vegna þess að [!INCLUDE[prod_short](includes/prod_short.md)] getur ekki sjálfkrafa endurnýjað aðgangslykilinn. Þetta getur til dæmis átt sér stað ef þú hefur ekki notað þjónustuna í einhvern tíma. Þú getur endurnýjað lykilinn handvirkt með því að nota aðgerðina **Endurnýja lykil**.

## <a name="settings-for-business-central-on-premises"></a>Stillingar fyrir Business Central á staðnum

Til að tengjast Business Central á staðnum þarf að búa til forrit í Tradeshift App Store. Þegar það er gert skal nota vefslóð framsendingar úr reitnum **Framsendingarvefslóð** á síðunni **Uppsetning skjalaskiptaþjónustu**. Eftir að þú hefur skráð forritið þitt mun Tradeshift útvega biðlarakenni og leyniorði biðlara. Í [!INCLUDE[prod_short](includes/prod_short.md)] skal færa inn þessi gildi í flýtiflipann **Heimild** á síðunni **Uppsetning skjalaskiptaþjónustu**.

Ef þú kýst frekar að geyma forritskennið og leynilykilinn á annarri staðsetningu, geturðu skilið reiti biðlarakennis og leynilykils biðlara eftir auða og skrifað viðbót til að sækja auðkennið og leynilykilinn frá staðsetningunni. Hægt er að gefa upp leynilykilinn við keyrslu með því að gerast áskrifandi að tilvikum OnGetClientId og OnGetClientSecret í codeunit 1410 „Stjórnun skjalaskiptaþjónustu“.

## <a name="see-related-training-at-microsoft-learn"></a>Sjá tengdar þjálfun hjá [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Sjá einnig

[Setja upp gagnaskipti](across-set-up-data-exchange.md)  
[Rafræn gagnaskipti](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]